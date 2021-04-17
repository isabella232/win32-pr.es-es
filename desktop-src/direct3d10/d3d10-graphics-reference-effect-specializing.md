---
description: La interfaz ID3D10EffectVariable tiene una serie de métodos para convertir la interfaz en el tipo de interfaz concreto que necesita.
ms.assetid: c0842a1d-b78c-44b2-89c7-452d54efe403
title: Interfaces especializadas (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0ce8bc29ae16ada650da7283beb1dd858948cae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652337"
---
# <a name="specializing-interfaces-direct3d-10"></a>Interfaces especializadas (Direct3D 10)

La [**interfaz ID3D10EffectVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable) tiene una serie de métodos para convertir la interfaz en el tipo de interfaz concreto que necesita. Los métodos tienen el formato de *tipo* e incluyen un método para cada tipo de variable de efecto (como asblend, AsConstantBuffer, etc.).

Por ejemplo, supongamos que tiene un efecto con dos variables globales: el tiempo y una transformación universal.


```
float    g_fTime;
float4x4 g_mWorld;
```



Este es un ejemplo (de [ejemplo SimpleSample10](https://msdn.microsoft.com/library/Ee416428(v=VS.85).aspx)) que obtiene estas variables:


```
ID3D10EffectVariable* g_pVariable;
ID3D10EffectMatrixVariable* g_pmWorld;
ID3D10EffectScalarVariable* g_pfTime;

g_pVariable = g_pEffect10->GetVariableByName("g_mWorld");
g_pmWorld = g_pVariable->AsMatrix();
g_pfTime = g_pEffect10->GetVariableByName("g_fTime");
g_pfTime = g_pVariable->AsScalar();
```



Al especializar las interfaces, podría reducir el código a una sola llamada.


```
g_pmWorld = (g_pEffect10->GetVariableByName("g_mWorld"))->AsMatrix();
g_pfTime = (g_pEffect10->GetVariableByName("g_fTime"))->AsScalar();
```



Las interfaces que heredan de la [**interfaz ID3D10EffectVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable) también tienen estos métodos, pero se han diseñado para devolver objetos no válidos. solo las llamadas de la **interfaz ID3D10EffectVariable** devuelven objetos válidos. Las aplicaciones pueden probar el objeto devuelto para ver si es válido llamando a [**ID3D10EffectVariable:: IsValid**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effectvariable-isvalid).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Efectos](d3d10-graphics-programming-guide-effects.md)
</dt> </dl>

 

 



