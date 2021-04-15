---
description: El método SetEncryptionKey establece la clave de cifrado necesaria para descifrar la sesión o una indicación de un mecanismo para obtener una clave utilizable de forma externa.
ms.assetid: 9efcf90e-3645-49f4-b27d-9a8246637310
title: 'ITConnection:: SetEncryptionKey (método) (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91d0ce079d3815897c348e553df0af8dece8592b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690197"
---
# <a name="itconnectionsetencryptionkey-method"></a>ITConnection:: SetEncryptionKey (método)

\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

El método **SetEncryptionKey** establece la clave de cifrado necesaria para descifrar la sesión o una indicación de un mecanismo para obtener una clave utilizable de forma externa.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetEncryptionKey(
  [in] BSTR pKeyType,
  [in] BSTR *ppKeyData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pKeyType* \[ de\]
</dt> <dd>

Puntero a un **BSTR** que contiene el tipo de clave de cifrado.

</dd> <dt>

*ppKeyData* \[ de\]
</dt> <dd>

Puntero a un **BSTR** que contiene información de la clave de cifrado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                          | Descripción                  |
|--------------------------------------------------------------------------------------|------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | El método se realizó correctamente.<br/> |



 

## <a name="remarks"></a>Observaciones

La aplicación debe usar [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) para asignar memoria para los parámetros *pKeyType* y *ppKeyData* . La aplicación debe usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar memoria cuando las variables ya no se necesiten.

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

 

