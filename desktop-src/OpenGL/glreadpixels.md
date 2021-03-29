---
title: función glReadPixels (GL. h)
description: La función glReadPixels Lee un bloque de píxeles de fotogramas.
ms.assetid: 41fbad5c-b8ca-456d-bbfc-b48c176e15b0
keywords:
- glReadPixels (función) OpenGL
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
ms.openlocfilehash: a853d67be282227168da4b90f4fdd47a49d2d212
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104421940"
---
# <a name="glreadpixels-function"></a>glReadPixels función)

La función **glReadPixels** Lee un bloque de píxeles de fotogramas.

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

La coordenada *x* de la ventana del primer píxel que se lee desde fotogramas. Junto con la coordenada *y* , especifica la ubicación de la esquina inferior izquierda de un bloque rectangular de píxeles.

</dd> <dt>

*y* 
</dt> <dd>

Coordenadas *y* de la ventana del primer píxel que se lee desde fotogramas. Junto con la coordenada *x* , especifica la ubicación de la esquina inferior izquierda de un bloque rectangular de píxeles.

</dd> <dt>

*width* 
</dt> <dd>

Ancho del rectángulo de píxeles.

</dd> <dt>

*height* 
</dt> <dd>

Alto del rectángulo de píxeles. Los parámetros de *ancho* y *alto* del valor "1" se corresponden con un solo píxel.

</dd> <dt>

*format* 
</dt> <dd>

Formato de los datos de píxeles. Se aceptan los siguientes valores simbólicos:



| Value                                                                                                                                                                                                                                                                                                                                                                                                                                                                           | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_INDEX"></span><span id="gl_color_index"></span><dl> <dt>**\_Índice de color de GL \_**</dt> </dl>                                                                                                                                                                                                                                                                                                               | Los índices de color se leen en el búfer de color seleccionado por [**glReadBuffer**](glreadbuffer.md). Cada índice se convierte en punto fijo, desplazado a la izquierda o a la derecha, según el valor y el signo del cambio de índice de contabilidad \_ \_ y se agrega al desplazamiento de índice de GL \_ \_ . Si \_ \_ el color del mapa de contabilidad es \_ true, los índices se reemplazan por sus asignaciones en el mapa de píxeles de contabilidad de la tabla \_ \_ \_ i \_ \_ .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="GL_STENCIL_INDEX"></span><span id="gl_stencil_index"></span><dl> <dt>**\_Índice de galería de símbolos GL \_**</dt> </dl>                                                                                                                                                                                                                                                                                                         | Los valores de estarcido se leen desde el búfer de estarcido. Cada índice se convierte en punto fijo, desplazado a la izquierda o a la derecha, según el valor y el signo del cambio de índice de contabilidad \_ \_ y se agrega al desplazamiento de índice de GL \_ \_ . Si \_ \_ la galería de símbolos GL \_ del mapa es true, los índices se sustituyen por sus asignaciones en la tabla GL píxel de la tabla \_ \_ \_ \_ a \_ s.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="GL_DEPTH_COMPONENT"></span><span id="gl_depth_component"></span><dl> <dt>**\_componente de profundidad de contab. \_**</dt> </dl>                                                                                                                                                                                                                                                                                                   | Los valores de profundidad se leen desde el búfer de profundidad. Cada componente se convierte en punto flotante, de modo que el valor de profundidad mínimo se asigna a 0,0 y el valor máximo se asigna a 1,0. A continuación, cada componente se multiplica por escala de profundidad de contabilidad \_ \_ , se agrega a \_ la diferencia de profundidad de contabilidad \_ y finalmente se fija en el intervalo de \[ 0 a 1 \] .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="GL_RED__GL_GREEN__GL_BLUE__GL_ALPHA__GL_RGB__GL_RGBA__GL_BGR_EXT__GL_BGRA_EXT__GL_LUMINANCE__GL_LUMINANCE_ALPHA"></span><span id="gl_red__gl_green__gl_blue__gl_alpha__gl_rgb__gl_rgba__gl_bgr_ext__gl_bgra_ext__gl_luminance__gl_luminance_alpha"></span><dl> <dt>**GL \_ rojo, GL \_ verde, GL \_ Blue, GL \_ alfa, GL \_ RGB, GL \_ RGBA, GL \_ BGR \_ ext, GL \_ BGRA \_ ext, GL \_ luminancia, GL \_ luminancia \_ Alpha**</dt> </dl> | El procesamiento difiere en función de si los búferes de color almacenan índices de color o componentes de color RGBA. Si los índices de color están almacenados, se leen del búfer de color seleccionado por [**glReadBuffer**](glreadbuffer.md). Cada índice se convierte en punto fijo, desplazado a la izquierda o a la derecha, según el valor y el signo del cambio de índice de contabilidad \_ \_ y se agrega al desplazamiento de índice de GL \_ \_ . A continuación, los índices se reemplazan por los valores rojo, verde, azul y alfa obtenidos mediante la indexación de la asignación de píxeles de GL i a R, el mapa de \_ \_ píxeles de \_ \_ \_ GL i a \_ \_ \_ \_ \_ G, el mapa de \_ píxeles de GL \_ \_ i \_ a \_ B y \_ la asignación de píxeles de GL \_ \_ i \_ a \_ las tablas. Si los componentes de color RGBA se almacenan en los búferes de color, se leen del búfer de color seleccionado por **glReadBuffer**. Cada componente de color se convierte en punto flotante, de modo que la intensidad cero se asigna a 0,0 y la intensidad completa se asigna a 1,0. Después, cada componente se multiplica por la escala de contabilidad \_ c \_ y se agrega a la diferencia de GL \_ c \_ , donde c es GL \_ rojo, GL \_ verde, GL \_ Blue y GL \_ alfa. Cada componente se fija en el intervalo \[ 0, 1 \] . Por último, si \_ \_ el color del mapa \_ de contabilidad es true, cada componente de color c se sustituye por su asignación en la tabla contabilidad de píxeles de contabilidad \_ \_ \_ c \_ a \_ c, donde c vuelve a ser de color \_ rojo, GL \_ verde, libro \_ azul y libro de contabilidad \_ . Cada componente se escala al tamaño de su tabla correspondiente antes de que se realice la búsqueda. Por último, se descartan los datos innecesarios. Por ejemplo, \_ el rojo de contabilidad descarta los componentes verde, azul y alfa, mientras \_ que el libro de contabilidad RGB descarta solo el componente alfa. Luminancia de libro de contabilidad \_ : calcula un valor de componente único como la suma de los componentes rojo, verde y azul, y \_ el alfa de luminancia de GL \_ hace lo mismo, a la vez que mantiene el alfa como un segundo valor.<br/> |



 

