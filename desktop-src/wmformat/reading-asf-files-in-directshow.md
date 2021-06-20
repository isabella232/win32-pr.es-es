---
title: Lectura de archivos ASF en DirectShow (Windows Media Format SDK 11)
description: La reproducción de archivos ASF se controla mediante el filtro WM ASF Reader. Obtenga información sobre cómo leer archivos ASF en DirectShow en el SDK Windows Media Format 11.
ms.assetid: eec2c91f-1762-4798-91d0-d68ec2160d6a
keywords:
- Windows Media Format SDK,DirectShow
- Windows Media Format SDK, leer archivos ASF
- Windows Media Format SDK,filtro del lector de ASF de WM
- Windows Media Format SDK,IMediaSeeking (interfaz)
- Formato de sistemas avanzados (ASF),DirectShow
- ASF (formato de sistemas avanzados),DirectShow
- Formato de sistemas avanzados (ASF), leer archivos
- ASF (formato de sistemas avanzados), leer archivos
- Formato de sistemas avanzados (ASF), filtro de lector DE ASF de WM
- ASF (formato de sistemas avanzados), filtro del lector DE ASF de WM
- Advanced Systems Format (ASF),IMediaSeeking (interfaz)
- ASF (formato de sistemas avanzados), interfaz IMediaSeeking
- DirectShow, leer archivos ASF
- Filtro DirectShow,WM ASF Reader
- Interfaz DirectShow,IMediaSeeking
- Filtro de lector de ASF de WM
- IMediaSeeking
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4aaab64798011eb21edbe43f49438db99d0bae6b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404328"
---
# <a name="reading-asf-files-in-directshow-windows-media-format-11-sdk"></a><span data-ttu-id="30b25-121">Lectura de archivos ASF en DirectShow (Windows Media Format SDK 11)</span><span class="sxs-lookup"><span data-stu-id="30b25-121">Reading ASF Files in DirectShow (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="30b25-122">La reproducción de archivos ASF se controla mediante el filtro [WM ASF Reader.](wm-asf-reader-filter.md)</span><span class="sxs-lookup"><span data-stu-id="30b25-122">Playback of ASF files is handled by the [WM ASF Reader](wm-asf-reader-filter.md) filter.</span></span> <span data-ttu-id="30b25-123">Cuando el Lector DE ASF de WM lee un archivo, crea automáticamente un pin de salida para cada secuencia, incluidas secuencias web, secuencias de comandos de script y cualquier otro tipo de secuencia arbitraria.</span><span class="sxs-lookup"><span data-stu-id="30b25-123">When the WM ASF Reader reads a file, it automatically creates an output pin for each stream, including Web streams, script command streams, and any other type of arbitrary stream.</span></span> <span data-ttu-id="30b25-124">En el caso de varios archivos de velocidad de bits, solo se crean pins para los flujos seleccionados actualmente.</span><span class="sxs-lookup"><span data-stu-id="30b25-124">In the case of multiple bit rate files, pins are created only for the currently selected streams.</span></span>

<span data-ttu-id="30b25-125">Wm ASF Reader admite la interfaz **IMediaSeeking** de DirectShow, que permite a las aplicaciones realizar búsquedas temporales dentro del archivo.</span><span class="sxs-lookup"><span data-stu-id="30b25-125">The WM ASF Reader supports the DirectShow **IMediaSeeking** interface, which enables applications to perform temporal seeking within the file.</span></span> <span data-ttu-id="30b25-126">Sin embargo, no se admite la reproducción a velocidades diferentes de 1.0 (como se especifica en **IMediaSeeking::SetRate**).</span><span class="sxs-lookup"><span data-stu-id="30b25-126">However, playback at speeds other than 1.0 (as specified in **IMediaSeeking::SetRate**) is not supported.</span></span>

<span data-ttu-id="30b25-127">El filtro también expone varias interfaces Windows Media Format SDK, como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="30b25-127">The filter also exposes several Windows Media Format SDK interfaces as described in the following table.</span></span>



