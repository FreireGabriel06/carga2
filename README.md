import React from "react";
import { Card, CardContent } from "@/components/ui/card";
import { Package, Thermometer, Clock, Truck, MapPin, RefreshCw, User, AlertTriangle, Lightbulb, Camera, Droplets } from "lucide-react";

const MonitoramentoCarga2 = () => {
  const progress = 80;
  const distanciaTotal = 2644.6;
  const distanciaAtual = 2115.68;
  const distanciaFaltante = 528.92;
  const tipoCarga = "Frutas";
  const luzUVC = "Ligada";

  return (
    <div className="p-4 bg-gray-50 text-gray-800 h-screen flex flex-col items-center relative overflow-auto font-sans">
      <button className="absolute top-3 left-3 flex items-center space-x-1 text-red-500 hover:text-red-700">
        <AlertTriangle size={20} />
        <span className="text-xs font-semibold">Reportar Problema</span>
      </button>

      <button className="absolute top-3 right-3 flex items-center space-x-1 text-blue-500 hover:text-blue-700">
        <User size={20} />
        <span className="text-xs font-semibold">Suporte</span>
      </button>

      <h1 className="text-2xl font-bold text-blue-700 mb-0">Fresh Route</h1>
      <h2 className="text-md font-medium text-gray-600 mb-4">Monitoramento Detalhado</h2>

      <div className="grid grid-cols-2 gap-3 mb-4 w-full">
        <Card className="bg-white shadow rounded-lg">
          <CardContent className="p-4 flex flex-col items-center">
            <Package size={28} className="text-orange-600 mb-2" />
            <p className="text-sm font-semibold">Tipo de Carga</p>
            <p className="text-lg font-bold">{tipoCarga}</p>
          </CardContent>
        </Card>

        <Card className="bg-white shadow rounded-lg">
          <CardContent className="p-4 flex flex-col items-center">
            <Thermometer size={28} className="text-blue-600 mb-2" />
            <p className="text-sm font-semibold">Temperatura</p>
            <p className="text-lg font-bold">10°C</p>
          </CardContent>
        </Card>

        <Card className="bg-white shadow rounded-lg">
          <CardContent className="p-4 flex flex-col items-center">
            <Droplets size={28} className="text-blue-400 mb-2" />
            <p className="text-sm font-semibold">Umidade</p>
            <p className="text-lg font-bold">90%-95%</p>
          </CardContent>
        </Card>

        <Card className="bg-white shadow rounded-lg">
          <CardContent className="p-4 flex flex-col items-center">
            <Clock size={28} className="text-red-600 mb-2" />
            <p className="text-sm font-semibold">Tempo Restante</p>
            <p className="text-lg font-bold">6h 36m</p>
          </CardContent>
        </Card>

        <Card className="bg-white shadow rounded-lg">
          <CardContent className="p-4 flex flex-col items-center">
            <Lightbulb size={28} className="text-indigo-600 mb-2" />
            <p className="text-sm font-semibold">LUZ UV-C</p>
            <p className="text-lg font-bold">{luzUVC}</p>
          </CardContent>
        </Card>

        <Card className="bg-white shadow rounded-lg">
          <CardContent className="p-4 flex flex-col items-center">
            <Camera size={28} className="text-yellow-600 mb-2" />
            <p className="text-sm font-semibold">Câmeras</p>
            <button className="mt-2 px-3 py-1 bg-blue-500 text-white rounded hover:bg-blue-600 transition duration-150">
              Acessar
            </button>
          </CardContent>
        </Card>
      </div>

      <Card className="bg-white shadow rounded-lg w-full mb-4">
        <CardContent className="p-3 flex flex-col items-center">
          <div className="flex items-center space-x-1 mb-2">
            <MapPin size={28} className="text-purple-600" />
            <p className="font-semibold text-sm">Distância</p>
            <button className="text-gray-500 hover:text-gray-700">
              <RefreshCw size={16} />
            </button>
          </div>
          <div className="text-center text-xs space-y-0.5">
            <p><strong>Total:</strong> {distanciaTotal.toFixed(2)} km</p>
            <p><strong>Percorrida:</strong> {distanciaAtual.toFixed(2)} km</p>
            <p><strong>Restante:</strong> {distanciaFaltante.toFixed(2)} km</p>
          </div>
        </CardContent>
      </Card>

      <Card className="bg-white shadow rounded-lg w-full">
        <CardContent className="p-4 flex flex-col items-center relative">
          <Truck size={28} className="text-green-600 mb-2" />
          <p className="text-sm font-semibold">Progresso</p>
          <div className="relative w-full mt-3">
            <div className="h-2 bg-gray-200 rounded-full overflow-hidden">
              <div className="h-full bg-green-500" style={{ width: `${progress}%` }}></div>
            </div>
            <Truck
              size={20}
              className="absolute -top-6 text-gray-700"
              style={{ left: `${progress}%`, transform: "translateX(-50%)" }}
            />
            <span
              className="absolute -top-9 text-xs font-bold"
              style={{ left: `${progress}%`, transform: "translateX(-50%)" }}
            >
              {progress}%
            </span>
          </div>
        </CardContent>
      </Card>
    </div>
  );
};

export default MonitoramentoCarga2;
