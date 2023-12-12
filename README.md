# weeklyimport os
from datetime import datetime, timedelta

# 设置周报文件夹的路径
weekly_report_dir = "path/to/your/weekly_reports"

# 获取当前日期和上周的日期
current_date = datetime.now()
last_week_date = current_date - timedelta(days=7)

# 格式化日期为 YYYY-MM-DD 格式
current_date_str = current_date.strftime('%Y-%m-%d')
last_week_date_str = last_week_date.strftime('%Y-%m-%d')

# 周报文件的名称
report_filename = f"Weekly_Report_{last_week_date_str}_to_{current_date_str}.md"

# 周报的完整路径
report_filepath = os.path.join(weekly_report_dir, report_filename)

# 创建并写入周报内容
with open(report_filepath, 'w') as report_file:
    report_file.write(f"# 周报 {last_week_date_str} - {current_date_str}\n\n")
    report_file.write("## 本周完成的任务\n\n")
    report_file.write("- 任务1\n")
    report_file.write("- 任务2\n")
    report_file.write("- 任务3\n\n")
    report_file.write("## 下周计划的任务\n\n")
    report_file.write("- 计划任务1\n")
    report_file.write("- 计划任务2\n")
    report_file.write("- 计划任务3\n")

print(f"周报已创建: {report_filepath}")
