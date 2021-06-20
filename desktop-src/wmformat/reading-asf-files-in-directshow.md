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
# <a name="reading-asf-files-in-directshow-windows-media-format-11-sdk"></a>Lectura de archivos ASF en DirectShow (Windows Media Format SDK 11)

La reproducción de archivos ASF se controla mediante el filtro [WM ASF Reader.](wm-asf-reader-filter.md) Cuando el Lector DE ASF de WM lee un archivo, crea automáticamente un pin de salida para cada secuencia, incluidas secuencias web, secuencias de comandos de script y cualquier otro tipo de secuencia arbitraria. En el caso de varios archivos de velocidad de bits, solo se crean pins para los flujos seleccionados actualmente.

Wm ASF Reader admite la interfaz **IMediaSeeking** de DirectShow, que permite a las aplicaciones realizar búsquedas temporales dentro del archivo. Sin embargo, no se admite la reproducción a velocidades diferentes de 1.0 (como se especifica en **IMediaSeeking::SetRate**).

El filtro también expone varias interfaces Windows Media Format SDK, como se describe en la tabla siguiente.



| Interfaz                                        | Cómo se expone                            | Comentarios                                                                                                                                                                                    |
|--------------------------------------------------|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)             | A **través de IServiceProvider en** el filtro | Se proporciona para las aplicaciones que necesitan reproducir contenido protegido por Digital Rights Management (DRM). Esta interfaz también se puede usar para obtener otras interfaces en el objeto lector directamente. |
| [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)           | **QueryInterface en** el filtro           | Se proporciona para que las aplicaciones puedan leer atributos de archivo y contenido, así como información de marcadores y scripts y metadatos.                                                                  |
| [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)   | **QueryInterface en** el filtro           | Parcialmente implementado en el filtro para que las aplicaciones puedan tener acceso a los métodos informativos en el objeto lector wm.                                                                      |
| [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) | **QueryInterface en** el filtro           | Parcialmente implementado en el filtro para que las aplicaciones puedan tener acceso a los métodos informativos en el objeto reader.                                                                         |



 

El [filtro WM ASF Reader](wm-asf-reader-filter.md) se hizo disponible por primera vez en DirectShow 8.0. La versión del filtro que se incluye con DirectShow 8.1 y 9.0 admite la versión 7. *x* del SDK Windows Media Format. La versión más reciente del filtro, junto con los demás componentes de QASF, se incluye con y admite el SDK de la serie Windows Media Format 9 y versiones posteriores, y reemplaza el filtro en DirectX 9.0. Si instala el SDK Windows Media Format después de instalar DirectX 8. *x* o 9. *x* SDK, sobrescribirá la versión de DirectX de qasf.dll con la versión de la serie 9. Esto no debería presentar ningún problema, excepto posiblemente en un escenario en el que se produciría un comportamiento diferente en el método **IGraphBuilder::RenderFile de** DirectShow. La Windows Media Format SDK de la serie 9 del lector de ASF wm es el filtro de origen predeterminado para las extensiones de nombre de archivo .asf, .wmv y .wma. Esto significa que el Administrador de gráficos de filtros crea automáticamente el lector de ASF wm y lo agrega al gráfico de filtros en métodos como **IGraphBuilder::RenderFile** o **IGraphBuilder::AddSourceFilter** cuando se especifica un archivo de este tipo. En DirectX 9.0 y versiones anteriores, y Windows XP Service Pack 1 y versiones anteriores, el método **RenderFile** usa el filtro de origen de Windows Media anterior. Este comportamiento se mantiene para garantizar la compatibilidad con versiones anteriores con las aplicaciones que usaban Reproductor de Windows Media 6.4. Para obtener más información sobre el filtro de origen de Windows Media heredado, consulte la documentación del SDK de DirectShow.

Para reproducir un archivo ASF con contenido basado en Windows Media mediante el lector DE ASF de WM, los tres pasos principales son crear una instancia del Administrador de gráficos de filtros, llamar a **IGraphBuilder::RenderFile** para crear el gráfico y, a continuación, llamar a **IMediaControl::Run** para reproducir el archivo. El ejemplo de código siguiente es un programa completo que reproduce un archivo ASF mediante DirectShow. Para ejecutar este ejemplo, debe tener instalado el SDK de DirectX y el entorno de compilación debe configurarse según las instrucciones del tema de documentación del SDK de DirectShow "Configurar el entorno de compilación". Además, debe especificar un archivo en el equipo en la llamada a **RenderFile**.


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



Tenga en cuenta que el código de aplicación de este ejemplo simple nunca hace referencia específicamente al lector de ASF wm. El Administrador de gráficos de filtros crea, conecta, ejecuta y finalmente libera ese filtro. Sin embargo, en muchos escenarios, es posible que desee configurar el lector DE ASF wm antes de comenzar la reproducción.

 

 




