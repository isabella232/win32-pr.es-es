---
description: Windows permite la definición local de caracteres no estándar en conjuntos de caracteres de doble byte (DBCS) y Unicode.
ms.assetid: 32d0ddab-4b3f-473e-bf92-3230b3746079
title: Juegos de caracteres y fuentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eeee925f55887ac8120474f14b727ea244dc02c3b1e7908f424c0dbf09d502b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068285"
---
# <a name="character-sets-and-fonts"></a>Juegos de caracteres y fuentes

Windows permite la definición local de caracteres no estándar en conjuntos de caracteres de doble [byte](double-byte-character-sets.md) (DBCS) y [Unicode](unicode.md). Para un DBCS, estos caracteres no estándar se conocen como caracteres definidos por el usuario final (EUDC). Unicode proporciona una funcionalidad similar a través de su área de uso privado (PUA). Las aplicaciones identifican un carácter especificado mediante el valor de caracteres DBCS o Unicode asociado.

Los valores de caracteres DBCS que se pueden asignar dependen del juego de caracteres especificado. Cada página de códigos Windows asia [oriental](code-pages.md) tiene al menos un intervalo de valores reservados para su uso como EUDC. Los intervalos se definen mediante la clave del Registro [EUDCCodeRange.](eudccoderange.md) Los valores Unicode para este propósito siempre proceden de la PUA Unicode, los valores U+E000 a U+F8FF, U+F0000 a U+FFFFD y U+100000 a U+10FFFD.

Para crear un carácter EUDC o PUA, el usuario elige un valor [](uniscribe-glossary.md) de carácter que se encuentra dentro del intervalo especificado y agrega el glifo a la fuente de la entrada que corresponde a ese valor de carácter. El usuario crea el glifo mediante un editor de EUDC o un paquete de fuentes adquirido a un proveedor de fuentes. Cualquier fuente DBCS puede contener EUDC y cualquier fuente Unicode puede contener caracteres PUA. La fuente se denomina una fuente EUDC/PUA "independiente" si solo contiene EUDC. La fuente es una fuente EUDC/PUA "integrada" si contiene caracteres estándar, así como EUDC.

La fuente EUDC/PUA predeterminada del sistema es una fuente que el sistema operativo asocia automáticamente a todas las fuentes DBCS y Unicode, excepto las fuentes que tienen fuentes EUDC/PUA asociadas explícitamente. Las aplicaciones establecen la fuente EUDC/PUA predeterminada del sistema estableciendo el valor del nombre SystemDefaultEUDCFont en la clave del Registro [EUDC.](eudc.md) De forma similar, las aplicaciones pueden asociar fuentes EUDC/PUA independientes a las fuentes correspondientes especificando un nombre de fuente y un archivo de fuente asociado en la clave EUDC. El sistema operativo siempre intenta encontrar primero el EUDC/PUA en la fuente seleccionada actualmente. Si no se encuentra la fuente, el sistema operativo busca el carácter en la fuente EUDC/PUA asociada, si se ha definido una para la fuente seleccionada actualmente. Si todavía no encuentra el carácter, el sistema operativo lo busca en la fuente EUDC/PUA predeterminada del sistema.

Las fuentes TrueType se pueden instalar como archivos .ttf o como archivos .tte. Dado que el sistema operativo oculta los archivos .tte, las aplicaciones no pueden enumerar ni examinar las fuentes instaladas mediante funciones de la API de GDI. En muchos sistemas operativos, la fuente EUDC/PUA predeterminada del sistema y las fuentes EUDC/PUA independientes se instalan como archivos .tte. Las aplicaciones como los editores EUDC y Panel de control deben usar entradas del Registro para agregar, modificar y eliminar dichas fuentes.

El uso de caracteres EUDC y PUA no conserva de forma confiable el significado en distintos equipos o juegos de caracteres. Consulte [End-User-Defined and Private Use Area Characters](end-user-defined-characters.md) (Caracteres de área de uso privado y definidos por el usuario final) para más información sobre el uso de caracteres EUDC y PUA.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Caracteres de área de uso privado y definido por el usuario final](end-user-defined-characters.md)
</dt> </dl>

 

 



