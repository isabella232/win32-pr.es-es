---
title: Leer archivos ASF en DirectShow (WINDOWS SDK de formato multimedia 11)
description: La reproducción de archivos ASF se controla mediante el filtro WM ASF Reader. Obtenga información sobre cómo leer archivos ASF DirectShow en el SDK Windows Media Format 11.
ms.assetid: eec2c91f-1762-4798-91d0-d68ec2160d6a
keywords:
- Windows SDK de formato multimedia, DirectShow
- Windows SDK de formato multimedia, lectura de archivos ASF
- Windows SDK de formato multimedia, filtro lector ASF de WM
- Windows SDK de formato multimedia, interfaz IMediaSeeking
- Formato de sistemas avanzados (ASF),DirectShow
- ASF (formato de sistemas avanzados), DirectShow
- Formato de sistemas avanzados (ASF), lectura de archivos
- ASF (formato de sistemas avanzados), lectura de archivos
- Formato de sistemas avanzados (ASF), filtro de lector ASF de WM
- ASF (formato de sistemas avanzados), filtro de lector ASF de WM
- Advanced Systems Format (ASF), interfaz IMediaSeeking
- ASF (formato de sistemas avanzados), interfaz IMediaSeeking
- DirectShow,lectura de archivos ASF
- DirectShow,filtro de lector ASF de WM
- DirectShow interfaz IMediaSeeking
- Filtro de lector ASF de WM
- IMediaSeeking
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4aaab64798011eb21edbe43f49438db99d0bae6b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466674"
---
# <a name="reading-asf-files-in-directshow-windows-media-format-11-sdk"></a>Leer archivos ASF en DirectShow (WINDOWS SDK de formato multimedia 11)

La reproducción de archivos ASF se controla mediante el filtro [WM ASF Reader.](wm-asf-reader-filter.md) Cuando el lector DE ASF de WM lee un archivo, crea automáticamente un pin de salida para cada secuencia, incluidos flujos web, secuencias de comandos de script y cualquier otro tipo de flujo arbitrario. En el caso de varios archivos de velocidad de bits, los pins solo se crean para las secuencias seleccionadas actualmente.

Wm ASF Reader admite la interfaz DirectShow **IMediaSeeking,** que permite a las aplicaciones realizar búsquedas temporales dentro del archivo. Sin embargo, no se admite la reproducción a velocidades diferentes de 1.0 (como se especifica en **IMediaSeeking::SetRate).**

El filtro también expone varias interfaces Windows SDK de formato multimedia como se describe en la tabla siguiente.



| Interfaz                                        | Exposición                            | Comentarios                                                                                                                                                                                    |
|--------------------------------------------------|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)             | A **través de IServiceProvider** en el filtro | Se proporciona para las aplicaciones que necesitan reproducir contenido protegido por Digital Rights Management (DRM). Esta interfaz también se puede usar para obtener otras interfaces en el objeto reader directamente. |
| [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)           | **QueryInterface en** el filtro           | Se proporciona para que las aplicaciones puedan leer atributos de archivo y contenido, así como información de marcadores y scripts y metadatos.                                                                  |
| [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)   | **QueryInterface en** el filtro           | Parcialmente implementado en el filtro para que las aplicaciones puedan tener acceso a los métodos informativos en el objeto WM Reader.                                                                      |
| [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) | **QueryInterface en** el filtro           | Parcialmente implementado en el filtro para que las aplicaciones puedan tener acceso a los métodos informativos en el objeto reader.                                                                         |



 

El [filtro WM ASF Reader](wm-asf-reader-filter.md) se hizo disponible por primera vez en DirectShow 8.0. La versión del filtro que se incluye con DirectShow 8.1 y 9.0 admite la versión 7. *x* del SDK Windows Media Format. La versión más reciente del filtro, junto con los demás componentes de QASF, se suministra con y admite el SDK de la serie Windows Media Format 9 y versiones posteriores, y reemplaza el filtro en DirectX 9.0. Si instala el SDK Windows Media Format después de instalar DirectX 8. *x* o 9. *x* SDK, sobrescribirá la versión de DirectX de qasf.dll con la versión de la serie 9. Esto no debe presentar ningún problema, excepto posiblemente en un escenario en el que dará lugar a un comportamiento diferente en el DirectShow **método IGraphBuilder::RenderFile.** La versión del SDK de la serie Windows Media Format 9 del lector DE ASF de WM es el filtro de origen predeterminado para las extensiones de nombre de archivo .asf, .wmv y .wma. Esto significa que el Administrador de filtros de Graph crea automáticamente el lector de ASF wm y lo agrega al gráfico de filtros en métodos como **IGraphBuilder::RenderFile** o **IGraphBuilder::AddSourceFilter** cuando se especifica un archivo de este tipo. En DirectX 9.0 y versiones anteriores, y Windows XP Service Pack 1 y versiones anteriores, el método **RenderFile** usa el filtro de origen multimedia Windows anterior. Este comportamiento se ha mantenido para garantizar la compatibilidad con versiones anteriores con las aplicaciones que usaban Reproductor de Windows Media 6.4. Para más información sobre el filtro de origen Windows multimedia heredado, consulte la documentación DirectShow SDK.

Para reproducir un archivo ASF con contenido basado en medios de Windows mediante el lector DE ASF de WM, los tres pasos principales son crear una instancia del Administrador de filtros Graph, llamar a **IGraphBuilder::RenderFile** para crear el gráfico y, a continuación, llamar a **IMediaControl::Run** para reproducir el archivo. El ejemplo de código siguiente es un programa completo que reproduce un archivo ASF mediante DirectShow. Para ejecutar este ejemplo, debe tener instalado el SDK de DirectX y el entorno de compilación debe configurarse según las instrucciones del tema de documentación del SDK de DirectShow "Configuración del entorno de compilación". Además, debe especificar un archivo en el equipo en la llamada a **RenderFile**.


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



Tenga en cuenta que el código de aplicación de este ejemplo simple nunca hace referencia específicamente al lector DE ASF de WM. El Administrador de filtros crea, conecta, ejecuta y Graph finalmente libera ese filtro. Sin embargo, en muchos escenarios, es posible que desee configurar el lector DE ASF wm antes de comenzar la reproducción.

 

 




