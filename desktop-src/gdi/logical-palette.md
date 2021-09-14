---
description: Una paleta lógica es una paleta de colores que una aplicación crea y asocia a un contexto de dispositivo determinado.
ms.assetid: 7cc86771-237d-4539-8f48-2474edb764a4
title: Paleta lógica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 597e049c4320ff3ac30099e767c35a3438237904
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127258084"
---
# <a name="logical-palette"></a>Paleta lógica

Una *paleta lógica es* una paleta de colores que una aplicación crea y asocia a un contexto de dispositivo determinado. Las paletas lógicas permiten a las aplicaciones definir y usar colores que satisfagan sus necesidades específicas. Las aplicaciones pueden crear cualquier número de paletas lógicas, usándolos para contextos de dispositivo independientes o cambiando entre ellos para un único contexto de dispositivo. El número máximo de paletas que puede crear una aplicación depende de los recursos del sistema.

Una aplicación crea una paleta lógica mediante la [**función CreatePalette.**](/windows/desktop/api/Wingdi/nf-wingdi-createpalette) La aplicación rellena una estructura [**LOGPALETTE,**](/windows/win32/api/wingdi/ns-wingdi-logpalette) que especifica el número de entradas y los valores de color de cada entrada y, a continuación, la aplicación pasa la estructura a **CreatePalette.** La función devuelve un identificador de paleta que la aplicación usa en todas las operaciones posteriores para identificar la paleta. Para usar colores en la paleta lógica, la aplicación selecciona la paleta en un contexto de dispositivo mediante la función [**SelectPalette**](/windows/desktop/api/Wingdi/nf-wingdi-selectpalette) y, a continuación, realiza la paleta mediante la [**función RealizePalette.**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) Los colores de la paleta están disponibles en cuanto se realiza la paleta lógica.

Una aplicación debe limitar el tamaño de sus paletas lógicas a entradas suficientes para representar los colores necesarios. Las aplicaciones no pueden crear paletas lógicas mayores que el tamaño máximo de la paleta, un valor dependiente del dispositivo. Las aplicaciones pueden obtener el tamaño máximo mediante la [**función GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) para recuperar el valor SIZEPALETTE.

Aunque una aplicación puede especificar cualquier valor de color para una entrada determinada en una paleta lógica, el dispositivo determinado no puede generar todos los colores. El sistema no proporciona una manera de detectar qué colores se admiten, pero la aplicación puede detectar el número total de estos colores mediante la recuperación de la resolución de color del dispositivo. La resolución de color, especificada en bits de color por píxel, es igual al valor COLORRES devuelto por la [**función GetDeviceCaps.**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) Un dispositivo con una resolución de color de 18 tiene 262 144 colores posibles. Si una aplicación solicita un color que no se admite, el sistema elige una aproximación adecuada.

Una vez creada una paleta lógica, una aplicación puede cambiar los colores de la paleta mediante la [**función SetPaletteEntries.**](/windows/desktop/api/Wingdi/nf-wingdi-setpaletteentries) Si la paleta lógica se ha seleccionado y realizado, cambiar la paleta no afecta inmediatamente a los colores que se muestran. La aplicación debe usar las [**funciones UnrealizeObject**](/windows/desktop/api/Wingdi/nf-wingdi-unrealizeobject) y [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) para actualizar los colores. En algunos casos, es posible que la aplicación deba anular la selección, anular la realización, seleccionar y realizar la paleta lógica para asegurarse de que los colores se actualizan exactamente como se solicitó. Si una aplicación selecciona una paleta lógica en más de un contexto de dispositivo, los cambios en la paleta lógica afectan a todos los contextos de dispositivo para los que está seleccionada.

Una aplicación puede cambiar el número de entradas de una paleta lógica mediante la [**función ResizePalette.**](/windows/desktop/api/Wingdi/nf-wingdi-resizepalette) Si la aplicación reduce el tamaño, las entradas restantes no se modifican. Si la aplicación amplía el tamaño, el sistema establece el color de cada nueva entrada en negro (0, 0, 0) y la marca en cero.

Una aplicación puede recuperar los valores de color y marca de las entradas de una paleta lógica determinada mediante la [**función GetPaletteEntries.**](/windows/desktop/api/Wingdi/nf-wingdi-getpaletteentries) Una aplicación puede recuperar el índice de la entrada en una paleta lógica determinada que coincida más estrechamente con un valor de color especificado mediante la función [**GetNearestPaletteIndex.**](/windows/desktop/api/Wingdi/nf-wingdi-getnearestpaletteindex)

Cuando una aplicación ya no necesita una paleta lógica, puede eliminarla mediante la [**función DeleteObject.**](/windows/desktop/api/Wingdi/nf-wingdi-deleteobject) La aplicación debe asegurarse de que la paleta lógica ya no esté seleccionada en un contexto de dispositivo antes de eliminar la paleta.

 

 



