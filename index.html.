  {key:'island',  label:'Dynamic Island',           color:'#7c5cff', icon:'<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.7" stroke-linecap="round"><rect x="3" y="8" width="18" height="7" rx="3.5"/><circle cx="8" cy="11.5" r="1.6"/><path d="M13 11.5h5"/></svg>'},
  {key:'ui',      label:'Taskbar & System UI',      color:'#22d3a6', icon:'<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.7" stroke-linecap="round"><rect x="3" y="4" width="18" height="12" rx="2"/><path d="M3 13h18"/><path d="M7 17.5h.01M10 17.5h.01M13 17.5h.01M16 17.5h.01"/><path d="M9 20.5h6"/></svg>'},
  {key:'theme',   label:'Themes & Wallpapers',      color:'#ff8a5c', icon:'<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.7" stroke-linecap="round"><circle cx="12" cy="12" r="8.5"/><circle cx="9" cy="9.5" r="1.3"/><circle cx="15" cy="9.5" r="1.3"/><circle cx="10" cy="15" r="1.3"/><circle cx="15" cy="14" r="1.3"/></svg>'},
  {key:'desktop', label:'Desktop Icons & Sounds',   color:'#4ea1ff', icon:'<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.7" stroke-linecap="round"><rect x="3" y="4" width="7" height="7" rx="1.5"/><rect x="14" y="4" width="7" height="7" rx="1.5"/><rect x="3" y="14" width="7" height="6" rx="1.5"/><path d="M14 14h4M14 17h7M14 20h3"/></svg>'}
  {key:'desktop', label:'Desktop Icons & Sounds',   color:'#4ea1ff', icon:'<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.7" stroke-linecap="round"><rect x="3" y="4" width="7" height="7" rx="1.5"/><rect x="14" y="4" width="7" height="7" rx="1.5"/><rect x="3" y="14" width="7" height="6" rx="1.5"/><path d="M14 14h4M14 17h7M14 20h3"/></svg>'},
  {key:'input',   label:'Cursors & Input',         color:'#ff6fb0', icon:'<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.7" stroke-linecap="round" stroke-linejoin="round"><path d="M6 3l12 8-5.2 1.2L16 19l-2.6 1.2-3.2-6.8L6 17z"/></svg>'}
];
const RISK = {
  safe:     {label:'Safe · no restart', cls:'safe'},
  explorer: {label:'Restarts Explorer', cls:'explorer'},
  overlay:  {label:'Overlay app',       cls:'overlay'}
  overlay:  {label:'Overlay app',       cls:'overlay'},
  runner:   {label:'Runs in background',cls:'overlay'}
};
function catOf(k){ return CATS.find(c => c.key === k); }

  tagline:'Switch Windows to the “No Sounds” scheme — no more dings and clicks.',
  desc:'Sets your per-user sound scheme to No Sounds and clears the current sound events, so notifications, errors and clicks stop making noise. Your previous scheme is backed up and restored by the undo script.',
  what:['System sounds, errors and clicks go silent','Notifications still show visually','Your previous sound scheme is backed up','Undo brings the sounds back']
},
{
  id:'cursor-black', cat:'input', risk:'safe', req:'Windows 10 & 11',
  name:'Black Cursor Scheme',
  tagline:'Switch to the built-in Windows Black cursors — sharp and easy to spot.',
  desc:'Reads the built-in “Windows Black” cursor scheme from your PC, writes it into your cursor settings and refreshes them instantly — no sign-out needed. The script only uses cursors that ship with Windows, then broadcasts the change so it takes effect immediately.',
  what:['Arrow, text, busy and resize cursors turn black','Applied instantly — no sign-out, no Explorer restart','Uses Windows\u2019 own built-in scheme files (nothing downloaded)','Undo restores your previous cursor set']
},
{
  id:'cursor-inverted', cat:'input', risk:'safe', req:'Windows 10 & 11',
  name:'Inverted Cursor Scheme',
  tagline:'High-contrast cursors that stay visible on any background.',
  desc:'Applies the built-in “Windows Inverted” scheme, which flips cursor colors against whatever is behind them — great for presentations and busy desktops. Same instant, no-restart mechanism as the black scheme.',
  what:['Cursors invert against light and dark backgrounds','Applied instantly — no sign-out needed','Falls back to the default scheme if it is missing on your PC','Undo restores your previous cursor set']
},
{
  id:'spotlight-wallpaper', cat:'theme', risk:'runner', req:'Windows 10 & 11 · needs internet',
  name:'Daily Spotlight Wallpaper',
  tagline:'A beautiful Bing photo on your desktop, refreshed automatically.',
  desc:'Downloads today\u2019s Bing daily photo, sets it as your wallpaper, then installs a tiny hidden watcher into your Startup folder that checks for a new photo every few hours. Your current wallpaper is saved first so the undo script can bring it back.',
  what:['Today\u2019s Bing photo becomes your wallpaper','A hidden background watcher refreshes it daily','Nothing to configure — it just keeps your desktop fresh','Undo stops the watcher and restores your old wallpaper']
},
{
  id:'auto-dark', cat:'theme', risk:'runner', req:'Windows 10 & 11',
  name:'Auto Dark Mode (scheduled)',
  tagline:'Light theme by day, dark by night — switched automatically.',
  desc:'Installs a tiny scheduler in your Startup folder that flips Windows between light and dark themes at fixed hours (dark from 19:00, light from 07:00 — both editable inside the generated script). It only switches when needed, then restarts Explorer to apply it.',
  what:['Dark mode automatically from 19:00 to 07:00','Light mode during the day','Hours are editable at the top of the generated scheduler','Undo stops the scheduler and restores your original theme']
},
{
  id:'opaque-windows', cat:'theme', risk:'explorer', req:'Windows 10 & 11',
  name:'Opaque Windows (no transparency)',
  tagline:'Disable acrylic and transparency for a solid, crisp look.',
  desc:'Turns off Windows transparency effects, so the taskbar, Start menu and app titlebars become solid instead of blurred. Nice on low-end GPUs and for people who prefer flat, readable surfaces.',
  what:['Taskbar and Start become fully opaque','Windows menus stop blurring what is behind them','Slightly lighter on the GPU','Undo brings transparency effects back']
},
{
  id:'taskbar-autohide', cat:'ui', risk:'explorer', req:'Windows 10 & 11',
  name:'Auto-Hide Taskbar',
  tagline:'Reclaim your screen — the taskbar tucks away until you hover.',
  desc:'Flips the auto-hide flag inside your taskbar settings (StuckRects3) and restarts Explorer. The whole screen becomes usable space; move your mouse to the bottom edge and the taskbar slides back out.',
  what:['Taskbar hides automatically, slides out on hover','Gives you back a strip of screen space','Your taskbar layout is backed up first','Undo restores the always-visible taskbar (sign out and back in if it flickers)']
},
{
  id:'show-hidden', cat:'ui', risk:'explorer', req:'Windows 10 & 11',
  name:'Show Hidden Files & Folders',
  tagline:'Make Explorer show the files Windows is hiding from you.',
  desc:'Sets Explorer\u2019s Hidden flag to “show hidden files, folders and drives”. Handy when hunting for leftover app data, license files or folder-level config that Windows keeps invisible.',
  what:['Hidden files and folders appear in Explorer','Look for faintly transparent icons in every folder','Undo hides them again','Files are never deleted — only visibility changes']
},
{
  id:'start-no-ads', cat:'ui', risk:'explorer', req:'Windows 10 & 11',
  name:'Turn Off Start Menu Suggestions',
  tagline:'No promoted apps, no suggested installs — a quieter Start menu.',
  desc:'Disables the Content Delivery Manager switches Windows uses to push suggested apps, inbox promotions and silent installs into Start. Six registry values, all backed up, all reverted by the undo script.',
  what:['Suggested apps disappear from Start','Silent app promotions are switched off','Backed up as one registry key','Undo re-enables Windows\u2019 suggestions']
},
{
  id:'snappy-menus', cat:'ui', risk:'explorer', req:'Windows 10 & 11',
  name:'Snappy Menus (0.05s delay)',
  tagline:'Right-click and start menus open instantly instead of after a pause.',
  desc:'Windows waits 400 ms before showing menus. This drops MenuShowDelay to 50 ms so context menus, the Start menu and dropdowns snap open the moment you click.',
  what:['Menus open about 8× faster','Notices instantly in right-click menus','Undo restores the default delay']
},
{
  id:'this-pc-desktop', cat:'desktop', risk:'explorer', req:'Windows 10 & 11',
  name:'Show “This PC” on the Desktop',
  tagline:'Put This PC and Network back where they used to be.',
  desc:'Writes the desktop-icon visibility values so This PC and Network appear on your desktop with their classic icons — one double-click away from drives and network shares.',
  what:['This PC icon appears on the desktop','Network icon comes back too','Works on Windows 10 and Windows 11','Undo hides them again']
}
];
/* ============================================================
    reg:[String.raw`HKCU\SOFTWARE\Policies\Microsoft\Windows\Explorer`],
    apply:[String.raw`reg add "HKCU\SOFTWARE\Policies\Microsoft\Windows\Explorer" /v DisableSearchBoxSuggestions /t REG_DWORD /d 1 /f | Out-Null`],
    undoFallback:[String.raw`reg delete "HKCU\SOFTWARE\Policies\Microsoft\Windows\Explorer" /v DisableSearchBoxSuggestions /f | Out-Null`],
    postUndo:[RAW`
$had = ''
if ($file -and (Test-Path $file)) { $had = Get-Content -Raw $file }
if (-not ($had -and ($had -match 'DisableSearchBoxSuggestions'))) {
  Remove-ItemProperty -Path 'HKCU:\SOFTWARE\Policies\Microsoft\Windows\Explorer' -Name DisableSearchBoxSuggestions -ErrorAction SilentlyContinue
}`],
    restart:true
  },
  'dark-mode': {

SCRIPTS['island-battery'] = {customApply: islandApply, customUndo: islandUndo};
SCRIPTS['island-compact'] = {customApply: islandApply, customUndo: islandUndo};

/* ============================================================
   New customization payloads (batch 2)
   ============================================================ */
