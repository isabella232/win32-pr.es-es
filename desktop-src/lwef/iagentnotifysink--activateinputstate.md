---
title: IAgentNotifySink ActivateInputState
description: IAgentNotifySink ActivateInputState
ms.assetid: 2476e475-d80c-47e9-bb60-e0fca41becc9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5821f5943bb87f9c19a66125028604fa5d116a7e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269119"
---
# <a name="iagentnotifysinkactivateinputstate"></a><span data-ttu-id="e6385-103">IAgentNotifySink::ActivateInputState</span><span class="sxs-lookup"><span data-stu-id="e6385-103">IAgentNotifySink::ActivateInputState</span></span>

<span data-ttu-id="e6385-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e6385-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT ActivateInputState(
   long dwCharID,   // character ID
   long bActivated  // input activation flag
);                          
```

<span data-ttu-id="e6385-105">Notifica a una aplicación cliente que ha cambiado el estado activo de entrada de un carácter.</span><span class="sxs-lookup"><span data-stu-id="e6385-105">Notifies a client application that a character's input active state changed.</span></span>

-   <span data-ttu-id="e6385-106">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="e6385-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="e6385-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="e6385-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="e6385-108">Identificador del carácter cuyo estado de activación de entrada ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="e6385-108">Identifier of the character whose input activation state changed.</span></span>

</dd> <dt>

<span data-ttu-id="e6385-109"><span id="bActivated"></span><span id="bactivated"></span><span id="BACTIVATED"></span>*bActivated*</span><span class="sxs-lookup"><span data-stu-id="e6385-109"><span id="bActivated"></span><span id="bactivated"></span><span id="BACTIVATED"></span>*bActivated*</span></span>
</dt> <dd>

<span data-ttu-id="e6385-110">Marca activa de entrada.</span><span class="sxs-lookup"><span data-stu-id="e6385-110">Input active flag.</span></span> <span data-ttu-id="e6385-111">Este valor booleano es **true** si el carácter al que hace referencia *dwCharID* se convirtió en una entrada activa; y **false** si el carácter perdió su estado activo de entrada.</span><span class="sxs-lookup"><span data-stu-id="e6385-111">This Boolean value is **True** if the character referred to by *dwCharID* became input active; and **False** if the character lost its input active state.</span></span>

</dd> </dl>

 

 




