# normapimienta
web
import React from 'react';
import { motion } from 'motion/react';
import { 
  ArrowRight, 
  Linkedin, 
  Mail, 
  ChevronRight, 
  ExternalLink,
  MessageSquare,
  Globe,
  Award,
  BookOpen
} from 'lucide-react';

// Assets
const PROFILE_IMAGE = "/input_file_0.png";
const BOOK_IMAGE = "/input_file_1.png";

const EMAIL = "normapimienta@yahoo.com.ar";
const LINKEDIN_URL = "https://www.linkedin.com/in/norma-pimienta-9436a4235/";

export default function App() {
  const fadeInUp = {
    initial: { opacity: 0, y: 30 },
    whileInView: { opacity: 1, y: 0 },
    viewport: { once: true },
    transition: { duration: 0.8, ease: "easeOut" }
  };

  return (
    <div className="min-h-screen bg-[#FDFCFB] text-gray-900 font-sans selection:bg-luxury-violet selection:text-white">
      {/* Navigation */}
      <nav className="fixed top-0 w-full z-50 bg-white/80 backdrop-blur-md border-b border-gray-100">
        <div className="max-w-7xl mx-auto px-6 h-20 flex items-center justify-between">
          <div className="flex items-center gap-2">
            <div className="w-8 h-8 bg-luxury-violet rounded-full flex items-center justify-center text-white font-serif italic text-xl">N</div>
            <span className="serif text-xl tracking-tight font-medium">Norma Pimienta</span>
          </div>
          <div className="hidden md:flex gap-10 text-[10px] uppercase tracking-[0.2em] font-bold text-gray-400">
            <a href="#trayectoria" className="hover:text-luxury-violet transition-colors">Trayectoria</a>
            <a href="#tesis" className="hover:text-luxury-violet transition-colors">Tesis</a>
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
      <section className="pt-40 pb-20 px-6">
        <div className="max-w-7xl mx-auto grid md:grid-cols-2 gap-16 items-center">
          <motion.div 
            initial={{ opacity: 0, x: -30 }}
            animate={{ opacity: 1, x: 0 }}
            transition={{ duration: 1 }}
          >
            <div className="flex items-center gap-3 mb-6">
              <div className="h-[1px] w-12 bg-luxury-violet"></div>
              <span className="text-luxury-violet text-[10px] font-bold uppercase tracking-[0.3em]">Capital. Innovación. Tecnología</span>
            </div>
            <h1 className="serif text-6xl md:text-8xl font-medium leading-[0.95] mb-8 tracking-tight text-luxury-violet">
              Norma <br />
              Pimienta
            </h1>
            <p className="text-xl md:text-2xl text-gray-600 mb-8 max-w-lg leading-relaxed font-light">
              Liderando la transición hacia un sistema financiero de impacto real
            </p>
            <p className="text-gray-500 mb-10 max-w-xl leading-relaxed">
              Trabajo en la intersección entre finanzas, conciencia y tecnología para canalizar capital hacia sistemas productivos reales, anticipando los nuevos modelos de financiamiento productivo.
            </p>
            <div className="flex flex-wrap gap-4">
              <a href={`mailto:${EMAIL}`} className="bg-luxury-violet text-white px-8 py-4 rounded-lg flex items-center gap-2 group hover:gap-4 transition-all duration-300 shadow-xl shadow-luxury-violet/20 font-semibold uppercase tracking-widest text-xs">
                Conversar <ArrowRight size={20} />
              </a>
              <a href="#proyecto" className="bg-white border border-gray-200 text-gray-800 px-8 py-4 rounded-lg hover:bg-gray-50 transition-all font-semibold uppercase tracking-widest text-xs">
                Ver Proyecto
              </a>
            </div>
            <div className="mt-12 flex flex-col gap-2 text-sm text-gray-400 italic">
              <span>Founder de Quantum Impact Finance</span>
              <span>Autora de "Dinero y Evolución"</span>
            </div>
          </motion.div>

          <motion.div 
            initial={{ opacity: 0, scale: 0.95 }}
            animate={{ opacity: 1, scale: 1 }}
            transition={{ duration: 1.2 }}
            className="relative"
          >
            <div className="aspect-[4/5] rounded-[4rem] overflow-hidden grayscale hover:grayscale-0 transition-all duration-1000 shadow-2xl">
              <img 
                src={PROFILE_IMAGE} 
                alt="Norma Pimienta" 
                className="w-full h-full object-cover scale-110 hover:scale-100 transition-transform duration-1000"
                referrerPolicy="no-referrer"
              />
            </div>
            {/* Decors */}
            <div className="absolute -bottom-10 -left-10 w-40 h-40 bg-soft-gold/10 rounded-full blur-3xl -z-10"></div>
            <div className="absolute -top-10 -right-10 w-40 h-40 bg-luxury-violet/10 rounded-full blur-3xl -z-10"></div>
          </motion.div>
        </div>
      </section>

      {/* Trayectoria Section */}
      <section id="trayectoria" className="py-32 bg-white px-6">
        <div className="max-w-7xl mx-auto">
          <div className="grid md:grid-cols-12 gap-12">
            <div className="md:col-span-5">
              <span className="text-[10px] font-bold uppercase tracking-[0.3em] text-gray-400 mb-4 block">Trayectoria</span>
              <h2 className="serif text-4xl mb-8 leading-tight">Experiencia que <br /> define la visión</h2>
              <p className="text-gray-500 leading-relaxed mb-12">
                Con más de dos décadas en el sector financiero y gubernamental, he liderado equipos y proyectos transformadores que integran la gestión pública con la innovación privada.
              </p>
              
              <div className="space-y-12">
                <div className="flex gap-6">
                  <div className="text-luxury-violet font-serif italic text-2xl">01</div>
                  <div>
                    <h4 className="font-bold text-xs uppercase tracking-widest mb-2">Fundadora</h4>
                    <p className="text-gray-600 font-medium italic">Quantum Impact Finance</p>
                    <p className="text-sm text-gray-400 mt-2">Plataforma de ingeniería financiera para la economía real y activos de impacto.</p>
                  </div>
                </div>
                <div className="flex gap-6">
                  <div className="text-luxury-violet font-serif italic text-2xl">02</div>
                  <div>
                    <h4 className="font-bold text-xs uppercase tracking-widest mb-2">Gestión Pública</h4>
                    <p className="text-gray-600 font-medium italic">Directora Nacional de Coordinación Ejecutiva</p>
                    <p className="text-sm text-gray-400 mt-2">Liderazgo en la modernización de procesos y articulación ministerial.</p>
                  </div>
                </div>
              </div>
            </div>

            <div className="md:col-span-7 grid grid-cols-2 gap-4">
              <div className="bg-[#FAF9F6] p-12 rounded-[3rem] flex flex-col justify-center items-center text-center">
                <div className="text-4xl font-serif mb-2">20+</div>
                <div className="text-xs uppercase tracking-widest opacity-70">Años Expertiz</div>
              </div>
              <div className="bg-luxury-violet p-12 rounded-[3rem] text-white flex flex-col justify-center items-center text-center">
                <div className="text-4xl font-serif mb-2">3</div>
                <div className="text-xs uppercase tracking-widest opacity-70">Ministerios Nacionales</div>
              </div>
            </div>
          </div>
        </div>
      </section>

      {/* Tesis Section (Editorial Style) */}
      <section id="tesis" className="py-32 px-6 bg-[#FAF9F6]">
        <div className="max-w-4xl mx-auto">
          <motion.div {...fadeInUp} className="text-center mb-20">
            <span className="text-[10px] font-bold uppercase tracking-[0.3em] text-luxury-violet mb-6 block">Tesis de Pensamiento</span>
            <h2 className="serif text-5xl md:text-7xl mb-8 leading-[1.1]">Finanzas con Conciencia</h2>
            <div className="h-1 w-20 bg-soft-gold mx-auto mb-8"></div>
            <p className="text-xl text-gray-500 italic font-light leading-relaxed">
              "El capital no es sólo un recurso numérico; es una herramienta de evolución que debe alinearse con el propósito productivo y el bienestar sistémico."
            </p>
          </motion.div>

          <div className="grid gap-12">
            <div className="bg-white p-12 rounded-3xl shadow-sm border border-gray-100 flex flex-col md:flex-row gap-10 items-start">
              <div className="w-16 h-16 bg-luxury-violet/5 rounded-2xl flex items-center justify-center shrink-0">
                <Globe className="text-luxury-violet" size={32} />
              </div>
              <div>
                <h3 className="serif text-2xl mb-4">Soberanía de Inversión</h3>
                <p className="text-gray-500 leading-relaxed">Anticipamos la necesidad de democratizar el acceso al capital a través de modelos descentralizados, donde la transparencia y el impacto real sean los pilares de la confianza.</p>
              </div>
            </div>

            <div className="bg-white p-12 rounded-3xl shadow-sm border border-gray-100 flex flex-col md:flex-row gap-10 items-start">
              <div className="w-16 h-16 bg-luxury-violet/5 rounded-2xl flex items-center justify-center shrink-0">
                <Award className="text-luxury-violet" size={32} />
              </div>
              <div>
                <h3 className="serif text-2xl mb-4">Nuevas Arquitecturas</h3>
                <p className="text-gray-500 leading-relaxed">El futuro exige instrumentos que recompensen no solo el retorno financiero, sino la regeneración de los tejidos sociales y productivos de nuestras regiones.</p>
              </div>
            </div>
          </div>
        </div>
      </section>

      {/* Libros Section */}
      <section className="py-32 px-6 overflow-hidden">
        <div className="max-w-7xl mx-auto">
          <div className="grid md:grid-cols-2 gap-20 items-center">
            <div className="relative">
              <motion.div 
                initial={{ rotate: -5 }}
                whileInView={{ rotate: 0 }}
                transition={{ duration: 1 }}
                className="w-full max-w-sm mx-auto shadow-[0_50px_100px_-20px_rgba(0,0,0,0.3)] rounded-lg overflow-hidden"
              >
                <img src={BOOK_IMAGE} alt="Libro Dinero y Evolución" className="w-full object-cover" />
              </motion.div>
              <div className="absolute -bottom-6 -right-6 bg-white p-6 rounded-2xl shadow-xl flex items-center gap-4 border border-gray-100">
                <BookOpen size={24} className="text-luxury-violet" />
                <div>
                  <div className="text-[8px] uppercase tracking-widest text-gray-400 font-bold">Publicado por</div>
                  <div className="text-xs font-bold italic">Grupo Editor Pampia</div>
                </div>
              </div>
            </div>
            <div>
              <span className="text-[10px] font-bold uppercase tracking-[0.3em] text-gray-400 mb-4 block">Literatura & Pensamiento</span>
              <h2 className="serif text-4xl md:text-5xl mb-8 leading-tight">
                “Dinero y Evolución: del materialismo a la No-dualidad”; <br />
                <span className="text-luxury-violet italic">2019, Buenos Aires, Grupo Editor Pampia</span>
              </h2>
              <p className="text-gray-500 mb-10 leading-relaxed">En esta obra, publicada en 2019, analizo la transición hacia nuevos paradigmas de prosperidad, anticipando las conversaciones actuales sobre el capital consciente y el cambio de Paradigma en relación al DINERO.</p>
              
              <div className="space-y-8 text-gray-600">
                <div>
                  <h4 className="text-xs uppercase tracking-widest font-bold mb-3 flex items-center gap-2">
                    <div className="h-1 w-4 bg-soft-gold"></div> Concepto Clave
                  </h4>
                  <p className="italic">La evolución de la consciencia sobre el valor y el intercambio.</p>
                </div>
                <div>
                  <h4 className="text-xs uppercase tracking-widest font-bold mb-3 flex items-center gap-2">
                    <div className="h-1 w-4 bg-soft-gold"></div> Propósito
                  </h4>
                  <p className="italic">Desmitificar la relación con la riqueza para ponerla al servicio de la vida.</p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>

      {/* Proyecto Section (The Vision) */}
      <section id="proyecto" className="py-32 px-6 bg-luxury-violet text-white rounded-[4rem] mx-6">
        <div className="max-w-7xl mx-auto">
          <div className="grid md:grid-cols-2 gap-20 items-center">
            <div>
              <span className="text-[10px] font-bold uppercase tracking-[0.3em] text-white/50 mb-6 block">The Main Focus</span>
              <h2 className="serif text-5xl md:text-7xl mb-10 leading-tight">Quantum Impact Finance</h2>
              <div className="space-y-6">
                <p className="text-violet-100 text-lg leading-relaxed mb-10">
                  Nueva infraestructura financiera para canalizar inversión hacia activos productivos reales mediante tokenización, AI y nuevas arquitecturas financieras, en América Latina y escala global.
                </p>
              </div>
              <div className="grid grid-cols-2 gap-6">
                {[
                  "financiamiento PyME y emprendedores",
                  "underwriting con IA",
                  "activos de impacto/Tokenización",
                  "crecimiento productivo",
                  "capital inteligente"
                ].map((label, i) => (
                  <div key={i} className="bg-white/10 p-8 rounded-3xl border border-white/5 flex flex-col justify-center">
                    <h5 className="serif text-xl">{label}</h5>
                  </div>
                ))}
              </div>
            </div>
            <div className="relative aspect-square grid grid-cols-2 gap-4">
               {[1,2,3,4].map(i => (
                 <div key={i} className={`rounded-3xl border border-white/10 bg-white/5 ${i%2 === 0 ? 'mt-8' : 'mb-8'}`}></div>
               ))}
               <div className="absolute inset-0 flex items-center justify-center">
                 <div className="w-48 h-48 bg-soft-gold rounded-full blur-[80px] opacity-20"></div>
                 <div className="serif text-3xl italic text-soft-gold tracking-widest">Quantum</div>
               </div>
            </div>
          </div>
        </div>
      </section>

      {/* CTA / Contact Section */}
      <section id="contacto" className="py-40 px-6 bg-white relative overflow-hidden">
        <div className="max-w-4xl mx-auto text-center">
          <motion.div {...fadeInUp}>
            <h2 className="serif text-5xl md:text-8xl mb-12 tracking-tighter text-luxury-violet">Diseñemos el futuro del capital.</h2>
            <p className="text-xl text-gray-500 mb-16 max-w-2xl mx-auto font-light leading-relaxed">
              Trabajo con inversores, emprendedores y visionarios que entienden que el viejo paradigma financiero ya no es suficiente. 
              Si estás alineado con esta visión, conversemos.
            </p>
            <div className="flex flex-wrap justify-center gap-6">
              <a href={`mailto:${EMAIL}`} className="bg-white text-luxury-violet px-10 py-5 rounded-full font-bold uppercase tracking-widest text-xs hover:bg-soft-gold hover:text-white transition-all shadow-2xl flex items-center gap-3">
                Agendar conversación <MessageSquare size={18} />
              </a>
              <a href={`mailto:${EMAIL}`} className="bg-transparent border border-white/30 text-white px-10 py-5 rounded-full font-bold uppercase tracking-widest text-xs hover:bg-white hover:text-luxury-violet transition-all">
                Contacto directo
              </a>
            </div>
            <div className="mt-20">
               <p className="text-white/40 mb-6 uppercase tracking-[0.3em] text-xs">Construyamos lo Nuevo</p>
               <a href={`mailto:${EMAIL}`} className="bg-soft-gold text-white px-12 py-4 rounded-full font-black uppercase tracking-widest text-xs hover:scale-105 transition-all inline-block">Contactar</a>
            </div>
          </motion.div>
        </div>
      </section>

      {/* Footer */}
      <footer className="bg-[#FAF9F6] py-20 px-6 border-t border-gray-100">
        <div className="max-w-7xl mx-auto">
          <div className="grid grid-cols-2 md:grid-cols-4 gap-12 mb-20">
            <div className="col-span-2">
              <div className="serif text-2xl mb-6">Norma Pimienta</div>
              <p className="text-sm text-gray-400 max-w-xs leading-relaxed uppercase tracking-widest font-medium">Finanzas. Conciencia. Innovación.</p>
            </div>
            <div>
              <h4 className="text-[10px] uppercase tracking-widest font-bold text-gray-400 mb-8">Secciones</h4>
              <ul className="space-y-4 text-[10px] uppercase tracking-widest font-bold text-gray-600">
                <li><a href="#trayectoria" className="hover:text-luxury-violet transition-colors">Trayectoria</a></li>
                <li><a href="#tesis" className="hover:text-luxury-violet transition-colors">Tesis</a></li>
                <li><a href="#proyecto" className="hover:text-luxury-violet transition-colors">Proyecto</a></li>
              </ul>
            </div>
            <div>
              <h4 className="text-[10px] uppercase tracking-widest font-bold text-gray-400 mb-8">Conectar</h4>
              <div className="flex gap-4">
                <a href={LINKEDIN_URL} target="_blank" className="w-10 h-10 rounded-full border border-gray-200 flex items-center justify-center text-gray-500 hover:bg-luxury-violet hover:text-white hover:border-luxury-violet transition-all">
                  <Linkedin size={20} />
                </a>
                <a href={`mailto:${EMAIL}`} className="w-10 h-10 rounded-full border border-gray-200 flex items-center justify-center text-gray-500 hover:bg-luxury-violet hover:text-white hover:border-luxury-violet transition-all">
                  <Mail size={20} />
                </a>
              </div>
              <p className="text-[10px] mt-4 text-gray-400">Email: {EMAIL}</p>
            </div>
          </div>
          <div className="pt-8 border-t border-gray-100 flex flex-col md:flex-row justify-between items-center gap-4 text-[10px] text-gray-400 uppercase tracking-widest font-medium">
            <p>© 2026 Norma Pimienta. Todos los derechos reservados.</p>
            <div className="flex gap-8">
              <a href="#" className="hover:text-luxury-violet cursor-not-allowed">Privacidad</a>
              <a href="#" className="hover:text-luxury-violet cursor-not-allowed">Protocolo</a>
            </div>
          </div>
        </div>
      </footer>
    </div>
  );
}
