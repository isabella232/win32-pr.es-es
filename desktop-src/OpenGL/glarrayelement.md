---
title: función glArrayElement (GL. h)
description: La función glArrayElement especifica los elementos de la matriz que se usan para representar un vértice.
ms.assetid: 2c4d76bb-e4c9-4baa-a190-66298b8a4335
keywords:
- glArrayElement (función) OpenGL
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
ms.openlocfilehash: 6a20aff9fcaa5bf922bc9447f7b7022a8cd1a9c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686008"
---
# <a name="glarrayelement-function"></a>glArrayElement función)

La función **glArrayElement** especifica los elementos de la matriz que se usan para representar un vértice.

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

Use la función **glArrayElement** dentro de pares [**glBegin**](glbegin.md) y [**glEnd**](glend.md) para especificar datos de vértices y atributos para los primitivos de punto, línea y polígono. La función **glArrayElement** especifica los datos para un solo vértice con datos de vértice y de atributo ubicados en el *Índice* de las matrices de vértices habilitadas.

Puede usar **glArrayElement** para construir primitivos mediante la indexación de datos de vértices, en lugar de hacerlo mediante el streaming de matrices de datos en orden de primero a último. Dado que **glArrayElement** especifica solo un solo vértice, puede especificar explícitamente atributos para primitivos individuales. Por ejemplo, puede establecer un solo normal para cada triángulo individual.

Al incluir llamadas a **glArrayElement** en las listas de visualización, los datos de la matriz necesarios, determinados por los punteros de matriz y los valores de habilitación, también se especifican en la lista de visualización. Los valores de puntero de matriz y habilitar se determinan cuando se crean listas de visualización, no cuando se ejecutan listas de presentación.

Puede leer y almacenar en caché los datos estáticos de la matriz en cualquier momento con **glArrayElement**. Cuando se modifican los elementos de una matriz estática sin especificar la matriz de nuevo, los resultados de las llamadas subsiguientes a **glArrayElement** son indefinidos.

Cuando se llama a **glArrayElement** sin llamar primero a **glEnableClientState**( \_ \_ matriz de vértices de GL), no se produce ningún dibujo, pero se modifican los atributos correspondientes a las matrices habilitadas. Aunque no se genera ningún error al especificar una matriz dentro de los pares **glBegin** y **glEnd** , los resultados son indefinidos.

> [!Note]  
> La función **glArrayElement** solo está disponible en la versión 1,1 o posterior de OpenGL.

 

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

 

 





