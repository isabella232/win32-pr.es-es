---
description: 'Clase FileIo: esta clase es la clase primaria para los eventos de E/S de archivo. La sintaxis siguiente se simplifica a partir del código MOF.'
ms.assetid: 8e006a63-a061-4b62-8f90-b8c8823bb047
title: Clase FileIo
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
ms.openlocfilehash: 716528902a115e23eae5b49ef572b87a71d11e25
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476901"
---
# <a name="fileio-class"></a>Clase FileIo

Esta clase es la clase primaria para los eventos de E/S de archivo.

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Guid("{90cbdc39-4a3e-11d1-84f4-0000f80464e3}"), EventVersion(2)]
class FileIo : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Members

La **clase FileIo** no define ningún miembro.

## <a name="remarks"></a>Observaciones

Para habilitar los eventos de E/S de archivo en una sesión de registro del kernel de NT, especifique la marca **EVENT TRACE FLAG DISK FILE \_ \_ \_ \_ \_ IO** en el miembro **EnableFlags** de una estructura [**EVENT TRACE \_ \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) al llamar a la [**función StartTrace.**](/windows/win32/api/evntrace/nf-evntrace-starttracea) También puede especificar una o varias de las marcas siguientes:

-   **\_E/S DE ARCHIVO DE MARCA DE SEGUIMIENTO DE \_ \_ \_ EVENTOS**
-   **EVENT \_ TRACE \_ FLAG \_ FILE \_ IO \_ INIT**

Los consumidores de seguimiento de eventos pueden implementar un procesamiento especial para eventos de E/S de archivos llamando a la función [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) y especificando [**FileIoGuid**](nt-kernel-logger-constants.md) como parámetro *pGuid.* Use los siguientes tipos de eventos para identificar el evento real al consumir eventos.



| Tipo de evento             | Descripción                                                                                                                                                                             |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| El valor del tipo de evento es 0  | Evento de nombre de archivo. La [**clase MOF FileIo \_ Name**](fileio-name.md) define los datos de evento para este evento.                                                                               |
| El valor del tipo de evento es 32 | Evento de creación de archivos. La [**clase MOF FileIo \_ Name**](fileio-name.md) define los datos de evento para este evento.                                                                             |
| El valor del tipo de evento es 35 | Evento de eliminación de archivos. La [**clase MOF FileIo \_ Name**](fileio-name.md) define los datos de evento para este evento.                                                                             |
| El valor del tipo de evento es 36 | Evento de desmontaje de archivos. Enumera todos los archivos abiertos en el equipo al final de la sesión de seguimiento. La [**clase MOF FileIo \_ Name**](fileio-name.md) define los datos de evento para este evento. |
| El valor del tipo de evento es 64 | Evento de creación de archivos. La [**clase MOF FileIo \_ Create**](fileio-create.md) define los datos de evento para este evento.                                                                         |
| El valor del tipo de evento es 72 | Evento de enumeración de directorios. La [**clase MOF FileIo \_ DirEnum**](fileio-direnum.md) define los datos de evento para este evento.                                                             |
| El valor del tipo de evento es 77 | Evento de notificación de directorio. La [**clase MOF FileIo \_ DirEnum**](fileio-direnum.md) define los datos de evento para este evento.                                                            |
| El valor del tipo de evento es 69 | Establecer evento de información. La [**clase MOF FileIo \_ Info**](fileio-info.md) define los datos de evento para este evento.                                                                         |
| El valor del tipo de evento es 70 | Evento de eliminación del archivo. La [**clase MOF FileIo \_ Info**](fileio-info.md) define los datos de evento para este evento.                                                                             |
| El valor del tipo de evento es 71 | Evento de cambio de nombre de archivo. La [**clase MOF FileIo \_ Info**](fileio-info.md) define los datos de evento para este evento.                                                                             |
| El valor del tipo de evento es 74 | Evento de información de archivo de consulta. La [**clase MOF FileIo \_ Info**](fileio-info.md) define los datos de evento para este evento.                                                                  |
| El valor del tipo de evento es 75 | Evento de control del sistema de archivos. La [**clase MOF FileIo \_ Info**](fileio-info.md) define los datos de evento para este evento.                                                                     |
| El valor del tipo de evento es 76 | Evento de fin de la operación. La [**clase MOF FileIo \_ OpEnd**](fileio-opend.md) define los datos de evento para este evento.                                                                      |
| El valor del tipo de evento es 67 | Evento de lectura de archivos. La [**clase MOF FileIo \_ ReadWrite**](fileio-readwrite.md) define los datos de evento para este evento.                                                                     |
| El valor del tipo de evento es 68 | Evento de escritura de archivos. La [**clase MOF FileIo \_ ReadWrite**](fileio-readwrite.md) define los datos de evento para este evento.                                                                    |
| El valor del tipo de evento es 65 | Evento de limpieza. El evento se genera cuando se libera el último identificador del archivo. La [**clase MOF \_ FileIo SimpleOp**](fileio-simpleop.md) define los datos de evento para este evento.   |
| El valor del tipo de evento es 66 | Cierre el evento. El evento se genera cuando se libera el objeto de archivo. La [**clase MOF \_ FileIo SimpleOp**](fileio-simpleop.md) define los datos de evento para este evento.                     |
| El valor del tipo de evento es 73 | Evento flush. Este evento se genera cuando los búferes de archivo se vacían completamente en el disco. La [**clase MOF \_ FileIo SimpleOp**](fileio-simpleop.md) define los datos de evento para este evento.  |



 

Los eventos de E/S de archivo se registran al principio de la operación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SystemTrace de MSNT \_**](msnt-systemtrace.md)
</dt> <dt>

[**FileIo \_ V0**](fileio-v0.md)
</dt> <dt>

[**FileIo \_ V1**](fileio-v1.md)
</dt> </dl>

 

 
