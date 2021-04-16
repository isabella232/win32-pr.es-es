---
description: Las aplicaciones pueden esperar en un evento cuando no es necesario representar en la pantalla (es decir, mientras se ocluidos).
ms.assetid: B9EC23C9-A311-4BD9-BBE8-908A1334A541
title: Esperar en un evento cuando no es necesaria la representación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b553ef52e812c5117e5d9669ba13b47b9f4280c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686264"
---
# <a name="waiting-on-an-event-when-rendering-is-unnecessary"></a>Esperar en un evento cuando no es necesaria la representación

Las aplicaciones pueden esperar en un evento cuando no es necesario representar en la pantalla (es decir, mientras se ocluidos). Cuando el Administrador de ventanas de escritorio (DWM) o una aplicación es ocluidos, no es necesario realizar ninguna representación y el sistema operativo puede permanecer en un estado de energía inferior durante períodos de tiempo más largos. Esto ahorra energía y amplía la duración de la batería.

Una aplicación puede esperar en un evento cuando:

-   Todos los monitores están desactivados.
-   La sesión en la que se ejecuta la aplicación está desconectada.
-   La aplicación se ejecuta en pantalla completa exclusivamente en una única configuración de monitor.
-   La aplicación se ejecuta en un escritorio diferente que el escritorio activo y no tiene permiso para representarse en el escritorio activo.

El sistema operativo desencadena el evento cuando la aplicación puede representarse de nuevo. El evento no se borra durante la actualización de un controlador o el proceso de detección y recuperación (TDR) de tiempo de espera, pero se borra cuando el nuevo adaptador y los monitores se activan.

Si desea que la aplicación reciba notificaciones sobre los cambios de estado de la oclusión, la aplicación debe registrarse para estos cambios. Una aplicación puede registrarse para recibir notificaciones sobre los cambios de estado de la oclusión a través de un mensaje a una ventana o a través de la señalización de eventos. Para registrarse para recibir mensajes de notificación en una ventana sobre los cambios de estado de la oclusión, una aplicación llama al método [**IDXGIFactory2:: RegisterOcclusionStatusWindow**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatuswindow) . Para registrarse para recibir notificaciones de los cambios de estado de la oclusión a través de la señalización de eventos, una aplicación llama al método [**IDXGIFactory2:: RegisterOcclusionStatusEvent**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatusevent) . Ambos métodos devuelven un puntero a un valor de clave que la aplicación puede usar para anular el registro de la notificación. Para anular el registro de la notificación, la aplicación pasa este valor de clave al método [**IDXGIFactory2:: UnregisterOcclusionStatus**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-unregisterocclusionstatus) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Mejoras en DXGI 1,2](dxgi-1-2-improvements.md)
</dt> </dl>

 

 



