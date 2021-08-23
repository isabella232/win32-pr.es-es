---
title: Función glPushAttrib (Gl.h)
description: Inserta la pila de atributos.
ms.assetid: 3c7b93cc-2112-4771-b422-a244821447e5
keywords:
- Función glPushAttrib OpenGL
topic_type:
- apiref
api_name:
- glPushAttrib
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 252859065ddae0439441acb6afd797d26bbed44a246b628b4f0350d7f3b1e2d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519995"
---
# <a name="glpushattrib-function"></a>Función glPushAttrib

Inserta la pila de atributos.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glPushAttrib(
   GLbitfield mask
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*mask* 
</dt> <dd>

Máscara que indica qué atributos se guardarán. Las constantes de máscara simbólica y su estado de OpenGL asociado son los siguientes (la lista de párrafos con sangría muestra qué atributos se guardan):

<dl> <dt>

<span id="GL_ACCUM_BUFFER_BIT_"></span><span id="gl_accum_buffer_bit_"></span>BIT \_ DE BÚFER DE GL ACCUM \_ \_ 
</dt> <dd>

Acumulación del valor sin borrar del búfer

</dd> <dt>

<span id="GL_COLOR_BUFFER_BIT"></span><span id="gl_color_buffer_bit"></span>BIT DE \_ BÚFER DE COLOR \_ \_ GL
</dt> <dd>

Bit \_ de habilitación de PRUEBA ALFA de GL \_

Función de prueba alfa y valor de referencia

Bit \_ de habilitación de GL BLEND

Combinación de funciones de origen y destino

Gl \_ DITHER enable bit

Configuración \_ de GL DRAW \_ BUFFER

Bit \_ de habilitación de GL LOGIC \_ OP

Función de operación lógica

Valores sin borrar del modo de color y del modo de índice

Máscaras de escritura en modo de color e índice

</dd> <dt>

<span id="GL_CURRENT_BIT"></span><span id="gl_current_bit"></span>GL \_ CURRENT \_ BIT
</dt> <dd>

Color RGBA actual

Índice de color actual

Vector normal actual

Coordenadas de textura actuales

Posición actual del trama GL \_ CURRENT RASTER POSITION VALID \_ \_ \_ flag

Color RGBA asociado a la posición de trama actual

Índice de color asociado a la posición de trama actual

Coordenadas de textura asociadas a la posición de trama actual

Marca \_ GL EDGE \_ FLAG

</dd> <dt>

<span id="GL_DEPTH_BUFFER_BIT"></span><span id="gl_depth_buffer_bit"></span>BIT DE \_ BÚFER DE PROFUNDIDAD DE \_ \_ GL
</dt> <dd>

GL \_ DEPTH TEST enable \_ bit

Función de prueba de búfer de profundidad

Valor sin borrar del búfer de profundidad

GL \_ DEPTH \_ WRITEMASK enable bit

</dd> <dt>

<span id="GL_ENABLE_BIT"></span><span id="gl_enable_bit"></span>GL \_ ENABLE \_ BIT
</dt> <dd>

Marca \_ GL ALPHA \_ TEST

Marca \_ GL AUTO \_ NORMAL

Marca BLEND de GL \_

Habilitar bits para los planos de recorte definibles por el usuario

\_MATERIAL DE COLOR \_ GL

Marca GL \_ CULL \_ FACE

Marca GL \_ DEPTH \_ TEST

Marca \_ GL DITHER

Marca \_ GL

GL \_ LIGHT *i* where 0 <= *i* < GL \_ MAX \_ LIGHTS

Marca \_ GL LIGHTING

Marca GL \_ LINE \_ SMOOTH

Marca \_ GL LINE \_ STIPPLE

Marca GL \_ COLOR \_ LOGIC \_ OP

Marca GL \_ INDEX \_ LOGIC \_ OP

GL \_ MAP1 \_ x donde x es un tipo de mapa

GL \_ MAP2 \_ x donde x es un tipo de mapa

Marca \_ GL NORMALIZE

Marca GL \_ POINT \_ SMOOTH

Marca GL \_ POLYGON \_ OFFSET \_ LINE

Marca GL \_ POLYGON \_ OFFSET \_ FILL

Marca GL \_ POLYGON \_ OFFSET \_ POINT

Marca GL \_ POLYGON \_ SMOOTH

Marca \_ STIPPLE DE POLÍGONO DE GL \_

Marca \_ DE PRUEBA DE GL LO QUE SE HA \_ DESAJEADO

Marca GL \_ STENCIL \_ TEST

Marca GL \_ TEXTURE \_ 1D

Marca GL \_ TEXTURE \_ 2D

Marcas GL \_ TEXTURE GEN x donde x es \_ \_ S, T, R o Q

</dd> <dt>

<span id="GL_EVAL_BIT"></span><span id="gl_eval_bit"></span>GL \_ EVAL \_ BIT
</dt> <dd>

GL \_ MAP1 \_ x enable bits, donde x es un tipo de mapa

GL \_ MAP2 \_ x enable bits, donde x es un tipo de mapa

Puntos de conexión y divisiones de cuadrícula 1D

Puntos de conexión y divisiones de cuadrícula 2D

GL \_ AUTO NORMAL enable \_ bit

</dd> <dt>

<span id="GL_FOG_BIT"></span><span id="gl_fog_bit"></span>GL \_ FOG \_ BIT
</dt> <dd>

Marca \_ de habilitación GL

Color de color rojo

Densidad de densidad

Inicio lineal de la matriz

Extremo lineal de la curva

Índice de indexación de indexación

Valor \_ DEL MODO GL GL DE GL \_

</dd> <dt>

<span id="GL_HINT_BIT"></span><span id="gl_hint_bit"></span>GL \_ HINT \_ BIT
</dt> <dd>

Configuración \_ GL PERSPECTIVE CORRECTION \_ \_ HINT

Configuración de GL \_ POINT \_ SMOOTH \_ HINT

Configuración DE GL \_ LINE \_ SMOOTH \_ HINT

Configuración DE \_ SMOOTH HINT de GL POLYGON \_ \_

Configuración \_ de GL GL HINT \_

</dd> <dt>

<span id="GL_LIGHTING_BIT"></span><span id="gl_lighting_bit"></span>GL \_ LIGHTING \_ BIT
</dt> <dd>

GL \_ COLOR MATERIAL enable \_ bit

Valor DE \_ GL \_ COLOR MATERIAL \_ FACE

Parámetros de material de color que están siguiendo el color actual

Color de la escena ambiente

Valor del VISOR LOCAL DE GL \_ LIGHT \_ MODEL \_ \_

Configuración \_ DE GL LIGHT MODEL TWO \_ \_ \_ SIDE

GL \_ LIGHTING enable bit

Habilitar bit para cada luz

Intensidad ambiental, difusa y especular para cada luz

Dirección, posición, exponente y ángulo de límite para cada luz

Factores de atenuación constante, lineal y cuadrática para cada luz

Color ambiente, difuso, especular y emisivo para cada material

Índices de color ambiente, difuso y especular para cada material

Exponente especular para cada valor de MATERIAL GL \_ SHADE \_ MODEL

</dd> <dt>

<span id="GL_LINE_BIT_"></span><span id="gl_line_bit_"></span>GL \_ LINE \_ BIT 
</dt> <dd>

Marca GL \_ LINE \_ SMOOTH

Bit \_ de habilitación de GL LINE \_ STIPPLE

Patrón de stipple de línea y contador de repetición

Ancho de línea

</dd> <dt>

<span id="GL_LIST_BIT"></span><span id="gl_list_bit"></span>GL \_ LIST \_ BIT
</dt> <dd>

Configuración de GL \_ LIST \_ BASE

</dd> <dt>

<span id="GL_PIXEL_MODE_BIT"></span><span id="gl_pixel_mode_bit"></span>BIT \_ DE MODO DE PÍXEL \_ \_ GL
</dt> <dd>

Configuración \_ de GL RED \_ BIAS y GL RED \_ \_ SCALE

Valores \_ GL GREEN \_ BIAS y GL GREEN \_ \_ SCALE

GL \_ BLUE \_ BIAS y GL BLUE \_ \_ SCALE

GL \_ ALPHA \_ BIAS y GL ALPHA \_ \_ SCALE

GL \_ DEPTH \_ BIAS y GL DEPTH \_ \_ SCALE

Valores GL \_ INDEX OFFSET y GL INDEX \_ \_ \_ SHIFT

Marcas GL \_ MAP COLOR y GL MAP \_ \_ \_ STENCIL

Factores \_ ZOOM X y GL ZOOM Y \_ \_ \_ de GL

Configuración de \_ READ BUFFER de GL \_

</dd> <dt>

<span id="GL_POINT_BIT"></span><span id="gl_point_bit"></span>GL \_ POINT \_ BIT
</dt> <dd>

Marca GL \_ POINT \_ SMOOTH

Tamaño del punto

</dd> <dt>

<span id="GL_POLYGON_BIT"></span><span id="gl_polygon_bit"></span>GL \_ POLYGON \_ BIT
</dt> <dd>

GL \_ CULL \_ FACE enable bit

Valor DE \_ GL CULL \_ FACE \_ MODE

Indicador \_ GL FRONT \_ FACE

Configuración del \_ MODO DE POLÍGONO DE GL \_

Marca GL \_ POLYGON \_ SMOOTH

Bit \_ de habilitación de GL POLYGON \_ STIPPLE

Marca GL \_ POLYGON \_ OFFSET \_ FILL

Marca GL \_ POLYGON \_ OFFSET \_ LINE

Marca GL \_ POLYGON \_ OFFSET \_ POINT

FACTOR DE \_ DESPLAZAMIENTO \_ DE POLÍGONO \_ GL

UNIDADES DE \_ \_ DESPLAZAMIENTO DE POLÍGONO \_ DE GL

</dd> <dt>

<span id="GL_POLYGON_STIPPLE_BIT"></span><span id="gl_polygon_stipple_bit"></span>GL \_ POLYGON \_ STIPPLE \_ BIT
</dt> <dd>

Imagen detippla de polígono

</dd> <dt>

<span id="GL_SCISSOR_BIT"></span><span id="gl_scissor_bit"></span>BIT \_ DE RESALTE \_ DE GL
</dt> <dd>

Marca \_ DE PRUEBA DE GL \_ SESO

Cuadro de verificación

</dd> <dt>

<span id="GL_STENCIL_BUFFER_BIT"></span><span id="gl_stencil_buffer_bit"></span>BIT DE \_ BÚFER DE GALERÍA DE SÍMBOLOS DE \_ \_ GL
</dt> <dd>

GL \_ STENCIL \_ TEST enable bit

Función de galería de símbolos y valor de referencia

Máscara de valor de galería de símbolos

Acciones de paso de búfer de profundidad, paso y error de galería de símbolos

Valor sin borrar del búfer de galería de símbolos

Máscara de escritura del búfer de galería de símbolos

</dd> <dt>

<span id="GL_TEXTURE_BIT"></span><span id="gl_texture_bit"></span>BIT \_ DE TEXTURA \_ GL
</dt> <dd>

Habilitar bits para las cuatro coordenadas de textura

Color de borde para cada imagen de textura

Función de minificación para cada imagen de textura

Función de ampliación para cada imagen de textura

Coordenadas de textura y modo de ajuste para cada imagen de textura

Color y modo para cada entorno de textura

Habilitar bits GL \_ TEXTURE \_ GEN \_ *x*; *x* es S, T, R y Q

Configuración del MODO GEN DE TEXTURA DE GL \_ \_ para \_ S, T, R y Q

Ecuaciones de plano glTexGen para S, T, R y Q

</dd> <dt>

<span id="GL_TRANSFORM_BIT"></span><span id="gl_transform_bit"></span>GL \_ TRANSFORM \_ BIT
</dt> <dd>

Coeficientes de los seis planos de recorte

Habilitar bits para los planos de recorte definibles por el usuario

Valor DEL \_ \_ MODO DE MATRIZ DE GL

Marca \_ NORMALIZE de GL

</dd> <dt>

<span id="GL_VIEWPORT_BIT"></span><span id="gl_viewport_bit"></span>GL \_ VIEWPORT \_ BIT
</dt> <dd>

Intervalo de profundidad (cerca y lejos)

Origen y extensión de la ventanilla

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ STACK \_ OVERFLOW**</dt> </dl>    | Se llamó a la función mientras la pila de atributos estaba llena.<br/>                                                                |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentarios

La **función glPushAttrib** toma un argumento, una máscara que indica qué grupos de variables de estado se guardarán en la pila de atributos. Las constantes simbólicas se usan para establecer bits en la máscara. Normalmente, el parámetro mask se construye aplicando la operación **OR** lógica a varias de estas constantes. Puede usar la máscara especial GL \_ ALL \_ ATTRIB \_ BITS para guardar todos los estados apilables.

La [**función glPopAttrib**](glpopattrib.md) restaura los valores de las variables de estado guardadas con el último **comando glPushAttrib.** Los no guardados se mantienen sin cambios.

Es un error insertar atributos en una pila completa o quitar atributos de una pila vacía. En cualquier caso, se establece la marca de error y no se realiza ningún otro cambio en el estado OpenGL.

Inicialmente, la pila de atributos está vacía.

No todos los valores del estado OpenGL se pueden guardar en la pila de atributos. Por ejemplo, no puede guardar el paquete de píxeles y desempaquetar el estado, representar el estado del modo y seleccionar y el estado de comentarios.

La profundidad de la pila de atributos depende de la implementación, pero debe ser al menos 16.

Las funciones siguientes recuperan información relacionada **con glPushAttrib** y [**glPopAttrib**](glpopattrib.md):

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento GL \_ ATTRIB \_ STACK \_ DEPTH

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento GL \_ MAX \_ ATTRIB \_ STACK \_ DEPTH

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glGetClipPlane**](glgetclipplane.md)
</dt> <dt>

[**glGetError**](glgeterror.md)
</dt> <dt>

[**glGetLight**](glgetlight.md)
</dt> <dt>

[**glGetMap**](glgetmap.md)
</dt> <dt>

[**glGetMaterial**](glgetmaterial.md)
</dt> <dt>

[**glGetPixelMap**](glgetpixelmap.md)
</dt> <dt>

[**glGetPolygonStipple**](glgetpolygonstipple.md)
</dt> <dt>

[**glGetString**](glgetstring.md)
</dt> <dt>

[**glGetTexEnv**](glgettexenv.md)
</dt> <dt>

[**glGetTexGen**](glgettexgen.md)
</dt> <dt>

[**glGetTexImage**](glgetteximage.md)
</dt> <dt>

[**glGetTexLevelParameter**](glgettexlevelparameter.md)
</dt> <dt>

[**glGetTexParameter**](glgettexparameter.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> </dl>

 

 





