---
description: El método get StopTime obtiene el valor de hora de finalización NTP (Protocolo de tiempo \_ de red). Si la hora de finalización es cero, la sesión no está limitada.
ms.assetid: f18042c0-e41d-43b3-a75d-6ab161afde6e
title: ItTime::get_StopTime (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9eca063fd67064e9f9140d03d97351313c4247dbe3351739fa6e2d336229ffe3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117945014"
---
# <a name="ittimeget_stoptime-method"></a>ItTime::get \_ StopTime (método)

\[Los controles e interfaces de conferencias de telefonía IP de Encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método get \_ StopTime** obtiene el valor de hora de finalización NTP (Protocolo de tiempo de red). Si la hora de finalización es cero, la sesión no está limitada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_StopTime(
  [out] DOUBLE *pTime
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pTime* \[ out\]
</dt> <dd>

Puntero a la hora de detenerse de la sesión.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | El método se realizó correctamente.<br/>                                    |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | El *parámetro pTime* no es un puntero válido.<br/>        |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No existe memoria suficiente para realizar la operación.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Error no especificado.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método aún no se ha implementado.<br/>                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITTime**](ittime.md)
</dt> <dt>

[**ITTime::put \_ StopTime**](ittime-put-stoptime.md)
</dt> </dl>

 

 




