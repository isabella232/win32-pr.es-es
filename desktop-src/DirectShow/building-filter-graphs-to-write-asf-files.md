---
description: Generar gráficos de filtro para escribir archivos ASF
ms.assetid: c4885152-d7d2-4749-a79a-e0effd38837d
title: Generar gráficos de filtro para escribir archivos ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0581672f9fd3e4bfa5e2c678c3bd3c0d3ea22fa0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495455"
---
# <a name="building-filter-graphs-to-write-asf-files"></a>Generar gráficos de filtro para escribir archivos ASF

Al crear contenido basado en Windows Media, las aplicaciones suelen usar uno de los siguientes escenarios:

-   Convertir o transcodificar contenido de otro formato en el formato de Windows Media.
-   Insertar contenido que no está basado en Windows Media (formatos de secuencia nativo) en archivos ASF.
-   Capturar datos activos y codificarlos inmediatamente en el formato de Windows Media.

Transcodificar archivos ASF

Puede crear un gráfico de filtros de transcodificación de archivos mediante el [escritor ASF de WM](wm-asf-writer-filter.md) de varias maneras. La manera más fácil es agregar el escritor ASF de WM al gráfico de filtro y, a continuación, usar el método IGraphBuilder:: RenderFile para generar el gráfico automáticamente.

Una manera alternativa es agregar cada filtro manualmente al gráfico y conectar los pin. Después de agregar el escritor ASF de WM, configúrelo con los métodos IConfigAsfWriter si el perfil predeterminado no es adecuado y conecte las clavijas de entrada del escritor ASF de WM a los pin de salida correspondientes en los filtros de nivel superior.

En la ilustración siguiente se muestran configuraciones típicas del gráfico de filtros de transcodificación ASF de WM.

![gráfico de filtros de transcodificación](images/asf-transcode.png)

Insertar formatos de secuencias nativas en archivos ASF

De forma predeterminada, el filtro del escritor ASF de WM espera secuencias de audio y vídeo sin comprimir en sus clavijas de entrada, y usa los códecs Windows Media Audio y Windows Media Video para comprimir las secuencias. Sin embargo, el contenedor de archivos ASF puede usarse para cualquier tipo de datos. Al colocar los datos multimedia digitales en un contenedor de archivos ASF, puede agregar características proporcionadas por ASF, como metadatos y administración de derechos digitales (DRM), sin tener que transcodificar el contenido.

Para crear un archivo ASF que contenga contenido que no esté basado en Windows Media, la aplicación debe comprimir la secuencia del gráfico de filtros ascendente del escritor ASF de WM y omitir el mecanismo de compresión del escritor ASF de WM llamando a [**IConfigAsfWriter2:: SetParam**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-setparam) como se indica a continuación:


```C++
pConfigAsfWriter2->SetParam(AM_CONFIGASFWRITER_PARAM_DONTCOMPRESS,TRUE,0)
```



A continuación, configure el filtro con el perfil deseado. Es fundamental que el tipo de medio del flujo de entrada coincida exactamente con el formato del perfil. En algunos casos, puede ser necesario examinar el formato del flujo de entrada y crear un perfil personalizado para que coincida con él.

Cuando conecte el escritor ASF de WM al filtro de nivel superior, use el método IGraphBuilder:: ConnectDirect. No use ningún método de "conexión inteligente", como IGraphBuilder:: Connect o IGraphBuilder:: RenderFile, para conectar el filtro porque se deshabilitará el modo "omitir compresión" del filtro.

Captura directa desde un dispositivo a un archivo ASF

Al capturar audio o vídeo directamente en un archivo ASF, el gráfico de filtros tendrá un aspecto similar al siguiente, en función del tipo de dispositivo de captura que se esté usando.

![gráfico de captura de vídeo de Windows Media](images/asf-webcam.png)

Para obtener más información sobre la creación de gráficos de captura de vídeo y audio, vea los temas siguientes:

-   [Captura de audio](audio-capture.md)
-   [Captura de vídeo](video-capture.md)

El escritor ASF de WM no se ejecutará a menos que todos los pin estén conectados. Si configura el escritor ASF de WM con el perfil de sistema predeterminado (no recomendado) o cualquier perfil con secuencias de audio y vídeo, se creará un PIN de entrada para cada flujo y cada uno de esos PIN debe estar conectado. Si no desea capturar audio, por ejemplo, asegúrese de configurar el filtro con un perfil de solo vídeo para que no se cree ningún PIN de audio.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear archivos ASF en DirectShow](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 



