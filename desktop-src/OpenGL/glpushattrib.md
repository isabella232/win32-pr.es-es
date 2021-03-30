---
title: función glPushAttrib (GL. h)
description: Envía la pila de atributos.
ms.assetid: 3c7b93cc-2112-4771-b422-a244821447e5
keywords:
- glPushAttrib (función) OpenGL
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
ms.openlocfilehash: 9e0bc15b85ddca3bdbe5f6774b5368c6f0cde8dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079055"
---
# <a name="glpushattrib-function"></a>glPushAttrib función)

Envía la pila de atributos.

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

Máscara que indica los atributos que se van a guardar. Las constantes de máscara simbólica y su estado de OpenGL asociado son las siguientes (la lista de párrafos con sangría que se guardan):

<dl> <dt>

<span id="GL_ACCUM_BUFFER_BIT_"></span><span id="gl_accum_buffer_bit_"></span>\_bit de \_ búfer de acumulación de GL \_ 
</dt> <dd>

Valor de eliminación de búfer de acumulación

</dd> <dt>

<span id="GL_COLOR_BUFFER_BIT"></span><span id="gl_color_buffer_bit"></span>\_bit de \_ búfer de color de contabilidad \_
</dt> <dd>

\_Bit de \_ habilitación de pruebas alfa de GL

Función de prueba alfa y valor de referencia

\_Bit de habilitación de GL Blend

Combinar funciones de origen y de destino

\_Bit de habilitación de trama de GL

Configuración de búfer de \_ dibujo de GL \_

\_Bit de habilitación de la lógica de GL \_

Logic OP (función)

Valores claros en modo de color e índice

Modo de color y writemasks de modo de índice

</dd> <dt>

<span id="GL_CURRENT_BIT"></span><span id="gl_current_bit"></span>\_bits actual de GL \_
</dt> <dd>

Color RGBA actual

Índice de color actual

Vector normal actual

Coordenadas de textura actuales

Posición de la trama actual \_ de contab \_ \_ \_

Color RGBA asociado a la posición de la trama actual

Índice de color asociado a la posición de la trama actual

Coordenadas de textura asociadas a la posición de la trama actual

Marca de marca de \_ borde de GL \_

</dd> <dt>

<span id="GL_DEPTH_BUFFER_BIT"></span><span id="gl_depth_buffer_bit"></span>\_bit de \_ búfer de profundidad de contabilidad \_
</dt> <dd>

\_Bit de \_ habilitación de prueba de profundidad de GL

Función de prueba de búfer de profundidad

Valor de borrar del búfer de profundidad

\_Bit de \_ habilitación de WRITEMASK de profundidad de GL

</dd> <dt>

<span id="GL_ENABLE_BIT"></span><span id="gl_enable_bit"></span>\_bit de habilitación de GL \_
</dt> <dd>

Marca de prueba de GL \_ alfa \_

\_Marca de \_ normalización automática de GL

\_Marca GL Blend

Habilitar bits para los planos de recorte definibles por el usuario

\_material de color GL \_

Marca de cara de \_ selección de contabilidad \_

Marca de prueba de \_ profundidad de GL \_

\_Marca de interpolación de contabilidad

Marca de niebla de GL \_

GL \_ Light *i* , donde 0 <= *i* < \_ \_ Lights Max GL

Marca de iluminación de GL \_

\_Marca de suavizado de línea de contabilidad \_

\_Marca punteada de línea de contabilidad \_

\_Marca de \_ operación de lógica de color de GL \_

\_Marca de \_ OP de lógica de índice de GL \_

GL \_ MAP1 \_ x, donde x es un tipo de mapa

