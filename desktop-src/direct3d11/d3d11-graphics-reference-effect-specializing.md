---
title: Especialización de interfaces (Direct3D 11)
description: ID3DX11EffectVariable tiene una serie de métodos para convertir la interfaz en el tipo concreto de interfaz que necesita.
ms.assetid: 20892af0-7d4a-4a89-b8d7-4ef225400697
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6e4cff9c74f7a4b4034578b7ddeec2c388f0f953534393ac27778c31ed3856c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119126079"
---
# <a name="specializing-interfaces-direct3d-11"></a>Especialización de interfaces (Direct3D 11)

[**ID3DX11EffectVariable tiene**](id3dx11effectvariable.md) una serie de métodos para convertir la interfaz en el tipo concreto de interfaz que necesita. Los métodos tienen la forma *AsType e* incluyen un método para cada tipo de variable de efecto (como AsBlend, AsConstantBuffer, etc.).

Por ejemplo, suponga que tiene un efecto con dos variables globales: tiempo y una transformación del mundo.


```
float    g_fTime;
float4x4 g_mWorld;
```



Este es un ejemplo que obtiene estas variables:


```
ID3DX11EffectVariable* g_pVariable;
ID3DX11EffectMatrixVariable* g_pmWorld;
ID3DX11EffectScalarVariable* g_pfTime;

g_pVariable = g_pEffect11->GetVariableByName("g_mWorld");
g_pmWorld = g_pVariable->AsMatrix();
g_pVariable = g_pEffect11->GetVariableByName("g_fTime");
g_pfTime = g_pVariable->AsScalar();
```



Al especializar las interfaces, puede reducir el código a una sola llamada.


```
g_pmWorld = (g_pEffect11->GetVariableByName("g_mWorld"))->AsMatrix();
g_pfTime = (g_pEffect11->GetVariableByName("g_fTime"))->AsScalar();
```



Las interfaces que heredan de [**ID3DX11EffectVariable**](id3dx11effectvariable.md) también tienen estos métodos, pero se han diseñado para devolver objetos no válidos; Solo las llamadas desde **ID3DX11EffectVariable** devuelven objetos válidos. Las aplicaciones pueden probar el objeto devuelto para ver si es válido llamando a [**ID3DX11EffectVariable::IsValid**](id3dx11effectvariable-isvalid.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Efectos (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 




