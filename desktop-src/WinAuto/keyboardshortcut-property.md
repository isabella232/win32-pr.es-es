---
title: Propiedad KeyboardShortcut
description: La propiedad KeyboardShortcut describe una combinación de teclas o teclas que activa un objeto accesible especificado.
ms.assetid: 42587468-f069-4ef1-868e-ac6a285e1715
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1cc82525bcfedbd370eebcfa6df078f5c98cfff7baf13d1e7e454648c054c87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119859975"
---
# <a name="keyboardshortcut-property"></a>Propiedad KeyboardShortcut

La **propiedad KeyboardShortcut** describe una combinación de teclas o teclas que activa un objeto accesible especificado.

La **propiedad KeyboardShortcut** se recupera llamando a [**IAccessible::get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut).

La cadena recuperada describe una tecla de *método* abreviado (también denominada acelerador de *teclado)* o una tecla de acceso *(también* denominada *mnemotécnica).* Una tecla de acceso es un carácter subrayado en el texto de un menú, elemento de menú o etiqueta de un control, como un botón de inserción.

La cadena recuperada debe contener el nombre de la clave junto con la tecla modificadora o las claves. La cadena debe tener el formato siguiente para que los clientes puedan analizarla fácilmente: \[ \[ tecla modificadora \] + \[ ... \] + \] nombre de clave.

Algunos ejemplos son ALT+F, CTRL+ALT+4, WIN+F1, CTRL+ALT+MAYÚS+RETROCESO o simplemente RETROCESO.

En la tabla siguiente se enumeran las teclas modificadoras.



| Tecla modificadora | Descripción                        |
|--------------|------------------------------------|
| ALT          | Tecla modificadora alternativa             |
| CTRL         | Tecla modificadora de control               |
| Mayús        | Tecla modificadora Mayús                 |
| Ganar          | Tecla del logotipo de Windows                   |
| FN           | Clave de función en equipos portátiles |



 

No localice las cadenas de método abreviado de teclado.

## <a name="handling-objects-that-have-both-key-types"></a>Controlar objetos que tienen ambos tipos de clave

Si un objeto tiene una tecla de método abreviado y una clave de acceso, la **propiedad KeyboardShortcut** devuelve la clave de acceso. La tecla de acceso es la que un usuario presionaría cuando el objeto o el elemento primario del objeto tienen el foco del teclado. Por ejemplo, el **elemento de** menú Imprimir podría tener una tecla de método abreviado (CTRL+P) y una tecla de acceso (P). Si un usuario presiona CTRL+P mientras el menú está activo, no ocurre nada. Pero si un usuario presiona P mientras el menú está activo, invoca el cuadro de diálogo Imprimir **de** la aplicación. En este caso, la **propiedad KeyboardShortcut** es "P" para reflejar lo que el usuario debe presionar cuando el menú tiene el foco del teclado.

 

 




