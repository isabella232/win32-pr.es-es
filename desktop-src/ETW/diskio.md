---
description: Esta clase es la clase primaria para los eventos de E/S de disco. La sintaxis siguiente se simplifica a partir del código MOF.
ms.assetid: 630fb6c6-b505-4384-ab7b-ee898d95bd41
title: DiskIo (clase)
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
ms.openlocfilehash: 0e91f5e8b84d77b0938f35da69a84c26fa0f34a4da63bce40330484a29e19b5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118395306"
---
# <a name="diskio-class"></a>DiskIo (clase)

Esta clase es la clase primaria para los eventos de E/S de disco.

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Guid("{3d6fa8d4-fe05-11d0-9dda-00c04fd7ba7c}")]
class DiskIo : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Miembros

La **clase DiskIo** no define ningún miembro.

## <a name="remarks"></a>Comentarios

Para habilitar eventos de E/S de disco en una sesión de registro del kernel de NT, especifique la marca **EVENT TRACE FLAG DISK \_ \_ \_ \_ IO** en el **miembro EnableFlags** de una estructura [**EVENT TRACE \_ \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) al llamar a la [**función StartTrace.**](/windows/win32/api/evntrace/nf-evntrace-starttracea) También puede especificar una o varias de las marcas siguientes:

-   **E/S \_ DE \_ \_ \_ E/S DE DISCO \_ DE MARCA DE SEGUIMIENTO DE EVENTOS**
-   **CONTROLADOR DE \_ MARCA DE SEGUIMIENTO DE \_ \_ EVENTOS**

Los consumidores de seguimiento de eventos pueden implementar un procesamiento especial para eventos de E/S de disco llamando a la función [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) y especificando [**DiskIoGuid**](nt-kernel-logger-constants.md) como parámetro *pGuid.* Use los siguientes tipos de eventos para identificar el evento de E/S de disco real al consumir eventos.



| Tipo de evento                                                                      | Descripción                                                                                                                                                   |
|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EVENT \_ TRACE \_ TYPE \_ IO \_ READ**(el valor del tipo de evento es 10)<br/>             | Evento de lectura. La [**clase MOF \_ DiskIo TypeGroup1**](diskio-typegroup1.md) define los datos de evento para este evento.                                              |
| **EVENT \_ TRACE \_ TYPE \_ IO \_ WRITE**(el valor del tipo de evento es 11)<br/>            | Evento de escritura. La [**clase MOF \_ DiskIo TypeGroup1**](diskio-typegroup1.md) define los datos de evento para este evento.                                             |
| **EVENT \_ TRACE \_ TYPE IO READ \_ \_ \_ INIT**(el valor del tipo de evento es 12)<br/>       | Inicializar evento de lectura. La [**clase MOF DiskIo \_ TypeGroup2**](diskio-typegroup2.md) define los datos de evento para este evento.                                   |
| **EVENT \_ TRACE \_ TYPE IO WRITE \_ \_ \_ INIT**(el valor del tipo de evento es 13)<br/>      | Inicializar evento de escritura. La [**clase MOF DiskIo \_ TypeGroup2**](diskio-typegroup2.md) define los datos de evento para este evento.                                  |
| **EVENT \_ TRACE \_ TYPE \_ IO \_ FLUSH**(el valor del tipo de evento es 14)<br/>            | Inicializar evento de escritura. La [**clase MOF DiskIo \_ TypeGroup3**](diskio-typegroup3.md) define los datos de evento para este evento.                                  |
| **EVENT \_ TRACE \_ TYPE IO FLUSH \_ \_ \_ INIT**(el valor del tipo de evento es 15)<br/>      | Inicializar evento de vaciado. La [**clase MOF DiskIo \_ TypeGroup2**](diskio-typegroup2.md) define los datos de evento para este evento.                                  |
| **EVENT \_ TRACE \_ TYPE IO REDIRECTED \_ \_ \_ INIT**(el valor del tipo de evento es 16)<br/> | Inicializar evento redirigido. Los eventos de E/S redirigidos se usan para asignar E/S de disco a Windows Imaging Format (WIM) al nombre de archivo dentro de WIM.                  |
| El valor del tipo de evento es 52<br/>                                               | Evento de solicitud completa del controlador. La [**clase MOF DriverCompleteRequest**](drivercompleterequest.md) define los datos de evento para este evento.                    |
| El valor del tipo de evento es 53<br/>                                               | Evento de devolución de solicitud completa del controlador. La clase MOF [**DriverCompleteRequestReturn**](drivercompleterequestreturn.md) define los datos de evento para este evento. |
| El valor del tipo de evento es 37<br/>                                               | Evento de rutina de finalización del controlador. La [**clase MOF DriverCompletionRoutine**](drivercompletionroutine.md) define los datos de evento para este evento.              |
| El valor del tipo de evento es 34<br/>                                               | Evento de llamada a la función principal del controlador. La [**clase MOF DriverMajorFunctionCall**](drivermajorfunctioncall.md) define los datos de evento para este evento.             |
| El valor del tipo de evento es 35<br/>                                               | Evento de devolución de llamada de función principal del controlador. La clase MOF [**DriverMajorFunctionReturn**](drivermajorfunctionreturn.md) define los datos de evento para este evento.  |



 

El proveedor de E/S de disco no puede identificar qué archivo se lee o escribe durante un evento de E/S de disco. Para recuperar el nombre del archivo asociado al evento de E/S de disco, habilite el proveedor de eventos de E/S de archivo.

Los eventos de E/S de disco se registran en el momento de finalización de E/S. Para determinar cuándo comenzó la operación de E/S, use los eventos de inicialización, por ejemplo, EVENT \_ TRACE TYPE IO READ \_ \_ \_ \_ INIT.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**DiskIo \_ TypeGroup1**](diskio-typegroup1.md)
</dt> <dt>

[**DiskIo \_ TypeGroup2**](diskio-typegroup2.md)
</dt> <dt>

[**DiskIo \_ TypeGroup3**](diskio-typegroup3.md)
</dt> <dt>

[**DriverCompleteRequest**](drivercompleterequest.md)
</dt> <dt>

[**DriverCompleteRequestReturn**](drivercompleterequestreturn.md)
</dt> <dt>

[**DriverCompletionRoutine**](drivercompletionroutine.md)
</dt> <dt>

[**DriverMajorFunctionCall**](drivermajorfunctioncall.md)
</dt> <dt>

[**DriverMajorFunctionReturn**](drivermajorfunctionreturn.md)
</dt> </dl>

 

 
