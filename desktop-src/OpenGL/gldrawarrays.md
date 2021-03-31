---
title: función glDrawArrays (GL. h)
description: La función glDrawArrays especifica varios primitivos que se van a representar.
ms.assetid: 6ebd467b-5a63-43e4-b3fd-242c704d7d13
keywords:
- glDrawArrays (función) OpenGL
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996524"
---
# <a name="gldrawarrays-function"></a>glDrawArrays función)

La función **glDrawArrays** especifica varios primitivos que se van a representar.

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

Tipo de primitivas que se van a representar. Las constantes siguientes especifican tipos aceptables de primitivas: \_ puntos de GL, \_ franja de líneas de libro de contabilidad \_ , bucle de línea de libro de contabilidad, \_ \_ \_ líneas de contabilidad general, franja de \_ triángulo de contabilidad \_ , ventilador de triángulo de contabilidad general, \_ triángulos de contabilidad, \_ \_ \_ franja cuádruple de GL, \_ cuádruples de contabilidad \_ y polígono de contabilidad \_ .

</dd> <dt>

*first* 
</dt> <dd>

Índice inicial de las matrices habilitadas.

</dd> <dt>

*count* 
</dt> <dd>

Número de índices que se van a representar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_valor no válido de GL \_**</dt> </dl>     | el *recuento* es negativo.<br/>                                                                                                      |
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>      | el *modo* no era un valor aceptado.<br/>                                                                                          |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

Con **glDrawArrays**, puede especificar varias primitivas geométricas que se van a representar. En lugar de llamar a funciones OpenGL independientes para pasar cada vértice, normal o color individual, puede especificar matrices independientes de vértices, normales y colores para definir una secuencia de primitivas (todo el mismo tipo) con una única llamada a **glDrawArrays**.

Cuando se llama a **glDrawArrays**, el *recuento* de elementos secuenciales de cada matriz habilitada se usa para construir una secuencia de primitivas geométricas, empezando por el *primer* elemento. El parámetro *mode* especifica qué tipo de primitivo se debe construir y cómo usar los elementos de la matriz para construir los primitivos.

Una vez que **glDrawArrays** devuelve, los valores de los atributos de vértice modificados por **glDrawArrays** son indefinidos. Por ejemplo, si \_ \_ la matriz de colores de GL está habilitada, el valor del color actual no está definido después de que **glDrawArrays** devuelva. Los atributos no modificados por **glDrawArrays** permanecen definidos. Cuando \_ \_ no se habilita la matriz de vértices de contabilidad, no se generan primitivas geométricas, pero los atributos correspondientes a las matrices habilitadas se modifican.

Puede incluir **glDrawArrays** en las listas de visualización. Cuando se incluye **glDrawArrays** en una lista de visualización, los datos de la matriz necesarios, determinados por los punteros de matriz y habilitados, se generan y se escriben en la lista de visualización. Los valores de punteros de matriz y habilitados se determinan durante la creación de listas de presentación.

Puede leer datos de matriz estática en cualquier momento. Si se modifican los elementos de una matriz estática y no se especifica de nuevo la matriz, los resultados de las llamadas subsiguientes a **glDrawArrays** no se definen.

Aunque no se genera ningún error cuando se especifica una matriz más de una vez dentro de pares [**glBegin**](glbegin.md) y [**glend**](glend.md) , los resultados son indefinidos.

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

 

 





