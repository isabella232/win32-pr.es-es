---
title: Enumeración DeviceTypes
description: Describe los tipos de dispositivos DLNA compatibles con Media Streaming API.
ms.assetid: ec6bbc1f-653a-414c-b458-1a5e1b101781
keywords:
- Enumeración DeviceTypes Media Streaming API
topic_type:
- apiref
api_name:
- DeviceTypes
api_location:
- Windows.Media.Streaming.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 969eb389a1216ec0e30f27a938ca4f5382397ac5489f87add87731b69824b87f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119100659"
---
# <a name="devicetypes-enumeration"></a>Enumeración DeviceTypes

Describe los tipos de dispositivos DLNA compatibles con Media Streaming API.

## <a name="syntax"></a>Syntax


```C++
typedef enum DeviceTypes { 
  Unknown               = 0x0,
  DigitalMediaRenderer  = 0x1,
  DigitalMediaServer    = 0x2,
  DigitalMediaPlayer    = 0x4
} DeviceTypes;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido**
</dt> <dd>

Tipo de dispositivo desconocido.

</dd> <dt>

<span id="DigitalMediaRenderer"></span><span id="digitalmediarenderer"></span><span id="DIGITALMEDIARENDERER"></span>**DigitalMediaRenderer**
</dt> <dd>

Representador de medios digitales (DMR) de DLNA. El valor es equivalente al tipo de **dispositivo urn:schemas-upnp-org:device:MediaRenderer:1**.

</dd> <dt>

<span id="DigitalMediaServer"></span><span id="digitalmediaserver"></span><span id="DIGITALMEDIASERVER"></span>**DigitalMediaServer**
</dt> <dd>

DlNA Digital Media Server (DMS). El valor es equivalente al tipo de **dispositivo urn:schemas-upnp-org:device:MediaServer:1**.

</dd> <dt>

<span id="DigitalMediaPlayer"></span><span id="digitalmediaplayer"></span><span id="DIGITALMEDIAPLAYER"></span>**DigitalMediaPlayer**
</dt> <dd>

DLNA Digital Media Player

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| Idl<br/> | <dl> <dt>Windows. Media.Streaming.idl (referencia Windows. Media.Streaming.idl)</dt> </dl> |



 

 





