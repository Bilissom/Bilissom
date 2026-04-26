import { motion } from "framer-motion";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";

export default function Portfolio() {
  return (
    <div className="min-h-screen bg-black text-white p-6">
      {/* HEADER */}
      <motion.h1
        initial={{ opacity: 0, y: -40 }}
        animate={{ opacity: 1, y: 0 }}
        className="text-4xl font-bold text-center mb-10"
      >
        Alisson Caio 🚀
      </motion.h1>

      {/* GRID DE PROJETOS */}
      <div className="grid md:grid-cols-2 gap-6">
        {/* PROJETO 1 */}
        <motion.div whileHover={{ scale: 1.05 }}>
          <Card className="rounded-2xl shadow-xl">
            <CardContent className="p-4">
              <h2 className="text-xl font-semibold">SoilLab</h2>
              <p className="text-sm opacity-70">
                Sistema desenvolvido para o Instituto Federal.
              </p>
              <div className="mt-4 flex gap-2">
                <Button>Ver Projeto</Button>
                <Button variant="outline">Código</Button>
              </div>
            </CardContent>
          </Card>
        </motion.div>

        {/* PROJETO 2 */}
        <motion.div whileHover={{ scale: 1.05 }}>
          <Card className="rounded-2xl shadow-xl">
            <CardContent className="p-4">
              <h2 className="text-xl font-semibold">Agenda Corp</h2>
              <p className="text-sm opacity-70">
                Aplicação de organização moderna e responsiva.
              </p>
              <div className="mt-4 flex gap-2">
                <Button>Ver Projeto</Button>
                <Button variant="outline">Código</Button>
              </div>
            </CardContent>
          </Card>
        </motion.div>
      </div>

      {/* FOOTER */}
      <div className="text-center mt-10 opacity-60">
        © 2026 Alisson Caio
      </div>
    </div>
  );
}
