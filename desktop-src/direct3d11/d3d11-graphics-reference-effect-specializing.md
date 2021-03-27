---
title: Interfaces especializadas (Direct3D 11)
description: ID3DX11EffectVariable tiene una serie de métodos para convertir la interfaz en el tipo de interfaz concreto que necesita.
ms.assetid: 20892af0-7d4a-4a89-b8d7-4ef225400697
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cb9f8adb5a5bb184473ff5679df99f0b71557fa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777605"
---
# <a name="specializing-interfaces-direct3d-11"></a>Interfaces especializadas (Direct3D 11)

[**ID3DX11EffectVariable**](id3dx11effectvariable.md) tiene una serie de métodos para convertir la interfaz en el tipo de interfaz concreto que necesita. Los métodos tienen el formato *astype* e incluyen un método para cada tipo de variable de efecto (como asblend, AsConstantBuffer, etc.).

Por ejemplo, supongamos que tiene un efecto con dos variables globales: el tiempo y una transformación universal.


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



Al especializar las interfaces, podría reducir el código a una sola llamada.


```
g_pmWorld = (g_pEffect11->GetVariableByName("g_mWorld"))->AsMatrix();
g_pfTime = (g_pEffect11->GetVariableByName("g_fTime"))->AsScalar();
```



Las interfaces que heredan de [**ID3DX11EffectVariable**](id3dx11effectvariable.md) también tienen estos métodos, pero se han diseñado para devolver objetos no válidos. solo las llamadas de **ID3DX11EffectVariable** devuelven objetos válidos. Las aplicaciones pueden probar el objeto devuelto para ver si es válido llamando a [**ID3DX11EffectVariable:: IsValid**](id3dx11effectvariable-isvalid.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Efectos (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 




