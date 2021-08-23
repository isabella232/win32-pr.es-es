---
description: El método get StartTime obtiene el valor de hora de inicio NTP (Protocolo de \_ hora de red) de 32 bits. La sesión se considera activa desde este momento.
ms.assetid: 511e4486-4c73-4610-8e64-9c70acc98eab
title: ItTime::get_StartTime (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea2fcc7aedf94d65f828714a7ebe5e6bbbfd760514654b2b634b479f2fd4802b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060763"
---
# <a name="ittimeget_starttime-method"></a>ItTime::get \_ StartTime (método)

\[Los controles e interfaces de conferencias de telefonía IP de Encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método get \_ StartTime** obtiene el valor de hora de inicio NTP (Protocolo de hora de red) de 32 bits. La sesión se considera activa desde este momento.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_StartTime(
  [out] DOUBLE *pTime
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pTime* \[ out\]
</dt> <dd>

Puntero a la hora de inicio de la sesión.

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

[**ITTime::put \_ StartTime**](ittime-put-starttime.md)
</dt> </dl>

 

 




