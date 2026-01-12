import React, { useState, useRef, useEffect } from 'react';
import { 
  Printer, 
  Type, 
  Bold, 
  Italic, 
  Underline, 
  AlignLeft, 
  AlignCenter, 
  AlignRight, 
  AlignJustify, 
  Heading, 
  Divide, 
  Sigma, 
  Minus,
  Download,
  Settings,
  Grid,
  Undo,
  Redo,
  FileText
} from 'lucide-react';

// --- Default Data ---
const DEFAULT_HEADER = {
  schoolName: "ADARSH PUBLIC SCHOOL",
  examName: "HALF YEARLY EXAMINATION - 2026",
  subject: "MATHEMATICS (गणित)",
  class: "X",
  time: "3 Hrs",
  maxMarks: "80",
};

const MATH_SYMBOLS = ["√", "π", "÷", "×", "≤", "≥", "≠", "∞", "≈", "±", "α", "β", "θ", "°", "²", "³"];

const App = () => {
  // --- State ---
  const [header, setHeader] = useState(DEFAULT_HEADER);
  const [showSettings, setShowSettings] = useState(false);
  const [fontFamily, setFontFamily] = useState("'Noto Serif', serif"); // Best for Exam papers
  const [fontSize, setFontSize] = useState("11pt");
  const [lineHeight, setLineHeight] = useState("1.5");
  const [paperMode, setPaperMode] = useState("split"); // split (2 columns) or full
  
  // Refs for content editable areas
  const leftColRef = useRef(null);
  const rightColRef = useRef(null);
  
  // --- Commands for Rich Text ---
  const execCmd = (command, value = null) => {
    document.execCommand(command, false, value);
    // Keep focus
  };

  const insertSymbol = (symbol) => {
    // Focus needs to be preserved, this inserts at cursor of last active editable
    document.execCommand('insertText', false, symbol);
  };

  const insertMarks = () => {
    const html = `&nbsp;<span style="float: right; font-weight: bold;">[ &nbsp;&nbsp; ]</span>`;
    document.execCommand('insertHTML', false, html);
  };
  
  const insertDottedLine = () => {
    const html = `<div style="border-bottom: 1px dashed #000; margin: 10px 0; width: 100%;"></div>`;
    document.execCommand('insertHTML', false, html);
  };

  const handlePrint = () => {
    window.print();
  };

  // --- Components ---

  const HeaderBlock = () => (
    <div className="w-full border-b-2 border-black mb-4 pb-2 font-serif text-center">
      <h1 className="text-2xl font-bold uppercase tracking-wide">{header.schoolName}</h1>
      <h2 className="text-lg font-semibold mt-1 uppercase">{header.examName}</h2>
      
      <div className="flex justify-between items-end mt-3 text-sm font-bold border-t border-black pt-2 px-2">
        <div className="text-left">
          <p>Class: {header.class}</p>
          <p>Subject: {header.subject}</p>
        </div>
        <div className="text-right">
          <p>Time: {header.time}</p>
          <p>M.M.: {header.maxMarks}</p>
        </div>
      </div>
    </div>
  );

  return (
    <div className="min-h-screen bg-gray-100 flex flex-col font-sans text-gray-900">
      
      {/* --- Style Injection for Fonts & Print --- */}
      <style>{`
        @import url('https://fonts.googleapis.com/css2?family=Noto+Sans:wght@400;700&family=Noto+Serif:ital,wght@0,400;0,700;1,400&family=Poppins:wght@400;600&family=Tiro+Devanagari+Hindi&display=swap');

        body {
          -webkit-print-color-adjust: exact !important;
          print-color-adjust: exact !important;
        }

        /* Editor Styles within the paper */
        .paper-content {
          font-family: ${fontFamily};
          font-size: ${fontSize};
          line-height: ${lineHeight};
          outline: none;
          min-height: 100%;
          text-align: justify;
        }
        
        .paper-content p { margin-bottom: 0.5rem; }
        .paper-content ol { list-style-type: decimal; margin-left: 1.5rem; }
        .paper-content ul { list-style-type: disc; margin-left: 1.5rem; }

        /* Print Specifics - CRITICAL FOR A4 */
        @media print {
          @page {
            size: A4 landscape;
            margin: 0;
          }
          body * {
            visibility: hidden;
          }
          #print-area, #print-area * {
            visibility: visible;
          }
          #print-area {
            position: absolute;
            left: 0;
            top: 0;
            width: 297mm;
            height: 210mm;
            margin: 0;
            padding: 0; /* Let internal padding handle safety zones */
            background: white;
            overflow: hidden; /* Strict A4 limit */
          }
          
          /* Hide UI elements */
          .no-print { display: none !important; }
        }
      `}</style>

      {/* --- Toolbar --- */}
      <div className="bg-white shadow-md border-b sticky top-0 z-50 p-2 no-print">
        <div className="max-w-7xl mx-auto flex flex-wrap items-center gap-2 justify-between">
          
          {/* Logo / Title */}
          <div className="flex items-center gap-2 mr-4">
            <div className="bg-indigo-600 text-white p-1.5 rounded">
              <FileText size={20} />
            </div>
            <span className="font-bold text-gray-700 hidden sm:block">ExamMaker Pro</span>
          </div>

          {/* Formatting Tools */}
          <div className="flex items-center gap-1 bg-gray-50 p-1 rounded-lg border">
            <button onClick={() => execCmd('bold')} className="p-1.5 hover:bg-gray-200 rounded" title="Bold"><Bold size={16}/></button>
            <button onClick={() => execCmd('italic')} className="p-1.5 hover:bg-gray-200 rounded" title="Italic"><Italic size={16}/></button>
            <button onClick={() => execCmd('underline')} className="p-1.5 hover:bg-gray-200 rounded" title="Underline"><Underline size={16}/></button>
            <div className="w-px h-6 bg-gray-300 mx-1"></div>
            <button onClick={() => execCmd('justifyLeft')} className="p-1.5 hover:bg-gray-200 rounded" title="Left"><AlignLeft size={16}/></button>
            <button onClick={() => execCmd('justifyCenter')} className="p-1.5 hover:bg-gray-200 rounded" title="Center"><AlignCenter size={16}/></button>
            <button onClick={() => execCmd('justifyRight')} className="p-1.5 hover:bg-gray-200 rounded" title="Right"><AlignRight size={16}/></button>
            <button onClick={() => execCmd('justifyFull')} className="p-1.5 hover:bg-gray-200 rounded" title="Justify"><AlignJustify size={16}/></button>
          </div>

          {/* Font & Exam Tools */}
          <div className="flex items-center gap-2">
            <select 
              className="p-1.5 border rounded text-sm bg-white" 
              value={fontFamily}
              onChange={(e) => setFontFamily(e.target.value)}
            >
              <option value="'Noto Serif', serif">Times / Serif</option>
              <option value="'Noto Sans', sans-serif">Arial / Sans</option>
              <option value="'Tiro Devanagari Hindi', serif">Hindi (Devanagari)</option>
              <option value="'Poppins', sans-serif">Modern (Poppins)</option>
            </select>

            <select 
              className="p-1.5 border rounded text-sm bg-white w-20"
              value={fontSize}
              onChange={(e) => setFontSize(e.target.value)}
            >
              <option value="9pt">9pt</option>
              <option value="10pt">10pt</option>
              <option value="11pt">11pt</option>
              <option value="12pt">12pt</option>
              <option value="14pt">14pt</option>
            </select>
          </div>

          {/* Insert Tools */}
          <div className="flex items-center gap-1 bg-indigo-50 p-1 rounded-lg border border-indigo-100">
             <button onClick={() => execCmd('superscript')} className="p-1.5 hover:bg-indigo-200 rounded text-xs font-bold" title="Superscript">x²</button>
             <button onClick={() => execCmd('subscript')} className="p-1.5 hover:bg-indigo-200 rounded text-xs font-bold" title="Subscript">x₂</button>
             <button onClick={insertMarks} className="px-2 py-1 bg-white border rounded text-xs hover:bg-gray-50 font-medium text-indigo-700 whitespace-nowrap" title="Insert Marks Box">+ Marks</button>
             <button onClick={insertDottedLine} className="px-2 py-1 bg-white border rounded text-xs hover:bg-gray-50 font-medium text-indigo-700 whitespace-nowrap" title="Insert Line">--- Line</button>
          </div>

          {/* Action Buttons */}
          <div className="flex items-center gap-2">
            <button 
              onClick={() => setShowSettings(!showSettings)} 
              className={`p-2 rounded-full ${showSettings ? 'bg-indigo-100 text-indigo-700' : 'hover:bg-gray-200'}`}
              title="Page Setup"
            >
              <Settings size={20} />
            </button>
            <button 
              onClick={handlePrint} 
              className="flex items-center gap-2 bg-green-600 hover:bg-green-700 text-white px-4 py-2 rounded shadow-sm font-medium transition-colors"
            >
              <Printer size={18} />
              <span>Print / PDF</span>
            </button>
          </div>
        </div>

        {/* Sub-Toolbar: Math Symbols */}
        <div className="max-w-7xl mx-auto flex items-center gap-1 mt-2 overflow-x-auto pb-1 px-1 custom-scrollbar">
            <span className="text-xs font-bold text-gray-500 uppercase mr-2">Math/Symbols:</span>
            {MATH_SYMBOLS.map(sym => (
                <button 
                    key={sym} 
                    onClick={() => insertSymbol(sym)}
                    className="w-7 h-7 flex items-center justify-center border rounded bg-white hover:bg-gray-100 text-sm font-serif"
                >
                    {sym}
                </button>
            ))}
        </div>
      </div>

      {/* --- Settings Modal --- */}
      {showSettings && (
        <div className="fixed inset-0 bg-black/50 z-50 flex items-center justify-center no-print" onClick={() => setShowSettings(false)}>
            <div className="bg-white p-6 rounded-lg shadow-xl w-full max-w-lg" onClick={e => e.stopPropagation()}>
                <h3 className="text-xl font-bold mb-4 flex items-center gap-2">
                    <Settings size={24} /> Paper Settings
                </h3>
                
                <div className="grid grid-cols-2 gap-4 mb-4">
                    <div>
                        <label className="block text-sm font-medium text-gray-700 mb-1">School Name</label>
                        <input type="text" className="w-full border rounded p-2" value={header.schoolName} onChange={e => setHeader({...header, schoolName: e.target.value})} />
                    </div>
                    <div>
                        <label className="block text-sm font-medium text-gray-700 mb-1">Exam Name</label>
                        <input type="text" className="w-full border rounded p-2" value={header.examName} onChange={e => setHeader({...header, examName: e.target.value})} />
                    </div>
                    <div>
                        <label className="block text-sm font-medium text-gray-700 mb-1">Subject</label>
                        <input type="text" className="w-full border rounded p-2" value={header.subject} onChange={e => setHeader({...header, subject: e.target.value})} />
                    </div>
                    <div>
                        <label className="block text-sm font-medium text-gray-700 mb-1">Class</label>
                        <input type="text" className="w-full border rounded p-2" value={header.class} onChange={e => setHeader({...header, class: e.target.value})} />
                    </div>
                    <div>
                        <label className="block text-sm font-medium text-gray-700 mb-1">Time</label>
                        <input type="text" className="w-full border rounded p-2" value={header.time} onChange={e => setHeader({...header, time: e.target.value})} />
                    </div>
                    <div>
                        <label className="block text-sm font-medium text-gray-700 mb-1">Max Marks</label>
                        <input type="text" className="w-full border rounded p-2" value={header.maxMarks} onChange={e => setHeader({...header, maxMarks: e.target.value})} />
                    </div>
                </div>
                
                <div className="flex justify-end pt-4 border-t">
                    <button onClick={() => setShowSettings(false)} className="bg-indigo-600 text-white px-6 py-2 rounded hover:bg-indigo-700">Save & Close</button>
                </div>
            </div>
        </div>
      )}

      {/* --- Main Workspace (The Paper) --- */}
      <div className="flex-1 overflow-auto p-4 md:p-8 flex justify-center bg-gray-200">
        
        {/* THE A4 PAPER CONTAINER */}
        <div 
          id="print-area" 
          className="bg-white shadow-2xl relative grid grid-cols-2 divide-x-2 divide-gray-300 divide-dashed"
          style={{ 
            width: '297mm', 
            height: '210mm',
            padding: '10mm', // Safe printing margins
            boxSizing: 'border-box'
          }}
        >
            {/* Center fold guide (visual only) */}
            <div className="absolute inset-y-0 left-1/2 w-px bg-gray-200 transform -translate-x-1/2 pointer-events-none no-print"></div>

            {/* --- Left Column --- */}
            <div className="h-full flex flex-col px-4 relative">
                {/* Header always on left page top? Or spread? Typically left page top for Question Papers */}
                <HeaderBlock />
                
                <div className="flex-1 relative">
                     <div 
                        ref={leftColRef}
                        contentEditable={true}
                        className="paper-content focus:bg-yellow-50/20 transition-colors"
                        suppressContentEditableWarning={true}
                        spellCheck={false}
                    >
                        <p><strong>Part A - General Knowledge (20 Marks)</strong></p>
                        <p><br/></p>
                        <p><strong>Q1.</strong> Answer the following questions briefly:</p>
                        <p>a) What is the capital of India? <span style={{float:'right', fontWeight:'bold'}}>[ 1 ]</span></p>
                        <p>b) Solve: 2x + 4 = 10 <span style={{float:'right', fontWeight:'bold'}}>[ 1 ]</span></p>
                        <p>c) Define Photosynthesis.</p>
                        <p><br/></p>
                        <p><strong>Q2.</strong> Match the following:</p>
                        <ol>
                            <li>Hydrogen &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; a. Blue Planet</li>
                            <li>Earth &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; b. Gas</li>
                        </ol>
                    </div>
                </div>
                
                <div className="text-center text-xs text-gray-400 mt-2 font-mono">Page 1</div>
            </div>

            {/* --- Right Column --- */}
            <div className="h-full flex flex-col px-4 relative">
                 {/* Only show header on right if user wants, usually exams have continuation on right. Let's keep it blank for content */}
                 <div className="h-8"></div> {/* Spacer to align with text start of left col roughly if needed */}
                 
                 <div className="flex-1 relative">
                    <div 
                        ref={rightColRef}
                        contentEditable={true}
                        className="paper-content focus:bg-yellow-50/20 transition-colors"
                        suppressContentEditableWarning={true}
                        spellCheck={false}
                    >
                        <p><strong>Part B - Mathematics (30 Marks)</strong></p>
                        <p><br/></p>
                        <p><strong>Q3.</strong> Solve the quadratic equation:</p>
                        <p style={{textAlign:'center', margin:'10px 0'}}>x² - 5x + 6 = 0</p>
                        <div style={{borderBottom: '1px dashed #000', margin: '10px 0', width: '100%'}}></div>
                        <p><br/></p>
                        <p><strong>Q4.</strong> Calculate the area of a circle where radius (r) = 7cm. (Use π = 22/7)</p>
                        <p><br/></p>
                        <p><strong>Q5.</strong> हिंदी अनुवाद करें:</p>
                        <p>"Honesty is the best policy."</p>
                        <p>उत्तर: __________________________</p>
                    </div>
                 </div>

                 <div className="text-center text-xs text-gray-400 mt-2 font-mono">Page 2</div>
            </div>

        </div>
      </div>

    </div>
  );
};

export default App;

