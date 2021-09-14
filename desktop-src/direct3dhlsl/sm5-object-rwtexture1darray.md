---
title: RWTexture1DArray
description: Un recurso de lectura y escritura. | RWTexture1DArray
ms.assetid: 214c7e7d-4e74-4f4f-bf78-98e9df0b3a0e
keywords:
- RWTexture1DArray HLSL
topic_type:
- apiref
api_name:
- RWTexture1DArray
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2e7f6841cb1f15b12c9755da2a9fae50e42ed333
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126888193"
---
# <a name="rwtexture1darray"></a>RWTexture1DArray

Un recurso de lectura y escritura.



| Método                                                             | Descripción                   |
|--------------------------------------------------------------------|-------------------------------|
| [**GetDimensions**](sm5-object-rwtexture1darray-getdimensions.md) | Obtiene las dimensiones de recursos. |
| [**Carga**](rwtexture1darray-load.md)                              | Lee los datos de textura.           |
| [**Operator\[\]**](sm5-object-rwtexture1darray-operatorindex.md)  | Obtiene una variable de recurso.     |



 

Puede anteceder **los objetos RWTexture1DArray** con la clase de almacenamiento **globalcoherent**. Esta clase de almacenamiento hace que las barreras de memoria y las sincronizaciones vaciarán los datos en toda la GPU para que otros grupos puedan ver las escrituras. Sin este especificador, una barrera de memoria o sincronización vaciará un UAV solo dentro del grupo actual.

Un **objeto RWTexture1DArray** requiere un tipo de elemento en una instrucción de declaración para el objeto. Por ejemplo, la siguiente declaración es correcta:


```
RWTexture1DArray<float> tex;
```



Dado que un objeto **RWTexture1DArray** es un objeto de tipo UAV, sus propiedades difieren de un objeto de tipo vista de recursos de sombreador (SRV), como un objeto [**Texture1DArray.**](sm5-object-texture1darray.md) Por ejemplo, puede leer y escribir en un objeto **RWTexture1DArray,** pero solo puede leer desde un objeto **Texture1DArray.**

Un **objeto RWTexture1DArray** no puede usar métodos de un objeto [**Texture1DArray,**](sm5-object-texture1darray.md) como [Sample](dx-graphics-hlsl-to-sample.md). Sin embargo, dado que puede crear varios tipos de vista en el mismo recurso, puede declarar varios tipos de textura como una sola textura en varios sombreadores. Por ejemplo, puede declarar y usar un objeto **RWTexture1DArray** como *texas* en un sombreador de proceso y, a continuación, declarar y usar un objeto **Texture1DArray** como *un objeto como objeto en* un sombreador de píxeles.

> [!Note]  
> El tiempo de ejecución aplica determinados patrones de uso al crear varios tipos de vista en el mismo recurso. Por ejemplo, el tiempo de ejecución no permite tener una asignación de UAV para un recurso y una asignación de SRV para el mismo recurso activo al mismo tiempo.

 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Este objeto se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                | Compatible |
|-----------------------------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md) y modelos de sombreador posteriores | sí       |



 

Este objeto es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Objetos del modelo de sombreador 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




