---
description: Evento por usuario generado al intentar descargar archivos de la Web. Este evento lo generan las aplicaciones solicitadas por el control parental.
ms.assetid: 2291fc75-55e5-417e-b393-748750a5b3d6
title: Evento WPCEVENT_WEB_FILEDOWNLOAD (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66bb04a53589a1cae41e2ba7d7a9c00835452e87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716995"
---
# <a name="wpcevent_web_filedownload-event"></a>\_Evento WPCEVENT Web \_ FILEDOWNLOAD

Evento por usuario generado al intentar descargar archivos de la Web. Este evento lo generan las aplicaciones solicitadas por el control parental.


```C++
const EVENT_DESCRIPTOR WPCEVENT_WEB_FILEDOWNLOAD = {0xa, 0x0, 0x10, 0x4, 0x18, 0xa, 0x8000000000000030};
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*URL* 
</dt> <dd>

Origen de la dirección URL que está intentando descargar.

</dd> <dt>

*AppName* 
</dt> <dd>

El nombre de la aplicación que está generando el evento.

</dd> <dt>

*Versión* 
</dt> <dd>

Versión de la aplicación que está generando el evento.

</dd> <dt>

*Bloqueado* 
</dt> <dd>

Un valor de la enumeración [**WPCFLAG \_ ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) que indica información sobre qué eventos están bloqueados y qué controles hay en su lugar.

</dd> <dt>

*Ruta de acceso* 
</dt> <dd>

Ruta de acceso de destino del archivo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                             |
| Encabezado<br/>                   | <dl> <dt>Wpcevent. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Uso de las API de registro para controles parentales](using-logging-apis-for-parental-controls.md)
</dt> <dt>

[**WPC \_ args \_ CONVERSATIONINITEVENT**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 




