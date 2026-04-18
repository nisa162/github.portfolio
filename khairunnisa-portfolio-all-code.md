# Khairunnisa Portfolio — Combined Source Code

Generated bundle of all portfolio source files in one document.


---

## `src/index.css`

```css
@tailwind base;
@tailwind components;
@tailwind utilities;

@layer base {
  :root {
    /* Brand: Deep Tech Blue + Electric Teal */
    --background: 210 40% 98%;
    --foreground: 222 47% 11%;

    --card: 0 0% 100%;
    --card-foreground: 222 47% 11%;

    --popover: 0 0% 100%;
    --popover-foreground: 222 47% 11%;

    --primary: 222 80% 22%;
    --primary-foreground: 210 40% 98%;
    --primary-glow: 220 90% 55%;

    --accent: 180 85% 42%;
    --accent-foreground: 222 47% 11%;
    --accent-glow: 190 95% 55%;

    --secondary: 210 40% 94%;
    --secondary-foreground: 222 47% 15%;

    --muted: 210 30% 94%;
    --muted-foreground: 215 16% 40%;

    --destructive: 0 84% 60%;
    --destructive-foreground: 210 40% 98%;

    --border: 215 25% 88%;
    --input: 215 25% 88%;
    --ring: 220 90% 55%;

    --radius: 0.85rem;

    /* Gradients */
    --gradient-hero: radial-gradient(ellipse at top left, hsl(220 90% 55% / 0.18), transparent 55%),
                     radial-gradient(ellipse at bottom right, hsl(180 85% 42% / 0.18), transparent 55%),
                     linear-gradient(180deg, hsl(210 40% 98%), hsl(210 40% 96%));
    --gradient-primary: linear-gradient(135deg, hsl(var(--primary)), hsl(var(--primary-glow)));
    --gradient-accent: linear-gradient(135deg, hsl(var(--accent)), hsl(var(--accent-glow)));
    --gradient-card: linear-gradient(145deg, hsl(0 0% 100%), hsl(210 40% 97%));
    --gradient-text: linear-gradient(135deg, hsl(var(--primary)), hsl(var(--accent)));

    /* Shadows */
    --shadow-soft: 0 4px 20px -8px hsl(222 47% 11% / 0.1);
    --shadow-elegant: 0 20px 50px -20px hsl(222 80% 22% / 0.25);
    --shadow-glow: 0 0 40px hsl(var(--accent) / 0.35);

    --transition-smooth: cubic-bezier(0.16, 1, 0.3, 1);

    --sidebar-background: 0 0% 98%;
    --sidebar-foreground: 240 5% 26%;
    --sidebar-primary: 240 6% 10%;
    --sidebar-primary-foreground: 0 0% 98%;
    --sidebar-accent: 240 5% 96%;
    --sidebar-accent-foreground: 240 6% 10%;
    --sidebar-border: 220 13% 91%;
    --sidebar-ring: 217 91% 60%;
  }

  .dark {
    --background: 222 47% 6%;
    --foreground: 210 40% 98%;
    --card: 222 47% 9%;
    --card-foreground: 210 40% 98%;
    --popover: 222 47% 9%;
    --popover-foreground: 210 40% 98%;
    --primary: 220 90% 60%;
    --primary-foreground: 222 47% 6%;
    --primary-glow: 200 95% 60%;
    --accent: 180 85% 50%;
    --accent-foreground: 222 47% 6%;
    --secondary: 217 33% 15%;
    --secondary-foreground: 210 40% 98%;
    --muted: 217 33% 15%;
    --muted-foreground: 215 20% 65%;
    --border: 217 33% 18%;
    --input: 217 33% 18%;
    --ring: 220 90% 60%;
    --gradient-card: linear-gradient(145deg, hsl(222 47% 9%), hsl(222 47% 11%));
  }
}

@layer base {
  * {
    @apply border-border;
  }
  html {
    scroll-behavior: smooth;
  }
  body {
    @apply bg-background text-foreground font-sans antialiased;
    font-family: 'Inter', system-ui, sans-serif;
  }
  h1, h2, h3, h4 {
    font-family: 'Space Grotesk', 'Inter', sans-serif;
    @apply tracking-tight;
  }
}

@layer utilities {
  .gradient-text {
    background: var(--gradient-text);
    -webkit-background-clip: text;
    background-clip: text;
    color: transparent;
  }
  .gradient-hero {
    background: var(--gradient-hero);
  }
  .gradient-primary {
    background: var(--gradient-primary);
  }
  .gradient-accent {
    background: var(--gradient-accent);
  }
  .glass {
    background: hsl(var(--background) / 0.7);
    backdrop-filter: blur(12px);
    -webkit-backdrop-filter: blur(12px);
  }
  .shadow-elegant {
    box-shadow: var(--shadow-elegant);
  }
  .shadow-soft {
    box-shadow: var(--shadow-soft);
  }
  .shadow-glow {
    box-shadow: var(--shadow-glow);
  }
  .hover-lift {
    transition: transform 0.4s var(--transition-smooth), box-shadow 0.4s var(--transition-smooth);
  }
  .hover-lift:hover {
    transform: translateY(-6px);
    box-shadow: var(--shadow-elegant);
  }
}

```


---

## `tailwind.config.ts`

