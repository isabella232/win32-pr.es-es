---
title: Entrada del mouse (introducción a Win32 y C++)
description: Entrada del mouse
ms.assetid: EB074CB6-2BB3-4593-A843-8EE25CA028BE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d71a560baf110892ba1b8f277c55fc124888b62b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105676531"
---
# <a name="mouse-input-get-started-with-win32-and-c"></a>Entrada del mouse (introducción a Win32 y C++)

Windows admite ratones con hasta cinco botones: izquierda, central y derecha, además de dos botones adicionales denominados XBUTTON1 y XBUTTON2.

![Ilustración que muestra los botones izquierdo (1), derecho (2), medio (3) y xbutton1 (4).](images/mouse.png)

La mayoría de los ratones de Windows tienen al menos los botones izquierdo y derecho. El botón primario del mouse se usa para señalar, seleccionar, arrastrar, etc. El botón secundario del mouse normalmente muestra un menú contextual. Algunos ratones tienen una rueda de desplazamiento situada entre los botones de la izquierda y la derecha. Dependiendo del mouse, es posible que también se pueda hacer clic en la rueda de desplazamiento, convirtiéndola en el botón central.

Los botones XBUTTON1 y XBUTTON2 se encuentran a menudo en los lados del mouse, cerca de la base. Estos botones adicionales no están presentes en todos los ratones. Si está presente, los botones XBUTTON1 y XBUTTON2 suelen estar asignados a una función de aplicación, como la navegación hacia delante y hacia atrás en un explorador Web.

Los usuarios de la mano izquierda suelen encontrar más cómodo intercambiar las funciones de los botones izquierdo y derecho, con el botón derecho como puntero y el botón izquierdo para mostrar el menú contextual. Por esta razón, la documentación de la ayuda de Windows usa el botón *primario* términos y el *botón secundario*, que hacen referencia a la función lógica en lugar de a la selección de ubicación física. En el valor predeterminado (mano derecha), el botón izquierdo es el botón primario y el derecho es el botón secundario. Sin embargo, los términos *haga clic con el botón derecho* y haga *clic* en acciones lógicas. *Hacer clic con el botón derecho* significa hacer clic en el botón principal, tanto si el botón está físicamente a la derecha como en el lado izquierdo del mouse.

Independientemente de la forma en que el usuario configure el mouse, Windows traduce automáticamente los mensajes del mouse para que sean coherentes. El usuario puede intercambiar los botones principal y secundario en medio de usar el programa y no afectará a la forma en que se comporta el programa.

En la documentación de MSDN se usa el botón *derecho* y el *botón primario* para hacer referencia al botón *principal* y *secundario* . Esta terminología es coherente con los nombres de los mensajes de ventana para la entrada del mouse. Solo tiene que recordar que se pueden intercambiar los botones físicos izquierdo y derecho.

## <a name="next"></a>Siguientes

[Responder a clics del mouse](mouse-clicks.md)

 

 




