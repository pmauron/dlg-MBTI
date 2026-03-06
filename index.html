import { useState, useEffect, useRef } from "react";

// ─── QUESTIONS ───────────────────────────────────────────────────────────────

const mbtiQuestions = [
  // E/I — 7 questions
  { id: "m1", dim: "EI", a: { en: "After a full day of meetings, I recharge by going to dinner with interesting people.", cn: "开完一整天的会后，我更愿意和有趣的人一起吃晚饭来恢复精力。", s: "E" }, b: { en: "After a full day of meetings, I recharge by having the evening completely to myself.", cn: "开完一整天的会后，我更愿意独自度过晚上来恢复精力。", s: "I" } },
  { id: "m2", dim: "EI", a: { en: "I develop my best ideas by talking them through with someone, even if I'm clearly leading.", cn: "我最好的想法是在和别人讨论中产生的，即使我在主导对话。", s: "E" }, b: { en: "I develop my best ideas alone first, then present them to others mostly formed.", cn: "我最好的想法是先独自思考，形成后再告诉别人。", s: "I" } },
  { id: "m3", dim: "EI", a: { en: "At a conference, I seek out conversations with strangers for unexpected value.", cn: "在会议上，我会主动和陌生人交流，寻找意想不到的收获。", s: "E" }, b: { en: "At a conference, I target specific people I've identified in advance.", cn: "在会议上，我会提前锁定目标，只和特定的人交流。", s: "I" } },
  { id: "m4", dim: "EI", a: { en: "When solving a complex problem, I naturally pull others in early to stress-test my thinking.", cn: "解决复杂问题时，我倾向于尽早让他人参与来检验我的想法。", s: "E" }, b: { en: "When solving a complex problem, I work it to near-completion before exposing it.", cn: "解决复杂问题时，我倾向于先独自完成大部分再让他人看到。", s: "I" } },
  { id: "m5", dim: "EI", a: { en: "A great weekend involves substantial time around other people.", cn: "美好的周末意味着花大量时间和他人在一起。", s: "E" }, b: { en: "A great weekend has significant blocks of solitary time.", cn: "美好的周末意味着拥有大段独处的时间。", s: "I" } },
  { id: "m6", dim: "EI", a: { en: "I find prolonged periods of working alone draining, even if the work is interesting.", cn: "即使工作有趣，长时间独自工作也会让我感到疲惫。", s: "E" }, b: { en: "I find prolonged periods of working alone energizing, as long as the work is interesting.", cn: "只要工作有趣，长时间独自工作反而让我充满活力。", s: "I" } },
  { id: "m7", dim: "EI", a: { en: "In a new city, I explore by engaging with locals and striking up conversations.", cn: "到一个新城市，我会通过和当地人交流来探索。", s: "E" }, b: { en: "In a new city, I explore by walking and observing on my own, researching in advance.", cn: "到一个新城市，我会提前做功课，然后独自步行观察来探索。", s: "I" } },
  // N/S — 4 questions
  { id: "m8", dim: "NS", a: { en: "When evaluating an opportunity, I first think about the structural position it creates.", cn: "评估机会时，我首先考虑它能创造的战略定位。", s: "N" }, b: { en: "When evaluating an opportunity, I first look at the current numbers and concrete evidence.", cn: "评估机会时，我首先看当前的数据和具体证据。", s: "S" } },
  { id: "m9", dim: "NS", a: { en: "I get more frustrated by teams that can't see the bigger picture.", cn: "团队看不到大局更让我沮丧。", s: "N" }, b: { en: "I get more frustrated by teams that miss critical details.", cn: "团队忽略关键细节更让我沮丧。", s: "S" } },
  { id: "m10", dim: "NS", a: { en: "I'd rather build something new from scratch than optimize something that already works.", cn: "我宁愿从零开始创造新东西，也不愿优化已有的。", s: "N" }, b: { en: "I'd rather perfect and scale something proven than start from zero.", cn: "我宁愿完善和扩展已验证的东西，也不愿从零开始。", s: "S" } },
  { id: "m11", dim: "NS", a: { en: "When I read an industry report, I'm drawn to implications and what's not being said.", cn: "读行业报告时，我更关注言外之意和潜在影响。", s: "N" }, b: { en: "When I read an industry report, I'm drawn to specific data points and methodology.", cn: "读行业报告时，我更关注具体数据和研究方法。", s: "S" } },
  // T/F — 4 questions
  { id: "m12", dim: "TF", a: { en: "When letting someone go, the hardest part is managing the operational disruption.", cn: "辞退员工时，最难的是处理对运营的影响。", s: "T" }, b: { en: "When letting someone go, the hardest part is the personal impact on them and the team.", cn: "辞退员工时，最难的是对当事人和团队的情感影响。", s: "F" } },
  { id: "m13", dim: "TF", a: { en: "I respect leaders who make tough calls quickly, even if people don't like it.", cn: "我尊重能快速做出艰难决定的领导，即使不受欢迎。", s: "T" }, b: { en: "I respect leaders who take time to bring people along, even if it's slower.", cn: "我尊重愿意花时间让大家达成共识的领导，即使效率较低。", s: "F" } },
  { id: "m14", dim: "TF", a: { en: "When giving feedback, I prioritize being accurate and direct over being diplomatic.", cn: "给反馈时，我更注重准确和直接，而非委婉。", s: "T" }, b: { en: "When giving feedback, I consider how the person will receive it before framing it.", cn: "给反馈时，我会先考虑对方的感受再决定如何表达。", s: "F" } },
  { id: "m15", dim: "TF", a: { en: "A decision is good if the logic and outcomes are sound, regardless of how people feel about the process.", cn: "只要逻辑和结果合理，决策就是好的，不管人们对过程的感受如何。", s: "T" }, b: { en: "A decision is only good if the people affected can understand and accept the reasoning.", cn: "只有当受影响的人能理解和接受其理由时，决策才是好的。", s: "F" } },
  // J/P — 5 questions
  { id: "m16", dim: "JP", a: { en: "I prefer to decide quickly and correct course later than to keep gathering information.", cn: "我更喜欢快速决定然后调整，而非持续收集信息。", s: "J" }, b: { en: "I prefer to stay flexible and keep options open until I have enough information.", cn: "我更喜欢保持灵活，在信息充分前保留选项。", s: "P" } },
  { id: "m17", dim: "JP", a: { en: "Ambiguity in roles and timelines bothers me — I want things defined.", cn: "角色和时间线的模糊让我困扰——我希望一切都明确。", s: "J" }, b: { en: "Ambiguity in roles and timelines doesn't bother me — I adapt as things unfold.", cn: "角色和时间线的模糊不会困扰我——我会随机应变。", s: "P" } },
  { id: "m18", dim: "JP", a: { en: "When a plan changes last minute, my first reaction is frustration.", cn: "计划临时变动时，我的第一反应是沮丧。", s: "J" }, b: { en: "When a plan changes last minute, I assess the new situation for opportunities.", cn: "计划临时变动时，我会评估新情况中的机会。", s: "P" } },
  { id: "m19", dim: "JP", a: { en: "I'd rather have a structured itinerary for a trip, even if I deviate from it.", cn: "旅行时我更喜欢有结构化的行程，即使可能偏离。", s: "J" }, b: { en: "I'd rather arrive with no plan and figure it out based on how I feel.", cn: "旅行时我更喜欢没有计划，随心所欲地探索。", s: "P" } },
  { id: "m20", dim: "JP", a: { en: "Starting a new project, I instinctively create structure first — timelines, owners, milestones.", cn: "启动新项目时，我本能地先建立结构——时间线、负责人、里程碑。", s: "J" }, b: { en: "Starting a new project, I instinctively start doing things and let structure emerge.", cn: "启动新项目时，我本能地先行动，让结构自然形成。", s: "P" } },
];

