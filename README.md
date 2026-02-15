<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Planilla de Personal - Mantenimiento y Construcción</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            margin: 0;
            padding: 20px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
        }

        .container {
            background: white;
            border-radius: 15px;
            box-shadow: 0 20px 40px rgba(0,0,0,0.1);
            overflow: hidden;
            margin: 0 auto;
            max-width: 100%;
        }

        .header {
            background: linear-gradient(135deg, #2c3e50 0%, #3498db 100%);
            color: white;
            padding: 30px;
            text-align: center;
        }

        .header h1 {
            margin: 0 0 15px 0;
            font-size: 2.2em;
            font-weight: 600;
        }

        .info-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 15px;
            margin-top: 20px;
        }

        .info-item {
            background: rgba(255,255,255,0.1);
            padding: 10px 15px;
            border-radius: 8px;
            backdrop-filter: blur(10px);
        }

        .info-label {
            font-size: 0.9em;
            opacity: 0.8;
            margin-bottom: 5px;
        }

        .info-value {
            font-weight: 600;
            font-size: 1.1em;
        }

        .stats {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 20px;
            margin: 20px;
        }

        .stat-card {
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.08);
            text-align: center;
        }

        .stat-number {
            font-size: 2em;
            font-weight: 700;
            color: #3498db;
            margin-bottom: 5px;
        }

        .stat-label {
            color: #7f8c8d;
            font-size: 0.9em;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .table-container {
            overflow-x: auto;
            padding: 0;
        }

        table {
            width: 100%;
            border-collapse: collapse;
            font-size: 12px;
        }

        th, td {
            padding: 12px 8px;
            text-align: left;
            border-bottom: 1px solid #e0e0e0;
            vertical-align: top;
        }

        th {
            background: linear-gradient(135deg, #34495e 0%, #2c3e50 100%);
            color: white;
            font-weight: 600;
            position: sticky;
            top: 0;
            z-index: 10;
            text-transform: uppercase;
            font-size: 11px;
            letter-spacing: 0.5px;
        }

        tr:nth-child(even) {
            background-color: #f8f9fa;
        }

        tr:hover {
            background-color: #e3f2fd;
            transition: background-color 0.3s ease;
        }

        .nacionalidad {
            font-weight: 600;
            padding: 4px 8px;
            border-radius: 12px;
            font-size: 10px;
            text-align: center;
            display: inline-block;
            min-width: 60px;
        }

        .nacionalidad.cr {
            background-color: #E3F2FD;
            color: #1976D2;
        }

        .nacionalidad.ni {
            background-color: #FFF3E0;
            color: #F57C00;
        }

        .nacionalidad.cu {
            background-color: #FFEBEE;
            color: #C62828;
        }

        .estado {
            padding: 4px 8px;
            border-radius: 12px;
            font-size: 10px;
            font-weight: 600;
            text-align: center;
            display: inline-block;
            min-width: 50px;
        }

        .activo {
            background-color: #E8F5E8;
            color: #2E7D32;
        }

        .inactivo {
            background-color: #FFEBEE;
            color: #C62828;
        }

        .proyecto {
            padding: 3px 6px;
            border-radius: 8px;
            font-size: 9px;
            font-weight: 600;
            text-align: center;
            display: inline-block;
            min-width: 85px;
        }

        .proyecto.mantenimiento {
            background-color: #FFF3E0;
            color: #F57C00;
        }

        .proyecto.construccion {
            background-color: #E0F2F1;
            color: #00897B;
        }

        .puesto {
            padding: 3px 6px;
            border-radius: 6px;
            font-size: 10px;
            background-color: #F5F5F5;
            color: #424242;
            display: inline-block;
        }

        .footer {
            padding: 30px;
            background: #f8f9fa;
            text-align: center;
            color: #666;
            border-top: 1px solid #e0e0e0;
        }

        @media (max-width: 768px) {
            .container {
                margin: 10px;
                border-radius: 10px;
            }

            .header {
                padding: 20px;
            }

            .header h1 {
                font-size: 1.5em;
            }

            table {
                font-size: 10px;
            }

            th, td {
                padding: 8px 4px;
            }

            .stats {
                grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
                gap: 15px;
                margin: 15px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1>👷 Nómina de Personal</h1>
            <h2 style="font-size: 1.3em; font-weight: 400; margin: 10px 0 0 0;">Mantenimiento y Construcción</h2>
            <div class="info-grid">
                <div class="info-item">
                    <div class="info-label">Empresa</div>
                    <div class="info-value">Grupo Mozu Sociedad Anónima</div>
                </div>
                <div class="info-item">
                    <div class="info-label">Período</div>
                    <div class="info-value">02 (Febero 2026)</div>
                </div>
                <div class="info-item">
                    <div class="info-label">Fecha Actualización</div>
                    <div class="info-value">15-02-2026</div>
                </div>
                <div class="info-item">
                    <div class="info-label">Tipo Planilla</div>
                    <div class="info-value">Mensual</div>
                </div>
            </div>
        </div>

        <div class="stats">
            <div class="stat-card">
                <div class="stat-number">11</div>
                <div class="stat-label">Total Empleados</div>
            </div>
            <div class="stat-card">
                <div class="stat-number">11</div>
                <div class="stat-label">Activos</div>
            </div>
            <div class="stat-card">
                <div class="stat-number">0</div>
                <div class="stat-label">Inactivos</div>
            </div>
            <div class="stat-card">
                <div class="stat-number">1</div>
                <div class="stat-label">Costa Rica</div>
            </div>
            <div class="stat-card">
                <div class="stat-number">9</div>
                <div class="stat-label">Nicaragua</div>
            </div>
            <div class="stat-card">
                <div class="stat-number">1</div>
                <div class="stat-label">Cuba</div>
            </div>
            <div class="stat-card">
                <div class="stat-number">7</div>
                <div class="stat-label">Mantenimiento</div>
            </div>
            <div class="stat-card">
                <div class="stat-number">4</div>
                <div class="stat-label">Construcción</div>
            </div>
        </div>

        <div class="table-container">
            <table>
                <thead>
                    <tr>
                        <th>Código</th>
                        <th>Nombre Completo</th>
                        <th>Identificación</th>
                        <th>Fecha Nacimiento</th>
                        <th>Puesto</th>
                        <th>Género</th>
                        <th>Nacionalidad</th>
                        <th>Teléfono</th>
                        <th>Correo Electrónico</th>
                        <th>Estado</th>
                        <th>Proyecto</th>
                    </tr>
                </thead>
                <tbody>
                    <!-- Empleados MANTENIMIENTO -->
                    <tr>
                        <td><strong>MZ-2304</strong></td>
                        <td><strong>EFRAIN JESUS BRAVO PINEDA</strong></td>
                        <td>1558-56929923</td>
                        <td>1/8/1983</td>
                        <td><span class="puesto">Jardinero</span></td>
                        <td>Masculino</td>
                        <td><span class="nacionalidad ni">Nicaragua</span></td>
                        <td>6410-1209</td>
                        <td>grupo.mozu@gmail.com</td>
                        <td><span class="estado activo">Activo</span></td>
                        <td><span class="proyecto mantenimiento">MANTENIMIENTO</span></td>
                    </tr>
                    <tr>
                        <td><strong>MZ-3106</strong></td>
                        <td><strong>ERICK ESPINOZA BARRIOS</strong></td>
                        <td>6-155806565711</td>
                        <td>22/8/1991</td>
                        <td><span class="puesto">Mantenimiento</span></td>
                        <td>Masculino</td>
                        <td><span class="nacionalidad ni">Nicaragua</span></td>
                        <td>6133-5572</td>
                        <td>grupo.mozu@gmail.com</td>
                        <td><span class="estado activo">Activo</span></td>
                        <td><span class="proyecto mantenimiento">MANTENIMIENTO</span></td>
                    </tr>
                    <tr>
                        <td><strong>MZ-3107</strong></td>
                        <td><strong>ERWIN GABRIL GARCIA SOZA</strong></td>
                        <td>5-NI27021996EGS8</td>
                        <td>27/2/1996</td>
                        <td><span class="puesto">Mantenimiento</span></td>
                        <td>Masculino</td>
                        <td><span class="nacionalidad ni">Nicaragua</span></td>
                        <td>6410-1209</td>
                        <td>grupo.mozu@gmail.com</td>
                        <td><span class="estado activo">Activo</span></td>
                        <td><span class="proyecto mantenimiento">MANTENIMIENTO</span></td>
                    </tr>
                    <tr>
                        <td><strong>MZ-3110</strong></td>
                        <td><strong>JORDING FRANCISCO MORAZAN BLANDON</strong></td>
                        <td>5-NI12071993JMB2</td>
                        <td>12/7/1993</td>
                        <td><span class="puesto">Mantenimiento</span></td>
                        <td>Masculino</td>
                        <td><span class="nacionalidad ni">Nicaragua</span></td>
                        <td>6410-1209</td>
                        <td>grupo.mozu@gmail.com</td>
                        <td><span class="estado activo">Activo</span></td>
                        <td><span class="proyecto mantenimiento">MANTENIMIENTO</span></td>
                    </tr>
                    <tr>
                        <td><strong>MZ-3111</strong></td>
                        <td><strong>JOSE ESTEBAN LOPEZ NOTIENE</strong></td>
                        <td>5-NI16082006JLN1</td>
                        <td>16/8/2006</td>
                        <td><span class="puesto">Mantenimiento</span></td>
                        <td>Masculino</td>
                        <td><span class="nacionalidad ni">Nicaragua</span></td>
                        <td>6410-1209</td>
                        <td>grupo.mozu@gmail.com</td>
                        <td><span class="estado activo">Activo</span></td>
                        <td><span class="proyecto mantenimiento">MANTENIMIENTO</span></td>
                    </tr>
                    <tr>
                        <td><strong>MZ-3125</strong></td>
                        <td><strong>JUAN MANUEL AMADOR OPORTA</strong></td>
                        <td>6-155851414414</td>
                        <td>10/2/1978</td>
                        <td><span class="puesto">Mantenimiento</span></td>
                        <td>Masculino</td>
                        <td><span class="nacionalidad ni">Nicaragua</span></td>
                        <td>6410-1209</td>
                        <td>grupo.mozu@gmail.com</td>
                        <td><span class="estado activo">Activo</span></td>
                        <td><span class="proyecto mantenimiento">MANTENIMIENTO</span></td>
                    </tr>
                    <tr>
                        <td><strong>MZ-3168</strong></td>
                        <td><strong>STIVEN FAJARDO GALIANO</strong></td>
                        <td>6-119200608721</td>
                        <td>1/2/2008</td>
                        <td><span class="puesto">Cub. Libre</span></td>
                        <td>Masculino</td>
                        <td><span class="nacionalidad cu">Cuba</span></td>
                        <td>6410-1209</td>
                        <td>grupo.mozu@gmail.com</td>
                        <td><span class="estado activo">Activo</span></td>
                        <td><span class="proyecto mantenimiento">MANTENIMIENTO</span></td>
                    </tr>

                    <!-- Empleados CONSTRUCCIÓN -->
                    <tr>
                        <td><strong>MZ-3167</strong></td>
                        <td><strong>ALVARO JOSE GRANADOS BLANDON</strong></td>
                        <td>6-155820305004</td>
                        <td>5/6/1985</td>
                        <td><span class="puesto">Operario</span></td>
                        <td>Masculino</td>
                        <td><span class="nacionalidad ni">Nicaragua</span></td>
                        <td>6410-1209</td>
                        <td>grupo.mozu@gmail.com</td>
                        <td><span class="estado activo">Activo</span></td>
                        <td><span class="proyecto construccion">CONSTRUCCIÓN</span></td>
                    </tr>
                    <tr>
                        <td><strong>MZ-3166</strong></td>
                        <td><strong>DILAN ADOLFO MONGE ANCHIA</strong></td>
                        <td>0-604140348</td>
                        <td>9/1/1994</td>
                        <td><span class="puesto">Operario</span></td>
                        <td>Masculino</td>
                        <td><span class="nacionalidad cr">Costa Rica</span></td>
                        <td>6410-1209</td>
                        <td>grupo.mozu@gmail.com</td>
                        <td><span class="estado activo">Activo</span></td>
                        <td><span class="proyecto construccion">CONSTRUCCIÓN</span></td>
                    </tr>
                    <tr>
                        <td><strong>MZ-3163</strong></td>
                        <td><strong>EUDIN MOISES MARTINEZ GOMEZ</strong></td>
                        <td>5-NI30121989EMG1</td>
                        <td>30/12/1989</td>
                        <td><span class="puesto">Ayudante</span></td>
                        <td>Masculino</td>
                        <td><span class="nacionalidad ni">Nicaragua</span></td>
                        <td>6410-1209</td>
                        <td>grupo.mozu@gmail.com</td>
                        <td><span class="estado activo">Activo</span></td>
                        <td><span class="proyecto construccion">CONSTRUCCIÓN</span></td>
                    </tr>
                    <tr>
                        <td><strong>MZ-3157</strong></td>
                        <td><strong>JOSMAN ODEL CORDERO REYES</strong></td>
                        <td>NI07112004JCR1</td>
                        <td>7/11/2004</td>
                        <td><span class="puesto">Ayudante</span></td>
                        <td>Masculino</td>
                        <td><span class="nacionalidad ni">Nicaragua</span></td>
                        <td>6410-1209</td>
                        <td>grupo.mozu@gmail.com</td>
                        <td><span class="estado activo">Activo</span></td>
                        <td><span class="proyecto construccion">CONSTRUCCIÓN</span></td>
                    </tr>
                </tbody>
            </table>
        </div>

        <div class="footer">
            <p><strong>Grupo Mozu S.A.</strong></p>
            <p>Planilla actualizada - Enero 2026</p>
            <p style="font-size: 0.9em; color: #999; margin-top: 10px;">
                Mantenimiento: 7 empleados | Construcción: 4 empleados | Total: 11 empleados
            </p>
        </div>
    </div>
</body>
</html>
