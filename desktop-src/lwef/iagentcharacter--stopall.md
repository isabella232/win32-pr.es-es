---
title: IAgentCharacter StopAll
description: IAgentCharacter StopAll
ms.assetid: cb0ce220-7b35-45c0-b587-30939d26740f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bbe745f0611d184fefd729c04e50635bc4006e8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714207"
---
# <a name="iagentcharacterstopall"></a><span data-ttu-id="803b2-103">IAgentCharacter:: StopAll</span><span class="sxs-lookup"><span data-stu-id="803b2-103">IAgentCharacter::StopAll</span></span>

<span data-ttu-id="803b2-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="803b2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT StopAll();
   long lType,  // request type
```

<span data-ttu-id="803b2-105">Detiene todas las animaciones (solicitudes) y las quita de la cola de animaciones del carácter.</span><span class="sxs-lookup"><span data-stu-id="803b2-105">Stops all animations (requests) and removes them from the character's animation queue.</span></span>

<dl> <dt>

<span data-ttu-id="803b2-106"><span id="lType"></span><span id="ltype"></span><span id="LTYPE"></span>*lType*</span><span class="sxs-lookup"><span data-stu-id="803b2-106"><span id="lType"></span><span id="ltype"></span><span id="LTYPE"></span>*lType*</span></span>
</dt> <dd>

<span data-ttu-id="803b2-107">Un campo de bits que indica los tipos de solicitudes que se van a detener (y quitar de la cola del carácter), que se componen de lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="803b2-107">A bitfield that indicates the types of requests to stop (and remove from the character's queue), comprised from the following:</span></span>



|                                                                                   |                                                                                                          |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="803b2-108">**const unsigned Long** **Stop \_ Type \_ All = 0xFFFFFFFF;**</span><span class="sxs-lookup"><span data-stu-id="803b2-108">**const unsigned long** **STOP\_TYPE\_ALL = 0xFFFFFFFF;**</span></span><br/>              | <span data-ttu-id="803b2-109">Detiene todas las solicitudes de animación, incluidas las solicitudes de [**preparación**](iagentcharacter--prepare.md) no en cola.</span><span class="sxs-lookup"><span data-stu-id="803b2-109">Stops all animation requests, including non-queued [**Prepare**](iagentcharacter--prepare.md) requests.</span></span> |
| <span data-ttu-id="803b2-110">**const unsigned Long** **Stop \_ Type \_ Play = 0x00000001;**</span><span class="sxs-lookup"><span data-stu-id="803b2-110">**const unsigned long** **STOP\_TYPE\_PLAY = 0x00000001;**</span></span><br/>             | <span data-ttu-id="803b2-111">Detiene todas las solicitudes de reproducción.</span><span class="sxs-lookup"><span data-stu-id="803b2-111">Stops all Play requests.</span></span>                                                                                 |
| <span data-ttu-id="803b2-112">**const unsigned Long** **Stop \_ Type \_ Move = 0x00000002;**</span><span class="sxs-lookup"><span data-stu-id="803b2-112">**const unsigned long** **STOP\_TYPE\_MOVE = 0x00000002;**</span></span><br/>             | <span data-ttu-id="803b2-113">Detiene todas las solicitudes de [**movimiento**](https://www.bing.com/search?q=**Move**) .</span><span class="sxs-lookup"><span data-stu-id="803b2-113">Stops all [**Move**](https://www.bing.com/search?q=**Move**) requests.</span></span>                                               |
| <span data-ttu-id="803b2-114">**const unsigned Long** **Stop \_ Escriba \_ Speak = 0x00000004;**</span><span class="sxs-lookup"><span data-stu-id="803b2-114">**const unsigned long** **STOP\_TYPE\_SPEAK = 0x00000004;**</span></span><br/>            | <span data-ttu-id="803b2-115">Detiene todas las solicitudes de [**voz**](iagentcharacter--speak.md) .</span><span class="sxs-lookup"><span data-stu-id="803b2-115">Stops all [**Speak**](iagentcharacter--speak.md) requests.</span></span>                                              |
| <span data-ttu-id="803b2-116">**const unsigned Long** **Stop \_ Escriba \_ Prepare = 0x00000008;**</span><span class="sxs-lookup"><span data-stu-id="803b2-116">**const unsigned long** **STOP\_TYPE\_PREPARE = 0x00000008;**</span></span><br/>          | <span data-ttu-id="803b2-117">Detiene todas las solicitudes de [**preparación**](iagentcharacter--prepare.md) en cola.</span><span class="sxs-lookup"><span data-stu-id="803b2-117">Stops all queued [**Prepare**](iagentcharacter--prepare.md) requests.</span></span>                                   |
| <span data-ttu-id="803b2-118">**const unsigned Long** **Stop \_ Type \_ NONQUEUEDPREPARE = 0x00000010;**</span><span class="sxs-lookup"><span data-stu-id="803b2-118">**const unsigned long** **STOP\_TYPE\_NONQUEUEDPREPARE = 0x00000010;**</span></span><br/> | <span data-ttu-id="803b2-119">Detiene todas las solicitudes de [**preparación**](iagentcharacter--prepare.md) no en cola.</span><span class="sxs-lookup"><span data-stu-id="803b2-119">Stops all non-queued [**Prepare**](iagentcharacter--prepare.md) requests.</span></span>                               |
| <span data-ttu-id="803b2-120">**const unsigned Long** **Stop \_ Type \_ visible = 0x00000020;**</span><span class="sxs-lookup"><span data-stu-id="803b2-120">**const unsigned long** **STOP\_TYPE\_VISIBLE = 0x00000020;**</span></span><br/>          | <span data-ttu-id="803b2-121">Detiene todas las solicitudes [**Hide**](iagentcharacter--hide.md) o [**Show**](iagentcharacter--show.md) .</span><span class="sxs-lookup"><span data-stu-id="803b2-121">Stops all [**Hide**](iagentcharacter--hide.md) or [**Show**](iagentcharacter--show.md) requests.</span></span>       |



 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="803b2-122">Consulte también</span><span class="sxs-lookup"><span data-stu-id="803b2-122">See Also</span></span>

[<span data-ttu-id="803b2-123">**IAgentCharacter:: Stop**</span><span class="sxs-lookup"><span data-stu-id="803b2-123">**IAgentCharacter::Stop**</span></span>](iagentcharacter--stop.md)


 

 





