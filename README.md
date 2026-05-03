# normapimienta
web
/**
 * Archivo: /src/App.tsx (Parte 1)
 */
import { motion } from "motion/react";
import { 
  ArrowRight, Linkedin, Mail, Target, Users, TrendingUp, 
  ShieldCheck, Globe, BookOpen, ChevronRight, MessageSquare, Award
} from "lucide-react";

// Datos de contacto
const EMAIL = "normapimienta@yahoo.com.ar";
const LINKEDIN_URL = "https://www.linkedin.com/in/norma-pimienta-9436a4235/";

// Imágenes (Rutas locales)
const PROFILE_IMAGE = "/input_file_0.png";
const BOOK_IMAGE = "/input_file_1.png";

export default function App() {
  const fadeInUp = {
    initial: { opacity: 0, y: 30 },
    whileInView: { opacity: 1, y: 0 },
    viewport: { once: true },
    transition: { duration: 0.8, ease: "easeOut" }
  };

  return (
    <div className="min-h-screen selection:bg-luxury-violet selection:text-white">
      {/* Navegación */}
      <nav className="fixed top-0 left-0 right-0 z-50 bg-premium-white/80 backdrop-blur-md border-b border-luxury-violet/5">
        <div className="max-w-7xl mx-auto px-6 h-20 flex items-center justify-between">
          <div className="text-luxury-violet font-serif text-xl font-semibold tracking-tight">
            NORMA PIMIENTA
          </div>
          <div className="hidden md:flex gap-8 text-sm uppercase tracking-widest font-medium text-gray-500">
            <a href="#sobre-mi" className="hover:text-luxury-violet transition-colors">Sobre Mí</a>
            <a href="#expertise" className="hover:text-luxury-violet transition-colors">Expertise</a>
            <a href="#proyecto" className="hover:text-luxury-violet transition-colors">Focus</a>
            <a href="#contacto" className="hover:text-luxury-violet transition-colors">Contacto</a>
          </div>
          <motion.a 
            href={`mailto:${EMAIL}`}
            whileHover={{ scale: 1.05 }}
            whileTap={{ scale: 0.95 }}
            className="bg-luxury-violet text-white px-6 py-2 rounded-full text-xs uppercase tracking-widest font-semibold hover:bg-opacity-90 transition-all shadow-sm"
          >
            Conversar
          </motion.a>
        </div>
      </nav>
{/* Hero Section */}
      <section className="relative pt-32 pb-20 md:pt-48 md:pb-32 px-6">
        <div className="max-w-7xl mx-auto">
          <div className="grid lg:grid-cols-2 gap-16 items-center">
            <motion.div 
              initial={{ opacity: 0, x: -50 }}
              animate={{ opacity: 1, x: 0 }}
              transition={{ duration: 1, ease: "easeOut" }}
            >
              <div className="inline-flex items-center gap-2 px-3 py-1 rounded-full bg-soft-gold/10 text-soft-gold border border-soft-gold/20 text-xs font-semibold uppercase tracking-widest mb-6">
                <Target size={14} />
                Capital. Innovación. Tecnología
              </div>
              <h1 className="serif text-6xl md:text-8xl font-medium leading-[0.95] mb-8 tracking-tight text-luxury-violet">
                Norma <br />
                Pimienta
              </h1>
              <p className="text-xl md:text-2xl text-gray-600 mb-8 max-w-lg leading-relaxed font-light">
                Liderando la transición hacia un sistema financiero de impacto real
              </p>
              <p className="text-gray-500 mb-10 max-w-xl leading-relaxed">
                Impulso el re-direccionamiento y circulación del dinero en la nueva economía. <br />
                Trabajo en la intersección entre finanzas, conciencia y tecnología para canalizar capital hacia sistemas productivos reales.
              </p>
              <div className="flex flex-wrap gap-4">
                <a href={`mailto:${EMAIL}`} className="bg-luxury-violet text-white px-8 py-4 rounded-lg flex items-center gap-2 group hover:gap-4 transition-all duration-300 shadow-xl shadow-luxury-violet/20 font-semibold uppercase tracking-widest text-xs">
                  Conversar <ArrowRight size={20} />
                </a>
                <a href="#proyecto" className="bg-white border border-gray-200 text-gray-800 px-8 py-4 rounded-lg hover:bg-gray-50 transition-all font-semibold uppercase tracking-widest text-xs">
                  Ver Proyecto
                </a>
              </div>
            </motion.div>
            
            <motion.div 
              initial={{ opacity: 0, scale: 0.9 }}
              animate={{ opacity: 1, scale: 1 }}
              transition={{ duration: 1.2, ease: "easeOut" }}
              className="relative"
            >
              <div className="aspect-[4/5] rounded-[2rem] overflow-hidden luxury-shadow relative z-10">
                <img src={PROFILE_IMAGE} className="w-full h-full object-cover" alt="Norma Pimienta" />
              </div>
            </motion.div>
          </div>
        </div>
      </section>

      {/* Frase de Impacto */}
      <section className="py-24 bg-luxury-violet text-white overflow-hidden relative">
        <div className="max-w-4xl mx-auto px-6 text-center">
          <motion.div {...fadeInUp}>
            <h2 className="serif text-4xl md:text-5xl mb-12 leading-tight">
              "El problema no es la falta de dinero. <br />
              <span className="gold-gradient italic">Es cómo se direcciona y cómo circula.</span>"
            </h2>
          </motion.div>
        </div>
      </section>
{/* Sobre Mí y Pilares */}
      <section id="sobre-mi" className="py-32 bg-premium-white border-y border-gray-100">
        <div className="max-w-7xl mx-auto px-6">
          <div className="grid lg:grid-cols-2 gap-20 items-center">
            <motion.div {...fadeInUp}>
              <span className="text-soft-gold uppercase tracking-[0.3em] text-xs font-bold mb-4 block">Sobre Mí</span>
              <h2 className="serif text-5xl mb-8 leading-tight"> Una combinación poco común de <span className="italic">experiencia, red y visión</span></h2>
              <p className="text-gray-600 leading-relaxed font-light text-lg mb-6">
                Fui impulsora de la banca ética en Argentina y Chile, conectando finanzas con propósito.
              </p>
              <div className="grid grid-cols-2 gap-4">
                <div className="bg-luxury-violet rounded-3xl p-8 text-white"><div className="text-4xl serif">+20</div><div className="text-xs uppercase opacity-70">Años Trayectoria</div></div>
                <div className="bg-soft-gold rounded-3xl p-8 text-white"><div className="text-4xl serif">3</div><div className="text-xs uppercase opacity-70">Ministerios</div></div>
              </div>
            </motion.div>
          </div>
        </div>
      </section>

      {/* Expertise */}
      <section id="expertise" className="py-32 px-6 bg-white">
        <div className="max-w-7xl mx-auto">
          <h2 className="serif text-5xl text-center mb-20 uppercase tracking-tight">Expertise</h2>
          <div className="grid lg:grid-cols-2 gap-12">
            <div className="space-y-6">
              {["sector privado PyME", "instituciones públicas", "medios de comunicación líderes", "redes estratégicas regionales"].map((item, i) => (
                <div key={i} className="flex gap-4 items-center p-6 bg-gray-50 rounded-2xl border border-gray-100">
                  <ShieldCheck className="text-luxury-violet" />
                  <span className="font-semibold text-gray-700">{item}</span>
                </div>
              ))}
            </div>
            <div className="bg-luxury-violet rounded-[3rem] p-12 text-white">
              <h3 className="serif text-3xl mb-6">Sector Público</h3>
              <p className="text-violet-100 italic">"Comprendo tanto la lógica del mercado como la dinámica institucional."</p>
            </div>
          </div>
        </div>
      </section>
{/* Libro */}
      <section className="py-40 bg-white relative">
        <div className="max-w-7xl mx-auto px-6 grid lg:grid-cols-2 gap-20 items-center">
          <div className="relative group lg:order-2">
            <div className="aspect-[3/4] max-w-sm mx-auto luxury-shadow rounded-xl overflow-hidden rotate-[-2deg]">
              <img src={BOOK_IMAGE} alt="Libro Dinero y Evolución" className="w-full h-full object-cover" />
            </div>
          </div>
          <div className="lg:order-1">
            <h2 className="serif text-4xl md:text-5xl mb-8">“Dinero y Evolución: del materialismo a la No-dualidad”</h2>
            <p className="text-gray-500 mb-10">En esta obra, publicada en 2019, analizo la transición hacia nuevos paradigmas de prosperidad, anticipando las conversaciones actuales sobre el capital consciente y el cambio de Paradigma en relación al DINERO.</p>
          </div>
        </div>
      </section>

      {/* Proyecto Quantum */}
      <section id="proyecto" className="py-32 bg-luxury-violet text-white">
        <div className="max-w-7xl mx-auto px-6">
          <div className="bg-white/5 border border-white/10 rounded-[4rem] p-12 md:p-20 backdrop-blur-2xl">
            <h2 className="serif text-5xl md:text-7xl mb-6">QUANTUM IMPACT FINANCE</h2>
            <p className="text-2xl font-serif italic text-soft-gold mb-12">Venture de Impacto (Pre-seed)</p>
            <p className="text-violet-100 text-lg max-w-2xl">Nueva infraestructura financiera para canalizar inversión hacia activos productivos reales mediante tokenización y AI.</p>
          </div>
        </div>
      </section>
{/* Contacto Final */}
      <section id="contacto" className="py-40 bg-luxury-violet relative text-center">
        <div className="max-w-5xl mx-auto px-6">
          <h2 className="serif text-6xl md:text-8xl text-white mb-10 leading-none">
            El futuro del dinero <br />
            <span className="gold-gradient italic">define nuestra Evolución</span>
          </h2>
          <div className="flex justify-center gap-6">
            <a href={`mailto:${EMAIL}`} className="bg-white text-luxury-violet px-10 py-5 rounded-full font-bold uppercase tracking-widest text-xs">Agendar conversación</a>
            <a href={LINKEDIN_URL} target="_blank" className="bg-transparent border border-white/30 text-white px-10 py-5 rounded-full font-bold uppercase tracking-widest text-xs">LinkedIn</a>
          </div>
        </div>
      </section>

      {/* Footer */}
      <footer className="py-20 bg-premium-white border-t border-gray-100">
        <div className="max-w-7xl mx-auto px-6 flex flex-col md:flex-row justify-between items-center text-[10px] text-gray-400 uppercase tracking-widest font-medium">
          <span>© 2026 Norma Pimienta. Todos los derechos reservados.</span>
          <span>Mendoza, Argentina • impacto real</span>
        </div>
      </footer>
    </div>
  );
}@import url('https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,700;1,400&family=Inter:wght@300;400;600&display=swap');
@import "tailwindcss";

@theme {
  --font-serif: "Cormorant Garamond", serif;
  --font-sans: "Inter", system-ui, sans-serif;
  --color-premium-white: #FAFAFA;
  --color-luxury-violet: #4C1D95;
  --color-soft-gold: #D4AF37;
}

.serif { font-family: var(--font-serif); }

.gold-gradient {
  background: linear-gradient(135deg, #D4AF37 0%, #F5E0A3 50%, #D4AF37 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.luxury-shadow {
  box-shadow: 0 10px 30px -10px rgba(76, 29, 149, 0.1);
}




