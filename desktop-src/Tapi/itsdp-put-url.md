---
description: El método put \_ Url establece la dirección URL.
ms.assetid: 538bb1dd-c7ad-446d-9df7-23363b466263
title: Método ITSdp::p ut_Url (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b791d18b97851e6b0b27a4ba26d1dfdbce7dbb7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073489"
---
# <a name="itsdpput_url-method"></a>ItSdp::p ut \_ Url (método)

\[Los controles e interfaces de la conferencia de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

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



 

## <a name="remarks"></a>Observaciones

La aplicación debe usar [**SysAllocString para**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) asignar memoria para el parámetro *pUrl* y usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar la memoria cuando la variable ya no sea necesaria.

Normalmente, una dirección URL se usa para hacer referencia a una página web que contiene recursos adicionales o información general sobre una conferencia.

Esta función puede enviar datos a través de la conexión sin cifrar; por lo tanto, alguien que intercepta en la red puede leer los datos. El riesgo de seguridad de enviar los datos en texto sin formato debe tenerse en cuenta antes de usar este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITSdp**](itsdp.md)
</dt> <dt>

[**ITSdp::get \_ Url**](itsdp-get-url.md)
</dt> </dl>

 

