# 💻 Basit Kabuk (Shell) Uygulaması - C | Simple Shell in C

## 📌 Proje Açıklaması | Project Description

**TR:**  
Bu proje, C programlama dili ile yazılmış basit bir **komut satırı yorumlayıcısı (shell)** uygulamasıdır. `exec`, giriş/çıkış yönlendirme (`<`, `>`), borulama (`|`) ve arka plan işlemleri (`&`) gibi temel kabuk özelliklerini destekler. Gömülü olarak `cd` komutu da uygulanmıştır. Komutlar ayrıştırılarak sistem çağrıları (`fork`, `execvp`, `pipe`, `dup2`, `open`, `wait`) ile çalıştırılır.

**EN:**  
This project is a simple **command-line shell interpreter** written in C. It supports core shell features like `exec`, input/output redirection (`<`, `>`), piping (`|`), and background execution (`&`). The `cd` command is also supported. Commands are parsed and executed using low-level system calls such as `fork`, `execvp`, `pipe`, `dup2`, `open`, and `wait`.

---

## 🔧 Desteklenen Özellikler | Supported Features

- 🧠 `exec` ile temel komut çalıştırma (e.g., `ls`, `cat`, `wc`)
- 📥 Giriş yönlendirme: `< input.txt`
- 📤 Çıkış yönlendirme: `> output.txt`
- 🧵 Komut borulama: `ls | sort | uniq`
- ⚙️ Arka planda çalıştırma: `cmd1 & cmd2`
- 📁 `cd` komutu desteği

---

## 📂 Dosyalar | Files

- `my_shell.c` → Shell uygulamasının C kaynak kodu  
- `input.sh` → Test komutlarını içeren örnek script

---

## 🖥️ Derleme ve Çalıştırma | Build & Run

### Derlemek için | To Compile:

```bash
gcc -o my_shell my_shell.c
```

### Shell'i çalıştırmak için | To Run the Shell:

```bash
./my_shell
```

---

## 🧪 Test Komutları | Sample Test Commands

`input.sh` dosyasındaki bazı örnekler:

```bash
ls > y
cat < y | sort | uniq | wc > y1
cat y1
ls | sort | > y2 & cat < y1 | sort | wc > y3
```

Bu komutlar, yönlendirme, borulama ve arka plan yürütmeyi aynı anda test eder.

---

## 📌 Örnek Kullanım | Example Usage

```
$ ls | sort > sorted.txt
$ cat < sorted.txt | uniq | wc > stats.txt
```

---


## 📄 Lisans | License

MIT License

---

## 🎓 Not

Bu shell uygulaması eğitim ve sistem programlama pratiği amacıyla geliştirilmiştir. Gerçek UNIX shell’lerinin tüm işlevselliğini hedeflemez.

> This shell is built for educational purposes and basic system programming practice. It does not aim to replicate full UNIX shell behavior.