const GUID_THISPC = '{20D04FE0-3AEA-1069-A2D8-08002B30309D}';
const GUID_NET    = '{F02C1A0D-BE21-4350-88B0-7367FC96EF3C}';
const HDI = RAW`HKCU\Software\Microsoft\Windows\CurrentVersion\Explorer\HideDesktopIcons`;
const CDM = RAW`HKCU\Software\Microsoft\Windows\CurrentVersion\ContentDeliveryManager`;

/* applies a built-in Windows cursor scheme (name is regex-matched) */
function cursorSchemeBody(prefer){
  return RAW`
$schemes = Get-Item 'HKCU:\Control Panel\Cursors\Schemes'
$names = @($schemes.GetValueNames())
if ($names.Count -eq 0) { throw 'No built-in cursor schemes were found on this PC.' }
$pick = $names | Where-Object { $_ -match '` + prefer + RAW`' } | Select-Object -First 1
if (-not $pick) { $pick = $names | Where-Object { $_ -like '*Windows*' } | Select-Object -First 1 }
if (-not $pick) { $pick = $names[0] }
$parts = @()
foreach ($row in @($schemes.GetValue($pick))) {
  foreach ($piece in ($row -split ';')) {
    $p = $piece.Trim()
    if ($p) { $parts += $p }
  }
}
if ($parts.Count -eq 0) { throw ('Scheme ' + $pick + ' contains no cursor paths.') }
$order = @('Arrow','Help','AppStarting','Wait','Cross','IBeam','Pen','No','SizeNS','SizeWE','SizeNWSE','SizeNESW','SizeAll','UpArrow','Hand','Pin')
for ($i = 0; $i -lt $parts.Count -and $i -lt $order.Length; $i++) {
  New-ItemProperty -Path 'HKCU:\Control Panel\Cursors' -Name $order[$i] -Value $parts[$i] -PropertyType String -Force | Out-Null
}
Set-Item -Path 'HKCU:\Control Panel\Cursors' -Value $pick
Add-Type -Namespace Win32 -Name ChipCur -MemberDefinition '[DllImport("user32.dll")] public static extern bool SystemParametersInfo(int uAction, int uParam, IntPtr lpvWinIni, int fuWinIni);'
[Win32.ChipCur]::SystemParametersInfo(21, 0, [IntPtr]::Zero, 3) | Out-Null`;
}
const CURSOR_VALUES = "@('Arrow','Help','AppStarting','Wait','Cross','IBeam','Pen','No','SizeNS','SizeWE','SizeNWSE','SizeNESW','SizeAll','UpArrow','Hand','Pin')";
const CURSOR_REFRESH = RAW`
$had = ''
if ($file -and (Test-Path $file)) { $had = Get-Content -Raw $file }
foreach ($n in ` + CURSOR_VALUES + RAW`) {
  if (-not ($had -and ($had -match [regex]::Escape($n)))) {
    Remove-ItemProperty -Path 'HKCU:\Control Panel\Cursors' -Name $n -ErrorAction SilentlyContinue
  }
}
Add-Type -Namespace Win32 -Name ChipCurUndo -MemberDefinition '[DllImport("user32.dll")] public static extern bool SystemParametersInfo(int uAction, int uParam, IntPtr lpvWinIni, int fuWinIni);'
[Win32.ChipCurUndo]::SystemParametersInfo(21, 0, [IntPtr]::Zero, 3) | Out-Null`;

