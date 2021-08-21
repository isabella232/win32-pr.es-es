---
description: El método put StartTime establece el valor de hora de inicio NTP (Protocolo de hora de \_ red) de 32 bits. La sesión se considera activa desde este momento.
ms.assetid: c7c96265-4588-4f05-83b6-6ef54f02650b
title: ItTime::p ut_StartTime (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b0e1fe25f2518396ec507f88d0a89c5928f676b64d626c32307336b95ef21e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003233"
---
# <a name="ittimeput_starttime-method"></a>ItTime::p ut \_ StartTime (método)

\[Los controles e interfaces de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método put \_ StartTime** establece el valor de hora de inicio NTP (Protocolo de hora de red) de 32 bits. La sesión se considera activa desde este momento.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_StartTime(
  [in] DOUBLE Time
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Hora* \[ En\]
</dt> <dd>

Hora de inicio de la sesión.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | El método se realizó correctamente.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | El *parámetro Tim* e no es válido.<br/>                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No existe memoria suficiente para realizar la operación.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Error no especificado.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método aún no se ha implementado.<br/>                  |



 

## <a name="remarks"></a>Comentarios

Esta función puede enviar datos a través de la conexión sin cifrar; por lo tanto, alguien que intercepta en la red puede leer los datos. El riesgo de seguridad de enviar los datos en texto sin formato debe tenerse en cuenta antes de usar este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITTime**](ittime.md)
</dt> <dt>

[**ITTime::get \_ StartTime**](ittime-get-starttime.md)
</dt> </dl>

 

 




