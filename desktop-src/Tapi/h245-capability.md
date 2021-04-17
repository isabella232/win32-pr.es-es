---
description: La \_ enumeración de la funcionalidad H245 describe la compatibilidad con el formato de audio y vídeo.
ms.assetid: 76aeb3a1-3233-4425-b9db-efacbedc309e
title: Enumeración H245_CAPABILITY (H323priv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae7a6f81f87480f221f87680d9cf086120deb2de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690954"
---
# <a name="h245_capability-enumeration"></a>\_Enumeración de la funcionalidad H245

\[**H245 \_ La funcionalidad** no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

La enumeración de la **\_ funcionalidad H245** describe la compatibilidad con el formato de audio y vídeo.

## <a name="syntax"></a>Sintaxis


```C++
} H245_CAPABILITY;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="HC_G711"></span><span id="hc_g711"></span>**HC \_ G711**
</dt> <dd>

Se admite el protocolo de audio G. 711.

</dd> <dt>

<span id="HC_G723"></span><span id="hc_g723"></span>**HC \_ G723**
</dt> <dd>

Se admite el protocolo de audio G. 723.

</dd> <dt>

<span id="HC_H263QCIF"></span><span id="hc_h263qcif"></span>**HC \_ H263QCIF**
</dt> <dd>

Se admite el protocolo de vídeo H. 263.

</dd> <dt>

<span id="HC_H261QCIF"></span><span id="hc_h261qcif"></span>**HC \_ H261QCIF**
</dt> <dd>

Se admite el protocolo de vídeo H. 263.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>H323priv. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IH323LineEx::SetDefaultCapabilityPreferrence**](ih323lineex-setdefaultcapabilitypreferrence.md)
</dt> </dl>

 

 




