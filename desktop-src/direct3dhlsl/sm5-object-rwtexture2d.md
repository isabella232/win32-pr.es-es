---
title: RWTexture2D
description: Un recurso de lectura y escritura. | RWTexture2D
ms.assetid: 19b383f1-c787-4c20-b77a-60ef9f212b9f
keywords:
- RWTexture2D HLSL
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473226"
---
# <a name="rwtexture2d"></a>RWTexture2D

Un recurso de lectura y escritura.



| Método                                                        | Descripción                   |
|---------------------------------------------------------------|-------------------------------|
| [**GetDimensions**](sm5-object-rwtexture2d-getdimensions.md) | Obtiene las dimensiones de recursos. |
| [**Carga**](rwtexture2d-load.md)                              | Lee los datos de textura.           |
| [**Operator\[\]**](sm5-object-rwtexture2d-operatorindex.md)  | Obtiene una variable de recurso.     |



 

Puede anteceder a los objetos RWTexture2D con la clase de almacenamiento **globalmentecoherente**. Esta clase de almacenamiento hace que las barreras de memoria y las sincronizaciones vaciarán los datos en toda la GPU para que otros grupos puedan ver escrituras. Sin este especificador, una barrera o sincronización de memoria vaciará solo una vista de acceso no ordenado (UAV) dentro del grupo actual.

Un objeto RWTexture2D requiere un tipo de elemento en una instrucción de declaración para el objeto. Por ejemplo, la declaración siguiente no es correcta:


```
// The following declaration is incorrectly coded.
RWTexture2D myTexture;
```



La declaración siguiente es correcta:


```
// The following declaration is correctly coded.
RWTexture2D<float> tex;
```



Dado que un objeto RWTexture2D es un objeto de tipo UAV, sus propiedades difieren de un objeto de tipo vista de recursos de sombreador (SRV), como un objeto [Texture2D.](sm5-object-texture2d.md) Por ejemplo, puede leer y escribir en un objeto RWTexture2D, pero solo puede leer desde un objeto Texture2D.

Un objeto RWTexture2D no puede usar métodos de un [objeto Texture2D,](sm5-object-texture2d.md) como [Sample](dx-graphics-hlsl-to-sample.md). Sin embargo, dado que puede crear varios tipos de vista en el mismo recurso, puede declarar varios tipos de textura como una sola textura en varios sombreadores. Por ejemplo, los fragmentos de código siguientes muestran cómo puede declarar y usar un objeto RWTexture2D como *texas* en un sombreador de proceso y, a continuación, declarar y usar un objeto Texture2D como *texas* en un sombreador de píxeles.

> [!Note]  
> El tiempo de ejecución aplica determinados patrones de uso al crear varios tipos de vista en el mismo recurso. Por ejemplo, el runtime no permite tener una asignación de UAV para un recurso y una asignación de SRV para el mismo recurso activo al mismo tiempo.

 

El código siguiente es para el sombreador de proceso:


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



El código siguiente es para el sombreador de píxeles:


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

 

 




