---
title: función glFeedbackBuffer (GL. h)
description: La función glFeedbackBuffer controla el modo de comentarios.
ms.assetid: fe3773a7-c264-4d49-8f90-1f2319f9af4f
keywords:
- glFeedbackBuffer (función) OpenGL
topic_type:
- apiref
api_name:
- glFeedbackBuffer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e64b232db640d41ca9a1e1f75d6ab766597d6511
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105666033"
---
# <a name="glfeedbackbuffer-function"></a>glFeedbackBuffer función)

La función **glFeedbackBuffer** controla el modo de comentarios.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glFeedbackBuffer(
   GLsizei size,
   GLenum  type,
   GLfloat *buffer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*size* 
</dt> <dd>

Número máximo de valores que se pueden escribir en el *búfer*.

</dd> <dt>

*type* 
</dt> <dd>

Una constante simbólica que describe la información que se devolverá para cada vértice. Se aceptan las siguientes constantes simbólicas: GL \_ 2D, GL \_ 3D, GL \_ 3D \_ color, GL \_ 3D \_ color \_ Texture y GL \_ 4D \_ color \_ Texture.

</dd> <dt>

*búfer* 
</dt> <dd>

Devuelve los datos de los comentarios.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>      | el *tipo* no era un valor aceptado.<br/>                                                                                                                                                                           |
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>      | *el tamaño* era negativo.<br/>                                                                                                                                                                                        |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | se llamó a **glFeedbackBuffer** mientras el modo de representación era comentarios de contabilidad \_ , o bien se llamó a [**glRenderMode**](glrendermode.md) con los comentarios de contabilidad de argumentos \_ antes de que se llamara a **glFeedbackBuffer** al menos una vez.<br/> |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/>                                                                                  |



## <a name="remarks"></a>Observaciones

La función **glFeedbackBuffer** controla los comentarios. Los comentarios, como la selección, son un modo OpenGL. El modo se selecciona llamando a [**glRenderMode**](glrendermode.md) con comentarios de contabilidad \_ . Cuando OpenGL está en modo de comentarios, no se genera ningún píxel mediante la rasterización. En su lugar, la información acerca de los primitivos que se habrían rasterizado se devolverá a la aplicación mediante OpenGL.

La función **glFeedbackBuffer** tiene tres argumentos:

-   *buffer* es un puntero a una matriz de valores de punto flotante en el que se coloca información de comentarios.
-   *tamaño* indica el tamaño de la matriz.
-   *Type* es una constante simbólica que describe la información que se devuelve para cada vértice.

Debe emitir **glFeedbackBuffer** antes de que se habilite el modo de comentarios (llamando a **glRenderMode** con los comentarios de contabilidad de argumentos \_ ). La configuración \_ de comentarios de contabilidad sin establecer el búfer de comentarios, o la llamada a **GlFeedbackBuffer** mientras OpenGL está en modo de comentarios, es un error.

Saque el modo de comentarios de OpenGL mediante una llamada a [**glRenderMode**](glrendermode.md) con un valor de parámetro distinto de comentarios de contabilidad \_ . Al hacerlo mientras OpenGL está en modo de comentarios, **glRenderMode** devuelve el número de entradas colocadas en la matriz de comentarios. El valor devuelto nunca supera el *tamaño*. Si los datos de comentarios requirieron más espacio que el disponible en el *búfer*, **glRenderMode** devuelve un valor negativo.

En el modo de comentarios, cada primitiva que se va a rasterizar genera un bloque de valores que se copia en la matriz de comentarios. Si esto haría que el número de entradas superara el máximo, **glFeedbackBuffer** escribe parcialmente el bloque para rellenar la matriz (si hay alguna habitación) y establece una marca de desbordamiento. Cada bloque comienza con un código que indica el tipo primitivo, seguido de los valores que describen los vértices del primitivo y los datos asociados. La función **glFeedbackBuffer** también escribe entradas para los mapas de bits y los rectángulos de píxeles. Los comentarios se producen después de la selección de polígono y la interpretación [**glPolygonMode**](glpolygonmode.md) de los polígonos ha tenido lugar, por lo que los polígonos que se seleccionan no se devuelven en el búfer de comentarios. También se puede producir después de que los polígonos con más de tres bordes se dividan en triángulos, si la implementación de OpenGL representa polígonos realizando esta descomposición.

Puede insertar un marcador en el búfer de comentarios con [**glPassThrough**](glpassthrough.md).

A continuación se encuentra la gramática de los bloques de valores escritos en el búfer de comentarios. Cada primitiva se indica con un valor de identificación único seguido de un número de vértices. Las entradas de polígono incluyen un valor entero que indica el número de vértices que siguen. Un vértice se devolverá como cierto número de valores de punto flotante, según lo determinado por el *tipo*. Los colores se devuelven como cuatro valores en el modo RGBA y un valor en modo de índice de color.

feedbackList < feedbackItem feedbackList \| feedbackItem

mapa de bits de < feedbackItem punto de \| segmento de segmento \| \| \| pixelRectangle \| passThru

punto < vértice del token del \_ punto de contabilidad \_

lineSegment < token de línea de libro de la línea de \_ \_ \| libro \_ \_ \_

Polygon < token de polígono de GL \_ \_ n polispec

vértice de vértice de vértice del vértice de polispec < polispec \|

mapa de bits < vértice del token de mapa de bits de GL \_ \_

pixelRectangle < libro de píxeles del token de píxel de la \_ \_ \_ \| \_ copia GL \_ \_ del vértice del token de píxel

passThru < el valor del token de la contabilidad de \_ paso \_ a través \_

Vertex < 2D \| 3D \| 3dColor \| 3dColorTexture \| 4dColorTexture

valor de < 2D

valor de valor de valor de < 3D

color del valor de 3dColor < valor de valor

3dColorTexture < valor color valor Tex

4dColorTexture < valor Value valor color Tex

color < \| Índice RGBA

RGBA < valor del valor del valor de valor

valor de < de índice

Tex < valor del valor del valor del valor

El parámetro de *valor* es un número de punto flotante y *n* es un entero de punto flotante que indica el número de vértices del polígono. Las siguientes son constantes de punto flotante simbólicas: token de punto de contabilidad general \_ \_ , token de línea de contabilidad \_ \_ , token de \_ restablecimiento de línea de libro de contabilidad \_ \_ , \_ \_ token de polígono de GL, token de mapa de bits de contabilidad, token de píxel de dibujo de GL, token de píxel de copia de contabilidad y token de \_ \_ \_ \_ \_ \_ \_ \_ paso de contab \_ \_ \_ . \_ \_ \_ El token de restablecimiento de línea de contabilidad se devuelve cuando se restablece el patrón punteado de línea. Los datos devueltos como vértice dependen del *tipo* de comentario.

En la tabla siguiente se proporciona la correspondencia entre el *tipo* y el número de valores por vértice; *k* es 1 en modo de índice de color y 4 en modo RGBA.



| Tipo                   | Coordenadas        | Color | Textura | Número total de valores |
|------------------------|--------------------|-------|---------|------------------------|
| GL en \_ 2D                 | *x*, *y*           |       |         | 2                      |
| GL \_ 3D                 | *x*, *y*, *z*      |       |         | 3                      |
| \_Color 3D de GL \_          | *x*, *y*, *z*      | *k*   |         | 3 + *k*                |
| \_Textura de \_ color \_ 3D de GL | *x*, *y*, *z*,     | *k*   | 4       | 7 + *k*                |
| \_Textura de \_ color \_ 4D de GL | *x*, *y*, *z*, *w* | *k*   | 4       | 8 + *k*                |



 

Las coordenadas de los vértices de comentarios se encuentran en coordenadas de ventana, excepto *w*, que está en coordenadas de recorte. Los colores de los comentarios se iluminan si la iluminación está habilitada. Se generan coordenadas de textura de comentarios si está habilitada la generación de coordenadas de textura. Siempre se transforman mediante la matriz de textura.

La función **glFeedbackBuffer** , cuando se usa en una lista de visualización, no se compila en la lista de visualización, sino que se ejecuta inmediatamente.

La siguiente función recupera información relacionada con **glFeedbackBuffer**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el \_ modo de representación de contabilidad de argumentos \_

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

[**glLineStipple**](gllinestipple.md)
</dt> <dt>

[**glPassThrough**](glpassthrough.md)
</dt> <dt>

[**glPolygonMode**](glpolygonmode.md)
</dt> <dt>

[**glRenderMode**](glrendermode.md)
</dt> <dt>

[**glSelectBuffer**](glselectbuffer.md)
</dt> </dl>

 

 





