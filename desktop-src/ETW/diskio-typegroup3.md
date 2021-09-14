---
description: Esta clase es la clase de tipo de evento para los eventos de vaciado de E/S de disco. La sintaxis siguiente se simplifica a partir del código MOF.
ms.assetid: 7f0c9bd4-e4d3-49c1-ae72-f6bdf938099f
title: DiskIo_TypeGroup3 clase
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127255056"
---
# <a name="diskio_typegroup3-class"></a>Clase \_ TypeGroup3 de DiskIo

Esta clase es la clase de tipo de evento para los eventos de vaciado de E/S de disco.

La sintaxis siguiente se simplifica a partir del código MOF.

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

## <a name="members"></a>Members

La **clase DiskIo \_ TypeGroup3** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase DiskIo \_ TypeGroup3** tiene estas propiedades.

<dl> <dt>

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

**HighResResponseTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)
</dt> </dl>

Recuento de tics de CPU desde el principio de la operación hasta el final de la operación.

</dd> <dt>

**Irp**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (4), [**Pointer**](event-tracing-mof-qualifiers.md)
</dt> </dl>

Paquete de solicitud de E/S. Esta propiedad identifica la actividad de E/S.

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

 **E/S \_ DE PAGINACIÓN \_ DE IRP**
</dt><span id="__IRP_MOUNT_COMPLETION"></span><span id="__irp_mount_completion"></span><dt>

 **FINALIZACIÓN DEL MONTAJE DE IRP \_ \_**
</dt><span id="__IRP_SYNCHRONOUS_API"></span><span id="__irp_synchronous_api"></span><dt>

 **API \_ SINCRÓNICA DE IRP \_**
</dt><span id="__IRP_ASSOCIATED_IRP"></span><span id="__irp_associated_irp"></span><dt>

 **IRP \_ ASOCIADO \_ A IRP**
</dt><span id="__IRP_BUFFERED_IO"></span><span id="__irp_buffered_io"></span><dt>

 **E/S EN BÚFER DE IRP \_ \_**
</dt><span id="IRP_DEALLOCATE_BUFFER"></span><span id="irp_deallocate_buffer"></span><dt>

**BÚFER DE \_ DESASIGNAR IRP \_**
</dt><span id="__IRP_INPUT_OPERATION"></span><span id="__irp_input_operation"></span><dt>

 **OPERACIÓN DE \_ ENTRADA DE \_ IRP**
</dt><span id="__IRP_SYNCHRONOUS_PAGING_IO"></span><span id="__irp_synchronous_paging_io"></span><dt>

 **E/S \_ DE \_ PAGINACIÓN SINCRÓNICA \_ DE IRP**
</dt><span id="__IRP_CREATE_OPERATION"></span><span id="__irp_create_operation"></span><dt>

 **OPERACIÓN DE CREACIÓN DE IRP \_ \_**
</dt><span id="IRP_READ_OPERATION"></span><span id="irp_read_operation"></span><dt>

**OPERACIÓN DE \_ LECTURA DE \_ IRP**
</dt><span id="__IRP_WRITE_OPERATION"></span><span id="__irp_write_operation"></span><dt>

 **OPERACIÓN DE \_ ESCRITURA DE \_ IRP**
</dt><span id="__IRP_CLOSE_OPERATION"></span><span id="__irp_close_operation"></span><dt>

 **OPERACIÓN DE \_ CIERRE DE \_ IRP**
</dt><span id="__IRP_DEFER_IO_COMPLETION"></span><span id="__irp_defer_io_completion"></span><dt>

 **IRP \_ APLAZAR LA \_ FINALIZACIÓN DE \_ E/S**
</dt> </dl>

</dd> <dt>

**IssuingThreadId**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (5)
</dt> </dl>

Identificador del subproceso emisor.

**Windows Server 2008 R2, Windows Server 2008, Windows 7 y Windows Vista:** Esta propiedad no se admite.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**DiskIo**](diskio.md)
</dt> </dl>

 

 