SCRIPTS['cursor-black'] = {
  reg:[RAW`HKCU\Control Panel\Cursors`],
  apply:[cursorSchemeBody('Black')],
  restart:false,
  postUndo:[CURSOR_REFRESH]
};
SCRIPTS['cursor-inverted'] = {
  reg:[RAW`HKCU\Control Panel\Cursors`],
  apply:[cursorSchemeBody('Inverted')],
  restart:false,
  postUndo:[CURSOR_REFRESH]
};
SCRIPTS['opaque-windows'] = {
  reg:[RAW`HKCU\SOFTWARE\Microsoft\Windows\DWM`],
  apply:[
    String.raw`reg add "HKCU\SOFTWARE\Microsoft\Windows\DWM" /v EnableTransparency /t REG_DWORD /d 0 /f | Out-Null`,
    'Stop-Process -Name dwm -Force -ErrorAction SilentlyContinue'
  ],
  postUndo:['Stop-Process -Name dwm -Force -ErrorAction SilentlyContinue'],
  restart:true
};
SCRIPTS['taskbar-autohide'] = {
  reg:[String.raw`HKCU\Software\Microsoft\Windows\CurrentVersion\Explorer\StuckRects3`],
  apply:[RAW`
$srKey = 'HKCU:\Software\Microsoft\Windows\CurrentVersion\Explorer\StuckRects3'
$settings = (Get-ItemProperty -Path $srKey -Name Settings).Settings
if (-not $settings -or $settings.Length -lt 9) { throw 'Could not read the taskbar settings.' }
$settings[8] = 2
New-ItemProperty -Path $srKey -Name Settings -Value ([byte[]]$settings) -PropertyType Binary -Force | Out-Null`],
  restart:true
};
SCRIPTS['show-hidden'] = {
  reg:[ADV],
  apply:[ADV_ADD + '/v Hidden /t REG_DWORD /d 1 /f | Out-Null'],
  restart:true
};
SCRIPTS['start-no-ads'] = {
  reg:[CDM],
  apply:[
    'SystemPaneSuggestionsEnabled','SilentInstalledAppsEnabled',
    'SubscribedContent-338387Enabled','SubscribedContent-338388Enabled',
    'SubscribedContent-338389Enabled','SubscribedContent-353694Enabled',
    'SubscribedContent-353696Enabled'
  ].map(v => 'reg add "' + CDM + '" /v ' + v + ' /t REG_DWORD /d 0 /f | Out-Null'),
  postUndo:[RAW`
$had = ''
if ($file -and (Test-Path $file)) { $had = Get-Content -Raw $file }
foreach ($v in @('SystemPaneSuggestionsEnabled','SilentInstalledAppsEnabled','SubscribedContent-338387Enabled','SubscribedContent-338388Enabled','SubscribedContent-338389Enabled','SubscribedContent-353694Enabled','SubscribedContent-353696Enabled')) {
  if (-not ($had -and ($had -match [regex]::Escape($v)))) {
    Remove-ItemProperty -Path 'HKCU:\Software\Microsoft\Windows\CurrentVersion\ContentDeliveryManager' -Name $v -ErrorAction SilentlyContinue
  }
}`],
  restart:true
};
SCRIPTS['snappy-menus'] = {
  reg:[RAW`HKCU\Control Panel\Desktop`],
  apply:[String.raw`reg add "HKCU\Control Panel\Desktop" /v MenuShowDelay /t REG_SZ /d 50 /f | Out-Null`],
  restart:true
};
SCRIPTS['this-pc-desktop'] = {
  reg:[HDI],
  apply:[
    'reg add "' + HDI + '" /f | Out-Null',
    'reg add "' + HDI + '\\NewStartPanel" /f | Out-Null',
    'reg add "' + HDI + '\\ClassicStartMenu" /f | Out-Null',
    'reg add "' + HDI + '\\NewStartPanel" /v "' + GUID_THISPC + '" /t REG_DWORD /d 0 /f | Out-Null',
    'reg add "' + HDI + '\\NewStartPanel" /v "' + GUID_NET + '" /t REG_DWORD /d 0 /f | Out-Null',
    'reg add "' + HDI + '\\ClassicStartMenu" /v "' + GUID_THISPC + '" /t REG_DWORD /d 0 /f | Out-Null',
    'reg add "' + HDI + '\\ClassicStartMenu" /v "' + GUID_NET + '" /t REG_DWORD /d 0 /f | Out-Null'
  ],
  postUndo:[RAW`
$had = ''
if ($file -and (Test-Path $file)) { $had = Get-Content -Raw $file }
foreach ($g in @('` + GUID_THISPC + RAW`', '` + GUID_NET + RAW`')) {
  if (-not ($had -and ($had -match [regex]::Escape($g)))) {
    foreach ($k in @('HKCU:\Software\Microsoft\Windows\CurrentVersion\Explorer\HideDesktopIcons\NewStartPanel','HKCU:\Software\Microsoft\Windows\CurrentVersion\Explorer\HideDesktopIcons\ClassicStartMenu')) {
      Remove-ItemProperty -Path $k -Name $g -ErrorAction SilentlyContinue
    }
  }
}`],
  restart:true
};
/* ============================================================
   Background runners: Spotlight wallpaper + scheduled auto dark mode
   ============================================================ */
