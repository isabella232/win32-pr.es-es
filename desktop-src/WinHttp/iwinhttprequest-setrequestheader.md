---
description: Agrega, cambia o elimina un encabezado de solicitud HTTP.
ms.assetid: 8cb4891d-0bdb-4dea-8ebe-d6ed26a50e41
title: 'IWinHttpRequest:: SetRequestHeader (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.SetRequestHeader
- WinHttpRequest.SetRequestHeader
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 9bc2ae6df420f38d11fb2f0f19d5fcbd0bcc0909
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678511"
---
# <a name="iwinhttprequestsetrequestheader-method"></a><span data-ttu-id="2f5c9-103">IWinHttpRequest:: SetRequestHeader (método)</span><span class="sxs-lookup"><span data-stu-id="2f5c9-103">IWinHttpRequest::SetRequestHeader method</span></span>

<span data-ttu-id="2f5c9-104">El método **SetRequestHeader** agrega, cambia o elimina un encabezado de solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="2f5c9-104">The **SetRequestHeader** method adds, changes, or deletes an HTTP request header.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f5c9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2f5c9-105">Syntax</span></span>


```C++
HRESULT SetRequestHeader(
  [in] BSTR Header,
  [in] BSTR Value
);
```



## <a name="parameters"></a><span data-ttu-id="2f5c9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2f5c9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f5c9-107">*Encabezado* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="2f5c9-107">*Header* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f5c9-108">Especifica el nombre del encabezado que se va a establecer, por ejemplo, "depth".</span><span class="sxs-lookup"><span data-stu-id="2f5c9-108">Specifies the name of the header to be set, for example, "depth".</span></span> <span data-ttu-id="2f5c9-109">Este parámetro no debe contener un signo de dos puntos y debe ser el texto real del encabezado HTTP.</span><span class="sxs-lookup"><span data-stu-id="2f5c9-109">This parameter should not contain a colon and must be the actual text of the HTTP header.</span></span>

</dd> <dt>

<span data-ttu-id="2f5c9-110">*Valor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="2f5c9-110">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f5c9-111">Especifica el valor del encabezado, por ejemplo, "Infinity".</span><span class="sxs-lookup"><span data-stu-id="2f5c9-111">Specifies the value of the header, for example, "infinity".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f5c9-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2f5c9-112">Return value</span></span>

<span data-ttu-id="2f5c9-113">El valor devuelto es correcto si se ejecuta correctamente o un valor de error en caso contrario. **\_**</span><span class="sxs-lookup"><span data-stu-id="2f5c9-113">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f5c9-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2f5c9-114">Remarks</span></span>

<span data-ttu-id="2f5c9-115">Los encabezados se transfieren a través de las redirecciones.</span><span class="sxs-lookup"><span data-stu-id="2f5c9-115">Headers are transferred across redirects.</span></span> <span data-ttu-id="2f5c9-116">Esto puede crear una vulnerabilidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="2f5c9-116">This can create a security vulnerability.</span></span> <span data-ttu-id="2f5c9-117">Para evitar que se transfieran los encabezados si se produce una redirección, utilice la devolución de llamada de [*\_ devolución de \_ llamada de estado de WinHTTP*](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) para corregir los encabezados específicos cuando se produce una redirección.</span><span class="sxs-lookup"><span data-stu-id="2f5c9-117">To avoid having headers transferred if a redirect occurs, use the [*WINHTTP\_STATUS\_CALLBACK*](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) callback to correct the specific headers when a redirect occurs.</span></span>

<span data-ttu-id="2f5c9-118">El método **SetRequestHeader** permite que la aplicación que realiza la llamada agregue o elimine un encabezado de solicitud HTTP antes de enviar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2f5c9-118">The **SetRequestHeader** method enables the calling application to add or delete an HTTP request header prior to sending the request.</span></span> <span data-ttu-id="2f5c9-119">El nombre del encabezado se proporciona en el *encabezado* y el token o el valor del encabezado se especifican en el *valor*.</span><span class="sxs-lookup"><span data-stu-id="2f5c9-119">The header name is given in *Header*, and the header token or value is given in *Value*.</span></span> <span data-ttu-id="2f5c9-120">Para agregar un encabezado, proporcione un nombre y un valor de encabezado.</span><span class="sxs-lookup"><span data-stu-id="2f5c9-120">To add a header, supply a header name and value.</span></span> <span data-ttu-id="2f5c9-121">Si ya existe otro encabezado con este nombre, se reemplazará.</span><span class="sxs-lookup"><span data-stu-id="2f5c9-121">If another header already exists with this name, it is replaced.</span></span> <span data-ttu-id="2f5c9-122">Para eliminar un encabezado, establezca *encabezado* en el nombre del encabezado que se va a eliminar y establezca *valor* en **null**.</span><span class="sxs-lookup"><span data-stu-id="2f5c9-122">To delete a header, set *Header* to the name of the header to delete and set *Value* to **NULL**.</span></span>