| <span data-ttu-id="30b25-128">Interfaz</span><span class="sxs-lookup"><span data-stu-id="30b25-128">Interface</span></span>                                        | <span data-ttu-id="30b25-129">Cómo se expone</span><span class="sxs-lookup"><span data-stu-id="30b25-129">How exposed</span></span>                            | <span data-ttu-id="30b25-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="30b25-130">Comments</span></span>                                                                                                                                                                                    |
|--------------------------------------------------|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="30b25-131">**IWMDRMReader**</span><span class="sxs-lookup"><span data-stu-id="30b25-131">**IWMDRMReader**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)             | <span data-ttu-id="30b25-132">A **través de IServiceProvider en** el filtro</span><span class="sxs-lookup"><span data-stu-id="30b25-132">Through **IServiceProvider** on filter</span></span> | <span data-ttu-id="30b25-133">Se proporciona para las aplicaciones que necesitan reproducir contenido protegido por Digital Rights Management (DRM).</span><span class="sxs-lookup"><span data-stu-id="30b25-133">Provided for applications that need to play content protected by Digital Rights Management (DRM).</span></span> <span data-ttu-id="30b25-134">Esta interfaz también se puede usar para obtener otras interfaces en el objeto lector directamente.</span><span class="sxs-lookup"><span data-stu-id="30b25-134">This interface can also be used to obtain other interfaces on the Reader Object directly.</span></span> |
| [<span data-ttu-id="30b25-135">**IWMHeaderInfo**</span><span class="sxs-lookup"><span data-stu-id="30b25-135">**IWMHeaderInfo**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)           | <span data-ttu-id="30b25-136">**QueryInterface en** el filtro</span><span class="sxs-lookup"><span data-stu-id="30b25-136">**QueryInterface** on filter</span></span>           | <span data-ttu-id="30b25-137">Se proporciona para que las aplicaciones puedan leer atributos de archivo y contenido, así como información de marcadores y scripts y metadatos.</span><span class="sxs-lookup"><span data-stu-id="30b25-137">Provided so that applications can read file and content attributes, as well as marker and script information and metadata.</span></span>                                                                  |
| [<span data-ttu-id="30b25-138">**IWMReaderAdvanced**</span><span class="sxs-lookup"><span data-stu-id="30b25-138">**IWMReaderAdvanced**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)   | <span data-ttu-id="30b25-139">**QueryInterface en** el filtro</span><span class="sxs-lookup"><span data-stu-id="30b25-139">**QueryInterface** on filter</span></span>           | <span data-ttu-id="30b25-140">Parcialmente implementado en el filtro para que las aplicaciones puedan tener acceso a los métodos informativos en el objeto lector wm.</span><span class="sxs-lookup"><span data-stu-id="30b25-140">Partially implemented on the filter so that applications can access the informational methods on the WM Reader object.</span></span>                                                                      |
| [<span data-ttu-id="30b25-141">**IWMReaderAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="30b25-141">**IWMReaderAdvanced2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) | <span data-ttu-id="30b25-142">**QueryInterface en** el filtro</span><span class="sxs-lookup"><span data-stu-id="30b25-142">**QueryInterface** on filter</span></span>           | <span data-ttu-id="30b25-143">Parcialmente implementado en el filtro para que las aplicaciones puedan tener acceso a los métodos informativos en el objeto reader.</span><span class="sxs-lookup"><span data-stu-id="30b25-143">Partially implemented on the filter so that applications can access the informational methods on the Reader Object.</span></span>                                                                         |



 

