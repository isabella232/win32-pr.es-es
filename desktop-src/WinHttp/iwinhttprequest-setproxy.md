---
description: Establece la información del servidor proxy.
ms.assetid: 279d0557-2718-4c50-b84c-cc7c8def57a6
title: 'IWinHttpRequest:: SetProxy (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.SetProxy
- WinHttpRequest.SetProxy
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 7af3c7c33b17e14c3adbdd70f3d2031e7438747a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717211"
---
# <a name="iwinhttprequestsetproxy-method"></a><span data-ttu-id="cdb18-103">IWinHttpRequest:: SetProxy (método)</span><span class="sxs-lookup"><span data-stu-id="cdb18-103">IWinHttpRequest::SetProxy method</span></span>

<span data-ttu-id="cdb18-104">El método **SetProxy** establece la información del servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="cdb18-104">The **SetProxy** method sets proxy server information.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdb18-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cdb18-105">Syntax</span></span>


```C++
HRESULT SetProxy(
  [in]           HTTPREQUEST_PROXY_SETTING ProxySetting,
  [in, optional] VARIANT                   ProxyServer,
  [in, optional] VARIANT                   BypassList
);
```



## <a name="parameters"></a><span data-ttu-id="cdb18-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cdb18-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cdb18-107">*ProxySetting* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cdb18-107">*ProxySetting* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdb18-108">Marcas que controlan este método.</span><span class="sxs-lookup"><span data-stu-id="cdb18-108">The flags that control this method.</span></span> <span data-ttu-id="cdb18-109">Puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="cdb18-109">Can be one of the following values.</span></span>



| <span data-ttu-id="cdb18-110">Value</span><span class="sxs-lookup"><span data-stu-id="cdb18-110">Value</span></span>                                                                                                           | <span data-ttu-id="cdb18-111">Significado</span><span class="sxs-lookup"><span data-stu-id="cdb18-111">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cdb18-112"><dt>HTTPREQUEST \_ PROXYSETTING \_ predeterminado</dt></span><span class="sxs-lookup"><span data-stu-id="cdb18-112"><dt>HTTPREQUEST\_PROXYSETTING\_DEFAULT</dt></span></span> </dl>   | <span data-ttu-id="cdb18-113">Configuración de proxy predeterminada.</span><span class="sxs-lookup"><span data-stu-id="cdb18-113">Default proxy setting.</span></span> <span data-ttu-id="cdb18-114">Equivalente a **HTTPREQUEST \_ PROXYSETTING \_ Preconfig**.</span><span class="sxs-lookup"><span data-stu-id="cdb18-114">Equivalent to **HTTPREQUEST\_PROXYSETTING\_PRECONFIG**.</span></span><br/>                                                                                                                                                                                                                                                             |
| <dl> <span data-ttu-id="cdb18-115"><dt>preconfiguración de \_ PROXYSETTING HTTPREQUEST \_</dt></span><span class="sxs-lookup"><span data-stu-id="cdb18-115"><dt>HTTPREQUEST\_PROXYSETTING\_PRECONFIG</dt></span></span> </dl> | <span data-ttu-id="cdb18-116">Indica que la configuración del proxy debe obtenerse del registro.</span><span class="sxs-lookup"><span data-stu-id="cdb18-116">Indicates that the proxy settings should be obtained from the registry.</span></span> <span data-ttu-id="cdb18-117">Se supone que se ha ejecutado [Proxycfg.exe](proxycfg-exe--a-proxy-configuration-tool.md) .</span><span class="sxs-lookup"><span data-stu-id="cdb18-117">This assumes that [Proxycfg.exe](proxycfg-exe--a-proxy-configuration-tool.md) has been run.</span></span> <span data-ttu-id="cdb18-118">Si Proxycfg.exe no se ha ejecutado y se ha especificado la **\_ \_ preconfiguración de HttpRequest PROXYSETTING** , el comportamiento es equivalente a **HttpRequest \_ PROXYSETTING \_ Direct**.</span><span class="sxs-lookup"><span data-stu-id="cdb18-118">If Proxycfg.exe has not been run and **HTTPREQUEST\_PROXYSETTING\_PRECONFIG** is specified, then the behavior is equivalent to **HTTPREQUEST\_PROXYSETTING\_DIRECT**.</span></span><br/> |
| <dl> <span data-ttu-id="cdb18-119"><dt>PROXYSETTING de HTTPREQUEST \_ \_ directo</dt></span><span class="sxs-lookup"><span data-stu-id="cdb18-119"><dt>HTTPREQUEST\_PROXYSETTING\_DIRECT</dt></span></span> </dl>    | <span data-ttu-id="cdb18-120">Indica que se debe tener acceso directamente a todos los servidores HTTP y HTTPS.</span><span class="sxs-lookup"><span data-stu-id="cdb18-120">Indicates that all HTTP and HTTPS servers should be accessed directly.</span></span> <span data-ttu-id="cdb18-121">Use este comando si no hay ningún servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="cdb18-121">Use this command if there is no proxy server.</span></span><br/>                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="cdb18-122"><dt>\_proxy PROXYSETTING \_ HTTPREQUEST</dt></span><span class="sxs-lookup"><span data-stu-id="cdb18-122"><dt>HTTPREQUEST\_PROXYSETTING\_PROXY</dt></span></span> </dl>     | <span data-ttu-id="cdb18-123">Cuando se especifica el **\_ \_ proxy HTTPREQUEST PROXYSETTING** , *varProxyServer* se debe establecer en una cadena de servidor proxy y *varBypassList* debe establecerse en una cadena de lista de omisión de dominio.</span><span class="sxs-lookup"><span data-stu-id="cdb18-123">When **HTTPREQUEST\_PROXYSETTING\_PROXY** is specified, *varProxyServer* should be set to a proxy server string and *varBypassList* should be set to a domain bypass list string.</span></span> <span data-ttu-id="cdb18-124">Esta configuración de proxy solo se aplica a la instancia actual del objeto [**WinHttpRequest**](winhttprequest.md) .</span><span class="sxs-lookup"><span data-stu-id="cdb18-124">This proxy configuration applies only to the current instance of the [**WinHttpRequest**](winhttprequest.md) object.</span></span><br/>                                    |



 

