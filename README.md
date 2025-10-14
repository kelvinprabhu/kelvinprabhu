<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Kelvin Prabhu - AI Alchemist 🧙‍♂️</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #0f0f1e 0%, #1a0033 50%, #0f1f2e 100%);
            color: #e0e0e0;
            overflow-x: hidden;
        }

        /* HEADER */
        header {
            background: linear-gradient(90deg, #ff006e, #8338ec, #3a86ff, #fb5607);
            padding: 2rem;
            text-align: center;
            position: relative;
            overflow: hidden;
            box-shadow: 0 0 30px rgba(255, 0, 110, 0.5);
        }

        header::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 200%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.3), transparent);
            animation: shimmer 3s infinite;
        }

        @keyframes shimmer {
            0% { left: -100%; }
            100% { left: 100%; }
        }

        h1 {
            font-size: 3rem;
            margin-bottom: 0.5rem;
            color: white;
            text-shadow: 0 0 20px rgba(0, 0, 0, 0.5);
            position: relative;
            z-index: 1;
        }

        .tagline {
            font-size: 1.3rem;
            color: #fff;
            text-shadow: 0 0 10px rgba(0, 0, 0, 0.3);
            position: relative;
            z-index: 1;
        }

        /* MAIN CONTAINER */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 3rem 2rem;
        }

        /* SECTIONS */
        .section {
            margin-bottom: 3rem;
            animation: fadeIn 0.6s ease-in;
        }

        @keyframes fadeIn {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .section-title {
            font-size: 2rem;
            margin-bottom: 1.5rem;
            background: linear-gradient(90deg, #ff006e, #8338ec, #3a86ff);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            position: relative;
            display: inline-block;
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 0;
            width: 100%;
            height: 3px;
            background: linear-gradient(90deg, #ff006e, #8338ec, #3a86ff);
            border-radius: 2px;
        }

        /* SKILLS */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1.5rem;
        }

        .skill-card {
            background: linear-gradient(135deg, rgba(51, 56, 236, 0.2), rgba(255, 0, 110, 0.2));
            border: 2px solid;
            border-image: linear-gradient(135deg, #ff006e, #8338ec, #3a86ff) 1;
            padding: 1.5rem;
            border-radius: 10px;
            cursor: pointer;
            transition: all 0.3s ease;
            backdrop-filter: blur(10px);
        }

        .skill-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 10px 30px rgba(255, 0, 110, 0.3);
            border-image: linear-gradient(135deg, #3a86ff, #fb5607, #ff006e) 1;
        }

        .skill-card h3 {
            color: #3a86ff;
            margin-bottom: 1rem;
            font-size: 1.2rem;
        }

        .skill-card ul {
            list-style: none;
        }

        .skill-card li {
            color: #b0b0b0;
            margin: 0.5rem 0;
            padding-left: 1.5rem;
            position: relative;
        }

        .skill-card li::before {
            content: '⚡';
            position: absolute;
            left: 0;
            color: #fb5607;
        }

        /* PROJECTS */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .project-card {
            background: linear-gradient(135deg, rgba(255, 0, 110, 0.1), rgba(58, 134, 255, 0.1));
            border: 2px solid rgba(255, 0, 110, 0.3);
            padding: 2rem;
            border-radius: 15px;
            transition: all 0.3s ease;
            backdrop-filter: blur(10px);
            position: relative;
            overflow: hidden;
        }

        .project-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 0, 110, 0.2), transparent);
            transition: left 0.5s ease;
        }

        .project-card:hover::before {
            left: 100%;
        }

        .project-card:hover {
            transform: translateY(-15px);
            border-color: #3a86ff;
            box-shadow: 0 15px 40px rgba(58, 134, 255, 0.4);
        }

        .project-title {
            font-size: 1.4rem;
            color: #ff006e;
            margin-bottom: 0.5rem;
            position: relative;
            z-index: 1;
        }

        .project-desc {
            color: #b0b0b0;
            margin-bottom: 1rem;
            line-height: 1.6;
            position: relative;
            z-index: 1;
        }

        .tech-stack {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
            margin-top: 1rem;
            position: relative;
            z-index: 1;
        }

        .tech-tag {
            background: linear-gradient(135deg, #8338ec, #3a86ff);
            color: white;
            padding: 0.3rem 0.8rem;
            border-radius: 20px;
            font-size: 0.85rem;
            font-weight: 500;
        }

        /* FOOTER */
        footer {
            background: linear-gradient(90deg, #1a0033, #0f0f1e, #1a0033);
            border-top: 2px solid;
            border-image: linear-gradient(90deg, #ff006e, #8338ec, #3a86ff, #fb5607) 1;
            padding: 3rem 2rem;
            text-align: center;
            margin-top: 4rem;
        }

        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
        }

        .footer-text {
            color: #b0b0b0;
            margin-bottom: 1.5rem;
            font-size: 1.1rem;
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            margin-bottom: 2rem;
            flex-wrap: wrap;
        }

        .social-links a {
            color: white;
            text-decoration: none;
            padding: 0.8rem 1.5rem;
            background: linear-gradient(135deg, #ff006e, #8338ec);
            border-radius: 25px;
            transition: all 0.3s ease;
            font-weight: 500;
        }

        .social-links a:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(255, 0, 110, 0.4);
            background: linear-gradient(135deg, #3a86ff, #fb5607);
        }

        .footer-quote {
            color: #8338ec;
            font-style: italic;
            margin-top: 2rem;
            font-size: 1rem;
        }

        .footer-divider {
            height: 2px;
            background: linear-gradient(90deg, transparent, #8338ec, transparent);
            margin: 2rem 0;
        }

        /* EMOJI ANIMATION */
        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-10px); }
        }

        .emoji {
            display: inline-block;
            animation: float 2s ease-in-out infinite;
        }

        /* RESPONSIVE */
        @media (max-width: 768px) {
            h1 {
                font-size: 2rem;
            }

            .tagline {
                font-size: 1rem;
            }

            .section-title {
                font-size: 1.5rem;
            }

            .skills-grid, .projects-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <!-- HEADER -->
    <header>
        <h1>🧙‍♂️ Kelvin Prabhu – AI Alchemist <span class="emoji">🤖</span></h1>
        <p class="tagline">Turning LLMs into Magic ✨ | One Bug at a Time 🐛</p>
    </header>

    <!-- MAIN CONTENT -->
    <div class="container">
        <!-- ABOUT SECTION -->
        <div class="section">
            <h2 class="section-title">🎯 About Me</h2>
            <p style="font-size: 1.1rem; line-height: 1.8; color: #d0d0d0; margin-top: 1rem;">
                Hey! I'm an AI/ML enthusiast who loves building intelligent systems that actually work (most of the time 😅). 
                Currently hunting for opportunities to work with <strong style="color: #ff006e;">LLMs, Agentic AI, and Deep Learning</strong>. 
                I've got hands-on experience with <strong style="color: #3a86ff;">LangChain, LangGraph, CrewAI</strong>, and I'm not afraid of a good reinforcement learning challenge 🚀
            </p>
        </div>

        <!-- SKILLS SECTION -->
        <div class="section">
            <h2 class="section-title">⚙️ Tech Stack</h2>
            <div class="skills-grid">
                <div class="skill-card">
                    <h3>🧠 AI/ML & LLMs</h3>
                    <ul>
                        <li>LangChain, LangGraph, CrewAI</li>
                        <li>PyTorch, TensorFlow</li>
                        <li>HuggingFace Transformers</li>
                        <li>RAG Systems & Vector DBs</li>
                        <li>Reinforcement Learning (Q-Learning)</li>
                    </ul>
                </div>

                <div class="skill-card">
                    <h3>🎨 Computer Vision & Deep Learning</h3>
                    <ul>
                        <li>MediaPipe, OpenCV</li>
                        <li>CNN, BiLSTM, Transformers</li>
                        <li>Pose Detection & Segmentation</li>
                        <li>Multi-modal Learning (CLIP/BLIP)</li>
                        <li>Real-time Processing</li>
                    </ul>
                </div>

                <div class="skill-card">
                    <h3>🌐 Backend & Full-Stack</h3>
                    <ul>
                        <li>Django, FastAPI, Flask</li>
                        <li>React, React Native, Next.js</li>
                        <li>REST APIs, WebSockets</li>
                        <li>Docker & Cloud Deployment</li>
                        <li>AWS, GCP</li>
                    </ul>
                </div>

                <div class="skill-card">
                    <h3>💾 Databases & Storage</h3>
                    <ul>
                        <li>PostgreSQL, MongoDB</li>
                        <li>Vector DBs: Pinecone, ChromaDB</li>
                        <li>Graph DB: Neo4j</li>
                        <li>Firebase, DynamoDB</li>
                        <li>FAISS for Semantic Search</li>
                    </ul>
                </div>

                <div class="skill-card">
                    <h3>📊 Data Science</h3>
                    <ul>
                        <li>pandas, NumPy, scikit-learn</li>
                        <li>EDA & Data Visualization</li>
                        <li>Feature Engineering</li>
                        <li>Power BI, Plotly</li>
                        <li>Statistical Analysis</li>
                    </ul>
                </div>

                <div class="skill-card">
                    <h3>💻 Languages & Tools</h3>
                    <ul>
                        <li>Python (Expert), JavaScript/TypeScript</li>
                        <li>Java, SQL, C/C++</li>
                        <li>Git/GitHub, Postman</li>
                        <li>VS Code, Cursor, Windsurf</li>
                        <li>Linux/MacOS</li>
                    </ul>
                </div>
            </div>
        </div>

        <!-- PROJECTS SECTION -->
        <div class="section">
            <h2 class="section-title">🚀 Projects That Don't Suck</h2>
            <div class="projects-grid">
                <div class="project-card">
                    <div class="project-title">🏋️ Trika.ai</div>
                    <div class="project-desc">
                        AI-powered fitness ecosystem with real-time pose detection, personalized coaching, meditation, and habit tracking.
                    </div>
                    <strong style="color: #3a86ff;">Key Features:</strong>
                    <ul style="margin-top: 0.5rem; color: #b0b0b0; margin-left: 1rem;">
                        <li>🎥 MediaPipe Pose + CNN + BiLSTM (22 workout classes)</li>
                        <li>🤖 RAG-powered fitness coach with conversational memory</li>
                        <li>🧘 AI-guided meditation with custom music generation</li>
                        <li>📊 Google Fitness API integration</li>
                    </ul>
                    <div class="tech-stack">
                        <span class="tech-tag">Next.js</span>
                        <span class="tech-tag">Django</span>
                        <span class="tech-tag">LangChain</span>
                        <span class="tech-tag">MediaPipe</span>
                        <span class="tech-tag">WebSockets</span>
                    </div>
                </div>

                <div class="project-card">
                    <div class="project-title">🌐 Web Owl 2.0</div>
                    <div class="project-desc">
                        Multi-agent RAG system that crawls the web, builds knowledge graphs, and answers questions with context.
                    </div>
                    <strong style="color: #3a86ff;">Key Features:</strong>
                    <ul style="margin-top: 0.5rem; color: #b0b0b0; margin-left: 1rem;">
                        <li>🕷️ Intelligent web crawler with Neo4j KG</li>
                        <li>🧠 Hybrid semantic + graph retrieval</li>
                        <li>💬 Conversational memory & context awareness</li>
                        <li>🎨 Multimodal input handling (CLIP/BLIP)</li>
                    </ul>
                    <div class="tech-stack">
                        <span class="tech-tag">LangChain</span>
                        <span class="tech-tag">LangGraph</span>
                        <span class="tech-tag">Neo4j</span>
                        <span class="tech-tag">FastAPI</span>
                        <span class="tech-tag">VectorDB</span>
                    </div>
                </div>

                <div class="project-card">
                    <div class="project-title">✈️ TripTacticx 2.0</div>
                    <div class="project-desc">
                        AI multi-agent travel planner that orchestrates specialized agents for bookings, stays, food, experiences & budgets.
                    </div>
                    <strong style="color: #3a86ff;">Key Features:</strong>
                    <ul style="margin-top: 0.5rem; color: #b0b0b0; margin-left: 1rem;">
                        <li>🤝 CrewAI-based multi-agent orchestration</li>
                        <li>📅 Real API integration (Booking, Travel, Weather)</li>
                        <li>📄 Auto-generated PDF itineraries</li>
                        <li>📧 Email delivery of trip plans</li>
                    </ul>
                    <div class="tech-stack">
                        <span class="tech-tag">CrewAI</span>
                        <span class="tech-tag">Next.js</span>
                        <span class="tech-tag">FastAPI</span>
                        <span class="tech-tag">APIs</span>
                        <span class="tech-tag">PDF Gen</span>
                    </div>
                </div>

                <div class="project-card">
                    <div class="project-title">🌙 Lunar Rover Navigation</div>
                    <div class="project-desc">
                        Reinforcement learning approach using Q-Learning for terrain-aware lunar rover navigation optimizing energy & safety.
                    </div>
                    <strong style="color: #3a86ff;">Key Features:</strong>
                    <ul style="margin-top: 0.5rem; color: #b0b0b0; margin-left: 1rem;">
                        <li>🎓 Published at IEEE SPACE 2025</li>
                        <li>⚡ Q-Learning policy for optimal pathfinding</li>
                        <li>🔋 Energy-aware navigation algorithms</li>
                        <li>🌍 Terrain classification & avoidance</li>
                    </ul>
                    <div class="tech-stack">
                        <span class="tech-tag">PyTorch</span>
                        <span class="tech-tag">Gym</span>
                        <span class="tech-tag">Q-Learning</span>
                        <span class="tech-tag">Research</span>
                    </div>
                </div>

                <div class="project-card">
                    <div class="project-title">📚 Procedural RAG</div>
                    <div class="project-desc">
                        Multilingual PDF-focused RAG system with voice support for document understanding across multiple languages.
                    </div>
                    <strong style="color: #3a86ff;">Key Features:</strong>
                    <ul style="margin-top: 0.5rem; color: #b0b0b0; margin-left: 1rem;">
                        <li>🌍 Multilingual support (Tamil, Hindi, Bengali)</li>
                        <li>🎤 Voice input/output capabilities</li>
                        <li>📖 PDF scraping & indexing</li>
                        <li>🔍 Semantic search with embeddings</li>
                    </ul>
                    <div class="tech-stack">
                        <span class="tech-tag">LangChain</span>
                        <span class="tech-tag">FastAPI</span>
                        <span class="tech-tag">IndicBERT</span>
                        <span class="tech-tag">Voice</span>
                    </div>
                </div>

                <div class="project-card">
                    <div class="project-title">🏗️ Camp Automation</div>
                    <div class="project-desc">
                        Full-stack production platform integrating WhatsApp, Instagram APIs, and email automation for client communications.
                    </div>
                    <strong style="color: #3a86ff;">Key Features:</strong>
                    <ul style="margin-top: 0.5rem; color: #b0b0b0; margin-left: 1rem;">
                        <li>📱 React Native mobile optimization (-23% latency)</li>
                        <li>📧 WATI WhatsApp & Meta API integration</li>
                        <li>⚡ 99.9% uptime with 1000+ active users</li>
                        <li>🔌 Third-party API orchestration</li>
                    </ul>
                    <div class="tech-stack">
                        <span class="tech-tag">Django</span>
                        <span class="tech-tag">React Native</span>
                        <span class="tech-tag">APIs</span>
                        <span class="tech-tag">AWS</span>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- FOOTER -->
    <footer>
        <div class="footer-content">
            <div class="footer-text">
                🎯 <strong>Actively looking for opportunities</strong> in AI/ML, LLM Applications, GenAI, and Research Roles
            </div>

            <div class="social-links">
                <a href="mailto:kelvinprabhu2071@gmail.com">📧 Email</a>
                <a href="https://linkedin.com/in/a-anto-kelvin-prabhu-48385b25a">💼 LinkedIn</a>
                <a href="https://github.com/kelvinprabhu">🐙 GitHub</a>
                <a href="https://kelvinportfolio2071.netlify.app">🌐 Portfolio</a>
                <a href="https://wa.me/918708687084?text=hey%20kelvin">💬 WhatsApp</a>
            </div>

            <div class="footer-divider"></div>

            <div class="footer-quote">
                "AI isn't magic, it's just code that sometimes looks like magic..." ✨
            </div>
        </div>
    </footer>
</body>
</html>