```ts
import type { Config } from "tailwindcss";

export default {
  darkMode: ["class"],
  content: ["./pages/**/*.{ts,tsx}", "./components/**/*.{ts,tsx}", "./app/**/*.{ts,tsx}", "./src/**/*.{ts,tsx}"],
  prefix: "",
  theme: {
    container: {
      center: true,
      padding: "2rem",
      screens: {
        "2xl": "1400px",
      },
    },
    extend: {
      colors: {
        border: "hsl(var(--border))",
        input: "hsl(var(--input))",
        ring: "hsl(var(--ring))",
        background: "hsl(var(--background))",
        foreground: "hsl(var(--foreground))",
        primary: {
          DEFAULT: "hsl(var(--primary))",
          foreground: "hsl(var(--primary-foreground))",
        },
        secondary: {
          DEFAULT: "hsl(var(--secondary))",
          foreground: "hsl(var(--secondary-foreground))",
        },
        destructive: {
          DEFAULT: "hsl(var(--destructive))",
          foreground: "hsl(var(--destructive-foreground))",
        },
        muted: {
          DEFAULT: "hsl(var(--muted))",
          foreground: "hsl(var(--muted-foreground))",
        },
        accent: {
          DEFAULT: "hsl(var(--accent))",
          foreground: "hsl(var(--accent-foreground))",
        },
        popover: {
          DEFAULT: "hsl(var(--popover))",
          foreground: "hsl(var(--popover-foreground))",
        },
        card: {
          DEFAULT: "hsl(var(--card))",
          foreground: "hsl(var(--card-foreground))",
        },
        sidebar: {
          DEFAULT: "hsl(var(--sidebar-background))",
          foreground: "hsl(var(--sidebar-foreground))",
          primary: "hsl(var(--sidebar-primary))",
          "primary-foreground": "hsl(var(--sidebar-primary-foreground))",
          accent: "hsl(var(--sidebar-accent))",
          "accent-foreground": "hsl(var(--sidebar-accent-foreground))",
          border: "hsl(var(--sidebar-border))",
          ring: "hsl(var(--sidebar-ring))",
        },
      },
      borderRadius: {
        lg: "var(--radius)",
        md: "calc(var(--radius) - 2px)",
        sm: "calc(var(--radius) - 4px)",
      },
      fontFamily: {
        sans: ["Inter", "system-ui", "sans-serif"],
        display: ["Space Grotesk", "Inter", "sans-serif"],
      },
      keyframes: {
        "accordion-down": { from: { height: "0" }, to: { height: "var(--radix-accordion-content-height)" } },
        "accordion-up": { from: { height: "var(--radix-accordion-content-height)" }, to: { height: "0" } },
        "fade-in": { "0%": { opacity: "0", transform: "translateY(16px)" }, "100%": { opacity: "1", transform: "translateY(0)" } },
        "fade-in-up": { "0%": { opacity: "0", transform: "translateY(30px)" }, "100%": { opacity: "1", transform: "translateY(0)" } },
        "scale-in": { "0%": { opacity: "0", transform: "scale(0.95)" }, "100%": { opacity: "1", transform: "scale(1)" } },
        "float": { "0%,100%": { transform: "translateY(0)" }, "50%": { transform: "translateY(-12px)" } },
        "glow-pulse": { "0%,100%": { boxShadow: "0 0 20px hsl(var(--accent) / 0.3)" }, "50%": { boxShadow: "0 0 40px hsl(var(--accent) / 0.6)" } },
      },
      animation: {
        "accordion-down": "accordion-down 0.2s ease-out",
        "accordion-up": "accordion-up 0.2s ease-out",
        "fade-in": "fade-in 0.6s ease-out forwards",
        "fade-in-up": "fade-in-up 0.7s ease-out forwards",
        "scale-in": "scale-in 0.5s ease-out forwards",
        "float": "float 6s ease-in-out infinite",
        "glow-pulse": "glow-pulse 3s ease-in-out infinite",
      },
    },
  },
  plugins: [require("tailwindcss-animate")],
} satisfies Config;

```


---

## `src/App.tsx`

```tsx
import { QueryClient, QueryClientProvider } from "@tanstack/react-query";
import { BrowserRouter, Route, Routes } from "react-router-dom";
import { Toaster as Sonner } from "@/components/ui/sonner";
import { Toaster } from "@/components/ui/toaster";
import { TooltipProvider } from "@/components/ui/tooltip";
import Index from "./pages/Index.tsx";
import NotFound from "./pages/NotFound.tsx";

const queryClient = new QueryClient();

const App = () => (
  <QueryClientProvider client={queryClient}>
    <TooltipProvider>
      <Toaster />
      <Sonner />
      <BrowserRouter>
        <Routes>
          <Route path="/" element={<Index />} />
          {/* ADD ALL CUSTOM ROUTES ABOVE THE CATCH-ALL "*" ROUTE */}
          <Route path="*" element={<NotFound />} />
        </Routes>
      </BrowserRouter>
    </TooltipProvider>
  </QueryClientProvider>
);

export default App;

```


---

## `src/pages/Index.tsx`

```tsx
import { Navbar } from "@/components/portfolio/Navbar";
import { Hero } from "@/components/portfolio/Hero";
import { About } from "@/components/portfolio/About";
import { Spotlight } from "@/components/portfolio/Spotlight";
import { Skills } from "@/components/portfolio/Skills";
import { Projects } from "@/components/portfolio/Projects";
import { Experience } from "@/components/portfolio/Experience";
import { Education } from "@/components/portfolio/Education";
import { Volunteer } from "@/components/portfolio/Volunteer";
import { Languages } from "@/components/portfolio/Languages";
import { Contact } from "@/components/portfolio/Contact";
import { Footer } from "@/components/portfolio/Footer";

const Index = () => {
  return (
    <main className="min-h-screen bg-background">
      <Navbar />
      <Hero />
      <About />
      <Spotlight />
      <Skills />
      <Projects />
      <Experience />
      <Education />
      <Volunteer />
      <Languages />
      <Contact />
      <Footer />
    </main>
  );
};

export default Index;

```


---

## `src/components/portfolio/Navbar.tsx`

```tsx
import { useEffect, useState } from "react";
import { Menu, X } from "lucide-react";
import { Button } from "@/components/ui/button";

const links = [
  { href: "#about", label: "About" },
  { href: "#spotlight", label: "Spotlight" },
  { href: "#skills", label: "Skills" },
  { href: "#projects", label: "Projects" },
  { href: "#experience", label: "Experience" },
  { href: "#education", label: "Education" },
  { href: "#contact", label: "Contact" },
];

export const Navbar = () => {
  const [scrolled, setScrolled] = useState(false);
  const [open, setOpen] = useState(false);

  useEffect(() => {
    const onScroll = () => setScrolled(window.scrollY > 20);
    window.addEventListener("scroll", onScroll);
    return () => window.removeEventListener("scroll", onScroll);
  }, []);

  return (
    <header
      className={`fixed top-0 inset-x-0 z-50 transition-all duration-300 ${
        scrolled ? "glass shadow-soft border-b border-border/50" : "bg-transparent"
      }`}
    >
      <nav className="container flex items-center justify-between h-16 md:h-20">
        <a href="#top" className="flex items-center gap-2 font-display font-bold text-lg">
          <span className="w-9 h-9 rounded-xl gradient-primary grid place-items-center text-primary-foreground shadow-glow">N</span>
          <span className="gradient-text">Khairunnisa</span>
        </a>

        <ul className="hidden lg:flex items-center gap-1">
          {links.map((l) => (
            <li key={l.href}>
              <a
                href={l.href}
                className="px-3 py-2 text-sm font-medium text-muted-foreground hover:text-foreground transition-colors rounded-md"
              >
                {l.label}
              </a>
            </li>
          ))}
        </ul>

        <div className="hidden lg:block">
          <Button asChild variant="default" size="sm" className="gradient-primary text-primary-foreground border-0 shadow-soft hover:shadow-glow transition-all">
            <a href="#contact">Let's Talk</a>
          </Button>
        </div>

        <button
          aria-label="Toggle menu"
          className="lg:hidden p-2 rounded-md hover:bg-secondary"
          onClick={() => setOpen(!open)}
        >
          {open ? <X size={20} /> : <Menu size={20} />}
        </button>
      </nav>

      {open && (
        <div className="lg:hidden glass border-t border-border/50 animate-fade-in">
          <ul className="container py-4 flex flex-col gap-1">
            {links.map((l) => (
              <li key={l.href}>
                <a
                  href={l.href}
                  onClick={() => setOpen(false)}
                  className="block px-3 py-2.5 rounded-md text-sm font-medium hover:bg-secondary"
                >
                  {l.label}
                </a>
              </li>
            ))}
          </ul>
        </div>
      )}
    </header>
  );
};

```


---

## `src/components/portfolio/Hero.tsx`

