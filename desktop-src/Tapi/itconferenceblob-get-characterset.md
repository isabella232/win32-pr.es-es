---
description: El método get \_ CharacterSet obtiene un descriptor BLOB \_ CHARACTER SET del juego de caracteres usado en el blob de conferencia \_ actual.
ms.assetid: 9783d18c-79f6-4faa-b12d-9504c13d54e3
title: ItConferenceBlob::get_CharacterSet (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20a9dd719d2ae9742a6ec4b3295e3e22ffe871b4a38c55d07e07a3421271553d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061003"
---
# <a name="itconferenceblobget_characterset-method"></a>ItConferenceBlob::get \_ CharacterSet (método)

\[Los controles e interfaces de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método get \_ CharacterSet** obtiene un descriptor [**BLOB CHARACTER \_ \_ SET**](blob-character-set.md) del juego de caracteres usado en el blob de conferencia actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_CharacterSet(
  [out] BLOB_CHARACTER_SET *pCharacterSet
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pCharacterSet* \[ out\]
</dt> <dd>

Puntero a un [**descriptor BLOB \_ CHARACTER \_ SET**](blob-character-set.md) del juego de caracteres.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                                   | Descripción                                                      |
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                          | El método se realizó correctamente.<br/>                                     |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>                     | El *parámetro pCharacterSet* no es un puntero válido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>                 | No existe memoria suficiente para realizar la operación.<br/>  |
| <dl> <dt>**E \_ FAIL**</dt> </dl>                        | Error no especificado.<br/>                                    |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>                     | Este método aún no se ha implementado.<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                  | *pCharacterSet* es **NULL.**<br/>                          |
| <dl> <dt>**(HRESULT) ERROR \_ DATOS NO \_ VÁLIDOS**</dt> </dl> | El juego de caracteres actual no es válido o no está disponible.<br/>  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITConferenceBlob**](itconferenceblob.md)
</dt> <dt>

[**JUEGO \_ DE CARACTERES DE \_ BLOB**](blob-character-set.md)
</dt> </dl>

 

 




