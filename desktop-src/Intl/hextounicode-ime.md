---
description: La edición enriquecida 3,0 admite el IME de HexToUnicode, que permite a un usuario convertir entre caracteres hexadecimales y Unicode mediante el uso de teclas de acceso rápido de una de estas dos maneras.
ms.assetid: 4b8c4de4-9c1c-459c-a640-367e86a9b9cc
title: HexToUnicode IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88042ce276082755613b28a7e4d070c8b3d695f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104547110"
---
# <a name="hextounicode-ime"></a>HexToUnicode IME

La edición enriquecida 3,0 admite el IME de HexToUnicode, que permite a un usuario convertir entre caracteres hexadecimales y Unicode mediante el uso de teclas de acceso rápido de una de estas dos maneras.

Con el primer método de conversión, el usuario escribe el código de carácter en hexadecimal y, a continuación, presiona ALT + X. El IME reemplaza los dígitos hexadecimales que preceden al punto de inserción con el carácter Unicode. Si la fuente actual no admite el código de carácter, se elige una fuente adecuada que lo admita. Para convertir de Unicode a hexadecimal, el usuario escribe MAYÚS + ALT + X. Esta entrada reemplaza el carácter Unicode que precede al punto de inserción con los dígitos hexadecimales. En concreto, este método permite al usuario determinar el carácter que se indica mediante un indicador de "glifo que falta". Si el código de carácter hexadecimal sigue inmediatamente a algunos caracteres hexadecimales legítimos (no de caracteres), el usuario selecciona los dígitos específicos que se van a convertir antes de escribir ALT + X. Un problema con este primer método es que ALT + X se usa a veces como una combinación de teclas para el comando Exit (es decir, eXit). Por ejemplo, en Microsoft Office, este comando solo aparece como una opción del menú **archivo** .

El segundo método de conversión entre caracteres hexadecimales y Unicode implica el panel numérico. Con este método, el usuario escribe los números de ALT + teclado (con valores mayores que 255) para escribir caracteres Unicode mediante valores decimales. Este método no es tan útil como el primero porque el usuario no puede ver qué dígitos hexadecimales se han escrito. Además, el usuario no puede corregir los dígitos hexadecimales, excepto si vuelve a escribir todos los dígitos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca del administrador de métodos de entrada](about-input-method-manager.md)
</dt> </dl>

 

 



