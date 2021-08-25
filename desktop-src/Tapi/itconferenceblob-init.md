---
description: El método Init inicializa el blob de conferencia basándose en una cadena textual. Si pBlob es NULL, se usan los valores predeterminados.
ms.assetid: ba492503-90ff-45dd-a39f-6d4451e57339
title: Método ITConferenceBlob::Init (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a4f7816d1de346e12b3fab799728f32fb146664846d9dcb6d7cd7df757d62e7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991938"
---
# <a name="itconferenceblobinit-method"></a>ITConferenceBlob::Init (método)

\[Los controles e interfaces de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método Init** inicializa el blob de conferencia basándose en una cadena textual. Si *pBlob es* **NULL,** se usan los valores predeterminados.

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

*pName* \[ En\]
</dt> <dd>

Puntero a una **representación BSTR** del nombre de la conferencia.

</dd> <dt>

*Juego de caracteres* \[ En\]
</dt> <dd>

[**BLOB \_ Descriptor \_ CHARACTER SET**](blob-character-set.md) del juego de caracteres.

</dd> <dt>

*pBlob* \[ En\]
</dt> <dd>

Puntero a un **BSTR** que contiene el blob de conferencia. Si **es NULL,** el blob de conferencia se inicializa con valores predeterminados. Actualmente, los valores de conferencia predeterminados solo están disponibles si el *parámetro CharacterSet* está establecido en BCS \_ ASCII.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Value                                                                                         | Significado                                                                    |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | El método se realizó correctamente.<br/>                                               |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | El *parámetro pName*, *CharacterSet* o *pBlob* no es válido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No existe memoria suficiente para realizar la operación.<br/>            |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Error no especificado.<br/>                                              |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método aún no se ha implementado.<br/>                             |



 

## <a name="remarks"></a>Comentarios

**ITConferenceBlob::Init** devolverá un error si el blob ya se ha inicializado.

La aplicación debe usar [**SysAllocString para**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) asignar memoria para los *parámetros pName* *y pBlob.* La aplicación debe usar [**SysFreeString para**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) liberar la memoria cuando las variables ya no sean necesarias.

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

 

