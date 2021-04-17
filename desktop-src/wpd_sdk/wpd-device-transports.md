---
description: El \_ tipo de \_ enumeración de transportes de dispositivos WPD especifica la relación de herencia para un servicio. Esta enumeración la usa la \_ propiedad de transporte del dispositivo WPD \_ .
ms.assetid: a9d48034-3588-4e48-a03a-91cbe679cbc9
title: Enumeración WPD_DEVICE_TRANSPORTS (PortableDevice. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708161"
---
# <a name="wpd_device_transports-enumeration"></a>\_Enumeración de transportes de dispositivos WPD \_

El tipo de enumeración de [**\_ \_ transportes de dispositivos WPD**](/windows/desktop/wpd_sdk/wpd-device-transports) especifica la relación de herencia para un servicio. Esta enumeración la usa la propiedad de **\_ \_ transporte del dispositivo WPD** .

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

<span id="WPD_DEVICE_TRANSPORT_UNSPECIFIED"></span><span id="wpd_device_transport_unspecified"></span>**transporte de dispositivo WPD no \_ \_ \_ especificado**
</dt> <dd>

No se especificó el tipo de transporte.

</dd> <dt>

<span id="WPD_DEVICE_TRANSPORT_USB"></span><span id="wpd_device_transport_usb"></span>**\_ \_ Puerto USB de transporte de dispositivo WPD \_**
</dt> <dd>

El dispositivo se conecta a través de USB.

</dd> <dt>

<span id="WPD_DEVICE_TRANSPORT_IP"></span><span id="wpd_device_transport_ip"></span>**\_IP de \_ transporte del dispositivo WPD \_**
</dt> <dd>

El dispositivo se conecta a través del Protocolo de Internet (IP).

</dd> <dt>

<span id="WPD_DEVICE_TRANSPORT_BLUETOOTH"></span><span id="wpd_device_transport_bluetooth"></span>**\_Bluetooth de \_ transporte de dispositivos de WPD \_**
</dt> <dd>

El dispositivo se conecta a través de Bluetooth.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



 