</dd> <dt>

<span data-ttu-id="cdb18-125">*ProxyServer* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="cdb18-125">*ProxyServer* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cdb18-126">Se establece en una cadena de servidor proxy cuando *ProxySetting* es igual a **HTTPREQUEST \_ ProxySetting \_ proxy**.</span><span class="sxs-lookup"><span data-stu-id="cdb18-126">Set to a proxy server string when *ProxySetting* equals **HTTPREQUEST\_PROXYSETTING\_PROXY**.</span></span>

</dd> <dt>

<span data-ttu-id="cdb18-127">*BypassList* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="cdb18-127">*BypassList* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cdb18-128">Se establece en una cadena de lista de omisión de dominio cuando *ProxySetting* es igual a **HTTPREQUEST \_ ProxySetting \_ proxy**.</span><span class="sxs-lookup"><span data-stu-id="cdb18-128">Set to a domain bypass list string when *ProxySetting* equals **HTTPREQUEST\_PROXYSETTING\_PROXY**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cdb18-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cdb18-129">Return value</span></span>

<span data-ttu-id="cdb18-130">El valor devuelto es correcto si se ejecuta correctamente o un valor de error en caso contrario. **\_**</span><span class="sxs-lookup"><span data-stu-id="cdb18-130">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="cdb18-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cdb18-131">Remarks</span></span>

