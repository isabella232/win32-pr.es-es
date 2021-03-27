---
description: El sistema controla los colores de los mapas de bits de forma distinta a los colores de los lápices, los pinceles y el texto.
ms.assetid: c315dd6e-87ee-4905-b193-186ea580ac0a
title: Color en mapas de bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 834744f35ccc8bd0c8714fa5bbb438b59c8b8db3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155664"
---
# <a name="color-in-bitmaps"></a>Color en mapas de bits

El sistema controla los colores de los mapas de bits de forma distinta a los colores de los lápices, los pinceles y el texto. Los mapas de bits compatibles, creados mediante la función [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap) o [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) , son específicos del dispositivo y conservan la información de color en un formato dependiente del dispositivo. No se usan valores de color y los colores no están sujetos a las aproximaciones y al tramado.

Los mapas de bits independientes del dispositivo (DIB) conservan la información de color como valores de color o índices de paleta de colores. Si se usan valores de color, los colores están sujetos a la aproximación, pero no a la interpolación. Los índices de paleta de colores solo se pueden usar con dispositivos que admiten paletas de colores. Aunque el sistema no aproxima ni trama los colores identificados por los índices, el color resultante puede ser diferente del previsto, ya que los índices producen resultados válidos solo en el contexto de la paleta de colores que era actual en el momento en que se creó el mapa de bits. Si la paleta cambia, haga lo mismo con los colores del mapa de bits. Para obtener más información sobre los índices de paleta, vea [paleta predeterminada](default-palette.md) y [**PALETTEINDEX**](/windows/desktop/api/Wingdi/nf-wingdi-paletteindex).

Además de hacer referencia a la paleta lógica, una aplicación también puede hacer referencia a un valor en una tabla de colores DIB. Para seleccionar un color en una tabla de colores DIB, llame a [**DIBINDEX**](/windows/desktop/api/Mmsystem/nf-mmsystem-dibindex). Tenga en cuenta que esto solo es posible para un contexto de dispositivo que tenga un DIB seleccionado en él.

 

 



