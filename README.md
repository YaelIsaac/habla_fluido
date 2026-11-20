# Habla Fluido · Aprende inglés con un tutor de IA en Flutter y TDD

**Materia:** Desarrollo de Aplicaciones Móviles
**Alumno:** González López Yael Isaac
**Fecha:** 20 de noviembre de 2026

## Descripción

App para practicar inglés todos los días con un tutor de inteligencia artificial. Arma un plan diario de 20 minutos que reparte el tiempo entre oído (dictado), pronunciación, lectura, escritura y conversación, y le da más tiempo a la habilidad más débil. La pronunciación y el dictado se califican comparando palabra por palabra (distancia de Levenshtein), las frases se repasan con repetición espaciada (algoritmo SM-2) y el tutor conversa al nivel del estudiante (MCER A1 a C1), corrige máximo 2 errores por turno y siempre hace otra pregunta. La llave de la IA nunca está en la app: vive en un servidor proxy en Node que valida entradas y salidas y limita las peticiones. Todo se desarrolló con TDD.

## Estructura del proyecto

<!-- PEGA AQUÍ LA CAPTURA -->

## Pruebas de casos (éxito y fallo)

## Pruebas del comparador (12) · test/comparador_test.dart

Pruebas: normalizar texto, distancia de Levenshtein y similitud, y comparar lo esperado contra lo dicho (pares mínimos, palabras omitidas o sobrantes y puntaje entre 0 y 1).

### Éxito (todas en verde)

<!-- PEGA AQUÍ LA CAPTURA -->

### Fallo (idéntico (ignora mayúsculas y signos) = 100%)

<!-- PEGA AQUÍ LA CAPTURA -->

## Pruebas de repaso y progreso (20) · test/repaso_progreso_test.dart

Pruebas: repetición espaciada SM-2 (intervalos, facilidad mínima, fechas, vencidas y mazo), progreso por habilidad (promedio, racha, habilidad más débil y subir de nivel) y plan diario de minutos.

### Éxito (todas en verde)

<!-- PEGA AQUÍ LA CAPTURA -->

### Fallo (secuencia 4, 5, 5, 2)

<!-- PEGA AQUÍ LA CAPTURA -->

## Pruebas del tutor (17) · test/tutor_test.dart

Pruebas: leer la respuesta de la IA como entrada no confiable, tutor simulado que corrige y limita a 2 correcciones, y cliente HTTP que exige HTTPS, recorta el historial y maneja errores.

### Éxito (todas en verde)

<!-- PEGA AQUÍ LA CAPTURA -->

### Fallo (corrige "I am agree")

<!-- PEGA AQUÍ LA CAPTURA -->

## Pruebas de ViewModels (29) · test/vms_test.dart

Pruebas: pronunciación, dictado, lectura, escritura, conversación, aprendizaje con persistencia y repaso.

### Éxito (todas en verde)

<!-- PEGA AQUÍ LA CAPTURA -->

### Fallo (inicia con un saludo del tutor, una sola vez)

<!-- PEGA AQUÍ LA CAPTURA -->

## Pruebas del servidor proxy (12) · proxy/test/proxy.test.js

Pruebas: prompt con reglas pedagógicas, validación de solicitudes, extracción segura de la respuesta del modelo, errores 400/404/502, límite de peticiones (429) y token de la app.

### Éxito (todas en verde)

<!-- PEGA AQUÍ LA CAPTURA -->

### Fallo (respuesta: descarta correcciones incompletas y recorta a 5)

<!-- PEGA AQUÍ LA CAPTURA -->

## Todas las pruebas de Flutter en verde (78)

<!-- PEGA AQUÍ LA CAPTURA -->

## Evidencia de la aplicación

### Inicio con el plan del día

<!-- PEGA AQUÍ LA CAPTURA -->

### Pronunciación con resultado palabra por palabra

<!-- PEGA AQUÍ LA CAPTURA -->

### Conversación con el tutor y correcciones

<!-- PEGA AQUÍ LA CAPTURA -->

## Conclusión

Con TDD toda la parte pedagógica quedó comprobada antes de hacer las pantallas: cómo se califica la pronunciación, cuándo repasar cada frase, cómo se reparte el plan del día y cómo corrige el tutor. Las capturas de fallo demuestran que las pruebas sí detectan errores. La respuesta de la IA se trata como entrada no confiable y la llave vive solo en el servidor proxy, nunca en la app. Gracias al tutor y a la voz simulados, todo se pudo probar sin internet y sin gastar en la API.
