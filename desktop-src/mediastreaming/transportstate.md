---
title: Enumeración TransportState
description: Define los Estados de transporte disponibles tal y como se define en las directrices de UPnP.
ms.assetid: 2F942EAC-514B-4E65-A12F-85558E9A96A0
keywords:
- Enumeración de TransportState de media streaming API
topic_type:
- apiref
api_name:
- TransportState
api_location:
- Windows.Media.Streaming.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 865d7e0f6a96727915833bb402860cde661162f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718982"
---
# <a name="transportstate-enumeration"></a>Enumeración TransportState

Define los Estados de transporte disponibles tal y como se define en las directrices de UPnP.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum _TransportState { 
  Unknown         = 0,
  Stopped         = 1,
  Playing         = 2,
  Transitioning   = 3,
  Paused          = 4,
  Recording       = 5,
  NoMediaPresent  = 6,
  Last            = 7
} TransportState;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown**
</dt> <dd>

Estado de dispositivo erróneo.

</dd> <dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Ha**
</dt> <dd>

El transporte del dispositivo s está detenido.

</dd> <dt>

<span id="Playing"></span><span id="playing"></span><span id="PLAYING"></span>**Tarjetas**
</dt> <dd>

El transporte del dispositivo s está en estado de reproducción.

</dd> <dt>

<span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transición**
</dt> <dd>

El transporte del dispositivo s está en un estado de transición que dará como resultado otro valor de estado.

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**En pausa**
</dt> <dd>

El transporte del dispositivo s está en estado de pausa.

</dd> <dt>

<span id="Recording"></span><span id="recording"></span><span id="RECORDING"></span>**Musicales**
</dt> <dd>

El transporte del dispositivo s está en un estado de grabación.

</dd> <dt>

<span id="NoMediaPresent"></span><span id="nomediapresent"></span><span id="NOMEDIAPRESENT"></span>**NoMediaPresent**
</dt> <dd>

El transporte del dispositivo s no tiene un URI establecido para la reproducción.

</dd> <dt>

<span id="Last"></span><span id="last"></span><span id="LAST"></span>**Guardado**
</dt> <dd>

El estado anterior del dispositivo es el estado de transporte actual.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| IDL<br/> | <dl> <dt>Windows. Media. streaming. idl (referencia a Windows. Media. streaming. idl)</dt> </dl> |



 

 





