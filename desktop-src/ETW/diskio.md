---
description: Esta clase es la clase primaria para los eventos de e/s de disco. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 630fb6c6-b505-4384-ab7b-ee898d95bd41
title: Clase desmontaje
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskIo
api_type:
- NA
api_location: ''
ms.openlocfilehash: 97f9907e4da51675bb1a5f562931e471ee0e133e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000969"
---
# <a name="diskio-class"></a><span data-ttu-id="1d435-104">Clase desmontaje</span><span class="sxs-lookup"><span data-stu-id="1d435-104">DiskIo class</span></span>

<span data-ttu-id="1d435-105">Esta clase es la clase primaria para los eventos de e/s de disco.</span><span class="sxs-lookup"><span data-stu-id="1d435-105">This class is the parent class for disk I/O events.</span></span>

<span data-ttu-id="1d435-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="1d435-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d435-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1d435-107">Syntax</span></span>

``` syntax
[Guid("{3d6fa8d4-fe05-11d0-9dda-00c04fd7ba7c}")]
class DiskIo : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="1d435-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="1d435-108">Members</span></span>

<span data-ttu-id="1d435-109">La clase **Desmontaje** no define ningún miembro.</span><span class="sxs-lookup"><span data-stu-id="1d435-109">The **DiskIo** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d435-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1d435-110">Remarks</span></span>

<span data-ttu-id="1d435-111">Para habilitar los eventos de e/s de disco en una sesión de registro del kernel de NT, especifique la marca de  e/s de disco de la marca de seguimiento de **eventos \_ \_ \_ \_** en el miembro EnableFlags de una estructura de [**\_ \_ propiedades de seguimiento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) al llamar a la función [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .</span><span class="sxs-lookup"><span data-stu-id="1d435-111">To enable disk I/0 events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_DISK\_IO** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span> <span data-ttu-id="1d435-112">También puede especificar una o varias de las marcas siguientes:</span><span class="sxs-lookup"><span data-stu-id="1d435-112">You can also specify one or more of the following flags:</span></span>

-   <span data-ttu-id="1d435-113">**marca de seguimiento de eventos \_ \_ \_ init de \_ e/s de disco \_**</span><span class="sxs-lookup"><span data-stu-id="1d435-113">**EVENT\_TRACE\_FLAG\_DISK\_IO\_INIT**</span></span>
-   <span data-ttu-id="1d435-114">**\_controlador de \_ marca de seguimiento de eventos \_**</span><span class="sxs-lookup"><span data-stu-id="1d435-114">**EVENT\_TRACE\_FLAG\_DRIVER**</span></span>

<span data-ttu-id="1d435-115">Los consumidores de seguimiento de eventos pueden implementar un procesamiento especial para los eventos de e/s de disco llamando a la función [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) y especificando [**DiskIoGuid**](nt-kernel-logger-constants.md) como parámetro *pGuid* .</span><span class="sxs-lookup"><span data-stu-id="1d435-115">Event trace consumers can implement special processing for disk I/O events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**DiskIoGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="1d435-116">Utilice los siguientes tipos de eventos para identificar el evento de e/s de disco real al consumir eventos.</span><span class="sxs-lookup"><span data-stu-id="1d435-116">Use the following event types to identify the actual disk I/O event when consuming events.</span></span>



| <span data-ttu-id="1d435-117">Tipo de evento</span><span class="sxs-lookup"><span data-stu-id="1d435-117">Event type</span></span>                                                                      | <span data-ttu-id="1d435-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="1d435-118">Description</span></span>                                                                                                                                                   |
|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d435-119">**Evento \_ de Tipo de seguimiento de \_ \_ e/s \_ leída**(el valor de tipo de evento es 10)</span><span class="sxs-lookup"><span data-stu-id="1d435-119">**EVENT\_TRACE\_TYPE\_IO\_READ**(Event type value is 10)</span></span><br/>             | <span data-ttu-id="1d435-120">Evento de lectura.</span><span class="sxs-lookup"><span data-stu-id="1d435-120">Read event.</span></span> <span data-ttu-id="1d435-121">La clase MOF [**desmontaje \_ TypeGroup1**](diskio-typegroup1.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="1d435-121">The [**DiskIo\_TypeGroup1**](diskio-typegroup1.md) MOF class defines the event data for this event.</span></span>                                              |
| <span data-ttu-id="1d435-122">**Evento \_ de Tipo de seguimiento de \_ \_ \_ escritura de e/s**(el valor de tipo de evento es 11)</span><span class="sxs-lookup"><span data-stu-id="1d435-122">**EVENT\_TRACE\_TYPE\_IO\_WRITE**(Event type value is 11)</span></span><br/>            | <span data-ttu-id="1d435-123">Escribir evento.</span><span class="sxs-lookup"><span data-stu-id="1d435-123">Write event.</span></span> <span data-ttu-id="1d435-124">La clase MOF [**desmontaje \_ TypeGroup1**](diskio-typegroup1.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="1d435-124">The [**DiskIo\_TypeGroup1**](diskio-typegroup1.md) MOF class defines the event data for this event.</span></span>                                             |
| <span data-ttu-id="1d435-125">**Evento \_ de Tipo de seguimiento \_ \_ IO \_ Read \_ init**(el valor del tipo de evento es 12)</span><span class="sxs-lookup"><span data-stu-id="1d435-125">**EVENT\_TRACE\_TYPE\_IO\_READ\_INIT**(Event type value is 12)</span></span><br/>       | <span data-ttu-id="1d435-126">Inicializar evento de lectura.</span><span class="sxs-lookup"><span data-stu-id="1d435-126">Initialize read event.</span></span> <span data-ttu-id="1d435-127">La clase MOF [**desmontaje \_ TypeGroup2**](diskio-typegroup2.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="1d435-127">The [**DiskIo\_TypeGroup2**](diskio-typegroup2.md) MOF class defines the event data for this event.</span></span>                                   |
| <span data-ttu-id="1d435-128">**Evento \_ de Tipo de seguimiento \_ \_ IO \_ Write \_ init**(el valor del tipo de evento es 13)</span><span class="sxs-lookup"><span data-stu-id="1d435-128">**EVENT\_TRACE\_TYPE\_IO\_WRITE\_INIT**(Event type value is 13)</span></span><br/>      | <span data-ttu-id="1d435-129">Inicializar evento de escritura.</span><span class="sxs-lookup"><span data-stu-id="1d435-129">Initialize write event.</span></span> <span data-ttu-id="1d435-130">La clase MOF [**desmontaje \_ TypeGroup2**](diskio-typegroup2.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="1d435-130">The [**DiskIo\_TypeGroup2**](diskio-typegroup2.md) MOF class defines the event data for this event.</span></span>                                  |
| <span data-ttu-id="1d435-131">**Evento \_ de \_ \_ \_ Vaciar el tipo de seguimiento de e/s**(el valor del tipo de evento es 14)</span><span class="sxs-lookup"><span data-stu-id="1d435-131">**EVENT\_TRACE\_TYPE\_IO\_FLUSH**(Event type value is 14)</span></span><br/>            | <span data-ttu-id="1d435-132">Inicializar evento de escritura.</span><span class="sxs-lookup"><span data-stu-id="1d435-132">Initialize write event.</span></span> <span data-ttu-id="1d435-133">La clase MOF [**desmontaje \_ TypeGroup3**](diskio-typegroup3.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="1d435-133">The [**DiskIo\_TypeGroup3**](diskio-typegroup3.md) MOF class defines the event data for this event.</span></span>                                  |
| <span data-ttu-id="1d435-134">**Evento \_ de Tipo de seguimiento de \_ \_ \_ \_ inicialización de salida de e/s**(el valor de tipo de evento es 15)</span><span class="sxs-lookup"><span data-stu-id="1d435-134">**EVENT\_TRACE\_TYPE\_IO\_FLUSH\_INIT**(Event type value is 15)</span></span><br/>      | <span data-ttu-id="1d435-135">Inicializar evento de vaciado.</span><span class="sxs-lookup"><span data-stu-id="1d435-135">Initialize flush event.</span></span> <span data-ttu-id="1d435-136">La clase MOF [**desmontaje \_ TypeGroup2**](diskio-typegroup2.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="1d435-136">The [**DiskIo\_TypeGroup2**](diskio-typegroup2.md) MOF class defines the event data for this event.</span></span>                                  |
| <span data-ttu-id="1d435-137">**Evento \_ de \_Tipo de \_ seguimiento \_ redireccionado \_ init**(el valor de tipo de evento es 16)</span><span class="sxs-lookup"><span data-stu-id="1d435-137">**EVENT\_TRACE\_TYPE\_IO\_REDIRECTED\_INIT**(Event type value is 16)</span></span><br/> | <span data-ttu-id="1d435-138">Inicializar evento redirigido.</span><span class="sxs-lookup"><span data-stu-id="1d435-138">Initialize redirected event.</span></span> <span data-ttu-id="1d435-139">Los eventos de e/s Redirigido se usan para asignar las e/s de disco a un formato de imagen de Windows (WIM) al nombre de archivo en WIM.</span><span class="sxs-lookup"><span data-stu-id="1d435-139">Redirected IO events are used to map disk IOs to a Windows Imaging Format (WIM) to the filename within the WIM.</span></span>                  |
| <span data-ttu-id="1d435-140">El valor del tipo de evento es 52</span><span class="sxs-lookup"><span data-stu-id="1d435-140">Event type value is 52</span></span><br/>                                               | <span data-ttu-id="1d435-141">Evento de solicitud de finalización de controlador.</span><span class="sxs-lookup"><span data-stu-id="1d435-141">Driver complete request event.</span></span> <span data-ttu-id="1d435-142">La clase MOF [**DriverCompleteRequest**](drivercompleterequest.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="1d435-142">The [**DriverCompleteRequest**](drivercompleterequest.md) MOF class defines the event data for this event.</span></span>                    |
| <span data-ttu-id="1d435-143">El valor del tipo de evento es 53</span><span class="sxs-lookup"><span data-stu-id="1d435-143">Event type value is 53</span></span><br/>                                               | <span data-ttu-id="1d435-144">Evento de devolución de solicitud de finalización de controlador.</span><span class="sxs-lookup"><span data-stu-id="1d435-144">Driver complete request return event.</span></span> <span data-ttu-id="1d435-145">La clase MOF [**DriverCompleteRequestReturn**](drivercompleterequestreturn.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="1d435-145">The [**DriverCompleteRequestReturn**](drivercompleterequestreturn.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="1d435-146">El valor del tipo de evento es 37</span><span class="sxs-lookup"><span data-stu-id="1d435-146">Event type value is 37</span></span><br/>                                               | <span data-ttu-id="1d435-147">Evento de rutina de finalización de controlador.</span><span class="sxs-lookup"><span data-stu-id="1d435-147">Driver completion routine event.</span></span> <span data-ttu-id="1d435-148">La clase MOF [**DriverCompletionRoutine**](drivercompletionroutine.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="1d435-148">The [**DriverCompletionRoutine**](drivercompletionroutine.md) MOF class defines the event data for this event.</span></span>              |
| <span data-ttu-id="1d435-149">El valor del tipo de evento es 34</span><span class="sxs-lookup"><span data-stu-id="1d435-149">Event type value is 34</span></span><br/>                                               | <span data-ttu-id="1d435-150">Evento de llamada de función principal de controlador.</span><span class="sxs-lookup"><span data-stu-id="1d435-150">Driver major function call event.</span></span> <span data-ttu-id="1d435-151">La clase MOF [**DriverMajorFunctionCall**](drivermajorfunctioncall.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="1d435-151">The [**DriverMajorFunctionCall**](drivermajorfunctioncall.md) MOF class defines the event data for this event.</span></span>             |
| <span data-ttu-id="1d435-152">El valor del tipo de evento es 35</span><span class="sxs-lookup"><span data-stu-id="1d435-152">Event type value is 35</span></span><br/>                                               | <span data-ttu-id="1d435-153">Evento de devolución de llamada de función principal de controlador.</span><span class="sxs-lookup"><span data-stu-id="1d435-153">Driver major function call return event.</span></span> <span data-ttu-id="1d435-154">La clase MOF [**DriverMajorFunctionReturn**](drivermajorfunctionreturn.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="1d435-154">The [**DriverMajorFunctionReturn**](drivermajorfunctionreturn.md) MOF class defines the event data for this event.</span></span>  |



 

<span data-ttu-id="1d435-155">El proveedor de e/s de disco no puede identificar el archivo que se lee o escribe durante un evento de e/s de disco.</span><span class="sxs-lookup"><span data-stu-id="1d435-155">The disk I/0 provider cannot identify which file is read or written during a disk I/O event.</span></span> <span data-ttu-id="1d435-156">Para recuperar el nombre del archivo asociado al evento de e/s de disco, habilite el proveedor de eventos I/0 de archivo.</span><span class="sxs-lookup"><span data-stu-id="1d435-156">To retrieve the name of the file associated with the disk I/O event, enable the file I/0 event provider.</span></span>

<span data-ttu-id="1d435-157">Los eventos de e/s de disco se registran en la hora de finalización de e/s.</span><span class="sxs-lookup"><span data-stu-id="1d435-157">Disk I/O events are recorded at the I/O completion time.</span></span> <span data-ttu-id="1d435-158">Para determinar Cuándo comenzó la operación de e/s, use los eventos de inicialización, por ejemplo, el tipo de seguimiento de eventos \_ \_ \_ IO \_ Read \_ init.</span><span class="sxs-lookup"><span data-stu-id="1d435-158">To determine when the I/O operation began, use the initialization events, for example, EVENT\_TRACE\_TYPE\_IO\_READ\_INIT.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d435-159">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d435-159">Requirements</span></span>



| <span data-ttu-id="1d435-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d435-160">Requirement</span></span> | <span data-ttu-id="1d435-161">Value</span><span class="sxs-lookup"><span data-stu-id="1d435-161">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1d435-162">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1d435-162">Minimum supported client</span></span><br/> | <span data-ttu-id="1d435-163">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="1d435-163">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="1d435-164">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1d435-164">Minimum supported server</span></span><br/> | <span data-ttu-id="1d435-165">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="1d435-165">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1d435-166">Vea también</span><span class="sxs-lookup"><span data-stu-id="1d435-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d435-167">**Desmontaje \_ TypeGroup1**</span><span class="sxs-lookup"><span data-stu-id="1d435-167">**DiskIo\_TypeGroup1**</span></span>](diskio-typegroup1.md)
</dt> <dt>

[<span data-ttu-id="1d435-168">**Desmontaje \_ TypeGroup2**</span><span class="sxs-lookup"><span data-stu-id="1d435-168">**DiskIo\_TypeGroup2**</span></span>](diskio-typegroup2.md)
</dt> <dt>

[<span data-ttu-id="1d435-169">**Desmontaje \_ TypeGroup3**</span><span class="sxs-lookup"><span data-stu-id="1d435-169">**DiskIo\_TypeGroup3**</span></span>](diskio-typegroup3.md)
</dt> <dt>

[<span data-ttu-id="1d435-170">**DriverCompleteRequest**</span><span class="sxs-lookup"><span data-stu-id="1d435-170">**DriverCompleteRequest**</span></span>](drivercompleterequest.md)
</dt> <dt>

[<span data-ttu-id="1d435-171">**DriverCompleteRequestReturn**</span><span class="sxs-lookup"><span data-stu-id="1d435-171">**DriverCompleteRequestReturn**</span></span>](drivercompleterequestreturn.md)
</dt> <dt>

[<span data-ttu-id="1d435-172">**DriverCompletionRoutine**</span><span class="sxs-lookup"><span data-stu-id="1d435-172">**DriverCompletionRoutine**</span></span>](drivercompletionroutine.md)
</dt> <dt>

[<span data-ttu-id="1d435-173">**DriverMajorFunctionCall**</span><span class="sxs-lookup"><span data-stu-id="1d435-173">**DriverMajorFunctionCall**</span></span>](drivermajorfunctioncall.md)
</dt> <dt>

[<span data-ttu-id="1d435-174">**DriverMajorFunctionReturn**</span><span class="sxs-lookup"><span data-stu-id="1d435-174">**DriverMajorFunctionReturn**</span></span>](drivermajorfunctionreturn.md)
</dt> </dl>

 

 
