---
description: El método init inicializa el BLOB de la Conferencia en función de una cadena de texto. Si pBlob es NULL, se usan los valores predeterminados.
ms.assetid: ba492503-90ff-45dd-a39f-6d4451e57339
title: 'ITConferenceBlob:: init (método) (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81bdd512ffeb4b380da04e59deb17315d00b7285
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690441"
---
# <a name="itconferenceblobinit-method"></a>ITConferenceBlob:: init (método)

\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

El método **init** inicializa el BLOB de la Conferencia en función de una cadena de texto. Si *pBlob* es **null**, se usan los valores predeterminados.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Init(
  [in] BSTR               pName,
  [in] BLOB_CHARACTER_SET CharacterSet,
  [in] BSTR               pBlob
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pName* \[ de\]
</dt> <dd>

Puntero a una representación **BSTR** del nombre de la Conferencia.

</dd> <dt>

*CharacterSet* \[ de\]
</dt> <dd>

[**BLOB \_ de Descriptor \_ del juego de caracteres del**](blob-character-set.md) juego de caracteres.

</dd> <dt>

*pBlob* \[ de\]
</dt> <dd>

Puntero a un **BSTR** que contiene el BLOB de la Conferencia. Si es **null**, el BLOB de la Conferencia se inicializa con los valores predeterminados. Actualmente, los valores de conferencia predeterminados solo están disponibles si el parámetro *characterSet* está establecido en el ASCII de BCS \_ .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Value                                                                                         | Significado                                                                    |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | El método se realizó correctamente.<br/>                                               |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | El parámetro *pName*, *characterSet* o *pBlob* no es válido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No hay memoria suficiente para realizar la operación.<br/>            |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Error no especificado.<br/>                                              |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método aún no se ha implementado.<br/>                             |



 

## <a name="remarks"></a>Observaciones

**ITConferenceBlob:: init** devolverá un error si ya se ha inicializado el BLOB.

La aplicación debe usar [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) para asignar memoria para los parámetros *pName* y *pBlob* . La aplicación debe usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar memoria cuando las variables ya no se necesiten.

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

 