```tsx
import { Button } from "@/components/ui/button";
import { Linkedin, Sparkles, MapPin, ArrowRight } from "lucide-react";
import profile from "@/assets/profile.jpg";

export const Hero = () => {
  return (
    <section id="top" className="relative min-h-screen flex items-center pt-24 pb-16 overflow-hidden gradient-hero">
      {/* Decorative grid */}
      <div className="absolute inset-0 opacity-[0.04] pointer-events-none"
        style={{
          backgroundImage: "linear-gradient(hsl(var(--foreground)) 1px, transparent 1px), linear-gradient(90deg, hsl(var(--foreground)) 1px, transparent 1px)",
          backgroundSize: "60px 60px",
        }}
      />
      {/* Floating orbs */}
      <div className="absolute top-1/4 -left-20 w-72 h-72 rounded-full bg-primary/20 blur-3xl animate-float" />
      <div className="absolute bottom-1/4 -right-20 w-80 h-80 rounded-full bg-accent/20 blur-3xl animate-float" style={{ animationDelay: "2s" }} />

      <div className="container relative z-10 grid lg:grid-cols-2 gap-12 items-center">
        <div className="order-2 lg:order-1 animate-fade-in-up">
          <div className="inline-flex items-center gap-2 px-3 py-1.5 rounded-full bg-secondary border border-border text-xs font-medium mb-6">
            <span className="w-2 h-2 rounded-full bg-accent animate-glow-pulse" />
            Open to opportunities · She/Her
          </div>
          <h1 className="font-display text-4xl sm:text-5xl lg:text-7xl font-bold leading-[1.05] mb-4">
            <span className="gradient-text">Khairunnisa</span>
          </h1>
          <p className="text-lg sm:text-xl text-muted-foreground mb-3 font-medium">
            Student · IT · AI · Coordinator Community · Younger Activist
          </p>
          <div className="flex items-center gap-2 text-sm text-muted-foreground mb-8">
            <MapPin size={16} className="text-accent" />
            Jakarta Barat, Jakarta Raya, Indonesia
          </div>
          <div className="flex flex-wrap gap-3">
            <Button asChild size="lg" className="gradient-primary text-primary-foreground border-0 shadow-soft hover:shadow-glow transition-all group">
              <a href="https://www.linkedin.com/in/khairunnisa-inspire-00722033a/" target="_blank" rel="noopener noreferrer">
                <Linkedin className="mr-2" size={18} /> Hubungi Saya di LinkedIn
              </a>
            </Button>
            <Button asChild size="lg" variant="outline" className="border-2 hover:border-accent hover:text-accent group">
              <a href="#projects">
                <Sparkles className="mr-2" size={18} /> Lihat Proyek AI Saya
                <ArrowRight className="ml-2 group-hover:translate-x-1 transition-transform" size={16} />
              </a>
            </Button>
          </div>
        </div>

        <div className="order-1 lg:order-2 flex justify-center lg:justify-end animate-scale-in">
          <div className="relative">
            <div className="absolute -inset-4 gradient-accent rounded-full blur-2xl opacity-40 animate-glow-pulse" />
            <div className="relative w-64 h-64 sm:w-80 sm:h-80 lg:w-[420px] lg:h-[420px] rounded-full p-1.5 gradient-primary shadow-elegant">
              <img
                src={profile}
                alt="Khairunnisa profile portrait"
                width={420}
                height={420}
                className="w-full h-full rounded-full object-cover bg-background"
              />
            </div>
            <div className="absolute -bottom-4 -left-4 glass border border-border rounded-2xl px-4 py-3 shadow-elegant animate-float" style={{ animationDelay: "1s" }}>
              <p className="text-xs text-muted-foreground">Future Goal</p>
              <p className="font-display font-semibold text-sm">AI/ML, Data Engineer & Social Activist 🚀</p>
            </div>
            <div className="absolute -top-2 -right-2 glass border border-border rounded-2xl px-4 py-3 shadow-elegant animate-float">
              <p className="text-xs text-muted-foreground">Currently</p>
              <p className="font-display font-semibold text-sm">Assistant Mentor DQLab</p>
            </div>
          </div>
        </div>
      </div>
    </section>
  );
};

```


---

## `src/components/portfolio/About.tsx`

```tsx
import { Section } from "./Section";
import { Globe2, BrainCircuit } from "lucide-react";

export const About = () => (
  <Section id="about" eyebrow="About Me" title="Mengenal Khairunnisa">
    <div className="grid lg:grid-cols-3 gap-8">
      <div className="lg:col-span-2 prose prose-lg max-w-none">
        <p className="text-lg leading-relaxed text-muted-foreground">
          Halo! Saya <span className="text-foreground font-semibold">Khairunnisa</span>, seorang mahasiswa jurusan Informatika di
          <span className="text-foreground font-semibold"> Institut Teknologi Sains Bandung</span> yang memiliki ketertarikan besar pada teknologi, komunikasi, dan pengembangan diri.
        </p>
        <p className="text-lg leading-relaxed text-muted-foreground mt-4">
          Saya aktif di berbagai kegiatan sosial dan organisasi yang telah membantu saya mengasah kemampuan
          <span className="text-foreground font-semibold"> leadership, teamwork, dan komunikasi publik</span>. Saat ini saya juga tengah memperdalam bidang
          <span className="gradient-text font-semibold"> Artificial Intelligence (AI)</span> dan pengembangan software berbasis web,
          dengan tujuan menjadi seorang <span className="text-foreground font-semibold">AI Engineer</span> di masa depan.
        </p>
      </div>

      <div className="space-y-4">
        <div className="group p-6 rounded-2xl bg-card border border-border hover-lift">
          <div className="w-12 h-12 rounded-xl gradient-primary grid place-items-center mb-4 shadow-soft">
            <Globe2 className="text-primary-foreground" size={22} />
          </div>
          <h3 className="font-display font-semibold text-lg mb-2">Visi Masa Depan</h3>
          <p className="text-sm text-muted-foreground leading-relaxed">
            Menjadi <span className="text-accent font-semibold">AI Engineer</span> yang aktif berkontribusi di bidang sosial.
          </p>
        </div>
        <div className="group p-6 rounded-2xl bg-card border border-border hover-lift">
          <div className="w-12 h-12 rounded-xl gradient-accent grid place-items-center mb-4 shadow-soft">
            <BrainCircuit className="text-accent-foreground" size={22} />
          </div>
          <h3 className="font-display font-semibold text-lg mb-2">Fokus Teknologi</h3>
          <p className="text-sm text-muted-foreground leading-relaxed">
            <span className="text-foreground font-semibold">AI Engineering</span> & <span className="text-foreground font-semibold">Data</span>.
          </p>
        </div>
      </div>
    </div>
  </Section>
);

```


---

## `src/components/portfolio/Section.tsx`

