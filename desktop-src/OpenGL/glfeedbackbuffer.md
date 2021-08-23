---
title: Función glFeedbackBuffer (Gl.h)
description: La función glFeedbackBuffer controla el modo de comentarios.
ms.assetid: fe3773a7-c264-4d49-8f90-1f2319f9af4f
keywords:
- Función glFeedbackBuffer OpenGL
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
ms.openlocfilehash: 76e51a08dac2bbf55509d4964218fc4b844581c797220294464b84c05de5e05b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580205"
---
# <a name="glfeedbackbuffer-function"></a>Función glFeedbackBuffer

La **función glFeedbackBuffer** controla el modo de comentarios.

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

Constante simbólica que describe la información que se devolverá para cada vértice. Se aceptan las siguientes constantes simbólicas: GL \_ 2D, GL \_ 3D, GL \_ 3D \_ COLOR, GL \_ 3D COLOR TEXTURE y \_ GL \_ \_ 4D \_ COLOR \_ TEXTURE.

</dd> <dt>

*Búfer* 
</dt> <dd>

Devuelve los datos de comentarios.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERACIÓN \_ NO \_ VÁLIDA DE GL**</dt> </dl>      | *Type* no era un valor aceptado.<br/>                                                                                                                                                                           |
| <dl> <dt>**ENUMERACIÓN \_ NO \_ VÁLIDA DE GL**</dt> </dl>      | *el tamaño* era negativo.<br/>                                                                                                                                                                                        |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | **Se llamó a glFeedbackBuffer** mientras el modo de representación era GL FEEDBACK o se llamó a glRenderMode con el argumento GL FEEDBACK antes de llamar a \_ [](glrendermode.md) \_ **glFeedbackBuffer** al menos una vez.<br/> |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/>                                                                                  |



## <a name="remarks"></a>Comentarios

La **función glFeedbackBuffer** controla los comentarios. Los comentarios, como la selección, son un modo OpenGL. El modo se selecciona mediante una llamada [**a glRenderMode**](glrendermode.md) con GL \_ FEEDBACK. Cuando OpenGL está en modo de comentarios, la rasterización no genera píxeles. En su lugar, la información sobre los primitivos que se hubieran rasterizado se vuelve a proporcionar a la aplicación mediante OpenGL.

La **función glFeedbackBuffer** tiene tres argumentos:

-   *buffer* es un puntero a una matriz de valores de punto flotante en la que se coloca información de comentarios.
-   *size* indica el tamaño de la matriz.
-   *Type* es una constante simbólica que describe la información que se alimenta de nuevo para cada vértice.

Debe emitir **glFeedbackBuffer antes** de habilitar el modo de comentarios (llamando **a glRenderMode** con el argumento GL \_ FEEDBACK). Establecer GL FEEDBACK sin establecer el búfer de comentarios o llamar \_ **a glFeedbackBuffer** mientras OpenGL está en modo de comentarios, es un error.

Para quitar OpenGL del modo de comentarios, llame a [**glRenderMode**](glrendermode.md) con un valor de parámetro distinto de GL \_ FEEDBACK. Cuando se hace mientras OpenGL está en modo de comentarios, **glRenderMode** devuelve el número de entradas colocadas en la matriz de comentarios. El valor devuelto nunca supera el *tamaño*. Si los datos de comentarios requerían más espacio del que estaba disponible en el *búfer,* **glRenderMode** devuelve un valor negativo.

En el modo de comentarios, cada primitivo que se rasterizaría genera un bloque de valores que se copia en la matriz de comentarios. Si lo hace, el número de entradas superaría el máximo, **glFeedbackBuffer** escribe parcialmente el bloque para rellenar la matriz (si queda espacio) y establece una marca de desbordamiento. Cada bloque comienza con un código que indica el tipo primitivo, seguido de valores que describen los vértices de la primitiva y los datos asociados. La **función glFeedbackBuffer** también escribe entradas para mapas de bits y rectángulos de píxeles. Los comentarios se producen después de que se haya realizado la selección de polígonos y la interpretación [**glPolygonMode**](glpolygonmode.md) de los polígonos, por lo que los polígonos que se han realizado la selección no se devuelven en el búfer de comentarios. También puede producirse después de que los polígonos con más de tres bordes se divide en triángulos, si la implementación de OpenGL representa polígonos realizando esta descomposición.