function psRunnerHeader(m, kind, blurb){
  const c = catOf(m.cat);
  return [
    '# =================================================================',
    '#  GEN-CHIP  -  ' + (kind === 'undo' ? 'undo script' : 'apply script'),
    '#  ' + m.name,
    '#  ' + m.tagline,
    '#  Category: ' + c.label + '   |   Risk: runs quietly in the background',
    '#',
  ].concat(blurb.map(l => '#  ' + l)).concat([
    '#',
    '#  Undo: run genchip-undo-' + m.id + '.ps1',
    '# =================================================================',
    '',
    "$ErrorActionPreference = 'Stop'",
    ''
  ]).join('\n');
}

const SPOTLIGHT_WATCHER = [
  "Add-Type -Namespace Win32 -Name ChipSpot -MemberDefinition '[DllImport(\"user32.dll\", CharSet = CharSet.Auto)] public static extern bool SystemParametersInfo(int uAction, int uParam, string lpvWinIni, int fuWinIni);'",
  "$dir = $PSScriptRoot",
  "if (-not $dir) { $dir = Split-Path -Parent $MyInvocation.MyCommand.Path }",
  "$stateFile = Join-Path $dir 'last.txt'",
  "$dest = Join-Path $dir 'today.jpg'",
  'function Save-Photo {',
  '  try {',
  "    $json = (Invoke-WebRequest -UseBasicParsing -Uri 'https://www.bing.com/HPImageArchive.aspx?format=js&idx=0&n=1' -TimeoutSec 20).Content | ConvertFrom-Json",
  '    if (-not $json -or -not $json.images -or $json.images.Count -eq 0) { return }',
  "    $url = 'https://www.bing.com' + $json.images[0].urlbase + '_1920x1080.jpg'",
  '    Invoke-WebRequest -UseBasicParsing -Uri $url -OutFile $dest -TimeoutSec 40',
  '    if (Test-Path $dest) {',
  RAW`      Set-ItemProperty -Path 'HKCU:\Control Panel\Desktop' -Name WallPaper -Value $dest`,
  '      [Win32.ChipSpot]::SystemParametersInfo(20, 0, $dest, 3) | Out-Null',
  "      Set-Content -Path $stateFile -Value ((Get-Date).Date.ToString('yyyyMMdd'))",
  '    }',
  '  } catch { }',
  '}',
  "Set-Content -Path (Join-Path $dir 'watcher.pid') -Value $PID",
  'Save-Photo',
  'while ($true) {',
  '  Start-Sleep -Seconds 21600',
  "  $today = (Get-Date).Date.ToString('yyyyMMdd')",
  "  $last = ''",
  '  if (Test-Path $stateFile) { $last = (Get-Content $stateFile -Raw).Trim() }',
  '  if ($last -ne $today) { Save-Photo }',
  '}'
];

