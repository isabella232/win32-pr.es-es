---
title: Lista de comandos
description: Una lista de comandos es una secuencia de comandos de GPU que se pueden grabar y reproducir. Una lista de comandos puede mejorar el rendimiento reduciendo la cantidad de sobrecarga generada por el tiempo de ejecución.
ms.assetid: 4f581bc7-6c5e-4e56-b768-7f3cc5dbcb3e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27f8821645588ac7a9b48a4f6ce562c8c48cf96
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777077"
---
# <a name="command-list"></a>Lista de comandos

Una lista de comandos es una secuencia de comandos de GPU que se pueden grabar y reproducir. Una lista de comandos puede mejorar el rendimiento reduciendo la cantidad de sobrecarga generada por el tiempo de ejecución.

Use una lista de comandos en los escenarios siguientes:

-   Dentro de un solo fotograma, representa parte de la escena en un subproceso mientras se graba otra parte de la escena en un segundo subproceso. Al final del marco, vuelva a reproducir la lista de comandos grabada en el primer subproceso. Use este método para escalar tareas de representación complejas entre varios subprocesos o núcleos.
-   Grabe previamente una lista de comandos antes de que tenga que representarla (por ejemplo, mientras se carga un nivel) y reproducirla de forma eficaz más adelante en la escena. Esta optimización funciona bien cuando es necesario representar algo a menudo.

Una lista de comandos es inmutable y está diseñada para grabarse y reproducirse durante una ejecución única de una aplicación. Una lista de comandos no se ha diseñado para que se registre previamente antes de la ejecución del juego y se cargue desde el medio, ya que no hay ninguna manera de conservar la lista.

Un contexto diferido debe registrar una lista de comandos, pero solo se puede reproducir en un contexto inmediato. Los contextos aplazados pueden generar listas de comandos simultáneamente.

-   Para grabar una lista de comandos, consulte [Cómo: grabar una lista de comandos](overviews-direct3d-11-render-multi-thread-command-list-record.md).
-   Para reproducir una lista de comandos, consulte [Cómo: reproducir una lista de comandos](overviews-direct3d-11-render-multi-thread-command-list-play.md).
-   Cuando se usa una lista de comandos, el rendimiento depende de la cantidad de compatibilidad implementada en un controlador. Para comprobar la compatibilidad con controladores, consulte [Cómo: comprobar la compatibilidad de controladores](overviews-direct3d-11-render-multi-thread-support.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representación inmediata y diferida](overviews-direct3d-11-render-multi-thread-render.md)
</dt> <dt>

[MultiThreading](overviews-direct3d-11-render-multi-thread.md)
</dt> </dl>

 

 




