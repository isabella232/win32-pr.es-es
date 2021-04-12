---
title: Propiedad KeyboardShortcut
description: La propiedad KeyboardShortcut describe una tecla o combinación de teclas que activa un objeto accesible especificado.
ms.assetid: 42587468-f069-4ef1-868e-ac6a285e1715
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 002c925151f3f1acc136190d7807d7bc814d30b9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268802"
---
# <a name="keyboardshortcut-property"></a>Propiedad KeyboardShortcut

La propiedad **KeyboardShortcut** describe una tecla o combinación de teclas que activa un objeto accesible especificado.

La propiedad **KeyboardShortcut** se recupera llamando a [**IAccessible:: get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut).

La cadena recuperada describe una *tecla de método abreviado* (también denominada *acelerador de teclado*) o una tecla de acceso (también denominada tecla de *acceso* ).  Una tecla de acceso es un carácter subrayado en el texto de un menú, un elemento de menú o una etiqueta de un control, como un botón de inserción.

La cadena recuperada debe contener el nombre de la clave, junto con la tecla modificadora o las teclas. La cadena debe tener el formato siguiente para que los clientes puedan analizarla con facilidad: el nombre de la clave del \[ \[ modificador. \] + \[ .. \] + \] .

Entre los ejemplos se incluyen ALT + F, CTRL + ALT + 4, WIN + F1, CTRL + ALT + MAYÚS + retroceso o simplemente retroceso.

En la tabla siguiente se enumeran las teclas modificadoras.



| Tecla modificadora | Descripción                        |
|--------------|------------------------------------|
| ALT          | Tecla modificadora alternativa             |
| CTRL         | Tecla modificador de control               |
| Mayús        | Shift (tecla modificador)                 |
| SUERTE          | Tecla del logotipo de Windows                   |
| FN           | Tecla de función en equipos portátiles |



 

No debe localizar cadenas de métodos abreviados de teclado.

## <a name="handling-objects-that-have-both-key-types"></a>Controlar objetos que tienen ambos tipos de clave

Si un objeto tiene una tecla de método abreviado y una tecla de acceso, la propiedad **KeyboardShortcut** devuelve la tecla de acceso. La tecla de acceso es la que un usuario presionaría cuando el objeto o el elemento primario del objeto tenga el foco de teclado. Por ejemplo, el elemento de menú **Imprimir** puede tener una tecla de método abreviado (Ctrl + P) y una tecla de acceso (P). Si un usuario presiona CTRL + P mientras el menú está activo, no sucede nada. Pero si un usuario presiona P mientras el menú está activo, invoca el cuadro de diálogo **Imprimir** de la aplicación. En este caso, la propiedad **KeyboardShortcut** es "P" para reflejar lo que el usuario debe presionar cuando el menú tiene el foco de teclado.

 

 




