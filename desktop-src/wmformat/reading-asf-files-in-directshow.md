---
title: Leer archivos ASF en DirectShow (Windows Media Format 11 SDK)
description: Leer archivos ASF en DirectShow
ms.assetid: eec2c91f-1762-4798-91d0-d68ec2160d6a
keywords:
- Windows Media Format SDK, DirectShow
- SDK de Windows Media Format, leer archivos ASF
- Windows Media Format SDK, filtro de lector ASF de WM
- SDK de Windows Media Format, interfaz IMediaSeeking
- Advanced Systems Format (ASF), DirectShow
- ASF (formato de sistemas avanzados), DirectShow
- Advanced Systems Format (ASF), leer archivos
- ASF (formato de sistemas avanzados), lectura de archivos
- Advanced Systems Format (ASF), filtro de lector ASF de WM
- ASF (formato de sistemas avanzados), filtro de lector ASF de WM
- Advanced Systems Format (ASF), IMediaSeeking (interfaz)
- ASF (formato de sistemas avanzados), interfaz IMediaSeeking
- DirectShow, leer archivos ASF
- DirectShow, filtro de lector ASF de WM
- DirectShow, interfaz IMediaSeeking
- Filtro de lector ASF de WM
- IMediaSeeking
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1ddf7ba34444f4a3b46f4413958bd26ba4bafc8
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104359627"
---
# <a name="reading-asf-files-in-directshow-windows-media-format-11-sdk"></a><span data-ttu-id="f1746-120">Leer archivos ASF en DirectShow (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="f1746-120">Reading ASF Files in DirectShow (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="f1746-121">La reproducción de archivos ASF se controla mediante el filtro [lector ASF de WM](wm-asf-reader-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="f1746-121">Playback of ASF files is handled by the [WM ASF Reader](wm-asf-reader-filter.md) filter.</span></span> <span data-ttu-id="f1746-122">Cuando el lector ASF de WM lee un archivo, crea automáticamente un PIN de salida para cada flujo, incluidas las secuencias Web, secuencias de comandos de script y cualquier otro tipo de secuencia arbitraria.</span><span class="sxs-lookup"><span data-stu-id="f1746-122">When the WM ASF Reader reads a file, it automatically creates an output pin for each stream, including Web streams, script command streams, and any other type of arbitrary stream.</span></span> <span data-ttu-id="f1746-123">En el caso de varios archivos de velocidad de bits, los pin solo se crean para las secuencias seleccionadas actualmente.</span><span class="sxs-lookup"><span data-stu-id="f1746-123">In the case of multiple bit rate files, pins are created only for the currently selected streams.</span></span>

<span data-ttu-id="f1746-124">El lector ASF de WM admite la interfaz **IMediaSeeking** de DirectShow, que permite a las aplicaciones realizar búsquedas temporales en el archivo.</span><span class="sxs-lookup"><span data-stu-id="f1746-124">The WM ASF Reader supports the DirectShow **IMediaSeeking** interface, which enables applications to perform temporal seeking within the file.</span></span> <span data-ttu-id="f1746-125">Sin embargo, no se admite la reproducción a velocidades distintas de 1,0 (tal y como se especifica en **IMediaSeeking:: SetRate**).</span><span class="sxs-lookup"><span data-stu-id="f1746-125">However, playback at speeds other than 1.0 (as specified in **IMediaSeeking::SetRate**) is not supported.</span></span>

<span data-ttu-id="f1746-126">El filtro también expone varias interfaces del SDK de Windows Media Format, como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="f1746-126">The filter also exposes several Windows Media Format SDK interfaces as described in the following table.</span></span>



