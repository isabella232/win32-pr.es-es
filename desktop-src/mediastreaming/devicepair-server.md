---
title: Propiedad del servidor DevicePair (Asptlb. h)
description: Obtiene el servidor para el par de dispositivo básico activo.
ms.assetid: 25FD523F-36C7-4165-BBB2-6A3410D896EF
keywords:
- Propiedad de servidor API de streaming de multimedia
- Propiedad de servidor API de streaming de multimedia, interfaz DevicePair
- Interfaz DevicePair API de streaming de multimedia, propiedad de servidor
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
ms.openlocfilehash: eec2c28e8118f6cf11e89c7ab4a5ba04abd8b8f5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718600"
---
# <a name="devicepairserver-property"></a>DevicePair:: Server (propiedad)

Obtiene el servidor para el par de dispositivo básico activo.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Server(
  [out] ActiveBasicDevice **value
);
```



## <a name="property-value"></a>Valor de propiedad

Recibe un objeto [**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85)) que representa el dispositivo de servidor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Asptlb. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**DevicePair**](/previous-versions/windows/desktop/legacy/dn385771(v=vs.85))
</dt> </dl>

 

