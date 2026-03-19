<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Linaje de David - Agenda de Bloques</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com" rel="stylesheet">
    <style>
        body { font-family: 'Poppins', sans-serif; }
        .font-linaje { font-family: 'Cinzel', serif; }
        .slot-occupied { background-color: #f3f4f6; color: #9ca3af; cursor: not-allowed; text-decoration: line-through; border: 1px solid #e5e7eb; }
        .slot-active { cursor: pointer; border: 1px solid #d1d5db; transition: all 0.2s; font-weight: 600; }
        .slot-active:hover { border-color: #b45309; background-color: #fffbeb; }
        .slot-selected { background-color: #b45309 !important; color: white !important; border-color: #b45309 !important; }
        .hidden-section { display: none; }
    </style>
</head>
<body class="bg-stone-50 text-stone-800">

    <nav class="bg-stone-900 text-white p-5 border-b-4 border-amber-600 sticky top-0 z-50 shadow-xl">
        <div class="container mx-auto flex justify-between items-center">
            <h1 class="text-xl md:text-2xl font-linaje text-amber-500 uppercase tracking-widest">Barbería Linaje de David</h1>
            <div class="flex gap-4">
                <button onclick="showSection('client-view')" class="text-xs font-bold uppercase hover:text-amber-400">Reservar</button>
                <button onclick="showSection('admin-login')" class="bg-amber-600 px-4 py-2 rounded-xl text-xs font-bold uppercase">Admin</button>
            </div>
        </div>
    </nav>

    <!-- VISTA CLIENTE -->
    <section id="client-view" class="container mx-auto py-8 px-4">
        <div class="max-w-6xl mx-auto bg-white rounded-3xl shadow-2xl overflow-hidden flex flex-col lg:flex-row border border-stone-200">
            <!-- Formulario -->
            <div class="lg:w-1/3 p-8 bg-stone-900 text-white">
                <h2 class="text-2xl font-linaje mb-6 text-amber-500 border-b border-stone-700 pb-2 uppercase italic">Nueva Cita</h2>
                <div class="space-y-4">
                    <input type="text" id="c-name" placeholder="Tu Nombre" class="w-full p-3 rounded-xl bg-stone-800 border-none outline-none focus:ring-2 focus:ring-amber-500">
                    <input type="tel" id="c-phone" placeholder="Celular" class="w-full p-3 rounded-xl bg-stone-800 border-none outline-none">
                    
                    <div>
                        <label class="text-[10px] font-black text-amber-500 uppercase ml-1">Fecha</label>
                        <input type="date" id="c-date" onchange="renderSlots()" class="w-full p-3 rounded-xl bg-stone-800 text-white border-none outline-none">
                    </div>
                    
                    <div>
                        <label class="text-[10px] font-black text-amber-500 uppercase ml-1">Servicio</label>
                        <select id="c-service" onchange="renderSlots()" class="w-full p-3 rounded-xl bg-stone-800 border-none text-amber-400 font-bold outline-none">
                            <option value="60">Solo Corte (1 Hora)</option>
                            <option value="60">Solo Barba (1 Hora)</option>
                            <option value="90">Corte y Barba (1h 30min)</option>
                        </select>
                    </div>

                    <div>
                        <label class="text-[10px] font-black text-amber-500 uppercase ml-1">Barbero</label>
                        <select id="c-barber" onchange="renderSlots()" class="w-full p-3 rounded-xl bg-stone-800 border-none outline-none"></select>
                    </div>
                </div>
                <button onclick="confirmBooking()" class="w-full mt-10 bg-amber-600 py-4 rounded-2xl font-black uppercase hover:bg-amber-500 transition shadow-lg">Agendar Ahora</button>
            </div>

            <!-- Horarios -->
            <div class="lg:w-2/3 p-10 bg-white">
                <div class="flex justify-between items-center mb-8 border-b pb-4">
                    <h3 class="font-bold text-stone-800 uppercase tracking-widest text-lg italic underline decoration-amber-500 decoration-4">Turnos Disponibles (30m)</h3>
                    <div id="display-date" class="text-amber-700 font-black text-xs px-4 py-2 bg-amber-50 rounded-full border border-amber-200 uppercase tracking-widest italic">---</div>
                </div>
                <div id="slots-container" class="grid grid-cols-2 sm:grid-cols-3 md:grid-cols-4 gap-4">
                    <!-- Los turnos aparecen cada 30 min -->
                </div>
                <div id="no-horario-msg" class="hidden text-center py-10 text-stone-400 font-bold uppercase italic text-xs tracking-widest">
                    No hay horario de atención definido para este día.
                </div>
            </div>
        </div>
    </section>

    <!-- ADMIN LOGIN -->
    <section id="admin-login" class="hidden-section py-24 px-4 text-center">
        <div class="max-w-sm mx-auto bg-white p-10 rounded-3xl shadow-xl border border-amber-100">
            <h2 class="text-xl font-linaje mb-8 uppercase italic tracking-widest">Acceso Staff</h2>
            <input type="password" id="admin-pass" placeholder="PIN" class="w-full p-4 border rounded-2xl mb-6 text-center text-2xl tracking-widest outline-none">
            <button onclick="checkAdmin()" class="w-full bg-stone-900 text-white py-4 rounded-2xl font-bold uppercase">Entrar</button>
        </div>
    </section>

    <!-- PANEL ADMIN -->
    <section id="admin-panel" class="hidden-section container mx-auto py-10 px-4">
        <div class="flex flex-col lg:flex-row justify-between items-end mb-10 gap-6 border-b-2 border-stone-200 pb-6">
            <div>
                <h2 class="text-4xl font-linaje text-stone-900 uppercase">Panel de Control</h2>
                <p class="text-amber-600 font-bold uppercase text-[10px] mt-1 italic">Gestión de Horarios Fijos</p>
            </div>
            <div class="flex flex-col sm:flex-row gap-4 items-center">
                <input type="date" id="admin-view-date" onchange="renderAdminPanel()" class="p-2 rounded-xl border font-bold text-amber-700">
                <button onclick="showSection('client-view')" class="text-red-500 font-black uppercase text-[10px] border-2 border-red-500 px-6 py-2 rounded-xl hover:bg-red-500 hover:text-white transition">Cerrar</button>
            </div>
        </div>

        <div class="grid grid-cols-1 lg:grid-cols-4 gap-8">
            <div class="space-y-6">
                <div class="bg-white p-6 rounded-3xl shadow-lg border-t-4 border-amber-500">
                    <h3 class="text-[10px] font-black text-stone-600 uppercase mb-4 tracking-widest">⚙️ Configurar Jornada</h3>
                    <div class="grid grid-cols-2 gap-3 mb-4">
                        <input type="number" id="h-inicio" class="w-full p-2 border rounded-lg text-center font-bold" placeholder="Abre">
                        <input type="number" id="h-fin" class="w-full p-2 border rounded-lg text-center font-bold" placeholder="Cierra">
                    </div>
                    <button onclick="saveDayConfig()" class="w-full bg-amber-600 text-white p-3 rounded-xl font-bold text-[10px] uppercase">Guardar Horario</button>
                    <p class="text-[8px] text-gray-400 mt-2 italic">* Se sumarán 30min de margen al cierre automáticamente.</p>
                </div>
            </div>

            <!-- Listado de Agenda -->
            <div class="lg:col-span-3 bg-white rounded-3xl shadow-lg border overflow-hidden">
                <table class="w-full text-left">
                    <thead class="bg-stone-900 text-white text-[10px] font-black uppercase">
                        <tr>
                            <th class="p-5">Hora Inicio</th>
                            <th class="p-5">Duración</th>
                            <th class="p-5">Cliente</th>
                            <th class="p-5">Servicio</th>
                            <th class="p-5 text-center">Acción</th>
                        </tr>
                    </thead>
                    <tbody id="admin-appointments-body" class="divide-y divide-stone-100"></tbody>
                </table>
            </div>
        </div>
    </section>

    <script>
        let barberos = JSON.parse(localStorage.getItem('ld_barbers')) || ["David", "Samuel"];
        let citas = JSON.parse(localStorage.getItem('ld_citas')) || [];
        let configDias = JSON.parse(localStorage.getItem('ld_day_configs')) || {};
        let selectedSlot = null;

        const timeToMin = (t) => { const [h, m] = t.split(':').map(Number); return h * 60 + m; };
        const minToTime = (m) => { 
            const h = Math.floor(m / 60); 
            const mins = m % 60;
            return `${h}:${mins === 0 ? '00' : mins}`;
        };

        window.onload = () => {
            const hoy = new Date().toISOString().split('T');
            document.getElementById('c-date').value = hoy;
            document.getElementById('admin-view-date').value = hoy;
            document.getElementById('c-barber').innerHTML = barberos.map(b => `<option value="${b}">${b}</option>`).join('');
            renderSlots();
        };

        function showSection(id) {
            document.querySelectorAll('section').forEach(s => s.classList.add('hidden-section'));
            document.getElementById(id).classList.remove('hidden-section');
            if(id === 'admin-panel') renderAdminPanel();
        }

        function checkAdmin() {
            if (document.getElementById('admin-pass').value === 'david777') showSection('admin-panel');
            else alert("PIN incorrecto");
        }

        function renderSlots() {
            const container = document.getElementById('slots-container');
            const noMsg = document.getElementById('no-horario-msg');
            const barber = document.getElementById('c-barber').value;
            const date = document.getElementById('c-date').value;
            const duracionSvc = parseInt(document.getElementById('c-service').value); 
            
            document.getElementById('display-date').innerText = date || "---";
            container.innerHTML = '';
            selectedSlot = null;

            const jornada = configDias[date];
            if(!jornada) { noMsg.classList.remove('hidden'); return; }
            noMsg.classList.add('hidden');

            const horaInicioMin = jornada.inicio * 60;
            const horaFinMin = (jornada.fin * 60) + 30; // Margen de 30min al cierre

            // Generar bloques fijos cada 30 minutos
            for (let m = horaInicioMin; m < horaFinMin; m += 30) {
                const timeStr = minToTime(m);
                const finSvcRequerido = m + duracionSvc;

                // Verificar si este bloque o los siguientes (según duración) están ocupados
                const isOccupied = citas.some(c => {
                    if (c.barbero !== barber || c.fecha !== date) return false;
                    const cStart = timeToMin(c.hora);
                    const cEnd = cStart + c.duracion;
                    // Solapamiento: el inicio o fin del nuevo servicio cae dentro de uno existente
                    return (m < cEnd && finSvcRequerido > cStart);
                });

                const btn = document.createElement('div');
                btn.innerText = timeStr;

                if (isOccupied) {
                    btn.className = 'p-4 text-center rounded-2xl slot-occupied text-[10px] font-black uppercase';
                    btn.innerText = 'OCUPADO';
                } else if (finSvcRequerido > horaFinMin) {
                    btn.className = 'p-4 text-center rounded-2xl bg-stone-50 text-stone-300 text-[10px] font-black uppercase cursor-not-allowed';
                    btn.innerText = 'FUERA HORARIO';
                } else {
                    btn.className = 'p-4 text-center rounded-2xl slot-active text-sm shadow-sm';
                    btn.onclick = () => {
                        document.querySelectorAll('.slot-active').forEach(el => el.classList.remove('slot-selected'));
                        btn.classList.add('slot-selected');
                        selectedSlot = timeStr;
                    };
                }
                container.appendChild(btn);
            }
        }

        function confirmBooking() {
            const s = document.getElementById('c-service');
            if(!selectedSlot) return alert("Selecciona una hora");
            
            citas.push({
                id: Date.now(),
                nombre: document.getElementById('c-name').value,
                celular: document.getElementById('c-phone').value,
                fecha: document.getElementById('c-date').value,
                servicio: s.options[s.selectedIndex].text,
                duracion: parseInt(s.value),
                barbero: document.getElementById('c-barber').value,
                hora: selectedSlot
            });
            localStorage.setItem('ld_citas', JSON.stringify(citas));
            alert("¡Cita confirmada!");
            renderSlots();
        }

        function saveDayConfig() {
            const date = document.getElementById('admin-view-date').value;
            configDias[date] = { 
                inicio: parseInt(document.getElementById('h-inicio').value), 
                fin: parseInt(document.getElementById('h-fin').value) 
            };
            localStorage.setItem('ld_day_configs', JSON.stringify(configDias));
            alert("Horario guardado para este día");
            renderAdminPanel();
        }

        function renderAdminPanel() {
            const tbody = document.getElementById('admin-appointments-body');
            const date = document.getElementById('admin-view-date').value;
            const filtradas = citas.filter(c => c.fecha === date).sort((a,b) => timeToMin(a.hora) - timeToMin(b.hora));
            
            tbody.innerHTML = filtradas.map(c => `
                <tr class="hover:bg-stone-50 transition">
                    <td class="p-5 font-black text-amber-700 text-lg italic">${c.hora}</td>
                    <td class="p-5 text-[10px] font-bold text-stone-400 uppercase">${c.duracion} min</td>
                    <td class="p-5 font-black text-[11px] uppercase">${c.nombre}</td>
                    <td class="p-5 text-[10px] uppercase font-black text-amber-600 italic">${c.servicio} (${c.barbero})</td>
                    <td class="p-5 text-center">
                        <button onclick="eliminar(${c.id})" class="text-red-500 font-black text-[9px] uppercase border border-red-500 px-3 py-1 rounded-xl">Eliminar</button>
                    </td>
                </tr>
            `).join('');
        }

        function eliminar(id) {
            citas = citas.filter(c => c.id !== id);
            localStorage.setItem('ld_citas', JSON.stringify(citas));
            renderAdminPanel();
        }
    </script>
</body>
</html>