function spotlightApply(m){
  const L = [psRunnerHeader(m, 'apply', [
    "Downloads today's Bing photo, saves it as your wallpaper, then installs",
    'a tiny hidden watcher into your Startup folder that keeps it fresh.',
    'Your current wallpaper setting is backed up first so undo can restore it.'
  ])];
  L.push(
    "$workDir = Join-Path (Join-Path $env:LOCALAPPDATA 'GEN-CHIP') 'spotlight'",
    "$backupDir = Join-Path (Join-Path $env:LOCALAPPDATA 'GEN-CHIP') 'backups'",
    'New-Item -ItemType Directory -Force -Path $workDir | Out-Null',
    'New-Item -ItemType Directory -Force -Path $backupDir | Out-Null',
    '',
    '# --- stop an older watcher',
    "$pidFile = Join-Path $workDir 'watcher.pid'",
    'if (Test-Path $pidFile) {',
    '  $prev = 0',
    '  $raw = Get-Content $pidFile -Raw -ErrorAction SilentlyContinue',
    '  if ($raw -and [int]::TryParse($raw.Trim(), [ref]$prev)) { Stop-Process -Id $prev -Force -ErrorAction SilentlyContinue }',
    '}',
    '',
    '# --- back up the current wallpaper settings'
  );
  L.push(RAW`if (Test-Path 'Registry::HKCU\Control Panel\Desktop') { reg export 'HKCU\Control Panel\Desktop' (Join-Path $backupDir 'genchip-spotlight-wallpaper-1.reg') /y | Out-Null }`);
  L.push(
    '',
    '# --- the watcher itself (runs hidden, checks for a new photo every 6 hours)',
    "$watcherSrc = @'"
  );
  SPOTLIGHT_WATCHER.forEach(l => L.push(l));
  L.push(
    "'@",
    "$watcherPath = Join-Path $workDir 'watcher.ps1'",
    'Set-Content -Path $watcherPath -Value $watcherSrc',
    '',
    '# --- start it now',
    "$launch = '-NoProfile -ExecutionPolicy Bypass -WindowStyle Hidden -File \"' + $watcherPath + '\"'",
    'Start-Process powershell -ArgumentList $launch',
    '',
    '# --- and start it again at every sign-in',
    "$startupDir = [Environment]::GetFolderPath('Startup')",
    "$cmdPath = Join-Path $startupDir 'GEN-CHIP Spotlight.cmd'",
    "$line = 'powershell -NoProfile -WindowStyle Hidden -File \"' + $watcherPath + '\"'",
    'Set-Content -Path $cmdPath -Value $line -Encoding ASCII',
    ''
  );
  Array.prototype.push.apply(L, psFinish(m, 'Applied'));
  return L.join('\n');
}

