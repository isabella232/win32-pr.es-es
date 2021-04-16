---
description: El \_ método get characterSet obtiene un \_ \_ descriptor de juego de caracteres de BLOB del juego de caracteres utilizado en el BLOB de la Conferencia actual.
ms.assetid: 9783d18c-79f6-4faa-b12d-9504c13d54e3
title: 'Método ITConferenceBlob:: get_CharacterSet (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 681085672f49c75a8434c4b0311e75d2b9cea270
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680208"
---
# <a name="itconferenceblobget_characterset-method"></a>ITConferenceBlob:: get \_ characterSet (método)

\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

El método **Get \_ characterSet** obtiene un descriptor de juego de [**\_ caracteres \_ de BLOB**](blob-character-set.md) del juego de caracteres utilizado en el BLOB de la Conferencia actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_CharacterSet(
  [out] BLOB_CHARACTER_SET *pCharacterSet
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pCharacterSet* \[ enuncia\]
</dt> <dd>

Puntero a un descriptor del juego de [**\_ \_ caracteres de BLOB**](blob-character-set.md) del juego de caracteres.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                                   | Descripción                                                      |
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                          | El método se realizó correctamente.<br/>                                     |
| <dl> <dt>**\_puntero E**</dt> </dl>                     | El parámetro *pCharacterSet* no es un puntero válido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>                 | No hay memoria suficiente para realizar la operación.<br/>  |
| <dl> <dt>**E \_ FAIL**</dt> </dl>                        | Error no especificado.<br/>                                    |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>                     | Este método aún no se ha implementado.<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                  | *pCharacterSet* es **null**.<br/>                          |
| <dl> <dt>**VALOR ERROR de \_ datos no válidos \_**</dt> </dl> | El juego de caracteres actual no es válido o no está disponible.<br/>  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITConferenceBlob**](itconferenceblob.md)
</dt> <dt>

[**\_juego de caracteres de blob \_**](blob-character-set.md)
</dt> </dl>

 

 




