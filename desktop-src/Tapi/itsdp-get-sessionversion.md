---
description: El método get SessionVersion obtiene el valor de 32 bits (idealmente Protocolo de tiempo de red o NTP) que \_ actúa como versión de la sesión.
ms.assetid: 39c2aef4-24e3-4ea0-8b23-dff842f9ab84
title: Método ITSdp::get_SessionVersion (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7661fb5f133d214748991510d56387991872fa69243353b5144623a1ef19f91
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119476595"
---
# <a name="itsdpget_sessionversion-method"></a>ItSdp::get \_ SessionVersion (método)

\[Los controles e interfaces de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método get \_ SessionVersion** obtiene el valor de 32 bits (idealmente Protocolo de tiempo de red o NTP) que actúa como versión de la sesión. Aunque esto se genera automáticamente cuando se crea la sesión, el usuario es responsable de cambiarla cuando se modifica el SDP.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_SessionVersion(
  [out] DOUBLE *pSessionVersion
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSessionVersion* \[ out\]
</dt> <dd>

Puntero al identificador de versión de sesión.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                        |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | El método se realizó correctamente.<br/>                                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | El *parámetro pSessionVersion* no es válido.<br/>           |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | El *parámetro pSessionVersion* no es un puntero válido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No existe memoria suficiente para realizar la operación.<br/>    |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Error no especificado.<br/>                                      |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método aún no se ha implementado.<br/>                     |



 

## <a name="remarks"></a>Observaciones

El valor devuelto de este método podría ser **ULONG,** Visual Basic no admite el **tipo ULONG.** Double **es** el siguiente tipo más pequeño que abarca todo el intervalo de valores necesarios.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITSdp**](itsdp.md)
</dt> <dt>

[**ITSdp::put \_ SessionVersion**](itsdp-put-sessionversion.md)
</dt> </dl>

 

 




