On branch main
Your branch is up to date with 'origin/main'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        part1/
        status_log.md

nothing added to commit but untracked files present (use "git add" to track)
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   part1/notes.txt
        new file:   part1/todo.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        part1/draft.md
        status_log.md
diff --git a/part1/notes.txt b/part1/notes.txt
index e69de29..064de99 100644
--- a/part1/notes.txt
+++ b/part1/notes.txt
@@ -0,0 +1,3 @@
+Nguyen Xuan Thanh
+B25DCTN110
+D25CTTN01-B
\ No newline at end of file
git fetch: Tải dữ liệu và lịch sử commit mới từ remote về máy tính, nhưng không thay đổi code trong thư mục làm việc hiện tại.
git pull: Bản chất là git fetch cộng với git merge. Nó vừa tải dữ liệu về, vừa tự động gộp (merge) dữ liệu đó vào nhánh hiện tại đang làm việc.