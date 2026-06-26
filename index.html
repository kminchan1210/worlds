import React, { useState, useEffect } from 'react';
import { Trophy, ArrowRight, RotateCcw, Medal, AlertTriangle, Shuffle, HelpCircle } from 'lucide-react';

// 피파 랭킹 및 국기 데이터
const teamData = {
  '아르헨티나': { code: 'ar', rank: 1 },
  '프랑스': { code: 'fr', rank: 2 },
  '벨기에': { code: 'be', rank: 3 },
  '잉글랜드': { code: 'gb-eng', rank: 4 },
  '브라질': { code: 'br', rank: 5 },
  '포르투갈': { code: 'pt', rank: 6 },
  '네덜란드': { code: 'nl', rank: 7 },
  '스페인': { code: 'es', rank: 8 },
  '이탈리아': { code: 'it', rank: 9 },
  '크로아티아': { code: 'hr', rank: 10 },
  '미국': { code: 'us', rank: 11 },
  '콜롬비아': { code: 'co', rank: 12 },
  '모로코': { code: 'ma', rank: 13 },
  '멕시코': { code: 'mx', rank: 14 },
  '우루과이': { code: 'uy', rank: 15 },
  '독일': { code: 'de', rank: 16 },
  '세네갈': { code: 'sn', rank: 17 },
  '일본': { code: 'jp', rank: 18 },
  '스위스': { code: 'ch', rank: 19 },
  '이란': { code: 'ir', rank: 20 },
  '대한민국': { code: 'kr', rank: 23 },
  '호주': { code: 'au', rank: 24 },
  '오스트리아': { code: 'at', rank: 25 },
  '우크라이나': { code: 'ua', rank: 22 },
  '스웨덴': { code: 'se', rank: 27 },
  '폴란드': { code: 'pl', rank: 28 },
  '웨일스': { code: 'gb-wls', rank: 29 },
  '나이지리아': { code: 'ng', rank: 30 },
  '에콰도르': { code: 'ec', rank: 31 },
  '페루': { code: 'pe', rank: 32 },
  '세르비아': { code: 'rs', rank: 33 },
  '카타르': { code: 'qa', rank: 34 },
  '체코': { code: 'cz', rank: 36 },
  '이집트': { code: 'eg', rank: 37 },
  '코트디부아르': { code: 'ci', rank: 38 },
  '스코틀랜드': { code: 'gb-sct', rank: 39 },
  '튀르키예': { code: 'tr', rank: 40 },
  '튀니지': { code: 'tn', rank: 41 },
  '알제리': { code: 'dz', rank: 43 },
  '노르웨이': { code: 'no', rank: 47 },
  '캐나다': { code: 'ca', rank: 49 },
  '사우디아라비아': { code: 'sa', rank: 53 },
  '파라과이': { code: 'py', rank: 56 },
  '남아프리카 공화국': { code: 'za', rank: 59 },
  '이라크': { code: 'iq', rank: 58 },
  '콩고 민주 공화국': { code: 'cd', rank: 63 },
  '카보베르데': { code: 'cv', rank: 65 },
  '우즈베키스탄': { code: 'uz', rank: 64 },
  '가나': { code: 'gh', rank: 68 },
  '보스니아 헤르체고비나': { code: 'ba', rank: 74 },
  '요르단': { code: 'jo', rank: 71 },
  '파나마': { code: 'pa', rank: 45 },
  '아이티': { code: 'ht', rank: 90 },
  '퀴라소': { code: 'cw', rank: 91 },
  '뉴질랜드': { code: 'nz', rank: 104 }
};

// 초기 조별리그 배치
const initialGroups = {
  A: ['멕시코', '남아프리카 공화국', '대한민국', '체코'],
  B: ['캐나다', '보스니아 헤르체고비나', '카타르', '스위스'],
  C: ['브라질', '모로코', '아이티', '스코틀랜드'],
  D: ['미국', '파라과이', '호주', '튀르키예'],
  E: ['독일', '퀴라소', '코트디부아르', '에콰도르'],
  F: ['네덜란드', '일본', '스웨덴', '튀니지'],
  G: ['벨기에', '이집트', '이란', '뉴질랜드'],
  H: ['스페인', '카보베르데', '사우디아라비아', '우루과이'],
  I: ['프랑스', '세네갈', '이라크', '노르웨이'],
  J: ['아르헨티나', '알제리', '오스트리아', '요르단'],
  K: ['포르투갈', '콩고 민주 공화국', '우즈베키스탄', '콜롬비아'],
  L: ['잉글랜드', '크로아티아', '가나', '파나마']
};

