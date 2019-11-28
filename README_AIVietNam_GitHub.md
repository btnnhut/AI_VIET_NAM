# NHỮNG LỆNH COMMAND CĂN BẢN VỀ Git và GitHub

<a name="mucluc"></a>
## [MỤC LỤC](#mucluc)
---
- [I. Giới thiệu](#gioithieu)
	- [1. Git là gi ?](#gitlagi)
	- [2. Github](#github)
	- [3. Chú thích](#chuthich)
	- [4. Tài liệu tham khảo](#tailieuthamkhao)

- [II. Git và GitHub](#gitvagithub)
	-	[1. Cài đặt và cấu hình](#caidatvacauhinh)
	-	[2. Một số lệnh git thông dụng](#motsolenhgitthongdung)
		-	[2.1 git remote add](#gitremoteadd)
		-	[2.2 git config --list](#gitconfig--list)
		-	[2.3 git pull](#gitpull)
		-	[2.4 git clone](#gitclone)
		-	[2.5 git status](#gitstatus)
		-	[2.6 git add](#gitadd)
		-	[2.7 git commit](#gitcommit)
		-	[2.8 git push](#gitpush)
		-	[2.9 git log](#gitlog)
		-	[2.10 git branch](#gitbranch)
		-	[2.11 git reset](#gitreset)
		-	[2.12 git branch](#gitbranch)
		-	[2.13 branch remote](#branchremote)
		-	[2.14 git stash](#gitstash)
		-	[2.15 git rebase](#gitrebase)

- [III. Tổng kết](#tongket)
- [IV. Liên hỗ trợ tốt](#lienhotrotot)
<a name="gioithieu"></a>

<br />

## I. Giới thiệu

---

Git và Github được sử dụng khá phổ biến trong giới lập trình viên, có nhiều kho mã nguồn có link từ [github.com](https://github.com). Nó rất tiện lợi và an toàn, đáp ứng tốt các nhu cầu làm việc nhóm. Để sử dụng Git và Github bạn cần có những kiến thức cơ bản dòng lệnh trên Linux (Vì Git được xây dựng trên Linux)

<a name="gitlagi"></a>

### 1. Git là gì ?

---

Git là một hệ thống quản lý phiên bản phân tán (Distributed Version Control System - DVCS)

<a name="github"></a>

### 2. Github

---

Github là một dịch vụ máy chủ repository để mọi lập trình viên có thể tạo tài khoản, nhằm tạo ra các repository github lưu trữ các project của nhóm.

<a name="chuthich"></a>

### 3. Chú thích

---

Bài viết này được thực hiện trên os window

1. Repository local: repository tại máy.
2. Repository git: repository trên [github.com](https://github.com).

<a name="tailieuthamkhao"></a>

### 4. Tài liệu tham khảo

---

- [Trang chủ git](https://git-scm.com)
- [Trang chủ github](https://github.com/)
- [Ebook về git tiếng Viêt](https://git-scm.com/book/vi/v1/B%E1%BA%AFt-%C4%90%E1%BA%A7u)
- [Ebook về git tiếng English](https://git-scm.com/book/en/v2/Getting-Started-About-Version-Control) **(nên đọc)**

<a name="gitvagithub"></a>

<br />

## II. Git và Github

---

<a name="caidatvacauhinh"></a>

### 1. Cài đặt và cấu hình git:

---

**Cài đặt git trên window**
Vào trang  [https://git-scm.com/download/win](https://git-scm.com/download/win) down về và tiến hành cài đặt trên window.
**Thiết lập repository local**
Tạo một Folder và dùng command cd đến Folder mới tạo, gõ lệnh sau để thiết lập repository local.
````
git init
````

<img src = https://i.imgur.com/w5T079z.png>

> Hiện lên như hình trên là thành công.
> Lệnh `git init` thiết lập cấu hình một repository local.

**Thiết lập email và name trong repository local**

````
git config --global user.email "email tài khoản github"
git config --global user.name "user github"
````
Hoặc 
```
git config user.email "email tài khoản github"
git config user.name "user github"
```

<img src=https://i.imgur.com/9qyFtlj.png>

> Thiết lập thông tin email và name config của repository local:

<a name="motsolenhgitthongdung"></a>

### 2. Một số lệnh git thông dụng

---

Tạo tài khoản trên [https://github.com](https://github.com) và tạo một repository github
Sau khi tạo tài khoản trên [https://github.com](https://github.com) ,  tìm hiểu về các lệnh căn bản sau:

<a name="gitremoteadd"></a>

- **2.1 git remote add**

````
git remote add origin <repository_github>
````

<img src=https://imgur.com/CigMVI8.png>

> Lệnh `git remote add` dùng để tạo liên kết giữa repository local và repository github.

Để xem tất cả những nối kết nối đến repository github:

```
git remote -v
```

<img src=https://i.imgur.com/ndEmG6I.png>

Để xóa một liên kết đến repository gihub:

```
git remote remove origin
```

<img src=https://i.imgur.com/e7Y5kB4.png>

Để thay đổi origin url

```
git remote set-url origin <repository_github>
```

Thêm remote:

```
git remote add remote_name <repository_github>
```

<a name="config--list"></a>

- **2.2 git config --list**

````
git config --list
````
<img src=https://imgur.com/gQbnibo.png>

> Lệnh dùng xem những thiết lập tại repository local, như hình trên ta thấy đã cấu hình email, name và liên kết đến 1 repository git.
> Đây là những cấu hình căn bản trong config để thực hiện một số lệnh tiếp theo.

<a name="gitpull"></a>

- **2.3 git pull**

````
git pull origin master
````

<img src=https://imgur.com/jOhbdrq.png>

> Lệnh `git pull` dùng để cập nhật những thay đổi từ repository github về repository local

<a name="gitclone"></a>

- **2.4 git clone**

````
git clone <repository github>
````

> Lệnh `git clone` copy một bản từ repository github về repository local

<a name="gitstatus"></a>

- **2.5 git status**

 ````
git status
 ````

<img src=https://imgur.com/8AeqaXi.png>

 > Lệnh `git status` xem trạng thái hiện tại của repository local. Thấy có một file mới trong repository local, để cập nhật những thay đổi ta dùng lệnh sau `git add`

```
git diff
```

> Xem những thay đổi, nhưng chưa ```add``` của những file hiện tại.

```
git diff --cached
```

> Xem thay đổi đã được ```add``` chưa ```commit``` của những file hiện tại.

```
git diff origin/master
```

> Xem thay đổi giữa local và master

```
git diff commit1_id commit2_id
```

> Xem thay đổi giữa hai commit

```
git diff --name-only commit1_id commit2_id
```

> Xem những files thay đổi giữa hai commits.

```
git diff-tree -no-commit-id --name-only -r commit_id
git show --pretty="format:" --name-only commit_id
```

> Xem những file thay đổi tại một commit bất kỳ

```
git diff --cached origin/master
```

> Xem thay đổi trước khi push

```
git show commit_id
```

> Xem thông tin cụ thể của một commit

<a name="gitadd"></a>

- **2.6 git add**

````
git add *
````
<img src=https://i.imgur.com/jzMLaNE.png>

> Lệnh `git add *` cập nhật tất cả những thay đổi, hoặc dùng 
````
git add <tên đầy đủ file>
````
> Chỉ cập nhật những file được chỉ định. Dùng lệnh `git status` xem kết quả

<img src=https://i.imgur.com/TrMGlZU.png>

<a name="gitcommit"></a>

- **2.7 git commit**

````
git commit -m <đặt tên commit>
````
<img src=https://i.imgur.com/rKgFF4d.png>

> Cập nhật những thay đổi đã thực hiện từ lệnh `git add`.
> Khi thực hiện `git commit` xong, thì mới cập nhật những thay đổi từ repository local lên repository github bằng lệnh `git push`

<a name="gitpush"></a>

- **2.8 git push**

````
git push origin master
````
Hoặc

```
git push -f origin master
```

<img src=https://i.imgur.com/Cq9mTkH.png>

> Lệnh `git push` cập nhật những thay đổi branch từ repository local đã được `git commit` lên repository github
>
> Tham số ```-f``` cập nhật bắt buột lên repository github
> 
> Lần đầu thực hiện sẽ hỏi username (tên tài khoản github muốn đẩy lên), và password tài khoản. Khi gõ password sẽ không hiện lên bất kỳ gì cả cứ gõ binh thường rồi enter.

hoặc

```
git push origin <local_branch>:<remote_branch>
```

> Dùng để push branch với một tên khác.


<a name="gitlog"></a>

-	**2.9 git log**

````
git log
````
<img src=https://i.imgur.com/yDyYlsl.png>

> Liệt kê những commit đã thực hiện tại repository local. Liệt kê chi tiết những commit đã thực hiện dùng lệnh sau:
````
git log -p
````

> Để thoát màn hình `git log -p` dùng phím `q`

```
git log-2
```

> Xem commit history cho hai commit gần nhất

```
git log -p -2
```

> Xem commit history cho hai commit gần nhất, bao gồm cả thay đổi

```
git log --pretty=oneline
```

> Xem commit history dưới dạng một dòng

<a name="gitbranch"></a>

- **2.10 git branch**

````
git branch
````
<img src=https://i.imgur.com/A3eAwRc.png>

> Kiểm tra mình đang ở branch nào ? Như hình là đang ở master

<a name="gitreset"></a>

- **2.11 git reset**

````
git reset --hard <commit-ish>
````
> Trở về một commit bất kỳ.

<a name="gitbranch"></a>

- **2.12 git branch**

```
git branch -d <name_branch>
```

Xóa name_branch nếu chưa được merge thì sẽ hiện thông báo lỗi là chưa được merge vào branch nào. Thay ```-d``` bằng ```-D``` sẽ xóa branch bất kể branch chưa được merge.

> Xóa nhiều branch bằng cách thêm nhiều tên branch ở cuối lệnh và cách nhau bằng một khoảng trắng.

<a name="branchremote"></a>

- **2.13 branch remote:**

```
git push --delete <name_remote> <name_branch>

git push <name_remote> --delete <name_branch>
```

> Tương tự xóa xóa nhiều branch, thêm tên branch ở cuối lệnh và cách nhau bằng một khoảng trắng.

<a name="gitstash"></a>

- **2.14 git stash**

```
git stash save
git stash
```

> Lưu lại toàn bộ công việc đang làm, sử dụng bao nhiêu lần tùy thích.

````
git stash list
````

> Xem lại danh sách các lần lưu thay đổi. Muốn xem cả nội dung của từng thay đổi ```git stash list -p```

```
git stash show stash@{1}
```

> Xem nội dung cụ thể hơn nữa của lần thay đổi thứ 1.

```
git stash apply stash@{1}
```

> Để tiếp tục làm việc tại ```stash``` số 1.

```
git stash drop stash@{1}
git stash pop stash@{1}
``` 

> Để xóa một stash cụ thể đã lưu.

```
git stash clear
```

> Xóa tất cả toàn bộ stash.

<a name="gitrebase"></a>

- **2.15 git rebase**

```
git rebase --interactive <commit_end_id>
git rebase -i <commit_end_id>
```

> Để gộp một nhóm commit thành 1 commit duy nhất, ```<commit_end_id>``` là id của commit cuối trong nhóm cần gộp

> * Mẹo: để xóa tất cả commit trong một git chỉ cần xóa Folder ```.git```
>
> * Tiếp theo [cấu hình lại git](#caidatvacauhinh)
>
> * Sau đó dùng ```git push -f origin master``` để cập nhật mới hoàn toàn

<br />

<a name="tongket"></a>

<br />

## III. Tổng kết

---

>Bài viết này mình tóm tắt lại những kiến thức thu được khi sử dụng git và github. Đây là tài liệu để mình tham khảo trong tương lai. Đồng thời hy vọng bài này có ích cho những bạn mới tìm hiểu về git và github. 
><br />
>>Để tìm hiểu kỹ hơn, có thể tham khảo nguồn sau:<br />
>> [https://github.com/hocchudong](https://github.com/hocchudong/git-github-for-sysadmin/blob/master/README.md)<br />
>>[https://github.com/hprobotic/git-tips](https://github.com/hprobotic/git-tips)<br />
>>Link tham gia [AI VIET NAM](https://aivietnam.ai/courses/aisummer2019/lessons/gioi-thieu-ve-khoa-hoc/)<br />

<a name="lienhotrotot"></a>

<br />

## IV. Liên hỗ trợ tốt

---

-Edit Markdown web 1: [https://stackedit.io](https://stackedit.io/)
