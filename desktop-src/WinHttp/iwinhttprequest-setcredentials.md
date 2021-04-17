---
description: Establece las credenciales que se van a usar con un servidor HTTP, ya sea un servidor proxy o un servidor de origen.
ms.assetid: d96c6e76-92b8-4ad7-8ca7-a9acbed523ff
title: 'IWinHttpRequest:: SetCredentials (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.SetCredentials
- WinHttpRequest.SetCredentials
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 46b0dfb321763a3b3bfe622e116f2e76c5e59423
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716295"
---
# <a name="iwinhttprequestsetcredentials-method"></a><span data-ttu-id="93780-103">IWinHttpRequest:: SetCredentials (método)</span><span class="sxs-lookup"><span data-stu-id="93780-103">IWinHttpRequest::SetCredentials method</span></span>

<span data-ttu-id="93780-104">El método **SetCredentials** establece las credenciales que se van a usar con un servidor http, ya sea un servidor proxy o un servidor de origen.</span><span class="sxs-lookup"><span data-stu-id="93780-104">The **SetCredentials** method sets credentials to be used with an HTTP server, whether it is a proxy server or an originating server.</span></span>

## <a name="syntax"></a><span data-ttu-id="93780-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="93780-105">Syntax</span></span>


```C++
HRESULT SetCredentials(
  [in] BSTR                             UserName,
  [in] BSTR                             Password,
  [in] HTTPREQUEST_SETCREDENTIALS_FLAGS Flags
);
```



## <a name="parameters"></a><span data-ttu-id="93780-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="93780-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93780-107">*Nombre de usuario* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="93780-107">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93780-108">Especifica el nombre de usuario para la autenticación.</span><span class="sxs-lookup"><span data-stu-id="93780-108">Specifies the user name for authentication.</span></span>

</dd> <dt>

<span data-ttu-id="93780-109">*Contraseña* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="93780-109">*Password* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93780-110">Especifica la contraseña para la autenticación.</span><span class="sxs-lookup"><span data-stu-id="93780-110">Specifies the password for authentication.</span></span> <span data-ttu-id="93780-111">Este parámetro se omite si *bstrUserName* es **null** o falta.</span><span class="sxs-lookup"><span data-stu-id="93780-111">This parameter is ignored if *bstrUserName* is **NULL** or missing.</span></span>

</dd> <dt>

<span data-ttu-id="93780-112">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="93780-112">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93780-113">Especifica el momento en que [**IWinHttpRequest**](iwinhttprequest-interface.md) usa las credenciales.</span><span class="sxs-lookup"><span data-stu-id="93780-113">Specifies when [**IWinHttpRequest**](iwinhttprequest-interface.md) uses credentials.</span></span> <span data-ttu-id="93780-114">Puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="93780-114">Can be one of the following values.</span></span>



| <span data-ttu-id="93780-115">Value</span><span class="sxs-lookup"><span data-stu-id="93780-115">Value</span></span>                                                                                                               | <span data-ttu-id="93780-116">Significado</span><span class="sxs-lookup"><span data-stu-id="93780-116">Meaning</span></span>                                        |
|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="93780-117"><dt>\_SETCREDENTIALS HTTPREQUEST \_ para \_ servidor</dt></span><span class="sxs-lookup"><span data-stu-id="93780-117"><dt>HTTPREQUEST\_SETCREDENTIALS\_FOR\_SERVER</dt></span></span> </dl> | <span data-ttu-id="93780-118">Las credenciales se pasan a un servidor.</span><span class="sxs-lookup"><span data-stu-id="93780-118">Credentials are passed to a server.</span></span><br/> |
| <dl> <span data-ttu-id="93780-119"><dt>\_SETCREDENTIALS HTTPREQUEST \_ para \_ proxy</dt></span><span class="sxs-lookup"><span data-stu-id="93780-119"><dt>HTTPREQUEST\_SETCREDENTIALS\_FOR\_PROXY</dt></span></span> </dl>  | <span data-ttu-id="93780-120">Las credenciales se pasan a un proxy.</span><span class="sxs-lookup"><span data-stu-id="93780-120">Credentials are passed to a proxy.</span></span><br/>  |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93780-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="93780-121">Return value</span></span>

