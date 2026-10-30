import React, { useState } from 'react';
import { 
  BarChart, Bar, XAxis, YAxis, CartesianGrid, Tooltip, Legend, ResponsiveContainer,
  PieChart, Pie, Cell, LabelList
} from 'recharts';
import { Settings, Printer, X, Save } from 'lucide-react';

// --- Initial Data State ---
const initialData = {
  header: {
    title: "รายงานสถานะทางการเงินและผลการดำเนินการ",
    subtitle: "มหาวิทยาลัยนเรศวร ประจำปีงบประมาณ 2569 (สำหรับ 6 เดือน สิ้นสุดวันที่ 31 มีนาคม 2569)"
  },
  kpis: {
    assets: { title: "สินทรัพย์รวม", unit: "(ล้านบาท)", value: "12,456.32", changeText: "▲ +5.64% เทียบกับปีก่อน", changeColor: "text-green-600", note: "สภาพคล่องสูงขึ้นจากเงินฝากประจำ", pillColor: "bg-orange-500" },
    equity: { title: "ส่วนของทุน/หนี้สิน", unit: "(ล้านบาท)", value: "14,402.89", changeText: "", changeColor: "", note: "หนี้สิน 1,036.21 (ทุน 84.4%) หนี้ไม่หมุนเวียนลดลง", pillColor: "bg-gray-600" },
    expenses: { title: "รายจ่ายรวม", unit: "(ล้านบาท)", value: "3,097.07", changeText: "▲ +0.88% (บุคลากร 38.02%)", changeColor: "text-green-600", note: "สัดส่วนหลัก 38.02% คือค่าใช้จ่ายบุคลากร", pillColor: "bg-orange-500" },
    revenue: { title: "รายได้รวม", unit: "(ล้านบาท)", value: "3,546.02", changeText: "▼ -10.35% เทียบกับปีก่อน", changeColor: "text-red-600", note: "รายได้หลักมาจากการขายบริการและงบประมาณ", pillColor: "bg-gray-400" }
  },
  compareChart: {
    title: "กราฟเทียบปี 2568 VS 2569",
    data: [
      { name: 'สินทรัพย์', year69: 12456.32, year68: 12670.50 },
      { name: 'หนี้สิน', year69: 1457.27, year68: 1036.23 },
      { name: 'ส่วนของทุน', year69: 11401.88, year68: 11213.24 },
      { name: 'รายได้', year69: 3946.03, year68: 3908.91 },
      { name: 'ค่าใช้จ่าย', year69: 3097.07, year68: 3076.88 },
    ]
  },
  budgetSummary: {
    title: "การบริหารจัดการงบประมาณ",
    totalValue: "รวม 7,277.393 ล้านบาท",
    pieData: [
      { name: 'แผ่นดิน', value: 35.7, color: '#9ca3af' }, // Gray
      { name: 'รายได้รวม', value: 64.3, color: '#f97316' }, // Orange
    ],
    details: {
      income: {
        title: "รายได้ (งบประมาณ 3,935.682 ล้านบาท)",
        items: ["เงินรับฝาก 728.562 ล้านบาท", "เงินบริจาคโดยมีวัตถุประสงค์ 3.914 ล้านบาท", "เงินกองทุน 8.617 ล้านบาท"]
      },
      land: {
        title: "แผ่นดิน (งบประมาณ 2,584.343 ล้านบาท)",
        items: ["งบกลาง 18.275 ล้านบาท"]
      }
    }
  },
  tables: {
    title: "การบริหารจัดการงบประมาณ (รายจ่ายจริง เทียบกับ งบประมาณ)",
    incomeTable: {
      title: "งบประมาณรายได้ (ภาพรวม 24.79%)",
      rows: [
        { name: 'งบส่วนกลาง', budget: '3,556.88', commit: '-', actual: '1,027.68', percent: 28.89, color: 'bg-orange-500' },
        { name: 'วิทยาศาสตร์ฯ', budget: '876.43', commit: '-', actual: '202.05', percent: 23.03, color: 'bg-orange-500' },
        { name: 'สนับสนุนวิชาการ', budget: '3,287.14', commit: '-', actual: '684.34', percent: 20.82, color: 'bg-orange-500' },
      ],
      note: "*ประสิทธิผลภาพรวมในการใช้งบประมาณร้อยละ 28.39 ยังต่ำกว่าที่ควรเป็น"
    },
    landTable: {
      title: "งบประมาณแผ่นดิน (ภาพรวม 62.61%)",
      rows: [
        { name: 'งบบุคลากร', budget: '2,284.28', commit: '-', actual: '1,430.09', percent: 62.61, color: 'bg-orange-500' },
        { name: 'งบดำเนินงาน', budget: '2,284.28', commit: '-', actual: '1,423.49', percent: 62.32, color: 'bg-orange-500' },
        { name: 'งบรายจ่ายอื่น', budget: '457.83', commit: '-', actual: '184.59', percent: 40.32, color: 'bg-orange-500' },
        { name: 'งบลงทุน', budget: '22.96', commit: '-', actual: '3.78', percent: 17.83, color: 'bg-orange-500' },
      ],
      note: "*ประสิทธิผลภาพรวมในการใช้งบประมาณร้อยละ 28.39 ยังต่ำกว่าที่ควรเป็น"
    }
  },
  efficiencyChart: {
    title: "ประสิทธิภาพการใช้งบประมาณ",
    subtitle: "เปรียบเทียบประมาณการรายรับ กับรายรับจริง (งบประมาณรายได้)",
    data: [
      { name: 'ภาพรวม', expect: 3660.38, actual: 1086.50 },
      { name: 'กลุ่มสนับสนุนฯ', expect: 721.93, actual: 123.82 },
      { name: 'กลุ่มมนุษยศาสตร์ฯ', expect: 300.96, actual: 8.63 },
      { name: 'กลุ่มวิทยาศาสตร์ฯ', expect: 208.59, actual: 25.00 },
      { name: 'กลุ่มวิทย์สุขภาพ', expect: 2437.90, actual: 529.04 },
    ]
  },
  accumulatedIncome: {
    title: "รายได้สะสม 3,116.262 ล้านบาท",
    data: [
      { name: 'กลุ่มสนับสนุน บริหารฯ', value: 689.41, color: '#fcd34d' }, // Yellow-ish
      { name: 'กลุ่มมนุษยศาสตร์ฯ', value: 722.07, color: '#f97316' }, // Orange
      { name: 'กลุ่มวิทยาศาสตร์ฯ', value: 259.77, color: '#fb923c' }, // Lighter Orange
      { name: 'กลุ่มวิทยาศาตร์สุขภาพ', value: 373.60, color: '#b45309' }, // Dark Orange
      { name: 'กองทุนคณะและเงินยืม', value: 894.78, color: '#d1d5db' }, // Light Gray
      { name: 'กองทุนทุนบำรุงรักษฯ', value: 176.63, color: '#9ca3af' }, // Gray
    ]
  }
};

