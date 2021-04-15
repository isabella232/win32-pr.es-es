---
description: Esta clase es la clase primaria para los eventos de seguimiento de la pila.
ms.assetid: 3c0ff01b-fb37-4931-9484-ff8048abca66
title: Clase StackWalk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StackWalk
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2ad873815cb5cea40c1a9d2f694eca8d0e90d11b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984471"
---
# <a name="stackwalk-class"></a><span data-ttu-id="d424c-103">Clase StackWalk</span><span class="sxs-lookup"><span data-stu-id="d424c-103">StackWalk class</span></span>

<span data-ttu-id="d424c-104">Esta clase es la clase primaria para los eventos de seguimiento de la pila.</span><span class="sxs-lookup"><span data-stu-id="d424c-104">This class is the parent class for stack tracing events.</span></span>

<span data-ttu-id="d424c-105">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="d424c-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d424c-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d424c-106">Syntax</span></span>

``` syntax
[Guid("{def2fe46-7bd6-4b80-bd94-f57fe20d0ce3}")]
class StackWalk : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="d424c-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="d424c-107">Members</span></span>

<span data-ttu-id="d424c-108">La clase **StackWalk** no define ningún miembro.</span><span class="sxs-lookup"><span data-stu-id="d424c-108">The **StackWalk** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="d424c-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d424c-109">Remarks</span></span>

<span data-ttu-id="d424c-110">Para habilitar el seguimiento de la pila de los eventos de kernel, llame a la función [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) y especifique los eventos y tipos de kernel para los que desea capturar el seguimiento de la pila.</span><span class="sxs-lookup"><span data-stu-id="d424c-110">To enable stack tracing of kernel events, call the [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) function and specify the kernel events and types for which you want to capture the stack trace.</span></span> <span data-ttu-id="d424c-111">Para habilitar el seguimiento de la pila para otros eventos, establezca el miembro **EnableProperty** de [**habilitar \_ \_ parámetros de seguimiento**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) en **evento \_ habilitar \_ \_ \_ seguimiento** de la pila de propiedades.</span><span class="sxs-lookup"><span data-stu-id="d424c-111">To enable stack tracing for other events, set the **EnableProperty** member of [**ENABLE\_TRACE\_PARAMETERS**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) to **EVENT\_ENABLE\_PROPERTY\_STACK\_TRACE**.</span></span>

<span data-ttu-id="d424c-112">Use el siguiente tipo de evento para identificar el evento real al consumir eventos.</span><span class="sxs-lookup"><span data-stu-id="d424c-112">Use the following event type to identify the actual event when consuming events.</span></span>



| <span data-ttu-id="d424c-113">Tipo de evento</span><span class="sxs-lookup"><span data-stu-id="d424c-113">Event type</span></span>           | <span data-ttu-id="d424c-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="d424c-114">Description</span></span>                                                                                                           |
|----------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d424c-115">Valor del tipo de evento, 32</span><span class="sxs-lookup"><span data-stu-id="d424c-115">Event type value, 32</span></span> | <span data-ttu-id="d424c-116">Evento de seguimiento de la pila.</span><span class="sxs-lookup"><span data-stu-id="d424c-116">Stack tracing event.</span></span> <span data-ttu-id="d424c-117">La clase MOF del [**\_ evento StackWalk**](stackwalk-event.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="d424c-117">The [**StackWalk\_Event**](stackwalk-event.md) MOF class defines the event data for this event.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="d424c-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d424c-118">Requirements</span></span>



| <span data-ttu-id="d424c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d424c-119">Requirement</span></span> | <span data-ttu-id="d424c-120">Value</span><span class="sxs-lookup"><span data-stu-id="d424c-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="d424c-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d424c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d424c-122">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="d424c-122">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="d424c-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d424c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d424c-124">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="d424c-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 
