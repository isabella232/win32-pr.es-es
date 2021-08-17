---
description: Esta clase es la clase de tipo de evento para los eventos de E/S de disco. La sintaxis siguiente se simplifica a partir del código MOF.
ms.assetid: fe7d4efa-3d39-4438-a1a6-af3f65ea3deb
title: DiskIo_TypeGroup1 clase
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
ms.openlocfilehash: 3a69643602a59fa7be8cd844f3f2908c92e2e08545f7444d1002ec1542b36730
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117814981"
---
# <a name="diskio_typegroup1-class"></a>DiskIo \_ TypeGroup1 (clase)

Esta clase es la clase de tipo de evento para los eventos de E/S de disco.

La sintaxis siguiente se simplifica a partir del código MOF.

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

La **clase DiskIo \_ TypeGroup1** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase DiskIo \_ TypeGroup1** tiene estas propiedades.

<dl> <dt>

**ByteOffset**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (5)
</dt> </dl>

Desplazamiento de bytes desde el principio del disco físico.

</dd> <dt>

**DiskNumber**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)
</dt> </dl>

Número que identifica el disco físico.

</dd> <dt>

**FileObject**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (6), [**Pointer**](event-tracing-mof-qualifiers.md)
</dt> </dl>

Coincide con el valor de este puntero con el valor del puntero **FileObject** en un evento [**FileIo \_ Name**](fileio-name.md) para determinar el archivo implicado en la operación de E/S.

</dd> <dt>

**HighResResponseTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (8)
</dt> </dl>

Tiempo entre el inicio y la finalización de E/S medido por el administrador de particiones (en las unidades de tic [**KeQueryPerformanceCounter).**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-kequeryperformancecounter)

**Windows Server 2003:** Esta propiedad tiene un [**valor WmiDataId**](event-tracing-mof-qualifiers.md) de 7.

**Windows 2000 Server y Windows 2000 Professional:** Esta propiedad no se admite.

</dd> <dt>

**Irp**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (7), [**Pointer**](event-tracing-mof-qualifiers.md)
</dt> </dl>

El paquete de solicitud de E/S, que identifica la actividad de E/S.

**Windows Server 2003, Windows 2000 Server y Windows 2000 Professional:** Esta propiedad no se admite.

</dd> <dt>

**IrpFlags**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (2), [**Format**](event-tracing-mof-qualifiers.md) ("x")
</dt> </dl>

Puede contener una o varias de las siguientes marcas de paquetes de solicitud de E/S (definidas en Ntddk.h, que es un archivo de encabezado DDK):

<dl><span id="__IRP_NOCACHE"></span><span id="__irp_nocache"></span><dt>

 **IRP \_ NOCACHE**
</dt><span id="__IRP_PAGING_IO"></span><span id="__irp_paging_io"></span><dt>

 **E/S \_ DE PAGINACIÓN DE \_ IRP**
</dt><span id="__IRP_MOUNT_COMPLETION"></span><span id="__irp_mount_completion"></span><dt>

 **FINALIZACIÓN DEL MONTAJE DE IRP \_ \_**
</dt><span id="__IRP_SYNCHRONOUS_API"></span><span id="__irp_synchronous_api"></span><dt>

 **API \_ SINCRÓNICA de IRP \_**
</dt><span id="__IRP_ASSOCIATED_IRP"></span><span id="__irp_associated_irp"></span><dt>

 **IRP \_ ASOCIADO \_ A IRP**
</dt><span id="__IRP_BUFFERED_IO"></span><span id="__irp_buffered_io"></span><dt>

 **E/S EN BÚFER DE IRP \_ \_**
</dt><span id="IRP_DEALLOCATE_BUFFER"></span><span id="irp_deallocate_buffer"></span><dt>

**BÚFER DE \_ DESASIGNAR IRP \_**
</dt><span id="__IRP_INPUT_OPERATION"></span><span id="__irp_input_operation"></span><dt>

 **OPERACIÓN DE ENTRADA \_ DE \_ IRP**
</dt><span id="__IRP_SYNCHRONOUS_PAGING_IO"></span><span id="__irp_synchronous_paging_io"></span><dt>

 **E/S \_ DE \_ PAGINACIÓN SINCRÓNICA DE IRP \_**
</dt><span id="__IRP_CREATE_OPERATION"></span><span id="__irp_create_operation"></span><dt>

 **OPERACIÓN CREATE DE IRP \_ \_**
</dt><span id="IRP_READ_OPERATION"></span><span id="irp_read_operation"></span><dt>

**OPERACIÓN DE \_ LECTURA DE \_ IRP**
</dt><span id="__IRP_WRITE_OPERATION"></span><span id="__irp_write_operation"></span><dt>

 **OPERACIÓN DE ESCRITURA \_ DE \_ IRP**
</dt><span id="__IRP_CLOSE_OPERATION"></span><span id="__irp_close_operation"></span><dt>

 **OPERACIÓN DE \_ CIERRE DE \_ IRP**
</dt><span id="__IRP_DEFER_IO_COMPLETION"></span><span id="__irp_defer_io_completion"></span><dt>

 **IRP \_ DEFER \_ IO \_ COMPLETION**
</dt> </dl>

</dd> <dt>

**IssuingThreadId**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (9)
</dt> </dl>

Identificador del subproceso emisor.

**Windows Server 2008 R2, Windows Server 2008, Windows 7, Windows Vista, Windows Server 2003 con SP1, Windows Server 2003, Windows 2000 Server y Windows 2000 Professional:** Esta propiedad no se admite.

</dd> <dt>

**Reserved**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (4)
</dt> </dl>

Reservado.

**Windows Server 2008 R2, Windows Server 2008 y Windows 7:** El nombre de la propiedad es **QueueDepth,** que contiene el recuento de tics de CPU desde el principio de la operación hasta el final de la operación. Tenga en cuenta que este valor puede desbordarse.

**Windows Vista, Windows Server 2003 con SP1, Windows Server 2003, Windows 2000 Server y Windows 2000 Professional:** El nombre de la propiedad es **ResponseTime**, que contiene el recuento de tics de CPU desde el principio de la operación hasta el final de la operación. Tenga en cuenta que este valor puede desbordarse.

</dd> <dt>

**TransferSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)
</dt> </dl>

Tamaño de los datos leídos o escritos desde el disco, en bytes.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Windows Server 2003 usa la siguiente definición para la clase de tipo de evento **\_ DiskIo TypeGroup1.**

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

La **propiedad ResponseTime** contiene el recuento de tics de CPU desde el principio de la operación hasta el final de la operación. Tenga en cuenta que este valor puede desbordarse.

No **se admite la propiedad HighResResponseTime.**

Windows Server 2003 con SP1 y Windows Vista usa la siguiente definición para la clase de tipo de evento **DiskIo \_ TypeGroup1.**

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

La **propiedad Irp** es el paquete de solicitud de E/S. Esta propiedad identifica la actividad de E/S. Puede usar esta propiedad con los eventos [**DiskIo \_ TypeGroup2**](diskio-typegroup2.md) para correlacionar el tiempo de respuesta.

Se **admite la propiedad HighResResponseTime.** La propiedad contiene el tiempo entre el inicio y la finalización de E/S medido por PartitionManager (en las unidades KeQueryPerformanceCounter). Use esta propiedad en lugar de la **propiedad ResponseTime** para determinar el tiempo de respuesta de E/S del disco.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**DiskIo**](diskio.md)
</dt> </dl>

 

 
