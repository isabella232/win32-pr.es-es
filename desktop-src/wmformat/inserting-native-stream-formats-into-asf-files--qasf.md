---
title: Insertar formatos de flujo nativos en archivos ASF (QASF)
description: Insertar formatos de flujo nativos en archivos ASF (QASF)
ms.assetid: ec7a69f3-0d4c-43dd-8d4b-fe066329a98f
keywords:
- Windows SDK de formato multimedia, formatos de secuencia nativos (QASF)
- Windows SDK de formato multimedia, inserción de formatos de secuencia nativos en archivos ASF (QASF)
- Windows SDK de formato multimedia, DirectShow
- Formato de sistemas avanzados (ASF), insertar formatos de flujo nativos (QASF)
- ASF (formato de sistemas avanzados), insertar formatos de flujo nativos (QASF)
- Formato de sistemas avanzados (ASF), formatos de flujo nativos (QASF)
- ASF (formato de sistemas avanzados), formatos de flujo nativos (QASF)
- Formato de sistemas avanzados (ASF), DirectShow
- ASF (formato de sistemas avanzados), DirectShow
- DirectShow, formatos de flujo nativos (QASF)
- DirectShow, insertar formatos de flujo nativos en archivos ASF (QASF)
- Windows SDK de formato multimedia, QASF
- Formato de sistemas avanzados (ASF),QASF
- ASF (formato de sistemas avanzados),QASF
- DirectShow,QASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b395748520943a62645a88c018131f909577191ebafbe1f9c4d3a80219cb39f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118701782"
---
# <a name="inserting-native-stream-formats-into-asf-files-qasf"></a>Insertar formatos de flujo nativos en archivos ASF (QASF)

De forma predeterminada, [WM ASF Writer](wm-asf-writer-filter.md) espera secuencias de audio y vídeo sin comprimir en sus pines de entrada y usa el SDK de formato multimedia de Windows para acceder a los códecs Windows Media Audio y Windows Media Video, que comprimen las secuencias. Pero el contenedor de archivos ASF se puede usar para cualquier tipo de datos. Al colocar datos multimedia digitales en un contenedor de archivos ASF, puede agregar características proporcionadas por ASF, como metadatos y administración de derechos digitales (DRM), sin tener que transcodificar el contenido.

Para crear un archivo ASF que contenga contenido que no esté basado en medios de Windows, la aplicación debe comprimir la secuencia en el gráfico de filtro ascendente del escritor de ASF de WM y omitir el mecanismo de compresión del escritor de ASF wm llamando a [**IConfigAsfWriter2::SetParam**](iconfigasfwriter2-setparam.md) de la siguiente manera:


```C++
pConfigAsfWriter2->SetParam(AM_CONFIGASFWRITER_PARAM_DONTCOMPRESS,TRUE,0)

```



A continuación, configure el filtro con el perfil deseado. Es esencial que el tipo de medio del flujo de entrada coincida exactamente con el formato del perfil. En algunos casos, puede ser necesario examinar el formato del flujo de entrada y crear un perfil personalizado para que coincida con él. Para obtener más información, [vea Para crear archivos ASF mediante códecs de terceros.](to-create-asf-files-using-third-party-codecs.md)

Cuando conecte WM ASF Writer al filtro ascendente, use el **método IGraphBuilder::ConnectDirect.** No use ningún método de "conexión inteligente", como **IGraphBuilder::Conectar** o **IGraphBuilder::RenderFile,** para conectar el filtro, ya que esto deshabilitará el modo de "compresión de omisión" del filtro.

 

 