// PULSIONS: forced-choice pairs between competing drivers
// Each question pits two drivers against each other
const pulsionsQuestions = [
  // Performance vs Social
  { id: "p1", a: { en: "I'd rather exceed my targets working independently than hit them as part of a close-knit team.", cn: "我宁愿独立超额完成目标，也不愿作为紧密团队的一员达成目标。", s: "P" }, b: { en: "I'd rather hit my targets as part of a close-knit team than exceed them working alone.", cn: "我宁愿作为紧密团队的一员达成目标，也不愿独立超额完成。", s: "So" } },
  // Liberté vs Sécurité
  { id: "p2", a: { en: "I'd take a role with full autonomy and uncertain income over a stable role with rigid structure.", cn: "我宁愿选择完全自主但收入不确定的职位，也不选稳定但僵化的职位。", s: "L" }, b: { en: "I'd take a stable role with rigid structure over one with full autonomy and uncertain income.", cn: "我宁愿选择稳定但僵化的职位，也不选完全自主但收入不确定的职位。", s: "Se" } },
  // Utilité vs Orgueil
  { id: "p3", a: { en: "I'd rather solve a critical problem that nobody knows I solved.", cn: "我宁愿解决一个关键问题但无人知晓。", s: "U" }, b: { en: "I'd rather be recognized for a visible contribution, even if it wasn't the most critical.", cn: "我宁愿因一个显眼的贡献获得认可，即使它不是最关键的。", s: "O" } },
  // Intérêt vs Performance
  { id: "p4", a: { en: "I'd rather work on a fascinating project with unclear ROI than a routine project with guaranteed results.", cn: "我宁愿做一个ROI不明确但引人入胜的项目，也不做有保证结果但常规的项目。", s: "I" }, b: { en: "I'd rather deliver guaranteed results on a routine project than explore something fascinating with unclear ROI.", cn: "我宁愿在常规项目上交付确定的成果，也不去探索ROI不明确的项目。", s: "P" } },
  // Social vs Liberté
  { id: "p5", a: { en: "I'd rather work in a collaborative environment with less personal freedom.", cn: "我宁愿在协作环境中工作，即使个人自由较少。", s: "So" }, b: { en: "I'd rather work independently with full freedom, even if it means less team connection.", cn: "我宁愿拥有完全的自由独立工作，即使团队联系较少。", s: "L" } },
  // Orgueil vs Sécurité
  { id: "p6", a: { en: "I'd take a high-profile role with significant risk over a secure role with no visibility.", cn: "我宁愿承担高曝光但风险大的角色，也不选安全但无人关注的角色。", s: "O" }, b: { en: "I'd take a secure role with no visibility over a high-profile role with significant risk.", cn: "我宁愿选择安全但无人关注的角色，也不承担高曝光但风险大的角色。", s: "Se" } },
  // Performance vs Liberté
  { id: "p7", a: { en: "I'd accept strict processes if they guarantee top performance.", cn: "如果严格的流程能保证顶级绩效，我愿意接受。", s: "P" }, b: { en: "I'd sacrifice some performance metrics to maintain my autonomy.", cn: "为了保持自主权，我愿意牺牲一些绩效指标。", s: "L" } },
  // Utilité vs Social
  { id: "p8", a: { en: "I'd rather be the person who fixes what's broken than the person everyone likes working with.", cn: "我宁愿做那个解决问题的人，而非人人都喜欢合作的人。", s: "U" }, b: { en: "I'd rather be the person everyone likes working with than the person who fixes what's broken.", cn: "我宁愿做人人都喜欢合作的人，而非那个解决问题的人。", s: "So" } },
  // Intérêt vs Sécurité
  { id: "p9", a: { en: "I'd move to an unfamiliar industry if the intellectual challenge excited me.", cn: "如果智力挑战吸引我，我愿意转行到陌生的行业。", s: "I" }, b: { en: "I'd stay in my current industry where I have deep expertise and stability.", cn: "我更愿意留在我有深厚专业知识和稳定性的行业。", s: "Se" } },
  // Orgueil vs Performance
  { id: "p10", a: { en: "I'd rather be publicly credited for the win than quietly outperform everyone.", cn: "我宁愿公开获得荣誉，也不愿默默超越所有人。", s: "O" }, b: { en: "I'd rather quietly outperform everyone than be publicly credited.", cn: "我宁愿默默超越所有人，也不在乎公开获得荣誉。", s: "P" } },
  // Liberté vs Utilité
  { id: "p11", a: { en: "I'd rather choose my own projects freely than be assigned to where I'm most needed.", cn: "我宁愿自由选择项目，也不愿被分配到最需要我的地方。", s: "L" }, b: { en: "I'd rather be assigned to where I'm most needed than choose freely.", cn: "我宁愿被分配到最需要我的地方，也不自由选择项目。", s: "U" } },
  // Social vs Intérêt
  { id: "p12", a: { en: "I'd choose a role with a great team over one with the most intellectually stimulating work.", cn: "我更看重优秀的团队，而非最具智力刺激的工作。", s: "So" }, b: { en: "I'd choose the most intellectually stimulating work over a role with a great team.", cn: "我更看重最具智力刺激的工作，而非优秀的团队。", s: "I" } },
  // Sécurité vs Utilité
  { id: "p13", a: { en: "I'd prioritize job security over taking on a critical but risky assignment.", cn: "我会优先考虑工作稳定性，而非承担关键但有风险的任务。", s: "Se" }, b: { en: "I'd take on a critical but risky assignment over prioritizing job security.", cn: "我更愿意承担关键但有风险的任务，而非优先考虑工作稳定性。", s: "U" } },
  // Orgueil vs Intérêt
  { id: "p14", a: { en: "I'd rather lead a high-visibility project than work on the most intellectually challenging one.", cn: "我宁愿领导一个高曝光的项目，也不做最具智力挑战的项目。", s: "O" }, b: { en: "I'd rather work on the most intellectually challenging project than lead a visible one.", cn: "我宁愿做最具智力挑战的项目，也不领导高曝光的项目。", s: "I" } },
  // Performance vs Sécurité
  { id: "p15", a: { en: "I'd risk failure to pursue an ambitious target over settling for a safe, achievable one.", cn: "我宁愿冒着失败的风险追求宏大目标，也不满足于安全可实现的目标。", s: "P" }, b: { en: "I'd settle for a safe, achievable target over risking failure on an ambitious one.", cn: "我宁愿选择安全可实现的目标，也不冒着失败的风险追求宏大目标。", s: "Se" } },
  // Liberté vs Orgueil
  { id: "p16", a: { en: "I'd rather work behind the scenes with full autonomy than be a recognized leader with constraints.", cn: "我宁愿在幕后拥有完全自主权，也不做受限制的知名领导。", s: "L" }, b: { en: "I'd rather be a recognized leader with constraints than work behind the scenes with full autonomy.", cn: "我宁愿做受限制的知名领导，也不在幕后拥有完全自主权。", s: "O" } },
  // Utilité vs Performance
  { id: "p17", a: { en: "I'd rather make a meaningful impact on one project than hit targets across many.", cn: "我宁愿在一个项目上产生有意义的影响，也不在许多项目上达成指标。", s: "U" }, b: { en: "I'd rather consistently hit targets across many projects than deeply impact one.", cn: "我宁愿在多个项目上持续达成指标，也不在一个项目上深入影响。", s: "P" } },
  // Social vs Sécurité
  { id: "p18", a: { en: "I'd leave a stable role if the team culture was toxic.", cn: "如果团队文化有害，我会离开一个稳定的职位。", s: "So" }, b: { en: "I'd stay in a toxic team culture if the role provided strong stability.", cn: "如果职位稳定性强，我会留在有害的团队文化中。", s: "Se" } },
  // Intérêt vs Liberté
  { id: "p19", a: { en: "I'd accept structured constraints if the work was intellectually fascinating.", cn: "如果工作在智力上引人入胜，我愿意接受结构化的约束。", s: "I" }, b: { en: "I'd choose freedom over fascinating work if the structure felt suffocating.", cn: "如果结构让人窒息，我会选择自由而非迷人的工作。", s: "L" } },
  // Utilité vs Intérêt
  { id: "p20", a: { en: "I'd rather solve urgent practical problems than explore interesting theoretical ones.", cn: "我宁愿解决紧迫的实际问题，也不探索有趣的理论问题。", s: "U" }, b: { en: "I'd rather explore interesting theoretical problems than solve urgent practical ones.", cn: "我宁愿探索有趣的理论问题，也不解决紧迫的实际问题。", s: "I" } },
  // Social vs Orgueil
  { id: "p21", a: { en: "I'd rather share credit with the team than receive individual recognition.", cn: "我宁愿与团队分享荣誉，也不接受个人认可。", s: "So" }, b: { en: "I'd rather receive individual recognition than share credit.", cn: "我宁愿接受个人认可，也不与团队分享荣誉。", s: "O" } },
  // Performance vs Utilité
  { id: "p22", a: { en: "I'm more motivated by beating benchmarks than by knowing my work matters to someone.", cn: "超越基准比知道我的工作对某人很重要更能激励我。", s: "P" }, b: { en: "I'm more motivated by knowing my work matters to someone than by beating benchmarks.", cn: "知道我的工作对某人很重要比超越基准更能激励我。", s: "U" } },
  // Liberté vs Social
  { id: "p23", a: { en: "I'd rather set my own schedule and work remotely than be in the office with the team daily.", cn: "我宁愿自定日程远程工作，也不每天和团队在办公室。", s: "L" }, b: { en: "I'd rather be in the office with the team daily than set my own schedule remotely.", cn: "我宁愿每天和团队在办公室，也不自定日程远程工作。", s: "So" } },
  // Orgueil vs Utilité
  { id: "p24", a: { en: "I'd rather present the results to leadership than be the one who did the actual work.", cn: "我宁愿向领导层展示成果，也不做实际工作。", s: "O" }, b: { en: "I'd rather do the actual work than present the results to leadership.", cn: "我宁愿做实际工作，也不向领导层展示成果。", s: "U" } },
  // Intérêt vs Orgueil
  { id: "p25", a: { en: "I'd rather master a complex skill nobody cares about than be praised for a simple one.", cn: "我宁愿掌握一项无人在意的复杂技能，也不因简单技能获得称赞。", s: "I" }, b: { en: "I'd rather be praised for a simple skill than master a complex one nobody cares about.", cn: "我宁愿因简单技能获得称赞，也不掌握无人在意的复杂技能。", s: "O" } },
];

