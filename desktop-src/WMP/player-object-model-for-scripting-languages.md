---
title: Modelo de objetos del reproductor para lenguajes de scripting
description: Modelo de objetos del reproductor para lenguajes de scripting
ms.assetid: 785c1a3a-902a-4f30-8419-bbfb11b584a3
keywords:
- Reproductor de Windows Media,modelo de objetos
- Reproductor de Windows Media de objetos, acerca de
- object model,about
- Reproductor de Windows Media ActiveX control,modelo de objetos
- ActiveX control,modelo de objetos
- Reproductor de Windows Media Control de ActiveX móvil,modelo de objetos
- Reproductor de Windows Media Móvil, modelo de objetos
- kit de desarrollo de software (SDK), Reproductor de Windows Media ActiveX de objetos de control
- SDK (kit de desarrollo de software), Reproductor de Windows Media ActiveX de objetos de control
- documentation,Reproductor de Windows Media ActiveX de objetos de control
- Reproductor de Windows Media,lenguajes de scripting
- Reproductor de Windows Media de objetos, lenguajes de scripting
- modelo de objetos, lenguajes de scripting
- Reproductor de Windows Media ActiveX control, lenguajes de scripting
- ActiveX control, lenguajes de scripting
- Reproductor de Windows Media Control de ActiveX móviles, lenguajes de scripting
- Reproductor de Windows Media Móvil, lenguajes de scripting
- lenguajes de scripting
- Reproductor de Windows Media,Objeto Player
- Reproductor de Windows Media modelo de objetos, objeto Player
- object model,Player object
- Reproductor de Windows Media ActiveX control, objeto Player
- ActiveX control, objeto Player
- Reproductor de Windows Media Control de ActiveX móvil, objeto Player
- Reproductor de Windows Media Objeto Mobile,Player
- Objeto Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bffe34bfc227dfe250a9c9d7ebb60977a9ab079c4a062067c65e83e62f0e5976
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996035"
---
# <a name="player-object-model-for-scripting-languages"></a>Modelo de objetos del reproductor para lenguajes de scripting

ActiveX utiliza el concepto de objetos para contener la funcionalidad de programación. Reproductor de Windows Media utiliza varios objetos para dividir la funcionalidad que proporciona el control. El objeto raíz es el **objeto Player** y los demás objetos se adjuntan al **objeto Player** a través de propiedades específicas.

En el diagrama siguiente se muestra cómo funciona Reproductor de Windows Media modelo de objetos de control ActiveX 11 para lenguajes de scripting.

![diagrama del modelo de objetos del Reproductor de Windows Media 11](images/playeromdiag.png)

En C++, y a veces en lenguajes .NET, los objetos se representan mediante interfaces COM. En el Reproductor de Windows Media de objetos, los nombres de interfaz COM son los mismos que el nombre del objeto, pero tienen el prefijo "IWMP". Por ejemplo, el **objeto Network** se expone a través de la **interfaz IWMPNetwork.**

En las secciones siguientes se proporcionan información general conceptual para cada objeto:

-   [Acerca de los objetos Cdrom y CdromCollection](about-the-cdrom-and-cdromcollection-objects.md)
-   [Acerca del objeto ClosedCaption](about-the-closedcaption-object.md)
-   [Acerca del objeto Controls](about-the-controls-object.md)
-   [Acerca del objeto DVD](about-the-dvd-object.md)
-   [Acerca de los objetos Error y ErrorItem](about-the-error-and-erroritem-objects.md)
-   [Acerca de Los objetos MediaCollection y Media](about-the-mediacollection-and-media-objects.md)
-   [Acerca del objeto MetadataPicture](about-the-metadatapicture-object.md)
-   [Acerca del objeto MetadataText](about-the-metadatatext-object.md)
-   [Acerca del objeto de red](about-the-network-object.md)
-   [Acerca del objeto Player](about-the-player-object.md)
-   [Acerca del objeto PlayerApplication](about-the-playerapplication-object.md)
-   [Acerca de los objetos Playlist, PlaylistCollection y PlaylistArray](about-the-playlist--playlistcollection--and-playlistarray-objects.md)
-   [Acerca del objeto de consulta](about-the-query-object.md)
-   [Acerca del objeto Configuración](about-the-settings-object.md)
-   [Acerca del objeto StringCollection](about-the-stringcollection-object.md)

Hay funcionalidad adicional disponible a través de determinadas interfaces COM. Si puede acceder a estas interfaces puede depender del lenguaje que use para la programación y otros factores, como el modo utilizado para crear la instancia del control Reproductor de Windows Media. Para obtener una lista completa de las interfaces COM expuestas por el control Reproductor de Windows Media, vea referencia del modelo de [objetos para C++.](object-model-reference-for-c.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca del modelo de objetos del reproductor**](about-the-player-object-model.md)
</dt> <dt>

[**Usar el control Reproductor de Windows Media en una .NET Framework solución**](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




