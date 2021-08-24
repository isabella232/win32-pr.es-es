---
title: Enumeración ConnectionStatus
description: Representa el estado del dispositivo en la red como se ha visto por última vez.
ms.assetid: e1893a59-ce7d-4e9c-a013-02ac916d4ee8
keywords:
- ConnectionStatus enumeration Media Streaming API
topic_type:
- apiref
api_name:
- ConnectionStatus
api_location:
- Windows.Media.Streaming.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8617012abe75d213e0de7be70811152315a888693c7336ef58cd34ceb98eba55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119721255"
---
# <a name="connectionstatus-enumeration"></a>Enumeración ConnectionStatus

Representa el estado del dispositivo en la red como se ha visto por última vez.

## <a name="syntax"></a>Syntax


```C++
typedef enum ConnectionStatus { 
  Online    = 0,
  Offline   = 1,
  Sleeping  = 2
} ConnectionStatus;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="Online"></span><span id="online"></span><span id="ONLINE"></span>**en línea**
</dt> <dd>

El dispositivo está en línea y activo en la red.

</dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**sin conexión**
</dt> <dd>

El dispositivo está desconectado.

</dd> <dt>

<span id="Sleeping"></span><span id="sleeping"></span><span id="SLEEPING"></span>**Dormir**
</dt> <dd>

El dispositivo está actualmente sin conexión, pero podría reactivarse automáticamente cuando se intenta comunicarse con él.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| Idl<br/> | <dl> <dt>Windows. Media.Streaming.idl (referencia Windows. Media.Streaming.idl)</dt> </dl> |



 

 





