### 扩展VM的内存：
```bash
# 启动一个 4核 10G内存 10G硬存的 VM
colima start --cpu 4 --memory 10 --disk 10
```

```bash
# 通过查看临时容器的RAM 确认配置生效
docker run --rm "debian:bullseye-slim" bash -c 'numfmt --to iec $(echo $(($(getconf _PHYS_PAGES) * $(getconf PAGE_SIZE))))'
```

输出：
```bash
9.8G
```

