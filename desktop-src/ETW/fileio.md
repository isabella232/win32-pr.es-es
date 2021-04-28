---
description: 'Clase FileIo: esta clase es la clase primaria para los eventos de E/S de archivo. La sintaxis siguiente se simplifica a partir del código MOF.'
ms.assetid: 8e006a63-a061-4b62-8f90-b8c8823bb047
title: Clase FileIo
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
ms.openlocfilehash: 716528902a115e23eae5b49ef572b87a71d11e25
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106533"
---
# <a name="fileio-class"></a><span data-ttu-id="0f856-104">Clase FileIo</span><span class="sxs-lookup"><span data-stu-id="0f856-104">FileIo class</span></span>

<span data-ttu-id="0f856-105">Esta clase es la clase primaria para los eventos de E/S de archivo.</span><span class="sxs-lookup"><span data-stu-id="0f856-105">This class is the parent class for file I/O events.</span></span>

<span data-ttu-id="0f856-106">La sintaxis siguiente se simplifica a partir del código MOF.</span><span class="sxs-lookup"><span data-stu-id="0f856-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f856-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0f856-107">Syntax</span></span>

``` syntax
[Guid("{90cbdc39-4a3e-11d1-84f4-0000f80464e3}"), EventVersion(2)]
class FileIo : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="0f856-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="0f856-108">Members</span></span>

<span data-ttu-id="0f856-109">La **clase FileIo** no define ningún miembro.</span><span class="sxs-lookup"><span data-stu-id="0f856-109">The **FileIo** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f856-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0f856-110">Remarks</span></span>

<span data-ttu-id="0f856-111">Para habilitar los eventos de E/S de archivo en una sesión de registro del kernel de NT, especifique la marca **EVENT TRACE FLAG DISK FILE \_ \_ \_ \_ \_ IO** en el miembro **EnableFlags** de una estructura [**EVENT TRACE \_ \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) al llamar a la [**función StartTrace.**](/windows/win32/api/evntrace/nf-evntrace-starttracea)</span><span class="sxs-lookup"><span data-stu-id="0f856-111">To enable the File IO events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_DISK\_FILE\_IO** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span> <span data-ttu-id="0f856-112">También puede especificar una o varias de las marcas siguientes:</span><span class="sxs-lookup"><span data-stu-id="0f856-112">You can also specify one or more of the following flags:</span></span>

-   <span data-ttu-id="0f856-113">**\_E/S DE ARCHIVO DE MARCA DE SEGUIMIENTO DE \_ \_ \_ EVENTOS**</span><span class="sxs-lookup"><span data-stu-id="0f856-113">**EVENT\_TRACE\_FLAG\_FILE\_IO**</span></span>
-   <span data-ttu-id="0f856-114">**EVENT \_ TRACE \_ FLAG \_ FILE \_ IO \_ INIT**</span><span class="sxs-lookup"><span data-stu-id="0f856-114">**EVENT\_TRACE\_FLAG\_FILE\_IO\_INIT**</span></span>

<span data-ttu-id="0f856-115">Los consumidores de seguimiento de eventos pueden implementar un procesamiento especial para eventos de E/S de archivos llamando a la función [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) y [**especificando FileIoGuid**](nt-kernel-logger-constants.md) como parámetro *pGuid.*</span><span class="sxs-lookup"><span data-stu-id="0f856-115">Event trace consumers can implement special processing for file I/O events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**FileIoGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="0f856-116">Use los siguientes tipos de eventos para identificar el evento real al consumir eventos.</span><span class="sxs-lookup"><span data-stu-id="0f856-116">Use the following event types to identify the actual event when consuming events.</span></span>



| <span data-ttu-id="0f856-117">Tipo de evento</span><span class="sxs-lookup"><span data-stu-id="0f856-117">Event type</span></span>             | <span data-ttu-id="0f856-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="0f856-118">Description</span></span>                                                                                                                                                                             |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f856-119">El valor del tipo de evento es 0</span><span class="sxs-lookup"><span data-stu-id="0f856-119">Event type value is 0</span></span>  | <span data-ttu-id="0f856-120">Evento de nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="0f856-120">File name event.</span></span> <span data-ttu-id="0f856-121">La [**clase MOF FileIo \_ Name**](fileio-name.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="0f856-121">The [**FileIo\_Name**](fileio-name.md) MOF class defines the event data for this event.</span></span>                                                                               |
| <span data-ttu-id="0f856-122">El valor del tipo de evento es 32</span><span class="sxs-lookup"><span data-stu-id="0f856-122">Event type value is 32</span></span> | <span data-ttu-id="0f856-123">Evento de creación de archivos.</span><span class="sxs-lookup"><span data-stu-id="0f856-123">File create event.</span></span> <span data-ttu-id="0f856-124">La [**clase MOF FileIo \_ Name**](fileio-name.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="0f856-124">The [**FileIo\_Name**](fileio-name.md) MOF class defines the event data for this event.</span></span>                                                                             |
| <span data-ttu-id="0f856-125">El valor del tipo de evento es 35</span><span class="sxs-lookup"><span data-stu-id="0f856-125">Event type value is 35</span></span> | <span data-ttu-id="0f856-126">Evento de eliminación de archivos.</span><span class="sxs-lookup"><span data-stu-id="0f856-126">File delete event.</span></span> <span data-ttu-id="0f856-127">La [**clase MOF FileIo \_ Name**](fileio-name.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="0f856-127">The [**FileIo\_Name**](fileio-name.md) MOF class defines the event data for this event.</span></span>                                                                             |
| <span data-ttu-id="0f856-128">El valor del tipo de evento es 36</span><span class="sxs-lookup"><span data-stu-id="0f856-128">Event type value is 36</span></span> | <span data-ttu-id="0f856-129">Evento de desmontaje de archivos.</span><span class="sxs-lookup"><span data-stu-id="0f856-129">File rundown event.</span></span> <span data-ttu-id="0f856-130">Enumera todos los archivos abiertos en el equipo al final de la sesión de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="0f856-130">Enumerates all open files on the computer at the end of the trace session.</span></span> <span data-ttu-id="0f856-131">La [**clase MOF FileIo \_ Name**](fileio-name.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="0f856-131">The [**FileIo\_Name**](fileio-name.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="0f856-132">El valor del tipo de evento es 64</span><span class="sxs-lookup"><span data-stu-id="0f856-132">Event type value is 64</span></span> | <span data-ttu-id="0f856-133">Evento de creación de archivos.</span><span class="sxs-lookup"><span data-stu-id="0f856-133">File create event.</span></span> <span data-ttu-id="0f856-134">La [**clase MOF FileIo \_ Create**](fileio-create.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="0f856-134">The [**FileIo\_Create**](fileio-create.md) MOF class defines the event data for this event.</span></span>                                                                         |
| <span data-ttu-id="0f856-135">El valor del tipo de evento es 72</span><span class="sxs-lookup"><span data-stu-id="0f856-135">Event type value is 72</span></span> | <span data-ttu-id="0f856-136">Evento de enumeración de directorios.</span><span class="sxs-lookup"><span data-stu-id="0f856-136">Directory enumeration event.</span></span> <span data-ttu-id="0f856-137">La [**clase MOF FileIo \_ DirEnum**](fileio-direnum.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="0f856-137">The [**FileIo\_DirEnum**](fileio-direnum.md) MOF class defines the event data for this event.</span></span>                                                             |
| <span data-ttu-id="0f856-138">El valor del tipo de evento es 77</span><span class="sxs-lookup"><span data-stu-id="0f856-138">Event type value is 77</span></span> | <span data-ttu-id="0f856-139">Evento de notificación de directorio.</span><span class="sxs-lookup"><span data-stu-id="0f856-139">Directory notification event.</span></span> <span data-ttu-id="0f856-140">La [**clase MOF FileIo \_ DirEnum**](fileio-direnum.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="0f856-140">The [**FileIo\_DirEnum**](fileio-direnum.md) MOF class defines the event data for this event.</span></span>                                                            |
| <span data-ttu-id="0f856-141">El valor del tipo de evento es 69</span><span class="sxs-lookup"><span data-stu-id="0f856-141">Event type value is 69</span></span> | <span data-ttu-id="0f856-142">Establecer evento de información.</span><span class="sxs-lookup"><span data-stu-id="0f856-142">Set information event.</span></span> <span data-ttu-id="0f856-143">La [**clase MOF FileIo \_ Info**](fileio-info.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="0f856-143">The [**FileIo\_Info**](fileio-info.md) MOF class defines the event data for this event.</span></span>                                                                         |
| <span data-ttu-id="0f856-144">El valor del tipo de evento es 70</span><span class="sxs-lookup"><span data-stu-id="0f856-144">Event type value is 70</span></span> | <span data-ttu-id="0f856-145">Evento de eliminación del archivo.</span><span class="sxs-lookup"><span data-stu-id="0f856-145">Delete file event.</span></span> <span data-ttu-id="0f856-146">La [**clase MOF FileIo \_ Info**](fileio-info.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="0f856-146">The [**FileIo\_Info**](fileio-info.md) MOF class defines the event data for this event.</span></span>                                                                             |
| <span data-ttu-id="0f856-147">El valor del tipo de evento es 71</span><span class="sxs-lookup"><span data-stu-id="0f856-147">Event type value is 71</span></span> | <span data-ttu-id="0f856-148">Cambiar el nombre del evento de archivo.</span><span class="sxs-lookup"><span data-stu-id="0f856-148">Rename file event.</span></span> <span data-ttu-id="0f856-149">La [**clase MOF FileIo \_ Info**](fileio-info.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="0f856-149">The [**FileIo\_Info**](fileio-info.md) MOF class defines the event data for this event.</span></span>                                                                             |
| <span data-ttu-id="0f856-150">El valor del tipo de evento es 74</span><span class="sxs-lookup"><span data-stu-id="0f856-150">Event type value is 74</span></span> | <span data-ttu-id="0f856-151">Evento de información del archivo de consulta.</span><span class="sxs-lookup"><span data-stu-id="0f856-151">Query file information event.</span></span> <span data-ttu-id="0f856-152">La [**clase MOF FileIo \_ Info**](fileio-info.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="0f856-152">The [**FileIo\_Info**](fileio-info.md) MOF class defines the event data for this event.</span></span>                                                                  |
| <span data-ttu-id="0f856-153">El valor del tipo de evento es 75</span><span class="sxs-lookup"><span data-stu-id="0f856-153">Event type value is 75</span></span> | <span data-ttu-id="0f856-154">Evento de control del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="0f856-154">File system control event.</span></span> <span data-ttu-id="0f856-155">La [**clase MOF FileIo \_ Info**](fileio-info.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="0f856-155">The [**FileIo\_Info**](fileio-info.md) MOF class defines the event data for this event.</span></span>                                                                     |
| <span data-ttu-id="0f856-156">El valor del tipo de evento es 76</span><span class="sxs-lookup"><span data-stu-id="0f856-156">Event type value is 76</span></span> | <span data-ttu-id="0f856-157">Evento de fin de la operación.</span><span class="sxs-lookup"><span data-stu-id="0f856-157">End of operation event.</span></span> <span data-ttu-id="0f856-158">La [**clase MOF FileIo \_ OpEnd**](fileio-opend.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="0f856-158">The [**FileIo\_OpEnd**](fileio-opend.md) MOF class defines the event data for this event.</span></span>                                                                      |
| <span data-ttu-id="0f856-159">El valor del tipo de evento es 67</span><span class="sxs-lookup"><span data-stu-id="0f856-159">Event type value is 67</span></span> | <span data-ttu-id="0f856-160">Evento de lectura de archivo.</span><span class="sxs-lookup"><span data-stu-id="0f856-160">File read event.</span></span> <span data-ttu-id="0f856-161">La [**clase MOF FileIo \_ ReadWrite**](fileio-readwrite.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="0f856-161">The [**FileIo\_ReadWrite**](fileio-readwrite.md) MOF class defines the event data for this event.</span></span>                                                                     |
| <span data-ttu-id="0f856-162">El valor del tipo de evento es 68</span><span class="sxs-lookup"><span data-stu-id="0f856-162">Event type value is 68</span></span> | <span data-ttu-id="0f856-163">Evento de escritura de archivos.</span><span class="sxs-lookup"><span data-stu-id="0f856-163">File write event.</span></span> <span data-ttu-id="0f856-164">La [**clase MOF FileIo \_ ReadWrite**](fileio-readwrite.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="0f856-164">The [**FileIo\_ReadWrite**](fileio-readwrite.md) MOF class defines the event data for this event.</span></span>                                                                    |
| <span data-ttu-id="0f856-165">El valor del tipo de evento es 65</span><span class="sxs-lookup"><span data-stu-id="0f856-165">Event type value is 65</span></span> | <span data-ttu-id="0f856-166">Evento de limpieza.</span><span class="sxs-lookup"><span data-stu-id="0f856-166">Clean up event.</span></span> <span data-ttu-id="0f856-167">El evento se genera cuando se libera el último identificador del archivo.</span><span class="sxs-lookup"><span data-stu-id="0f856-167">The event is generated when the last handle to the file is released.</span></span> <span data-ttu-id="0f856-168">La [**clase MOF \_ FileIo SimpleOp**](fileio-simpleop.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="0f856-168">The [**FileIo\_SimpleOp**](fileio-simpleop.md) MOF class defines the event data for this event.</span></span>   |
| <span data-ttu-id="0f856-169">El valor del tipo de evento es 66</span><span class="sxs-lookup"><span data-stu-id="0f856-169">Event type value is 66</span></span> | <span data-ttu-id="0f856-170">Cierre el evento.</span><span class="sxs-lookup"><span data-stu-id="0f856-170">Close event.</span></span> <span data-ttu-id="0f856-171">El evento se genera cuando se libera el objeto de archivo.</span><span class="sxs-lookup"><span data-stu-id="0f856-171">The event is generated when the file object is freed.</span></span> <span data-ttu-id="0f856-172">La [**clase MOF \_ FileIo SimpleOp**](fileio-simpleop.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="0f856-172">The [**FileIo\_SimpleOp**](fileio-simpleop.md) MOF class defines the event data for this event.</span></span>                     |
| <span data-ttu-id="0f856-173">El valor del tipo de evento es 73</span><span class="sxs-lookup"><span data-stu-id="0f856-173">Event type value is 73</span></span> | <span data-ttu-id="0f856-174">Evento flush.</span><span class="sxs-lookup"><span data-stu-id="0f856-174">Flush event.</span></span> <span data-ttu-id="0f856-175">Este evento se genera cuando los búferes de archivo se vacían completamente en el disco.</span><span class="sxs-lookup"><span data-stu-id="0f856-175">This event is generated when the file buffers are fully flushed to disk.</span></span> <span data-ttu-id="0f856-176">La [**clase MOF \_ FileIo SimpleOp**](fileio-simpleop.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="0f856-176">The [**FileIo\_SimpleOp**](fileio-simpleop.md) MOF class defines the event data for this event.</span></span>  |



 

<span data-ttu-id="0f856-177">Los eventos de E/S de archivo se registran al principio de la operación.</span><span class="sxs-lookup"><span data-stu-id="0f856-177">File IO events are logged at the beginning of the operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f856-178">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f856-178">Requirements</span></span>



| <span data-ttu-id="0f856-179">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f856-179">Requirement</span></span> | <span data-ttu-id="0f856-180">Valor</span><span class="sxs-lookup"><span data-stu-id="0f856-180">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0f856-181">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0f856-181">Minimum supported client</span></span><br/> | <span data-ttu-id="0f856-182">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0f856-182">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0f856-183">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0f856-183">Minimum supported server</span></span><br/> | <span data-ttu-id="0f856-184">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="0f856-184">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0f856-185">Consulte también</span><span class="sxs-lookup"><span data-stu-id="0f856-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f856-186">**SystemTrace de MSNT \_**</span><span class="sxs-lookup"><span data-stu-id="0f856-186">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="0f856-187">**FileIo \_ V0**</span><span class="sxs-lookup"><span data-stu-id="0f856-187">**FileIo\_V0**</span></span>](fileio-v0.md)
</dt> <dt>

[<span data-ttu-id="0f856-188">**FileIo \_ V1**</span><span class="sxs-lookup"><span data-stu-id="0f856-188">**FileIo\_V1**</span></span>](fileio-v1.md)
</dt> </dl>

 

 
