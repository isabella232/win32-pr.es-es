---
description: Abre una conexión HTTP a un recurso HTTP.
ms.assetid: 5207e873-44c0-4eeb-9db8-d8b69432070c
title: 'IWinHttpRequest:: Open (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.Open
- WinHttpRequest.Open
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 5543832eb1ebc3df210237eff71d415de14b2f62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697342"
---
# <a name="iwinhttprequestopen-method"></a>IWinHttpRequest:: Open (método)

El método **Open** abre una conexión http a un recurso http.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Open(
  [in]           BSTR    Method,
  [in]           BSTR    Url,
  [in, optional] VARIANT Async
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Método* \[ de\]
</dt> <dd>

Especifica el [*verbo http*](glossary.md) utilizado para el método **abierto** , como "Get" o "put". Use siempre mayúsculas como algunos servidores para omitir los *verbos http* en minúsculas.

</dd> <dt>

*Dirección URL* \[ de\]
</dt> <dd>

Especifica el nombre del recurso. Debe ser una dirección URL absoluta.

</dd> <dt>

*Async* \[ en, opcional\]
</dt> <dd>

Indica si se va a abrir en modo asincrónico.



| Value                                                                                                                                                         | Significado                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="VARIANT_FALSE"></span><span id="variant_false"></span><dl> <dt>**VARIANTE \_ false**</dt> </dl> | Abre la conexión HTTP en modo sincrónico. Una llamada a [**send**](iwinhttprequest-send.md) no vuelve hasta que [WinHTTP](about-winhttp.md) ha recibido por completo la respuesta.<br/> |
| <span id="VARIANT_TRUE"></span><span id="variant_true"></span><dl> <dt>**VARIANTE \_ true**</dt> </dl>    | Abre la conexión HTTP en modo asincrónico.<br/>                                                                                                                                        |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es correcto si se ejecuta correctamente o un valor de error en caso contrario. **\_**

## <a name="remarks"></a>Observaciones

Este método abre una conexión al recurso identificado en la *dirección URL* mediante el [*verbo http*](glossary.md) proporcionado en el *método*.

> [!Note]  
> En Windows XP y Windows 2000, consulte la sección [requisitos de tiempo de ejecución](winhttp-start-page.md) de la página de inicio de winhttp.

 

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo abrir una conexión HTTP, enviar una solicitud HTTP y leer el texto de la respuesta.


```C++
#include <windows.h>
#include <stdio.h>
#include <objbase.h>

#include "httprequest.h"

#pragma comment(lib, "ole32.lib")
#pragma comment(lib, "oleaut32.lib")

// IID for IWinHttpRequest.
const IID IID_IWinHttpRequest =
{
  0x06f29373,
  0x5c5a,
  0x4b54,
  {0xb0, 0x25, 0x6e, 0xf1, 0xbf, 0x8a, 0xbf, 0x0e}
};

int main()
{
    // Variable for return value
    HRESULT    hr;

    // Initialize COM
    hr = CoInitialize( NULL );

    IWinHttpRequest *  pIWinHttpRequest = NULL;

    BSTR            bstrResponse = NULL;
    VARIANT         varFalse;
    VARIANT         varEmpty;

    CLSID           clsid;

    VariantInit(&varFalse);
    V_VT(&varFalse)   = VT_BOOL;
    V_BOOL(&varFalse) = VARIANT_FALSE;

    VariantInit(&varEmpty);
    V_VT(&varEmpty) = VT_ERROR;

    hr = CLSIDFromProgID(L"WinHttp.WinHttpRequest.5.1",
                           &clsid);

    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(clsid,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_IWinHttpRequest,
                              (void **)&pIWinHttpRequest);
    }
    if (SUCCEEDED(hr))
    {
        // Open WinHttpRequest.
        BSTR bstrMethod  = SysAllocString(L"GET");
        BSTR bstrUrl = SysAllocString(L"https://microsoft.com");
        hr = pIWinHttpRequest->Open(bstrMethod,
                                    bstrUrl,
                                    varFalse);
        SysFreeString(bstrMethod);
        SysFreeString(bstrUrl);
    }
    if (SUCCEEDED(hr))
    {
        // Send Request.
        hr = pIWinHttpRequest->Send(varEmpty);
    }
    if (SUCCEEDED(hr))
    {
        // Get Response text.
        hr = pIWinHttpRequest->get_ResponseText(&bstrResponse);
    }
    if (SUCCEEDED(hr))
    {
        // Print the response to a console.
        wprintf(L"%.256s",bstrResponse);
    }

    // Release memory.
    if (pIWinHttpRequest)
        pIWinHttpRequest->Release();
    if (bstrResponse)
        SysFreeString(bstrResponse);

    CoUninitialize();
    return 0;
}

```



En el ejemplo de scripting siguiente se muestra cómo abrir una conexión HTTP, enviar una solicitud HTTP y leer el texto de la respuesta.


```JScript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Initialize an HTTP request.  
WinHttpReq.Open("GET", "https://www.microsoft.com", false);

// Send the HTTP request.
WinHttpReq.Send(); 

// Display the response text.
WScript.Echo( WinHttpReq.ResponseText);
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

[Versiones de WinHTTP](winhttp-versions.md)
</dt> </dl>

 

 