function spotlightUndo(m){
  const L = [psRunnerHeader(m, 'undo', [
    'Stops the wallpaper watcher, removes it from Windows startup and',
    'restores the wallpaper you had before installing this customization.'
  ])];
  L.push(
    "$workDir = Join-Path (Join-Path $env:LOCALAPPDATA 'GEN-CHIP') 'spotlight'",
    "$backupDir = Join-Path (Join-Path $env:LOCALAPPDATA 'GEN-CHIP') 'backups'",
    '',
    '# --- stop the watcher',
    "$pidFile = Join-Path $workDir 'watcher.pid'",
    'if (Test-Path $pidFile) {',
    '  $prev = 0',
    '  $raw = Get-Content $pidFile -Raw -ErrorAction SilentlyContinue',
    '  if ($raw -and [int]::TryParse($raw.Trim(), [ref]$prev)) { Stop-Process -Id $prev -Force -ErrorAction SilentlyContinue }',
    '  Remove-Item $pidFile -Force -ErrorAction SilentlyContinue',
    '}',
    '',
    '# --- remove the Startup entry',
    "$startupDir = [Environment]::GetFolderPath('Startup')",
    "Remove-Item (Join-Path $startupDir 'GEN-CHIP Spotlight.cmd') -Force -ErrorAction SilentlyContinue",
    ''
  );
  L.push(RAW`$bk = Join-Path $backupDir 'genchip-spotlight-wallpaper-1.reg'`);
  L.push('if (Test-Path $bk) { reg import $bk | Out-Null }', '');
  L.push(RAW`
Add-Type -Namespace Win32 -Name ChipSpotUndo -MemberDefinition '[DllImport("user32.dll", CharSet = CharSet.Auto)] public static extern bool SystemParametersInfo(int uAction, int uParam, string lpvWinIni, int fuWinIni);'
$wp = (Get-ItemProperty -Path 'HKCU:\Control Panel\Desktop').WallPaper
if ($wp -and (Test-Path -LiteralPath $wp)) { [Win32.ChipSpotUndo]::SystemParametersInfo(20, 0, $wp, 3) | Out-Null }`);
  L.push(
    '',
    'Remove-Item $workDir -Recurse -Force -ErrorAction SilentlyContinue',
    '',
    "Write-Host ''",
    "Write-Host 'Wallpaper watcher stopped - your previous wallpaper is back.' -ForegroundColor Green",
    "Write-Host 'Run the apply script any time to switch it on again.' -ForegroundColor DarkGray",
    "Write-Host ''",
    "Read-Host 'Press Enter to close'",
    ''
  );
  return L.join('\n');
}

