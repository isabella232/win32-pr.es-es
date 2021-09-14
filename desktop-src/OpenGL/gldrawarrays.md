---
title: Función glDrawArrays (Gl.h)
description: La función glDrawArrays especifica varias primitivas que se representan.
ms.assetid: 6ebd467b-5a63-43e4-b3fd-242c704d7d13
keywords:
- Función glDrawArrays OpenGL
topic_type:
- apiref
api_name:
- glDrawArrays
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88b20cf3a3e3b2c96a8172f53f8126815efe16d6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362068"
---
# <a name="gldrawarrays-function"></a>Función glDrawArrays

La **función glDrawArrays** especifica varias primitivas que se representan.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glDrawArrays(
   GLenum  mode,
   GLint   first,
   GLsizei count
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*mode* 
</dt> <dd>

Tipo de primitivas que se representará. Las constantes siguientes especifican tipos aceptables de primitivas: GL \_ POINTS, GL \_ LINE \_ STRIP, GL \_ LINE \_ LOOP, GL \_ LINES, GL TRIANGLE \_ \_ STRIP, GL TRIANGLE \_ \_ FAN, GL TRIANGLE \_ FAN, GL \_ TRIANGLES, GL QUAD \_ STRIP, GL \_ QUADS y GL \_ POLYGON.

</dd> <dt>

*first* 
</dt> <dd>

Índice inicial de las matrices habilitadas.

</dd> <dt>

*count* 
</dt> <dd>

Número de índices que se representará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**VALOR \_ NO VÁLIDO DE \_ GL**</dt> </dl>     | *count* era negativo.<br/>                                                                                                      |
| <dl> <dt>**ENUMERACIÓN \_ NO \_ VÁLIDA DE GL**</dt> </dl>      | *mode* no era un valor aceptado.<br/>                                                                                          |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

Con **glDrawArrays,** puede especificar varias primitivas geométricas para representar. En lugar de llamar a funciones OpenGL independientes para pasar cada vértice individual, normal o color, puede especificar matrices independientes de vértices, normales y colores para definir una secuencia de primitivas (todas del mismo tipo) con una sola llamada a **glDrawArrays**.

Cuando se llama a **glDrawArrays** *,* se usan los elementos secuenciales de recuento de cada matriz habilitada para construir una secuencia de primitivas geométricas, empezando por *el primer* elemento. El *parámetro mode* especifica qué tipo de primitivo construir y cómo usar los elementos de matriz para construir las primitivas.

Después **de que glDrawArrays** vuelva, los valores de los atributos de vértice modificados por **glDrawArrays** no están definidos. Por ejemplo, si GL COLOR ARRAY está habilitado, el valor del color actual no está definido después de que se devuelva \_ \_ **glDrawArrays.** Los atributos no **modificados por glDrawArrays** permanecen definidos. Cuando GL VERTEX ARRAY no está habilitado, no se generan primitivas geométricas, pero se modifican los atributos correspondientes a \_ \_ las matrices habilitadas.

Puede incluir **glDrawArrays en** listas para mostrar. Cuando se incluye **glDrawArrays** en una lista de visualización, los datos de matriz necesarios, determinados por los punteros de matriz y las habilitaciones, se generan y se introducen en la lista de visualización. Los valores de los punteros de matriz y las habilitaciones se determinan durante la creación de listas para mostrar.

Puede leer los datos de la matriz estática en cualquier momento. Si se modifican elementos de matriz estáticos y no se vuelve a especificar la matriz, los resultados de las llamadas posteriores **a glDrawArrays** no están definidos.

Aunque no se genera ningún error al especificar una matriz más de una vez dentro de los pares [**glBegin y glBegin,**](glbegin.md) los resultados no están definidos. [](glend.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**glArrayElement**](glarrayelement.md)
</dt> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glColorPointer**](glcolorpointer.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGetPointerv**](glgetpointerv.md)
</dt> <dt>

[**glGetString**](glgetstring.md)
</dt> <dt>

[**glIndexPointer**](glindexpointer.md)
</dt> <dt>

[**glNormalPointer**](glnormalpointer.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> <dt>

[**glVertexPointer**](glvertexpointer.md)
</dt> </dl>

 

 





