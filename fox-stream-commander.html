<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Voice Commander</title>
<style>
*{box-sizing:border-box;margin:0;padding:0}
body{font-family:'Segoe UI',sans-serif;background:#0e0e10;color:#efeff1;min-height:100vh;padding:16px;font-size:14px}
h1{color:#9147ff;font-size:18px;font-weight:600;margin-bottom:2px}
.sub{color:#adadb8;font-size:12px;margin-bottom:16px}
.grid{display:grid;grid-template-columns:1fr 1fr;gap:12px;margin-bottom:12px}
@media(max-width:640px){.grid{grid-template-columns:1fr}}
.card{background:#18181b;border:0.5px solid #3a3a3d;border-radius:8px;padding:14px}
.card h2{font-size:11px;font-weight:600;color:#adadb8;text-transform:uppercase;letter-spacing:.08em;margin-bottom:10px}
label{display:block;font-size:12px;color:#adadb8;margin-bottom:3px;margin-top:8px}
label:first-of-type{margin-top:0}
input,select{width:100%;background:#0e0e10;border:0.5px solid #3a3a3d;color:#efeff1;border-radius:5px;padding:6px 9px;font-size:12px;outline:none}
input:focus,select:focus{border-color:#9147ff}
button{border:none;border-radius:5px;padding:7px 14px;font-size:12px;cursor:pointer;font-weight:600}
.btn-purple{background:#9147ff;color:#fff}.btn-purple:hover{background:#772ce8}
.btn-purple:disabled{background:#3a3a3d;color:#adadb8;cursor:not-allowed}
.btn-red{background:#e91916;color:#fff}.btn-red:hover{background:#bf0e0b}
.btn-green{background:#00b159;color:#fff}.btn-green:hover{background:#009146}
.btn-ghost{background:transparent;border:0.5px solid #3a3a3d;color:#adadb8}.btn-ghost:hover{border-color:#9147ff;color:#9147ff}
.btn-twitch{background:#9147ff;color:#fff;display:flex;align-items:center;gap:8px;padding:9px 18px;font-size:13px;border-radius:6px;width:100%;justify-content:center}
.btn-twitch:hover{background:#772ce8}
.btn-sm{padding:4px 10px;font-size:11px}
.status-bar{display:flex;align-items:center;gap:10px;padding:10px 14px;background:#18181b;border:0.5px solid #3a3a3d;border-radius:8px;margin-bottom:12px}
.dot{width:9px;height:9px;border-radius:50%;background:#3a3a3d;flex-shrink:0;transition:background .3s}
.dot.listening{background:#9147ff;animation:pulse 1s infinite}
.dot.error{background:#e91916}
@keyframes pulse{0%,100%{opacity:1}50%{opacity:.4}}
.status-text{flex:1;font-size:12px;color:#adadb8}
.transcript{background:#0e0e10;border:0.5px solid #3a3a3d;border-radius:5px;padding:8px;font-size:12px;color:#adadb8;font-style:italic;min-height:36px;margin-bottom:10px}
.log{background:#0e0e10;border:0.5px solid #3a3a3d;border-radius:5px;height:180px;overflow-y:auto;padding:8px;font-size:11px;font-family:monospace}
.le{padding:1px 0;border-bottom:0.5px solid #1f1f23}
.le.cmd{color:#9147ff}.le.chat{color:#00b159}.le.err{color:#e91916}.le.obs{color:#ff8c00}.le.info{color:#adadb8}.le.match{color:#ffb347}
.commands-grid{display:grid;grid-template-columns:1fr 1fr;gap:8px}
.cmd-card{background:#0e0e10;border:0.5px solid #3a3a3d;border-radius:5px;padding:8px}
.cmd-phrase{font-size:11px;font-weight:600;color:#9147ff;margin-bottom:2px}
.cmd-desc{font-size:10px;color:#adadb8}
.badge{display:inline-block;padding:1px 7px;border-radius:3px;font-size:10px;font-weight:600}
.badge-purple{background:#2d1b4e;color:#9147ff}
.row{display:flex;gap:8px;align-items:center;margin-top:8px}
.conn-status{font-size:11px}
.conn-ok{color:#00b159}.conn-no{color:#adadb8}
.section-row{display:flex;align-items:center;justify-content:space-between;margin-bottom:8px}
input[type="number"]{width:70px}
.user-pill{display:flex;align-items:center;gap:8px;background:#1a1a1d;border:0.5px solid #3a3a3d;border-radius:20px;padding:5px 12px 5px 5px}
.user-avatar{width:28px;height:28px;border-radius:50%;border:1.5px solid #9147ff}
.user-name{font-size:12px;font-weight:600;color:#efeff1}
.user-badge{font-size:10px;color:#9147ff}
.logout-btn{background:transparent;border:none;color:#adadb8;font-size:11px;cursor:pointer;padding:2px 6px}
.logout-btn:hover{color:#e91916}
.auth-section{text-align:center;padding:8px 0}
.auth-info{font-size:11px;color:#adadb8;margin-bottom:10px;line-height:1.5}
.scope-list{font-size:10px;color:#7a7a80;margin-top:6px}

/* Confirm dialog */
.confirm-overlay{position:fixed;inset:0;background:rgba(0,0,0,0.7);display:flex;align-items:center;justify-content:center;z-index:100;display:none}
.confirm-box{background:#18181b;border:1px solid #9147ff;border-radius:10px;padding:20px;width:300px;text-align:center}
.confirm-box h3{font-size:14px;color:#efeff1;margin-bottom:6px}
.confirm-box p{font-size:12px;color:#adadb8;margin-bottom:6px}
.confirm-username{font-size:18px;font-weight:700;color:#9147ff;margin:10px 0}
.confirm-heard{font-size:11px;color:#7a7a80;margin-bottom:14px}
.confirm-actions{display:flex;gap:10px;justify-content:center}

/* Chatters panel */
.chatters-bar{display:flex;align-items:center;justify-content:space-between;margin-bottom:6px}
.chatters-list{background:#0e0e10;border:0.5px solid #3a3a3d;border-radius:5px;max-height:80px;overflow-y:auto;padding:4px 6px;font-size:11px;color:#adadb8;font-family:monospace}
.chatter-tag{display:inline-block;background:#1a1a1d;border:0.5px solid #3a3a3d;border-radius:3px;padding:1px 5px;margin:1px;font-size:10px;color:#adadb8}
</style>
</head>
<body>

<h1>Voice Commander</h1>
<p class="sub">Voice-activated Twitch moderation & stream control</p>

<!-- Confirm Dialog -->
<div class="confirm-overlay" id="confirm-overlay">
  <div class="confirm-box">
    <h3 id="confirm-title">Confirm Action</h3>
    <p id="confirm-action-label">Did you mean:</p>
    <div class="confirm-username" id="confirm-username">—</div>
    <div class="confirm-heard" id="confirm-heard">Heard: "—"</div>
    <div class="confirm-actions">
      <button class="btn-green" onclick="confirmAction(true)">Yes, do it</button>
      <button class="btn-ghost" onclick="confirmAction(false)">Cancel</button>
    </div>
  </div>
</div>

<div class="status-bar">
  <div class="dot" id="mic-dot"></div>
  <div class="status-text" id="status-text">Login with Twitch to begin</div>
  <button class="btn-purple" id="listen-btn" onclick="toggleListening()" disabled>Start Listening</button>
</div>

<div class="transcript" id="transcript">Waiting for voice input...</div>

<div class="grid">
  <!-- Twitch Auth -->
  <div class="card">
    <h2>Twitch Account</h2>
    <div id="auth-logged-out" class="auth-section">
      <p class="auth-info">Sign in with your Twitch account to enable chat, moderation, and stream controls.</p>
      <button class="btn-twitch" onclick="startOAuth()">
        <svg width="16" height="16" viewBox="0 0 24 24" fill="white"><path d="M11.571 4.714h1.715v5.143H11.57zm4.715 0H18v5.143h-1.714zM6 0L1.714 4.286v15.428h5.143V24l4.286-4.286h3.428L22.286 12V0zm14.571 11.143l-3.428 3.428h-3.429l-3 3v-3H6.857V1.714h13.714z"/></svg>
        Login with Twitch
      </button>
      <p class="scope-list">Requests: chat, moderation, channel management</p>
    </div>
    <div id="auth-logged-in" style="display:none">
      <div class="user-pill">
        <img class="user-avatar" id="user-avatar" src="" alt="" />
        <div>
          <div class="user-name" id="user-name">—</div>
          <div class="user-badge">● Connected</div>
        </div>
        <button class="logout-btn" onclick="logout()">Logout</button>
      </div>
      <div style="margin-top:10px">
        <button class="btn-purple" style="width:100%" onclick="connectChat()">Connect to Chat</button>
      </div>
      <div class="row" style="margin-top:6px">
        <span class="conn-status conn-no" id="twitch-status-text">● Chat not connected</span>
      </div>
    </div>
  </div>

  <!-- OBS Setup -->
  <div class="card">
    <h2>OBS WebSocket</h2>
    <p style="font-size:11px;color:#adadb8;margin-bottom:8px">Requires OBS 28+. Enable under Tools → WebSocket Server Settings.</p>
    <label>WebSocket URL</label>
    <input id="obs-url" value="ws://localhost:4455" />
    <label>Password (if set)</label>
    <input id="obs-pass" placeholder="optional" type="password" />
    <label>BRB Scene Name (exact)</label>
    <input id="brb-scene" value="BRB" />
    <div class="row">
      <button class="btn-ghost" onclick="connectOBS()">Connect OBS</button>
      <span class="conn-status conn-no" id="obs-status-text">● Not connected</span>
    </div>
  </div>
</div>

<!-- Active Chatters -->
<div class="card" style="margin-bottom:12px">
  <div class="chatters-bar">
    <h2 style="margin:0">Active Chatters</h2>
    <div style="display:flex;gap:6px;align-items:center">
      <span style="font-size:10px;color:#7a7a80" id="chatter-count">0 users</span>
      <button class="btn-ghost btn-sm" onclick="refreshChatters()">Refresh</button>
    </div>
  </div>
  <div class="chatters-list" id="chatters-list">Connect to chat to see active viewers...</div>
</div>

<!-- Commands Reference -->
<div class="card" style="margin-bottom:12px">
  <div class="section-row">
    <h2 style="margin:0">Voice Commands</h2>
    <span class="badge badge-purple">Say these out loud</span>
  </div>
  <div class="commands-grid">
    <div class="cmd-card"><div class="cmd-phrase">"ban [username]"</div><div class="cmd-desc">Permanently bans user from chat</div></div>
    <div class="cmd-card"><div class="cmd-phrase">"timeout [username]"</div><div class="cmd-desc">Times out user (configurable duration)</div></div>
    <div class="cmd-card"><div class="cmd-phrase">"shoutout [username]"</div><div class="cmd-desc">Posts a shoutout message in chat</div></div>
    <div class="cmd-card"><div class="cmd-phrase">"unban [username]"</div><div class="cmd-desc">Removes a ban or active timeout</div></div>
    <div class="cmd-card"><div class="cmd-phrase">"poll [question], [opt1], [opt2]"</div><div class="cmd-desc">Starts a chat poll</div></div>
    <div class="cmd-card"><div class="cmd-phrase">"brb" / "be right back"</div><div class="cmd-desc">Switches OBS to BRB scene</div></div>
    <div class="cmd-card"><div class="cmd-phrase">"welcome back" / "im back"</div><div class="cmd-desc">Returns OBS to main scene</div></div>
    <div class="cmd-card"><div class="cmd-phrase">"raid [username]"</div><div class="cmd-desc">Posts raid call-to-action in chat</div></div>
  </div>
  <div style="margin-top:10px">
    <label style="margin-top:0">Timeout Duration (seconds)</label>
    <input type="number" id="timeout-dur" value="600" min="1" max="1209600" style="width:80px" />
  </div>
</div>

<!-- Log -->
<div class="card">
  <div class="section-row">
    <h2 style="margin:0">Activity Log</h2>
    <button class="btn-ghost btn-sm" onclick="clearLog()">Clear</button>
  </div>
  <div class="log" id="log">
    <div class="le info">-- Voice Commander ready --</div>
  </div>
</div>

<script>
const CLIENT_ID = 'bntjnscnzznfat54fxl91dboqb4rz3';
const REDIRECT_URI = location.href.split('?')[0].split('#')[0];
const SCOPES = ['chat:read','chat:edit','moderator:manage:banned_users','moderator:read:chatters','channel:manage:raids','channel:manage:polls','user:read:email'].join(' ');

let accessToken=null, userId=null, userLogin=null;
let recognition=null, isListening=false;
let twitchSocket=null, twitchConnected=false;
let obsSocket=null, obsConnected=false, mainScene=null;
let obsMessageId=1, obsPendingRequests={};
let chatters=new Set(); // live chatter usernames (lowercase)
let pendingAction=null; // {fn, username, heard, title}
let chattersRefreshTimer=null;

// ── Logging ────────────────────────────────────────────────────────────────
function log(msg,cls='info'){
  const el=document.getElementById('log');
  const d=document.createElement('div');
  d.className=`le ${cls}`;
  d.textContent=`[${new Date().toLocaleTimeString()}] ${msg}`;
  el.appendChild(d); el.scrollTop=el.scrollHeight;
}
function clearLog(){document.getElementById('log').innerHTML='';}
function setMic(state,text){
  const dot=document.getElementById('mic-dot');
  dot.className='dot'+(state==='listening'?' listening':state==='error'?' error':'');
  document.getElementById('status-text').textContent=text;
}

// ── Fuzzy username matching ────────────────────────────────────────────────
// Normalise: remove spaces, lowercase, collapse letters (e.g. spoken "s t r e a m" → "stream")
function normalise(str){
  return str.toLowerCase()
    .replace(/\s+/g,'')           // join spaced letters: "s t r e a m" → "stream"
    .replace(/[^a-z0-9_]/g,'')   // strip non-username chars
    .replace(/zero/g,'0').replace(/one/g,'1').replace(/two/g,'2')
    .replace(/three/g,'3').replace(/four/g,'4').replace(/five/g,'5')
    .replace(/six/g,'6').replace(/seven/g,'7').replace(/eight/g,'8').replace(/nine/g,'9');
}

// Levenshtein distance
function levenshtein(a,b){
  const m=a.length, n=b.length;
  const dp=Array.from({length:m+1},(_,i)=>Array.from({length:n+1},(_,j)=>i===0?j:j===0?i:0));
  for(let i=1;i<=m;i++) for(let j=1;j<=n;j++)
    dp[i][j]=a[i-1]===b[j-1]?dp[i-1][j-1]:1+Math.min(dp[i-1][j],dp[i][j-1],dp[i-1][j-1]);
  return dp[m][n];
}

// Find best matching chatter for a spoken string
// Returns {username, score} or null
function findBestMatch(spoken){
  const norm = normalise(spoken);
  if(!norm) return null;

  let best=null, bestScore=Infinity;

  for(const chatter of chatters){
    const cn = normalise(chatter);
    // Exact match wins immediately
    if(cn===norm) return {username:chatter, score:0};

    // Also try if chatter name starts with or contains the spoken string
    const containsScore = cn.includes(norm) ? 0.5 : Infinity;

    const dist = levenshtein(norm, cn);
    // Normalise by length so short names don't get unfair advantage
    const score = Math.min(dist / Math.max(cn.length, norm.length), containsScore);

    if(score < bestScore){ bestScore=score; best=chatter; }
  }

  // Only accept if score is reasonable (< 0.55 similarity threshold)
  if(best && bestScore < 0.55) return {username:best, score:bestScore};
  return null;
}

// ── Confirm dialog ─────────────────────────────────────────────────────────
function showConfirm(title, username, heard, actionFn){
  pendingAction={fn:actionFn, username};
  document.getElementById('confirm-title').textContent=title;
  document.getElementById('confirm-username').textContent=username;
  document.getElementById('confirm-heard').textContent=`Heard: "${heard}"`;
  document.getElementById('confirm-overlay').style.display='flex';
}
function confirmAction(yes){
  document.getElementById('confirm-overlay').style.display='none';
  if(yes && pendingAction) pendingAction.fn(pendingAction.username);
  pendingAction=null;
}

// ── Resolve username with fuzzy match + confirm ────────────────────────────
function resolveWithConfirm(spoken, title, actionFn){
  const norm = normalise(spoken);
  // Direct exact match in chatters — no confirm needed
  if(chatters.has(norm)){ actionFn(norm); return; }

  const match = findBestMatch(spoken);
  if(match){
    if(match.score===0){ actionFn(match.username); return; }
    log(`Fuzzy match: "${spoken}" → "${match.username}" (score ${match.score.toFixed(2)})`,'match');
    showConfirm(title, match.username, spoken, actionFn);
  } else {
    // No match in chatters — fall back to spoken word stitched together
    const fallback = norm || spoken.replace(/\s/g,'');
    log(`No chatter match for "${spoken}", using "${fallback}" directly`,'info');
    showConfirm(title, fallback, spoken, actionFn);
  }
}

// ── Chatters (Helix API) ───────────────────────────────────────────────────
async function refreshChatters(){
  if(!accessToken||!userId) return;
  try{
    let cursor='', all=[];
    do{
      const url=`https://api.twitch.tv/helix/chat/chatters?broadcaster_id=${userId}&moderator_id=${userId}&first=1000`+(cursor?`&after=${cursor}`:'');
      const res=await fetch(url,{headers:{'Authorization':`Bearer ${accessToken}`,'Client-Id':CLIENT_ID}});
      const data=await res.json();
      if(!data.data) break;
      all=all.concat(data.data.map(c=>c.user_login));
      cursor=data.pagination?.cursor||'';
    } while(cursor);

    chatters=new Set(all);
    document.getElementById('chatter-count').textContent=`${chatters.size} users`;
    const list=document.getElementById('chatters-list');
    if(chatters.size===0){ list.textContent='No active chatters found.'; return; }
    list.innerHTML=[...chatters].map(c=>`<span class="chatter-tag">${c}</span>`).join('');
    log(`Chatters refreshed: ${chatters.size} active`,'info');
  } catch(e){ log('Chatters fetch error: '+e.message,'err'); }
}

// ── OAuth ──────────────────────────────────────────────────────────────────
function startOAuth(){
  const state=Math.random().toString(36).slice(2);
  sessionStorage.setItem('oauth_state',state);
  window.location.href=`https://id.twitch.tv/oauth2/authorize?client_id=${CLIENT_ID}&redirect_uri=${encodeURIComponent(REDIRECT_URI)}&response_type=token&scope=${encodeURIComponent(SCOPES)}&state=${state}&force_verify=false`;
}
function parseOAuthCallback(){
  const hash=window.location.hash.substring(1);
  if(!hash) return;
  const params=new URLSearchParams(hash);
  const token=params.get('access_token');
  if(!token) return;
  history.replaceState(null,'',window.location.pathname);
  accessToken=token;
  sessionStorage.setItem('vc_token',token);
  fetchUserInfo();
}
function tryRestoreSession(){
  const saved=sessionStorage.getItem('vc_token');
  if(saved){accessToken=saved; fetchUserInfo();}
}
async function fetchUserInfo(){
  try{
    const res=await fetch('https://api.twitch.tv/helix/users',{headers:{'Authorization':`Bearer ${accessToken}`,'Client-Id':CLIENT_ID}});
    if(!res.ok){logout();return;}
    const data=await res.json();
    const user=data.data[0];
    userId=user.id; userLogin=user.login;
    document.getElementById('user-avatar').src=user.profile_image_url;
    document.getElementById('user-name').textContent=user.display_name;
    document.getElementById('auth-logged-out').style.display='none';
    document.getElementById('auth-logged-in').style.display='block';
    document.getElementById('listen-btn').disabled=false;
    setMic('','Logged in as '+user.display_name+' — connect chat to begin');
    log(`Logged in as ${user.display_name}`,'chat');
  } catch(e){log('User info error: '+e.message,'err');}
}
function logout(){
  accessToken=null; userId=null; userLogin=null;
  sessionStorage.removeItem('vc_token');
  document.getElementById('auth-logged-out').style.display='block';
  document.getElementById('auth-logged-in').style.display='none';
  document.getElementById('listen-btn').disabled=true;
  if(twitchSocket) twitchSocket.close();
  if(chattersRefreshTimer) clearInterval(chattersRefreshTimer);
  chatters=new Set();
  setMic('','Login with Twitch to begin');
  log('Logged out.','info');
}

// ── Twitch Chat IRC ────────────────────────────────────────────────────────
function connectChat(){
  if(!accessToken||!userLogin){log('Not logged in.','err');return;}
  if(twitchSocket) twitchSocket.close();
  twitchSocket=new WebSocket('wss://irc-ws.chat.twitch.tv:443');
  twitchSocket.onopen=()=>{
    twitchSocket.send('CAP REQ :twitch.tv/tags twitch.tv/commands');
    twitchSocket.send(`PASS oauth:${accessToken}`);
    twitchSocket.send(`NICK ${userLogin}`);
    twitchSocket.send(`JOIN #${userLogin}`);
  };
  twitchSocket.onmessage=e=>{
    if(e.data.includes('PING')){twitchSocket.send('PONG :tmi.twitch.tv');return;}
    // Track chatters from live messages
    const msgMatch=e.data.match(/display-name=([^;]+);/);
    if(msgMatch && e.data.includes('PRIVMSG')){
      chatters.add(msgMatch[1].toLowerCase());
      document.getElementById('chatter-count').textContent=`${chatters.size} users`;
    }
    if(e.data.includes('Welcome, GLHF!')||e.data.includes('001')){
      twitchConnected=true;
      document.getElementById('twitch-status-text').textContent='● Chat connected';
      document.getElementById('twitch-status-text').className='conn-status conn-ok';
      setMic('',`Ready — listening for commands in #${userLogin}`);
      log(`Chat connected to #${userLogin}`,'chat');
      // Initial chatter fetch + auto-refresh every 60s
      refreshChatters();
      if(chattersRefreshTimer) clearInterval(chattersRefreshTimer);
      chattersRefreshTimer=setInterval(refreshChatters,60000);
    }
    if(e.data.includes('Login authentication failed')){log('Chat auth failed.','err');logout();}
  };
  twitchSocket.onclose=()=>{
    twitchConnected=false;
    document.getElementById('twitch-status-text').textContent='● Chat disconnected';
    document.getElementById('twitch-status-text').className='conn-status conn-no';
    log('Chat disconnected.','info');
  };
}
function sendChat(msg){
  if(twitchSocket&&twitchSocket.readyState===WebSocket.OPEN){
    twitchSocket.send(`PRIVMSG #${userLogin} :${msg}`);
    log(`Chat → ${msg}`,'chat');
  } else log(`[No chat] ${msg}`,'info');
}

// ── Twitch Helix API ───────────────────────────────────────────────────────
async function twitchAPI(method,endpoint,body){
  if(!accessToken){log('Not authenticated.','err');return null;}
  try{
    const res=await fetch(`https://api.twitch.tv/helix/${endpoint}`,{
      method,
      headers:{'Authorization':`Bearer ${accessToken}`,'Client-Id':CLIENT_ID,'Content-Type':'application/json'},
      body:body?JSON.stringify(body):undefined
    });
    if(res.status===204) return {};
    const json=await res.json();
    if(!res.ok){log(`API error: ${json.message||res.status}`,'err');return null;}
    return json;
  } catch(e){log(`API error: ${e.message}`,'err');return null;}
}
async function resolveUserId(username){
  const data=await twitchAPI('GET',`users?login=${username}`);
  if(!data||!data.data||!data.data[0]){log(`User not found: ${username}`,'err');return null;}
  return data.data[0].id;
}

async function banUser(username){
  const uid=await resolveUserId(username); if(!uid) return;
  const r=await twitchAPI('POST',`moderation/bans?broadcaster_id=${userId}&moderator_id=${userId}`,{data:{user_id:uid,reason:'Banned via Voice Commander'}});
  if(r!==null){log(`Banned: ${username}`,'cmd');}
}
async function timeoutUser(username){
  const dur=parseInt(document.getElementById('timeout-dur').value)||600;
  const uid=await resolveUserId(username); if(!uid) return;
  const r=await twitchAPI('POST',`moderation/bans?broadcaster_id=${userId}&moderator_id=${userId}`,{data:{user_id:uid,duration:dur,reason:'Timed out via Voice Commander'}});
  if(r!==null) log(`Timeout ${dur}s: ${username}`,'cmd');
}
async function unbanUser(username){
  const uid=await resolveUserId(username); if(!uid) return;
  await twitchAPI('DELETE',`moderation/bans?broadcaster_id=${userId}&moderator_id=${userId}&user_id=${uid}`);
  log(`Unbanned: ${username}`,'cmd');
}
function shoutout(username){
  sendChat(`PogChamp Big shoutout to @${username}! Go give them a follow → twitch.tv/${username} 🔥`);
  log(`Shoutout: ${username}`,'cmd');
}
function raid(username){
  sendChat(`Chat, we're raiding @${username}! Let's go! 🔥`);
  log(`Raid call: ${username}`,'cmd');
}
function startPoll(question,options){
  if(options.length<2){log('Poll needs at least 2 options.','err');return;}
  sendChat(`📊 POLL: ${question} — `+options.map((o,i)=>`${i+1}) ${o}`).join(' | ')+' — Vote now!');
  log(`Poll: ${question}`,'cmd');
}

// ── OBS WebSocket v5 ───────────────────────────────────────────────────────
function connectOBS(){
  const url=document.getElementById('obs-url').value.trim();
  const pass=document.getElementById('obs-pass').value.trim();
  if(obsSocket) obsSocket.close();
  obsSocket=new WebSocket(url);
  obsSocket.onopen=()=>log('OBS connecting...','obs');
  obsSocket.onmessage=e=>{
    const msg=JSON.parse(e.data);
    if(msg.op===0){
      const auth={op:1,d:{rpcVersion:1}};
      if(pass&&msg.d.authentication) auth.d.authentication=pass;
      obsSocket.send(JSON.stringify(auth));
    }
    if(msg.op===2){
      obsConnected=true;
      document.getElementById('obs-status-text').textContent='● Connected';
      document.getElementById('obs-status-text').className='conn-status conn-ok';
      log('OBS connected!','obs');
      obsRequest('GetCurrentProgramScene').then(r=>{if(r&&r.sceneName){mainScene=r.sceneName;log(`Main scene: ${mainScene}`,'obs');}});
    }
    if(msg.op===7){
      const id=msg.d.requestId;
      if(obsPendingRequests[id]){obsPendingRequests[id](msg.d.responseData);delete obsPendingRequests[id];}
    }
  };
  obsSocket.onclose=()=>{
    obsConnected=false;
    document.getElementById('obs-status-text').textContent='● Disconnected';
    document.getElementById('obs-status-text').className='conn-status conn-no';
    log('OBS disconnected.','obs');
  };
  obsSocket.onerror=()=>log('OBS connection failed.','err');
}
function obsRequest(type,data={}){
  return new Promise(resolve=>{
    if(!obsSocket||obsSocket.readyState!==WebSocket.OPEN){resolve(null);return;}
    const id=String(obsMessageId++);
    obsPendingRequests[id]=resolve;
    obsSocket.send(JSON.stringify({op:6,d:{requestType:type,requestId:id,requestData:data}}));
    setTimeout(()=>{if(obsPendingRequests[id]){delete obsPendingRequests[id];resolve(null);}},3000);
  });
}
async function switchScene(sceneName){
  if(!obsConnected){log('OBS not connected.','err');return;}
  await obsRequest('SetCurrentProgramScene',{sceneName});
  log(`OBS → ${sceneName}`,'obs');
}

// ── Voice ──────────────────────────────────────────────────────────────────
function toggleListening(){isListening?stopListening():startListening();}
function startListening(){
  const SR=window.SpeechRecognition||window.webkitSpeechRecognition;
  if(!SR){log('Speech recognition not supported. Use Chrome or Edge.','err');return;}
  recognition=new SR();
  recognition.continuous=true; recognition.interimResults=true; recognition.lang='en-US';
  recognition.onstart=()=>{
    isListening=true;
    setMic('listening','Listening for commands...');
    document.getElementById('listen-btn').textContent='Stop Listening';
    document.getElementById('listen-btn').className='btn-red';
    log('Mic active.','info');
  };
  recognition.onresult=e=>{
    let interim='',final='';
    for(let i=e.resultIndex;i<e.results.length;i++){
      const t=e.results[i][0].transcript;
      if(e.results[i].isFinal) final+=t; else interim+=t;
    }
    document.getElementById('transcript').textContent=(final||interim)||'...';
    if(final) processCommand(final.trim().toLowerCase());
  };
  recognition.onerror=e=>{
    if(e.error==='not-allowed'){setMic('error','Mic access denied.');log('Mic denied.','err');}
    else if(e.error!=='no-speech') log(`Speech error: ${e.error}`,'err');
  };
  recognition.onend=()=>{if(isListening) recognition.start();};
  recognition.start();
}
function stopListening(){
  isListening=false; if(recognition) recognition.stop();
  setMic('','Stopped.');
  document.getElementById('listen-btn').textContent='Start Listening';
  document.getElementById('listen-btn').className='btn-purple';
  log('Mic stopped.','info');
}

// ── Command Parser ─────────────────────────────────────────────────────────
function processCommand(text){
  if(/\b(brb|be right back|taking a break)\b/.test(text)){
    switchScene(document.getElementById('brb-scene').value.trim()||'BRB');
    sendChat('Be right back! BibleThump');
    log('BRB','cmd'); return;
  }
  if(/\b(welcome back|i'?m back|im back|i am back)\b/.test(text)){
    if(mainScene) switchScene(mainScene);
    sendChat("We're back! Let's gooo 🔥");
    log('Back','cmd'); return;
  }

  // Extract command keyword and everything after it
  const cmdPatterns=[
    {re:/\bban\s+(.+)/,             title:'Ban user',     fn: u=>banUser(u)},
    {re:/\btimeout\s+(.+)/,         title:'Timeout user', fn: u=>timeoutUser(u)},
    {re:/\bunban\s+(.+)/,           title:'Unban user',   fn: u=>unbanUser(u)},
    {re:/\b(shoutout|shout out|so)\s+(.+)/, title:'Shoutout',   fn: u=>shoutout(u), grp:2},
    {re:/\braid\s+(.+)/,            title:'Raid',         fn: u=>raid(u)},
  ];

  for(const {re,title,fn,grp} of cmdPatterns){
    const m=text.match(re);
    if(m){
      const spoken=(m[grp||1]).trim();
      resolveWithConfirm(spoken, title, fn);
      return;
    }
  }

  const pollMatch=text.match(/\bpoll\s+(.+)/);
  if(pollMatch){
    const parts=pollMatch[1].split(/\s*,\s*/);
    if(parts.length>=3) startPoll(parts[0],parts.slice(1));
    else log('Poll format: "poll question, option1, option2"','err');
    return;
  }
}

// ── Init ───────────────────────────────────────────────────────────────────
parseOAuthCallback();
tryRestoreSession();
</script>
</body>
</html>
