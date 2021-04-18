---
title: Enumeración MPDETECTION_ORIGIN (MpClient. h)
description: Origen de la detección.
ms.assetid: 9FEE2FAD-3E44-4134-B968-53E971F6B092
keywords:
- MPDETECTION_ORIGIN enumeración características de entorno heredado de Windows
- PMPDETECTION_ORIGIN el puntero de enumeración características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MPDETECTION_ORIGIN
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed4224aafef2c72db2a8d3b27f338ca83feaf64f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105656519"
---
# <a name="mpdetection_origin-enumeration"></a>\_Enumeración de origen MPDETECTION

Origen de la detección.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum tagMPDETECTION_ORIGIN { 
  MPDETECTION_ORIGIN_UNKNOWN        = 0,
  MPDETECTION_ORIGIN_LOCAL_MACHINE  = 1 << 0,
  MPDETECTION_ORIGIN_NETWORKSHARE   = 1 << 1,
  MPDETECTION_ORIGIN_INTERNET       = 1 << 2,
  MPDETECTION_ORIGIN_OUTBOUND       = 1 << 3,
  MPDETECTION_ORIGIN_INBOUND        = 1 << 4
} MPDETECTION_ORIGIN, *PMPDETECTION_ORIGIN;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MPDETECTION_ORIGIN_UNKNOWN"></span><span id="mpdetection_origin_unknown"></span>**origen de MPDETECTION \_ \_ desconocido**
</dt> <dd>

Origen detectado de amenaza desconocida.

</dd> <dt>

<span id="MPDETECTION_ORIGIN_LOCAL_MACHINE"></span><span id="mpdetection_origin_local_machine"></span>**\_ \_ máquina local de origen de MPDETECTION \_**
</dt> <dd>

Amenaza detectada en el equipo local.

</dd> <dt>

<span id="MPDETECTION_ORIGIN_NETWORKSHARE"></span><span id="mpdetection_origin_networkshare"></span>**MPDETECTION \_ Origin \_ NETWORKSHARE**
</dt> <dd>

Amenaza detectada en el recurso compartido de red.

</dd> <dt>

<span id="MPDETECTION_ORIGIN_INTERNET"></span><span id="mpdetection_origin_internet"></span>**MPDETECTION \_ Origin \_ Internet**
</dt> <dd>

Amenaza detectada en Internet.

</dd> <dt>

<span id="MPDETECTION_ORIGIN_OUTBOUND"></span><span id="mpdetection_origin_outbound"></span>**\_salida de origen de MPDETECTION \_**
</dt> <dd>

Amenaza detectada en una conexión de salida.

</dd> <dt>

<span id="MPDETECTION_ORIGIN_INBOUND"></span><span id="mpdetection_origin_inbound"></span>**\_entrada de origen de MPDETECTION \_**
</dt> <dd>

Amenaza detectada en una conexión entrante.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





