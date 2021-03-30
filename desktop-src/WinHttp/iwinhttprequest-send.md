---
description: El método send envía una solicitud HTTP a un servidor HTTP.
ms.assetid: 4f30d6b7-d1c3-43f1-9829-260b7c84518f
title: 'IWinHttpRequest:: Send (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.Send
- WinHttpRequest.Send
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 0040ed6c09814a2b2112a91173d84430b8130a30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816131"
---
# <a name="iwinhttprequestsend-method"></a><span data-ttu-id="b4347-103">IWinHttpRequest:: Send (método)</span><span class="sxs-lookup"><span data-stu-id="b4347-103">IWinHttpRequest::Send method</span></span>

<span data-ttu-id="b4347-104">El método **send** envía una solicitud HTTP a un servidor http.</span><span class="sxs-lookup"><span data-stu-id="b4347-104">The **Send** method sends an HTTP request to an HTTP server.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4347-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b4347-105">Syntax</span></span>


```C++
HRESULT Send(
  [in, optional] VARIANT Body
);
```



## <a name="parameters"></a><span data-ttu-id="b4347-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b4347-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4347-107">*Cuerpo* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b4347-107">*Body* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b4347-108">Datos que se van a enviar al servidor.</span><span class="sxs-lookup"><span data-stu-id="b4347-108">Data to be sent to the server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4347-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b4347-109">Return value</span></span>

<span data-ttu-id="b4347-110">El valor devuelto es correcto si se ejecuta correctamente o un valor de error en caso contrario. **\_**</span><span class="sxs-lookup"><span data-stu-id="b4347-110">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4347-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b4347-111">Remarks</span></span>

<span data-ttu-id="b4347-112">La solicitud que se va a enviar se definió en una llamada anterior al método [**Open**](iwinhttprequest-open.md) .</span><span class="sxs-lookup"><span data-stu-id="b4347-112">The request to be sent was defined in a prior call to the [**Open**](iwinhttprequest-open.md) method.</span></span> <span data-ttu-id="b4347-113">La aplicación que realiza la llamada puede proporcionar datos que se van a enviar al servidor a través del parámetro *Body* .</span><span class="sxs-lookup"><span data-stu-id="b4347-113">The calling application can provide data to be sent to the server through the *Body* parameter.</span></span> <span data-ttu-id="b4347-114">Si el [*verbo http*](glossary.md) del [**abierto**](iwinhttprequest-open.md) del objeto es "Get", este método envía la solicitud sin *cuerpo*, incluso si la aplicación que realiza la llamada lo proporciona.</span><span class="sxs-lookup"><span data-stu-id="b4347-114">If the [*HTTP verb*](glossary.md) of the object's [**Open**](iwinhttprequest-open.md) is "GET", this method sends the request without *Body*, even if it is provided by the calling application.</span></span>

> [!Note]  
> <span data-ttu-id="b4347-115">En Windows XP y Windows 2000, consulte la sección [requisitos de tiempo de ejecución](winhttp-start-page.md) de la página de inicio de winhttp.</span><span class="sxs-lookup"><span data-stu-id="b4347-115">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHttp start page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="b4347-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="b4347-116">Examples</span></span>

<span data-ttu-id="b4347-117">En el ejemplo siguiente se muestra cómo abrir una conexión HTTP, enviar una solicitud HTTP y leer el texto de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b4347-117">The following example shows how to open an HTTP connection, send an HTTP request, and read the response text.</span></span>


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
    // variable for return value
    HRESULT    hr;

    // initialize COM
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
    {    // Get Response text.
        hr = pIWinHttpRequest->get_ResponseText(&bstrResponse);
    }

    // Print response to console.
    wprintf(L"%.256s",bstrResponse);

    // Release memory.
    if (pIWinHttpRequest)
        pIWinHttpRequest->Release();
    if (bstrResponse)
        SysFreeString(bstrResponse);

    CoUninitialize();
    return 0;
}

```



<span data-ttu-id="b4347-118">En el ejemplo de scripting siguiente se muestra cómo abrir una conexión HTTP, enviar una solicitud HTTP y leer el texto de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b4347-118">The following scripting example shows how to open an HTTP connection, send an HTTP request, and read the response text.</span></span>


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



<span data-ttu-id="b4347-119">En el siguiente ejemplo de scripting se muestra cómo publicar datos en un servidor HTTP.</span><span class="sxs-lookup"><span data-stu-id="b4347-119">The following scripting example shows how to post data to an HTTP server.</span></span>


```JScript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Initialize an HTTP request.  
WinHttpReq.Open("PUT", "https://postserver/newdoc.htm", false);

// Post data to the HTTP server.
WinHttpReq.Send("Post data");
```



## <a name="requirements"></a><span data-ttu-id="b4347-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4347-120">Requirements</span></span>



| <span data-ttu-id="b4347-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4347-121">Requirement</span></span> | <span data-ttu-id="b4347-122">Value</span><span class="sxs-lookup"><span data-stu-id="b4347-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4347-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b4347-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b4347-124">Windows XP, Windows 2000 Professional con las \[ aplicaciones de escritorio de SP3 únicamente\]</span><span class="sxs-lookup"><span data-stu-id="b4347-124">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="b4347-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b4347-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b4347-126">Windows Server 2003, Windows 2000 Server con \[ solo aplicaciones de escritorio de SP3\]</span><span class="sxs-lookup"><span data-stu-id="b4347-126">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="b4347-127">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="b4347-127">Redistributable</span></span><br/>          | <span data-ttu-id="b4347-128">WinHTTP 5,0 e Internet Explorer 5,01 o posterior en Windows XP y Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="b4347-128">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="b4347-129">IDL</span><span class="sxs-lookup"><span data-stu-id="b4347-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b4347-130"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b4347-130"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="b4347-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b4347-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="b4347-132"><dt>Winhttp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b4347-132"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="b4347-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b4347-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4347-134"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4347-134"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="b4347-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="b4347-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4347-136">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="b4347-136">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="b4347-137">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="b4347-137">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="b4347-138">Versiones de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="b4347-138">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