const AUTO_DARK_WATCHER = [
  "$lightHour = 7      # hour to switch back to the light theme",
  "$darkHour = 19      # hour to switch to the dark theme",
  RAW`$key = 'HKCU:\Software\Microsoft\Windows\CurrentVersion\Themes\Personalize'`,
  'function Set-Theme([bool]$dark) {',
  '  $v = 1',
  '  if ($dark) { $v = 0 }',
  '  New-ItemProperty -Path $key -Name AppsUseLightTheme -Value $v -PropertyType DWord -Force | Out-Null',
  '  New-ItemProperty -Path $key -Name SystemUsesLightTheme -Value $v -PropertyType DWord -Force | Out-Null',
  '  Stop-Process -Name explorer -Force -ErrorAction SilentlyContinue',
  '  Start-Sleep -Seconds 1',
  '  if (-not (Get-Process explorer -ErrorAction SilentlyContinue)) { Start-Process explorer }',
  '}',
  "Set-Content -Path (Join-Path $PSScriptRoot 'scheduler.pid') -Value $PID",
  "$last = ''",
  'while ($true) {',
  '  $h = (Get-Date).Hour',
  '  $isDark = (($h -ge $darkHour) -or ($h -lt $lightHour))',
  "  $flag = 'light'",
  "  if ($isDark) { $flag = 'dark' }",
  '  if ($flag -ne $last) { Set-Theme $isDark; $last = $flag }',
  '  Start-Sleep -Seconds 60',
  '}'
];

