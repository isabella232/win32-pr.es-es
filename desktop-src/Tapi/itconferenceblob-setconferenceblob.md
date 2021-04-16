---
description: El método SetConferenceBlob confirma los cambios en el BLOB de la Conferencia. Para inicializar el BLOB de la Conferencia por primera vez, utilice en su lugar el método init.
ms.assetid: 4a65edb9-77de-42d9-85a1-1e3c41706417
title: 'ITConferenceBlob:: SetConferenceBlob (método) (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47779807e5bde6a070b4600aec903309c7679dc8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680205"
---
# <a name="itconferenceblobsetconferenceblob-method"></a>ITConferenceBlob:: SetConferenceBlob (método)

\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

El método **SetConferenceBlob** confirma los cambios en el BLOB de la Conferencia. Para inicializar el BLOB de la Conferencia por primera vez, utilice en su lugar el método [**init**](itconferenceblob-init.md) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetConferenceBlob(
  [in] BLOB_CHARACTER_SET CharacterSet,
  [in] BSTR               pBlob
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*CharacterSet* \[ de\]
</dt> <dd>

[**BLOB \_ de \_**](blob-character-set.md) Descriptor del juego de caracteres del juego de caracteres del BLOB de la Conferencia.

</dd> <dt>

*pBlob* \[ de\]
</dt> <dd>

Puntero a un **BSTR** que contiene el BLOB de la Conferencia.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                      |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | El método se realizó correctamente.<br/>                                     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | El parámetro *characterSet* o *pBlob* no es válido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No hay memoria suficiente para realizar la operación.<br/>  |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Error no especificado.<br/>                                    |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método aún no se ha implementado.<br/>                   |



 

## <a name="remarks"></a>Observaciones

La aplicación debe usar [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) para asignar memoria para el parámetro *PBlob* y usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar memoria cuando la variable ya no se necesite.

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

 

