---
description: Para crear un mapa de bits, use las funciones CreateBitmap, CreateBitmapIndirect o CreateCompatibleBitmap, CreateDIBitmap y CreateDiscardableBitmap.
ms.assetid: 313072fc-68c9-4ece-95bb-2748ccbd7f57
title: Creación de mapas de bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d00a0bc5a39d1b5e6053a34a87c28d6792a42b0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276025"
---
# <a name="bitmap-creation"></a>Creación de mapas de bits

Para crear un mapa de bits, use las funciones [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap), [**CreateBitmapIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect)o [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) , [**CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap)y [**CreateDiscardableBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap).

Estas funciones permiten especificar el ancho y el alto, en píxeles, del mapa de bits. Las funciones [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap) y [**CreateBitmapIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect) también permiten especificar el número de planos de color y el número de bits necesarios para identificar el color. Por otro lado, las funciones [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) y [**CreateDiscardableBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap) utilizan un contexto de dispositivo especificado para obtener el número de planos de color y el número de bits necesarios para identificar el color.

La función [**CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap) crea un mapa de bits dependiente del dispositivo a partir de un mapa de bits independiente del dispositivo. Contiene una tabla de colores que describe cómo se corresponden los valores de píxeles con los valores de color RGB. Para obtener más información, consulte [mapas de bits dependientes del dispositivo](device-dependent-bitmaps.md) y [mapas de bits independientes del dispositivo](device-independent-bitmaps.md).

Una vez creado el mapa de bits, no se puede cambiar su tamaño, el número de planos de color o el número de bits necesario para identificar el color.

Cuando ya no necesite un mapa de bits, llame a la función [**DeleteObject**](/windows/desktop/api/Wingdi/nf-wingdi-deleteobject) para eliminarlo.

 

 



