---
title: Función glArrayElement (Gl.h)
description: La función glArrayElement especifica los elementos de matriz utilizados para representar un vértice.
ms.assetid: 2c4d76bb-e4c9-4baa-a190-66298b8a4335
keywords:
- Función glArrayElement OpenGL
topic_type:
- apiref
api_name:
- glArrayElement
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb6fdf3b90c5145c46730e530f26ba7d4f7f3875e51cc4d510e9763d03e27207
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118618065"
---
# <a name="glarrayelement-function"></a>Función glArrayElement

La **función glArrayElement** especifica los elementos de matriz utilizados para representar un vértice.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glArrayElement(
   GLint index
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*índice* 
</dt> <dd>

Índice de las matrices habilitadas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Use la **función glArrayElement dentro** de los pares [**glBegin**](glbegin.md) y [**glEnd**](glend.md) para especificar datos de vértices y atributos para primitivas de punto, línea y polígono. La **función glArrayElement** especifica los datos de un solo vértice mediante los datos de vértice y atributo ubicados en el *índice* de las matrices de vértices habilitadas.

Puede usar **glArrayElement para** construir primitivas mediante la indexación de datos de vértices, en lugar de transmitir por secuencias a través de matrices de datos en orden de primero a último. Dado **que glArrayElement** especifica un solo vértice, puede especificar explícitamente atributos para primitivas individuales. Por ejemplo, puede establecer un único valor normal para cada triángulo individual.

Cuando se incluyen llamadas **a glArrayElement** en listas para mostrar, los datos de matriz necesarios, determinados por los punteros de matriz y los valores de habilitación, también se introducen en la lista de visualización. Los valores de puntero de matriz y habilitación se determinan cuando se crean listas de visualización, no cuando se ejecutan listas de visualización.

Puede leer y almacenar en caché datos de matriz estática en cualquier momento **con glArrayElement**. Al modificar los elementos de una matriz estática sin volver a especificar la matriz, los resultados de las llamadas posteriores a **glArrayElement** no están definidos.

Cuando se llama **a glArrayElement** sin llamar primero **a glEnableClientState**(GL VERTEX ARRAY), no se produce ningún dibujo, pero se modifican los atributos correspondientes a las \_ \_ matrices habilitadas. Aunque no se genera ningún error al especificar una matriz dentro de los pares **glBegin** y **glEnd,** los resultados no están definidos.

> [!Note]  
> La **función glArrayElement** solo está disponible en OpenGL versión 1.1 o posterior.

 

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

[**glColorPointer**](glcolorpointer.md)
</dt> <dt>

[**glDrawArrays**](gldrawarrays.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glEnableClientState**](glenableclientstate.md)
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

 

 





