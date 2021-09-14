---
title: tex2Dlod
description: Muestrea una textura 2D con mapas mip. El LOD de mipmap se especifica en t.w.
ms.assetid: 689eff39-f6ac-4c25-8b92-ca68707ae8ad
keywords:
- tex2Dlod HLSL
topic_type:
- apiref
api_name:
- tex2Dlod
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f63a922fe86dc10d984369a1a872f84089b4db34
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072727"
---
# <a name="tex2dlod"></a>tex2Dlod

Muestrea una textura 2D con mapas mip. El LOD de mipmap se especifica en t.w.



| ret tex2Dlod(s, t) |
|--------------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                   | Descripción                               |
|--------------------------------------------------------|-------------------------------------------|
| <span id="s"></span><span id="S"></span>*s*<br/> | \[en \] el estado sampler.<br/>      |
| <span id="t"></span><span id="T"></span>*T*<br/> | \[en \] la coordenada de textura.<br/> |



 

## <a name="return-value"></a>Valor devuelto

Valor de los datos de textura.

## <a name="type-description"></a>Descripción del tipo



| Nombre | Entrada o salida | [**Tipo de plantilla**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Size |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| s    | in     | [**Objeto**](dx-graphics-hlsl-intrinsic-functions.md) | [sampler2D](dx-graphics-hlsl-sampler.md)                      | 1    |
| t    | in     | [**Vector**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 4    |
| Ret  | out    | [**Vector**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 4    |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                       | Compatible |
|------------------------------------------------------------------------------------|-----------|
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) y modelos de sombreador superiores | sí       |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md)                          | No        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | No        |



 

## <a name="remarks"></a>Observaciones

A partir de Direct3D 10, puede usar la nueva sintaxis HLSL para acceder a texturas y otros recursos. Puede reemplazar las funciones de búsqueda de textura de estilo intrínseco, como **tex2Dlod,** por un estilo más orientado a objetos. En este estilo orientado a objetos, las texturas se desacoplan de los muestreadores y tienen métodos para cargar y muestrear.

Para muestrear una textura 2D, en lugar de usar **texas2Dlod** como en este código:


```
sampler S;
...
color = tex2Dlod(S, Location);
```



Use el [método SampleLevel](dx-graphics-hlsl-to-samplelevel.md) de un [**objeto Texture como**](dx-graphics-hlsl-to-type.md) en este código:


```
Texture2D MyTexture;
SamplerState MySampler;
...
color = MyTexture.SampleLevel(MySampler, Location, LOD);
```



Para usar las funciones de búsqueda de textura de estilo intrínseco, como **texas2Dlod,** con el modelo de sombreador [4](dx-graphics-hlsl-sm4.md) y versiones posteriores, use [**D3DCOMPILE \_ ENABLE \_ BACKWARDS \_ COMPATIBILITY**](d3dcompile-constants.md) para compilar. Sin embargo, si desea tener como destino el modelo de sombreador 4 y versiones posteriores (incluso [ \* \_ \_ 4 0 \_ nivel \_ 9) \_ \* ](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro)con código de estilo orientado a objetos más reciente, migre a la sintaxis HLSL más reciente.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Funciones intrínsecas (HLSL de DirectX)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

