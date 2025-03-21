<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <title>Monitoramento de Carga</title>
  <script src="https://unpkg.com/lucide@latest"></script>
  <script>
    window.onload = () => {
      lucide.createIcons();
    };
  </script>
  <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
</head>
<body class="bg-gray-50 text-gray-800 h-screen flex flex-col items-center overflow-auto font-sans relative p-4">

  <button class="absolute top-3 left-3 flex items-center space-x-1 text-red-500 hover:text-red-700">
    <i data-lucide="alert-triangle" class="w-5 h-5"></i>
    <span class="text-xs font-semibold">Reportar Problema</span>
  </button>

  <button class="absolute top-3 right-3 flex items-center space-x-1 text-blue-500 hover:text-blue-700">
    <i data-lucide="user" class="w-5 h-5"></i>
    <span class="text-xs font-semibold">Suporte</span>
  </button>

  <h1 class="text-2xl font-bold text-blue-700 mb-0">Fresh Route</h1>
  <h2 class="text-md font-medium text-gray-600 mb-4">Monitoramento Detalhado</h2>

  <div class="grid grid-cols-1 sm:grid-cols-2 gap-3 mb-4 w-full">

    <div class="bg-white shadow rounded-lg p-4 flex flex-col items-center">
      <i data-lucide="package" class="w-7 h-7 text-orange-600 mb-2"></i>
      <p class="text-sm font-semibold">Tipo de Carga</p>
      <p class="text-lg font-bold">Frutas</p>
    </div>

    <div class="bg-white shadow rounded-lg p-4 flex flex-col items-center">
      <i data-lucide="thermometer" class="w-7 h-7 text-blue-600 mb-2"></i>
      <p class="text-sm font-semibold">Temperatura</p>
      <p class="text-lg font-bold">10°C</p>
    </div>

    <div class="bg-white shadow rounded-lg p-4 flex flex-col items-center">
      <i data-lucide="droplets" class="w-7 h-7 text-blue-400 mb-2"></i>
      <p class="text-sm font-semibold">Umidade</p>
      <p class="text-lg font-bold">90%-95%</p>
    </div>

    <div class="bg-white shadow rounded-lg p-4 flex flex-col items-center">
      <i data-lucide="clock" class="w-7 h-7 text-red-600 mb-2"></i>
      <p class="text-sm font-semibold">Tempo Restante</p>
      <p class="text-lg font-bold">6h 36m</p>
    </div>

    <div class="bg-white shadow rounded-lg p-4 flex flex-col items-center">
      <i data-lucide="lightbulb" class="w-7 h-7 text-indigo-600 mb-2"></i>
      <p class="text-sm font-semibold">LUZ UV-C</p>
      <p class="text-lg font-bold">Ligada</p>
    </div>

    <div class="bg-white shadow rounded-lg p-4 flex flex-col items-center">
      <i data-lucide="camera" class="w-7 h-7 text-yellow-600 mb-2"></i>
      <p class="text-sm font-semibold">Câmeras</p>
      <button class="mt-2 px-3 py-1 bg-blue-500 text-white rounded hover:bg-blue-600 transition duration-150">
        Acessar
      </button>
    </div>

  </div>

  <div class="bg-white shadow rounded-lg w-full mb-4 p-3 flex flex-col items-center">
    <div class="flex items-center space-x-1 mb-2">
      <i data-lucide="map-pin" class="w-7 h-7 text-purple-600"></i>
      <p class="font-semibold text-sm">Distância</p>
      <button class="text-gray-500 hover:text-gray-700">
        <i data-lucide="refresh-cw" class="w-4 h-4"></i>
      </button>
    </div>
    <div class="text-center text-xs space-y-0.5">
      <p><strong>Total:</strong> 2644.60 km</p>
      <p><strong>Percorrida:</strong> 2115.68 km</p>
      <p><strong>Restante:</strong> 528.92 km</p>
    </div>
  </div>

  <div class="bg-white shadow rounded-lg w-full p-4 flex flex-col items-center relative">
    <i data-lucide="truck" class="w-7 h-7 text-green-600 mb-2"></i>
    <p class="text-sm font-semibold">Progresso</p>

    <div class="relative w-full mt-3">
      <div class="h-2 bg-gray-200 rounded-full overflow-hidden">
        <div class="h-full bg-green-500" style="width: 80%;"></div>
      </div>
      <i data-lucide="truck" class="absolute -top-6 w-5 h-5 text-gray-700" style="left: 80%; transform: translateX(-50%);"></i>
      <span class="absolute -top-9 text-xs font-bold" style="left: 80%; transform: translateX(-50%);">80%</span>
    </div>
  </div>

</body>
</html>
