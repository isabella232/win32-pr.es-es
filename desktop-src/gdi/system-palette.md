---
description: El sistema mantiene una paleta del sistema para cada dispositivo que utiliza las paletas.
ms.assetid: 4c93ce8c-6b3a-4016-bb47-786c25b93374
title: Paleta del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d8738cf63eef0b77f2d184f2cf95b6550b81053
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997656"
---
# <a name="system-palette"></a>Paleta del sistema

El sistema mantiene una *paleta del sistema* para cada dispositivo que utiliza las paletas. La paleta del sistema contiene los valores de color de todos los colores que el dispositivo puede mostrar o dibujar actualmente. Aparte de ver el contenido de la paleta del sistema, las aplicaciones no pueden tener acceso directamente a la paleta del sistema. En su lugar, el sistema tiene un control completo de la paleta del sistema y solo permite el acceso a través del uso de las paletas lógicas.

Una aplicación puede ver el contenido de la paleta del sistema mediante la función [**GetSystemPaletteEntries**](/windows/desktop/api/Wingdi/nf-wingdi-getsystempaletteentries) . Esta función recupera el contenido de una o varias entradas, hasta el número total de entradas de la paleta del sistema. El total siempre es igual al número devuelto para el valor SIZEPALETTE por la función [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) y es igual que el tamaño máximo de cualquier paleta lógica determinada.

Aunque las aplicaciones no pueden cambiar los colores de la paleta del sistema directamente, pueden provocar cambios al realizar las paletas lógicas. Para obtener una paleta, el sistema examina cada color solicitado e intenta encontrar una entrada en la paleta del sistema que contenga una coincidencia exacta. Si el sistema encuentra un color coincidente, asigna el índice de la paleta lógica al índice de la paleta del sistema correspondiente. Si el sistema no encuentra una coincidencia exacta, copia el color solicitado en una entrada de la paleta del sistema sin usar antes de asignar los índices. Si todas las entradas de la paleta del sistema están en uso, el sistema asigna el índice de la paleta lógica a la entrada de la paleta del sistema cuyo color coincide más estrechamente con el color solicitado. Una vez establecida esta asignación, las aplicaciones no pueden invalidarla. Por ejemplo, las aplicaciones no pueden utilizar índices de paleta del sistema para especificar los colores; solo se permiten índices de paleta lógicos.

Las aplicaciones pueden modificar el modo en que se asignan los índices estableciendo el miembro **peFlags** de la estructura [**PALETTEENTRY**](/previous-versions//dd162769(v=vs.85)) en los valores seleccionados al crear la paleta lógica. Por ejemplo, la \_ marca PC nocollapse indica al sistema que copie inmediatamente el color solicitado en una entrada de la paleta del sistema sin usar, independientemente de si una entrada de la paleta del sistema ya contiene ese color. Además, la marca de PC \_ Explicit indica al sistema que asigne el índice de la paleta lógica a un índice de la paleta del sistema especificado explícitamente. (La aplicación proporciona el índice de la paleta del sistema en la palabra de orden inferior de la estructura **PALETTEENTRY** ).

Las paletas se pueden realizar como una paleta de fondo o de primer plano especificando **true** o **false** respectivamente para el parámetro *bForceBackground* en la función [**SelectPalette**](/windows/desktop/api/Wingdi/nf-wingdi-selectpalette) . Solo puede haber una paleta de primer plano en el sistema a la vez. Si la ventana es la ventana activa actualmente o un descendiente de la ventana activa actualmente, puede obtener una paleta de primer plano. De lo contrario, la paleta se realiza como una paleta de fondo, independientemente del valor del parámetro *bForceBackground* . La propiedad Critical de una paleta de primer plano es que, cuando se realiza, puede sobrescribir todas las entradas (excepto las entradas estáticas) en la paleta del sistema. Para ello, el sistema marca todas las entradas que no son estáticas en la paleta del sistema como no utilizadas antes de la realización de una paleta de primer plano, con lo que se eliminan todas las entradas usadas. No se produce ningún preprocesamiento en la paleta del sistema para la realización de una paleta de fondo. La paleta de primer plano establece todos los colores no estáticos posibles. Las paletas de fondo solo pueden establecer lo que permanece abierto y se clasifican por orden de prioridad en la primera de ellas. Normalmente, las aplicaciones usan las paletas de fondo para las ventanas secundarias que obtienen sus propias paletas individuales. Esto ayuda a minimizar el número de cambios que se producen en la paleta del sistema.

Una entrada de la paleta del sistema sin usar es cualquier entrada que no esté reservada y no contenga un color estático. Las entradas reservadas se marcan explícitamente con el \_ valor reservado de PC. Estas entradas se crean cuando una aplicación obtiene una paleta lógica para la animación de la paleta. El sistema crea entradas de color estáticas que se corresponden con los colores de la paleta predeterminada. La función [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) se puede usar para recuperar el valor NUMRESERVED, que especifica el número de entradas de la paleta del sistema reservadas para los colores estáticos.

Dado que la paleta del sistema tiene un número limitado de entradas, la selección y la finalización de una paleta lógica para un dispositivo determinado pueden afectar a los colores asociados a otras paletas lógicas para el mismo dispositivo. Estos cambios de color son especialmente importantes cuando se producen en la pantalla. Una aplicación puede asegurarse de que se usan colores razonables para su paleta lógica seleccionada actualmente restableciendo la paleta antes de cada uso. Una aplicación restablece la paleta llamando a las funciones [**UnrealizeObject**](/windows/desktop/api/Wingdi/nf-wingdi-unrealizeobject) y [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) . El uso de estas funciones hace que el sistema reasigne los colores de la paleta lógica a colores razonables en la paleta del sistema.

 

 
