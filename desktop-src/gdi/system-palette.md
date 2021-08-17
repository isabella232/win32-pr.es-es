---
description: El sistema mantiene una paleta del sistema para cada dispositivo que usa paletas.
ms.assetid: 4c93ce8c-6b3a-4016-bb47-786c25b93374
title: Paleta del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e540bd4068989a3c457568c2451dbc91f77755065f3bc70af03f9577fcebee9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117698137"
---
# <a name="system-palette"></a>Paleta del sistema

El sistema mantiene una paleta *del sistema para* cada dispositivo que usa paletas. La paleta del sistema contiene los valores de color de todos los colores que el dispositivo puede mostrar o dibujar actualmente. Aparte de ver el contenido de la paleta del sistema, las aplicaciones no pueden acceder directamente a la paleta del sistema. En su lugar, el sistema tiene control completo de la paleta del sistema y solo permite el acceso mediante el uso de paletas lógicas.

Una aplicación puede ver el contenido de la paleta del sistema mediante la [**función GetSystemPaletteEntries.**](/windows/desktop/api/Wingdi/nf-wingdi-getsystempaletteentries) Esta función recupera el contenido de una o varias entradas, hasta el número total de entradas de la paleta del sistema. El total siempre es igual al número devuelto para el valor SIZEPALETTE por la función [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) y es el mismo que el tamaño máximo de cualquier paleta lógica determinada.

Aunque las aplicaciones no pueden cambiar los colores de la paleta del sistema directamente, pueden producir cambios al realizar paletas lógicas. Para realizar una paleta, el sistema examina cada color solicitado e intenta encontrar una entrada en la paleta del sistema que contenga una coincidencia exacta. Si el sistema encuentra un color que coincida, asigna el índice de la paleta lógica al índice de paleta del sistema correspondiente. Si el sistema no encuentra una coincidencia exacta, copia el color solicitado en una entrada de paleta del sistema sin usar antes de asignar los índices. Si todas las entradas de la paleta del sistema están en uso, el sistema asigna el índice de la paleta lógica a la entrada de la paleta del sistema cuyo color coincide más estrechamente con el color solicitado. Una vez establecida esta asignación, las aplicaciones no pueden invalidarla. Por ejemplo, las aplicaciones no pueden usar índices de paleta del sistema para especificar colores; solo se permiten índices de paleta lógica.

Las aplicaciones pueden modificar la forma en que se asignan los índices estableciendo el **miembro peFlags** de la estructura [**PALETTEENTRY**](/previous-versions//dd162769(v=vs.85)) en los valores seleccionados al crear la paleta lógica. Por ejemplo, la marca PC NOCOLLAPSE indica al sistema que copie inmediatamente el color solicitado en una entrada de paleta del sistema sin usar, independientemente de si una entrada de paleta del sistema ya contiene \_ ese color. Además, la marca PC EXPLICIT dirige al sistema para asignar el índice de la paleta lógica a un índice de paleta del sistema especificado \_ explícitamente. (La aplicación proporciona el índice de la paleta del sistema en la palabra de orden bajo de la **estructura PALETTEENTRY).**

Las paletas se pueden realizar como una paleta de fondo o una paleta de primer plano especificando **TRUE** o **FALSE** respectivamente para el *parámetro bForceBackground* en la [**función SelectPalette.**](/windows/desktop/api/Wingdi/nf-wingdi-selectpalette) Solo puede haber una paleta de primer plano en el sistema a la vez. Si la ventana es la ventana activa actualmente o descendiente de la ventana activa actualmente, puede realizar una paleta de primer plano. De lo contrario, la paleta se realiza como una paleta de fondo independientemente del valor del *parámetro bForceBackground.* La propiedad crítica de una paleta de primer plano es que, cuando se realiza, puede sobrescribir todas las entradas (excepto las entradas estáticas) en la paleta del sistema. Para ello, el sistema marca todas las entradas que no son estáticas en la paleta del sistema como no utilizadas antes de la realización de una paleta de primer plano, lo que elimina todas las entradas usadas. No se produce ningún preprocesamiento en la paleta del sistema para la realización de una paleta de fondo. La paleta de primer plano establece todos los colores posibles no estáticos. Las paletas de fondo solo pueden establecer lo que permanece abierto y se priorizan por orden de llegada. Normalmente, las aplicaciones usan paletas de fondo para ventanas secundarias que se dan cuenta de sus propias paletas individuales. Esto ayuda a minimizar el número de cambios que se producen en la paleta del sistema.

Una entrada de la paleta del sistema no utilizada es cualquier entrada que no está reservada y no contiene un color estático. Las entradas reservadas se marcan explícitamente con el valor \_ RESERVADO de PC. Estas entradas se crean cuando una aplicación realiza una paleta lógica para la animación de paleta. El sistema crea entradas de color estático y corresponden a los colores de la paleta predeterminada. La [**función GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) se puede usar para recuperar el valor NUMRESERVED, que especifica el número de entradas de la paleta del sistema reservadas para colores estáticos.

Dado que la paleta del sistema tiene un número limitado de entradas, la selección y realización de una paleta lógica para un dispositivo determinado puede afectar a los colores asociados a otras paletas lógicas para el mismo dispositivo. Estos cambios de color son especialmente drásticos cuando se producen en la pantalla. Una aplicación puede asegurarse de que se usan colores razonables para su paleta lógica seleccionada actualmente mediante el restablecimiento de la paleta antes de cada uso. Una aplicación restablece la paleta mediante una llamada a las funciones [**UnrealizeObject**](/windows/desktop/api/Wingdi/nf-wingdi-unrealizeobject) y [**RealizePalette.**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) El uso de estas funciones hace que el sistema vuelva a asignar los colores de la paleta lógica a colores razonables en la paleta del sistema.

 

 
