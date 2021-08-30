---
description: El sistema controla los colores en mapas de bits de forma diferente a los colores de los lápices, pinceles y texto.
ms.assetid: c315dd6e-87ee-4905-b193-186ea580ac0a
title: Color en mapas de bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 782951cfaee0d50fe426505868d01bc5d3fd791f9d8ea0b1e3bca94e28680b7d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119849251"
---
# <a name="color-in-bitmaps"></a>Color en mapas de bits

El sistema controla los colores en mapas de bits de forma diferente a los colores de los lápices, pinceles y texto. Los mapas de bits compatibles, creados mediante la [**función CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap) o [**CreateCompatibleBitmap,**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) son específicos del dispositivo y conservan la información de color en un formato dependiente del dispositivo. No se usan valores de color y los colores no están sujetos a aproximaciones ni a dithering.

Los mapas de bits independientes del dispositivo (DIB) conservan la información de color como valores de color o índices de paleta de colores. Si se usan valores de color, los colores están sujetos a aproximación, pero no a dithering. Los índices de paleta de colores solo se pueden usar con dispositivos que admiten paletas de colores. Aunque el sistema no aproxima ni dite los colores identificados por los índices, el color resultante puede ser diferente del previsto, ya que los índices producen resultados válidos solo en el contexto de la paleta de colores que estaba actual en el momento en que se creó el mapa de bits. Si cambia la paleta, haga lo mismo con los colores del mapa de bits. Para obtener más información sobre los índices de paleta, vea [Paleta predeterminada y](default-palette.md) [**PALETTEINDEX.**](/windows/desktop/api/Wingdi/nf-wingdi-paletteindex)

Además de hacer referencia a la paleta lógica, una aplicación también puede hacer referencia a un valor en una tabla de colores DIB. Para seleccionar un color en una tabla de colores DIB, llame a [**DIBINDEX**](/windows/desktop/api/Mmsystem/nf-mmsystem-dibindex). Tenga en cuenta que esto solo es posible para un contexto de dispositivo que tenga una DIB seleccionada en él.

 

 



