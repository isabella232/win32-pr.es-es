---
title: Uso de url y suversión de servidor
description: Uso de url y suversión de servidor
ms.assetid: d0d15b1c-5631-486e-8490-b85ec51bd355
keywords:
- Windows Listas de reproducción de metarchivo multimedia, sustecciones de direcciones URL
- playlists,url rollovers
- listas de reproducción de metarchivo, sustecciones de direcciones URL
- Windows Listas de reproducción de metarchivo multimedia, sustecciones de servidor
- listas de reproducción, sudores de servidor
- listas de reproducción de metarchivo, sustecciones de servidor
- Windows Listas de reproducción de metarchivo multimedia, sustecciones de protocolo
- listas de reproducción, sudores de protocolo
- listas de reproducción de metarchivo, sustecciones de protocolo
- Reproductor de Windows Media,subaciones de dirección URL
- Reproductor de Windows Media,subrecuperaciones de servidor
- Reproductor de Windows Media,subrecuperaciones de protocolo
- Subaciones de direcciones URL
- subaciones de servidor
- subaciones de protocolo
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: eae38e81f8ae23199628e543f65f2766491f1a2a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359873"
---
# <a name="using-url-and-server-rollover"></a>Uso de url y suversión de servidor

Puede usar listas de reproducción de metarchivo para proporcionar un medio de revertir automáticamente a orígenes de contenido alternativos cuando no se puede acceder a una secuencia ni reproducirla. Puede usar este método de suversión para especificar orígenes del mismo contenido en servidores diferentes o en distintos tipos de servidores. Por ejemplo, puede especificar una primera alternativa en un servidor Windows Media. Si ese contenido no se puede reproducir, el cliente puede revertir a una segunda alternativa en un servidor web. Reproductor de Windows Media automáticamente intenta revertir a distintos protocolos según la configuración de la propiedad Windows Media antes de probar las direcciones URL de suversión en la lista de reproducción.

Establezca la suvolución de servidor y protocolo **colocando** varios elementos REF en sucesión dentro de un **elemento ENTRY.** Cada **elemento REF** especifica una ubicación o protocolo alternativos para un archivo multimedia o una secuencia.

Código de ejemplo


```XML
<!--Server and protocol rollover is set for the file Rollover.wma.-->
<ASX version="3.0">
    <TITLE>MyServer Rollover</TITLE>
   <ENTRY>
      <REF HREF="mms://Server1.proseware.com/Path/Rollover.wma"/>
      <REF HREF="mms://Server2.proseware.com/Path/Rollover.wma"/>
      <REF HREF="mms://Server3.proseware.com/Path/Rollover.wma"/>
      <REF HREF="https://www.proseware.com/Path/Rollover.wma"/>
   </ENTRY>
</ASX>

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Creación de listas de reproducción de metarchivo**](creating-metafile-playlists.md)
</dt> <dt>

[**Uso de listas de reproducción de metarchivo**](using-metafile-playlists.md)
</dt> </dl>

 

 




