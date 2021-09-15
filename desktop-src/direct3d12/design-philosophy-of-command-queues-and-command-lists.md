---
title: Diseño de la filosofía de las colas y las listas de comandos
description: Los objetivos de habilitar la reutilización del trabajo de representación y del escalado multiproceso requerían cambios fundamentales en la forma en que las aplicaciones de Direct3D envían el trabajo de representación a la GPU.
ms.assetid: C85C8C41-2306-4568-8FAE-F57EDA624298
keywords:
- lista de comandos
- bundle
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 812275a630464dbe9137d587a672803f4d0c72f9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359800"
---
# <a name="design-philosophy-of-command-queues-and-command-lists"></a>Diseño de la filosofía de las colas y las listas de comandos

Los objetivos de habilitar la reutilización del trabajo de representación y del escalado multiproceso requerían cambios fundamentales en la forma en que las aplicaciones de Direct3D envían el trabajo de representación a la GPU. En Direct3D 12, el proceso de envío del trabajo de representación difiere de las versiones anteriores de tres maneras importantes:

<dl> 1. Eliminación del contexto inmediato. Esto habilita el multiproceso.  
2. Las aplicaciones ahora poseen cómo se agrupan las llamadas de representación en elementos de trabajo de la unidad de procesamiento gráfico (GPU). Esto permite volver a usar.  
3. Las aplicaciones ahora controlan explícitamente cuándo se envía el trabajo a la GPU. Esto habilita los elementos 1 y 2.  
</dl>

-   [Eliminación del contexto inmediato](#removal-of-the-immediate-context)
-   [Agrupación de elementos de trabajo de GPU](#grouping-of-gpu-work-items)
-   [Envío de trabajo de GPU](#gpu-work-submission)
-   [Temas relacionados](#related-topics)

## <a name="removal-of-the-immediate-context"></a>Eliminación del contexto inmediato

El cambio más grande de Microsoft Direct3D 11 a Microsoft Direct3D 12 es que ya no hay un único contexto inmediato asociado a un dispositivo. En su lugar, para representar, las aplicaciones crean listas de comandos en las que se puede llamar a las API de representación tradicionales. Una lista de comandos es similar al método de representación de una aplicación de Direct3D 11 que usa el contexto inmediato en que contiene llamadas que dibujan primitivas o cambian el estado de representación. Al igual que los contextos inmediatos, cada lista de comandos no tiene subprocesos libres; sin embargo, se pueden registrar varias listas de comandos simultáneamente, lo que aprovecha los procesadores modernos de varios núcleos.

Las listas de comandos normalmente se ejecutan una vez. Sin embargo, una lista de comandos se puede ejecutar varias veces si la aplicación garantiza que las ejecuciones anteriores se completan antes de enviar nuevas ejecuciones. Para obtener más información sobre la sincronización de listas de comandos, vea [Executing and synchronizing command lists](executing-and-synchronizing-command-lists.md).

## <a name="grouping-of-gpu-work-items"></a>Agrupación de elementos de trabajo de GPU

Además de las listas de comandos, Direct3D 12 aprovecha la funcionalidad presente actualmente en todo el hardware mediante la adición de un segundo nivel de listas de comandos, que se *denominan agrupaciones*. Para ayudar a distinguir estos dos tipos, las listas de comandos de primer nivel se pueden denominar listas *de comandos directos.* El propósito de los paquetes es permitir a las aplicaciones agrupar un pequeño número de comandos de API para una ejecución repetida posterior desde listas de comandos directas. En el momento de crear un paquete, el controlador realizará tanto procesamiento previo como sea posible para que la ejecución posterior sea eficaz. Las agrupaciones se pueden ejecutar desde dentro de varias listas de comandos y varias veces dentro de la misma lista de comandos.

El nuevo uso de agrupaciones es un gran controlador de eficiencia mejorada con subprocesos de CPU únicos. Dado que las agrupaciones se procesan previamente y se pueden enviar varias veces, hay ciertas restricciones en las operaciones que se pueden realizar dentro de un paquete. Para obtener más información, vea [Creación y grabación de listas de comandos y agrupaciones.](recording-command-lists-and-bundles.md)

## <a name="gpu-work-submission"></a>Envío de trabajo de GPU

Para ejecutar el trabajo en la GPU, una aplicación debe enviar explícitamente una lista de comandos a una cola de comandos asociada al dispositivo Direct3D. Se puede enviar una lista de comandos directos para su ejecución varias veces, pero la aplicación es responsable de garantizar que la lista de comandos directos haya terminado de ejecutarse en la GPU antes de volver a enviarla. Las agrupaciones no tienen restricciones de uso simultáneo y se pueden ejecutar varias veces en varias listas de comandos, pero no se pueden enviar directamente a una cola de comandos para su ejecución.

Cualquier subproceso puede enviar una lista de comandos a cualquier cola de comandos en cualquier momento y el tiempo de ejecución serializará automáticamente el envío de la lista de comandos en la cola de comandos conservando el orden de envío.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Envío de trabajo en Direct3D 12](command-queues-and-command-lists.md)
</dt> </dl>

 

 




