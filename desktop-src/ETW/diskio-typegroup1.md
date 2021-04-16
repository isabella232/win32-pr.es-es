---
description: Esta clase es la clase de tipo de evento para los eventos de e/s de disco. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: fe7d4efa-3d39-4438-a1a6-af3f65ea3deb
title: DiskIo_TypeGroup1 (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskIo_TypeGroup1
- DiskIo_TypeGroup1.DiskNumber
- DiskIo_TypeGroup1.IrpFlags
- DiskIo_TypeGroup1.TransferSize
- DiskIo_TypeGroup1.Reserved
- DiskIo_TypeGroup1.ByteOffset
- DiskIo_TypeGroup1.FileObject
- DiskIo_TypeGroup1.Irp
- DiskIo_TypeGroup1.HighResResponseTime
- DiskIo_TypeGroup1.IssuingThreadId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9d20f80eb840283600f5d106f89c6cf8032ee746
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542515"
---
# <a name="diskio_typegroup1-class"></a><span data-ttu-id="20342-104">Desmontaje \_ TypeGroup1 (clase)</span><span class="sxs-lookup"><span data-stu-id="20342-104">DiskIo\_TypeGroup1 class</span></span>

<span data-ttu-id="20342-105">Esta clase es la clase de tipo de evento para los eventos de e/s de disco.</span><span class="sxs-lookup"><span data-stu-id="20342-105">This class is the event type class for disk I/O events.</span></span>

<span data-ttu-id="20342-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="20342-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="20342-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="20342-107">Syntax</span></span>

``` syntax
[EventType{10,11}, EventTypeName{"Read","Write"}]
class DiskIo_TypeGroup1 : DiskIo
{
  uint32 DiskNumber;
  uint32 IrpFlags;
  uint32 TransferSize;
  uint32 Reserved;
  sint64 ByteOffset;
  uint32 FileObject;
  uint32 Irp;
  uint64 HighResResponseTime;
  uint32 IssuingThreadId;
};
```

## <a name="members"></a><span data-ttu-id="20342-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="20342-108">Members</span></span>

<span data-ttu-id="20342-109">La clase **desmontaje \_ TypeGroup1** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="20342-109">The **DiskIo\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="20342-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="20342-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="20342-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="20342-111">Properties</span></span>

<span data-ttu-id="20342-112">La clase **desmontaje \_ TypeGroup1** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="20342-112">The **DiskIo\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="20342-113">**Byteoffset (**</span><span class="sxs-lookup"><span data-stu-id="20342-113">**ByteOffset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20342-114">Tipo de datos: **sint64**</span><span class="sxs-lookup"><span data-stu-id="20342-114">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="20342-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="20342-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20342-116">Calificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (5)</span><span class="sxs-lookup"><span data-stu-id="20342-116">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (5)</span></span>
</dt> </dl>

<span data-ttu-id="20342-117">Desplazamiento de bytes desde el principio del disco físico.</span><span class="sxs-lookup"><span data-stu-id="20342-117">Byte offset from the beginning of the physical disk.</span></span>

</dd> <dt>

<span data-ttu-id="20342-118">**Númerodedisco corresponde**</span><span class="sxs-lookup"><span data-stu-id="20342-118">**DiskNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20342-119">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="20342-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="20342-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="20342-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20342-121">Calificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)</span><span class="sxs-lookup"><span data-stu-id="20342-121">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)</span></span>
</dt> </dl>

<span data-ttu-id="20342-122">Número que identifica el disco físico.</span><span class="sxs-lookup"><span data-stu-id="20342-122">Number that identifies the physical disk.</span></span>

</dd> <dt>

<span data-ttu-id="20342-123">**FileObject**</span><span class="sxs-lookup"><span data-stu-id="20342-123">**FileObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20342-124">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="20342-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="20342-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="20342-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20342-126">Calificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (6), [**puntero**](event-tracing-mof-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="20342-126">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (6), [**Pointer**](event-tracing-mof-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="20342-127">Haga coincidir el valor de este puntero con el valor de puntero de **FileObject** en un evento de [**\_ nombre FileIo**](fileio-name.md) para determinar el archivo implicado en la operación de e/s.</span><span class="sxs-lookup"><span data-stu-id="20342-127">Match the value of this pointer to the **FileObject** pointer value in a [**FileIo\_Name**](fileio-name.md) event to determine the file involved in the I/O operation.</span></span>

</dd> <dt>

<span data-ttu-id="20342-128">**HighResResponseTime**</span><span class="sxs-lookup"><span data-stu-id="20342-128">**HighResResponseTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20342-129">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="20342-129">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="20342-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="20342-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20342-131">Calificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (8)</span><span class="sxs-lookup"><span data-stu-id="20342-131">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (8)</span></span>
</dt> </dl>

<span data-ttu-id="20342-132">Tiempo transcurrido entre el inicio y la finalización de e/s medido por el administrador de particiones (en las unidades de paso [**KeQueryPerformanceCounter**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-kequeryperformancecounter) ).</span><span class="sxs-lookup"><span data-stu-id="20342-132">The time between I/O initiation and completion as measured by the partition manager (in the [**KeQueryPerformanceCounter**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-kequeryperformancecounter) tick units).</span></span>

<span data-ttu-id="20342-133">**Windows Server 2003:** Esta propiedad tiene un valor de [**WmiDataId**](event-tracing-mof-qualifiers.md) de 7.</span><span class="sxs-lookup"><span data-stu-id="20342-133">**Windows Server 2003:** This property has a [**WmiDataId**](event-tracing-mof-qualifiers.md) value of 7.</span></span>

<span data-ttu-id="20342-134">**Windows 2000 Server y windows 2000 Professional:** Esta propiedad no se admite.</span><span class="sxs-lookup"><span data-stu-id="20342-134">**Windows 2000 Server and Windows 2000 Professional:** This property is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="20342-135">**IRP**</span><span class="sxs-lookup"><span data-stu-id="20342-135">**Irp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20342-136">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="20342-136">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="20342-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="20342-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20342-138">Calificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (7), [**puntero**](event-tracing-mof-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="20342-138">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (7), [**Pointer**](event-tracing-mof-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="20342-139">El paquete de solicitud de e/s, que identifica la actividad de e/s.</span><span class="sxs-lookup"><span data-stu-id="20342-139">The I/O request packet, which identifies the I/O activity.</span></span>

<span data-ttu-id="20342-140">**Windows server 2003, windows 2000 Server y windows 2000 Professional:** Esta propiedad no se admite.</span><span class="sxs-lookup"><span data-stu-id="20342-140">**Windows Server 2003, Windows 2000 Server and Windows 2000 Professional:** This property is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="20342-141">**IrpFlags**</span><span class="sxs-lookup"><span data-stu-id="20342-141">**IrpFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20342-142">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="20342-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="20342-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="20342-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20342-144">Calificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (2), [**Format**](event-tracing-mof-qualifiers.md) ("x")</span><span class="sxs-lookup"><span data-stu-id="20342-144">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (2), [**Format**](event-tracing-mof-qualifiers.md) ("x")</span></span>
</dt> </dl>

<span data-ttu-id="20342-145">Puede contener una o varias de las siguientes marcas de paquete de solicitud de e/s (definidas en Ntddk. h, que es un archivo de encabezado de DDK):</span><span class="sxs-lookup"><span data-stu-id="20342-145">Can contain one or more of the following I/O request packet flags (defined in Ntddk.h, which is a DDK header file):</span></span>

<dl><span id="__IRP_NOCACHE"></span><span id="__irp_nocache"></span><dt>

 <span data-ttu-id="20342-146">**IRP \_ NOcache**</span><span class="sxs-lookup"><span data-stu-id="20342-146">**IRP\_NOCACHE**</span></span>
</dt><span id="__IRP_PAGING_IO"></span><span id="__irp_paging_io"></span><dt>

 <span data-ttu-id="20342-147">**\_ \_ e/s de PAGINAción IRP**</span><span class="sxs-lookup"><span data-stu-id="20342-147">**IRP\_PAGING\_IO**</span></span>
</dt><span id="__IRP_MOUNT_COMPLETION"></span><span id="__irp_mount_completion"></span><dt>

 <span data-ttu-id="20342-148">**\_finalización de montaje IRP \_**</span><span class="sxs-lookup"><span data-stu-id="20342-148">**IRP\_MOUNT\_COMPLETION**</span></span>
</dt><span id="__IRP_SYNCHRONOUS_API"></span><span id="__irp_synchronous_api"></span><dt>

 <span data-ttu-id="20342-149">**\_API sincrónica IRP \_**</span><span class="sxs-lookup"><span data-stu-id="20342-149">**IRP\_SYNCHRONOUS\_API**</span></span>
</dt><span id="__IRP_ASSOCIATED_IRP"></span><span id="__irp_associated_irp"></span><dt>

 <span data-ttu-id="20342-150">**\_IRP asociado de IRP \_**</span><span class="sxs-lookup"><span data-stu-id="20342-150">**IRP\_ASSOCIATED\_IRP**</span></span>
</dt><span id="__IRP_BUFFERED_IO"></span><span id="__irp_buffered_io"></span><dt>

 <span data-ttu-id="20342-151">**\_ \_ e/s de búfer IRP**</span><span class="sxs-lookup"><span data-stu-id="20342-151">**IRP\_BUFFERED\_IO**</span></span>
</dt><span id="IRP_DEALLOCATE_BUFFER"></span><span id="irp_deallocate_buffer"></span><dt>

<span data-ttu-id="20342-152">**\_búfer de DESasignación de IRP \_**</span><span class="sxs-lookup"><span data-stu-id="20342-152">**IRP\_DEALLOCATE\_BUFFER**</span></span>
</dt><span id="__IRP_INPUT_OPERATION"></span><span id="__irp_input_operation"></span><dt>

 <span data-ttu-id="20342-153">**\_operación de entrada IRP \_**</span><span class="sxs-lookup"><span data-stu-id="20342-153">**IRP\_INPUT\_OPERATION**</span></span>
</dt><span id="__IRP_SYNCHRONOUS_PAGING_IO"></span><span id="__irp_synchronous_paging_io"></span><dt>

 <span data-ttu-id="20342-154">**\_ \_ e/s de paginación sincrónica IRP \_**</span><span class="sxs-lookup"><span data-stu-id="20342-154">**IRP\_SYNCHRONOUS\_PAGING\_IO**</span></span>
</dt><span id="__IRP_CREATE_OPERATION"></span><span id="__irp_create_operation"></span><dt>

 <span data-ttu-id="20342-155">**\_operación de creación de IRP \_**</span><span class="sxs-lookup"><span data-stu-id="20342-155">**IRP\_CREATE\_OPERATION**</span></span>
</dt><span id="IRP_READ_OPERATION"></span><span id="irp_read_operation"></span><dt>

<span data-ttu-id="20342-156">**\_operación de lectura IRP \_**</span><span class="sxs-lookup"><span data-stu-id="20342-156">**IRP\_READ\_OPERATION**</span></span>
</dt><span id="__IRP_WRITE_OPERATION"></span><span id="__irp_write_operation"></span><dt>

 <span data-ttu-id="20342-157">**\_operación de escritura IRP \_**</span><span class="sxs-lookup"><span data-stu-id="20342-157">**IRP\_WRITE\_OPERATION**</span></span>
</dt><span id="__IRP_CLOSE_OPERATION"></span><span id="__irp_close_operation"></span><dt>

 <span data-ttu-id="20342-158">**\_operación de cierre IRP \_**</span><span class="sxs-lookup"><span data-stu-id="20342-158">**IRP\_CLOSE\_OPERATION**</span></span>
</dt><span id="__IRP_DEFER_IO_COMPLETION"></span><span id="__irp_defer_io_completion"></span><dt>

 <span data-ttu-id="20342-159">**IRP \_ aplazar \_ finalización de e/s \_**</span><span class="sxs-lookup"><span data-stu-id="20342-159">**IRP\_DEFER\_IO\_COMPLETION**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="20342-160">**IssuingThreadId**</span><span class="sxs-lookup"><span data-stu-id="20342-160">**IssuingThreadId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20342-161">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="20342-161">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="20342-162">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="20342-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20342-163">Calificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (9)</span><span class="sxs-lookup"><span data-stu-id="20342-163">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (9)</span></span>
</dt> </dl>

<span data-ttu-id="20342-164">Identificador del subproceso que se emite.</span><span class="sxs-lookup"><span data-stu-id="20342-164">The identifier of the issuing thread.</span></span>

<span data-ttu-id="20342-165">**Windows server 2008 R2, Windows server 2008, Windows 7, Windows Vista, Windows server 2003 con SP1, Windows server 2003, windows 2000 Server y windows 2000 Professional:** Esta propiedad no se admite.</span><span class="sxs-lookup"><span data-stu-id="20342-165">**Windows Server 2008 R2, Windows Server 2008, Windows 7, Windows Vista, Windows Server 2003 with SP1, Windows Server 2003, Windows 2000 Server and Windows 2000 Professional:** This property is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="20342-166">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="20342-166">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20342-167">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="20342-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="20342-168">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="20342-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20342-169">Calificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (4)</span><span class="sxs-lookup"><span data-stu-id="20342-169">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (4)</span></span>
</dt> </dl>

<span data-ttu-id="20342-170">Reservado.</span><span class="sxs-lookup"><span data-stu-id="20342-170">Reserved.</span></span>

<span data-ttu-id="20342-171">**Windows server 2008 R2, Windows server 2008 y Windows 7:** El nombre de la propiedad es **QueueDepth**, que contiene el recuento de TICs de CPU desde el principio de la operación hasta el final de la operación.</span><span class="sxs-lookup"><span data-stu-id="20342-171">**Windows Server 2008 R2, Windows Server 2008 and Windows 7:** The name of the property is **QueueDepth**, which contains the CPU tick count from the beginning of the operation to the end of the operation.</span></span> <span data-ttu-id="20342-172">Tenga en cuenta que este valor puede desbordarse.</span><span class="sxs-lookup"><span data-stu-id="20342-172">Note that this value can overflow.</span></span>

<span data-ttu-id="20342-173">**Windows Vista, Windows server 2003 con SP1, Windows server 2003, windows 2000 Server y windows 2000 Professional:** El nombre de la propiedad es **ResponseTime**, que contiene el recuento de TICs de CPU desde el principio de la operación hasta el final de la operación.</span><span class="sxs-lookup"><span data-stu-id="20342-173">**Windows Vista, Windows Server 2003 with SP1, Windows Server 2003, Windows 2000 Server and Windows 2000 Professional:** The name of the property is **ResponseTime**, which contains the CPU tick count from the beginning of the operation to the end of the operation.</span></span> <span data-ttu-id="20342-174">Tenga en cuenta que este valor puede desbordarse.</span><span class="sxs-lookup"><span data-stu-id="20342-174">Note that this value can overflow.</span></span>

</dd> <dt>

<span data-ttu-id="20342-175">**Transferir**</span><span class="sxs-lookup"><span data-stu-id="20342-175">**TransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20342-176">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="20342-176">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="20342-177">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="20342-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20342-178">Calificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)</span><span class="sxs-lookup"><span data-stu-id="20342-178">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)</span></span>
</dt> </dl>

<span data-ttu-id="20342-179">Tamaño de los datos leídos o escritos desde el disco, en bytes.</span><span class="sxs-lookup"><span data-stu-id="20342-179">Size of data read to or written from disk, in bytes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="20342-180">Observaciones</span><span class="sxs-lookup"><span data-stu-id="20342-180">Remarks</span></span>

<span data-ttu-id="20342-181">Windows Server 2003 usa la siguiente definición para la clase de tipo de evento **desmontaje \_ TypeGroup1** .</span><span class="sxs-lookup"><span data-stu-id="20342-181">Windows Server 2003 uses the following definition for the **DiskIo\_TypeGroup1** event type class.</span></span>

``` syntax
[EventType{10, 11}, EventTypeName{"Read", "Write"}]
class DiskIo_TypeGroup1 : DiskIo
{
    [WmiDataId(1), read] uint32 DiskNumber;
    [WmiDataId(2), format("x"), read] uint32 IrpFlags;
    [WmiDataId(3), read] uint32 TransferSize;
    [WmiDataId(4), read] uint32 ResponseTime;
    [WmiDataId(5), read] uint64 ByteOffset;
    [WmiDataId(6), pointer, read] uint32 FileObject;
    [WmiDataId(7), read] uint64 HighResResponseTime;
};
```

<span data-ttu-id="20342-182">La propiedad **ResponseTime** contiene el recuento de TICs de la CPU desde el principio de la operación hasta el final de la operación.</span><span class="sxs-lookup"><span data-stu-id="20342-182">The **ResponseTime** property contains the CPU tick count from the beginning of the operation to the end of the operation.</span></span> <span data-ttu-id="20342-183">Tenga en cuenta que este valor puede desbordarse.</span><span class="sxs-lookup"><span data-stu-id="20342-183">Note that this value can overflow.</span></span>

<span data-ttu-id="20342-184">No se admite la propiedad **HighResResponseTime** .</span><span class="sxs-lookup"><span data-stu-id="20342-184">The **HighResResponseTime** property is not supported.</span></span>

<span data-ttu-id="20342-185">Windows Server 2003 con SP1 y Windows Vista usan la siguiente definición para la clase de tipo de evento **desmontaje \_ TypeGroup1** .</span><span class="sxs-lookup"><span data-stu-id="20342-185">Windows Server 2003 with SP1 and Windows Vista uses the following definition for the **DiskIo\_TypeGroup1** event type class.</span></span>

``` syntax
[EventType{10, 11}, EventTypeName{"Read", "Write"}]
class DiskIo_TypeGroup1 : DiskIo
{
    [WmiDataId(1), read] uint32 DiskNumber;
    [WmiDataId(2), format("x"), read] uint32 IrpFlags;
    [WmiDataId(3), read] uint32 TransferSize;
    [WmiDataId(4), read] uint32 ResponseTime;
    [WmiDataId(5), read] uint64 ByteOffset;
    [WmiDataId(6), pointer, read] uint32 FileObject;
    [WmiDataId(7), pointer, read] uint32 Irp;
    [WmiDataId(8), read] uint64 HighResResponseTime;
};
```

<span data-ttu-id="20342-186">La propiedad **IRP** es el paquete de solicitud de e/s.</span><span class="sxs-lookup"><span data-stu-id="20342-186">The **Irp** property is the I/O request packet.</span></span> <span data-ttu-id="20342-187">Esta propiedad identifica la actividad de e/s.</span><span class="sxs-lookup"><span data-stu-id="20342-187">This property identifies the I/O activity.</span></span> <span data-ttu-id="20342-188">Puede usar esta propiedad con los eventos [**de \_ TypeGroup2 de desmontaje**](diskio-typegroup2.md) para correlacionar el tiempo de respuesta.</span><span class="sxs-lookup"><span data-stu-id="20342-188">You can use this property with the [**DiskIo\_TypeGroup2**](diskio-typegroup2.md) events to correlate response time.</span></span>

<span data-ttu-id="20342-189">Se admite la propiedad **HighResResponseTime** .</span><span class="sxs-lookup"><span data-stu-id="20342-189">The **HighResResponseTime** property is supported.</span></span> <span data-ttu-id="20342-190">La propiedad contiene el tiempo entre el inicio y la finalización de e/s medido por PartitionManager (en las unidades KeQueryPerformanceCounter).</span><span class="sxs-lookup"><span data-stu-id="20342-190">The property contains the time between I/O initiation and completion as measured by PartitionManager (in the KeQueryPerformanceCounter units).</span></span> <span data-ttu-id="20342-191">Utilice esta propiedad en lugar de la propiedad **ResponseTime** para determinar el tiempo de respuesta de e/s de disco.</span><span class="sxs-lookup"><span data-stu-id="20342-191">Use this property instead of the **ResponseTime** property to determine the disk I/O response time.</span></span>

## <a name="requirements"></a><span data-ttu-id="20342-192">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20342-192">Requirements</span></span>



| <span data-ttu-id="20342-193">Requisito</span><span class="sxs-lookup"><span data-stu-id="20342-193">Requirement</span></span> | <span data-ttu-id="20342-194">Value</span><span class="sxs-lookup"><span data-stu-id="20342-194">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="20342-195">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="20342-195">Minimum supported client</span></span><br/> | <span data-ttu-id="20342-196">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="20342-196">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="20342-197">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="20342-197">Minimum supported server</span></span><br/> | <span data-ttu-id="20342-198">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="20342-198">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="20342-199">Vea también</span><span class="sxs-lookup"><span data-stu-id="20342-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20342-200">**Desmontaje**</span><span class="sxs-lookup"><span data-stu-id="20342-200">**DiskIo**</span></span>](diskio.md)
</dt> </dl>

 

 
