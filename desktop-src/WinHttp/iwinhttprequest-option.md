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
# <a name="iwinhttprequestoption-property"></a><span data-ttu-id="dfe52-103">IWinHttpRequest:: Option (propiedad)</span><span class="sxs-lookup"><span data-stu-id="dfe52-103">IWinHttpRequest::Option property</span></span>

<span data-ttu-id="dfe52-104">La propiedad **Option** establece o recupera un valor de opción de servicios http de Microsoft Windows (WinHTTP).</span><span class="sxs-lookup"><span data-stu-id="dfe52-104">The **Option** property sets or retrieves a Microsoft Windows HTTP Services (WinHTTP) option value.</span></span>

<span data-ttu-id="dfe52-105">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="dfe52-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfe52-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dfe52-106">Syntax</span></span>


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





## <a name="property-value"></a><span data-ttu-id="dfe52-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="dfe52-107">Property value</span></span>

<span data-ttu-id="dfe52-108">Valor de **tipo Variant** que contiene el valor de la opción.</span><span class="sxs-lookup"><span data-stu-id="dfe52-108">A **Variant** value that contains the option value.</span></span>

<span data-ttu-id="dfe52-109">El parámetro *Option* especifica el [**WinHttpRequestOption**](winhttprequestoption.md) que se va a establecer o recuperar.</span><span class="sxs-lookup"><span data-stu-id="dfe52-109">The *Option* parameter specifies the [**WinHttpRequestOption**](winhttprequestoption.md) to set or retrieve.</span></span>

## <a name="error-codes"></a><span data-ttu-id="dfe52-110">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="dfe52-110">Error codes</span></span>

<span data-ttu-id="dfe52-111">El valor devuelto es correcto si se ejecuta correctamente o un valor de error en caso contrario. **\_**</span><span class="sxs-lookup"><span data-stu-id="dfe52-111">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="dfe52-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dfe52-112">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="dfe52-113">En Windows XP y Windows 2000, consulte la sección [requisitos de tiempo de ejecución](winhttp-start-page.md) de la página de inicio de winhttp.</span><span class="sxs-lookup"><span data-stu-id="dfe52-113">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="dfe52-114">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="dfe52-114">Examples</span></span>

<span data-ttu-id="dfe52-115">En el ejemplo siguiente se muestra cómo establecer y ver la opción de cadena de [*agente de usuario*](glossary.md) y ver otras opciones.</span><span class="sxs-lookup"><span data-stu-id="dfe52-115">The following example shows how to set and view the [*user agent*](glossary.md) string option and view various other options.</span></span>


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



<span data-ttu-id="dfe52-116">En el siguiente ejemplo de scripting se muestra cómo establecer y ver las opciones.</span><span class="sxs-lookup"><span data-stu-id="dfe52-116">The following scripting example shows how to set and view options.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="dfe52-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dfe52-117">Requirements</span></span>



| <span data-ttu-id="dfe52-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="dfe52-118">Requirement</span></span> | <span data-ttu-id="dfe52-119">Value</span><span class="sxs-lookup"><span data-stu-id="dfe52-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfe52-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dfe52-120">Minimum supported client</span></span><br/> | <span data-ttu-id="dfe52-121">Windows XP, Windows 2000 Professional con las \[ aplicaciones de escritorio de SP3 únicamente\]</span><span class="sxs-lookup"><span data-stu-id="dfe52-121">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="dfe52-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dfe52-122">Minimum supported server</span></span><br/> | <span data-ttu-id="dfe52-123">Windows Server 2003, Windows 2000 Server con \[ solo aplicaciones de escritorio de SP3\]</span><span class="sxs-lookup"><span data-stu-id="dfe52-123">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="dfe52-124">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="dfe52-124">Redistributable</span></span><br/>          | <span data-ttu-id="dfe52-125">WinHTTP 5,0 e Internet Explorer 5,01 o posterior en Windows XP y Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="dfe52-125">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="dfe52-126">IDL</span><span class="sxs-lookup"><span data-stu-id="dfe52-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="dfe52-127"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="dfe52-127"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="dfe52-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dfe52-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="dfe52-129"><dt>Winhttp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dfe52-129"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="dfe52-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="dfe52-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dfe52-131"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dfe52-131"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="dfe52-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="dfe52-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfe52-133">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="dfe52-133">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="dfe52-134">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="dfe52-134">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="dfe52-135">Versiones de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="dfe52-135">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> <dt>

[<span data-ttu-id="dfe52-136">**WinHttpRequestOption**</span><span class="sxs-lookup"><span data-stu-id="dfe52-136">**WinHttpRequestOption**</span></span>](winhttprequestoption.md)
</dt> </dl>

 

 




