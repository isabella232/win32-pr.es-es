---
description: El método WaitForResponse espera a que se complete un método de envío asincrónico, con un valor de tiempo de espera opcional, en segundos.
ms.assetid: 33265710-ecdc-4eae-8822-161dffbd03fc
title: 'IWinHttpRequest:: WaitForResponse (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.WaitForResponse
- WinHttpRequest.WaitForResponse
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: fe9e3508273a3ee52d72ede65fd6575d72decb8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678294"
---
# <a name="iwinhttprequestwaitforresponse-method"></a><span data-ttu-id="62042-103">IWinHttpRequest:: WaitForResponse (método)</span><span class="sxs-lookup"><span data-stu-id="62042-103">IWinHttpRequest::WaitForResponse method</span></span>

<span data-ttu-id="62042-104">El método **WaitForResponse** espera a que se complete un método de [**envío**](iwinhttprequest-send.md) asincrónico, con un valor de tiempo de espera opcional, en segundos.</span><span class="sxs-lookup"><span data-stu-id="62042-104">The **WaitForResponse** method waits for an asynchronous [**Send**](iwinhttprequest-send.md) method to complete, with optional time-out value, in seconds.</span></span>

## <a name="syntax"></a><span data-ttu-id="62042-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="62042-105">Syntax</span></span>


```C++
HRESULT WaitForResponse(
  [in, optional] VARIANT      Timeout,
  [out, retval]  VARIANT_BOOL *Succeeded
);
```



## <a name="parameters"></a><span data-ttu-id="62042-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="62042-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62042-107">*Tiempo de espera* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="62042-107">*Timeout* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="62042-108">Valor de tiempo de espera, en segundos.</span><span class="sxs-lookup"><span data-stu-id="62042-108">Time-out value, in seconds.</span></span> <span data-ttu-id="62042-109">El tiempo de espera predeterminado es infinito.</span><span class="sxs-lookup"><span data-stu-id="62042-109">Default time-out is infinite.</span></span> <span data-ttu-id="62042-110">Para establecer explícitamente el tiempo de espera en infinito, use el valor-1.</span><span class="sxs-lookup"><span data-stu-id="62042-110">To explicitly set time-out to infinite, use the value -1.</span></span>

</dd> <dt>

<span data-ttu-id="62042-111">*Correcto* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="62042-111">*Succeeded* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="62042-112">Recibe uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="62042-112">Receives one of the following values.</span></span>



| <span data-ttu-id="62042-113">Value</span><span class="sxs-lookup"><span data-stu-id="62042-113">Value</span></span>                                                                                                                                                         | <span data-ttu-id="62042-114">Significado</span><span class="sxs-lookup"><span data-stu-id="62042-114">Meaning</span></span>                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="VARIANT_TRUE"></span><span id="variant_true"></span><dl> <span data-ttu-id="62042-115"><dt>**VARIANTE \_ true**</dt></span><span class="sxs-lookup"><span data-stu-id="62042-115"><dt>**VARIANT\_TRUE**</dt></span></span> </dl>    | <span data-ttu-id="62042-116">Se recibió una respuesta.</span><span class="sxs-lookup"><span data-stu-id="62042-116">A response has been received.</span></span><br/>               |
| <span id="VARIANT_FALSE"></span><span id="variant_false"></span><dl> <span data-ttu-id="62042-117"><dt>**VARIANTE \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="62042-117"><dt>**VARIANT\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="62042-118">Se superó el período de tiempo de espera especificado.</span><span class="sxs-lookup"><span data-stu-id="62042-118">The specified time-out period was exceeded.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62042-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="62042-119">Return value</span></span>

<span data-ttu-id="62042-120">El valor devuelto es correcto si se ejecuta correctamente o un valor de error en caso contrario. **\_**</span><span class="sxs-lookup"><span data-stu-id="62042-120">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="62042-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="62042-121">Remarks</span></span>

<span data-ttu-id="62042-122">Este método suspende la ejecución mientras se espera una respuesta a una solicitud asincrónica.</span><span class="sxs-lookup"><span data-stu-id="62042-122">This method suspends execution while waiting for a response to an asynchronous request.</span></span> <span data-ttu-id="62042-123">Se debe llamar a este método después de un [**envío**](iwinhttprequest-send.md).</span><span class="sxs-lookup"><span data-stu-id="62042-123">This method should be called after a [**Send**](iwinhttprequest-send.md).</span></span> <span data-ttu-id="62042-124">Las aplicaciones que llaman pueden especificar un valor de *tiempo de espera* opcional, en segundos.</span><span class="sxs-lookup"><span data-stu-id="62042-124">Calling applications can specify an optional *Timeout* value, in seconds.</span></span> <span data-ttu-id="62042-125">Si se agota el tiempo de espera de este método, la solicitud no se anula.</span><span class="sxs-lookup"><span data-stu-id="62042-125">If this method times out, the request is not aborted.</span></span> <span data-ttu-id="62042-126">De esta manera, la aplicación que realiza la llamada puede continuar esperando la solicitud, si lo desea, en una llamada subsiguiente a este método.</span><span class="sxs-lookup"><span data-stu-id="62042-126">This way, the calling application can continue to wait for the request, if desired, in a subsequent call to this method.</span></span>

