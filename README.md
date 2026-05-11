import React from 'react';
import { Mail, Github, Linkedin, ExternalLink, Code, Palette, Globe } from 'lucide-react';

export default function Portfolio() {
  const projects = [
    {
      title: "Amory Cake - UI/UX Design",
      desc: "Thiết kế website tiệm bánh hiện đại với phong cách ngọt ngào, tối ưu trải nghiệm người dùng.",
      role: "Thiết kế giao diện (UI) & Trải nghiệm (UX)",
      tech: "Figma, Photoshop, AI Image Gen",
      image: "https://images.unsplash.com/photo-1519340333755-5072134bc221?q=80&w=2070" // Thay bằng ảnh Amory Cake
    },
    {
      title: "Velaro Uniform Branding",
      desc: "Phát triển bộ nhận diện thương hiệu và thiết kế mẫu áo Polo chuyên nghiệp cho doanh nghiệp.",
      role: "Designer chính & Brand Strategist",
      tech: "Illustrator, Mockup AI",
      image: "https://images.unsplash.com/photo-1521572163474-6864f9cf17ab?q=80&w=1780" // Thay bằng ảnh Velaro
    }
  ];

  const skills = [
    { name: "Graphic Design", level: "90%" },
    { name: "UI/UX Design", level: "85%" },
    { name: "3D Modeling (Tripo/Blender)", level: "75%" },
    { name: "Front-end Dev (React/Tailwind)", level: "70%" },
    { name: "English Proficiency", level: "80%" }
  ];

  return (
    <div className="min-h-screen bg-[#0f172a] text-slate-200 font-sans selection:bg-cyan-500/30">
      
      {/* 1. HERO SECTION (Giới thiệu) */}
      <section className="relative h-screen flex items-center justify-center overflow-hidden border-b border-slate-800">
        <div className="absolute inset-0 z-0 bg-[radial-gradient(circle_at_50%_50%,rgba(6,182,212,0.1),transparent_50%)]"></div>
        <div className="container mx-auto px-6 text-center z-10">
          <h1 className="text-6xl md:text-8xl font-black mb-4 tracking-tighter bg-gradient-to-r from-white to-slate-500 bg-clip-text text-transparent">
            NGUYỄN VĂN A
          </h1>
          <p className="text-xl md:text-2xl font-medium text-cyan-400 mb-8 uppercase tracking-[0.2em]">
            Creative Designer & 3D Artist
          </p>
          <p className="max-w-2xl mx-auto text-slate-400 text-lg italic">
            "Biến những ý tưởng trừu tượng thành trải nghiệm thị giác sống động thông qua sự kết hợp giữa tư duy thiết kế và công nghệ AI."
          </p>
        </div>
      </section>

      {/* 2. ABOUT SECTION (Giới thiệu bản thân) */}
      <section id="about" className="py-24 container mx-auto px-6">
        <div className="grid md:grid-cols-2 gap-16 items-center">
          <div>
            <h2 className="text-3xl font-bold mb-6 flex items-center gap-3">
              <span className="w-12 h-[2px] bg-cyan-500"></span> Giới thiệu bản thân
            </h2>
            <p className="text-slate-400 leading-relaxed mb-6">
              Mình là sinh viên năm cuối chuyên ngành Thiết kế, luôn tìm kiếm sự giao thoa giữa nghệ thuật truyền thống và công nghệ số. Định hướng của mình là trở thành một Product Designer đa năng, có khả năng làm chủ cả 2D, 3D và lập trình giao diện.
            </p>
            <div className="grid grid-cols-2 gap-4">
              <div className="p-4 rounded-xl bg-slate-800/50 border border-slate-700">
                <h4 className="text-cyan-400 font-bold italic">Mục tiêu</h4>
                <p className="text-sm">Xây dựng hệ sinh thái thiết kế thông minh.</p>
              </div>
              <div className="p-4 rounded-xl bg-slate-800/50 border border-slate-700">
                <h4 className="text-cyan-400 font-bold italic">Sở thích</h4>
                <p className="text-sm">Vẽ Digital, nhiếp ảnh và khám phá AI.</p>
              </div>
            </div>
          </div>
          <div className="relative group">
             {/* Placeholder cho ảnh chân dung hoặc Model 3D của bạn */}
             <div className="aspect-square bg-gradient-to-tr from-cyan-900 to-slate-800 rounded-2xl border border-slate-700 flex items-center justify-center">
                <span className="text-slate-500">Your 3D Model Here</span>
             </div>
          </div>
        </div>
      </section>

      {/* 3. SKILLS SECTION (Kỹ năng) */}
      <section className="py-24 bg-slate-900/50 border-y border-slate-800">
        <div className="container mx-auto px-6">
          <h2 className="text-3xl font-bold mb-12 text-center">Năng lực cốt lõi</h2>
          <div className="max-w-3xl mx-auto space-y-8">
            {skills.map((skill, i) => (
              <div key={i}>
                <div className="flex justify-between mb-2">
                  <span className="font-medium">{skill.name}</span>
                  <span className="text-cyan-400">{skill.level}</span>
                </div>
                <div className="h-2 w-full bg-slate-800 rounded-full overflow-hidden">
                  <div className="h-full bg-cyan-500 rounded-full transition-all duration-1000" style={{ width: skill.level }}></div>
                </div>
              </div>
            ))}
          </div>
        </div>
      </section>

      {/* 4. PROJECTS SECTION (Dự án) */}
      <section id="projects" className="py-24 container mx-auto px-6">
        <h2 className="text-3xl font-bold mb-16">Dự án tiêu biểu</h2>
        <div className="grid md:grid-cols-2 gap-12">
          {projects.map((item, index) => (
            <div key={index} className="group relative bg-slate-800 rounded-3xl overflow-hidden border border-slate-700 hover:border-cyan-500/50 transition-all duration-500">
              <div className="h-72 overflow-hidden">
                <img src={item.image} alt={item.title} className="w-full h-full object-cover group-hover:scale-110 transition-transform duration-700" />
              </div>
              <div className="p-8">
                <h3 className="text-2xl font-bold mb-3">{item.title}</h3>
                <p className="text-slate-400 mb-4 text-sm leading-relaxed">{item.desc}</p>
                <div className="space-y-2 mb-6">
                  <p className="text-xs text-cyan-400 uppercase tracking-widest font-bold">Vai trò: {item.role}</p>
                  <p className="text-xs text-slate-500 uppercase tracking-widest font-bold text-nowrap truncate">Công cụ: {item.tech}</p>
                </div>
                <button className="flex items-center gap-2 text-white hover:text-cyan-400 transition font-medium">
                  Chi tiết dự án <ExternalLink size={16} />
                </button>
              </div>
            </div>
          ))}
        </div>
      </section>

      {/* 5. CONTACT SECTION (Liên hệ) */}
      <section id="contact" className="py-32 container mx-auto px-6 text-center">
        <h2 className="text-5xl font-bold mb-8">Hãy cùng tạo nên điều <span className="text-cyan-400">kỳ diệu</span></h2>
        <p className="text-slate-400 mb-12 max-w-lg mx-auto">
          Mình luôn sẵn sàng cho các dự án freelance hoặc cơ hội thực tập. Đừng ngần ngại liên hệ nhé!
        </p>
        <div className="flex flex-col md:flex-row items-center justify-center gap-6">
          <a href="mailto:email@example.com" className="flex items-center gap-3 bg-white text-black px-8 py-4 rounded-full font-bold hover:bg-cyan-400 hover:text-white transition-all">
            <Mail size={20} /> Gửi Email cho mình
          </a>
          <div className="flex gap-4">
            <a href="#" className="p-4 bg-slate-800 rounded-full hover:text-cyan-400 transition"><Github /></a>
            <a href="#" className="p-4 bg-slate-800 rounded-full hover:text-cyan-400 transition"><Linkedin /></a>
          </div>
        </div>
      </section>

      <footer className="py-10 text-center text-slate-600 text-sm border-t border-slate-900">
        © 2026 Designed & Built by [Tên Bạn] - Powered by Next.js
      </footer>
    </div>
  );
}
