---
description: El \_ método get SessionID obtiene el valor de NTP de 32 bits (Protocolo de tiempo de red) que actúa como identificador de sesión. Se genera automáticamente cuando se crea la sesión.
ms.assetid: 5177f120-4b93-40bc-9481-aedf65a8dee9
title: 'Método ITSdp:: get_SessionId (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ad593b61f4c935a220e59383ae170569f04af54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690332"
---
# <a name="itsdpget_sessionid-method"></a>ITSdp:: get \_ SessionID (método)

\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

El método **Get \_ SessionID** obtiene el valor de NTP de 32 bits (Protocolo de tiempo de red) que actúa como identificador de sesión. Se genera automáticamente cuando se crea la sesión.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_SessionId(
  [out] DOUBLE *pSessionId
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSessionId* \[ enuncia\]
</dt> <dd>

Puntero al identificador de sesión.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | El método se realizó correctamente.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | El parámetro *pSessionId* no es válido.<br/>             |
| <dl> <dt>**\_puntero E**</dt> </dl>     | El parámetro *pSessionId* no es un puntero válido.<br/>   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No hay memoria suficiente para realizar la operación.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Error no especificado.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método aún no se ha implementado.<br/>                  |



 

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
</dt> </dl>

 

 




