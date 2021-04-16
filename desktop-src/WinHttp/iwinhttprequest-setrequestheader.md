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
# <a name="iwinhttprequestsetrequestheader-method"></a>IWinHttpRequest:: SetRequestHeader (método)

El método **SetRequestHeader** agrega, cambia o elimina un encabezado de solicitud HTTP.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetRequestHeader(
  [in] BSTR Header,
  [in] BSTR Value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Encabezado* \[ de de\]
</dt> <dd>

Especifica el nombre del encabezado que se va a establecer, por ejemplo, "depth". Este parámetro no debe contener un signo de dos puntos y debe ser el texto real del encabezado HTTP.

</dd> <dt>

*Valor* \[ de de\]
</dt> <dd>

Especifica el valor del encabezado, por ejemplo, "Infinity".

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es correcto si se ejecuta correctamente o un valor de error en caso contrario. **\_**

## <a name="remarks"></a>Observaciones

Los encabezados se transfieren a través de las redirecciones. Esto puede crear una vulnerabilidad de seguridad. Para evitar que se transfieran los encabezados si se produce una redirección, utilice la devolución de llamada de [*\_ devolución de \_ llamada de estado de WinHTTP*](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) para corregir los encabezados específicos cuando se produce una redirección.

El método **SetRequestHeader** permite que la aplicación que realiza la llamada agregue o elimine un encabezado de solicitud HTTP antes de enviar la solicitud. El nombre del encabezado se proporciona en el *encabezado* y el token o el valor del encabezado se especifican en el *valor*. Para agregar un encabezado, proporcione un nombre y un valor de encabezado. Si ya existe otro encabezado con este nombre, se reemplazará. Para eliminar un encabezado, establezca *encabezado* en el nombre del encabezado que se va a eliminar y establezca *valor* en **null**.

Se validan el nombre y el valor de los encabezados de solicitud agregados con este método. Los encabezados deben tener el formato correcto. Para obtener más información acerca de los encabezados HTTP válidos, vea [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt). Si se usa un encabezado no válido, se produce un error y no se agrega el encabezado.

> [!Note]  
> En Windows XP y Windows 2000, consulte la sección [requisitos de tiempo de ejecución](winhttp-start-page.md) de la página de inicio de winhttp.

 

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo abrir una conexión HTTP, establecer un encabezado de solicitud, enviar una solicitud HTTP y leer el texto de la respuesta. Este ejemplo debe ejecutarse desde un símbolo del sistema.


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



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP, Windows 2000 Professional con las \[ aplicaciones de escritorio de SP3 únicamente\]<br/>            |
| Servidor mínimo compatible<br/> | Windows Server 2003, Windows 2000 Server con \[ solo aplicaciones de escritorio de SP3\]<br/>         |
| Redistribuible<br/>          | WinHTTP 5,0 e Internet Explorer 5,01 o posterior en Windows XP y Windows 2000.<br/> |
| IDL<br/>                      | <dl> <dt>HttpRequest. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winhttp. lib</dt> </dl>     |
| Archivo DLL<br/>                      | <dl> <dt>Winhttp.dll</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IWinHttpRequest**](iwinhttprequest-interface.md)
</dt> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[Versiones de WinHTTP](winhttp-versions.md)
</dt> </dl>

 

