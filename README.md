<style>
  @keyframes fadeInUp {
    from {
      opacity: 0;
      transform: translateY(40px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }

  @keyframes neonPulse {
    0% { text-shadow: 0 0 8px #00f7ff, 0 0 16px #00f7ff; }
    50% { text-shadow: 0 0 20px #00f7ff, 0 0 32px #00f7ff, 0 0 45px #00f7ff; }
    100% { text-shadow: 0 0 8px #00f7ff, 0 0 16px #00f7ff; }
  }

  @keyframes typing {
    from { width: 0 }
    to { width: 100% }
  }

  @keyframes blink {
    50% { border-color: transparent; }
  }

  @keyframes shine {
    100% { transform: translateX(300%); }
  }

  .about-hero {
    text-align: center;
    margin: 60px 0 40px 0;
    animation: fadeInUp 1.2s ease forwards;
  }

  .typewriter {
    display: inline-block;
    overflow: hidden;
    border-right: 4px solid #00f7ff;
    white-space: nowrap;
    font-size: 2.6rem;
    font-weight: 900;
    color: #00f7ff;
    font-family: 'Segoe UI', system-ui, sans-serif;
    animation: 
      typing 3s steps(26, end) forwards,
      blink 0.8s step-end infinite;
    padding-right: 8px;
    letter-spacing: -1px;
  }

  .section-title {
    text-align: center;
    font-size: 2.1rem;
    margin: 50px 0 35px 0;
    color: #ffffff;
    animation: neonPulse 3s ease infinite;
    letter-spacing: 3px;
    font-family: 'Segoe UI', system-ui, sans-serif;
  }

  /* TIGHT 2-COLUMN GRID - no empty space beside cards */
  .cards-container {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 28px;
    max-width: 820px;
    margin: 0 auto;
  }

  .card {
    background: linear-gradient(145deg, #0f172a, #1e2937);
    border: 2px solid rgba(0, 247, 255, 0.3);
    border-radius: 24px;
    padding: 34px 30px;
    box-shadow: 0 15px 35px -10px rgba(0, 247, 255, 0.25);
    transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
    animation: fadeInUp 0.9s ease forwards;
    position: relative;
    overflow: hidden;
    height: 100%;
  }

  .card::before {
    content: '';
    position: absolute;
    top: -50%;
    left: -50%;
    width: 40%;
    height: 300%;
    background: linear-gradient(
      120deg,
      transparent,
      rgba(255,255,255,0.18),
      transparent
    );
    transform: skewX(-25deg);
    animation: shine 5s linear infinite;
  }

  .card:hover {
    transform: scale(1.07) translateY(-14px);
    box-shadow: 0 28px 55px -12px rgba(0, 247, 255, 0.55);
    border-color: #00f7ff;
  }

  .card h3 {
    font-size: 1.65rem;
    margin-bottom: 24px;
    color: #00f7ff;
    display: flex;
    align-items: center;
    gap: 14px;
    text-shadow: 0 0 14px #00f7ff;
    font-family: 'Segoe UI', system-ui, sans-serif;
  }

  .card-content {
    color: #e2e8f0;
    line-height: 1.85;
    font-size: 1.08rem;
    font-family: 'Segoe UI', system-ui, sans-serif;
  }

  .card-content ul {
    list-style: none;
    padding: 0;
    margin: 0;
  }

  .card-content li {
    margin-bottom: 14px;
    position: relative;
    padding-left: 28px;
  }

  .card-content li:before {
    content: '▶';
    position: absolute;
    left: 0;
    color: #67e8f9;
    font-size: 1.1rem;
  }

  .socials-container {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 24px;
    margin: 20px 0 60px 0;
    flex-wrap: wrap;
  }

  /* Mobile - stack to 1 column */
  @media (max-width: 768px) {
    .typewriter { font-size: 2.1rem; }
    .section-title { font-size: 1.85rem; }
    .cards-container {
      grid-template-columns: 1fr;
      max-width: 100%;
    }
  }
</style>

# 💫 About Me

<div class="about-hero">
  <span class="typewriter">Hello, I am Yash Patel.</span>
</div>

<h2 class="section-title">🚀 WORK I DO</h2>

<div class="cards-container">

  <!-- Core Engineering Card -->
  <div class="card" style="animation-delay: 0.1s;">
    <h3>🔧 Core Engineering</h3>
    <div class="card-content">
      <ul>
        <li>Write clean, production-quality Python code for ML Systems</li>
        <li>Design and implement end-to-end data and ML pipelines</li>
        <li>Build, Train, Evaluate and Deploy deep learning models using PyTorch/JAX</li>
        <li>Architect infrastructure for Training and Evaluation of ML and DL models</li>
      </ul>
    </div>
  </div>

  <!-- GenAI Engineering Card -->
  <div class="card" style="animation-delay: 0.3s;">
    <h3>🤖 GenAI Engineering</h3>
    <div class="card-content">
      <ul>
        <li>PEFT methods to fine-tune LLMs and SLMs for specific use cases</li>
        <li>Design and Implement RAG</li>
        <li>Build Agentic-AI Systems with autonomous reasoning and tool use</li>
        <li>Apply Prompt Engineering and LLM orchestration Techniques</li>
        <li>Integrate and work with embedding models and vector databases</li>
      </ul>
    </div>
  </div>

  <!-- MLOps & Production Card -->
  <div class="card" style="animation-delay: 0.5s;">
    <h3>⚡ MLOps and Production</h3>
    <div class="card-content">
      <ul>
        <li>Build and Deploy model serving infrastructure at scale</li>
        <li>Implement MLOps and LLMOps practices across the model lifecycle</li>
        <li>Monitor deployed models — detect drifts, degradation and failure modes</li>
        <li>Optimize model for inference — speed, cost and memory</li>
      </ul>
    </div>
  </div>

  <!-- Scaling & System Design Card -->
  <div class="card" style="animation-delay: 0.7s;">
    <h3>📈 Scaling and System Designing</h3>
    <div class="card-content">
      <ul>
        <li>Design distributed training pipelines for large-scale models</li>
        <li>Design ML systems at scale — architecture, reliability and throughput</li>
        <li>Build scalable data ingestion and processing pipelines</li>
      </ul>
    </div>
  </div>

</div>

<h2 class="section-title">🌐 Socials</h2>

<div class="socials-container">
  [![LinkedIn](https://img.shields.io/badge/LinkedIn-%230077B5.svg?logo=linkedin&logoColor=white)](https://linkedin.com/in/yashkumar-patel-yp30a06a04) 
  [![email](https://img.shields.io/badge/Email-D14836?logo=gmail&logoColor=white)](mailto:pyash.xds@gmail.com)
</div>

<h2 class="section-title">💻 TECH STACK</h2>

![PyTorch](https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?style=for-the-badge&logo=PyTorch&logoColor=white)
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![C++](https://img.shields.io/badge/c++-%2300599C.svg?style=for-the-badge&logo=c%2B%2B&logoColor=white)
![Hugging Face](https://img.shields.io/badge/Hugging%20Face-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white)
![Kubeflow](https://img.shields.io/badge/Kubeflow-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white)
![mlflow](https://img.shields.io/badge/mlflow-%23d9ead3.svg?style=for-the-badge&logo=numpy&logoColor=blue)
![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-%23FF6F00.svg?style=for-the-badge&logo=TensorFlow&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/github%20actions-%232671E5.svg?style=for-the-badge&logo=githubactions&logoColor=white)
![Git](https://img.shields.io/badge/git-%23F05033.svg?style=for-the-badge&logo=git&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-%23FF9900.svg?style=for-the-badge&logo=amazon-aws&logoColor=white)
![AWS SageMaker](https://img.shields.io/badge/AWS%20SageMaker-FF9900?style=for-the-badge&logo=amazonaws&logoColor=white)
![AWS Bedrock](https://img.shields.io/badge/AWS%20Bedrock-FF9900?style=for-the-badge&logo=amazonaws&logoColor=white)
![Azure](https://img.shields.io/badge/azure-%230072C6.svg?style=for-the-badge&logo=microsoftazure&logoColor=white)
![Azure ML](https://img.shields.io/badge/Azure%20ML-0078D4?style=for-the-badge&logo=microsoftazure&logoColor=white)
![Google Cloud](https://img.shields.io/badge/GoogleCloud-%234285F4.svg?style=for-the-badge&logo=google-cloud&logoColor=white)
![Apache Spark](https://img.shields.io/badge/Apache%20Spark-FDEE21?style=for-the-badge&logo=apachespark&logoColor=black)
![Apache Kafka](https://img.shields.io/badge/Apache%20Kafka-000?style=for-the-badge&logo=apachekafka)
![FastAPI](https://img.shields.io/badge/FastAPI-005571?style=for-the-badge&logo=fastapi)
![Flask](https://img.shields.io/badge/flask-%23000.svg?style=for-the-badge&logo=flask&logoColor=white)
![Jinja](https://img.shields.io/badge/jinja-white.svg?style=for-the-badge&logo=jinja&logoColor=black)
![React](https://img.shields.io/badge/react-%2320232a.svg?style=for-the-badge&logo=react&logoColor=%2361DAFB)
![Snowflake](https://img.shields.io/badge/snowflake-%2329B5E8.svg?style=for-the-badge&logo=snowflake&logoColor=white)
![Socket.io](https://img.shields.io/badge/Socket.io-black?style=for-the-badge&logo=socket.io&badgeColor=010101)
![Apache Airflow](https://img.shields.io/badge/Apache%20Airflow-017CEE?style=for-the-badge&logo=Apache%20Airflow&logoColor=white)
![Jenkins](https://img.shields.io/badge/jenkins-%232C5263.svg?style=for-the-badge&logo=jenkins&logoColor=white)
![MySQL](https://img.shields.io/badge/mysql-4479A1.svg?style=for-the-badge&logo=mysql&logoColor=white)
![Postgres](https://img.shields.io/badge/postgres-%23316192.svg?style=for-the-badge&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/redis-%23DD0031.svg?style=for-the-badge&logo=redis&logoColor=white)
![SQLite](https://img.shields.io/badge/sqlite-%2307405e.svg?style=for-the-badge&logo=sqlite&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=for-the-badge&logo=supabase&logoColor=white)
![AmazonDynamoDB](https://img.shields.io/badge/Amazon%20DynamoDB-4053D6?style=for-the-badge&logo=Amazon%20DynamoDB&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-%234ea94b.svg?style=for-the-badge&logo=mongodb&logoColor=white)
![Keras](https://img.shields.io/badge/Keras-%23D00000.svg?style=for-the-badge&logo=Keras&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
![DVC](https://img.shields.io/badge/DVC-4F4F4F?style=for-the-badge&logo=dvc&logoColor=white)
![Dagshub](https://img.shields.io/badge/DagsHub-FF6B00?style=for-the-badge&logo=dagshub&logoColor=white)
![Ollama](https://img.shields.io/badge/Ollama-000000?style=for-the-badge&logo=ollama&logoColor=white)
![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=for-the-badge&logo=openai&logoColor=white)
![OpenRouter](https://img.shields.io/badge/OpenRouter-000000?style=for-the-badge&logo=openai&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white)
![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white)
![Autogen](https://img.shields.io/badge/Autogen-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white)
![CrewAI](https://img.shields.io/badge/CrewAI-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white)
![Pinecone](https://img.shields.io/badge/Pinecone-00A86B?style=for-the-badge&logo=pinecone&logoColor=white)
![Chroma](https://img.shields.io/badge/Chroma-FF6B00?style=for-the-badge&logo=chromadb&logoColor=white)
![Evidently](https://img.shields.io/badge/Evidently-FF6B00?style=for-the-badge&logo=evidently&logoColor=white)
![DeepSpeed](https://img.shields.io/badge/DeepSpeed-000000?style=for-the-badge&logo=microsoft&logoColor=white)
![FSDP](https://img.shields.io/badge/FSDP-000000?style=for-the-badge&logo=microsoft&logoColor=white)
![ONNX](https://img.shields.io/badge/ONNX-0055FF?style=for-the-badge&logo=onnx&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F2C811?style=for-the-badge&logo=grafana&logoColor=black)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=for-the-badge&logo=prometheus&logoColor=white)
![Mamba](https://img.shields.io/badge/Mamba-000000?style=for-the-badge&logo=python&logoColor=white)
![MoE](https://img.shields.io/badge/MoE-000000?style=for-the-badge&logo=python&logoColor=white)
![GitHub](https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white)

<h2 class="section-title">📊 GitHub Stats</h2>

![](https://github-readme-stats.shion.dev/api?username=pYashXds&theme=dark&hide_border=false&include_all_commits=true&count_private=false)  
![](https://streak-stats.demolab.com/?user=pYashXds&theme=dark&hide_border=false)  
![](https://github-readme-stats.shion.dev/api/top-langs/?username=pYashXds&theme=dark&hide_border=false&include_all_commits=true&count_private=false&layout=compact)

<h2 class="section-title">🏆 GitHub Trophies</h2>

![](https://github-profile-trophy.vercel.app/?username=pYashXds&theme=radical&no-frame=false&no-bg=true&margin-w=4)

### ✍️ Random Dev Quote
![](https://quotes-github-readme.vercel.app/api?type=horizontal&theme=radical)

### 🔝 Top Contributed Repo
![](https://github-contributor-stats.vercel.app/api?username=pYashXds&limit=5&theme=dark&combine_all_yearly_contributions=true)

---

[![](https://komarev.com/ghpvc/?username=pYashXds&icon=0&color=0)](https://visitcount.itsvg.in)

<!-- Proudly created with 🔥 by Yash Patel -->