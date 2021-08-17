---
title: Propiedad DevicePair Server (Asptlb.h)
description: Obtiene el servidor para el par de dispositivos básico activo.
ms.assetid: 25FD523F-36C7-4165-BBB2-6A3410D896EF
keywords:
- Propiedad de servidor Media Streaming API
- Propiedad de servidor Media Streaming API, interfaz DevicePair
- Interfaz DevicePair Media Streaming API, propiedad Server
topic_type:
- apiref
api_name:
- DevicePair.Server
- DevicePair.get_Server
api_location:
- asptlb.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d0939a27d96de8f2c8ff53ffd7b0bd766292b873450fb138d0877e916c691f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119100729"
---
# <a name="devicepairserver-property"></a>DevicePair::Server, propiedad

Obtiene el servidor para el par de dispositivos básico activo.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Server(
  [out] ActiveBasicDevice **value
);
```



## <a name="property-value"></a>Valor de propiedad

Recibe un [**objeto ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85)) que representa el dispositivo del servidor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Asptlb.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**DevicePair**](/previous-versions/windows/desktop/legacy/dn385771(v=vs.85))
</dt> </dl>

 

