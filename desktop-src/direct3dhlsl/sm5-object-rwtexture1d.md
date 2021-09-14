---
title: RWTexture1D
description: Un recurso de lectura y escritura. | RWTexture1D
ms.assetid: 47866e5a-b26b-4264-9291-c8940882d662
keywords:
- RWTexture1D HLSL
topic_type:
- apiref
api_name:
- RWTexture1D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 695b73cc14541505ee1b2d4391aac2d145eec8d7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974669"
---
# <a name="rwtexture1d"></a>RWTexture1D

Un recurso de lectura y escritura.



| Método                                                        | Descripción                   |
|---------------------------------------------------------------|-------------------------------|
| [**GetDimensions**](sm5-object-rwtexture1d-getdimensions.md) | Obtiene las dimensiones de recursos. |
| [**Carga**](rwtexture1d-load.md)                              | Lee los datos de textura.           |
| [**Operador\[\]**](sm5-object-rwtexture1d-operatorindex.md)  | Obtiene una variable de recurso.     |



 

Puede anteceder **a los objetos RWTexture1D** con la clase de almacenamiento **globalmentecoherente**. Esta clase de almacenamiento hace que las barreras de memoria y las sincronizaciones vaciarán los datos en toda la GPU para que otros grupos puedan ver escrituras. Sin este especificador, una barrera o sincronización de memoria vaciará un UAV solo dentro del grupo actual.

Un **objeto RWTexture1D** requiere un tipo de elemento en una instrucción de declaración para el objeto. Por ejemplo, la declaración siguiente es correcta:


```
RWTexture1D<float> tex;
```



Dado que un objeto **RWTexture1D** es un objeto de tipo UAV, sus propiedades difieren de un objeto de tipo vista de recursos de sombreador (SRV), como un objeto [**Texture1D.**](sm5-object-texture1d.md) Por ejemplo, puede leer y escribir en un objeto **RWTexture1D,** pero solo puede leer desde un **objeto Texture1D.**

Un **objeto RWTexture1D** no puede usar métodos de un objeto [**Texture1D,**](sm5-object-texture1d.md) como [Sample](dx-graphics-hlsl-to-sample.md). Sin embargo, dado que puede crear varios tipos de vista en el mismo recurso, puede declarar varios tipos de textura como una sola textura en varios sombreadores. Por ejemplo, puede declarar y usar un objeto **RWTexture1D** como *texas* en un sombreador de proceso y, a continuación, declarar y usar un objeto **Texture1D** como *texas* en un sombreador de píxeles.

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



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Objetos del modelo de sombreador 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




