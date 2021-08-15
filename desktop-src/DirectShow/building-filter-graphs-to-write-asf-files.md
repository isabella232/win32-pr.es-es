---
description: Compilar gráficos de filtro para escribir archivos ASF
ms.assetid: c4885152-d7d2-4749-a79a-e0effd38837d
title: Compilar gráficos de filtro para escribir archivos ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe53dcee310be34c321dfc2e988807184735a24b0793d68e3ca7dea10d0b29e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118662758"
---
# <a name="building-filter-graphs-to-write-asf-files"></a>Compilar gráficos de filtro para escribir archivos ASF

Al crear Windows contenido basado en multimedia, las aplicaciones suelen usar uno de los escenarios siguientes:

-   Convertir o transcodificación de contenido de otro formato a Windows formato multimedia.
-   Insertar contenido que no se Windows basado en multimedia (formatos de flujo nativos) en archivos ASF.
-   Captura de datos en directo y codificación inmediatamente en Windows Media Format.

Transcodificación de archivos ASF

Puede crear un gráfico de filtros de transcodificación de archivos mediante [WM ASF Writer](wm-asf-writer-filter.md) de varias maneras. La manera más fácil es agregar WM ASF Writer al gráfico de filtros y, a continuación, usar el método IGraphBuilder::RenderFile para compilar el gráfico automáticamente.

Una manera alternativa es agregar cada filtro manualmente al gráfico y conectar los pines. Después de agregar WM ASF Writer, configúrelo mediante los métodos IConfigAsfWriter si el perfil predeterminado no es adecuado y conecte los pins de entrada de WM ASF Writer a los pins de salida correspondientes en los filtros ascendentes.

En la ilustración siguiente se muestran las configuraciones de gráfico de filtro de transcodificación de WM ASF Writer típicas.

![Gráfico de filtros de transcodificación](images/asf-transcode.png)

Insertar formatos de secuencia nativos en archivos ASF

De forma predeterminada, el filtro WM ASF Writer espera secuencias de audio y vídeo sin comprimir en sus pasadores de entrada y usa los códecs Windows Media Audio y Windows Media Video para comprimir las secuencias. Sin embargo, el contenedor de archivos asf se puede usar para cualquier tipo de datos. Al colocar datos multimedia digitales en un contenedor de archivos ASF, puede agregar características proporcionadas por ASF, como metadatos y administración de derechos digitales (DRM), sin tener que transcodificar el contenido.

Para crear un archivo ASF que contenga contenido que no esté basado en medios de Windows, la aplicación debe comprimir la secuencia en el gráfico de filtro ascendente al escritor de ASF de WM y omitir el mecanismo de compresión de WM ASF Writer llamando a [**IConfigAsfWriter2::SetParam**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-setparam) como se muestra a continuación:


```C++
pConfigAsfWriter2->SetParam(AM_CONFIGASFWRITER_PARAM_DONTCOMPRESS,TRUE,0)
```



A continuación, configure el filtro con el perfil deseado. Es esencial que el tipo de medio del flujo de entrada coincida exactamente con el formato del perfil. En algunos casos, puede ser necesario examinar el formato del flujo de entrada y crear un perfil personalizado para que coincida con él.

Cuando conecte WM ASF Writer al filtro ascendente, use el método IGraphBuilder::ConnectDirect. No use ningún método de "conexión inteligente", como IGraphBuilder::Conectar o IGraphBuilder::RenderFile, para conectar el filtro, ya que esto deshabilitará el modo de "omisión de compresión" del filtro.

Capturar directamente desde un dispositivo a un archivo ASF

Al capturar audio o vídeo directamente en un archivo ASF, el gráfico de filtro tendrá un aspecto similar al siguiente, en función del tipo de dispositivo de captura que se esté utilizando.

![Gráfico de captura de vídeo de Windows Media](images/asf-webcam.png)

Para obtener más información sobre cómo crear gráficos de captura de vídeo y audio, vea los temas siguientes:

-   [Captura de audio](audio-capture.md)
-   [Captura de vídeo](video-capture.md)

Wm ASF Writer no se ejecutará a menos que todos sus pines estén conectados. Si configura WM ASF Writer con el perfil de sistema predeterminado (no recomendado) o cualquier perfil con secuencias de audio y vídeo, se creará un pin de entrada para cada secuencia y cada uno de esos pines debe estar conectado. Si no piensa capturar audio, por ejemplo, asegúrese de configurar el filtro con un perfil de solo vídeo para que no se cree ninguna marca de audio.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear archivos ASF en DirectShow](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 



