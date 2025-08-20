<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cybersecurity Repository - README</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&family=Fira+Code:wght@400;500&display=swap');
        
        body {
            font-family: 'Inter', sans-serif;
            background: linear-gradient(135deg, #0f1419 0%, #1a1f2e 50%, #0f1419 100%);
            color: #e2e8f0;
        }
        
        .code-font {
            font-family: 'Fira Code', monospace;
        }
        
        .glow {
            box-shadow: 0 0 20px rgba(34, 197, 94, 0.3);
        }
        
        .glow-blue {
            box-shadow: 0 0 20px rgba(59, 130, 246, 0.3);
        }
        
        .glow-purple {
            box-shadow: 0 0 20px rgba(147, 51, 234, 0.3);
        }
        
        .glow-red {
            box-shadow: 0 0 20px rgba(239, 68, 68, 0.3);
        }
        
        .card {
            background: rgba(15, 20, 25, 0.8);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(34, 197, 94, 0.2);
            transition: all 0.3s ease;
        }
        
        .card:hover {
            border-color: rgba(34, 197, 94, 0.4);
            transform: translateY(-5px);
        }
        
        .terminal {
            background: #0d1117;
            border: 1px solid #30363d;
            border-radius: 8px;
            overflow: hidden;
        }
        
        .terminal-header {
            background: #161b22;
            padding: 10px 15px;
            border-bottom: 1px solid #30363d;
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        .terminal-dot {
            width: 12px;
            height: 12px;
            border-radius: 50%;
        }
        
        .matrix-bg {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: -1;
            opacity: 0.1;
        }
        
        .badge {
            display: inline-flex;
            align-items: center;
            gap: 6px;
            padding: 4px 12px;
            border-radius: 20px;
            font-size: 0.875rem;
            font-weight: 500;
            transition: all 0.3s ease;
        }
        
        .badge:hover {
            transform: scale(1.05);
        }
        
        .skill-icon {
            transition: all 0.3s ease;
        }
        
        .skill-icon:hover {
            transform: scale(1.2) rotate(5deg);
        }
        
        .pulse {
            animation: pulse 2s infinite;
        }
        
        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
        }
        
        .cyber-grid {
            background-image: 
                linear-gradient(rgba(34, 197, 94, 0.1) 1px, transparent 1px),
                linear-gradient(90deg, rgba(34, 197, 94, 0.1) 1px, transparent 1px);
            background-size: 50px 50px;
        }
        
        .typing-effect {
            border-right: 2px solid #22c55e;
            animation: blink 1s infinite;
        }
        
        @keyframes blink {
            0%, 50% { border-color: #22c55e; }
            51%, 100% { border-color: transparent; }
        }
        
        .neon-text {
            text-shadow: 0 0 10px #22c55e, 0 0 20px #22c55e, 0 0 30px #22c55e;
        }
        
        .progress-bar {
            background: linear-gradient(90deg, #22c55e 0%, #16a34a 100%);
            height: 6px;
            border-radius: 3px;
            transition: width 0.3s ease;
        }
    </style>
</head>
<body class="min-h-screen cyber-grid">
    <!-- Matrix Background Effect -->
    <canvas class="matrix-bg" id="matrix"></canvas>
    
    <div class="container mx-auto px-4 py-8 max-w-6xl">
        <!-- Header Section -->
        <div class="text-center mb-12">
            <div class="flex justify-center mb-6">
                <div class="relative">
                    <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/db33df18-5be4-423d-b866-ce4a341330c6.png" alt="Cybersecurity shield logo with glowing green circuit patterns and digital lock symbol" class="rounded-full glow border-4 border-green-500">
                    <div class="absolute -top-2 -right-2 w-6 h-6 bg-green-500 rounded-full pulse"></div>
                </div>
            </div>
            
            <h1 class="text-5xl font-bold mb-4 neon-text typing-effect" id="title">
                Cybersecurity Repository
            </h1>
            
            <p class="text-xl text-gray-300 mb-6 max-w-3xl mx-auto">
                Bem-vindo ao arsenal definitivo de cibersegurança! Este repositório contém ferramentas, scripts e conhecimentos avançados para profissionais de segurança da informação.
            </p>
            
            <div class="flex justify-center gap-4 flex-wrap">
                <span class="badge bg-green-500/20 text-green-400 border border-green-500/30">
                    <i class="fas fa-shield-alt"></i>
                    Ethical Hacking
                </span>
                <span class="badge bg-blue-500/20 text-blue-400 border border-blue-500/30">
                    <i class="fas fa-bug"></i>
                    Penetration Testing
                </span>
                <span class="badge bg-purple-500/20 text-purple-400 border border-purple-500/30">
                    <i class="fas fa-search"></i>
                    Digital Forensics
                </span>
                <span class="badge bg-red-500/20 text-red-400 border border-red-500/30">
                    <i class="fas fa-exclamation-triangle"></i>
                    Incident Response
                </span>
            </div>
        </div>

        <!-- Statistics Section -->
        <div class="grid grid-cols-1 md:grid-cols-4 gap-6 mb-12">
            <div class="card rounded-lg p-6 text-center glow">
                <i class="fas fa-code text-3xl text-green-400 mb-3"></i>
                <div class="text-2xl font-bold text-white">150+</div>
                <div class="text-gray-400">Scripts & Tools</div>
            </div>
            <div class="card rounded-lg p-6 text-center glow-blue">
                <i class="fas fa-bug text-3xl text-blue-400 mb-3"></i>
                <div class="text-2xl font-bold text-white">50+</div>
                <div class="text-gray-400">Vulnerabilities Found</div>
            </div>
            <div class="card rounded-lg p-6 text-center glow-purple">
                <i class="fas fa-graduation-cap text-3xl text-purple-400 mb-3"></i>
                <div class="text-2xl font-bold text-white">25+</div>
                <div class="text-gray-400">Labs Completed</div>
            </div>
            <div class="card rounded-lg p-6 text-center glow-red">
                <i class="fas fa-trophy text-3xl text-yellow-400 mb-3"></i>
                <div class="text-2xl font-bold text-white">10+</div>
                <div class="text-gray-400">CTF Wins</div>
            </div>
        </div>

        <!-- About Section -->
        <div class="card rounded-lg p-8 mb-12">
            <h2 class="text-3xl font-bold mb-6 text-center">
                <i class="fas fa-info-circle text-green-400 mr-3"></i>
                Sobre o Repositório
            </h2>
            <div class="grid grid-cols-1 lg:grid-cols-2 gap-8">
                <div>
                    <p class="text-gray-300 leading-relaxed mb-4">
                        Este repositório é uma coleção abrangente de recursos, ferramentas e projetos práticos voltados para a área de cibersegurança. Desenvolvido com foco em aprendizado contínuo e aplicação prática.
                    </p>
                    <p class="text-gray-300 leading-relaxed">
                        Aqui você encontrará desde scripts básicos de automação até análises complexas de malware e técnicas avançadas de penetration testing.
                    </p>
                </div>
                <div>
                    <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/7ac559ae-af95-4707-982f-73bb19796bf0.png" alt="Modern cybersecurity operations center with multiple monitors showing network traffic analysis, threat detection dashboards, and security metrics" class="rounded-lg w-full">
                </div>
            </div>
        </div>

        <!-- Focus Areas -->
        <div class="card rounded-lg p-8 mb-12">
            <h2 class="text-3xl font-bold mb-8 text-center">
                <i class="fas fa-crosshairs text-green-400 mr-3"></i>
                Áreas de Especialização
            </h2>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6">
                <div class="bg-gradient-to-br from-green-500/10 to-green-600/10 p-6 rounded-lg border border-green-500/20 hover:border-green-500/40 transition-all">
                    <i class="fas fa-user-ninja text-2xl text-green-400 mb-3"></i>
                    <h3 class="font-semibold mb-2">Ethical Hacking</h3>
                    <p class="text-sm text-gray-400">Técnicas avançadas de penetration testing e análise de vulnerabilidades</p>
                </div>
                <div class="bg-gradient-to-br from-blue-500/10 to-blue-600/10 p-6 rounded-lg border border-blue-500/20 hover:border-blue-500/40 transition-all">
                    <i class="fas fa-network-wired text-2xl text-blue-400 mb-3"></i>
                    <h3 class="font-semibold mb-2">Network Security</h3>
                    <p class="text-sm text-gray-400">Monitoramento e proteção de infraestruturas de rede</p>
                </div>
                <div class="bg-gradient-to-br from-purple-500/10 to-purple-600/10 p-6 rounded-lg border border-purple-500/20 hover:border-purple-500/40 transition-all">
                    <i class="fas fa-search text-2xl text-purple-400 mb-3"></i>
                    <h3 class="font-semibold mb-2">Digital Forensics</h3>
                    <p class="text-sm text-gray-400">Análise forense de sistemas e recuperação de evidências</p>
                </div>
                <div class="bg-gradient-to-br from-red-500/10 to-red-600/10 p-6 rounded-lg border border-red-500/20 hover:border-red-500/40 transition-all">
                    <i class="fas fa-lock text-2xl text-red-400 mb-3"></i>
                    <h3 class="font-semibold mb-2">Cryptography</h3>
                    <p class="text-sm text-gray-400">Implementação e análise de algoritmos criptográficos</p>
                </div>
            </div>
        </div>

        <!-- Repository Structure -->
        <div class="card rounded-lg p-8 mb-12">
            <h2 class="text-3xl font-bold mb-6">
                <i class="fas fa-folder-tree text-green-400 mr-3"></i>
                Estrutura do Repositório
            </h2>
            <div class="terminal">
                <div class="terminal-header">
                    <div class="terminal-dot bg-red-500"></div>
                    <div class="terminal-dot bg-yellow-500"></div>
                    <div class="terminal-dot bg-green-500"></div>
                    <span class="text-gray-400 ml-3 code-font">cybersecurity-repo/</span>
                </div>
                <div class="p-6 code-font text-sm">
                    <div class="space-y-2">
                        <div class="flex items-center"><i class="fas fa-folder text-blue-400 mr-2"></i> <span class="text-green-400">tools/</span> <span class="text-gray-500 ml-4"># Ferramentas e scripts personalizados</span></div>
                        <div class="flex items-center"><i class="fas fa-folder text-blue-400 mr-2"></i> <span class="text-green-400">documentation/</span> <span class="text-gray-500 ml-4"># Documentações e guias técnicos</span></div>
                        <div class="flex items-center"><i class="fas fa-folder text-blue-400 mr-2"></i> <span class="text-green-400">labs/</span> <span class="text-gray-500 ml-4"># Laboratórios práticos e CTFs</span></div>
                        <div class="flex items-center"><i class="fas fa-folder text-blue-400 mr-2"></i> <span class="text-green-400">reports/</span> <span class="text-gray-500 ml-4"># Relatórios de penetration testing</span></div>
                        <div class="flex items-center"><i class="fas fa-folder text-blue-400 mr-2"></i> <span class="text-green-400">learning/</span> <span class="text-gray-500 ml-4"># Materiais de estudo e certificações</span></div>
                        <div class="flex items-center"><i class="fas fa-folder text-blue-400 mr-2"></i> <span class="text-green-400">incidents/</span> <span class="text-gray-500 ml-4"># Análise de incidentes reais</span></div>
                        <div class="flex items-center"><i class="fas fa-folder text-blue-400 mr-2"></i> <span class="text-green-400">malware/</span> <span class="text-gray-500 ml-4"># Análise de malware e samples</span></div>
                        <div class="flex items-center"><i class="fas fa-folder text-blue-400 mr-2"></i> <span class="text-green-400">automation/</span> <span class="text-gray-500 ml-4"># Scripts de automação de segurança</span></div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Technologies and Tools -->
        <div class="card rounded-lg p-8 mb-12">
            <h2 class="text-3xl font-bold mb-8 text-center">
                <i class="fas fa-tools text-green-400 mr-3"></i>
                Arsenal Tecnológico
            </h2>
            
            <!-- Programming Languages -->
            <div class="mb-8">
                <h3 class="text-xl font-semibold mb-4 text-green-400">Linguagens de Programação</h3>
                <div class="flex flex-wrap gap-3">
                    <div class="skill-icon badge bg-blue-500/20 text-blue-400 border border-blue-500/30">
                        <i class="fab fa-python"></i> Python
                    </div>
                    <div class="skill-icon badge bg-green-500/20 text-green-400 border border-green-500/30">
                        <i class="fas fa-terminal"></i> Bash
                    </div>
                    <div class="skill-icon badge bg-blue-600/20 text-blue-300 border border-blue-600/30">
                        <i class="fas fa-code"></i> PowerShell
                    </div>
                    <div class="skill-icon badge bg-orange-500/20 text-orange-400 border border-orange-500/30">
                        <i class="fab fa-js"></i> JavaScript
                    </div>
                    <div class="skill-icon badge bg-red-500/20 text-red-400 border border-red-500/30">
                        <i class="fas fa-code"></i> C/C++
                    </div>
                </div>
            </div>
            
            <!-- Security Tools -->
            <div class="mb-8">
                <h3 class="text-xl font-semibold mb-4 text-green-400">Ferramentas de Segurança</h3>
                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4">
                    <div class="bg-gray-800/50 p-4 rounded-lg border border-gray-700">
                        <div class="flex items-center mb-2">
                            <i class="fas fa-search text-green-400 mr-2"></i>
                            <span class="font-semibold">Nmap</span>
                        </div>
                        <p class="text-sm text-gray-400">Network Discovery & Scanning</p>
                    </div>
                    <div class="bg-gray-800/50 p-4 rounded-lg border border-gray-700">
                        <div class="flex items-center mb-2">
                            <i class="fas fa-bomb text-red-400 mr-2"></i>
                            <span class="font-semibold">Metasploit</span>
                        </div>
                        <p class="text-sm text-gray-400">Penetration Testing Framework</p>
                    </div>
                    <div class="bg-gray-800/50 p-4 rounded-lg border border-gray-700">
                        <div class="flex items-center mb-2">
                            <i class="fas fa-eye text-blue-400 mr-2"></i>
                            <span class="font-semibold">Wireshark</span>
                        </div>
                        <p class="text-sm text-gray-400">Network Protocol Analyzer</p>
                    </div>
                    <div class="bg-gray-800/50 p-4 rounded-lg border border-gray-700">
                        <div class="flex items-center mb-2">
                            <i class="fas fa-fire text-orange-400 mr-2"></i>
                            <span class="font-semibold">Burp Suite</span>
                        </div>
                        <p class="text-sm text-gray-400">Web Application Security</p>
                    </div>
                    <div class="bg-gray-800/50 p-4 rounded-lg border border-gray-700">
                        <div class="flex items-center mb-2">
                            <i class="fas fa-shield-virus text-purple-400 mr-2"></i>
                            <span class="font-semibold">OWASP ZAP</span>
                        </div>
                        <p class="text-sm text-gray-400">Security Testing Proxy</p>
                    </div>
                    <div class="bg-gray-800/50 p-4 rounded-lg border border-gray-700">
                        <div class="flex items-center mb-2">
                            <i class="fas fa-chart-line text-yellow-400 mr-2"></i>
                            <span class="font-semibold">Splunk</span>
                        </div>
                        <p class="text-sm text-gray-400">SIEM & Log Analysis</p>
                    </div>
                </div>
            </div>
            
            <!-- Operating Systems -->
            <div>
                <h3 class="text-xl font-semibold mb-4 text-green-400">Sistemas Operacionais</h3>
                <div class="flex flex-wrap gap-3">
                    <div class="skill-icon badge bg-red-500/20 text-red-400 border border-red-500/30">
                        <i class="fab fa-linux"></i> Kali Linux
                    </div>
                    <div class="skill-icon badge bg-blue-500/20 text-blue-400 border border-blue-500/30">
                        <i class="fab fa-linux"></i> Parrot Security OS
                    </div>
                    <div class="skill-icon badge bg-blue-600/20 text-blue-300 border border-blue-600/30">
                        <i class="fab fa-windows"></i> Windows Server
                    </div>
                    <div class="skill-icon badge bg-orange-500/20 text-orange-400 border border-orange-500/30">
                        <i class="fab fa-ubuntu"></i> Ubuntu Server
                    </div>
                </div>
            </div>
        </div>

        <!-- Featured Projects -->
        <div class="card rounded-lg p-8 mb-12">
            <h2 class="text-3xl font-bold mb-8 text-center">
                <i class="fas fa-star text-yellow-400 mr-3"></i>
                Projetos em Destaque
            </h2>
            <div class="grid grid-cols-1 lg:grid-cols-3 gap-6">
                <div class="bg-gradient-to-br from-green-500/10 to-emerald-600/10 p-6 rounded-lg border border-green-500/20 hover:border-green-500/40 transition-all">
                    <div class="flex items-center mb-4">
                        <i class="fas fa-search-plus text-2xl text-green-400 mr-3"></i>
                        <h3 class="text-xl font-semibold">Advanced Vulnerability Scanner</h3>
                    </div>
                    <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/5572de5b-fc0a-4b6e-a359-cdda8d1937ed.png" alt="Terminal interface showing vulnerability scan results with color-coded severity levels and detailed CVE information" class="rounded-lg mb-4 w-full">
                    <p class="text-gray-300 mb-4">Scanner automatizado multi-threaded para identificação de vulnerabilidades em aplicações web e APIs.</p>
                    <div class="flex flex-wrap gap-2 mb-4">
                        <span class="text-xs px-2 py-1 bg-blue-500/20 text-blue-400 rounded">Python</span>
                        <span class="text-xs px-2 py-1 bg-green-500/20 text-green-400 rounded">Nmap</span>
                        <span class="text-xs px-2 py-1 bg-purple-500/20 text-purple-400 rounded">REST API</span>
                    </div>
                    <button class="w-full bg-green-500/20 hover:bg-green-500/30 border border-green-500/30 text-green-400 py-2 rounded transition-all">
                        <i class="fab fa-github mr-2"></i>Ver Projeto
                    </button>
                </div>
                
                <div class="bg-gradient-to-br from-blue-500/10 to-blue-600/10 p-6 rounded-lg border border-blue-500/20 hover:border-blue-500/40 transition-all">
                    <div class="flex items-center mb-4">
                        <i class="fas fa-network-wired text-2xl text-blue-400 mr-3"></i>
                        <h3 class="text-xl font-semibold">Network Security Monitor</h3>
                    </div>
                    <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/b0d41524-868a-4d97-bf6d-104336c63cf0.png" alt="Real-time network monitoring dashboard with traffic graphs, intrusion detection alerts, and geographical threat map" class="rounded-lg mb-4 w-full">
                    <p class="text-gray-300 mb-4">Sistema real-time para monitoramento de rede com detecção de intrusões e análise de tráfego suspeito.</p>
                    <div class="flex flex-wrap gap-2 mb-4">
                        <span class="text-xs px-2 py-1 bg-red-500/20 text-red-400 rounded">Wireshark</span>
                        <span class="text-xs px-2 py-1 bg-blue-500/20 text-blue-400 rounded">Snort</span>
                        <span class="text-xs px-2 py-1 bg-green-500/20 text-green-400 rounded">ELK Stack</span>
                    </div>
                    <button class="w-full bg-blue-500/20 hover:bg-blue-500/30 border border-blue-500/30 text-blue-400 py-2 rounded transition-all">
                        <i class="fab fa-github mr-2"></i>Ver Projeto
                    </button>
                </div>
                
                <div class="bg-gradient-to-br from-purple-500/10 to-purple-600/10 p-6 rounded-lg border border-purple-500/20 hover:border-purple-500/40 transition-all">
                    <div class="flex items-center mb-4">
                        <i class="fas fa-lock text-2xl text-purple-400 mr-3"></i>
                        <h3 class="text-xl font-semibold">Malware Analysis Lab</h3>
                    </div>
                    <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/1c436195-728b-4cbf-8555-fbc459cb94de.png" alt="Malware analysis interface showing hexadecimal code, behavioral analysis graphs, and sandboxed execution environment" class="rounded-lg mb-4 w-full">
                    <p class="text-gray-300 mb-4">Ambiente sandboxed para análise segura de malware com ferramentas de reverse engineering.</p>
                    <div class="flex flex-wrap gap-2 mb-4">
                        <span class="text-xs px-2 py-1 bg-purple-500/20 text-purple-400 rounded">IDA Pro</span>
                        <span class="text-xs px-2 py-1 bg-red-500/20 text-red-400 rounded">Ghidra</span>
                        <span class="text-xs px-2 py-1 bg-yellow-500/20 text-yellow-400 rounded">Volatility</span>
                    </div>
                    <button class="w-full bg-purple-500/20 hover:bg-purple-500/30 border border-purple-500/30 text-purple-400 py-2 rounded transition-all">
                        <i class="fab fa-github mr-2"></i>Ver Projeto
                    </button>
                </div>
            </div>
        </div>

        <!-- Certifications Progress -->
        <div class="card rounded-lg p-8 mb-12">
            <h2 class="text-3xl font-bold mb-8 text-center">
                <i class="fas fa-certificate text-yellow-400 mr-3"></i>
                Jornada de Certificações
            </h2>
            <div class="space-y-6">
                <div class="bg-gray-800/50 p-4 rounded-lg">
                    <div class="flex justify-between items-center mb-2">
                        <span class="font-semibold text-green-400">CEH (Certified Ethical Hacker)</span>
                        <span class="text-green-400">100%</span>
                    </div>
                    <div class="w-full bg-gray-700 rounded-full h-2">
                        <div class="progress-bar w-full"></div>
                    </div>
                </div>
                
                <div class="bg-gray-800/50 p-4 rounded-lg">
                    <div class="flex justify-between items-center mb-2">
                        <span class="font-semibold text-blue-400">OSCP (Offensive Security Certified Professional)</span>
                        <span class="text-blue-400">75%</span>
                    </div>
                    <div class="w-full bg-gray-700 rounded-full h-2">
                        <div class="progress-bar w-3/4 bg-gradient-to-r from-blue-500 to-blue-600"></div>
                    </div>
                </div>
                
                <div class="bg-gray-800/50 p-4 rounded-lg">
                    <div class="flex justify-between items-center mb-2">
                        <span class="font-semibold text-purple-400">CISSP (Certified Information Systems Security Professional)</span>
                        <span class="text-purple-400">50%</span>
                    </div>
                    <div class="w-full bg-gray-700 rounded-full h-2">
                        <div class="progress-bar w-1/2 bg-gradient-to-r from-purple-500 to-purple-600"></div>
                    </div>
                </div>
                
                <div class="bg-gray-800/50 p-4 rounded-lg">
                    <div class="flex justify-between items-center mb-2">
                        <span class="font-semibold text-red-400">GCIH (GIAC Certified Incident Handler)</span>
                        <span class="text-red-400">25%</span>
                    </div>
                    <div class="w-full bg-gray-700 rounded-full h-2">
                        <div class="progress-bar w-1/4 bg-gradient-to-r from-red-500 to-red-600"></div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Learning Resources -->
        <div class="card rounded-lg p-8 mb-12">
            <h2 class="text-3xl font-bold mb-8 text-center">
                <i class="fas fa-book text-blue-400 mr-3"></i>
                Recursos de Aprendizado
            </h2>
            <div class="grid grid-cols-1 lg:grid-cols-2 gap-8">
                <div>
                    <h3 class="text-xl font-semibold mb-4 text-green-400">Livros Recomendados</h3>
                    <div class="space-y-3">
                        <div class="flex items-center p-3 bg-gray-800/50 rounded-lg">
                            <i class="fas fa-book text-green-400 mr-3"></i>
                            <div>
                                <div class="font-semibold">The Web Application Hacker's Handbook</div>
                                <div class="text-sm text-gray-400">Dafydd Stuttard</div>
                            </div>
                        </div>
                        <div class="flex items-center p-3 bg-gray-800/50 rounded-lg">
                            <i class="fas fa-book text-blue-400 mr-3"></i>
                            <div>
                                <div class="font-semibold">Hacking: The Art of Exploitation</div>
                                <div class="text-sm text-gray-400">Jon Erickson</div>
                            </div>
                        </div>
                        <div class="flex items-center p-3 bg-gray-800/50 rounded-lg">
                            <i class="fas fa-book text-purple-400 mr-3"></i>
                            <div>
                                <div class="font-semibold">The Tangled Web</div>
                                <div class="text-sm text-gray-400">Michal Zalewski</div>
                            </div>
                        </div>
                    </div>
                </div>
                
                <div>
                    <h3 class="text-xl font-semibold mb-4 text-green-400">Plataformas de Prática</h3>
                    <div class="space-y-3">
                        <div class="flex items-center p-3 bg-gray-800/50 rounded-lg hover:bg-gray-700/50 transition-all cursor-pointer">
                            <i class="fas fa-cube text-green-400 mr-3"></i>
                            <div>
                                <div class="font-semibold">HackTheBox</div>
                                <div class="text-sm text-gray-400">Advanced penetration testing labs</div>
                            </div>
                        </div>
                        <div class="flex items-center p-3 bg-gray-800/50 rounded-lg hover:bg-gray-700/50 transition-all cursor-pointer">
                            <i class="fas fa-gamepad text-blue-400 mr-3"></i>
                            <div>
                                <div class="font-semibold">TryHackMe</div>
                                <div class="text-sm text-gray-400">Beginner-friendly cybersecurity challenges</div>
                            </div>
                        </div>
                        <div class="flex items-center p-3 bg-gray-800/50 rounded-lg hover:bg-gray-700/50 transition-all cursor-pointer">
                            <i class="fas fa-server text-purple-400 mr-3"></i>
                            <div>
                                <div class="font-semibold">VulnHub</div>
                                <div class="text-sm text-gray-400">Vulnerable VMs for practice</div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Contact Section -->
        <div class="card rounded-lg p-8 mb-12">
            <h2 class="text-3xl font-bold mb-8 text-center">
                <i class="fas fa-envelope text-green-400 mr-3"></i>
                Conecte-se Comigo
            </h2>
            <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
                <a href="#" class="flex items-center justify-center p-6 bg-blue-500/10 hover:bg-blue-500/20 border border-blue-500/30 rounded-lg transition-all group">
                    <i class="fab fa-linkedin text-3xl text-blue-400 mr-4 group-hover:scale-110 transition-transform"></i>
                    <div>
                        <div class="font-semibold">LinkedIn</div>
                        <div class="text-sm text-gray-400">Conecte-se profissionalmente</div>
                    </div>
                </a>
                
                <a href="#" class="flex items-center justify-center p-6 bg-gray-500/10 hover:bg-gray-500/20 border border-gray-500/30 rounded-lg transition-all group">
                    <i class="fab fa-github text-3xl text-gray-400 mr-4 group-hover:scale-110 transition-transform"></i>
                    <div>
                        <div class="font-semibold">GitHub</div>
                        <div class="text-sm text-gray-400">Veja meus repositórios</div>
                    </div>
                </a>
                
                <a href="#" class="flex items-center justify-center p-6 bg-green-500/10 hover:bg-green-500/20 border border-green-500/30 rounded-lg transition-all group">
                    <i class="fas fa-envelope text-3xl text-green-400 mr-4 group-hover:scale-110 transition-transform"></i>
                    <div>
                        <div class="font-semibold">Email</div>
                        <div class="text-sm text-gray-400">Entre em contato direto</div>
                    </div>
                </a>
            </div>
        </div>

        <!-- Disclaimer -->
        <div class="card rounded-lg p-8 mb-12 border-red-500/20">
            <div class="flex items-center mb-4">
                <i class="fas fa-exclamation-triangle text-3xl text-red-400 mr-4"></i>
                <h2 class="text-2xl font-bold text-red-400">Aviso Legal Importante</h2>
            </div>
            <div class="bg-red-500/10 p-4 rounded-lg border border-red-500/20">
                <p class="text-gray-300 leading-relaxed">
                    <strong class="text-red-400">ATENÇÃO:</strong> Todos os conteúdos, ferramentas e técnicas apresentadas neste repositório são destinados exclusivamente para fins educacionais, pesquisa em segurança e testes autorizados. O uso inadequado dessas informações pode ser ilegal. Sempre obtenha autorização adequada e por escrito antes de realizar qualquer teste de segurança. O autor não se responsabiliza pelo uso indevido das informações aqui contidas.
                </p>
            </div>
        </div>

        <!-- Footer -->
        <footer class="text-center">
            <div class="flex justify-center mb-4">
                <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/00fc852a-b882-41da-b565-470d6c4528fc.png" alt="Visitor counter badge showing current number of repository views in green digital style" class="opacity-80">
            </div>
            <p class="text-gray-400 mb-4">
                Se este repositório foi útil para você, considere dar uma estrela! 
                <i class="fas fa-star text-yellow-400 ml-1"></i>
            </p>
            <p class="text-sm text-gray-500">
                © 2024 Cybersecurity Repository. Construído com paixão por segurança da informação.
            </p>
        </footer>
    </div>

    <script>
        // Matrix Rain Effect
        const canvas = document.getElementById('matrix');
        const ctx = canvas.getContext('2d');

        canvas.width = window.innerWidth;
        canvas.height = window.innerHeight;

        const characters = '01';
        const fontSize = 14;
        const columns = canvas.width / fontSize;

        const drops = [];
        for (let x = 0; x < columns; x++) {
            drops[x] = 1;
        }

        function draw() {
            ctx.fillStyle = 'rgba(15, 20, 25, 0.04)';
            ctx.fillRect(0, 0, canvas.width, canvas.height);

            ctx.fillStyle = '#22c55e';
            ctx.font = fontSize + 'px monospace';

            for (let i = 0; i < drops.length; i++) {
                const text = characters[Math.floor(Math.random() * characters.length)];
                ctx.fillText(text, i * fontSize, drops[i] * fontSize);

                if (drops[i] * fontSize > canvas.height && Math.random() > 0.975) {
                    drops[i] = 0;
                }
                drops[i]++;
            }
        }

        setInterval(draw, 35);

        // Typing Effect for Title
        const title = document.getElementById('title');
        const text = 'Cybersecurity Repository';
        let index = 0;

        function typeWriter() {
            if (index < text.length) {
                title.textContent = text.substring(0, index + 1);
                index++;
                setTimeout(typeWriter, 100);
            }
        }

        // Start typing effect after page loads
        window.addEventListener('load', () => {
            title.textContent = '';
            setTimeout(typeWriter, 1000);
        });

        // Resize canvas when window is resized
        window.addEventListener('resize', () => {
            canvas.width = window.innerWidth;
            canvas.height = window.innerHeight;
        });

        // Add interactive hover effects
        document.querySelectorAll('.card').forEach(card => {
            card.addEventListener('mouseenter', function() {
                this.style.transform = 'translateY(-5px) scale(1.02)';
            });
            
            card.addEventListener('mouseleave', function() {
                this.style.transform = 'translateY(0) scale(1)';
            });
        });

        // Progress bar animation
        const progressBars = document.querySelectorAll('.progress-bar');
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.transform = 'scaleX(1)';
                }
            });
        });

        progressBars.forEach(bar => {
            bar.style.transformOrigin = 'left';
            bar.style.transform = 'scaleX(0)';
            bar.style.transition = 'transform 1s ease-in-out';
            observer.observe(bar);
        });
    </script>
</body>
</html>

