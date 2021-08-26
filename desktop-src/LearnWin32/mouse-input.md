---
title: Entrada del mouse (Introducción con Win32 y C++)
description: Entrada del mouse
ms.assetid: EB074CB6-2BB3-4593-A843-8EE25CA028BE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28ff39b798b1438bca33bc9ab9b077333dca351e32a5945b939beba2c13f5894
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119897054"
---
# <a name="mouse-input-get-started-with-win32-and-c"></a>Entrada del mouse (Introducción con Win32 y C++)

Windows admite mouse con hasta cinco botones: izquierdo, medio y derecho, además de dos botones adicionales denominados XBUTTON1 y XBUTTON2.

![ilustración que muestra los botones left (1), right (2), middle (3) y xbutton1 (4).](images/mouse.png)

La mayoría de los Windows tienen al menos los botones izquierdo y derecho. El botón izquierdo del mouse se usa para apuntar, seleccionar, arrastrar, etc. Normalmente, el botón derecho del mouse muestra un menú contextual. Algunos mouse tienen una rueda de desplazamiento situada entre los botones izquierdo y derecho. Dependiendo del mouse, la rueda de desplazamiento también puede hacer clic, lo que lo hace el botón central.

Los botones XBUTTON1 y XBUTTON2 a menudo se encuentran a los lados del mouse, cerca de la base. Estos botones adicionales no están presentes en todos los mouse. Si están presentes, los botones XBUTTON1 y XBUTTON2 a menudo se asignan a una función de aplicación, como la navegación hacia delante y hacia atrás en un explorador web.

A menudo, a los usuarios de la izquierda les resulta más cómodo intercambiar las funciones de los botones izquierdo y derecho, con el botón derecho como puntero y el botón izquierdo para mostrar el menú contextual. Por esta razón, la documentación Windows  ayuda usa los términos botón principal y botón *secundario,* que hacen referencia a la función lógica en lugar de a la colocación física. En el valor predeterminado (con la mano derecha), el botón izquierdo es el botón principal y el derecho es el secundario. Sin embargo, los *términos clic con el botón derecho* y clic *izquierdo* hacen referencia a acciones lógicas. *Hacer clic con el* botón derecho significa hacer clic en el botón principal, independientemente de si ese botón está físicamente en el lado derecho o izquierdo del mouse.

Independientemente de cómo configure el usuario el mouse, Windows automáticamente los mensajes del mouse para que sean coherentes. El usuario puede intercambiar los botones principal y secundario en medio del uso del programa, y no afectará a cómo se comporta el programa.

La documentación de MSDN usa los *términos botón derecho* *y botón izquierdo para* hacer referencia al *botón* principal *y* secundario. Esta terminología es coherente con los nombres de los mensajes de ventana para la entrada del mouse. Recuerde que los botones físicos izquierdo y derecho se pueden intercambiar.

## <a name="next"></a>Siguientes

[Responder a los clics del mouse](mouse-clicks.md)

 

 




