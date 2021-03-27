---
title: RWTexture1DArray
description: Un recurso de lectura/escritura. | RWTexture1DArray
ms.assetid: 214c7e7d-4e74-4f4f-bf78-98e9df0b3a0e
keywords:
- HLSL de RWTexture1DArray
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
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104003633"
---
# <a name="rwtexture1darray"></a>RWTexture1DArray

Un recurso de lectura/escritura.



| Método                                                             | Descripción                   |
|--------------------------------------------------------------------|-------------------------------|
| [**GetDimensions**](sm5-object-rwtexture1darray-getdimensions.md) | Obtiene las dimensiones de recursos. |
| [**Carga**](rwtexture1darray-load.md)                              | Lee los datos de textura.           |
| [**Operador\[\]**](sm5-object-rwtexture1darray-operatorindex.md)  | Obtiene una variable de recurso.     |



 

Puede prefijar objetos **RWTexture1DArray** con la clase de almacenamiento **globallycoherent**. Esta clase de almacenamiento provoca barreras de memoria y sincronizaciones para vaciar los datos en toda la GPU, de modo que otros grupos puedan ver escrituras. Sin este especificador, una barrera de memoria o una sincronización vaciará un UAV solo dentro del grupo actual.

Un objeto **RWTexture1DArray** requiere un tipo de elemento en una instrucción de declaración para el objeto. Por ejemplo, la siguiente declaración es correcta:


```
RWTexture1DArray<float> tex;
```



Dado que un objeto **RWTexture1DArray** es un objeto de tipo UAV, sus propiedades difieren de un objeto de tipo de vista de recursos de sombreador (SRV), como un objeto [**Texture1DArray**](sm5-object-texture1darray.md) . Por ejemplo, puede leer y escribir en un objeto **RWTexture1DArray** , pero solo puede leer desde un objeto **Texture1DArray** .

Un objeto **RWTexture1DArray** no puede utilizar métodos de un objeto [**Texture1DArray**](sm5-object-texture1darray.md) , como [ejemplo](dx-graphics-hlsl-to-sample.md). Sin embargo, como puede crear varios tipos de vistas en el mismo recurso, puede declarar varios tipos de textura como una sola textura en varios sombreadores. Por ejemplo, puede declarar y usar un objeto **RWTexture1DArray** como *Tex* en un sombreador de cálculo y, a continuación, declarar y usar un objeto **Texture1DArray** como *Tex* en un sombreador de píxeles.

> [!Note]  
> El tiempo de ejecución exige determinados patrones de uso al crear varios tipos de vistas en el mismo recurso. Por ejemplo, el tiempo de ejecución no permite tener una asignación UAV para un recurso y una asignación SRV para el mismo recurso activo al mismo tiempo.

 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Este objeto es compatible con los siguientes modelos de sombreador.



| Modelo de sombreador                                                                | Compatible |
|-----------------------------------------------------------------------------|-----------|
| Modelos de sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y versiones posteriores | sí       |



 

Este objeto es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos del modelo de sombreador 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




