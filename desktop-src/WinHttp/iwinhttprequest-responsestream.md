---
description: Recupera el cuerpo de la entidad de respuesta como IStream.
ms.assetid: e12a9338-5e0c-4672-bbc6-31375b872e94
title: Propiedad IWinHttpRequest::ResponseStream
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.ResponseStream
- IWinHttpRequest.get_ResponseStream
- WinHttpRequest.ResponseStream
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: f29fad2ccfcac5cbca1c6ef13e0aeef5bdd0f4764e81dd14cabdfa58fd30fbde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118563223"
---
# <a name="iwinhttprequestresponsestream-property"></a>Propiedad IWinHttpRequest::ResponseStream

La **propiedad ResponseStream** recupera el cuerpo de la entidad de respuesta como [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_ResponseStream(
  [out, retval] VARIANT *Body
);
```


```JScript

vtResponseStream = WinHttpRequest.ResponseStream
```





## <a name="property-value"></a>Valor de propiedad

Variante **que** recibe un puntero a una [**interfaz IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) que se puede consultar para una [**interfaz IStream.**](/windows/desktop/api/objidl/nn-objidl-istream) Esta secuencia devuelve los datos sin procesar tal como se reciben directamente desde el servidor.

## <a name="error-codes"></a>Códigos de error

El valor devuelto es **S \_ OK on** success o un valor de error en caso contrario.

Será E **\_ PENDING si** la operación [**de envío**](iwinhttprequest-send.md) anterior no se ha completado.

## <a name="remarks"></a>Comentarios

Llame [**a QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en el puntero devuelto para obtener un puntero a una [**interfaz IStream.**](/windows/desktop/api/objidl/nn-objidl-istream) Esta propiedad devuelve los datos de respuesta como **IStream**. Esta propiedad solo se puede invocar después de llamar [**al**](iwinhttprequest-send.md) método Send.

> [!Note]  
> Para Windows XP y Windows 2000, consulte la sección [Requisitos](winhttp-start-page.md) en tiempo de ejecución de la página de inicio de WinHTTP.

 

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo abrir una conexión HTTP, enviar una solicitud HTTP y leer la respuesta como [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream). Los datos de **IStream se** escriben en el archivo Temp1.gif.


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

#define Trace(_s) fprintf(stderr, _s) 
#define TraceErr(_s, _hr) fprintf(stderr, _s, _hr) 
#define Check(_hr,_s) if (FAILED(_hr)) { fprintf(stderr, _s ## " 0x%08lx\n", _hr); return -1; }

int main(int argc, char* argv[])
{
    UNREFERENCED_PARAMETER(argc);
    UNREFERENCED_PARAMETER(argv);
    
    // Variable for return value.
    HRESULT    hr;

    // Initialize COM.
    hr = CoInitialize( NULL );

    IWinHttpRequest *  pIWinHttpRequest = NULL;

    BSTR            bstrResponse = NULL;
    VARIANT         varFalse;
    VARIANT         varEmpty;
    VARIANT            varResponse;

    VariantInit(&varResponse);
    
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

    // ==== Get binary (.gif) file and write it to disk. =========
    if (SUCCEEDED(hr))
    {    // Open WinHttpRequest for synchronous access.
        BSTR bstrMethod = SysAllocString(L"GET");
        BSTR bstrUrl = SysAllocString(
            L"https://www.microsoft.com/library/homepage/images/ms-banner.gif");
        hr = pIWinHttpRequest->Open(bstrMethod, bstrUrl, varFalse);
        SysFreeString(bstrMethod);
        SysFreeString(bstrUrl);
    }
    if (SUCCEEDED(hr))
    {    // Send Request.
        hr = pIWinHttpRequest->Send(varEmpty);
    }
    if (SUCCEEDED(hr))
    {    // Get response body.
        hr = pIWinHttpRequest->get_ResponseBody(&varResponse);
    }
    if (SUCCEEDED(hr))
    {    // Print response to file temp1.gif.
        long UpperBounds;
        long LowerBounds;
        unsigned char* buff;
        // Verify that varResponse contains array of unsigned bytes.
        if (varResponse.vt == (VT_ARRAY | VT_UI1)) {
            long Dims = SafeArrayGetDim(varResponse.parray);
            // The array should only have 1 dimension.
            if (Dims == 1) {
                // Get upper and lower array bounds.
                SafeArrayGetLBound(varResponse.parray, 1, 
                                   &LowerBounds);
                SafeArrayGetUBound(varResponse.parray, 1, 
                                   &UpperBounds);
                UpperBounds++;
                // Lock SAFEARRAY for access.
                SafeArrayAccessData (varResponse.parray, 
                                     (void**)&buff);
                // Output array to file temp.gif.
                HANDLE hFile; 
                DWORD  dwBytesWritten;
                // Create file.
                hFile = CreateFile(TEXT("Temp1.gif"),     
                    GENERIC_WRITE,              // Open for writing. 
                    0,                          // Do not share. 
                    NULL,                       // No security. 
                    CREATE_ALWAYS,              // Overwrite existing.
                    FILE_ATTRIBUTE_NORMAL,      // Normal file.
                    NULL);                      // No attribute template.

                if (hFile == INVALID_HANDLE_VALUE) 
                    {
                    wprintf(L"Could not open file."); // Process error.
                    }
                else
                    {
                    WriteFile(hFile, buff, UpperBounds - LowerBounds, 
                        &dwBytesWritten, NULL); 
                    }
                CloseHandle(hFile);
                SafeArrayUnaccessData (varResponse.parray);
            }
        }    
    }

    // ======== Get binary (.gif) file and write 
    // it to disk using IStream. ================
    if (SUCCEEDED(hr))
    {    // Open WinHttpRequest for synchronous access.
        BSTR bstrMethod = SysAllocString(L"GET");
        BSTR bstrUrl = SysAllocString(
            L"https://www.microsoft.com/library/homepage/images/ms-banner.gif");
        hr = pIWinHttpRequest->Open(bstrMethod, bstrUrl, varFalse);
        SysFreeString(bstrMethod);
        SysFreeString(bstrUrl);
    }
    if (SUCCEEDED(hr))
    {    // Send Request.
        hr = pIWinHttpRequest->Send(varEmpty);
    }
    if (SUCCEEDED(hr))
    {    // Get Response as an IStream.
        hr = pIWinHttpRequest->get_ResponseStream(&varResponse);
    }
    if (SUCCEEDED(hr))
    {    // Print response to file temp1.gif.
        IStream*    pStream = NULL; 
        BYTE        bBuffer[8192]; 
        DWORD       cb, cbRead, cbWritten; 
        // Check that an IStream was received.
        if (VT_UNKNOWN == V_VT(&varResponse) || 
            VT_STREAM == V_VT(&varResponse)) 
        { 
            // Get IStream interface pStream.
            hr = V_UNKNOWN(&varResponse)->QueryInterface(IID_IStream, 
                                 reinterpret_cast<void**>(&pStream)); 
            Check(hr, "QI for IStream"); 
        } 
        else 
        { 
            wprintf(L"Unexpected vartype for Response\n"); 
            return -1; 
        } 

        HANDLE hFile; 
        // Open file Temp2.gif for output.
        hFile = CreateFile(TEXT("Temp2.gif"),     
            GENERIC_WRITE,                // Open for writing. 
            0,                            // Do not share. 
            NULL,                         // No security. 
            CREATE_ALWAYS,                // Overwrite existing.
            FILE_ATTRIBUTE_NORMAL,        // Normal file.
            NULL);                        // No attribute template.
        if (hFile == INVALID_HANDLE_VALUE) 
            {
            wprintf(L"Could not open file.");  // Process error.
            }
        else
            {
            // Copy data from the response stream to file. 
            cb = sizeof(bBuffer); 
            hr = pStream->Read(bBuffer, cb, &cbRead); 
            while (SUCCEEDED(hr) && 0 != cbRead) 
                { 
                if (!WriteFile(hFile, bBuffer, 
                               cbRead, &cbWritten, NULL)) 
                    { 
                    TraceErr("WriteFile fails with 0x%08lx\n", 
                             HRESULT_FROM_WIN32(GetLastError())); 
                    return -1; 
                    } 
                hr = pStream->Read(bBuffer, cb, &cbRead); 
                } 
            }
        CloseHandle(hFile);
        pStream->Release(); 
        VariantClear(&varResponse); 
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



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP, Windows 2000 Professional solo con aplicaciones de escritorio sp3 \[\]<br/>            |
| Servidor mínimo compatible<br/> | Windows Server 2003, Windows 2000 Server solo con aplicaciones de escritorio SP3 \[\]<br/>         |
| Redistribuible<br/>          | WinHTTP 5.0 y Internet Explorer 5.01 o posterior en Windows XP y Windows 2000.<br/> |
| Idl<br/>                      | <dl> <dt>HttpRequest.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winhttp.lib</dt> </dl>     |
| Archivo DLL<br/>                      | <dl> <dt>Winhttp.dll</dt> </dl>     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IWinHttpRequest**](iwinhttprequest-interface.md)
</dt> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[**ResponseBody**](iwinhttprequest-responsebody.md)
</dt> <dt>

[**ResponseText**](iwinhttprequest-responsetext.md)
</dt> <dt>

[Versiones de WinHTTP](winhttp-versions.md)
</dt> </dl>

 

