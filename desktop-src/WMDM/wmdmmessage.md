---
title: Enumeración WMDMMessage
description: El tipo de enumeración WMDMMessage define los tipos y los Estados de los mensajes.
ms.assetid: 49a77100-8890-4e40-852f-c6fd436f22c5
keywords:
- Enumeración WMDMMessage de Windows Media Administrador de dispositivos
topic_type:
- apiref
api_name:
- WMDMMessage
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7489dc7059f10e1a6f61d1a290f8f664a385f96c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698690"
---
# <a name="wmdmmessage-enumeration"></a>Enumeración WMDMMessage

El tipo de enumeración **WMDMMessage** define los tipos y los Estados de los mensajes.

## <a name="syntax"></a>Sintaxis


```C++
enum WMDMMessage {
  WMDM_MSG_DEVICE_ARRIVAL, 
  WMDM_MSG_DEVICE_REMOVAL, 
  WMDM_MSG_MEDIA_ARRIVAL, 
  WMDM_MSG_MEDIA_REMOVAL 

};
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WMDM_MSG_DEVICE_ARRIVAL"></span><span id="wmdm_msg_device_arrival"></span>**\_llegada del \_ dispositivo de mensajes de WMDM \_**
</dt> <dd>

Se ha conectado un dispositivo Administrador de dispositivos de Windows Media.

</dd> <dt>

<span id="WMDM_MSG_DEVICE_REMOVAL"></span><span id="wmdm_msg_device_removal"></span>**\_eliminación de \_ dispositivos de mensajes de WMDM \_**
</dt> <dd>

Se ha quitado un dispositivo Administrador de dispositivos de Windows Media.

</dd> <dt>

<span id="WMDM_MSG_MEDIA_ARRIVAL"></span><span id="wmdm_msg_media_arrival"></span>**\_llegada del \_ medio de mensajes de WMDM \_**
</dt> <dd>

Los medios se han insertado en un dispositivo Administrador de dispositivos de Windows Media.

</dd> <dt>

<span id="WMDM_MSG_MEDIA_REMOVAL"></span><span id="wmdm_msg_media_removal"></span>**eliminación de los medios de mensajes de WMDM \_ \_ \_**
</dt> <dd>

Los medios se han quitado de un dispositivo Administrador de dispositivos de Windows Media.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Tipos de enumeración**](enumeration-types.md)
</dt> </dl>

 

 