<span data-ttu-id="30b25-144">El [filtro WM ASF Reader](wm-asf-reader-filter.md) se hizo disponible por primera vez en DirectShow 8.0.</span><span class="sxs-lookup"><span data-stu-id="30b25-144">The [WM ASF Reader](wm-asf-reader-filter.md) filter was first made available in DirectShow 8.0.</span></span> <span data-ttu-id="30b25-145">La versión del filtro que se incluye con DirectShow 8.1 y 9.0 admite la versión 7. *x* del SDK Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="30b25-145">The version of the filter that ships with DirectShow 8.1 and 9.0 supports version 7.*x* of the Windows Media Format SDK.</span></span> <span data-ttu-id="30b25-146">La versión más reciente del filtro, junto con los demás componentes de QASF, se incluye con y admite el SDK de la serie Windows Media Format 9 y versiones posteriores, y reemplaza el filtro en DirectX 9.0.</span><span class="sxs-lookup"><span data-stu-id="30b25-146">The most recent version of the filter, along with the other QASF components, ships with and supports the Windows Media Format 9 Series SDK, and later versions, and it supersedes the filter in DirectX 9.0.</span></span> <span data-ttu-id="30b25-147">Si instala el SDK Windows Media Format después de instalar DirectX 8. *x* o 9. *x* SDK, sobrescribirá la versión de DirectX de qasf.dll con la versión de la serie 9.</span><span class="sxs-lookup"><span data-stu-id="30b25-147">If you install the Windows Media Format SDK after installing the DirectX 8.*x* or 9.*x* SDK, you will overwrite the DirectX version of qasf.dll with the 9 Series version.</span></span> <span data-ttu-id="30b25-148">Esto no debería presentar ningún problema, excepto posiblemente en un escenario en el que se produciría un comportamiento diferente en el método **IGraphBuilder::RenderFile de** DirectShow.</span><span class="sxs-lookup"><span data-stu-id="30b25-148">This should not present any problems except possibly in one scenario where it will result in different behavior in the DirectShow **IGraphBuilder::RenderFile** method.</span></span> <span data-ttu-id="30b25-149">La Windows Media Format SDK de la serie 9 del lector de ASF wm es el filtro de origen predeterminado para las extensiones de nombre de archivo .asf, .wmv y .wma.</span><span class="sxs-lookup"><span data-stu-id="30b25-149">The Windows Media Format 9 Series SDK version of the WM ASF Reader is the default source filter for the .asf, .wmv, and .wma file name extensions.</span></span> <span data-ttu-id="30b25-150">Esto significa que el Administrador de gráficos de filtros crea automáticamente el lector de ASF wm y lo agrega al gráfico de filtros en métodos como **IGraphBuilder::RenderFile** o **IGraphBuilder::AddSourceFilter** cuando se especifica un archivo de este tipo.</span><span class="sxs-lookup"><span data-stu-id="30b25-150">This means that the WM ASF Reader is automatically created and added to the filter graph by the Filter Graph Manager in methods such as **IGraphBuilder::RenderFile** or **IGraphBuilder::AddSourceFilter** when a file of this type is specified.</span></span> <span data-ttu-id="30b25-151">En DirectX 9.0 y versiones anteriores, y Windows XP Service Pack 1 y versiones anteriores, el método **RenderFile** usa el filtro de origen de Windows Media anterior.</span><span class="sxs-lookup"><span data-stu-id="30b25-151">In DirectX 9.0 and earlier, and Windows XP Service Pack 1 and earlier, the **RenderFile** method uses the older Windows Media Source Filter.</span></span> <span data-ttu-id="30b25-152">Este comportamiento se mantiene para garantizar la compatibilidad con versiones anteriores con las aplicaciones que usaban Reproductor de Windows Media 6.4.</span><span class="sxs-lookup"><span data-stu-id="30b25-152">This behavior was maintained to ensure backward compatibility with applications that used the Windows Media Player 6.4.</span></span> <span data-ttu-id="30b25-153">Para obtener más información sobre el filtro de origen de Windows Media heredado, consulte la documentación del SDK de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="30b25-153">For more information about the legacy Windows Media Source Filter, see the DirectShow SDK Documentation.</span></span>

<span data-ttu-id="30b25-154">Para reproducir un archivo ASF con contenido basado en Windows Media mediante el lector DE ASF de WM, los tres pasos principales son crear una instancia del Administrador de gráficos de filtros, llamar a **IGraphBuilder::RenderFile** para crear el gráfico y, a continuación, llamar a **IMediaControl::Run** para reproducir el archivo.</span><span class="sxs-lookup"><span data-stu-id="30b25-154">To play an ASF file with Windows Media–based content using the WM ASF Reader, the three primary steps are to create an instance of the Filter Graph Manager, call **IGraphBuilder::RenderFile** to create the graph, and then call **IMediaControl::Run** to play the file.</span></span> <span data-ttu-id="30b25-155">El ejemplo de código siguiente es un programa completo que reproduce un archivo ASF mediante DirectShow.</span><span class="sxs-lookup"><span data-stu-id="30b25-155">The following code example is a complete program that plays an ASF file using DirectShow.</span></span> <span data-ttu-id="30b25-156">Para ejecutar este ejemplo, debe tener instalado el SDK de DirectX y el entorno de compilación debe configurarse según las instrucciones del tema de documentación del SDK de DirectShow "Configurar el entorno de compilación".</span><span class="sxs-lookup"><span data-stu-id="30b25-156">To run this example, you must have the DirectX SDK installed and your build environment must be configured according to the instructions in the DirectShow SDK documentation topic "Setting Up the Build Environment."</span></span> <span data-ttu-id="30b25-157">Además, debe especificar un archivo en el equipo en la llamada a **RenderFile**.</span><span class="sxs-lookup"><span data-stu-id="30b25-157">Also, you must specify a file on your computer in the call to **RenderFile**.</span></span>


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



<span data-ttu-id="30b25-158">Tenga en cuenta que el código de aplicación de este ejemplo simple nunca hace referencia específicamente al lector de ASF wm.</span><span class="sxs-lookup"><span data-stu-id="30b25-158">Note that the application code for this simple example never references the WM ASF Reader specifically.</span></span> <span data-ttu-id="30b25-159">El Administrador de gráficos de filtros crea, conecta, ejecuta y finalmente libera ese filtro.</span><span class="sxs-lookup"><span data-stu-id="30b25-159">That filter is created, connected, run, and eventually released by the Filter Graph Manager.</span></span> <span data-ttu-id="30b25-160">Sin embargo, en muchos escenarios, es posible que desee configurar el lector DE ASF wm antes de comenzar la reproducción.</span><span class="sxs-lookup"><span data-stu-id="30b25-160">In many scenarios, however, you may want to configure the WM ASF Reader before beginning playback.</span></span>

 

 




