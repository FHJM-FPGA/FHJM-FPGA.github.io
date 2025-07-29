<!DOCTYPE html>
<html lang="zh-CN">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>绯红姜梦FPGA | 个人网站</title>
  <!-- Tailwind CSS -->
  <script src="https://cdn.tailwindcss.com"></script>
  <!-- Font Awesome -->
  <link href="https://cdn.jsdelivr.net/npm/font-awesome@4.7.0/css/font-awesome.min.css" rel="stylesheet">
  
  <!-- 自定义 Tailwind 配置 -->
  <script>
    tailwind.config = {
      theme: {
        extend: {
          colors: {
            primary: '#165DFF',
            secondary: '#FF7D00',
            dark: '#1E293B',
            light: '#F8FAFC'
          },
          fontFamily: {
            inter: ['Inter', 'system-ui', 'sans-serif'],
          },
        },
      }
    }
  </script>
  
  <style type="text/tailwindcss">
    @layer utilities {
      .content-auto {
        content-visibility: auto;
      }
      .text-shadow {
        text-shadow: 0 2px 4px rgba(0,0,0,0.1);
      }
      .animate-float {
        animation: float 3s ease-in-out infinite;
      }
      @keyframes float {
        0% { transform: translateY(0px); }
        50% { transform: translateY(-10px); }
        100% { transform: translateY(0px); }
      }
    }
  </style>
