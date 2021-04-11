---
description: Recupera el texto de Estado HTTP.
ms.assetid: 480babbd-432c-4722-98df-a73ba5928e1f
title: 'IWinHttpRequest:: StatusText (propiedad)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.StatusText
- IWinHttpRequest.get_StatusText
- WinHttpRequest.StatusText
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 41288d87b8194caf3a2a14cc89cd5acbffec902c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083465"
---
# <a name="iwinhttprequeststatustext-property"></a>IWinHttpRequest:: StatusText (propiedad)

La propiedad **statusText** recupera el texto de estado http.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_StatusText(
  [out, retval] BSTR *Status
);
```


```JScript

StatusText = WinHttpRequest.StatusText
```





## <a name="property-value"></a>Valor de propiedad

**BSTR** que recibe el texto de estado http.

## <a name="error-codes"></a>Códigos de error

El valor devuelto es correcto si se ejecuta correctamente o un valor de error en caso contrario. **\_**

## <a name="remarks"></a>Observaciones

Recupera la parte de texto de la línea de respuesta del servidor, haciendo que esté disponible el "descriptivo" equivalente al código de Estado HTTP numérico. Los resultados de esta propiedad solo son válidos después de que el método [**send**](iwinhttprequest-send.md) se haya completado correctamente.

> [!Note]  
> En Windows XP y Windows 2000, consulte la sección [requisitos de tiempo de ejecución](winhttp-start-page.md) de la página de inicio de winhttp.

 

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo abrir una conexión HTTP, enviar una solicitud HTTP, mostrar el [**Estado**](iwinhttprequest-status.md) y **statusText** y leer el texto de la respuesta. Este ejemplo debe ejecutarse desde un símbolo del sistema.


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

    // Initialize COM.
    hr = CoInitialize( NULL );

    IWinHttpRequest *  pIWinHttpRequest = NULL;

    BSTR            bstrResponse = NULL;
    VARIANT         varFalse;
    VARIANT         varEmpty;
    LONG            lStatus = 0;
    BSTR            bstrStatusText = NULL;

    CLSID           clsid;

    VariantInit(&varFalse);
    V_VT(&varFalse)   = VT_BOOL;
    V_BOOL(&varFalse) = VARIANT_FALSE;

    VariantInit(&varEmpty);
    V_VT(&varEmpty) = VT_ERROR;

    hr = CLSIDFromProgID(L"WinHttp.WinHttpRequest.5.1", &clsid);

    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(clsid, NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_IWinHttpRequest,
                              (void **)&pIWinHttpRequest);
    }
    if (SUCCEEDED(hr))
    {    // Open WinHttpRequest.
        BSTR bstrMethod  = SysAllocString(L"GET");
        BSTR bstrUrl = SysAllocString(L"https://microsoft.com");
        hr = pIWinHttpRequest->Open(bstrMethod, bstrUrl, varFalse);
        SysFreeString(bstrMethod);
        SysFreeString(bstrUrl);
    }
    if (SUCCEEDED(hr))
    {    // Send Request.
        hr = pIWinHttpRequest->Send(varEmpty);
    }
    if (SUCCEEDED(hr))
    {    // Send Request.
        hr = pIWinHttpRequest->get_Status(&lStatus);
        hr = pIWinHttpRequest->get_StatusText(&bstrStatusText);
    }
    if (SUCCEEDED(hr))
    {    // Get Response text.
        hr = pIWinHttpRequest->GetAllResponseHeaders(&bstrResponse);
    }
    if (SUCCEEDED(hr))
    {    // Print response to console.
        wprintf(L"%s\n\n", bstrResponse);
        wprintf(L"%u - %s\n\n", lStatus, bstrStatusText);
    }

    // Release memory.
    if (pIWinHttpRequest)
        pIWinHttpRequest->Release();
    if (bstrStatusText)
        SysFreeString(bstrStatusText);
    if (bstrResponse)
        SysFreeString(bstrResponse);

    CoUninitialize();
    return 0;
}

```



En el ejemplo de scripting siguiente se muestra cómo abrir una conexión HTTP, enviar una solicitud HTTP, mostrar el [**Estado**](iwinhttprequest-status.md) y **statusText** y leer los encabezados de respuesta.


```JScript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Initialize an HTTP request.  
WinHttpReq.Open("GET", "https://www.microsoft.com", false);

// Send the HTTP request.
WinHttpReq.Send(); 

// Display the status.
WScript.Echo( WinHttpReq.Status + " - " + WinHttpReq.StatusText);

// Display the date header.
WScript.Echo( WinHttpReq.GetAllResponseHeaders());
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

[**Status**](iwinhttprequest-status.md)
</dt> <dt>

[Versiones de WinHTTP](winhttp-versions.md)
</dt> </dl>

 

 




