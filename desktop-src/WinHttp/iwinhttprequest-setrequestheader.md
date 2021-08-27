---
description: Agrega, cambia o elimina un encabezado de solicitud HTTP.
ms.assetid: 8cb4891d-0bdb-4dea-8ebe-d6ed26a50e41
title: IWinHttpRequest::SetRequestHeader (método)
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
ms.openlocfilehash: 1f6db5ef09a0eca56fec8101d710c62eb5165742d47e3961593f38d4a59851ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052033"
---
# <a name="iwinhttprequestsetrequestheader-method"></a>IWinHttpRequest::SetRequestHeader (método)

El **método SetRequestHeader** agrega, cambia o elimina un encabezado de solicitud HTTP.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetRequestHeader(
  [in] BSTR Header,
  [in] BSTR Value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Encabezado* \[ En\]
</dt> <dd>

Especifica el nombre del encabezado que se va a establecer, por ejemplo, "depth". Este parámetro no debe contener dos puntos y debe ser el texto real del encabezado HTTP.

</dd> <dt>

*Valor* \[ En\]
</dt> <dd>

Especifica el valor del encabezado, por ejemplo, "infinito".

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es **S \_ OK on** success o un valor de error en caso contrario.

## <a name="remarks"></a>Comentarios

Los encabezados se transfieren entre redireccionamientos. Esto puede crear una vulnerabilidad de seguridad. Para evitar que se transfieran encabezados si se produce una redirección, use la devolución de llamada [*\_ \_ CALLBACK DE ESTADO WINHTTP*](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) para corregir los encabezados específicos cuando se produce una redirección.

El **método SetRequestHeader** permite que la aplicación que realiza la llamada agregue o elimine un encabezado de solicitud HTTP antes de enviar la solicitud. El nombre del encabezado se da en *Encabezado* y el token de encabezado o el valor se da en *Valor*. Para agregar un encabezado, proporcione un nombre de encabezado y un valor. Si ya existe otro encabezado con este nombre, se reemplaza. Para eliminar un encabezado, establezca *Encabezado* en el nombre del encabezado que se eliminará y *establezca Valor* en **NULL.**

Se validan el nombre y el valor de los encabezados de solicitud agregados con este método. Los encabezados deben tener un formato correcto. Para obtener más información sobre los encabezados HTTP válidos, [vea RFC 2616](https://www.ietf.org/rfc/rfc2616.txt). Si se usa un encabezado no válido, se produce un error y no se agrega el encabezado.

> [!Note]  
> Para Windows XP y Windows 2000, consulte la sección [Requisitos](winhttp-start-page.md) en tiempo de ejecución de la página de inicio de WinHTTP.

 

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo abrir una conexión HTTP, establecer un encabezado de solicitud, enviar una solicitud HTTP y leer el texto de respuesta. Este ejemplo debe ejecutarse desde un símbolo del sistema.


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



En el ejemplo de scripting siguiente se muestra cómo abrir una conexión HTTP, establecer un encabezado de solicitud y enviar una solicitud HTTP.


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



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP, Windows 2000 Professional solo con aplicaciones de escritorio sp3 \[\]<br/>            |
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

[Versiones de WinHTTP](winhttp-versions.md)
</dt> </dl>

 

