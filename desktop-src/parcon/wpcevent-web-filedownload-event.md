---
description: Evento por usuario generado al intentar descargar archivos desde la web. Este evento lo generan las aplicaciones que solicitan los controles parentales.
ms.assetid: 2291fc75-55e5-417e-b393-748750a5b3d6
title: WPCEVENT_WEB_FILEDOWNLOAD evento (Wpcevent.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7430b87e7c227fe351e3182f344c60ece0b5a3138b94fe19fee950f96ec24b6a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112715"
---
# <a name="wpcevent_web_filedownload-event"></a>Evento WPCEVENT \_ WEB \_ FILEDOWNLOAD

Evento por usuario generado al intentar descargar archivos desde la web. Este evento lo generan las aplicaciones que solicitan los controles parentales.


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

Nombre de la aplicación que genera el evento.

</dd> <dt>

*Versión* 
</dt> <dd>

Versión de la aplicación que genera el evento.

</dd> <dt>

*Bloqueado* 
</dt> <dd>

Valor de la enumeración [**\_ WPCFLAG ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) que indica información sobre qué eventos están bloqueados para su uso y qué controles están en su lugar.

</dd> <dt>

*Ruta de acceso* 
</dt> <dd>

Ruta de acceso de destino del archivo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                             |
| Header<br/>                   | <dl> <dt>Wpcevent.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Uso de las API de registro para los controles parentales](using-logging-apis-for-parental-controls.md)
</dt> <dt>

[**WPC \_ ARGS \_ CONVERSATIONINITEVENT**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 




