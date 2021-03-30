---
title: DVD
description: DVD
ms.assetid: b3634a28-b1d6-44a5-97e4-fcc1f655d652
keywords:
- Windows Media Player, migrar DVDs
- Modelo de objetos de Windows Media Player, DVDs
- modelo de objetos, DVDs
- Control ActiveX de Windows Media Player, DVDs
- Control ActiveX, DVDs
- Control ActiveX móvil de Windows Media Player, DVDs
- Windows Media Player Mobile, migrar DVDs
- Guía de migración, DVDs
- Migración de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05e0a19818ac01b5e3d6138f896f26fe674c5ef2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777161"
---
# <a name="dvd"></a>DVD

El control ActiveX de Windows Media Player 6,4 contiene un objeto de **DVD** que expone diversos métodos y propiedades, así como un evento, para tratar específicamente con el contenido del DVD. Por ejemplo, para determinar el número de títulos de DVD disponibles, se usa **Player6**. propiedad **titlesAvailable** :


```C++
var numTitles = WMP64.DVD.TitlesAvailable;

```



El modelo de objetos de Windows Media Player 7 o posterior implementa un enfoque más integrado en DVD. Las propiedades, los métodos y los eventos específicos de DVD solo se implementan si es necesario. De lo contrario, la funcionalidad del modelo de objetos existente funciona con los medios de DVD como cabría esperar. Por ejemplo, para determinar el número de títulos de DVD disponibles cuando se usa Windows Media Player 7 o posterior, se recupera un objeto de **lista de reproducción** del objeto **CDROM** :


```C++
var dvdTitles = WMP9.cdromCollection.item(0).playlist;

```



En el ejemplo anterior se recupera un objeto de **lista de reproducción** con una primera entrada que representa el DVD de la primera unidad. Las entradas adicionales representan títulos de DVD individuales. Por lo tanto, el número de títulos disponibles se puede calcular de la manera siguiente:


```C++
var numTitles = dvdTitles.count - 1;

```



Estas son las principales diferencias a tener en cuenta al migrar desde la versión 6,4:

-   La reproducción de DVD solo se admite cuando se usa Windows Media Player para Windows XP o posterior y el sistema operativo Windows XP o posterior.
-   Las unidades de DVD-ROM se enumeran exactamente igual que las unidades de CD-ROM mediante el objeto **CdromCollection** .
-   Las unidades de DVD-ROM individuales se administran mediante el objeto **CDROM** .
-   El objeto **DVD** extiende el modelo de objetos con métodos y una propiedad específicamente para trabajar con DVD.
-   Hay dos nuevos eventos, **OpenPlaylistSwitch** y **DomainChange**, específicamente para trabajar con DVD.
-   El contenido del DVD se organiza mediante objetos de **lista de reproducción** y objetos **multimedia** .
-   Los idiomas de DVD se administran mediante la funcionalidad de lenguaje disponible en el objeto **Controls** (Windows Media Player 9 series o posterior).
-   Los controles de transporte y la información de posición para DVD funcionan igual que para otros tipos de medios digitales.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de migración del modelo de objetos**](object-model-migration-guide.md)
</dt> <dt>

[**Usar el control Media Player de Windows con Visual Basic**](using-the-windows-media-player-control-with-visual-basic.md)
</dt> </dl>

 

 




