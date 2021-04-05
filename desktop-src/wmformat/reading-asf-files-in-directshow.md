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
# <a name="reading-asf-files-in-directshow-windows-media-format-11-sdk"></a>Leer archivos ASF en DirectShow (Windows Media Format 11 SDK)

La reproducción de archivos ASF se controla mediante el filtro [lector ASF de WM](wm-asf-reader-filter.md) . Cuando el lector ASF de WM lee un archivo, crea automáticamente un PIN de salida para cada flujo, incluidas las secuencias Web, secuencias de comandos de script y cualquier otro tipo de secuencia arbitraria. En el caso de varios archivos de velocidad de bits, los pin solo se crean para las secuencias seleccionadas actualmente.

El lector ASF de WM admite la interfaz **IMediaSeeking** de DirectShow, que permite a las aplicaciones realizar búsquedas temporales en el archivo. Sin embargo, no se admite la reproducción a velocidades distintas de 1,0 (tal y como se especifica en **IMediaSeeking:: SetRate**).

El filtro también expone varias interfaces del SDK de Windows Media Format, como se describe en la tabla siguiente.



| Interfaz                                        | Cómo se exponen                            | Comentarios                                                                                                                                                                                    |
|--------------------------------------------------|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)             | A través de **IServiceProvider** en filtro | Se proporciona para las aplicaciones que necesitan reproducir contenido protegido por Rights Management digitales (DRM). Esta interfaz también se puede usar para obtener otras interfaces en el objeto de lector directamente. |
| [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)           | **QueryInterface** en filtro           | Proporcionado para que las aplicaciones puedan leer atributos de archivo y de contenido, así como información de marcadores y metadatos.                                                                  |
| [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)   | **QueryInterface** en filtro           | Implementado parcialmente en el filtro para que las aplicaciones puedan tener acceso a los métodos informativos del objeto lector de WM.                                                                      |
| [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) | **QueryInterface** en filtro           | Implementado parcialmente en el filtro para que las aplicaciones puedan tener acceso a los métodos informativos del objeto lector.                                                                         |



 

El filtro [lector ASF de WM](wm-asf-reader-filter.md) estaba disponible por primera vez en DirectShow 8,0. La versión del filtro que se incluye con DirectShow 8,1 y 9,0 admite la versión 7. *x* del SDK de Windows Media Format. La versión más reciente del filtro, junto con los demás componentes de QASF, se suministra con y es compatible con el SDK de Windows Media Format 9 series y versiones posteriores, y reemplaza el filtro en DirectX 9,0. Si instala el SDK de Windows Media Format después de instalar DirectX 8. *x* o 9. *x* SDK, sobrescribirá la versión de DirectX de qasf.dll con la versión de la serie 9. Esto no debería presentar ningún problema, excepto posiblemente en un escenario en el que se producirá un comportamiento diferente en el método DirectShow **IGraphBuilder:: RenderFile** . La versión del SDK de Windows Media Format 9 series del lector ASF de WM es el filtro de origen predeterminado para las extensiones de nombre de archivo. ASF,. WMV y. WMA. Esto significa que el lector ASF de WM se crea y agrega automáticamente al gráfico de filtro mediante el administrador de gráficos de filtro en métodos como **IGraphBuilder:: RenderFile** o **IGraphBuilder:: AddSourceFilter** cuando se especifica un archivo de este tipo. En DirectX 9,0 y versiones anteriores, y Windows XP Service Pack 1 y versiones anteriores, el método **RenderFile** usa el filtro de origen de Windows Media anterior. Este comportamiento se mantuvo para garantizar la compatibilidad con versiones anteriores de las aplicaciones que usaban Windows Media Player 6,4. Para obtener más información sobre el filtro de origen de medios de Windows heredado, vea la documentación del SDK de DirectShow.

Para reproducir un archivo ASF con contenido basado en Windows Media mediante el lector ASF de WM, los tres pasos principales son crear una instancia del administrador de gráficos de filtros, llamar a **IGraphBuilder:: RenderFile** para crear el gráfico y, a continuación, llamar a **IMediaControl:: Run** para reproducir el archivo. El siguiente ejemplo de código es un programa completo que reproduce un archivo ASF mediante DirectShow. Para ejecutar este ejemplo, debe tener instalado el SDK de DirectX y el entorno de compilación debe configurarse de acuerdo con las instrucciones del tema de la documentación del SDK de DirectShow sobre cómo configurar el entorno de compilación. Además, debe especificar un archivo en el equipo en la llamada a **RenderFile**.


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



Tenga en cuenta que el código de aplicación de este sencillo ejemplo nunca hace referencia al lector ASF de WM en concreto. Dicho filtro se crea, conecta, ejecuta y finalmente se libera mediante el administrador de gráficos de filtro. Sin embargo, en muchos escenarios, es posible que desee configurar el lector ASF de WM antes de comenzar la reproducción.

 

 




