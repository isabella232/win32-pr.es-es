---
title: Para transcodificar contenido con recompresión inteligente
description: Para transcodificar contenido con recompresión inteligente
ms.assetid: 02398462-b0a4-4a17-84e3-4c6f9f26639f
keywords:
- Windows SDK de formato multimedia, transcodificación de contenido
- Windows SDK de formato multimedia, recompresión inteligente
- Windows SDK de formato multimedia, recompresión
- Windows SDK de formato multimedia, Windows códecs de audio multimedia
- Formato de sistemas avanzados (ASF), transcodificación de contenido
- ASF (formato de sistemas avanzados), transcodificación de contenido
- Formato de sistemas avanzados (ASF), recompresión inteligente
- ASF (formato de sistemas avanzados), recompresión inteligente
- Formato de sistemas avanzados (ASF), recompresión
- ASF (formato de sistemas avanzados), recompresión
- Formato de sistemas avanzados (ASF), Windows códecs de audio multimedia
- ASF (formato de sistemas avanzados), Windows códecs de audio multimedia
- transcodificación de contenido
- recompresión inteligente
- Recompresión
- Windows Códecs de audio multimedia, transcodificación de contenido
- códecs, Windows códecs de audio multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee1cf363e196feca81ef9757f006b211758c2ff7fbdd1f50b5136992b394f8dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118699096"
---
# <a name="to-transcode-content-with-smart-recompression"></a>Para transcodificar contenido con recompresión inteligente

Puede transcodificar contenido de una velocidad de bits a otra mediante el SDK Windows Media Format. Normalmente, esto implica simplemente la decodización del contenido y su codificación de nuevo a la velocidad de bits deseada. El códec Windows Media Audio 9 admite la recompresión inteligente, que permite la transcodificación que logra una mejor calidad de lo normal.

Para la recompresión inteligente, la secuencia de audio original debe codificarse con el códec Windows media audio. Se admiten todas las versiones del códec, pero los códecs de audio especializados (Windows Media Audio 9 Professional y Windows Media Audio 9 Voice) no lo son. Si el audio original se codifica con el códec sin pérdida de Windows Media Audio 9, no es necesario usar la recompresión inteligente, ya que no se perdió información en la codificación original.

Para usar la recompresión inteligente, realice los pasos siguientes.

1.  Configure un objeto de lector con el archivo de código fuente para su lectura. Para obtener más información, vea [Leer archivos ASF.](reading-asf-files.md)
2.  Configure un objeto de escritor que se usará para transcodificación del archivo. Establezca el nombre de archivo para el nuevo archivo. Seleccione un perfil que se usará para el nuevo archivo. Establezca el perfil seleccionado en el objeto de escritor. Para obtener más información, vea [Escribir archivos ASF.](writing-asf-files.md)
3.  Obtenga un puntero a la [**interfaz IWMProfile**](iwmprofile.md) del objeto reader llamando a **IWMReader::QueryInterface**.
4.  Recupere la [**interfaz IWMStreamConfig para**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) la secuencia de audio que se va a transcodificar llamando a [**IWMProfile::GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream).
5.  Obtenga la [**interfaz IWMMediaProps para**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops) el objeto de configuración de flujo llamando a **IWMStreamConfig::QueryInterface**.
6.  Recupere la [**estructura \_ WM MEDIA \_ TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) para la secuencia realizando dos llamadas a [**IWMMediaProps::GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype). Obtenga el tamaño de la estructura en la primera llamada y asigne memoria para que un búfer pase en la segunda llamada.
7.  Obtenga un puntero a la [**interfaz IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) para la entrada en el escritor mediante una llamada a [**IWMWriter::GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops).
8.  Obtenga la [**interfaz IWMPropertyVault para**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) el objeto de propiedades de medios de entrada llamando a **IWMInputMediaProps::QueryInterface**.
9.  Use el [**método IWMPropertyVault::SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) para establecer la propiedad \_ g wszOriginalWaveFormat. Use la **estructura DEDATOSATEX** obtenida en el paso 6 como valor de la propiedad .
10. Incluya los cambios realizados en las propiedades del medio de entrada llamando a [**IWMWriter::SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) y pasando un puntero a la **interfaz IWMInputMediaProps.**
11. Comience a leer ejemplos del archivo original y pasarlos al escritor con llamadas a [**IWMWriter::WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Temas avanzados**](advanced-topics.md)
</dt> <dt>

[**Interfaz IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops)
</dt> <dt>

[**IWMMediaProps (interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)
</dt> <dt>

[**IWMProfile (interfaz)**](iwmprofile.md)
</dt> <dt>

[**IWMPropertyVault (interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault)
</dt> <dt>

[**Interfaz IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)
</dt> </dl>

 

 