</head>
<body class="font-inter bg-light text-dark min-h-screen flex flex-col">
  <!-- 导航栏 -->
  <header class="sticky top-0 z-50 bg-white/90 backdrop-blur-sm shadow-sm transition-all duration-300">
    <div class="container mx-auto px-4 py-4 flex justify-between items-center">
      <a href="index.html" class="text-primary font-bold text-2xl flex items-center">
        <span class="mr-2 text-secondary"><i class="fa fa-microchip"></i></span>
        绯红姜梦FPGA
      </a>
      
      <!-- 桌面导航 -->
      <nav class="hidden md:flex space-x-8">
        <a href="index.html" class="text-dark hover:text-primary transition-colors font-medium">首页</a>
        <a href="pages/about.html" class="text-dark hover:text-primary transition-colors font-medium">关于</a>
        <a href="posts/" class="text-dark hover:text-primary transition-colors font-medium">博客</a>
      </nav>
      
      <!-- 移动端菜单按钮 -->
      <button id="menu-toggle" class="md:hidden text-dark focus:outline-none">
        <i class="fa fa-bars text-xl"></i>
      </button>
    </div>
    
    <!-- 移动端导航菜单 -->
    <div id="mobile-menu" class="md:hidden hidden bg-white border-t">
      <div class="container mx-auto px-4 py-3 flex flex-col space-y-3">
        <a href="index.html" class="text-dark hover:text-primary transition-colors py-2">首页</a>
        <a href="pages/about.html" class="text-dark hover:text-primary transition-colors py-2">关于</a>
        <a href="posts/" class="text-dark hover:text-primary transition-colors py-2">博客</a>
      </div>
    </div>
  </header>

  <!-- 主内容 -->
  <main class="flex-grow">
    <!-- 英雄区域 -->
    <section class="relative bg-gradient-to-br from-primary/10 to-primary/5 py-20 md:py-32 overflow-hidden">
      <div class="container mx-auto px-4 relative z-10">
        <div class="max-w-3xl mx-auto text-center">
          <h1 class="text-[clamp(2.5rem,5vw,4rem)] font-bold text-dark leading-tight mb-6 text-shadow">
            探索<span class="text-primary">FPGA</span>与数字电路的无限可能
          </h1>
          <p class="text-[clamp(1.1rem,2vw,1.3rem)] text-gray-600 mb-8 max-w-2xl mx-auto">
            我是绯红姜梦，FPGA 工程师与技术爱好者。这里记录了我的学习笔记、项目经验和技术思考。
          </p>
          <div class="flex flex-col sm:flex-row justify-center gap-4">
            <a href="pages/about.html" class="btn bg-primary hover:bg-primary/90 text-white px-8 py-3 rounded-lg transition-all transform hover:scale-105 font-medium shadow-lg hover:shadow-primary/20">
              了解更多
            </a>
            <a href="posts/" class="btn bg-white hover:bg-gray-50 text-primary border border-primary px-8 py-3 rounded-lg transition-all transform hover:scale-105 font-medium shadow-md">
              浏览博客
            </a>
          </div>
        </div>
      </div>
      
      <!-- 装饰元素 -->
      <div class="absolute -top-20 -right-20 w-64 h-64 bg-primary/10 rounded-full blur-3xl"></div>
      <div class="absolute -bottom-32 -left-32 w-80 h-80 bg-secondary/10 rounded-full blur-3xl"></div>
    </section>
    
    <!-- 关于区域 -->
    <section class="py-16 bg-white">
      <div class="container mx-auto px-4">
        <div class="text-center mb-12">
          <h2 class="text-[clamp(1.8rem,3vw,2.5rem)] font-bold text-dark mb-4">关于我</h2>
          <div class="w-20 h-1 bg-primary mx-auto mb-6"></div>
        </div>
        
        <div class="grid md:grid-cols-2 gap-12 items-center">
          <div class="order-2 md:order-1">
            <h3 class="text-2xl font-bold text-dark mb-4">FPGA 工程师 & 技术博主</h3>
            <p class="text-gray-600 mb-6">
              拥有5年FPGA开发经验，专注于数字电路设计、高速接口和嵌入式系统开发。目前在XX科技担任高级FPGA工程师，负责XX项目的架构设计与实现。
            </p>
            <p class="text-gray-600 mb-6">
              我热衷于分享技术知识，通过博客记录学习过程中的经验与思考，内容涵盖Verilog/VHDL编程、时序分析、IP核开发等主题。
            </p>
            <div class="flex flex-wrap gap-3 mb-8">
              <span class="px-4 py-1 bg-primary/10 text-primary rounded-full text-sm">Verilog</span>
              <span class="px-4 py-1 bg-primary/10 text-primary rounded-full text-sm">VHDL</span>
              <span class="px-4 py-1 bg-primary/10 text-primary rounded-full text-sm">时序分析</span>
              <span class="px-4 py-1 bg-primary/10 text-primary rounded-full text-sm">高速接口</span>
              <span class="px-4 py-1 bg-primary/10 text-primary rounded-full text-sm">嵌入式系统</span>
            </div>
            <a href="pages/about.html" class="inline-flex items-center text-primary hover:text-primary/80 font-medium transition-colors">
              查看更多详情 <i class="fa fa-arrow-right ml-2"></i>
            </a>
          </div>
          <div class="order-1 md:order-2 flex justify-center">
            <div class="relative">
              <img src="https://picsum.photos/seed/fpga/500/500" alt="绯红姜梦FPGA照片" class="w-full max-w-md rounded-lg shadow-xl transform hover:scale-[1.02] transition-transform duration-300">
              <div class="absolute -bottom-4 -right-4 w-20 h-20 bg-secondary rounded-lg -z-10"></div>
              <div class="absolute -top-4 -left-4 w-20 h-20 bg-primary rounded-lg -z-10"></div>
            </div>
          </div>
        </div>
      </div>
    </section>
    
    <!-- 博客文章区域 -->
    <section class="py-16 bg-gray-50">
      <div class="container mx-auto px-4">
        <div class="text-center mb-12">
          <h2 class="text-[clamp(1.8rem,3vw,2.5rem)] font-bold text-dark mb-4">最新博客</h2>
          <p class="text-gray-600 max-w-2xl mx-auto">探索我分享的最新技术文章和项目经验</p>
          <div class="w-20 h-1 bg-primary mx-auto mt-6"></div>
        </div>
        
        <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
          <!-- 文章卡片 1 -->
          <article class="bg-white rounded-xl overflow-hidden shadow-md hover:shadow-xl transition-shadow group">
            <div class="relative overflow-hidden h-52">
              <img src="https://picsum.photos/seed/fpga1/600/400" alt="FPGA时序分析技术" class="w-full h-full object-cover transition-transform duration-500 group-hover:scale-110">
              <div class="absolute top-4 left-4 bg-primary text-white text-xs font-bold px-3 py-1 rounded-full">
                FPGA基础
              </div>
            </div>
            <div class="p-6">
              <h3 class="text-xl font-bold text-dark mb-2 group-hover:text-primary transition-colors">FPGA时序分析技术详解</h3>
              <p class="text-gray-600 mb-4 line-clamp-3">深入理解时序约束、时序路径和时序报告，掌握解决时序违例的实用技巧和方法。</p>
              <div class="flex justify-between items-center">
                <span class="text-sm text-gray-500"><i class="fa fa-calendar-o mr-1"></i> 2025-07-15</span>
                <a href="#" class="text-primary hover:text-primary/80 font-medium text-sm flex items-center">
                  阅读更多 <i class="fa fa-angle-right ml-1"></i>
                </a>
              </div>
            </div>
          </article>
          
          <!-- 文章卡片 2 -->
          <article class="bg-white rounded-xl overflow-hidden shadow-md hover:shadow-xl transition-shadow group">
            <div class="relative overflow-hidden h-52">
              <img src="https://picsum.photos/seed/fpga2/600/400" alt="高速接口设计" class="w-full h-full object-cover transition-transform duration-500 group-hover:scale-110">
              <div class="absolute top-4 left-4 bg-secondary text-white text-xs font-bold px-3 py-1 rounded-full">
                高速接口
              </div>
            </div>
            <div class="p-6">
              <h3 class="text-xl font-bold text-dark mb-2 group-hover:text-primary transition-colors">PCIe Gen4在FPGA中的实现</h3>
              <p class="text-gray-600 mb-4 line-clamp-3">详细介绍PCIe Gen4协议架构，以及如何在Xilinx和Intel FPGA平台上实现高速数据传输。</p>
              <div class="flex justify-between items-center">
                <span class="text-sm text-gray-500"><i class="fa fa-calendar-o mr-1"></i> 2025-07-02</span>
                <a href="#" class="text-primary hover:text-primary/80 font-medium text-sm flex items-center">
                  阅读更多 <i class="fa fa-angle-right ml-1"></i>
                </a>
              </div>
            </div>
          </article>
          
          <!-- 文章卡片 3 -->
          <article class="bg-white rounded-xl overflow-hidden shadow-md hover:shadow-xl transition-shadow group">
            <div class="relative overflow-hidden h-52">
              <img src="https://picsum.photos/seed/fpga3/600/400" alt="嵌入式系统开发" class="w-full h-full object-cover transition-transform duration-500 group-hover:scale-110">
              <div class="absolute top-4 left-4 bg-primary text-white text-xs font-bold px-3 py-1 rounded-full">
                嵌入式系统
              </div>
            </div>
            <div class="p-6">
              <h3 class="text-xl font-bold text-dark mb-2 group-hover:text-primary transition-colors">基于Zynq的SoC设计实战</h3>
              <p class="text-gray-600 mb-4 line-clamp-3">从硬件设计到软件开发，全面讲解如何构建高性能、低功耗的Zynq全可编程SoC系统。</p>
              <div class="flex justify-between items-center">
                <span class="text-sm text-gray-500"><i class="fa fa-calendar-o mr-1"></i> 2025-06-18</span>
                <a href="#" class="text-primary hover:text-primary/80 font-medium text-sm flex items-center">
                  阅读更多 <i class="fa fa-angle-right ml-1"></i>
                </a>
              </div>
            </div>
          </article>
        </div>
        
        <div class="text-center mt-10">
          <a href="posts/" class="inline-block bg-white border border-primary text-primary hover:bg-primary hover:text-white px-8 py-3 rounded-lg transition-all font-medium shadow-sm">
            查看所有文章
          </a>
        </div>
      </div>
    </section>
    
    <!-- 技能区域 -->
    <section class="py-16 bg-white">
      <div class="container mx-auto px-4">
        <div class="text-center mb-12">
          <h2 class="text-[clamp(1.8rem,3vw,2.5rem)] font-bold text-dark mb-4">专业技能</h2>
          <p class="text-gray-600 max-w-2xl mx-auto">我的技术栈与专业能力</p>
          <div class="w-20 h-1 bg-primary mx-auto mt-6"></div>
        </div>
        
        <div class="grid md:grid-cols-2 gap-12">
          <!-- 技能栏 -->
          <div>
            <div class="mb-8">
              <div class="flex justify-between mb-2">
                <span class="font-medium">Verilog/VHDL</span>
                <span>90%</span>
              </div>
              <div class="h-2 bg-gray-200 rounded-full overflow-hidden">
                <div class="h-full bg-primary rounded-full" style="width: 90%"></div>
              </div>
            </div>
            
            <div class="mb-8">
              <div class="flex justify-between mb-2">
                <span class="font-medium">时序分析</span>
                <span>85%</span>
              </div>
              <div class="h-2 bg-gray-200 rounded-full overflow-hidden">
                <div class="h-full bg-primary rounded-full" style="width: 85%"></div>
              </div>
            </div>
            
            <div class="mb-8">
              <div class="flex justify-between mb-2">
                <span class="font-medium">高速接口设计</span>
                <span>80%</span>
              </div>
              <div class="h-2 bg-gray-200 rounded-full overflow-hidden">
                <div class="h-full bg-primary rounded-full" style="width: 80%"></div>
              </div>
            </div>
            
            <div class="mb-8">
              <div class="flex justify-between mb-2">
                <span class="font-medium">嵌入式系统开发</span>
                <span>75%</span>
              </div>
              <div class="h-2 bg-gray-200 rounded-full overflow-hidden">
                <div class="h-full bg-primary rounded-full" style="width: 75%"></div>
              </div>
            </div>
            
            <div class="mb-8">
              <div class="flex justify-between mb-2">
                <span class="font-medium">Python/C++</span>
                <span>70%</span>
              </div>
              <div class="h-2 bg-gray-200 rounded-full overflow-hidden">
                <div class="h-full bg-primary rounded-full" style="width: 70%"></div>
              </div>
            </div>
          </div>
          
          <!-- 工具与平台 -->
          <div>
            <h3 class="text-xl font-bold text-dark mb-6">工具与平台</h3>
            <div class="grid grid-cols-2 gap-4">
              <div class="bg-gray-50 p-4 rounded-lg flex items-center">
                <div class="w-12 h-12 rounded-full bg-primary/10 flex items-center justify-center text-primary mr-4">
                  <i class="fa fa-microchip text-xl"></i>
                </div>
                <div>
                  <h4 class="font-medium">Xilinx</h4>
                  <p class="text-sm text-gray-500">Vivado, ISE</p>
                </div>
              </div>
              
              <div class="bg-gray-50 p-4 rounded-lg flex items-center">
                <div class="w-12 h-12 rounded-full bg-primary/10 flex items-center justify-center text-primary mr-4">
                  <i class="fa fa-microchip text-xl"></i>
                </div>
                <div>
                  <h4 class="font-medium">Intel</h4>
                  <p class="text-sm text-gray-500">Quartus Prime</p>
                </div>
              </div>
              
              <div class="bg-gray-50 p-4 rounded-lg flex items-center">
                <div class="w-12 h-12 rounded-full bg-primary/10 flex items-center justify-center text-primary mr-4">
                  <i class="fa fa-code text-xl"></i>
                </div>
                <div>
                  <h4 class="font-medium">仿真工具</h4>
                  <p class="text-sm text-gray-500">ModelSim, Vivado Simulator</p>
                </div>
              </div>
              
              <div class="bg-gray-50 p-4 rounded-lg flex items-center">
                <div class="w-12 h-12 rounded-full bg-primary/10 flex items-center justify-center text-primary mr-4">
                  <i class="fa fa-sitemap text-xl"></i>
                </div>
                <div>
                  <h4 class="font-medium">调试工具</h4>
                  <p class="text-sm text-gray-500">ChipScope, SignalTap</p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
    
    <!-- 联系区域 -->
    <section class="py-16 bg-gradient-to-br from-primary to-primary/80 text-white">
      <div class="container mx-auto px-4">
        <div class="text-center mb-12">
          <h2 class="text-[clamp(1.8rem,3vw,2.5rem)] font-bold mb-4">联系我</h2>
          <p class="max-w-2xl mx-auto opacity-90">有任何问题或合作机会，请随时与我联系</p>
          <div class="w-20 h-1 bg-white mx-auto mt-6"></div>
        </div>
        
        <div class="max-w-3xl mx-auto">
          <form class="space-y-6">
            <div class="grid md:grid-cols-2 gap-6">
              <div>
                <label for="name" class="block text-sm font-medium mb-2">姓名</label>
                <input type="text" id="name" class="w-full px-4 py-3 bg-white/10 border border-white/20 rounded-lg focus:outline-none focus:ring-2 focus:ring-white/50 text-white placeholder-white/60" placeholder="请输入您的姓名">
              </div>
              <div>
                <label for="email" class="block text-sm font-medium mb-2">邮箱</label>
                <input type="email" id="email" class="w-full px-4 py-3 bg-white/10 border border-white/20 rounded-lg focus:outline-none focus:ring-2 focus:ring-white/50 text-white placeholder-white/60" placeholder="请输入您的邮箱">
              </div>
            </div>
            <div>
              <label for="subject" class="block text-sm font-medium mb-2">主题</label>
              <input type="text" id="subject" class="w-full px-4 py-3 bg-white/10 border border-white/20 rounded-lg focus:outline-none focus:ring-2 focus:ring-white/50 text-white placeholder-white/60" placeholder="请输入邮件主题">
            </div>
            <div>
              <label for="message" class="block text-sm font-medium mb-2">消息</label>
              <textarea id="message" rows="5" class="w-full px-4 py-3 bg-white/10 border border-white/20 rounded-lg focus:outline-none focus:ring-2 focus:ring-white/50 text-white placeholder-white/60" placeholder="请输入您的消息内容"></textarea>
            </div>
            <div class="text-center">
              <button type="submit" class="bg-white text-primary hover:bg-white/90 px-8 py-3 rounded-lg transition-all transform hover:scale-105 font-medium shadow-lg">
                发送消息
              </button>
            </div>
          </form>
        </div>
      </div>
    </section>
  </main>

  <!-- 页脚 -->
  <footer class="bg-dark text-white py-12">
    <div class="container mx-auto px-4">
      <div class="grid md:grid-cols-4 gap-8">
        <div>
          <h3 class="text-xl font-bold mb-4 flex items-center">
            <span class="mr-2 text-secondary"><i class="fa fa-microchip"></i></span>
            绯红姜梦FPGA
          </h3>
          <p class="text-gray-400 mb-4">FPGA工程师与技术爱好者，分享数字电路设计与嵌入式系统开发的知识与经验。</p>
          <div class="flex space-x-4">
            <a href="#" class="text-gray-400 hover:text-white transition-colors">
              <i class="fa fa-github text-xl"></i>
            </a>
            <a href="#" class="text-gray-400 hover:text-white transition-colors">
              <i class="fa fa-linkedin text-xl"></i>
            </a>
            <a href="#" class="text-gray-400 hover:text-white transition-colors">
              <i class="fa fa-twitter text-xl"></i>
            </a>
            <a href="#" class="text-gray-400 hover:text-white transition-colors">
              <i class="fa fa-youtube-play text-xl"></i>
            </a>
          </div>
        </div>
        
        <div>
          <h4 class="text-lg font-medium mb-4">快速链接</h4>
          <ul class="space-y-2">
            <li><a href="index.html" class="text-gray-400 hover:text-white transition-colors">首页</a></li>
            <li><a href="pages/about.html" class="text-gray-400 hover:text-white transition-colors">关于我</a></li>
            <li><a href="posts/" class="text-gray-400 hover:text-white transition-colors">博客</a></li>
            <li><a href="#" class="text-gray-400 hover:text-white transition-colors">项目</a></li>
            <li><a href="#" class="text-gray-400 hover:text-white transition-colors">联系我</a></li>
          </ul>
        </div>
        
        <div>
          <h4 class="text-lg font-medium mb-4">博客分类</h4>
          <ul class="space-y-2">
            <li><a href="#" class="text-gray-400 hover:text-white transition-colors">FPGA基础</a></li>
            <li><a href="#" class="text-gray-400 hover:text-white transition-colors">高速接口</a></li>
            <li><a href="#" class="text-gray-400 hover:text-white transition-colors">嵌入式系统</a></li>
            <li><a href="#" class="text-gray-400 hover:text-white transition-colors">工具教程</a></li>
            <li><a href="#" class="text-gray-400 hover:text-white transition-colors">行业动态</a></li>
          </ul>
        </div>
        
        <div>
          <h4 class="text-lg font-medium mb-4">订阅更新</h4>
          <p class="text-gray-400 mb-4">订阅我的博客，获取最新技术文章和项目更新。</p>
          <form class="flex">
            <input type="email" placeholder="您的邮箱地址" class="px-4 py-2 bg-white/10 border border-white/20 rounded-l-lg focus:outline-none focus:ring-2 focus:ring-white/50 text-white placeholder-white/60 flex-grow">
            <button type="submit" class="bg-secondary hover:bg-secondary/90 px-4 py-2 rounded-r-lg transition-colors">
              <i class="fa fa-paper-plane"></i>
            </button>
          </form>
        </div>
      </div>
      
      <div class="border-t border-gray-800 mt-12 pt-8 text-center text-gray-500 text-sm">
        <p>&copy; 2025 绯红姜梦FPGA. 保留所有权利.</p>
      </div>
    </div>
  </footer>

  <!-- JavaScript -->
  <script>
    // 移动端菜单切换
    const menuToggle = document.getElementById('menu-toggle');
    const mobileMenu = document.getElementById('mobile-menu');
    
    menuToggle.addEventListener('click', () => {
      mobileMenu.classList.toggle('hidden');
    });
    
    // 滚动时导航栏样式变化
    window.addEventListener('scroll', () => {
      const header = document.querySelector('header');
      if (window.scrollY > 50) {
        header.classList.add('py-2', 'shadow-md');
        header.classList.remove('py-4', 'shadow-sm');
      } else {
        header.classList.add('py-4', 'shadow-sm');
        header.classList.remove('py-2', 'shadow-md');
      }
    });
    
    // 平滑滚动
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
      anchor.addEventListener('click', function (e) {
        e.preventDefault();
        
        const targetId = this.getAttribute('href');
        if (targetId === '#') return;
        
        const targetElement = document.querySelector(targetId);
        if (targetElement) {
          targetElement.scrollIntoView({
            behavior: 'smooth'
          });
        }
      });
    });
  </script>
</body>
</html>