<span data-ttu-id="62042-127">La llamada a esta propiedad después de un método de [**envío**](iwinhttprequest-send.md) sincrónico vuelve inmediatamente y no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="62042-127">Calling this property after a synchronous [**Send**](iwinhttprequest-send.md) method returns immediately and has no effect.</span></span>

> [!Note]  
> <span data-ttu-id="62042-128">En Windows XP y Windows 2000, consulte la sección [requisitos de tiempo de ejecución](winhttp-start-page.md) de la página de inicio de winhttp.</span><span class="sxs-lookup"><span data-stu-id="62042-128">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="62042-129">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="62042-129">Examples</span></span>

<span data-ttu-id="62042-130">En el ejemplo siguiente se muestra cómo abrir una conexión HTTP asincrónica, enviar una solicitud HTTP, esperar la respuesta y leer el texto de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="62042-130">The following example shows how to open an asynchronous HTTP connection, send an HTTP request, wait for the response and read the response text.</span></span>


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
    VARIANT         varTrue;
    VARIANT         varEmpty;

    CLSID           clsid;

    VariantInit(&varTrue);
    V_VT(&varTrue)   = VT_BOOL;
    V_BOOL(&varTrue) = VARIANT_TRUE;

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
        hr = pIWinHttpRequest->Open(bstrMethod, bstrUrl, varTrue);
        SysFreeString(bstrMethod);
        SysFreeString(bstrUrl);
    }
    if (SUCCEEDED(hr))
    {    // Send Request.
        hr = pIWinHttpRequest->Send(varEmpty);
    }
    if (SUCCEEDED(hr))
    {    // Wait for response.
        VARIANT_BOOL varResult;
        hr = pIWinHttpRequest->WaitForResponse(varEmpty, &varResult);
    }
    if (SUCCEEDED(hr))
    {    // Get Response text.
        hr = pIWinHttpRequest->get_ResponseText(&bstrResponse);
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



<span data-ttu-id="62042-131">En el ejemplo de scripting siguiente se muestra cómo abrir una conexión HTTP asincrónica, enviar una solicitud HTTP, esperar una respuesta y leer el texto de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="62042-131">The following scripting example shows how to open an asynchronous HTTP connection, send an HTTP request, wait for a response, and read the response text.</span></span>


```JScript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Initialize an HTTP request.  
WinHttpReq.Open("GET", "https://www.microsoft.com", true);

// Send the HTTP request.
WinHttpReq.Send(); 

// Wait for the response.
WinHttpReq.WaitForResponse();

// Display the response text.
WScript.Echo( WinHttpReq.ResponseText);
```



## <a name="requirements"></a><span data-ttu-id="62042-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62042-132">Requirements</span></span>



| <span data-ttu-id="62042-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="62042-133">Requirement</span></span> | <span data-ttu-id="62042-134">Value</span><span class="sxs-lookup"><span data-stu-id="62042-134">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="62042-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="62042-135">Minimum supported client</span></span><br/> | <span data-ttu-id="62042-136">Windows XP, Windows 2000 Professional con las \[ aplicaciones de escritorio de SP3 únicamente\]</span><span class="sxs-lookup"><span data-stu-id="62042-136">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="62042-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="62042-137">Minimum supported server</span></span><br/> | <span data-ttu-id="62042-138">Windows Server 2003, Windows 2000 Server con \[ solo aplicaciones de escritorio de SP3\]</span><span class="sxs-lookup"><span data-stu-id="62042-138">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="62042-139">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="62042-139">Redistributable</span></span><br/>          | <span data-ttu-id="62042-140">WinHTTP 5,0 e Internet Explorer 5,01 o posterior en Windows XP y Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="62042-140">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="62042-141">IDL</span><span class="sxs-lookup"><span data-stu-id="62042-141">IDL</span></span><br/>                      | <dl> <span data-ttu-id="62042-142"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="62042-142"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="62042-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="62042-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="62042-144"><dt>Winhttp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="62042-144"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="62042-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="62042-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62042-146"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62042-146"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="62042-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="62042-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62042-148">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="62042-148">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="62042-149">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="62042-149">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="62042-150">**Ábra**</span><span class="sxs-lookup"><span data-stu-id="62042-150">**Open**</span></span>](iwinhttprequest-open.md)
</dt> <dt>

[<span data-ttu-id="62042-151">Versiones de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="62042-151">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




