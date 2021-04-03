---
title: IAgentCharacterEx GetVersion
description: IAgentCharacterEx GetVersion
ms.assetid: 78f6d7b6-f72d-4af8-a014-3acd185926f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f5c72d9304aa689cda83117d57f26c2da776c9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075535"
---
# <a name="iagentcharacterexgetversion"></a><span data-ttu-id="1364d-103">IAgentCharacterEx:: GetVersion</span><span class="sxs-lookup"><span data-stu-id="1364d-103">IAgentCharacterEx::GetVersion</span></span>

<span data-ttu-id="1364d-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1364d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVersion(
   short * psMajor,  // address of major version
   short * psMinor   // address of minor version
);
```

<span data-ttu-id="1364d-105">Recupera el número de versión del conjunto de animaciones estándar de caracteres.</span><span class="sxs-lookup"><span data-stu-id="1364d-105">Retrieves the version number of the character standard animation set.</span></span>

-   <span data-ttu-id="1364d-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="1364d-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="1364d-107"><span id="psMajor"></span><span id="psmajor"></span><span id="PSMAJOR"></span>*psMajor*</span><span class="sxs-lookup"><span data-stu-id="1364d-107"><span id="psMajor"></span><span id="psmajor"></span><span id="PSMAJOR"></span>*psMajor*</span></span>
</dt> <dd>

<span data-ttu-id="1364d-108">Dirección de una variable que recibe la versión principal.</span><span class="sxs-lookup"><span data-stu-id="1364d-108">Address of a variable that receives the major version.</span></span>

</dd> <dt>

<span data-ttu-id="1364d-109"><span id="psMinor"></span><span id="psminor"></span><span id="PSMINOR"></span>*psMinor*</span><span class="sxs-lookup"><span data-stu-id="1364d-109"><span id="psMinor"></span><span id="psminor"></span><span id="PSMINOR"></span>*psMinor*</span></span>
</dt> <dd>

<span data-ttu-id="1364d-110">Dirección de una variable que recibe la versión secundaria.</span><span class="sxs-lookup"><span data-stu-id="1364d-110">Address of a variable that receives the minor version.</span></span>

</dd> </dl>

<span data-ttu-id="1364d-111">El número de versión del conjunto de animaciones estándar se establece automáticamente al compilarlo con el editor de caracteres del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1364d-111">The standard animation set version number is automatically set when you build it with the Microsoft Agent Character Editor.</span></span>

 

 




