---
description: El método SetTimeouts especifica los componentes de tiempo de espera individuales de una operación de envío/recepción, en milisegundos.
ms.assetid: c2b6c432-5f3b-4361-8026-1b843c6697ae
title: IWinHttpRequest::SetTimeouts (método)
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
ms.openlocfilehash: e31fbe80f106735a43126b2be5181478b932e2f813b207984959cf013d3fd752
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118562461"
---
# <a name="iwinhttprequestsettimeouts-method"></a>IWinHttpRequest::SetTimeouts (método)

El **método SetTimeouts** especifica los componentes de tiempo de espera individuales de una operación de envío/recepción, en milisegundos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetTimeouts(
  [in] long ResolveTimeout,
  [in] long ConnectTimeout,
  [in] long SendTimeout,
  [in] long ReceiveTimeout
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ResolveTimeout* \[ En\]
</dt> <dd>

Valor de tiempo de espera aplicado al resolver un nombre de host (como ) en una dirección `www.microsoft.com` IP (por ejemplo, 192.168.131.199), en milisegundos. El valor predeterminado es cero, lo que significa que no hay tiempo de espera (infinito). Si se especifica el tiempo de espera de DNS mediante NAME \_ RESOLUTION \_ TIMEOUT, hay una sobrecarga de un subproceso por solicitud.

</dd> <dt>

*ConnectTimeout* \[ En\]
</dt> <dd>

Valor de tiempo de espera aplicado al establecer un socket de comunicación con el servidor de destino, en milisegundos. El valor predeterminado es 60 000 (60 segundos).

</dd> <dt>

*SendTimeout* \[ En\]
</dt> <dd>

Valor de tiempo de espera aplicado al enviar un paquete individual de datos de solicitud en el socket de comunicación al servidor de destino, en milisegundos. Normalmente, una solicitud grande enviada a un servidor HTTP se divide en varios paquetes. el tiempo de espera de envío se aplica al envío individual de cada paquete. El valor predeterminado es 30 000 (30 segundos).

</dd> <dt>

*ReceiveTimeout* \[ En\]
</dt> <dd>

Valor de tiempo de espera aplicado al recibir un paquete de datos de respuesta del servidor de destino, en milisegundos. Las respuestas grandes se divide en varios paquetes; el tiempo de espera de recepción se aplica a la captura de cada paquete de datos del socket. El valor predeterminado es 30 000 (30 segundos).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es **S \_ OK on** success o un valor de error en caso contrario.

## <a name="remarks"></a>Observaciones

Todos los parámetros son obligatorios. Un valor de 0 o -1 establece un tiempo de espera para esperar infinitamente. Un valor mayor que 0 establece el valor de tiempo de espera en milisegundos. Por ejemplo, 30 000 establecería el tiempo de espera en 30 segundos. Todos los valores negativos distintos de -1 hacen que este método no se pueda usar.

Los valores de tiempo de espera se aplican en la capa winsock.

> [!Note]  
> Para Windows XP y Windows 2000, consulte la sección [Requisitos](winhttp-start-page.md) en tiempo de ejecución de la página de inicio de WinHttp.

 

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo establecer todos los tiempos de espera de WinHTTP en 30 segundos, abrir una conexión HTTP, enviar una solicitud HTTP y leer el texto de respuesta.


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



En el ejemplo de scripting siguiente se muestra cómo establecer todos los tiempos de espera de WinHTTP en 30 segundos, abrir una conexión HTTP y enviar una solicitud HTTP.


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



## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

 

 




