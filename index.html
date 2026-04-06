<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Nikwe - Ultimate Hub V40</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://unpkg.com/lucide@latest"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Sora:wght@100;400;600;800&display=swap');

        :root {
            --primary: #020617;
            --glass-base: rgba(255, 255, 255, 0.94);
            --field-bg: #f3f4f6;
        }

        body {
            font-family: 'Sora', 'PingFang SC', sans-serif;
            height: 100vh;
            width: 100vw;
            overflow: hidden;
            margin: 0;
            color: var(--primary);
            background-color: #000;
            background-position: center;
            background-size: cover;
            transition: background-image 1.2s ease-in-out;
        }

        /* 极清背景层 */
        #wallpaper-scrim {
            position: fixed;
            inset: 0;
            backdrop-filter: blur(1px) brightness(0.95);
            -webkit-backdrop-filter: blur(1px) brightness(0.95);
            background: rgba(0, 0, 0, 0.03);
            z-index: -1;
            display: none;
        }

        .glass-panel {
            background: var(--glass-base);
            backdrop-filter: blur(40px) saturate(160%);
            -webkit-backdrop-filter: blur(40px) saturate(160%);
            border: 1px solid rgba(255, 255, 255, 0.4);
            box-shadow: 0 40px 100px -20px rgba(0, 0, 0, 0.15);
        }

        .frosted-ai-bar {
            background: rgba(255, 255, 255, 0.5);
            backdrop-filter: blur(30px) saturate(180%) brightness(1.1);
            -webkit-backdrop-filter: blur(30px) saturate(180%) brightness(1.1);
            border: 1px solid rgba(255, 255, 255, 0.8);
            box-shadow: 0 20px 50px rgba(0,0,0,0.1);
        }

        /* 全系统强制统一输入规范 */
        input, textarea, select {
            width: 100% !important;
            height: 50px !important;
            background: var(--field-bg) !important;
            border: 1px solid rgba(0,0,0,0.06) !important;
            border-radius: 16px !important;
            padding: 0 18px !important;
            font-size: 14px !important;
            font-weight: 500 !important;
            color: #1e293b !important;
            outline: none !important;
            transition: all 0.2s cubic-bezier(0.4, 0, 0.2, 1) !important;
            box-shadow: inset 0 2px 4px rgba(0,0,0,0.02) !important;
            font-family: 'Sora', sans-serif !important;
            box-sizing: border-box !important;
        }
        input:focus, textarea:focus, select:focus { background: #fff !important; border-color: #000 !important; box-shadow: 0 0 0 4px rgba(0,0,0,0.04) !important; }
        textarea { height: auto !important; min-height: 110px !important; padding: 15px 18px !important; }

        .brand-logo { display: flex; align-items: center; letter-spacing: -0.06em; font-size: 1.5rem; }
        .brand-nik { font-weight: 800; color: #000; }
        .brand-we { font-weight: 100; color: #94a3b8; margin-left: 1px; }

        .panel-drawer-l { width: 520px; max-width: 100vw; z-index: 900; }
        .panel-drawer-r { width: 440px; max-width: 100vw; z-index: 900; }
        
        /* 核心布局：单容器 Dock 杜绝重叠 */
        .master-dock-bar {
            position: fixed;
            bottom: 30px;
            left: 0;
            width: 100vw;
            padding: 0 30px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            z-index: 800;
            pointer-events: none; 
        }
        .dock-group { display: flex; gap: 12px; pointer-events: auto; }
        
        .dock-icon {
            @apply h-14 w-14 glass-panel rounded-[20px] flex items-center justify-center hover:scale-110 active:scale-95 transition-all shadow-xl cursor-pointer;
        }

        .ai-capsule-container {
            width: 480px;
            max-width: 45vw;
            pointer-events: auto;
        }

        .sw-mini { width: 36px; height: 18px; background: #cbd5e1; border-radius: 100px; position: relative; cursor: pointer; transition: 0.3s; }
        .sw-mini::after { content: ''; position: absolute; top: 2px; left: 2px; width: 14px; height: 14px; background: #fff; border-radius: 50%; transition: 0.3s; }
        .sw-mini.active { background: #000; }
        .sw-mini.active::after { left: 18px; }

        .capsule-color-dot { @apply w-4 h-4 rounded-full cursor-pointer border border-black/5 hover:scale-125 transition-all; }

        @media (max-width: 640px) {
            .master-dock-bar { bottom: 10px; flex-direction: column; height: auto; gap: 10px; padding: 0 10px; }
            .ai-capsule-container { width: 90vw; max-width: 90vw; order: -1; }
            #display-time { font-size: 5rem; }
            .panel-drawer-l, .panel-drawer-r { width: 100vw !important; }
        }

        .chat-scroll::-webkit-scrollbar { width: 4px; }
        .chat-scroll::-webkit-scrollbar-thumb { background: rgba(0,0,0,0.08); border-radius: 10px; }
    </style>
</head>
<body class="relative flex items-center justify-center">

    <div id="wallpaper-scrim"></div>

    <div class="absolute top-10 left-10 select-none z-50 brand-logo">
        <span class="brand-nik">NIK</span>
        <span class="brand-we">WE</span>
    </div>

    <!-- 首页看板 -->
    <main class="text-center z-0 px-6">
        <div id="display-time" class="text-8xl md:text-[10rem] font-thin tracking-tighter mb-4 text-slate-950 select-none">00:00</div>
        
        <div class="flex items-center justify-center gap-6 text-[11px] font-black tracking-[0.5em] uppercase text-slate-950">
            <span id="cur-temp">--°C</span>
            <div id="voice-dot-ui" class="hidden relative">
                <div class="w-2.5 h-2.5 bg-blue-600 rounded-full animate-ping"></div>
            </div>
            <span id="cur-weather">CONNECTING</span>
        </div>

        <div id="display-date" class="text-[13px] uppercase tracking-[0.7em] text-slate-800 mt-5 mb-10 italic font-extrabold">2026 / 04 / 06</div>

        <nav id="home-tiles" class="flex flex-wrap justify-center gap-x-12 gap-y-4 text-[11px] font-black uppercase tracking-widest text-slate-950 hover:text-black transition-all"></nav>
    </main>

    <!-- 统一 Dock 容器 -->
    <div class="master-dock-bar">
        <div class="dock-group">
            <button id="dock-todo" class="dock-icon" title="Objectives"><i data-lucide="calendar"></i></button>
            <button id="dock-notebook" class="dock-icon" title="Notebook"><i data-lucide="book-marked"></i></button>
            <button id="dock-sticky" class="dock-icon" title="Capsules"><i data-lucide="layout-grid"></i></button>
        </div>

        <div class="ai-capsule-container">
            <div class="frosted-ai-bar h-14 flex items-center px-4 gap-3 rounded-[24px] shadow-2xl">
                <i data-lucide="sparkles" class="w-5 h-5 text-slate-400"></i>
                <input type="text" id="ai-input-val" class="!bg-transparent !border-none !shadow-none !h-full !p-0 font-bold" placeholder="询问 AI 或发起指令...">
                <button id="ai-send-btn" class="bg-black text-white w-10 h-10 rounded-xl flex items-center justify-center shrink-0 shadow-lg active:scale-90 transition-all">↑</button>
            </div>
        </div>

        <div class="dock-group">
            <button id="dock-pm" class="dock-icon" title="Private Channel"><i data-lucide="shield-check" class="text-blue-600"></i></button>
            <button id="dock-config" class="dock-icon" title="System Settings"><i data-lucide="settings-2"></i></button>
        </div>
    </div>

    <!-- 面板：待办 -->
    <div id="panel-todo" class="fixed top-0 left-0 h-full panel-drawer-l glass-panel border-r hidden flex-col p-12 animate-in">
        <div class="flex justify-between items-center mb-10 px-2">
            <h2 class="text-3xl font-black italic tracking-tighter uppercase">Objectives</h2>
            <button class="close-all-ui text-slate-300 hover:text-black p-1"><i data-lucide="x"></i></button>
        </div>
        <div class="flex-1 flex flex-col min-h-0">
            <div class="bg-slate-50 p-8 rounded-[2.5rem] border border-slate-100 mb-10 space-y-4">
                <input type="text" id="todo-in-text" class="!bg-transparent !border-none !p-2 !shadow-none font-bold" placeholder="准备做什么？">
                <div class="flex gap-4">
                    <input type="datetime-local" id="todo-time-in" class="flex-1">
                    <button id="todo-add-btn" class="bg-black text-white px-8 rounded-2xl font-bold uppercase text-[10px]">ADD</button>
                </div>
            </div>
            <ul id="todo-render-list" class="space-y-4 overflow-y-auto chat-scroll flex-1 pr-2"></ul>
        </div>
    </div>

    <!-- 面板：笔记本 -->
    <div id="panel-notebook" class="fixed top-0 left-0 h-full panel-drawer-l glass-panel border-r hidden flex-col p-12 animate-in">
        <div class="flex justify-between items-center mb-10 px-2">
            <h2 class="text-3xl font-black italic tracking-tighter uppercase text-slate-950">Notebook</h2>
            <button class="close-all-ui text-slate-300 hover:text-black p-1"><i data-lucide="x"></i></button>
        </div>
        <div class="flex flex-col gap-6 flex-1 min-h-0">
            <div class="flex-none space-y-4">
                <div class="flex items-center justify-between px-2">
                    <label class="text-[9px] font-black uppercase text-slate-400">Current Mood</label>
                    <div id="nb-mood-picker" class="flex gap-3 text-xl">
                        <button class="mood-opt grayscale hover:grayscale-0 transition-all" data-mood="😊">😊</button>
                        <button class="mood-opt grayscale hover:grayscale-0 transition-all" data-mood="😐">😐</button>
                        <button class="mood-opt grayscale hover:grayscale-0 transition-all" data-mood="😴">😴</button>
                        <button class="mood-opt grayscale hover:grayscale-0 transition-all" data-mood="🔥">🔥</button>
                        <button class="mood-opt grayscale hover:grayscale-0 transition-all" data-mood="😢">😢</button>
                    </div>
                </div>
                <textarea id="nb-input" placeholder="开始记录思考..."></textarea>
                <div class="flex gap-3">
                    <button id="nb-save-btn" class="flex-1 bg-black text-white py-5 rounded-2xl font-black text-[11px] uppercase shadow-lg">同步到存档</button>
                    <button onclick="window.open('https://www.kdocs.cn')" class="bg-blue-50 text-blue-600 px-6 rounded-2xl border border-blue-100 flex items-center justify-center hover:bg-blue-100">
                        <i data-lucide="file-text" class="w-5 h-5"></i>
                    </button>
                </div>
            </div>
            <div class="mt-4 flex-1 flex flex-col min-h-0 border-t border-slate-100 pt-8">
                <label class="text-[10px] font-black opacity-30 uppercase tracking-widest block mb-4">ARCHIVE</label>
                <div id="nb-history-render" class="flex-1 overflow-y-auto chat-scroll space-y-5 pr-4 pb-10"></div>
            </div>
        </div>
    </div>

    <!-- 面板：便签 (缩小卡片高度 + 添加表情装饰) -->
    <div id="panel-sticky" class="fixed top-0 left-0 h-full panel-drawer-l glass-panel border-r hidden flex-col p-12 animate-in">
        <div class="flex justify-between items-center mb-12 px-2">
            <h2 class="text-3xl font-black italic tracking-tighter uppercase">Capsules</h2>
            <div class="flex items-center gap-6">
                <button id="sticky-new-trigger" class="bg-black text-white px-8 py-3 rounded-full font-bold text-[10px] shadow-xl">+ NEW</button>
                <button class="close-all-ui text-slate-300 hover:text-black p-1"><i data-lucide="x"></i></button>
            </div>
        </div>
        <div id="sticky-render-grid" class="flex-1 overflow-y-auto chat-scroll space-y-10 pr-4 pb-10"></div>
    </div>

    <!-- 面板：私信 -->
    <div id="panel-pm-view" class="fixed top-0 right-0 h-full panel-drawer-r glass-panel border-l hidden flex-col p-14 animate-in">
        <div class="flex justify-between items-center mb-12">
            <h2 class="text-2xl font-black italic tracking-widest uppercase">Private</h2>
            <button class="close-all-ui text-slate-400 hover:text-black p-1"><i data-lucide="x"></i></button>
        </div>
        <div id="pm-auth-scr" class="flex-1 flex flex-col items-center justify-center p-8 text-center animate-in">
            <div class="w-24 h-24 bg-slate-50 rounded-[3rem] mb-8 flex items-center justify-center text-slate-200 shadow-inner"><i data-lucide="shield-check" class="w-12 h-12"></i></div>
            <input type="text" id="pm-room-id" placeholder="Pairing Room ID" class="text-center mb-6">
            <button id="pm-auth-btn" class="bg-black text-white w-full py-5 rounded-2xl font-bold uppercase text-[11px] shadow-xl">确认建立连接</button>
        </div>
        <div id="pm-active-scr" class="hidden flex-1 flex flex-col animate-in">
            <div id="pm-chat-log" class="flex-1 overflow-y-auto p-4 space-y-4 text-sm italic opacity-30 text-center">信道就绪</div>
            <div class="mt-auto pt-8 border-t border-slate-100">
                <input id="pm-plain-in" placeholder="输入互传内容...">
                <button id="pm-send-trigger" class="w-full mt-4 bg-blue-600 text-white py-4 rounded-xl font-bold text-[11px]">SEND</button>
            </div>
        </div>
    </div>

    <!-- 面板：设置 -->
    <div id="panel-config" class="fixed top-0 right-0 h-full panel-drawer-r glass-panel border-l hidden flex-col p-14 animate-in">
        <div class="flex justify-between items-center mb-10">
            <h2 class="text-2xl font-black italic tracking-widest uppercase text-slate-900">System</h2>
            <button class="close-all-ui text-slate-400 hover:text-black p-1"><i data-lucide="x"></i></button>
        </div>
        <div class="flex-1 overflow-y-auto chat-scroll space-y-10 pr-2">
            <div class="p-8 bg-slate-50/80 rounded-[2.5rem] border border-slate-200 shadow-sm space-y-6">
                <label class="text-[10px] font-black opacity-40 uppercase tracking-widest block">AI Plugins & Engine</label>
                <button id="btn-set-local" class="w-full py-3 bg-blue-50 text-blue-600 rounded-xl text-[10px] font-black uppercase border border-blue-100 hover:bg-blue-100 transition-all mb-4">使用本地大模型预设 (Local LLM)</button>
                <div class="flex items-center justify-between text-xs font-bold border-t border-slate-100 pt-4">
                    <span>实时联网搜索</span>
                    <input type="checkbox" class="w-8 h-4 bg-slate-200 rounded-full appearance-none checked:bg-green-500 transition-all cursor-pointer relative after:content-[''] after:absolute after:top-0.5 after:left-0.5 after:bg-white after:w-3 after:h-3 after:rounded-full checked:after:translate-x-4">
                </div>
                <div class="flex items-center justify-between text-xs font-bold">
                    <span>代码执行环境</span>
                    <input type="checkbox" class="w-8 h-4 bg-slate-200 rounded-full appearance-none checked:bg-green-500 transition-all cursor-pointer relative after:content-[''] after:absolute after:top-0.5 after:left-0.5 after:bg-white after:w-3 after:h-3 after:rounded-full checked:after:translate-x-4">
                </div>
            </div>

            <div class="p-8 bg-slate-100/50 rounded-[2.5rem] border border-slate-100 flex items-center justify-around shadow-sm">
                <div class="flex flex-col items-center gap-2">
                    <span class="text-[9px] font-black uppercase text-slate-400 tracking-widest">Wallpaper</span>
                    <div id="sw-mini-wp" class="sw-mini"></div>
                </div>
                <div class="w-px h-10 bg-slate-200"></div>
                <div class="flex flex-col items-center gap-2">
                    <span class="text-[9px] font-black uppercase text-slate-400 tracking-widest">AI Wake</span>
                    <div id="sw-mini-voice" class="sw-mini"></div>
                </div>
            </div>

            <div class="p-8 bg-slate-50 rounded-[2.5rem] space-y-5 border border-slate-100 shadow-sm">
                <label class="text-[10px] font-black opacity-40 uppercase tracking-widest block text-center">Home Tiles</label>
                <div id="cfg-app-list" class="space-y-3"></div>
                <div class="space-y-3 mt-6">
                    <input id="in-app-name" placeholder="名称">
                    <input id="in-app-url" placeholder="网址 https://...">
                    <button id="btn-add-tile" class="bg-black text-white w-full py-4 rounded-xl font-bold text-[9px] uppercase mt-2 shadow-lg">ADD TO HOME</button>
                </div>
            </div>

            <div class="p-8 bg-slate-50 rounded-[2.5rem] space-y-5 border border-slate-100 shadow-sm">
                <label class="text-[10px] font-black opacity-40 uppercase tracking-widest block text-center">API Backend</label>
                <input id="cfg-ai-base" placeholder="API 地址">
                <input id="cfg-ai-key" type="password" placeholder="API Key">
                <input id="cfg-ai-model" placeholder="模型名称">
            </div>

            <button id="btn-save-all" class="w-full bg-slate-950 text-white py-5 rounded-2xl font-black uppercase text-xs shadow-2xl">同步设置并刷新生效</button>
        </div>
    </div>

    <!-- AI 历史弹出 -->
    <div id="panel-ai-history" class="fixed bottom-28 left-1/2 -translate-x-1/2 w-[520px] max-w-[92vw] h-[500px] glass-panel rounded-[3rem] hidden flex-col p-8 z-[850] shadow-2xl animate-in border border-white">
        <div class="flex justify-between items-center mb-6 px-2">
            <span class="text-[10px] font-black uppercase opacity-20 tracking-widest italic">Conversations</span>
            <button class="close-all-ui text-slate-400 p-1"><i data-lucide="chevron-down"></i></button>
        </div>
        <div id="ai-chat-render" class="flex-1 overflow-y-auto chat-scroll space-y-6 text-[14px]"></div>
    </div>

    <script>
        const $ = id => document.getElementById(id);
        const LS = {
            get: k => JSON.parse(localStorage.getItem('nik_v40_' + k)),
            set: (k, v) => localStorage.setItem('nik_v40_' + k, JSON.stringify(v))
        };

        const config = LS.get('cfg') || {
            navs: [{ name: 'Github', url: 'https://github.com' }],
            ai: { baseUrl: '', apiKey: '', model: '' },
            bg: true,
            voice: false
        };

        let todos = LS.get('todos') || [];
        let notebooks = LS.get('notebooks') || [];
        let stickies = LS.get('stickies') || [];
        let currentMood = "😊";

        function initWallpaper() {
            const scrim = $('wallpaper-scrim');
            if (config.bg) {
                const bing = "https://bing.biturl.top/?resolution=1920&format=image&index=0";
                document.body.style.backgroundImage = `url('${bing}')`;
                if(scrim) scrim.style.display = 'block';
            } else {
                document.body.style.backgroundImage = 'none';
                if(scrim) scrim.style.display = 'none';
            }
        }

        async function fetchWeather() {
            try {
                const res = await fetch('https://wttr.in/?format=%t+%C');
                const text = await res.text();
                const parts = text.split(' ');
                $('cur-temp').textContent = parts[0] || '--°C';
                $('cur-weather').textContent = parts[1] ? parts[1].toUpperCase() : 'STATION';
            } catch(e) { $('cur-weather').textContent = 'STATION'; }
        }

        function checkReminders() {
            const now = new Date();
            const offset = now.getTimezoneOffset() * 60000;
            const nowLocal = (new Date(now - offset)).toISOString().slice(0, 16);
            todos.forEach((t) => {
                if (!t.done && t.time && t.time <= nowLocal && !t.alerted) {
                    t.alerted = true;
                    if (Notification.permission === "granted") new Notification("Nikwe", { body: `预定提醒：${t.text}` });
                    saveAndRenderTodos();
                }
            });
        }

        function renderTodos() {
            const list = $('todo-render-list');
            if (!list) return;
            list.innerHTML = todos.map((t, i) => `
                <li class="bg-white/70 p-6 rounded-[2.5rem] border border-white shadow-sm flex flex-col gap-4 animate-in">
                    <div class="flex items-center gap-5">
                        <input type="checkbox" ${t.done ? 'checked' : ''} onchange="toggleTask(${i}, this.checked)" class="!w-6 !h-6 cursor-pointer">
                        <span class="flex-1 text-[15px] font-bold ${t.done ? 'line-through opacity-20' : 'text-slate-700'}">${t.text}</span>
                        <button onclick="delTask(${i})" class="text-red-400 hover:text-red-600 transition-colors"><i data-lucide="trash-2" class="w-5 h-5"></i></button>
                    </div>
                    ${t.time ? `<div class="ml-11 text-[10px] font-black uppercase opacity-40 flex items-center gap-2 text-slate-500"><i data-lucide="clock" class="w-3.5 h-3.5"></i> ${t.time.replace('T',' ')}</div>` : ''}
                </li>`).join('');
            lucide.createIcons();
        }
        window.toggleTask = (i, v) => { todos[i].done = v; saveAndRenderTodos(); };
        window.delTask = (i) => { todos.splice(i, 1); saveAndRenderTodos(); };
        function saveAndRenderTodos() { LS.set('todos', todos); renderTodos(); }

        function renderNotebook() {
            const list = $('nb-history-render');
            if(!list) return;
            list.innerHTML = notebooks.map((n, i) => `
                <div class="p-8 bg-white/70 rounded-[2.5rem] border border-white shadow-sm group animate-in">
                    <div class="flex justify-between items-start mb-3">
                        <p class="text-[14px] text-slate-800 font-medium whitespace-pre-wrap leading-relaxed flex-1">${n.content}</p>
                        <span class="text-2xl ml-4">${n.mood || '😊'}</span>
                    </div>
                    <div class="mt-5 pt-4 border-t border-slate-100 flex justify-between items-center text-[9px] font-black uppercase opacity-30">
                        <span>${n.time}</span>
                        <button onclick="delNote(${i})" class="text-red-500 opacity-0 group-hover:opacity-100 transition-all font-bold">删除</button>
                    </div>
                </div>`).join('');
        }
        window.delNote = i => { notebooks.splice(i, 1); LS.set('notebooks', notebooks); renderNotebook(); };

        // 便签渲染：缩小卡片高度 + 添加回形针/松树表情
        function renderStickies() {
            const grid = $('sticky-render-grid');
            if (!grid) return;
            const colors = ['#ffffff', '#fef3c7', '#dcfce7', '#dbeafe', '#fce7f3', '#f1f5f9'];
            grid.innerHTML = stickies.map((s) => `
                <div class="p-8 rounded-[3.5rem] flex flex-col shadow-xl border-l-[12px] bg-white animate-in relative group h-[20rem]" style="border-left-color: ${s.color || '#000'}">
                    <!-- 装饰表情 -->
                    <div class="absolute top-6 right-6 text-xl opacity-30 select-none">📎</div>
                    
                    <textarea oninput="updateSticky('${s.id}', this.value)" class="bg-transparent flex-1 text-[15px] font-bold resize-none leading-relaxed text-slate-800 outline-none" placeholder="Spirit Capsule...">${s.content}</textarea>
                    
                    <div class="mt-4 flex items-center justify-between">
                        <div class="flex gap-2.5">
                            ${colors.map(c => `<div class="capsule-color-dot" style="background:${c}" onclick="setStickyColor('${s.id}', '${c}')"></div>`).join('')}
                        </div>
                        <div class="text-lg opacity-20 select-none">🌲</div>
                    </div>

                    <select onchange="linkStickyTask('${s.id}', this.value)" class="!h-9 !text-[9px] uppercase font-black !bg-slate-50 mt-4 cursor-pointer">
                        <option value="">+ LINK OBJECTIVE</option>
                        ${todos.map((t, idx) => `<option value="${idx}">${t.done ? '✓' : '○'} ${t.text}</option>`).join('')}
                    </select>
                    
                    <div class="flex justify-between items-center mt-6 pt-4 border-t border-black/5">
                        <div class="flex gap-4">
                            <button id="save-ui-${s.id}" onclick="saveSpecificSticky('${s.id}')" class="text-[9px] font-black opacity-30 hover:opacity-100 uppercase flex items-center gap-2"><i data-lucide="save" class="w-3.5 h-3.5"></i> SAVE</button>
                            <button onclick="addTodoFromSticky('${s.id}')" class="text-[9px] font-black opacity-30 hover:opacity-100 uppercase flex items-center gap-2"><i data-lucide="corner-right-up" class="w-3.5 h-3.5"></i> TASK</button>
                        </div>
                        <button onclick="delSticky('${s.id}')" class="text-[9px] font-black text-red-600 opacity-20 hover:opacity-100 uppercase">Del</button>
                    </div>
                </div>`).join('');
            lucide.createIcons();
        }
        
        window.updateSticky = (id, v) => { 
            const note = stickies.find(n => n.id === id);
            if(note) { note.content = v; LS.set('stickies', stickies); }
        };
        window.saveSpecificSticky = (id) => { 
            LS.set('stickies', stickies); 
            const btn = $(`save-ui-${id}`);
            if(btn) { 
                const original = btn.innerHTML; 
                btn.innerHTML = "SAVED ✔"; 
                setTimeout(() => { btn.innerHTML = original; lucide.createIcons(); }, 1200); 
            }
        };
        window.setStickyColor = (id, c) => { 
            const note = stickies.find(n => n.id === id);
            if(note) { note.color = c; LS.set('stickies', stickies); renderStickies(); }
        };
        window.delSticky = (id) => { 
            stickies = stickies.filter(n => n.id !== id);
            LS.set('stickies', stickies); renderStickies(); 
        };
        window.linkStickyTask = (id, tIdx) => {
            const note = stickies.find(n => n.id === id);
            if(note && tIdx !== "") { 
                note.content = `[REF: ${todos[tIdx].text}] ` + note.content; 
                LS.set('stickies', stickies); renderStickies(); 
            }
        };
        window.addTodoFromSticky = (id) => {
            const note = stickies.find(n => n.id === id);
            if(note) {
                todos.unshift({ text: note.content, time: null, done: false, alerted: false });
                saveAndRenderTodos();
                toggleUI('panel-todo');
            }
        };

        function renderNavs() {
            const main = $('home-tiles'), cfg = $('cfg-app-list');
            if (main) main.innerHTML = config.navs.map(n => `<a href="${n.url}" target="_blank" class="hover:underline decoration-4 underline-offset-8 transition-all font-black uppercase text-slate-950">${n.name}</a>`).join('');
            if (cfg) cfg.innerHTML = config.navs.map((n, i) => `
                <div class="flex justify-between items-center bg-white p-5 rounded-3xl shadow-sm border border-slate-100">
                    <span class="text-[11px] font-black uppercase text-slate-800">${n.name}</span>
                    <button onclick="removeApp(${i})" class="text-red-400"><i data-lucide="x" class="w-4 h-4"></i></button>
                </div>`).join('');
            lucide.createIcons();
        }
        window.removeApp = i => { config.navs.splice(i, 1); renderNavs(); };

        function toggleUI(id) {
            const panels = ['panel-todo', 'panel-sticky', 'panel-notebook', 'panel-pm-view', 'panel-config', 'panel-ai-history'];
            panels.forEach(p => {
                const t = $(p);
                if (!t) return;
                if (p === id) {
                    const isHidden = t.classList.contains('hidden');
                    if (isHidden) { t.classList.remove('hidden'); t.style.display='flex'; }
                    else { t.classList.add('hidden'); t.style.display='none'; }
                } else {
                    t.classList.add('hidden'); t.style.display='none';
                }
            });
        }

        window.onload = () => {
            lucide.createIcons();
            initWallpaper();
            fetchWeather();
            renderTodos();
            renderNotebook();
            renderStickies();
            renderNavs();

            if (config.bg) $('sw-mini-wp').classList.add('active');
            if (config.voice) $('sw-mini-voice').classList.add('active');
            
            setInterval(() => {
                const now = new Date();
                if ($('display-time')) $('display-time').textContent = now.toLocaleTimeString('zh-CN', { hour: '2-digit', minute: '2-digit', hour12: false });
                if ($('display-date')) $('display-date').textContent = now.toLocaleDateString('zh-CN', { year: 'numeric', month: '2-digit', day: '2-digit' }).replace(/\//g, ' / ');
                checkReminders();
            }, 1000);

            const bind = (id, fn) => { if($(id)) $(id).onclick = fn; };
            bind('dock-todo', () => toggleUI('panel-todo'));
            bind('dock-notebook', () => toggleUI('panel-notebook'));
            bind('dock-sticky', () => toggleUI('panel-sticky'));
            bind('dock-pm', () => toggleUI('panel-pm-view'));
            bind('dock-config', () => toggleUI('panel-config'));
            bind('ai-send-btn', () => toggleUI('panel-ai-history'));
            
            bind('nb-save-btn', () => {
                const v = $('nb-input').value.trim();
                if(v) { notebooks.unshift({ content: v, mood: currentMood, time: new Date().toLocaleString() }); $('nb-input').value=''; LS.set('notebooks', notebooks); renderNotebook(); }
            });
            bind('sticky-new-trigger', () => { 
                const newId = 'note-' + Date.now();
                stickies.unshift({id: newId, content: '', color: '#000'}); 
                LS.set('stickies', stickies); renderStickies(); 
            });

            document.querySelectorAll('.mood-opt').forEach(btn => {
                btn.onclick = () => {
                    document.querySelectorAll('.mood-opt').forEach(b => b.classList.add('grayscale'));
                    btn.classList.remove('grayscale');
                    currentMood = btn.dataset.mood;
                };
            });

            bind('btn-add-tile', () => {
                const n = $('in-app-name').value, u = $('in-app-url').value;
                if (n && u) { config.navs.push({name:n, url:u}); $('in-app-name').value=''; $('in-app-url').value=''; renderNavs(); }
            });

            bind('btn-set-local', () => {
                $('cfg-ai-base').value = "http://localhost:11434/v1";
                $('cfg-ai-key').value = "ollama";
                $('cfg-ai-model').value = "llama3";
            });

            document.querySelectorAll('.close-all-ui').forEach(b => {
                b.onclick = function() {
                    const p = this.closest('div[id^="panel-"]');
                    if (p) toggleUI(p.id);
                };
            });

            bind('sw-mini-wp', () => { config.bg = !config.bg; $('sw-mini-wp').classList.toggle('active'); initWallpaper(); LS.set('cfg', config); });
            bind('sw-mini-voice', () => { config.voice = !config.voice; $('sw-mini-voice').classList.toggle('active'); LS.set('cfg', config); });

            bind('pm-auth-btn', () => { if($('pm-room-id').value) { $('pm-auth-scr').classList.add('hidden'); $('pm-active-scr').classList.remove('hidden'); } });

            bind('btn-save-all', () => {
                config.ai = { baseUrl: $('cfg-ai-base').value, apiKey: $('cfg-ai-key').value, model: $('cfg-ai-model').value };
                LS.set('cfg', config); location.reload();
            });

            window.addEventListener('keydown', e => {
                if (e.key === 'Escape') {
                    const active = ['panel-todo', 'panel-sticky', 'panel-notebook', 'panel-pm-view', 'panel-config', 'panel-ai-history'].find(id => !$(id).classList.contains('hidden'));
                    if (active) toggleUI(active);
                }
            });

            document.addEventListener('keypress', e => { if (e.key === 'Enter' && document.activeElement === $('todo-in-text')) {
                const content = $('todo-in-text').value.trim();
                const time = $('todo-time-in').value;
                if (content) {
                    todos.unshift({ text: content, time: time, done: false, alerted: false });
                    $('todo-in-text').value = ''; $('todo-time-in').value = '';
                    saveAndRenderTodos();
                }
            }});
            
            if (Notification.permission === "default") Notification.requestPermission();
        };
    </script>
</body>
</html>
