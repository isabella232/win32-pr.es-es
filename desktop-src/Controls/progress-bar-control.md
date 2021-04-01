---
title: Acerca de los controles de barra de progreso
description: Una barra de progreso es una ventana que una aplicación puede utilizar para indicar el progreso de una operación larga. Está compuesto de un rectángulo que se anima a medida que progresa una operación.
ms.assetid: 1db7a5c9-71cd-4ebc-86b8-8159f30348fa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f00c80b1f9e97cec1657fe979a19437f607251b8
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103793989"
---
# <a name="about-progress-bar-controls"></a>Acerca de los controles de barra de progreso

Una barra de progreso es una ventana que una aplicación puede utilizar para indicar el progreso de una operación larga.

Está compuesto de un rectángulo que se anima a medida que progresa una operación.

En la ilustración siguiente se muestra una barra de progreso que no utiliza estilos visuales.

![captura de pantalla de una barra de progreso que agrega rectángulos en una línea para indicar el progreso](images/pb-oldstyle.png)

En la ilustración siguiente se muestra una barra de progreso con estilos visuales. La apariencia del control variará en función del sistema operativo y del tema seleccionado. Para obtener más información, vea [estilos visuales](themes-overview.md).

![captura de pantalla de una barra de progreso que alarga un rectángulo verde animado para indicar el progreso](images/pb-newstyle.png)

En los siguientes encabezados se incluye más información.

-   [Usar barras de progreso](#using-progress-bars)
    -   [Intervalo y posición actual](#range-and-current-position)
    -   [Procesamiento de mensajes de la barra de progreso predeterminada](#default-progress-bar-message-processing)
    -   [Estilo de marquesina](#marquee-style)

## <a name="using-progress-bars"></a>Usar barras de progreso

Puede crear una barra de progreso mediante la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , especificando la clase de ventana [**\_ clase de progreso**](common-control-window-classes.md) . Esta clase de ventana se registra cuando se carga el archivo DLL de controles comunes. Para obtener más información, vea [acerca de los controles comunes](common-controls-intro.md).

El control también está disponible en el cuadro de herramientas Microsoft Visual Studio, donde se denomina control de progreso.

### <a name="range-and-current-position"></a>Intervalo y posición actual

El *intervalo* de una barra de progreso representa la duración completa de la operación y la *posición actual* representa el progreso que ha realizado la aplicación para completar la operación. El procedimiento de ventana usa el rango y la posición actual para determinar el porcentaje de la barra de progreso que se va a rellenar con el color de resaltado.

Si no establece los valores del intervalo, el sistema establece el valor mínimo en 0 y el valor máximo en 100. Puede ajustar el intervalo a los enteros cómodos mediante el mensaje de [**\_ SetRange de PBM**](pbm-setrange.md) .

Una barra de progreso proporciona varios mensajes que se pueden utilizar para establecer la posición actual. El mensaje de [**\_ SETPOS de PBM**](pbm-setpos.md) establece la posición en un valor determinado. El [**mensaje \_ DELTAPOS de PBM**](pbm-deltapos.md) hace avanzar la posición agregando un valor especificado a la posición actual.

El [**mensaje \_ SETSTEP de PBM**](pbm-setstep.md) le permite especificar un incremento de paso para una barra de progreso. Posteriormente, cada vez que envíe el mensaje de [**\_ STEPIT de PBM**](pbm-stepit.md) a la barra de progreso, la posición actual avanzará en el incremento especificado. De forma predeterminada, el incremento de paso se establece en 10.

### <a name="default-progress-bar-message-processing"></a>Procesamiento de mensajes de la barra de progreso predeterminada

En esta sección se describen los mensajes administrados por el procedimiento de ventana para la clase de [**\_ clase Progress**](common-control-window-classes.md) .



| Message            | Procesamiento realizado                                                                                                                                                               |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **creación de WM \_**     | Asigna e inicializa una estructura inicial.                                                                                                                                    |
| **destrucción de WM \_**    | Libera todos los recursos asociados a la barra de progreso.                                                                                                                              |
| **ERASEBKGND de WM \_** | Dibuja el fondo y los bordes de la barra de progreso.                                                                                                                              |
| **GETFONT de WM \_**    | Devuelve el identificador de la fuente actual. La barra de progreso no dibuja texto actualmente, por lo que el envío de este mensaje no tiene ningún efecto en el control.                                       |
| **pintura de WM \_**      | Dibuja la barra de progreso. Si el parámetro *wParam* no es **null**, el control supone que el valor es HDC y pinta usando ese contexto de dispositivo.                              |
| **WM \_**    | Guarda el identificador de la nueva fuente y devuelve el identificador de la fuente anterior. La barra de progreso no dibuja texto actualmente, por lo que el envío de este mensaje no tiene ningún efecto en el control. |



 

### <a name="marquee-style"></a>Estilo de marquesina

Al crear el control de barra de progreso con el estilo de [**\_ marquesina de PBS**](progress-bar-control-styles.md) , puede animarlo de manera que muestre la actividad, pero no indica qué proporción de la tarea se ha completado. La parte resaltada de la barra de progreso se mueve varias veces a lo largo de la longitud de la barra. Puede iniciar y detener la animación y controlar su velocidad mediante el envío del mensaje de [**\_ SETMARQUEE de PBM**](pbm-setmarquee.md) . Las barras de progreso de la marquesina no tienen un intervalo o una posición.

En la ilustración siguiente se muestra una barra de progreso en el modo de marquesina. La parte resaltada se desplaza por la barra.

![captura de pantalla de una barra de progreso que desplaza un resaltado verde por un rectángulo gris para indicar el progreso](images/pb-marquee.png)

 

 