```tsx
import { ReactNode } from "react";

interface SectionProps {
  id?: string;
  eyebrow?: string;
  title: string;
  subtitle?: string;
  children: ReactNode;
  className?: string;
}

export const Section = ({ id, eyebrow, title, subtitle, children, className = "" }: SectionProps) => {
  return (
    <section id={id} className={`py-20 md:py-28 ${className}`}>
      <div className="container">
        <div className="max-w-2xl mb-12 md:mb-16">
          {eyebrow && (
            <p className="inline-block px-3 py-1 rounded-full bg-accent/10 text-accent text-xs font-semibold tracking-wider uppercase mb-4">
              {eyebrow}
            </p>
          )}
          <h2 className="font-display text-3xl md:text-5xl font-bold mb-4">
            {title}
          </h2>
          {subtitle && <p className="text-lg text-muted-foreground leading-relaxed">{subtitle}</p>}
        </div>
        {children}
      </div>
    </section>
  );
};

```


---

## `src/components/portfolio/Spotlight.tsx`

```tsx
import { Section } from "./Section";
import { Award, Globe } from "lucide-react";
import activity1 from "@/assets/activity-1.jpg";
import activity2 from "@/assets/activity-2.jpg";
import activity3 from "@/assets/activity-3.jpg";
import activity4 from "@/assets/activity-4.jpg";
import activity5 from "@/assets/activity-5.jpg";
import activity6 from "@/assets/activity-6.jpg";
import activity7 from "@/assets/activity-7.jpg";
import activity8 from "@/assets/activity-8.jpg";
import activity9 from "@/assets/activity-9.jpg";
import activity10 from "@/assets/activity-10.jpg";
import activity11 from "@/assets/activity-11.jpg";
import activity12 from "@/assets/activity-12.jpg";
import activity13 from "@/assets/activity-13.jpg";
import activity14 from "@/assets/activity-14.jpg";

const items = [
  {
    icon: Award,
    title: "Google Student Ambassador 2025",
    badge: "Google",
    description:
      'Diakui sebagai "AI adoption leader on campus" di ITSB. Berpengalaman mengadvokasi integrasi AI di lingkungan kampus.',
    gradient: "gradient-primary",
  },
  {
    icon: Globe,
    title: "18th APNG Camp — Asia Pacific Next Generation Fellow",
    badge: "International",
    description:
      "Berpartisipasi dalam camp internasional di Indonesia dengan peserta dari 17 negara untuk membahas masa depan digital regional.",
    gradient: "gradient-accent",
  },
];

const gallery = [
  { src: activity1, caption: "The Next Dimension — Pendidikan Pioneer Muda, Kampus ITSB", alt: "Khairunnisa menjadi pembicara di acara Pendidikan Pioneer Muda ITSB" },
  { src: activity2, caption: "APNG Camp 18 — Society 5.0 in the Asia-Pacific, Pradita University", alt: "Foto bersama seluruh fellow APNG Camp 18 di Pradita University" },
  { src: activity3, caption: "Community Choice Award — APNG Camp 18", alt: "Khairunnisa bersama tim menerima Community Choice Award di APNG Camp 18" },
  { src: activity4, caption: "Google Student Ambassador 2025 — AI Adoption Leader Award", alt: "Trofi penghargaan Google Student Ambassador 2025" },
  { src: activity5, caption: "Ring the Bell for Gender Equality 2026 — Indonesia Stock Exchange (IDX)", alt: "Foto bersama peserta Ring the Bell for Gender Equality 2026 di IDX" },
  { src: activity6, caption: "Badan Ekraf Developer Day 2025 — Accelerating Creative Transformation", alt: "Khairunnisa bersama peserta Badan Ekraf Developer Day 2025" },
  { src: activity7, caption: "Indonesia Summit 2025 — Bersama Cinta Laura Kiehl", alt: "Khairunnisa berfoto bersama Cinta Laura di Indonesia Summit 2025" },
  { src: activity8, caption: "Microsoft Elevate x Dicoding x NTT Data — Training Program", alt: "Foto bersama peserta program Microsoft Elevate, Dicoding, dan NTT Data" },
  { src: activity9, caption: "Ministry of Foreign Affairs RI — Diplomatic Engagement 2025", alt: "Khairunnisa bersama tamu di acara Kementerian Luar Negeri RI 2025" },
  { src: activity10, caption: "Diplomatic Meeting — Bersama Diplomat Internasional", alt: "Khairunnisa bersama diplomat internasional dalam pertemuan resmi" },
  { src: activity11, caption: "Forum Diskusi & Networking — Kolaborasi Lintas Sektor", alt: "Khairunnisa bersama peserta forum diskusi dan networking" },
  { src: activity12, caption: "Public Speaking — Ring the Bell for Gender Equality 2026 di IDX", alt: "Khairunnisa berbicara di podium Ring the Bell for Gender Equality 2026 di Indonesia Stock Exchange" },
  { src: activity13, caption: "Badan Ekraf Developer Day 2025 — Networking Session", alt: "Khairunnisa bersama peserta networking di Badan Ekraf Developer Day 2025" },
  { src: activity14, caption: "Diskusi Kelas — Kolaborasi & Pembelajaran", alt: "Khairunnisa bersama rekan dalam sesi diskusi kelas" },
];

export const Spotlight = () => (
  <Section
    id="spotlight"
    eyebrow="Achievement Spotlight"
    title="Pencapaian Utama"
    subtitle="Pengakuan dan kesempatan yang membentuk perjalanan saya di teknologi dan komunitas global."
  >
    <div className="grid md:grid-cols-2 gap-6">
      {items.map((item, i) => (
        <div
          key={item.title}
          className="group relative p-8 rounded-3xl bg-card border border-border hover-lift overflow-hidden"
        >
          <div className={`absolute -top-20 -right-20 w-48 h-48 rounded-full ${item.gradient} opacity-10 blur-2xl group-hover:opacity-20 transition-opacity`} />
          <div className="relative">
            <div className={`w-16 h-16 rounded-2xl ${item.gradient} grid place-items-center mb-6 shadow-soft`}>
              <item.icon className={i === 0 ? "text-primary-foreground" : "text-accent-foreground"} size={28} />
            </div>
            <span className="inline-block px-2.5 py-1 rounded-md bg-secondary text-xs font-semibold mb-3">
              {item.badge}
            </span>
            <h3 className="font-display text-xl md:text-2xl font-bold mb-3 leading-tight">
              {item.title}
            </h3>
            <p className="text-muted-foreground leading-relaxed">{item.description}</p>
          </div>
        </div>
      ))}
    </div>

    <div className="mt-12">
      <h3 className="font-display text-xl md:text-2xl font-bold mb-6 text-center">Galeri Aktivitas</h3>
      <div className="grid sm:grid-cols-2 lg:grid-cols-4 gap-5">
        {gallery.map((g) => (
          <figure key={g.caption} className="group rounded-2xl overflow-hidden bg-card border border-border hover-lift">
            <div className="aspect-[4/3] overflow-hidden">
              <img
                src={g.src}
                alt={g.alt}
                loading="lazy"
                className="w-full h-full object-cover group-hover:scale-105 transition-transform duration-500"
              />
            </div>
            <figcaption className="p-4 text-xs text-muted-foreground leading-relaxed">{g.caption}</figcaption>
          </figure>
        ))}
      </div>
    </div>
  </Section>
);

```


