---
title: IAgentCharacter StopAll
description: IAgentCharacter StopAll
ms.assetid: cb0ce220-7b35-45c0-b587-30939d26740f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 558ca23b500ee2146470c8d595b2a5a64febf59a
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120918"
---
# <a name="iagentcharacterstopall"></a><span data-ttu-id="b3552-103">IAgentCharacter::StopAll</span><span class="sxs-lookup"><span data-stu-id="b3552-103">IAgentCharacter::StopAll</span></span>

<span data-ttu-id="b3552-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b3552-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT StopAll();
   long lType,  // request type
```

<span data-ttu-id="b3552-105">Detiene todas las animaciones (solicitudes) y las quita de la cola de animación del carácter.</span><span class="sxs-lookup"><span data-stu-id="b3552-105">Stops all animations (requests) and removes them from the character's animation queue.</span></span>

<dl> <dt>

<span data-ttu-id="b3552-106"><span id="lType"></span><span id="ltype"></span><span id="LTYPE"></span>*lType*</span><span class="sxs-lookup"><span data-stu-id="b3552-106"><span id="lType"></span><span id="ltype"></span><span id="LTYPE"></span>*lType*</span></span>
</dt> <dd>

<span data-ttu-id="b3552-107">Campo de bits que indica los tipos de solicitudes que se detienen (y quitan de la cola del carácter), que consta de lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="b3552-107">A bitfield that indicates the types of requests to stop (and remove from the character's queue), comprised from the following:</span></span>



| <span data-ttu-id="b3552-108">Valor</span><span class="sxs-lookup"><span data-stu-id="b3552-108">Value</span></span>                                                                                  |  <span data-ttu-id="b3552-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="b3552-109">Description</span></span>                                                                                                        |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3552-110">**const unsigned long** **STOP TYPE ALL = \_ \_ 0xFFFFFFFF;**</span><span class="sxs-lookup"><span data-stu-id="b3552-110">**const unsigned long** **STOP\_TYPE\_ALL = 0xFFFFFFFF;**</span></span><br/>              | <span data-ttu-id="b3552-111">Detiene todas las solicitudes de animación, incluidas las solicitudes [**de preparación**](iagentcharacter--prepare.md) no en cola.</span><span class="sxs-lookup"><span data-stu-id="b3552-111">Stops all animation requests, including non-queued [**Prepare**](iagentcharacter--prepare.md) requests.</span></span> |
| <span data-ttu-id="b3552-112">**const unsigned long** **STOP TYPE PLAY = \_ \_ 0x00000001;**</span><span class="sxs-lookup"><span data-stu-id="b3552-112">**const unsigned long** **STOP\_TYPE\_PLAY = 0x00000001;**</span></span><br/>             | <span data-ttu-id="b3552-113">Detiene todas las solicitudes de reproducción.</span><span class="sxs-lookup"><span data-stu-id="b3552-113">Stops all Play requests.</span></span>                                                                                 |
| <span data-ttu-id="b3552-114">**const unsigned long** **STOP TYPE MOVE = \_ \_ 0x00000002;**</span><span class="sxs-lookup"><span data-stu-id="b3552-114">**const unsigned long** **STOP\_TYPE\_MOVE = 0x00000002;**</span></span><br/>             | <span data-ttu-id="b3552-115">Detiene todas [**las solicitudes**](https://www.bing.com/search?q=**Move**) move.</span><span class="sxs-lookup"><span data-stu-id="b3552-115">Stops all [**Move**](https://www.bing.com/search?q=**Move**) requests.</span></span>                                               |
| <span data-ttu-id="b3552-116">**const unsigned long** **STOP TYPE SPEAK = \_ \_ 0x00000004;**</span><span class="sxs-lookup"><span data-stu-id="b3552-116">**const unsigned long** **STOP\_TYPE\_SPEAK = 0x00000004;**</span></span><br/>            | <span data-ttu-id="b3552-117">Detiene todas las [**solicitudes speak.**](iagentcharacter--speak.md)</span><span class="sxs-lookup"><span data-stu-id="b3552-117">Stops all [**Speak**](iagentcharacter--speak.md) requests.</span></span>                                              |
| <span data-ttu-id="b3552-118">**const unsigned long** **STOP TYPE PREPARE = \_ \_ 0x00000008;**</span><span class="sxs-lookup"><span data-stu-id="b3552-118">**const unsigned long** **STOP\_TYPE\_PREPARE = 0x00000008;**</span></span><br/>          | <span data-ttu-id="b3552-119">Detiene todas las solicitudes [**de preparación en**](iagentcharacter--prepare.md) cola.</span><span class="sxs-lookup"><span data-stu-id="b3552-119">Stops all queued [**Prepare**](iagentcharacter--prepare.md) requests.</span></span>                                   |
| <span data-ttu-id="b3552-120">**const unsigned long** **STOP TYPE \_ \_ NONQUEUEDPREPARE = 0x00000010;**</span><span class="sxs-lookup"><span data-stu-id="b3552-120">**const unsigned long** **STOP\_TYPE\_NONQUEUEDPREPARE = 0x00000010;**</span></span><br/> | <span data-ttu-id="b3552-121">Detiene todas las solicitudes de [**preparación que no están en**](iagentcharacter--prepare.md) cola.</span><span class="sxs-lookup"><span data-stu-id="b3552-121">Stops all non-queued [**Prepare**](iagentcharacter--prepare.md) requests.</span></span>                               |
| <span data-ttu-id="b3552-122">**const unsigned long** **STOP TYPE VISIBLE = \_ \_ 0x00000020;**</span><span class="sxs-lookup"><span data-stu-id="b3552-122">**const unsigned long** **STOP\_TYPE\_VISIBLE = 0x00000020;**</span></span><br/>          | <span data-ttu-id="b3552-123">Detiene todas [**las solicitudes**](iagentcharacter--hide.md) Ocultar [**o**](iagentcharacter--show.md) Mostrar.</span><span class="sxs-lookup"><span data-stu-id="b3552-123">Stops all [**Hide**](iagentcharacter--hide.md) or [**Show**](iagentcharacter--show.md) requests.</span></span>       |



 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="b3552-124">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b3552-124">See Also</span></span>

[<span data-ttu-id="b3552-125">**IAgentCharacter::Stop**</span><span class="sxs-lookup"><span data-stu-id="b3552-125">**IAgentCharacter::Stop**</span></span>](iagentcharacter--stop.md)


 

 





