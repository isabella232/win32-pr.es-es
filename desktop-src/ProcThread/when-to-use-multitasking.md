---
description: 'Hay dos maneras de implementar la multitarea: como un solo proceso con varios subprocesos o como varios procesos, cada uno con uno o más subprocesos.'
ms.assetid: ac0a8163-1498-4274-acfc-6a36b4c02a27
title: Cuándo usar la multitarea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b17e52f39a08120d3038663a95307ad72f228cfc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105677982"
---
# <a name="when-to-use-multitasking"></a>Cuándo usar la multitarea

Hay dos maneras de implementar la multitarea: como un solo proceso con varios subprocesos o como varios procesos, cada uno con uno o más subprocesos. Una aplicación puede poner cada subproceso que requiera un espacio de direcciones privado y recursos privados en su propio proceso, para protegerlo de las actividades de otros subprocesos del proceso.

Un proceso multiproceso puede administrar tareas mutuamente exclusivas con subprocesos, como proporcionar una interfaz de usuario y realizar cálculos en segundo plano. La creación de un proceso multiproceso también puede ser una manera cómoda de estructurar un programa que realiza varias tareas similares o idénticas simultáneamente. Por ejemplo, un servidor de canalización con nombre puede crear un subproceso para cada proceso de cliente que se adjunta a la canalización. Este subproceso administra la comunicación entre el servidor y el cliente. El proceso podría usar varios subprocesos para realizar las tareas siguientes:

-   Administrar la entrada de varias ventanas.
-   Administrar la entrada desde varios dispositivos de comunicaciones.
-   Distinguir tareas de diversas prioridades. Por ejemplo, un subproceso de prioridad alta administra tareas críticas en el tiempo, y un subproceso de prioridad baja realiza otras tareas.
-   Permitir que la interfaz de usuario siga respondiendo, mientras se asigna tiempo a tareas en segundo plano.

Normalmente, es más eficaz para una aplicación implementar la multitarea mediante la creación de un único proceso multiproceso, en lugar de crear varios procesos, por las razones siguientes:

-   El sistema puede realizar un cambio de contexto más rápidamente para los subprocesos que los procesos, ya que un proceso tiene más sobrecarga que un subproceso (el contexto del proceso es mayor que el contexto del subproceso).
-   Todos los subprocesos de un proceso comparten el mismo espacio de direcciones y pueden tener acceso a las variables globales del proceso, lo que puede simplificar la comunicación entre subprocesos.
-   Todos los subprocesos de un proceso pueden compartir identificadores abiertos en los recursos, como archivos y canalizaciones.

Hay otras técnicas que puede usar en lugar de multithreading. Las más importantes son las siguientes: la entrada y salida (e/s) asincrónica, los puertos de finalización de e/s, las llamadas a procedimiento asincrónico (APC) y la capacidad de esperar varios eventos.

Un solo subproceso puede iniciar varias solicitudes de e/s que requieren mucho tiempo y que se pueden ejecutar simultáneamente mediante la e/s asincrónica. La e/s asincrónica se puede realizar en archivos, canalizaciones y dispositivos de comunicación en serie. Para obtener más información, vea [sincronización y entrada y salida superpuestas](../sync/synchronization-and-overlapped-input-and-output.md).

Un solo subproceso puede bloquear su propia ejecución mientras se espera a que se produzcan uno o varios eventos. Esto es más eficaz que el uso de varios subprocesos, cada uno de los cuales espera un único evento y más eficaz que usar un único subproceso que consume tiempo de procesador al comprobar continuamente si se producen eventos. Para obtener más información, vea [funciones de espera](../sync/wait-functions.md).

 

 
