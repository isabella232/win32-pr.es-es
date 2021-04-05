---
title: Insertar formatos de secuencias nativas en archivos ASF (QASF)
description: Insertar formatos de secuencias nativas en archivos ASF (QASF)
ms.assetid: ec7a69f3-0d4c-43dd-8d4b-fe066329a98f
keywords:
- SDK de Windows Media Format, formatos de secuencias nativas (QASF)
- SDK de Windows Media Format, insertar formatos de secuencias nativas en archivos ASF (QASF)
- Windows Media Format SDK, DirectShow
- Advanced Systems Format (ASF), insertar formatos de secuencias nativas (QASF)
- ASF (formato de sistemas avanzados), insertar formatos de secuencias nativas (QASF)
- Advanced Systems Format (ASF), formatos de secuencias nativas (QASF)
- ASF (formato de sistemas avanzados), formatos de secuencias nativas (QASF)
- Advanced Systems Format (ASF), DirectShow
- ASF (formato de sistemas avanzados), DirectShow
- DirectShow, formatos de secuencias nativas (QASF)
- DirectShow, insertar formatos de secuencias nativas en archivos ASF (QASF)
- SDK de Windows Media Format, QASF
- Advanced Systems Format (ASF), QASF
- ASF (formato de sistemas avanzados), QASF
- DirectShow, QASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af4736c450b3620a05fe01dcc1808adc297ebbd1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903748"
---
# <a name="inserting-native-stream-formats-into-asf-files-qasf"></a>Insertar formatos de secuencias nativas en archivos ASF (QASF)

De forma predeterminada, el [escritor ASF de WM](wm-asf-writer-filter.md) espera secuencias de audio y vídeo sin comprimir en sus clavijas de entrada y usa el SDK de Windows Media Format para tener acceso a los códecs Windows Media Audio y Windows Media Video, que comprimen las secuencias. Sin embargo, el contenedor de archivos ASF puede usarse para cualquier tipo de datos. Al colocar los datos multimedia digitales en un contenedor de archivos ASF, puede agregar características proporcionadas por ASF, como metadatos y administración de derechos digitales (DRM), sin tener que transcodificar el contenido.

Para crear un archivo ASF que contenga contenido que no esté basado en Windows Media, la aplicación debe comprimir la secuencia del gráfico de filtros ascendente del escritor ASF de WM y omitir el mecanismo de compresión del escritor ASF de WM llamando a [**IConfigAsfWriter2:: SetParam**](iconfigasfwriter2-setparam.md) como se indica a continuación:


```C++
pConfigAsfWriter2->SetParam(AM_CONFIGASFWRITER_PARAM_DONTCOMPRESS,TRUE,0)

```



A continuación, configure el filtro con el perfil deseado. Es fundamental que el tipo de medio del flujo de entrada coincida exactamente con el formato del perfil. En algunos casos, puede ser necesario examinar el formato del flujo de entrada y crear un perfil personalizado para que coincida con él. Para obtener más información, vea [para crear archivos ASF con códecs de terceros](to-create-asf-files-using-third-party-codecs.md).

Cuando conecte el escritor ASF de WM al filtro de nivel superior, use el método **IGraphBuilder:: ConnectDirect** . No use ningún método de "conexión inteligente", como **IGraphBuilder:: Connect** o **IGraphBuilder:: RenderFile** , para conectar el filtro porque se deshabilitará el modo "omitir compresión" del filtro.

 

 




