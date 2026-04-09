# English Mock Interview Tool 鈥?SPEC.md

## 1. Concept & Vision

涓€涓府鍔╃敤鎴风粌涔犺嫳璇潰璇曠殑娌夋蹈寮忓伐鍏枫€傞€氳繃涓板瘜鐨勯搴撱€佸嵆鏃跺弽棣堝拰璇勫垎绯荤粺锛屾ā鎷熺湡瀹為潰璇曞満鏅€傛敮鎸佸绉嶉潰璇曠被鍨嬶紙琛屼负闈€佹妧鏈潰銆佸帇鍔涢潰绛夛級锛岀敤鎴峰洖绛斿悗鑾峰緱璇︾粏璇勫垎鍜岀籂姝ｅ缓璁€?
鏁翠綋椋庢牸锛?*涓撲笟浣嗕笉鍘嬫姂**锛屽儚涓€涓创韬殑闈㈣瘯鏁欑粌鍦ㄨ韩杈广€?
## 2. Design Language

**Aesthetic:** 骞插噣銆佷笓涓氱殑宸ュ叿鎰燂紝甯︿竴鐐规俯鏆栥€傚儚鏄?Notion + Linear 鐨勭粨鍚堚€斺€斿姛鑳藉己浣嗙晫闈㈠弸濂姐€?
**Color Palette:**
- Background: `#0F172A` (娣辫摑榛?
- Surface: `#1E293B` (鍗＄墖鑳屾櫙)
- Primary: `#3B82F6` (钃濓紝淇′换/涓撲笟)
- Accent: `#10B981` (缁匡紝鎴愬姛/姝ｇ‘)
- Warning: `#F59E0B` (姗欙紝鎻愰啋)
- Error: `#EF4444` (绾紝閿欒)
- Text Primary: `#F8FAFC`
- Text Secondary: `#94A3B8`

**Typography:**
- Headings: Inter (bold)
- Body: Inter (regular)
- Mono: JetBrains Mono (浠ｇ爜/璇勫垎)

**Motion:**
- 鍗＄墖鍒囨崲: slide + fade, 300ms ease-out
- 璇勫垎鍑虹幇: scale up from 0.8 + fade, 400ms
- 姝ｇ‘/閿欒鍙嶉: shake (error) / pulse (success)
- 杩涘害鏉? smooth width transition

## 3. Layout & Structure

```
鈹屸攢鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹?鈹? Header: Logo + 闈㈣瘯绫诲瀷鍒囨崲 + 杩涘害鎸囩ず鍣?    鈹?鈹溾攢鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹?鈹?                                            鈹?鈹? 鈹屸攢鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹?  鈹?鈹? 鈹? Question Card (澶у崱鐗?              鈹?  鈹?鈹? 鈹? - 棰樺彿 + 闅惧害鏍囩                    鈹?  鈹?鈹? 鈹? - 闂姝ｆ枃                           鈹?  鈹?鈹? 鈹? - 鎻愮ず璇嶏紙鍙€夛級                      鈹?  鈹?鈹? 鈹斺攢鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹?  鈹?鈹?                                            鈹?鈹? 鈹屸攢鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹?  鈹?鈹? 鈹? Answer Area                        鈹?  鈹?鈹? 鈹? - Textarea (鏀寔璇煶杈撳叆 TODO)       鈹?  鈹?鈹? 鈹? - 瀛楃璁℃暟                           鈹?  鈹?鈹? 鈹斺攢鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹?  鈹?鈹?                                            鈹?鈹? [ Submit Answer ]                         鈹?鈹?                                            鈹?鈹溾攢鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹?鈹? Feedback Panel (灞曞紑鍚?                    鈹?鈹? - 鎬诲垎 + 鍚勭淮搴﹁瘎鍒?                        鈹?鈹? - 绛旀鍒嗘瀽 / 绀鸿寖鍥炵瓟                        鈹?鈹? - 璇硶/璇嶆眹绾犳                             鈹?鈹? [ Next Question ]                         鈹?鈹斺攢鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹€鈹?```

**Responsive:** 鍗曞垪甯冨眬锛岀Щ鍔ㄧ鍙嬪ソ銆?
## 4. Features & Interactions

### 4.1 棰樺簱绯荤粺
- **鍒嗙被:**
  - `general` 鈥?閫氱敤寮€鍦?缁撳熬闂 (e.g. "Tell me about yourself")
  - `behavioral` 鈥?STAR鍘熷垯琛屼负闂 (e.g. "Tell me about a time you dealt with conflict")
  - `technical` 鈥?鎶€鏈兘鍔涢棶棰?(e.g. "Explain a project you built")
  - `pressure` 鈥?鍘嬪姏娴嬭瘯闂 (e.g. "What's your biggest weakness?")
  - `industry` 鈥?琛屼笟璁ょ煡闂 (e.g. "Why our company?")
- **闅惧害:** `easy` / `medium` / `hard`
- 姣忕被鑷冲皯 15 閬撻锛岄殢鏈烘娊鍙栦笉閲嶅鐩村埌鐢ㄥ畬

### 4.2 闂瓟娴佺▼
1. 鏄剧ず闂 + 鍙€夋彁绀?2. 鐢ㄦ埛鍦?textarea 杈撳叆绛旀锛堟渶浣?50 瀛楃锛?3. 鐐瑰嚮 Submit 鎴?Ctrl+Enter 鎻愪氦
4. 灞曠ず feedback panel

### 4.3 璇勫垎绯荤粺 (鎬诲垎 100)
| 缁村害 | 鏉冮噸 | 璇勫垎鏍囧噯 |
|------|------|----------|
| Content | 30% | 鍥炵瓟鐩稿叧鎬с€佸畬鏁存€с€佹湁鏃犺窇棰?|
| Grammar | 25% | 璇硶姝ｇ‘鎬с€佸鏉傚彞浣跨敤 |
| Vocabulary | 25% | 璇嶆眹澶氭牱鎬с€侀珮绾ц瘝姹囦娇鐢?|
| Fluency | 20% | 娴佺晠搴︺€佸仠椤挎鏁?|

璇勫垎绠楁硶锛氬熀浜庡叧閿瘝妫€鍑?+ 瑙勫垯鍒ゆ柇锛堢畝鍗曞疄鐜帮紝鍙墿灞?AI锛?
### 4.4 鍙嶉闈㈡澘
- 鍚勭淮搴﹀垎鏁?+ 闆疯揪鍥撅紙CSS 瀹炵幇锛?- 绛旀浼樼偣锛堢豢鑹查珮浜級
- 闂绾犳锛堢孩鑹蹭笅鍒掔嚎 + 瑙ｉ噴锛?- 绀鸿寖鍥炵瓟锛堝彲鎶樺彔锛?
### 4.5 杩涘害杩借釜
- 椤堕儴杩涘害鏉★細褰撳墠棰樺彿 / 鎬婚鏁?- 闈㈣瘯绫诲瀷鍒囨崲鏃堕噸缃?- 瀹屾垚鍚庢樉绀烘€荤粨鎶ュ憡

### 4.6 浜や簰缁嗚妭
- **Submit 鎸夐挳:** 绂佺敤鐘舵€佹椂鍙樼伆锛宭oading 鏃舵樉绀?spinner
- **Textarea:** 鑷姩 focus锛宲laceholder 鍔ㄦ€佹彁绀?- **Keyboard:** Ctrl+Enter 鎻愪氦锛孍scape 鍏抽棴 feedback
- **Toast:** 鎿嶄綔鎴愬姛/澶辫触绠€鐭彁绀?
## 5. Component Inventory

### QuestionCard
- 棰樺彿 badge (e.g. "Q3")
- 闅惧害鏍囩 (color-coded: green/orange/red)
- 闂鏂囨湰 (large, readable)
- 鍙€夋彁绀?(collapsed by default, "Show hint")

### AnswerInput
- Textarea (min-height: 150px, resize vertical)
- Character counter (bottom-right, turns red near limit)
- Placeholder: "Type your answer here... (Ctrl+Enter to submit)"

### SubmitButton
- States: default, hover (glow), loading (spinner), disabled (grayed)
- Full width on mobile

### FeedbackPanel
- Slide-down animation on appear
- Score ring (SVG circle with animated stroke-dasharray)
- Dimension bars (horizontal progress bars with labels)
- Correct/Incorrect highlights in answer review
- Model answer accordion

### ProgressBar
- Thin bar at top (3px height)
- Gradient fill (primary 鈫?accent)

### CategoryTabs
- Horizontal scrollable tabs
- Active state: underline + bold

### SummaryCard (end of session)
- Total score (large number)
- Breakdown by category
- "Practice Again" button

## 6. Technical Approach

**Stack:**
- Single HTML file
- Tailwind CSS (via CDN)
- Vanilla JavaScript (ES6+)
- No build step 鈥?vibe coding friendly

**Architecture:**
```
index.html
鈹溾攢鈹€ <style> embedded CSS (if needed beyond Tailwind)
鈹溾攢鈹€ Question Bank (JS object)
鈹溾攢鈹€ State Management (simple object)
鈹?  鈹溾攢鈹€ currentCategory
鈹?  鈹溾攢鈹€ currentQuestionIndex
鈹?  鈹溾攢鈹€ usedQuestions (Set)
鈹?  鈹溾攢鈹€ answers (array)
鈹?  鈹斺攢鈹€ sessionScore
鈹溾攢鈹€ Functions
鈹?  鈹溾攢鈹€ loadQuestion()
鈹?  鈹溾攢鈹€ submitAnswer()
鈹?  鈹溾攢鈹€ calculateScore()
鈹?  鈹溾攢鈹€ showFeedback()
鈹?  鈹溾攢鈹€ nextQuestion()
鈹?  鈹斺攢鈹€ endSession()
鈹斺攢鈹€ Event Listeners
```

**璇勫垎绠楁硶锛堢畝鍖栫増锛?**
- 瀹氫箟姣忛"鍏抽敭璇?鍒楄〃
- Content: 妫€鍑哄叧閿瘝鏁伴噺
- Grammar: 绠€鍗曟鍒欐娴嬪父瑙侀敊璇?- Vocabulary: 妫€娴嬮珮绾ц瘝姹囦娇鐢?- Fluency: 鏍规嵁绛旀闀垮害/鍙ュ瓙鏁颁及绠?
**鎵╁睍鎬?**
- 棰樺簱鍙嫭绔嬩负 JSON 鏂囦欢
- 棰勭暀 AI 璇勫垎鎺ュ彛锛堟湭鏉ュ彲鎺?GPT API锛?
## 7. Question Bank (Initial Set)

姣忕被鑷冲皯 15 棰橈紝瑕嗙洊甯歌闈㈣瘯鍦烘櫙锛?
### General (15棰?
1. "Tell me about yourself."
2. "What are your strengths?"
3. "What are your weaknesses?"
4. "Why are you interested in this role?"
5. "Where do you see yourself in 5 years?"
... 绛?
### Behavioral (15棰? 鈥?STAR 鏍煎紡
1. "Tell me about a time you dealt with a difficult coworker."
2. "Describe a situation where you had to meet a tight deadline."
3. "Give an example of a goal you reached and how you achieved it."
... 绛?
### Technical (10棰?
1. "Walk me through a project you're proud of."
2. "How do you handle technical challenges?"
... 绛?
### Pressure (10棰?
1. "Tell me about your biggest failure."
2. "Why should we hire you over other candidates?"
... 绛?
### Industry (10棰?
1. "What do you know about our company?"
2. "What trends in our industry excite you?"
... 绛?
---
*Last updated: 2026-04-09*