</dd> <dt>

*type* 
</dt> <dd>

El tipo de datos de los datos de píxeles. Debe ser uno de los valores siguientes.



| Tipo                | Máscara de índice | Conversión de componentes |
|---------------------|------------|----------------------|
| \_byte sin signo de \_ GL  | 281        | (281) *c*             |
| BYTE de GL \_            | 271        | \[(271) *c*-1 \] /2     |
| mapa de bits de GL \_          | 1          | 1                    |
| libro de contabilidad \_ corto sin signo \_ | 2 61       | (2 61) *c*            |
| CONTABILIDAD \_ breve           | 2 51       | \[(2 51) *c* 1 \] /2     |
| libro de contabilidad \_ sin signo \_\_ | 2 1       | (2 1) *c*            |
| GL \_ int             | 2 1      | \[(2 1) *c* 1 \] /2     |
| valor \_ float de GL           | ninguno       | *c*                  |



 

</dd> <dt>

*píxeles* 
</dt> <dd>

Devuelve los datos de píxeles.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>      | el *formato* o *tipo* no era un valor aceptado.<br/>                                                                              |
| <dl> <dt>**\_valor no válido de GL \_**</dt> </dl>     | El *ancho* o el *alto* era negativo.<br/>                                                                                   |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | el *formato* era \_ el índice de color GL \_ y los búferes de color almacenaron los componentes de color RGBA o BGRA.<br/>                                 |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | el *formato* es el \_ Índice de estarcido GL y no \_ hay ningún búfer de estarcido.<br/>                                                          |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | el *formato* del componente de profundidad del libro de contabilidad es \_ y no \_ hay ningún búfer de profundidad.<br/>                                                          |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |

