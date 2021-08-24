---
description: Cuando se realiza una acción determinada, la aplicación envía y recibe de forma casi instantánea los eventos del sistema (con el prefijo \_ ISG).
ms.assetid: deca6d17-fe2c-4130-88ca-d0605bcb6084
title: Escala de tiempo de mensajes del mouse y eventos del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 635147b3f30b8746c75901de78336102ac8d1b41a685919c27f990496f5f225d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119819614"
---
# <a name="timeline-of-mouse-messages-and-system-events"></a>Escala de tiempo de mensajes del mouse y eventos del sistema

Cuando se realiza una acción determinada, la aplicación envía y recibe de forma casi instantánea los eventos del sistema (con el prefijo \_ ISG). Los mensajes del mouse (con el prefijo WM) se envían cuando se realiza la acción y la aplicación los recibe después del tiempo necesario para que el servicio de mensajería de Microsoft Windows procese \_ el evento. Además, **CursorDown y** **CursorUp** son eventos de lápiz que se reciben desde el hardware del lápiz. Se envían cuando el lápiz de tableta toca la pantalla y cuando se eleva de la pantalla, respectivamente.

Los eventos de lápiz y los mensajes del mouse no se sincronizan. No hay ninguna garantía de que los mensajes del mouse y los eventos de lápiz correspondientes se produzcan en un orden determinado. En el gráfico siguiente se muestra la secuencia esperada, pero no siempre predecible, de eventos del sistema y del mouse que se envían. Observe en el gráfico que los eventos del mouse se retrasan cuando se detectan eventos de gestos del sistema.

![secuencia esperada de eventos del sistema y del mouse para la entrada de lápiz](images/ccdafa48-13c0-4af7-aec5-ed162be4bbe7.jpg)

## <a name="important-implementation-considerations"></a>Consideraciones de implementación importantes

Tenga en cuenta lo siguiente al desarrollar para mensajes del mouse y eventos del sistema:

-   Tanto los eventos de lápiz como los mensajes del mouse se envían a una aplicación, independientemente de si se usa el lápiz o el mouse.
-   Si la aplicación escucha mensajes de lápiz y mouse, es difícil predecir la relación de los mensajes y, por tanto, el comportamiento final. Los eventos de lápiz y los mensajes del mouse no se sincronizan. No hay ninguna garantía de que los mensajes del mouse y los eventos de lápiz correspondientes (como WM \_ LBUTTONDOWN e **ISG \_ TAP,** o WM \_ LBUTTONDBLCLK e **ISG \_ DBLTAP)** se produzcan en un orden determinado. La relación entre estos mensajes es compleja.
-   Se recomienda no mezclar y emparejar eventos de mouse y lápiz en la misma característica de aplicación. Por ejemplo, es posible que una característica de aplicación que responda a **CursorDown** y **MouseUp** no se comporte como se esperaba ahora o con versiones futuras del SDK de Tablet PC.
-   Para la secuencia de eventos de retención, si el usuario arrastra el lápiz de tableta antes de que se complete la secuencia, los eventos que se envían se corresponden con el arrastre izquierdo. Por ejemplo, cuando se inicia la arrastre, se envían **ISG \_ DRAG** y WM \_ LBUTTONDOWN. Cuando finalmente se eleva el lápiz, se envían **CursorUp** y WM \_ LBUTTONUP. Es posible que el evento de gesto del sistema no se desaprenda inmediatamente porque debe determinar qué tipo de evento se está produciendo.
-   Una pulsación doble con un lápiz de tableta suele ser menos precisa que un doble clic con un mouse. Esto proviene de la naturaleza inherente de realizar una doble pulsación con un lápiz de tableta. Dado que el usuario debe elevar el lápiz de tableta para realizar una doble pulsación, el tiempo entre pulsaciones suele ser mayor que el tiempo correspondiente entre los clics de un doble clic. Además, es probable que las dos pulsaciones del lápiz de tableta se produzcan en coordenadas de pantalla que están más separadas que las de los dos clics del mouse. Para adaptarse a esto, Windows XP Tablet PC Edition tiene una configuración para la distancia temporal y espacial entre las dos pulsaciones de una pulsación doble que son independientes de la configuración del mouse para un doble clic. Esta configuración se puede ajustar en tabletas y Configuración en Panel de control.

Debido a estas consideraciones, las aplicaciones deben escuchar solo un conjunto de mensajes en lugar de ambos. Si va a compilar una aplicación habilitada para lápiz, escuche solo los mensajes del sistema y del lápiz. Estos mensajes son predecibles y funcionan bien con el lápiz de tableta. Si va a compilar una aplicación que no está habilitada para lápiz, escuche solo los mensajes del mouse.

 

 



