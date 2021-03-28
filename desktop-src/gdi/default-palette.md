---
description: La paleta predeterminada es una matriz de valores de color que identifican los colores que se pueden usar con un contexto de dispositivo de forma predeterminada.
ms.assetid: 7972d5da-2b73-4cd7-a2ee-fca3a571f611
title: Paleta predeterminada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c100eeb144ab4f6483281b33739578642880a91f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908500"
---
# <a name="default-palette"></a>Paleta predeterminada

La *paleta predeterminada* es una matriz de valores de color que identifican los colores que se pueden usar con un contexto de dispositivo de forma predeterminada. el sistema asocia la paleta predeterminada a un contexto siempre que una aplicación crea un contexto para un dispositivo que admite paletas de colores. La paleta predeterminada garantiza que los colores estén disponibles para su uso por parte de una aplicación sin realizar ninguna otra acción.

Normalmente, la paleta predeterminada tiene 20 entradas (colores), pero el número exacto de entradas puede variar de un dispositivo a un dispositivo. Este número es igual al valor NUMCOLORS devuelto por la función [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) . Una aplicación puede recuperar los valores de color de los colores de la paleta predeterminada enumerando bolígrafos sólidos, la misma técnica que se usa para detectar los colores disponibles en los dispositivos que no son de paleta. Los colores de la paleta predeterminada dependen del dispositivo. Los dispositivos de visualización, por ejemplo, suelen usar los 16 colores estándar de la pantalla VGA y otros 4 colores definidos por Windows. Los dispositivos de impresión pueden usar otros colores predeterminados.

Cuando se usa la paleta predeterminada, las aplicaciones usan valores de color para especificar los colores del lápiz y del texto. Si el color solicitado no está en la paleta, el sistema lo aproxima con el color más cercano de la paleta. Si una aplicación solicita un color de pincel sólido que no está en la paleta, el sistema simula el color interpolando con los colores que se encuentran en la paleta.

Para evitar las aproximaciones y el tramado, las aplicaciones también pueden especificar colores de lápiz, pincel y texto mediante índices de paleta de colores en lugar de valores de color. Un índice de paleta de colores es un valor entero que identifica una entrada específica de la paleta. Las aplicaciones pueden usar índices de paleta de colores en lugar de valores de color, pero deben usar la macro [**PALETTEINDEX**](/windows/desktop/api/Wingdi/nf-wingdi-paletteindex) para crear los índices.

Los índices de paleta de colores solo son útiles para los dispositivos que admiten las paletas de colores. Para evitar esta dependencia del dispositivo, las aplicaciones que usan el mismo código para dibujar en los dispositivos de paleta y de no paleta deben usar valores de color relativos a la paleta para especificar los colores de lápiz, pincel y texto. Estos valores son idénticos a los valores de color excepto al crear pinceles sólidos. (En los dispositivos de paleta, un color de pincel sólido especificado por un valor de color relativo a la paleta está sujeto a la aproximación de color en lugar de a la interpolación). Las aplicaciones deben usar la macro [**PALETTERGB**](/windows/desktop/api/Wingdi/nf-wingdi-palettergb) para crear valores de color relativos a la paleta.

El sistema no permite que una aplicación cambie las entradas de la paleta predeterminada. Para usar colores distintos de los de la paleta predeterminada, una aplicación debe crear su propia paleta lógica y seleccionar la paleta en el contexto del dispositivo.

 

 



