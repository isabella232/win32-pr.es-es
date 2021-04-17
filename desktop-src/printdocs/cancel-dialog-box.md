---
description: En este tema se describe cómo mostrar el progreso del trabajo de impresión al usuario y cómo concederles la opción de cancelar un trabajo de impresión que está actualmente en curso.
ms.assetid: 2b7a0ab7-bf7e-473d-ab43-8b79478d4453
title: 'Cómo: mostrar el progreso del trabajo de impresión'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9effc778f6affaba5b53cbd96a7a428ea5554d8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677787"
---
# <a name="how-to-display-the-print-job-progress"></a>Cómo: mostrar el progreso del trabajo de impresión

En este tema se describe cómo mostrar el progreso del trabajo de impresión al usuario y cómo concederles la opción de cancelar un trabajo de impresión que está actualmente en curso.

## <a name="overview"></a>Información general

Un procedimiento de cuadro de diálogo de progreso de impresión normalmente realiza las siguientes funciones.

-   Muestra el progreso del trabajo de impresión al usuario.
-   Inicie el subproceso de procesamiento de impresión.
-   Mostrar un botón **Cancelar** para que el usuario pueda detener un trabajo de impresión antes de que finalice.

En realidad, lo único que debe hacer el procedimiento del cuadro de diálogo progreso de la impresión es mostrar el progreso del trabajo de impresión al usuario. Sin embargo, dado que las otras dos funciones de la lista anterior están estrechamente relacionadas, también se han incluido en este módulo.

## <a name="displaying-print-job-progress"></a>Mostrar el progreso del trabajo de impresión

Un procedimiento de cuadro de diálogo de progreso de impresión controla los siguientes mensajes de ventana.

-   **INITDIALOG de WM \_**

    Inicializa los controles que usa el cuadro de diálogo.

-   **SETCURSOR de WM \_**

    Establece el cursor en un puntero cuando el usuario puede cancelar un trabajo de impresión y en el cursor de espera cuando el trabajo de impresión se encuentra en un punto en el que no se puede cancelar.

-   **\_impresión de \_ Inicio \_ de impresión de usuario**

    Establece los parámetros de la barra de progreso para el trabajo de impresión y crea el subproceso de impresión para empezar a procesar el trabajo de impresión.

    Se trata de un mensaje de ventana específico de la aplicación.

-   **\_comando de WM-IDCANCEL**

    Establece el evento CANCEL para indicar al subproceso de procesamiento de impresión que cancele el trabajo de impresión.

-   **\_actualización de \_ Estado de impresión de usuario \_**

    Actualiza la barra de progreso y el texto de estado para mostrar el estado actual del trabajo de impresión.

    Se trata de un mensaje de ventana específico de la aplicación.

-   **\_cierre de impresión del usuario \_**

    Establece el texto de estado de cierre en el cuadro de diálogo de progreso para indicar que el trabajo de impresión se está cerrando.

    Se trata de un mensaje de ventana específico de la aplicación.

-   **impresión de usuario \_ \_ completada**

    Muestra el mensaje "trabajo de impresión completado" al usuario y libera los identificadores y eventos utilizados en este trabajo de impresión.

    Se trata de un mensaje de ventana específico de la aplicación.

 

 



