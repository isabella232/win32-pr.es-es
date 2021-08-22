---
description: Para crear un mapa de bits, use las funciones CreateBitmap, CreateBitmapIndirect o CreateCompatibleBitmap, CreateDIBitmap y CreateDiscardableBitmap.
ms.assetid: 313072fc-68c9-4ece-95bb-2748ccbd7f57
title: Creación de mapas de bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db37dd14f8be47ebf93c7ee7f586c54c2e55ea900402d9c255a3196987aaed43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119038263"
---
# <a name="bitmap-creation"></a>Creación de mapas de bits

Para crear un mapa de bits, use las funciones [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap), [**CreateBitmapIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect)o [**CreateCompatibleBitmap,**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) [**CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap)y [**CreateDiscardableBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap).

Estas funciones permiten especificar el ancho y alto, en píxeles, del mapa de bits. Las [**funciones CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap) y [**CreateBitmapIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect) también permiten especificar el número de planos de color y el número de bits necesarios para identificar el color. Por otro lado, las funciones [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) y [**CreateDiscardableBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap) usan un contexto de dispositivo especificado para obtener el número de planos de color y el número de bits necesarios para identificar el color.

La [**función CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap) crea un mapa de bits dependiente del dispositivo a partir de un mapa de bits independiente del dispositivo. Contiene una tabla de colores que describe cómo se corresponden los valores de píxel con los valores de color RGB. Para obtener más información, vea [Mapas de bits dependientes del dispositivo y](device-dependent-bitmaps.md) Mapas de bits independientes del [dispositivo.](device-independent-bitmaps.md)

Una vez creado el mapa de bits, no puede cambiar su tamaño, número de planos de color o número de bits necesarios para identificar el color.

Cuando ya no necesite un mapa de bits, llame a [**la función DeleteObject**](/windows/desktop/api/Wingdi/nf-wingdi-deleteobject) para eliminarlo.

 

 



