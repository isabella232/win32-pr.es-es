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
# <a name="diskio_typegroup1-class"></a>Desmontaje \_ TypeGroup1 (clase)

Esta clase es la clase de tipo de evento para los eventos de e/s de disco.

La siguiente sintaxis se simplifica desde el código MOF.

## <a name="syntax"></a>Sintaxis

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

## <a name="members"></a>Miembros

La clase **desmontaje \_ TypeGroup1** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **desmontaje \_ TypeGroup1** tiene estas propiedades.

<dl> <dt>

**Byteoffset (**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (5)
</dt> </dl>

Desplazamiento de bytes desde el principio del disco físico.

</dd> <dt>

**Númerodedisco corresponde**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)
</dt> </dl>

Número que identifica el disco físico.

</dd> <dt>

**FileObject**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (6), [**puntero**](event-tracing-mof-qualifiers.md)
</dt> </dl>

Haga coincidir el valor de este puntero con el valor de puntero de **FileObject** en un evento de [**\_ nombre FileIo**](fileio-name.md) para determinar el archivo implicado en la operación de e/s.

</dd> <dt>

**HighResResponseTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (8)
</dt> </dl>

Tiempo transcurrido entre el inicio y la finalización de e/s medido por el administrador de particiones (en las unidades de paso [**KeQueryPerformanceCounter**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-kequeryperformancecounter) ).

**Windows Server 2003:** Esta propiedad tiene un valor de [**WmiDataId**](event-tracing-mof-qualifiers.md) de 7.

**Windows 2000 Server y windows 2000 Professional:** Esta propiedad no se admite.

</dd> <dt>

**IRP**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (7), [**puntero**](event-tracing-mof-qualifiers.md)
</dt> </dl>

El paquete de solicitud de e/s, que identifica la actividad de e/s.

**Windows server 2003, windows 2000 Server y windows 2000 Professional:** Esta propiedad no se admite.

</dd> <dt>

**IrpFlags**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (2), [**Format**](event-tracing-mof-qualifiers.md) ("x")
</dt> </dl>

Puede contener una o varias de las siguientes marcas de paquete de solicitud de e/s (definidas en Ntddk. h, que es un archivo de encabezado de DDK):

<dl><span id="__IRP_NOCACHE"></span><span id="__irp_nocache"></span><dt>

 **IRP \_ NOcache**
</dt><span id="__IRP_PAGING_IO"></span><span id="__irp_paging_io"></span><dt>

 **\_ \_ e/s de PAGINAción IRP**
</dt><span id="__IRP_MOUNT_COMPLETION"></span><span id="__irp_mount_completion"></span><dt>

 **\_finalización de montaje IRP \_**
</dt><span id="__IRP_SYNCHRONOUS_API"></span><span id="__irp_synchronous_api"></span><dt>

 **\_API sincrónica IRP \_**
</dt><span id="__IRP_ASSOCIATED_IRP"></span><span id="__irp_associated_irp"></span><dt>

 **\_IRP asociado de IRP \_**
</dt><span id="__IRP_BUFFERED_IO"></span><span id="__irp_buffered_io"></span><dt>

 **\_ \_ e/s de búfer IRP**
</dt><span id="IRP_DEALLOCATE_BUFFER"></span><span id="irp_deallocate_buffer"></span><dt>

**\_búfer de DESasignación de IRP \_**
</dt><span id="__IRP_INPUT_OPERATION"></span><span id="__irp_input_operation"></span><dt>

 **\_operación de entrada IRP \_**
</dt><span id="__IRP_SYNCHRONOUS_PAGING_IO"></span><span id="__irp_synchronous_paging_io"></span><dt>

 **\_ \_ e/s de paginación sincrónica IRP \_**
</dt><span id="__IRP_CREATE_OPERATION"></span><span id="__irp_create_operation"></span><dt>

 **\_operación de creación de IRP \_**
</dt><span id="IRP_READ_OPERATION"></span><span id="irp_read_operation"></span><dt>

**\_operación de lectura IRP \_**
</dt><span id="__IRP_WRITE_OPERATION"></span><span id="__irp_write_operation"></span><dt>

 **\_operación de escritura IRP \_**
</dt><span id="__IRP_CLOSE_OPERATION"></span><span id="__irp_close_operation"></span><dt>

 **\_operación de cierre IRP \_**
</dt><span id="__IRP_DEFER_IO_COMPLETION"></span><span id="__irp_defer_io_completion"></span><dt>

 **IRP \_ aplazar \_ finalización de e/s \_**
</dt> </dl>

</dd> <dt>

**IssuingThreadId**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (9)
</dt> </dl>

Identificador del subproceso que se emite.

**Windows server 2008 R2, Windows server 2008, Windows 7, Windows Vista, Windows server 2003 con SP1, Windows server 2003, windows 2000 Server y windows 2000 Professional:** Esta propiedad no se admite.

</dd> <dt>

**Reserved**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (4)
</dt> </dl>

Reservado.

**Windows server 2008 R2, Windows server 2008 y Windows 7:** El nombre de la propiedad es **QueueDepth**, que contiene el recuento de TICs de CPU desde el principio de la operación hasta el final de la operación. Tenga en cuenta que este valor puede desbordarse.

**Windows Vista, Windows server 2003 con SP1, Windows server 2003, windows 2000 Server y windows 2000 Professional:** El nombre de la propiedad es **ResponseTime**, que contiene el recuento de TICs de CPU desde el principio de la operación hasta el final de la operación. Tenga en cuenta que este valor puede desbordarse.

</dd> <dt>

**Transferir**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)
</dt> </dl>

Tamaño de los datos leídos o escritos desde el disco, en bytes.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Windows Server 2003 usa la siguiente definición para la clase de tipo de evento **desmontaje \_ TypeGroup1** .

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

La propiedad **ResponseTime** contiene el recuento de TICs de la CPU desde el principio de la operación hasta el final de la operación. Tenga en cuenta que este valor puede desbordarse.

No se admite la propiedad **HighResResponseTime** .

Windows Server 2003 con SP1 y Windows Vista usan la siguiente definición para la clase de tipo de evento **desmontaje \_ TypeGroup1** .

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

La propiedad **IRP** es el paquete de solicitud de e/s. Esta propiedad identifica la actividad de e/s. Puede usar esta propiedad con los eventos [**de \_ TypeGroup2 de desmontaje**](diskio-typegroup2.md) para correlacionar el tiempo de respuesta.

Se admite la propiedad **HighResResponseTime** . La propiedad contiene el tiempo entre el inicio y la finalización de e/s medido por PartitionManager (en las unidades KeQueryPerformanceCounter). Utilice esta propiedad en lugar de la propiedad **ResponseTime** para determinar el tiempo de respuesta de e/s de disco.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Desmontaje**](diskio.md)
</dt> </dl>

 

 
