---
description: El método GetEmailNames obtiene una matriz de nombres de correo electrónico asociada al BLOB de la Conferencia.
ms.assetid: e51f25d7-41e5-408e-930b-396c7ac24437
title: 'ITSdp:: GetEmailNames (método) (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31f0200b5cc6ea0422f47a323cd1c57d7e0f9a5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690006"
---
# <a name="itsdpgetemailnames-method"></a>ITSdp:: GetEmailNames (método)

\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

El método **GetEmailNames** obtiene una matriz de nombres de correo electrónico asociada al BLOB de la Conferencia.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetEmailNames(
  [out] VARIANT *pAddresses,
  [out] VARIANT *pNames
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pAddresses* \[ enuncia\]
</dt> <dd>

Puntero **Variant** a una matriz SafeArray de **BSTR** s que enumera las direcciones de correo electrónico.

</dd> <dt>

*pNames* \[ enuncia\]
</dt> <dd>

Puntero **Variant** a una matriz SafeArray de nombres de lista **BSTR** s.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                               |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | El método se realizó correctamente.<br/>                                              |
| <dl> <dt>**\_puntero E**</dt> </dl>     | El parámetro *pAddresses* o *pNames* no es un puntero válido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No hay memoria suficiente para realizar la operación.<br/>           |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Error no especificado.<br/>                                             |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método aún no se ha implementado.<br/>                            |



 

## <a name="remarks"></a>Observaciones

Las listas a las que apuntan *pAddresses* y *pNames* tienen la misma longitud.

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

 

 




