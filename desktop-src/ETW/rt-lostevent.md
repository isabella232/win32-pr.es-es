---
description: Esta clase de tipo de evento se usa para indicar que los eventos se han perdido en una sesión en tiempo real. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 19c747c0-2d9f-49c5-81e4-06a870371bac
title: RT_LostEvent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RT_LostEvent
api_type:
- NA
api_location: ''
ms.openlocfilehash: b689dd95aa1e078572d33de64f245e4844698d5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541870"
---
# <a name="rt_lostevent-class"></a><span data-ttu-id="8917f-104">RT \_ LostEvent (clase)</span><span class="sxs-lookup"><span data-stu-id="8917f-104">RT\_LostEvent class</span></span>

<span data-ttu-id="8917f-105">Esta clase de tipo de evento se usa para indicar que los eventos se han perdido en una sesión en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="8917f-105">This event type class is used to indicate that events were lost in a real-time session.</span></span>

<span data-ttu-id="8917f-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="8917f-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="8917f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8917f-107">Syntax</span></span>

``` syntax
[EventType{32, 33, 34}, EventTypeName{"RTLostEvent", "RTLostBuffer", "RTLostFile"}]
class RT_LostEvent : Lost_Event
{
};
```

## <a name="members"></a><span data-ttu-id="8917f-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="8917f-108">Members</span></span>

<span data-ttu-id="8917f-109">La clase **RT \_ LostEvent** no define ningún miembro.</span><span class="sxs-lookup"><span data-stu-id="8917f-109">The **RT\_LostEvent** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="8917f-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8917f-110">Remarks</span></span>

<span data-ttu-id="8917f-111">El tipo de evento RTLostEvent indica que se han perdido uno o varios eventos.</span><span class="sxs-lookup"><span data-stu-id="8917f-111">The RTLostEvent event type indicates that one or more events were lost.</span></span> <span data-ttu-id="8917f-112">El tipo de evento RTLostBuffer indica que se han perdido uno o más búferes.</span><span class="sxs-lookup"><span data-stu-id="8917f-112">The RTLostBuffer event type indicates that one or more buffers were lost.</span></span> <span data-ttu-id="8917f-113">Los tipos de eventos RTLostEvent y RTLostBuffer se entregan antes de procesar los eventos del búfer.</span><span class="sxs-lookup"><span data-stu-id="8917f-113">The RTLostEvent and RTLostBuffer event types are delivered before processing events from the buffer.</span></span>

<span data-ttu-id="8917f-114">RTLostFile indica que se perdió el archivo de copia de seguridad utilizado por el registrador automático para capturar eventos.</span><span class="sxs-lookup"><span data-stu-id="8917f-114">The RTLostFile indicates that the backing file used by the AutoLogger to capture events was lost.</span></span>

<span data-ttu-id="8917f-115">Perder eventos depende de la frecuencia con la que se registran los eventos y de cuánto tiempo dedica el consumidor a procesar los eventos.</span><span class="sxs-lookup"><span data-stu-id="8917f-115">Loosing events depends on the frequency with which the events are logged and how much time the consumer spends processing the events.</span></span>

## <a name="requirements"></a><span data-ttu-id="8917f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8917f-116">Requirements</span></span>



| <span data-ttu-id="8917f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="8917f-117">Requirement</span></span> | <span data-ttu-id="8917f-118">Value</span><span class="sxs-lookup"><span data-stu-id="8917f-118">Value</span></span> |
|-------------------------------------|------------------------------------------------|
| <span data-ttu-id="8917f-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8917f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8917f-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8917f-120">Windows Vista \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="8917f-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8917f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8917f-122">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="8917f-122">None supported</span></span><br/>                      |



## <a name="see-also"></a><span data-ttu-id="8917f-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="8917f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8917f-124">**\_Evento perdido**</span><span class="sxs-lookup"><span data-stu-id="8917f-124">**Lost\_Event**</span></span>](lost-event.md)
</dt> </dl>

 

 




