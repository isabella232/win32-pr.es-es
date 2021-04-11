---
description: El método SetTimeouts especifica los componentes de tiempo de espera individuales de una operación de envío y recepción, en milisegundos.
ms.assetid: c2b6c432-5f3b-4361-8026-1b843c6697ae
title: 'IWinHttpRequest:: SetTimeouts (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.SetTimeouts
- WinHttpRequest.SetTimeouts
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 3f2f81585fdf444b6b5ab1795f183897687732ed
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/10/2021
ms.locfileid: "104280221"
---
# <a name="iwinhttprequestsettimeouts-method"></a><span data-ttu-id="31585-103">IWinHttpRequest:: SetTimeouts (método)</span><span class="sxs-lookup"><span data-stu-id="31585-103">IWinHttpRequest::SetTimeouts method</span></span>

<span data-ttu-id="31585-104">El método **SetTimeouts** especifica los componentes de tiempo de espera individuales de una operación de envío y recepción, en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="31585-104">The **SetTimeouts** method specifies the individual time-out components of a send/receive operation, in milliseconds.</span></span>

## <a name="syntax"></a><span data-ttu-id="31585-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="31585-105">Syntax</span></span>


```C++
HRESULT SetTimeouts(
  [in] long ResolveTimeout,
  [in] long ConnectTimeout,
  [in] long SendTimeout,
  [in] long ReceiveTimeout
);
```



## <a name="parameters"></a><span data-ttu-id="31585-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="31585-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31585-107">*ResolveTimeout* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="31585-107">*ResolveTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31585-108">Valor de tiempo de espera que se aplica al resolver un nombre de host (como `www.microsoft.com` ) en una dirección IP (por ejemplo, 192.168.131.199), en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="31585-108">Time-out value applied when resolving a host name (such as `www.microsoft.com`) to an IP address (such as 192.168.131.199), in milliseconds.</span></span> <span data-ttu-id="31585-109">El valor predeterminado es cero, lo que significa que no hay tiempo de espera (infinito).</span><span class="sxs-lookup"><span data-stu-id="31585-109">The default value is zero, meaning no time-out (infinite).</span></span> <span data-ttu-id="31585-110">Si se especifica el tiempo de espera de DNS mediante el \_ \_ tiempo de espera de resolución de nombres, existe una sobrecarga de un subproceso por solicitud.</span><span class="sxs-lookup"><span data-stu-id="31585-110">If DNS timeout is specified using NAME\_RESOLUTION\_TIMEOUT, there is an overhead of one thread per request.</span></span>

</dd> <dt>

<span data-ttu-id="31585-111">*ConnectTimeout* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="31585-111">*ConnectTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31585-112">Valor de tiempo de espera aplicado al establecer un socket de comunicación con el servidor de destino, en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="31585-112">Time-out value applied when establishing a communication socket with the target server, in milliseconds.</span></span> <span data-ttu-id="31585-113">El valor predeterminado es 60.000 (60 segundos).</span><span class="sxs-lookup"><span data-stu-id="31585-113">The default value is 60,000 (60 seconds).</span></span>

</dd> <dt>

<span data-ttu-id="31585-114">*SendTimeout* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="31585-114">*SendTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31585-115">Valor de tiempo de espera aplicado al enviar un paquete individual de datos de solicitud en el socket de comunicación al servidor de destino, en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="31585-115">Time-out value applied when sending an individual packet of request data on the communication socket to the target server, in milliseconds.</span></span> <span data-ttu-id="31585-116">Normalmente, una solicitud grande enviada a un servidor HTTP se divide en varios paquetes. el tiempo de espera de envío se aplica al envío individual de cada paquete.</span><span class="sxs-lookup"><span data-stu-id="31585-116">A large request sent to an HTTP server are normally be broken up into multiple packets; the send time-out applies to sending each packet individually.</span></span> <span data-ttu-id="31585-117">El valor predeterminado es 30.000 (30 segundos).</span><span class="sxs-lookup"><span data-stu-id="31585-117">The default value is 30,000 (30 seconds).</span></span>

</dd> <dt>

<span data-ttu-id="31585-118">*ReceiveTimeout* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="31585-118">*ReceiveTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31585-119">Valor de tiempo de espera aplicado al recibir un paquete de datos de respuesta del servidor de destino, en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="31585-119">Time-out value applied when receiving a packet of response data from the target server, in milliseconds.</span></span> <span data-ttu-id="31585-120">Las respuestas grandes se dividen en varios paquetes. el tiempo de espera de recepción se aplica a la captura de cada paquete de datos fuera del socket.</span><span class="sxs-lookup"><span data-stu-id="31585-120">Large responses are be broken up into multiple packets; the receive time-out applies to fetching each packet of data off the socket.</span></span> <span data-ttu-id="31585-121">El valor predeterminado es 30.000 (30 segundos).</span><span class="sxs-lookup"><span data-stu-id="31585-121">The default value is 30,000 (30 seconds).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31585-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="31585-122">Return value</span></span>

