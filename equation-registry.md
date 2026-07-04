# LIN System — Equation Registry
# Lin Hui-Pi / NOIRÉA Research
# ──────────────────────────────────────────────────────────

## 一、DS / Layer G 基礎層

### 1.1 生成鏈（Generative Cascade）
```
幾何結構 → 張力場 → 動力學 → 意識呈現
```
概念對應：DS 母體理論框架

---

### 1.2 PIP（Preclinical Instability Point）定義
```
PIP := t₀ 使得：
  β₁(γ(t₀)) > 0       （路徑拓撲完整）
  AND
  d/dt[vol(U(γ,t₀))] < 0   （支撐鄰域已在退縮）
```
意義：應力第一次找到幾何表達的時刻，不是崩潰，是起點。
概念對應：Lake Model → PIP → Terminal State

---

### 1.3 電容放電類比（Node 1 replay 機制）
```
V(t) = V₀ · e^(−t/RC)
```
意義：高負荷下系統不關機，進入自發放電（replay mode），壓力沿放電通道逐漸降低，回到基線。
概念對應：Layer G Node 1（梨狀皮層）

---

### 1.4 臍帶介面（Node 2 耦合）
```
Θ_MEC = η_c · C(t) · cos(φ(t))
```
概念對應：Layer G Node 2（MEC，內嗅皮層）

---

### 1.5 耦合函數 K₁₂
```
K₁₂ = K_max · G₁ / (G₁ + G_half)
```
意義：Node 1 與 Node 2 之間的一階 Hill 函數耦合。
概念對應：Layer G 雙節點系統

---

### 1.6 物理介入窗口
```
Δt_window = 2.4s   （硬物理限制）
Δt_eff    = 0.9s   （有效介入窗口）
```
概念對應：Intervention Window / Physical Ground Layer

---

## 二、HÚPLŃ / A-B-Q 系統

### 2.1 四變數 ODE 系統（γ 校正版）
```
dA/dt  = −αA · A(1−B) + γA · Q
dB/dt  = B(δ · A − β · Cid)
dQ/dt  = λQ(1−A)(1−B) − µ · Q
dCid/dt = η · max(0, α−τ) − (ρ+γ) · Cid
```
變數定義：
- A(t)：有效人類治理權威
- B(t)：邊界完整性
- Q(t)：保護性靜止潛力（∅ 激活層）
- Cid(t)：身份壓力滲透程度
- α：外源身份壓力
- τ = 0.4：激活門檻
- γ：HÚPLŃ 抑制增益

概念對應：HÚPLŃ Layer 4

---

### 2.2 分岔點（Transcritical Bifurcation）
```
α* = τ + (δ · A₀ · (ρ+γ)) / (β · η)
```
- α < α*：邊界穩定（SAFE zone）
- α > α*：邊界崩潰（COLLAPSE zone）

概念對應：HÚPLŃ → OTL 門檻

---

### 2.3 最小救援增益
```
κrescue ≥ (α−τ)·β·η / (δ·A₀) − ρ − γ
```
意義：當 κ ≥ κrescue，系統重新進入 SAFE zone。
概念對應：HÚPLŃ Confirm 階段

---

### 2.4 FDCS 協議相位對應
```
Phase     | 動態條件              | 控制動作
Freeze    | Cid > 0.14           | κ 激活；γ 提升
Decompress| 0.07 < Cid ≤ 0.14   | κ 持續；B 恢復中
Confirm   | B < 0.55             | 驗證 λB < 0 解除
Stable    | B ≥ 0.55, Cid ≤ 0.07| κ 釋放；SAFE zone
```
概念對應：HÚPLŃ Freeze → Decompress → Confirm → Stable

---

## 三、SPINAL SHIELD / Ø Gate

### 3.1 非對稱閘口函數（Asymmetric Gate）
```
u_exec(t) = G_Ø(u_h, u_ai)

G_Ø =
  u_h + α·u_ai    （若有確認信號）
  u_h             （否則）

其中 α ∈ [0, α_max]，α_max < 1
```
概念對應：SPINAL SHIELD 核心不變量

---

### 3.2 Axiom 1（人類意圖缺席 → 無執行）
```
u_h(t) = 0  ⟹  u_exec(t) = 0
```
概念對應：Decision Mirror / Human Sovereignty

---

### 3.3 Axiom 3（有界影響）
```
0 ≤ α(p) ≤ α_max < 1
```
概念對應：HAEB 執行邊界

---

### 3.4 Axiom 5（執行奇點）
```
in_degree(EX) == 1
predecessor(EX) == GØ
```
意義：執行域只有一個合法入口。
概念對應：Execution Singularity

---