function autoDarkApply(m){
  const L = [psRunnerHeader(m, 'apply', [
    'Installs a tiny scheduler in your Startup folder that flips Windows',
    'between light and dark themes at fixed hours. Edit $lightHour and',
    '$darkHour at the top of the generated scheduler to change the times.'
  ])];
  L.push(
    "$workDir = Join-Path (Join-Path $env:LOCALAPPDATA 'GEN-CHIP') 'auto-dark'",
    "$backupDir = Join-Path (Join-Path $env:LOCALAPPDATA 'GEN-CHIP') 'backups'",
    'New-Item -ItemType Directory -Force -Path $workDir | Out-Null',
    'New-Item -ItemType Directory -Force -Path $backupDir | Out-Null',
    '',
    '# --- stop an older scheduler',
    "$pidFile = Join-Path $workDir 'scheduler.pid'",
    'if (Test-Path $pidFile) {',
    '  $prev = 0',
    '  $raw = Get-Content $pidFile -Raw -ErrorAction SilentlyContinue',
    '  if ($raw -and [int]::TryParse($raw.Trim(), [ref]$prev)) { Stop-Process -Id $prev -Force -ErrorAction SilentlyContinue }',
    '}',
    '',
    '# --- back up the current theme settings'
  );
  L.push(RAW`if (Test-Path 'Registry::HKCU\Software\Microsoft\Windows\CurrentVersion\Themes\Personalize') { reg export 'HKCU\Software\Microsoft\Windows\CurrentVersion\Themes\Personalize' (Join-Path $backupDir 'genchip-auto-dark-1.reg') /y | Out-Null }`);
  L.push('', '# --- the scheduler (runs hidden, checks the clock every minute)', "$watcherSrc = @'");
  AUTO_DARK_WATCHER.forEach(l => L.push(l));
  L.push(
    "'@",
    "$watcherPath = Join-Path $workDir 'scheduler.ps1'",
    'Set-Content -Path $watcherPath -Value $watcherSrc',
    '',
    '# --- start it now',
    "$launch = '-NoProfile -ExecutionPolicy Bypass -WindowStyle Hidden -File \"' + $watcherPath + '\"'",
    'Start-Process powershell -ArgumentList $launch',
    '',
    '# --- and start it again at every sign-in',
    "$startupDir = [Environment]::GetFolderPath('Startup')",
    "$cmdPath = Join-Path $startupDir 'GEN-CHIP Auto Dark.cmd'",
    "$line = 'powershell -NoProfile -WindowStyle Hidden -File \"' + $watcherPath + '\"'",
    'Set-Content -Path $cmdPath -Value $line -Encoding ASCII',
    ''
  );
  Array.prototype.push.apply(L, psFinish(m, 'Applied'));
  return L.join('\n');
}

function autoDarkUndo(m){
  const L = [psRunnerHeader(m, 'undo', [
    'Stops the scheduler, removes it from Windows startup and restores',
    'the theme settings you had before installing this customization.'
  ])];
  L.push(
    "$workDir = Join-Path (Join-Path $env:LOCALAPPDATA 'GEN-CHIP') 'auto-dark'",
    "$backupDir = Join-Path (Join-Path $env:LOCALAPPDATA 'GEN-CHIP') 'backups'",
    '',
    '# --- stop the scheduler',
    "$pidFile = Join-Path $workDir 'scheduler.pid'",
    'if (Test-Path $pidFile) {',
    '  $prev = 0',
    '  $raw = Get-Content $pidFile -Raw -ErrorAction SilentlyContinue',
    '  if ($raw -and [int]::TryParse($raw.Trim(), [ref]$prev)) { Stop-Process -Id $prev -Force -ErrorAction SilentlyContinue }',
    '  Remove-Item $pidFile -Force -ErrorAction SilentlyContinue',
    '}',
    '',
    '# --- remove the Startup entry',
    "$startupDir = [Environment]::GetFolderPath('Startup')",
    "Remove-Item (Join-Path $startupDir 'GEN-CHIP Auto Dark.cmd') -Force -ErrorAction SilentlyContinue",
    '',
    '# --- restore the previous theme',
    "$bk = Join-Path $backupDir 'genchip-auto-dark-1.reg'",
    'if (Test-Path $bk) { reg import $bk | Out-Null }',
    'Stop-Process -Name explorer -Force -ErrorAction SilentlyContinue',
    'Start-Sleep -Seconds 1',
    'if (-not (Get-Process explorer -ErrorAction SilentlyContinue)) { Start-Process explorer }',
    'Remove-Item $workDir -Recurse -Force -ErrorAction SilentlyContinue',
    '',
    "Write-Host ''",
    "Write-Host 'Scheduler stopped - automatic theme switching is off.' -ForegroundColor Green",
    "Write-Host 'Your previous theme settings were restored.' -ForegroundColor DarkGray",
    "Write-Host ''",
    "Read-Host 'Press Enter to close'",
    ''
  );
  return L.join('\n');
}

SCRIPTS['spotlight-wallpaper'] = {customApply: spotlightApply, customUndo: spotlightUndo};
SCRIPTS['auto-dark'] = {customApply: autoDarkApply, customUndo: autoDarkUndo};

/* ============================================================
   UI
   ============================================================ */
const state = {cat:'all', q:'', installed:{}};
