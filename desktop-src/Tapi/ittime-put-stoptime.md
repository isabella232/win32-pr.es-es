---
description: El método put StopTime establece el valor de hora de finalización \_ NTP (Protocolo de hora de red). Si la hora de finalización es cero, la sesión no está limitada.
ms.assetid: 6f07054c-5fb2-4ee4-9025-3acf9b51ddbd
title: ItTime::p ut_StopTime (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e3aa32615988e52ccaa845a8fb7ec52f2e863c7193ee393d7d184e2b3002f59
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117762387"
---
# <a name="ittimeput_stoptime-method"></a>ItTime::p ut \_ StopTime (Método)

\[Las interfaces y los controles de conferencia de telefonía IP de Rendezvous no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método put \_ StopTime** establece el valor de hora de finalización NTP (Protocolo de hora de red). Si la hora de finalización es cero, la sesión no está limitada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_StopTime(
  [in] DOUBLE Time
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Hora* \[ En\]
</dt> <dd>

Hora de detenerse para la sesión.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | El método se realizó correctamente.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | El *parámetro Time* no es válido.<br/>                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No existe memoria suficiente para realizar la operación.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Error no especificado.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método aún no se ha implementado.<br/>                  |



 

## <a name="remarks"></a>Comentarios

Esta función puede enviar datos a través de la conexión en formato sin cifrar; por lo tanto, es posible que alguien interceptado en la red pueda leer los datos. El riesgo de seguridad de enviar los datos en texto no texto debe tenerse en cuenta antes de usar este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ITTime**](ittime.md)
</dt> <dt>

[**ITTime::get \_ StopTime**](ittime-get-stoptime.md)
</dt> </dl>

 

 




