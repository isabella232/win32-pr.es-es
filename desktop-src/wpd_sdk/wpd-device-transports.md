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
ms.openlocfilehash: 574c6b0b00980d110f2374e7426dd101c9122854
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467043"
---
# <a name="wpd_device_transports-enumeration"></a>Enumeración \_ WPD DEVICE \_ TRANSPORTS

El [**tipo de \_ enumeración \_ WPD DEVICE TRANSPORTS**](/windows/desktop/wpd_sdk/wpd-device-transports) especifica la relación de herencia de un servicio. Esta enumeración la usa la **propiedad \_ WPD DEVICE \_ TRANSPORT.**

## <a name="syntax"></a>Sintaxis


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



 

