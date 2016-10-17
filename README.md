### Generate default config
### ranger --copy-config=all

### Insert to end of file ~/.config/ranger/rc.conf
```
set sort_case_insensitive True
set sort_directories_first True
set draw_borders True
set scroll_offset 10
set column_ratios 1,3,3
set dirname_in_tabs True
set preview_directories True
set show_cursor True
set use_preview_script True
set preview_files True
set collapse_preview True
set padding_right True

map <C-a> console scout -pstg%space
map ff shell echo -n %f | xclip -selection primary && echo -n %f | xclip -selection clipboard
map fd shell echo -n %d/%f | xclip -selection primary && echo -n %d/%f | xclip -selection clipboard
map fc shell xclip -selection primary %f && xclip -selection clipboard %f
map f+ shell -s chmod +x %s
map f- shell -s chmod -x %s
map <F2> console rename %f

map df flat -1
map ddf flat 0
```
