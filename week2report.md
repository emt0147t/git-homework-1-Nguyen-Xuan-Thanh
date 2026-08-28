PART A
#Em sử dụng nhanh 'main' thay cho 'master'
1.
git checkout main
touch week2.md
git add week2.md
git commit -m"Add week2.md file"
git checkout -b week2
2.
touch file1.txt
git add file1.txt
git commit -m "working1"
touch file2.txt
git add file2.txt
git commit -m "working2"
3.
echo "Dong noi dung o nhanh week2" >> week2.md
git add week2.md
git commit -m "Update week2.md on branch week2"
git checkout main
echo "Khi chuyển sang nhánh main, nội dung đã thêm ở nhánh week2 không hiển thị. Git giữ cho thư mục làm việc của mỗi nhánh độc lập hoàn toàn với nhau."
git add week2.md
git commit -m "Document findings about branch separation"
4.
git checkout -b week2b
git merge week2
Xóa các dòng xung đột <<<<<<<,======,>>>>>>> và lưu
git add week2.md
git commit -m "Merge week2 into week2b using 3-way merge"
git branch -d week2

PART B
1.
git checkout -b wip
touch wip.txt
git add wip.txt
git commit -m "Add wip.txt"
git checkout main
git merge week2b
2.
git branch --merged
git branch --no-merged
3.
git branch -d week2b
4.
git branch -m wip work-in-progress
git push -u origin work-in-progress
PART C
1.
git checkout work-in-progress
echo "Them noi dung de test" >> wip.txt
git commit -a -m "Update wip.txt"
2.
git branch -vv
3.
git push origin work-in-progress
PART D
1.
git checkout main
git checkout -b experiment
touch exp1.txt
git add exp1.txt
git commit -m "Commit 1 on experiment"
touch exp2.txt
git add exp2.txt
git commit -m "Commit 2 on experiment"
2.
git checkout main
touch main1.txt
git add main1.txt
git commit -m "Commit on main"
3.
git checkout experiment
git rebase main
4.
echo "Lệnh Rebase cất các commit của nhánh experiment, cập nhật nhánh này bắt đầu từ commit mới nhất của main, rồi đắp các commit đã cất lên trên cùng để tạo thành 1 đường thẳng." >> week2.md
git add week2.md
git commit -m "Explain rebase in week2.md"
5.
git checkout main
git merge experiment
6.
git push origin main