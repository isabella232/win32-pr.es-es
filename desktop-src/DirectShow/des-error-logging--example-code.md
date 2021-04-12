---
description: 'Registro de errores DES: código de ejemplo'
ms.assetid: e734daed-9230-4376-839f-7e09da7bc275
title: 'Registro de errores DES: código de ejemplo'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a9e0d47535e1d4035669a0e672a30fb2520c676
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104538236"
---
# <a name="des-error-logging-example-code"></a><span data-ttu-id="dacc0-103">Registro de errores DES: código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="dacc0-103">DES Error Logging: Example Code</span></span>

<span data-ttu-id="dacc0-104">\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]</span><span class="sxs-lookup"><span data-stu-id="dacc0-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="dacc0-105">En el código de ejemplo siguiente se muestra una aplicación de consola completa que carga y muestra una vista previa de un archivo de proyecto XML de [servicios de edición de DirectShow](directshow-editing-services.md) , mediante la clase de registro de errores que se describe en esta sección.</span><span class="sxs-lookup"><span data-stu-id="dacc0-105">The following sample code presents a complete console application that loads and previews a [DirectShow Editing Services](directshow-editing-services.md) XML project file, using the error logging class described in this section.</span></span> <span data-ttu-id="dacc0-106">(Consulte [errores de registro](logging-errors.md)). El nombre del archivo de proyecto está codificado de forma rígida en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="dacc0-106">(See [Logging Errors](logging-errors.md).) The name of the project file is hard-coded into the application.</span></span>

<span data-ttu-id="dacc0-107">Para que el código sea más corto, la aplicación de consola utiliza punteros inteligentes ATL, lo que elimina la necesidad de llamar a **QueryInterface** y **Release**.</span><span class="sxs-lookup"><span data-stu-id="dacc0-107">To make the code shorter, the console application uses ATL smart pointers, which removes the need to call **QueryInterface** and **Release**.</span></span> <span data-ttu-id="dacc0-108">Si lo prefiere, puede modificar la aplicación de ejemplo en [cargar y obtener una vista previa de un proyecto](loading-and-previewing-a-project.md).</span><span class="sxs-lookup"><span data-stu-id="dacc0-108">If you prefer, you can modify the sample application in [Loading and Previewing a Project](loading-and-previewing-a-project.md).</span></span> <span data-ttu-id="dacc0-109">Simplemente agregue el código que se muestra en la sección anterior.</span><span class="sxs-lookup"><span data-stu-id="dacc0-109">Simply add the code shown in the previous section.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="dacc0-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dacc0-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dacc0-111">Errores de registro</span><span class="sxs-lookup"><span data-stu-id="dacc0-111">Logging Errors</span></span>](logging-errors.md)
</dt> </dl>

 

 



