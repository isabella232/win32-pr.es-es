---
description: Esta clase es la clase primaria para los eventos de e/s de archivo. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 8e006a63-a061-4b62-8f90-b8c8823bb047
title: FileIo (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2f7c032cb7af325efa1d2ea76702068fc7b3be62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985086"
---
# <a name="fileio-class"></a><span data-ttu-id="92b80-104">FileIo (clase)</span><span class="sxs-lookup"><span data-stu-id="92b80-104">FileIo class</span></span>

<span data-ttu-id="92b80-105">Esta clase es la clase primaria para los eventos de e/s de archivo.</span><span class="sxs-lookup"><span data-stu-id="92b80-105">This class is the parent class for file I/O events.</span></span>

<span data-ttu-id="92b80-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="92b80-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="92b80-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92b80-107">Syntax</span></span>

``` syntax
[Guid("{90cbdc39-4a3e-11d1-84f4-0000f80464e3}"), EventVersion(2)]
class FileIo : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="92b80-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="92b80-108">Members</span></span>

<span data-ttu-id="92b80-109">La clase **FileIo** no define ningún miembro.</span><span class="sxs-lookup"><span data-stu-id="92b80-109">The **FileIo** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="92b80-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="92b80-110">Remarks</span></span>

<span data-ttu-id="92b80-111">Para habilitar los eventos de e/s de archivo en una sesión de registro del kernel de NT, especifique el indicador de **\_ \_ \_ \_ \_ e/s de archivo de disco de marca de seguimiento de eventos** en el miembro **EnableFlags** de una estructura de [**\_ \_ propiedades de seguimiento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) al llamar a la función [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .</span><span class="sxs-lookup"><span data-stu-id="92b80-111">To enable the File IO events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_DISK\_FILE\_IO** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span> <span data-ttu-id="92b80-112">También puede especificar una o varias de las marcas siguientes:</span><span class="sxs-lookup"><span data-stu-id="92b80-112">You can also specify one or more of the following flags:</span></span>

-   <span data-ttu-id="92b80-113">**\_ \_ \_ e/s de archivo de marca de seguimiento de eventos \_**</span><span class="sxs-lookup"><span data-stu-id="92b80-113">**EVENT\_TRACE\_FLAG\_FILE\_IO**</span></span>
-   <span data-ttu-id="92b80-114">**\_inicial de \_ \_ \_ e/s de archivo de marca de seguimiento de eventos \_**</span><span class="sxs-lookup"><span data-stu-id="92b80-114">**EVENT\_TRACE\_FLAG\_FILE\_IO\_INIT**</span></span>

<span data-ttu-id="92b80-115">Los consumidores de seguimiento de eventos pueden implementar un procesamiento especial para los eventos de e/s de archivos llamando a la función [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) y especificando [**FileIoGuid**](nt-kernel-logger-constants.md) como parámetro *pGuid* .</span><span class="sxs-lookup"><span data-stu-id="92b80-115">Event trace consumers can implement special processing for file I/O events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**FileIoGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="92b80-116">Utilice los siguientes tipos de eventos para identificar el evento real al consumir eventos.</span><span class="sxs-lookup"><span data-stu-id="92b80-116">Use the following event types to identify the actual event when consuming events.</span></span>



| <span data-ttu-id="92b80-117">Tipo de evento</span><span class="sxs-lookup"><span data-stu-id="92b80-117">Event type</span></span>             | <span data-ttu-id="92b80-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="92b80-118">Description</span></span>                                                                                                                                                                             |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92b80-119">El valor del tipo de evento es 0</span><span class="sxs-lookup"><span data-stu-id="92b80-119">Event type value is 0</span></span>  | <span data-ttu-id="92b80-120">Evento de nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="92b80-120">File name event.</span></span> <span data-ttu-id="92b80-121">La clase de MOF [**\_ nombre de FileIo**](fileio-name.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="92b80-121">The [**FileIo\_Name**](fileio-name.md) MOF class defines the event data for this event.</span></span>                                                                               |
| <span data-ttu-id="92b80-122">El valor del tipo de evento es 32</span><span class="sxs-lookup"><span data-stu-id="92b80-122">Event type value is 32</span></span> | <span data-ttu-id="92b80-123">Evento de creación de archivo.</span><span class="sxs-lookup"><span data-stu-id="92b80-123">File create event.</span></span> <span data-ttu-id="92b80-124">La clase de MOF [**\_ nombre de FileIo**](fileio-name.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="92b80-124">The [**FileIo\_Name**](fileio-name.md) MOF class defines the event data for this event.</span></span>                                                                             |
| <span data-ttu-id="92b80-125">El valor del tipo de evento es 35</span><span class="sxs-lookup"><span data-stu-id="92b80-125">Event type value is 35</span></span> | <span data-ttu-id="92b80-126">Evento de eliminación de archivo.</span><span class="sxs-lookup"><span data-stu-id="92b80-126">File delete event.</span></span> <span data-ttu-id="92b80-127">La clase de MOF [**\_ nombre de FileIo**](fileio-name.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="92b80-127">The [**FileIo\_Name**](fileio-name.md) MOF class defines the event data for this event.</span></span>                                                                             |
| <span data-ttu-id="92b80-128">El valor del tipo de evento es 36</span><span class="sxs-lookup"><span data-stu-id="92b80-128">Event type value is 36</span></span> | <span data-ttu-id="92b80-129">Evento de detención de archivo.</span><span class="sxs-lookup"><span data-stu-id="92b80-129">File rundown event.</span></span> <span data-ttu-id="92b80-130">Enumera todos los archivos abiertos en el equipo al final de la sesión de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="92b80-130">Enumerates all open files on the computer at the end of the trace session.</span></span> <span data-ttu-id="92b80-131">La clase de MOF [**\_ nombre de FileIo**](fileio-name.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="92b80-131">The [**FileIo\_Name**](fileio-name.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="92b80-132">El valor del tipo de evento es 64</span><span class="sxs-lookup"><span data-stu-id="92b80-132">Event type value is 64</span></span> | <span data-ttu-id="92b80-133">Evento de creación de archivo.</span><span class="sxs-lookup"><span data-stu-id="92b80-133">File create event.</span></span> <span data-ttu-id="92b80-134">La clase [**FileIo \_ Create**](fileio-create.md) mof define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="92b80-134">The [**FileIo\_Create**](fileio-create.md) MOF class defines the event data for this event.</span></span>                                                                         |
| <span data-ttu-id="92b80-135">El valor del tipo de evento es 72</span><span class="sxs-lookup"><span data-stu-id="92b80-135">Event type value is 72</span></span> | <span data-ttu-id="92b80-136">Evento de enumeración de directorio.</span><span class="sxs-lookup"><span data-stu-id="92b80-136">Directory enumeration event.</span></span> <span data-ttu-id="92b80-137">La clase de MOF [**\_ DirEnum de FileIo**](fileio-direnum.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="92b80-137">The [**FileIo\_DirEnum**](fileio-direnum.md) MOF class defines the event data for this event.</span></span>                                                             |
| <span data-ttu-id="92b80-138">El valor del tipo de evento es 77</span><span class="sxs-lookup"><span data-stu-id="92b80-138">Event type value is 77</span></span> | <span data-ttu-id="92b80-139">Evento de notificación de directorio.</span><span class="sxs-lookup"><span data-stu-id="92b80-139">Directory notification event.</span></span> <span data-ttu-id="92b80-140">La clase de MOF [**\_ DirEnum de FileIo**](fileio-direnum.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="92b80-140">The [**FileIo\_DirEnum**](fileio-direnum.md) MOF class defines the event data for this event.</span></span>                                                            |
| <span data-ttu-id="92b80-141">El valor del tipo de evento es 69</span><span class="sxs-lookup"><span data-stu-id="92b80-141">Event type value is 69</span></span> | <span data-ttu-id="92b80-142">Evento de información de conjunto.</span><span class="sxs-lookup"><span data-stu-id="92b80-142">Set information event.</span></span> <span data-ttu-id="92b80-143">La clase de MOF [**\_ info**](fileio-info.md) de la clase define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="92b80-143">The [**FileIo\_Info**](fileio-info.md) MOF class defines the event data for this event.</span></span>                                                                         |
| <span data-ttu-id="92b80-144">El valor del tipo de evento es 70</span><span class="sxs-lookup"><span data-stu-id="92b80-144">Event type value is 70</span></span> | <span data-ttu-id="92b80-145">Evento de eliminación de archivo.</span><span class="sxs-lookup"><span data-stu-id="92b80-145">Delete file event.</span></span> <span data-ttu-id="92b80-146">La clase de MOF [**\_ info**](fileio-info.md) de la clase define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="92b80-146">The [**FileIo\_Info**](fileio-info.md) MOF class defines the event data for this event.</span></span>                                                                             |
| <span data-ttu-id="92b80-147">El valor del tipo de evento es 71</span><span class="sxs-lookup"><span data-stu-id="92b80-147">Event type value is 71</span></span> | <span data-ttu-id="92b80-148">Evento de cambio de nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="92b80-148">Rename file event.</span></span> <span data-ttu-id="92b80-149">La clase de MOF [**\_ info**](fileio-info.md) de la clase define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="92b80-149">The [**FileIo\_Info**](fileio-info.md) MOF class defines the event data for this event.</span></span>                                                                             |
| <span data-ttu-id="92b80-150">El valor del tipo de evento es 74</span><span class="sxs-lookup"><span data-stu-id="92b80-150">Event type value is 74</span></span> | <span data-ttu-id="92b80-151">Evento de información de archivo de consulta.</span><span class="sxs-lookup"><span data-stu-id="92b80-151">Query file information event.</span></span> <span data-ttu-id="92b80-152">La clase de MOF [**\_ info**](fileio-info.md) de la clase define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="92b80-152">The [**FileIo\_Info**](fileio-info.md) MOF class defines the event data for this event.</span></span>                                                                  |
| <span data-ttu-id="92b80-153">El valor del tipo de evento es 75</span><span class="sxs-lookup"><span data-stu-id="92b80-153">Event type value is 75</span></span> | <span data-ttu-id="92b80-154">Evento de control del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="92b80-154">File system control event.</span></span> <span data-ttu-id="92b80-155">La clase de MOF [**\_ info**](fileio-info.md) de la clase define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="92b80-155">The [**FileIo\_Info**](fileio-info.md) MOF class defines the event data for this event.</span></span>                                                                     |
| <span data-ttu-id="92b80-156">El valor del tipo de evento es 76</span><span class="sxs-lookup"><span data-stu-id="92b80-156">Event type value is 76</span></span> | <span data-ttu-id="92b80-157">Evento de fin de operación.</span><span class="sxs-lookup"><span data-stu-id="92b80-157">End of operation event.</span></span> <span data-ttu-id="92b80-158">La clase MOF [**\_ abierta en FileIo**](fileio-opend.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="92b80-158">The [**FileIo\_OpEnd**](fileio-opend.md) MOF class defines the event data for this event.</span></span>                                                                      |
| <span data-ttu-id="92b80-159">El valor del tipo de evento es 67</span><span class="sxs-lookup"><span data-stu-id="92b80-159">Event type value is 67</span></span> | <span data-ttu-id="92b80-160">Evento de lectura de archivo.</span><span class="sxs-lookup"><span data-stu-id="92b80-160">File read event.</span></span> <span data-ttu-id="92b80-161">La clase de MOF [**\_ ReadWrite ReadWrite**](fileio-readwrite.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="92b80-161">The [**FileIo\_ReadWrite**](fileio-readwrite.md) MOF class defines the event data for this event.</span></span>                                                                     |
| <span data-ttu-id="92b80-162">El valor del tipo de evento es 68</span><span class="sxs-lookup"><span data-stu-id="92b80-162">Event type value is 68</span></span> | <span data-ttu-id="92b80-163">Evento de escritura de archivo.</span><span class="sxs-lookup"><span data-stu-id="92b80-163">File write event.</span></span> <span data-ttu-id="92b80-164">La clase de MOF [**\_ ReadWrite ReadWrite**](fileio-readwrite.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="92b80-164">The [**FileIo\_ReadWrite**](fileio-readwrite.md) MOF class defines the event data for this event.</span></span>                                                                    |
| <span data-ttu-id="92b80-165">El valor del tipo de evento es 65</span><span class="sxs-lookup"><span data-stu-id="92b80-165">Event type value is 65</span></span> | <span data-ttu-id="92b80-166">Evento de limpieza.</span><span class="sxs-lookup"><span data-stu-id="92b80-166">Clean up event.</span></span> <span data-ttu-id="92b80-167">El evento se genera cuando se libera el último identificador del archivo.</span><span class="sxs-lookup"><span data-stu-id="92b80-167">The event is generated when the last handle to the file is released.</span></span> <span data-ttu-id="92b80-168">La clase de MOF [**\_ SimpleOp de FileIo**](fileio-simpleop.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="92b80-168">The [**FileIo\_SimpleOp**](fileio-simpleop.md) MOF class defines the event data for this event.</span></span>   |
| <span data-ttu-id="92b80-169">El valor del tipo de evento es 66</span><span class="sxs-lookup"><span data-stu-id="92b80-169">Event type value is 66</span></span> | <span data-ttu-id="92b80-170">Evento de cierre.</span><span class="sxs-lookup"><span data-stu-id="92b80-170">Close event.</span></span> <span data-ttu-id="92b80-171">El evento se genera cuando se libera el objeto de archivo.</span><span class="sxs-lookup"><span data-stu-id="92b80-171">The event is generated when the file object is freed.</span></span> <span data-ttu-id="92b80-172">La clase de MOF [**\_ SimpleOp de FileIo**](fileio-simpleop.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="92b80-172">The [**FileIo\_SimpleOp**](fileio-simpleop.md) MOF class defines the event data for this event.</span></span>                     |
| <span data-ttu-id="92b80-173">El valor del tipo de evento es 73</span><span class="sxs-lookup"><span data-stu-id="92b80-173">Event type value is 73</span></span> | <span data-ttu-id="92b80-174">Evento de vaciado.</span><span class="sxs-lookup"><span data-stu-id="92b80-174">Flush event.</span></span> <span data-ttu-id="92b80-175">Este evento se genera cuando los búferes de archivo se vacían por completo en el disco.</span><span class="sxs-lookup"><span data-stu-id="92b80-175">This event is generated when the file buffers are fully flushed to disk.</span></span> <span data-ttu-id="92b80-176">La clase de MOF [**\_ SimpleOp de FileIo**](fileio-simpleop.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="92b80-176">The [**FileIo\_SimpleOp**](fileio-simpleop.md) MOF class defines the event data for this event.</span></span>  |



 

<span data-ttu-id="92b80-177">Los eventos de e/s de archivos se registran al principio de la operación.</span><span class="sxs-lookup"><span data-stu-id="92b80-177">File IO events are logged at the beginning of the operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="92b80-178">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92b80-178">Requirements</span></span>



| <span data-ttu-id="92b80-179">Requisito</span><span class="sxs-lookup"><span data-stu-id="92b80-179">Requirement</span></span> | <span data-ttu-id="92b80-180">Value</span><span class="sxs-lookup"><span data-stu-id="92b80-180">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="92b80-181">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="92b80-181">Minimum supported client</span></span><br/> | <span data-ttu-id="92b80-182">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="92b80-182">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="92b80-183">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="92b80-183">Minimum supported server</span></span><br/> | <span data-ttu-id="92b80-184">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="92b80-184">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="92b80-185">Vea también</span><span class="sxs-lookup"><span data-stu-id="92b80-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92b80-186">**MSNT \_ SystemTrace**</span><span class="sxs-lookup"><span data-stu-id="92b80-186">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="92b80-187">**FileIo \_ v0**</span><span class="sxs-lookup"><span data-stu-id="92b80-187">**FileIo\_V0**</span></span>](fileio-v0.md)
</dt> <dt>

[<span data-ttu-id="92b80-188">**FileIo \_ v1**</span><span class="sxs-lookup"><span data-stu-id="92b80-188">**FileIo\_V1**</span></span>](fileio-v1.md)
</dt> </dl>

 

 