---

## `src/components/portfolio/Skills.tsx`

```tsx
import { Section } from "./Section";
import { Sparkles, Code2, Wrench } from "lucide-react";

const groups = [
  {
    icon: Sparkles,
    title: "Top Skills",
    description: "Keahlian inti yang paling menonjol",
    skills: ["Prompt Engineering", "Artificial Intelligence (AI)", "Renewable Energy", "Public Speaking", "Strategic Public Relations Planning"],
    accent: "gradient-primary",
  },
  {
    icon: Code2,
    title: "Tech & Data",
    description: "Fundamental teknis & data",
    skills: ["Data Cleansing (R, Excel)", "C++ Basics", "Calculus", "Linear Algebra", "Computer Vision (EcoScan AI)"],
    accent: "gradient-accent",
  },
  {
    icon: Wrench,
    title: "Tools & Platforms",
    description: "Stack & ecosystem yang dikuasai",
    skills: ["Microsoft Fabric", "PySpark", "Python (Pandas)", "Scikit-Learn", "Azure Blob Storage", "MLflow", "Flask", "SQLite", "Bootstrap 5", "Canva", "Meta Insights"],
    accent: "gradient-primary",
  },
];

export const Skills = () => (
  <Section
    id="skills"
    eyebrow="Skills"
    title="Keahlian & Kompetensi"
    subtitle="Kombinasi keahlian teknis, analitis, dan komunikasi yang dikembangkan melalui proyek nyata dan organisasi."
    className="bg-secondary/30"
  >
    <div className="grid md:grid-cols-3 gap-6">
      {groups.map((g) => (
        <div key={g.title} className="p-6 rounded-2xl bg-card border border-border hover-lift">
          <div className={`w-12 h-12 rounded-xl ${g.accent} grid place-items-center mb-4 shadow-soft`}>
            <g.icon className="text-primary-foreground" size={20} />
          </div>
          <h3 className="font-display text-xl font-bold mb-1">{g.title}</h3>
          <p className="text-sm text-muted-foreground mb-5">{g.description}</p>
          <div className="flex flex-wrap gap-2">
            {g.skills.map((s) => (
              <span
                key={s}
                className="px-3 py-1.5 text-xs font-medium rounded-full bg-secondary border border-border hover:border-accent hover:text-accent transition-colors"
              >
                {s}
              </span>
            ))}
          </div>
        </div>
      ))}
    </div>
  </Section>
);

```


---

## `src/components/portfolio/Projects.tsx`

```tsx
import { Section } from "./Section";
import { Database, HeartPulse, Wallet, Recycle } from "lucide-react";

const projects = [
  {
    icon: Database,
    role: "AI Engineer Enthusiast",
    title: "Preparing Data for AI Models using Microsoft Fabric",
    subtitle: "Simulasi End-to-End",
    description:
      'Mengolah raw data ritel (oj_sales_data) menjadi AI-ready data dengan menerapkan prinsip "Garbage In, Garbage Out". Workflow: Data Ingestion (PySpark via Azure Blob Storage) → Data Cleansing & Transformation (Pandas, datetime/numerical casting) → EDA (Data Wrangler untuk validasi kualitas 0% missing/duplicates).',
    tags: ["Microsoft Fabric", "PySpark", "Python", "Azure", "Data Wrangler", "Data Engineering"],
    accent: "from-primary to-primary-glow",
  },
  {
    icon: HeartPulse,
    title: "Klasifikasi Penyakit Jantung",
    subtitle: "Mini-Project — Heart Disease Prediction",
    description:
      "Proyek Machine Learning menggunakan Python dan Heart Dataset dari Kaggle untuk memprediksi kemungkinan penyakit jantung berdasarkan fitur kesehatan pasien. Mencapai akurasi awal 74% menggunakan Support Vector Classifier (SVC).",
    tags: ["Data Science", "Machine Learning", "Python", "Pandas", "Scikit-Learn", "SVC"],
    accent: "from-accent to-accent-glow",
  },
  {
    icon: Wallet,
    title: "Sistem Pengatur Keuangan Perusahaan",
    subtitle: "Web Application",
    description:
      "Aplikasi web untuk mengatur dan menganalisis transaksi keuangan perusahaan. Fitur: Login Admin, Dashboard Keuangan (total kas, pemasukan, pengeluaran), serta Laporan Bulanan Otomatis (CSV/Excel).",
    tags: ["Flask", "Python", "SQLite", "SQLAlchemy", "Pandas", "Bootstrap 5"],
    accent: "from-primary to-accent",
  },
  {
    icon: Recycle,
    title: 'Konsep Aplikasi "EcoScan AI"',
    subtitle: "Concept Design",
    description:
      "Desain konsep aplikasi manajemen sampah berbasis Computer Vision yang membantu pengguna mengidentifikasi dan memilah sampah secara otomatis untuk mendukung sustainability.",
    tags: ["Concept", "AI", "Computer Vision", "Sustainability"],
    accent: "from-accent to-primary",
  },
];

export const Projects = () => (
  <Section
    id="projects"
    eyebrow="Projects"
    title="Proyek Pilihan"
    subtitle="Penerapan praktis dari pembelajaran AI, data engineering, dan pengembangan web."
  >
    <div className="grid md:grid-cols-2 gap-6">
      {projects.map((p) => (
        <article
          key={p.title}
          className="group relative p-7 rounded-3xl bg-card border border-border hover-lift overflow-hidden"
        >
          <div className={`absolute inset-0 bg-gradient-to-br ${p.accent} opacity-0 group-hover:opacity-[0.04] transition-opacity`} />
          <div className="relative">
            <div className={`w-14 h-14 rounded-2xl bg-gradient-to-br ${p.accent} grid place-items-center mb-5 shadow-soft`}>
              <p.icon className="text-primary-foreground" size={24} />
            </div>
            {p.role && (
              <p className="text-xs font-semibold tracking-wider uppercase text-accent mb-2">{p.role}</p>
            )}
            <h3 className="font-display text-xl font-bold mb-1 leading-tight">{p.title}</h3>
            {p.subtitle && <p className="text-sm text-muted-foreground mb-3 italic">{p.subtitle}</p>}
            <p className="text-sm text-muted-foreground leading-relaxed mb-5">{p.description}</p>
            <div className="flex flex-wrap gap-2">
              {p.tags.map((t) => (
                <span key={t} className="px-2.5 py-1 text-xs font-medium rounded-md bg-secondary border border-border">
                  {t}
                </span>
              ))}
            </div>
          </div>
        </article>
      ))}
    </div>
  </Section>
);

```


---

## `src/components/portfolio/Experience.tsx`

