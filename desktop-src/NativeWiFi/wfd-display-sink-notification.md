---
description: Describe la notificación que se pasa a la función de devolución de llamada de notificación de receptor de visualización de WFD \_ \_ \_ \_ .
ms.assetid: 1CB91DD9-5B58-4FE0-B7B0-E6189760511A
title: WFD_DISPLAY_SINK_NOTIFICATION estructura (Wfdsink. h)
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
ms.openlocfilehash: d4c2a15bbe6ef0df62fc0d607c97ecb3a2b54ec6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667130"
---
# <a name="wfd_display_sink_notification-structure"></a>\_Mostrar la \_ estructura de notificación del receptor \_ de WFD

La estructura de notificación del receptor de visualización de WFD describe la notificación que se pasa a la función de devolución de llamada de [**notificación de receptor de visualización de WFD \_ \_ \_ \_**](wfd-display-sink-notification-callback.md) . **\_ \_ \_**

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _WFD_DISPLAY_SINK_NOTIFICATION {
  WFD_DISPLAY_SINK_OBJECT_HEADER     Header;
  WFD_DISPLAY_SINK_NOTIFICATION_TYPE type;
  WCHAR                              strRemoteDeviceName[WFD_SINK_MAX_DEVICE_NAME_LENGTH + 1];
  DOT11_MAC_ADDRESS                  RemoteDeviceAddress;
  union {
    struct {
      HANDLE                  hSessionHandle;
      DOT11_WPS_CONFIG_METHOD PossibleConfigMethods;
    } ProvisioningRequestInfo;
    struct {
      DOT11_WFD_GROUP_ID GroupID;
    } ReconnectRequestInfo;
    struct {
      HANDLE             hSessionHandle;
      GUID               guidSessionInterface;
      DOT11_WFD_GROUP_ID GroupID;
      PWSTR              strProfile;
      SOCKADDR_STORAGE   LocalAddress;
      SOCKADDR_STORAGE   RemoteAddress;
      USHORT             uRTSPPort;
    } ConnectedInfo;
  };
} WFD_DISPLAY_SINK_NOTIFICATION, *PWFD_DISPLAY_SINK_NOTIFICATION;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Header**
</dt> <dd>

Un [**\_ encabezado de \_ \_ objeto \_ de receptor de visualización de WFD**](wfd-display-sink-object-header.md) que describe los datos incluidos en la notificación.

</dd> <dt>

**type**
</dt> <dd>

Un valor de tipo de notificación de receptor de visualización de WFD que indica el tipo de notificación. [**\_ \_ \_ \_**](wfd-display-sink-notification-type.md) Este parámetro también determina la información que se va a usar en la Unión siguiente.

</dd> <dt>

**strRemoteDeviceName**
</dt> <dd>

Contiene una cadena terminada en NULL que contiene el nombre del dispositivo remoto. \_ \_ \_ \_ \_ La longitud máxima del nombre del dispositivo del receptor de WFD se define como el valor (32).

</dd> <dt>

**RemoteDeviceAddress**
</dt> <dd>

Una [**\_ \_ dirección Mac de DOT11**](dot11-mac-address-type.md) que contiene el BSSID del dispositivo remoto.

</dd> <dt>

**ProvisioningRequestInfo**
</dt> <dd>

Información sobre una solicitud de aprovisionamiento. Use este si *Type* tiene el valor **ProvisioningRequestNotification**.

<dl> <dt>

**hSessionHandle**
</dt> <dd>

Identificador de la sesión.

</dd> <dt>

**PossibleConfigMethods**
</dt> <dd>

Métodos posibles para mostrar la interfaz de usuario para la aceptación interactiva.

</dd> </dl> </dd> <dt>

**ReconnectRequestInfo**
</dt> <dd>

Información sobre una solicitud de reconexión. Use este si *Type* tiene el valor **ReconnectRequestNotification**.

<dl> <dt>

**GroupID**
</dt> <dd>

Identificador del grupo.

</dd> </dl> </dd> <dt>

**ConnectedInfo**
</dt> <dd>

Información acerca de una notificación conectada. Use este si *Type* tiene el valor **ConnectedNotification**.

<dl> <dt>

**hSessionHandle**
</dt> <dd>

Identificador de la sesión.

</dd> <dt>

**guidSessionInterface**
</dt> <dd>

Un GUID que indica la interfaz de sesión.

</dd> <dt>

**GroupID**
</dt> <dd>

Identificador del grupo.

</dd> <dt>

**strProfile**
</dt> <dd>

Puntero a una cadena terminada en NULL que describe el perfil.

</dd> <dt>

**LocalAddress**
</dt> <dd>

Dirección local.

</dd> <dt>

**RemoteAddress**
</dt> <dd>

La dirección remota.

</dd> <dt>

**uRTSPPort**
</dt> <dd>

Puerto RTSP.

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio Windows 8.1\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]<br/>                              |
| Encabezado<br/>                   | <dl> <dt>Wfdsink. h</dt> </dl> |



 

 




