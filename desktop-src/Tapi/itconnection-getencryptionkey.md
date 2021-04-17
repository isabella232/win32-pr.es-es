---
description: El método GetEncryptionKey obtiene la clave de cifrado.
ms.assetid: a80d8660-d13e-483f-b1d7-ee2043ef5cab
title: 'ITConnection:: GetEncryptionKey (método) (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a826dc8424222587f2838804ec035fb23c2e41d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690203"
---
# <a name="itconnectiongetencryptionkey-method"></a>ITConnection:: GetEncryptionKey (método)

\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

El método **GetEncryptionKey** obtiene la clave de cifrado.

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

*ppKeyType* \[ enuncia\]
</dt> <dd>

Puntero a un **BSTR** que contiene el tipo de clave de cifrado.

</dd> <dt>

*pfValidKeyData* \[ enuncia\]
</dt> <dd>

Indica la validez de los datos de claves de cifrado.

</dd> <dt>

*ppKeyData* \[ enuncia\]
</dt> <dd>

Puntero a un **BSTR** que contiene los datos de la clave de cifrado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | El método se realizó correctamente.<br/>                                                                 |
| <dl> <dt>**\_puntero E**</dt> </dl>     | El parámetro *ppKeyType, pfValidKeyData* o *ppKeyData* no es un puntero válido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No hay memoria suficiente para realizar la operación.<br/>                              |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Error no especificado.<br/>                                                                |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método aún no se ha implementado.<br/>                                               |



 

## <a name="remarks"></a>Observaciones

La aplicación debe usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar la memoria asignada para los parámetros *ppKeyType* y *ppKeyData* .

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
</dt> </dl>

 

