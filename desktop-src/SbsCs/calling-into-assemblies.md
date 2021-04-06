---
description: Cuando se llama a entryPoints de un ensamblado, se recomienda usar el mismo contexto de activación que estaba activo al buscar el ensamblado.
ms.assetid: 8b2de5f5-ea95-441f-9345-b64de53ea05f
title: Llamar a ensamblados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03e4742b19ea47e03fac5f7d0318248ea167182e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002186"
---
# <a name="calling-into-assemblies"></a><span data-ttu-id="283d4-103">Llamar a ensamblados</span><span class="sxs-lookup"><span data-stu-id="283d4-103">Calling Into Assemblies</span></span>

<span data-ttu-id="283d4-104">Cuando se llama a entryPoints de un ensamblado, se recomienda usar el mismo contexto de activación que estaba activo al buscar el ensamblado.</span><span class="sxs-lookup"><span data-stu-id="283d4-104">When calling into the entrypoints of an assembly, it is recommended that you use the same activation context that was active when searching for the assembly.</span></span> <span data-ttu-id="283d4-105">Como mínimo, asegúrese de que el componente que carga el ensamblado no obtiene accidentalmente el contexto de activación que está usando la aplicación.</span><span class="sxs-lookup"><span data-stu-id="283d4-105">At minimum, ensure that the component loading the assembly does not accidentally get the activation context your application is using.</span></span> <span data-ttu-id="283d4-106">La pérdida de contexto de activación a través de los límites de DLL puede provocar dependencias inesperadas.</span><span class="sxs-lookup"><span data-stu-id="283d4-106">Leaking activation context across DLL boundaries can lead to unexpected dependencies.</span></span> <span data-ttu-id="283d4-107">Esto no es un problema si la aplicación compila el reconocimiento de \_ aislamiento \_ habilitado porque, en ese caso, no hay ningún contexto de activación activo de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="283d4-107">This is not a problem if your application compiles ISOLATION\_AWARE\_ENABLED because in that case no activation context is active by default.</span></span> <span data-ttu-id="283d4-108">Si no compila con el reconocimiento de \_ aislamiento \_ habilitado definido, debe activar el contexto de activación **null** o el mismo contexto de activación que se usó para cargar el ensamblado.</span><span class="sxs-lookup"><span data-stu-id="283d4-108">If you do not compile with ISOLATION\_AWARE\_ENABLED defined, you should activate the **NULL** activation context or the same activation context that was used to load the assembly.</span></span>

<span data-ttu-id="283d4-109">En el ejemplo siguiente se garantiza que la DLL hospedada se ejecuta en un contexto que reconoce:</span><span class="sxs-lookup"><span data-stu-id="283d4-109">The following example ensures that the hosted DLL runs in a context that it recognizes:</span></span>

``` syntax
ULONG_PTR ulpCookie;
ActivateActCtx(hTheActCtxForMyDll, &ulpCookie);
__try 
{
        MyDllIsolatedFunction();
    myDllIsolatedComInterface->Funct();
}
__finally 
{
    DeactivateActCtx(0, ulpCookie);
}
```

 

 



