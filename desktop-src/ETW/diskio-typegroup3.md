---
description: Esta clase es la clase de tipo de evento para eventos de vaciado de e/s de disco. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 7f0c9bd4-e4d3-49c1-ae72-f6bdf938099f
title: DiskIo_TypeGroup3 (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskIo_TypeGroup3
- DiskIo_TypeGroup3.DiskNumber
- DiskIo_TypeGroup3.IrpFlags
- DiskIo_TypeGroup3.HighResResponseTime
- DiskIo_TypeGroup3.Irp
- DiskIo_TypeGroup3.IssuingThreadId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 63ca227269dab249be755da22288ce41696a19e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984234"
---
# <a name="diskio_typegroup3-class"></a><span data-ttu-id="2d46e-104">Desmontaje \_ TypeGroup3 (clase)</span><span class="sxs-lookup"><span data-stu-id="2d46e-104">DiskIo\_TypeGroup3 class</span></span>

<span data-ttu-id="2d46e-105">Esta clase es la clase de tipo de evento para eventos de vaciado de e/s de disco.</span><span class="sxs-lookup"><span data-stu-id="2d46e-105">This class is the event type class for disk I/O flush events.</span></span>

<span data-ttu-id="2d46e-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="2d46e-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d46e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2d46e-107">Syntax</span></span>

``` syntax
[EventType{14}, EventTypeName{"FlushBuffers"}]
class DiskIo_TypeGroup3 : DiskIo
{
  uint32 DiskNumber;
  uint32 IrpFlags;
  uint64 HighResResponseTime;
  uint32 Irp;
  uint32 IssuingThreadId;
};
```

## <a name="members"></a><span data-ttu-id="2d46e-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="2d46e-108">Members</span></span>

<span data-ttu-id="2d46e-109">La clase **desmontaje \_ TypeGroup3** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2d46e-109">The **DiskIo\_TypeGroup3** class has these types of members:</span></span>

-   [<span data-ttu-id="2d46e-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2d46e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2d46e-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2d46e-111">Properties</span></span>

<span data-ttu-id="2d46e-112">La clase **desmontaje \_ TypeGroup3** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="2d46e-112">The **DiskIo\_TypeGroup3** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2d46e-113">**Númerodedisco corresponde**</span><span class="sxs-lookup"><span data-stu-id="2d46e-113">**DiskNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d46e-114">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2d46e-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2d46e-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2d46e-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d46e-116">Calificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)</span><span class="sxs-lookup"><span data-stu-id="2d46e-116">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)</span></span>
</dt> </dl>

<span data-ttu-id="2d46e-117">Número que identifica el disco físico.</span><span class="sxs-lookup"><span data-stu-id="2d46e-117">Number that identifies the physical disk.</span></span>

</dd> <dt>

<span data-ttu-id="2d46e-118">**HighResResponseTime**</span><span class="sxs-lookup"><span data-stu-id="2d46e-118">**HighResResponseTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d46e-119">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2d46e-119">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2d46e-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2d46e-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d46e-121">Calificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)</span><span class="sxs-lookup"><span data-stu-id="2d46e-121">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)</span></span>
</dt> </dl>

<span data-ttu-id="2d46e-122">Recuento de TICs de CPU desde el principio de la operación hasta el final de la operación.</span><span class="sxs-lookup"><span data-stu-id="2d46e-122">CPU tick count from the beginning of the operation to the end of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="2d46e-123">**IRP**</span><span class="sxs-lookup"><span data-stu-id="2d46e-123">**Irp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d46e-124">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2d46e-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2d46e-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2d46e-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d46e-126">Calificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (4), [**puntero**](event-tracing-mof-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="2d46e-126">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (4), [**Pointer**](event-tracing-mof-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="2d46e-127">Paquete de solicitud de e/s.</span><span class="sxs-lookup"><span data-stu-id="2d46e-127">I/O request packet.</span></span> <span data-ttu-id="2d46e-128">Esta propiedad identifica la actividad de e/s.</span><span class="sxs-lookup"><span data-stu-id="2d46e-128">This property identifies the I/O activity.</span></span>

</dd> <dt>

<span data-ttu-id="2d46e-129">**IrpFlags**</span><span class="sxs-lookup"><span data-stu-id="2d46e-129">**IrpFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d46e-130">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2d46e-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2d46e-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2d46e-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d46e-132">Calificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (2), [**Format**](event-tracing-mof-qualifiers.md) ("x")</span><span class="sxs-lookup"><span data-stu-id="2d46e-132">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (2), [**Format**](event-tracing-mof-qualifiers.md) ("x")</span></span>
</dt> </dl>

<span data-ttu-id="2d46e-133">Puede contener una o varias de las siguientes marcas de paquete de solicitud de e/s (definidas en Ntddk. h, que es un archivo de encabezado de DDK):</span><span class="sxs-lookup"><span data-stu-id="2d46e-133">Can contain one or more of the following I/O request packet flags (defined in Ntddk.h, which is a DDK header file):</span></span>

<dl><span id="__IRP_NOCACHE"></span><span id="__irp_nocache"></span><dt>

 <span data-ttu-id="2d46e-134">**IRP \_ NOcache**</span><span class="sxs-lookup"><span data-stu-id="2d46e-134">**IRP\_NOCACHE**</span></span>
</dt><span id="__IRP_PAGING_IO"></span><span id="__irp_paging_io"></span><dt>

 <span data-ttu-id="2d46e-135">**\_ \_ e/s de PAGINAción IRP**</span><span class="sxs-lookup"><span data-stu-id="2d46e-135">**IRP\_PAGING\_IO**</span></span>
</dt><span id="__IRP_MOUNT_COMPLETION"></span><span id="__irp_mount_completion"></span><dt>

 <span data-ttu-id="2d46e-136">**\_finalización de montaje IRP \_**</span><span class="sxs-lookup"><span data-stu-id="2d46e-136">**IRP\_MOUNT\_COMPLETION**</span></span>
</dt><span id="__IRP_SYNCHRONOUS_API"></span><span id="__irp_synchronous_api"></span><dt>

 <span data-ttu-id="2d46e-137">**\_API sincrónica IRP \_**</span><span class="sxs-lookup"><span data-stu-id="2d46e-137">**IRP\_SYNCHRONOUS\_API**</span></span>
</dt><span id="__IRP_ASSOCIATED_IRP"></span><span id="__irp_associated_irp"></span><dt>

 <span data-ttu-id="2d46e-138">**\_IRP asociado de IRP \_**</span><span class="sxs-lookup"><span data-stu-id="2d46e-138">**IRP\_ASSOCIATED\_IRP**</span></span>
</dt><span id="__IRP_BUFFERED_IO"></span><span id="__irp_buffered_io"></span><dt>

 <span data-ttu-id="2d46e-139">**\_ \_ e/s de búfer IRP**</span><span class="sxs-lookup"><span data-stu-id="2d46e-139">**IRP\_BUFFERED\_IO**</span></span>
</dt><span id="IRP_DEALLOCATE_BUFFER"></span><span id="irp_deallocate_buffer"></span><dt>

<span data-ttu-id="2d46e-140">**\_búfer de DESasignación de IRP \_**</span><span class="sxs-lookup"><span data-stu-id="2d46e-140">**IRP\_DEALLOCATE\_BUFFER**</span></span>
</dt><span id="__IRP_INPUT_OPERATION"></span><span id="__irp_input_operation"></span><dt>

 <span data-ttu-id="2d46e-141">**\_operación de entrada IRP \_**</span><span class="sxs-lookup"><span data-stu-id="2d46e-141">**IRP\_INPUT\_OPERATION**</span></span>
</dt><span id="__IRP_SYNCHRONOUS_PAGING_IO"></span><span id="__irp_synchronous_paging_io"></span><dt>

 <span data-ttu-id="2d46e-142">**\_ \_ e/s de paginación sincrónica IRP \_**</span><span class="sxs-lookup"><span data-stu-id="2d46e-142">**IRP\_SYNCHRONOUS\_PAGING\_IO**</span></span>
</dt><span id="__IRP_CREATE_OPERATION"></span><span id="__irp_create_operation"></span><dt>

 <span data-ttu-id="2d46e-143">**\_operación de creación de IRP \_**</span><span class="sxs-lookup"><span data-stu-id="2d46e-143">**IRP\_CREATE\_OPERATION**</span></span>
</dt><span id="IRP_READ_OPERATION"></span><span id="irp_read_operation"></span><dt>

<span data-ttu-id="2d46e-144">**\_operación de lectura IRP \_**</span><span class="sxs-lookup"><span data-stu-id="2d46e-144">**IRP\_READ\_OPERATION**</span></span>
</dt><span id="__IRP_WRITE_OPERATION"></span><span id="__irp_write_operation"></span><dt>

 <span data-ttu-id="2d46e-145">**\_operación de escritura IRP \_**</span><span class="sxs-lookup"><span data-stu-id="2d46e-145">**IRP\_WRITE\_OPERATION**</span></span>
</dt><span id="__IRP_CLOSE_OPERATION"></span><span id="__irp_close_operation"></span><dt>

 <span data-ttu-id="2d46e-146">**\_operación de cierre IRP \_**</span><span class="sxs-lookup"><span data-stu-id="2d46e-146">**IRP\_CLOSE\_OPERATION**</span></span>
</dt><span id="__IRP_DEFER_IO_COMPLETION"></span><span id="__irp_defer_io_completion"></span><dt>

 <span data-ttu-id="2d46e-147">**IRP \_ aplazar \_ finalización de e/s \_**</span><span class="sxs-lookup"><span data-stu-id="2d46e-147">**IRP\_DEFER\_IO\_COMPLETION**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2d46e-148">**IssuingThreadId**</span><span class="sxs-lookup"><span data-stu-id="2d46e-148">**IssuingThreadId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d46e-149">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2d46e-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2d46e-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2d46e-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d46e-151">Calificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (5)</span><span class="sxs-lookup"><span data-stu-id="2d46e-151">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (5)</span></span>
</dt> </dl>

<span data-ttu-id="2d46e-152">Identificador del subproceso que se emite.</span><span class="sxs-lookup"><span data-stu-id="2d46e-152">The identifier of the issuing thread.</span></span>

<span data-ttu-id="2d46e-153">**Windows server 2008 R2, Windows server 2008, Windows 7 y Windows Vista:** Esta propiedad no se admite.</span><span class="sxs-lookup"><span data-stu-id="2d46e-153">**Windows Server 2008 R2, Windows Server 2008, Windows 7 and Windows Vista:** This property is not supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2d46e-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d46e-154">Requirements</span></span>



| <span data-ttu-id="2d46e-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d46e-155">Requirement</span></span> | <span data-ttu-id="2d46e-156">Value</span><span class="sxs-lookup"><span data-stu-id="2d46e-156">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2d46e-157">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2d46e-157">Minimum supported client</span></span><br/> | <span data-ttu-id="2d46e-158">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2d46e-158">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2d46e-159">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2d46e-159">Minimum supported server</span></span><br/> | <span data-ttu-id="2d46e-160">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="2d46e-160">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2d46e-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="2d46e-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d46e-162">**Desmontaje**</span><span class="sxs-lookup"><span data-stu-id="2d46e-162">**DiskIo**</span></span>](diskio.md)
</dt> </dl>

 

 




