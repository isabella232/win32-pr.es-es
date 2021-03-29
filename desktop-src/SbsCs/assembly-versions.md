---
description: Cada ensamblado simultáneo debe tener una versión.
ms.assetid: 0b78ecf6-fbff-4172-9b0d-09f993666db1
title: Versiones de ensamblado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48c9e32ecc0990572f17264edd2ff51c205a01c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814779"
---
# <a name="assembly-versions"></a><span data-ttu-id="41c53-103">Versiones de ensamblado</span><span class="sxs-lookup"><span data-stu-id="41c53-103">Assembly Versions</span></span>

<span data-ttu-id="41c53-104">Cada ensamblado simultáneo debe tener una versión.</span><span class="sxs-lookup"><span data-stu-id="41c53-104">Every side-by-side assembly must have a version.</span></span> <span data-ttu-id="41c53-105">Cada versión del ensamblado está asociada a un número de versión que tiene cuatro partes separadas por puntos: *principal. secundaria. compilación. revisión*.</span><span class="sxs-lookup"><span data-stu-id="41c53-105">Each assembly version is associated with a version number having four parts separated by periods: *major.minor.build.revision*.</span></span> <span data-ttu-id="41c53-106">Si se realiza un cambio en un ensamblado que hace que sea incompatible con las versiones existentes, se deben cambiar las partes *principales* o *secundarias* del número de versión.</span><span class="sxs-lookup"><span data-stu-id="41c53-106">If a change is made to an assembly making it incompatible with existing versions, the *major* or *minor* parts of the version number must be changed.</span></span> <span data-ttu-id="41c53-107">Un número de versión que solo cambia en las partes de la *compilación* o de la *revisión* indica que el ensamblado es compatible con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="41c53-107">A version number that changes only in the *build* or *revision* parts indicates that the assembly is backward compatible with prior versions.</span></span>

<span data-ttu-id="41c53-108">La versión debe especificarse en los elementos **assemblyIdentity** de los [manifiestos](manifests.md).</span><span class="sxs-lookup"><span data-stu-id="41c53-108">The version must be specified in **assemblyIdentity** elements of [manifests](manifests.md).</span></span> <span data-ttu-id="41c53-109">Use el formato de versión de cuatro partes: mmmmm. nnnnn. ooooo. ppppp.</span><span class="sxs-lookup"><span data-stu-id="41c53-109">Use the four-part version format: mmmmm.nnnnn.ooooo.ppppp.</span></span> <span data-ttu-id="41c53-110">Cada una de las partes separadas por puntos puede ser 0-65535, ambos inclusive.</span><span class="sxs-lookup"><span data-stu-id="41c53-110">Each of the parts separated by periods can be 0-65535 inclusive.</span></span>

 

 



