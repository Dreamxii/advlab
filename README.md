import yt_dlp  บรรทัดนี้เป็นการ import ไลบรารี yt_dlpสำหรับดาวน์โหลดวิดีโอหรือเสียงจาก YouTube และเว็บไซต์อื่นๆต้องติดตั้ง yt-dlp ก่อนใช้:
def download_youtube_video(url, save_path=".") เป็นการกำหนดชื่อฟังก์ชัน download_youtube_video สำหรับใช้ ดาวน์โหลดวิดีโอจาก URL ที่ให้มา
 ydl_opts = {
        'outtmpl': f'{save_path}/%(title)s.%(ext)s',
        'format': 'best',
        'noplaylist': True,
        'quiet': False,
        'no_warnings': True,
         }                       : เป็นการตั้งค่าการดาวน์โหลดต่างๆ เช่น  'format': 'best', คือดาวน์โหลดวิดีโอคุณภาพดีที่สุดที่มี
         except Exception as e:
        print(f"An error occurred: {e}")  ถ้ามีข้อผิดพลาด (เช่น URL ผิด หรือปัญหาเน็ต) จะจับ error แล้วพิมพ์ข้อความออกมา