// --- Reusable Pill Container ---
const PillContainer = ({ title, titleColor = "bg-gray-700", children, className = "" }) => (
  <div className={`relative border border-gray-300 rounded-xl pt-6 pb-4 px-4 bg-white ${className}`}>
    <div className={`absolute top-0 left-1/2 -translate-x-1/2 -translate-y-1/2 px-6 py-1.5 rounded-full text-white font-bold text-sm md:text-base whitespace-nowrap shadow-sm ${titleColor}`}>
      {title}
    </div>
    {children}
  </div>
);

export default function App() {
  const [data, setData] = useState(initialData);
  const [isEditing, setIsEditing] = useState(false);
  const [primaryColor, setPrimaryColor] = useState('#f97316'); // เพิ่ม State สำหรับสีหลัก (ค่าเริ่มต้นสีส้ม)

  // --- Handlers for Inputs ---
  const handleKPIChange = (key, field, value) => {
    setData(prev => ({ ...prev, kpis: { ...prev.kpis, [key]: { ...prev.kpis[key], [field]: value } } }));
  };

  const handlePrint = () => window.print();

  return (
    <div className="min-h-screen bg-gray-50 text-gray-800 font-sans print:bg-white print:m-0 pb-10">
      {/* เพิ่ม CSS แบบ Dynamic เพื่อดึงสี primaryColor ไปใช้ทั่วทั้งแอป */}
      <style>{`
        .theme-bg { background-color: ${primaryColor} !important; color: white !important; }
        .theme-text { color: ${primaryColor} !important; }
        .theme-border { border-color: ${primaryColor} !important; }
        .theme-border-l { border-left-color: ${primaryColor} !important; }
        .theme-bg-light { background-color: ${primaryColor}15 !important; } /* สีโปร่งใส 15% */
      `}</style>

      {/* Top Bar / Edit Button (Hidden on Print) */}
      <div className="bg-white shadow-sm p-4 flex justify-between items-center print:hidden sticky top-0 z-50">
        <h1 className="text-lg font-bold text-gray-600">Dynamic Dashboard - Edit Mode</h1>
        <div className="flex gap-2">
          <button onClick={handlePrint} className="flex items-center gap-2 px-4 py-2 bg-gray-100 text-gray-700 rounded-lg hover:bg-gray-200 transition font-medium">
            <Printer size={18} /> พิมพ์รายงาน (PDF)
          </button>
          <button onClick={() => setIsEditing(true)} className="flex items-center gap-2 px-4 py-2 theme-bg rounded-lg hover:opacity-90 transition font-medium shadow-md">
            <Settings size={18} /> ตั้งค่า/แก้ไขข้อมูล
          </button>
        </div>
      </div>

      {/* Main Dashboard Canvas */}
      <div className="max-w-[1200px] mx-auto p-4 md:p-8 print:p-0 print:max-w-full">
        
        {/* Header Section */}
        <div className="text-center mb-10 mt-4">
          <h1 className="text-3xl font-extrabold text-gray-900 mb-2">{data.header.title}</h1>
          <p className="text-gray-600">{data.header.subtitle}</p>
        </div>

        {/* --- ROW 1: KPIs & Comparison Chart --- */}
        <div className="flex flex-col lg:flex-row gap-6 mb-8">
          {/* Left: 4 KPIs (2x2 Grid) */}
          <div className="w-full lg:w-5/12 grid grid-cols-2 gap-x-4 gap-y-8 mt-4">
            {Object.entries(data.kpis).map(([key, kpi]) => (
              <PillContainer key={key} title={<>{kpi.title} <br/><span className="text-xs font-normal">{kpi.unit}</span></>} titleColor={kpi.pillColor === 'bg-orange-500' ? 'theme-bg' : kpi.pillColor} className="text-center flex flex-col justify-center min-h-[140px]">
                <div className="text-3xl font-extrabold mt-2 mb-1">{kpi.value}</div>
                {kpi.changeText && <div className={`text-xs font-bold ${kpi.changeColor}`}>{kpi.changeText}</div>}
                <div className="text-xs text-gray-500 mt-2 leading-tight">{kpi.note}</div>
              </PillContainer>
            ))}
          </div>

          {/* Right: Compare Chart */}
          <div className="w-full lg:w-7/12 mt-4">
            <PillContainer title={data.compareChart.title} titleColor="bg-gray-600" className="h-full min-h-[300px]">
              <div className="flex justify-center gap-4 text-xs font-bold mb-2">
                <span className="flex items-center gap-1"><div className="w-3 h-3 rounded-full theme-bg"></div> 31 มี.ค. 2569</span>
                <span className="flex items-center gap-1"><div className="w-3 h-3 rounded-full bg-gray-400"></div> 31 มี.ค. 2568</span>
              </div>
              <div className="h-[250px] w-full">
                <ResponsiveContainer width="100%" height="100%">
                  <BarChart data={data.compareChart.data} margin={{ top: 10, right: 10, left: -20, bottom: 0 }}>
                    <CartesianGrid strokeDasharray="3 3" vertical={false} />
                    <XAxis dataKey="name" axisLine={true} tickLine={false} tick={{ fontSize: 10, fontWeight: 'bold' }} />
                    <YAxis axisLine={false} tickLine={false} tick={{ fontSize: 10 }} tickFormatter={(val) => val > 0 ? `${val/1000}K` : '0'} />
                    <Tooltip cursor={{fill: '#f3f4f6'}} />
                    <Bar dataKey="year69" fill={primaryColor} radius={[2, 2, 0, 0]} barSize={20} />
                    <Bar dataKey="year68" fill="#9ca3af" radius={[2, 2, 0, 0]} barSize={20} />
                  </BarChart>
                </ResponsiveContainer>
              </div>
            </PillContainer>
          </div>
        </div>

        {/* --- ROW 2: Budget Management --- */}
        <div className="w-full mb-8 mt-10">
          <PillContainer title={data.budgetSummary.title} titleColor="bg-gray-700">
            <h2 className="text-xl font-extrabold text-center mb-4">{data.budgetSummary.totalValue}</h2>
            <div className="flex flex-col md:flex-row items-center">
              
              {/* Pie Chart */}
              <div className="w-full md:w-1/3 h-[200px] relative">
                <ResponsiveContainer width="100%" height="100%">
                  <PieChart>
                    <Pie data={data.budgetSummary.pieData} innerRadius={50} outerRadius={80} dataKey="value" stroke="none">
                      {data.budgetSummary.pieData.map((entry, index) => (
                        <Cell key={`cell-${index}`} fill={entry.color === '#f97316' ? primaryColor : entry.color} />
                      ))}
                    </Pie>
                  </PieChart>
                </ResponsiveContainer>
                {/* Custom Labels to match image exactly */}
                <div className="absolute top-1/2 left-4 -translate-y-1/2 text-center text-sm font-bold text-gray-700">
                  แผ่นดิน<br/>35.7%
                </div>
                <div className="absolute bottom-4 right-10 text-center text-sm font-bold theme-text">
                  รายได้รวม 64.3%
                </div>
              </div>

              {/* Stacked Details Boxes */}
              <div className="w-full md:w-2/3 space-y-4 px-4 pb-4">
                {/* Income Box */}
                <div className="theme-bg-light theme-border border rounded-r-xl border-l-4 theme-border-l p-4">
                  <div className="font-bold theme-text mb-2">{data.budgetSummary.details.income.title}</div>
                  <ul className="list-disc list-inside text-sm text-gray-700 space-y-1">
                    {data.budgetSummary.details.income.items.map((item, i) => <li key={i}>{item}</li>)}
                  </ul>
                </div>
                {/* Land Box */}
                <div className="bg-gray-50 border border-gray-100 rounded-r-xl border-l-4 border-l-gray-400 p-4">
                  <div className="font-bold text-gray-700 mb-2">{data.budgetSummary.details.land.title}</div>
                  <ul className="list-disc list-inside text-sm text-gray-700 space-y-1">
                    {data.budgetSummary.details.land.items.map((item, i) => <li key={i}>{item}</li>)}
                  </ul>
                </div>
              </div>

            </div>
          </PillContainer>
        </div>

        {/* --- ROW 3: Tables & Charts Split --- */}
        <div className="flex flex-col lg:flex-row gap-6 mt-10">
          
          {/* Left Column: Tables Container */}
          <div className="w-full lg:w-1/2">
            <PillContainer title={data.tables.title} titleColor="bg-gray-700">
              
              {/* Income Table */}
              <div className="mb-6">
                <h3 className="text-blue-700 font-bold mb-2">{data.tables.incomeTable.title}</h3>
                <div className="overflow-x-auto">
                  <table className="w-full text-xs text-center border-collapse border border-gray-200">
                    <thead className="bg-gray-50 font-bold">
                      <tr>
                        <th className="border border-gray-200 p-2 text-left">กองทุน / กลุ่ม</th>
                        <th className="border border-gray-200 p-2">งบประมาณ</th>
                        <th className="border border-gray-200 p-2">ผูกพัน</th>
                        <th className="border border-gray-200 p-2">จ่ายจริง</th>
                        <th className="border border-gray-200 p-2">ร้อยละ</th>
                        <th className="border border-gray-200 p-2">มาตรการเร่งรัด</th>
                      </tr>
                    </thead>
                    <tbody>
                      {data.tables.incomeTable.rows.map((row, i) => (
                        <tr key={i}>
                          <td className="border border-gray-200 p-2 text-left font-bold">{row.name}</td>
                          <td className="border border-gray-200 p-2">{row.budget}</td>
                          <td className="border border-gray-200 p-2">{row.commit}</td>
                          <td className="border border-gray-200 p-2 font-bold">{row.actual}</td>
                          <td className="border border-gray-200 p-2 font-bold">
                            <div>{row.percent}</div>
                            <div className="w-full bg-gray-200 h-1.5 mt-1 rounded-full overflow-hidden">
                              <div className={`${row.color === 'bg-orange-500' ? 'theme-bg' : row.color} h-full`} style={{ width: `${row.percent}%` }}></div>
                            </div>
                          </td>
                          <td className="border border-gray-200 p-2"></td>
                        </tr>
                      ))}
                    </tbody>
                  </table>
                </div>
                <div className="text-[10px] text-gray-500 mt-1 italic font-bold">{data.tables.incomeTable.note}</div>
              </div>

              {/* Land Table */}
              <div>
                <h3 className="text-blue-700 font-bold mb-2">{data.tables.landTable.title}</h3>
                <div className="overflow-x-auto">
                  <table className="w-full text-xs text-center border-collapse border border-gray-200">
                    <thead className="bg-gray-50 font-bold">
                      <tr>
                        <th className="border border-gray-200 p-2 text-left">แผนงาน</th>
                        <th className="border border-gray-200 p-2">งบประมาณ</th>
                        <th className="border border-gray-200 p-2">ผูกพัน</th>
                        <th className="border border-gray-200 p-2">จ่ายจริง</th>
                        <th className="border border-gray-200 p-2">ร้อยละ</th>
                        <th className="border border-gray-200 p-2">มาตรการเร่งรัด</th>
                      </tr>
                    </thead>
                    <tbody>
                      {data.tables.landTable.rows.map((row, i) => (
                        <tr key={i}>
                          <td className="border border-gray-200 p-2 text-left font-bold">{row.name}</td>
                          <td className="border border-gray-200 p-2">{row.budget}</td>
                          <td className="border border-gray-200 p-2">{row.commit}</td>
                          <td className="border border-gray-200 p-2 font-bold">{row.actual}</td>
                          <td className="border border-gray-200 p-2 font-bold">
                            <div>{row.percent}</div>
                            <div className="w-full bg-gray-200 h-1.5 mt-1 rounded-full overflow-hidden">
                              <div className={`${row.color === 'bg-orange-500' ? 'theme-bg' : row.color} h-full`} style={{ width: `${row.percent}%` }}></div>
                            </div>
                          </td>
                          <td className="border border-gray-200 p-2"></td>
                        </tr>
                      ))}
                    </tbody>
                  </table>
                </div>
                <div className="text-[10px] text-gray-500 mt-1 italic font-bold">{data.tables.landTable.note}</div>
              </div>

            </PillContainer>
          </div>

          {/* Right Column: 2 Stacked Charts */}
          <div className="w-full lg:w-1/2 flex flex-col gap-10">
            
            {/* Efficiency Chart */}
            <PillContainer title={data.efficiencyChart.title} titleColor="bg-gray-700" className="flex-1">
              <div className="text-center text-xs font-bold text-gray-600 mb-4">{data.efficiencyChart.subtitle}</div>
              <div className="h-[200px] w-full">
                <ResponsiveContainer width="100%" height="100%">
                  <BarChart data={data.efficiencyChart.data} margin={{ top: 15, right: 5, left: -25, bottom: 20 }}>
                    <CartesianGrid strokeDasharray="3 3" vertical={false} />
                    <XAxis dataKey="name" axisLine={true} tickLine={false} tick={{ fontSize: 9, fontWeight: 'bold' }} interval={0} />
                    <YAxis axisLine={false} tickLine={false} tick={{ fontSize: 10 }} />
                    <Tooltip cursor={{fill: '#f3f4f6'}} />
                    <Bar dataKey="expect" fill="#fcd34d" barSize={25}>
                       <LabelList dataKey="expect" position="top" style={{fontSize: '9px', fontWeight: 'bold', fill: '#d97706'}} />
                    </Bar>
                    <Bar dataKey="actual" fill="#ea580c" barSize={25}>
                       <LabelList dataKey="actual" position="top" style={{fontSize: '9px', fontWeight: 'bold', fill: '#ea580c'}} />
                    </Bar>
                  </BarChart>
                </ResponsiveContainer>
              </div>
            </PillContainer>

            {/* Accumulated Income Chart (Horizontal) */}
            <PillContainer title={data.accumulatedIncome.title} titleColor="bg-gray-700" className="flex-1">
              <div className="h-[200px] w-full mt-2">
                <ResponsiveContainer width="100%" height="100%">
                  <BarChart data={data.accumulatedIncome.data} layout="vertical" margin={{ top: 0, right: 30, left: 20, bottom: 0 }}>
                    <XAxis type="number" axisLine={true} tickLine={false} tick={{ fontSize: 10 }} domain={[0, 1000]} />
                    <YAxis type="category" dataKey="name" axisLine={true} tickLine={false} tick={{ fontSize: 9, fontWeight: 'bold' }} width={120} />
                    <Tooltip cursor={{fill: '#f3f4f6'}} />
                    <Bar dataKey="value" barSize={12} radius={[0, 4, 4, 0]}>
                      {data.accumulatedIncome.data.map((entry, index) => (
                        <Cell key={`cell-${index}`} fill={entry.color === '#f97316' ? primaryColor : entry.color} />
                      ))}
                      <LabelList dataKey="value" position="right" style={{fontSize: '10px', fontWeight: 'bold'}} />
                    </Bar>
                  </BarChart>
                </ResponsiveContainer>
              </div>
            </PillContainer>

          </div>
        </div>

      </div>

      {/* --- EDIT MODE MODAL --- */}
      {isEditing && (
        <div className="fixed inset-0 bg-black/60 z-[100] flex justify-center items-start overflow-y-auto p-4 md:p-10">
          <div className="bg-white rounded-2xl shadow-2xl w-full max-w-4xl relative animate-in zoom-in-95 duration-200">
            {/* Modal Header */}
            <div className="sticky top-0 bg-white border-b p-4 px-6 rounded-t-2xl flex justify-between items-center z-10">
              <h2 className="text-xl font-bold flex items-center gap-2"><Settings className="theme-text"/> ตั้งค่าข้อมูลและสีแดชบอร์ด</h2>
              <div className="flex gap-2">
                <button onClick={() => setIsEditing(false)} className="flex items-center gap-1 px-4 py-2 theme-bg rounded-lg hover:opacity-90 font-bold text-sm text-white">
                  <Save size={16} /> บันทึกและปิด
                </button>
              </div>
            </div>

            {/* Modal Body */}
            <div className="p-6 space-y-8">
              
              {/* Color Picker Section */}
              <section>
                <div className="flex items-center gap-2 mb-4 border-b pb-2">
                  <div className="w-8 h-8 rounded-full theme-bg-light flex items-center justify-center theme-text font-bold">🎨</div>
                  <h3 className="font-bold text-lg">ปรับแต่งสี (Theme Color)</h3>
                </div>
                <div className="flex items-center gap-4 p-4 border rounded-xl bg-gray-50">
                   <label className="font-bold text-gray-700">สีหลักของรายงาน:</label>
                   <input 
                     type="color" 
                     value={primaryColor}
                     onChange={(e) => setPrimaryColor(e.target.value)}
                     className="w-12 h-12 rounded cursor-pointer border-0 p-0 bg-transparent"
                   />
                   <span className="text-gray-500 text-sm">คลิกที่กล่องสีเพื่อเลือกสีใหม่ กราฟและป้ายกำกับจะเปลี่ยนสีตามทันที</span>
                </div>
              </section>

              {/* KPIs Edit Section */}
              <section>
                <div className="flex items-center gap-2 mb-4 border-b pb-2">
                  <div className="w-8 h-8 rounded-full theme-bg-light flex items-center justify-center theme-text font-bold">1</div>
                  <h3 className="font-bold text-lg">แก้ไขข้อผิดพลาด (KPIs)</h3>
                </div>
                <div className="grid grid-cols-1 md:grid-cols-2 gap-4">
                  {Object.entries(data.kpis).map(([key, kpi]) => (
                    <div key={key} className="p-4 border rounded-xl bg-gray-50 space-y-3">
                      <div className="font-bold text-gray-700 bg-gray-200 inline-block px-3 py-1 rounded-md text-sm">{kpi.title}</div>
                      <div>
                        <label className="text-xs font-bold text-gray-500">ตัวเลขหลัก</label>
                        <input type="text" value={kpi.value} onChange={(e) => handleKPIChange(key, 'value', e.target.value)} className="w-full border p-2 rounded mt-1 focus:ring-2 focus:ring-orange-500 outline-none" />
                      </div>
                      <div className="grid grid-cols-2 gap-2">
                        <div>
                          <label className="text-xs font-bold text-gray-500">ข้อความเปอร์เซ็นต์ (ถ้ามี)</label>
                          <input type="text" value={kpi.changeText} onChange={(e) => handleKPIChange(key, 'changeText', e.target.value)} className="w-full border p-2 rounded mt-1 text-sm outline-none" />
                        </div>
                        <div>
                          <label className="text-xs font-bold text-gray-500">สีข้อความเปอร์เซ็นต์</label>
                          <select value={kpi.changeColor} onChange={(e) => handleKPIChange(key, 'changeColor', e.target.value)} className="w-full border p-2 rounded mt-1 text-sm outline-none">
                            <option value="text-green-600">สีเขียว (บวก)</option>
                            <option value="text-red-600">สีแดง (ลบ)</option>
                            <option value="">ไม่มีสี (ว่าง)</option>
                          </select>
                        </div>
                      </div>
                      <div>
                        <label className="text-xs font-bold text-gray-500">คำอธิบายเพิ่มเติม</label>
                        <input type="text" value={kpi.note} onChange={(e) => handleKPIChange(key, 'note', e.target.value)} className="w-full border p-2 rounded mt-1 text-sm outline-none" />
                      </div>
                    </div>
                  ))}
                </div>
              </section>

              {/* Chart Data Edit Preview Message */}
              <section>
                <div className="flex items-center gap-2 mb-4 border-b pb-2">
                  <div className="w-8 h-8 rounded-full bg-gray-200 flex items-center justify-center text-gray-600 font-bold">2</div>
                  <h3 className="font-bold text-lg">ตารางและกราฟ (Charts & Tables)</h3>
                </div>
                <div className="bg-blue-50 border border-blue-200 text-blue-800 p-4 rounded-xl text-sm flex gap-3 items-start">
                  <div>ℹ️</div>
                  <div>
                    <strong>คำแนะนำสำหรับผู้ดูแลระบบ:</strong> ในโหมดสาธิตนี้ ระบบได้เชื่อมโยงการเปลี่ยนค่าของกล่องสรุป KPI ไว้ให้แล้ว หากต้องการแก้ไขข้อมูลตารางและกราฟแบบละเอียด 
                    คุณสามารถแก้ไขตรงใน State (Object <code>initialData</code>) ของโค้ด หรือเชื่อมต่อกับระบบฐานข้อมูล Backend API / Excel Upload ในขั้นตอนต่อไปได้อย่างง่ายดาย เนื่องจากโครงสร้างข้อมูลถูกจัดเตรียมไว้เป็น JSON แล้ว
                  </div>
                </div>
              </section>

            </div>
          </div>
        </div>
      )}

    </div>
  );
}