```tsx
import { Section } from "./Section";
import { Briefcase } from "lucide-react";

const experiences = [
  {
    company: "MySkill",
    role: "Campus Ambassador (Paruh Waktu)",
    period: "Feb 2026 — Saat ini",
    description: "Fokus: Communication, Pengembangan Personal.",
  },
  {
    company: "HUMI — PT Humpuss Maritim Internasional Tbk",
    role: "Social Media Marketing Specialist (Kontrak)",
    period: "Jan 2026 — Saat ini",
    description:
      "Perencanaan, pengelolaan, dan optimalisasi konten media sosial (Instagram, LinkedIn) untuk brand awareness dan engagement. Menganalisis performa konten menggunakan insight & analytics.",
  },
  {
    company: "Partai GOLKAR",
    role: "AMPG Anggota Biro Digital (Purnawaktu)",
    period: "Jan 2026 — Saat ini",
    description: "Focus: Programming, PHP.",
  },
  {
    company: "BLACKBOX.AI",
    role: "Content Creator (Jarak jauh)",
    period: "Jan 2026 — Saat ini",
    description: "Focus: AI Prompting, Prompt Engineering.",
  },
  {
    company: "Generasi Energi Bersih (Gen B) Jakarta Selatan",
    role: "Koordinator Pengembangan Relawan",
    period: "2025 — Saat ini",
    description:
      "Terpilih sebagai Koordinator Pengembangan Relawan Gen B Jaksel: (1) mengembangkan & mengelola program pelatihan relawan; (2) mengkoordinasikan kegiatan pelatihan & pengembangan; (3) meningkatkan kualitas relawan melalui evaluasi & pemantauan; (4) menjalin kerja sama dengan organisasi lain & stakeholder. Fokus: Organizational Development & Leadership Development.",
  },
  {
    company: "DQLab",
    role: "Project Based — Mentor Assistant (Kontrak)",
    period: "Des 2025 — Saat ini",
    description:
      "Menjawab pertanyaan teknis (SQL, Python, Excel) di komunitas, mendampingi project-based learning, debugging dasar.",
  },
  {
    company: "Kunci Hukum Indonesia",
    role: "Community Development Intern (Magang)",
    period: "Des 2025 — Mar 2026 · 4 bln",
    description:
      "Community Development, Strategic Communications, dan keahlian terkait. Mendukung program pengembangan komunitas dan komunikasi strategis organisasi.",
  },
  {
    company: "DQLab",
    role: "Project Based — Admin Community (Kontrak)",
    period: "Agu 2025 — Nov 2025",
    description:
      "Mengelola grup komunitas online, aktivasi kegiatan daring, meningkatkan keterlibatan anggota.",
  },
  {
    company: "PT Hatmoko Karya Terdepan",
    role: "Sales And Marketing Specialist (Magang · Jarak jauh)",
    period: "Jul 2025 — Sep 2025 · 3 bln",
    description: "Sales, Pemasaran, dan Strategi Pemasaran.",
  },
  {
    company: "Rumah Relawan Peduli",
    role: "The Core Team Jabodetabek (Magang)",
    period: "Feb 2025 — Agu 2025 · 7 bln",
    description: "Bagian dari core team Jabodetabek mendukung kegiatan kerelawanan lintas wilayah.",
  },
  {
    company: "Nextage Power",
    role: "Diplomacy Division (Purnawaktu)",
    period: "Mar 2025 — Jul 2025 · 5 bln",
    description:
      "Membangun relasi & kerja sama nasional/internasional, mengelola komunikasi dengan pihak eksternal (negosiasi, pertemuan, korespondensi), mewakili organisasi di forum internasional, menganalisis situasi politik/ekonomi/sosial, serta mempromosikan kepentingan organisasi melalui diplomasi efektif. Keahlian: Diplomacy, Public Diplomacy, +9 keahlian.",
  },
  {
    company: "Lingkar Sahabat Yatim (LSY)",
    role: "Social Media Management (Purnawaktu)",
    period: "Jan 2025 — Jun 2025 · 6 bln",
    description:
      "Membuat & mengelola akun media sosial perusahaan, menyusun profil akun, mengkoordinasi seluruh anggota tim, mengunggah konten, memantau & merespons komentar/pertanyaan/keluhan, serta menyusun rencana untuk meningkatkan engagement dan konversi.",
  },
  {
    company: "SMA Nurul Ilmi Darunnajah 14",
    role: "Chief of Central Language Section (Purnawaktu · Di lokasi)",
    period: "Jun 2023 — Jun 2024 · 1 thn 1 bln",
    description:
      "Mengkoordinasi seluruh anggota pesantren untuk menggunakan bahasa Inggris & Arab sebagai 'Crown of Language', menyusun program kerja kebahasaan, menganalisis kefasihan anggota, menyusun SOP berbahasa, serta menerapkan sanksi atas pelanggaran berbahasa Indonesia di lingkungan asrama.",
  },
];

export const Experience = () => (
  <Section
    id="experience"
    eyebrow="Experience"
    title="Perjalanan Profesional"
    subtitle="Kontribusi nyata di komunitas, teknologi, dan komunikasi."
    className="bg-secondary/30"
  >
    <div className="relative max-w-3xl mx-auto">
      {/* Timeline line */}
      <div className="absolute left-4 md:left-1/2 top-0 bottom-0 w-px bg-gradient-to-b from-primary via-accent to-transparent md:-translate-x-1/2" />

      <div className="space-y-10">
        {experiences.map((e, i) => (
          <div
            key={i}
            className={`relative grid md:grid-cols-2 gap-6 md:gap-12 items-start ${
              i % 2 === 0 ? "" : "md:[&>*:first-child]:order-2"
            }`}
          >
            {/* Dot */}
            <div className="absolute left-4 md:left-1/2 top-6 -translate-x-1/2 w-4 h-4 rounded-full gradient-accent ring-4 ring-background shadow-glow z-10" />

            <div className={`pl-12 md:pl-0 ${i % 2 === 0 ? "md:text-right md:pr-8" : "md:pl-8"}`}>
              <p className="text-xs font-semibold tracking-wider uppercase text-accent">{e.period}</p>
              <h3 className="font-display text-xl font-bold mt-1">{e.company}</h3>
            </div>
            <div className={`pl-12 md:pl-0 ${i % 2 === 0 ? "md:pl-8" : "md:text-right md:pr-8"}`}>
              <div className="p-5 rounded-2xl bg-card border border-border hover-lift inline-block text-left">
                <div className="flex items-center gap-2 mb-2">
                  <Briefcase size={16} className="text-accent" />
                  <p className="font-semibold">{e.role}</p>
                </div>
                <p className="text-sm text-muted-foreground leading-relaxed">{e.description}</p>
              </div>
            </div>
          </div>
        ))}
      </div>
    </div>
  </Section>
);

```


---

## `src/components/portfolio/Education.tsx`

