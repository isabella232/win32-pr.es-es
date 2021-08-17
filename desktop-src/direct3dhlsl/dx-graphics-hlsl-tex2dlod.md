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
ms.openlocfilehash: f9581418eb2a3d8736fcd0e125eaafec11494e6b6d5471cef33f9592475d5ec0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117725683"
---
# <a name="tex2dlod"></a>tex2Dlod

Muestrea una textura 2D con mapas mip. El LOD de mipmap se especifica en t.w.



| ret tex2Dlod(s, t) |
|--------------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                   | Descripción                               |
|--------------------------------------------------------|-------------------------------------------|
| <span id="s"></span><span id="S"></span>*s*<br/> | \[en \] el estado del muestreador.<br/>      |
| <span id="t"></span><span id="T"></span>*T*<br/> | \[en \] la coordenada de textura.<br/> |



 

## <a name="return-value"></a>Valor devuelto

Valor de los datos de textura.

## <a name="type-description"></a>Descripción del tipo



| Nombre | Entrada o salida | [**Tipo de plantilla**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Size |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| s    | in     | [**object**](dx-graphics-hlsl-intrinsic-functions.md) | [sampler2D](dx-graphics-hlsl-sampler.md)                      | 1    |
| t    | in     | [**Vector**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 4    |
| Ret  | out    | [**Vector**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 4    |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                       | Compatible |
|------------------------------------------------------------------------------------|-----------|
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) y modelos de sombreador superiores | Sí       |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md)                          | No        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | No        |



 

## <a name="remarks"></a>Comentarios

A partir de Direct3D 10, puede usar la nueva sintaxis HLSL para acceder a texturas y otros recursos. Puede reemplazar las funciones de búsqueda de textura de estilo intrínseco, como **tex2Dlod,** por un estilo más orientado a objetos. En este estilo orientado a objetos, las texturas se desacoplan de los muestreadores y tienen métodos para cargar y muestreo.

Para muestrear una textura 2D, en lugar de **usar tex2Dlod** como en este código:


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



Para usar las funciones de búsqueda de textura de estilo intrínseco, como **tex2Dlod**, con el modelo de sombreador [4](dx-graphics-hlsl-sm4.md) y versiones posteriores, use [**D3DCOMPILE \_ ENABLE \_ BACKWARDS \_ COMPATIBILITY**](d3dcompile-constants.md) para compilar. Sin embargo, si quiere tener como destino el modelo de sombreador 4 y versiones posteriores (incluso [ \* \_ \_ 4 0 \_ nivel \_ 9) \_ \* ](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro)con código de estilo orientado a objetos más reciente, migre a la sintaxis HLSL más reciente.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funciones intrínsecas (HLSL de DirectX)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

