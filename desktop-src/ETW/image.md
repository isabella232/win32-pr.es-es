---
description: Esta clase es la clase primaria para los eventos de imagen. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: a719a34c-7e32-4758-9031-6ca2b2873e3e
title: Clase Image
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Image
api_type:
- NA
api_location: ''
ms.openlocfilehash: 47280a81b882f91ad71c6cd91004d1c0885afddf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985595"
---
# <a name="image-class"></a><span data-ttu-id="e1dea-104">Clase Image</span><span class="sxs-lookup"><span data-stu-id="e1dea-104">Image class</span></span>

<span data-ttu-id="e1dea-105">Esta clase es la clase primaria para los eventos de imagen.</span><span class="sxs-lookup"><span data-stu-id="e1dea-105">This class is the parent class for image events.</span></span>

<span data-ttu-id="e1dea-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="e1dea-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1dea-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e1dea-107">Syntax</span></span>

``` syntax
[Guid("{2cb15d1d-5fc1-11d2-abe1-00a0c911f518}"), EventVersion(2)]
class Image : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="e1dea-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="e1dea-108">Members</span></span>

<span data-ttu-id="e1dea-109">La clase **Image** no define ningún miembro.</span><span class="sxs-lookup"><span data-stu-id="e1dea-109">The **Image** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1dea-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e1dea-110">Remarks</span></span>

<span data-ttu-id="e1dea-111">Para habilitar los eventos de imagen en una sesión de registro del kernel de NT, especifique la marca de carga  de la imagen de la marca de seguimiento de **eventos \_ \_ \_ \_** en el miembro EnableFlags de la estructura de [**propiedades de \_ seguimiento \_ de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) al llamar a la función [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .</span><span class="sxs-lookup"><span data-stu-id="e1dea-111">To enable image events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_IMAGE\_LOAD** flag in the **EnableFlags** member of the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span>

<span data-ttu-id="e1dea-112">Los consumidores de seguimiento de eventos pueden implementar un procesamiento especial para los eventos de carga de imágenes mediante una llamada a la función [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) y especificando [**ImageLoadGuid**](nt-kernel-logger-constants.md) como parámetro *pGuid* .</span><span class="sxs-lookup"><span data-stu-id="e1dea-112">Event trace consumers can implement special processing for image load events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**ImageLoadGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="e1dea-113">Utilice los siguientes tipos de eventos para identificar los eventos de carga de imágenes al consumir eventos.</span><span class="sxs-lookup"><span data-stu-id="e1dea-113">Use the following event types to identify image load events when consuming events.</span></span>



| <span data-ttu-id="e1dea-114">Tipo de evento</span><span class="sxs-lookup"><span data-stu-id="e1dea-114">Event type</span></span>                                                          | <span data-ttu-id="e1dea-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="e1dea-115">Description</span></span>                                                                                                                                                                                                                                      |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1dea-116">**Evento \_ de \_ \_ Carga del tipo de seguimiento**(el valor del tipo de evento es 10)</span><span class="sxs-lookup"><span data-stu-id="e1dea-116">**EVENT\_TRACE\_TYPE\_LOAD**(Event type value is 10)</span></span><br/>     | <span data-ttu-id="e1dea-117">Evento de carga de imagen.</span><span class="sxs-lookup"><span data-stu-id="e1dea-117">Image load event.</span></span> <span data-ttu-id="e1dea-118">Se genera cuando se carga un archivo ejecutable o DLL.</span><span class="sxs-lookup"><span data-stu-id="e1dea-118">Generated when a DLL or executable file is loaded.</span></span> <span data-ttu-id="e1dea-119">El proveedor solo genera un evento por primera vez que se carga un archivo DLL determinado.</span><span class="sxs-lookup"><span data-stu-id="e1dea-119">The provider generates only one event for the first time a given DLL is loaded.</span></span> <span data-ttu-id="e1dea-120">La clase MOF de [**\_ carga de imagen**](image-load.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="e1dea-120">The [**Image\_Load**](image-load.md) MOF class defines the event data for this event.</span></span>      |
| <span data-ttu-id="e1dea-121">**Evento \_ de Tipo de seguimiento \_ \_ End**(el valor de tipo de evento es 2)</span><span class="sxs-lookup"><span data-stu-id="e1dea-121">**EVENT\_TRACE\_TYPE\_END**(Event type value is 2)</span></span><br/>       | <span data-ttu-id="e1dea-122">Evento de descarga de imagen.</span><span class="sxs-lookup"><span data-stu-id="e1dea-122">Image unload event.</span></span> <span data-ttu-id="e1dea-123">Se genera cuando se descarga un archivo ejecutable o DLL.</span><span class="sxs-lookup"><span data-stu-id="e1dea-123">Generated when a DLL or executable file is unloaded.</span></span> <span data-ttu-id="e1dea-124">El proveedor solo genera un evento por la última vez que se descarga un archivo DLL determinado.</span><span class="sxs-lookup"><span data-stu-id="e1dea-124">The provider generates only one event for the last time a given DLL is unloaded.</span></span> <span data-ttu-id="e1dea-125">La clase MOF de [**\_ carga de imagen**](image-load.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="e1dea-125">The [**Image\_Load**](image-load.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="e1dea-126">**Evento \_ de Tipo de seguimiento \_ \_ DC \_ Start**(el valor de tipo de evento es 3)</span><span class="sxs-lookup"><span data-stu-id="e1dea-126">**EVENT\_TRACE\_TYPE\_DC\_START**(Event type value is 3)</span></span><br/> | <span data-ttu-id="e1dea-127">Evento de inicio de recopilación de datos.</span><span class="sxs-lookup"><span data-stu-id="e1dea-127">Data collection start event.</span></span> <span data-ttu-id="e1dea-128">Enumera todas las imágenes cargadas al principio del seguimiento.</span><span class="sxs-lookup"><span data-stu-id="e1dea-128">Enumerates all loaded images at the beginning of the trace.</span></span> <span data-ttu-id="e1dea-129">La clase MOF de [**\_ carga de imagen**](image-load.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="e1dea-129">The [**Image\_Load**](image-load.md) MOF class defines the event data for this event.</span></span>                                                                  |
| <span data-ttu-id="e1dea-130">**Evento \_ de Tipo de seguimiento \_ \_ DC \_ End**(el valor del tipo de evento es 4)</span><span class="sxs-lookup"><span data-stu-id="e1dea-130">**EVENT\_TRACE\_TYPE\_DC\_END**(Event type value is 4)</span></span><br/>   | <span data-ttu-id="e1dea-131">Evento de finalización de recopilación de datos.</span><span class="sxs-lookup"><span data-stu-id="e1dea-131">Data collection end event.</span></span> <span data-ttu-id="e1dea-132">Enumera todas las imágenes cargadas al final del seguimiento.</span><span class="sxs-lookup"><span data-stu-id="e1dea-132">Enumerates all loaded images at the end of the trace.</span></span> <span data-ttu-id="e1dea-133">La clase MOF de [**\_ carga de imagen**](image-load.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="e1dea-133">The [**Image\_Load**](image-load.md) MOF class defines the event data for this event.</span></span>                                                                          |



 

## <a name="requirements"></a><span data-ttu-id="e1dea-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1dea-134">Requirements</span></span>



| <span data-ttu-id="e1dea-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1dea-135">Requirement</span></span> | <span data-ttu-id="e1dea-136">Value</span><span class="sxs-lookup"><span data-stu-id="e1dea-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e1dea-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e1dea-137">Minimum supported client</span></span><br/> | <span data-ttu-id="e1dea-138">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e1dea-138">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e1dea-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e1dea-139">Minimum supported server</span></span><br/> | <span data-ttu-id="e1dea-140">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e1dea-140">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e1dea-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="e1dea-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1dea-142">**MSNT \_ SystemTrace**</span><span class="sxs-lookup"><span data-stu-id="e1dea-142">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="e1dea-143">**Carga de imágenes \_**</span><span class="sxs-lookup"><span data-stu-id="e1dea-143">**Image\_Load**</span></span>](image-load.md)
</dt> <dt>

[<span data-ttu-id="e1dea-144">**Imagen \_ v0**</span><span class="sxs-lookup"><span data-stu-id="e1dea-144">**Image\_V0**</span></span>](image-v0.md)
</dt> <dt>

[<span data-ttu-id="e1dea-145">**Imagen \_ v1**</span><span class="sxs-lookup"><span data-stu-id="e1dea-145">**Image\_V1**</span></span>](image-v1.md)
</dt> </dl>

 

 