## <a name="remarks"></a>Observaciones

La función **glReadPixels** devuelve los datos de píxeles desde fotogramas, empezando por el píxel cuya esquina inferior izquierda está en la ubicación (*x*, *y*), en la memoria de cliente a partir de los *píxeles* de la ubicación. Varios parámetros controlan el procesamiento de los datos de píxeles antes de colocarlos en la memoria del cliente. Estos parámetros se establecen con tres comandos: [**glPixelStore**](glpixelstore-functions.md), [**glPixelTransfer**](glpixeltransfer.md)y [**glPixelMap**](glpixelmap.md). En este tema se describen los efectos de la mayoría de los **glReadPixels** , pero no todos los parámetros especificados por estos tres comandos.

La función **glReadPixels** devuelve valores de cada píxel con la esquina inferior izquierda en (*x* + i, *y* + j) para 0 = i < *ancho* y 0 = j < *alto*. Este píxel se dice que es el píxel *i* de la fila *j*. Los píxeles se devuelven en el orden de las filas de la fila más baja a la más alta, de izquierda a derecha en cada fila.

Los factores de desplazamiento, escala, diferencia y búsqueda descritos anteriormente se especifican en [**glPixelTransfer**](glpixeltransfer.md). El contenido de la tabla de búsqueda se especifica mediante [**glPixelMap**](glpixelmap.md).

El último paso consiste en convertir los índices o componentes en el formato adecuado, según se especifica en *tipo*. Si el *formato* es el índice de \_ color GL \_ o \_ \_ el índice de estarcido GL y el *tipo* no es Float de GL \_ , cada índice se enmascara con el valor de máscara que se indica en la tabla siguiente. Si *Type* es de tipo flotante de contabilidad \_ , cada índice de entero se convierte en un formato de punto flotante de precisión sencilla.

Si el *formato* es GL \_ rojo, GL \_ verde, GL \_ Blue, GL \_ Alpha, GL \_ RGB, GL \_ RGBA, GL \_ BGR \_ ext, GL BGRA ext, GL GL \_ \_ \_ o luminancia de GL \_ \_ alfa y *tipo* no es Float de GL \_ , cada componente se multiplica por el multiplicador que se muestra en la tabla anterior. Si Type es Float de GL \_ , cada componente se pasa tal cual (o se convierte en el formato de punto flotante de precisión sencilla del cliente si es diferente del utilizado por OpenGL).

Los valores devueltos se colocan en la memoria como se indica a continuación. Si el *formato* es \_ el \_ Índice de color de contabilidad, el \_ Índice de la galería de símbolos GL \_ , el componente de profundidad de contabilidad general, \_ \_ GL \_ rojo, GL \_ verde, GL \_ azul, GL \_ alfa o \_ luminancia de contabilidad, se devuelve un solo valor y los datos del píxel *i* de la fila *j* se colocan en la ubicación (*j* )*width*  +  *i*. GL \_ RGB y GL \_ BGR \_ ext devuelven tres valores, GL \_ RGBA y GL \_ BGRA \_ ext devuelven cuatro valores y \_ \_ la luminancia de GL alfa devuelve dos valores para cada píxel, donde todos los valores correspondientes a un píxel único ocupan espacio contiguo en *píxeles*. Los parámetros de almacenamiento establecidos por [**glPixelStore**](glpixelstore-functions.md), como los \_ bytes de intercambio de los paquetes de contabilidad y el \_ paquete de \_ GL \_ \_ LSB \_ en primer lugar, afectan a la manera en que los datos se escriben en la memoria. Consulte [**glPixelStore**](glpixelstore-functions.md) para obtener una descripción.

Los valores de los píxeles que se encuentran fuera de la ventana conectada al contexto de OpenGL actual no están definidos.

Si se genera un error, no se realiza ningún cambio en el contenido de los *píxeles*.

La siguiente función recupera información relacionada con **glReadPixels**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento del \_ modo de índice de GL \_

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

 

 