<span data-ttu-id="93780-122">El valor devuelto es correcto si se ejecuta correctamente o un valor de error en caso contrario. **\_**</span><span class="sxs-lookup"><span data-stu-id="93780-122">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="93780-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="93780-123">Remarks</span></span>

<span data-ttu-id="93780-124">Este método devuelve un valor de error si una llamada a [**Open**](iwinhttprequest-open.md) no se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="93780-124">This method returns an error value if a call to [**Open**](iwinhttprequest-open.md) has not completed successfully.</span></span> <span data-ttu-id="93780-125">Se supone que se debe producir cierta medida de interacción con un servidor proxy o un servidor de origen antes de que los usuarios puedan establecer credenciales para la sesión.</span><span class="sxs-lookup"><span data-stu-id="93780-125">It is assumed that some measure of interaction with a proxy server or origin server must occur before users can set credentials for the session.</span></span> <span data-ttu-id="93780-126">Además, hasta que los usuarios sepan qué esquemas de autenticación son compatibles, no pueden dar formato a las credenciales.</span><span class="sxs-lookup"><span data-stu-id="93780-126">Moreover, until users know which authentication scheme(s) are supported, they cannot format the credentials.</span></span>

> [!Note]  
> <span data-ttu-id="93780-127">En Windows XP y Windows 2000, consulte la sección [requisitos de tiempo de ejecución](winhttp-start-page.md) de la página de inicio de winhttp.</span><span class="sxs-lookup"><span data-stu-id="93780-127">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

<span data-ttu-id="93780-128">Para autenticarse tanto en el servidor como en el proxy, la aplicación debe llamar dos veces a **SetCredentials** ; en primer lugar, con el parámetro *Flags* establecido en **HttpRequest \_ SETCREDENTIALS \_ para \_ Server** y en Second, con el parámetro *Flags* establecido en **HttpRequest \_ SETCREDENTIALS \_ for \_ proxy**.</span><span class="sxs-lookup"><span data-stu-id="93780-128">To authenticate with both the server and the proxy, the application must call **SetCredentials** twice; first with the *Flags* parameter set to **HTTPREQUEST\_SETCREDENTIALS\_FOR\_SERVER**, and second, with the *Flags* parameter set to **HTTPREQUEST\_SETCREDENTIALS\_FOR\_PROXY**.</span></span>

## <a name="examples"></a><span data-ttu-id="93780-129">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="93780-129">Examples</span></span>

