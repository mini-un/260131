[index.html](https://github.com/user-attachments/files/24990741/index.html)
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <title>무엇이든 먹어보살</title>
    <style>
        /* [CSS] 전체 스타일 */
        body {
            background-color: #f8f9fa;
            font-family: 'Pretendard', sans-serif;
            text-align: center;
            padding-top: 1px;
            margin: 0;
        }

        h1 { color: #333; margin-bottom: 10px; }
        .description { color: #666; margin-bottom: 30px; }

        /* [CSS] 버튼 그룹 */
        .button-group {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin-bottom: 50px;
        }

        .btn {
            padding: 12px 24px;
            font-size: 16px;
            font-weight: bold;
            color: white;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            transition: 0.3s;
        }

        .btn-blue { background-color: #3498db; }
        .btn-green { background-color: #2ecc71; }
        .btn-orange { background-color: #e67e22; }
        .btn-yellow { background-color: #ffd700; color: #333; }

        .btn:hover { transform: translateY(-3px); box-shadow: 0 5px 15px rgba(0,0,0,0.1); opacity: 0.8; }

        /* -------------------------------------------------- */
        /* [CSS] 절대 좌표 배치를 위한 설정 영역 */
        /* -------------------------------------------------- */
        
        .position-area {
            position: relative;   /* 자식(사진)들의 기준점이 됩니다 */
            width: 100%;          /* 화면 전체 너비 사용 */
            height: 600px;        /* 사진들이 배치될 넉넉한 높이 */
            margin-top: 20px;
        }

        .position-area img {
            position: absolute;   /* 기준점을 바탕으로 자유롭게 배치 */
            width: 380px;         /* 사진 크기 조절 */
            height: 280px;
            object-fit: cover;
            border-radius: 12px;
            box-shadow: 0 10px 20px rgba(0,0,0,0.15);
            transition: 0.3s;
        }

        /* 각 사진의 위치 지정 (원하는 대로 수정하세요!) */
        /* top: 위에서부터 거리, left/right: 왼쪽/오른쪽에서부터 거리 */
        .img1 { top: 20px;  left: 10%; transform: rotate(-5deg); }
        .img2 { top: 150px; left: 30%; transform: rotate(8deg); z-index: 2; }
        .img3 { top: 25px;  right: 30%; transform: rotate(-10deg); }
        .img4 { top: 120px; right: 10%; transform: rotate(8deg); z-index: 2; }

        .position-area img:hover {
            transform: scale(1.1) rotate(0deg); /* 마우스 올리면 커지고 똑바로 서기 */
            z-index: 10; /* 겹쳐있어도 맨 위로 올라오게 함 */
        }
    </style>
</head>
<body>

    <h1>무엇이든 골라보살</h1>
    <p class="description">지금 메뉴가 고민된다면? 버튼을 눌러보시게나</p>

    <div class="button-group">
        <button class="btn btn-blue" onclick="window.open('https://www.google.com')">한식</button>
        <button class="btn btn-green" onclick="window.open('https://www.naver.com')">양식</button>
        <button class="btn btn-orange" onclick="window.open('https://www.youtube.com')">중식</button>
        <button class="btn btn-yellow" onclick="window.open('https://www.youtube.com')">일식</button>
    </div>

    <div class="position-area">
        <img src="bg1.jpg" alt="음식사진1" class="img1">
        <img src="bg2.jpg" alt="음식사진2" class="img2">
        <img src="bg3.jpg" alt="음식사진3" class="img3">
        <img src="bg4.jpg" alt="음식사진4" class="img4">
    </div>

</body>
</html>
