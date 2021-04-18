---
description: Clase primaria para los eventos de encabezado de registro. Esta clase siempre es la primera clase de seguimiento de eventos que se envía a un consumidor (este evento no se envía a los consumidores en tiempo real). La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: fb507d9a-6ed2-4cb1-8cea-85c0a3832e51
title: Clase EventTraceEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EventTraceEvent
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0036ee0a49225568aac066735824fe55ce8f0fa6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984495"
---
# <a name="eventtraceevent-class"></a><span data-ttu-id="37824-105">Clase EventTraceEvent</span><span class="sxs-lookup"><span data-stu-id="37824-105">EventTraceEvent class</span></span>

<span data-ttu-id="37824-106">Clase primaria para los eventos de encabezado de registro.</span><span class="sxs-lookup"><span data-stu-id="37824-106">The parent class for log header events.</span></span> <span data-ttu-id="37824-107">Esta clase siempre es la primera clase de seguimiento de eventos que se envía a un consumidor (este evento no se envía a los consumidores en tiempo real).</span><span class="sxs-lookup"><span data-stu-id="37824-107">This class is always the first event trace class sent to a consumer (this event is not sent to real-time consumers).</span></span>

<span data-ttu-id="37824-108">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="37824-108">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="37824-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="37824-109">Syntax</span></span>

``` syntax
[Guid("{68fdd900-4a3e-11d1-84f4-0000f80464e3}")]
class EventTraceEvent : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="37824-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="37824-110">Members</span></span>

<span data-ttu-id="37824-111">La clase **EventTraceEvent** no define ningún miembro.</span><span class="sxs-lookup"><span data-stu-id="37824-111">The **EventTraceEvent** class does not define any members.</span></span>

## <a name="requirements"></a><span data-ttu-id="37824-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37824-112">Requirements</span></span>



| <span data-ttu-id="37824-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="37824-113">Requirement</span></span> | <span data-ttu-id="37824-114">Value</span><span class="sxs-lookup"><span data-stu-id="37824-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="37824-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="37824-115">Minimum supported client</span></span><br/> | <span data-ttu-id="37824-116">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="37824-116">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="37824-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="37824-117">Minimum supported server</span></span><br/> | <span data-ttu-id="37824-118">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="37824-118">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="37824-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="37824-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37824-120">**MSNT \_ SystemTrace**</span><span class="sxs-lookup"><span data-stu-id="37824-120">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="37824-121">**\_Encabezado eventtracer**</span><span class="sxs-lookup"><span data-stu-id="37824-121">**EventTrace\_Header**</span></span>](eventtrace-header.md)
</dt> </dl>

 

 