// Pulsion code to full label
const pulsionLabels = {
  P: { en: "Performance", cn: "绩效" },
  U: { en: "Utilité", cn: "实用" },
  L: { en: "Liberté", cn: "自由" },
  So: { en: "Social", cn: "社交" },
  I: { en: "Intérêt", cn: "兴趣" },
  O: { en: "Orgueil", cn: "荣誉" },
  Se: { en: "Sécurité", cn: "安全" },
};
const pulsionColors = { P: "#E50B67", U: "#0EA5E9", L: "#F59E0B", So: "#10B981", I: "#8B5CF6", O: "#EF4444", Se: "#6B7280" };
const pulsionOrder = ["P", "U", "L", "So", "I", "O", "Se"];

const dimLabels = { EI: ["E", "I"], NS: ["N", "S"], TF: ["T", "F"], JP: ["J", "P"] };
const dimColors = { EI: "#EA580C", NS: "#16A34A", TF: "#0EA5E9", JP: "#9333EA" };
const dimNames = {
  EI: { en: ["Extraversion", "Introversion"], cn: ["外向", "内向"] },
  NS: { en: ["Intuition", "Sensing"], cn: ["直觉", "感觉"] },
  TF: { en: ["Thinking", "Feeling"], cn: ["思维", "情感"] },
  JP: { en: ["Judging", "Perceiving"], cn: ["判断", "感知"] },
};

