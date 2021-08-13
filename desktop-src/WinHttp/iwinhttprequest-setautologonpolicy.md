---
description: Establece la directiva de inicio de sesión automático actual.
ms.assetid: bc8e8c9c-574e-4392-b336-2c06947022ee
title: IWinHttpRequest::SetAutoLogonPolicy (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.SetAutoLogonPolicy
- WinHttpRequest.SetAutoLogonPolicy
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: b6375d5c5b6c9b6c8acebcdd05a2ad778bb37e75c067a44100a5c67a92876248
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118562891"
---
# <a name="iwinhttprequestsetautologonpolicy-method"></a>IWinHttpRequest::SetAutoLogonPolicy (método)

El **método SetAutoLogonPolicy** establece la directiva [de inicio de sesión automático actual.](authentication-in-winhttp.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetAutoLogonPolicy(
  [in] WinHttpRequestAutoLogonPolicy AutoLogonPolicy
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*AutoLogonPolicy* \[ En\]
</dt> <dd>

Especifica la directiva de inicio de sesión automático actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es **S \_ OK si se** ejecuta correctamente o un valor de error en caso contrario.

## <a name="remarks"></a>Observaciones

La directiva predeterminada es [**AutoLogonPolicy \_ OnlyIfBypassProxy.**](winhttprequestautologonpolicy.md)

Llame **a SetAutoLogonPolicy para** establecer la directiva de inicio de sesión automático antes de llamar a [**Send**](iwinhttprequest-send.md) para enviar la solicitud.

> [!Note]  
> Para Windows XP y Windows 2000, consulte la sección [Requisitos](winhttp-start-page.md) en tiempo de ejecución de la página de inicio de WinHTTP.

 

## <a name="examples"></a>Ejemplos

En el ejemplo de scripting siguiente se muestra cómo establecer la directiva de inicio de sesión automático para que nunca use la autenticación NTLM o Negotiate automáticamente.


```JScript
// Instantiate a WinHttpRequest object.
var HttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");
    
// Open an HTTP connection.
HttpReq.Open("GET", "https://www.fabrikam.com/", false);
    
// Do not automatically send user credentials.
HttpReq.SetAutoLogonPolicy(2);

// Send the HTTP Request.
HttpReq.Send();
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP, Windows 2000 Professional solo con aplicaciones de escritorio SP3 \[\]<br/>            |
| Servidor mínimo compatible<br/> | Windows Server 2003, Windows 2000 Server solo con aplicaciones de escritorio SP3 \[\]<br/>         |
| Redistribuible<br/>          | WinHTTP 5.0 y Internet Explorer 5.01 o posterior en Windows XP y Windows 2000.<br/> |
| Idl<br/>                      | <dl> <dt>HttpRequest.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winhttp.lib</dt> </dl>     |
| Archivo DLL<br/>                      | <dl> <dt>Winhttp.dll</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IWinHttpRequest**](iwinhttprequest-interface.md)
</dt> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[Autenticación en WinHTTP](authentication-in-winhttp.md)
</dt> <dt>

[Versiones winHTTP](winhttp-versions.md)
</dt> </dl>

 

 




