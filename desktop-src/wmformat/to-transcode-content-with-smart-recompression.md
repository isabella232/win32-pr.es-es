---
title: Para transcodificar contenido con recompresión inteligente
description: Para transcodificar contenido con recompresión inteligente
ms.assetid: 02398462-b0a4-4a17-84e3-4c6f9f26639f
keywords:
- SDK de Windows Media Format, transcodificación de contenido
- SDK de Windows Media Format, recompresión inteligente
- SDK de Windows Media Format, recompresión
- Windows Media Format SDK, códecs de Windows Media Audio
- Formato de sistemas avanzados (ASF), transcodificación de contenido
- ASF (formato de sistemas avanzados), transcodificar contenido
- Advanced Systems Format (ASF), recompresión inteligente
- ASF (formato de sistemas avanzados), recompresión inteligente
- Advanced Systems Format (ASF), recompresión
- ASF (formato de sistemas avanzados), recompresión
- Formatos de sistema avanzado (ASF), códecs de Windows Media Audio
- ASF (formato de sistemas avanzados), códecs de Windows Media Audio
- transcodificar contenido
- recompresión inteligente
- recompresión
- Códecs de Windows Media Audio, transcodificación de contenido
- códecs, códecs de Windows Media Audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a1317989ea9384d4a9747d712af1ce5c61d484c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104358692"
---
# <a name="to-transcode-content-with-smart-recompression"></a>Para transcodificar contenido con recompresión inteligente

Puede transcodificar contenido de una velocidad de bits a otra mediante el SDK de Windows Media Format. Normalmente, esto implica simplemente descodificar el contenido y codificarlo de nuevo a la velocidad de bits deseada. El códec Windows Media Audio 9 admite la recompresión inteligente, que permite la transcodificación que consigue una mejor calidad que la normal.

Para la recompresión inteligente, la secuencia de audio original debe estar codificada con el códec Windows Media Audio. Se admiten todas las versiones del códec, pero no los códecs de audio especializados (Windows Media Audio 9 Professional y Windows Media Audio 9 Voice). Si el audio original se ha codificado con el códec Windows Media Audio 9 Lossless, no es necesario utilizar la recompresión inteligente, ya que no se ha perdido información en la codificación original.

Para usar la recompresión inteligente, realice los pasos siguientes.

1.  Configure un objeto de lector con el archivo de origen para leerlo. Para obtener más información, consulte [leer archivos ASF](reading-asf-files.md).
2.  Configure un objeto de escritor que se usará para transcodificar el archivo. Establezca el nombre de archivo para el nuevo archivo. Seleccione un perfil para usarlo con el nuevo archivo. Establezca el perfil seleccionado en el objeto escritor. Para obtener más información, consulte [Writing ASF files](writing-asf-files.md).
3.  Obtiene un puntero a la interfaz [**IWMProfile**](iwmprofile.md) del objeto lector llamando a **IWMReader:: QueryInterface**.
4.  Recupere la interfaz [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) para la secuencia de audio que se va a transcodificar mediante una llamada a [**IWMProfile:: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream).
5.  Obtenga la interfaz [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops) para el objeto de configuración de flujo llamando a **IWMStreamConfig:: QueryInterface**.
6.  Recupere la estructura de [**\_ \_ tipo de medio de WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) para la secuencia realizando dos llamadas a [**IWMMediaProps:: GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype). Obtiene el tamaño de la estructura en la primera llamada y asigna memoria para un búfer que se va a pasar en la segunda llamada.
7.  Obtiene un puntero a la interfaz [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) para la entrada en el escritor llamando a [**IWMWriter:: GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops).
8.  Obtenga la interfaz [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) para el objeto de las propiedades de los medios de entrada mediante una llamada a **IWMInputMediaProps:: QueryInterface**.
9.  Use el método [**IWMPropertyVault:: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) para establecer la \_ propiedad g wszOriginalWaveFormat. Use la estructura **WAVEFORMATEX** obtenida en el paso 6 como el valor de la propiedad.
10. Incluya los cambios realizados en las propiedades de los medios de entrada mediante una llamada a [**IWMWriter:: SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) y pasándole un puntero a la interfaz **IWMInputMediaProps** .
11. Comience a leer ejemplos del archivo original y a pasarlos al escritor con llamadas a [**IWMWriter:: WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Temas avanzados**](advanced-topics.md)
</dt> <dt>

[**Interfaz IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops)
</dt> <dt>

[**Interfaz IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)
</dt> <dt>

[**Interfaz IWMProfile**](iwmprofile.md)
</dt> <dt>

[**Interfaz IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault)
</dt> <dt>

[**Interfaz IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)
</dt> </dl>

 

 




