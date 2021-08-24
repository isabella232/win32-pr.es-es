---
title: Acerca de los carets
description: En este tema se de abordan los carets.
ms.assetid: 4487c93c-9a0f-467c-86b1-969f664d5526
keywords:
- resources,carets
- carets,removing
- líneas parpadeando
- bloques de parpadeo
- mapas de bits parpadeantes
- carets,visibility
- carets,blink times
- tiempos de parpadeo
- carets,positions
- quitar los caretos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65ed2cbe50771b893c7a2ccc0874a882aabb23a1d0b4ba27822d7ce0ec47a18b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119461325"
---
# <a name="about-carets"></a>Acerca de los carets

El sistema proporciona un caret por cola de mensajes. Una ventana debe crear un caret solo cuando tiene el foco del teclado o está activo. La ventana debe destruir el carácter de diálogo antes de perder el foco del teclado o de quedarse inactivo. Para obtener más información sobre la entrada de teclado, vea [Entrada de teclado](/windows/desktop/inputdev/keyboard-input).

Use la [**función CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret) para especificar los parámetros de un caret. El sistema forma un elemento de careta al invertir el color de píxel dentro del rectángulo especificado por la posición, el ancho y el alto del cursor. El ancho y el alto se especifican en unidades lógicas; por lo tanto, la apariencia de un caret está sujeta al modo de asignación de la ventana.

En esta sección se tratan los temas siguientes.

-   [Visibilidad del elemento de caret](#caret-visibility)
-   [Tiempo de parpadeo del caret](#caret-blink-time)
-   [Posición del cursor de cursor](#caret-position)
-   [Quitar un caret](#removing-a-caret)

## <a name="caret-visibility"></a>Visibilidad del elemento de caret

Una vez definido el caret, use la [**función ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret) para que el caret sea visible. Cuando aparece el caret, comienza a parpadear automáticamente. Para mostrar un sólido caret, el sistema invierte cada píxel del rectángulo; para mostrar un caret gris, el sistema invierte todos los demás píxeles; para mostrar un mapa de bits, el sistema invierte solo los bits en blanco del mapa de bits.

## <a name="caret-blink-time"></a>Tiempo de parpadeo del caret

El tiempo transcurrido, en milisegundos, necesario para invertir el caret se denomina tiempo *de parpadeo.* El cursor de cursor parpadeará siempre que el subproceso propietario de la cola de mensajes tenga un bombeo de mensajes que procese los mensajes.

El usuario puede establecer el tiempo de parpadeo del cursor de Panel de control y las aplicaciones deben respetar la configuración que el usuario ha elegido. Una aplicación puede determinar el tiempo de parpadeo del aviso mediante la [**función GetCaretBlinkTime.**](/windows/desktop/api/Winuser/nf-winuser-getcaretblinktime) Si está escribiendo una aplicación que permite al usuario ajustar el tiempo de parpadeo, como un applet de Panel de control, use la función [**SetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) para establecer la velocidad del tiempo de parpadeo en un número especificado de milisegundos.

El *tiempo de flash* es el tiempo transcurrido, en milisegundos, necesario para mostrar, invertir y restaurar la presentación del centro de diálogo. El tiempo de flash de un caret es el doble que el tiempo de parpadeo.

## <a name="caret-position"></a>Posición del cursor de cursor

Puede determinar la posición del caret mediante la [**función GetCaretPos.**](/windows/desktop/api/Winuser/nf-winuser-getcaretpos) La posición, en coordenadas de cliente, se copia en una estructura especificada por un parámetro en **GetCaretPos**. Una aplicación puede mover un caret en una ventana mediante la [**función SetCaretPos.**](/windows/desktop/api/Winuser/nf-winuser-setcaretpos) Una ventana puede mover un caret solo si ya posee el caret. **SetCaretPos puede** mover el caret tanto si está visible como si no.

## <a name="removing-a-caret"></a>Quitar un caret

Puede quitar temporalmente un carácter de diálogo si lo oculta o puede quitar permanentemente el carácter de diálogo si lo destruye. Para ocultar el caret, use la [**función HideCaret.**](/windows/desktop/api/Winuser/nf-winuser-hidecaret) Esto resulta útil cuando la aplicación debe volver a dibujar la pantalla mientras procesa un mensaje, pero debe mantener el caret fuera del camino. Cuando la aplicación termina de dibujar, puede volver a mostrar el caret mediante la [**función ShowCaret.**](/windows/desktop/api/Winuser/nf-winuser-showcaret) Ocultar el objeto de inserción no destruye su forma ni invalida el punto de inserción. Ocultar el caret es acumulativo; Es decir, si la aplicación llama a **HideCaret** cinco veces, también debe llamar a **ShowCaret** cinco veces antes de que el caret vuelva a aparecer.

Para quitar el caret de la pantalla y destruir su forma, use la [**función DestroyCaret.**](/windows/desktop/api/Winuser/nf-winuser-destroycaret) **DestroyCaret** destruye el caret solo si la ventana implicada en la tarea actual posee el caret.

 

 