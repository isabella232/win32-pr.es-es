---
title: Información general acerca de la arquitectura
description: Esta introducción a la arquitectura proporciona contexto para Windows Touch API para tabletas y tecnologías táctiles y explica cómo encaja en la arquitectura Windows 7.
ms.assetid: b284e96f-0998-408c-ae84-92a3acdc3014
keywords:
- Windows Información general sobre la arquitectura táctil
- Windows Táctil, manipulaciones
- Windows Touch,messages
- Windows Táctil, inercia
- Windows Táctil, gestos
- gestos, acerca de
- manipulaciones, acerca de
- inercia, acerca de
- procesador de manipulación, introducción a la arquitectura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36b5ce003c88a66e96072fa9f96bc6ae73bd91cb39f53e03ab3748dd14a194d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119448671"
---
# <a name="architectural-overview"></a>Información general acerca de la arquitectura

Esta introducción a la arquitectura proporciona contexto para Windows Touch API para tabletas y tecnologías táctiles y explica cómo encaja en la arquitectura Windows 7.

## <a name="messages-for-windows-touch-input-and-gestures"></a>Mensajes para Windows entrada táctil y gestos

Las características de mensajería Windows Touch se habilitan mediante la escucha e interpretación de mensajes durante la ejecución. En la ilustración siguiente se muestra cómo se generan mensajes desde hardware y se envían a las aplicaciones Windows 7.

![ilustración que muestra cómo Windows 7 envía mensajes desde hardware multitáctil a una aplicación](images/wm-multitouch-messaging.png)

En la columna situada más a la izquierda de la ilustración, el hardware táctil recibe la entrada de un usuario. A continuación, un controlador se comunica entre el hardware y el sistema operativo. A continuación, el sistema operativo genera un [**mensaje WM \_ TOUCH**](wm-touchdown.md) o [**WM \_ GESTURE**](wm-gesture.md) que luego se envía al HWND de una aplicación. A continuación, la aplicación actualiza la interfaz de usuario dada la información encapsulada en el mensaje.

Las aplicaciones reciben gestos de forma predeterminada. A menos que una aplicación se registre para Windows los mensajes de entrada táctiles con la función [**RegisterTouchWindow,**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow) Windows crea notificaciones de gestos [**(mensajes DE WM \_ GESTURE)**](wm-gesture.md) y se envían a esa ventana de aplicación. Si una ventana de aplicación se registra para recibir mensajes táctiles, se envían notificaciones Windows entrada táctil [**(mensajes WM \_ TOUCH)**](wm-touchdown.md) a esa ventana de aplicación. Windows Los mensajes táctiles y gestuales son expansiones en el sentido de que, una vez que se realiza una entrada táctil o un gesto comienza en una ventana de la aplicación, todos los mensajes se envían a esa aplicación hasta que se completa el gesto o se completa la entrada táctil principal.

Para la compatibilidad heredada, Windows los mensajes [**\_ DE WM GESTURE**](wm-gesture.md) si se han burbujas y, a continuación, enviarán o postarán los mensajes adecuados que se asignan al gesto. Para evitar que se rompa la compatibilidad heredada, asegúrese de reenviar mensajes \_ DE WM GESTURE mediante [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca). Puede encontrar más información sobre la compatibilidad heredada en la sección Windows información general sobre los [gestos táctiles.](windows-touch-gestures-overview.md)

## <a name="manipulations-and-inertia"></a>Manipulaciones e inercia

Windows Los programadores táctiles deben ser capaces de interpretar los gestos de varios orígenes de una manera significativa para el gesto que tiene lugar. Microsoft proporciona la API de manipulación para realizar estos cálculos. Las manipulaciones son básicamente gestos con valores asociados a ellos que describen todo el gesto. Después de conectar los datos de entrada al procesador de manipulación, puede recuperar la información pertinente a la acción que el usuario realiza en el objeto. En la ilustración siguiente se muestra una manera de usar manipulaciones.

![ilustración que muestra los mensajes táctiles de Windows pasados al procesador de manipulación de un objeto, que controla eventos con la \- interfaz imanipulationevents](images/manipulation-arch.png)

En la parte superior izquierda de la ilustración, el usuario ha tocado la pantalla, lo que crea mensajes táctiles. Estos mensajes contienen una coordenada X y una coordenada Y que se usan para determinar el objeto que está en el foco. El objeto en el foco contiene un procesador de manipulación. A continuación, en el mensaje [**WM \_ TOUCH**](wm-touchdown.md) con la marca **TOUCHEVENTF \_ UP,** se selecciona el objeto en el foco del usuario, se hace referencia al procesador de manipulación y se envía el mensaje al procesador de manipulación. Los **mensajes WM \_ TOUCH** posteriores asociados a este contacto se envían al procesador de manipulación hasta que se recibe el mensaje **WM \_ TOUCH** con la **marca TOUCHEVENTF \_ UP** y se desreferencia el objeto seleccionado. En la sección inferior derecha de la ilustración, se usa un receptor de eventos de manipulación que implementa la interfaz [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) para controlar los eventos de manipulación, que se genera mientras se crean los mensajes táctiles. El receptor de eventos puede realizar actualizaciones en la interfaz en función de los eventos de manipulación mientras se producen.

En Windows touch, es habitual incorporar física simple para que los objetos se detengan sin problemas, en lugar de detenerse repentinamente cuando ya no se tocan. Microsoft proporciona inertia API para realizar los cálculos de esta física simple para que la aplicación pueda comportarse de forma similar a otras aplicaciones. Esto también le ahorra el esfuerzo necesario para crear una funcionalidad física sólida. En la ilustración siguiente se muestra cómo puede usar la inercia.

![ilustración que muestra los mensajes táctiles de Windows pasados a la interfaz de inertiaprocessor de un objeto, que genera eventos con la \- interfaz imanipulationevents](images/inertia-arch.png)

Observe las similitudes entre la inercia y la manipulación. La única diferencia entre los dos es que, en el caso de la inercia, los mensajes interpretados se entregan a un procesador de inercia en lugar de a un procesador de manipulación y el procesador de inercia genera los eventos. En la parte superior izquierda de la ilustración, en el mensaje [**WM \_ TOUCH**](wm-touchdown.md) con la marca **TOUCHEVENTF \_ UP,** los mensajes táctiles se usan para identificar un objeto en el foco que contiene un procesador de inercia y un procesador de manipulación. Los **mensajes WM \_ TOUCH** posteriores se envían al procesador de manipulación y el procesador de manipulación realiza actualizaciones en la interfaz de usuario de la aplicación. Una vez completada la manipulación, los valores de velocidad de la manipulación se usan para configurar un procesador de inercia. Como se muestra en la columna central, se llama al método [**Process**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-process) [**o ProcessTime**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-processtime) en la interfaz [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) mediante un temporizador u otro bucle en un subproceso independiente hasta que las llamadas indican que el procesador ha terminado de procesarse. Mientras se realizan estas llamadas, se genera un evento de manipulación, que se controla mediante un receptor de eventos de manipulación basado en la [**\_ interfaz IManipulationEvents.**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) En la sección inferior derecha de la ilustración, este receptor de eventos realiza actualizaciones en la interfaz de usuario de la aplicación en función de los eventos de manipulación cuando se producen a través de controladores de eventos en el receptor de eventos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación](programming-guide.md)
</dt> </dl>

 

 