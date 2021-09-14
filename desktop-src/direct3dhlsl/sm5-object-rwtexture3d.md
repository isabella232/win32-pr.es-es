---
title: RWTexture3D
description: Un recurso de lectura y escritura. | RWTexture3D
ms.assetid: 4d02810e-4f3c-4b20-b057-0ff27d6732b5
keywords:
- RWTexture3D HLSL
topic_type:
- apiref
api_name:
- RWTexture3D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9b89ed7ff724eabef9fc2b2757c6ac0e5272c69e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126963544"
---
# <a name="rwtexture3d"></a>RWTexture3D

Un recurso de lectura y escritura.



| Método                                                        | Descripción                   |
|---------------------------------------------------------------|-------------------------------|
| [**GetDimensions**](sm5-object-rwtexture3d-getdimensions.md) | Obtiene las dimensiones de recursos. |
| [**Carga**](rwtexture3d-load.md)                              | Lee los datos de textura.           |
| [**Operador\[\]**](sm5-object-rwtexture3d-operatorindex.md)  | Obtiene una variable de recurso.     |



 

Puede anteceder **a los objetos RWTexture3D** con la clase de almacenamiento **globalmentecoherente**. Esta clase de almacenamiento hace que las barreras de memoria y las sincronizaciones vaciarán los datos en toda la GPU para que otros grupos puedan ver escrituras. Sin este especificador, una barrera o sincronización de memoria vaciará un UAV solo dentro del grupo actual.

Un **objeto RWTexture3D** requiere un tipo de elemento en una instrucción de declaración para el objeto. Por ejemplo, la declaración siguiente es correcta:


```
RWTexture3D<float> tex;
```



Dado que un objeto **RWTexture3D** es un objeto de tipo UAV, sus propiedades difieren de un objeto de tipo vista de recursos de sombreador (SRV), como un objeto [**Texture3D.**](sm5-object-texture3d.md) Por ejemplo, puede leer y escribir en un objeto **RWTexture3D,** pero solo puede leer desde un **objeto Texture3D.**

Un **objeto RWTexture3D** no puede usar métodos de un objeto [**Texture3D,**](sm5-object-texture3d.md) como [Sample](dx-graphics-hlsl-to-sample.md). Sin embargo, dado que puede crear varios tipos de vista en el mismo recurso, puede declarar varios tipos de textura como una sola textura en varios sombreadores. Por ejemplo, puede declarar y usar un objeto **RWTexture3D** como *texas* en un sombreador de proceso y, a continuación, declarar y usar un objeto **Texture3D** como *texas* en un sombreador de píxeles.

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

 

 




