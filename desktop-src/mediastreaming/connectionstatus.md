---
title: Enumeración ConnectionStatus
description: Representa el estado del dispositivo en la red como se ha visto por última vez.
ms.assetid: e1893a59-ce7d-4e9c-a013-02ac916d4ee8
keywords:
- Enumeración ConnectionStatus Media Streaming API
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
ms.openlocfilehash: 61368a494e5bff0f6aca575380937b98f9d6b650
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127580768"
---
# <a name="connectionstatus-enumeration"></a>Enumeración ConnectionStatus

Representa el estado del dispositivo en la red como se ha visto por última vez.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum ConnectionStatus { 
  Online    = 0,
  Offline   = 1,
  Sleeping  = 2
} ConnectionStatus;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="Online"></span><span id="online"></span><span id="ONLINE"></span>**En línea**
</dt> <dd>

El dispositivo está en línea y activo en la red.

</dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Sin conexión**
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
| IDL<br/> | <dl> <dt>Windows. Media.Streaming.idl (referencia Windows. Media.Streaming.idl)</dt> </dl> |



 

 





