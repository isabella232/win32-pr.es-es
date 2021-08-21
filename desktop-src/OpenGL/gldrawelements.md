---
title: Función glDrawElements (Gl.h)
description: La función glDrawElements representa primitivas a partir de datos de matriz.
ms.assetid: fb433294-106e-48d5-ad49-4434934fe072
keywords:
- Función glDrawElements OpenGL
topic_type:
- apiref
api_name:
- glDrawElements
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b260c1112f7ec588b4d83655e5d0aa465b63682164f2ca745b63d3f421e5794c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118616577"
---
# <a name="gldrawelements-function"></a>Función glDrawElements

La **función glDrawElements** representa primitivas a partir de datos de matriz.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glDrawElements(
         GLenum  mode,
         GLsizei count,
         GLenum  type,
   const GLvoid  *indices
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*mode* 
</dt> <dd>

Tipo de primitivas que se representará. Puede asumir uno de los siguientes valores \_ simbólicos: GL POINTS, GL \_ LINE \_ STRIP, GL LINE \_ \_ LOOP, GL \_ LINES, GL TRIANGLE \_ \_ STRIP, GL TRIANGLE \_ \_ FAN, GL TRIANGLE \_ FAN, GL TRIANGLES, \_ GL QUAD \_ STRIP, GL \_ QUADS y GL \_ POLYGON.

</dd> <dt>

*count* 
</dt> <dd>

Número de elementos que se representarán.

</dd> <dt>

*type* 
</dt> <dd>

Tipo de los valores de los índices. Debe ser uno de GL \_ UNSIGNED \_ BYTE, GL \_ UNSIGNED \_ SHORT o GL \_ UNSIGNED \_ INT.

</dd> <dt>

*índices* 
</dt> <dd>

Puntero a la ubicación donde se almacenan los índices.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERACIÓN \_ NO \_ VÁLIDA DE GL**</dt> </dl>      | *mode* no era un valor aceptado.<br/>                                                                                          |
| <dl> <dt>**VALOR \_ NO VÁLIDO DE \_ GL**</dt> </dl>     | *count* era un valor negativo.<br/>                                                                                              |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La **función glDrawElements** permite especificar varias primitivas geométricas con muy pocas llamadas de función. En lugar de llamar a una función OpenGL para pasar cada vértice individual, normal o color, puede especificar matrices independientes de vértices, normales y colores con antelación y usarlas para definir una secuencia de primitivas (todas del mismo tipo) con una sola llamada a **glDrawElements**.

Cuando se llama a la función  **glDrawElements,** se usan elementos secuenciales de recuento de *índices* para construir una secuencia de primitivas geométricas. El *parámetro mode* especifica qué tipo de primitivas se construyen y cómo se usan los elementos de la matriz para construir estos primitivos. Si GL \_ VERTEX ARRAY no está \_ habilitado, no se genera ninguna primitiva geométrica.

Los atributos de vértice modificados por **glDrawElements** tienen un valor no especificado después de que se devuelva **glDrawElements.** Por ejemplo, si GL COLOR ARRAY está habilitado, el valor del color actual no está \_ definido después de ejecutar \_ **glDrawElements.** Los atributos que no se modifican permanecen sin cambios.

Puede incluir la función **glDrawElements** en las listas de presentación. Cuando **glDrawElements** se incluye en una lista de visualización, los datos de matriz necesarios (determinados por los punteros de matriz y las habilitaciones) también se introducen en la lista de visualización. Dado que los punteros de matriz y las habilitaciones son variables de estado del lado cliente, sus valores afectan a las listas de presentación cuando se crean las listas, no cuando se ejecutan las listas.

> [!Note]  
> La **función glDrawElements** solo está disponible en OpenGL versión 1.1 o posterior.

 

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

[**glArrayElement**](glarrayelement.md)
</dt> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glColorPointer**](glcolorpointer.md)
</dt> <dt>

[**glDrawArrays**](gldrawarrays.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGetPointerv**](glgetpointerv.md)
</dt> <dt>

[**glIndexPointer**](glindexpointer.md)
</dt> <dt>

[**glNormalPointer**](glnormalpointer.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> <dt>

[**glVertexPointer**](glvertexpointer.md)
</dt> </dl>

 

 





