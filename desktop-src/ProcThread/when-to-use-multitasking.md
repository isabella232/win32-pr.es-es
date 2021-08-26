---
description: 'Hay dos maneras de implementar la multitarea: como un único proceso con varios subprocesos o como varios procesos, cada uno con uno o varios subprocesos.'
ms.assetid: ac0a8163-1498-4274-acfc-6a36b4c02a27
title: Cuándo usar multitarea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee3e37f63ada4aa1a17355ac3bc5b7361d498a1a20ec87b490965b53c4811ebb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031345"
---
# <a name="when-to-use-multitasking"></a>Cuándo usar multitarea

Hay dos maneras de implementar la multitarea: como un único proceso con varios subprocesos o como varios procesos, cada uno con uno o varios subprocesos. Una aplicación puede colocar cada subproceso que requiere un espacio de direcciones privadas y recursos privados en su propio proceso, para protegerlo de las actividades de otros subprocesos de proceso.

Un proceso multiproceso puede administrar tareas mutuamente excluyentes con subprocesos, como proporcionar una interfaz de usuario y realizar cálculos en segundo plano. La creación de un proceso multiproceso también puede ser una manera cómoda de estructurar un programa que realiza varias tareas similares o idénticas simultáneamente. Por ejemplo, un servidor de canalización con nombre puede crear un subproceso para cada proceso de cliente que se asocia a la canalización. Este subproceso administra la comunicación entre el servidor y el cliente. El proceso podría usar varios subprocesos para realizar las siguientes tareas:

-   Administrar la entrada para varias ventanas.
-   Administrar la entrada de varios dispositivos de comunicaciones.
-   Distinguir tareas de diversas prioridades. Por ejemplo, un subproceso de prioridad alta administra tareas críticas en el tiempo, y un subproceso de prioridad baja realiza otras tareas.
-   Permitir que la interfaz de usuario siga respondiendo, mientras se asigna tiempo a tareas en segundo plano.

Normalmente, es más eficaz para una aplicación implementar la multitarea mediante la creación de un único proceso multiproceso, en lugar de crear varios procesos, por los siguientes motivos:

-   El sistema puede realizar un cambio de contexto más rápidamente para subprocesos que procesos, porque un proceso tiene más sobrecarga que un subproceso (el contexto de proceso es mayor que el contexto del subproceso).
-   Todos los subprocesos de un proceso comparten el mismo espacio de direcciones y pueden acceder a las variables globales del proceso, lo que puede simplificar la comunicación entre subprocesos.
-   Todos los subprocesos de un proceso pueden compartir identificadores abiertos con recursos, como archivos y canalizaciones.

Hay otras técnicas que puede usar en lugar de multithreading. Los más significativos son los siguientes: entrada y salida asincrónicas (E/S), puertos de finalización de E/S, llamadas a procedimientos asincrónicos (APC) y la capacidad de esperar varios eventos.

Un único subproceso puede iniciar varias solicitudes de E/S lentas que se pueden ejecutar simultáneamente mediante E/S asincrónica. La E/S asincrónica se puede realizar en archivos, canalizaciones y dispositivos de comunicación en serie. Para obtener más información, vea [Synchronization and Overlapped Input and Output](../sync/synchronization-and-overlapped-input-and-output.md).

Un único subproceso puede bloquear su propia ejecución mientras se espera a que se produzcan uno o varios eventos. Esto es más eficaz que usar varios subprocesos, cada uno esperando un único evento y más eficaz que usar un único subproceso que consume tiempo de procesador comprobando continuamente si se producen eventos. Para obtener más información, vea [Wait Functions](../sync/wait-functions.md).

 

 
