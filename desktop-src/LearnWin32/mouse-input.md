---
title: Entrada del mouse (Introducción con Win32 y C++)
description: Entrada del mouse
ms.assetid: EB074CB6-2BB3-4593-A843-8EE25CA028BE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d71a560baf110892ba1b8f277c55fc124888b62b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159954"
---
# <a name="mouse-input-get-started-with-win32-and-c"></a>Entrada del mouse (Introducción con Win32 y C++)

Windows admite mouses con hasta cinco botones: izquierdo, medio y derecho, además de dos botones adicionales denominados XBUTTON1 y XBUTTON2.

![Ilustración que muestra los botones izquierdo (1), derecho (2), medio (3) y xbutton1 (4).](images/mouse.png)

La mayoría de los Windows tienen al menos los botones izquierdo y derecho. El botón izquierdo del mouse se usa para apuntar, seleccionar, arrastrar, etc. Normalmente, el botón derecho del mouse muestra un menú contextual. Algunos mouse tienen una rueda de desplazamiento situada entre los botones izquierdo y derecho. Dependiendo del mouse, es posible que también se pueda hacer clic en la rueda de desplazamiento, lo que lo hace el botón central.

Los botones XBUTTON1 y XBUTTON2 a menudo se encuentran en los lados del mouse, cerca de la base. Estos botones adicionales no están presentes en todos los mouse. Si está presente, los botones XBUTTON1 y XBUTTON2 a menudo se asignan a una función de aplicación, como la navegación hacia delante y hacia atrás en un explorador web.

A menudo, a los usuarios de la izquierda les resulta más cómodo intercambiar las funciones de los botones izquierdo y derecho, con el botón derecho como puntero y el botón izquierdo para mostrar el menú contextual. Por este motivo, la documentación Windows ayuda  usa los términos botón principal y botón *secundario,* que hacen referencia a la función lógica en lugar de a la selección de ubicación física. En la configuración predeterminada (con la mano derecha), el botón izquierdo es el botón principal y el derecho es el secundario. Sin embargo, los *términos clic con el botón derecho* y clic *izquierdo* hacen referencia a acciones lógicas. *Hacer clic con el* botón derecho significa hacer clic en el botón principal, independientemente de si ese botón está físicamente en el lado derecho o izquierdo del mouse.

Independientemente de cómo configure el usuario el mouse, Windows automáticamente los mensajes del mouse para que sean coherentes. El usuario puede intercambiar los botones principal y secundario en medio del uso del programa, y no afectará al comportamiento del programa.

La documentación de MSDN usa los *términos botón derecho* *y botón izquierdo para* hacer referencia al *botón* principal *y* secundario. Esta terminología es coherente con los nombres de los mensajes de ventana para la entrada del mouse. Recuerde que los botones físicos izquierdo y derecho podrían intercambiarse.

## <a name="next"></a>Siguientes

[Respuesta a los clics del mouse](mouse-clicks.md)

 

 