```tsx
import { Section } from "./Section";
import { GraduationCap, BadgeCheck } from "lucide-react";

const education = [
  { school: "Institut Teknologi Sains Bandung (ITSB)", detail: "Informatika", period: "Jul 2025 — Agu 2027" },
  { school: "SMA Muhammadiyah 18 Jakarta", detail: "Natural Sciences", period: "Jun 2024 — Mei 2025" },
];

const certs = [
  { title: "Ms. Office Terapan", issuer: "LPK Muhammadiyah Jakarta", date: "Mei 2025", note: "Skor 92 — Ms. Excel Terapan" },
  { title: "Berinovasi dengan AI", issuer: "Plan International", date: "Des 2025" },
  { title: "R Fundamental for Data Science", issuer: "DQLab", date: "Des 2025", note: "R, Data Science, +2 keahlian" },
  { title: "Introduction to Financial Literacy", issuer: "Dicoding Indonesia", date: "Des 2025", note: "ID: 98XWO1K6LZM3 · Berlaku s.d. Des 2028" },
  { title: "Sertifikat Penyelesaian Kursus Artificial Intelligence", issuer: "BISA AI Academy", date: "Des 2025", note: "ID: 2025/506/49203 · Berlaku s.d. Sep 2030" },
  { title: "Dasar dan Penggunaan Generatif AI", issuer: "CODEPOLITAN", date: "Sep 2025", note: "ID: CP-RAI/2025/09/1767" },
  { title: "Prompt Engineering", issuer: "Sololearn", date: "Sep 2025", note: "AI, Prompt Engineering, +2 keahlian" },
  { title: "Social Media Marketing with AI", issuer: "Sololearn", date: "Agu 2025" },
  { title: "Tackling Plastic Pollution Masterclass", issuer: "ASEAN Youth Organization", date: "Jul 2025", note: "ID: #2f89ed3a04272f89" },
  { title: "Internet Introduction", issuer: "MySkill", date: "Jun 2025", note: "ID: MS-13/6/2025-iFOOFNh99u8s2fj11GF4" },
  { title: "Memulai Pemrograman dengan Python", issuer: "Dicoding Indonesia", date: "Mei 2025", note: "ID: 72ZD5L40VZYW · Berlaku s.d. Mei 2028" },
  { title: "Korean Language Beginner Batch 1", issuer: "KT&G SangSanguniv", date: "Feb 2025", note: "Hangeul" },
  { title: "Anggota Pelajar Penggerak Merah Putih", issuer: "Kementerian Pendidikan dan Kebudayaan RI", date: "Jan 2025", note: "ID: PPMP-AB2/2025-I/5828" },
  { title: "Siswa Satu Tapak Suci Putera Muhammadiyah", issuer: "Tapak Suci Putera Muhammadiyah", date: "Des 2022", note: "Silat, Bela Diri" },
  { title: "Memorizing of Holy Quran 2 Juz", issuer: "LTQN", date: "Jan 2023" },
];

export const Education = () => (
  <Section id="education" eyebrow="Education & Certifications" title="Pendidikan & Sertifikasi">
    <div className="grid lg:grid-cols-2 gap-8">
      <div>
        <div className="flex items-center gap-3 mb-6">
          <div className="w-10 h-10 rounded-xl gradient-primary grid place-items-center">
            <GraduationCap className="text-primary-foreground" size={20} />
          </div>
          <h3 className="font-display text-2xl font-bold">Pendidikan</h3>
        </div>
        <div className="space-y-4">
          {education.map((e) => (
            <div key={e.school} className="p-6 rounded-2xl bg-card border border-border hover-lift">
              <p className="text-xs font-semibold uppercase tracking-wider text-accent mb-1">{e.period}</p>
              <h4 className="font-display text-lg font-bold">{e.school}</h4>
              <p className="text-sm text-muted-foreground mt-1">{e.detail}</p>
            </div>
          ))}
        </div>
      </div>

      <div>
        <div className="flex items-center gap-3 mb-6">
          <div className="w-10 h-10 rounded-xl gradient-accent grid place-items-center">
            <BadgeCheck className="text-accent-foreground" size={20} />
          </div>
          <h3 className="font-display text-2xl font-bold">Lisensi & Sertifikasi</h3>
        </div>
        <div className="space-y-4">
          {certs.map((c) => (
            <div key={c.title} className="p-6 rounded-2xl bg-card border border-border hover-lift">
              <div className="flex items-start justify-between gap-4">
                <div>
                  <h4 className="font-display font-bold">{c.title}</h4>
                  <p className="text-sm text-muted-foreground mt-0.5">{c.issuer}</p>
                  {c.note && <p className="text-xs text-accent font-medium mt-2">{c.note}</p>}
                </div>
                <span className="text-xs font-medium text-muted-foreground whitespace-nowrap">{c.date}</span>
              </div>
            </div>
          ))}
        </div>
      </div>
    </div>
  </Section>
);

```


---

## `src/components/portfolio/Volunteer.tsx`

```tsx
import { Section } from "./Section";
import { Heart, Trophy } from "lucide-react";

const volunteer = [
  { org: "Green Generation Indonesia", role: "Lingkungan — \"Green Generation Beraksi 2.0\"", date: "Jan 2025" },
  { org: "Global Peace Foundation Indonesia", role: "Hak Asasi Manusia", date: "Feb 2025" },
];

const awards = [
  { title: "Peringkat 3 Kelas 4 TMI", issuer: "Pondok Pesantren Nurul Ilmi Darunnajah 14", date: "Mei 2023" },
];

export const Volunteer = () => (
  <Section
    id="volunteer"
    eyebrow="Community"
    title="Sukarela & Penghargaan"
    className="bg-secondary/30"
  >
    <div className="grid md:grid-cols-2 gap-8">
      <div>
        <div className="flex items-center gap-3 mb-6">
          <div className="w-10 h-10 rounded-xl gradient-accent grid place-items-center">
            <Heart className="text-accent-foreground" size={20} />
          </div>
          <h3 className="font-display text-2xl font-bold">Kegiatan Sukarela</h3>
        </div>
        <div className="space-y-4">
          {volunteer.map((v) => (
            <div key={v.org} className="p-6 rounded-2xl bg-card border border-border hover-lift">
              <div className="flex justify-between items-start gap-3">
                <div>
                  <h4 className="font-display font-bold">{v.org}</h4>
                  <p className="text-sm text-muted-foreground mt-1">{v.role}</p>
                </div>
                <span className="text-xs font-medium text-muted-foreground whitespace-nowrap">{v.date}</span>
              </div>
            </div>
          ))}
        </div>
      </div>

      <div>
        <div className="flex items-center gap-3 mb-6">
          <div className="w-10 h-10 rounded-xl gradient-primary grid place-items-center">
            <Trophy className="text-primary-foreground" size={20} />
          </div>
          <h3 className="font-display text-2xl font-bold">Penghargaan</h3>
        </div>
        <div className="space-y-4">
          {awards.map((a) => (
            <div key={a.title} className="p-6 rounded-2xl bg-card border border-border hover-lift">
              <div className="flex justify-between items-start gap-3">
                <div>
                  <h4 className="font-display font-bold">{a.title}</h4>
                  <p className="text-sm text-muted-foreground mt-1">{a.issuer}</p>
                </div>
                <span className="text-xs font-medium text-muted-foreground whitespace-nowrap">{a.date}</span>
              </div>
            </div>
          ))}
        </div>
      </div>
    </div>
  </Section>
);

```


---

## `src/components/portfolio/Languages.tsx`

