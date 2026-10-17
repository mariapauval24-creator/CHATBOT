# Sistema experto de solicitud de becas

**Materia:** Infraestructura de Negocio (LNV319)\
**Universidad:** Universidad De La Salle Bajío\
**Herramientas:** Twine (Harlowe) y GitHub Pages

## Descripción

Chatbot de cinco preguntas que orienta sobre becas académicas y
económicas, o recomienda consultar a un asesor. Las reglas son criterios
de ejemplo para una actividad escolar, no requisitos oficiales.

## Cinco niveles

1.  Situación académica: inscrito, en proceso, no inscrito.
2.  Promedio: 9.0--10, 8.0--8.9, menor de 8.0.
3.  Necesidad económica: mucha, poca, ninguna.
4.  Semestre: 1.º--2.º, 3.º--6.º, 7.º o superior.
5.  Materias reprobadas: ninguna, una, dos o más.

## Base de conocimiento: reglas SI--ENTONCES

  -----------------------------------------------------------------------
  SI                      ENTONCES                ¿Por qué?
  ----------------------- ----------------------- -----------------------
  No está inscrito        No elegible             La inscripción es un
                                                  criterio básico del
                                                  sistema.

  Tiene promedio menor de No elegible             No alcanza el promedio
  8.0                                             mínimo definido.

  Tiene dos o más         No elegible             Se requiere mejorar el
  materias reprobadas                             desempeño académico.

  Está inscrito, promedio Beca académica          Reconoce el buen
  9.0--10 y cero                                  desempeño escolar.
  reprobadas                                      

  Está inscrito, promedio Beca económica          Combina necesidad
  8.0--8.9, necesita                              económica y rendimiento
  apoyo y cero reprobadas                         adecuado.
  -----------------------------------------------------------------------

**Desvío implementado:** la evaluación dirige a `NoElegible` cuando la
persona no está inscrita, tiene promedio menor de 8.0 o acumula dos o
más materias reprobadas. Otros casos que requieren revisión se envían a
`Asesor`. El semestre se registra, pero por ahora no cambia la
recomendación.

## Reflexión de negocio

### 1. ¿Qué proceso automatiza el chatbot?

Automatiza la orientación inicial sobre solicitudes de beca. Recopila
datos académicos y económicos y presenta una recomendación preliminar
sin que un asesor tenga que realizar todas las preguntas.

### 2. ¿Qué indicador mejoraría?

Podría disminuir el tiempo de primera respuesta a estudiantes y reducir
las consultas repetitivas sobre criterios básicos.

### 3. ¿Cuándo debe escalar a un humano y por qué?

Cuando una persona está en proceso de inscripción, tiene una materia
reprobada o presenta circunstancias especiales. Un asesor debe revisar
estos casos porque una decisión automática equivocada podría afectar el
acceso a un apoyo y se necesita una atención más empática.

### 4. ¿Qué usuario no encuentra su opción y cómo lo atenderían?

Un estudiante con una situación familiar extraordinaria o que busca una
beca especial no contemplada en las preguntas. Se le ofrecería la opción
de hablar con un asesor para explicar su situación.

## Entrega en GitHub

Subir al repositorio público: - `index.html` exportado desde Twine. -
Archivo de respaldo obtenido con **Archive**. - Foto del árbol de
decisiones dibujado en papel. - Este archivo `README.md`.

Para publicar, entrar en **Settings → Pages**, seleccionar **Deploy from
a branch**, rama **main** y carpeta **/(root)**.

## Pruebas

Se comprobaron las rutas de beca académica y beca económica. Falta
verificar las rutas de no elegible y asesor y revisar que ningún pasaje
quede vacío o sin salida.

## Integrantes

Agregar nombres de los integrantes del equipo.
