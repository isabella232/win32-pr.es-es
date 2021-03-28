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
# <a name="diskio_typegroup3-class"></a>Desmontaje \_ TypeGroup3 (clase)

Esta clase es la clase de tipo de evento para eventos de vaciado de e/s de disco.

La siguiente sintaxis se simplifica desde el código MOF.

## <a name="syntax"></a>Sintaxis

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

## <a name="members"></a>Miembros

La clase **desmontaje \_ TypeGroup3** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **desmontaje \_ TypeGroup3** tiene estas propiedades.

<dl> <dt>

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

**HighResResponseTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)
</dt> </dl>

Recuento de TICs de CPU desde el principio de la operación hasta el final de la operación.

</dd> <dt>

**IRP**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (4), [**puntero**](event-tracing-mof-qualifiers.md)
</dt> </dl>

Paquete de solicitud de e/s. Esta propiedad identifica la actividad de e/s.

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

Calificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (5)
</dt> </dl>

Identificador del subproceso que se emite.

**Windows server 2008 R2, Windows server 2008, Windows 7 y Windows Vista:** Esta propiedad no se admite.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Desmontaje**](diskio.md)
</dt> </dl>

 

 




