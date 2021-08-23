---
description: El método GetPhoneNumbers obtiene una matriz de números de teléfono asociados a un blob de conferencia.
ms.assetid: c4ad6c5a-e15c-45ae-94de-763a843554bb
title: Método ITSdp::GetPhoneNumbers (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d417a86ba89269055aa7e30a94724f58da7978d58d80a61d65f6caec8793d5ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060813"
---
# <a name="itsdpgetphonenumbers-method"></a>ItSdp::GetPhoneNumbers (método)

\[Las interfaces y los controles de conferencia de telefonía IP de Rendezvous no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método GetPhoneNumbers** obtiene una matriz de números de teléfono asociados a un blob de conferencia.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetPhoneNumbers(
  [out] VARIANT *pNumbers,
  [out] VARIANT *pNames
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pNumbers* \[ out\]
</dt> <dd>

**Puntero VARIANT** a una SAFEARRAY de **BSTR** que enumera números de teléfono.

</dd> <dt>

*pNames* \[ out\]
</dt> <dd>

**Puntero VARIANT** a una SAFEARRAY de nombres de lista de **BSTR.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                             |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | El método se realizó correctamente.<br/>                                            |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | El *parámetro pNumbers* o *pNames* no es un puntero válido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No existe memoria suficiente para realizar la operación.<br/>         |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Error no especificado.<br/>                                           |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método aún no se ha implementado.<br/>                          |



 

## <a name="remarks"></a>Comentarios

Las listas a *las que apuntan pNumbers* y *pNames* tienen la misma longitud.

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
</dt> </dl>

 

 




