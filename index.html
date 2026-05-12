<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover" />
  <meta name="apple-mobile-web-app-capable" content="yes" />
  <meta name="apple-mobile-web-app-status-bar-style" content="black-translucent" />
  <meta name="apple-mobile-web-app-title" content="Trader Journal" />
  <meta name="theme-color" content="#0A0A0A" />
  <title>Trader Journal</title>
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;500;600;700&family=Sora:wght@300;400;500;600;700&display=swap" rel="stylesheet" />
  <style>
    * { box-sizing: border-box; margin: 0; padding: 0; }
    html, body, #root { height: 100%; background: #0A0A0A; }
    body { font-family: 'Sora', sans-serif; color: #F9FAFB; overscroll-behavior: none; }
    :root { color-scheme: dark; }
    ::-webkit-scrollbar { width: 4px; }
    ::-webkit-scrollbar-track { background: transparent; }
    ::-webkit-scrollbar-thumb { background: #2A2A2A; border-radius: 2px; }
    input, textarea, select { outline: none; font-family: inherit; }
    button { cursor: pointer; font-family: inherit; border: none; background: none; }
    * { -webkit-tap-highlight-color: transparent; user-select: none; }
    input, textarea { user-select: text; }
  </style>
</head>
<body>
  <div id="root"></div>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/react/18.2.0/umd/react.production.min.js"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/react-dom/18.2.0/umd/react-dom.production.min.js"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/babel-standalone/7.23.2/babel.min.js"></script>
  <script type="text/babel">
    const { useState, useEffect, useMemo, useCallback, createContext, useContext } = React;

    const C = {
      bg:"#0A0A0A",bg2:"#111111",bg3:"#1A1A1A",
      border:"#2A2A2A",tint:"#00C896",tintDim:"#00C89620",
      profit:"#00C896",loss:"#FF4D4D",lossDim:"#FF4D4D20",
      warning:"#FFB830",text:"#F9FAFB",text2:"#9CA3AF",text3:"#6B7280",
    };

    // ── i18n ─────────────────────────────────────────────────────────────────
    const LANG_KEY = "tj_lang";
    const T = {
      ru: {
        home:"Главная",journal:"Журнал",calc:"Калькулятор",stats:"Статистика",settings:"Настройки",
        totalR:"Итого R",trades:"сделок",openPos:"открытых позиций",
        equityCurve:"Кривая капитала (R)",tradeClasses:"Классы сделок",
        recentTrades:"Последние сделки",allTrades:"Все",
        emptyTitle:"Начни дневник",emptyDesc:"Записывай сделки по шаблону: сценарий, психология, результат",
        addTrade:"Добавить сделку",
        searchPh:"Поиск по инструменту...",
        all:"Все",open:"Открытые",closed:"Закрытые",
        noTrades:"Нет сделок",noResults:"Нет результатов",
        noTradesHint:"Нажмите + чтобы записать первую сделку",noResultsHint:"Измените фильтр",
        calcTitle:"Калькулятор",posSizeTitle:"Размер позиции",
        instrument:"Инструмент",direction:"Направление",
        longBtn:"↑ Long",shortBtn:"↓ Short",
        balance:"Баланс",riskPct:"Риск %",leverage:"Кредитное плечо",
        quickBal:"Быстрый баланс",riskLevel:"Уровень риска",riskAmt:"Сумма риска",
        entryPrice:"Цена входа",stopLoss:"Стоп Лосс",takeProfit:"Тейк Профит",
        priceM:"Цена",pipsM:"Пипсы",rrM:"R:R",
        slWarn:"⚠ SL не соответствует направлению",
        resultTitle:"Результат",lotSize:"Размер позиции",units:"Единиц",
        riskUSD:"Риск ($)",slPips:"SL пипсов",margin:"Маржа",potProfit:"Потенциал прибыли",
        openInJournal:"📋 Открыть сделку в журнале",calcHint:"Введите цену входа и стоп лосс",
        newTrade:"Новая сделка",save:"Сохранить",prefillBanner:"Данные из калькулятора",
        sec1:"Общие данные",sec2:"Главный сценарий",sec3:"Альтернативный сценарий",
        sec4:"План сделки",sec5:"Психология до входа",
        instrLabel:"Инструмент *",instrPh:"EURUSD, BTC, NASDAQ…",
        htf:"HTF",ltf:"LTF",sessions:"Сессии",
        mktType:"Тип рынка",trend:"Тренд",correction:"Коррекция",range:"Диапазон",
        vol:"Волатильность",low:"Низкая",medium:"Средняя",high:"Высокая",
        structure:"Текущая структура",structPh:"Импульс 1–2 сформирован",
        devWave:"Развивающаяся волна",devWavePh:"3 of 3, волна C…",
        structStart:"Начало структуры",fibTarget:"Цель по Fib",fibPh:"1.618",
        scenLogic:"Логика сценария",scenPh:"2–3 предложения…",
        invalidation:"Уровень инвалидации",
        altMarkup:"Альтернативная разметка",altPh:"Сложная коррекция ABC…",
        altProb:"Вероятность (%)",altBias:"Смена bias при",altConfirm:"Что подтвердит альтернативу",
        entryType:"Тип входа (волна)",impulse:"ИМПУЛЬС",corrLabel:"КОРРЕКЦИЯ",
        entryPoint:"Точка входа",plannedRR:"Плановый R:R",
        riskPctL:"Риск %",posSizeL:"Размер позиции",
        cancelCond:"Условия отмены",cancelPh:"Если цена…",
        energy:"Энергия",focus:"Фокус",calm:"Спокойствие",pressure:"Давление результата",
        lossStreak:"Серия убытков",no:"Нет",yes:"Да",
        biases:"Искажения",fomo:"FOMO",
        biasConf:"Подтверждающее искажение",biasRev:"Желание отыграться",biasOver:"Переуверенность",
        readyQ:"Я готов принять стоп, если сценарий сломается?",
        del:"Удалить",reopen:"Переоткрыть сделку",
        closeTrade:"Закрыть сделку",tradeRes:"Результат сделки",
        resR:"Результат R *",resUSD:"Результат USD",maeL:"MAE (R)",mfeL:"MFE (R)",
        tradeClass:"Класс сделки",errType:"Тип ошибки",
        errNone:"Нет",errAn:"Анализ",errEx:"Исполнение",
        wouldRep:"Повторил бы?",conclusion:"Главный вывод",conclusionPh:"Что узнал из этой сделки…",
        cancel:"Отмена",saveBtn:"Сохранить",
        timeframes:"Таймфреймы",mainScen:"Главный сценарий",tradePlan:"План сделки",conclusionT:"Вывод",logic:"Логика",
        statsTitle:"Статистика",overallStats:"Общая статистика",totalTrades:"Всего сделок",
        avgWin:"Avg Win",avgLoss:"Avg Loss",bestTrade:"Best Trade",worstTrade:"Worst Trade",
        byMonth:"По месяцам",byInstr:"По инструментам",noStatsHint:"Нет закрытых сделок для статистики",
        settingsTitle:"Настройки",langSection:"Язык / Language",
        exportSection:"Экспорт",importSection:"Импорт",dangerSection:"Опасная зона",
        currentJournal:"Текущий журнал",formatLabel:"Формат",
        jsonSub:"Полный бэкап",csvSub:"Excel / Sheets",
        copyBtn:"📋 Скопировать",copiedToast:"Скопировано в буфер!",copyErr:"Ошибка копирования",
        iosTitle:"Как сохранить на iPhone:",
        iosS1:"Нажмите «Скопировать» выше",iosS2:"Откройте приложение «Заметки»",
        iosS3:"Создайте новую заметку → вставьте (удержите → Вставить)",
        iosS4:"При импорте — скопируйте текст заметки и вставьте в поле ниже",
        dlBtn:"⬇️ Скачать",
        importDesc:"Загрузите JSON-файл или вставьте его содержимое вручную.",
        importMode:"Режим импорта",merge:"Объединить",replace:"Заменить всё",
        mergeHint:"Добавит новые сделки, существующие не тронет",
        replaceHint:"⚠️ Удалит все текущие сделки и заменит импортированными",
        chooseFile:"📂 Выбрать JSON файл",pasteLabel:"или вставить JSON вручную",
        importReady:"✓ Данные готовы к импорту",
        importBtn:"⬆️ Импортировать",replaceBtn:"⚠️ Заменить и импортировать",
        noDataToast:"Вставьте JSON или выберите файл",noTradesInFile:"Нет сделок в файле",parseErr:"Ошибка парсинга JSON",
        clearAll:"🗑 Очистить все данные",clearDesc:"Полная очистка журнала. Действие необратимо.",
        clearConfirm:(n)=>`Удалить все ${n} сделок? Это действие нельзя отменить.`,
        exportedToast:(n)=>`Экспортировано ${n} сделок`,csvToast:(n)=>`CSV экспортирован (${n} строк)`,
        delTradeConfirm:"Удалить сделку?",instrReq:"Укажите инструмент",resReq:"Укажите результат R",
        sAsia:"Азия",sLondon:"Лондон",sNY:"Нью-Йорк",sLonNY:"Лондон/НЙ",sLonAsia:"Лондон/Азия",
        pip:"Пип",typeL:"Тип",pipPerLot:"Пип/$лот",pipsLabel:"пипс",wW:"П",wL:"У",
        viewModeTitle:"Версия приложения",mobileView:"Мобильная (iOS)",webView:"Веб (ПК)",
      },
      en: {
        home:"Home",journal:"Journal",calc:"Calculator",stats:"Statistics",settings:"Settings",
        totalR:"Total R",trades:"trades",openPos:"open positions",
        equityCurve:"Equity Curve (R)",tradeClasses:"Trade Classes",
        recentTrades:"Recent Trades",allTrades:"All",
        emptyTitle:"Start your journal",emptyDesc:"Log trades: scenario, psychology, result",
        addTrade:"Add Trade",
        searchPh:"Search by instrument...",
        all:"All",open:"Open",closed:"Closed",
        noTrades:"No trades",noResults:"No results",
        noTradesHint:"Tap + to log your first trade",noResultsHint:"Change the filter",
        calcTitle:"Calculator",posSizeTitle:"Position Size",
        instrument:"Instrument",direction:"Direction",
        longBtn:"↑ Long",shortBtn:"↓ Short",
        balance:"Balance",riskPct:"Risk %",leverage:"Leverage",
        quickBal:"Quick Balance",riskLevel:"Risk Level",riskAmt:"Risk Amount",
        entryPrice:"Entry Price",stopLoss:"Stop Loss",takeProfit:"Take Profit",
        priceM:"Price",pipsM:"Pips",rrM:"R:R",
        slWarn:"⚠ SL doesn't match direction",
        resultTitle:"Result",lotSize:"Position Size",units:"Units",
        riskUSD:"Risk ($)",slPips:"SL Pips",margin:"Margin",potProfit:"Potential Profit",
        openInJournal:"📋 Open Trade in Journal",calcHint:"Enter entry price and stop loss",
        newTrade:"New Trade",save:"Save",prefillBanner:"Data from Calculator",
        sec1:"General",sec2:"Main Scenario",sec3:"Alternative Scenario",
        sec4:"Trade Plan",sec5:"Psychology",
        instrLabel:"Instrument *",instrPh:"EURUSD, BTC, NASDAQ…",
        htf:"HTF",ltf:"LTF",sessions:"Sessions",
        mktType:"Market Type",trend:"Trend",correction:"Correction",range:"Range",
        vol:"Volatility",low:"Low",medium:"Medium",high:"High",
        structure:"Current Structure",structPh:"Impulse 1–2 formed",
        devWave:"Developing Wave",devWavePh:"3 of 3, wave C…",
        structStart:"Structure Start",fibTarget:"Fib Target",fibPh:"1.618",
        scenLogic:"Scenario Logic",scenPh:"2–3 sentences…",
        invalidation:"Invalidation Level",
        altMarkup:"Alternative Markup",altPh:"Complex ABC correction…",
        altProb:"Probability (%)",altBias:"Bias change at",altConfirm:"What confirms the alternative",
        entryType:"Entry Type (wave)",impulse:"IMPULSE",corrLabel:"CORRECTION",
        entryPoint:"Entry Point",plannedRR:"Planned R:R",
        riskPctL:"Risk %",posSizeL:"Position Size",
        cancelCond:"Cancel Conditions",cancelPh:"If price…",
        energy:"Energy",focus:"Focus",calm:"Calm",pressure:"Result Pressure",
        lossStreak:"Loss Streak",no:"No",yes:"Yes",
        biases:"Biases",fomo:"FOMO",
        biasConf:"Confirmation Bias",biasRev:"Revenge Trading",biasOver:"Overconfidence",
        readyQ:"I'm ready to accept the stop if the scenario breaks?",
        del:"Delete",reopen:"Reopen Trade",
        closeTrade:"Close Trade",tradeRes:"Trade Result",
        resR:"Result R *",resUSD:"Result USD",maeL:"MAE (R)",mfeL:"MFE (R)",
        tradeClass:"Trade Class",errType:"Error Type",
        errNone:"None",errAn:"Analysis",errEx:"Execution",
        wouldRep:"Would repeat?",conclusion:"Main Conclusion",conclusionPh:"What did I learn…",
        cancel:"Cancel",saveBtn:"Save",
        timeframes:"Timeframes",mainScen:"Main Scenario",tradePlan:"Trade Plan",conclusionT:"Conclusion",logic:"Logic",
        statsTitle:"Statistics",overallStats:"Overall Stats",totalTrades:"Total Trades",
        avgWin:"Avg Win",avgLoss:"Avg Loss",bestTrade:"Best Trade",worstTrade:"Worst Trade",
        byMonth:"By Month",byInstr:"By Instrument",noStatsHint:"No closed trades for statistics",
        settingsTitle:"Settings",langSection:"Language / Язык",
        exportSection:"Export",importSection:"Import",dangerSection:"Danger Zone",
        currentJournal:"Current Journal",formatLabel:"Format",
        jsonSub:"Full backup",csvSub:"Excel / Sheets",
        copyBtn:"📋 Copy",copiedToast:"Copied to clipboard!",copyErr:"Copy failed",
        iosTitle:"How to save on iPhone:",
        iosS1:"Tap «Copy» above",iosS2:"Open the «Notes» app",
        iosS3:"Create a new note → paste (hold → Paste)",
        iosS4:"To import — copy the note text and paste it below",
        dlBtn:"⬇️ Download",
        importDesc:"Load a JSON file or paste its contents manually.",
        importMode:"Import Mode",merge:"Merge",replace:"Replace All",
        mergeHint:"Adds new trades, existing ones untouched",
        replaceHint:"⚠️ Deletes all current trades and replaces them",
        chooseFile:"📂 Choose JSON File",pasteLabel:"or paste JSON manually",
        importReady:"✓ Ready to import",
        importBtn:"⬆️ Import",replaceBtn:"⚠️ Replace & Import",
        noDataToast:"Paste JSON or choose a file",noTradesInFile:"No trades in file",parseErr:"JSON parse error",
        clearAll:"🗑 Clear All Data",clearDesc:"Full journal wipe. Cannot be undone.",
        clearConfirm:(n)=>`Delete all ${n} trades? This cannot be undone.`,
        exportedToast:(n)=>`Exported ${n} trades`,csvToast:(n)=>`CSV exported (${n} rows)`,
        delTradeConfirm:"Delete this trade?",instrReq:"Enter instrument",resReq:"Enter result R",
        sAsia:"Asia",sLondon:"London",sNY:"New York",sLonNY:"London/NY",sLonAsia:"London/Asia",
        pip:"Pip",typeL:"Type",pipPerLot:"Pip/$lot",pipsLabel:"pips",wW:"W",wL:"L",
        viewModeTitle:"App Version",mobileView:"Mobile (iOS)",webView:"Web (Desktop)",
      },
    };

    // ── Lang Context ──────────────────────────────────────────────────────────
    const LangCtx = createContext(null);
    const useLang = () => useContext(LangCtx);
    function LangProvider({ children }) {
      const [lang, setLangRaw] = useState(() => localStorage.getItem(LANG_KEY) || "ru");
      const setLang = l => { setLangRaw(l); localStorage.setItem(LANG_KEY, l); };
      return <LangCtx.Provider value={{ lang, setLang, t: T[lang] }}>{children}</LangCtx.Provider>;
    }

    // ── View Mode Context ─────────────────────────────────────────────────────
    const VM_KEY = "tj_view_mode";
    const isIOSDevice = /iPad|iPhone|iPod/.test(navigator.userAgent) ||
      (navigator.platform === "MacIntel" && navigator.maxTouchPoints > 1);
    const ViewCtx = createContext(null);
    const useView = () => useContext(ViewCtx);
    function ViewProvider({ children }) {
      const [viewMode, setViewModeRaw] = useState(
        () => localStorage.getItem(VM_KEY) || (isIOSDevice ? "mobile" : "web")
      );
      const setViewMode = v => { setViewModeRaw(v); localStorage.setItem(VM_KEY, v); };
      return <ViewCtx.Provider value={{ viewMode, setViewMode }}>{children}</ViewCtx.Provider>;
    }

    // ── Storage ───────────────────────────────────────────────────────────────
    const SK = "tj_trades_v3";
    function loadTrades() { try { const r = localStorage.getItem(SK); return r ? JSON.parse(r) : []; } catch { return []; } }
    function saveTrades(t) { try { localStorage.setItem(SK, JSON.stringify(t)); } catch {} }
    function uid() { return Date.now().toString(36) + Math.random().toString(36).slice(2,7); }

    // ── Trades Context ────────────────────────────────────────────────────────
    const TradesCtx = createContext(null);
    const useTrades = () => useContext(TradesCtx);
    function computeStats(trades) {
      const cl = trades.filter(t => t.status==="closed" && t.resultR!=null);
      const wins = cl.filter(t => t.resultR>0), losses = cl.filter(t => t.resultR<0);
      const tR = cl.reduce((s,t)=>s+t.resultR,0);
      const tW = wins.reduce((s,t)=>s+t.resultR,0);
      const tL = Math.abs(losses.reduce((s,t)=>s+t.resultR,0));
      const tU = cl.reduce((s,t)=>s+(t.resultUSD??0),0);
      const cls={"A+":0,A:0,B:0,C:0,D:0};
      cl.forEach(t=>{if(t.tradeClass)cls[t.tradeClass]++;});
      return { total:cl.length,wins:wins.length,losses:losses.length,
        winRate:cl.length?(wins.length/cl.length)*100:0,
        totalR:tR,totalUSD:tU,
        avgWin:wins.length?tW/wins.length:0,avgLoss:losses.length?tL/losses.length:0,
        pf:tL>0?tW/tL:tW>0?Infinity:0,
        best:cl.length?Math.max(...cl.map(t=>t.resultR)):0,
        worst:cl.length?Math.min(...cl.map(t=>t.resultR)):0,
        open:trades.filter(t=>t.status==="open").length,cls };
    }
    function TradesProvider({ children }) {
      const [trades,setTrades] = useState(loadTrades);
      useEffect(()=>saveTrades(trades),[trades]);
      const stats = useMemo(()=>computeStats(trades),[trades]);
      const addTrade = useCallback(d=>setTrades(p=>[{...d,id:uid(),date:d.date||new Date().toISOString()},...p]),[]);
      const updateTrade = useCallback((id,u)=>setTrades(p=>p.map(t=>t.id===id?{...t,...u}:t)),[]);
      const deleteTrade = useCallback(id=>setTrades(p=>p.filter(t=>t.id!==id)),[]);
      return <TradesCtx.Provider value={{trades,stats,addTrade,updateTrade,deleteTrade}}>{children}</TradesCtx.Provider>;
    }

    // ── UI Primitives ─────────────────────────────────────────────────────────
    const Card=({children,style,glow})=><div style={{background:C.bg2,border:`1px solid ${glow?C.tint+"50":C.border}`,borderRadius:16,padding:16,boxShadow:glow?`0 0 20px ${C.tint}15`:"none",...style}}>{children}</div>;
    const Label=({children,style})=><div style={{fontSize:10,fontFamily:"'JetBrains Mono',monospace",letterSpacing:1.2,textTransform:"uppercase",color:C.text3,marginBottom:6,...style}}>{children}</div>;
    const Chip=({label,active,onClick,color})=>{const col=color||C.tint;return <button onClick={onClick} style={{padding:"5px 12px",borderRadius:20,fontSize:12,fontWeight:600,background:active?col:C.bg3,color:active?"#fff":C.text2,border:`1px solid ${active?col:C.border}`}}>{label}</button>;};
    function Input({label,value,onChange,type="text",placeholder,prefix,suffix,multiline,style}){
      const s={background:C.bg3,border:`1px solid ${C.border}`,borderRadius:10,color:C.text,fontSize:14,width:"100%",fontFamily:"'Sora',sans-serif",padding:"10px 12px"};
      return(<div style={style}>{label&&<Label>{label}</Label>}<div style={{position:"relative",display:"flex",alignItems:"center"}}>{prefix&&<span style={{position:"absolute",left:12,color:C.text3,fontSize:14,pointerEvents:"none"}}>{prefix}</span>}{multiline?<textarea value={value} onChange={e=>onChange(e.target.value)} placeholder={placeholder} rows={3} style={{...s,resize:"vertical",paddingLeft:prefix?28:12,lineHeight:1.5}}/>:<input type={type} value={value} onChange={e=>onChange(e.target.value)} placeholder={placeholder} style={{...s,paddingLeft:prefix?28:12,paddingRight:suffix?36:12}}/>}{suffix&&<span style={{position:"absolute",right:12,color:C.text3,fontSize:13,pointerEvents:"none"}}>{suffix}</span>}</div></div>);
    }
    const ScoreRow=({label,value,onChange})=><div style={{display:"flex",alignItems:"center",justifyContent:"space-between",padding:"6px 0"}}><span style={{fontSize:13,color:C.text2,flex:1}}>{label}</span><div style={{display:"flex",gap:6}}>{[1,2,3,4,5].map(n=><button key={n} onClick={()=>onChange(n)} style={{width:28,height:28,borderRadius:14,fontSize:11,fontWeight:700,background:n<=value?C.tint:C.bg3,color:n<=value?"#fff":C.text3}}>{n}</button>)}</div></div>;
    const Toggle=({label,value,onChange})=><button onClick={()=>onChange(!value)} style={{display:"flex",alignItems:"center",gap:10,padding:"8px 12px",borderRadius:10,width:"100%",textAlign:"left",background:value?C.lossDim:C.bg3,border:`1px solid ${value?C.loss+"50":"transparent"}`}}><div style={{width:18,height:18,borderRadius:5,display:"flex",alignItems:"center",justifyContent:"center",background:value?C.loss:C.border,fontSize:11,color:"#fff",fontWeight:700}}>{value?"✓":""}</div><span style={{fontSize:13,color:value?C.loss:C.text2,fontWeight:500}}>{label}</span></button>;
    const SectionHeader=({n,title})=><div style={{display:"flex",alignItems:"center",gap:10,paddingBottom:12,borderBottom:`1px solid ${C.border}`,marginBottom:4}}><div style={{width:24,height:24,borderRadius:12,background:C.tintDim,display:"flex",alignItems:"center",justifyContent:"center",fontSize:12,fontWeight:700,color:C.tint,fontFamily:"'JetBrains Mono',monospace"}}>{n}</div><span style={{fontSize:14,fontWeight:700,color:C.text}}>{title}</span></div>;
    const Seg=({options,value,onChange})=><div style={{display:"flex",background:C.bg3,borderRadius:10,padding:3,gap:3}}>{options.map(o=><button key={o.value} onClick={()=>onChange(o.value)} style={{flex:1,padding:"7px 4px",borderRadius:8,fontSize:12,fontWeight:600,background:value===o.value?C.tint:"transparent",color:value===o.value?"#fff":C.text2}}>{o.label}</button>)}</div>;
    const StatCard=({label,value,sub,color})=><Card style={{flex:1,minWidth:0}}><div style={{fontSize:10,fontFamily:"'JetBrains Mono',monospace",letterSpacing:1,color:C.text3,textTransform:"uppercase",marginBottom:6}}>{label}</div><div style={{fontSize:22,fontWeight:700,color:color||C.text,fontFamily:"'JetBrains Mono',monospace",lineHeight:1.1}}>{value}</div>{sub&&<div style={{fontSize:11,color:C.text3,marginTop:4}}>{sub}</div>}</Card>;

    // ── Equity Chart ──────────────────────────────────────────────────────────
    function EquityChart({trades}){
      const pts2=useMemo(()=>{const arr=trades.filter(t=>t.status==="closed"&&t.resultR!=null).slice().reverse();let c=0;return arr.map(t=>{c+=t.resultR;return c;});},[trades]);
      if(pts2.length<2)return null;
      const mn=Math.min(...pts2,0),mx=Math.max(...pts2,0),rng=mx-mn||1;
      const W=400,H=80,p=4;
      const pts=pts2.map((v,i)=>`${p+(i/(pts2.length-1))*(W-p*2)},${p+(1-(v-mn)/rng)*(H-p*2)}`).join(" ");
      const col=pts2[pts2.length-1]>=0?C.profit:C.loss;
      return(<div style={{overflow:"hidden",borderRadius:8}}><svg viewBox={`0 0 ${W} ${H}`} style={{width:"100%",height:70}} preserveAspectRatio="none"><defs><linearGradient id="eg" x1="0" y1="0" x2="0" y2="1"><stop offset="0%" stopColor={col} stopOpacity="0.25"/><stop offset="100%" stopColor={col} stopOpacity="0"/></linearGradient></defs>{mn<0&&mx>0&&<line x1={p} x2={W-p} y1={p+(1-(0-mn)/rng)*(H-p*2)} y2={p+(1-(0-mn)/rng)*(H-p*2)} stroke={C.border} strokeWidth={1} strokeDasharray="3 3"/>}<polyline points={pts} fill="none" stroke={col} strokeWidth={2} strokeLinecap="round" strokeLinejoin="round"/><polygon points={`${p},${H} ${pts} ${W-p},${H}`} fill="url(#eg)"/></svg></div>);
    }

    const CLS_COLOR={"A+":"#00C896",A:"#34D399",B:"#60A5FA",C:"#FBBF24",D:"#F87171"};

    // ── TradeCard ─────────────────────────────────────────────────────────────
    function TradeCard({trade,onClick}){
      const isOpen=trade.status==="open";
      const rC=trade.resultR==null?C.text2:trade.resultR>0?C.profit:C.loss;
      const [hov,setHov]=useState(false);
      return(<button onClick={onClick} onMouseEnter={()=>setHov(true)} onMouseLeave={()=>setHov(false)} style={{display:"flex",alignItems:"center",gap:12,padding:"12px 16px",background:C.bg2,border:`1px solid ${hov?C.tint+"60":C.border}`,borderRadius:14,width:"100%",textAlign:"left",marginBottom:8}}>
        <div style={{width:8,height:8,borderRadius:4,flexShrink:0,background:isOpen?C.warning:trade.resultR>0?C.profit:C.loss,boxShadow:isOpen?`0 0 6px ${C.warning}`:"none"}}/>
        <div style={{flex:1,minWidth:0}}>
          <div style={{display:"flex",alignItems:"center",gap:8,marginBottom:2}}>
            <span style={{fontWeight:700,fontFamily:"'JetBrains Mono',monospace",fontSize:14,color:C.text}}>{trade.instrument}</span>
            {trade.tradeClass&&<span style={{fontSize:10,fontWeight:700,padding:"1px 6px",borderRadius:5,background:(CLS_COLOR[trade.tradeClass]||C.text3)+"25",color:CLS_COLOR[trade.tradeClass]||C.text3}}>{trade.tradeClass}</span>}
            {trade.entryType&&<span style={{fontSize:10,color:C.text3}}>W{trade.entryType}</span>}
          </div>
          <div style={{fontSize:11,color:C.text3,fontFamily:"'JetBrains Mono',monospace"}}>{new Date(trade.date).toLocaleDateString("ru-RU")}{trade.developingWave?` · ${trade.developingWave}`:""}</div>
        </div>
        <div style={{textAlign:"right",flexShrink:0}}>
          {isOpen?<span style={{fontSize:11,color:C.warning,fontWeight:600}}>OPEN</span>:<span style={{fontSize:16,fontWeight:700,fontFamily:"'JetBrains Mono',monospace",color:rC}}>{trade.resultR!=null?`${trade.resultR>=0?"+":""}${trade.resultR.toFixed(2)}R`:"—"}</span>}
          {trade.resultUSD!=null&&!isOpen&&<div style={{fontSize:10,color:C.text3,fontFamily:"'JetBrains Mono',monospace"}}>${trade.resultUSD>=0?"+":""}{trade.resultUSD.toFixed(2)}</div>}
        </div>
        <span style={{color:C.text3,fontSize:18,marginLeft:4}}>›</span>
      </button>);
    }

    // ── Dashboard ─────────────────────────────────────────────────────────────
    function Dashboard({onNav,onOpenTrade}){
      const {trades,stats}=useTrades();const {t}=useLang();
      const rC=stats.totalR>0?C.profit:stats.totalR<0?C.loss:C.text;
      return(<div style={{padding:"0 0 100px"}}>
        <div style={{padding:"max(24px,env(safe-area-inset-top)) 16px 16px",display:"flex",alignItems:"flex-start",justifyContent:"space-between"}}>
          <div>
            <div style={{fontSize:11,fontFamily:"'JetBrains Mono',monospace",letterSpacing:1,color:C.text3,textTransform:"uppercase",marginBottom:4}}>{t.totalR}</div>
            <div style={{fontSize:48,fontWeight:700,color:rC,fontFamily:"'JetBrains Mono',monospace",lineHeight:1,letterSpacing:-2}}>{stats.total===0?"0R":`${stats.totalR>=0?"+":""}${stats.totalR.toFixed(1)}R`}</div>
            {stats.totalUSD!==0&&<div style={{fontSize:15,color:C.text2,marginTop:3,fontFamily:"'JetBrains Mono',monospace"}}>{stats.totalUSD>=0?"+":""}${Math.abs(stats.totalUSD).toFixed(2)}</div>}
            <div style={{fontSize:12,color:C.text3,marginTop:6}}>{stats.total} {t.trades} · WR {stats.winRate.toFixed(0)}%</div>
          </div>
          <button onClick={()=>onNav("new")} style={{width:48,height:48,borderRadius:24,background:C.tint,color:"#fff",fontSize:24,display:"flex",alignItems:"center",justifyContent:"center",flexShrink:0,marginTop:8}}>+</button>
        </div>
        {trades.filter(x=>x.status==="closed").length>=2&&<div style={{padding:"0 16px 12px"}}><Card><div style={{fontSize:12,fontWeight:700,color:C.text,marginBottom:8}}>{t.equityCurve}</div><EquityChart trades={trades}/></Card></div>}
        <div style={{padding:"0 16px",display:"grid",gridTemplateColumns:"1fr 1fr",gap:10,marginBottom:10}}>
          <StatCard label="Win Rate" value={`${stats.winRate.toFixed(0)}%`} sub={`${stats.wins}${t.wW} / ${stats.losses}${t.wL}`} color={stats.winRate>=50?C.profit:C.loss}/>
          <StatCard label="Profit Factor" value={stats.pf===Infinity?"∞":stats.pf===0?"—":stats.pf.toFixed(2)} color={stats.pf>=1.5?C.profit:stats.pf>=1?C.warning:C.loss}/>
          <StatCard label={t.avgWin} value={stats.avgWin?`+${stats.avgWin.toFixed(2)}R`:"—"} color={C.profit}/>
          <StatCard label={t.avgLoss} value={stats.avgLoss?`-${stats.avgLoss.toFixed(2)}R`:"—"} color={C.loss}/>
          <StatCard label={t.bestTrade} value={stats.best?`${stats.best>0?"+":""}${stats.best.toFixed(1)}R`:"—"} color={C.profit}/>
          <StatCard label={t.worstTrade} value={stats.worst?`${stats.worst.toFixed(1)}R`:"—"} color={C.loss}/>
        </div>
        {stats.total>0&&<div style={{padding:"0 16px 10px"}}><Card><div style={{fontSize:12,fontWeight:700,color:C.text,marginBottom:10}}>{t.tradeClasses}</div><div style={{display:"flex",justifyContent:"space-around"}}>{["A+","A","B","C","D"].map(c=><div key={c} style={{display:"flex",flexDirection:"column",alignItems:"center",gap:4}}><div style={{width:10,height:10,borderRadius:5,background:CLS_COLOR[c]}}/><span style={{fontSize:11,color:C.text2,fontWeight:600}}>{c}</span><span style={{fontSize:16,fontWeight:700,fontFamily:"'JetBrains Mono',monospace",color:C.text}}>{stats.cls[c]}</span></div>)}</div></Card></div>}
        {stats.open>0&&<div style={{margin:"0 16px 10px",padding:"10px 14px",borderRadius:12,background:C.warning+"12",border:`1px solid ${C.warning}25`,display:"flex",alignItems:"center",gap:8}}><span style={{color:C.warning}}>⚡</span><span style={{fontSize:13,color:C.warning,fontWeight:600}}>{stats.open} {t.openPos}</span></div>}
        {trades.slice(0,5).length>0&&<div style={{padding:"0 16px"}}><div style={{display:"flex",justifyContent:"space-between",alignItems:"center",marginBottom:10}}><span style={{fontSize:14,fontWeight:700,color:C.text}}>{t.recentTrades}</span><button onClick={()=>onNav("journal")} style={{fontSize:13,color:C.tint}}>{t.allTrades}</button></div>{trades.slice(0,5).map(tr=><TradeCard key={tr.id} trade={tr} onClick={()=>onOpenTrade(tr.id)}/>)}</div>}
        {trades.length===0&&<div style={{margin:"16px",padding:32,borderRadius:20,border:`1px dashed ${C.border}`,textAlign:"center"}}><div style={{fontSize:32,marginBottom:12}}>📈</div><div style={{fontSize:18,fontWeight:700,color:C.text,marginBottom:8}}>{t.emptyTitle}</div><div style={{fontSize:14,color:C.text2,lineHeight:1.6,marginBottom:20}}>{t.emptyDesc}</div><button onClick={()=>onNav("new")} style={{padding:"12px 28px",borderRadius:14,background:C.tint,color:"#fff",fontSize:14,fontWeight:600}}>{t.addTrade}</button></div>}
      </div>);
    }

    // ── Journal ───────────────────────────────────────────────────────────────
    function Journal({onNav,onOpenTrade}){
      const {trades}=useTrades();const {t}=useLang();
      const [filter,setFilter]=useState("all");const [search,setSearch]=useState("");
      const FILTERS=[{label:t.all,value:"all"},{label:t.open,value:"open"},{label:t.closed,value:"closed"},{label:"A+",value:"A+"},{label:"A",value:"A"},{label:"B",value:"B"},{label:"C/D",value:"C"}];
      const filtered=useMemo(()=>{let r=trades;if(filter==="open")r=r.filter(x=>x.status==="open");else if(filter==="closed")r=r.filter(x=>x.status==="closed");else if(["A+","A","B","C","D"].includes(filter))r=r.filter(x=>x.tradeClass===filter);if(search.trim()){const q=search.toLowerCase();r=r.filter(x=>x.instrument?.toLowerCase().includes(q)||x.developingWave?.toLowerCase().includes(q)||x.scenarioLogic?.toLowerCase().includes(q));}return r;},[trades,filter,search]);
      return(<div style={{padding:"0 0 100px"}}>
        <div style={{padding:"max(24px,env(safe-area-inset-top)) 16px 12px",display:"flex",alignItems:"center",justifyContent:"space-between"}}><div style={{fontSize:26,fontWeight:700,color:C.text}}>{t.journal}</div><button onClick={()=>onNav("new")} style={{width:38,height:38,borderRadius:19,background:C.tint,color:"#fff",fontSize:22,display:"flex",alignItems:"center",justifyContent:"center"}}>+</button></div>
        <div style={{margin:"0 16px 10px",display:"flex",alignItems:"center",gap:8,background:C.bg3,borderRadius:12,padding:"8px 14px"}}><span style={{color:C.text3}}>🔍</span><input value={search} onChange={e=>setSearch(e.target.value)} placeholder={t.searchPh} style={{flex:1,background:"none",color:C.text,fontSize:14}}/>{search&&<button onClick={()=>setSearch("")} style={{color:C.text3,fontSize:16}}>×</button>}</div>
        <div style={{display:"flex",gap:6,padding:"0 16px 12px",flexWrap:"wrap"}}>{FILTERS.map(f=><Chip key={f.value} label={f.label} active={filter===f.value} onClick={()=>setFilter(f.value)}/>)}</div>
        <div style={{padding:"0 16px"}}>{filtered.length===0?<div style={{textAlign:"center",padding:"60px 0"}}><div style={{fontSize:32,marginBottom:12}}>📭</div><div style={{color:C.text,fontWeight:600,marginBottom:6}}>{trades.length===0?t.noTrades:t.noResults}</div><div style={{color:C.text3,fontSize:13}}>{trades.length===0?t.noTradesHint:t.noResultsHint}</div></div>:filtered.map(tr=><TradeCard key={tr.id} trade={tr} onClick={()=>onOpenTrade(tr.id)}/>)}</div>
      </div>);
    }

    // ── Calculator ────────────────────────────────────────────────────────────
    const POPULAR=["GBPUSD","EURUSD","USDCHF","USDJPY","NZDUSD","USDCAD","AUDUSD","XAUUSD","XAGUSD","BCOUSD","BTCUSDT"];
    function detectInstr(sym){
      const s=sym.toUpperCase();
      if(s.includes("JPY"))return{pip:0.01,label:"Forex JPY",cs:100000};
      if(["BTC","ETH","XRP","SOL","BNB"].some(c=>s.includes(c)))return{pip:1,label:"Crypto",cs:1};
      if(["NAS","SP5","US3","DAX","FTSE","DOW"].some(c=>s.includes(c)))return{pip:0.1,label:"Index",cs:10};
      if(s.includes("XAU")||s.includes("GOLD"))return{pip:0.01,label:"Gold",cs:100};
      if(s.includes("XAG"))return{pip:0.001,label:"Silver",cs:5000};
      if(s.includes("BCO")||s.includes("OIL")||s.includes("WTI"))return{pip:0.01,label:"Oil",cs:100};
      return{pip:0.0001,label:"Forex",cs:100000};
    }
    function Calculator({onOpenInJournal}){
      const {t}=useLang();
      const [sym,setSym]=useState("GBPUSD");const [showPop,setShowPop]=useState(false);
      const [dir,setDir]=useState("long");
      const [bal,setBal]=useState("10000");const [risk,setRisk]=useState("1");const [lev,setLev]=useState("100");
      const [entry,setEntry]=useState("");const [sl,setSl]=useState("");const [slM,setSlM]=useState("price");
      const [tp,setTp]=useState("");const [tpM,setTpM]=useState("price");
      const info=useMemo(()=>detectInstr(sym),[sym]);
      const calc=useMemo(()=>{
        const pn=s=>parseFloat(String(s).replace(",","."))||0;
        const b=pn(bal),r=pn(risk),lv=pn(lev)||1,en=pn(entry),sln=pn(sl),tpn=pn(tp);
        const rU=b*(r/100),pvl=info.pip*info.cs;
        const slp=slM==="pips"?sln:(en>0&&sln>0?Math.abs(en-sln)/info.pip:0);
        const dOk=slM!=="price"||!(en>0&&sln>0)||(dir==="long"?sln<en:sln>en);
        const lots=slp>0?rU/(slp*pvl):0;
        const posU=lots*info.cs*(en>0?en:1),marg=posU/lv;
        const tpp=tpM==="pips"?tpn:tpM==="rr"&&slp>0?slp*tpn:(en>0&&tpn>0?Math.abs(tpn-en)/info.pip:0);
        return{rU,lots,slp,tpp,profU:tpp*pvl*lots,rr:slp>0&&tpp>0?tpp/slp:0,marg,dOk,pvl,units:lots*info.cs};
      },[bal,risk,lev,entry,sl,slM,tp,tpM,info,dir]);
      const fL=v=>!v?"—":`${v.toFixed(v>=0.01?2:3)} lot`;
      const RR=({label,value,color,big})=><div style={{display:"flex",justifyContent:"space-between",alignItems:"center",padding:"10px 0",borderBottom:`1px solid ${C.border}`}}><span style={{fontSize:13,color:C.text2}}>{label}</span><span style={{fontSize:big?22:14,fontWeight:700,color:color||C.text,fontFamily:"'JetBrains Mono',monospace"}}>{value}</span></div>;
      const QB=({values,selected,onSel,fmt})=><div style={{display:"flex",flexWrap:"wrap",gap:6}}>{values.map(v=>{const a=String(v)===String(selected);return<button key={v} onClick={()=>onSel(v)} style={{padding:"5px 10px",borderRadius:8,fontSize:12,fontWeight:600,background:a?C.tint:C.bg3,color:a?"#fff":C.text2,border:`1px solid ${a?C.tint:C.border}`}}>{fmt?fmt(v):v}</button>;})}</div>;
      const send=()=>onOpenInJournal({instrument:sym,direction:dir,entryPoint:entry?parseFloat(entry):undefined,stopLoss:sl&&slM==="price"?parseFloat(sl):undefined,takeProfit:tp&&tpM==="price"?parseFloat(tp):undefined,plannedRR:calc.rr>0?calc.rr:undefined,riskPercent:parseFloat(risk)||undefined,positionSize:calc.lots>0?parseFloat(calc.lots.toFixed(calc.lots>=0.01?2:3)):undefined});
      return(<div style={{padding:"0 0 100px"}}>
        <div style={{padding:"max(24px,env(safe-area-inset-top)) 16px 8px"}}><div style={{fontSize:26,fontWeight:700,color:C.text}}>{t.calcTitle}</div><div style={{fontSize:12,color:C.text3}}>{t.posSizeTitle}</div></div>
        <div style={{padding:"0 16px",display:"flex",flexDirection:"column",gap:12}}>
          <Card>
            <Label>{t.instrument}</Label>
            <div style={{display:"flex",gap:8,marginBottom:8}}><input value={sym} onChange={e=>{setSym(e.target.value.toUpperCase());setShowPop(false);}} style={{flex:1,background:C.bg3,border:`1px solid ${C.border}`,borderRadius:10,color:C.text,fontSize:16,fontWeight:600,padding:"10px 12px",fontFamily:"'JetBrains Mono',monospace"}}/><button onClick={()=>setShowPop(p=>!p)} style={{padding:"0 14px",background:C.bg3,border:`1px solid ${C.border}`,borderRadius:10,color:C.text2,fontSize:16}}>{showPop?"▲":"▼"}</button></div>
            <div style={{display:"flex",gap:12,flexWrap:"wrap",marginBottom:4}}><span style={{fontSize:11,color:C.text3}}>{t.pip}: <b style={{color:C.tint}}>{info.pip}</b></span><span style={{fontSize:11,color:C.text3}}>{t.typeL}: <b style={{color:C.tint}}>{info.label}</b></span><span style={{fontSize:11,color:C.text3}}>{t.pipPerLot}: <b style={{color:C.tint}}>${calc.pvl.toFixed(2)}</b></span></div>
            {showPop&&<div style={{display:"flex",flexWrap:"wrap",gap:6,marginTop:6}}>{POPULAR.map(s=><button key={s} onClick={()=>{setSym(s);setShowPop(false);}} style={{padding:"4px 10px",borderRadius:8,fontSize:12,fontWeight:600,background:sym===s?C.tint:C.bg3,color:sym===s?"#fff":C.text2,border:`1px solid ${sym===s?C.tint:C.border}`}}>{s}</button>)}</div>}
          </Card>
          <Card><Label>{t.direction}</Label><div style={{display:"flex",gap:10}}>{["long","short"].map(d=>{const a=dir===d,col=d==="long"?C.profit:C.loss;return<button key={d} onClick={()=>setDir(d)} style={{flex:1,padding:"12px",borderRadius:12,fontWeight:700,fontSize:15,background:a?col+"20":C.bg3,color:a?col:C.text2,border:`1.5px solid ${a?col:C.border}`}}>{d==="long"?t.longBtn:t.shortBtn}</button>;})} </div></Card>
          <Card>
            <div style={{display:"grid",gridTemplateColumns:"1fr 1fr",gap:10,marginBottom:10}}><Input label={t.balance} value={bal} onChange={setBal} type="number" prefix="$"/><Input label={t.riskPct} value={risk} onChange={setRisk} type="number" suffix="%"/></div>
            <Label>{t.quickBal}</Label><QB values={[5000,10000,25000,50000,100000]} selected={parseFloat(bal)} onSel={v=>setBal(String(v))} fmt={v=>`$${v>=1000?v/1000+"k":v}`}/>
            <div style={{marginTop:10}}><Label>{t.riskLevel}</Label><QB values={[0.5,1,1.5,2,3,5]} selected={parseFloat(risk)} onSel={v=>setRisk(String(v))} fmt={v=>`${v}%`}/></div>
            <div style={{marginTop:10,background:C.tintDim,borderRadius:10,padding:"10px 14px",display:"flex",justifyContent:"space-between",alignItems:"center",border:`1px solid ${C.tint}30`}}><span style={{fontSize:13,color:C.text3}}>{t.riskAmt}</span><span style={{fontSize:18,fontWeight:700,color:C.tint,fontFamily:"'JetBrains Mono',monospace"}}>${calc.rU.toFixed(2)}</span></div>
          </Card>
          <Card><Input label={t.leverage} value={lev} onChange={setLev} type="number" prefix="1:" style={{marginBottom:10}}/><QB values={[1,2,5,10,20,50,100,200,500]} selected={parseFloat(lev)} onSel={v=>setLev(String(v))} fmt={v=>`1:${v}`}/></Card>
          <Card>
            <Input label={t.entryPrice} value={entry} onChange={setEntry} type="number" placeholder="0.00000" style={{marginBottom:10}}/>
            <div style={{display:"flex",justifyContent:"space-between",alignItems:"center",marginBottom:6}}><span style={{fontSize:11,fontWeight:700,color:C.loss}}>{t.stopLoss.toUpperCase()}</span><div style={{display:"flex",gap:4}}>{[{label:t.priceM,value:"price"},{label:t.pipsM,value:"pips"}].map(m=><button key={m.value} onClick={()=>setSlM(m.value)} style={{padding:"4px 10px",borderRadius:6,fontSize:11,fontWeight:600,background:slM===m.value?C.tint:C.bg3,color:slM===m.value?"#fff":C.text2}}>{m.label}</button>)}</div></div>
            <Input value={sl} onChange={setSl} type="number" placeholder={slM==="price"?"0.00000":t.pipsM} suffix={slM==="pips"?"pips":undefined}/>
            {calc.slp>0&&<div style={{marginTop:4,display:"flex",gap:12}}><span style={{fontSize:11,color:C.text3}}>= {calc.slp.toFixed(1)} {t.pipsLabel}</span>{!calc.dOk&&<span style={{fontSize:11,color:C.warning}}>{t.slWarn}</span>}</div>}
            <div style={{display:"flex",justifyContent:"space-between",alignItems:"center",marginTop:12,marginBottom:6}}><span style={{fontSize:11,fontWeight:700,color:C.profit}}>{t.takeProfit.toUpperCase()}</span><div style={{display:"flex",gap:4}}>{[{label:t.priceM,value:"price"},{label:t.pipsM,value:"pips"},{label:t.rrM,value:"rr"}].map(m=><button key={m.value} onClick={()=>setTpM(m.value)} style={{padding:"4px 10px",borderRadius:6,fontSize:11,fontWeight:600,background:tpM===m.value?C.tint:C.bg3,color:tpM===m.value?"#fff":C.text2}}>{m.label}</button>)}</div></div>
            <Input value={tp} onChange={setTp} type="number" placeholder={tpM==="price"?"0.00000":tpM==="pips"?t.pipsM:"2"} prefix={tpM==="rr"?"1:":undefined} suffix={tpM==="pips"?"pips":undefined}/>
            {calc.tpp>0&&<div style={{marginTop:4,fontSize:11,color:C.text3}}>= {calc.tpp.toFixed(1)} {t.pipsLabel}</div>}
          </Card>
          {calc.lots>0?<>
            <Card glow><div style={{fontSize:14,fontWeight:700,color:C.text,marginBottom:6}}>{t.resultTitle}</div>
              <RR label={t.lotSize} value={fL(calc.lots)} color={dir==="long"?C.profit:C.loss} big/>
              <RR label={t.units} value={calc.units>0?Math.round(calc.units).toLocaleString("ru-RU"):"—"}/>
              <RR label={t.riskUSD} value={`$${calc.rU.toFixed(2)}`} color={C.loss}/>
              <RR label={t.slPips} value={`${calc.slp.toFixed(1)}`}/>
              {calc.marg>0&&<RR label={t.margin} value={`$${calc.marg.toFixed(2)}`}/>}
              {calc.profU>0&&<RR label={t.potProfit} value={`$${calc.profU.toFixed(2)}`} color={C.profit}/>}
              {calc.rr>0&&<RR label="R:R" value={`1:${calc.rr.toFixed(2)}`} color={calc.rr>=2?C.profit:calc.rr>=1?C.warning:C.loss}/>}
            </Card>
            <button onClick={send} style={{width:"100%",padding:"14px",borderRadius:14,background:`linear-gradient(135deg,${C.tint},#00A876)`,color:"#fff",fontWeight:700,fontSize:15,display:"flex",alignItems:"center",justifyContent:"center",gap:8,boxShadow:`0 4px 20px ${C.tint}40`}}>{t.openInJournal}</button>
          </>:<div style={{textAlign:"center",padding:"28px 16px",border:`1px dashed ${C.border}`,borderRadius:16}}><div style={{fontSize:24,marginBottom:8}}>🎯</div><div style={{color:C.text3,fontSize:13}}>{t.calcHint}</div></div>}
        </div>
      </div>);
    }

    // ── Stats ─────────────────────────────────────────────────────────────────
    function Stats(){
      const {trades,stats}=useTrades();const {t}=useLang();
      const mR=useMemo(()=>{const m={};trades.filter(x=>x.status==="closed"&&x.resultR!=null).forEach(x=>{const d=new Date(x.date),k=`${d.getFullYear()}-${String(d.getMonth()+1).padStart(2,"0")}`;m[k]=(m[k]??0)+x.resultR;});return Object.entries(m).sort().slice(-6);},[trades]);
      const bI=useMemo(()=>{const m={};trades.filter(x=>x.status==="closed"&&x.resultR!=null).forEach(x=>{const k=x.instrument;if(!m[k])m[k]={r:0,count:0,wins:0};m[k].r+=x.resultR;m[k].count++;if(x.resultR>0)m[k].wins++;});return Object.entries(m).sort((a,b)=>b[1].r-a[1].r).slice(0,8);},[trades]);
      const MR=({label,value,color})=><div style={{display:"flex",justifyContent:"space-between",alignItems:"center",padding:"10px 0",borderBottom:`1px solid ${C.border}`}}><span style={{fontSize:13,color:C.text2}}>{label}</span><span style={{fontSize:13,fontWeight:700,color:color||C.text,fontFamily:"'JetBrains Mono',monospace"}}>{value}</span></div>;
      return(<div style={{padding:"0 0 100px"}}>
        <div style={{padding:"max(24px,env(safe-area-inset-top)) 16px 12px"}}><div style={{fontSize:26,fontWeight:700,color:C.text}}>{t.statsTitle}</div></div>
        <div style={{padding:"0 16px",display:"flex",flexDirection:"column",gap:12}}>
          <Card><div style={{fontSize:12,fontWeight:700,color:C.text,marginBottom:6}}>{t.overallStats}</div>
            <MR label={t.totalTrades} value={stats.total}/><MR label="Win Rate" value={`${stats.winRate.toFixed(1)}%`} color={stats.winRate>=50?C.profit:C.loss}/>
            <MR label="Profit Factor" value={stats.pf===Infinity?"∞":stats.pf.toFixed(2)} color={stats.pf>=1.5?C.profit:C.loss}/>
            <MR label={t.totalR} value={`${stats.totalR>=0?"+":""}${stats.totalR.toFixed(2)}R`} color={stats.totalR>=0?C.profit:C.loss}/>
            <MR label="Total USD" value={`${stats.totalUSD>=0?"+":""}$${Math.abs(stats.totalUSD).toFixed(2)}`} color={stats.totalUSD>=0?C.profit:C.loss}/>
            <MR label={t.avgWin} value={`+${stats.avgWin.toFixed(2)}R`} color={C.profit}/><MR label={t.avgLoss} value={`-${stats.avgLoss.toFixed(2)}R`} color={C.loss}/>
            <MR label={t.bestTrade} value={`${stats.best>=0?"+":""}${stats.best.toFixed(2)}R`} color={C.profit}/><MR label={t.worstTrade} value={`${stats.worst.toFixed(2)}R`} color={C.loss}/>
          </Card>
          {mR.length>0&&<Card><div style={{fontSize:12,fontWeight:700,color:C.text,marginBottom:6}}>{t.byMonth}</div>{mR.map(([mo,r])=><div key={mo} style={{display:"flex",alignItems:"center",gap:10,padding:"8px 0",borderBottom:`1px solid ${C.border}`}}><span style={{fontSize:12,color:C.text3,fontFamily:"'JetBrains Mono',monospace",minWidth:60}}>{mo}</span><div style={{flex:1,height:6,background:C.bg3,borderRadius:3,overflow:"hidden"}}><div style={{height:"100%",borderRadius:3,width:`${Math.min(100,Math.abs(r)/Math.max(...mR.map(([,v])=>Math.abs(v)))*100)}%`,background:r>=0?C.profit:C.loss}}/></div><span style={{fontSize:12,fontWeight:700,fontFamily:"'JetBrains Mono',monospace",color:r>=0?C.profit:C.loss,minWidth:55,textAlign:"right"}}>{r>=0?"+":""}{r.toFixed(2)}R</span></div>)}</Card>}
          {bI.length>0&&<Card><div style={{fontSize:12,fontWeight:700,color:C.text,marginBottom:6}}>{t.byInstr}</div>{bI.map(([s2,d])=><div key={s2} style={{display:"flex",alignItems:"center",gap:10,padding:"8px 0",borderBottom:`1px solid ${C.border}`}}><span style={{fontSize:12,fontWeight:700,fontFamily:"'JetBrains Mono',monospace",color:C.text,minWidth:70}}>{s2}</span><span style={{fontSize:11,color:C.text3}}>{d.count} · WR {(d.wins/d.count*100).toFixed(0)}%</span><span style={{marginLeft:"auto",fontSize:13,fontWeight:700,fontFamily:"'JetBrains Mono',monospace",color:d.r>=0?C.profit:C.loss}}>{d.r>=0?"+":""}{d.r.toFixed(2)}R</span></div>)}</Card>}
          {stats.total===0&&<div style={{textAlign:"center",padding:40,color:C.text3}}>{t.noStatsHint}</div>}
        </div>
      </div>);
    }

    // ── New Trade ─────────────────────────────────────────────────────────────
    function NewTrade({onBack,onSaved,prefill={}}){
      const {addTrade}=useTrades();const {t}=useLang();
      const SESS=[t.sAsia,t.sLondon,t.sNY,t.sLonNY,t.sLonAsia];
      const [instr,setInstr]=useState(prefill.instrument||"");const [sess,setSess]=useState([]);
      const [htf,setHtf]=useState("");const [ltf,setLtf]=useState("");
      const [mktType,setMktType]=useState("trend");const [vol,setVol]=useState("medium");
      const [curStr,setCurStr]=useState("");const [devWave,setDevWave]=useState("");
      const [strStart,setStrStart]=useState("");const [fibT,setFibT]=useState("");
      const [scenL,setScenL]=useState("");const [inv,setInv]=useState("");
      const [altM,setAltM]=useState("");const [altP,setAltP]=useState("");const [altC,setAltC]=useState("");const [altB,setAltB]=useState("");
      const [eType,setEType]=useState("");
      const [ep,setEp]=useState(prefill.entryPoint!=null?String(prefill.entryPoint):"");
      const [sl2,setSl2]=useState(prefill.stopLoss!=null?String(prefill.stopLoss):"");
      const [tp2,setTp2]=useState(prefill.takeProfit!=null?String(prefill.takeProfit):"");
      const [rp,setRp]=useState(prefill.riskPercent!=null?String(prefill.riskPercent):"");
      const [ps,setPs]=useState(prefill.positionSize!=null?String(prefill.positionSize):"");
      const [cc,setCc]=useState("");
      const [pE,setPE]=useState(3);const [pF,setPF]=useState(3);const [pC,setPC]=useState(3);const [pP,setPP]=useState(2);
      const [pLS,setPLS]=useState(false);const [bF,setBF]=useState(false);const [bC,setBC]=useState(false);const [bR,setBR]=useState(false);const [bO,setBO]=useState(false);
      const [rta,setRta]=useState(true);
      const aRR=useMemo(()=>{const e=parseFloat(ep),s=parseFloat(sl2),tp=parseFloat(tp2);if(!e||!s||!tp||e===s)return null;return Math.abs(tp-e)/Math.abs(e-s);},[ep,sl2,tp2]);
      function save(){if(!instr.trim()){alert(t.instrReq);return;}addTrade({instrument:instr.toUpperCase(),sessions:sess,htfTimeframe:htf,ltfTimeframe:ltf,marketType:mktType,volatility:vol,currentStructure:curStr,developingWave:devWave,structureStart:strStart,fibTarget:fibT,scenarioLogic:scenL,invalidationLevel:inv,altMarkup:altM,altProbability:parseFloat(altP)||undefined,altConfirmation:altC,altBiasChange:altB,entryType:eType||undefined,entryPoint:parseFloat(ep)||undefined,stopLoss:parseFloat(sl2)||undefined,takeProfit:parseFloat(tp2)||undefined,plannedRR:prefill.plannedRR??aRR,riskPercent:parseFloat(rp)||undefined,positionSize:parseFloat(ps)||undefined,cancelConditions:cc,psychEnergy:pE,psychFocus:pF,psychCalm:pC,psychPressure:pP,psychLossStreak:pLS,biasFOMO:bF,biasConfirmation:bC,biasRevenge:bR,biasOverconfidence:bO,readyToAcceptStop:rta,status:"open",date:new Date().toISOString()});onSaved();}
      return(<div style={{height:"100%",display:"flex",flexDirection:"column"}}>
        <div style={{padding:"16px",paddingTop:"max(16px,env(safe-area-inset-top))",display:"flex",alignItems:"center",justifyContent:"space-between",borderBottom:`1px solid ${C.border}`,background:C.bg,position:"sticky",top:0,zIndex:10}}>
          <button onClick={onBack} style={{color:C.text2,fontSize:24,lineHeight:1}}>←</button>
          <span style={{fontSize:15,fontWeight:700,color:C.text}}>{t.newTrade}</span>
          <button onClick={save} style={{padding:"7px 18px",borderRadius:20,background:C.tint,color:"#fff",fontSize:13,fontWeight:600}}>{t.save}</button>
        </div>
        <div style={{flex:1,overflowY:"auto",padding:"12px 16px 100px",display:"flex",flexDirection:"column",gap:12}}>
          {prefill.instrument&&<div style={{display:"flex",alignItems:"center",gap:10,padding:"10px 14px",borderRadius:12,background:C.tintDim,border:`1px solid ${C.tint}40`}}><span>⚡</span><div><div style={{fontSize:12,fontWeight:700,color:C.tint}}>{t.prefillBanner}</div><div style={{fontSize:11,color:C.text2}}>{prefill.instrument} · {prefill.direction==="long"?t.longBtn:t.shortBtn}{prefill.positionSize?` · ${prefill.positionSize} lot`:""}{prefill.plannedRR?` · R:R 1:${prefill.plannedRR.toFixed(2)}`:""}</div></div></div>}
          <Card><SectionHeader n="1" title={t.sec1}/>
            <Input label={t.instrLabel} value={instr} onChange={v=>setInstr(v.toUpperCase())} placeholder={t.instrPh}/>
            <div style={{display:"grid",gridTemplateColumns:"1fr 1fr",gap:10}}><Input label={t.htf} value={htf} onChange={setHtf} placeholder="H4"/><Input label={t.ltf} value={ltf} onChange={setLtf} placeholder="M15"/></div>
            <Label>{t.sessions}</Label><div style={{display:"flex",flexWrap:"wrap",gap:8}}>{SESS.map(s=>{const a=sess.includes(s);return<button key={s} onClick={()=>setSess(p=>a?p.filter(x=>x!==s):[...p,s])} style={{padding:"6px 14px",borderRadius:20,fontSize:12,fontWeight:600,background:a?C.tint:C.bg3,color:a?"#fff":C.text2,border:`1px solid ${a?C.tint:C.border}`}}>{s}</button>;})}</div>
            <Label>{t.mktType}</Label><Seg options={[{label:t.trend,value:"trend"},{label:t.correction,value:"correction"},{label:t.range,value:"range"}]} value={mktType} onChange={setMktType}/>
            <Label>{t.vol}</Label><Seg options={[{label:t.low,value:"low"},{label:t.medium,value:"medium"},{label:t.high,value:"high"}]} value={vol} onChange={setVol}/>
          </Card>
          <Card><SectionHeader n="2" title={t.sec2}/>
            <Input label={t.structure} value={curStr} onChange={setCurStr} placeholder={t.structPh}/>
            <Input label={t.devWave} value={devWave} onChange={setDevWave} placeholder={t.devWavePh}/>
            <div style={{display:"grid",gridTemplateColumns:"1fr 1fr",gap:10}}><Input label={t.structStart} value={strStart} onChange={setStrStart}/><Input label={t.fibTarget} value={fibT} onChange={setFibT} placeholder={t.fibPh}/></div>
            <Input label={t.scenLogic} value={scenL} onChange={setScenL} placeholder={t.scenPh} multiline/>
            <Input label={t.invalidation} value={inv} onChange={setInv}/>
          </Card>
          <Card><SectionHeader n="3" title={t.sec3}/>
            <Input label={t.altMarkup} value={altM} onChange={setAltM} placeholder={t.altPh} multiline/>
            <div style={{display:"grid",gridTemplateColumns:"1fr 1fr",gap:10}}><Input label={t.altProb} value={altP} onChange={setAltP} type="number" placeholder="30"/><Input label={t.altBias} value={altB} onChange={setAltB}/></div>
            <Input label={t.altConfirm} value={altC} onChange={setAltC}/>
          </Card>
          <Card><SectionHeader n="4" title={t.sec4}/>
            <Label>{t.entryType}</Label>
            <div style={{marginBottom:6}}>
              <div style={{fontSize:10,color:C.text3,marginBottom:4}}>{t.impulse}</div>
              <div style={{display:"flex",gap:8}}>{["1","2","3","4","5"].map(w=><button key={w} onClick={()=>setEType(w)} style={{flex:1,padding:"10px 0",borderRadius:10,fontWeight:700,fontSize:15,background:eType===w?C.tint:C.bg3,color:eType===w?"#fff":C.text2,border:`1px solid ${eType===w?C.tint:C.border}`}}>{w}</button>)}</div>
              <div style={{fontSize:10,color:C.text3,margin:"8px 0 4px"}}>{t.corrLabel}</div>
              <div style={{display:"flex",gap:8}}>{["A","B","C"].map(w=><button key={w} onClick={()=>setEType(w)} style={{flex:1,padding:"10px 0",borderRadius:10,fontWeight:700,fontSize:15,background:eType===w?"#818CF8":C.bg3,color:eType===w?"#fff":C.text2,border:`1px solid ${eType===w?"#818CF8":C.border}`}}>{w}</button>)}</div>
            </div>
            <div style={{display:"grid",gridTemplateColumns:"1fr 1fr",gap:10}}><Input label={t.entryPoint} value={ep} onChange={setEp} type="number" placeholder="0.00"/><Input label={t.stopLoss} value={sl2} onChange={setSl2} type="number" placeholder="0.00"/></div>
            <div style={{display:"grid",gridTemplateColumns:"1fr 1fr",gap:10}}>
              <Input label={t.takeProfit} value={tp2} onChange={setTp2} type="number" placeholder="0.00"/>
              <div><Label>{t.plannedRR}</Label><div style={{background:aRR?(aRR>=2?C.profit+"20":aRR>=1?C.warning+"20":C.loss+"20"):C.bg3,borderRadius:10,padding:"10px 12px",textAlign:"center",fontWeight:700,fontSize:17,fontFamily:"'JetBrains Mono',monospace",color:aRR?(aRR>=2?C.profit:aRR>=1?C.warning:C.loss):C.text3}}>{aRR?`1:${aRR.toFixed(2)}`:"—"}</div></div>
            </div>
            <div style={{display:"grid",gridTemplateColumns:"1fr 1fr",gap:10}}><Input label={t.riskPctL} value={rp} onChange={setRp} type="number" placeholder="1"/><Input label={t.posSizeL} value={ps} onChange={setPs} type="number"/></div>
            <Input label={t.cancelCond} value={cc} onChange={setCc} placeholder={t.cancelPh} multiline/>
          </Card>
          <Card><SectionHeader n="5" title={t.sec5}/>
            <ScoreRow label={t.energy} value={pE} onChange={setPE}/>
            <ScoreRow label={t.focus} value={pF} onChange={setPF}/>
            <ScoreRow label={t.calm} value={pC} onChange={setPC}/>
            <ScoreRow label={t.pressure} value={pP} onChange={setPP}/>
            <Label style={{marginTop:8}}>{t.lossStreak}</Label>
            <Seg options={[{label:t.no,value:"no"},{label:t.yes,value:"yes"}]} value={pLS?"yes":"no"} onChange={v=>setPLS(v==="yes")}/>
            <Label style={{marginTop:8}}>{t.biases}</Label>
            <div style={{display:"flex",flexDirection:"column",gap:6}}>
              <Toggle label={t.fomo} value={bF} onChange={setBF}/>
              <Toggle label={t.biasConf} value={bC} onChange={setBC}/>
              <Toggle label={t.biasRev} value={bR} onChange={setBR}/>
              <Toggle label={t.biasOver} value={bO} onChange={setBO}/>
            </div>
            <div style={{marginTop:8,padding:14,borderRadius:14,background:rta?C.profit+"12":C.loss+"12",border:`1px solid ${rta?C.profit+"40":C.loss+"40"}`}}>
              <div style={{fontSize:13,color:C.text,marginBottom:10}}>{t.readyQ}</div>
              <div style={{display:"flex",gap:10}}>
                <button onClick={()=>setRta(true)} style={{flex:1,padding:10,borderRadius:10,fontWeight:700,fontSize:14,background:rta?C.profit:C.bg3,color:rta?"#fff":C.text2}}>{t.yes}</button>
                <button onClick={()=>setRta(false)} style={{flex:1,padding:10,borderRadius:10,fontWeight:700,fontSize:14,background:!rta?C.loss:C.bg3,color:!rta?"#fff":C.text2}}>{t.no}</button>
              </div>
            </div>
          </Card>
        </div>
      </div>);
    }

    // ── Trade Detail ──────────────────────────────────────────────────────────
    function TradeDetail({tradeId,onBack}){
      const {trades,updateTrade,deleteTrade}=useTrades();const {t}=useLang();
      const trade=trades.find(x=>x.id===tradeId);
      const [closing,setClosing]=useState(false);
      const [rR,setRR]=useState("");const [rU,setRU]=useState("");const [mae,setMae]=useState("");const [mfe,setMfe]=useState("");
      const [tClass,setTClass]=useState("");const [concl,setConcl]=useState("");const [eT,setET]=useState("none");const [wR,setWR]=useState(true);
      if(!trade)return null;
      const close=()=>{if(!rR){alert(t.resReq);return;}updateTrade(trade.id,{status:"closed",resultR:parseFloat(rR),resultUSD:parseFloat(rU)||undefined,mae:parseFloat(mae)||undefined,mfe:parseFloat(mfe)||undefined,tradeClass:tClass||undefined,mainConclusion:concl,errorType:eT,wouldRepeat:wR});setClosing(false);};
      const del=()=>{if(confirm(t.delTradeConfirm)){deleteTrade(trade.id);onBack();}};
      const rC=trade.resultR==null?C.text:trade.resultR>0?C.profit:C.loss;
      const Row=({label,value})=>value?<div style={{display:"flex",padding:"8px 0",borderBottom:`1px solid ${C.border}`,gap:12}}><span style={{fontSize:12,color:C.text3,minWidth:130,flexShrink:0}}>{label}</span><span style={{fontSize:12,color:C.text}}>{value}</span></div>:null;
      return(<div style={{height:"100%",display:"flex",flexDirection:"column"}}>
        <div style={{padding:"16px",paddingTop:"max(16px,env(safe-area-inset-top))",display:"flex",alignItems:"center",justifyContent:"space-between",borderBottom:`1px solid ${C.border}`,background:C.bg,position:"sticky",top:0,zIndex:10}}>
          <button onClick={onBack} style={{color:C.text2,fontSize:24}}>←</button>
          <span style={{fontFamily:"'JetBrains Mono',monospace",fontWeight:700,color:C.text,fontSize:16}}>{trade.instrument}</span>
          <button onClick={del} style={{color:C.loss,fontSize:13}}>{t.del}</button>
        </div>
        <div style={{flex:1,overflowY:"auto",padding:"12px 16px 100px",display:"flex",flexDirection:"column",gap:12}}>
          <Card glow={trade.status==="closed"&&trade.resultR>0}>
            <div style={{display:"flex",justifyContent:"space-between",alignItems:"flex-start"}}>
              <div><div style={{fontSize:11,fontFamily:"'JetBrains Mono',monospace",color:C.text3,marginBottom:4}}>{new Date(trade.date).toLocaleDateString("ru-RU",{day:"2-digit",month:"short",year:"numeric"})}</div><div style={{display:"flex",gap:8,alignItems:"center",flexWrap:"wrap"}}>{trade.tradeClass&&<span style={{padding:"3px 10px",borderRadius:8,fontSize:12,fontWeight:700,background:(CLS_COLOR[trade.tradeClass]||C.text3)+"25",color:CLS_COLOR[trade.tradeClass]}}>{trade.tradeClass}</span>}{trade.entryType&&<span style={{fontSize:12,color:C.text3}}>W{trade.entryType}</span>}</div></div>
              {trade.status==="open"?<span style={{fontSize:11,color:C.warning,fontWeight:700,background:C.warning+"20",padding:"4px 10px",borderRadius:8}}>OPEN</span>:<div style={{textAlign:"right"}}><div style={{fontSize:28,fontWeight:700,fontFamily:"'JetBrains Mono',monospace",color:rC}}>{trade.resultR>=0?"+":""}{trade.resultR?.toFixed(2)}R</div>{trade.resultUSD!=null&&<div style={{fontSize:12,color:C.text3,fontFamily:"'JetBrains Mono',monospace"}}>${trade.resultUSD>=0?"+":""}{trade.resultUSD?.toFixed(2)}</div>}</div>}
            </div>
          </Card>
          {(trade.htfTimeframe||trade.sessions?.length>0)&&<Card><div style={{fontSize:12,fontWeight:700,color:C.text,marginBottom:6}}>{t.timeframes}</div><Row label="HTF" value={trade.htfTimeframe}/><Row label="LTF" value={trade.ltfTimeframe}/>{trade.sessions?.length>0&&<Row label={t.sessions} value={trade.sessions.join(", ")}/>}</Card>}
          {(trade.currentStructure||trade.scenarioLogic)&&<Card><div style={{fontSize:12,fontWeight:700,color:C.text,marginBottom:6}}>{t.mainScen}</div><Row label={t.structure} value={trade.currentStructure}/><Row label={t.devWave} value={trade.developingWave}/><Row label={t.fibTarget} value={trade.fibTarget}/><Row label={t.invalidation} value={trade.invalidationLevel}/>{trade.scenarioLogic&&<div style={{marginTop:8,padding:"10px 12px",background:C.bg3,borderRadius:10}}><div style={{fontSize:11,color:C.text3,marginBottom:4}}>{t.logic}</div><div style={{fontSize:13,color:C.text,lineHeight:1.6}}>{trade.scenarioLogic}</div></div>}</Card>}
          {(trade.entryPoint||trade.stopLoss)&&<Card><div style={{fontSize:12,fontWeight:700,color:C.text,marginBottom:6}}>{t.tradePlan}</div><Row label={t.entryPoint} value={trade.entryPoint}/><Row label={t.stopLoss} value={trade.stopLoss}/><Row label={t.takeProfit} value={trade.takeProfit}/><Row label={t.plannedRR} value={trade.plannedRR?`1:${trade.plannedRR.toFixed(2)}`:null}/><Row label={t.riskPctL} value={trade.riskPercent?`${trade.riskPercent}%`:null}/></Card>}
          {trade.mainConclusion&&<Card><div style={{fontSize:12,fontWeight:700,color:C.text,marginBottom:6}}>{t.conclusionT}</div><div style={{fontSize:13,color:C.text,lineHeight:1.6}}>{trade.mainConclusion}</div></Card>}
          {trade.status==="open"&&!closing&&<button onClick={()=>setClosing(true)} style={{padding:"14px",borderRadius:14,background:C.tint,color:"#fff",fontWeight:700,fontSize:15}}>{t.closeTrade}</button>}
          {trade.status==="open"&&closing&&<Card>
            <div style={{fontSize:14,fontWeight:700,color:C.text,marginBottom:12}}>{t.tradeRes}</div>
            <div style={{display:"grid",gridTemplateColumns:"1fr 1fr",gap:10,marginBottom:10}}><Input label={t.resR} value={rR} onChange={setRR} type="number" placeholder="2.5 / -1"/><Input label={t.resUSD} value={rU} onChange={setRU} type="number" placeholder="250"/><Input label={t.maeL} value={mae} onChange={setMae} type="number" placeholder="-0.5"/><Input label={t.mfeL} value={mfe} onChange={setMfe} type="number" placeholder="3.2"/></div>
            <Label>{t.tradeClass}</Label><div style={{display:"flex",gap:8,marginBottom:10}}>{["A+","A","B","C","D"].map(c=><button key={c} onClick={()=>setTClass(c)} style={{flex:1,padding:"10px 0",borderRadius:10,fontWeight:700,fontSize:14,background:tClass===c?(CLS_COLOR[c]||C.tint):C.bg3,color:tClass===c?"#fff":C.text2}}>{c}</button>)}</div>
            <Label>{t.errType}</Label><Seg options={[{label:t.errNone,value:"none"},{label:t.errAn,value:"analysis"},{label:t.errEx,value:"execution"}]} value={eT} onChange={setET}/>
            <Label style={{marginTop:10}}>{t.wouldRep}</Label><Seg options={[{label:t.yes,value:"yes"},{label:t.no,value:"no"}]} value={wR?"yes":"no"} onChange={v=>setWR(v==="yes")}/>
            <Input label={t.conclusion} value={concl} onChange={setConcl} placeholder={t.conclusionPh} multiline style={{marginTop:10}}/>
            <div style={{display:"grid",gridTemplateColumns:"1fr 1fr",gap:10,marginTop:12}}><button onClick={()=>setClosing(false)} style={{padding:12,borderRadius:12,background:C.bg3,color:C.text2,fontWeight:600}}>{t.cancel}</button><button onClick={close} style={{padding:12,borderRadius:12,background:C.tint,color:"#fff",fontWeight:700}}>{t.saveBtn}</button></div>
          </Card>}
          {trade.status==="closed"&&<button onClick={()=>updateTrade(trade.id,{status:"open",resultR:undefined,resultUSD:undefined})} style={{padding:12,borderRadius:12,background:C.bg3,color:C.text2,border:`1px solid ${C.border}`,fontSize:13}}>{t.reopen}</button>}
        </div>
      </div>);
    }

    // ── Settings ──────────────────────────────────────────────────────────────
    function Settings(){
      const {trades,stats}=useTrades();const {lang,setLang,t}=useLang();
      const {viewMode,setViewMode}=useView();
      const [fmt,setFmt]=useState("json");const [importText,setImportText]=useState("");const [iMode,setIMode]=useState("merge");
      const [toast,setToast]=useState(null);const fileRef=React.useRef();
      const isIOS=/iPad|iPhone|iPod/.test(navigator.userAgent);
      const showToast=(msg,ok=true)=>{setToast({msg,ok});setTimeout(()=>setToast(null),3000);};

      function getPayload(){
        if(fmt==="json") return{text:JSON.stringify({version:1,exportedAt:new Date().toISOString(),trades},null,2),ext:"json"};
        const cols=["id","date","instrument","status","resultR","resultUSD","tradeClass","entryType","marketType","volatility","developingWave","entryPoint","stopLoss","takeProfit","plannedRR","riskPercent","positionSize","psychEnergy","psychFocus","psychCalm","psychPressure","mainConclusion","errorType","wouldRepeat"];
        const esc=v=>v==null?"":String(v).includes(",")?`"${String(v).replace(/"/g,'""')}"`:String(v);
        return{text:[cols.join(","),...trades.map(tr=>cols.map(c=>esc(tr[c])).join(","))].join("\n"),ext:"csv"};
      }

      function handleCopy(){const{text}=getPayload();navigator.clipboard.writeText(text).then(()=>showToast(t.copiedToast)).catch(()=>showToast(t.copyErr,false));}

      function handleDownload(){
        const{text,ext}=getPayload();const mime=ext==="json"?"application/json":"text/csv";
        const filename=`trader-journal-${new Date().toISOString().slice(0,10)}.${ext}`;
        const blob=new Blob([text],{type:mime});const url=URL.createObjectURL(blob);
        const a=document.createElement("a");a.href=url;a.download=filename;
        document.body.appendChild(a);a.click();setTimeout(()=>{document.body.removeChild(a);URL.revokeObjectURL(url);},300);
        showToast(ext==="json"?t.exportedToast(trades.length):t.csvToast(trades.length));
      }

      function handleFile(e){const f=e.target.files[0];if(!f)return;const r=new FileReader();r.onload=ev=>setImportText(ev.target.result);r.readAsText(f);e.target.value="";}

      function handleImport(){
        if(!importText.trim()){showToast(t.noDataToast,false);return;}
        try{
          const parsed=JSON.parse(importText);const incoming=Array.isArray(parsed)?parsed:(parsed.trades||[]);
          if(!incoming.length){showToast(t.noTradesInFile,false);return;}
          const cur=loadTrades();
          const result=iMode==="replace"?incoming:[...incoming.filter(x=>!new Set(cur.map(y=>y.id)).has(x.id)),...cur];
          saveTrades(result);window.location.reload();
        }catch{showToast(t.parseErr,false);}
      }

      const Sec=({title,children})=><div style={{marginBottom:4}}><div style={{fontSize:11,fontFamily:"'JetBrains Mono',monospace",letterSpacing:1,color:C.text3,textTransform:"uppercase",marginBottom:8,paddingLeft:4}}>{title}</div>{children}</div>;

      return(<div style={{padding:"0 0 100px"}}>
        {toast&&<div style={{position:"fixed",top:60,left:"50%",transform:"translateX(-50%)",zIndex:999,background:toast.ok?C.profit:C.loss,color:"#fff",padding:"10px 20px",borderRadius:20,fontSize:13,fontWeight:600,whiteSpace:"nowrap",boxShadow:`0 4px 20px ${toast.ok?C.profit:C.loss}50`}}>{toast.ok?"✓":"✕"} {toast.msg}</div>}
        <div style={{padding:"max(24px,env(safe-area-inset-top)) 16px 12px"}}><div style={{fontSize:26,fontWeight:700,color:C.text}}>{t.settingsTitle}</div></div>
        <div style={{padding:"0 16px",display:"flex",flexDirection:"column",gap:16}}>

          {/* Language */}
          <Sec title={t.langSection}>
            <Card>
              <div style={{display:"flex",gap:10}}>
                {[{v:"ru",flag:"🇷🇺",label:"Русский"},{v:"en",flag:"🇬🇧",label:"English"}].map(l=>{
                  const a=lang===l.v;
                  return<button key={l.v} onClick={()=>setLang(l.v)} style={{flex:1,padding:"14px 10px",borderRadius:12,textAlign:"center",background:a?C.tint:C.bg3,border:`1.5px solid ${a?C.tint:C.border}`,boxShadow:a?`0 0 14px ${C.tint}40`:"none"}}>
                    <div style={{fontSize:24,marginBottom:4}}>{l.flag}</div>
                    <div style={{fontSize:13,fontWeight:700,color:a?"#fff":C.text}}>{l.label}</div>
                  </button>;
                })}
              </div>
            </Card>
          </Sec>

          {/* View Mode */}
          <Sec title={t.viewModeTitle}>
            <Card>
              <div style={{display:"flex",gap:10}}>
                {[
                  {v:"mobile", icon:"📱", label:t.mobileView},
                  {v:"web",    icon:"🖥",  label:t.webView},
                ].map(item=>{
                  const a=viewMode===item.v;
                  return<button key={item.v} onClick={()=>setViewMode(item.v)} style={{flex:1,padding:"14px 10px",borderRadius:12,textAlign:"center",background:a?C.tint:C.bg3,border:`1.5px solid ${a?C.tint:C.border}`,boxShadow:a?`0 0 14px ${C.tint}40`:"none"}}>
                    <div style={{fontSize:24,marginBottom:4}}>{item.icon}</div>
                    <div style={{fontSize:13,fontWeight:700,color:a?"#fff":C.text}}>{item.label}</div>
                  </button>;
                })}
              </div>
            </Card>
          </Sec>

          {/* Journal summary */}
          <Card style={{background:C.tintDim,border:`1px solid ${C.tint}30`}}>
            <div style={{display:"flex",justifyContent:"space-between",alignItems:"center"}}>
              <div><div style={{fontSize:13,fontWeight:700,color:C.tint}}>{t.currentJournal}</div><div style={{fontSize:12,color:C.text2,marginTop:2}}>{trades.length} {t.trades} · {stats.open} {t.open.toLowerCase()} · {stats.total} {t.closed.toLowerCase()}</div></div>
              <div style={{fontSize:28,fontWeight:700,fontFamily:"'JetBrains Mono',monospace",color:stats.totalR>=0?C.profit:C.loss}}>{stats.totalR>=0?"+":""}{stats.totalR.toFixed(1)}R</div>
            </div>
          </Card>

          {/* Export */}
          <Sec title={t.exportSection}>
            <Card>
              <Label>{t.formatLabel}</Label>
              <div style={{display:"flex",gap:10,marginBottom:14}}>
                {[{v:"json",icon:"📦",label:"JSON",sub:t.jsonSub},{v:"csv",icon:"📊",label:"CSV",sub:t.csvSub}].map(f=>{
                  const a=fmt===f.v;
                  return<button key={f.v} onClick={()=>setFmt(f.v)} style={{flex:1,padding:"12px 10px",borderRadius:12,textAlign:"center",background:a?C.tint:C.bg3,border:`1.5px solid ${a?C.tint:C.border}`,boxShadow:a?`0 0 14px ${C.tint}40`:"none"}}>
                    <div style={{fontSize:20,marginBottom:4}}>{f.icon}</div>
                    <div style={{fontSize:13,fontWeight:700,color:a?"#fff":C.text}}>{f.label}</div>
                    <div style={{fontSize:10,color:a?"rgba(255,255,255,0.75)":C.text3,marginTop:2}}>{f.sub}</div>
                  </button>;
                })}
              </div>
              {/* Copy — always shown, works on iOS and desktop */}
              <button onClick={handleCopy} style={{width:"100%",padding:"14px",borderRadius:12,fontWeight:700,fontSize:15,background:C.tint,color:"#fff",border:"none",boxShadow:`0 4px 16px ${C.tint}40`,marginBottom:isIOS?0:8}}>
                {t.copyBtn} {fmt.toUpperCase()}
              </button>
              {/* Download — desktop only */}
              {!isIOS&&<button onClick={handleDownload} style={{width:"100%",marginTop:8,padding:"13px",borderRadius:12,fontWeight:700,fontSize:14,background:C.bg3,color:C.text,border:`1px solid ${C.border}`}}>
                {t.dlBtn} {fmt.toUpperCase()}
              </button>}
              {/* iOS hint */}
              {isIOS&&<div style={{marginTop:12,padding:"12px 14px",borderRadius:10,background:C.bg3,border:`1px solid ${C.border}`}}>
                <div style={{fontSize:12,fontWeight:700,color:C.text,marginBottom:8}}>{t.iosTitle}</div>
                {[t.iosS1,t.iosS2,t.iosS3,t.iosS4].map((s,i)=><div key={i} style={{display:"flex",gap:10,marginBottom:6,alignItems:"flex-start"}}><div style={{width:20,height:20,borderRadius:10,background:C.tintDim,flexShrink:0,display:"flex",alignItems:"center",justifyContent:"center",fontSize:10,fontWeight:700,color:C.tint}}>{i+1}</div><span style={{fontSize:12,color:C.text2,lineHeight:1.5}}>{s}</span></div>)}
              </div>}
            </Card>
          </Sec>

          {/* Import */}
          <Sec title={t.importSection}>
            <Card>
              <div style={{fontSize:13,color:C.text2,marginBottom:12,lineHeight:1.5}}>{t.importDesc}</div>
              <Label>{t.importMode}</Label>
              <Seg options={[{label:t.merge,value:"merge"},{label:t.replace,value:"replace"}]} value={iMode} onChange={setIMode}/>
              <div style={{fontSize:11,color:C.text3,marginTop:6,marginBottom:12}}>{iMode==="merge"?t.mergeHint:t.replaceHint}</div>
              <input ref={fileRef} type="file" accept=".json" onChange={handleFile} style={{display:"none"}}/>
              <button onClick={()=>fileRef.current.click()} style={{width:"100%",padding:"13px",borderRadius:12,fontWeight:700,fontSize:14,background:C.bg3,color:C.text,border:`1px dashed ${C.border}`,marginBottom:10}}>{t.chooseFile}</button>
              <Label>{t.pasteLabel}</Label>
              <textarea value={importText} onChange={e=>setImportText(e.target.value)} placeholder={'{\n  "trades": [...]\n}'} rows={5} style={{width:"100%",background:C.bg3,border:`1px solid ${importText?C.tint+"60":C.border}`,borderRadius:10,color:C.text,fontSize:12,padding:"10px 12px",fontFamily:"'JetBrains Mono',monospace",resize:"vertical",lineHeight:1.5}}/>
              {importText&&<div style={{fontSize:11,color:C.tint,marginTop:4,marginBottom:8}}>{t.importReady}</div>}
              <button onClick={handleImport} disabled={!importText.trim()} style={{width:"100%",marginTop:8,padding:"13px",borderRadius:12,fontWeight:700,fontSize:14,background:importText.trim()?C.tint:C.bg3,color:importText.trim()?"#fff":C.text3,border:"none",opacity:importText.trim()?1:0.5}}>
                {iMode==="replace"?t.replaceBtn:t.importBtn}
              </button>
            </Card>
          </Sec>

          {/* Danger */}
          <Sec title={t.dangerSection}>
            <Card style={{border:`1px solid ${C.loss}30`}}>
              <div style={{fontSize:13,color:C.text2,marginBottom:12}}>{t.clearDesc}</div>
              <button onClick={()=>{if(confirm(t.clearConfirm(trades.length))){saveTrades([]);window.location.reload();}}} style={{width:"100%",padding:"12px",borderRadius:12,fontWeight:700,fontSize:14,background:C.lossDim,color:C.loss,border:`1px solid ${C.loss}40`}}>{t.clearAll}</button>
            </Card>
          </Sec>

        </div>
      </div>);
    }

    // ── Sidebar (web mode) ────────────────────────────────────────────────────
    function Sidebar({ active, onNav }) {
      const { t } = useLang();
      const NAV = [
        { id:"dashboard", label:t.home,     icon:"⊡" },
        { id:"journal",   label:t.journal,  icon:"≡" },
        { id:"calc",      label:t.calc,     icon:"◇" },
        { id:"stats",     label:t.stats,    icon:"▦" },
        { id:"settings",  label:t.settings, icon:"⚙" },
      ];
      return (
        <div style={{
          width:200, flexShrink:0,
          background:C.bg2, borderRight:`1px solid ${C.border}`,
          display:"flex", flexDirection:"column",
          padding:"28px 12px 24px", gap:4,
        }}>
          <div style={{
            fontSize:15, fontWeight:700, color:C.tint,
            fontFamily:"'JetBrains Mono',monospace",
            marginBottom:24, padding:"0 8px", letterSpacing:1,
          }}>
            TRADER JOURNAL
          </div>
          {NAV.map(item => {
            const a = active === item.id;
            return (
              <button key={item.id} onClick={() => onNav(item.id)} style={{
                display:"flex", alignItems:"center", gap:10,
                padding:"10px 12px", borderRadius:10, textAlign:"left",
                background: a ? C.tintDim : "transparent",
                border:`1px solid ${a ? C.tint+"40" : "transparent"}`,
              }}>
                <span style={{ fontSize:18, color:a ? C.tint : C.text3 }}>{item.icon}</span>
                <span style={{ fontSize:13, fontWeight:a?700:400, color:a ? C.tint : C.text2 }}>{item.label}</span>
              </button>
            );
          })}
          <div style={{ marginTop:"auto" }}>
            <button onClick={() => onNav("new")} style={{
              width:"100%", padding:"12px", borderRadius:12,
              background:C.tint, color:"#fff", fontWeight:700, fontSize:13,
              display:"flex", alignItems:"center", justifyContent:"center", gap:6,
            }}>
              <span style={{ fontSize:18, lineHeight:1 }}>+</span> {t.addTrade}
            </button>
          </div>
        </div>
      );
    }

    // ── Bottom Nav ────────────────────────────────────────────────────────────
    function BottomNav({active,onNav}){
      const {t}=useLang();
      const NAV=[{id:"dashboard",label:t.home,icon:"⊡"},{id:"journal",label:t.journal,icon:"≡"},{id:"calc",label:t.calc,icon:"◇"},{id:"stats",label:t.stats,icon:"▦"},{id:"settings",label:t.settings,icon:"⚙"}];
      return(<div style={{position:"fixed",bottom:0,left:0,right:0,background:C.bg+"F0",borderTop:`1px solid ${C.border}`,display:"flex",padding:"8px 0",paddingBottom:"max(20px,env(safe-area-inset-bottom))",backdropFilter:"blur(16px)",zIndex:100}}>
        {NAV.map(item=>{const a=active===item.id;return<button key={item.id} onClick={()=>onNav(item.id)} style={{flex:1,display:"flex",flexDirection:"column",alignItems:"center",gap:3,padding:"6px 0"}}><span style={{fontSize:20,color:a?C.tint:C.text3}}>{item.icon}</span><span style={{fontSize:10,color:a?C.tint:C.text3,fontWeight:a?700:400}}>{item.label}</span></button>;})}
      </div>);
    }

    // ── App ───────────────────────────────────────────────────────────────────
    function AppContent() {
      const { viewMode } = useView();
      const [screen,setScreen]=useState("dashboard");
      const [activeTab,setActiveTab]=useState("dashboard");
      const [selId,setSelId]=useState(null);
      const [prefill,setPrefill]=useState(null);
      const nav=id=>{if(id==="new"){setPrefill(null);setScreen("new");}else{setScreen(id);setActiveTab(id);}};
      const openTrade=id=>{setSelId(id);setScreen("trade");};
      const openInJournal=data=>{setPrefill(data);setScreen("new");};
      const showNav=!["new","trade"].includes(screen);

      const screens = <>
        {screen==="dashboard"&&<Dashboard onNav={nav} onOpenTrade={openTrade}/>}
        {screen==="journal"&&<Journal onNav={nav} onOpenTrade={openTrade}/>}
        {screen==="calc"&&<Calculator onOpenInJournal={openInJournal}/>}
        {screen==="stats"&&<Stats/>}
        {screen==="settings"&&<Settings/>}
        {screen==="new"&&<NewTrade prefill={prefill||{}} onBack={()=>{setPrefill(null);setScreen(activeTab);}} onSaved={()=>{setPrefill(null);setScreen("journal");}}/>}
        {screen==="trade"&&<TradeDetail tradeId={selId} onBack={()=>setScreen(activeTab)}/>}
      </>;

      if (viewMode === "web") {
        return (
          <div style={{display:"flex",height:"100vh",background:C.bg,overflow:"hidden"}}>
            {showNav && <Sidebar active={activeTab} onNav={nav}/>}
            <div style={{flex:1,display:"flex",flexDirection:"column",overflow:"hidden"}}>
              <div style={{flex:1,overflowY:(screen==="new"||screen==="trade")?"hidden":"auto"}}>
                {screens}
              </div>
            </div>
          </div>
        );
      }

      return (
        <div style={{height:"100vh",maxWidth:480,margin:"0 auto",background:C.bg,position:"relative",display:"flex",flexDirection:"column"}}>
          <div style={{flex:1,overflowY:(screen==="new"||screen==="trade")?"hidden":"auto"}}>
            {screens}
          </div>
          {showNav&&<BottomNav active={activeTab} onNav={nav}/>}
        </div>
      );
    }

    function App(){
      return (
        <LangProvider>
          <TradesProvider>
            <ViewProvider>
              <AppContent/>
            </ViewProvider>
          </TradesProvider>
        </LangProvider>
      );
    }

    ReactDOM.createRoot(document.getElementById("root")).render(<App/>);
  </script>
</body>
</html>
