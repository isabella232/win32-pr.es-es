---
title: RWTexture2DArray
description: Un recurso de lectura y escritura. | RWTexture2DArray
ms.assetid: 6a6f3655-f1c0-4d5b-91a2-d79da65858b8
keywords:
- RWTexture2DArray HLSL
topic_type:
- apiref
api_name:
- RWTexture2DArray
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5ada0fcaba729eff37f41f1ae7666841175689ff
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070348"
---
# <a name="rwtexture2darray"></a>RWTexture2DArray

Un recurso de lectura y escritura.



| Método                                                             | Descripción                   |
|--------------------------------------------------------------------|-------------------------------|
| [**GetDimensions**](sm5-object-rwtexture2darray-getdimensions.md) | Obtiene las dimensiones de recursos. |
| [**Carga**](rwtexture2darray-load.md)                              | Lee los datos de textura.           |
| [**Operator\[\]**](sm5-object-rwtexture2darray-operatorindex.md)  | Obtiene una variable de recurso.     |



 

Puede **prefijer los objetos RWTexture2DArray** con la clase de almacenamiento **globalmentecoherente**. Esta clase de almacenamiento hace que las barreras de memoria y las sincronizaciones vaciarán los datos en toda la GPU para que otros grupos puedan ver escrituras. Sin este especificador, una barrera o sincronización de memoria vaciará un UAV solo dentro del grupo actual.

Un **objeto RWTexture2DArray** requiere un tipo de elemento en una instrucción de declaración para el objeto. Por ejemplo, la declaración siguiente es correcta:


```
RWTexture2DArray<float> tex;
```



Dado que un objeto **RWTexture2DArray** es un objeto de tipo UAV, sus propiedades difieren de un objeto de tipo vista de recursos de sombreador (SRV), como un objeto [**Texture2DArray.**](sm5-object-texture2darray.md) Por ejemplo, puede leer y escribir en un objeto **RWTexture2DArray,** pero solo puede leer desde un objeto **Texture2DArray.**

Un **objeto RWTexture2DArray** no puede usar métodos de un [**objeto Texture2DArray,**](sm5-object-texture2darray.md) como [Sample](dx-graphics-hlsl-to-sample.md). Sin embargo, dado que puede crear varios tipos de vista en el mismo recurso, puede declarar varios tipos de textura como una sola textura en varios sombreadores. Por ejemplo, puede declarar y usar un objeto **RWTexture2DArray** como *texas* en un sombreador de proceso y, a continuación, declarar y usar un objeto **Texture2DArray** como *texas* en un sombreador de píxeles.

> [!Note]  
> El tiempo de ejecución aplica determinados patrones de uso al crear varios tipos de vista en el mismo recurso. Por ejemplo, el runtime no permite tener una asignación de UAV para un recurso y una asignación de SRV para el mismo recurso activo al mismo tiempo.

 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Este objeto se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                | Compatible |
|-----------------------------------------------------------------------------|-----------|
| [Modelos de sombreador 5](d3d11-graphics-reference-sm5.md) y superiores | sí       |



 

Este objeto es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos del modelo de sombreador 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