```tsx
import { Section } from "./Section";
import { Languages as LangIcon } from "lucide-react";

const langs = [
  { name: "Bahasa Inggris", level: "Tingkat Profesional", score: "Duolingo 103", value: 85 },
  { name: "Bahasa Mandarin", level: "Tingkat Dasar", score: "Duolingo 13", value: 20 },
];

export const Languages = () => (
  <Section id="languages" eyebrow="Languages" title="Bahasa">
    <div className="grid md:grid-cols-2 gap-6 max-w-4xl">
      {langs.map((l) => (
        <div key={l.name} className="p-7 rounded-2xl bg-card border border-border hover-lift">
          <div className="flex items-start justify-between mb-4">
            <div className="flex items-center gap-3">
              <div className="w-11 h-11 rounded-xl gradient-primary grid place-items-center">
                <LangIcon className="text-primary-foreground" size={20} />
              </div>
              <div>
                <h3 className="font-display text-lg font-bold">{l.name}</h3>
                <p className="text-sm text-muted-foreground">{l.level}</p>
              </div>
            </div>
            <span className="text-xs font-semibold px-2.5 py-1 rounded-md bg-secondary border border-border">
              {l.score}
            </span>
          </div>
          <div className="h-2 rounded-full bg-secondary overflow-hidden">
            <div
              className="h-full gradient-accent rounded-full transition-all duration-1000"
              style={{ width: `${l.value}%` }}
            />
          </div>
        </div>
      ))}
    </div>
  </Section>
);

```


---

## `src/components/portfolio/Contact.tsx`

```tsx
import { useState } from "react";
import { Section } from "./Section";
import { Button } from "@/components/ui/button";
import { Input } from "@/components/ui/input";
import { Textarea } from "@/components/ui/textarea";
import { Label } from "@/components/ui/label";
import { Linkedin, Instagram, Github, Send, Mail } from "lucide-react";
import { toast } from "@/hooks/use-toast";

export const Contact = () => {
  const [form, setForm] = useState({ name: "", email: "", message: "" });

  const onSubmit = (e: React.FormEvent) => {
    e.preventDefault();
    if (!form.name || !form.email || !form.message) {
      toast({ title: "Lengkapi formulir", description: "Mohon isi semua field." });
      return;
    }
    toast({
      title: "Pesan terkirim! 🚀",
      description: `Terima kasih ${form.name}, saya akan segera merespons.`,
    });
    setForm({ name: "", email: "", message: "" });
  };

  return (
    <Section
      id="contact"
      eyebrow="Get in Touch"
      title="Mari Berkolaborasi & Terkoneksi!"
      subtitle="Terbuka untuk kesempatan kolaborasi, magang, atau proyek pengembangan diri di dunia teknologi dan komunikasi."
    >
      <div className="grid lg:grid-cols-5 gap-8">
        <form onSubmit={onSubmit} className="lg:col-span-3 p-8 rounded-3xl bg-card border border-border shadow-soft space-y-5">
          <div className="grid sm:grid-cols-2 gap-4">
            <div className="space-y-2">
              <Label htmlFor="name">Nama</Label>
              <Input id="name" value={form.name} onChange={(e) => setForm({ ...form, name: e.target.value })} placeholder="Nama Anda" />
            </div>
            <div className="space-y-2">
              <Label htmlFor="email">Email</Label>
              <Input id="email" type="email" value={form.email} onChange={(e) => setForm({ ...form, email: e.target.value })} placeholder="email@anda.com" />
            </div>
          </div>
          <div className="space-y-2">
            <Label htmlFor="message">Pesan</Label>
            <Textarea id="message" rows={6} value={form.message} onChange={(e) => setForm({ ...form, message: e.target.value })} placeholder="Ceritakan tentang proyek atau ide kolaborasi Anda..." />
          </div>
          <Button type="submit" size="lg" className="gradient-primary text-primary-foreground border-0 shadow-soft hover:shadow-glow w-full sm:w-auto">
            <Send size={18} className="mr-2" /> Kirim Pesan
          </Button>
        </form>

        <div className="lg:col-span-2 space-y-4">
          <div className="p-6 rounded-2xl bg-card border border-border">
            <h3 className="font-display text-lg font-bold mb-4">Terhubung di Sosial Media</h3>
            <div className="space-y-3">
              <a
                href="https://www.linkedin.com/in/khairunnisa-inspire-00722033a/"
                target="_blank"
                rel="noopener noreferrer"
                className="flex items-center gap-3 p-3 rounded-xl border border-border hover:border-accent hover:bg-accent/5 transition-all"
              >
                <div className="w-10 h-10 rounded-lg gradient-primary grid place-items-center">
                  <Linkedin size={18} className="text-primary-foreground" />
                </div>
                <div>
                  <p className="font-semibold text-sm">LinkedIn</p>
                  <p className="text-xs text-muted-foreground">Khairunnisa Inspire</p>
                </div>
              </a>
              <a
                href="https://www.instagram.com/khairunnisa.inspire/"
                target="_blank"
                rel="noopener noreferrer"
                className="flex items-center gap-3 p-3 rounded-xl border border-border hover:border-accent hover:bg-accent/5 transition-all"
              >
                <div className="w-10 h-10 rounded-lg gradient-accent grid place-items-center">
                  <Instagram size={18} className="text-accent-foreground" />
                </div>
                <div>
                  <p className="font-semibold text-sm">Instagram</p>
                  <p className="text-xs text-muted-foreground">@khairunnisa.inspire</p>
                </div>
              </a>
              <a
                href="https://github.com/nisa162"
                target="_blank"
                rel="noopener noreferrer"
                className="flex items-center gap-3 p-3 rounded-xl border border-border hover:border-accent hover:bg-accent/5 transition-all"
              >
                <div className="w-10 h-10 rounded-lg gradient-primary grid place-items-center">
                  <Github size={18} className="text-primary-foreground" />
                </div>
                <div>
                  <p className="font-semibold text-sm">GitHub</p>
                  <p className="text-xs text-muted-foreground">@nisa162</p>
                </div>
              </a>
            </div>
          </div>
          <a
            href="mailto:khairunnisanisa5767@gmail.com"
            className="block p-6 rounded-2xl gradient-primary text-primary-foreground hover:shadow-glow transition-all"
          >
            <Mail size={22} className="mb-3" />
            <p className="text-sm opacity-80">Direct email</p>
            <p className="font-semibold break-all">khairunnisanisa5767@gmail.com</p>
          </a>
        </div>
      </div>
    </Section>
  );
};

```


---

## `src/components/portfolio/Footer.tsx`

```tsx
export const Footer = () => (
  <footer className="border-t border-border py-10 bg-secondary/30">
    <div className="container flex flex-col sm:flex-row items-center justify-between gap-4 text-sm text-muted-foreground">
      <p>© 2026 Khairunnisa. All Rights Reserved.</p>
      <p className="flex items-center gap-2">
        Built with <span className="gradient-text font-semibold">passion</span> in Jakarta · Khairunnisa
      </p>
    </div>
  </footer>
);

```
