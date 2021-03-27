---
description: La administración del color de imagen (ICM) de Microsoft garantiza que una imagen de color, un objeto gráfico o un objeto de texto se representan lo más cerca posible de su intención original en cualquier dispositivo, a pesar de las diferencias en las tecnologías de creación de imágenes y las capacidades de color entre los dispositivos.
ms.assetid: 7b3cb9a4-ffd2-4867-85bd-0e663fdde6e3
title: ICM-Enabled funciones de mapa de bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4b89dac569aafad1ef94b066bc97f588bac62c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908485"
---
# <a name="icm-enabled-bitmap-functions"></a>ICM-Enabled funciones de mapa de bits

La administración del color de imagen (ICM) de Microsoft garantiza que una imagen de color, un objeto gráfico o un objeto de texto se representan lo más cerca posible de su intención original en cualquier dispositivo, a pesar de las diferencias en las tecnologías de creación de imágenes y las capacidades de color entre los dispositivos. Tanto si está digitalizando una imagen como en otro gráfico en un escáner de color, descargándolo a través de Internet, viéndolo o editándolo en pantalla o imprimiendo en papel, película u otros medios, ICM 2,0 le ayuda a mantener la coherencia y la precisión de los colores. Para obtener más información acerca de ICM, consulte [sistema de color de Windows](/previous-versions//dd372446(v=vs.85)).

Hay varias funciones en la interfaz de dispositivo gráfico (GDI) que utilizan o operan en los datos de color. Las siguientes funciones de mapa de bits están habilitadas para su uso con ICM:

-   [**BitBlt**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt)
-   [**CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap)
-   [**CreateDIBSection**](/windows/desktop/api/Wingdi/nf-wingdi-createdibsection)
-   [**MaskBlt**](/windows/desktop/api/Wingdi/nf-wingdi-maskblt)
-   [**SetDIBColorTable**](/windows/desktop/api/Wingdi/nf-wingdi-setdibcolortable)
-   [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt)
-   [**SetDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-setdibits)
-   [**SetDIBitsToDevice**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice)
-   [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits)

 

 