| <span data-ttu-id="f1746-127">Interfaz</span><span class="sxs-lookup"><span data-stu-id="f1746-127">Interface</span></span>                                        | <span data-ttu-id="f1746-128">Cómo se exponen</span><span class="sxs-lookup"><span data-stu-id="f1746-128">How exposed</span></span>                            | <span data-ttu-id="f1746-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f1746-129">Comments</span></span>                                                                                                                                                                                    |
|--------------------------------------------------|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f1746-130">**IWMDRMReader**</span><span class="sxs-lookup"><span data-stu-id="f1746-130">**IWMDRMReader**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)             | <span data-ttu-id="f1746-131">A través de **IServiceProvider** en filtro</span><span class="sxs-lookup"><span data-stu-id="f1746-131">Through **IServiceProvider** on filter</span></span> | <span data-ttu-id="f1746-132">Se proporciona para las aplicaciones que necesitan reproducir contenido protegido por Rights Management digitales (DRM).</span><span class="sxs-lookup"><span data-stu-id="f1746-132">Provided for applications that need to play content protected by Digital Rights Management (DRM).</span></span> <span data-ttu-id="f1746-133">Esta interfaz también se puede usar para obtener otras interfaces en el objeto de lector directamente.</span><span class="sxs-lookup"><span data-stu-id="f1746-133">This interface can also be used to obtain other interfaces on the Reader Object directly.</span></span> |
| [<span data-ttu-id="f1746-134">**IWMHeaderInfo**</span><span class="sxs-lookup"><span data-stu-id="f1746-134">**IWMHeaderInfo**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)           | <span data-ttu-id="f1746-135">**QueryInterface** en filtro</span><span class="sxs-lookup"><span data-stu-id="f1746-135">**QueryInterface** on filter</span></span>           | <span data-ttu-id="f1746-136">Proporcionado para que las aplicaciones puedan leer atributos de archivo y de contenido, así como información de marcadores y metadatos.</span><span class="sxs-lookup"><span data-stu-id="f1746-136">Provided so that applications can read file and content attributes, as well as marker and script information and metadata.</span></span>                                                                  |
| [<span data-ttu-id="f1746-137">**IWMReaderAdvanced**</span><span class="sxs-lookup"><span data-stu-id="f1746-137">**IWMReaderAdvanced**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)   | <span data-ttu-id="f1746-138">**QueryInterface** en filtro</span><span class="sxs-lookup"><span data-stu-id="f1746-138">**QueryInterface** on filter</span></span>           | <span data-ttu-id="f1746-139">Implementado parcialmente en el filtro para que las aplicaciones puedan tener acceso a los métodos informativos del objeto lector de WM.</span><span class="sxs-lookup"><span data-stu-id="f1746-139">Partially implemented on the filter so that applications can access the informational methods on the WM Reader object.</span></span>                                                                      |
| [<span data-ttu-id="f1746-140">**IWMReaderAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="f1746-140">**IWMReaderAdvanced2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) | <span data-ttu-id="f1746-141">**QueryInterface** en filtro</span><span class="sxs-lookup"><span data-stu-id="f1746-141">**QueryInterface** on filter</span></span>           | <span data-ttu-id="f1746-142">Implementado parcialmente en el filtro para que las aplicaciones puedan tener acceso a los métodos informativos del objeto lector.</span><span class="sxs-lookup"><span data-stu-id="f1746-142">Partially implemented on the filter so that applications can access the informational methods on the Reader Object.</span></span>                                                                         |



 

<span data-ttu-id="f1746-143">El filtro [lector ASF de WM](wm-asf-reader-filter.md) estaba disponible por primera vez en DirectShow 8,0.</span><span class="sxs-lookup"><span data-stu-id="f1746-143">The [WM ASF Reader](wm-asf-reader-filter.md) filter was first made available in DirectShow 8.0.</span></span> <span data-ttu-id="f1746-144">La versión del filtro que se incluye con DirectShow 8,1 y 9,0 admite la versión 7. *x* del SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="f1746-144">The version of the filter that ships with DirectShow 8.1 and 9.0 supports version 7.*x* of the Windows Media Format SDK.</span></span> <span data-ttu-id="f1746-145">La versión más reciente del filtro, junto con los demás componentes de QASF, se suministra con y es compatible con el SDK de Windows Media Format 9 series y versiones posteriores, y reemplaza el filtro en DirectX 9,0.</span><span class="sxs-lookup"><span data-stu-id="f1746-145">The most recent version of the filter, along with the other QASF components, ships with and supports the Windows Media Format 9 Series SDK, and later versions, and it supersedes the filter in DirectX 9.0.</span></span> <span data-ttu-id="f1746-146">Si instala el SDK de Windows Media Format después de instalar DirectX 8. *x* o 9. *x* SDK, sobrescribirá la versión de DirectX de qasf.dll con la versión de la serie 9.</span><span class="sxs-lookup"><span data-stu-id="f1746-146">If you install the Windows Media Format SDK after installing the DirectX 8.*x* or 9.*x* SDK, you will overwrite the DirectX version of qasf.dll with the 9 Series version.</span></span> <span data-ttu-id="f1746-147">Esto no debería presentar ningún problema, excepto posiblemente en un escenario en el que se producirá un comportamiento diferente en el método DirectShow **IGraphBuilder:: RenderFile** .</span><span class="sxs-lookup"><span data-stu-id="f1746-147">This should not present any problems except possibly in one scenario where it will result in different behavior in the DirectShow **IGraphBuilder::RenderFile** method.</span></span> <span data-ttu-id="f1746-148">La versión del SDK de Windows Media Format 9 series del lector ASF de WM es el filtro de origen predeterminado para las extensiones de nombre de archivo. ASF,. WMV y. WMA.</span><span class="sxs-lookup"><span data-stu-id="f1746-148">The Windows Media Format 9 Series SDK version of the WM ASF Reader is the default source filter for the .asf, .wmv, and .wma file name extensions.</span></span> <span data-ttu-id="f1746-149">Esto significa que el lector ASF de WM se crea y agrega automáticamente al gráfico de filtro mediante el administrador de gráficos de filtro en métodos como **IGraphBuilder:: RenderFile** o **IGraphBuilder:: AddSourceFilter** cuando se especifica un archivo de este tipo.</span><span class="sxs-lookup"><span data-stu-id="f1746-149">This means that the WM ASF Reader is automatically created and added to the filter graph by the Filter Graph Manager in methods such as **IGraphBuilder::RenderFile** or **IGraphBuilder::AddSourceFilter** when a file of this type is specified.</span></span> <span data-ttu-id="f1746-150">En DirectX 9,0 y versiones anteriores, y Windows XP Service Pack 1 y versiones anteriores, el método **RenderFile** usa el filtro de origen de Windows Media anterior.</span><span class="sxs-lookup"><span data-stu-id="f1746-150">In DirectX 9.0 and earlier, and Windows XP Service Pack 1 and earlier, the **RenderFile** method uses the older Windows Media Source Filter.</span></span> <span data-ttu-id="f1746-151">Este comportamiento se mantuvo para garantizar la compatibilidad con versiones anteriores de las aplicaciones que usaban Windows Media Player 6,4.</span><span class="sxs-lookup"><span data-stu-id="f1746-151">This behavior was maintained to ensure backward compatibility with applications that used the Windows Media Player 6.4.</span></span> <span data-ttu-id="f1746-152">Para obtener más información sobre el filtro de origen de medios de Windows heredado, vea la documentación del SDK de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="f1746-152">For more information about the legacy Windows Media Source Filter, see the DirectShow SDK Documentation.</span></span>

