---
title: Enumeración DeviceTypes
description: Describe los tipos de dispositivo DLNA que admite la API de streaming de multimedia.
ms.assetid: ec6bbc1f-653a-414c-b458-1a5e1b101781
keywords:
- Enumeración de DeviceTypes de media streaming API
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
ms.openlocfilehash: 9caf60fa5736f9db442da5787746a49f71c61c89
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718599"
---
# <a name="devicetypes-enumeration"></a>Enumeración DeviceTypes

Describe los tipos de dispositivo DLNA que admite la API de streaming de multimedia.

## <a name="syntax"></a>Sintaxis


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

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown**
</dt> <dd>

Tipo de dispositivo desconocido.

</dd> <dt>

<span id="DigitalMediaRenderer"></span><span id="digitalmediarenderer"></span><span id="DIGITALMEDIARENDERER"></span>**DigitalMediaRenderer**
</dt> <dd>

Representador de medios digitales DLNA (DMR). El valor es equivalente al tipo de dispositivo **urn: schemas-UPnP-org: Device: MediaRenderer: 1**.

</dd> <dt>

<span id="DigitalMediaServer"></span><span id="digitalmediaserver"></span><span id="DIGITALMEDIASERVER"></span>**DigitalMediaServer**
</dt> <dd>

Servidor de medios digitales DLNA (DMS). El valor es equivalente al tipo de dispositivo **urn: schemas-UPnP-org: Device: MediaServer: 1**.

</dd> <dt>

<span id="DigitalMediaPlayer"></span><span id="digitalmediaplayer"></span><span id="DIGITALMEDIAPLAYER"></span>**DigitalMediaPlayer**
</dt> <dd>

Media Player digitales DLNA

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| IDL<br/> | <dl> <dt>Windows. Media. streaming. idl (referencia a Windows. Media. streaming. idl)</dt> </dl> |



 

 





