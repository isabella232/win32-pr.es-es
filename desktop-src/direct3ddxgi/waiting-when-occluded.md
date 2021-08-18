---
description: Las aplicaciones pueden esperar en un evento cuando la representación en la pantalla no es necesaria (es decir, mientras están oclusiones).
ms.assetid: B9EC23C9-A311-4BD9-BBE8-908A1334A541
title: Esperar a un evento cuando la representación no es necesaria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0db1aa4805aa1dde25947ed25c90d14c9f3c2f4c8693d3599f1382937ee0dbc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118517878"
---
# <a name="waiting-on-an-event-when-rendering-is-unnecessary"></a>Esperar a un evento cuando la representación no es necesaria

Las aplicaciones pueden esperar en un evento cuando la representación en la pantalla no es necesaria (es decir, mientras están oclusiones). Cuando se Administrador de ventanas de escritorio (DWM) o una aplicación, no es necesaria ninguna representación y el sistema operativo puede permanecer en estados de energía inferiores durante períodos de tiempo más largos. Esto ahorra energía y amplía la duración de la batería.

Una aplicación puede esperar en un evento cuando:

-   Todos los monitores están desactivados.
-   La sesión en la que se ejecuta la aplicación está desconectada.
-   La aplicación se ejecuta en pantalla completa exclusivamente en una única configuración de monitor.
-   La aplicación se ejecuta en un escritorio diferente al escritorio activo y no tiene permiso para representarse en el escritorio activo.

El sistema operativo desencadena el evento cuando la aplicación puede volver a representarse. El evento no se borra durante una actualización del controlador ni durante la detección y recuperación de tiempo de espera (TDR), pero se borra cuando el nuevo adaptador y los monitores se activan.

Si desea que se notifique a la aplicación sobre los cambios de estado de oclusión, la aplicación debe registrarse para estos cambios. Una aplicación puede registrarse para recibir notificaciones sobre los cambios de estado de oclusión a través de un mensaje a una ventana o a través de la señalización de eventos. Para registrarse para recibir mensajes de notificación en una ventana sobre los cambios de estado de oclusión, una aplicación llama al método [**IDXGIFactory2::RegisterOcclusionStatusWindow.**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatuswindow) Para registrarse para recibir la notificación de los cambios de estado de oclusión a través de la señalización de eventos, una aplicación llama al método [**IDXGIFactory2::RegisterOcclusionStatusEvent.**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatusevent) Ambos métodos devuelven un puntero a un valor de clave que la aplicación puede usar para anular el registro de la notificación. Para anular el registro de la notificación, la aplicación pasa este valor de clave al [**método IDXGIFactory2::UnregisterOcclusionStatus.**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-unregisterocclusionstatus)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Mejoras de DXGI 1.2](dxgi-1-2-improvements.md)
</dt> </dl>

 

 



