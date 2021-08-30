---
description: El método get \_ AddressType obtiene el tipo de dirección.
ms.assetid: b2ff6303-6beb-429c-ad1a-2f729749e5db
title: Método ITConnection::get_AddressType (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10fdfc4c46a84e2a859c0cfb73276fd34a54153ba8d36b235adbec2a1ca4ba09
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119975825"
---
# <a name="itconnectionget_addresstype-method"></a>ItConnection::get \_ AddressType (método)

\[Las interfaces y los controles de conferencia de telefonía IP de Rendezvous no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método get \_ AddressType** obtiene el tipo de dirección.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_AddressType(
  [out] BSTR *ppAddressType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppAddressType* \[ out\]
</dt> <dd>

Puntero a un **BSTR** que contiene el tipo de dirección.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                      |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | El método se realizó correctamente.<br/>                                     |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | El *parámetro ppAddressType* no es un puntero válido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No existe memoria suficiente para realizar la operación.<br/>  |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Error no especificado.<br/>                                    |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método aún no se ha implementado.<br/>                   |



 

## <a name="remarks"></a>Comentarios

La aplicación debe usar [**SysFreeString para**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) liberar la memoria asignada para el *parámetro ppAddressType.*

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITConnection**](itconnection.md)
</dt> <dt>

[**ITConnection::put \_ AddressType**](itconnection-put-addresstype.md)
</dt> </dl>

 

