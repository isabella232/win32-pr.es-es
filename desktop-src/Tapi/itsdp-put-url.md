---
description: El método put \_ Url establece la dirección URL.
ms.assetid: 538bb1dd-c7ad-446d-9df7-23363b466263
title: Método ITSdp::p ut_Url (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f6023b9c1210dbd92159486e037e53c8270e53d128db19906fe39c6ec9f6358
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660235"
---
# <a name="itsdpput_url-method"></a>ItSdp::p ut \_ Url (Método)

\[Las interfaces y los controles de conferencia de telefonía IP de Rendezvous no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método put \_ Url** establece la dirección URL.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_Url(
  [in] BSTR pUrl
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pUrl* \[ En\]
</dt> <dd>

Puntero a una **representación BSTR** de la dirección URL.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | El método se realizó correctamente.<br/>                                    |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | El *parámetro pUrl* no es un puntero válido.<br/>         |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No existe memoria suficiente para realizar la operación.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Error no especificado.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método aún no se ha implementado.<br/>                  |



 

## <a name="remarks"></a>Comentarios

La aplicación debe usar [**SysAllocString para**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) asignar memoria para el parámetro *pUrl* y usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar la memoria cuando la variable ya no sea necesaria.

Normalmente, una dirección URL se usa para hacer referencia a una página web que contiene recursos adicionales o información general sobre una conferencia.

Esta función puede enviar datos a través de la conexión en formato sin cifrar; por lo tanto, es posible que alguien interceptado en la red pueda leer los datos. El riesgo de seguridad de enviar los datos en texto no texto debe tenerse en cuenta antes de usar este método.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITSdp**](itsdp.md)
</dt> <dt>

[**ITSdp::get \_ Url**](itsdp-get-url.md)
</dt> </dl>

 