<span data-ttu-id="31585-123">El valor devuelto es correcto si se ejecuta correctamente o un valor de error en caso contrario. **\_**</span><span class="sxs-lookup"><span data-stu-id="31585-123">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="31585-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="31585-124">Remarks</span></span>

<span data-ttu-id="31585-125">Todos los parámetros son obligatorios.</span><span class="sxs-lookup"><span data-stu-id="31585-125">All parameters are required.</span></span> <span data-ttu-id="31585-126">Un valor de 0 o-1 establece un tiempo de espera para esperar infinitamente.</span><span class="sxs-lookup"><span data-stu-id="31585-126">A value of 0 or -1 sets a time-out to wait infinitely.</span></span> <span data-ttu-id="31585-127">Un valor mayor que 0 establece el valor de tiempo de espera en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="31585-127">A value greater than 0 sets the time-out value in milliseconds.</span></span> <span data-ttu-id="31585-128">Por ejemplo, 30.000 establecería el tiempo de espera en 30 segundos.</span><span class="sxs-lookup"><span data-stu-id="31585-128">For example, 30,000 would set the time-out to 30 seconds.</span></span> <span data-ttu-id="31585-129">Todos los valores negativos distintos de-1 hacen que este método produzca un error.</span><span class="sxs-lookup"><span data-stu-id="31585-129">All negative values other than -1 cause this method to fail.</span></span>

<span data-ttu-id="31585-130">Los valores de tiempo de espera se aplican en la capa de Winsock.</span><span class="sxs-lookup"><span data-stu-id="31585-130">Time-out values are applied at the Winsock layer.</span></span>

> [!Note]  
> <span data-ttu-id="31585-131">En Windows XP y Windows 2000, consulte la sección [requisitos de tiempo de ejecución](winhttp-start-page.md) de la página de inicio de winhttp.</span><span class="sxs-lookup"><span data-stu-id="31585-131">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHttp start page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="31585-132">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="31585-132">Examples</span></span>

<span data-ttu-id="31585-133">En el ejemplo siguiente se muestra cómo establecer todos los tiempos de espera de WinHTTP en 30 segundos, abrir una conexión HTTP, enviar una solicitud HTTP y leer el texto de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="31585-133">The following example shows how to set all WinHTTP time-outs to 30 seconds, open an HTTP connection, send an HTTP request, and read the response text.</span></span>


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
    {    // Set Time-outs.
        hr = pIWinHttpRequest->SetTimeouts(30000, 30000,
                                           30000, 30000);
    }
    if (SUCCEEDED(hr))
    {    // Open WinHttpRequest.
        BSTR bstrMethod  = SysAllocString(L"GET");
        BSTR bstrUrl = SysAllocString(L"https://microsoft.com");
        hr = pIWinHttpRequest->Open(bstrMethod,
                                    bstrUrl,
                                    varFalse);
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
    {    // Print response to console.
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



<span data-ttu-id="31585-134">En el ejemplo de scripting siguiente se muestra cómo establecer todos los tiempos de espera de WinHTTP en 30 segundos, abrir una conexión HTTP y enviar una solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="31585-134">The following scripting example shows how to set all WinHTTP time-outs to 30 seconds, open an HTTP connection, and send an HTTP request.</span></span>


```JScript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Set time-outs. If time-outs are set, they must 
// be set before open.
WinHttpReq.SetTimeouts(30000, 30000, 30000, 30000);

// Initialize an HTTP request.  
WinHttpReq.Open("GET", "https://www.microsoft.com", false);

// Send the HTTP request.
WinHttpReq.Send();
```



## <a name="requirements"></a><span data-ttu-id="31585-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31585-135">Requirements</span></span>



| <span data-ttu-id="31585-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="31585-136">Requirement</span></span> | <span data-ttu-id="31585-137">Value</span><span class="sxs-lookup"><span data-stu-id="31585-137">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="31585-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="31585-138">Minimum supported client</span></span><br/> | <span data-ttu-id="31585-139">Windows XP, Windows 2000 Professional con las \[ aplicaciones de escritorio de SP3 únicamente\]</span><span class="sxs-lookup"><span data-stu-id="31585-139">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="31585-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="31585-140">Minimum supported server</span></span><br/> | <span data-ttu-id="31585-141">Windows Server 2003, Windows 2000 Server con \[ solo aplicaciones de escritorio de SP3\]</span><span class="sxs-lookup"><span data-stu-id="31585-141">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="31585-142">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="31585-142">Redistributable</span></span><br/>          | <span data-ttu-id="31585-143">WinHTTP 5,0 e Internet Explorer 5,01 o posterior en Windows XP y Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="31585-143">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="31585-144">IDL</span><span class="sxs-lookup"><span data-stu-id="31585-144">IDL</span></span><br/>                      | <dl> <span data-ttu-id="31585-145"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="31585-145"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="31585-146">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="31585-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="31585-147"><dt>Winhttp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="31585-147"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="31585-148">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="31585-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31585-149"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31585-149"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="31585-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="31585-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31585-151">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="31585-151">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="31585-152">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="31585-152">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="31585-153">Versiones de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="31585-153">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




