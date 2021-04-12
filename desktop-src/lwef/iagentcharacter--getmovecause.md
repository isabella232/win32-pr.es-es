---
title: IAgentCharacter GetMoveCause
description: IAgentCharacter GetMoveCause
ms.assetid: 36cdd3bc-65b6-469f-9344-93403c1d24e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 612fcbfd4470d17e2365373458a8ded899a8180a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419206"
---
# <a name="iagentcharactergetmovecause"></a><span data-ttu-id="3f42b-103">IAgentCharacter::GetMoveCause</span><span class="sxs-lookup"><span data-stu-id="3f42b-103">IAgentCharacter::GetMoveCause</span></span>

<span data-ttu-id="3f42b-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3f42b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetMoveCause(
   long * pdwCause  // address of variable for cause of character move
);
```

<span data-ttu-id="3f42b-105">Recupera la causa del último movimiento del carácter.</span><span class="sxs-lookup"><span data-stu-id="3f42b-105">Retrieves the cause of the character's last move.</span></span>

-   <span data-ttu-id="3f42b-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="3f42b-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="3f42b-107"><span id="pdwCause"></span><span id="pdwcause"></span><span id="PDWCAUSE"></span>*pdwCause*</span><span class="sxs-lookup"><span data-stu-id="3f42b-107"><span id="pdwCause"></span><span id="pdwcause"></span><span id="PDWCAUSE"></span>*pdwCause*</span></span>
</dt> <dd>

<span data-ttu-id="3f42b-108">Dirección de una variable que recibe la causa del último movimiento del carácter y será uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="3f42b-108">Address of a variable that receives the cause of the character's last move and will be one of the following:</span></span>



|                                                                |                                                                                      |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3f42b-109">**const unsigned short** **NeverMoved = 0;**</span><span class="sxs-lookup"><span data-stu-id="3f42b-109">**const unsigned short** **NeverMoved = 0;**</span></span><br/>        | <span data-ttu-id="3f42b-110">No se ha despasado el carácter.</span><span class="sxs-lookup"><span data-stu-id="3f42b-110">Character has not been moved.</span></span>                                                        |
| <span data-ttu-id="3f42b-111">**const unsigned short** **UserMoved = 1;**</span><span class="sxs-lookup"><span data-stu-id="3f42b-111">**const unsigned short** **UserMoved = 1;**</span></span><br/>         | <span data-ttu-id="3f42b-112">El usuario arrastró el carácter.</span><span class="sxs-lookup"><span data-stu-id="3f42b-112">User dragged the character.</span></span>                                                          |
| <span data-ttu-id="3f42b-113">**const unsigned short** **ProgramMoved = 2;**</span><span class="sxs-lookup"><span data-stu-id="3f42b-113">**const unsigned short** **ProgramMoved = 2;**</span></span><br/>      | <span data-ttu-id="3f42b-114">La aplicación ha cambiado el carácter.</span><span class="sxs-lookup"><span data-stu-id="3f42b-114">Your application moved the character.</span></span>                                                |
| <span data-ttu-id="3f42b-115">**const unsigned short** **OtherProgramMoved = 3;**</span><span class="sxs-lookup"><span data-stu-id="3f42b-115">**const unsigned short** **OtherProgramMoved = 3;**</span></span><br/> | <span data-ttu-id="3f42b-116">Otra aplicación ha cambiado el carácter.</span><span class="sxs-lookup"><span data-stu-id="3f42b-116">Another application moved the character.</span></span>                                             |
| <span data-ttu-id="3f42b-117">**const unsigned short** **SystemMoved = 4**</span><span class="sxs-lookup"><span data-stu-id="3f42b-117">**const unsigned short** **SystemMoved = 4**</span></span><br/>        | <span data-ttu-id="3f42b-118">El servidor ha quitado el carácter para mantenerlo en la pantalla después de un cambio en la resolución de pantalla.</span><span class="sxs-lookup"><span data-stu-id="3f42b-118">The server moved the character to keep it onscreen after a screen resolution change.</span></span> |



 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="3f42b-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="3f42b-119">See Also</span></span>

[<span data-ttu-id="3f42b-120">**IAgentNotifySink:: Move**</span><span class="sxs-lookup"><span data-stu-id="3f42b-120">**IAgentNotifySink::Move**</span></span>](iagentnotifysink--move.md)


 

 





