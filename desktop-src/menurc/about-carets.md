---
title: Acerca de los carets
description: En este tema se de abordan los carets.
ms.assetid: 4487c93c-9a0f-467c-86b1-969f664d5526
keywords:
- resources,carets
- carets,removing
- líneas parpadeando
- bloques parpadeando
- mapas de bits parpadeantes
- carets,visibility
- carets,blink times
- tiempos de parpadeo
- carets,positions
- quitar los caretas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a19eb3895ada13297f090a09529b2bcb7c75dee
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360072"
---
# <a name="about-carets"></a>Acerca de los carets

El sistema proporciona un centro de atención por cola de mensajes. Una ventana debe crear un centro de diálogo solo cuando tiene el foco del teclado o está activo. La ventana debe destruir el carácter de diálogo antes de perder el foco del teclado o de quedarse inactivo. Para obtener más información sobre la entrada de teclado, vea [Entrada de teclado](/windows/desktop/inputdev/keyboard-input).

Use la [**función CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret) para especificar los parámetros de un caret. El sistema forma un elemento de careta al invertir el color de píxel dentro del rectángulo especificado por la posición, el ancho y el alto del cursor. El ancho y el alto se especifican en unidades lógicas; Por lo tanto, la apariencia de un objeto de asignación está sujeta al modo de asignación de la ventana.

En esta sección se tratan los temas siguientes.

-   [Visibilidad del caret](#caret-visibility)
-   [Tiempo de parpadeo del caret](#caret-blink-time)
-   [Posición del caret](#caret-position)
-   [Quitar un caret](#removing-a-caret)

## <a name="caret-visibility"></a>Visibilidad del caret

Una vez definido el signo de cuidado, use la [**función ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret) para que el signo de cuidado sea visible. Cuando aparece el caret, comienza a parpadear automáticamente. Para mostrar un caret sólido, el sistema invierte cada píxel del rectángulo; para mostrar un caret gris, el sistema invierte cada píxel; para mostrar un mapa de bits, el sistema invierte solo los bits en blanco del mapa de bits.

## <a name="caret-blink-time"></a>Tiempo de parpadeo del caret

El tiempo transcurrido, en milisegundos, necesario para invertir el cursor de subrayado se denomina tiempo *de parpadeo.* El cursor de cursor parpadeará siempre que el subproceso propietario de la cola de mensajes tenga un bombeo de mensajes que procese los mensajes.

El usuario puede establecer la hora de parpadeo del icono de Panel de control y las aplicaciones deben respetar la configuración que el usuario ha elegido. Una aplicación puede determinar el tiempo de parpadeo del centro de atención mediante la [**función GetCaretBlinkTime.**](/windows/desktop/api/Winuser/nf-winuser-getcaretblinktime) Si está escribiendo una aplicación que permite al usuario ajustar el tiempo de parpadeo, como un applet de Panel de control, use la función [**SetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) para establecer la velocidad del tiempo de parpadeo en un número especificado de milisegundos.

El *tiempo de flash* es el tiempo transcurrido, en milisegundos, necesario para mostrar, invertir y restaurar la presentación del centro de diálogo. El tiempo de flash de un centro de atención es el doble que el tiempo de parpadeo.

## <a name="caret-position"></a>Posición del caret

Puede determinar la posición del caret mediante la [**función GetCaretPos.**](/windows/desktop/api/Winuser/nf-winuser-getcaretpos) La posición, en coordenadas de cliente, se copia en una estructura especificada por un parámetro en **GetCaretPos**. Una aplicación puede mover un aviso en una ventana mediante la [**función SetCaretPos.**](/windows/desktop/api/Winuser/nf-winuser-setcaretpos) Una ventana solo puede mover un caret si ya posee el centro de atención. **SetCaretPos puede** mover el signo de cuidado tanto si está visible como si no.

## <a name="removing-a-caret"></a>Quitar un caret

Puede quitar temporalmente un carácter de careta ocultándose, o bien puede quitar permanentemente el carácter de asociado si lo destruye. Para ocultar el caret, use la [**función HideCaret.**](/windows/desktop/api/Winuser/nf-winuser-hidecaret) Esto resulta útil cuando la aplicación debe volver a dibujar la pantalla durante el procesamiento de un mensaje, pero debe mantener el centro de atención fuera del camino. Cuando la aplicación termina de dibujar, puede volver a mostrar el caret mediante la [**función ShowCaret.**](/windows/desktop/api/Winuser/nf-winuser-showcaret) Ocultar el objeto de inserción no destruye su forma ni invalida el punto de inserción. Ocultar el caret es acumulativo; Es decir, si la aplicación llama a **HideCaret** cinco veces, también debe llamar a **ShowCaret** cinco veces antes de que el caret vuelva a aparecer.

Para quitar el objeto de la pantalla y destruir su forma, use la [**función DestroyCaret.**](/windows/desktop/api/Winuser/nf-winuser-destroycaret) **DestroyCaret** destruye el caret solo si la ventana implicada en la tarea actual posee el objeto de careta.

 

 