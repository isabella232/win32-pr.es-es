---
title: RWTexture3D
description: Un recurso de lectura/escritura. | RWTexture3D
ms.assetid: 4d02810e-4f3c-4b20-b057-0ff27d6732b5
keywords:
- HLSL de RWTexture3D
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
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362133"
---
# <a name="rwtexture3d"></a>RWTexture3D

Un recurso de lectura/escritura.



| Método                                                        | Descripción                   |
|---------------------------------------------------------------|-------------------------------|
| [**GetDimensions**](sm5-object-rwtexture3d-getdimensions.md) | Obtiene las dimensiones de recursos. |
| [**Carga**](rwtexture3d-load.md)                              | Lee los datos de textura.           |
| [**Operador\[\]**](sm5-object-rwtexture3d-operatorindex.md)  | Obtiene una variable de recurso.     |



 

Puede prefijar objetos **RWTexture3D** con la clase de almacenamiento **globallycoherent**. Esta clase de almacenamiento provoca barreras de memoria y sincronizaciones para vaciar los datos en toda la GPU, de modo que otros grupos puedan ver escrituras. Sin este especificador, una barrera de memoria o una sincronización vaciará un UAV solo dentro del grupo actual.

Un objeto **RWTexture3D** requiere un tipo de elemento en una instrucción de declaración para el objeto. Por ejemplo, la siguiente declaración es correcta:


```
RWTexture3D<float> tex;
```



Dado que un objeto **RWTexture3D** es un objeto de tipo UAV, sus propiedades difieren de un objeto de tipo de vista de recursos de sombreador (SRV), como un objeto [**Texture3D**](sm5-object-texture3d.md) . Por ejemplo, puede leer y escribir en un objeto **RWTexture3D** , pero solo puede leer desde un objeto **Texture3D** .

Un objeto **RWTexture3D** no puede utilizar métodos de un objeto [**Texture3D**](sm5-object-texture3d.md) , como [ejemplo](dx-graphics-hlsl-to-sample.md). Sin embargo, como puede crear varios tipos de vistas en el mismo recurso, puede declarar varios tipos de textura como una sola textura en varios sombreadores. Por ejemplo, puede declarar y usar un objeto **RWTexture3D** como *Tex* en un sombreador de cálculo y, a continuación, declarar y usar un objeto **Texture3D** como *Tex* en un sombreador de píxeles.

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

 

 




