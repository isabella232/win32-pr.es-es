---
description: Creación de gráficos de filtro para escribir archivos ASF
ms.assetid: c4885152-d7d2-4749-a79a-e0effd38837d
title: Creación de gráficos de filtro para escribir archivos ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0581672f9fd3e4bfa5e2c678c3bd3c0d3ea22fa0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161677"
---
# <a name="building-filter-graphs-to-write-asf-files"></a>Creación de gráficos de filtro para escribir archivos ASF

Al crear Windows contenido basado en multimedia, las aplicaciones suelen usar uno de los escenarios siguientes:

-   Convertir o transcodificación de contenido de otro formato a Windows formato multimedia.
-   Insertar contenido que no se Windows basado en multimedia (formatos de secuencia nativos) en archivos ASF.
-   Captura de datos en directo y codificación inmediatamente en Windows formato multimedia.

Transcodificación de archivos ASF

Puede crear un gráfico de filtros de transcodificación de archivos mediante [WM ASF Writer](wm-asf-writer-filter.md) de varias maneras. La manera más fácil es agregar wm asf writer al gráfico de filtro y, a continuación, usar el método IGraphBuilder::RenderFile para compilar el gráfico automáticamente.

Una manera alternativa es agregar cada filtro manualmente al gráfico y conectar los pines. Después de agregar WM ASF Writer, configúrelo mediante los métodos IConfigAsfWriter si el perfil predeterminado no es adecuado y conecte los pines de entrada de WM ASF Writer a los pins de salida correspondientes en los filtros ascendentes.

En la ilustración siguiente se muestran las configuraciones de gráficos de filtro de transcodificación de WM ASF Writer típicas.

![Gráfico de filtros de transcodificación](images/asf-transcode.png)

Inserción de formatos de flujo nativos en archivos ASF

De forma predeterminada, el filtro WM ASF Writer espera secuencias de audio y vídeo sin comprimir en sus pines de entrada y usa los códecs Windows Media Audio y Windows Media Video para comprimir las secuencias. Sin embargo, el contenedor de archivos ASF se puede usar para cualquier tipo de datos. Al colocar datos multimedia digitales en un contenedor de archivos ASF, puede agregar características proporcionadas por ASF, como metadatos y administración de derechos digitales (DRM), sin tener que transcodificar el contenido.

Para crear un archivo ASF que contenga contenido que no esté basado en medios de Windows, la aplicación debe comprimir la secuencia en el gráfico de filtro ascendente del escritor de ASF de WM y omitir el mecanismo de compresión del escritor de ASF wm llamando a [**IConfigAsfWriter2::SetParam**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-setparam) como se muestra a continuación:


```C++
pConfigAsfWriter2->SetParam(AM_CONFIGASFWRITER_PARAM_DONTCOMPRESS,TRUE,0)
```



A continuación, configure el filtro con el perfil deseado. Es esencial que el tipo de medio del flujo de entrada coincida exactamente con el formato del perfil. En algunos casos, puede ser necesario examinar el formato del flujo de entrada y crear un perfil personalizado para que coincida con él.

Cuando conecte WM ASF Writer al filtro ascendente, use el método IGraphBuilder::ConnectDirect. No use ningún método de "conexión inteligente", como IGraphBuilder::Conectar o IGraphBuilder::RenderFile, para conectar el filtro, ya que esto deshabilitará el modo de "compresión de omisión" del filtro.

Capturar directamente desde un dispositivo a un archivo ASF

Al capturar audio o vídeo directamente en un archivo ASF, el gráfico de filtro tendrá un aspecto similar al siguiente, dependiendo del tipo de dispositivo de captura que se esté utilizando.

![Gráfico de captura de vídeo de Windows Media](images/asf-webcam.png)

Para obtener más información sobre cómo crear gráficos de captura de vídeo y audio, vea los temas siguientes:

-   [Captura de audio](audio-capture.md)
-   [Captura de vídeo](video-capture.md)

Wm ASF Writer no se ejecutará a menos que todos sus pines estén conectados. Si configura WM ASF Writer con el perfil del sistema predeterminado (no recomendado) o cualquier perfil con secuencias de audio y vídeo, se creará un pin de entrada para cada secuencia y cada uno de esos pines debe estar conectado. Si no piensa capturar audio, por ejemplo, asegúrese de configurar el filtro con un perfil de solo vídeo para que no se cree ninguna marca de audio.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Creación de archivos ASF en DirectShow](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 



