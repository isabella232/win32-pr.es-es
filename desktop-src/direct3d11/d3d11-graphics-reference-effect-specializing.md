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
# <a name="specializing-interfaces-direct3d-11"></a><span data-ttu-id="259df-103">Interfaces especializadas (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="259df-103">Specializing Interfaces (Direct3D 11)</span></span>

<span data-ttu-id="259df-104">[**ID3DX11EffectVariable**](id3dx11effectvariable.md) tiene una serie de métodos para convertir la interfaz en el tipo de interfaz concreto que necesita.</span><span class="sxs-lookup"><span data-stu-id="259df-104">[**ID3DX11EffectVariable**](id3dx11effectvariable.md) has a number of methods for casting the interface into the particular type of interface you need.</span></span> <span data-ttu-id="259df-105">Los métodos tienen el formato *astype* e incluyen un método para cada tipo de variable de efecto (como asblend, AsConstantBuffer, etc.).</span><span class="sxs-lookup"><span data-stu-id="259df-105">The methods are of the form *AsType* and include a method for each type of effect variable (such as AsBlend, AsConstantBuffer etc..)</span></span>

<span data-ttu-id="259df-106">Por ejemplo, supongamos que tiene un efecto con dos variables globales: el tiempo y una transformación universal.</span><span class="sxs-lookup"><span data-stu-id="259df-106">For example, suppose you have an effect with two global variables: time and a world transform.</span></span>


```
float    g_fTime;
float4x4 g_mWorld;
```



<span data-ttu-id="259df-107">Este es un ejemplo que obtiene estas variables:</span><span class="sxs-lookup"><span data-stu-id="259df-107">Here is an example that gets these variables:</span></span>


```
ID3DX11EffectVariable* g_pVariable;
ID3DX11EffectMatrixVariable* g_pmWorld;
ID3DX11EffectScalarVariable* g_pfTime;

g_pVariable = g_pEffect11->GetVariableByName("g_mWorld");
g_pmWorld = g_pVariable->AsMatrix();
g_pVariable = g_pEffect11->GetVariableByName("g_fTime");
g_pfTime = g_pVariable->AsScalar();
```



<span data-ttu-id="259df-108">Al especializar las interfaces, podría reducir el código a una sola llamada.</span><span class="sxs-lookup"><span data-stu-id="259df-108">By specializing the interfaces, you could reduce the code to a single call.</span></span>


```
g_pmWorld = (g_pEffect11->GetVariableByName("g_mWorld"))->AsMatrix();
g_pfTime = (g_pEffect11->GetVariableByName("g_fTime"))->AsScalar();
```



<span data-ttu-id="259df-109">Las interfaces que heredan de [**ID3DX11EffectVariable**](id3dx11effectvariable.md) también tienen estos métodos, pero se han diseñado para devolver objetos no válidos. solo las llamadas de **ID3DX11EffectVariable** devuelven objetos válidos.</span><span class="sxs-lookup"><span data-stu-id="259df-109">Interfaces that inherit from [**ID3DX11EffectVariable**](id3dx11effectvariable.md) also have these methods, but they have been designed to return invalid objects; only calls from **ID3DX11EffectVariable** return valid objects.</span></span> <span data-ttu-id="259df-110">Las aplicaciones pueden probar el objeto devuelto para ver si es válido llamando a [**ID3DX11EffectVariable:: IsValid**](id3dx11effectvariable-isvalid.md).</span><span class="sxs-lookup"><span data-stu-id="259df-110">Applications can test the returned object to see if it is valid by calling [**ID3DX11EffectVariable::IsValid**](id3dx11effectvariable-isvalid.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="259df-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="259df-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="259df-112">Efectos (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="259df-112">Effects (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 