GL \_ MAP2 ( \_ x, donde x es un tipo de mapa

\_Marca de normalización de contabilidad

\_Marca de suavizado de punto de contabilidad \_

\_Marca de \_ línea de desplazamiento de polígono de GL \_

\_Marca de \_ relleno de desplazamiento de polígono de GL \_

\_Marca de \_ punto de desplazamiento de polígono de GL \_

\_Marca de Polígono suave de GL \_

\_ \_ Marca punteada de GL poligonal

Marca de prueba de \_ tijera de GL \_

Marca de prueba de \_ estarcido de GL \_

\_Marca de textura 1D de GL \_

\_Marca 2D de textura GL \_

Marcas GL \_ Texture \_ \_ x, donde x es S, T, R o Q

</dd> <dt>

<span id="GL_EVAL_BIT"></span><span id="gl_eval_bit"></span>\_bit de evaluación de GL \_
</dt> <dd>

GL \_ MAP1 \_ x habilitar bits, donde x es un tipo de mapa

GL \_ MAP2 ( \_ x habilitar bits, donde x es un tipo de mapa

puntos de conexión y divisiones de la cuadrícula 1D

puntos de conexión y divisiones de la cuadrícula 2D

\_Bit de \_ habilitación de normalización automática de GL

</dd> <dt>

<span id="GL_FOG_BIT"></span><span id="gl_fog_bit"></span>\_bit de niebla de contabilidad \_
</dt> <dd>

\_Marca de habilitación de niebla de GL

Color de niebla

Densidad de niebla

Inicio de niebla lineal

Finalización de la niebla lineal

Índice de niebla

Valor del modo de \_ niebla de contabilidad \_

</dd> <dt>

<span id="GL_HINT_BIT"></span><span id="gl_hint_bit"></span>\_bit de sugerencia de GL \_
</dt> <dd>

\_Configuración de \_ sugerencia de corrección de perspectiva de GL \_

\_Valor de \_ sugerencia de suavizado de punto de contabilidad \_

\_Valor de \_ sugerencia de suavizado de línea de contabilidad \_

\_Valor de \_ sugerencia de suavizado de polígono de GL \_

Configuración de la sugerencia de niebla de GL \_ \_

</dd> <dt>

<span id="GL_LIGHTING_BIT"></span><span id="gl_lighting_bit"></span>\_bit de iluminación de GL \_
</dt> <dd>

\_Bit de \_ habilitación del material de color GL

\_Valor de \_ superficie de material de color de GL \_

Parámetros de material de color que están realizando el seguimiento del color actual

Color de la escena ambiente

\_Valor del \_ \_ visor local del modelo de contabilidad solar \_

\_Configuración de \_ \_ dos \_ lados del modelo de contabilidad solar

\_Bit de habilitación de iluminación de GL

Habilitar bit para cada luz

Intensidad de ambiente, difuso y especular para cada luz

Dirección, posición, exponente y ángulo límite para cada luz

Factores de atenuación constante, lineal y cuadrático para cada luz

Color ambiente, difuso, especular y emisor para cada material

Índices de color ambiente, difuso y especular para cada material

Exponente especular para cada \_ configuración de modelo de sombreado de contabilidad de materiales \_

</dd> <dt>

<span id="GL_LINE_BIT_"></span><span id="gl_line_bit_"></span>\_bit de línea de contabilidad \_ 
</dt> <dd>

\_Marca de suavizado de línea de contabilidad \_

\_Bit de habilitación de línea de contabilidad \_ punteada

Patrón punteado de línea y contador de repetición

Ancho de línea

</dd> <dt>

<span id="GL_LIST_BIT"></span><span id="gl_list_bit"></span>\_bit de lista de contab. \_
</dt> <dd>

Configuración de base de \_ lista de contabilidad \_

</dd> <dt>

<span id="GL_PIXEL_MODE_BIT"></span><span id="gl_pixel_mode_bit"></span>\_bit de \_ modo de píxel de contabilidad \_
</dt> <dd>

\_ \_ Configuración de sesgo rojo de GL y escala de rojo de contabilidad \_ \_

\_ \_ Valores de escala verde de GL y escala de verde de contabilidad \_ \_

\_Tendencia azul \_ de GL y \_ escala azul de contabilidad \_

\_Tendencia alfa \_ de contabilidad general \_ y \_ escala de alfa

\_ \_ Tendencia de profundidad de GL y \_ escala de profundidad de contabilidad \_

\_ \_ Valores de desplazamiento de índice de GL y cambio de índice de contabilidad \_ \_

\_ \_ \_ Marcas de estarcido de mapa de contabilidad y contab. \_

\_Zoom \_ de GL X y contabilidad \_ \_ y factores de zoom de GL

Configuración de búfer de \_ lectura de GL \_

</dd> <dt>

<span id="GL_POINT_BIT"></span><span id="gl_point_bit"></span>\_bit de punta de contabilidad \_
</dt> <dd>

\_Marca de suavizado de punto de contabilidad \_

Tamaño del punto

</dd> <dt>

<span id="GL_POLYGON_BIT"></span><span id="gl_polygon_bit"></span>\_bit de polígono de GL \_
</dt> <dd>

\_Bit de \_ habilitación de la cara de selección de contabilidad

\_Valor del \_ modo de cara de selección de contabilidad \_

\_Indicador de cara frontal de contabilidad \_

\_Configuración de modo polígono de GL \_

\_Marca de Polígono suave de GL \_

\_Bit de habilitación de los polígonos de GL \_

\_Marca de \_ relleno de desplazamiento de polígono de GL \_

\_Marca de \_ línea de desplazamiento de polígono de GL \_

\_Marca de \_ punto de desplazamiento de polígono de GL \_

\_factor de \_ desplazamiento de polígono de GL \_

\_unidades de \_ desplazamiento de polígono de GL \_

</dd> <dt>

<span id="GL_POLYGON_STIPPLE_BIT"></span><span id="gl_polygon_stipple_bit"></span>\_bit de \_ punteado de los polígonos de contabilidad \_
</dt> <dd>

Imagen de punteado de polígono

</dd> <dt>

<span id="GL_SCISSOR_BIT"></span><span id="gl_scissor_bit"></span>\_bit de tijera de GL \_
</dt> <dd>

Marca de prueba de \_ tijera de GL \_

Cuadro de tijeras

</dd> <dt>

<span id="GL_STENCIL_BUFFER_BIT"></span><span id="gl_stencil_buffer_bit"></span>\_bit de \_ búfer de estarcido GL \_
</dt> <dd>

\_Habilitar bits de la prueba de estarcido GL \_

Función de estarcido y valor de referencia

Máscara de valor de estarcido

Acciones de paso de búfer de error, de paso y de profundidad de la galería de símbolos

Valor sin formato del búfer de estarcido

Búfer de estarcido writemask

</dd> <dt>

<span id="GL_TEXTURE_BIT"></span><span id="gl_texture_bit"></span>\_bit de textura de GL \_
</dt> <dd>

Habilitar bits para las cuatro coordenadas de textura

Color de borde de cada imagen de textura

Función minificación para cada imagen de textura

Función de ampliación para cada imagen de textura

Coordenadas de textura y el modo de ajuste para cada imagen de textura

Color y modo para cada entorno de textura

Habilitar la textura GL de bits \_ \_ gen \_ *x*; *x* es S, T, R y Q

\_ \_ \_ Configuración del modo de generación de texturas GL para S, T, R y Q

ecuaciones de plano glTexGen para S, T, R y Q

</dd> <dt>

<span id="GL_TRANSFORM_BIT"></span><span id="gl_transform_bit"></span>\_bit de transformación de contabilidad \_
</dt> <dd>

Coeficientes de los seis planos de recorte

Habilitar bits para los planos de recorte definibles por el usuario

Valor del modo de \_ matriz de contabilidad \_

\_Marca de normalización de contabilidad

</dd> <dt>

<span id="GL_VIEWPORT_BIT"></span><span id="gl_viewport_bit"></span>\_bit de ventanilla de GL \_
</dt> <dd>

Rango de profundidad (Near y Far)

Origen y extensión de la ventanilla

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**desbordamiento de la pila de GL \_ \_**</dt> </dl>    | Se llamó a la función mientras la pila de atributos estaba llena.<br/>                                                                |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La función **glPushAttrib** toma un argumento, una máscara que indica los grupos de variables de estado que se van a guardar en la pila de atributos. Las constantes simbólicas se utilizan para establecer bits en la máscara. El parámetro Mask se construye normalmente aplicando la operación **or** lógica a varias de estas constantes. Puede usar la máscara especial GL \_ All \_ attrib \_ bits para guardar todos los Estados apilables.

La función [**glPopAttrib**](glpopattrib.md) restaura los valores de las variables de estado guardadas con el último comando **glPushAttrib** . Los que no se han guardado permanecen inalterados.

Es un error insertar atributos en una pila completa o desactivar los atributos de una pila vacía. En cualquier caso, se establece la marca de error y no se realiza ningún otro cambio en el estado de OpenGL.

Inicialmente, la pila de atributos está vacía.

No todos los valores del estado de OpenGL se pueden guardar en la pila de atributos. Por ejemplo, no puede guardar el paquete de píxeles y desempaquetar, el estado del modo de representación y el estado de selección y de comentarios.

La profundidad de la pila de atributos depende de la implementación, pero debe ser al menos 16.

Las siguientes funciones recuperan información relacionada con **glPushAttrib** y [**glPopAttrib**](glpopattrib.md):

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento GL de la \_ pila de atrib \_ \_

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ profundidad máxima de la pila de Max \_ \_ \_

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
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

 

 





