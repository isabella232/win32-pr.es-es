---
description: El \_ método get SessionVersion obtiene el valor de 32 bits (idealmente, el protocolo de tiempo de red o NTP) que sirve como versión de sesión.
ms.assetid: 39c2aef4-24e3-4ea0-8b23-dff842f9ab84
title: 'Método ITSdp:: get_SessionVersion (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3466844f3f21f54ec0ec76a3569e7af25e4b0143
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681297"
---
# <a name="itsdpget_sessionversion-method"></a>ITSdp:: get \_ SessionVersion (método)

\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

El método **Get \_ SessionVersion** obtiene el valor de 32 bits (idealmente, el protocolo de tiempo de red o NTP) que sirve como versión de sesión. Aunque esto se genera automáticamente cuando se crea la sesión, el usuario es responsable de cambiarla cuando se modifica SDP.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_SessionVersion(
  [out] DOUBLE *pSessionVersion
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSessionVersion* \[ enuncia\]
</dt> <dd>

Puntero al identificador de la versión de sesión.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                        |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | El método se realizó correctamente.<br/>                                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | El parámetro *pSessionVersion* no es válido.<br/>           |
| <dl> <dt>**\_puntero E**</dt> </dl>     | El parámetro *pSessionVersion* no es un puntero válido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No hay memoria suficiente para realizar la operación.<br/>    |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Error no especificado.<br/>                                      |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método aún no se ha implementado.<br/>                     |



 

## <a name="remarks"></a>Observaciones

El valor devuelto de este método podría ser **ULong**, pero Visual Basic no admite el tipo **ULong** . Un **valor Double** es el siguiente tipo más pequeño que abarca todo el intervalo de valores requerido.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITSdp**](itsdp.md)
</dt> <dt>

[**ITSdp::p UT \_ SessionVersion**](itsdp-put-sessionversion.md)
</dt> </dl>

 

 




