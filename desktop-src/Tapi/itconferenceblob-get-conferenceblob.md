---
description: El \_ método get ConferenceBlob obtiene un puntero al BLOB de la Conferencia textual actualmente almacenado en el objeto de BLOB de la Conferencia.
ms.assetid: eb378f84-11bc-4f6e-9133-bc303e07eb53
title: 'Método ITConferenceBlob:: get_ConferenceBlob (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e5642f60f7abc1cb10734de1897d35bd5222dd2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680207"
---
# <a name="itconferenceblobget_conferenceblob-method"></a>ITConferenceBlob:: get \_ ConferenceBlob (método)

\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

El método **Get \_ ConferenceBlob** obtiene un puntero al BLOB de la Conferencia textual actualmente almacenado en el objeto de BLOB de la Conferencia.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_ConferenceBlob(
  [out] BSTR *ppBlob
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppBlob* \[ enuncia\]
</dt> <dd>

Puntero a un **BSTR** que contiene el BLOB de la Conferencia.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | El método se realizó correctamente.<br/>                                    |
| <dl> <dt>**\_puntero E**</dt> </dl>     | El parámetro *ppBlob* no es un puntero válido.<br/>       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No hay memoria suficiente para realizar la operación.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Error no especificado.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método aún no se ha implementado.<br/>                  |



 

## <a name="remarks"></a>Observaciones

La aplicación debe usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar la memoria asignada para el parámetro *ppBlob* .

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

 

