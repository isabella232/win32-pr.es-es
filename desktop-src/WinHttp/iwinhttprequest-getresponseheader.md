---
description: Recupera los encabezados de respuesta HTTP.
ms.assetid: 3d59ee83-280c-4074-82e1-ded203fa1049
title: 'IWinHttpRequest:: GetResponseHeader (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.GetResponseHeader
- WinHttpRequest.GetResponseHeader
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 6e51b0973c7b078c7de592565db19bf6e029c5a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706983"
---
# <a name="iwinhttprequestgetresponseheader-method"></a><span data-ttu-id="1f04e-103">IWinHttpRequest:: GetResponseHeader (método)</span><span class="sxs-lookup"><span data-stu-id="1f04e-103">IWinHttpRequest::GetResponseHeader method</span></span>

<span data-ttu-id="1f04e-104">El método **GetResponseHeader** recupera los encabezados de respuesta http.</span><span class="sxs-lookup"><span data-stu-id="1f04e-104">The **GetResponseHeader** method retrieves the HTTP response headers.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f04e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1f04e-105">Syntax</span></span>


```C++
HRESULT GetResponseHeader(
  [in]          BSTR Header,
  [out, retval] BSTR *Value
);
```



## <a name="parameters"></a><span data-ttu-id="1f04e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1f04e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f04e-107">*Encabezado* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="1f04e-107">*Header* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f04e-108">Especifica el nombre del encabezado que no distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="1f04e-108">Specifies the case-insensitive header name.</span></span>

</dd> <dt>

<span data-ttu-id="1f04e-109">*Valor* \[ de out, retval\]</span><span class="sxs-lookup"><span data-stu-id="1f04e-109">*Value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="1f04e-110">Recibe la información de encabezado resultante.</span><span class="sxs-lookup"><span data-stu-id="1f04e-110">Receives the resulting header information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f04e-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1f04e-111">Return value</span></span>

<span data-ttu-id="1f04e-112">El valor devuelto es correcto si se ejecuta correctamente o un valor de error en caso contrario. **\_**</span><span class="sxs-lookup"><span data-stu-id="1f04e-112">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f04e-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1f04e-113">Remarks</span></span>

<span data-ttu-id="1f04e-114">Este método devuelve el valor del encabezado de respuesta denominado en el *encabezado*.</span><span class="sxs-lookup"><span data-stu-id="1f04e-114">This method returns the value of the response header named in *Header*.</span></span> <span data-ttu-id="1f04e-115">Tenga en cuenta que los clientes de automatización, como script, obtienen los datos de encabezado como el valor devuelto de la llamada de función, no a través de un parámetro de función.</span><span class="sxs-lookup"><span data-stu-id="1f04e-115">Be aware that automation clients, such as script, get the header data as the return value of the function call, not through a function parameter.</span></span> <span data-ttu-id="1f04e-116">Invoque este método solo después de que se haya llamado al método [**send**](iwinhttprequest-send.md) .</span><span class="sxs-lookup"><span data-stu-id="1f04e-116">Invoke this method only after the [**Send**](iwinhttprequest-send.md) method has been called.</span></span>

> [!Note]  
> <span data-ttu-id="1f04e-117">En Windows XP y Windows 2000, consulte la sección [requisitos de tiempo de ejecución](winhttp-start-page.md) de la página de inicio de winhttp.</span><span class="sxs-lookup"><span data-stu-id="1f04e-117">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="1f04e-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="1f04e-118">Examples</span></span>

<span data-ttu-id="1f04e-119">En el ejemplo siguiente se muestra cómo abrir una conexión HTTP, enviar una solicitud HTTP y obtener el encabezado Date de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1f04e-119">The following example shows how to open an HTTP connection, send an HTTP request, and get the date header from the response.</span></span> <span data-ttu-id="1f04e-120">Este ejemplo debe ejecutarse desde un símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="1f04e-120">This example must be run from a command prompt.</span></span>


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
        BSTR bstrName = SysAllocString(L"Date");
        hr = pIWinHttpRequest->GetResponseHeader(bstrName,
                                             &bstrResponse);
    }
    if (SUCCEEDED(hr))
    {
        // Print response to console.
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



<span data-ttu-id="1f04e-121">En el ejemplo de scripting siguiente se muestra cómo abrir una conexión HTTP, enviar una solicitud HTTP y obtener el encabezado Date de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1f04e-121">The following scripting example shows how to open an HTTP connection, send an HTTP request, and get the date header from the response.</span></span>


```JScript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Initialize an HTTP request.  
WinHttpReq.Open("GET", 
                "https://www.microsoft.com", 
                 false);

// Send the HTTP request.
WinHttpReq.Send(); 

// Display the date header.
WScript.Echo( WinHttpReq.GetResponseHeader("Date"));
```



## <a name="requirements"></a><span data-ttu-id="1f04e-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f04e-122">Requirements</span></span>



| <span data-ttu-id="1f04e-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f04e-123">Requirement</span></span> | <span data-ttu-id="1f04e-124">Value</span><span class="sxs-lookup"><span data-stu-id="1f04e-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f04e-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1f04e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1f04e-126">Windows XP, Windows 2000 Professional con las \[ aplicaciones de escritorio de SP3 únicamente\]</span><span class="sxs-lookup"><span data-stu-id="1f04e-126">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="1f04e-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1f04e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1f04e-128">Windows Server 2003, Windows 2000 Server con \[ solo aplicaciones de escritorio de SP3\]</span><span class="sxs-lookup"><span data-stu-id="1f04e-128">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="1f04e-129">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="1f04e-129">Redistributable</span></span><br/>          | <span data-ttu-id="1f04e-130">WinHTTP 5,0 e Internet Explorer 5,01 o posterior en Windows XP y Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="1f04e-130">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="1f04e-131">IDL</span><span class="sxs-lookup"><span data-stu-id="1f04e-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1f04e-132"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1f04e-132"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="1f04e-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1f04e-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="1f04e-134"><dt>Winhttp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1f04e-134"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="1f04e-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1f04e-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f04e-136"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f04e-136"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="1f04e-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="1f04e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f04e-138">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="1f04e-138">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="1f04e-139">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="1f04e-139">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="1f04e-140">**GetAllResponseHeaders**</span><span class="sxs-lookup"><span data-stu-id="1f04e-140">**GetAllResponseHeaders**</span></span>](iwinhttprequest-getallresponseheaders.md)
</dt> <dt>

[<span data-ttu-id="1f04e-141">Versiones de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="1f04e-141">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