<span data-ttu-id="2f5c9-123">Se validan el nombre y el valor de los encabezados de solicitud agregados con este método.</span><span class="sxs-lookup"><span data-stu-id="2f5c9-123">The name and value of request headers added with this method are validated.</span></span> <span data-ttu-id="2f5c9-124">Los encabezados deben tener el formato correcto.</span><span class="sxs-lookup"><span data-stu-id="2f5c9-124">Headers must be well formed.</span></span> <span data-ttu-id="2f5c9-125">Para obtener más información acerca de los encabezados HTTP válidos, vea [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span><span class="sxs-lookup"><span data-stu-id="2f5c9-125">For more information about valid HTTP headers, see [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span></span> <span data-ttu-id="2f5c9-126">Si se usa un encabezado no válido, se produce un error y no se agrega el encabezado.</span><span class="sxs-lookup"><span data-stu-id="2f5c9-126">If an invalid header is used, an error occurs and the header is not added.</span></span>

> [!Note]  
> <span data-ttu-id="2f5c9-127">En Windows XP y Windows 2000, consulte la sección [requisitos de tiempo de ejecución](winhttp-start-page.md) de la página de inicio de winhttp.</span><span class="sxs-lookup"><span data-stu-id="2f5c9-127">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="2f5c9-128">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="2f5c9-128">Examples</span></span>

<span data-ttu-id="2f5c9-129">En el ejemplo siguiente se muestra cómo abrir una conexión HTTP, establecer un encabezado de solicitud, enviar una solicitud HTTP y leer el texto de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2f5c9-129">The following example shows how to open an HTTP connection, set a request header, send an HTTP request, and read the response text.</span></span> <span data-ttu-id="2f5c9-130">Este ejemplo debe ejecutarse desde un símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="2f5c9-130">This example must be run from a command prompt.</span></span>


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
    {    // Open WinHttpRequest.
        BSTR bstrMethod  = SysAllocString(L"GET");
        BSTR bstrUrl = SysAllocString(L"https://microsoft.com");
        hr = pIWinHttpRequest->Open(bstrMethod, bstrUrl, varFalse);
        SysFreeString(bstrMethod);
        SysFreeString(bstrUrl);
    }
    if (SUCCEEDED(hr))
    {    // Set request header.
        BSTR bstrName  = SysAllocString(L"Date");
        BSTR bstrValue = SysAllocString(L"Fri, 16 Mar 2001 00:25:54 GMT");
        hr = pIWinHttpRequest->SetRequestHeader(bstrName, bstrValue);
        SysFreeString(bstrName);
        SysFreeString(bstrValue);
    }
    if (SUCCEEDED(hr))
    {    // Send Request.
        hr = pIWinHttpRequest->Send(varEmpty);
    }
    if (SUCCEEDED(hr))
    {    // Get Response headers.
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



<span data-ttu-id="2f5c9-131">En el ejemplo de scripting siguiente se muestra cómo abrir una conexión HTTP, establecer un encabezado de solicitud y enviar una solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="2f5c9-131">The following scripting example shows how to open an HTTP connection, set a request header, and send an HTTP request.</span></span>


```JScript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Initialize an HTTP request.  
WinHttpReq.Open("GET", "https://www.microsoft.com", false);

// Add/replace a request header.
WinHttpReq.SetRequestHeader("Date", Date());

// Send the HTTP request.
WinHttpReq.Send();
```



## <a name="requirements"></a><span data-ttu-id="2f5c9-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f5c9-132">Requirements</span></span>



| <span data-ttu-id="2f5c9-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f5c9-133">Requirement</span></span> | <span data-ttu-id="2f5c9-134">Value</span><span class="sxs-lookup"><span data-stu-id="2f5c9-134">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f5c9-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2f5c9-135">Minimum supported client</span></span><br/> | <span data-ttu-id="2f5c9-136">Windows XP, Windows 2000 Professional con las \[ aplicaciones de escritorio de SP3 únicamente\]</span><span class="sxs-lookup"><span data-stu-id="2f5c9-136">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="2f5c9-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2f5c9-137">Minimum supported server</span></span><br/> | <span data-ttu-id="2f5c9-138">Windows Server 2003, Windows 2000 Server con \[ solo aplicaciones de escritorio de SP3\]</span><span class="sxs-lookup"><span data-stu-id="2f5c9-138">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="2f5c9-139">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="2f5c9-139">Redistributable</span></span><br/>          | <span data-ttu-id="2f5c9-140">WinHTTP 5,0 e Internet Explorer 5,01 o posterior en Windows XP y Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="2f5c9-140">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="2f5c9-141">IDL</span><span class="sxs-lookup"><span data-stu-id="2f5c9-141">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2f5c9-142"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2f5c9-142"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="2f5c9-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2f5c9-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="2f5c9-144"><dt>Winhttp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2f5c9-144"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="2f5c9-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2f5c9-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f5c9-146"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f5c9-146"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="2f5c9-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="2f5c9-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f5c9-148">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="2f5c9-148">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="2f5c9-149">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="2f5c9-149">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="2f5c9-150">Versiones de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="2f5c9-150">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

