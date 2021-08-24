---
description: El tipo de \_ enumeración WPD DEVICE \_ TRANSPORTS especifica la relación de herencia de un servicio. Esta enumeración la usa la propiedad \_ WPD DEVICE \_ TRANSPORT.
ms.assetid: a9d48034-3588-4e48-a03a-91cbe679cbc9
title: WPD_DEVICE_TRANSPORTS enumeración (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_DEVICE_TRANSPORTS
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 5f091a84c573038c7d74cf5c2760c298a2542f70f06bdb45d1e72954c9dd5f25
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119703825"
---
# <a name="wpd_device_transports-enumeration"></a>Enumeración \_ WPD DEVICE \_ TRANSPORTS

El [**tipo de \_ enumeración \_ WPD DEVICE TRANSPORTS**](/windows/desktop/wpd_sdk/wpd-device-transports) especifica la relación de herencia de un servicio. Esta enumeración la usa la **propiedad \_ WPD DEVICE \_ TRANSPORT.**

## <a name="syntax"></a>Syntax


```C++
typedef enum tagWPD_DEVICE_TRANSPORTS { 
  WPD_DEVICE_TRANSPORT_UNSPECIFIED  = 0,
  WPD_DEVICE_TRANSPORT_USB          = 1,
  WPD_DEVICE_TRANSPORT_IP           = 2,
  WPD_DEVICE_TRANSPORT_BLUETOOTH    = 3
} WPD_DEVICE_TRANSPORTS;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_DEVICE_TRANSPORT_UNSPECIFIED"></span><span id="wpd_device_transport_unspecified"></span>**TRANSPORTE DE \_ DISPOSITIVO \_ WPD \_ SIN ESPECIFICAR**
</dt> <dd>

No se especificó el tipo de transporte.

</dd> <dt>

<span id="WPD_DEVICE_TRANSPORT_USB"></span><span id="wpd_device_transport_usb"></span>**WPD \_ DEVICE \_ TRANSPORT \_ USB**
</dt> <dd>

El dispositivo se conecta a través de USB.

</dd> <dt>

<span id="WPD_DEVICE_TRANSPORT_IP"></span><span id="wpd_device_transport_ip"></span>**IP DE \_ TRANSPORTE \_ DE DISPOSITIVO \_ WPD**
</dt> <dd>

El dispositivo está conectado a través del protocolo de Internet (IP).

</dd> <dt>

<span id="WPD_DEVICE_TRANSPORT_BLUETOOTH"></span><span id="wpd_device_transport_bluetooth"></span>**BLUETOOTH DE \_ TRANSPORTE \_ DE DISPOSITIVO \_ WPD**
</dt> <dd>

El dispositivo se conecta a través de Bluetooth.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



 

