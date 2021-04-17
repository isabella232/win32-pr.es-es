---
description: Recupera todos los encabezados de respuesta HTTP.
ms.assetid: 68b13d4c-5afd-486d-8b78-a7eef0f59a24
title: 'IWinHttpRequest:: GetAllResponseHeaders (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.GetAllResponseHeaders
- WinHttpRequest.GetAllResponseHeaders
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 74c113216cf41e2f9816176dd28ba5e84208c635
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652975"
---
# <a name="iwinhttprequestgetallresponseheaders-method"></a><span data-ttu-id="027d9-103">IWinHttpRequest:: GetAllResponseHeaders (método)</span><span class="sxs-lookup"><span data-stu-id="027d9-103">IWinHttpRequest::GetAllResponseHeaders method</span></span>

<span data-ttu-id="027d9-104">El método **GetAllResponseHeaders** recupera todos los encabezados de respuesta http.</span><span class="sxs-lookup"><span data-stu-id="027d9-104">The **GetAllResponseHeaders** method retrieves all HTTP response headers.</span></span>

## <a name="syntax"></a><span data-ttu-id="027d9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="027d9-105">Syntax</span></span>


```C++
HRESULT GetAllResponseHeaders(
  [out, retval] BSTR *Headers
);
```



## <a name="parameters"></a><span data-ttu-id="027d9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="027d9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="027d9-107">*Encabezados de* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="027d9-107">*Headers* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="027d9-108">Recibe la información de encabezado resultante.</span><span class="sxs-lookup"><span data-stu-id="027d9-108">Receives the resulting header information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="027d9-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="027d9-109">Return value</span></span>

<span data-ttu-id="027d9-110">El valor devuelto es correcto si se ejecuta correctamente o un valor de error en caso contrario. **\_**</span><span class="sxs-lookup"><span data-stu-id="027d9-110">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="027d9-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="027d9-111">Remarks</span></span>

<span data-ttu-id="027d9-112">Este método devuelve todos los encabezados contenidos en la respuesta del servidor más reciente.</span><span class="sxs-lookup"><span data-stu-id="027d9-112">This method returns all of the headers contained in the most recent server response.</span></span> <span data-ttu-id="027d9-113">Los encabezados individuales se delimitan mediante una combinación de retorno de carro y avance de línea (ASCII 13 y 10).</span><span class="sxs-lookup"><span data-stu-id="027d9-113">The individual headers are delimited by a carriage return and line feed combination (ASCII 13 and 10).</span></span> <span data-ttu-id="027d9-114">La última entrada va seguida de dos delimitadores (13, 10, 13, 10).</span><span class="sxs-lookup"><span data-stu-id="027d9-114">The last entry is followed by two delimiters (13, 10, 13, 10).</span></span> <span data-ttu-id="027d9-115">Invoque este método solo después de que se haya llamado al método [**send**](iwinhttprequest-send.md) .</span><span class="sxs-lookup"><span data-stu-id="027d9-115">Invoke this method only after the [**Send**](iwinhttprequest-send.md) method has been called.</span></span>

> [!Note]  
> <span data-ttu-id="027d9-116">En Windows XP y Windows 2000, consulte la sección [requisitos de tiempo de ejecución](winhttp-start-page.md) de la página de inicio de winhttp.</span><span class="sxs-lookup"><span data-stu-id="027d9-116">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="027d9-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="027d9-117">Examples</span></span>

<span data-ttu-id="027d9-118">En el ejemplo siguiente se muestra cómo abrir una conexión HTTP, enviar una solicitud HTTP y obtener todos los encabezados de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="027d9-118">The following example shows how to open an HTTP connection, send an HTTP request, and get all of the headers from the response.</span></span> <span data-ttu-id="027d9-119">Este ejemplo debe ejecutarse desde un símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="027d9-119">This example should be run from a command prompt.</span></span>


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

int main(int argc, char* argv[])
{
    UNREFERENCED_PARAMETER(argc);
    UNREFERENCED_PARAMETER(argv);

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
        hr = pIWinHttpRequest->GetAllResponseHeaders(&bstrResponse);
    }
    if (SUCCEEDED(hr))
    {    // Print the response to a console.
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



<span data-ttu-id="027d9-120">En el siguiente ejemplo de scripting se muestra cómo abrir una conexión HTTP, enviar una solicitud HTTP y obtener todos los encabezados de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="027d9-120">The following scripting example shows how to open an HTTP connection, send an HTTP request, and get all of the headers from the response.</span></span>


```JScript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Initialize an HTTP request.  
WinHttpReq.Open("GET", "https://www.microsoft.com", false);

// Send the HTTP request.
WinHttpReq.Send(); 

// Get all response headers.
WScript.Echo( WinHttpReq.GetAllResponseHeaders());
```



## <a name="requirements"></a><span data-ttu-id="027d9-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="027d9-121">Requirements</span></span>



| <span data-ttu-id="027d9-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="027d9-122">Requirement</span></span> | <span data-ttu-id="027d9-123">Value</span><span class="sxs-lookup"><span data-stu-id="027d9-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="027d9-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="027d9-124">Minimum supported client</span></span><br/> | <span data-ttu-id="027d9-125">Windows XP, Windows 2000 Professional con las \[ aplicaciones de escritorio de SP3 únicamente\]</span><span class="sxs-lookup"><span data-stu-id="027d9-125">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="027d9-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="027d9-126">Minimum supported server</span></span><br/> | <span data-ttu-id="027d9-127">Windows Server 2003, Windows 2000 Server con \[ solo aplicaciones de escritorio de SP3\]</span><span class="sxs-lookup"><span data-stu-id="027d9-127">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="027d9-128">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="027d9-128">Redistributable</span></span><br/>          | <span data-ttu-id="027d9-129">WinHTTP 5,0 e Internet Explorer 5,01 o posterior en Windows XP y Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="027d9-129">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="027d9-130">IDL</span><span class="sxs-lookup"><span data-stu-id="027d9-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="027d9-131"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="027d9-131"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="027d9-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="027d9-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="027d9-133"><dt>Winhttp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="027d9-133"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="027d9-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="027d9-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="027d9-135"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="027d9-135"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="027d9-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="027d9-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="027d9-137">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="027d9-137">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="027d9-138">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="027d9-138">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="027d9-139">**GetResponseHeader**</span><span class="sxs-lookup"><span data-stu-id="027d9-139">**GetResponseHeader**</span></span>](iwinhttprequest-getresponseheader.md)
</dt> <dt>

[<span data-ttu-id="027d9-140">Versiones de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="027d9-140">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




