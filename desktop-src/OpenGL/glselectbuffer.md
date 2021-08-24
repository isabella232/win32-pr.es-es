---
title: Función glSelectBuffer (Gl.h)
description: La función glSelectBuffer establece un búfer para los valores de modo de selección.
ms.assetid: b5c64364-1f47-4281-96b5-95c3f5c8e753
keywords:
- Función glSelectBuffer OpenGL
topic_type:
- apiref
api_name:
- glSelectBuffer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17c40030c34ece43f4e24ac6937c35400fed7ab7acc005e99c653b233e08b69e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519825"
---
# <a name="glselectbuffer-function"></a>Función glSelectBuffer

La **función glSelectBuffer** establece un búfer para los valores de modo de selección.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glSelectBuffer(
   GLsizei size,
   GLuint  *buffer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*size* 
</dt> <dd>

Tamaño del *búfer*.

</dd> <dt>

*Búfer* 
</dt> <dd>

Devuelve los datos de selección.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**VALOR \_ NO VÁLIDO DE \_ GL**</dt> </dl>     | *el tamaño* era negativo.<br/>                                                                                                       |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función mientras el modo de representación era GL \_ SELECT.<br/>                                                              |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentarios

La **función glSelectBuffer** tiene dos parámetros: *buffer* es un puntero a una matriz de enteros sin signo y *size* indica el tamaño de la matriz. El *parámetro buffer* devuelve valores de la pila de nombres (vea [**glInitNames**](glinitnames.md), [**glLoadName**](glloadname.md), [**glPushName**](glpushname.md)) cuando el modo de representación es GL \_ SELECT (vea [**glRenderMode).**](glrendermode.md) La **función glSelectBuffer** debe emitirse antes de habilitar el modo de selección y no debe emitirse mientras el modo de representación sea GL \_ SELECT.

Un programador usa la selección para determinar qué primitivas se dibujan en alguna región de una ventana. La región se define mediante las matrices modelview y perspective actuales.

En el modo de selección, no se generan fragmentos de píxeles a partir de la rasterización. En su lugar, si una primitiva forma una intersección con el volumen de recorte definido por el frustum de visualización y los planos de recorte definidos por el usuario, esta primitiva produce una selección. (En el caso de los polígonos, no se produce ningún impacto si el polígono está en la línea). Cuando se realiza un cambio en la pila de nombres o cuando se  llama a [**glRenderMode,**](glrendermode.md) se copia un registro de aciertos en el búfer si se ha producido algún acierto desde el último evento de este tipo (un cambio de pila de nombres o una llamada **glRenderMode).** El registro de llamadas consta del número de nombres de la pila de nombres en el momento del evento; seguido de los valores de profundidad mínimo y máximo de todos los vértices que se han alcanzado desde el evento anterior; seguido del contenido de la pila de nombres, nombre inferior en primer lugar.

Los valores de profundidad devueltos se asignan de forma que el mayor valor entero sin signo corresponde a la profundidad de coordenadas de ventana 1,0 y cero corresponde a la profundidad de coordenadas de ventana 0,0.

Un índice interno en *el búfer* se restablece a cero cada vez que se entra en modo de selección. Cada vez que se copia un registro de acceso en el *búfer*, el índice se incrementa para apuntar a la celda justo después del final del bloque de nombres, es decir, a la siguiente celda disponible. Si el registro de acceso es mayor que el número de ubicaciones restantes en el búfer *,* se copian todos los datos que caben y se establece la marca de desbordamiento. Si la pila de nombres está vacía cuando se copia un registro de llamadas, ese registro consta de cero seguido de los valores de profundidad mínimo y máximo.

El modo de selección se cierra mediante una llamada **a glRenderMode** con un argumento distinto de GL \_ SELECT. Cada vez que se llama a **glRenderMode** mientras el modo de representación es GL SELECT, devuelve el número de registros de llamadas copiados en el búfer, restablece la marca de desbordamiento y el puntero del búfer de selección e inicializa la pila de nombres para que esté \_ vacía. Si se estableció el bit de desbordamiento cuando se llamó a **glRenderMode,** se devuelve un recuento de registros de llamadas negativo.

El contenido del *búfer* no está definido hasta que [**se llama a glRenderMode**](glrendermode.md) con un argumento distinto de GL \_ SELECT.

Las **primitivas glBegin** / **glEnd** y las llamadas [**a glRasterPos**](glrasterpos-functions.md) pueden producir aciertos.

La función siguiente recupera información relacionada con **glSelectBuffer**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ NAME STACK \_ \_ DEPTH

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

[**glFeedbackBuffer**](glfeedbackbuffer.md)
</dt> <dt>

[**glInitNames**](glinitnames.md)
</dt> <dt>

[**glLoadName**](glloadname.md)
</dt> <dt>

[**glPushName**](glpushname.md)
</dt> <dt>

[**glRenderMode**](glrendermode.md)
</dt> </dl>

 

 





