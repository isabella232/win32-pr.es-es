---
description: El \_ método put AddressType establece el tipo de dirección.
ms.assetid: 73c64904-925c-4a35-a8f9-88b196b59b1e
title: 'ITConnection: método de ut_AddressType de:p (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cb9bc9b83a71f78a68b6efc2fa73c259c4afe9e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679319"
---
# <a name="itconnectionput_addresstype-method"></a>ITConnection::p \_ método UT AddressType

\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

El método **Put \_ AddressType** establece el tipo de dirección.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_AddressType(
  [in] BSTR pAddressType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pAddressType* \[ de\]
</dt> <dd>

Puntero a un **BSTR** que contiene el tipo de dirección.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | El método se realizó correctamente.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | El parámetro *pAddressType* no es válido.<br/>           |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No hay memoria suficiente para realizar la operación.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Error no especificado.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método aún no se ha implementado.<br/>                  |



 

## <a name="remarks"></a>Observaciones

La aplicación debe usar [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) para asignar memoria para el parámetro *PAddressType* y usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar memoria cuando la variable ya no se necesite.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITConnection**](itconnection.md)
</dt> <dt>

[**ITConnection:: get \_ AddressType**](itconnection-get-addresstype.md)
</dt> </dl>

 

