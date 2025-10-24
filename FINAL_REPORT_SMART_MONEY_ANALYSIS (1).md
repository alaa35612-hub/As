# FINAL_REPORT_SMART_MONEY_ANALYSIS

**المؤشر**: Smart Money Algo Pro E5 - CHADBULL
**التاريخ**: 2025-10-23 13:55:04

## فهرس المحتويات
1. [Pullback](#pullback)
2. [Market Structure](#market-structure)
3. [Order Block](#order-block)
4. [SCOB / Zone Type](#scob--zone-type)
5. [قائمة التحقق (Coverage 99.99%)](#قائمة-التحقق-coverage-9999)
6. [الإعدادات الكاملة](#الإعدادات-الكاملة)

## Pullback
### الإعدادات
- showHL: False
- showMn: False

### الأحداث المكتشفة
- عدد ملصقات Pullback: 0

## Market Structure
### الإعدادات
- showSMC: True
- lengSMC: 40
- structure_type: Choch with IDM

### الكيانات
- خطوط الهيكل: 0
- تنبيهات الهيكل: 0

## Order Block
### الإعدادات
- extndBox: True
- showExob: True
- showIdmob: True
- showSCOB: True

### المناطق الفعالة
- إجمالي الصناديق: 0
- تنبيهات IDM EXT: 0

## SCOB / Zone Type
### الإعدادات
- Show SCOB: True
- Bullish SCOB اللون: #0b3ff9
- Bearish SCOB اللون: #da781d

### إشارات الشموع
- ألوان الأعمدة المسجلة: 0
- تنبيهات Order Flow: 0

## فلترة الأحداث
- `console.max_age_bars` يتحكم بعدد الأعمدة الأخيرة المسموح بها عند عرض قسم `latest_events`. أي حدث أقدم من هذه النافذة يتم تجاهله، بينما القيمة 0 تعطل الفلترة وتحافظ على كل السجلات التاريخية للمنطقة.
- ماسح Binance يتجاهل تلقائيًا الأزواج التي تحتوي أحدث سجلات `latest_events` على طابع زمني يطابق الشمعة الحالية أو الشمعة السابقة، لضمان عرض الرموز التي لم تشهد حدثًا فوريًا عند لحظة المسح.

## قائمة التحقق (Coverage 99.99%)

| الحزمة | المدخلات | المتغيرات | المصفوفات | الدوال | التنبيهات | العناصر المرسومة |
|--------|----------|-----------|-----------|--------|-----------|--------------------|
| Pullback | 3 | 6 | 4 | 3 | 0 | 0 |
| Market Structure | 6 | 18 | 12 | 10 | 0 | 0 |
| Order Block | 18 | 22 | 16 | 12 | 0 | 0 |
| SCOB | 3 | 5 | 4 | 4 | 0 | 0 |


## الإعدادات الكاملة
- عدد الشموع المحللة: 0
- candle.colorISB: color.rgb(187, 6, 247, 77)
- candle.colorOSB_down: #da781d
- candle.colorOSB_up: #0b3ff9
- candle.label_color_bearish: color.rgb(255, 82, 82, 90)
- candle.label_color_bullish: color.rgb(33, 149, 243, 90)
- candle.showISB: False
- candle.showOSB: False
- candle.trendRule: SMA50
- console.max_age_bars: 0
- demand_supply.i_tf_ob: 
- demand_supply.i_tf_ob_mtf: 240
- demand_supply.ibear_ob_css: #ef3a3a19
- demand_supply.ibear_ob_css_2: color.new(#5d606b, 25)
- demand_supply.ibull_ob_css: #5f6b5d19
- demand_supply.ibull_ob_css_2: color.new(#5d606b, 25)
- demand_supply.iob_showlast: 5
- demand_supply.length_extend_ob: 20
- demand_supply.length_extend_ob_mtf: 20
- demand_supply.line_style_ob_1: line.style_solid
- demand_supply.line_style_ob_2: line.style_solid
- demand_supply.max_obs: 8
- demand_supply.max_obs_mtf: 4
- demand_supply.max_width_ob: 3.0
- demand_supply.mittigation_filt: wick
- demand_supply.mittigation_filt_mtf: Wicks
- demand_supply.ob_extend: False
- demand_supply.ob_extend_mtf: False
- demand_supply.ob_loockback: 10
- demand_supply.ob_showlast: 5
- demand_supply.ob_text_color_1: color.new(#787b86, 0)
- demand_supply.ob_text_color_2: color.new(#787b86, 0)
- demand_supply.ob_type__: All
- demand_supply.ob_type__mtf: All
- demand_supply.overlapping_filt: True
- demand_supply.overlapping_filt_mtf: True
- demand_supply.percent_text: False
- demand_supply.percent_text_2: False
- demand_supply.show_line_ob_1: False
- demand_supply.show_line_ob_2: False
- demand_supply.show_order_blocks: False
- demand_supply.show_order_blocks_mtf: False
- demand_supply.style: Colored
- demand_supply.text_size_ob_: size.normal
- demand_supply.text_size_ob_2: size.small
- demand_supply.v_buy: #00dbff4d
- demand_supply.v_lookback: 10
- demand_supply.v_sell: #e91e634d
- demand_supply.volume_text: False
- demand_supply.volume_text_2: False
- fvg.fvg_color_fill: True
- fvg.fvg_extend: False
- fvg.fvg_extend_B: True
- fvg.fvg_shade_fill: False
- fvg.i_bearishfvgcolor: color.new(color.green,90)
- fvg.i_bullishfvgcolor: color.new(color.green,100)
- fvg.i_deleteonfill: True
- fvg.i_fillByMid: True
- fvg.i_midPointColor: color.rgb(249, 250, 253, 99)
- fvg.i_mtf: HTF
- fvg.i_mtfbearishfvgcolor: color.yellow
- fvg.i_mtfbullishfvgcolor: color.yellow
- fvg.i_mtfos: 50
- fvg.i_textColor: color.white
- fvg.i_tf: 
- fvg.i_tfos: 10
- fvg.length_extend: 20
- fvg.max_fvg: 8
- fvg.max_width_fvg: 1.5
- fvg.mid_style: Solid
- fvg.mittigation_filt_fvg: Touch
- fvg.remove_small: True
- fvg.show_fvg: False
- ict_structure.bosColor1: color.green
- ict_structure.bosColor2: color.red
- ict_structure.eq_bear_color: #787b86
- ict_structure.eq_bull_color: #787b86
- ict_structure.eq_threshold: 0.3
- ict_structure.label_sizes_s: Medium
- ict_structure.ms_type: All
- ict_structure.showSwing: False
- ict_structure.show_equal_highlow: False
- ict_structure.showms: False
- ict_structure.swingSize: 10
- key_levels.Color_4H_Levels: color.orange
- key_levels.Color_Daily_Levels: #08bcd4
- key_levels.Color_Monday_Levels: color.white
- key_levels.MonthlyColor: #098c30
- key_levels.MonthlyTextType: True
- key_levels.Monthly_style: Dotted
- key_levels.QuarterlyTextType: True
- key_levels.Quaterly_style: Dotted
- key_levels.Show_4H_Levels: False
- key_levels.Show_Daily_Levels: False
- key_levels.Show_Monday_Levels: False
- key_levels.Show_Monthly_Levels: False
- key_levels.Show_Quaterly_Levels: False
- key_levels.Show_Weekly_Levels: False
- key_levels.Show_Yearly_Levels: False
- key_levels.Style_4H_Levels: Dotted
- key_levels.Style_Daily_Levels: Dotted
- key_levels.Style_Monday_Levels: Dotted
- key_levels.Text_4H_Levels: True
- key_levels.Text_Daily_Levels: True
- key_levels.Text_Monday_Levels: True
- key_levels.WeeklyColor: #fffcbc
- key_levels.WeeklyTextType: True
- key_levels.Weekly_style: Dotted
- key_levels.YearlyColor: #ffbcdb
- key_levels.YearlyTextType: True
- key_levels.Yearly_style: Dotted
- key_levels.displayStyle: Standard
- key_levels.distanceright: 25
- key_levels.labelsize: Small
- key_levels.linesize: Small
- key_levels.linestyle: Solid
- key_levels.quarterlyColor: #bcffd0
- key_levels.radistance: 250
- liquidity._candleType: Close
- liquidity._highLineStyleHTF: Solid
- liquidity.box_width: 2.5
- liquidity.currentTF: False
- liquidity.displayLimit: 20
- liquidity.displayStyle_liq: Boxes
- liquidity.extentionMax: False
- liquidity.highBoxBorderColorHTF: color.new(#e91e624d,90)
- liquidity.highLineColorHTF: #e91e624d
- liquidity.htfTF: 
- liquidity.leftBars: 20
- liquidity.length_extend_liq: 20
- liquidity.lineWidthHTF: 2
- liquidity.liquidity_text_color: color.black
- liquidity.lowBoxBorderColorHTF: color.new(#00bbf94d,90)
- liquidity.lowLineColorHTF: #00bbf94d
- liquidity.mitiOptions: Remove
- order_block.clrtxtextbear: color.red
- order_block.clrtxtextbearbg: color.rgb(255, 82, 82, 83)
- order_block.clrtxtextbeariem: color.red
- order_block.clrtxtextbeariembg: color.rgb(255, 82, 82, 86)
- order_block.clrtxtextbull: color.green
- order_block.clrtxtextbullbg: color.rgb(76, 175, 79, 86)
- order_block.clrtxtextbulliem: color.green
- order_block.clrtxtextbulliembg: color.rgb(76, 175, 79, 86)
- order_block.colorDemand: #2f825f00
- order_block.colorMitigated: #c0c0c000
- order_block.colorSupply: #cd5c4800
- order_block.extndBox: True
- order_block.poi_type: Mother Bar
- order_block.scobDn: #da781d
- order_block.scobUp: #0b3ff9
- order_block.showBrkob: True
- order_block.showExob: True
- order_block.showIdmob: True
- order_block.showPOI: True
- order_block.showSCOB: True
- order_block.txtsiz: size.auto
- order_flow.ClrMajorOFBear: color.rgb(33, 149, 243, 72)
- order_flow.ClrMajorOFBull: color.rgb(33, 149, 243, 71)
- order_flow.ClrMinorOFBear: color.rgb(155, 39, 176, 86)
- order_flow.ClrMinorOFBull: color.rgb(155, 39, 176, 81)
- order_flow.clrObBBTated: color.rgb(136, 142, 252, 86)
- order_flow.maxTested: 20
- order_flow.showISOB: True
- order_flow.showISOBMax: 10
- order_flow.showMajoinMiner: False
- order_flow.showMajoinMinerMax: 10
- order_flow.showTsted: False
- pullback.colorHL: #000000
- pullback.showHL: False
- pullback.showMn: False
- sessions.AsiaColor: color.rgb(33, 5, 241)
- sessions.Asiat: 0000-0900
- sessions.LondonColor: color.rgb(15, 13, 13)
- sessions.Londont: 0800-1600
- sessions.SessionTextType: False
- sessions.Short_text_London: True
- sessions.Short_text_NY: True
- sessions.Short_text_TKY: True
- sessions.USColor: color.rgb(190, 8, 236)
- sessions.USt: 1400-2100
- sessions.asia_HL: True
- sessions.asia_OC: True
- sessions.is_londonrange_enabled: False
- sessions.is_tokyorange_enabled: False
- sessions.is_usrange_enabled: False
- sessions.london_HL: True
- sessions.london_OC: True
- sessions.us_HL: True
- sessions.us_OC: True
- structure.bear: color.red
- structure.bull: color.green
- structure.colorIDM: color.rgb(0, 0, 0, 20)
- structure.lengSMC: 40
- structure.showCircleHL: True
- structure.showSMC: True
- structure.structure_type: Choch with IDM
- structure_util.colorSweep: color.gray
- structure_util.isOTE: False
- structure_util.lengMid: 40
- structure_util.lengPdh: 40
- structure_util.lengPdl: 40
- structure_util.markX: False
- structure_util.ote1: 0.78
- structure_util.ote2: 0.61
- structure_util.oteclr: #ff95002b
- structure_util.showMid: True
- structure_util.showPdh: False
- structure_util.showPdl: False
- structure_util.showSw: True
- structure_util.showTP: False
- structure_util.sizGd: size.normal
- support_resistance.avoidFalseBreaks: True
- support_resistance.debug_enabledHistory: True
- support_resistance.debug_labelPivots: None
- support_resistance.debug_lastXResistances: 3
- support_resistance.debug_lastXSupports: 3
- support_resistance.debug_maxHistoryRecords: 10
- support_resistance.debug_pivotLabelText: False
- support_resistance.debug_removeDuplicateRS: True
- support_resistance.debug_showBrokenOnLabel: False
- support_resistance.enableBreakAlerts: True
- support_resistance.enableRetestAlerts: True
- support_resistance.enableZones: False
- support_resistance.expandLines: True
- support_resistance.falseBreakoutVolumeThresholdOpt: 0.3
- support_resistance.inverseBrokenLineColor: True
- support_resistance.labelsAlign: Right
- support_resistance.labelsize: Small
- support_resistance.lineStyle_: ....
- support_resistance.lineWidth: 1
- support_resistance.memoryOptimizatonEnabled: True
- support_resistance.pivotRange: 15
- support_resistance.resistanceColor: #f2364580
- support_resistance.resistanceSupportCount: 3
- support_resistance.showBreaks: True
- support_resistance.showRetests: True
- support_resistance.strength: 1
- support_resistance.supportColor: #08998180
- support_resistance.textColor: #11101051
- support_resistance.timeframe1Enabled: True
- support_resistance.timeframe1_: 
- support_resistance.timeframe2: 240
- support_resistance.timeframe2Enabled: True
- support_resistance.timeframe3: 30
- support_resistance.timeframe3Enabled: False
- support_resistance.zoneWidth: 1
- support_resistance.zoneWidthType: Dynamic
- swing_detection.atr_Len: 500
- swing_detection.bearColor: color.new(color.maroon, 0)
- swing_detection.bearStyle: Dashed
- swing_detection.bearWidth: 1
- swing_detection.bullColor: color.new(color.teal, 0)
- swing_detection.bullStyle: Dashed
- swing_detection.bullWidth: 1
- swing_detection.cooldownPeriod: 10
- swing_detection.display_third: False
- swing_detection.dnCss: #f23645
- swing_detection.length3: 20
- swing_detection.mult: 1.0
- swing_detection.showSwing_: True
- swing_detection.swingClr: color.new(color.orange, 0)
- swing_detection.unbrokenCss: #2157f3
- swing_detection.upCss: #089981
- zigzag.dncol: #2157f3
- zigzag.extend: True
- zigzag.length1: 100
- zigzag.midcol: #ff5d00
- zigzag.show_ext: True
- zigzag.show_labels: True
- zigzag.upcol: #ff1100
