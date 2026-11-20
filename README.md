# Habla Fluido · Aprende inglés con un tutor de IA en Flutter y TDD

**Materia:** Desarrollo de Aplicaciones Móviles
**Alumno:** González López Yael Isaac
**Fecha:** 20 de noviembre de 2026

## Estructura del proyecto

<img width="161" height="368" alt="image" src="https://github.com/user-attachments/assets/68d55bb6-afc6-42eb-a469-183aa8e38cbd" />

## Pruebas de casos (éxito y fallo)

## Pruebas del comparador (12) · test/comparador_test.dart

Pruebas: normalizar texto, distancia de Levenshtein y similitud, y comparar lo esperado contra lo dicho (pares mínimos, palabras omitidas o sobrantes y puntaje entre 0 y 1).

### Éxito (todas en verde)

<img width="401" height="439" alt="image" src="https://github.com/user-attachments/assets/7bb04eee-056b-4181-ba9b-606655a616b0" />

### Fallo (idéntico (ignora mayúsculas y signos) = 100%)

<img width="400" height="314" alt="image" src="https://github.com/user-attachments/assets/db08a1b4-301d-4c33-9656-97b8d6c8cc3f" />

## Pruebas de repaso y progreso (20) · test/repaso_progreso_test.dart

Pruebas: repetición espaciada SM-2 (intervalos, facilidad mínima, fechas, vencidas y mazo), progreso por habilidad (promedio, racha, habilidad más débil y subir de nivel) y plan diario de minutos.

### Éxito (todas en verde)

<img width="402" height="436" alt="image" src="https://github.com/user-attachments/assets/0b622a35-158a-4b14-b407-93e83735ecb9" />

### Fallo (secuencia 4, 5, 5, 2)

<img width="400" height="373" alt="image" src="https://github.com/user-attachments/assets/58f9f4b4-98a4-4c04-ad64-9f7345e0b5aa" />

## Pruebas del tutor (17) · test/tutor_test.dart

Pruebas: leer la respuesta de la IA como entrada no confiable, tutor simulado que corrige y limita a 2 correcciones, y cliente HTTP que exige HTTPS, recorta el historial y maneja errores.

### Éxito (todas en verde)

<img width="400" height="406" alt="image" src="https://github.com/user-attachments/assets/a92e38a1-9602-429c-ab7c-939dc9f0265e" />

### Fallo (corrige "I am agree")

<img width="400" height="372" alt="image" src="https://github.com/user-attachments/assets/d9d4fc83-25df-4eba-a5d7-ce34b6b7ccb9" />

## Pruebas de ViewModels (29) · test/vms_test.dart

Pruebas: pronunciación, dictado, lectura, escritura, conversación, aprendizaje con persistencia y repaso.

### Éxito (todas en verde)

<img width="401" height="437" alt="image" src="https://github.com/user-attachments/assets/fdee24ea-2402-46b8-944c-61a5733e4e3e" />

### Fallo (inicia con un saludo del tutor, una sola vez)

<img width="399" height="411" alt="image" src="https://github.com/user-attachments/assets/cab8e5fe-2c54-42e8-ba65-d0ad87a82b8d" />

## Pruebas del servidor proxy (12) · proxy/test/proxy.test.js

Pruebas: prompt con reglas pedagógicas, validación de solicitudes, extracción segura de la respuesta del modelo, errores 400/404/502, límite de peticiones (429) y token de la app.

### Éxito (todas en verde)

<img width="398" height="227" alt="image" src="https://github.com/user-attachments/assets/bd420ef6-7c56-43b3-86a8-bf7130013aaf" />

### Fallo (respuesta: descarta correcciones incompletas y recorta a 5)

<img width="393" height="290" alt="image" src="https://github.com/user-attachments/assets/d02ddf18-8487-4c05-b566-48697d3861ca" />

## Todas las pruebas de Flutter en verde (78)

<img width="391" height="50" alt="image" src="https://github.com/user-attachments/assets/83427db3-ac3c-4c59-8be6-64428584040f" />

## Evidencia de la aplicación

### Inicio con el plan del día

<img width="300" height="650" alt="WhatsApp Image 2026-11-20 at 13 30 53" src="https://github.com/user-attachments/assets/81bc2f14-ab2d-435f-b669-ba2117955b36" />

### Pronunciación con resultado palabra por palabra

<img width="300" height="650" alt="WhatsApp Image 2026-11-20 at 13 30 54" src="https://github.com/user-attachments/assets/73f687e7-bc94-44ff-83de-68335ae1a74d" />

### Conversación con el tutor y correcciones

<img width="300" height="650" alt="WhatsApp Image 2026-11-20 at 13 30 54 (1)" src="https://github.com/user-attachments/assets/0797ace9-bd48-4fcd-8afb-6e9bacbc7069" />
