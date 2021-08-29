---
title: Acerca de los controles de barra de progreso
description: Una barra de progreso es una ventana que una aplicación puede usar para indicar el progreso de una operación larga. Consta de un rectángulo animado a medida que progresa una operación.
ms.assetid: 1db7a5c9-71cd-4ebc-86b8-8159f30348fa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e46b8950da2cadcc1dc3d8f36d9005487be245440a76f700ec7fdfe2a196d87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061685"
---
# <a name="about-progress-bar-controls"></a>Acerca de los controles de barra de progreso

Una barra de progreso es una ventana que una aplicación puede usar para indicar el progreso de una operación larga.

Consta de un rectángulo animado a medida que progresa una operación.

En la ilustración siguiente se muestra una barra de progreso que no usa estilos visuales.

![captura de pantalla de una barra de progreso que agrega rectángulos en una línea para indicar el progreso](images/pb-oldstyle.png)

En la ilustración siguiente se muestra una barra de progreso con estilos visuales. La apariencia del control variará según el sistema operativo y el tema seleccionado. Para obtener más información, vea [Estilos visuales.](themes-overview.md)

![captura de pantalla de una barra de progreso que larga un rectángulo verde animado para indicar el progreso](images/pb-newstyle.png)

Encontrará más información en los encabezados siguientes.

-   [Uso de barras de progreso](#using-progress-bars)
    -   [Rango y posición actual](#range-and-current-position)
    -   [Procesamiento de mensajes de barra de progreso predeterminado](#default-progress-bar-message-processing)
    -   [Estilo de marquesina](#marquee-style)

## <a name="using-progress-bars"></a>Uso de barras de progreso

Puede crear una barra de progreso mediante la [**función CreateWindowEx,**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) especificando la [**clase de ventana PROGRESS \_ CLASS.**](common-control-window-classes.md) Esta clase de ventana se registra cuando se carga el archivo DLL de controles comunes. Para obtener más información, vea [Acerca de los controles comunes.](common-controls-intro.md)

El control también está disponible en el cuadro Microsoft Visual Studio, donde se denomina Control de progreso.

### <a name="range-and-current-position"></a>Rango y posición actual

El intervalo de una barra *de* progreso representa  toda la duración de la operación y la posición actual representa el progreso que la aplicación ha realizado para completar la operación. El procedimiento de ventana usa el intervalo y la posición actual para determinar el porcentaje de la barra de progreso que se va a rellenar con el color de resaltado.

Si no establece los valores de intervalo, el sistema establece el valor mínimo en 0 y el valor máximo en 100. Puede ajustar el intervalo a enteros prácticos mediante el mensaje [**\_ PBM SETRANGE.**](pbm-setrange.md)

Una barra de progreso proporciona varios mensajes que puede usar para establecer la posición actual. El [**mensaje \_ SETPOS de PBM**](pbm-setpos.md) establece la posición en un valor determinado. El [**mensaje \_ PBM DELTAPOS**](pbm-deltapos.md) avanza la posición agregando un valor especificado a la posición actual.

El [**mensaje \_ PBM SETSTEP**](pbm-setstep.md) permite especificar un incremento de paso para una barra de progreso. Posteriormente, cada vez que se envía el mensaje [**\_ STEPIT**](pbm-stepit.md) de PBM a la barra de progreso, la posición actual avanza según el incremento especificado. De forma predeterminada, el incremento de paso se establece en 10.

### <a name="default-progress-bar-message-processing"></a>Procesamiento de mensajes de barra de progreso predeterminado

En esta sección se describen los mensajes que controla el procedimiento de ventana para la [**clase PROGRESS \_ CLASS.**](common-control-window-classes.md)



| Message            | Procesamiento realizado                                                                                                                                                               |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **WM \_ CREATE**     | Asigna e inicializa una estructura inicial.                                                                                                                                    |
| **WM \_ DESTROY**    | Libera todos los recursos asociados a la barra de progreso.                                                                                                                              |
| **WM \_ ERASEBND** | Dibuja el fondo y los bordes de la barra de progreso.                                                                                                                              |
| **WM \_ GETFONT**    | Devuelve el identificador a la fuente actual. Actualmente, la barra de progreso no dibuja texto, por lo que enviar este mensaje no tiene ningún efecto en el control.                                       |
| **WM \_ PAINT**      | Dibuja la barra de progreso. Si el *parámetro wParam* no es **NULL,** el control supone que el valor es un HDC y pinta con ese contexto de dispositivo.                              |
| **WM \_ SETFONT**    | Guarda el identificador en la nueva fuente y devuelve el identificador a la fuente anterior. Actualmente, la barra de progreso no dibuja texto, por lo que enviar este mensaje no tiene ningún efecto en el control. |



 

### <a name="marquee-style"></a>Estilo de marquesina

Al crear el control de barra de progreso con el estilo [**\_ MARQUEE de PBS,**](progress-bar-control-styles.md) puede animarlo de forma que muestre la actividad, pero no indique qué proporción de la tarea se ha completado. La parte resaltada de la barra de progreso se mueve repetidamente a lo largo de la longitud de la barra. Puede iniciar y detener la animación y controlar su velocidad mediante el envío del mensaje [**\_ SETMARQUEE de PBM.**](pbm-setmarquee.md) Las barras de progreso de marquesina no tienen un intervalo ni una posición.

En la ilustración siguiente se muestra una barra de progreso en modo de marquesina. La parte resaltada se mueve a través de la barra.

![captura de pantalla de una barra de progreso que mueve un resaltado verde a través de un rectángulo gris para indicar el progreso](images/pb-marquee.png)

 

 