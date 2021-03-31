---
title: función glSelectBuffer (GL. h)
description: La función glSelectBuffer establece un búfer para los valores del modo de selección.
ms.assetid: b5c64364-1f47-4281-96b5-95c3f5c8e753
keywords:
- glSelectBuffer (función) OpenGL
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
ms.openlocfilehash: efa5b97abad6575de77a760c72e3eb05e90461c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801178"
---
# <a name="glselectbuffer-function"></a>glSelectBuffer función)

La función **glSelectBuffer** establece un búfer para los valores del modo de selección.

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

*búfer* 
</dt> <dd>

Devuelve los datos de la selección.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_valor no válido de GL \_**</dt> </dl>     | *el tamaño* era negativo.<br/>                                                                                                       |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función mientras que el modo de representación era GL \_ Select.<br/>                                                              |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La función **glSelectBuffer** tiene dos parámetros: *buffer* es un puntero a una matriz de enteros sin signo y *size* indica el tamaño de la matriz. El parámetro *buffer* devuelve valores de la pila de nombres (consulte [**glInitNames**](glinitnames.md), [**glLoadName**](glloadname.md), [**glPushName**](glpushname.md)) cuando el modo de representación es GL \_ Select (vea [**glRenderMode**](glrendermode.md)). Se debe emitir la función **glSelectBuffer** antes de que esté habilitado el modo de selección, y no debe emitirse mientras el modo de representación sea Select de contabilidad \_ .

Un programador utiliza la selección para determinar qué primitivas se dibujan en alguna región de una ventana. La región se define mediante las matrices MODELVIEW y Perspective actuales.

En el modo de selección, no se generan fragmentos de píxeles desde la rasterización. En su lugar, si una primitiva forma una intersección con el volumen de clip definido por el frustum de visualización y los planos de recorte definidos por el usuario, este primitivo provocará un acierto de la selección. (Con polígonos, no se produce ninguna interrupción si se selecciona el polígono). Cuando se realiza un cambio en la pila de nombres, o cuando se llama a [**glRenderMode**](glrendermode.md) , se copia un registro de aciertos en el *búfer* si se ha producido algún acierto desde el último evento de este tipo (un cambio en la pila de nombres o una llamada a **glRenderMode** ). El registro de aciertos consta del número de nombres en la pila de nombres en el momento del evento; seguido de los valores de profundidad máximo y mínimo de todos los vértices que se alcanzaron desde el evento anterior; seguido del nombre de la pila de nombres, el nombre de la parte inferior en primer lugar.

Los valores devueltos de profundidad se asignan de modo que el valor entero sin signo más grande se corresponde con la profundidad de coordenadas de la ventana 1,0 y cero corresponde a profundidad de coordenadas de la ventana 0,0.

Un índice interno en el *búfer* se restablece en cero siempre que se especifica el modo de selección. Cada vez que se copia un registro de aciertos en el *búfer*, el índice se incrementa para apuntar a la celda que se encuentra justo después del final del bloque de namesthat, a la siguiente celda disponible. Si el registro de aciertos es mayor que el número de ubicaciones restantes en el *búfer*, se copian tantos datos como quepan y se establece la marca de desbordamiento. Si la pila de nombres está vacía cuando se copia un registro de aciertos, dicho registro consta de cero seguido de los valores de profundidad mínimo y máximo.

El modo de selección se termina llamando a **glRenderMode** con un argumento distinto de GL \_ Select. Siempre que se llama a **glRenderMode** mientras el modo de representación es GL \_ Select, devuelve el número de registros de aciertos copiados en el *búfer*, restablece la marca de desbordamiento y el puntero del búfer de selección e inicializa la pila de nombres para que esté vacía. Si se estableció el bit de desbordamiento cuando se llamó a **glRenderMode** , se devuelve un número de registros de aciertos negativos.

El contenido del *búfer* no está definido hasta que se llame a [**glRenderMode**](glrendermode.md) con un argumento distinto de \_ la selección de contabilidad.

Las primitivas de **glBegin** / **glEnd** y las llamadas a [**glRasterPos**](glrasterpos-functions.md) pueden dar lugar a aciertos.

La siguiente función recupera información relacionada con **glSelectBuffer**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento de profundidad de la pila de nombre del libro \_ \_ \_

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

 

 