<span data-ttu-id="f1746-153">Para reproducir un archivo ASF con contenido basado en Windows Media mediante el lector ASF de WM, los tres pasos principales son crear una instancia del administrador de gráficos de filtros, llamar a **IGraphBuilder:: RenderFile** para crear el gráfico y, a continuación, llamar a **IMediaControl:: Run** para reproducir el archivo.</span><span class="sxs-lookup"><span data-stu-id="f1746-153">To play an ASF file with Windows Media–based content using the WM ASF Reader, the three primary steps are to create an instance of the Filter Graph Manager, call **IGraphBuilder::RenderFile** to create the graph, and then call **IMediaControl::Run** to play the file.</span></span> <span data-ttu-id="f1746-154">El siguiente ejemplo de código es un programa completo que reproduce un archivo ASF mediante DirectShow.</span><span class="sxs-lookup"><span data-stu-id="f1746-154">The following code example is a complete program that plays an ASF file using DirectShow.</span></span> <span data-ttu-id="f1746-155">Para ejecutar este ejemplo, debe tener instalado el SDK de DirectX y el entorno de compilación debe configurarse de acuerdo con las instrucciones del tema de la documentación del SDK de DirectShow sobre cómo configurar el entorno de compilación.</span><span class="sxs-lookup"><span data-stu-id="f1746-155">To run this example, you must have the DirectX SDK installed and your build environment must be configured according to the instructions in the DirectShow SDK documentation topic "Setting Up the Build Environment."</span></span> <span data-ttu-id="f1746-156">Además, debe especificar un archivo en el equipo en la llamada a **RenderFile**.</span><span class="sxs-lookup"><span data-stu-id="f1746-156">Also, you must specify a file on your computer in the call to **RenderFile**.</span></span>


```C++
#include <dshow.h>
#include <stdio.h>

void main(void)
{
    IGraphBuilder *pGraph = NULL;
    IMediaControl *pControl = NULL;
    IMediaEvent   *pEvent = NULL;

    // Initialize the COM library.
    HRESULT hr = CoInitialize(NULL);
    if (FAILED(hr))
    {
        printf("ERROR - Could not initialize COM library");
        return;
    }

    // Create the Filter Graph Manager and query for interfaces.
    hr = CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER, 
                        IID_IGraphBuilder, (void **)&pGraph);
    if (FAILED(hr))
    {
        printf("ERROR - Could not create the Filter Graph Manager.");
        return;
    }

    hr = pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
    hr = pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);

    // Build the graph. IMPORTANT: Change this string to a file
    // on your system.
    hr = pGraph->RenderFile(L"test.wmv", NULL);
    if (SUCCEEDED(hr))
    {
        // Run the graph.
        hr = pControl->Run();
        if (SUCCEEDED(hr))
        {
            // Wait for completion.
            long evCode;
            pEvent->WaitForCompletion(INFINITE, &evCode);

            // Note: Do not use INFINITE in a real application, because it
            // can block indefinitely.
        }
    }
    pControl->Release();
    pEvent->Release();
    pGraph->Release();
    CoUninitialize();
}

```



<span data-ttu-id="f1746-157">Tenga en cuenta que el código de aplicación de este sencillo ejemplo nunca hace referencia al lector ASF de WM en concreto.</span><span class="sxs-lookup"><span data-stu-id="f1746-157">Note that the application code for this simple example never references the WM ASF Reader specifically.</span></span> <span data-ttu-id="f1746-158">Dicho filtro se crea, conecta, ejecuta y finalmente se libera mediante el administrador de gráficos de filtro.</span><span class="sxs-lookup"><span data-stu-id="f1746-158">That filter is created, connected, run, and eventually released by the Filter Graph Manager.</span></span> <span data-ttu-id="f1746-159">Sin embargo, en muchos escenarios, es posible que desee configurar el lector ASF de WM antes de comenzar la reproducción.</span><span class="sxs-lookup"><span data-stu-id="f1746-159">In many scenarios, however, you may want to configure the WM ASF Reader before beginning playback.</span></span>

 

 




