[html.index.txt](https://github.com/user-attachments/files/24857858/html.index.txt)
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Many Circles | ������ �������</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://www.gstatic.com/firebasejs/8.10.0/firebase-app.js"></script>
    <script src="https://www.gstatic.com/firebasejs/8.10.0/firebase-database.js"></script>
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;700;900&display=swap" rel="stylesheet">
    <style>
        body { font-family: 'Cairo', sans-serif; background-color: #f8fafc; }
        .circle-bg { background-image: radial-gradient(#3b82f6 0.5px, transparent 0.5px); background-size: 30px 30px; }
        .glass { background: rgba(255, 255, 255, 0.85); backdrop-filter: blur(10px); border: 1px solid rgba(255, 255, 255, 0.3); }
        .hidden { display: none; }
    </style>
</head>
<body class="circle-bg min-h-screen flex items-center justify-center p-4">

    <div id="roleScreen" class="w-full max-w-md glass p-8 rounded-[2.5rem] shadow-2xl transition-all">
        <div class="text-center mb-10">
            <div class="w-24 h-24 mx-auto bg-blue-600 rounded-full flex items-center justify-center shadow-xl mb-4 border-4 border-white overflow-hidden">
                <span class="text-white text-3xl font-black">MC</span>
            </div>
            <h1 class="text-3xl font-black text-slate-800 tracking-tight">Many Circles</h1>
            <p class="text-slate-500 mt-2 font-medium">���� ����� �������� ��������</p>
        </div>

        <div class="space-y-4">
            <button onclick="showSection('admin')" class="w-full flex items-center p-5 bg-white hover:bg-blue-600 group rounded-3xl transition-all shadow-sm border border-slate-100">
                <div class="bg-blue-100 text-blue-600 p-3 rounded-2xl group-hover:bg-blue-400 group-hover:text-white transition-colors text-2xl">??</div>
                <div class="mr-4 text-right">
                    <h2 class="font-bold text-slate-800 group-hover:text-white transition-colors">����� ������</h2>
                    <p class="text-xs text-slate-400 group-hover:text-blue-100 transition-colors">����� �������� �������� ������</p>
                </div>
            </button>

            <button onclick="showSection('teacher')" class="w-full flex items-center p-5 bg-white hover:bg-emerald-600 group rounded-3xl transition-all shadow-sm border border-slate-100">
                <div class="bg-emerald-100 text-emerald-600 p-3 rounded-2xl group-hover:bg-emerald-400 group-hover:text-white transition-colors text-2xl">??�??</div>
                <div class="mr-4 text-right">
                    <h2 class="font-bold text-slate-800 group-hover:text-white transition-colors">����� ��������</h2>
                    <p class="text-xs text-slate-400 group-hover:text-emerald-100 transition-colors">����� ������ ���������</p>
                </div>
            </button>

            <button onclick="showSection('parent')" class="w-full flex items-center p-5 bg-white hover:bg-amber-500 group rounded-3xl transition-all shadow-sm border border-slate-100">
                <div class="bg-amber-100 text-amber-600 p-3 rounded-2xl group-hover:bg-amber-400 group-hover:text-white transition-colors text-2xl">??</div>
                <div class="mr-4 text-right">
                    <h2 class="font-bold text-slate-800 group-hover:text-white transition-colors">������ ������</h2>
                    <p class="text-xs text-slate-400 group-hover:text-amber-50 transition-colors">������ ������� ��������</p>
                </div>
            </button>
        </div>
    </div>

    <script>
        // ��� ������ Firebase ������ ��
        const firebaseConfig = {
            apiKey: "AIzaSyC4K55wOZy3w44cCNX1i_cmk4-g4P-L40",
            authDomain: "many-circles.firebaseapp.com",
            databaseURL: "https://many-circles-default-rtdb.firebaseio.com",
            projectId: "many-circles",
            storageBucket: "many-circles.firebasestorage.app",
            messagingSenderId: "905475370717",
            appId: "1:905475370717:web:587b788750f31a1d26f534"
        };
        firebase.initializeApp(firebaseConfig);
        const db = firebase.database();

        function showSection(role) {
            alert("�� ��� " + role + " ������ ��������. ������� ����� ���� ������.");
            // ����� �� ������ ������� ����� ����� ������ ��� �����
        }
    </script>
</body>
</html>