<span data-ttu-id="93780-130">En el ejemplo siguiente se muestra cómo abrir una conexión HTTP, establecer credenciales para el servidor, enviar una solicitud HTTP y leer el texto de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="93780-130">The following example shows how to open an HTTP connection, set credentials for the server, send an HTTP request, and read the response text.</span></span> <span data-ttu-id="93780-131">Este ejemplo debe ejecutarse desde un símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="93780-131">This example must be run from a command prompt.</span></span>


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
        BSTR bstrMethod = SysAllocString(L"GET");
        BSTR bstrUrl = SysAllocString(L"https://microsoft.com");
        hr = pIWinHttpRequest->Open(bstrMethod, bstrUrl, varFalse);
        SysFreeString(bstrMethod);
        SysFreeString(bstrUrl);
    }
    if (SUCCEEDED(hr))
    {    // Set Credentials.
        BSTR bstrUserName = SysAllocString(L"User Name");
        BSTR bstrPassword = SysAllocString(L"Password");
        hr = pIWinHttpRequest->SetCredentials(
                               bstrUserName,
                               bstrPassword,
                               HTTPREQUEST_SETCREDENTIALS_FOR_SERVER);
        SysFreeString(bstrUserName);
        SysFreeString(bstrPassword);
    }
    if (SUCCEEDED(hr))
    {    // Send Request.
        hr = pIWinHttpRequest->Send(varEmpty);
    }
    if (SUCCEEDED(hr))
    {    // Get Response text.
        hr = pIWinHttpRequest->get_ResponseText(&bstrResponse);
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



<span data-ttu-id="93780-132">En el ejemplo de scripting siguiente se muestra cómo abrir una conexión HTTP, establecer las credenciales del servidor, establecer las credenciales de un proxy si se usa uno, enviar una solicitud HTTP y leer el texto de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="93780-132">The following scripting example shows how to open an HTTP connection, set credentials for the server, set credentials for a proxy if one is used, send an HTTP request, and read the response text.</span></span>


```JScript
// HttpRequest SetCredentials flags
HTTPREQUEST_SETCREDENTIALS_FOR_SERVER = 0;
HTTPREQUEST_SETCREDENTIALS_FOR_PROXY = 1;

// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Specify the target resource.
var targURL = "https://msdn.microsoft.com/downloads/samples/"+
              "internet/winhttp/auth/authenticate.asp";    
WinHttpReq.open("GET", targURL, false);

var Done = false;
var LastStatus=0;
do {
    // Send a request to the server and wait for a response.                               
    WinHttpReq.send(); 
    
    // Obtain the status code from the response.
    var Status = WinHttpReq.Status;

    switch (Status){
        // A 200 status indicates that the resource was retrieved.
        case 200:
            Done = true;
            break;
                
        // A 401 status indicates that the server 
        // requires authentication.    
        case 401:
            WScript.Echo("Requires Server UserName and Password.");

            // Specify the target resource.
            WinHttpReq.open("GET", targURL, false);
                            
            // Set credentials for the server.
            WinHttpReq.SetCredentials("User Name", "Password", 
                        HTTPREQUEST_SETCREDENTIALS_FOR_SERVER);

            // If the same credentials are requested twice, abort 
            // the request.  For simplicity, this sample does not 
            // check for a repeated sequence of status codes.
            if (LastStatus==401)
                Done = true;
            break;

        // A 407 status indicates that the proxy 
        // requires authentication.    
        case 407:
            WScript.Echo("Requires Proxy UserName and Password.");
                
            // Specify the target resource.
            WinHttpReq.open("GET", targURL, false);
    
            // Set credentials for the proxy.
            WinHttpReq.SetCredentials("User Name", "Password", 
                HTTPREQUEST_SETCREDENTIALS_FOR_PROXY);

            // If the same credentials are requested twice, abort 
            // the request.  For simplicity, this sample does not 
            // check for a repeated sequence of status codes.
            if (LastStatus==407)
                Done = true;
            break;
        
        // Any other status is unexpected.
        default:
            WScript.Echo("Unexpected Status: "+Status);
            Done = true;
            break;
    }
    
    // Keep track of the last status code.
    LastStatus = Status;
    
} while (!Done);

// Display the results of the request.
WScript.Echo(WinHttpReq.Status + "   " + WinHttpReq.StatusText);
WScript.Echo(WinHttpReq.GetAllResponseHeaders());
```



## <a name="requirements"></a><span data-ttu-id="93780-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93780-133">Requirements</span></span>



| <span data-ttu-id="93780-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="93780-134">Requirement</span></span> | <span data-ttu-id="93780-135">Value</span><span class="sxs-lookup"><span data-stu-id="93780-135">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="93780-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="93780-136">Minimum supported client</span></span><br/> | <span data-ttu-id="93780-137">Windows XP, Windows 2000 Professional con las \[ aplicaciones de escritorio de SP3 únicamente\]</span><span class="sxs-lookup"><span data-stu-id="93780-137">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="93780-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="93780-138">Minimum supported server</span></span><br/> | <span data-ttu-id="93780-139">Windows Server 2003, Windows 2000 Server con \[ solo aplicaciones de escritorio de SP3\]</span><span class="sxs-lookup"><span data-stu-id="93780-139">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="93780-140">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="93780-140">Redistributable</span></span><br/>          | <span data-ttu-id="93780-141">WinHTTP 5,0 e Internet Explorer 5,01 o posterior en Windows XP y Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="93780-141">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="93780-142">IDL</span><span class="sxs-lookup"><span data-stu-id="93780-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="93780-143"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="93780-143"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="93780-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="93780-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="93780-145"><dt>Winhttp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="93780-145"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="93780-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="93780-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93780-147"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93780-147"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="93780-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="93780-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93780-149">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="93780-149">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="93780-150">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="93780-150">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="93780-151">Versiones de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="93780-151">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




