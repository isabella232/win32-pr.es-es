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
# <a name="iwinhttprequestopen-method"></a><span data-ttu-id="92bd4-103">IWinHttpRequest:: Open (método)</span><span class="sxs-lookup"><span data-stu-id="92bd4-103">IWinHttpRequest::Open method</span></span>

<span data-ttu-id="92bd4-104">El método **Open** abre una conexión http a un recurso http.</span><span class="sxs-lookup"><span data-stu-id="92bd4-104">The **Open** method opens an HTTP connection to an HTTP resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="92bd4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92bd4-105">Syntax</span></span>


```C++
HRESULT Open(
  [in]           BSTR    Method,
  [in]           BSTR    Url,
  [in, optional] VARIANT Async
);
```



## <a name="parameters"></a><span data-ttu-id="92bd4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="92bd4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92bd4-107">*Método* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="92bd4-107">*Method* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92bd4-108">Especifica el [*verbo http*](glossary.md) utilizado para el método **abierto** , como "Get" o "put".</span><span class="sxs-lookup"><span data-stu-id="92bd4-108">Specifies the [*HTTP verb*](glossary.md) used for the **Open** method, such as "GET" or "PUT".</span></span> <span data-ttu-id="92bd4-109">Use siempre mayúsculas como algunos servidores para omitir los *verbos http* en minúsculas.</span><span class="sxs-lookup"><span data-stu-id="92bd4-109">Always use uppercase as some servers ignore lowercase *HTTP verb* s.</span></span>

</dd> <dt>

<span data-ttu-id="92bd4-110">*Dirección URL* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="92bd4-110">*Url* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92bd4-111">Especifica el nombre del recurso.</span><span class="sxs-lookup"><span data-stu-id="92bd4-111">Specifies the name of the resource.</span></span> <span data-ttu-id="92bd4-112">Debe ser una dirección URL absoluta.</span><span class="sxs-lookup"><span data-stu-id="92bd4-112">This must be an absolute URL.</span></span>

</dd> <dt>

<span data-ttu-id="92bd4-113">*Async* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="92bd4-113">*Async* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="92bd4-114">Indica si se va a abrir en modo asincrónico.</span><span class="sxs-lookup"><span data-stu-id="92bd4-114">Indicates whether to open in asynchronous mode.</span></span>



| <span data-ttu-id="92bd4-115">Value</span><span class="sxs-lookup"><span data-stu-id="92bd4-115">Value</span></span>                                                                                                                                                         | <span data-ttu-id="92bd4-116">Significado</span><span class="sxs-lookup"><span data-stu-id="92bd4-116">Meaning</span></span>                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="VARIANT_FALSE"></span><span id="variant_false"></span><dl> <span data-ttu-id="92bd4-117"><dt>**VARIANTE \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="92bd4-117"><dt>**VARIANT\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="92bd4-118">Abre la conexión HTTP en modo sincrónico.</span><span class="sxs-lookup"><span data-stu-id="92bd4-118">Opens the HTTP connection in synchronous mode.</span></span> <span data-ttu-id="92bd4-119">Una llamada a [**send**](iwinhttprequest-send.md) no vuelve hasta que [WinHTTP](about-winhttp.md) ha recibido por completo la respuesta.</span><span class="sxs-lookup"><span data-stu-id="92bd4-119">A call to [**Send**](iwinhttprequest-send.md) does not return until [WinHTTP](about-winhttp.md) has completely received the response.</span></span><br/> |
| <span id="VARIANT_TRUE"></span><span id="variant_true"></span><dl> <span data-ttu-id="92bd4-120"><dt>**VARIANTE \_ true**</dt></span><span class="sxs-lookup"><span data-stu-id="92bd4-120"><dt>**VARIANT\_TRUE**</dt></span></span> </dl>    | <span data-ttu-id="92bd4-121">Abre la conexión HTTP en modo asincrónico.</span><span class="sxs-lookup"><span data-stu-id="92bd4-121">Opens the HTTP connection in asynchronous mode.</span></span><br/>                                                                                                                                        |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92bd4-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="92bd4-122">Return value</span></span>

<span data-ttu-id="92bd4-123">El valor devuelto es correcto si se ejecuta correctamente o un valor de error en caso contrario. **\_**</span><span class="sxs-lookup"><span data-stu-id="92bd4-123">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="92bd4-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="92bd4-124">Remarks</span></span>

<span data-ttu-id="92bd4-125">Este método abre una conexión al recurso identificado en la *dirección URL* mediante el [*verbo http*](glossary.md) proporcionado en el *método*.</span><span class="sxs-lookup"><span data-stu-id="92bd4-125">This method opens a connection to the resource identified in *Url* using the [*HTTP verb*](glossary.md) given in *Method*.</span></span>

> [!Note]  
> <span data-ttu-id="92bd4-126">En Windows XP y Windows 2000, consulte la sección [requisitos de tiempo de ejecución](winhttp-start-page.md) de la página de inicio de winhttp.</span><span class="sxs-lookup"><span data-stu-id="92bd4-126">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="92bd4-127">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="92bd4-127">Examples</span></span>

<span data-ttu-id="92bd4-128">En el ejemplo siguiente se muestra cómo abrir una conexión HTTP, enviar una solicitud HTTP y leer el texto de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="92bd4-128">The following example shows how to open an HTTP connection, send an HTTP request, and read the response text.</span></span>


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



<span data-ttu-id="92bd4-129">En el ejemplo de scripting siguiente se muestra cómo abrir una conexión HTTP, enviar una solicitud HTTP y leer el texto de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="92bd4-129">The following scripting example shows how to open an HTTP connection, send an HTTP request, and read the response text.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="92bd4-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92bd4-130">Requirements</span></span>



| <span data-ttu-id="92bd4-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="92bd4-131">Requirement</span></span> | <span data-ttu-id="92bd4-132">Value</span><span class="sxs-lookup"><span data-stu-id="92bd4-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="92bd4-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="92bd4-133">Minimum supported client</span></span><br/> | <span data-ttu-id="92bd4-134">Windows XP, Windows 2000 Professional con las \[ aplicaciones de escritorio de SP3 únicamente\]</span><span class="sxs-lookup"><span data-stu-id="92bd4-134">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="92bd4-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="92bd4-135">Minimum supported server</span></span><br/> | <span data-ttu-id="92bd4-136">Windows Server 2003, Windows 2000 Server con \[ solo aplicaciones de escritorio de SP3\]</span><span class="sxs-lookup"><span data-stu-id="92bd4-136">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="92bd4-137">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="92bd4-137">Redistributable</span></span><br/>          | <span data-ttu-id="92bd4-138">WinHTTP 5,0 e Internet Explorer 5,01 o posterior en Windows XP y Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="92bd4-138">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="92bd4-139">IDL</span><span class="sxs-lookup"><span data-stu-id="92bd4-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="92bd4-140"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="92bd4-140"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="92bd4-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="92bd4-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="92bd4-142"><dt>Winhttp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="92bd4-142"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="92bd4-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="92bd4-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="92bd4-144"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92bd4-144"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="92bd4-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="92bd4-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92bd4-146">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="92bd4-146">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="92bd4-147">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="92bd4-147">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="92bd4-148">Versiones de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="92bd4-148">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