// 8개 와일드카드 슬롯 정보와 매칭 가능한 조 목록 규칙
const wildcardSlots = [
  { idx: 0, label: "매치 1 (E조 1위 상대)", allowed: ['A', 'B', 'C', 'D', 'F'] },
  { idx: 1, label: "매치 2 (I조 1위 상대)", allowed: ['C', 'D', 'F', 'G', 'H'] },
  { idx: 2, label: "매치 7 (A조 1위 상대)", allowed: ['C', 'E', 'F', 'I', 'J'] },
  { idx: 3, label: "매치 8 (L조 1위 상대)", allowed: ['E', 'H', 'I', 'J', 'K'] },
  { idx: 4, label: "매치 11 (D조 1위 상대)", allowed: ['B', 'E', 'F', 'I', 'J'] },
  { idx: 5, label: "매치 12 (G조 1위 상대)", allowed: ['A', 'E', 'H', 'I', 'J'] },
  { idx: 6, label: "매치 15 (B조 1위 상대)", allowed: ['E', 'F', 'G', 'I', 'J'] },
  { idx: 7, label: "매치 16 (K조 1위 상대)", allowed: ['D', 'E', 'I', 'J', 'L'] }
];

export default function App() {
  const [step, setStep] = useState(0);
  const [standings, setStandings] = useState(initialGroups);
  const [wildcards, setWildcards] = useState([]);
  
  // 8개 와일드카드 매치 슬롯별 선택 완료된 국가 배열 (크기 8)
  const [wildcardAssignments, setWildcardAssignments] = useState(new Array(8).fill(null));

  const [r32, setR32] = useState([]);
  const [r16, setR16] = useState([]);
  const [qf, setQf] = useState([]);
  const [sf, setSf] = useState([]);
  const [finals, setFinals] = useState({ final: null, third: null });
  const [draggedItem, setDraggedItem] = useState(null);

  // 선택한 와일드카드가 변경될 때 배치 초기화
  useEffect(() => {
    setWildcardAssignments(new Array(8).fill(null));
  }, [wildcards]);

  const getTeamGroup = (teamName) => {
    return Object.keys(initialGroups).find(g => standings[g].includes(teamName));
  };

  // 특정 팀이 이 대진 슬롯에 배정될 수 있는지 검사
  const isTeamEligibleForSlot = (teamName, slotIdx) => {
    if (!teamName) return false;
    const group = getTeamGroup(teamName);
    return wildcardSlots[slotIdx].allowed.includes(group);
  };

  // 수동 매칭 선택 이벤트 핸들러
  const assignTeamToSlot = (teamName, slotIdx) => {
    const newAssignments = [...wildcardAssignments];

    // 중복 배치 제거: 이미 이 팀이 다른 슬롯에 배치되어 있었다면 비우기
    const prevSlotIdx = newAssignments.indexOf(teamName);
    if (prevSlotIdx !== -1) {
      newAssignments[prevSlotIdx] = null;
    }

    // 새 슬롯에 배정
    newAssignments[slotIdx] = teamName;
    setWildcardAssignments(newAssignments);
  };

  // 와일드카드 자동 분배 배치 알고리즘 (백트래킹)
  const autoAssign = () => {
    if (wildcards.length !== 8) return;
    let used = new Array(8).fill(false);
    let matched = new Array(8).fill(null);

    const solve = (slotIdx) => {
      if (slotIdx === 8) return true;
      const allowed = wildcardSlots[slotIdx].allowed;
      
      for (let i = 0; i < 8; i++) {
        if (!used[i]) {
          const wcGroup = getTeamGroup(wildcards[i]);
          if (allowed.includes(wcGroup)) {
            used[i] = true;
            matched[slotIdx] = wildcards[i];
            if (solve(slotIdx + 1)) return true;
            used[i] = false;
            matched[slotIdx] = null;
          }
        }
      }
      return false;
    };

    if (solve(0)) {
      setWildcardAssignments(matched);
    } else {
      alert("⚠️ 선택하신 3위 팀들의 조합으로는 공식 피파 와일드카드 규칙에 맞는 완벽한 대진 매칭을 완성할 수 없습니다! 다른 3위 팀들을 골라보세요.");
    }
  };

  // 모든 슬롯이 8개 중복 없이 꽉 채워졌는지 검증
  const isAssignmentComplete = () => {
    if (wildcardAssignments.includes(null)) return false;
    const uniqueAssignments = new Set(wildcardAssignments.filter(Boolean));
    if (uniqueAssignments.size !== 8) return false;

    // 모든 팀이 제한 조건에 잘 부합하는지 한 번 더 확인
    return wildcardAssignments.every((team, idx) => isTeamEligibleForSlot(team, idx));
  };

  const renderTeam = (teamName, showGroupInfo = false, align = 'center') => {
    if (!teamName) return null;
    const teamInfo = teamData[teamName];
    if (!teamInfo) return <span className="font-semibold">{teamName}</span>;

    let groupInfoStr = "";
    if (showGroupInfo) {
      for (const [groupName, teams] of Object.entries(standings)) {
        const idx = teams.indexOf(teamName);
        if (idx !== -1) {
          groupInfoStr = `${groupName}조 ${idx + 1}위`;
          break;
        }
      }
    }

    const justifyClass = align === 'start' ? 'justify-start' : align === 'end' ? 'justify-end' : 'justify-center';
    const alignClass = align === 'start' ? 'items-start' : align === 'end' ? 'items-end' : 'items-center';
    const textCenterClass = align === 'center' ? 'text-center' : 'text-left';

    return (
      <div className={`flex flex-col ${alignClass} w-full overflow-hidden`}>
        {showGroupInfo && groupInfoStr && (
           <span className="text-[10px] sm:text-xs px-2 py-0.5 rounded-full bg-black/10 mb-1 whitespace-nowrap">
             {groupInfoStr}
           </span>
        )}
        <div className={`flex flex-wrap items-center ${justifyClass} gap-x-1.5 gap-y-0.5 w-full`}>
          <img
            src={`https://flagcdn.com/w40/${teamInfo.code}.png`}
            alt={`${teamName} 국기`}
            className="w-5 sm:w-6 h-auto border border-gray-300 shadow-sm rounded-sm shrink-0 bg-white"
          />
          <span className={`font-bold text-sm sm:text-base leading-tight break-keep ${textCenterClass}`}>
            {teamName}
          </span>
          <span className="text-[11px] sm:text-xs font-normal opacity-80 whitespace-nowrap shrink-0">
            ({teamInfo.rank}위)
          </span>
        </div>
      </div>
    );
  };

  const handleDragStart = (e, groupName, index) => {
    setDraggedItem({ groupName, index });
    e.dataTransfer.effectAllowed = 'move';
    setTimeout(() => { e.target.classList.add('opacity-40'); }, 0);
  };

  const handleDragEnd = (e) => {
    e.target.classList.remove('opacity-40');
    setDraggedItem(null);
  };

  const handleDragOver = (e) => {
    e.preventDefault();
  };

  const handleDrop = (e, targetGroupName, targetIndex) => {
    e.preventDefault();
    if (!draggedItem) return;
    if (draggedItem.groupName !== targetGroupName) return;

    const newStandings = { ...standings };
    const group = [...newStandings[targetGroupName]];
    const draggedTeam = group[draggedItem.index];
    group.splice(draggedItem.index, 1); 
    group.splice(targetIndex, 0, draggedTeam);
    
    newStandings[targetGroupName] = group;
    setStandings(newStandings);
    setDraggedItem(null);
  };

  const toggleWildcard = (teamName) => {
    if (wildcards.includes(teamName)) {
      setWildcards(wildcards.filter(t => t !== teamName));
    } else {
      if (wildcards.length < 8) {
        setWildcards([...wildcards, teamName]);
      } else {
        alert("와일드카드(3위) 진출팀은 8개까지만 선택할 수 있습니다!");
      }
    }
  };

  const generateRound32 = () => {
    if (!isAssignmentComplete()) return;
    const getTeam = (g, rank) => standings[g][rank - 1]; 

    // 사용자가 직접 확정한 wildcardAssignments 인덱스별 대진 대치
    const matches = [
      { id: 1, label: "매치 1", t1: getTeam('E', 1), t2: wildcardAssignments[0], winner: null }, 
      { id: 2, label: "매치 2", t1: getTeam('I', 1), t2: wildcardAssignments[1], winner: null }, 
      { id: 3, label: "매치 3", t1: getTeam('A', 2), t2: getTeam('B', 2), winner: null }, 
      { id: 4, label: "매치 4", t1: getTeam('F', 1), t2: getTeam('C', 2), winner: null }, 
      { id: 5, label: "매치 5", t1: getTeam('C', 1), t2: getTeam('F', 2), winner: null }, 
      { id: 6, label: "매치 6", t1: getTeam('E', 2), t2: getTeam('I', 2), winner: null }, 
      { id: 7, label: "매치 7", t1: getTeam('A', 1), t2: wildcardAssignments[2], winner: null }, 
      { id: 8, label: "매치 8", t1: getTeam('L', 1), t2: wildcardAssignments[3], winner: null }, 
      { id: 9, label: "매치 9", t1: getTeam('K', 2), t2: getTeam('L', 2), winner: null }, 
      { id: 10, label: "매치 10", t1: getTeam('H', 1), t2: getTeam('J', 2), winner: null }, 
      { id: 11, label: "매치 11", t1: getTeam('D', 1), t2: wildcardAssignments[4], winner: null }, 
      { id: 12, label: "매치 12", t1: getTeam('G', 1), t2: wildcardAssignments[5], winner: null }, 
      { id: 13, label: "매치 13", t1: getTeam('J', 1), t2: getTeam('H', 2), winner: null }, 
      { id: 14, label: "매치 14", t1: getTeam('D', 2), t2: getTeam('G', 2), winner: null }, 
      { id: 15, label: "매치 15", t1: getTeam('B', 1), t2: wildcardAssignments[6], winner: null }, 
      { id: 16, label: "매치 16", t1: getTeam('K', 1), t2: wildcardAssignments[7], winner: null }, 
    ];
    setR32(matches);
    setStep(2); 
  };

  const generateNextRoundMatches = (prevRoundMatches) => {
    const nextRound = [];
    for (let i = 0; i < prevRoundMatches.length; i += 2) {
      nextRound.push({
        id: `M_${prevRoundMatches[i].id}_${prevRoundMatches[i+1].id}`,
        label: `${prevRoundMatches[i].label.split(' ')[1]}·${prevRoundMatches[i+1].label.split(' ')[1]} 승자전`,
        t1: prevRoundMatches[i].winner,
        t2: prevRoundMatches[i+1].winner,
        winner: null
      });
    }
    return nextRound;
  };

  const handleMatchWinner = (currentMatches, setMatches, matchId, winnerTeam) => {
    const newMatches = currentMatches.map(m => m.id === matchId ? { ...m, winner: winnerTeam } : m);
    setMatches(newMatches);
  };

  const handleFinalsWinner = (matchType, winnerTeam) => {
    setFinals({ ...finals, [matchType]: { ...finals[matchType], winner: winnerTeam } });
  };

  const goToNextRound = () => {
    if (step === 2) { setR16(generateNextRoundMatches(r32)); setStep(3); }
    else if (step === 3) { setQf(generateNextRoundMatches(r16)); setStep(4); }
    else if (step === 4) { setSf(generateNextRoundMatches(qf)); setStep(5); }
    else if (step === 5) {
      setFinals({
        final: { id: 'F1', label: '결승전', t1: sf[0].winner, t2: sf[1].winner, winner: null },
        third: { id: 'T1', label: '3위 결정전', t1: sf[0].t1 === sf[0].winner ? sf[0].t2 : sf[0].t1, t2: sf[1].t1 === sf[1].winner ? sf[1].t2 : sf[1].t1, winner: null }
      });
      setStep(6);
    } else if (step === 6) { setStep(7); }
  };

  const resetApp = () => { setStandings(initialGroups); setWildcards([]); setStep(0); };

  const stepsList = ['조별리그', '와일드카드 대진', '32강', '16강', '8강', '4강', '결승', '결과'];

  return (
    <div className="min-h-screen bg-slate-100 font-sans text-gray-800 pb-20">
      <header className="bg-blue-900 text-white p-6 shadow-md text-center">
        <h1 className="text-3xl md:text-4xl font-extrabold flex items-center justify-center gap-3">
          <Trophy size={40} className="text-yellow-300" />
          2026 FIFA 월드컵 시뮬레이터
        </h1>
        <p className="mt-2 text-blue-100 font-medium">공식 피파 대진표 규칙에 맞춰 나만의 대진을 완성하세요!</p>
      </header>

      <div className="max-w-6xl mx-auto px-4 py-6">
        <div className="flex flex-wrap justify-center gap-2 mb-8">
          {stepsList.map((s, idx) => (
            <span key={s} className={`px-3 py-1 rounded-full text-sm font-bold transition-colors ${
              step === idx ? 'bg-blue-600 text-white' : step > idx ? 'bg-green-500 text-white' : 'bg-gray-200 text-gray-500'
            }`}>
              {idx + 1}. {s}
            </span>
          ))}
        </div>

        {/* 1단계: 조별리그 */}
        {step === 0 && (
          <div className="animate-fade-in">
            <div className="text-center mb-6">
              <h2 className="text-2xl font-bold">1단계: 조별 리그 순위 결정</h2>
              <p className="text-gray-600 mt-2 bg-yellow-100 inline-block px-4 py-1 rounded-lg">각 조 안에서 팀을 <strong className="text-black">드래그(Drag)</strong>하여 최종 순위로 나열하세요!</p>
            </div>
            <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-4">
              {Object.keys(standings).map(groupName => (
                <div key={groupName} className="bg-white rounded-xl shadow border-t-4 border-blue-900 overflow-hidden">
                  <div className="bg-black text-white text-center font-bold py-2">GROUP {groupName}</div>
                  <ul className="p-3 space-y-2">
                    {standings[groupName].map((team, idx) => (
                      <li 
                        key={team} 
                        draggable
                        onDragStart={(e) => handleDragStart(e, groupName, idx)}
                        onDragOver={handleDragOver}
                        onDrop={(e) => handleDrop(e, groupName, idx)}
                        onDragEnd={handleDragEnd}
                        className={`flex items-center bg-gray-50 p-2 rounded border border-gray-200 cursor-grab active:cursor-grabbing hover:bg-gray-100 transition-colors ${
                          draggedItem?.groupName === groupName && draggedItem?.index === idx ? 'opacity-40 border-dashed border-blue-500' : ''
                        }`}
                      >
                        <span className={`font-bold w-6 h-6 flex items-center justify-center rounded text-sm shrink-0 ${idx < 2 ? 'bg-blue-100 text-blue-700' : idx === 2 ? 'bg-green-100 text-green-700' : 'bg-gray-200 text-gray-500'}`}>
                          {idx + 1}
                        </span>
                        <div className="flex-1 ml-3 pointer-events-none flex items-center h-full overflow-hidden">
                          {renderTeam(team, false, 'start')}
                        </div>
                      </li>
                    ))}
                  </ul>
                </div>
              ))}
            </div>
            <div className="text-center mt-8">
              <button onClick={() => setStep(1)} className="bg-blue-600 hover:bg-blue-700 text-white px-8 py-3 rounded-full font-bold text-lg inline-flex items-center gap-2 shadow-lg transition-transform hover:scale-105">
                순위 확정하고 다음으로 <ArrowRight size={20} />
              </button>
            </div>
          </div>
        )}

        {/* 2단계: 와일드카드 선택 및 대진 직접 배치 */}
        {step === 1 && (
          <div className="animate-fade-in max-w-6xl mx-auto space-y-12">
            
            {/* A. 와일드카드 진출국 8개 선정 */}
            <div className="bg-white p-6 rounded-2xl shadow border border-gray-200">
              <div className="text-center mb-6">
                <h2 className="text-2xl font-bold">2단계 (A): 와일드카드 (3위 진출팀) 선택</h2>
                <p className="text-gray-600">조 3위를 기록한 12개 국가 중 성적이 가장 좋은 8개 국가를 선택하세요.</p>
                
                <div className="mt-4 inline-block bg-blue-100 text-blue-800 px-6 py-2 rounded-full font-extrabold text-xl">
                  선택된 팀: {wildcards.length} / 8
                </div>
              </div>
              
              <div className="grid grid-cols-2 md:grid-cols-4 lg:grid-cols-6 gap-4">
                {Object.keys(standings).map(g => {
                  const team3rd = standings[g][2];
                  const isSelected = wildcards.includes(team3rd);
                  return (
                    <button
                      key={g}
                      onClick={() => toggleWildcard(team3rd)}
                      className={`p-2 sm:p-3 rounded-xl font-bold border-2 transition-all shadow-sm flex flex-col items-center justify-center gap-1.5 w-full overflow-hidden ${
                        isSelected ? 'bg-green-500 border-green-600 text-white scale-105' : 'bg-white border-gray-200 text-gray-700 hover:border-green-300'
                      }`}
                    >
                      <div className={`text-[10px] sm:text-[11px] font-normal px-2 py-0.5 rounded-full whitespace-nowrap shrink-0 ${isSelected ? 'bg-green-600' : 'bg-gray-100'}`}>{g}조 3위</div>
                      <div className="w-full flex justify-center items-center">
                        {renderTeam(team3rd, false, 'center')}
                      </div>
                    </button>
                  )
                })}
              </div>
            </div>

            {/* B. 와일드카드 대진 배치 (8개 팀 선정 시에만 공개) */}
            {wildcards.length === 8 && (
              <div className="bg-white p-6 rounded-2xl shadow border border-gray-200 space-y-6">
                <div className="text-center max-w-2xl mx-auto space-y-2">
                  <h2 className="text-2xl font-bold text-blue-900">2단계 (B): 와일드카드 32강 상대 대진 직접 지정</h2>
                  <p className="text-gray-600 text-sm">
                    각 대진 매치에 어울릴 상대를 골라주세요. <br />
                    각 슬롯마다 피파 공식 규칙에 맞는 <strong className="text-blue-600">허용된 조의 3위 팀</strong>들만 선택할 수 있습니다.
                  </p>
                  
                  <div className="pt-2">
                    <button 
                      onClick={autoAssign} 
                      className="inline-flex items-center gap-2 bg-purple-600 hover:bg-purple-700 text-white text-sm font-bold px-5 py-2.5 rounded-lg shadow transition"
                    >
                      <Shuffle size={16} /> 자동으로 대진 추천 배치하기
                    </button>
                  </div>
                </div>

                <div className="grid grid-cols-1 md:grid-cols-2 gap-6">
                  {wildcardSlots.map((slot) => {
                    const eligibleSelectedTeams = wildcards.filter(team => isTeamEligibleForSlot(team, slot.idx));
                    const assignedTeam = wildcardAssignments[slot.idx];

                    return (
                      <div key={slot.idx} className={`p-4 rounded-xl border-2 transition ${assignedTeam ? 'border-blue-200 bg-blue-50/40' : 'border-dashed border-gray-300'}`}>
                        <div className="flex justify-between items-start mb-3">
                          <div>
                            <span className="text-xs font-bold text-gray-400 block">SLOT {slot.idx + 1}</span>
                            <h4 className="font-bold text-gray-800 text-base">{slot.label}</h4>
                          </div>
                          <span className="text-[10px] bg-gray-200 px-2 py-0.5 rounded text-gray-600 font-semibold uppercase">
                            허용 조: {slot.allowed.join(', ')}
                          </span>
                        </div>

                        {/* 매칭 대상국가 버튼들 */}
                        <div className="flex flex-wrap gap-2 mb-3">
                          {eligibleSelectedTeams.length > 0 ? (
                            eligibleSelectedTeams.map((team) => {
                              const isThisAssigned = assignedTeam === team;
                              const isAssignedElsewhere = wildcardAssignments.includes(team) && !isThisAssigned;

                              return (
                                <button
                                  key={team}
                                  onClick={() => assignTeamToSlot(team, slot.idx)}
                                  className={`px-3 py-1.5 rounded-lg text-xs font-bold border flex items-center gap-1.5 transition ${
                                    isThisAssigned
                                      ? 'bg-blue-600 border-blue-700 text-white shadow-sm'
                                      : isAssignedElsewhere
                                      ? 'bg-gray-100 border-gray-200 text-gray-400 opacity-60 hover:bg-gray-200'
                                      : 'bg-white border-gray-300 hover:border-blue-500 text-gray-700'
                                  }`}
                                >
                                  {team} ({getTeamGroup(team)}조)
                                  {isAssignedElsewhere && <span className="text-[9px] font-normal text-gray-500">(이동)</span>}
                                </button>
                              );
                            })
                          ) : (
                            <span className="text-xs text-red-500 font-semibold flex items-center gap-1 py-1">
                              <AlertTriangle size={14} /> 현재 선택하신 3위 국가들 중에 이 자리에 배치 가능한 국가가 없습니다.
                            </span>
                          )}
                        </div>

                        {/* 현재 배치 상태 메시지 */}
                        <div className="text-sm font-bold flex items-center gap-2 bg-white p-2 rounded border border-gray-200 justify-between w-full overflow-hidden">
                          <span className="text-xs text-gray-500 shrink-0">배치된 대진 상대:</span>
                          {assignedTeam ? (
                            <div className="flex items-center gap-2 text-blue-700 w-full overflow-hidden">
                              {renderTeam(assignedTeam, false, 'start')}
                            </div>
                          ) : (
                            <span className="text-xs text-amber-500 italic font-medium flex items-center gap-1">
                              <HelpCircle size={14} /> 미지정 (후보군 선택)
                            </span>
                          )}
                        </div>
                      </div>
                    );
                  })}
                </div>
              </div>
            )}

            {/* 이전/다음 단계 컨트롤 버튼 */}
            <div className="text-center mt-8 flex flex-wrap justify-center gap-4">
              <button onClick={() => setStep(0)} className="bg-gray-400 hover:bg-gray-500 text-white px-6 py-3 rounded-full font-bold transition-transform hover:scale-105">
                이전 단계로
              </button>
              <button 
                onClick={generateRound32} 
                disabled={!isAssignmentComplete()}
                className="bg-blue-600 hover:bg-blue-700 disabled:bg-blue-300 text-white px-8 py-3 rounded-full font-bold text-lg inline-flex items-center gap-2 shadow-lg transition-transform hover:scale-105"
              >
                32강 공식 대진 확정 <ArrowRight size={20} />
              </button>
            </div>
          </div>
        )}

        {/* 3단계 ~ 6단계: 토너먼트 매치 진행 */}
        {step >= 2 && step <= 5 && (() => {
          const roundData = step === 2 ? r32 : step === 3 ? r16 : step === 4 ? qf : sf;
          const setRoundData = step === 2 ? setR32 : step === 3 ? setR16 : step === 4 ? setQf : setSf;
          const roundName = step === 2 ? "32강전" : step === 3 ? "16강전" : step === 4 ? "8강전" : "4강전";
          const allMatchesDone = roundData.every(m => m.winner !== null);

          return (
            <div className="animate-fade-in max-w-4xl mx-auto">
               <div className="text-center mb-8">
                <h2 className="text-3xl font-extrabold text-blue-900">{roundName}</h2>
                <p className="text-gray-600 mt-2">다음 라운드로 진출시킬 승리 팀을 탭(클릭)하세요!</p>
              </div>

              <div className="grid grid-cols-1 md:grid-cols-2 gap-4">
                {roundData.map((m) => (
                  <div key={m.id} className="flex flex-col bg-white rounded-xl shadow-md overflow-hidden border border-gray-200">
                    <div className="bg-gray-100 px-4 py-1 text-xs font-bold text-gray-500 border-b border-gray-200 flex justify-between">
                      <span>{m.label}</span>
                      {m.winner && <span className="text-blue-600">진출 확정</span>}
                    </div>
                    <div className="flex items-stretch justify-between h-full">
                      <button
                        className={`flex-1 flex flex-col items-center justify-center p-3 sm:p-4 w-full overflow-hidden text-sm sm:text-base font-bold transition-colors ${
                          m.winner === m.t1 ? 'bg-blue-600 text-white' : 'bg-white hover:bg-gray-50 text-gray-800'
                        }`}
                        onClick={() => handleMatchWinner(roundData, setRoundData, m.id, m.t1)}
                      >
                        {renderTeam(m.t1, true, 'center')}
                      </button>
                      
                      <div className="w-8 sm:w-10 flex items-center justify-center bg-gray-50 border-x border-gray-100 font-black text-gray-300 italic text-xs shrink-0">VS</div>
                      
                      <button
                        className={`flex-1 flex flex-col items-center justify-center p-3 sm:p-4 w-full overflow-hidden text-sm sm:text-base font-bold transition-colors ${
                          m.winner === m.t2 ? 'bg-red-600 text-white' : 'bg-white hover:bg-gray-50 text-gray-800'
                        }`}
                        onClick={() => handleMatchWinner(roundData, setRoundData, m.id, m.t2)}
                      >
                        {renderTeam(m.t2, true, 'center')}
                      </button>
                    </div>
                  </div>
                ))}
              </div>

              <div className="text-center mt-10 flex flex-wrap justify-center gap-4">
                <button 
                  onClick={() => setStep(step - 1)} 
                  className="bg-gray-400 hover:bg-gray-500 text-white px-6 py-4 rounded-full font-bold text-lg shadow-md transition-transform hover:scale-105"
                >
                  이전 단계로
                </button>
                <button 
                  onClick={goToNextRound} 
                  disabled={!allMatchesDone}
                  className="bg-yellow-500 hover:bg-yellow-600 disabled:bg-gray-300 text-white px-8 py-4 rounded-full font-extrabold text-xl inline-flex items-center gap-2 shadow-lg transition-transform hover:scale-105"
                >
                  {allMatchesDone ? "다음 라운드 진행" : "모든 매치의 승자를 골라주세요"} <ArrowRight size={24} />
                </button>
              </div>
            </div>
          );
        })()}

        {/* 7단계: 결승 및 3위 결정전 */}
        {step === 6 && (
           <div className="animate-fade-in max-w-3xl mx-auto">
             <div className="text-center mb-10">
              <h2 className="text-4xl font-extrabold text-yellow-600 flex justify-center gap-2"><Trophy/> 대망의 결승전 <Trophy/></h2>
            </div>

            <div className="bg-yellow-50 p-4 sm:p-6 rounded-2xl shadow-xl border-2 border-yellow-400 mb-8">
              <h3 className="text-center font-bold text-xl mb-4 text-yellow-800">우승팀 결정</h3>
              <div className="flex items-stretch justify-between bg-white rounded-xl shadow overflow-hidden">
                <button className={`flex-1 flex flex-col items-center justify-center p-3 sm:p-6 w-full overflow-hidden text-base sm:text-xl font-bold transition ${finals.final.winner === finals.final.t1 ? 'bg-yellow-500 text-white' : 'bg-white hover:bg-gray-50'}`} onClick={() => handleFinalsWinner('final', finals.final.t1)}>
                  {renderTeam(finals.final.t1, true, 'center')}
                </button>
                <div className="w-10 sm:w-12 flex items-center justify-center bg-gray-50 border-x font-black text-gray-300 text-xs sm:text-sm shrink-0">VS</div>
                <button className={`flex-1 flex flex-col items-center justify-center p-3 sm:p-6 w-full overflow-hidden text-base sm:text-xl font-bold transition ${finals.final.winner === finals.final.t2 ? 'bg-yellow-500 text-white' : 'bg-white hover:bg-gray-50'}`} onClick={() => handleFinalsWinner('final', finals.final.t2)}>
                  {renderTeam(finals.final.t2, true, 'center')}
                </button>
              </div>
            </div>

            <div className="bg-gray-100 p-4 sm:p-6 rounded-2xl shadow-md border border-gray-300">
              <h3 className="text-center font-bold text-lg mb-4 text-gray-600">3위 결정전</h3>
              <div className="flex items-stretch justify-between bg-white rounded-xl shadow overflow-hidden">
                <button className={`flex-1 flex flex-col items-center justify-center p-3 sm:p-4 w-full overflow-hidden text-base sm:text-lg font-bold transition ${finals.third.winner === finals.third.t1 ? 'bg-gray-500 text-white' : 'bg-white hover:bg-gray-50'}`} onClick={() => handleFinalsWinner('third', finals.third.t1)}>
                  {renderTeam(finals.third.t1, true, 'center')}
                </button>
                <div className="w-10 sm:w-12 flex items-center justify-center bg-gray-50 border-x font-black text-gray-300 text-xs sm:text-sm shrink-0">VS</div>
                <button className={`flex-1 flex flex-col items-center justify-center p-3 sm:p-4 w-full overflow-hidden text-base sm:text-lg font-bold transition ${finals.third.winner === finals.third.t2 ? 'bg-gray-500 text-white' : 'bg-white hover:bg-gray-50'}`} onClick={() => handleFinalsWinner('third', finals.third.t2)}>
                  {renderTeam(finals.third.t2, true, 'center')}
                </button>
              </div>
            </div>

            <div className="text-center mt-10 flex flex-wrap justify-center gap-4">
                <button onClick={() => setStep(5)} className="bg-gray-400 hover:bg-gray-500 text-white px-8 py-4 rounded-full font-bold text-xl shadow-md transition-transform hover:scale-105">
                  이전 단계로
                </button>
                <button onClick={goToNextRound} disabled={!finals.final.winner || !finals.third.winner} className="bg-blue-600 hover:bg-blue-700 disabled:bg-gray-300 text-white px-10 py-4 rounded-full font-extrabold text-2xl shadow-xl transition-transform hover:scale-110">
                  최종 결과 확인하기
                </button>
              </div>
           </div>
        )}

        {/* 8단계: 최종 결과 발표 */}
        {step === 7 && (() => {
          const firstPlace = finals.final.winner;
          const secondPlace = finals.final.t1 === firstPlace ? finals.final.t2 : finals.final.t1;
          const thirdPlace = finals.third.winner;
          const fourthPlace = finals.third.t1 === thirdPlace ? finals.third.t2 : finals.third.t1;

          return (
            <div className="animate-fade-in max-w-4xl mx-auto text-center">
              <h2 className="text-4xl font-black mb-12 text-blue-900">🎉 2026 월드컵 최종 예측 결과 🎉</h2>
              
              <div className="flex flex-col md:flex-row justify-center items-end gap-4 md:gap-8 mb-16 h-64 mt-20">
                <div className="w-full md:w-1/3 flex flex-col items-center order-2 md:order-1 overflow-hidden">
                  <div className="text-xl md:text-2xl font-bold mb-2 w-full">{renderTeam(secondPlace, false, 'center')}</div>
                  <div className="w-full bg-gray-300 h-32 rounded-t-xl flex justify-center pt-4 shadow-inner">
                    <Medal className="text-gray-500" size={40} />
                  </div>
                  <div className="bg-gray-400 text-white w-full py-1 font-bold">2위</div>
                </div>
                
                <div className="w-full md:w-1/3 flex flex-col items-center order-1 md:order-2 z-10 -mt-10 overflow-hidden">
                  <Trophy className="text-yellow-500 mb-2 animate-bounce" size={60} />
                  <div className="text-2xl md:text-3xl font-black text-red-600 mb-2 w-full">{renderTeam(firstPlace, false, 'center')}</div>
                  <div className="w-full bg-yellow-400 h-48 rounded-t-xl flex justify-center pt-4 shadow-2xl">
                    <span className="text-yellow-700 font-black text-2xl">WINNER</span>
                  </div>
                  <div className="bg-yellow-600 text-white w-full py-2 font-black text-xl">1위 (우승)</div>
                </div>

                <div className="w-full md:w-1/3 flex flex-col items-center order-3 md:order-3 overflow-hidden">
                  <div className="text-lg md:text-xl font-bold mb-2 w-full">{renderTeam(thirdPlace, false, 'center')}</div>
                  <div className="w-full bg-orange-300 h-24 rounded-t-xl flex justify-center pt-2 shadow-inner">
                    <Medal className="text-orange-700" size={30} />
                  </div>
                  <div className="bg-orange-500 text-white w-full py-1 font-bold">3위</div>
                </div>
              </div>

              <div className="bg-white p-4 rounded-xl shadow flex flex-wrap justify-center items-center gap-2 border text-lg mt-8 mx-auto w-full max-w-sm overflow-hidden">
                <span className="font-bold text-gray-500 shrink-0">4위</span>
                <div className="flex-1">{renderTeam(fourthPlace, false, 'start')}</div>
              </div>

              <div className="mt-16 flex flex-wrap justify-center gap-4">
                <button onClick={() => setStep(6)} className="bg-gray-400 hover:bg-gray-500 text-white px-6 py-3 rounded-full font-bold inline-flex items-center gap-2 transition-transform hover:scale-105">
                  이전 단계로
                </button>
                <button onClick={resetApp} className="bg-gray-800 hover:bg-black text-white px-6 py-3 rounded-full font-bold inline-flex items-center gap-2 transition-transform hover:scale-105">
                  <RotateCcw size={20} /> 처음부터 다시 예측하기
                </button>
              </div>
            </div>
          );
        })()}
      </div>
    </div>
  );
}
