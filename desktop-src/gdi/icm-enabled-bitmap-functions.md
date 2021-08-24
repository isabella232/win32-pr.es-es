---
description: Microsoft Image Color Management (ICM) garantiza que una imagen de color, un objeto gráfico u objeto de texto se represente lo más cerca posible de su intención original en cualquier dispositivo, a pesar de las diferencias en las tecnologías de creación de imágenes y las funcionalidades de color entre dispositivos.
ms.assetid: 7b3cb9a4-ffd2-4867-85bd-0e663fdde6e3
title: ICM-Enabled de mapa de bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d38341851eb9ba2aed25cc93afbf7b869909430a30ecb626bf3a452883fdea97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831975"
---
# <a name="icm-enabled-bitmap-functions"></a>ICM-Enabled de mapa de bits

Microsoft Image Color Management (ICM) garantiza que una imagen de color, un objeto gráfico u objeto de texto se represente lo más cerca posible de su intención original en cualquier dispositivo, a pesar de las diferencias en las tecnologías de creación de imágenes y las funcionalidades de color entre dispositivos. Tanto si va a examinar una imagen u otro gráfico en un escáner de colores, descargarla a través de Internet, visualizarla o editarla en pantalla, o imprimirla en papel, película u otros medios, ICM 2.0 le ayuda a mantener los colores coherentes y precisos. Para obtener más información sobre ICM, [vea Windows Color System](/previous-versions//dd372446(v=vs.85)).

Hay varias funciones en la interfaz del dispositivo gráfico (GDI) que usan o funcionan con datos de color. Las siguientes funciones de mapa de bits están habilitadas para su uso con ICM:

-   [**BitBlt**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt)
-   [**CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap)
-   [**CreateDIBSection**](/windows/desktop/api/Wingdi/nf-wingdi-createdibsection)
-   [**MaskBlt**](/windows/desktop/api/Wingdi/nf-wingdi-maskblt)
-   [**SetDIBColorTable**](/windows/desktop/api/Wingdi/nf-wingdi-setdibcolortable)
-   [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt)
-   [**SetDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-setdibits)
-   [**SetDIBitsToDevice**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice)
-   [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits)

 

 
