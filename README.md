# rohan
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Code Mentor | Your Personal Programming Guru</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        .mentor-bg {
            background: linear-gradient(135deg, #1e3a8a 0%, #1e40af 50%, #2563eb 100%);
        }
        .card-flip {
            transition: transform 0.6s;
            transform-style: preserve-3d;
        }
        .card-flipped {
            transform: rotateY(180deg);
        }
        .skill-bar {
            transition: width 1s ease-in-out;
        }
        .roadmap-item:hover {
            transform: translateX(5px);
        }
        .avatar-pulse {
            animation: pulse 2s infinite;
        }
        @keyframes pulse {
            0% { box-shadow: 0 0 0 0 rgba(37, 99, 235, 0.7); }
            70% { box-shadow: 0 0 0 10px rgba(37, 99, 235, 0); }
            100% { box-shadow: 0 0 0 0 rgba(37, 99, 235, 0); }
        }
    </style>
</head>
<body class="bg-gray-50 min-h-screen font-sans">
    <!-- Navigation -->
    <nav class="mentor-bg text-white shadow-lg">
        <div class="container mx-auto px-4 py-3 flex justify-between items-center">
            <div class="flex items-center space-x-2">
                <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/7a4d606c-eb03-4de6-85a7-0680a234c4fb.png" alt="Code Mentor logo - a wise owl wearing glasses" class="rounded-full h-10 w-10">
                <span class="text-xl font-bold">Code Mentor</span>
            </div>
            <div class="hidden md:flex space-x-6">
                <a href="#" class="nav-link hover:text-blue-200 transition" data-tab="dashboard">Dashboard</a>
                <a href="#" class="nav-link hover:text-blue-200 transition" data-tab="roadmap">Learning Path</a>
                <a href="#" class="nav-link hover:text-blue-200 transition" data-tab="assessment">Skill Check</a>
                <a href="#" class="nav-link hover:text-blue-200 transition" data-tab="mentor">Mentor AI</a>
                <a href="#" class="nav-link hover:text-blue-200 transition" data-tab="resources">Resources</a>
            </div>
            <button class="md:hidden text-white focus:outline-none" id="mobile-menu-button">
                <i class="fas fa-bars text-2xl"></i>
            </button>
        </div>
    </nav>

    <!-- Mobile Menu -->
    <div class="hidden mentor-bg text-white py-2 px-4 shadow-md" id="mobile-menu">
        <a href="#" class="block py-2 nav-link" data-tab="dashboard">Dashboard</a>
        <a href="#" class="block py-2 nav-link" data-tab="roadmap">Learning Path</a>
        <a href="#" class="block py-2 nav-link" data-tab="assessment">Skill Check</a>
        <a href="#" class="block py-2 nav-link" data-tab="mentor">Mentor AI</a>
        <a href="#" class="block py-2 nav-link" data-tab="resources">Resources</a>
    </div>

    <!-- Main Content -->
    <main class="container mx-auto px-4 py-8">
        <!-- Dashboard Tab -->
        <div id="dashboard" class="tab-content active">
            <section class="mb-12">
                <div class="flex items-start justify-between mb-6">
                    <div>
                        <h1 class="text-3xl font-bold text-gray-800">Welcome Back, Apprentice</h1>
                        <p class="text-gray-600">Your personalized programming learning dashboard</p>
                    </div>
                    <div class="flex items-center bg-blue-50 rounded-full px-4 py-2">
                        <div class="relative">
                            <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/7a4d606c-eb03-4de6-85a7-0680a234c4fb.png" alt="Mentor avatar - wise old programmer with glasses" class="h-12 w-12 rounded-full avatar-pulse">
                            <span class="absolute bottom-0 right-0 h-3 w-3 bg-green-500 rounded-full"></span>
                        </div>
                        <div class="ml-3">
                            <p class="text-sm font-medium text-gray-700">Master Yoda</p>
                            <p class="text-xs text-gray-500">Your Code Mentor</p>
                        </div>
                    </div>
                </div>

                <!-- Progress Overview -->
                <div class="grid grid-cols-1 md:grid-cols-3 gap-6 mb-8">
                    <div class="bg-white p-6 rounded-xl shadow-md">
                        <h3 class="font-bold text-gray-800 mb-3">Current Focus</h3>
                        <div class="flex items-center">
                            <div class="p-2 rounded-full bg-blue-100 text-blue-600 mr-3">
                                <i class="fas fa-project-diagram"></i>
                            </div>
                            <div>
                                <p class="font-medium">Data Structures</p>
                                <p class="text-sm text-gray-500">Linked Lists, Trees, Graphs</p>
                            </div>
                        </div>
                        <div class="mt-4">
                            <div class="flex justify-between text-sm mb-1">
                                <span>Progress</span>
                                <span>42%</span>
                            </div>
                            <div class="w-full bg-gray-200 rounded-full h-2">
                                <div class="skill-bar bg-blue-600 h-2 rounded-full" style="width: 42%"></div>
                            </div>
                        </div>
                    </div>
                    
                    <div class="bg-white p-6 rounded-xl shadow-md">
                        <h3 class="font-bold text-gray-800 mb-3">Next Milestone</h3>
                        <div class="flex items-center">
                            <div class="p-2 rounded-full bg-indigo-100 text-indigo-600 mr-3">
                                <i class="fas fa-flag-checkered"></i>
                            </div>
                            <div>
                                <p class="font-medium">Algorithm Mastery</p>
                                <p class="text-sm text-gray-500">Sorting & Searching</p>
                            </div>
                        </div>
                        <div class="mt-4">
                            <div class="flex justify-between text-sm mb-1">
                                <span>Starts in</span>
                                <span>3 days</span>
                            </div>
                            <div class="w-full bg-gray-200 rounded-full h-2">
                                <div class="skill-bar bg-indigo-600 h-2 rounded-full" style="width: 15%"></div>
                            </div>
                        </div>
                    </div>
                    
                    <div class="bg-white p-6 rounded-xl shadow-md">
                        <h3 class="font-bold text-gray-800 mb-3">Mentor's Note</h3>
                        <div class="flex">
                            <div class="p-2 rounded-full bg-purple-100 text-purple-600 mr-3 flex-shrink-0">
                                <i class="fas fa-quote-left"></i>
                            </div>
                            <p class="text-sm italic text-gray-600">"Remember to practice recursion daily. A programmer who masters recursion can solve any problem."</p>
                        </div>
                        <button class="mt-3 text-sm text-blue-600 hover:text-blue-800 flex items-center">
                            <i class="fas fa-comment-dots mr-1"></i> Ask a follow-up
                        </button>
                    </div>
                </div>

                <!-- Quick Actions -->
                <h2 class="text-2xl font-bold text-gray-800 mb-4">Quick Actions</h2>
                <div class="grid grid-cols-2 md:grid-cols-4 gap-4 mb-8">
                    <a href="#" data-tab="roadmap" class="quick-action-card flex flex-col items-center justify-center p-4 bg-white rounded-xl shadow-md hover:shadow-lg transition">
                        <div class="p-3 rounded-full bg-blue-100 text-blue-600 mb-3">
                            <i class="fas fa-map-marked-alt text-2xl"></i>
                        </div>
                        <span class="font-medium">New Roadmap</span>
                    </a>
                    <a href="#" data-tab="assessment" class="quick-action-card flex flex-col items-center justify-center p-4 bg-white rounded-xl shadow-md hover:shadow-lg transition">
                        <div class="p-3 rounded-full bg-indigo-100 text-indigo-600 mb-3">
                            <i class="fas fa-clipboard-check text-2xl"></i>
                        </div>
                        <span class="font-medium">Skill Test</span>
                    </a>
                    <a href="#" data-tab="mentor" class="quick-action-card flex flex-col items-center justify-center p-4 bg-white rounded-xl shadow-md hover:shadow-lg transition">
                        <div class="p-3 rounded-full bg-purple-100 text-purple-600 mb-3">
                            <i class="fas fa-robot text-2xl"></i>
                        </div>
                        <span class="font-medium">Ask Mentor</span>
                    </a>
                    <a href="#" data-tab="resources" class="quick-action-card flex flex-col items-center justify-center p-4 bg-white rounded-xl shadow-md hover:shadow-lg transition">
                        <div class="p-3 rounded-full bg-green-100 text-green-600 mb-3">
                            <i class="fas fa-book-open text-2xl"></i>
                        </div>
                        <span class="font-medium">Resources</span>
                    </a>
                </div>

                <!-- Today's Tasks -->
                <div class="bg-white rounded-xl shadow-md p-6">
                    <div class="flex justify-between items-center mb-4">
                        <h2 class="text-xl font-bold text-gray-800">Today's Learning Tasks</h2>
                        <button class="text-blue-600 hover:text-blue-800 text-sm font-medium">
                            <i class="fas fa-plus mr-1"></i> Add Task
                        </button>
                    </div>
                    <ul class="space-y-3">
                        <li class="flex items-center p-3 hover:bg-gray-50 rounded-lg transition">
                            <input type="checkbox" class="h-5 w-5 text-blue-600 rounded mr-3">
                            <div class="flex-1">
                                <p class="font-medium">Implement linked list in Python</p>
                                <div class="flex items-center text-xs text-gray-500 mt-1">
                                    <span class="mr-2">Data Structures</span>
                                    <span class="flex items-center">
                                        <i class="fas fa-clock mr-1"></i> 45 mins
                                    </span>
                                </div>
                            </div>
                            <button class="text-gray-400 hover:text-gray-600">
                                <i class="fas fa-ellipsis-v"></i>
                            </button>
                        </li>
                        <li class="flex items-center p-3 hover:bg-gray-50 rounded-lg transition">
                            <input type="checkbox" class="h-5 w-5 text-blue-600 rounded mr-3">
                            <div class="flex-1">
                                <p class="font-medium">Watch recursion tutorial videos</p>
                                <div class="flex items-center text-xs text-gray-500 mt-1">
                                    <span class="mr-2">Algorithms</span>
                                    <span class="flex items-center">
                                        <i class="fas fa-clock mr-1"></i> 1 hour
                                    </span>
                                </div>
                            </div>
                            <button class="text-gray-400 hover:text-gray-600">
                                <i class="fas fa-ellipsis-v"></i>
                            </button>
                        </li>
                        <li class="flex items-center p-3 hover:bg-gray-50 rounded-lg transition">
                            <input type="checkbox" class="h-5 w-5 text-blue-600 rounded mr-3">
                            <div class="flex-1">
                                <p class="font-medium">Complete OOP exercises in Java</p>
                                <div class="flex items-center text-xs text-gray-500 mt-1">
                                    <span class="mr-2">Java</span>
                                    <span class="flex items-center">
                                        <i class="fas fa-clock mr-1"></i> 1.5 hours
                                    </span>
                                </div>
                            </div>
                            <button class="text-gray-400 hover:text-gray-600">
                                <i class="fas fa-ellipsis-v"></i>
                            </button>
                        </li>
                    </ul>
                </div>
            </section>
        </div>

        <!-- Roadmap Tab -->
        <div id="roadmap" class="tab-content hidden">
            <section class="mb-8">
                <div class="flex justify-between items-center mb-6">
                    <h1 class="text-3xl font-bold text-gray-800">Personalized Learning Path</h1>
                    <button id="new-path-btn" class="bg-blue-600 hover:bg-blue-700 text-white px-4 py-2 rounded-lg transition">
                        <i class="fas fa-plus mr-2"></i> New Path
                    </button>
                </div>

                <!-- Path Generator -->
                <div class="bg-white rounded-xl shadow-md p-6 mb-8">
                    <h2 class="text-xl font-bold text-gray-800 mb-4">Create Custom Learning Path</h2>
                    <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-1">Technology</label>
                            <select class="w-full p-2 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-500">
                                <option value="">Select technology</option>
                                <option value="python">Python</option>
                                <option value="java">Java</option>
                                <option value="c">C Programming</option>
                                <option value="javascript">JavaScript</option>
                                <option value="dsa">Data Structures</option>
                                <option value="algo">Algorithms</option>
                                <option value="ai">Generative AI</option>
                                <option value="ml">Machine Learning</option>
                            </select>
                        </div>
                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-1">Current Level</label>
                            <select class="w-full p-2 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-500">
                                <option value="beginner">Beginner</option>
                                <option value="intermediate">Intermediate</option>
                                <option value="advanced">Advanced</option>
                            </select>
                        </div>
                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-1">Time Commitment</label>
                            <select class="w-full p-2 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-500">
                                <option value="casual">Casual (5-10 hrs/week)</option>
                                <option value="regular">Regular (10-20 hrs/week)</option>
                                <option value="intensive">Intensive (20+ hrs/week)</option>
                            </select>
                        </div>
                    </div>
                    <button class="mt-4 bg-blue-600 hover:bg-blue-700 text-white px-4 py-2 rounded-lg transition">
                        Generate Path
                    </button>
                </div>

                <!-- Current Path -->
                <div class="bg-white rounded-xl shadow-md p-6 mb-8">
                    <div class="flex justify-between items-center mb-4">
                        <h2 class="text-xl font-bold text-gray-800">Your Data Structures Mastery Path</h2>
                        <div class="flex items-center">
                            <span class="text-sm text-gray-500 mr-3">Progress: 42%</span>
                            <div class="w-24 bg-gray-200 rounded-full h-2">
                                <div class="skill-bar bg-blue-600 h-2 rounded-full" style="width: 42%"></div>
                            </div>
                        </div>
                    </div>
                    
                    <div class="space-y-6">
                        <!-- Phase 1 -->
                        <div class="roadmap-item border-l-4 border-blue-500 pl-4 py-2 transition">
                            <div class="flex justify-between items-start">
                                <div>
                                    <h3 class="font-bold text-lg text-blue-700">Phase 1: Foundations (2 weeks)</h3>
                                    <p class="text-sm text-gray-500">Master the building blocks of data structures</p>
                                </div>
                                <span class="bg-green-100 text-green-800 text-xs px-2 py-1 rounded-full">Completed</span>
                            </div>
                            <ul class="list-disc pl-5 mt-3 space-y-2">
                                <li class="flex justify-between">
                                    <span>Arrays & ArrayLists</span>
                                    <i class="fas fa-check text-green-500"></i>
                                </li>
                                <li class="flex justify-between">
                                    <span>Stacks & Queues</span>
                                    <i class="fas fa-check text-green-500"></i>
                                </li>
                                <li class="flex justify-between">
                                    <span>Basic Complexity Analysis</span>
                                    <i class="fas fa-check text-green-500"></i>
                                </li>
                            </ul>
                        </div>
                        
                        <!-- Phase 2 -->
                        <div class="roadmap-item border-l-4 border-blue-500 pl-4 py-2 transition">
                            <div class="flex justify-between items-start">
                                <div>
                                    <h3 class="font-bold text-lg text-blue-700">Phase 2: Linear Structures (3 weeks)</h3>
                                    <p class="text-sm text-gray-500">Current focus - 60% complete</p>
                                </div>
                                <span class="bg-yellow-100 text-yellow-800 text-xs px-2 py-1 rounded-full">In Progress</span>
                            </div>
                            <ul class="list-disc pl-5 mt-3 space-y-2">
                                <li class="flex justify-between">
                                    <span>Linked Lists (Singly/Doubly)</span>
                                    <i class="fas fa-check text-green-500"></i>
                                </li>
                                <li class="flex justify-between">
                                    <span>Hash Tables</span>
                                    <div class="flex items-center">
                                        <span class="text-xs text-gray-500 mr-2">2/5 exercises</span>
                                        <div class="w-12 bg-gray-200 rounded-full h-1">
                                            <div class="skill-bar bg-blue-600 h-1 rounded-full" style="width: 40%"></div>
                                        </div>
                                    </div>
                                </li>
                                <li class="flex justify-between">
                                    <span>Advanced Complexity Analysis</span>
                                    <div class="flex items-center">
                                        <span class="text-xs text-gray-500 mr-2">1/3 lessons</span>
                                        <div class="w-12 bg-gray-200 rounded-full h-1">
                                            <div class="skill-bar bg-blue-600 h-1 rounded-full" style="width: 33%"></div>
                                        </div>
                                    </div>
                                </li>
                            </ul>
                        </div>
                        
                        <!-- Phase 3 -->
                        <div class="roadmap-item border-l-4 border-blue-500 pl-4 py-2 transition opacity-60">
                            <div class="flex justify-between items-start">
                                <div>
                                    <h3 class="font-bold text-lg text-blue-700">Phase 3: Non-Linear Structures (4 weeks)</h3>
                                    <p class="text-sm text-gray-500">Starts in 1 week</p>
                                </div>
                                <span class="bg-gray-100 text-gray-800 text-xs px-2 py-1 rounded-full">Upcoming</span>
                            </div>
                            <ul class="list-disc pl-5 mt-3 space-y-2">
                                <li>Trees (Binary, BST, AVL)</li>
                                <li>Graphs (Traversals, Pathfinding)</li>
                                <li>Heaps & Priority Queues</li>
                            </ul>
                        </div>
                    </div>
                </div>

                <!-- Mentor's Recommendations -->
                <div class="bg-white rounded-xl shadow-md p-6">
                    <div class="flex items-center mb-4">
                        <div class="p-2 rounded-full bg-blue-100 text-blue-600 mr-3">
                            <i class="fas fa-lightbulb"></i>
                        </div>
                        <h2 class="text-xl font-bold text-gray-800">Mentor's Focus Recommendations</h2>
                    </div>
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                        <div class="border border-blue-100 bg-blue-50 rounded-lg p-4">
                            <div class="flex items-center mb-2">
                                <div class="p-1 rounded-full bg-blue-200 text-blue-700 mr-2">
                                    <i class="fas fa-exclamation-circle text-sm"></i>
                                </div>
                                <h4 class="font-medium text-blue-800">Priority Focus</h4>
                            </div>
                            <p class="text-sm text-gray-700">Hash Tables implementation - crucial for interview preparation and real-world applications.</p>
                        </div>
                        <div class="border border-purple-100 bg-purple-50 rounded-lg p-4">
                            <div class="flex items-center mb-2">
                                <div class="p-1 rounded-full bg-purple-200 text-purple-700 mr-2">
                                    <i class="fas fa-chart-line text-sm"></i>
                                </div>
                                <h4 class="font-medium text-purple-800">Emerging Trend</h4>
                            </div>
                            <p class="text-sm text-gray-700">Graph algorithms are becoming increasingly important in AI/ML applications.</p>
                        </div>
                    </div>
                </div>
            </section>
        </div>

        <!-- Assessment Tab -->
        <div id="assessment" class="tab-content hidden">
            <section class="mb-8">
                <div class="flex justify-between items-center mb-6">
                    <h1 class="text-3xl font-bold text-gray-800">Skill Assessment</h1>
                    <button class="text-blue-600 hover:text-blue-800 font-medium">
                        <i class="fas fa-history mr-1"></i> View History
                    </button>
                </div>

                <!-- Skill Evaluation -->
                <div class="bg-white rounded-xl shadow-md p-6 mb-8">
                    <h2 class="text-xl font-bold text-gray-800 mb-4">Your Current Skill Profile</h2>
                    <div class="space-y-5">
                        <div>
                            <div class="flex justify-between mb-1">
                                <span class="font-medium">Python Programming</span>
                                <span class="text-sm text-gray-500">Intermediate</span>
                            </div>
                            <div class="w-full bg-gray-200 rounded-full h-2.5">
                                <div class="skill-bar bg-blue-600 h-2.5 rounded-full" style="width: 65%"></div>
                            </div>
                        </div>
                        <div>
                            <div class="flex justify-between mb-1">
                                <span class="font-medium">Java OOP</span>
                                <span class="text-sm text-gray-500">Beginner</span>
                            </div>
                            <div class="w-full bg-gray-200 rounded-full h-2.5">
                                <div class="skill-bar bg-blue-600 h-2.5 rounded-full" style="width: 30%"></div>
                            </div>
                        </div>
                        <div>
                            <div class="flex justify-between mb-1">
                                <span class="font-medium">Data Structures</span>
                                <span class="text-sm text-gray-500">Intermediate</span>
                            </div>
                            <div class="w-full bg-gray-200 rounded-full h-2.5">
                                <div class="skill-bar bg-blue-600 h-2.5 rounded-full" style="width: 55%"></div>
                            </div>
                        </div>
                        <div>
                            <div class="flex justify-between mb-1">
                                <span class="font-medium">Algorithms</span>
                                <span class="text-sm text-gray-500">Beginner</span>
                            </div>
                            <div class="w-full bg-gray-200 rounded-full h-2.5">
                                <div class="skill-bar bg-blue-600 h-2.5 rounded-full" style="width: 40%"></div>
                            </div>
                        </div>
                        <div>
                            <div class="flex justify-between mb-1">
                                <span class="font-medium">C Programming
