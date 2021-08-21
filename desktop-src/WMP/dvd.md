---
title: DVD
description: DVD
ms.assetid: b3634a28-b1d6-44a5-97e4-fcc1f655d652
keywords:
- Reproductor de Windows Media, migrar DVD
- Reproductor de Windows Media de objetos, DVD
- object model,DVDs
- Reproductor de Windows Media ActiveX control,DVDs
- ActiveX control,DVDs
- Reproductor de Windows Media Control de ActiveX móviles, DVDs
- Reproductor de Windows Media Mobile,migrating DVDs
- guía de migración, DVDs
- Migración de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 178d07d87bf9c36b982893febb5354251e1cf4ba97cf9c29bfe7bad29e1480fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118839421"
---
# <a name="dvd"></a>DVD

El control Reproductor de Windows Media 6.4 ActiveX contiene un objeto **DVD** que expone una variedad de métodos y propiedades, y un evento, para tratar específicamente con contenido de DVD. Por ejemplo, para determinar el número de títulos de DVD disponibles, use **player6**. **titlesAvailable,** propiedad:


```C++
var numTitles = WMP64.DVD.TitlesAvailable;

```



El Reproductor de Windows Media objeto 7 o posterior implementa un enfoque más integrado para EL DVD. Las propiedades, métodos y eventos específicos de DVD se implementan solo cuando es necesario. De lo contrario, la funcionalidad del modelo de objetos existente funciona con medios de DVD como se podría esperar. Por ejemplo, para determinar el número de títulos de DVD disponibles al usar Reproductor de Windows Media 7 o posterior, recupere un objeto **Playlist** del **objeto Cdrom:**


```C++
var dvdTitles = WMP9.cdromCollection.item(0).playlist;

```



En el ejemplo anterior se recupera un objeto **Playlist** con una primera entrada que representa el medio de DVD en la primera unidad. Las entradas adicionales representan títulos de DVD individuales. Por lo tanto, el número de títulos disponibles se puede calcular de la manera siguiente:


```C++
var numTitles = dvdTitles.count - 1;

```



Estas son las principales diferencias que se tienen en cuenta al migrar desde la versión 6.4:

-   La reproducción de DVD solo se admite cuando se Reproductor de Windows Media para Windows XP o posterior y el Windows operativo XP o posterior.
-   Las unidades de DVD-ROM se enumeran exactamente igual que las unidades de CD-ROM mediante el **objeto CdromCollection.**
-   Las unidades de DVD-ROM individuales se administran mediante el **objeto Cdrom.**
-   El **objeto DVD** amplía el modelo de objetos con métodos y una propiedad específicamente para trabajar con DVD.
-   Hay dos nuevos eventos, **OpenPlaylistSwitch** y **DomainChange,** específicamente para trabajar con DVD.
-   El contenido de DVD se organiza mediante **objetos De lista** de reproducción y **Objetos** multimedia.
-   Los idiomas de DVD se administran mediante la funcionalidad de lenguaje disponible en el objeto **Controls** (Reproductor de Windows Media serie 9 o posterior).
-   Los controles de transporte y la información de posición del DVD funcionan igual que para otros tipos de medios digitales.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de migración del modelo de objetos**](object-model-migration-guide.md)
</dt> <dt>

[**Usar el control Reproductor de Windows Media con Visual Basic**](using-the-windows-media-player-control-with-visual-basic.md)
</dt> </dl>

 

 




