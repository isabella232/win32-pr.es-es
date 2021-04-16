---
description: El \_ método get MediaTitle recupera un título textual para los medios que la aplicación puede usar para fines informativos o de presentación. Debe ser una cadena que se pueda convertir en ASCII si el juego de caracteres es ASCII. De lo contrario, puede ser cualquier cadena BSTR.
ms.assetid: c5567672-54f0-45d6-81d2-5a501a33c25f
title: 'Método ITMedia:: get_MediaTitle (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59f2ec4bf16fc27c23277113ee13c8fe02f89c6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680174"
---
# <a name="itmediaget_mediatitle-method"></a>ITMedia:: get \_ MediaTitle (método)

\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

El método **Get \_ MediaTitle** recupera un título textual para los medios que la aplicación puede usar para fines informativos o de presentación. Debe ser una cadena que se pueda convertir en ASCII si el juego de caracteres es ASCII. De lo contrario, puede ser cualquier cadena **BSTR** .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_MediaTitle(
  [out] BSTR *ppMediaTitle
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppMediaTitle* \[ enuncia\]
</dt> <dd>

Puntero a un **BSTR** que contiene el título del medio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | El método se realizó correctamente.<br/>                                    |
| <dl> <dt>**\_puntero E**</dt> </dl>     | El parámetro *ppMediaTitle* no es un puntero válido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No hay memoria suficiente para realizar la operación.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Error no especificado.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método aún no se ha implementado.<br/>                  |



 

## <a name="remarks"></a>Observaciones

La aplicación debe usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar la memoria asignada para el parámetro *ppMediaTitle* .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITMedia**](itmedia.md)
</dt> <dt>

[**ITMedia::P UT \_ MediaTitle**](itmedia-put-mediatitle.md)
</dt> </dl>

 

