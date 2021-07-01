---
title: IAgentCharacter GetMoveCause
description: IAgentCharacter GetMoveCause
ms.assetid: 36cdd3bc-65b6-469f-9344-93403c1d24e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be943cf3b25b789838215f0209b16e67d5b50659
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119690"
---
# <a name="iagentcharactergetmovecause"></a><span data-ttu-id="ad274-103">IAgentCharacter::GetMoveCause</span><span class="sxs-lookup"><span data-stu-id="ad274-103">IAgentCharacter::GetMoveCause</span></span>

<span data-ttu-id="ad274-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ad274-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetMoveCause(
   long * pdwCause  // address of variable for cause of character move
);
```

<span data-ttu-id="ad274-105">Recupera la causa del último movimiento del carácter.</span><span class="sxs-lookup"><span data-stu-id="ad274-105">Retrieves the cause of the character's last move.</span></span>

-   <span data-ttu-id="ad274-106">Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="ad274-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="ad274-107"><span id="pdwCause"></span><span id="pdwcause"></span><span id="PDWCAUSE"></span>*pdwCause*</span><span class="sxs-lookup"><span data-stu-id="ad274-107"><span id="pdwCause"></span><span id="pdwcause"></span><span id="PDWCAUSE"></span>*pdwCause*</span></span>
</dt> <dd>

<span data-ttu-id="ad274-108">Dirección de una variable que recibe la causa del último movimiento del carácter y será una de las siguientes:</span><span class="sxs-lookup"><span data-stu-id="ad274-108">Address of a variable that receives the cause of the character's last move and will be one of the following:</span></span>



| <span data-ttu-id="ad274-109">Valor</span><span class="sxs-lookup"><span data-stu-id="ad274-109">Value</span></span>                                                               | <span data-ttu-id="ad274-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="ad274-110">Description</span></span>                                                                                     |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ad274-111">**const unsigned short** **NeverMoved = 0;**</span><span class="sxs-lookup"><span data-stu-id="ad274-111">**const unsigned short** **NeverMoved = 0;**</span></span><br/>        | <span data-ttu-id="ad274-112">El carácter no se ha movido.</span><span class="sxs-lookup"><span data-stu-id="ad274-112">Character has not been moved.</span></span>                                                        |
| <span data-ttu-id="ad274-113">**const unsigned short** **UserMoved = 1;**</span><span class="sxs-lookup"><span data-stu-id="ad274-113">**const unsigned short** **UserMoved = 1;**</span></span><br/>         | <span data-ttu-id="ad274-114">El usuario arrastró el carácter.</span><span class="sxs-lookup"><span data-stu-id="ad274-114">User dragged the character.</span></span>                                                          |
| <span data-ttu-id="ad274-115">**const unsigned short** **ProgramMoved = 2;**</span><span class="sxs-lookup"><span data-stu-id="ad274-115">**const unsigned short** **ProgramMoved = 2;**</span></span><br/>      | <span data-ttu-id="ad274-116">La aplicación movió el carácter.</span><span class="sxs-lookup"><span data-stu-id="ad274-116">Your application moved the character.</span></span>                                                |
| <span data-ttu-id="ad274-117">**const unsigned short** **OtherProgramMoved = 3;**</span><span class="sxs-lookup"><span data-stu-id="ad274-117">**const unsigned short** **OtherProgramMoved = 3;**</span></span><br/> | <span data-ttu-id="ad274-118">Otra aplicación movió el carácter.</span><span class="sxs-lookup"><span data-stu-id="ad274-118">Another application moved the character.</span></span>                                             |
| <span data-ttu-id="ad274-119">**const unsigned short** **SystemMoved = 4**</span><span class="sxs-lookup"><span data-stu-id="ad274-119">**const unsigned short** **SystemMoved = 4**</span></span><br/>        | <span data-ttu-id="ad274-120">El servidor movió el carácter para mantenerlo en pantalla después de un cambio de resolución de pantalla.</span><span class="sxs-lookup"><span data-stu-id="ad274-120">The server moved the character to keep it onscreen after a screen resolution change.</span></span> |



 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="ad274-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ad274-121">See Also</span></span>

[<span data-ttu-id="ad274-122">**IAgentNotifySink::Move**</span><span class="sxs-lookup"><span data-stu-id="ad274-122">**IAgentNotifySink::Move**</span></span>](iagentnotifysink--move.md)


 

 





