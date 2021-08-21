---
description: El método GetEncryptionKey obtiene la clave de cifrado.
ms.assetid: a80d8660-d13e-483f-b1d7-ee2043ef5cab
title: Método ITConnection::GetEncryptionKey (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a237073d4842cd26797b046a4d973390ff5ef254b574bcafbc6f10abca932aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060983"
---
# <a name="itconnectiongetencryptionkey-method"></a>ItConnection::GetEncryptionKey (método)

\[Las interfaces y los controles de conferencia de telefonía IP de Rendezvous no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método GetEncryptionKey** obtiene la clave de cifrado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetEncryptionKey(
  [out] BSTR         *ppKeyType,
  [out] VARIANT_BOOL *pfValidKeyData,
  [out] BSTR         *ppKeyData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppKeyType* \[ out\]
</dt> <dd>

Puntero a un **BSTR** que contiene el tipo de clave de cifrado.

</dd> <dt>

*pfValidKeyData* \[ out\]
</dt> <dd>

Indica la validez de los datos de clave de cifrado.

</dd> <dt>

*ppKeyData* \[ out\]
</dt> <dd>

Puntero a un **BSTR** que contiene los datos de la clave de cifrado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | El método se realizó correctamente.<br/>                                                                 |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | El *parámetro ppKeyType, pfValidKeyData o* *ppKeyData* no es un puntero válido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No existe memoria suficiente para realizar la operación.<br/>                              |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Error no especificado.<br/>                                                                |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método aún no se ha implementado.<br/>                                               |



 

## <a name="remarks"></a>Comentarios

La aplicación debe usar [**SysFreeString para**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) liberar la memoria asignada para los *parámetros ppKeyType* y *ppKeyData.*

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITConnection**](itconnection.md)
</dt> </dl>

 