<span data-ttu-id="cdb18-132">Permite a la aplicación que realiza la llamada especificar el uso de la información de proxy predeterminada (configurada por la herramienta de configuración de proxy) o invalidar [Proxycfg.exe](proxycfg-exe--a-proxy-configuration-tool.md).</span><span class="sxs-lookup"><span data-stu-id="cdb18-132">Enables the calling application to specify use of default proxy information (configured by the proxy configuration tool) or to override [Proxycfg.exe](proxycfg-exe--a-proxy-configuration-tool.md).</span></span> <span data-ttu-id="cdb18-133">Se debe llamar a este método antes de llamar al método [**send**](iwinhttprequest-send.md) .</span><span class="sxs-lookup"><span data-stu-id="cdb18-133">This method must be called before calling the [**Send**](iwinhttprequest-send.md) method.</span></span> <span data-ttu-id="cdb18-134">Si se llama a este método después del método [**send**](iwinhttprequest-send.md) , no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="cdb18-134">If this method is called after the [**Send**](iwinhttprequest-send.md) method, it has no effect.</span></span>

<span data-ttu-id="cdb18-135">[**IWinHttpRequest**](iwinhttprequest-interface.md) pasa estos parámetros a los servicios http de Microsoft Windows (WinHTTP).</span><span class="sxs-lookup"><span data-stu-id="cdb18-135">[**IWinHttpRequest**](iwinhttprequest-interface.md) passes these parameters to Microsoft Windows HTTP Services (WinHTTP).</span></span>

> [!Note]  
> <span data-ttu-id="cdb18-136">En Windows XP y Windows 2000, consulte la sección [requisitos de tiempo de ejecución](winhttp-start-page.md) de la página de inicio de winhttp.</span><span class="sxs-lookup"><span data-stu-id="cdb18-136">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="cdb18-137">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="cdb18-137">Examples</span></span>

<span data-ttu-id="cdb18-138">En el ejemplo siguiente se muestra cómo establecer la configuración de proxy para un servidor proxy determinado, abrir una conexión HTTP, enviar una solicitud HTTP y leer el texto de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cdb18-138">The following example shows how to set the proxy settings for a particular proxy server, open an HTTP connection, send an HTTP request, and read the response text.</span></span> <span data-ttu-id="cdb18-139">Este ejemplo debe ejecutarse desde un símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="cdb18-139">This example must be run from a command prompt.</span></span> <span data-ttu-id="cdb18-140">Esta configuración de proxy solo funciona si tiene un servidor proxy denominado " \_ servidor proxy" que usa el puerto 80 y el equipo puede omitir el servidor proxy cuando el nombre de host termina con ". Microsoft.com".</span><span class="sxs-lookup"><span data-stu-id="cdb18-140">These proxy settings work only if you have a proxy server named "proxy\_server" that uses port 80 and your computer can bypass the proxy server when the host name ends with ".microsoft.com".</span></span>


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
    VARIANT         varProxy;
    VARIANT         varUrl;
    
    CLSID           clsid;

    VariantInit(&varFalse);
    V_VT(&varFalse)   = VT_BOOL;
    V_BOOL(&varFalse) = VARIANT_FALSE;

    VariantInit(&varEmpty);
    V_VT(&varEmpty) = VT_ERROR;

    VariantInit(&varProxy);
    VariantInit(&varUrl);

    hr = CLSIDFromProgID(L"WinHttp.WinHttpRequest.5.1", &clsid);

    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(clsid, NULL, 
                              CLSCTX_INPROC_SERVER, 
                              IID_IWinHttpRequest, 
                              (void **)&pIWinHttpRequest);
    }
    if (SUCCEEDED(hr))
    {   // Specify proxy and URL.
                varProxy.vt = VT_BSTR;
                varProxy.bstrVal = SysAllocString(L"proxy_server:80");
                varUrl.vt = VT_BSTR;
                varUrl.bstrVal = SysAllocString(L"*.microsoft.com");
                hr = pIWinHttpRequest->SetProxy(HTTPREQUEST_PROXYSETTING_PROXY,
                                    varProxy, varUrl); 
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
    if (SUCCEEDED(hr))
    {   // Print the response to a console.
                wprintf(L"%.256s",bstrResponse);
    }
        
        // Release memory.
    if (pIWinHttpRequest)
        pIWinHttpRequest->Release();
        if (varProxy.bstrVal)
                SysFreeString(varProxy.bstrVal);
        if (varUrl.bstrVal)
                SysFreeString(varUrl.bstrVal);
    if (bstrResponse)
        SysFreeString(bstrResponse);
        
        CoUninitialize();
        return 0;
}
```



<span data-ttu-id="cdb18-141">En el ejemplo de scripting siguiente se muestra cómo establecer la configuración de proxy para un servidor proxy determinado, abrir una conexión HTTP, enviar una solicitud HTTP y leer el texto de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cdb18-141">The following scripting example shows how to set the proxy settings for a particular proxy server, open an HTTP connection, send an HTTP request, and read the response text.</span></span> <span data-ttu-id="cdb18-142">Esta configuración de proxy solo funciona si tiene un servidor proxy denominado " \_ servidor proxy" que usa el puerto 80 y el equipo puede omitir el servidor proxy cuando el nombre de host termina con ". Microsoft.com".</span><span class="sxs-lookup"><span data-stu-id="cdb18-142">These proxy settings work only if you have a proxy server named "proxy\_server" that uses port 80 and your computer can bypass the proxy server when the host name ends with ".microsoft.com".</span></span>


```JScript
// HttpRequest SetCredentials flags.
HTTPREQUEST_PROXYSETTING_DEFAULT   = 0;
HTTPREQUEST_PROXYSETTING_PRECONFIG = 0;
HTTPREQUEST_PROXYSETTING_DIRECT    = 1;
HTTPREQUEST_PROXYSETTING_PROXY     = 2;

// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Use proxy_server for all requests outside of 
// the microsoft.com domain.
WinHttpReq.SetProxy( HTTPREQUEST_PROXYSETTING_PROXY, 
                     "proxy_server:80", 
                     "*.microsoft.com");

// Initialize an HTTP request.  
WinHttpReq.Open("GET", "https://www.microsoft.com", false);

// Send the HTTP request.
WinHttpReq.Send(); 

// Display the response text.
WScript.Echo( WinHttpReq.ResponseText);
```



## <a name="requirements"></a><span data-ttu-id="cdb18-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cdb18-143">Requirements</span></span>



| <span data-ttu-id="cdb18-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="cdb18-144">Requirement</span></span> | <span data-ttu-id="cdb18-145">Value</span><span class="sxs-lookup"><span data-stu-id="cdb18-145">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdb18-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cdb18-146">Minimum supported client</span></span><br/> | <span data-ttu-id="cdb18-147">Windows XP, Windows 2000 Professional con las \[ aplicaciones de escritorio de SP3 únicamente\]</span><span class="sxs-lookup"><span data-stu-id="cdb18-147">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="cdb18-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cdb18-148">Minimum supported server</span></span><br/> | <span data-ttu-id="cdb18-149">Windows Server 2003, Windows 2000 Server con \[ solo aplicaciones de escritorio de SP3\]</span><span class="sxs-lookup"><span data-stu-id="cdb18-149">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="cdb18-150">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="cdb18-150">Redistributable</span></span><br/>          | <span data-ttu-id="cdb18-151">WinHTTP 5,0 e Internet Explorer 5,01 o posterior en Windows XP y Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="cdb18-151">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="cdb18-152">IDL</span><span class="sxs-lookup"><span data-stu-id="cdb18-152">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cdb18-153"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cdb18-153"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="cdb18-154">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cdb18-154">Library</span></span><br/>                  | <dl> <span data-ttu-id="cdb18-155"><dt>Winhttp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cdb18-155"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="cdb18-156">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cdb18-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cdb18-157"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cdb18-157"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="cdb18-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="cdb18-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdb18-159">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="cdb18-159">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="cdb18-160">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="cdb18-160">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="cdb18-161">Versiones de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="cdb18-161">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