Puede insertar un marcador en el búfer de comentarios [**con glPassThrough.**](glpassthrough.md)

A continuación se muestra la gramática de los bloques de valores escritos en el búfer de comentarios. Cada primitivo se indica con un valor de identificación único seguido de un número de vértices. Las entradas de polígono incluyen un valor entero que indica cuántos vértices siguen. Un vértice se introduce como un número determinado de valores de punto flotante, determinado por *el tipo*. Los colores se alimentan como cuatro valores en modo RGBA y un valor en modo de índice de color.

feedbackList < feedbackItem feedbackList \| feedbackItem

feedbackItem < point \| lineSegment \| polygon bitmap \| \| pixelRectangle \| passThru

point < vértice GL \_ POINT \_ TOKEN

lineSegment < vértice de vértice GL \_ LINE TOKEN GL LINE RESET TOKEN vertex vertex \_ \| \_ \_ \_ vertex

polygon < GL \_ POLYGON \_ TOKEN n polySpec

polySpec < vértice de vértice polySpec vértice \| vértice

mapa de bits < vértice \_ DE TOKEN DE MAPA DE BITS DE \_ GL

pixelRectangle < vértice \_ GL DRAW \_ PIXEL TOKEN GL COPY PIXEL TOKEN \_ \| \_ \_ \_ vertex

passThru < VALOR DE TOKEN \_ DE PASO A TRAVÉS \_ \_ DE GL

vertex < 2d \| 3d \| 3dColor \| 3dColorTexture \| 4dColorTexture

Valor de < 2d

3d < valor de valor

Color de valor < 3dColor

3dColorTexture < value value color tex

4dColorTexture < value value value color texas

color < rgba \| index

rgba < value value value value

index < value

valor < valor de valor de texas

El *parámetro* value es un número de punto flotante y *n* es un entero de punto flotante que da el número de vértices en el polígono. Las siguientes son constantes de punto flotante simbólico: GL \_ POINT \_ TOKEN, GL \_ LINE \_ TOKEN, GL LINE RESET \_ \_ \_ TOKEN, GL POLYGON \_ \_ TOKEN, GL BITMAP \_ \_ TOKEN, GL DRAW PIXEL \_ TOKEN, GL COPY PIXEL TOKEN y \_ \_ GL PASS THROUGH \_ \_ \_ \_ \_ \_ TOKEN. GL LINE RESET TOKEN se devuelve cada vez que se restablece el patrón \_ \_ \_ detippla de línea. Los datos devueltos como vértices dependen del tipo de *comentarios*.

En la tabla siguiente se proporciona la correspondencia entre *el tipo* y el número de valores por vértice; *k* es 1 en modo de índice de color y 4 en modo RGBA.



| Tipo                   | Coordenadas        | Color | Textura | Número total de valores |
|------------------------|--------------------|-------|---------|------------------------|
| GL \_ 2D                 | *x*, *y*           |       |         | 2                      |
| GL \_ 3D                 | *x*, *y*, *z*      |       |         | 3                      |
| GL \_ 3D \_ COLOR          | *x*, *y*, *z*      | *K*   |         | 3 + *k*                |
| TEXTURA DE COLOR GL \_ 3D \_ \_ | *x*, *y*, *z*,     | *K*   | 4       | 7 + *k*                |
| TEXTURA \_ DE COLOR 4D GL \_ \_ | *x*, *y*, *z*, *w* | *K*   | 4       | 8 + *k*                |



 

Las coordenadas de vértice de comentarios están en coordenadas de ventana, *excepto w*, que está en coordenadas de recorte. Los colores de los comentarios se encienden, si la iluminación está habilitada. Se generan coordenadas de textura de comentarios, si la generación de coordenadas de textura está habilitada. Siempre se transforman mediante la matriz de textura.

La **función glFeedbackBuffer,** cuando se usa en una lista de visualización, no se compila en la lista de visualización, sino que se ejecuta inmediatamente.

La función siguiente recupera información relacionada con **glFeedbackBuffer**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ RENDER \_ MODE

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

 

 





