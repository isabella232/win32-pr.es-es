---
title: IAgentEx GetVersion
description: IAgentEx GetVersion
ms.assetid: e5d55fcd-c1b4-4c9e-b3c7-4471af2f86af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 359abb1d22e2cd34fb6b31d85012ac0110f14037
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357317"
---
# <a name="iagentexgetversion"></a><span data-ttu-id="d9777-103">IAgentEx:: GetVersion</span><span class="sxs-lookup"><span data-stu-id="d9777-103">IAgentEx::GetVersion</span></span>

<span data-ttu-id="d9777-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d9777-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVersion(
   short * psMajor,  // address of major version
   short * psMinor   // address of minor version
);
```

<span data-ttu-id="d9777-105">Recupera el número de versión del servidor de agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d9777-105">Retrieves the version number of Microsoft Agent server.</span></span>

-   <span data-ttu-id="d9777-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="d9777-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="d9777-107"><span id="psMajor"></span><span id="psmajor"></span><span id="PSMAJOR"></span>*psMajor*</span><span class="sxs-lookup"><span data-stu-id="d9777-107"><span id="psMajor"></span><span id="psmajor"></span><span id="PSMAJOR"></span>*psMajor*</span></span>
</dt> <dd>

<span data-ttu-id="d9777-108">Dirección de una variable que recibe la versión principal.</span><span class="sxs-lookup"><span data-stu-id="d9777-108">Address of a variable that receives the major version.</span></span>

</dd> <dt>

<span data-ttu-id="d9777-109"><span id="psMinor"></span><span id="psminor"></span><span id="PSMINOR"></span>*psMinor*</span><span class="sxs-lookup"><span data-stu-id="d9777-109"><span id="psMinor"></span><span id="psminor"></span><span id="PSMINOR"></span>*psMinor*</span></span>
</dt> <dd>

<span data-ttu-id="d9777-110">Dirección de una variable que recibe la versión secundaria.</span><span class="sxs-lookup"><span data-stu-id="d9777-110">Address of a variable that receives the minor version.</span></span>

</dd> </dl>

 

 




