---
description: Windows permite la definición local de caracteres no estándar en juegos de caracteres de doble byte (DBCS) y Unicode.
ms.assetid: 32d0ddab-4b3f-473e-bf92-3230b3746079
title: Juegos de caracteres y fuentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43dbf3dae2875ec6d714419bb45411f3208bfe5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686724"
---
# <a name="character-sets-and-fonts"></a>Juegos de caracteres y fuentes

Windows permite la definición local de caracteres no estándar en [juegos de caracteres de doble byte](double-byte-character-sets.md) (DBCS) y [Unicode](unicode.md). En el caso de un DBCS, estos caracteres no estándar se conocen como caracteres definidos por el usuario final (EUDC). Unicode proporciona una funcionalidad similar a través de su área de uso privado (PUA). Las aplicaciones identifican un carácter especificado mediante el valor de caracteres DBCS o Unicode asociado.

Los valores de caracteres DBCS que se pueden asignar dependen del juego de caracteres especificado. Cada [Página de códigos](code-pages.md) de Windows de Asia oriental tiene al menos un intervalo de valores reservados para su uso como EUDCs. Los intervalos se definen mediante la clave del registro [EUDCCodeRange](eudccoderange.md) . Los valores Unicode para este propósito siempre proceden de la PUA Unicode, los valores U + E000 y a U + F8FF, U + F0000 a U + FFFFD y U + 100000 a U + 10FFFD.

Para crear un carácter EUDC o PUA, el usuario elige un valor de carácter que se encuentra dentro del intervalo especificado y agrega el [glifo](uniscribe-glossary.md) a la fuente de la entrada que corresponde a ese valor de carácter. El usuario crea el glifo mediante un editor EUDC o usando un paquete de fuentes adquirido a un proveedor de fuentes. Cualquier fuente DBCS puede contener EUDCs y cualquier fuente Unicode puede contener caracteres PUA. La fuente se denomina una fuente EUDC/PUA "independiente" si solo contiene EUDCs. La fuente es una fuente EUDC/PUA "integrada" si contiene caracteres estándar, así como EUDCs.

La fuente EUDC/PUA predeterminada del sistema es una fuente que el sistema operativo asocia automáticamente a todas las fuentes DBCS y Unicode, excepto las fuentes que tienen asociadas explícitamente fuentes EUDC/PUA. Las aplicaciones establecen la fuente EUDC/PUA predeterminada del sistema estableciendo el valor del nombre SystemDefaultEUDCFont en la clave del registro [EUDC](eudc.md) . Del mismo modo, las aplicaciones pueden asociar fuentes EUDC/PUA independientes con las fuentes correspondientes especificando un nombre de fuente y un archivo de fuente asociado con la clave EUDC. El sistema operativo siempre intenta buscar primero el EUDC/PUA en la fuente seleccionada actualmente. Si no se encuentra la fuente, el sistema operativo busca el carácter en la fuente EUDC/PUA asociada, si se ha definido uno para la fuente seleccionada actualmente. Si todavía no se encuentra el carácter, el sistema operativo lo busca en la fuente de EUDC/PUA predeterminada del sistema.

Las fuentes TrueType se pueden instalar como archivos. ttf o como archivos. TTE. Dado que el sistema operativo oculta los archivos. TTE, las aplicaciones no pueden enumerar o examinar de otro modo las fuentes instaladas mediante las funciones de la API de GDI. En muchos sistemas operativos, la fuente de EUDC/PUA predeterminada del sistema y las fuentes EUDC/PUA independientes se instalan como archivos. TTE. Las aplicaciones como los editores de EUDC y el panel de control deben usar entradas del registro para agregar, modificar y eliminar dichas fuentes.

El uso de caracteres de EUDC y PUA no conserva de forma confiable el significado entre distintos equipos o juegos de caracteres. Consulte [caracteres de área de uso privado y definidos por el usuario final](end-user-defined-characters.md) para obtener más precauciones sobre el uso de los caracteres EUDC y PUA.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Caracteres de área de uso privado y definidos por el usuario final](end-user-defined-characters.md)
</dt> </dl>

 

 



