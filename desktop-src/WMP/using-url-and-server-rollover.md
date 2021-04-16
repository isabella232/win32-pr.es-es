---
title: Usar URL y sustitución de servidor
description: Usar URL y sustitución de servidor
ms.assetid: d0d15b1c-5631-486e-8490-b85ec51bd355
keywords:
- Listas de reproducción de metarchivos de Windows Media, sustitución de direcciones URL
- listas de reproducción, sustitución de direcciones URL
- listas de reproducción de metarchivos, sustitución de direcciones URL
- Listas de reproducción de metarchivos de Windows Media, sustituciones de servidor
- listas de reproducción, sustitución de servidor
- listas de reproducción de metarchivos, sustitución de servidor
- Listas de reproducción de metarchivos de Windows Media, sustitución de protocolo
- listas de reproducción, sustitución de protocolo
- listas de reproducción de metarchivos, sustitución de protocolo
- Windows Media Player, sustitución de direcciones URL
- Windows Media Player, sustitución de servidor
- Windows Media Player, sustitución de protocolos
- Sustitución de direcciones URL
- sustituciones de servidor
- sustituciones de protocolo
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: eae38e81f8ae23199628e543f65f2766491f1a2a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357167"
---
# <a name="using-url-and-server-rollover"></a>Usar URL y sustitución de servidor

Puede usar listas de reproducción de metarchivos para proporcionar un medio de propagación automática a orígenes de contenido alternativo cuando no se puede tener acceso a una secuencia o reproducirla. Puede usar este método de sustitución incremental para especificar orígenes del mismo contenido en distintos servidores o en diferentes tipos de servidores. Por ejemplo, puede especificar una primera alternativa en otro servidor de Windows Media. Si no se puede reproducir el contenido, el cliente puede pasar a una segunda alternativa en un servidor Web. Windows Media Player intenta revertir automáticamente a protocolos diferentes según su configuración de propiedades de Windows Media antes de probar las direcciones URL de sustitución en la lista de reproducción.

Establezca la sustitución de servidor y protocolo colocando varios elementos **ref** en sucesión dentro de un elemento de **entrada** . Cada elemento **ref** especifica una ubicación alternativa o protocolo para un archivo multimedia o una secuencia.

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

[**Crear listas de reproducción de metarchivo**](creating-metafile-playlists.md)
</dt> <dt>

[**Usar listas de reproducción de metarchivo**](using-metafile-playlists.md)
</dt> </dl>

 

 




