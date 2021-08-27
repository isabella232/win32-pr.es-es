---
title: MPDETECTION_ORIGIN enumeración (MpClient.h)
description: Origen de la detección.
ms.assetid: 9FEE2FAD-3E44-4134-B968-53E971F6B092
keywords:
- MPDETECTION_ORIGIN enumeración heredada de Windows environment
- PMPDETECTION_ORIGIN puntero de enumeración Legacy Windows Environment Features
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
ms.openlocfilehash: 70b46ed86276ccb3fc3bd4d2b26388d778c102c1c1fa3bb7ced8f1ad64cd0203
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092365"
---
# <a name="mpdetection_origin-enumeration"></a>Enumeración MPDETECTION \_ ORIGIN

Origen de la detección.

## <a name="syntax"></a>Syntax


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

<span id="MPDETECTION_ORIGIN_UNKNOWN"></span><span id="mpdetection_origin_unknown"></span>**ORIGEN DE MPDETECTION \_ \_ DESCONOCIDO**
</dt> <dd>

Origen desconocido de la amenaza detectada.

</dd> <dt>

<span id="MPDETECTION_ORIGIN_LOCAL_MACHINE"></span><span id="mpdetection_origin_local_machine"></span>**MÁQUINA LOCAL DE \_ ORIGEN DE MPDETECTION \_ \_**
</dt> <dd>

Amenaza detectada en la máquina local.

</dd> <dt>

<span id="MPDETECTION_ORIGIN_NETWORKSHARE"></span><span id="mpdetection_origin_networkshare"></span>**MPDETECTION \_ ORIGIN \_ NETWORKSHARE**
</dt> <dd>

Amenaza detectada en el recurso compartido de red.

</dd> <dt>

<span id="MPDETECTION_ORIGIN_INTERNET"></span><span id="mpdetection_origin_internet"></span>**MPDETECTION \_ ORIGIN \_ INTERNET**
</dt> <dd>

Se detectó una amenaza en Internet.

</dd> <dt>

<span id="MPDETECTION_ORIGIN_OUTBOUND"></span><span id="mpdetection_origin_outbound"></span>**SALIDA DE ORIGEN \_ DE MPDETECTION \_**
</dt> <dd>

Amenaza detectada en una conexión saliente.

</dd> <dt>

<span id="MPDETECTION_ORIGIN_INBOUND"></span><span id="mpdetection_origin_inbound"></span>**ORIGEN DE MPDETECTION \_ \_ ENTRANTE**
</dt> <dd>

Amenaza detectada en una conexión entrante.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





