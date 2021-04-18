---
description: Recupera el cuerpo de la entidad de respuesta como texto.
ms.assetid: 87caf64f-be11-45c9-af1e-997a55c5e76e
title: 'IWinHttpRequest:: ResponseText (propiedad)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.ResponseText
- IWinHttpRequest.get_ResponseText
- WinHttpRequest.ResponseText
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 93e0a9b17ba356f9ce6b038be114f5f2c9804eab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716644"
---
# <a name="iwinhttprequestresponsetext-property"></a><span data-ttu-id="4c58b-103">IWinHttpRequest:: ResponseText (propiedad)</span><span class="sxs-lookup"><span data-stu-id="4c58b-103">IWinHttpRequest::ResponseText property</span></span>

<span data-ttu-id="4c58b-104">La propiedad **responseText** recupera el cuerpo de la entidad de respuesta como texto.</span><span class="sxs-lookup"><span data-stu-id="4c58b-104">The **ResponseText** property retrieves the response entity body as text.</span></span>

<span data-ttu-id="4c58b-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="4c58b-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c58b-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4c58b-106">Syntax</span></span>


```C++
HRESULT get_ResponseText(
  [out, retval] BSTR *Body
);
```


```JScript

strResponseText = WinHttpRequest.ResponseText
```





## <a name="property-value"></a><span data-ttu-id="4c58b-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="4c58b-107">Property value</span></span>

<span data-ttu-id="4c58b-108">**BSTR** que recibe el cuerpo de la entidad de la respuesta como texto.</span><span class="sxs-lookup"><span data-stu-id="4c58b-108">**BSTR** that receives the entity body of the response as text.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4c58b-109">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="4c58b-109">Error codes</span></span>

<span data-ttu-id="4c58b-110">El valor devuelto es correcto si se ejecuta correctamente o un valor de error en caso contrario. **\_**</span><span class="sxs-lookup"><span data-stu-id="4c58b-110">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c58b-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4c58b-111">Remarks</span></span>

<span data-ttu-id="4c58b-112">Esta propiedad solo se puede invocar después de que se haya llamado al método [**send**](iwinhttprequest-send.md) .</span><span class="sxs-lookup"><span data-stu-id="4c58b-112">This property can only be invoked after the [**Send**](iwinhttprequest-send.md) method has been called.</span></span>

<span data-ttu-id="4c58b-113">Al utilizar esta propiedad en modo sincrónico, el límite para el número de caracteres que devuelve es aproximadamente 2.169.895.</span><span class="sxs-lookup"><span data-stu-id="4c58b-113">When using this property in synchronous mode, the limit to the number of characters it returns is approximately 2,169,895.</span></span>

> [!Note]  
> <span data-ttu-id="4c58b-114">En Windows XP y Windows 2000, consulte la sección [requisitos de tiempo de ejecución](winhttp-start-page.md) de la página de inicio de winhttp.</span><span class="sxs-lookup"><span data-stu-id="4c58b-114">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="4c58b-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="4c58b-115">Examples</span></span>

<span data-ttu-id="4c58b-116">En el ejemplo siguiente se muestra cómo abrir una conexión HTTP, enviar una solicitud HTTP y leer el texto de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4c58b-116">The following example shows how to open an HTTP connection, send an HTTP request, and read the response text.</span></span> <span data-ttu-id="4c58b-117">Este ejemplo debe ejecutarse desde un símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="4c58b-117">This example must be run from a command prompt.</span></span>


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
    {   // Open WinHttpRequest.
        BSTR bstrMethod  = SysAllocString(L"GET");
        BSTR bstrUrl = SysAllocString(L"https://microsoft.com");
        hr = pIWinHttpRequest->Open(bstrMethod, bstrUrl, varFalse);
        SysFreeString(bstrMethod);
        SysFreeString(bstrUrl);
    }
    if (SUCCEEDED(hr))
    {   // Send Request.
        hr = pIWinHttpRequest->Send(varEmpty);
    }
    if (SUCCEEDED(hr))
    {   // Get Response text.
        hr = pIWinHttpRequest->get_ResponseText(&bstrResponse);
    }

    // Print the response to a console.
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



<span data-ttu-id="4c58b-118">En el ejemplo de scripting siguiente se muestra cómo abrir una conexión HTTP, enviar una solicitud HTTP y leer el texto de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4c58b-118">The following scripting example shows how to open an HTTP connection, send an HTTP request, and read the response text.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="4c58b-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c58b-119">Requirements</span></span>



| <span data-ttu-id="4c58b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c58b-120">Requirement</span></span> | <span data-ttu-id="4c58b-121">Value</span><span class="sxs-lookup"><span data-stu-id="4c58b-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c58b-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4c58b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4c58b-123">Windows XP, Windows 2000 Professional con las \[ aplicaciones de escritorio de SP3 únicamente\]</span><span class="sxs-lookup"><span data-stu-id="4c58b-123">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="4c58b-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4c58b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4c58b-125">Windows Server 2003, Windows 2000 Server con \[ solo aplicaciones de escritorio de SP3\]</span><span class="sxs-lookup"><span data-stu-id="4c58b-125">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="4c58b-126">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="4c58b-126">Redistributable</span></span><br/>          | <span data-ttu-id="4c58b-127">WinHTTP 5,0 e Internet Explorer 5,01 o posterior en Windows XP y Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="4c58b-127">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="4c58b-128">IDL</span><span class="sxs-lookup"><span data-stu-id="4c58b-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4c58b-129"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4c58b-129"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="4c58b-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4c58b-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="4c58b-131"><dt>Winhttp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4c58b-131"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="4c58b-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4c58b-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4c58b-133"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c58b-133"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="4c58b-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="4c58b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c58b-135">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="4c58b-135">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="4c58b-136">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="4c58b-136">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="4c58b-137">**ResponseBody**</span><span class="sxs-lookup"><span data-stu-id="4c58b-137">**ResponseBody**</span></span>](iwinhttprequest-responsebody.md)
</dt> <dt>

[<span data-ttu-id="4c58b-138">**ResponseStream**</span><span class="sxs-lookup"><span data-stu-id="4c58b-138">**ResponseStream**</span></span>](iwinhttprequest-responsestream.md)
</dt> <dt>

[<span data-ttu-id="4c58b-139">Versiones de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="4c58b-139">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




