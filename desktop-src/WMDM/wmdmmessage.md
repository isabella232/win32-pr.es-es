---
title: Enumeración WMDMMessage
description: El tipo de enumeración WMDMMessage define los tipos de mensaje y los estados.
ms.assetid: 49a77100-8890-4e40-852f-c6fd436f22c5
keywords:
- Ventanas multimedia de enumeración WMDMMessage Administrador de dispositivos
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
ms.openlocfilehash: 348092e079428e0b147d8143411cee7766365913115f968ed0e112b209383077
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862665"
---
# <a name="wmdmmessage-enumeration"></a>Enumeración WMDMMessage

El **tipo de enumeración WMDMMessage** define los tipos de mensaje y los estados.

## <a name="syntax"></a>Syntax


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

<span id="WMDM_MSG_DEVICE_ARRIVAL"></span><span id="wmdm_msg_device_arrival"></span>**LLEGADA DEL DISPOSITIVO \_ WMDM MSG \_ \_**
</dt> <dd>

Se ha Windows un Administrador de dispositivos multimedia conectado.

</dd> <dt>

<span id="WMDM_MSG_DEVICE_REMOVAL"></span><span id="wmdm_msg_device_removal"></span>**ELIMINACIÓN DE \_ DISPOSITIVOS DE MENSAJES WMDM \_ \_**
</dt> <dd>

Se ha Windows un Administrador de dispositivos multimedia.

</dd> <dt>

<span id="WMDM_MSG_MEDIA_ARRIVAL"></span><span id="wmdm_msg_media_arrival"></span>**LLEGADA DE MEDIOS \_ DE MENSAJES WMDM \_ \_**
</dt> <dd>

Los medios se han insertado en un Windows multimedia Administrador de dispositivos dispositivo.

</dd> <dt>

<span id="WMDM_MSG_MEDIA_REMOVAL"></span><span id="wmdm_msg_media_removal"></span>**ELIMINACIÓN DE \_ MEDIOS DE MENSAJES WMDM \_ \_**
</dt> <dd>

Los medios se han quitado de un Windows multimedia Administrador de dispositivos dispositivo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdm.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Tipos de enumeración**](enumeration-types.md)
</dt> </dl>

 

 





