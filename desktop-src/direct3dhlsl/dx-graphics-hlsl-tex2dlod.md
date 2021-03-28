---
title: tex2Dlod
description: Muestrea una textura 2D con mapas MIP. El LOD de mipmap se especifica en t.w.
ms.assetid: 689eff39-f6ac-4c25-8b92-ca68707ae8ad
keywords:
- HLSL de tex2Dlod
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
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104983983"
---
# <a name="tex2dlod"></a>tex2Dlod

Muestrea una textura 2D con mapas MIP. El LOD de mipmap se especifica en t.w.



| RET tex2Dlod (s, t) |
|--------------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                   | Descripción                               |
|--------------------------------------------------------|-------------------------------------------|
| <span id="s"></span><span id="S"></span>*seg*<br/> | \[en \] el estado de la muestra.<br/>      |
| <span id="t"></span><span id="T"></span>*h*<br/> | \[en \] la coordenada de textura.<br/> |



 

## <a name="return-value"></a>Valor devuelto

Valor de los datos de textura.

## <a name="type-description"></a>Descripción del tipo



| Nombre | Entrada o salida | [**Tipo de plantilla**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Tamaño |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| s    | in     | [**object**](dx-graphics-hlsl-intrinsic-functions.md) | [sampler2D](dx-graphics-hlsl-sampler.md)                      | 1    |
| t    | in     | [**medios**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 4    |
| direcc  | out    | [**medios**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 4    |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                       | Compatible |
|------------------------------------------------------------------------------------|-----------|
| Modelador [modelo 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) y modelos de sombreador más altos | sí       |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md)                          | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | no        |



 

## <a name="remarks"></a>Observaciones

A partir de Direct3D 10, puede usar la nueva sintaxis de HLSL para tener acceso a las texturas y otros recursos. Puede reemplazar las funciones de búsqueda de textura de estilo intrínseco, como **tex2Dlod**, con un estilo más orientado a objetos. En este estilo orientado a objetos, las texturas se desacoplan de los muestreadores y tienen métodos para cargar y realizar el muestreo.

Para muestrear una textura 2D, en lugar de usar **tex2Dlod** como en este código:


```
sampler S;
...
color = tex2Dlod(S, Location);
```



Use el método [SampleLevel](dx-graphics-hlsl-to-samplelevel.md) de un [**objeto Texture**](dx-graphics-hlsl-to-type.md) como en este código:


```
Texture2D MyTexture;
SamplerState MySampler;
...
color = MyTexture.SampleLevel(MySampler, Location, LOD);
```



Para usar las funciones de búsqueda de textura de estilo intrínseco, como **tex2Dlod**, con el [modelo de sombreador 4](dx-graphics-hlsl-sm4.md) y versiones posteriores, use [**D3DCOMPILE habilitar la \_ \_ \_ compatibilidad con versiones anteriores**](d3dcompile-constants.md) para compilar. Sin embargo, si desea tener como destino el modelo de sombreador 4 y superior (incluso [ \* \_ 4 \_ 0 de \_ nivel \_ 9 \_ \* ](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro)) con código de estilo orientado a objetos más reciente, migre a la sintaxis de HLSL más reciente.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funciones intrínsecas (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

