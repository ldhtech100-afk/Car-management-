```react
import React, { useState, useEffect, useMemo } from 'react';
import { 
  LayoutColumns, 
  CheckCircle2, 
  Clock, 
  AlertCircle, 
  Plus, 
  Trash2, 
  ChevronRight, 
  BarChart3, 
  Calendar,
  Settings,
  Search,
  Filter,
  MoreVertical
} from 'lucide-react';

const App = () => {
  // State Management
  const [tasks, setTasks] = useState([
    { id: '1', title: 'Design System Update', status: 'In Progress', priority: 'High', dueDate: '2024-06-20', category: 'Design' },
    { id: '2', title: 'API Integration', status: 'To Do', priority: 'Medium', dueDate: '2024-06-25', category: 'Development' },
    { id: '3', title: 'Client Feedback Review', status: 'Done', priority: 'Low', dueDate: '2024-06-15', category: 'Product' },
    { id: '4', title: 'Mobile Optimization', status: 'In Progress', priority: 'High', dueDate: '2024-06-22', category: 'Development' },
  ]);

  const [activeTab, setActiveTab] = useState('board');
  const [isModalOpen, setIsModalOpen] = useState(false);
  const [searchQuery, setSearchQuery] = useState('');
  const [newTask, setNewTask] = useState({ title: '', status: 'To Do', priority: 'Medium', category: 'General' });

  // Filtered Tasks
  const filteredTasks = tasks.filter(t => 
    t.title.toLowerCase().includes(searchQuery.toLowerCase()) ||
    t.category.toLowerCase().includes(searchQuery.toLowerCase())
  );

  // Statistics
  const stats = useMemo(() => {
    const total = tasks.length;
    const completed = tasks.filter(t => t.status === 'Done').length;
    const progress = total === 0 ? 0 : Math.round((completed / total) * 100);
    return { total, completed, progress };
  }, [tasks]);

  // Handlers
  const addTask = (e) => {
    e.preventDefault();
    if (!newTask.title) return;
    const task = {
      ...newTask,
      id: Date.now().toString(),
      dueDate: new Date().toISOString().split('T')[0]
    };
    setTasks([...tasks, task]);
    setNewTask({ title: '', status: 'To Do', priority: 'Medium', category: 'General' });
    setIsModalOpen(false);
  };

  const deleteTask = (id) => {
    setTasks(tasks.filter(t => t.id !== id));
  };

  const updateStatus = (id, newStatus) => {
    setTasks(tasks.map(t => t.id === id ? { ...t, status: newStatus } : t));
  };

  // Sub-components
  const StatusBadge = ({ status }) => {
    const styles = {
      'To Do': 'bg-slate-100 text-slate-700',
      'In Progress': 'bg-blue-100 text-blue-700',
      'Done': 'bg-emerald-100 text-emerald-700'
    };
    return <span className={`px-2 py-1 rounded-md text-xs font-medium ${styles[status]}`}>{status}</span>;
  };

  const PriorityBadge = ({ priority }) => {
    const styles = {
      'High': 'text-red-600',
      'Medium': 'text-amber-600',
      'Low': 'text-blue-600'
    };
    return (
      <span className={`flex items-center gap-1 text-xs font-bold ${styles[priority]}`}>
        <div className={`w-1.5 h-1.5 rounded-full bg-current`} />
        {priority}
      </span>
    );
  };

  return (
    <div className="min-h-screen bg-slate-50 text-slate-900 font-sans">
      {/* Sidebar Navigation */}
      <div className="fixed left-0 top-0 h-full w-20 md:w-64 bg-white border-r border-slate-200 hidden sm:flex flex-col">
        <div className="p-6 flex items-center gap-3">
          <div className="w-8 h-8 bg-indigo-600 rounded-lg flex items-center justify-center text-white font-bold">P</div>
          <span className="font-bold text-xl hidden md:block tracking-tight">ProjectX</span>
        </div>
        
        <nav className="flex-1 px-4 space-y-2 mt-4">
          {[
            { id: 'board', icon: LayoutColumns, label: 'Task Board' },
            { id: 'analytics', icon: BarChart3, label: 'Analytics' },
            { id: 'calendar', icon: Calendar, label: 'Schedule' },
            { id: 'settings', icon: Settings, label: 'Settings' }
          ].map((item) => (
            <button
              key={item.id}
              onClick={() => setActiveTab(item.id)}
              className={`w-full flex items-center gap-3 px-4 py-3 rounded-xl transition-all ${
                activeTab === item.id ? 'bg-indigo-50 text-indigo-700' : 'text-slate-500 hover:bg-slate-50'
              }`}
            >
              <item.icon size={20} />
              <span className="font-medium hidden md:block">{item.label}</span>
            </button>
          ))}
        </nav>
      </div>

      {/* Main Content */}
      <main className="sm:ml-20 md:ml-64 p-4 md:p-8">
        {/* Header */}
        <header className="flex flex-col md:flex-row md:items-center justify-between gap-4 mb-8">
          <div>
            <h1 className="text-2xl md:text-3xl font-bold text-slate-900">Project Overview</h1>
            <p className="text-slate-500 mt-1">Manage your team's workflow and tasks.</p>
          </div>
          <div className="flex items-center gap-3">
            <div className="relative">
              <Search className="absolute left-3 top-1/2 -translate-y-1/2 text-slate-400" size={18} />
              <input 
                type="text" 
                placeholder="Search tasks..."
                className="pl-10 pr-4 py-2 bg-white border border-slate-200 rounded-xl focus:ring-2 focus:ring-indigo-500 outline-none w-full md:w-64 transition-all"
                value={searchQuery}
                onChange={(e) => setSearchQuery(e.target.value)}
              />
            </div>
            <button 
              onClick={() => setIsModalOpen(true)}
              className="bg-indigo-600 hover:bg-indigo-700 text-white px-4 py-2 rounded-xl flex items-center gap-2 font-medium transition-colors shadow-sm"
            >
              <Plus size={20} />
              <span className="hidden sm:inline">New Task</span>
            </button>
          </div>
        </header>

        {/* Stats Grid */}
        <div className="grid grid-cols-1 sm:grid-cols-3 gap-6 mb-8">
          <div className="bg-white p-6 rounded-2xl border border-slate-200 shadow-sm hover:shadow-md transition-shadow">
            <div className="flex items-center justify-between mb-4">
              <div className="p-2 bg-blue-50 text-blue-600 rounded-lg"><Clock size={20} /></div>
              <span className="text-sm font-medium text-slate-400">Total Tasks</span>
            </div>
            <div className="text-3xl font-bold">{stats.total}</div>
          </div>
          <div className="bg-white p-6 rounded-2xl border border-slate-200 shadow-sm hover:shadow-md transition-shadow">
            <div className="flex items-center justify-between mb-4">
              <div className="p-2 bg-emerald-50 text-emerald-600 rounded-lg"><CheckCircle2 size={20} /></div>
              <span className="text-sm font-medium text-slate-400">Completed</span>
            </div>
            <div className="text-3xl font-bold">{stats.completed}</div>
          </div>
          <div className="bg-white p-6 rounded-2xl border border-slate-200 shadow-sm hover:shadow-md transition-shadow">
            <div className="flex items-center justify-between mb-4">
              <div className="p-2 bg-indigo-50 text-indigo-600 rounded-lg"><BarChart3 size={20} /></div>
              <span className="text-sm font-medium text-slate-400">Completion Rate</span>
            </div>
            <div className="flex items-center gap-3">
              <div className="text-3xl font-bold">{stats.progress}%</div>
              <div className="flex-1 h-2 bg-slate-100 rounded-full overflow-hidden">
                <div className="h-full bg-indigo-500 transition-all duration-500" style={{ width: `${stats.progress}%` }} />
              </div>
            </div>
          </div>
        </div>

        {/* Board View */}
        {activeTab === 'board' && (
          <div className="grid grid-cols-1 lg:grid-cols-3 gap-6">
            {['To Do', 'In Progress', 'Done'].map((colStatus) => (
              <div key={colStatus} className="flex flex-col gap-4">
                <div className="flex items-center justify-between px-2">
                  <h3 className="font-semibold text-slate-700 flex items-center gap-2">
                    {colStatus} 
                    <span className="bg-slate-200 text-slate-600 px-2 py-0.5 rounded-full text-xs">
                      {filteredTasks.filter(t => t.status === colStatus).length}
                    </span>
                  </h3>
                  <button className="text-slate-400 hover:text-slate-600"><MoreVertical size={16} /></button>
                </div>
                
                <div className="flex flex-col gap-3 min-h-[200px]">
                  {filteredTasks.filter(t => t.status === colStatus).map(task => (
                    <div 
                      key={task.id} 
                      className="bg-white p-4 rounded-xl border border-slate-200 shadow-sm group hover:border-indigo-300 transition-all cursor-pointer"
                    >
                      <div className="flex justify-between items-start mb-2">
                        <span className="text-[10px] uppercase tracking-wider font-bold text-slate-400">{task.category}</span>
                        <PriorityBadge priority={task.priority} />
                      </div>
                      <h4 className="font-semibold text-slate-800 mb-4">{task.title}</h4>
                      <div className="flex items-center justify-between mt-auto pt-3 border-t border-slate-50">
                        <div className="flex items-center gap-2 text-slate-400">
                          <Calendar size={14} />
                          <span className="text-xs">{task.dueDate}</span>
                        </div>
                        <div className="flex items-center gap-1 opacity-0 group-hover:opacity-100 transition-opacity">
                          <button 
                            onClick={() => deleteTask(task.id)}
                            className="p-1.5 text-slate-400 hover:text-red-500 hover:bg-red-50 rounded-lg"
                          >
                            <Trash2 size={14} />
                          </button>
                          {colStatus !== 'Done' && (
                            <button 
                              onClick={() => updateStatus(task.id, colStatus === 'To Do' ? 'In Progress' : 'Done')}
                              className="p-1.5 text-slate-400 hover:text-indigo-600 hover:bg-indigo-50 rounded-lg"
                            >
                              <ChevronRight size={14} />
                            </button>
                          )}
                        </div>
                      </div>
                    </div>
                  ))}
                  
                  {filteredTasks.filter(t => t.status === colStatus).length === 0 && (
                    <div className="border-2 border-dashed border-slate-200 rounded-xl py-8 flex flex-col items-center justify-center text-slate-400">
                      <p className="text-sm italic">No tasks here</p>
                    </div>
                  )}
                </div>
              </div>
            ))}
          </div>
        )}

        {/* Analytics Placeholder */}
        {activeTab !== 'board' && (
          <div className="bg-white rounded-3xl border border-slate-200 p-12 flex flex-col items-center justify-center text-center">
            <div className="w-20 h-20 bg-slate-50 rounded-full flex items-center justify-center text-slate-300 mb-6">
              <AlertCircle size={40} />
            </div>
            <h2 className="text-xl font-bold mb-2 uppercase tracking-wide">Feature Under Construction</h2>
            <p className="text-slate-500 max-w-sm">The {activeTab} module is coming soon in the next sprint.</p>
          </div>
        )}
      </main>

      {/* New Task Modal */}
      {isModalOpen && (
        <div className="fixed inset-0 bg-slate-900/40 backdrop-blur-sm flex items-center justify-center p-4 z-50">
          <div className="bg-white rounded-3xl w-full max-w-md shadow-2xl overflow-hidden animate-in fade-in zoom-in duration-200">
            <div className="p-6 border-b border-slate-100 flex justify-between items-center bg-indigo-50/50">
              <h2 className="text-xl font-bold text-slate-800">Create New Task</h2>
              <button onClick={() => setIsModalOpen(false)} className="text-slate-400 hover:text-slate-600">✕</button>
            </div>
            <form onSubmit={addTask} className="p-6 space-y-4">
              <div>
                <label className="block text-sm font-semibold text-slate-700 mb-1">Task Title</label>
                <input 
                  autoFocus
                  type="text" 
                  className="w-full px-4 py-3 bg-slate-50 border border-slate-200 rounded-xl focus:ring-2 focus:ring-indigo-500 outline-none transition-all"
                  placeholder="What needs to be done?"
                  value={newTask.title}
                  onChange={(e) => setNewTask({...newTask, title: e.target.value})}
                />
              </div>
              <div className="grid grid-cols-2 gap-4">
                <div>
                  <label className="block text-sm font-semibold text-slate-700 mb-1">Priority</label>
                  <select 
                    className="w-full px-4 py-3 bg-slate-50 border border-slate-200 rounded-xl outline-none"
                    value={newTask.priority}
                    onChange={(e) => setNewTask({...newTask, priority: e.target.value})}
                  >
                    <option>Low</option>
                    <option>Medium</option>
                    <option>High</option>
                  </select>
                </div>
                <div>
                  <label className="block text-sm font-semibold text-slate-700 mb-1">Category</label>
                  <select 
                    className="w-full px-4 py-3 bg-slate-50 border border-slate-200 rounded-xl outline-none"
                    value={newTask.category}
                    onChange={(e) => setNewTask({...newTask, category: e.target.value})}
                  >
                    <option>General</option>
                    <option>Design</option>
                    <option>Development</option>
                    <option>Product</option>
                    <option>Marketing</option>
                  </select>
                </div>
              </div>
              <div className="pt-4 flex gap-3">
                <button 
                  type="button"
                  onClick={() => setIsModalOpen(false)}
                  className="flex-1 px-4 py-3 bg-slate-100 hover:bg-slate-200 text-slate-700 font-bold rounded-xl transition-colors"
                >
                  Cancel
                </button>
                <button 
                  type="submit"
                  className="flex-1 px-4 py-3 bg-indigo-600 hover:bg-indigo-700 text-white font-bold rounded-xl transition-colors shadow-lg shadow-indigo-200"
                >
                  Create Task
                </button>
              </div>
            </form>
          </div>
        </div>
      )}
    </div>
  );
};

export default App;

```
