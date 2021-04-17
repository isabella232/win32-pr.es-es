---
description: Establece la Directiva de inicio de sesión automático actual.
ms.assetid: bc8e8c9c-574e-4392-b336-2c06947022ee
title: 'IWinHttpRequest:: SetAutoLogonPolicy (método)'
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
ms.openlocfilehash: cad8bd0080d10a1395a0a9d275951ff961a60bf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716643"
---
# <a name="iwinhttprequestsetautologonpolicy-method"></a>IWinHttpRequest:: SetAutoLogonPolicy (método)

El método **SetAutoLogonPolicy** establece la [Directiva de inicio de sesión automático](authentication-in-winhttp.md)actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetAutoLogonPolicy(
  [in] WinHttpRequestAutoLogonPolicy AutoLogonPolicy
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*AutoLogonPolicy* \[ de\]
</dt> <dd>

Especifica la Directiva de inicio de sesión automático actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es correcto si se ejecuta correctamente o un valor de error en caso contrario. **\_**

## <a name="remarks"></a>Observaciones

La directiva predeterminada es [**AutoLogonPolicy \_ OnlyIfBypassProxy**](winhttprequestautologonpolicy.md).

Llame a **SetAutoLogonPolicy** para establecer la Directiva de inicio de sesión automático antes de llamar a [**send**](iwinhttprequest-send.md) para enviar la solicitud.

> [!Note]  
> En Windows XP y Windows 2000, consulte la sección [requisitos de tiempo de ejecución](winhttp-start-page.md) de la página de inicio de winhttp.

 

## <a name="examples"></a>Ejemplos

En el ejemplo de scripting siguiente se muestra cómo establecer la Directiva de inicio de sesión automático para que nunca use NTLM o negociar la autenticación automáticamente.


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
| Cliente mínimo compatible<br/> | Windows XP, Windows 2000 Professional con las \[ aplicaciones de escritorio de SP3 únicamente\]<br/>            |
| Servidor mínimo compatible<br/> | Windows Server 2003, Windows 2000 Server con \[ solo aplicaciones de escritorio de SP3\]<br/>         |
| Redistribuible<br/>          | WinHTTP 5,0 e Internet Explorer 5,01 o posterior en Windows XP y Windows 2000.<br/> |
| IDL<br/>                      | <dl> <dt>HttpRequest. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winhttp. lib</dt> </dl>     |
| Archivo DLL<br/>                      | <dl> <dt>Winhttp.dll</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IWinHttpRequest**](iwinhttprequest-interface.md)
</dt> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[Autenticación en WinHTTP](authentication-in-winhttp.md)
</dt> <dt>

[Versiones de WinHTTP](winhttp-versions.md)
</dt> </dl>

 

 




