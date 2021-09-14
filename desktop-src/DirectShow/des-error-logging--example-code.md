---
description: 'Registro de errores DES: código de ejemplo'
ms.assetid: e734daed-9230-4376-839f-7e09da7bc275
title: 'Registro de errores DES: código de ejemplo'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a9e0d47535e1d4035669a0e672a30fb2520c676
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061228"
---
# <a name="des-error-logging-example-code"></a>Registro de errores DES: código de ejemplo

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

El código de ejemplo siguiente presenta una aplicación de consola completa que carga y muestra una vista previa de un archivo de proyecto XML de [DirectShow Editing Services,](directshow-editing-services.md) mediante la clase de registro de errores descrita en esta sección. (Vea [Errores de registro).](logging-errors.md) El nombre del archivo de proyecto está codificado de forma hard-code en la aplicación.

Para que el código sea más corto, la aplicación de consola usa punteros inteligentes ATL, lo que elimina la necesidad de llamar a **QueryInterface** y **Release.** Si lo prefiere, puede modificar la aplicación de ejemplo en [Carga y vista previa de un Project](loading-and-previewing-a-project.md). Simplemente agregue el código que se muestra en la sección anterior.


```C++
#include <atlbase.h>
#include <dshow.h>
#include <qedit.h>
#include <stdio.h>

// Declare error logging class.
class CErrReporter;

// (The implementation of CErrReporter was given previously.)

void __cdecl main(void)
{
    HRESULT hr = CoInitialize(NULL);

    if (FAILED(hr))
    {
        // Error handling is omitted for clarity.
    }

    { // Scope for smart pointers.

    CComPtr<IAMTimeline>   pTL;
    CComPtr<IRenderEngine> pRenderEngine; 
    CComPtr<IXml2Dex>      pXML; 
    CComPtr<IGraphBuilder> pGraph;

    hr = CoCreateInstance(CLSID_AMTimeline, NULL, CLSCTX_INPROC_SERVER, 
                IID_IAMTimeline, (void**) &pTL);
    hr = CoCreateInstance(CLSID_Xml2Dex, NULL, CLSCTX_INPROC_SERVER, 
                IID_IXml2Dex, (void**) &pXML);
    hr = CoCreateInstance(CLSID_RenderEngine, NULL, CLSCTX_INPROC_SERVER,
                IID_IRenderEngine, (void**) &pRenderEngine);

    // Set the error log.
    CComQIPtr<IAMSetErrorLog, &IID_IAMSetErrorLog> pSetLog(pTL);
    if (pSetLog)
    {
        IAMErrorLog *pLog = new CErrReporter;    
        pSetLog->put_ErrorLog(pLog);
    }
   
    // Load and preview the project.
    CComBSTR bstrFile(OLESTR("C:\\example.xtl"));
    hr = pXML->ReadXMLFile(pTL, bstrFile); 
    if (SUCCEEDED(hr))
    {
        hr = pRenderEngine->SetTimelineObject(pTL);
        hr = pRenderEngine->ConnectFrontEnd( );
        hr = pRenderEngine->RenderOutputPins( );
        hr = pRenderEngine->GetFilterGraph(&pGraph);

        CComQIPtr<IMediaControl, &IID_IMediaControl> pControl(pGraph);
        CComQIPtr<IMediaEvent, &IID_IMediaEvent> pEvent(pGraph);
        pControl->Run();

        long evCode;
        hr = pEvent->WaitForCompletion(INFINITE, &evCode);
        pControl->Stop();
    }
    // Clean up.
    pRenderEngine->ScrapIt();
    }
    CoUninitialize();
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Errores de registro](logging-errors.md)
</dt> </dl>

 

 



