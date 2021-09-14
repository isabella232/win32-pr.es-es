---
description: En este tema se describe cómo mostrar el progreso del trabajo de impresión al usuario y darle la opción de cancelar un trabajo de impresión que está actualmente en curso.
ms.assetid: 2b7a0ab7-bf7e-473d-ab43-8b79478d4453
title: 'Cómo: Mostrar el progreso del trabajo de impresión'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9effc778f6affaba5b53cbd96a7a428ea5554d8c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168122"
---
# <a name="how-to-display-the-print-job-progress"></a>Cómo: Mostrar el progreso del trabajo de impresión

En este tema se describe cómo mostrar el progreso del trabajo de impresión al usuario y darle la opción de cancelar un trabajo de impresión que está actualmente en curso.

## <a name="overview"></a>Información general

Normalmente, un procedimiento de diálogo de progreso de impresión realiza las siguientes funciones.

-   Muestra el progreso del trabajo de impresión al usuario.
-   Inicie el subproceso de procesamiento de impresión.
-   Muestra un **botón** Cancelar para que el usuario pueda detener un trabajo de impresión antes de que finalice.

Estrictamente hablando, lo único que debe hacer el procedimiento del cuadro de diálogo de progreso de impresión es mostrar el progreso del trabajo de impresión al usuario. Sin embargo, dado que las otras dos funciones de la lista anterior están estrechamente relacionadas, también se han incluido en este módulo.

## <a name="displaying-print-job-progress"></a>Mostrar el progreso del trabajo de impresión

Un procedimiento de cuadro de diálogo de progreso de impresión controla los siguientes mensajes de ventana.

-   **WM \_ INITDIALOG**

    Inicializa los controles que usa el cuadro de diálogo.

-   **WM \_ SETCURSOR**

    Establece el cursor en un puntero cuando el usuario puede cancelar un trabajo de impresión y en el cursor de espera cuando el trabajo de impresión se encuentra en un punto en el que no se puede cancelar.

-   **INICIO DE \_ IMPRESIÓN \_ DE USUARIO IMPRESIÓN \_**

    Establece los parámetros de la barra de progreso del trabajo de impresión y crea el subproceso de impresión para iniciar el procesamiento del trabajo de impresión.

    Se trata de un mensaje de ventana específico de la aplicación.

-   **COMANDO \_ WM: IDCANCEL**

    Establece el evento de cancelación para que le diga al subproceso de procesamiento de impresión que cancele el trabajo de impresión.

-   **ACTUALIZACIÓN \_ DEL ESTADO DE IMPRESIÓN DEL \_ \_ USUARIO**

    Actualiza la barra de progreso y el texto de estado para mostrar el estado actual del trabajo de impresión.

    Se trata de un mensaje de ventana específico de la aplicación.

-   **CIERRE \_ DE IMPRESIÓN DE \_ USUARIO**

    Establece el texto de estado de cierre en el cuadro de diálogo de progreso para indicar que el trabajo de impresión se está cerrando.

    Se trata de un mensaje de ventana específico de la aplicación.

-   **USER \_ PRINT \_ COMPLETE**

    Muestra el mensaje "Imprimir el trabajo completado" al usuario y libera los identificadores y eventos que se usaron en este trabajo de impresión.

    Se trata de un mensaje de ventana específico de la aplicación.

 

 



