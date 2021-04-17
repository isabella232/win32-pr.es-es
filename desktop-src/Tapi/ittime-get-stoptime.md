---
description: El \_ método get StopTime obtiene el valor de hora de finalización del Protocolo de tiempo de red (NTP). Si la hora de finalización es cero, la sesión no está enlazada.
ms.assetid: f18042c0-e41d-43b3-a75d-6ab161afde6e
title: 'Método ITTime:: get_StopTime (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b55ac03c4701884b5a4b7716cb2758887b6160bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690244"
---
# <a name="ittimeget_stoptime-method"></a>ITTime:: get \_ StopTime (método)

\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

El método **Get \_ StopTime** obtiene el valor de hora de finalización del Protocolo de tiempo de red (NTP). Si la hora de finalización es cero, la sesión no está enlazada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_StopTime(
  [out] DOUBLE *pTime
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pTime* \[ enuncia\]
</dt> <dd>

Puntero a la hora de detención de la sesión.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | El método se realizó correctamente.<br/>                                    |
| <dl> <dt>**\_puntero E**</dt> </dl>     | El parámetro *pTime* no es un puntero válido.<br/>        |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No hay memoria suficiente para realizar la operación.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Error no especificado.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método aún no se ha implementado.<br/>                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITTime**](ittime.md)
</dt> <dt>

[**ITTime::p UT \_ StopTime**](ittime-put-stoptime.md)
</dt> </dl>

 

 




