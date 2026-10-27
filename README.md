# Simulador de trayectoria · lanzador de tenis de mesa

Simulador de la trayectoria de la bola para un lanzador de dos rodillos. Introduce las RPM de backspin y topspin, el ángulo del tubo y la altura de salida, y obtén:

- Velocidad de la bola.
- Tipo y cantidad de efecto (backspin, topspin o sin efecto, con rotación estimada).
- Distancia de caída sobre la mesa y si cae dentro de ella.
- Altura máxima, ángulo de bajada y altura de rebote.
- Gráficos de la trayectoria, de la distancia según el ángulo y una tabla comparativa.

Funciona sin instalar nada: basta abrir `index.html` en el navegador.

## Modelo

- Velocidad de salida: `v = 0.666 × promedio de las velocidades de superficie de los dos rodillos`. El factor se calibró con siete configuraciones medidas (error medio 0.05 m/s).
- Trayectoria: arrastre aerodinámico (Cd 0.40) y efecto Magnus proporcional al giro estimado.
- Rebote: coeficiente vertical 0.90 y pérdida horizontal de 10 %.
- Rotación: estimación con un factor de eficiencia de 0.15 que no está calibrado. Sirve para comparar configuraciones, no como cifra absoluta.

## Limitaciones

- La distancia de caída de las configuraciones sin medir es una estimación.
- El modelo no está validado para ángulos mayores de 40°; los lobs son los menos seguros.
- La altura del rebote depende del coeficiente de restitución de la mesa, que puede diferir en otras superficies.

## Calibración

Los presets C01 a C14 corresponden a la calibración del lanzador. Para cambiar el factor de salida, escribe una velocidad medida en el campo correspondiente.

## Licencia

Uso libre para entrenamiento y pruebas.