const shuffleSeed = 42;
const shouldFlip = (id) => {
  let h = 0;
  for (let i = 0; i < id.length; i++) h = ((h << 5) - h + id.charCodeAt(i)) | 0;
  return (Math.abs(h) % 7) > 3;
};

const t = (lang, en, cn) => lang === "cn" ? cn : en;

// ─── RADAR CHART ─────────────────────────────────────────────────────────────

function RadarChart({ scores, lang }) {
  const cx = 160, cy = 160, r = 120;
  const n = pulsionOrder.length;
  const maxScore = Math.max(...pulsionOrder.map(k => scores[k] || 0), 1);

  const pts = pulsionOrder.map((k, i) => {
    const angle = (Math.PI * 2 * i) / n - Math.PI / 2;
    const val = (scores[k] || 0) / maxScore;
    return { x: cx + Math.cos(angle) * r * val, y: cy + Math.sin(angle) * r * val, k, angle };
  });

  const labelPts = pulsionOrder.map((k, i) => {
    const angle = (Math.PI * 2 * i) / n - Math.PI / 2;
    return { x: cx + Math.cos(angle) * (r + 30), y: cy + Math.sin(angle) * (r + 30), k, angle };
  });

  const gridLevels = [0.25, 0.5, 0.75, 1.0];
  const polygon = pts.map(p => `${p.x},${p.y}`).join(" ");

  return (
    <svg viewBox="0 0 320 320" style={{ width: "100%", maxWidth: 320 }}>
      {gridLevels.map((lv, li) => (
        <polygon key={li} points={pulsionOrder.map((_, i) => {
          const a = (Math.PI * 2 * i) / n - Math.PI / 2;
          return `${cx + Math.cos(a) * r * lv},${cy + Math.sin(a) * r * lv}`;
        }).join(" ")} fill="none" stroke="#333" strokeWidth={0.5} opacity={0.4} />
      ))}
      {pulsionOrder.map((_, i) => {
        const a = (Math.PI * 2 * i) / n - Math.PI / 2;
        return <line key={i} x1={cx} y1={cy} x2={cx + Math.cos(a) * r} y2={cy + Math.sin(a) * r} stroke="#333" strokeWidth={0.5} opacity={0.4} />;
      })}
      <polygon points={polygon} fill="#E50B67" fillOpacity={0.15} stroke="#E50B67" strokeWidth={2} />
      {pts.map((p, i) => <circle key={i} cx={p.x} cy={p.y} r={4} fill={pulsionColors[p.k]} />)}
      {labelPts.map((p, i) => (
        <text key={i} x={p.x} y={p.y} textAnchor="middle" dominantBaseline="middle" fill={pulsionColors[p.k]} fontSize={11} fontWeight="600" fontFamily="'Montserrat', sans-serif">
          {pulsionLabels[p.k][lang]}
        </text>
      ))}
    </svg>
  );
}

// ─── MAIN APP ────────────────────────────────────────────────────────────────

