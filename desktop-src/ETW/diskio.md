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
# <a name="diskio-class"></a>Clase desmontaje

Esta clase es la clase primaria para los eventos de e/s de disco.

La siguiente sintaxis se simplifica desde el código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Guid("{3d6fa8d4-fe05-11d0-9dda-00c04fd7ba7c}")]
class DiskIo : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Miembros

La clase **Desmontaje** no define ningún miembro.

## <a name="remarks"></a>Observaciones

Para habilitar los eventos de e/s de disco en una sesión de registro del kernel de NT, especifique la marca de  e/s de disco de la marca de seguimiento de **eventos \_ \_ \_ \_** en el miembro EnableFlags de una estructura de [**\_ \_ propiedades de seguimiento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) al llamar a la función [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) . También puede especificar una o varias de las marcas siguientes:

-   **marca de seguimiento de eventos \_ \_ \_ init de \_ e/s de disco \_**
-   **\_controlador de \_ marca de seguimiento de eventos \_**

Los consumidores de seguimiento de eventos pueden implementar un procesamiento especial para los eventos de e/s de disco llamando a la función [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) y especificando [**DiskIoGuid**](nt-kernel-logger-constants.md) como parámetro *pGuid* . Utilice los siguientes tipos de eventos para identificar el evento de e/s de disco real al consumir eventos.



| Tipo de evento                                                                      | Descripción                                                                                                                                                   |
|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Evento \_ de Tipo de seguimiento de \_ \_ e/s \_ leída**(el valor de tipo de evento es 10)<br/>             | Evento de lectura. La clase MOF [**desmontaje \_ TypeGroup1**](diskio-typegroup1.md) define los datos de evento para este evento.                                              |
| **Evento \_ de Tipo de seguimiento de \_ \_ \_ escritura de e/s**(el valor de tipo de evento es 11)<br/>            | Escribir evento. La clase MOF [**desmontaje \_ TypeGroup1**](diskio-typegroup1.md) define los datos de evento para este evento.                                             |
| **Evento \_ de Tipo de seguimiento \_ \_ IO \_ Read \_ init**(el valor del tipo de evento es 12)<br/>       | Inicializar evento de lectura. La clase MOF [**desmontaje \_ TypeGroup2**](diskio-typegroup2.md) define los datos de evento para este evento.                                   |
| **Evento \_ de Tipo de seguimiento \_ \_ IO \_ Write \_ init**(el valor del tipo de evento es 13)<br/>      | Inicializar evento de escritura. La clase MOF [**desmontaje \_ TypeGroup2**](diskio-typegroup2.md) define los datos de evento para este evento.                                  |
| **Evento \_ de \_ \_ \_ Vaciar el tipo de seguimiento de e/s**(el valor del tipo de evento es 14)<br/>            | Inicializar evento de escritura. La clase MOF [**desmontaje \_ TypeGroup3**](diskio-typegroup3.md) define los datos de evento para este evento.                                  |
| **Evento \_ de Tipo de seguimiento de \_ \_ \_ \_ inicialización de salida de e/s**(el valor de tipo de evento es 15)<br/>      | Inicializar evento de vaciado. La clase MOF [**desmontaje \_ TypeGroup2**](diskio-typegroup2.md) define los datos de evento para este evento.                                  |
| **Evento \_ de \_Tipo de \_ seguimiento \_ redireccionado \_ init**(el valor de tipo de evento es 16)<br/> | Inicializar evento redirigido. Los eventos de e/s Redirigido se usan para asignar las e/s de disco a un formato de imagen de Windows (WIM) al nombre de archivo en WIM.                  |
| El valor del tipo de evento es 52<br/>                                               | Evento de solicitud de finalización de controlador. La clase MOF [**DriverCompleteRequest**](drivercompleterequest.md) define los datos de evento para este evento.                    |
| El valor del tipo de evento es 53<br/>                                               | Evento de devolución de solicitud de finalización de controlador. La clase MOF [**DriverCompleteRequestReturn**](drivercompleterequestreturn.md) define los datos de evento para este evento. |
| El valor del tipo de evento es 37<br/>                                               | Evento de rutina de finalización de controlador. La clase MOF [**DriverCompletionRoutine**](drivercompletionroutine.md) define los datos de evento para este evento.              |
| El valor del tipo de evento es 34<br/>                                               | Evento de llamada de función principal de controlador. La clase MOF [**DriverMajorFunctionCall**](drivermajorfunctioncall.md) define los datos de evento para este evento.             |
| El valor del tipo de evento es 35<br/>                                               | Evento de devolución de llamada de función principal de controlador. La clase MOF [**DriverMajorFunctionReturn**](drivermajorfunctionreturn.md) define los datos de evento para este evento.  |



 

El proveedor de e/s de disco no puede identificar el archivo que se lee o escribe durante un evento de e/s de disco. Para recuperar el nombre del archivo asociado al evento de e/s de disco, habilite el proveedor de eventos I/0 de archivo.

Los eventos de e/s de disco se registran en la hora de finalización de e/s. Para determinar Cuándo comenzó la operación de e/s, use los eventos de inicialización, por ejemplo, el tipo de seguimiento de eventos \_ \_ \_ IO \_ Read \_ init.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Desmontaje \_ TypeGroup1**](diskio-typegroup1.md)
</dt> <dt>

[**Desmontaje \_ TypeGroup2**](diskio-typegroup2.md)
</dt> <dt>

[**Desmontaje \_ TypeGroup3**](diskio-typegroup3.md)
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

 

 
