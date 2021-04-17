---
description: Cuando se realiza una acción determinada, la aplicación envía los eventos del sistema (con el prefijo ISG \_ ).
ms.assetid: deca6d17-fe2c-4130-88ca-d0605bcb6084
title: Escala de tiempo de los mensajes del mouse y eventos del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aee3e6cb7882e1628fee0d2bc40f79ed1e29f55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716299"
---
# <a name="timeline-of-mouse-messages-and-system-events"></a>Escala de tiempo de los mensajes del mouse y eventos del sistema

Cuando se realiza una acción determinada, la aplicación envía los eventos del sistema (con el prefijo ISG \_ ). Los mensajes del mouse (con el prefijo WM \_ ) se envían cuando se realiza la acción y los recibe la aplicación después del tiempo que el servicio de mensajería de Microsoft Windows tarda en procesar el evento. Además, **CursorDown** y **CursorUp** son eventos de lápiz que se reciben del hardware del lápiz. Se envían cuando el lápiz de Tablet PC toca la pantalla y cuando se levanta de la pantalla, respectivamente.

Los eventos de lápiz y los mensajes del mouse no se sincronizan. No hay ninguna garantía de que los mensajes del mouse y los eventos del lápiz correspondientes se realicen en un orden determinado. En el gráfico siguiente se muestra la secuencia esperada, pero no siempre predecible, de eventos del sistema y del mouse que se envían. Observe que en el gráfico se retrasan los eventos del mouse cuando se detectan eventos de gesto del sistema.

![secuencia esperada de eventos del sistema y del mouse para la entrada manuscrita](images/ccdafa48-13c0-4af7-aec5-ed162be4bbe7.jpg)

## <a name="important-implementation-considerations"></a>Consideraciones importantes sobre la implementación

Tenga en cuenta lo siguiente al desarrollar para los mensajes del mouse y los eventos del sistema:

-   Los eventos de lápiz y los mensajes del mouse se envían a una aplicación, independientemente de si se usa el lápiz o el mouse.
-   Si la aplicación escucha los mensajes de lápiz y del mouse, es difícil predecir la relación de los mensajes y, por tanto, el comportamiento eventual. Los eventos de lápiz y los mensajes del mouse no se sincronizan. No hay ninguna garantía de que los mensajes del mouse y los eventos del lápiz correspondientes (como WM \_ LBUTTONDOWN y **ISG \_ TAP**, o WM \_ LBUTTONDBLCLK y **ISG \_ DBLTAP**) se produzcan en un orden determinado. La relación entre estos mensajes es compleja.
-   Se recomienda no mezclar y hacer coincidir los eventos del mouse y del lápiz en la misma característica de aplicación. Por ejemplo, es posible que una característica de aplicación que responde a **CursorDown** y a **MouseUp** no se comporte como se esperaba ahora o con versiones futuras del SDK de Tablet PC.
-   En el caso de la secuencia de eventos de retención, si el usuario arrastra el lápiz de Tablet PC antes de que se complete la secuencia, los eventos que se envían se corresponden con los de arrastre a la izquierda. Por ejemplo, cuando se inicia la acción de arrastrar, se envían los **ISG de \_ arrastre** y de WM \_ LBUTTONDOWN. Cuando se levanta el lápiz, se envían los **CursorUp** y \_ LBUTTONUP de WM. Es posible que el evento de gestos del sistema no se active inmediatamente porque debe determinar qué tipo de evento se está produciendo.
-   Un doble punteo con un lápiz de Tablet PC suele ser menos preciso que un doble clic con un mouse. Esto proviene de la naturaleza inherente de la realización de un doble punteo con un lápiz de Tablet PC. Dado que el usuario debe levantar el lápiz de Tablet PC para realizar una doble punteo, el tiempo entre los grifos suele ser mayor que el tiempo correspondiente entre los clics de un doble clic. Además, es probable que los dos grifos del lápiz de Tablet PC se encuentren en coordenadas de pantalla más alejadas que las de los dos clics del mouse. Para dar cabida a esto, Windows XP Tablet PC Edition tiene la configuración de la distancia temporal y espacial entre los dos grifos de un doble punteo que son independientes de la configuración del mouse para un doble clic. Esta configuración se puede ajustar en la configuración de lápiz y tablero del panel de control.

Debido a estas consideraciones, las aplicaciones deben escuchar solo un conjunto de mensajes en lugar de ambos. Si va a compilar una aplicación habilitada para el lápiz, escuche solo los mensajes del sistema y del lápiz. Estos mensajes son predecibles y funcionan bien con el lápiz de Tablet PC. Si va a compilar una aplicación que no está habilitada para el lápiz, escuche solo los mensajes del mouse.

 

 



