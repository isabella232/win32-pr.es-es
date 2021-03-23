---
title: Diseño de la filosofía de las colas de comandos y listas de comandos
description: Los objetivos de habilitar la reutilización del trabajo de representación y del escalado multiproceso requieren cambios fundamentales en el modo en que las aplicaciones de Direct3D envían el trabajo de representación a la GPU.
ms.assetid: C85C8C41-2306-4568-8FAE-F57EDA624298
keywords:
- lista de comandos
- bundle
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 812275a630464dbe9137d587a672803f4d0c72f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104583"
---
# <a name="design-philosophy-of-command-queues-and-command-lists"></a>Diseño de la filosofía de las colas de comandos y listas de comandos

Los objetivos de habilitar la reutilización del trabajo de representación y del escalado multiproceso requieren cambios fundamentales en el modo en que las aplicaciones de Direct3D envían el trabajo de representación a la GPU. En Direct3D 12, el proceso de envío del trabajo de representación es diferente de las versiones anteriores de tres maneras importantes:

<dl> 1. Eliminación del contexto inmediato. Esto habilita el multithreading.  
2. Las aplicaciones ahora poseen el modo en que las llamadas de representación se agrupan en elementos de trabajo de la unidad de procesamiento de gráficos (GPU). Esto permite volver a usar.  
3. Ahora, las aplicaciones controlan explícitamente Cuándo se envía el trabajo a la GPU. Esto habilita los elementos 1 y 2.  
</dl>

-   [Eliminación del contexto inmediato](#removal-of-the-immediate-context)
-   [Agrupación de elementos de trabajo de GPU](#grouping-of-gpu-work-items)
-   [Envío de trabajo de GPU](#gpu-work-submission)
-   [Temas relacionados](#related-topics)

## <a name="removal-of-the-immediate-context"></a>Eliminación del contexto inmediato

El cambio más grande de Microsoft Direct3D 11 a Microsoft Direct3D 12 es que ya no hay un contexto único y inmediato asociado a un dispositivo. En su lugar, para representar, las aplicaciones crean listas de comandos en las que se puede llamar a las API de representación tradicionales. Una lista de comandos es similar al método Render de una aplicación Direct3D 11 que usaba el contexto inmediato en que contiene llamadas que dibujan primitivas o cambian el estado de representación. Al igual que los contextos inmediatos, cada lista de comandos no es de subproceso libre; sin embargo, se pueden grabar varias listas de comandos simultáneamente, lo que aprovecha los procesadores modernos de varios núcleos.

Normalmente, las listas de comandos se ejecutan una vez. Sin embargo, se puede ejecutar varias veces una lista de comandos si la aplicación garantiza que las ejecuciones anteriores se hayan completado antes de enviar nuevas ejecuciones. Para obtener más información acerca de la sincronización de la lista de comandos, vea [Ejecutar y sincronizar listas de comandos](executing-and-synchronizing-command-lists.md).

## <a name="grouping-of-gpu-work-items"></a>Agrupación de elementos de trabajo de GPU

Además de las listas de comandos, Direct3D 12 aprovecha la funcionalidad presente en todo el hardware en la actualidad agregando un segundo nivel de listas de comandos, que se denominan *agrupaciones*. Para ayudar a distinguir estos dos tipos, se puede hacer referencia a las listas de comandos de primer nivel como *listas de comandos directas*. El propósito de las agrupaciones es permitir que las aplicaciones agrupen un pequeño número de comandos de la API juntos para una ejecución posterior, repetidas desde las listas de comandos directas. En el momento de crear un paquete, el controlador realizará el preprocesamiento que sea posible para que la ejecución posterior sea eficaz. Después, los paquetes se pueden ejecutar desde varias listas de comandos y varias veces dentro de la misma lista de comandos.

La reutilización de los paquetes es un gran controlador de eficacia mejorada con subprocesos de CPU únicos. Dado que las agrupaciones se procesan previamente y se pueden enviar varias veces, existen algunas restricciones sobre las operaciones que se pueden realizar en una agrupación. Para obtener más información, vea [crear y grabar listas de comandos y agrupaciones](recording-command-lists-and-bundles.md).

## <a name="gpu-work-submission"></a>Envío de trabajo de GPU

Para ejecutar el trabajo en la GPU, una aplicación debe enviar explícitamente una lista de comandos a una cola de comandos asociada con el dispositivo Direct3D. Una lista de comandos directa se puede enviar para su ejecución varias veces, pero la aplicación es responsable de garantizar que la lista de comandos directos ha terminado de ejecutarse en la GPU antes de volver a enviarla. Las agrupaciones no tienen restricciones de uso simultáneo y se pueden ejecutar varias veces en varias listas de comandos, pero las agrupaciones no se pueden enviar directamente a una cola de comandos para su ejecución.

Cualquier subproceso puede enviar una lista de comandos a cualquier cola de comandos en cualquier momento, y el tiempo de ejecución serializará automáticamente el envío de la lista de comandos en la cola de comandos mientras se conserva el orden de envío.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Envío de trabajo en Direct3D 12](command-queues-and-command-lists.md)
</dt> </dl>

 

 




