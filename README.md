# Python Useful Module

常用 Python 小功能合集，封装成易于复用的工具模块。

## 📦 安装

```bash
# 克隆仓库
git clone https://github.com/Rockelbel/python_useful_module.git

# 直接使用
from python_useful_module import utils
```

## 🛠️ 工具模块

### 文件操作 (file_utils.py)

| 函数 | 功能 |
|------|------|
| `read_json()` | 读取 JSON 文件 |
| `write_json()` | 写入 JSON 文件 |
| `ensure_dir()` | 确保目录存在 |
| `get_file_size()` | 获取文件大小（友好格式） |

### 时间日期 (time_utils.py)

| 函数 | 功能 |
|------|------|
| `now_str()` | 获取当前时间字符串 |
| `timestamp()` | 获取当前时间戳 |
| `format_duration()` | 格式化时间间隔 |
| `parse_date()` | 解析日期字符串 |

### 数据转换 (data_utils.py)

| 函数 | 功能 |
|------|------|
| `chunk_list()` | 列表分块 |
| `unique()` | 去重保持顺序 |
| `flatten()` | 扁平化嵌套列表 |
| `safe_get()` | 安全获取字典值 |

### 字符串处理 (string_utils.py)

| 函数 | 功能 |
|------|------|
| `slugify()` | 转换为 URL 友好格式 |
| `truncate()` | 截断字符串 |
| `camel_to_snake()` | 驼峰转下划线 |
| `snake_to_camel()` | 下划线转驼峰 |

## 💡 使用示例

```python
from utils.file_utils import read_json, write_json
from utils.time_utils import now_str, format_duration
from utils.data_utils import chunk_list, unique

# 读取/写入 JSON
data = read_json('config.json')
write_json('output.json', data)

# 时间处理
print(now_str())  # 2024-01-15 10:30:45
print(format_duration(3661))  # 1小时1分1秒

# 数据处理
items = [1, 2, 2, 3, 3, 3]
print(unique(items))  # [1, 2, 3]

chunks = chunk_list([1,2,3,4,5], 2)
print(chunks)  # [[1,2], [3,4], [5]]
```

## 📁 项目结构

```
python_useful_module/
├── utils/
│   ├── __init__.py
│   ├── file_utils.py
│   ├── time_utils.py
│   ├── data_utils.py
│   └── string_utils.py
├── tests/
│   └── test_utils.py
├── README.md
└── setup.py
```

## 🚀 计划添加

- [ ] 网络请求工具 (http_utils.py)
- [ ] 缓存工具 (cache_utils.py)
- [ ] 正则工具 (regex_utils.py)
- [ ] Excel/CSV 处理 (excel_utils.py)
- [ ] 日志工具 (log_utils.py)

## 🤝 贡献

欢迎提交 PR 添加更多实用工具函数。

## 📄 许可证

MIT License
