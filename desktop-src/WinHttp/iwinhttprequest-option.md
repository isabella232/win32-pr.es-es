---
description: Establece o recupera un valor de opción de servicios HTTP de Microsoft Windows (WinHTTP).
ms.assetid: 913573e6-fad3-42a5-bb5d-25a3d2ac9616
title: 'IWinHttpRequest:: Option (propiedad)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.Option
- IWinHttpRequest.get_Option
- IWinHttpRequest.put_Option
- WinHttpRequest.Option
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: c76df3f09871984da9f4bc093e9ac96d7484558f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688531"
---
# <a name="iwinhttprequestoption-property"></a>IWinHttpRequest:: Option (propiedad)

La propiedad **Option** establece o recupera un valor de opción de servicios http de Microsoft Windows (WinHTTP).

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_Option(
  [in]          WinHttpRequestOption Option,
  [in]          VARIANT              Value
);

HRESULT get_Option(
  [in]          WinHttpRequestOption Option,
  [out, retval] VARIANT              *Value
);
```


```JScript

vtOption = WinHttpRequest.Option
WinHttpRequest.Option = vtOption
```





## <a name="property-value"></a>Valor de propiedad

Valor de **tipo Variant** que contiene el valor de la opción.

El parámetro *Option* especifica el [**WinHttpRequestOption**](winhttprequestoption.md) que se va a establecer o recuperar.

## <a name="error-codes"></a>Códigos de error

El valor devuelto es correcto si se ejecuta correctamente o un valor de error en caso contrario. **\_**

## <a name="remarks"></a>Observaciones

> [!Note]  
> En Windows XP y Windows 2000, consulte la sección [requisitos de tiempo de ejecución](winhttp-start-page.md) de la página de inicio de winhttp.

 

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo establecer y ver la opción de cadena de [*agente de usuario*](glossary.md) y ver otras opciones.


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
    VARIANT         varUserAgent;

    CLSID           clsid;

    VariantInit(&varFalse);
    V_VT(&varFalse)   = VT_BOOL;
    V_BOOL(&varFalse) = VARIANT_FALSE;

    VariantInit(&varEmpty);
    V_VT(&varEmpty) = VT_ERROR;

    varUserAgent.vt = VT_BSTR;
    varUserAgent.bstrVal = NULL;

    hr = CLSIDFromProgID(L"WinHttp.WinHttpRequest.5.1", &clsid);

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
        // Specify the user agent.
        varUserAgent.vt = VT_BSTR;
        varUserAgent.bstrVal =
                   SysAllocString(
                           L"A WinHttpRequest Example Program");

        //varUserAgent is L"A WinHttpRequest Example Program");
        hr = pIWinHttpRequest->put_Option(
                                 WinHttpRequestOption_UserAgentString,
                                 varUserAgent);
    }
    if (SUCCEEDED(hr))
    {    // Send Request.
        hr = pIWinHttpRequest->Send(varEmpty);
    }
    if (SUCCEEDED(hr))
    {
        // Get user agent string.
        hr = pIWinHttpRequest->get_Option(
                                 WinHttpRequestOption_UserAgentString,
                                 &varUserAgent);
        // Print response to console.
        wprintf(L"%s\n\n", varUserAgent.bstrVal);

        // Get URL.
        hr = pIWinHttpRequest->get_Option(WinHttpRequestOption_URL,
                                          &varUserAgent);
        // Print response to console.
        wprintf(L"%s\n\n", varUserAgent.bstrVal);

        // Get URL Code Page.
        hr = pIWinHttpRequest->get_Option(
                                     WinHttpRequestOption_URLCodePage,
                                     &varUserAgent);
        // Print response to console.
        wprintf(L"%u\n\n", varUserAgent.lVal);

        // Convert percent symbols to escape sequences.
        hr = pIWinHttpRequest->get_Option(
                              WinHttpRequestOption_EscapePercentInURL,
                              &varUserAgent);
        // Print response to console.
        wprintf(L"%s\n", varUserAgent.boolVal?L"True":L"False");
    }

    // Release memory.
    if (pIWinHttpRequest)
        pIWinHttpRequest->Release();
    if (bstrResponse)
        SysFreeString(bstrResponse);
    if (varUserAgent.bstrVal)
        SysFreeString(varUserAgent.bstrVal);

    CoUninitialize();
    return 0;
}

```



En el siguiente ejemplo de scripting se muestra cómo establecer y ver las opciones.


```JScript
// Define the constants used by the option property.
WinHttpRequestOption_UserAgentString = 0;    // Name of the user agent
WinHttpRequestOption_URL = 1;                // Current URL
WinHttpRequestOption_URLCodePage = 2;        // Code page
WinHttpRequestOption_EscapePercentInURL = 3; // Convert percents 
                                             // in the URL

// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Initialize an HTTP request.  
WinHttpReq.Open("GET", "https://www.microsoft.com", false);

// Send the HTTP request.
WinHttpReq.Send(); 

// Display the WinHTTP option values.
WScript.Echo( 'User agent:      '+
             WinHttpReq.Option(WinHttpRequestOption_UserAgentString));
WScript.Echo( 'URL:             '+
             WinHttpReq.Option(WinHttpRequestOption_URL));
WScript.Echo( 'Code page:       '+
             WinHttpReq.Option(WinHttpRequestOption_URLCodePage));
WScript.Echo( 'Escape percents: '+
          WinHttpReq.Option(WinHttpRequestOption_EscapePercentInURL));
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
</dt> <dt>

[**WinHttpRequestOption**](winhttprequestoption.md)
</dt> </dl>

 

 




