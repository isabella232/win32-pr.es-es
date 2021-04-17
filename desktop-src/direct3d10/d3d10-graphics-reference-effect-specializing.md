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
# <a name="specializing-interfaces-direct3d-10"></a><span data-ttu-id="53a4c-103">Interfaces especializadas (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="53a4c-103">Specializing Interfaces (Direct3D 10)</span></span>

<span data-ttu-id="53a4c-104">La [**interfaz ID3D10EffectVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable) tiene una serie de métodos para convertir la interfaz en el tipo de interfaz concreto que necesita.</span><span class="sxs-lookup"><span data-stu-id="53a4c-104">[**ID3D10EffectVariable Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable) has a number of methods for casting the interface into the particular type of interface you need.</span></span> <span data-ttu-id="53a4c-105">Los métodos tienen el formato de *tipo* e incluyen un método para cada tipo de variable de efecto (como asblend, AsConstantBuffer, etc.).</span><span class="sxs-lookup"><span data-stu-id="53a4c-105">The methods are of the form As *Type* and include a method for each type of effect variable (such as AsBlend, AsConstantBuffer etc..)</span></span>

<span data-ttu-id="53a4c-106">Por ejemplo, supongamos que tiene un efecto con dos variables globales: el tiempo y una transformación universal.</span><span class="sxs-lookup"><span data-stu-id="53a4c-106">For example, suppose you have an effect with two global variables: time and a world transform.</span></span>


```
float    g_fTime;
float4x4 g_mWorld;
```



<span data-ttu-id="53a4c-107">Este es un ejemplo (de [ejemplo SimpleSample10](https://msdn.microsoft.com/library/Ee416428(v=VS.85).aspx)) que obtiene estas variables:</span><span class="sxs-lookup"><span data-stu-id="53a4c-107">Here is an example (from [SimpleSample10 Sample](https://msdn.microsoft.com/library/Ee416428(v=VS.85).aspx)) that gets these variables:</span></span>


```
ID3D10EffectVariable* g_pVariable;
ID3D10EffectMatrixVariable* g_pmWorld;
ID3D10EffectScalarVariable* g_pfTime;

g_pVariable = g_pEffect10->GetVariableByName("g_mWorld");
g_pmWorld = g_pVariable->AsMatrix();
g_pfTime = g_pEffect10->GetVariableByName("g_fTime");
g_pfTime = g_pVariable->AsScalar();
```



<span data-ttu-id="53a4c-108">Al especializar las interfaces, podría reducir el código a una sola llamada.</span><span class="sxs-lookup"><span data-stu-id="53a4c-108">By specializing the interfaces, you could reduce the code to a single call.</span></span>


```
g_pmWorld = (g_pEffect10->GetVariableByName("g_mWorld"))->AsMatrix();
g_pfTime = (g_pEffect10->GetVariableByName("g_fTime"))->AsScalar();
```



<span data-ttu-id="53a4c-109">Las interfaces que heredan de la [**interfaz ID3D10EffectVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable) también tienen estos métodos, pero se han diseñado para devolver objetos no válidos. solo las llamadas de la **interfaz ID3D10EffectVariable** devuelven objetos válidos.</span><span class="sxs-lookup"><span data-stu-id="53a4c-109">Interfaces that inherit from [**ID3D10EffectVariable Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable) also have these methods, but they have been designed to return invalid objects; only calls from **ID3D10EffectVariable Interface** return valid objects.</span></span> <span data-ttu-id="53a4c-110">Las aplicaciones pueden probar el objeto devuelto para ver si es válido llamando a [**ID3D10EffectVariable:: IsValid**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effectvariable-isvalid).</span><span class="sxs-lookup"><span data-stu-id="53a4c-110">Applications can test the returned object to see if it is valid by calling [**ID3D10EffectVariable::IsValid**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effectvariable-isvalid).</span></span>

## <a name="related-topics"></a><span data-ttu-id="53a4c-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="53a4c-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53a4c-112">Efectos</span><span class="sxs-lookup"><span data-stu-id="53a4c-112">Effects</span></span>](d3d10-graphics-programming-guide-effects.md)
</dt> </dl>

 

 



