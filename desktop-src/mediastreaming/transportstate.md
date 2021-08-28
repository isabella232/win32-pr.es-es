---
title: Enumeración TransportState
description: Define los estados de transporte disponibles tal como se definen en las directrices de UPnP.
ms.assetid: 2F942EAC-514B-4E65-A12F-85558E9A96A0
keywords:
- Enumeración TransportState Media Streaming API
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
ms.openlocfilehash: a21fc8d0f2799cfba734d605d0c4d2835744ddeb130327ea39a22090d13464f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663104"
---
# <a name="transportstate-enumeration"></a>Enumeración TransportState

Define los estados de transporte disponibles tal como se definen en las directrices de UPnP.

## <a name="syntax"></a>Syntax


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

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido**
</dt> <dd>

Estado de dispositivo erróneo.

</dd> <dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Detenido**
</dt> <dd>

El transporte del dispositivo está en estado detenido.

</dd> <dt>

<span id="Playing"></span><span id="playing"></span><span id="PLAYING"></span>**Jugando**
</dt> <dd>

El transporte del dispositivo está en un estado de reproducción.

</dd> <dt>

<span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transición**
</dt> <dd>

El transporte del dispositivo está en un estado de transición que dará como resultado otro valor de estado.

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Pausa**
</dt> <dd>

El transporte del dispositivo está en estado en pausa.

</dd> <dt>

<span id="Recording"></span><span id="recording"></span><span id="RECORDING"></span>**Grabación**
</dt> <dd>

El transporte del dispositivo está en un estado de grabación.

</dd> <dt>

<span id="NoMediaPresent"></span><span id="nomediapresent"></span><span id="NOMEDIAPRESENT"></span>**NoMediaPresent**
</dt> <dd>

El transporte del dispositivo no tiene un URI establecido para la reproducción.

</dd> <dt>

<span id="Last"></span><span id="last"></span><span id="LAST"></span>**Última**
</dt> <dd>

Estado anterior del dispositivo al estado de transporte actual.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| Idl<br/> | <dl> <dt>Windows. Media.Streaming.idl (referencia Windows. Media.Streaming.idl)</dt> </dl> |



 

 





