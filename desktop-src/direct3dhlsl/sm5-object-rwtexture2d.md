---
title: RWTexture2D
description: Un recurso de lectura/escritura. | RWTexture2D
ms.assetid: 19b383f1-c787-4c20-b77a-60ef9f212b9f
keywords:
- HLSL de RWTexture2D
topic_type:
- apiref
api_name:
- RWTexture2D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ccdeae4dd47d3ad4bf5d756c2ca362033eae6814
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362193"
---
# <a name="rwtexture2d"></a>RWTexture2D

Un recurso de lectura/escritura.



| Método                                                        | Descripción                   |
|---------------------------------------------------------------|-------------------------------|
| [**GetDimensions**](sm5-object-rwtexture2d-getdimensions.md) | Obtiene las dimensiones de recursos. |
| [**Carga**](rwtexture2d-load.md)                              | Lee los datos de textura.           |
| [**Operador\[\]**](sm5-object-rwtexture2d-operatorindex.md)  | Obtiene una variable de recurso.     |



 

Puede prefijar objetos RWTexture2D con la clase de almacenamiento **globallycoherent**. Esta clase de almacenamiento provoca barreras de memoria y sincronizaciones para vaciar los datos en toda la GPU, de modo que otros grupos puedan ver escrituras. Sin este especificador, una barrera de memoria o una sincronización solo vaciará una vista de acceso desordenado (UAV) en el grupo actual.

Un objeto RWTexture2D requiere un tipo de elemento en una instrucción de declaración para el objeto. Por ejemplo, la siguiente declaración no es correcta:


```
// The following declaration is incorrectly coded.
RWTexture2D myTexture;
```



La siguiente declaración es correcta:


```
// The following declaration is correctly coded.
RWTexture2D<float> tex;
```



Dado que un objeto RWTexture2D es un objeto de tipo UAV, sus propiedades difieren de un objeto de tipo de vista de recursos de sombreador (SRV), como un objeto [Texture2D](sm5-object-texture2d.md) . Por ejemplo, puede leer y escribir en un objeto RWTexture2D, pero solo puede leer desde un objeto Texture2D.

Un objeto RWTexture2D no puede utilizar métodos de un objeto [Texture2D](sm5-object-texture2d.md) , como [ejemplo](dx-graphics-hlsl-to-sample.md). Sin embargo, como puede crear varios tipos de vistas en el mismo recurso, puede declarar varios tipos de textura como una sola textura en varios sombreadores. Por ejemplo, los fragmentos de código siguientes muestran cómo se puede declarar y usar un objeto RWTexture2D como *Tex* en un sombreador de cálculo y, a continuación, declarar y usar un objeto Texture2D como *Tex* en un sombreador de píxeles.

> [!Note]  
> El tiempo de ejecución exige determinados patrones de uso al crear varios tipos de vistas en el mismo recurso. Por ejemplo, el tiempo de ejecución no permite tener una asignación UAV para un recurso y una asignación SRV para el mismo recurso activo al mismo tiempo.

 

El código siguiente es para el sombreador de cálculo:


```
RWTexture2D<float> tex;
[numthreads(groupDim_x, groupDim_y, 1)]
void main(
    uint3 groupId : SV_GroupID,
    uint3 groupThreadId : SV_GroupThreadID,
    uint3 dispatchThreadId : SV_DispatchThreadID,
    uint groupIndex : SV_GroupIndex)
{
    tex [dispatchThreadId.xy] = <something>;
}
```



El siguiente código es para el sombreador de píxeles:


```
struct PixelShaderInput
{
    float4 pos : SV_POSITION;
    float2 tex : TEXTURE;
};

Texture2D<float> tex;
float4 main(PixelShaderInput input) : SV_TARGET
{
    return tex.Sample(TextureSampler, input.tex);
}
```



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

 

 




