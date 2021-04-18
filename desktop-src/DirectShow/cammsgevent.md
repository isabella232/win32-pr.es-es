---
description: La clase CAMMsgEvent es un contenedor para los objetos de evento que realizan el procesamiento de mensajes.
ms.assetid: 4b94febe-169f-4f04-be93-043a8c75e3b4
title: Clase CAMMsgEvent (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMMsgEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4ebac7aae11f7a7b7d6b846e262e93b5759210b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671051"
---
# <a name="cammsgevent-class"></a><span data-ttu-id="32a27-103">Clase CAMMsgEvent</span><span class="sxs-lookup"><span data-stu-id="32a27-103">CAMMsgEvent class</span></span>

![jerarquía de clases cammsgevent](images/util06.png)

<span data-ttu-id="32a27-105">La `CAMMsgEvent` clase es un contenedor para los objetos de evento que realizan el procesamiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="32a27-105">The `CAMMsgEvent` class is a wrapper for event objects that perform message processing.</span></span>

<span data-ttu-id="32a27-106">Esta clase se deriva del objeto [**CAMEvent**](camevent.md) .</span><span class="sxs-lookup"><span data-stu-id="32a27-106">This class derives from the [**CAMEvent**](camevent.md) object.</span></span> <span data-ttu-id="32a27-107">Agrega un método, [**CAMMsgEvent:: WaitMsg**](cammsgevent-waitmsg.md), que envía los mensajes entrantes mientras se espera.</span><span class="sxs-lookup"><span data-stu-id="32a27-107">It adds one method, [**CAMMsgEvent::WaitMsg**](cammsgevent-waitmsg.md), which dispatches incoming messages while waiting.</span></span>



| <span data-ttu-id="32a27-108">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="32a27-108">Public Methods</span></span>                                 | <span data-ttu-id="32a27-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="32a27-109">Description</span></span>                                                          |
|------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="32a27-110">**CAMMsgEvent**</span><span class="sxs-lookup"><span data-stu-id="32a27-110">**CAMMsgEvent**</span></span>](cammsgevent-cammsgevent.md) | <span data-ttu-id="32a27-111">Constructor.</span><span class="sxs-lookup"><span data-stu-id="32a27-111">Constructor.</span></span>                                                         |
| [<span data-ttu-id="32a27-112">**WaitMsg**</span><span class="sxs-lookup"><span data-stu-id="32a27-112">**WaitMsg**</span></span>](cammsgevent-waitmsg.md)         | <span data-ttu-id="32a27-113">Espera a que se señale el evento y envía los mensajes enviados.</span><span class="sxs-lookup"><span data-stu-id="32a27-113">Waits for the event to be signaled, while dispatching sent messages.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="32a27-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32a27-114">Requirements</span></span>



| <span data-ttu-id="32a27-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="32a27-115">Requirement</span></span> | <span data-ttu-id="32a27-116">Value</span><span class="sxs-lookup"><span data-stu-id="32a27-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32a27-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="32a27-117">Header</span></span><br/>  | <dl> <span data-ttu-id="32a27-118"><dt>Wxutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="32a27-118"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="32a27-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="32a27-119">Library</span></span><br/> | <dl> <span data-ttu-id="32a27-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="32a27-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




