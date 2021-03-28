---
description: Esta clase es la clase primaria para los eventos de imagen. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: a719a34c-7e32-4758-9031-6ca2b2873e3e
title: Clase Image
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Image
api_type:
- NA
api_location: ''
ms.openlocfilehash: 47280a81b882f91ad71c6cd91004d1c0885afddf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985595"
---
# <a name="image-class"></a>Clase Image

Esta clase es la clase primaria para los eventos de imagen.

La siguiente sintaxis se simplifica desde el código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Guid("{2cb15d1d-5fc1-11d2-abe1-00a0c911f518}"), EventVersion(2)]
class Image : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Miembros

La clase **Image** no define ningún miembro.

## <a name="remarks"></a>Observaciones

Para habilitar los eventos de imagen en una sesión de registro del kernel de NT, especifique la marca de carga  de la imagen de la marca de seguimiento de **eventos \_ \_ \_ \_** en el miembro EnableFlags de la estructura de [**propiedades de \_ seguimiento \_ de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) al llamar a la función [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .

Los consumidores de seguimiento de eventos pueden implementar un procesamiento especial para los eventos de carga de imágenes mediante una llamada a la función [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) y especificando [**ImageLoadGuid**](nt-kernel-logger-constants.md) como parámetro *pGuid* . Utilice los siguientes tipos de eventos para identificar los eventos de carga de imágenes al consumir eventos.



| Tipo de evento                                                          | Descripción                                                                                                                                                                                                                                      |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Evento \_ de \_ \_ Carga del tipo de seguimiento**(el valor del tipo de evento es 10)<br/>     | Evento de carga de imagen. Se genera cuando se carga un archivo ejecutable o DLL. El proveedor solo genera un evento por primera vez que se carga un archivo DLL determinado. La clase MOF de [**\_ carga de imagen**](image-load.md) define los datos de evento para este evento.      |
| **Evento \_ de Tipo de seguimiento \_ \_ End**(el valor de tipo de evento es 2)<br/>       | Evento de descarga de imagen. Se genera cuando se descarga un archivo ejecutable o DLL. El proveedor solo genera un evento por la última vez que se descarga un archivo DLL determinado. La clase MOF de [**\_ carga de imagen**](image-load.md) define los datos de evento para este evento. |
| **Evento \_ de Tipo de seguimiento \_ \_ DC \_ Start**(el valor de tipo de evento es 3)<br/> | Evento de inicio de recopilación de datos. Enumera todas las imágenes cargadas al principio del seguimiento. La clase MOF de [**\_ carga de imagen**](image-load.md) define los datos de evento para este evento.                                                                  |
| **Evento \_ de Tipo de seguimiento \_ \_ DC \_ End**(el valor del tipo de evento es 4)<br/>   | Evento de finalización de recopilación de datos. Enumera todas las imágenes cargadas al final del seguimiento. La clase MOF de [**\_ carga de imagen**](image-load.md) define los datos de evento para este evento.                                                                          |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MSNT \_ SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**Carga de imágenes \_**](image-load.md)
</dt> <dt>

[**Imagen \_ v0**](image-v0.md)
</dt> <dt>

[**Imagen \_ v1**](image-v1.md)
</dt> </dl>

 

 
