---
title: Información general acerca de la arquitectura
description: Esta información general sobre la arquitectura proporciona contexto para la API Touch de Windows para tabletas y tecnologías táctiles y explica cómo encaja en la arquitectura de Windows 7 más grande.
ms.assetid: b284e96f-0998-408c-ae84-92a3acdc3014
keywords:
- Windows Touch, información general sobre la arquitectura
- Windows Touch, manipulaciones
- Windows Touch, mensajes
- Windows Touch, inercia
- Windows Touch, gestos
- gestos, acerca de
- manipulaciones, acerca de
- inercia, acerca de
- procesador de manipulación, información general sobre la arquitectura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b807113211d77f0aad0ed01fc24570d033063474
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995271"
---
# <a name="architectural-overview"></a>Información general acerca de la arquitectura

Esta información general sobre la arquitectura proporciona contexto para la API Touch de Windows para tabletas y tecnologías táctiles y explica cómo encaja en la arquitectura de Windows 7 más grande.

## <a name="messages-for-windows-touch-input-and-gestures"></a>Mensajes para la entrada y los gestos de Windows Touch

Las características de mensajería para Windows Touch están habilitadas escuchando e interpretando mensajes durante la ejecución. En la siguiente ilustración se muestra cómo se generan los mensajes desde hardware y se envían a las aplicaciones de Windows 7.

![Ilustración en la que se muestra cómo Windows 7 envía mensajes de hardware de multitoque a una aplicación](images/wm-multitouch-messaging.png)

En la columna situada más a la izquierda de la ilustración, el hardware sensible al tacto recibe la entrada de un usuario. Después, un controlador se comunica entre el hardware y el sistema operativo. Después, el sistema operativo genera un mensaje de [**\_ movimiento**](wm-gesture.md) de WM [**\_ Touch**](wm-touchdown.md) o WM que se envía al HWND de una aplicación. A continuación, la aplicación actualiza la interfaz de usuario en función de la información encapsulada en el mensaje.

De forma predeterminada, las aplicaciones reciben gestos. A menos que una aplicación se registre para los mensajes de entrada táctiles de Windows con la función [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow) , Windows crea las notificaciones para los gestos (mensajes de [**\_ gestos de WM**](wm-gesture.md) ) y se envían a esa ventana de la aplicación. Si una ventana de la aplicación se registra para recibir mensajes táctiles, las notificaciones de entrada táctil de Windows (mensajes [**\_ Touch de WM**](wm-touchdown.md) ) se envían a esa ventana de la aplicación. Los mensajes táctiles y gestos de Windows son expansivos en el sentido de que, una vez que se realiza una entrada táctil o se inicia un gesto en una ventana de la aplicación, todos los mensajes se envían a esa aplicación hasta que se completa el movimiento o hasta que se completa el toque principal.

En el caso de la compatibilidad heredada, Windows interpreta los mensajes de [**\_ gestos de WM**](wm-gesture.md) si se propagan y, a continuación, envía o publica los mensajes correspondientes que se asignan al gesto. Para evitar la interrupción del soporte heredado, asegúrese de reenviar \_ mensajes de gestos de WM mediante [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca). Puede encontrar más información sobre la compatibilidad heredada en la sección [información general sobre gestos táctiles de Windows](windows-touch-gestures-overview.md).

## <a name="manipulations-and-inertia"></a>Manipulaciones e inercia

Los programadores de Windows Touch deben ser capaces de interpretar los gestos de varios orígenes de una manera que sea significativa para el gesto. Microsoft proporciona la API de manipulación para realizar estos cálculos. Las manipulaciones son esencialmente gestos con valores asociados que describen el gesto completo. Después de conectar los datos de entrada al procesador de manipulación, puede recuperar la información pertinente para la acción que realiza el usuario en el objeto. En la ilustración siguiente se muestra una manera de usar manipulaciones.

![Ilustración en la que se muestran los mensajes de Windows Touch pasados al procesador de manipulación de un objeto, que controla los eventos con la \- interfaz imanipulationevents](images/manipulation-arch.png)

En la parte superior izquierda de la ilustración, el usuario ha tocado la pantalla, que crea mensajes táctiles. Estos mensajes contienen una coordenada x y una coordenada y que se usan para determinar el objeto que tiene el foco. El objeto en el foco contiene un procesador de manipulación. Después, en el mensaje de [**\_ pantalla táctil de WM**](wm-touchdown.md) con la marca **TOUCHEVENTF \_ up** , se selecciona el objeto en el foco del usuario, se hace referencia al procesador de manipulación y el mensaje se envía al procesador de manipulación. Los **mensajes \_ táctiles de WM** posteriores asociados a este contacto se envían al procesador de manipulación hasta que se recibe el mensaje de **\_ pantalla táctil de WM** con la marca **TOUCHEVENTF \_ up** y se desreferencia el objeto seleccionado. En la sección inferior derecha de la ilustración, se usa un receptor de eventos de manipulación que implementa la interfaz [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) para controlar los eventos de manipulación, que se generan mientras se crean los mensajes táctiles. El receptor de eventos puede realizar actualizaciones en la interfaz en función de los eventos de manipulación mientras se producen.

En las aplicaciones táctiles de Windows, es habitual incorporar física simple para que los objetos lleguen a una detención sin problemas, en lugar de detenerse repentinamente cuando ya no se tocan. Microsoft proporciona la API de inercia para realizar los cálculos para esta física simple, de forma que la aplicación pueda comportarse de forma similar a otras aplicaciones. Esto también le ahorra el esfuerzo necesario para crear una funcionalidad física sólida. En la ilustración siguiente se muestra cómo puede usar la inercia.

![Ilustración en la que se muestran los mensajes táctiles de Windows que se pasan a la interfaz iinertiaprocessor de un objeto, que genera eventos con la \- interfaz imanipulationevents](images/inertia-arch.png)

Tenga en cuenta las similitudes entre la inercia y la manipulación. La única diferencia entre los dos es que, en el caso de la inercia, los mensajes interpretados se entregan a un procesador de inercia en lugar de a un procesador de manipulación y el procesador de inercia genera los eventos. En la parte superior izquierda de la ilustración, en el mensaje de [**\_ toque de WM**](wm-touchdown.md) con la marca **TOUCHEVENTF \_ up** , los mensajes táctiles se usan para identificar un objeto en el foco que contiene un procesador de inercia y un procesador de manipulación. Los **mensajes \_ táctiles de WM** posteriores se envían al procesador de manipulación y el procesador de manipulación realiza actualizaciones en la interfaz de usuario de la aplicación. Una vez completada la manipulación, se usan los valores de velocidad de la manipulación para configurar un procesador de inercia. Como se muestra en la columna central, se llama al método [**Process**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-process) o [**ProcessTime**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-processtime) en la interfaz [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) mediante un temporizador u otro bucle en un subproceso independiente hasta que las llamadas indican que el procesador ha finalizado el procesamiento. Mientras se realizan estas llamadas, se generan eventos de manipulación, que se controlan mediante un receptor de eventos de manipulación basado en la interfaz [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) . En la sección inferior derecha de la ilustración, este receptor de eventos realiza actualizaciones en la interfaz de usuario de la aplicación en función de los eventos de manipulación cuando se producen a través de controladores de eventos en el receptor de eventos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación](programming-guide.md)
</dt> </dl>

 

 