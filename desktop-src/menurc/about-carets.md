---
title: Acerca de las intercalaciones
description: En este tema se describen las intercalaciones.
ms.assetid: 4487c93c-9a0f-467c-86b1-969f664d5526
keywords:
- recursos, insumos
- insumos, quitar
- líneas intermitentes
- bloques en parpadeo
- parpadeo de mapas de bits
- intercalaciones, visibilidad
- Acentos, tiempos de intermitencia
- tiempos de intermitencia
- insumos, posiciones
- quitar insumos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a19eb3895ada13297f090a09529b2bcb7c75dee
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105704957"
---
# <a name="about-carets"></a>Acerca de las intercalaciones

El sistema proporciona un símbolo de intercalación por cola de mensajes. Una ventana debe crear un símbolo de intercalación solo cuando tiene el foco de teclado o está activo. La ventana debe destruir el símbolo de intercalación antes de perder el foco de teclado o de ser inactivo. Para obtener más información sobre la entrada mediante teclado, consulte [entrada de teclado](/windows/desktop/inputdev/keyboard-input).

Use la función [**CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret) para especificar los parámetros de un símbolo de intercalación. El sistema forma un símbolo de intercalación al invertir el color del píxel dentro del rectángulo especificado por la posición, el ancho y el alto del símbolo de intercalación. El ancho y el alto se especifican en unidades lógicas; por lo tanto, la apariencia de un símbolo de intercalación está sujeta al modo de asignación de la ventana.

Los temas siguientes se describen en esta sección.

-   [Visibilidad del símbolo de intercalación](#caret-visibility)
-   [Tiempo de parpadeo del símbolo de intercalación](#caret-blink-time)
-   [Posición del símbolo de intercalación](#caret-position)
-   [Quitar un símbolo de intercalación](#removing-a-caret)

## <a name="caret-visibility"></a>Visibilidad del símbolo de intercalación

Una vez definido el símbolo de intercalación, use la función [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret) para que el símbolo de intercalación esté visible. Cuando aparece el símbolo de intercalación, comienza automáticamente el parpadeo. Para mostrar un símbolo de intercalación sólido, el sistema invierte todos los píxeles del rectángulo; para mostrar un símbolo de intercalación gris, el sistema invierte todos los demás píxeles; para mostrar un símbolo de intercalación de mapa de bits, el sistema invierte solo los bits blancos del mapa de bits.

## <a name="caret-blink-time"></a>Tiempo de parpadeo del símbolo de intercalación

El tiempo transcurrido, en milisegundos, necesario para invertir el símbolo de intercalación se denomina *tiempo de intermitencia*. El símbolo de intercalación parpadeará siempre que el subproceso propietario de la cola de mensajes tenga un bombeo de mensajes que procese los mensajes.

El usuario puede establecer el tiempo de parpadeo del símbolo de intercalación mediante el panel de control y las aplicaciones deben respetar los valores de configuración que el usuario haya elegido. Una aplicación puede determinar el tiempo de parpadeo del símbolo de intercalación mediante la función [**GetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-getcaretblinktime) . Si está escribiendo una aplicación que permite al usuario ajustar el tiempo de intermitencia, como un applet del panel de control, utilice la función [**SetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) para establecer la velocidad del tiempo de intermitencia en un número especificado de milisegundos.

La *hora de Flash* es el tiempo transcurrido, en milisegundos, necesario para mostrar, invertir y restaurar la pantalla del símbolo de intercalación. La hora de parpadeo de un símbolo de intercalación es dos veces mayor que el tiempo de intermitencia.

## <a name="caret-position"></a>Posición del símbolo de intercalación

Puede determinar la posición del símbolo de intercalación mediante la función [**GetCaretPos**](/windows/desktop/api/Winuser/nf-winuser-getcaretpos) . La posición, en coordenadas de cliente, se copia en una estructura especificada por un parámetro en **GetCaretPos**. Una aplicación puede desplace un símbolo de intercalación en una ventana mediante la función [**SetCaretPos**](/windows/desktop/api/Winuser/nf-winuser-setcaretpos) . Una ventana solo puede desplace un símbolo de intercalación si ya posee el símbolo de intercalación. **SetCaretPos** puede desplace el símbolo de intercalación si está visible o no.

## <a name="removing-a-caret"></a>Quitar un símbolo de intercalación

Puede quitar temporalmente un símbolo de intercalación si lo oculta o puede quitarlo de forma permanente si lo destruye. Para ocultar el símbolo de intercalación, use la función [**HideCaret**](/windows/desktop/api/Winuser/nf-winuser-hidecaret) . Esto resulta útil cuando la aplicación debe volver a dibujar la pantalla mientras se procesa un mensaje, pero debe mantener el símbolo de intercalación fuera del camino. Cuando la aplicación termina de dibujar, puede volver a mostrar el símbolo de intercalación mediante la función [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret) . Ocultar el símbolo de intercalación no destruye su forma ni invalida el punto de inserción. Ocultar el símbolo de intercalación es acumulativo; es decir, si la aplicación llama a **HideCaret** cinco veces, también debe llamar a **ShowCaret** cinco veces antes de que el símbolo de intercalación vuelva a aparecer.

Para quitar el símbolo de intercalación de la pantalla y destruir su forma, use el uso de la función [**DestroyCaret**](/windows/desktop/api/Winuser/nf-winuser-destroycaret) . **DestroyCaret** destruye el símbolo de intercalación solo si la ventana implicada en la tarea actual posee el símbolo de intercalación.

 

 