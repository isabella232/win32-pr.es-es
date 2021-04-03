---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 3A4C5579-7543-4E0B-921D-BED42C2583D9
title: D (aplicaciones aisladas y ensamblados en paralelo)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20c8912f24478f79be8aa00c963dc27cb46ec756
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082776"
---
# <a name="d-isolated-applications-and-side-by-side-assemblies"></a><span data-ttu-id="c6d73-103">D (aplicaciones aisladas y ensamblados en paralelo)</span><span class="sxs-lookup"><span data-stu-id="c6d73-103">D (Isolated Applications and Side-by-side Assemblies)</span></span>

<span data-ttu-id="c6d73-104">[A](a-sbscs-gly.md) B C D E F [G](g-sbscs-gly.md) H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N o [p](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) [s](s-sbscs-gly.md) T U V W X Y Z</span><span class="sxs-lookup"><span data-stu-id="c6d73-104">[A](a-sbscs-gly.md) B C D E F [G](g-sbscs-gly.md) H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O [P](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T U V W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="c6d73-105"><span id="_win32_def_context_assemblyidentity_gly"></span><span id="_WIN32_DEF_CONTEXT_ASSEMBLYIDENTITY_GLY"></span>**Autodef: contexto assemblyIdentity**</span><span class="sxs-lookup"><span data-stu-id="c6d73-105"><span id="_win32_def_context_assemblyidentity_gly"></span><span id="_WIN32_DEF_CONTEXT_ASSEMBLYIDENTITY_GLY"></span>**DEF-context assemblyIdentity**</span></span>
</dt> <dd>

<span data-ttu-id="c6d73-106">Un subelemento **assemblyIdentity** que define el ensamblado en paralelo descrito por el manifiesto.</span><span class="sxs-lookup"><span data-stu-id="c6d73-106">An **assemblyIdentity** subelement defining the side-by-side assembly described by the manifest.</span></span> <span data-ttu-id="c6d73-107">Un subelemento **assemblyIdentity** de Def-context siempre es el primer subelemento de un elemento **Assembly** .</span><span class="sxs-lookup"><span data-stu-id="c6d73-107">A DEF-context **assemblyIdentity** subelement is always the first subelement of an **assembly** element.</span></span>

</dd> <dt>

<span data-ttu-id="c6d73-108"><span id="_win32_dll_versioning_conflict_gly"></span><span id="_WIN32_DLL_VERSIONING_CONFLICT_GLY"></span>**Conflicto de control de versiones de DLL**</span><span class="sxs-lookup"><span data-stu-id="c6d73-108"><span id="_win32_dll_versioning_conflict_gly"></span><span id="_WIN32_DLL_VERSIONING_CONFLICT_GLY"></span>**DLL versioning conflict**</span></span>
</dt> <dd>

<span data-ttu-id="c6d73-109">Problema de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="c6d73-109">Compatibility problem.</span></span> <span data-ttu-id="c6d73-110">Los problemas de uso compartido de ensamblados se producen cuando una aplicación instala una versión de un ensamblado compartido que no es compatible con versiones anteriores de la versión instalada previamente.</span><span class="sxs-lookup"><span data-stu-id="c6d73-110">Assembly sharing problems occur when an application installs a version of a shared assembly that is not backward compatible with the previously installed version.</span></span> <span data-ttu-id="c6d73-111">Una solución a los conflictos de control de versiones de DLL es usar el uso compartido de ensamblados en paralelo y aplicaciones aisladas.</span><span class="sxs-lookup"><span data-stu-id="c6d73-111">A solution to DLL versioning conflicts is to use side-by-side assembly sharing and isolated applications.</span></span> <span data-ttu-id="c6d73-112">Con el uso compartido de ensamblados en paralelo, se pueden ejecutar simultáneamente varias versiones del mismo ensamblado de Windows.</span><span class="sxs-lookup"><span data-stu-id="c6d73-112">With side-by-side assembly sharing, multiple versions of the same Windows assembly can run simultaneously.</span></span> <span data-ttu-id="c6d73-113">Los desarrolladores pueden elegir el ensamblado en paralelo que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="c6d73-113">Developers can choose which side-by-side assembly to use.</span></span>

</dd> </dl>

 

 



