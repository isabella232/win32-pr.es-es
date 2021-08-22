---
description: Esta clase es la clase primaria para los eventos de imagen. La sintaxis siguiente se simplifica a partir del código MOF.
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
ms.openlocfilehash: a7db8595dd09790d875e502e479d14669a6df90b8de38b71fcf9ed58f2b68b53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070115"
---
# <a name="image-class"></a>Clase Image

Esta clase es la clase primaria para los eventos de imagen.

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Guid("{2cb15d1d-5fc1-11d2-abe1-00a0c911f518}"), EventVersion(2)]
class Image : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Miembros

La **clase Image** no define ningún miembro.

## <a name="remarks"></a>Comentarios

Para habilitar eventos de imagen en una sesión de registro del kernel de NT, especifique la marca **EVENT TRACE FLAG IMAGE \_ \_ \_ \_ LOAD** en el miembro **EnableFlags** de la estructura [**EVENT TRACE \_ \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) al llamar a la [**función StartTrace.**](/windows/win32/api/evntrace/nf-evntrace-starttracea)

Los consumidores de seguimiento de eventos pueden implementar un procesamiento especial para los eventos de carga de imágenes llamando a la función [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) y especificando [**ImageLoadGuid**](nt-kernel-logger-constants.md) como parámetro *pGuid.* Use los siguientes tipos de eventos para identificar los eventos de carga de imágenes al consumir eventos.



| Tipo de evento                                                          | Descripción                                                                                                                                                                                                                                      |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EVENTO \_ TRACE \_ TYPE \_ LOAD**(el valor del tipo de evento es 10)<br/>     | Evento de carga de imagen. Se genera cuando se carga un archivo DLL o ejecutable. El proveedor genera solo un evento por primera vez que se carga un archivo DLL determinado. La [**clase MOF \_ Image Load**](image-load.md) define los datos de evento para este evento.      |
| **EVENTO \_ TRACE \_ TYPE \_ END**(el valor del tipo de evento es 2)<br/>       | Evento de descarga de imágenes. Se genera cuando se descarga un archivo DLL o ejecutable. El proveedor genera solo un evento para la última vez que se descarga un archivo DLL determinado. La [**clase MOF \_ Image Load**](image-load.md) define los datos de evento para este evento. |
| **EVENTO \_ TRACE \_ TYPE \_ DC \_ START**(el valor del tipo de evento es 3)<br/> | Evento de inicio de la recopilación de datos. Enumera todas las imágenes cargadas al principio del seguimiento. La [**clase MOF \_ Image Load**](image-load.md) define los datos de evento para este evento.                                                                  |
| **EVENTO \_ TRACE \_ TYPE \_ DC \_ END**(el valor del tipo de evento es 4)<br/>   | Evento final de recopilación de datos. Enumera todas las imágenes cargadas al final del seguimiento. La [**clase MOF \_ Image Load**](image-load.md) define los datos de evento para este evento.                                                                          |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SystemTrace de MSNT \_**](msnt-systemtrace.md)
</dt> <dt>

[**Carga de \_ imágenes**](image-load.md)
</dt> <dt>

[**Imagen \_ V0**](image-v0.md)
</dt> <dt>

[**Imagen \_ V1**](image-v1.md)
</dt> </dl>

 

 
