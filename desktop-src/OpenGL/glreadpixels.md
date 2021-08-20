---
title: Función glReadPixels (Gl.h)
description: La función glReadPixels lee un bloque de píxeles del búfer de fotogramas.
ms.assetid: 41fbad5c-b8ca-456d-bbfc-b48c176e15b0
keywords:
- Función glReadPixels OpenGL
topic_type:
- apiref
api_name:
- glReadPixels
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b03a90fcd6ee5179a900739c40e78f796c6340d9609f4cfbeb21e6a70156afe5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937945"
---
# <a name="glreadpixels-function"></a>Función glReadPixels

La **función glReadPixels** lee un bloque de píxeles del búfer de fotogramas.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glReadPixels(
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height,
   GLenum  format,
   GLenum  type,
   GLvoid  *pixels
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*x* 
</dt> <dd>

*Coordenada x* de la ventana del primer píxel que se lee desde el búfer de fotogramas. Junto con la *coordenada y,* especifica la ubicación de la esquina inferior izquierda de un bloque rectangular de píxeles.

</dd> <dt>

*y* 
</dt> <dd>

Coordenadas de *ventana y* del primer píxel que se lee desde el búfer de fotogramas. Junto con la *coordenada x,* especifica la ubicación de la esquina inferior izquierda de un bloque rectangular de píxeles.

</dd> <dt>

*width* 
</dt> <dd>

Ancho del rectángulo de píxeles.

</dd> <dt>

*height* 
</dt> <dd>

Alto del rectángulo de píxeles. *Los* parámetros *de ancho* y alto del valor "1" corresponden a un solo píxel.

</dd> <dt>

*format* 
</dt> <dd>

Formato de los datos de píxel. Se aceptan los siguientes valores simbólicos:



| Value                                                                                                                                                                                                                                                                                                                                                                                                                                                                           | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_INDEX"></span><span id="gl_color_index"></span><dl> <dt>**GL \_ COLOR \_ INDEX**</dt> </dl>                                                                                                                                                                                                                                                                                                               | Los índices de color se leen del búfer de colores seleccionado por [**glReadBuffer.**](glreadbuffer.md) Cada índice se convierte a un punto fijo, se desplaza a la izquierda o a la derecha, en función del valor y el signo de GL INDEX SHIFT, y se agrega a \_ \_ GL INDEX \_ \_ OFFSET. Si GL MAP COLOR es GL TRUE, los índices se reemplazan por sus asignaciones en la tabla \_ GL PIXEL MAP I TO \_ \_ \_ \_ \_ \_ \_ I.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="GL_STENCIL_INDEX"></span><span id="gl_stencil_index"></span><dl> <dt>**GL \_ STENCIL \_ INDEX**</dt> </dl>                                                                                                                                                                                                                                                                                                         | Los valores de galería de símbolos se leen desde el búfer de galería de símbolos. Cada índice se convierte a un punto fijo, se desplaza a la izquierda o a la derecha, en función del valor y el signo de GL INDEX SHIFT, y se agrega a \_ \_ GL INDEX \_ \_ OFFSET. Si GL \_ MAP STENCIL es GL TRUE, los índices se reemplazan por sus asignaciones en la tabla \_ GL PIXEL MAP S TO \_ \_ \_ \_ \_ \_ S.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="GL_DEPTH_COMPONENT"></span><span id="gl_depth_component"></span><dl> <dt>**COMPONENTE \_ DE PROFUNDIDAD DE \_ GL**</dt> </dl>                                                                                                                                                                                                                                                                                                   | Los valores de profundidad se leen desde el búfer de profundidad. Cada componente se convierte en punto flotante de forma que el valor de profundidad mínimo se asigna a 0,0 y el valor máximo se asigna a 1,0. A continuación, cada componente se multiplica por GL DEPTH SCALE, se agrega a GL DEPTH BIAS y, por último, se fija al \_ \_ intervalo \_ \_ \[ 0,1. \]<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="GL_RED__GL_GREEN__GL_BLUE__GL_ALPHA__GL_RGB__GL_RGBA__GL_BGR_EXT__GL_BGRA_EXT__GL_LUMINANCE__GL_LUMINANCE_ALPHA"></span><span id="gl_red__gl_green__gl_blue__gl_alpha__gl_rgb__gl_rgba__gl_bgr_ext__gl_bgra_ext__gl_luminance__gl_luminance_alpha"></span><dl> <dt>**GL \_ RED, GL \_ GREEN, GL \_ BLUE, GL \_ ALPHA, GL \_ RGB, GL \_ RGBA, GL \_ BGR \_ EXT, GL \_ BGRA \_ EXT, GL \_ LUMINANCE, GL \_ LUMINANCE \_ ALPHA**</dt> </dl> | El procesamiento difiere en función de si los búferes de color almacenan índices de color o componentes de color RGBA. Si se almacenan índices de color, se leen desde el búfer de color seleccionado por [**glReadBuffer.**](glreadbuffer.md) Cada índice se convierte a un punto fijo, se desplaza a la izquierda o a la derecha, en función del valor y el signo de GL INDEX SHIFT, y se agrega a \_ \_ GL INDEX \_ \_ OFFSET. A continuación, los índices se reemplazan por los valores rojo, verde, azul y alfa obtenidos mediante la indexación de las tablas GL \_ PIXEL MAP I TO \_ \_ \_ \_ R, GL PIXEL MAP \_ I TO G, GL PIXEL MAP I TO B y \_ GL PIXEL MAP I \_ \_ \_ TO \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ A. Si los componentes de color RGBA se almacenan en los búferes de color, se leen desde el búfer de colores seleccionado por **glReadBuffer.** Cada componente de color se convierte en punto flotante de forma que la intensidad cero se asigna a 0,0 y la intensidad completa se asigna a 1,0. A continuación, cada componente se multiplica por GL c SCALE y se agrega a \_ \_ GL c BIAS, donde c es GL \_ \_ \_ RED, GL \_ GREEN, GL \_ BLUE y GL \_ ALPHA. Cada componente se fija en el intervalo \[ 0,1. \] Por último, si GL MAP COLOR es GL TRUE, cada componente de color c se reemplaza por su asignación en la tabla GL PIXEL MAP c TO c, donde c de nuevo es \_ \_ GL \_ \_ \_ \_ \_ \_ \_ RED, GL \_ GREEN, GL BLUE y GL \_ \_ ALPHA. Cada componente se escala al tamaño de su tabla correspondiente antes de realizar la búsqueda. Por último, se descartan los datos innecesarios. Por ejemplo, GL RED descarta los componentes verde, azul y alfa, mientras que GL RGB descarta \_ \_ solo el componente alfa. GL LUMINANCE calcula un único valor de componente como la suma de los componentes rojo, verde y azul, y \_ GL LUMINANCE ALPHA hace lo mismo, manteniendo alfa como segundo \_ \_ valor.<br/> |



 

</dd> <dt>

*type* 
</dt> <dd>

Tipo de datos de los datos de píxel. Debe ser uno de los siguientes valores:



| Tipo                | Máscara de índice | Conversión de componentes |
|---------------------|------------|----------------------|
| GL \_ UNSIGNED \_ BYTE  | 281        | (281) *c*             |
| GL \_ BYTE            | 271        | \[(271) *c*-1 \] /2     |
| MAPA DE BITS \_ DE GL          | 1          | 1                    |
| GL \_ UNSIGNED \_ SHORT | 2 61       | (2 61) *c*            |
| GL \_ SHORT           | 2 51       | \[(2 51) *c* 1 \] /2     |
| GL \_ UNSIGNED \_ INT\_ | 2 1       | (2 1) *c*            |
| GL \_ INT             | 2 1      | \[(2 1) *c* 1 \] /2     |
| GL \_ FLOAT           | ninguno       | *c*                  |



 

</dd> <dt>

*píxeles* 
</dt> <dd>

Devuelve los datos de píxel.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERACIÓN \_ NO \_ VÁLIDA DE GL**</dt> </dl>      | *format* o *type* no era un valor aceptado.<br/>                                                                              |
| <dl> <dt>**VALOR \_ NO VÁLIDO DE \_ GL**</dt> </dl>     | El *ancho o* alto *era* negativo.<br/>                                                                                   |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | *format* era GL \_ COLOR INDEX y los \_ búferes de color almacenaban los componentes de color RGBA o BGRA.<br/>                                 |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | *format* era GL \_ STENCIL INDEX y no había ningún búfer \_ de galería de símbolos.<br/>                                                          |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | *format* era GL \_ DEPTH COMPONENT y no había ningún búfer de \_ profundidad.<br/>                                                          |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |

## <a name="remarks"></a>Comentarios

La **función glReadPixels** devuelve datos de píxeles del búfer de fotogramas, empezando por el píxel cuya esquina inferior izquierda se encuentra en la ubicación *(x*, *y*), en la memoria del cliente a partir de píxeles *de ubicación.* Varios parámetros controlan el procesamiento de los datos de píxeles antes de colocarse en la memoria del cliente. Estos parámetros se establecen con tres comandos: [**glPixelStore,**](glpixelstore-functions.md) [**glPixelTransfer**](glpixeltransfer.md)y [**glPixelMap.**](glpixelmap.md) En este tema se describen los efectos en **glReadPixels** de la mayoría, pero no en todos los parámetros especificados por estos tres comandos.

La **función glReadPixels** devuelve valores de cada píxel con la esquina inferior izquierda en (*x* + i, *y* + j) para 0 = i < *width* y 0 = j < *height*. Se dice que este píxel es *el primer* píxel de la *fila j.* Los píxeles se devuelven en orden de fila de la fila más baja a la más alta, de izquierda a derecha en cada fila.

[**GlPixelTransfer**](glpixeltransfer.md)especifica los factores de desplazamiento, escala, sesgo y búsqueda descritos anteriormente. GlPixelMap especifica el contenido de la tabla [**de búsqueda.**](glpixelmap.md)

El paso final implica convertir los índices o componentes al formato adecuado, tal y como especifica el *tipo*. Si *format* es GL COLOR INDEX o \_ GL \_ STENCIL INDEX y el tipo no es GL FLOAT, cada índice se enmascara con el valor de máscara especificado \_ \_ en la tabla  \_ siguiente. Si *type* es GL \_ FLOAT, cada índice entero se convierte al formato de punto flotante de precisión sencilla.

Si  el formato es GL \_ RED, GL \_ GREEN, GL \_ BLUE, GL \_ ALPHA, GL \_ RGB, GL \_ RGBA, GL \_ BGR \_ EXT, GL \_ BGRA \_ EXT, GL \_ LUMINANCE o GL \_ LUMINANCE \_ ALPHA  \_ y el tipo no es GL FLOAT, cada componente se multiplica por el multiplicador mostrado en la tabla anterior. Si type es GL FLOAT, cada componente se pasa tal y como está (o se convierte al formato de punto flotante de precisión sencilla del cliente si es diferente del utilizado por \_ OpenGL).

Los valores devueltos se colocan en la memoria como se muestra a continuación. Si *format* es GL \_ COLOR \_ INDEX, GL \_ STENCIL \_ INDEX, GL DEPTH \_ \_ COMPONENT, GL \_ \_ RED, GL GREEN, GL BLUE, GL ALPHA o \_ GL \_ \_ LUMINANCE,     +  se devuelve un valor único y los datos del píxel i de la fila j se colocan en la ubicación ( j ) width i . GL RGB y GL BGR EXT devuelven tres \_ valores, GL RGBA y GL BGRA EXT devuelven cuatro valores, y \_ GL \_ \_ \_ \_ \_ LUMINANCE \_ ALPHA devuelve dos valores para cada píxel, con todos los valores correspondientes a un solo píxel que ocupan espacio contiguo en píxeles. Storage parámetros establecidos por [**glPixelStore,**](glpixelstore-functions.md)como GL PACK SWAP BYTES y \_ GL PACK \_ \_ \_ \_ LSB \_ FIRST, afectan a la forma en que se escriben los datos en la memoria. Consulte [**glPixelStore para**](glpixelstore-functions.md) obtener una descripción.

Los valores de píxeles que se encuentran fuera de la ventana conectada al contexto openGL actual no están definidos.

Si se genera un error, no se realiza ningún cambio en el contenido de *píxeles*.

La función siguiente recupera información relacionada con **glReadPixels**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ INDEX \_ MODE

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glPixelMap**](glpixelmap.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glReadBuffer**](glreadbuffer.md)
</dt> </dl>

 

 