export default function PulsionsAssessment() {
  const [lang, setLang] = useState("en");
  const [phase, setPhase] = useState("welcome"); // welcome, mbti, transition, pulsions, results
  const [currentQ, setCurrentQ] = useState(0);
  const [mbtiAnswers, setMbtiAnswers] = useState({});
  const [pulAnswers, setPulAnswers] = useState({});
  const containerRef = useRef(null);

  useEffect(() => {
    if (containerRef.current) containerRef.current.scrollTo({ top: 0, behavior: "smooth" });
  }, [currentQ, phase]);

  const questions = phase === "mbti" ? mbtiQuestions : pulsionsQuestions;
  const answers = phase === "mbti" ? mbtiAnswers : pulAnswers;
  const setAnswers = phase === "mbti" ? setMbtiAnswers : setPulAnswers;
  const progress = Object.keys(answers).length;
  const total = questions.length;
  const allDone = progress === total;

  const handleAnswer = (qId, score) => {
    const next = { ...answers, [qId]: score };
    if (phase === "mbti") setMbtiAnswers(next); else setPulAnswers(next);
    if (currentQ < total - 1) setTimeout(() => setCurrentQ(currentQ + 1), 180);
  };

  const computeMBTI = () => {
    const c = { E: 0, I: 0, N: 0, S: 0, T: 0, F: 0, J: 0, P: 0 };
    Object.values(mbtiAnswers).forEach(s => { c[s] = (c[s] || 0) + 1; });
    const dims = {};
    ["EI", "NS", "TF", "JP"].forEach(d => {
      const [l, r] = dimLabels[d];
      dims[d] = { pct: Math.round((c[l] / (c[l] + c[r])) * 100), letter: c[l] >= c[r] ? l : r };
    });
    return dims;
  };

  const computePulsions = () => {
    const c = {};
    pulsionOrder.forEach(k => { c[k] = 0; });
    Object.values(pulAnswers).forEach(s => { c[s] = (c[s] || 0) + 1; });
    const sorted = pulsionOrder.slice().sort((a, b) => c[b] - c[a]);
    return { scores: c, dominant: sorted[0], secondary: sorted[1] };
  };

  // ─── STYLES ──────────────────────────────────────────────────────────────
  const S = {
    root: { minHeight: "100vh", background: "#0A0A0F", color: "#E5E5E5", fontFamily: "'Montserrat', 'Noto Sans SC', system-ui, sans-serif", overflowY: "auto" },
    container: { maxWidth: 600, margin: "0 auto", padding: "32px 20px" },
    coral: "#E50B67",
    coralLight: "#FF2D78",
    dark: "#0A0A0F",
    card: { background: "#111118", border: "1px solid #1E1E2A", borderRadius: 12, padding: 24, marginBottom: 16 },
    langToggle: { position: "absolute", top: 16, right: 20, display: "flex", gap: 4 },
    langBtn: (active) => ({
      padding: "4px 12px", borderRadius: 4, border: "none", cursor: "pointer", fontSize: 12, fontWeight: 600,
      background: active ? "#E50B67" : "#1E1E2A", color: active ? "#FFF" : "#666",
      fontFamily: "'Montserrat', sans-serif",
    }),
  };

  // ─── WELCOME ─────────────────────────────────────────────────────────────
  if (phase === "welcome") {
    return (
      <div ref={containerRef} style={S.root}>
        <div style={{ position: "relative" }}>
          <div style={S.langToggle}>
            <button onClick={() => setLang("en")} style={S.langBtn(lang === "en")}>EN</button>
            <button onClick={() => setLang("cn")} style={S.langBtn(lang === "cn")}>中文</button>
          </div>
        </div>
        <div style={{ ...S.container, textAlign: "center", paddingTop: 80 }}>
          <div style={{ fontSize: 11, textTransform: "uppercase", letterSpacing: 4, color: "#E50B67", marginBottom: 24 }}>
            Digital Luxury Group
          </div>
          <div style={{ fontSize: 36, fontWeight: 800, color: "#FFF", marginBottom: 8, lineHeight: 1.2 }}>
            {t(lang, "Candidate Profile Assessment", "候选人性格评估")}
          </div>
          <div style={{ fontSize: 15, color: "#888", marginBottom: 48, lineHeight: 1.6 }}>
            {t(lang, "MBTI Personality Type + PULSIONS Motivational Drivers", "MBTI人格类型 + PULSIONS动机驱动评估")}
          </div>
          <div style={{ ...S.card, textAlign: "left", marginBottom: 32 }}>
            <div style={{ fontSize: 13, fontWeight: 700, color: "#E50B67", marginBottom: 12, textTransform: "uppercase", letterSpacing: 2 }}>
              {t(lang, "What to expect", "评估说明")}
            </div>
            <div style={{ fontSize: 14, color: "#AAA", lineHeight: 1.8 }}>
              {t(lang,
                "This assessment consists of 45 forced-choice questions in two parts. Part 1 (20 questions) maps your personality type across four dimensions. Part 2 (25 questions) identifies your primary motivational drivers. There are no right or wrong answers — choose the statement that feels more true, more often. The assessment takes approximately 12-15 minutes.",
                "本评估包含两部分共45道选择题。第一部分（20题）评估四个维度的人格类型。第二部分（25题）识别您的主要动机驱动力。没有对错之分——请选择更符合您日常真实感受的选项。评估大约需要12-15分钟。"
              )}
            </div>
          </div>
          <div style={{ display: "flex", gap: 16, justifyContent: "center", marginBottom: 48 }}>
            <div style={{ ...S.card, flex: 1, textAlign: "center", padding: 20 }}>
              <div style={{ fontSize: 28, fontWeight: 800, color: "#FFF" }}>20</div>
              <div style={{ fontSize: 11, color: "#666", marginTop: 4 }}>{t(lang, "MBTI Questions", "MBTI题目")}</div>
            </div>
            <div style={{ ...S.card, flex: 1, textAlign: "center", padding: 20 }}>
              <div style={{ fontSize: 28, fontWeight: 800, color: "#FFF" }}>25</div>
              <div style={{ fontSize: 11, color: "#666", marginTop: 4 }}>{t(lang, "PULSIONS Questions", "PULSIONS题目")}</div>
            </div>
            <div style={{ ...S.card, flex: 1, textAlign: "center", padding: 20 }}>
              <div style={{ fontSize: 28, fontWeight: 800, color: "#FFF" }}>~12</div>
              <div style={{ fontSize: 11, color: "#666", marginTop: 4 }}>{t(lang, "Minutes", "分钟")}</div>
            </div>
          </div>
          <button
            onClick={() => { setPhase("mbti"); setCurrentQ(0); }}
            style={{
              padding: "16px 48px", background: "#E50B67", border: "none", borderRadius: 8,
              color: "#FFF", fontSize: 16, fontWeight: 700, cursor: "pointer",
              fontFamily: "'Montserrat', sans-serif", letterSpacing: 1,
              boxShadow: "0 0 30px rgba(229,11,103,0.3)", transition: "all 0.2s",
            }}
            onMouseEnter={e => { e.target.style.background = "#FF2D78"; e.target.style.boxShadow = "0 0 40px rgba(229,11,103,0.5)"; }}
            onMouseLeave={e => { e.target.style.background = "#E50B67"; e.target.style.boxShadow = "0 0 30px rgba(229,11,103,0.3)"; }}
          >
            {t(lang, "Begin Assessment", "开始评估")} →
          </button>
        </div>
      </div>
    );
  }

  // ─── TRANSITION ──────────────────────────────────────────────────────────
  if (phase === "transition") {
    return (
      <div ref={containerRef} style={S.root}>
        <div style={{ position: "relative" }}>
          <div style={S.langToggle}>
            <button onClick={() => setLang("en")} style={S.langBtn(lang === "en")}>EN</button>
            <button onClick={() => setLang("cn")} style={S.langBtn(lang === "cn")}>中文</button>
          </div>
        </div>
        <div style={{ ...S.container, textAlign: "center", paddingTop: 80 }}>
          <div style={{ fontSize: 13, color: "#10B981", fontWeight: 600, marginBottom: 8 }}>✓ {t(lang, "Part 1 Complete", "第一部分完成")}</div>
          <div style={{ fontSize: 28, fontWeight: 800, color: "#FFF", marginBottom: 16 }}>
            {t(lang, "PULSIONS", "PULSIONS")}
          </div>
          <div style={{ fontSize: 15, color: "#888", marginBottom: 12, lineHeight: 1.6 }}>
            {t(lang, "Motivational Drivers Assessment", "动机驱动力评估")}
          </div>
          <div style={{ fontSize: 14, color: "#666", marginBottom: 48, lineHeight: 1.7, maxWidth: 440, margin: "0 auto 48px" }}>
            {t(lang,
              "Part 2 presents 25 scenario pairs. In each, choose the option that resonates more with how you naturally think and act. Focus on your instinctive preference, not what you think is expected.",
              "第二部分包含25对场景选择。每题请选择更符合您自然想法和行为方式的选项。关注您的本能偏好，而非您认为被期望的答案。"
            )}
          </div>
          <button
            onClick={() => { setPhase("pulsions"); setCurrentQ(0); }}
            style={{
              padding: "16px 48px", background: "#E50B67", border: "none", borderRadius: 8,
              color: "#FFF", fontSize: 16, fontWeight: 700, cursor: "pointer",
              fontFamily: "'Montserrat', sans-serif", letterSpacing: 1,
              boxShadow: "0 0 30px rgba(229,11,103,0.3)", transition: "all 0.2s",
            }}
            onMouseEnter={e => { e.target.style.background = "#FF2D78"; }}
            onMouseLeave={e => { e.target.style.background = "#E50B67"; }}
          >
            {t(lang, "Continue", "继续")} →
          </button>
        </div>
      </div>
    );
  }

  // ─── RESULTS ─────────────────────────────────────────────────────────────
  if (phase === "results") {
    const mbti = computeMBTI();
    const pul = computePulsions();
    const type = mbti.EI.letter + mbti.NS.letter + mbti.TF.letter + mbti.JP.letter;

    return (
      <div ref={containerRef} style={S.root}>
        <div style={{ position: "relative" }}>
          <div style={S.langToggle}>
            <button onClick={() => setLang("en")} style={S.langBtn(lang === "en")}>EN</button>
            <button onClick={() => setLang("cn")} style={S.langBtn(lang === "cn")}>中文</button>
          </div>
        </div>
        <div style={S.container}>
          <div style={{ textAlign: "center", marginBottom: 48 }}>
            <div style={{ fontSize: 11, textTransform: "uppercase", letterSpacing: 4, color: "#E50B67", marginBottom: 24 }}>
              Digital Luxury Group
            </div>
            <div style={{ fontSize: 14, textTransform: "uppercase", letterSpacing: 3, color: "#666", marginBottom: 12 }}>
              {t(lang, "Assessment Results", "评估结果")}
            </div>
          </div>

          {/* MBTI Section */}
          <div style={{ ...S.card, marginBottom: 24 }}>
            <div style={{ fontSize: 12, textTransform: "uppercase", letterSpacing: 2, color: "#E50B67", marginBottom: 16 }}>
              {t(lang, "Part 1 — Personality Type", "第一部分 — 人格类型")}
            </div>
            <div style={{ textAlign: "center", marginBottom: 24 }}>
              <div style={{ fontSize: 56, fontWeight: 800, color: "#FFF", letterSpacing: 6 }}>{type}</div>
            </div>
            {["EI", "NS", "TF", "JP"].map(dim => {
              const r = mbti[dim];
              const color = dimColors[dim];
              const names = dimNames[dim][lang];
              const strength = Math.abs(r.pct - 50);
              const conf = strength > 35 ? t(lang, "Very clear", "非常明确") : strength > 20 ? t(lang, "Clear", "明确") : strength > 10 ? t(lang, "Moderate", "中等") : t(lang, "Borderline", "临界");
              return (
                <div key={dim} style={{ marginBottom: 20 }}>
                  <div style={{ display: "flex", justifyContent: "space-between", alignItems: "center", marginBottom: 6 }}>
                    <span style={{ fontSize: 12, fontWeight: 600, color }}>{names[0]}</span>
                    <span style={{ fontSize: 10, color: "#555", padding: "2px 8px", background: "#1E1E2A", borderRadius: 4 }}>{conf}</span>
                    <span style={{ fontSize: 12, fontWeight: 600, color: "#666" }}>{names[1]}</span>
                  </div>
                  <div style={{ position: "relative", height: 6, background: "#1E1E2A", borderRadius: 3 }}>
                    <div style={{ position: "absolute", left: 0, top: 0, height: "100%", width: `${r.pct}%`, background: color, borderRadius: 3, transition: "width 0.6s" }} />
                    <div style={{ position: "absolute", left: "50%", top: -3, width: 1, height: 12, background: "#333" }} />
                  </div>
                  <div style={{ display: "flex", justifyContent: "space-between", marginTop: 4 }}>
                    <span style={{ fontSize: 16, fontWeight: 700, color: r.pct >= 50 ? color : "#444" }}>{r.pct}%</span>
                    <span style={{ fontSize: 16, fontWeight: 700, color: r.pct < 50 ? "#CCC" : "#444" }}>{100 - r.pct}%</span>
                  </div>
                </div>
              );
            })}
          </div>

          {/* PULSIONS Section */}
          <div style={{ ...S.card, marginBottom: 24 }}>
            <div style={{ fontSize: 12, textTransform: "uppercase", letterSpacing: 2, color: "#E50B67", marginBottom: 16 }}>
              {t(lang, "Part 2 — Motivational Drivers", "第二部分 — 动机驱动力")}
            </div>
            <div style={{ display: "flex", justifyContent: "center", marginBottom: 24 }}>
              <RadarChart scores={pul.scores} lang={lang} />
            </div>
            <div style={{ display: "flex", gap: 12, justifyContent: "center", marginBottom: 24 }}>
              <div style={{ padding: "12px 20px", borderRadius: 8, background: `${pulsionColors[pul.dominant]}22`, border: `1px solid ${pulsionColors[pul.dominant]}66`, textAlign: "center" }}>
                <div style={{ fontSize: 10, textTransform: "uppercase", letterSpacing: 2, color: "#888", marginBottom: 4 }}>{t(lang, "Dominant", "主导")}</div>
                <div style={{ fontSize: 20, fontWeight: 800, color: pulsionColors[pul.dominant] }}>{pulsionLabels[pul.dominant][lang]}</div>
                <div style={{ fontSize: 12, color: "#666", marginTop: 2 }}>{pul.scores[pul.dominant]}/{total} {t(lang, "selections", "次选择")}</div>
              </div>
              <div style={{ padding: "12px 20px", borderRadius: 8, background: `${pulsionColors[pul.secondary]}15`, border: `1px solid ${pulsionColors[pul.secondary]}44`, textAlign: "center" }}>
                <div style={{ fontSize: 10, textTransform: "uppercase", letterSpacing: 2, color: "#888", marginBottom: 4 }}>{t(lang, "Secondary", "辅助")}</div>
                <div style={{ fontSize: 20, fontWeight: 800, color: pulsionColors[pul.secondary] }}>{pulsionLabels[pul.secondary][lang]}</div>
                <div style={{ fontSize: 12, color: "#666", marginTop: 2 }}>{pul.scores[pul.secondary]}/{total} {t(lang, "selections", "次选择")}</div>
              </div>
            </div>
            {/* All scores bar chart */}
            <div style={{ marginTop: 16 }}>
              {pulsionOrder.slice().sort((a, b) => pul.scores[b] - pul.scores[a]).map(k => {
                const maxS = Math.max(...Object.values(pul.scores));
                const w = maxS > 0 ? (pul.scores[k] / maxS) * 100 : 0;
                return (
                  <div key={k} style={{ display: "flex", alignItems: "center", gap: 12, marginBottom: 8 }}>
                    <div style={{ width: 80, fontSize: 12, fontWeight: 600, color: pulsionColors[k], textAlign: "right" }}>{pulsionLabels[k][lang]}</div>
                    <div style={{ flex: 1, height: 8, background: "#1E1E2A", borderRadius: 4, overflow: "hidden" }}>
                      <div style={{ height: "100%", width: `${w}%`, background: pulsionColors[k], borderRadius: 4, transition: "width 0.6s" }} />
                    </div>
                    <div style={{ width: 24, fontSize: 12, color: "#666", textAlign: "right" }}>{pul.scores[k]}</div>
                  </div>
                );
              })}
            </div>
          </div>

          {/* Footer */}
          <div style={{ textAlign: "center", padding: "24px 0", borderTop: "1px solid #1E1E2A", marginTop: 16 }}>
            <div style={{ fontSize: 11, color: "#444" }}>Digital Luxury Group · {t(lang, "Candidate Profile Assessment", "候选人性格评估")} · 2026</div>
          </div>
        </div>
      </div>
    );
  }

  // ─── QUESTION VIEW (MBTI & PULSIONS) ─────────────────────────────────────
  const q = questions[currentQ];
  const flip = shouldFlip(q.id);
  const optA = flip ? q.b : q.a;
  const optB = flip ? q.a : q.b;
  const sectionLabel = phase === "mbti"
    ? t(lang, "Part 1 — Personality Type", "第一部分 — 人格类型")
    : t(lang, "Part 2 — Motivational Drivers", "第二部分 — 动机驱动力");
  const globalProgress = phase === "mbti" ? progress : 20 + progress;
  const globalTotal = 45;

  return (
    <div ref={containerRef} style={S.root}>
      <div style={{ position: "relative" }}>
        <div style={S.langToggle}>
          <button onClick={() => setLang("en")} style={S.langBtn(lang === "en")}>EN</button>
          <button onClick={() => setLang("cn")} style={S.langBtn(lang === "cn")}>中文</button>
        </div>
      </div>
      <div style={S.container}>
        {/* Header */}
        <div style={{ textAlign: "center", marginBottom: 32 }}>
          <div style={{ fontSize: 11, textTransform: "uppercase", letterSpacing: 4, color: "#E50B67", marginBottom: 8 }}>
            Digital Luxury Group
          </div>
          <div style={{ fontSize: 12, color: "#555" }}>{sectionLabel}</div>
        </div>

        {/* Global progress */}
        <div style={{ marginBottom: 8 }}>
          <div style={{ display: "flex", justifyContent: "space-between", marginBottom: 6 }}>
            <span style={{ fontSize: 11, color: "#555" }}>{globalProgress} / {globalTotal}</span>
            <span style={{ fontSize: 11, color: "#E50B67" }}>
              {t(lang, `Question ${currentQ + 1} of ${total}`, `第 ${currentQ + 1} / ${total} 题`)}
            </span>
          </div>
          <div style={{ height: 2, background: "#1E1E2A", borderRadius: 1 }}>
            <div style={{ height: "100%", width: `${(globalProgress / globalTotal) * 100}%`, background: "#E50B67", transition: "width 0.3s", borderRadius: 1 }} />
          </div>
        </div>

        {/* Question dots */}
        <div style={{ display: "flex", gap: 4, justifyContent: "center", marginBottom: 28, flexWrap: "wrap" }}>
          {questions.map((qq, i) => (
            <button key={qq.id} onClick={() => setCurrentQ(i)} style={{
              width: 24, height: 24, borderRadius: 5, border: "none", cursor: "pointer", fontSize: 10, fontWeight: 600,
              background: i === currentQ ? "#E50B67" : answers[qq.id] ? "#1E1E2A" : "#111118",
              color: i === currentQ ? "#FFF" : answers[qq.id] ? "#666" : "#333",
              transition: "all 0.15s", fontFamily: "'Montserrat', sans-serif",
            }}>
              {i + 1}
            </button>
          ))}
        </div>

        {/* Instruction */}
        <div style={{ fontSize: 13, color: "#555", marginBottom: 20 }}>
          {t(lang, "Choose the statement that feels more true, more often:", "请选择更符合您日常真实感受的选项：")}
        </div>

        {/* Options */}
        {[optA, optB].map((opt, i) => {
          const isSelected = answers[q.id] === opt.s;
          return (
            <button key={i} onClick={() => handleAnswer(q.id, opt.s)} style={{
              width: "100%", textAlign: "left", padding: "18px 22px", marginBottom: 10,
              background: isSelected ? "#1A0A14" : "transparent",
              border: isSelected ? "1px solid #E50B67" : "1px solid #1E1E2A",
              borderRadius: 10, cursor: "pointer",
              color: isSelected ? "#FFF" : "#AAA",
              fontSize: 14, lineHeight: 1.6, transition: "all 0.15s",
              fontFamily: "'Montserrat', 'Noto Sans SC', sans-serif",
            }}
              onMouseEnter={e => { if (!isSelected) { e.target.style.borderColor = "#333"; e.target.style.color = "#CCC"; } }}
              onMouseLeave={e => { if (!isSelected) { e.target.style.borderColor = "#1E1E2A"; e.target.style.color = "#AAA"; } }}
            >
              {opt[lang]}
            </button>
          );
        })}

        {/* Navigation */}
        <div style={{ display: "flex", justifyContent: "space-between", marginTop: 28 }}>
          <button onClick={() => {
            if (currentQ > 0) setCurrentQ(currentQ - 1);
            else if (phase === "pulsions") { setPhase("mbti"); setCurrentQ(mbtiQuestions.length - 1); }
          }} style={{
            padding: "10px 20px", background: "transparent", border: "1px solid #1E1E2A",
            color: (currentQ > 0 || phase === "pulsions") ? "#666" : "#222", borderRadius: 6, cursor: (currentQ > 0 || phase === "pulsions") ? "pointer" : "default",
            fontSize: 12, fontFamily: "'Montserrat', sans-serif",
          }}>
            ← {t(lang, "Back", "返回")}
          </button>

          {currentQ < total - 1 ? (
            <button onClick={() => setCurrentQ(currentQ + 1)} style={{
              padding: "10px 20px", background: "transparent", border: "1px solid #1E1E2A",
              color: "#666", borderRadius: 6, cursor: "pointer", fontSize: 12,
              fontFamily: "'Montserrat', sans-serif",
            }}>
              {t(lang, "Skip", "跳过")} →
            </button>
          ) : (
            <button
              onClick={() => {
                if (!allDone) return;
                if (phase === "mbti") { setPhase("transition"); }
                else { setPhase("results"); }
              }}
              disabled={!allDone}
              style={{
                padding: "12px 28px",
                background: allDone ? "#E50B67" : "#1E1E2A",
                border: "none", color: allDone ? "#FFF" : "#444",
                borderRadius: 6, cursor: allDone ? "pointer" : "default",
                fontSize: 13, fontWeight: 700,
                fontFamily: "'Montserrat', sans-serif",
                boxShadow: allDone ? "0 0 20px rgba(229,11,103,0.3)" : "none",
              }}
            >
              {phase === "mbti" ? t(lang, "Next Section", "下一部分") : t(lang, "See Results", "查看结果")} →
            </button>
          )}
        </div>
      </div>
    </div>
  );
}
