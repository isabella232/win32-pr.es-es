---
title: Enumeración TransportStatus
description: Define el estado de transporte disponible tal como se define en las directrices de UPnP.
ms.assetid: 6fde82f0-9bc4-4abb-9d10-0000501c2b24
keywords:
- Enumeración TransportStatus Media Streaming API
topic_type:
- apiref
api_name:
- TransportStatus
api_location:
- Windows.Media.Streaming.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb4a9de34f358db96b468dbd3329483a8e09b6b7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127571640"
---
# <a name="transportstatus-enumeration"></a>Enumeración TransportStatus

Define el estado de transporte disponible tal como se define en las directrices de UPnP.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum TransportStatus { 
  Unknown        = 0,
  Ok             = 1,
  ErrorOccurred  = 2,
  Last           = 3
} TransportStatus;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido**
</dt> <dd>

Estado de dispositivo erróneo.

</dd> <dt>

<span id="Ok"></span><span id="ok"></span><span id="OK"></span>**Vale**
</dt> <dd>

El dispositivo está en buen estado.

</dd> <dt>

<span id="ErrorOccurred"></span><span id="erroroccurred"></span><span id="ERROROCCURRED"></span>**ErrorOccurred**
</dt> <dd>

Se produjo un error en el dispositivo.

</dd> <dt>

<span id="Last"></span><span id="last"></span><span id="LAST"></span>**Última**
</dt> <dd>

Estado anterior del dispositivo al estado de transporte actual.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| IDL<br/> | <dl> <dt>Windows. Media.Streaming.idl (referencia Windows. Media.Streaming.idl)</dt> </dl> |



 

 





