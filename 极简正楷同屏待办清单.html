<!doctype html>
<html lang="zh-CN">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no, viewport-fit=cover">
<title>今日与明日 — 极简正楷待办</title>
<meta name="apple-mobile-web-app-capable" content="yes">
<meta name="apple-mobile-web-app-status-bar-style" content="default">
<meta name="apple-mobile-web-app-title" content="今日与明日">
<meta name="theme-color" content="#fdfcf7">
<style>
  :root {
    --bg: #fdfcf7;
    --surface: #ffffff;
    --ink: #1f2421;
    --muted: #767d78;
    --light: #a3a8a4;
    --line: #e6e8e3;
    --accent: #556b5d;
    --warn: #9a5b36;
    --font-kai: "Kaiti SC", "STKaiti", "楷体", "KaiTi", "BiauKai", "DFKai-SB", serif;
  }

  * { box-sizing: border-box; -webkit-tap-highlight-color: transparent; }
  body {
    margin: 0;
    background: var(--bg);
    color: var(--ink);
    font: 16px/1.7 var(--font-kai);
    -webkit-font-smoothing: antialiased;
    padding-bottom: 120px;
  }
  button, input, select { font-family: var(--font-kai); font-size: inherit; color: inherit; }
  button { cursor: pointer; border: 0; background: transparent; }

  .wrap { max-width: 1100px; margin: 0 auto; padding: 24px 20px; }

  header {
    display: flex;
    justify-content: space-between;
    align-items: baseline;
    border-bottom: 1px solid var(--line);
    padding-bottom: 14px;
    margin-bottom: 22px;
  }
  header h1 { margin: 0; font-size: 22px; font-weight: 700; letter-spacing: 0.08em; }
  header p { margin: 2px 0 0; font-size: 13px; color: var(--muted); }
  .nav-actions { display: flex; gap: 12px; }
  .link-btn { font-size: 13px; color: var(--muted); padding: 2px 0; border-bottom: 1px solid transparent; }
  .link-btn:hover { color: var(--ink); border-bottom-color: var(--ink); }

  /* 倒计时横向滚动条 */
  .section-title { font-size: 14px; font-weight: 600; color: var(--muted); letter-spacing: 0.1em; margin-bottom: 10px; display: flex; justify-content: space-between; align-items: baseline; }
  .countdown-row {
    display: flex; gap: 12px; overflow-x: auto; padding-bottom: 6px; margin-bottom: 24px; scrollbar-width: none;
  }
  .countdown-row::-webkit-scrollbar { display: none; }
  .cd-box {
    flex: 0 0 auto; min-width: 175px; background: var(--surface); border: 1px solid var(--line); border-radius: 8px; padding: 12px 14px;
    display: flex; justify-content: space-between; align-items: center; position: relative;
  }
  .cd-box.urgent { background: #fcf6f0; border-color: #ebd7cc; }
  .cd-name { font-size: 15px; font-weight: 600; white-space: nowrap; overflow: hidden; text-overflow: ellipsis; max-width: 110px; }
  .cd-num-box { text-align: right; }
  .cd-days { font-size: 22px; font-weight: 700; line-height: 1; color: var(--accent); }
  .cd-box.urgent .cd-days { color: var(--warn); }
  .cd-unit { font-size: 11px; color: var(--muted); }
  .cd-del { position: absolute; top: 2px; right: 4px; font-size: 12px; color: var(--light); }

  /* 多日并排看板 */
  .board-grid {
    display: flex; gap: 16px; overflow-x: auto; scroll-snap-type: x mandatory; scroll-behavior: smooth; padding-bottom: 10px; margin-bottom: 28px; scrollbar-width: none;
  }
  .board-grid::-webkit-scrollbar { display: none; }
  .day-card {
    flex: 0 0 84%; scroll-snap-align: start; background: var(--surface); border: 1px solid var(--line); border-radius: 10px; padding: 18px;
    min-height: 290px; display: flex; flex-direction: column;
  }
  .day-card.today-card { border-color: #d1ded4; background: #ffffff; }
  .day-card-header { display: flex; justify-content: space-between; align-items: baseline; border-bottom: 1px solid var(--line); padding-bottom: 10px; margin-bottom: 10px; }
  .day-title { font-size: 18px; font-weight: 700; }
  .day-card.today-card .day-title { color: var(--accent); }
  .day-sub { font-size: 13px; color: var(--muted); }

  .task-list-box { flex: 1; display: flex; flex-direction: column; }
  .task-item { display: flex; align-items: center; gap: 8px; padding: 6px 0; border-bottom: 1px dashed #f2f2ee; }
  .task-item:last-child { border-bottom: none; }
  .checkbox-wrap { width: 26px; height: 26px; display: flex; align-items: center; justify-content: center; cursor: pointer; flex: none; }
  .custom-checkbox { width: 15px; height: 15px; border-radius: 3px; border: 1.5px solid var(--light); display: flex; align-items: center; justify-content: center; }
  .task-item.completed .custom-checkbox { background: var(--ink); border-color: var(--ink); }
  .task-item.completed .custom-checkbox::after { content: ""; width: 4px; height: 8px; border: solid #fff; border-width: 0 1.5px 1.5px 0; transform: rotate(45deg); }
  .task-text { flex: 1; font-size: 15px; white-space: nowrap; overflow: hidden; text-overflow: ellipsis; cursor: pointer; }
  .task-item.completed .task-text { text-decoration: line-through; color: var(--light); }
  .task-del { font-size: 12px; color: var(--light); padding: 2px 4px; }
  .task-del:hover { color: var(--warn); }

  .inline-input-row { margin-top: 10px; padding-top: 8px; border-top: 1px solid var(--line); }
  .inline-input-row input { width: 100%; border: 0; background: transparent; outline: none; font-size: 14px; padding: 4px 0; }
  .inline-input-row input::placeholder { color: var(--light); }

  /* 月度总清单 */
  .pool-section { background: var(--surface); border: 1px solid var(--line); border-radius: 10px; padding: 18px; }
  .pool-head { display: flex; justify-content: space-between; align-items: baseline; border-bottom: 1px solid var(--line); padding-bottom: 10px; margin-bottom: 10px; }
  .pool-head h2 { margin: 0; font-size: 17px; font-weight: 700; }
  .pool-items { display: flex; flex-direction: column; }
  .pool-row { display: flex; align-items: center; gap: 8px; padding: 8px 0; border-bottom: 1px solid #f2f2ee; }
  .pool-row:last-child { border-bottom: none; }
  .pool-row-title { flex: 1; font-size: 15px; white-space: nowrap; overflow: hidden; text-overflow: ellipsis; cursor: pointer; }
  .pool-row.completed .pool-row-title { text-decoration: line-through; color: var(--light); }
  .move-btns { display: flex; gap: 4px; }
  .move-btn { font-size: 12px; padding: 2px 6px; border: 1px solid var(--line); border-radius: 4px; color: var(--muted); background: var(--bg); }

  /* 底部固定拇指输入栏 */
  .bottom-bar {
    position: fixed; bottom: 0; left: 0; right: 0; background: rgba(253, 252, 247, 0.95);
    backdrop-filter: blur(8px); border-top: 1px solid var(--line); padding: 10px 16px calc(10px + env(safe-area-inset-bottom)); z-index: 40;
  }
  .bottom-inner { max-width: 900px; margin: 0 auto; display: flex; flex-direction: column; gap: 6px; }
  .target-selectors { display: flex; gap: 16px; font-size: 13px; }
  .target-tab { color: var(--muted); cursor: pointer; border-bottom: 1.5px solid transparent; padding-bottom: 1px; }
  .target-tab.active { color: var(--ink); font-weight: 700; border-bottom-color: var(--ink); }
  .bottom-input-wrap { display: flex; gap: 8px; }
  .bottom-input-wrap input { flex: 1; border: 1px solid var(--line); background: var(--surface); border-radius: 8px; padding: 10px 14px; font-size: 16px; outline: none; }
  .bottom-input-wrap input:focus { border-color: var(--ink); }
  .submit-btn { background: var(--ink); color: #fff; padding: 0 20px; border-radius: 8px; font-size: 15px; }

  /* 弹窗样式 */
  .modal-mask { position: fixed; inset: 0; background: rgba(31,36,33,0.4); display: none; align-items: flex-end; justify-content: center; z-index: 50; }
  .modal-mask.show { display: flex; }
  .modal-box { width: 100%; max-width: 440px; background: var(--surface); border-radius: 16px 16px 0 0; padding: 24px 20px calc(24px + env(safe-area-inset-bottom)); }
  .modal-box h3 { margin: 0 0 16px; font-size: 18px; font-weight: 700; }
  .field { margin-bottom: 14px; }
  .field label { display: block; font-size: 13px; color: var(--muted); margin-bottom: 6px; }
  .field input, .field select { width: 100%; border: 1px solid var(--line); border-radius: 8px; padding: 10px 12px; font-size: 16px; outline: none; background: #fff; }
  .modal-actions { display: flex; gap: 10px; margin-top: 18px; }
  .modal-actions button { flex: 1; padding: 11px; border-radius: 8px; font-size: 16px; }
  .btn-close { background: #f2f2ee; color: var(--ink); }
  .btn-ok { background: var(--ink); color: #fff; }

  .toast {
    position: fixed; top: 16px; left: 50%; transform: translateX(-50%) translateY(-20px);
    background: var(--ink); color: #fff; font-size: 13px; padding: 6px 16px; border-radius: 99px;
    opacity: 0; transition: all .2s; z-index: 60; pointer-events: none;
  }
  .toast.show { opacity: 1; transform: translateX(-50%) translateY(0); }

  @media (min-width: 768px) {
    .wrap { padding: 32px; }
    .day-card { flex: 1 1 0; min-width: 220px; }
    .modal-mask { align-items: center; padding: 16px; }
    .modal-box { border-radius: 12px; }
  }
</style>
</head>
<body>

<div class="wrap">
  <header>
    <div>
      <h1>今日与明日</h1>
      <p id="headerDateText">加载中...</p>
    </div>
    <div class="nav-actions">
      <button class="link-btn" id="openEventModal">＋ 倒计时</button>
      <button class="link-btn" id="exportBtn">备份</button>
    </div>
  </header>

  <div class="section-title">
    <span>重要倒计时提醒</span>
  </div>
  <div class="countdown-row" id="countdownRow"></div>

  <div class="section-title" style="justify-content:space-between">
    <span>未来日程看板</span>
    <div>
      <button class="link-btn" onclick="document.getElementById('boardGrid').scrollTo({left:0,behavior:'smooth'})" style="margin-right:12px">回到今天</button>
      <button class="link-btn" onclick="extendDays()">＋ 多看三天</button>
    </div>
  </div>
  <div class="board-grid" id="boardGrid"></div>

  <div class="pool-section">
    <div class="pool-head">
      <h2 id="poolTitle">本月总清单</h2>
      <span class="day-sub" id="poolBadge">0 项待排期</span>
    </div>
    <div class="pool-items" id="poolItemsList"></div>
  </div>
</div>

<!-- 底部固定拇指输入栏 -->
<div class="bottom-bar">
  <div class="bottom-inner">
    <div class="target-selectors">
      <span class="target-tab active" data-target="0">记入今天</span>
      <span class="target-tab" data-target="1">记入明天</span>
      <span class="target-tab" data-target="2">记入后天</span>
      <span class="target-tab" data-target="month">放入本月总清单</span>
    </div>
    <form class="bottom-input-wrap" id="bottomForm">
      <input type="text" id="bottomInput" placeholder="写下待办事项，直接记入「今天」..." autocomplete="off" required>
      <button type="submit" class="submit-btn">记下</button>
    </form>
  </div>
</div>

<!-- 新建倒计时弹窗 -->
<div class="modal-mask" id="eventModal">
  <div class="modal-box">
<h3>新建倒计时提醒</h3>
    <form id="eventForm">
      <div class="field">
        <label>事件名称（如：后天重要会议）</label>
        <input type="text" id="evName" required maxlength="50" placeholder="例如：项目汇报">
      </div>
      <div class="field">
        <label>发生日期与时间</label>
        <input type="datetime-local" id="evDate" required>
      </div>
      <div class="modal-actions">
        <button type="button" class="btn-close" onclick="closeModal()">取消</button>
        <button type="submit" class="btn-ok">保存</button>
      </div>
    </form>
  </div>
</div>

<div class="toast" id="toast"></div>

<script>
  const $ = id => document.getElementById(id);
  const toast = msg => {
    const t = $('toast'); t.textContent = msg; t.classList.add('show');
    setTimeout(() => t.classList.remove('show'), 2200);
  };

  const today0 = () => { const d = new Date(); d.setHours(0,0,0,0); return d; };
  const iso = d => { const x = new Date(d); return `${x.getFullYear()}-${String(x.getMonth()+1).padStart(2,'0')}-${String(x.getDate()).padStart(2,'0')}`; };
  const uid = () => Math.random().toString(36).slice(2) + Date.now().toString(36);
  const escapeHTML = s => String(s ?? '').replace(/[&<>"']/g, c => ({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'}[c]));
  const WEEKDAYS = ['周日', '周一', '周二', '周三', '周四', '周五', '周六'];

  let data = { tasks: [], events: [] };
  let displayDays = 4; // 默认展示今、明、后、大后天共 4 天
  let targetMode = '0'; // 底部输入默认记入今天

  function save() { localStorage.setItem('minimalKaitiTodo', JSON.stringify(data)); }
  function load() {
    try {
      const raw = localStorage.getItem('minimalKaitiTodo');
      if (raw) {
        const p = JSON.parse(raw);
        data = { tasks: Array.isArray(p.tasks)?p.tasks:[], events: Array.isArray(p.events)?p.events:[] };
        return;
      }
    } catch(e) {}
    // 默认示例数据
    const t = today0();
    const d0 = iso(t), d1 = iso(new Date(t.getFullYear(), t.getMonth(), t.getDate()+1)), d2 = iso(new Date(t.getFullYear(), t.getMonth(), t.getDate()+2));
    const evTime = new Date(t.getFullYear(), t.getMonth(), t.getDate()+2, 10, 0).toISOString().slice(0,16);
    data = {
      tasks: [
        { id: uid(), title: '梳理本月所有核心任务', date: d0, completed: false },
        { id: uid(), title: '阅读专业书籍 30 分钟', date: d0, completed: true },
        { id: uid(), title: '准备后天会议的资料', date: d1, completed: false },
        { id: uid(), title: '给家里打个电话', date: d2, completed: false },
        { id: uid(), title: '买一本新笔记本', date: '', completed: false }
      ],
      events: [
        { id: uid(), name: '后天重要会议', date: evTime }
      ]
    };
    save();
  }

  function render() {
    const now = today0();
    $('headerDateText').textContent = `${now.getFullYear()}年${now.getMonth()+1}月${now.getDate()}日 ${WEEKDAYS[now.getDay()]}`;

    // 1. 渲染顶部倒计时
    const evs = data.events.filter(e => new Date(e.date) >= now).sort((a,b)=>new Date(a.date)-new Date(b.date));
    $('countdownRow').innerHTML = evs.map(e => {
      const diffDays = Math.ceil((new Date(e.date) - now) / 86400000);
      const urgent = diffDays <= 2;
      return `
        <div class="cd-box ${urgent?'urgent':''}">
          <div>
            <div class="cd-name">${escapeHTML(e.name)}</div>
            <div style="font-size:11px;color:var(--muted);margin-top:2px">${diffDays<=0?'今天进行':'还有机会'}</div>
          </div>
          <div class="cd-num-box">
            <div class="cd-days">${diffDays<=0?0:diffDays}</div>
            <div class="cd-unit">天后</div>
          </div>
          <button class="cd-del" onclick="removeEvent('${e.id}')">×</button>
        </div>
      `;
    }).join('') || '<div style="color:var(--muted);font-size:13px;padding:6px 0">暂无重要倒计时</div>';

    // 2. 渲染多日看板
    const board = $('boardGrid');
    board.innerHTML = '';
    for (let i = 0; i < displayDays; i++) {
      const d = new Date(now);
      d.setDate(d.getDate() + i);
      const dStr = iso(d);
      const isToday = i === 0;
      const titleName = i === 0 ? '今天' : i === 1 ? '明天' : i === 2 ? '后天' : `${WEEKDAYS[d.getDay()]} (${d.getMonth()+1}/${d.getDate()})`;
      const dayTasks = data.tasks.filter(t => t.date === dStr);
      const doneCount = dayTasks.filter(t => t.completed).length;

      const card = document.createElement('div');
      card.className = `day-card ${isToday?'today-card':''}`;
      card.innerHTML = `
        <div class="day-card-header">
          <div>
            <span class="day-title">${titleName}</span>
            <span class="day-sub" style="margin-left:6px">${d.getMonth()+1}月${d.getDate()}日</span>
          </div>
          <span class="day-sub">${doneCount}/${dayTasks.length}</span>
        </div>
        <div class="task-list-box">
          ${dayTasks.map(t => `
            <div class="task-item ${t.completed?'completed':''}">
              <div class="checkbox-wrap" onclick="toggleTask('${t.id}')">
                <div class="custom-checkbox"></div>
              </div>
              <span class="task-text" onclick="editTask('${t.id}')">${escapeHTML(t.title)}</span>
              <button class="task-del" onclick="removeTask('${t.id}')">删</button>
            </div>
          `).join('') || '<div style="color:var(--light);font-size:13px;text-align:center;padding:16px 0">暂无安排</div>'}
        </div>
        <div class="inline-input-row">
          <input type="text" placeholder="＋ 记入${titleName}..." onkeydown="if(event.key==='Enter')quickAdd(this,'${dStr}')">
        </div>
      `;
      board.appendChild(card);
    }

    // 3. 渲染本月总清单
    const unassigned = data.tasks.filter(t => !t.date);
    $('poolBadge').textContent = `${unassigned.length} 项未排期`;
    $('poolItemsList').innerHTML = unassigned.map(t => `
      <div class="pool-row ${t.completed?'completed':''}">
        <div class="checkbox-wrap" onclick="toggleTask('${t.id}')">
          <div class="custom-checkbox"></div>
        </div>
        <span class="pool-row-title" onclick="editTask('${t.id}')">${escapeHTML(t.title)}</span>
        <div class="move-btns">
          <button class="move-btn" onclick="moveTaskDate('${t.id}', 0)">今天</button>
          <button class="move-btn" onclick="moveTaskDate('${t.id}', 1)">明天</button>
          <button class="move-btn" onclick="removeTask('${t.id}')">删</button>
        </div>
      </div>
    `).join('') || '<div style="color:var(--light);font-size:13px;padding:10px 0">所有待办均已分配到具体日期。</div>';
  }

  // 任务交互函数
  window.toggleTask = function(id) {
    const t = data.tasks.find(x => x.id === id);
    if (t) { t.completed = !t.completed; save(); render(); }
  };
  window.removeTask = function(id) {
    data.tasks = data.tasks.filter(x => x.id !== id);
    save(); render(); toast('已删除');
  };
  window.moveTaskDate = function(id, offset) {
    const t = data.tasks.find(x => x.id === id);
    if (t) {
      const d = today0(); d.setDate(d.getDate() + offset);
      t.date = iso(d); save(); render(); toast('已排期');
    }
  };
  window.editTask = function(id) {
    const t = data.tasks.find(x => x.id === id);
    if (!t) return;
    const val = prompt('修改待办名称：', t.title);
    if (val !== null && val.trim() !== '') { t.title = val.trim(); save(); render(); }
  };
  window.quickAdd = function(input, dateStr) {
    const v = input.value.trim();
    if (!v) return;
    data.tasks.push({ id: uid(), title: v, date: dateStr, completed: false });
    input.value = ''; save(); render(); toast('已添加');
  };
  window.removeEvent = function(id) {
    data.events = data.events.filter(x => x.id !== id);
    save(); render(); toast('已移除倒计时');
  };
  window.extendDays = function() {
    displayDays = Math.min(displayDays + 3, 14);
    render(); toast('已扩展看板');
  };

  // 底部输入栏切换
  document.querySelectorAll('.target-tab').forEach(tab => {
    tab.onclick = () => {
      document.querySelectorAll('.target-tab').forEach(b => b.classList.remove('active'));
      tab.classList.add('active');
      targetMode = tab.dataset.target;
      const name = tab.textContent.replace('记入', '').replace('放入', '');
      $('bottomInput').placeholder = `写下待办事项，直接记入「${name}」...`;
    };
  });

  $('bottomForm').onsubmit = e => {
    e.preventDefault();
    const v = $('bottomInput').value.trim();
    if (!v) return;
    let targetDate = '';
    if (targetMode !== 'month') {
      const d = today0(); d.setDate(d.getDate() + Number(targetMode));
      targetDate = iso(d);
    }
    data.tasks.push({ id: uid(), title: v, date: targetDate, completed: false });
    $('bottomInput').value = '';
    save(); render(); toast('已记录');
  };

  // 弹窗控制
  $('openEventModal').onclick = () => {
    const d = new Date(Date.now() + 86400000); d.setMinutes(0,0,0);
    $('evDate').value = new Date(d.getTime() - d.getTimezoneOffset()*60000).toISOString().slice(0,16);
    $('eventModal').classList.add('show');
  };
  window.closeModal = () => $('eventModal').classList.remove('show');

  $('eventForm').onsubmit = e => {
    e.preventDefault();
    data.events.push({ id: uid(), name: $('evName').value.trim(), date: $('evDate').value });
    closeModal(); $('eventForm').reset();
    save(); render(); toast('倒计时已创建');
  };

  $('exportBtn').onclick = () => {
    const blob = new Blob([JSON.stringify(data, null, 2)], { type: 'application/json' });
    const a = document.createElement('a'); a.href = URL.createObjectURL(blob);
    a.download = `todo-${iso(new Date())}.json`; a.click(); URL.revokeObjectURL(a.href);
    toast('备份文件已导出');
  };

  load();
  render();
</script>
</body>
</html>