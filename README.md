<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <!-- Meta tag actualizado para móviles: evita el zoom accidental de la página -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Simulador 3D - Vivienda Bioclimática</title>
    <style>
        body {
            margin: 0;
            overflow: hidden;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #222;
            /* Evita gestos de recarga del navegador en móviles al deslizar */
            touch-action: none; 
        }

        /* Interfaz de Usuario (UI) */
        #ui-container {
            position: absolute;
            top: 20px;
            left: 20px;
            width: 320px;
            background: rgba(255, 255, 255, 0.95);
            padding: 20px;
            border-radius: 12px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.3);
            pointer-events: auto;
            z-index: 10;
            box-sizing: border-box;
        }

        h2 { margin-top: 0; font-size: 1.2rem; color: #333; }
        p { font-size: 0.9rem; color: #555; margin-bottom: 20px; line-height: 1.4; }

        .control-group {
            margin-bottom: 15px;
            padding-bottom: 15px;
            border-bottom: 1px solid #ddd;
        }

        .control-group:last-child { border-bottom: none; margin-bottom: 0; padding-bottom: 0; }

        button {
            width: 100%;
            padding: 12px 10px; /* Botones un poco más grandes para los dedos */
            margin-bottom: 10px;
            border: 2px solid #333;
            border-radius: 8px;
            background: white;
            color: #333;
            font-weight: bold;
            font-size: 1rem;
            cursor: pointer;
            transition: all 0.3s ease;
            /* Elimina el resaltado azul en móviles al tocar */
            -webkit-tap-highlight-color: transparent; 
        }

        button.active {
            background: #333;
            color: white;
            border-color: #333;
        
