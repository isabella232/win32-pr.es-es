---
description: Esta clase es la clase primaria para los eventos de e/s de archivo. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 8e006a63-a061-4b62-8f90-b8c8823bb047
title: FileIo (clase)
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
ms.openlocfilehash: 2f7c032cb7af325efa1d2ea76702068fc7b3be62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985086"
---
# <a name="fileio-class"></a>FileIo (clase)

Esta clase es la clase primaria para los eventos de e/s de archivo.

La siguiente sintaxis se simplifica desde el código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Guid("{90cbdc39-4a3e-11d1-84f4-0000f80464e3}"), EventVersion(2)]
class FileIo : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Miembros

La clase **FileIo** no define ningún miembro.

## <a name="remarks"></a>Observaciones

Para habilitar los eventos de e/s de archivo en una sesión de registro del kernel de NT, especifique el indicador de **\_ \_ \_ \_ \_ e/s de archivo de disco de marca de seguimiento de eventos** en el miembro **EnableFlags** de una estructura de [**\_ \_ propiedades de seguimiento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) al llamar a la función [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) . También puede especificar una o varias de las marcas siguientes:

-   **\_ \_ \_ e/s de archivo de marca de seguimiento de eventos \_**
-   **\_inicial de \_ \_ \_ e/s de archivo de marca de seguimiento de eventos \_**

Los consumidores de seguimiento de eventos pueden implementar un procesamiento especial para los eventos de e/s de archivos llamando a la función [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) y especificando [**FileIoGuid**](nt-kernel-logger-constants.md) como parámetro *pGuid* . Utilice los siguientes tipos de eventos para identificar el evento real al consumir eventos.



| Tipo de evento             | Descripción                                                                                                                                                                             |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| El valor del tipo de evento es 0  | Evento de nombre de archivo. La clase de MOF [**\_ nombre de FileIo**](fileio-name.md) define los datos de evento para este evento.                                                                               |
| El valor del tipo de evento es 32 | Evento de creación de archivo. La clase de MOF [**\_ nombre de FileIo**](fileio-name.md) define los datos de evento para este evento.                                                                             |
| El valor del tipo de evento es 35 | Evento de eliminación de archivo. La clase de MOF [**\_ nombre de FileIo**](fileio-name.md) define los datos de evento para este evento.                                                                             |
| El valor del tipo de evento es 36 | Evento de detención de archivo. Enumera todos los archivos abiertos en el equipo al final de la sesión de seguimiento. La clase de MOF [**\_ nombre de FileIo**](fileio-name.md) define los datos de evento para este evento. |
| El valor del tipo de evento es 64 | Evento de creación de archivo. La clase [**FileIo \_ Create**](fileio-create.md) mof define los datos de evento para este evento.                                                                         |
| El valor del tipo de evento es 72 | Evento de enumeración de directorio. La clase de MOF [**\_ DirEnum de FileIo**](fileio-direnum.md) define los datos de evento para este evento.                                                             |
| El valor del tipo de evento es 77 | Evento de notificación de directorio. La clase de MOF [**\_ DirEnum de FileIo**](fileio-direnum.md) define los datos de evento para este evento.                                                            |
| El valor del tipo de evento es 69 | Evento de información de conjunto. La clase de MOF [**\_ info**](fileio-info.md) de la clase define los datos de evento para este evento.                                                                         |
| El valor del tipo de evento es 70 | Evento de eliminación de archivo. La clase de MOF [**\_ info**](fileio-info.md) de la clase define los datos de evento para este evento.                                                                             |
| El valor del tipo de evento es 71 | Evento de cambio de nombre de archivo. La clase de MOF [**\_ info**](fileio-info.md) de la clase define los datos de evento para este evento.                                                                             |
| El valor del tipo de evento es 74 | Evento de información de archivo de consulta. La clase de MOF [**\_ info**](fileio-info.md) de la clase define los datos de evento para este evento.                                                                  |
| El valor del tipo de evento es 75 | Evento de control del sistema de archivos. La clase de MOF [**\_ info**](fileio-info.md) de la clase define los datos de evento para este evento.                                                                     |
| El valor del tipo de evento es 76 | Evento de fin de operación. La clase MOF [**\_ abierta en FileIo**](fileio-opend.md) define los datos de evento para este evento.                                                                      |
| El valor del tipo de evento es 67 | Evento de lectura de archivo. La clase de MOF [**\_ ReadWrite ReadWrite**](fileio-readwrite.md) define los datos de evento para este evento.                                                                     |
| El valor del tipo de evento es 68 | Evento de escritura de archivo. La clase de MOF [**\_ ReadWrite ReadWrite**](fileio-readwrite.md) define los datos de evento para este evento.                                                                    |
| El valor del tipo de evento es 65 | Evento de limpieza. El evento se genera cuando se libera el último identificador del archivo. La clase de MOF [**\_ SimpleOp de FileIo**](fileio-simpleop.md) define los datos de evento para este evento.   |
| El valor del tipo de evento es 66 | Evento de cierre. El evento se genera cuando se libera el objeto de archivo. La clase de MOF [**\_ SimpleOp de FileIo**](fileio-simpleop.md) define los datos de evento para este evento.                     |
| El valor del tipo de evento es 73 | Evento de vaciado. Este evento se genera cuando los búferes de archivo se vacían por completo en el disco. La clase de MOF [**\_ SimpleOp de FileIo**](fileio-simpleop.md) define los datos de evento para este evento.  |



 

Los eventos de e/s de archivos se registran al principio de la operación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MSNT \_ SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**FileIo \_ v0**](fileio-v0.md)
</dt> <dt>

[**FileIo \_ v1**](fileio-v1.md)
</dt> </dl>

 

 
