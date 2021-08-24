---
description: Describe el resultado que se puede establecer opcionalmente después de procesar una notificación de receptor de pantalla en la función DEVOLUCIÓN DE LLAMADA DE NOTIFICACIÓN DEL RECEPTOR DE PANTALLA DE \_ \_ \_ \_ WFD.
ms.assetid: 6ED04294-2ED9-455B-9274-8C3DB06D4B21
title: WFD_DISPLAY_SINK_NOTIFICATION_RESULT estructura (Wfdsink.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFD_DISPLAY_SINK_NOTIFICATION
api_type:
- HeaderDef
api_location:
- wfdsink.h
ms.openlocfilehash: d72f444d409a7a3d43103967aff671fa7c808e5a37858e79f175db3511960e95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119780085"
---
# <a name="wfd_display_sink_notification_result-structure"></a>Estructura DE \_ RESULTADOS DE \_ NOTIFICACIÓN DEL RECEPTOR DE VISUALIZACIÓN \_ \_ DE WFD

La **estructura WFD \_ DISPLAY SINK \_ NOTIFICATION \_ \_ RESULT** describe el resultado que, opcionalmente, se puede establecer después de procesar una notificación de receptor de pantalla en la función DEVOLUCIÓN DE LLAMADA DE NOTIFICACIÓN DEL RECEPTOR DISPLAY [**\_ \_ de \_ \_ WFD.**](wfd-display-sink-notification-callback.md)

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _WFD_DISPLAY_SINK_NOTIFICATION {
  WFD_DISPLAY_SINK_OBJECT_HEADER     Header;
  WFD_DISPLAY_SINK_NOTIFICATION_TYPE type;
  union {
    struct {
      DOT11_WPS_CONFIG_METHOD ConfigMethod;
      UINT32                  uPassKeyLength;
      WCHAR                   Passkey[WFD_SINK_WPS_INFO_MAX_PASSKEY_LENGTH];
    } ProvisioningData;
    struct {
      PWSTR strProfile;
    } ReconnectData;
  };
} WFD_DISPLAY_SINK_NOTIFICATION, *PWFD_DISPLAY_SINK_NOTIFICATION;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Header**
</dt> <dd>

Un [**ENCABEZADO DE OBJETO DE RECEPTOR DE VISUALIZACIÓN \_ \_ \_ \_ DE WFD**](wfd-display-sink-object-header.md) que describe los datos incluidos en el resultado de la notificación.

</dd> <dt>

**type**
</dt> <dd>

Valor [**WFD \_ DISPLAY SINK NOTIFICATION \_ \_ \_ TYPE**](wfd-display-sink-notification-type.md) que indica el tipo del resultado de la notificación. Este parámetro también determina qué información se va a usar en la unión siguiente.

</dd> <dt>

**ProvisioningData**
</dt> <dd>

Información sobre el resultado de una solicitud de aprovisionamiento. Úsese si *el tipo* tiene el valor **ProvisioningRequestNotification.**

<dl> <dt>

**ConfigMethod**
</dt> <dd>

Método para mostrar la interfaz de usuario para la aceptación interactiva.

</dd> <dt>

**uPassKeyLength**
</dt> <dd>

Número de caracteres anchos de *passkey,* sin contar ningún terminador NULL.

</dd> <dt>

**Contraseña**
</dt> <dd>

Contiene la clave de paso como una matriz de caracteres anchos. WFD \_ SINK \_ WPS INFO MAX \_ \_ \_ PASSKEY LENGTH se define como el valor \_ (8).

</dd> </dl> </dd> <dt>

**ReconnectData**
</dt> <dd>

Información sobre el resultado de una solicitud de reconexión. Úsese si *el tipo* tiene el valor **ReconnectRequestNotification.**

<dl> <dt>

**strProfile**
</dt> <dd>

Puntero a una cadena terminada en NULL que describe el perfil.

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 solo aplicaciones de escritorio\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                              |
| Header<br/>                   | <dl> <dt>Wfdsink.h</dt> </dl> |



 

 




