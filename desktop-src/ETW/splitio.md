---
description: Esta clase es la clase primaria para los eventos de e/s divididos. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: d65c5180-6f1a-45cc-bca8-eac13857d383
title: Clase SplitIo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SplitIo
api_type:
- NA
api_location: ''
ms.openlocfilehash: f2efc14ce8804852f983ebe9dcb852c8c0669899
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985082"
---
# <a name="splitio-class"></a><span data-ttu-id="97fdd-104">Clase SplitIo</span><span class="sxs-lookup"><span data-stu-id="97fdd-104">SplitIo class</span></span>

<span data-ttu-id="97fdd-105">Esta clase es la clase primaria para los eventos de e/s divididos.</span><span class="sxs-lookup"><span data-stu-id="97fdd-105">This class is the parent class for split IO events.</span></span>

<span data-ttu-id="97fdd-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="97fdd-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="97fdd-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="97fdd-107">Syntax</span></span>

``` syntax
[Guid("{d837ca92-12b9-44a5-ad6a-3a65b3578aa8}")]
class SplitIo : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="97fdd-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="97fdd-108">Members</span></span>

<span data-ttu-id="97fdd-109">La clase **SplitIo** no define ningún miembro.</span><span class="sxs-lookup"><span data-stu-id="97fdd-109">The **SplitIo** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="97fdd-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="97fdd-110">Remarks</span></span>

<span data-ttu-id="97fdd-111">Para habilitar los eventos de e/s divididos en una sesión de registro del kernel de NT, especifique la marca de la **marca de seguimiento de eventos \_ Split de \_ \_ \_ e/s** en el miembro **EnableFlags** de una estructura de [**propiedades de \_ seguimiento \_ de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) al llamar a la función [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .</span><span class="sxs-lookup"><span data-stu-id="97fdd-111">To enable split IO events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_SPLIT\_IO** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span>

<span data-ttu-id="97fdd-112">Los consumidores de seguimiento de eventos pueden implementar un procesamiento especial para los eventos de e/s dividida llamando a la función [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) y especificando [**SplitIoGuid**](nt-kernel-logger-constants.md) como parámetro *pGuid* .</span><span class="sxs-lookup"><span data-stu-id="97fdd-112">Event trace consumers can implement special processing for split IO events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**SplitIoGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="97fdd-113">Use el siguiente tipo de evento para identificar el evento real al consumir eventos.</span><span class="sxs-lookup"><span data-stu-id="97fdd-113">Use the following event type to identify the actual event when consuming events.</span></span>



| <span data-ttu-id="97fdd-114">Tipo de evento</span><span class="sxs-lookup"><span data-stu-id="97fdd-114">Event type</span></span>           | <span data-ttu-id="97fdd-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="97fdd-115">Description</span></span>                                                                                                |
|----------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97fdd-116">Valor del tipo de evento, 32</span><span class="sxs-lookup"><span data-stu-id="97fdd-116">Event type value, 32</span></span> | <span data-ttu-id="97fdd-117">Evento de e/s dividido.</span><span class="sxs-lookup"><span data-stu-id="97fdd-117">Split IO event.</span></span> <span data-ttu-id="97fdd-118">La clase MOF [**SplitIo \_ info**](splitio-info.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="97fdd-118">The [**SplitIo\_Info**](splitio-info.md) MOF class defines the event data for this event.</span></span> |



 

<span data-ttu-id="97fdd-119">Los eventos de e/s divididos indican que las solicitudes de e/s se han dividido en varias solicitudes de e/s de disco debido al hardware del disco de creación de reflejo subyacente.</span><span class="sxs-lookup"><span data-stu-id="97fdd-119">Split IO events indicate that the IO requests have been split into multiple disk IO requests due to the underlying mirroring disk hardware.</span></span>

## <a name="requirements"></a><span data-ttu-id="97fdd-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="97fdd-120">Requirements</span></span>



| <span data-ttu-id="97fdd-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="97fdd-121">Requirement</span></span> | <span data-ttu-id="97fdd-122">Value</span><span class="sxs-lookup"><span data-stu-id="97fdd-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="97fdd-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="97fdd-123">Minimum supported client</span></span><br/> | <span data-ttu-id="97fdd-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="97fdd-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="97fdd-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="97fdd-125">Minimum supported server</span></span><br/> | <span data-ttu-id="97fdd-126">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="97fdd-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 
