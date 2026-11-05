# Complejo Cacaotero Bonaventuriano · Recorrido virtual 3D

*Del cacao valluno a su mesa*

Recorrido virtual 3D en primera persona de un complejo cacaotero colombiano completo, ambientado en el valle geográfico del río Cauca (Valle del Cauca, Colombia). Corre en el navegador y está pensado para la enseñanza de la agroindustria del cacao: el visitante entra al complejo en un día normal de trabajo y **ve ocurrir el proceso**, no solo un escenario quieto.

La cadena completa que se recorre:

**cultivo agroforestal → cosecha y quiebre de mazorcas → transporte y acopio → recepción y báscula → fermentación → secado → bodega de grano seco → transformación → empaque → bodega y despacho → tienda de chocolate**


## Controles

| Tecla | Acción |
|---|---|
| `W A S D` o flechas | Moverse |
| Mouse | Mirar (haz clic en la escena para capturar el puntero) |
| `Shift` | Correr (en dron: volar más rápido) |
| `Espacio` | Salto pequeño |
| `1` | Modo caminar |
| `2` | Modo dron (`Q` baja, `E` sube) |
| `3` | Recorrido guiado |
| `M` | Lista "Ir a zona" |
| `N` | Activar o silenciar el sonido |
| `H` | Ocultar o mostrar la ayuda |
| `F` | Contador de cuadros por segundo, llamadas de dibujo y triángulos |
| `Esc` | Interrumpir el recorrido guiado |

También puedes teletransportarte haciendo clic en el minimapa.
**En celular o tableta:** la mitad izquierda de la pantalla es una palanca virtual para moverse y la mitad derecha, arrastrando, mueve la mirada.

## Modos de visita

- **Caminar:** a la altura de los ojos de una persona. Se puede entrar caminando por los portones a la fermentación, la bodega de grano, la planta de transformación, el empaque y la bodega de producto terminado, y andar entre los surcos del cacaotal.
- **Dron:** vuelo libre de 1,8 m a 900 m de altura para ver el complejo completo.
- **Recorrido guiado:** la cámara viaja sola por 26 planos y se detiene en 15 paradas con un subtítulo explicativo. Al terminar queda en modo dron.

## Lo que se ve ocurrir

- **Camiones de cacao en baba:** seis camiones de estacas esperan junto al lote en cosecha y luego bajan a la planta. Se pesan en la báscula de entrada con el semáforo en rojo. Los coteros vacían las canecas en la tolva. Los camiones dan la vuelta por la glorieta, se pesan a la salida y regresan al campo. Cuando coinciden, hacen cola.
- **Acopio de cacao seco:** camionetas de asociaciones de productores llegan, se pesan y descargan sacos.
- **Cosecha:** las cuadrillas recorren el lote árbol por árbol con la media luna. Las mazorcas desaparecen de los árboles cosechados, quedan montones en las calles y se forman puntos de quiebre con cáscara y baldes de cacao en baba. Al terminar, el lote se restablece.
- **Fermentación:** un operario pasa la masa de un cajón al de abajo. El color de la masa cambia según el día.
- **Secado:** operarios rastrillan el grano en las marquesinas y el techo de la elba se desliza.
- **Transformación:** tostadores, conchas, mesa vibratoria, moldes y chocolatinas en movimiento, con un operario en cada puesto.
- **Empaque y despacho:** un robot paletizador apila sacos y los montacargas mueven pallets. Los furgones entran en reversa a los muelles, abren puertas, cargan y salen.
- **Alrededores:** tránsito en la vía nacional, humo y vapor de las chimeneas, ganado, banderas y sonido ambiente generado en el navegador.

## Zonas del complejo

Portería y báscula · Recepción y calidad · Fermentación · Secado · Bodega de grano seco · Planta de transformación · Cascarilla, caldera y compostaje · Empaque · Bodega de producto terminado · Administración y laboratorio · Taller y combustible · Tienda de chocolate · Planta de tratamiento (PTAR) · Vivero y patio de campo · Estación de bombeo · Cultivo de cacao

## Calidad gráfica

En la pantalla de inicio se elige la calidad, que también se puede cambiar durante el recorrido con el botón **Calidad**:

- **Alta:** para PC con tarjeta gráfica dedicada.
- **Media:** opción por defecto en escritorio.
- **Baja:** opción por defecto en celular. Recomendada para portátiles con gráfica integrada.

La escena es grande. Si el movimiento se siente lento, baja la calidad.

## Aspectos técnicos

- Un solo archivo HTML con todo el CSS y el JavaScript en un `<script type="module">`.
- [Three.js](https://threejs.org/) 0.169.0 cargado con un *import map* desde jsDelivr, más los complementos GLTFLoader, RGBELoader, Sky y BufferGeometryUtils. No usa ninguna otra librería.
- Todo el mundo (terreno, edificios, máquinas, vehículos, personas y árboles) se construye por código con primitivas. El azar usa una semilla fija, así que el mundo sale idéntico en cada carga.
- Al iniciar, intenta descargar en segundo plano texturas PBR y un cielo HDRI de Poly Haven, además de algunas texturas y modelos de aves y caballos de los ejemplos de three.js. Si no hay conexión con esos servidores, usa texturas generadas por código y el mundo se ve completo de todas formas. Las aves y los caballos solo aparecen si sus modelos cargan.
- Para el rendimiento, la geometría estática se fusiona y lo repetido usa mallas instanciadas. La vegetación cercana se genera por celdas alrededor de la cámara y el detalle lejano deja de dibujarse.

## Requisitos

- Navegador reciente con WebGL 2 (Chrome o Edge recomendados).
- Conexión a internet para cargar Three.js y la fuente Inter.

## Créditos

- Concepto, contenido pedagógico y dirección: Luis Fernando Delgado Muñoz.
- Desarrollo del código asistido por Claude (Anthropic).
- Motor 3D: [Three.js](https://threejs.org/) (licencia MIT).
- Texturas y cielo HDRI: [Poly Haven](https://polyhaven.com/) (CC0).
- Fuente: [Inter](https://rsms.me/inter/), a través de Google Fonts (SIL Open Font License).

La empresa "Cacaotera Bonaventuriana" y su marca son ficticias, creadas con fines educativos.
