---
title: Enumeración TransportStatus
description: Define el estado de transporte disponible tal y como se define en las directrices de UPnP.
ms.assetid: 6fde82f0-9bc4-4abb-9d10-0000501c2b24
keywords:
- Enumeración de TransportStatus de media streaming API
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718981"
---
# <a name="transportstatus-enumeration"></a>Enumeración TransportStatus

Define el estado de transporte disponible tal y como se define en las directrices de UPnP.

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

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown**
</dt> <dd>

Estado de dispositivo erróneo.

</dd> <dt>

<span id="Ok"></span><span id="ok"></span><span id="OK"></span>**Vale**
</dt> <dd>

El dispositivo está en buen estado.

</dd> <dt>

<span id="ErrorOccurred"></span><span id="erroroccurred"></span><span id="ERROROCCURRED"></span>**ErrorOccurred**
</dt> <dd>

Error en el dispositivo.

</dd> <dt>

<span id="Last"></span><span id="last"></span><span id="LAST"></span>**Guardado**
</dt> <dd>

El estado anterior del dispositivo es el estado de transporte actual.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| IDL<br/> | <dl> <dt>Windows. Media. streaming. idl (referencia a Windows. Media. streaming. idl)</dt> </dl> |



 

 





