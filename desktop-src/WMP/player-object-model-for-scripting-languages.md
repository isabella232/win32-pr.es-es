---
title: Modelo de objetos del reproductor para lenguajes de scripting
description: Modelo de objetos del reproductor para lenguajes de scripting
ms.assetid: 785c1a3a-902a-4f30-8419-bbfb11b584a3
keywords:
- Media Player de Windows, modelo de objetos
- Modelo de objetos de Windows Media Player, acerca de
- modelo de objetos, acerca de
- Control ActiveX de Windows Media Player, modelo de objetos
- Control ActiveX, modelo de objetos
- Control ActiveX móvil de Windows Media Player, modelo de objetos
- Windows Media Player Mobile, modelo de objetos
- Kit de desarrollo de software (SDK), modelo de objetos de controles ActiveX de Windows Media Player
- SDK (kit de desarrollo de software), modelo de objetos de controles ActiveX de Windows Media Player
- documentación, modelo de objetos de controles ActiveX de Windows Media Player
- Windows Media Player, lenguajes de scripting
- Modelo de objetos de Windows Media Player, lenguajes de scripting
- modelo de objetos, lenguajes de scripting
- Control ActiveX de Windows Media Player, lenguajes de scripting
- Control ActiveX, lenguajes de scripting
- Control ActiveX móvil de Windows Media Player, lenguajes de scripting
- Windows Media Player Mobile, lenguajes de scripting
- lenguajes de scripting
- Media Player de Windows, objeto Player
- Modelo de objetos de Windows Media Player, objeto Player
- modelo de objetos, objeto Player
- Control ActiveX de Windows Media Player, objeto Player
- Control ActiveX, objeto Player
- Control ActiveX móvil de Windows Media Player, objeto Player
- Windows Media Player Mobile, objeto Player
- Objeto Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 670bff03075fd98812dbee269115e297a137e92d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104568865"
---
# <a name="player-object-model-for-scripting-languages"></a>Modelo de objetos del reproductor para lenguajes de scripting

ActiveX utiliza el concepto de objetos para contener la funcionalidad de programación. Windows Media Player utiliza varios objetos para dividir la funcionalidad que proporciona el control. El objeto raíz es el objeto **Player** y los demás objetos se adjuntan al objeto **Player** a través de propiedades específicas.

En el diagrama siguiente se muestra cómo funciona el modelo de objetos de control ActiveX de Windows Media Player 11 para los lenguajes de scripting.

![diagrama del modelo de objetos del reproductor de Windows Media 11](images/playeromdiag.png)

En C++, y a veces en lenguajes .NET, los objetos se representan mediante interfaces COM. En el modelo de objetos de Windows Media Player, los nombres de interfaz COM son los mismos que el nombre de objeto, pero llevan el prefijo "IWMP". Por ejemplo, el objeto de **red** se expone a través de la interfaz **IWMPNetwork** .

En las secciones siguientes se proporcionan información general conceptual para cada objeto:

-   [Acerca de los objetos CDROM y CdromCollection](about-the-cdrom-and-cdromcollection-objects.md)
-   [Acerca del objeto ClosedCaption](about-the-closedcaption-object.md)
-   [Acerca del objeto Controls](about-the-controls-object.md)
-   [Acerca del objeto de DVD](about-the-dvd-object.md)
-   [Acerca de los objetos error y ErrorItem](about-the-error-and-erroritem-objects.md)
-   [Acerca de los objetos MediaCollection y multimedia](about-the-mediacollection-and-media-objects.md)
-   [Acerca del objeto MetadataPicture](about-the-metadatapicture-object.md)
-   [Acerca del objeto MetadataText](about-the-metadatatext-object.md)
-   [Acerca del objeto de red](about-the-network-object.md)
-   [Acerca del objeto Player](about-the-player-object.md)
-   [Acerca del objeto PlayerApplication](about-the-playerapplication-object.md)
-   [Acerca de los objetos playlist, PlaylistCollection y PlaylistArray](about-the-playlist--playlistcollection--and-playlistarray-objects.md)
-   [Acerca del objeto de consulta](about-the-query-object.md)
-   [Acerca del objeto de configuración](about-the-settings-object.md)
-   [Acerca del objeto StringCollection](about-the-stringcollection-object.md)

Hay funcionalidad adicional disponible a través de ciertas interfaces COM. El acceso a estas interfaces puede depender del lenguaje que se use para programar y otros factores, como el modo utilizado para crear la instancia del control Media Player de Windows. Para obtener una lista completa de las interfaces COM que expone el control Media Player de Windows, vea la [Referencia del modelo de objetos de C++](object-model-reference-for-c.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca del modelo de objetos de Player**](about-the-player-object-model.md)
</dt> <dt>

[**Usar el control de Media Player de Windows en una solución de .NET Framework**](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




