# CC-VM

# C4 — Procedure to Transfer Two Text Files from One Virtual Machine to Another Virtual Machine

## Step 1 — Create Text Files in VM1

```bash
echo "This is File 1" > file1.txt
echo "This is File 2" > file2.txt
```

---

## Step 2 — Display Files Before Transfer in VM1

```bash
cat file1.txt
cat file2.txt
```

---

## Step 3 — Add Some Text in Both Files

```bash
echo "Added text in File 1" >> file1.txt
echo "Added text in File 2" >> file2.txt
```

---

## Step 4 — Display Updated Files in VM1

```bash
cat file1.txt
cat file2.txt
```

---

## Step 5 — Transfer Files from VM1 to VM2

```bash
scp file1.txt vagrant@VM2_IP:/home/vagrant/
scp file2.txt vagrant@VM2_IP:/home/vagrant/
```

---

## Step 6 — Connecting

```bash
yes
```

---

## Step 7 — Display Files After Transfer in VM2

```bash
cat file1.txt
cat file2.txt
```

---

# List All Files Present in Both VMs

## In VM1

```bash
ls
```

## In VM2

```bash
ls
```
---
## NOTE- If "Connection Refused"

```bash
sudo apt update
sudo apt install openssh-server -y
sudo systemctl start ssh
```
