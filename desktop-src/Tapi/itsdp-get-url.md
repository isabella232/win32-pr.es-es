---
description: El método get \_ Url obtiene la dirección URL.
ms.assetid: 9ea2ddf6-b8c7-4bfa-aab3-ff2d2056837f
title: Método ITSdp::get_Url (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48c024a176c4acadebad7973df01a8448cdbf83ed50b1b404f01baef00e8c8b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873685"
---
# <a name="itsdpget_url-method"></a>ItSdp::get \_ (método)

\[Los controles e interfaces de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método get \_ Url** obtiene la dirección URL.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Url(
  [out] BSTR *ppUrl
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppUrl* \[ out\]
</dt> <dd>

Puntero a una **representación BSTR** de la dirección URL.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | El método se realizó correctamente.<br/>                                    |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | El *parámetro ppUrl* no es un puntero válido.<br/>        |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No existe memoria suficiente para realizar la operación.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Error no especificado.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método aún no se ha implementado.<br/>                  |



 

## <a name="remarks"></a>Comentarios

La aplicación debe usar [**SysFreeString para**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) liberar la memoria asignada para el *parámetro ppUrl.*

Normalmente, una dirección URL se usa para hacer referencia a una página web que contiene recursos adicionales o información general sobre una conferencia.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITSdp**](itsdp.md)
</dt> <dt>

[**ITSdp::put \_ Url**](itsdp-put-url.md)
</dt> </dl>

 

