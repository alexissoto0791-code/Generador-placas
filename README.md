# Placa de Transformador

Aplicación web interactiva para generar placas de características de transformadores de distribución monofásicos (Magnetron, Rymel y Siemens), calculando automáticamente los valores según el voltaje primario, voltaje secundario, capacidad (kVA) y porcentaje de las derivaciones (taps).

## ¿Qué hace?

- Permite elegir la **marca** (Magnetron, Rymel, Siemens) y muestra únicamente los campos que trae esa placa real — evita mostrar términos que no le corresponden a esa marca.
- Calcula automáticamente:
  - Corriente primaria y secundaria (A = kVA × 1000 / V)
  - Voltaje y corriente en cada una de las 5 posiciones de derivación (taps)
  - BIL / nivel de aislamiento según el voltaje primario (15 kV o 34.5 kV)
  - Peso total y litros de aceite dieléctrico (valor de referencia)
  - % de impedancia (Uz) y corriente de cortocircuito (valor de referencia)
- El voltaje secundario se escribe manualmente (por defecto `120/240`).

## Datos de entrada

| Parámetro | Opciones |
|---|---|
| Voltaje primario | 34500 V, 13200 V, 7620 V |
| Voltaje secundario | Campo libre (ej. `120/240`) |
| Capacidad | 3, 5, 10, 15, 25, 30, 37.5, 45, 50, 75, 112.5, 150 kVA |
| Paso de derivaciones | 5%, 10%, 12% |

## Aviso sobre los valores de referencia

Los campos marcados con **\*** en la placa (peso, litros de aceite, % Uz, corriente de cortocircuito) son **valores promedio de referencia**, calculados a partir de fichas técnicas de fabricantes bajo norma NTC 818 / ANSI C57.12.00. No reemplazan el dato real obtenido en la prueba de fábrica de cada transformador específico.

## Cómo publicarlo con GitHub Pages

1. Sube el contenido de este repositorio (ya incluye `index.html`).
2. Ve a **Settings → Pages**.
3. En **Source**, elige **Deploy from a branch**.
4. Selecciona la rama `main` y la carpeta **/ (root)**, y guarda.
5. En 1-2 minutos, GitHub mostrará el enlace público, con el formato:
   `https://tu-usuario.github.io/nombre-del-repositorio/`

## Tecnología

Archivo único en HTML, CSS y JavaScript (sin dependencias externas ni backend). Se puede abrir directamente en cualquier navegador sin instalación.
