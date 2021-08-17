---
description: La enumeración H245 CAPABILITY describe la compatibilidad \_ con el formato de audio y vídeo.
ms.assetid: 76aeb3a1-3233-4425-b9db-efacbedc309e
title: H245_CAPABILITY enumeración (H323priv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1666eb918748696263247f00f0d0e17ac9424e6c4bf85c5574f866bb10e28be1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140558"
---
# <a name="h245_capability-enumeration"></a>Enumeración H245 \_ CAPABILITY

\[**H245 \_ CAPABILITY** no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

La **enumeración H245 \_ CAPABILITY** describe la compatibilidad con el formato de audio y vídeo.

## <a name="syntax"></a>Syntax


```C++
} H245_CAPABILITY;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="HC_G711"></span><span id="hc_g711"></span>**HC \_ G711**
</dt> <dd>

Se admite el protocolo de audio G.711.

</dd> <dt>

<span id="HC_G723"></span><span id="hc_g723"></span>**HC \_ G723**
</dt> <dd>

Se admite el protocolo de audio G.723.

</dd> <dt>

<span id="HC_H263QCIF"></span><span id="hc_h263qcif"></span>**HC \_ H263QCIF**
</dt> <dd>

Se admite el protocolo de vídeo H.263.

</dd> <dt>

<span id="HC_H261QCIF"></span><span id="hc_h261qcif"></span>**HC \_ H261QCIF**
</dt> <dd>

Se admite el protocolo de vídeo H.263.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Header<br/>       | <dl> <dt>H323priv.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IH323LineEx::SetDefaultCapabilityPreferrence**](ih323lineex-setdefaultcapabilitypreferrence.md)
</dt> </dl>

 

 




