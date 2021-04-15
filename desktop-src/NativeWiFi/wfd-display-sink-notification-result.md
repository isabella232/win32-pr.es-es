---
description: Describe el resultado que puede establecer de forma opcional después de procesar un notificación receptor de pantalla en la función de devolución de llamada de notificación de receptor de visualización de WFD \_ \_ \_ \_ .
ms.assetid: 6ED04294-2ED9-455B-9274-8C3DB06D4B21
title: WFD_DISPLAY_SINK_NOTIFICATION_RESULT estructura (Wfdsink. h)
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
ms.openlocfilehash: dc23416d4d13284862aea652dd71909e71879afc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669745"
---
# <a name="wfd_display_sink_notification_result-structure"></a>La \_ \_ estructura de \_ resultado de notificación de receptor de visualización de WFD \_

La estructura de resultados de notificación del receptor de visualización de WFD describe el resultado que puede establecer opcionalmente después de procesar un notificación receptor de pantalla en la función de devolución de llamada de [**notificación de receptor de visualización de WFD \_ \_ \_ \_**](wfd-display-sink-notification-callback.md) . **\_ \_ \_ \_**

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

Un [**\_ encabezado de \_ \_ objeto \_ de receptor de visualización de WFD**](wfd-display-sink-object-header.md) que describe los datos incluidos en el resultado de la notificación.

</dd> <dt>

**type**
</dt> <dd>

Un valor de tipo de notificación de receptor de visualización de WFD que indica el tipo de resultado de la notificación. [**\_ \_ \_ \_**](wfd-display-sink-notification-type.md) Este parámetro también determina la información que se va a usar en la Unión siguiente.

</dd> <dt>

**ProvisioningData**
</dt> <dd>

Información sobre el resultado de una solicitud de aprovisionamiento. Use este si *Type* tiene el valor **ProvisioningRequestNotification**.

<dl> <dt>

**ConfigMethod**
</dt> <dd>

Método para mostrar la interfaz de usuario para la aceptación interactiva.

</dd> <dt>

**uPassKeyLength**
</dt> <dd>

Número de caracteres anchos de la *clave de paso*, sin contar ningún terminador null.

</dd> <dt>

**Bluetooth**
</dt> <dd>

Contiene la clave Pass como una matriz de caracteres anchos. \_ \_ \_ \_ \_ La longitud máxima de la clave de paso de información del receptor de WFD \_ se define como el valor (8).

</dd> </dl> </dd> <dt>

**ReconnectData**
</dt> <dd>

Información sobre el resultado de una solicitud de reconexión. Use este si *Type* tiene el valor **ReconnectRequestNotification**.

<dl> <dt>

**strProfile**
</dt> <dd>

Puntero a una cadena terminada en NULL que describe el perfil.

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio Windows 8.1\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]<br/>                              |
| Encabezado<br/>                   | <dl> <dt>Wfdsink. h</dt> </dl> |



 

 




