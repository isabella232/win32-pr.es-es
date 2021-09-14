---
description: El método put \_ AddressType establece el tipo de dirección.
ms.assetid: 73c64904-925c-4a35-a8f9-88b196b59b1e
title: Método ITConnection::p ut_AddressType (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cb9bc9b83a71f78a68b6efc2fa73c259c4afe9e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170705"
---
# <a name="itconnectionput_addresstype-method"></a>ItConnection::p ut \_ AddressType (método)

\[Los controles e interfaces de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método put \_ AddressType** establece el tipo de dirección.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_AddressType(
  [in] BSTR pAddressType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pAddressType* \[ En\]
</dt> <dd>

Puntero a un **BSTR** que contiene el tipo de dirección.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | El método se realizó correctamente.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | El *parámetro pAddressType* no es válido.<br/>           |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No existe memoria suficiente para realizar la operación.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Error no especificado.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método aún no se ha implementado.<br/>                  |



 

## <a name="remarks"></a>Observaciones

La aplicación debe usar [**SysAllocString para**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) asignar memoria para el parámetro *pAddressType* y usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar la memoria cuando la variable ya no sea necesaria.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITConnection**](itconnection.md)
</dt> <dt>

[**ITConnection::get \_ AddressType**](itconnection-get-addresstype.md)
</dt> </dl>

 

