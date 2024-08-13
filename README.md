import time

# Convert the timer to seconds

Total_time = 15 * 60

# Timer countdown
for remaining in range(total_time, 0, -1):
    minutes, seconds = divmod(remaining, 60)
    if remaining > 60:
        color = "\033[93m"  # オレンジ
    else:
        color = "\033[91m"  # 赤
    print(f"{color}{minutes:02}:{seconds:02}\033[0m", end="\r")
    time.sleep(1)

print("\033[91m00:00\033[0m")  # タイマー終了時
