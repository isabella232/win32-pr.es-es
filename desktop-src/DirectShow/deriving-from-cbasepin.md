---
description: Derivación de CBasePin
ms.assetid: ef453bec-e5a9-4185-94e3-f934e748b11f
title: Derivación de CBasePin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82ab56da3ae326be175c9519b5248e53fa02b82f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677204"
---
# <a name="deriving-from-cbasepin"></a><span data-ttu-id="9b646-103">Derivación de CBasePin</span><span class="sxs-lookup"><span data-stu-id="9b646-103">Deriving from CBasePin</span></span>

<span data-ttu-id="9b646-104">Para implementar un PIN mediante [**CBasePin**](cbasepin.md), debe derivar una nueva clase de la clase base e invalidar algunos de sus métodos.</span><span class="sxs-lookup"><span data-stu-id="9b646-104">To implement a pin using [**CBasePin**](cbasepin.md), you must derive a new class from the base class and override several of its methods.</span></span> <span data-ttu-id="9b646-105">Debe invalidar los métodos siguientes:</span><span class="sxs-lookup"><span data-stu-id="9b646-105">You must override the following methods:</span></span>

-   [<span data-ttu-id="9b646-106">**CBasePin::CheckMediaType**</span><span class="sxs-lookup"><span data-stu-id="9b646-106">**CBasePin::CheckMediaType**</span></span>](cbasepin-checkmediatype.md)
-   [<span data-ttu-id="9b646-107">**CBasePin::GetMediaType**</span><span class="sxs-lookup"><span data-stu-id="9b646-107">**CBasePin::GetMediaType**</span></span>](cbasepin-getmediatype.md)

<span data-ttu-id="9b646-108">Probablemente tendrá que invalidar estos métodos adicionales:</span><span class="sxs-lookup"><span data-stu-id="9b646-108">You will probably need to override these additional methods:</span></span>

-   [<span data-ttu-id="9b646-109">**CBasePin:: Active**</span><span class="sxs-lookup"><span data-stu-id="9b646-109">**CBasePin::Active**</span></span>](cbasepin-active.md)
-   [<span data-ttu-id="9b646-110">**CBasePin::BreakConnect**</span><span class="sxs-lookup"><span data-stu-id="9b646-110">**CBasePin::BreakConnect**</span></span>](cbasepin-breakconnect.md)
-   [<span data-ttu-id="9b646-111">**CBasePin::CheckConnect**</span><span class="sxs-lookup"><span data-stu-id="9b646-111">**CBasePin::CheckConnect**</span></span>](cbasepin-checkconnect.md)
-   [<span data-ttu-id="9b646-112">**CBasePin::CompleteConnect**</span><span class="sxs-lookup"><span data-stu-id="9b646-112">**CBasePin::CompleteConnect**</span></span>](cbasepin-completeconnect.md)
-   [<span data-ttu-id="9b646-113">**CBasePin:: EndOfStream**</span><span class="sxs-lookup"><span data-stu-id="9b646-113">**CBasePin::EndOfStream**</span></span>](cbasepin-endofstream.md)
-   [<span data-ttu-id="9b646-114">**CBasePin:: inactivo**</span><span class="sxs-lookup"><span data-stu-id="9b646-114">**CBasePin::Inactive**</span></span>](cbasepin-inactive.md)
-   [<span data-ttu-id="9b646-115">**CBasePin:: Notify**</span><span class="sxs-lookup"><span data-stu-id="9b646-115">**CBasePin::Notify**</span></span>](cbasepin-notify.md)
-   [<span data-ttu-id="9b646-116">**CBasePin:: Run**</span><span class="sxs-lookup"><span data-stu-id="9b646-116">**CBasePin::Run**</span></span>](cbasepin-run.md)

<span data-ttu-id="9b646-117">Por último, debe implementar los métodos [**IPin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) y [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) .</span><span class="sxs-lookup"><span data-stu-id="9b646-117">Finally, you must must implement the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) and [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) methods.</span></span>

<span data-ttu-id="9b646-118">Algunos de estos métodos se implementan en clases base que derivan de **CBasePin**, como [**CBaseInputPin**](cbaseinputpin.md) y [**CBaseOutputPin**](cbaseoutputpin.md).</span><span class="sxs-lookup"><span data-stu-id="9b646-118">Some of these methods are implemented in base classes that derive from **CBasePin**, such as [**CBaseInputPin**](cbaseinputpin.md) and [**CBaseOutputPin**](cbaseoutputpin.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9b646-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9b646-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b646-120">**CBasePin**</span><span class="sxs-lookup"><span data-stu-id="9b646-120">**CBasePin**</span></span>](cbasepin.md)
</dt> </dl>

 

 



