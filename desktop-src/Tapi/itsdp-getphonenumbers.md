---
description: El método GetPhoneNumbers obtiene una matriz de números de teléfono asociados a un BLOB de conferencia.
ms.assetid: c4ad6c5a-e15c-45ae-94de-763a843554bb
title: 'ITSdp:: GetPhoneNumbers (método) (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 465bc6b2d2167ca17d25b8f50466f111724ea3b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681082"
---
# <a name="itsdpgetphonenumbers-method"></a>ITSdp:: GetPhoneNumbers (método)

\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

El método **GetPhoneNumbers** obtiene una matriz de números de teléfono asociados a un BLOB de conferencia.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetPhoneNumbers(
  [out] VARIANT *pNumbers,
  [out] VARIANT *pNames
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pNumbers* \[ enuncia\]
</dt> <dd>

Puntero **Variant** a una matriz SafeArray de **BSTR** s que enumera los números de teléfono.

</dd> <dt>

*pNames* \[ enuncia\]
</dt> <dd>

Puntero **Variant** a una matriz SafeArray de nombres de lista **BSTR** s.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                             |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | El método se realizó correctamente.<br/>                                            |
| <dl> <dt>**\_puntero E**</dt> </dl>     | El parámetro *pNumbers* o *pNames* no es un puntero válido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No hay memoria suficiente para realizar la operación.<br/>         |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Error no especificado.<br/>                                           |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método aún no se ha implementado.<br/>                          |



 

## <a name="remarks"></a>Observaciones

Las listas a las que apuntan *pNumbers* y *pNames* tienen la misma longitud.

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

 

 




