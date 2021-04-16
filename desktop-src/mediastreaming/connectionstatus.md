---
title: Enumeración ConnectionStatus
description: Representa el estado del dispositivo en la red que se ha detectado por última vez.
ms.assetid: e1893a59-ce7d-4e9c-a013-02ac916d4ee8
keywords:
- Enumeración de ConnectionStatus de media streaming API
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718769"
---
# <a name="connectionstatus-enumeration"></a>Enumeración ConnectionStatus

Representa el estado del dispositivo en la red que se ha detectado por última vez.

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

<span id="Online"></span><span id="online"></span><span id="ONLINE"></span>**Pantalla**
</dt> <dd>

El dispositivo está en línea y activo en la red.

</dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**N**
</dt> <dd>

El dispositivo está desconectado.

</dd> <dt>

<span id="Sleeping"></span><span id="sleeping"></span><span id="SLEEPING"></span>**Actividad**
</dt> <dd>

El dispositivo está actualmente sin conexión, pero se puede reactivar automáticamente cuando se realiza un intento de comunicación con él.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| IDL<br/> | <dl> <dt>Windows. Media. streaming. idl (referencia a Windows. Media. streaming. idl)</dt> </dl> |



 

 





