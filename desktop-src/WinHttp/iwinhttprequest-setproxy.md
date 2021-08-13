---
description: Establece la información del servidor proxy.
ms.assetid: 279d0557-2718-4c50-b84c-cc7c8def57a6
title: IWinHttpRequest::SetProxy (método)
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
ms.openlocfilehash: bb85466da6b7492d04bd2e69f4cd51c0c390e9595df13af8d7e6768596771822
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118562615"
---
# <a name="iwinhttprequestsetproxy-method"></a>IWinHttpRequest::SetProxy (método)

El **método SetProxy** establece la información del servidor proxy.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetProxy(
  [in]           HTTPREQUEST_PROXY_SETTING ProxySetting,
  [in, optional] VARIANT                   ProxyServer,
  [in, optional] VARIANT                   BypassList
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ProxySetting* \[ En\]
</dt> <dd>

Marcas que controlan este método. Puede ser uno de los siguientes valores.



| Value                                                                                                           | Significado                                                                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>HTTPREQUEST \_ PROXYSETTING \_ DEFAULT</dt> </dl>   | Configuración predeterminada del proxy. Equivalente a **HTTPREQUEST \_ PROXYSETTING \_ PRECONFIG**.<br/>                                                                                                                                                                                                                                                             |
| <dl> <dt>HTTPREQUEST \_ PROXYSETTING \_ PRECONFIG</dt> </dl> | Indica que la configuración del proxy debe obtenerse del registro. Esto supone [ que ](proxycfg-exe--a-proxy-configuration-tool.md)Proxycfg.exese ha ejecutado. Si Proxycfg.exe se ha ejecutado y se especifica **HTTPREQUEST \_ PROXYSETTING \_ PRECONFIG,** el comportamiento es equivalente a **HTTPREQUEST \_ PROXYSETTING \_ DIRECT**.<br/> |
| <dl> <dt>HTTPREQUEST \_ PROXYSETTING \_ DIRECT</dt> </dl>    | Indica que se debe acceder directamente a todos los servidores HTTP y HTTPS. Use este comando si no hay ningún servidor proxy.<br/>                                                                                                                                                                                                                       |
| <dl> <dt>PROXY DE \_ HTTPREQUESTSETTING \_ PROXY</dt> </dl>     | Cuando **se \_ especifica \_ HTTPREQUEST PROXYSETTING PROXY,** *varProxyServer* debe establecerse en una cadena de servidor proxy y *varBypassList* debe establecerse en una cadena de lista de omisión de dominio. Esta configuración de proxy solo se aplica a la instancia actual del [**objeto WinHttpRequest.**](winhttprequest.md)<br/>                                    |



 

</dd> <dt>

*ProxyServer* \[ en, opcional\]
</dt> <dd>

Se establece en una cadena de servidor proxy cuando *ProxySetting* es igual a **HTTPREQUEST \_ PROXYSETTING \_ PROXY**.

</dd> <dt>

*BypassList* \[ en, opcional\]
</dt> <dd>

Se establece en una cadena de lista de omisión de dominio *cuando ProxySetting* es igual a **HTTPREQUEST \_ PROXYSETTING \_ PROXY**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es **S \_ OK si se** ejecuta correctamente o un valor de error en caso contrario.

## <a name="remarks"></a>Observaciones

Permite a la aplicación que realiza la llamada especificar el uso de información de proxy predeterminada (configurada por la herramienta de configuración de proxy) o invalidar [Proxycfg.exe](proxycfg-exe--a-proxy-configuration-tool.md). Se debe llamar a este método antes de llamar al [**método**](iwinhttprequest-send.md) Send. Si se llama a este método después [**del método Send,**](iwinhttprequest-send.md) no tiene ningún efecto.

[**IWinHttpRequest**](iwinhttprequest-interface.md) pasa estos parámetros a Microsoft Windows servicios HTTP (WinHTTP).

> [!Note]  
> Para Windows XP y Windows 2000, consulte la sección [Requisitos](winhttp-start-page.md) en tiempo de ejecución de la página de inicio de WinHTTP.

 

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo establecer la configuración de proxy para un servidor proxy determinado, abrir una conexión HTTP, enviar una solicitud HTTP y leer el texto de respuesta. Este ejemplo debe ejecutarse desde un símbolo del sistema. Esta configuración de proxy solo funciona si tiene un servidor proxy denominado "servidor proxy" que usa el puerto 80 y el equipo puede omitir el servidor proxy cuando el nombre de host termina con \_ ".microsoft.com".


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



En el ejemplo de scripting siguiente se muestra cómo establecer la configuración de proxy para un servidor proxy determinado, abrir una conexión HTTP, enviar una solicitud HTTP y leer el texto de respuesta. Esta configuración de proxy solo funciona si tiene un servidor proxy denominado "servidor proxy" que usa el puerto 80 y el equipo puede omitir el servidor proxy cuando el nombre de host termina con \_ ".microsoft.com".


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



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP, Windows 2000 Professional solo con aplicaciones de escritorio SP3 \[\]<br/>            |
| Servidor mínimo compatible<br/> | Windows Server 2003, Windows 2000 Server solo con aplicaciones de escritorio SP3 \[\]<br/>         |
| Redistribuible<br/>          | WinHTTP 5.0 y Internet Explorer 5.01 o posterior en Windows XP y Windows 2000.<br/> |
| Idl<br/>                      | <dl> <dt>HttpRequest.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winhttp.lib</dt> </dl>     |
| Archivo DLL<br/>                      | <dl> <dt>Winhttp.dll</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IWinHttpRequest**](iwinhttprequest-interface.md)
</dt> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[Versiones winHTTP](winhttp-versions.md)
</dt> </dl>

 

 