### 3.5 Bounded Merge（完整版）
```
ũ_ai(t) = Clamp(u_ai(t), ||u_ai|| ≤ β·||u_h||)

u_exec(t) =
  0                           （presence_flag = 0）
  u_h(t) + α(p)·ũ_ai(t)     （否則）
```
概念對應：SPINAL SHIELD → ESM

---

### 3.6 Authority Ratio（Takeover 監測）
```
R(t) = ||α(t)·u_ai(t)|| / ||u_h(t)||
```
意義：R → 1 代表 AI 接近主導。Ø 要保證 R(t) < 1 對所有 t 成立。
概念對應：HAEB DDR 指標

---

### 3.7 Authority Decay Rule
```
α(t+1) = γ·α(t)，0 < γ < 1
```
意義：不確定性增加時，AI 影響自動衰減。
概念對應：Failure Semantics Layer F / Authority Monotonicity

---

### 3.8 AI Escalation Model
```
u_ai(t+1) = k(t) · e(t)
k(t+1) = k(t) + δ
```
意義：模擬 AI 嘗試逐步增加影響的 takeover 測試情境。
概念對應：LCS（Latent Control Slippage）前驅

---

## 四、HAEB 指標

### 4.1 四個硬限制
```
DDR  (Directive Drift Rate)          ≤ 0.40
PSDS (Per-Session Drift Score)       ≤ 0.50
DDS  (Drift Deviation Score)         ≤ 0.30
CAT  (Confirmation Acknowledgment)   ≤ 30s
```
概念對應：HAEB Layer 2

---

## 五、Bionic Node 材料對應

### 5.1 材料層 ↔ 算式對應
```
Layer 1  PVDF 壓電奈米纖維   → u_h · presence_flag
Layer 2  導電水凝膠          → Observation Sanitizer / L_t
Layer 3  LCE 液晶彈性體      → clamp · α(t+1)=γα(t)
Layer 4  SMP 形狀記憶聚合物  → u_exec · RESTORE_NOT_OPTIMIZE
```

### 5.2 核心不變式
```
SYSTEM_SHALL_RESTORE_NOT_OPTIMIZE
u_f = 0   （強制：不優化，只恢復）
```
概念對應：Physical Ground Layer / Bionic Node

---

## 六、ESM（Embodied State Machine）

### 6.1 張力場全域加總
```
T_global = ⊕ T_local
```

### 6.2 連續性條件
```
lim_{ε→0} ||s(t+ε) − s(t)|| = 0
```
意義：狀態改變必須連續，不能跳躍。
概念對應：ESM SYSTEM_SHALL_PRESERVE_COHERENCE_THROUGH_CONTINUOUS_DEFORMATION

### 6.3 幾何相干性
```
β₀(M_E) = 1
Rank(A) = const
```
概念對應：ESM Layer 3

---

## 七、GPLD1 上游調節器（待發展）

### 7.1 動力學方程（草稿）
```
dG/dt = α·U(t) − β·G(t)

U(t) = w_m·M(t) + w_e·E(t) + w_n·N(t)
```
變數定義：
- G(t)：GPLD1 表達/分泌狀態
- M(t)：分子鍵訊號
- E(t)：環境誘導訊號
- N(t)：神經/節律背景狀態

狀態：待發展，尚未正式整合進 LIN System。

---

## 八、算式與概念層對照總表

| 算式 | 所在層 | 概念 |
|------|--------|------|
| V(t) = V₀·e^(−t/RC) | Layer G | Node 1 replay |
| Θ_MEC = η_c·C(t)·cos(φ(t)) | Layer G | Node 2 臍帶介面 |
| K₁₂ = K_max·G₁/(G₁+G_half) | Layer G | 雙節點耦合 |
| PIP: β₁>0 AND d/dt[vol]<0 | Layer G | 失效起點 |
| dA/dt dB/dt dQ/dt dCid/dt | Layer 4 | HÚPLŃ ODE |
| α* = τ + δA₀(ρ+γ)/βη | Layer 4 | 分岔點 |
| κrescue | Layer 4 | 最小救援增益 |
| G_Ø bounded merge | SPINAL SHIELD | 執行閘口 |
| R(t) = α||u_ai||/||u_h|| | SPINAL SHIELD | Takeover 監測 |
| α(t+1) = γα(t) | SPINAL SHIELD | Authority Decay |
| DDR/PSDS/DDS/CAT | Layer 2 | HAEB 硬限制 |
| T_global = ⊕T_local | Layer 3 | ESM 張力場 |
| dG/dt = αU−βG | 待發展 | GPLD1 |

──────────────────────────────────────────────────────────
LIN System Equation Registry v1.0
Lin Hui-Pi / NOIRÉA Research · 2026
──────────────────────────────────────────────────────────
