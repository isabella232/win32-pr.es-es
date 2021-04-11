---
description: Las API de manipulación directa permiten crear excelentes experiencias de usuario pan, zoom y arrastre. Para ello, procesa la entrada táctil en una región u objeto, genera transformaciones de salida y aplica las transformaciones a los elementos de la interfaz de usuario.
ms.assetid: 26358bc5-71e9-40f0-9243-9bddd961a0e5
title: Manipulación directa
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 6db2a50893914dfb25050768f88cb289a1ecf3ea
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152268"
---
# <a name="direct-manipulation"></a>Manipulación directa

Las API de manipulación directa permiten crear excelentes experiencias de usuario pan, zoom y arrastre. Para ello, procesa la entrada táctil en una región u objeto, genera transformaciones de salida y aplica las transformaciones a los elementos de la interfaz de usuario. Puede usar la manipulación directa para optimizar la capacidad de respuesta y reducir la latencia a través del procesamiento de entrada fuera de subproceso, la prueba de posicionamiento de entrada sin subproceso opcional y la predicción de entrada y salida.

Cualquier aplicación que use la manipulación directa para procesar interacciones táctiles muestra las animaciones de Windows 8 fluidas y los comportamientos de comentarios de interacción que se ajustan a las [directrices para interacciones de usuario comunes](/windows/uwp/design/input/).

## <a name="developer-audience"></a>Audiencia de los desarrolladores

La API de manipulación directa está dirigida a desarrolladores experimentados que saben C/C++, tienen una comprensión sólida del [modelo de objetos componentes (com)](../com/component-object-model--com--portal.md)y están familiarizados con los conceptos de programación de Windows.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

La manipulación directa se presentó en Windows 8. Se incluye en las versiones de 32 y 64 bits.

## <a name="why-use-directmanipulation"></a>Por qué usar DirectManipulation

### <a name="handles-interactions-in-a-straightforward-and-consistent-manner"></a>Controla las interacciones de una manera sencilla y coherente

La manipulación directa funciona declarando previamente los comportamientos e interacciones de una región u objeto. Por ejemplo, una página web se configura a menudo para la panorámica y el zoom. En tiempo de ejecución, la entrada se asocia a esta región u objeto a través de una llamada de API simple. A partir de este punto, la manipulación directa directa realiza todo el trabajo pesado de procesar la entrada, aplicar restricciones y personalidad, y generar las transformaciones de salida.

### <a name="build-responsive-touch-applications"></a>Creación de aplicaciones táctiles con capacidad de respuesta

Para optimizar la capacidad de respuesta y minimizar la latencia, el procesamiento de la manipulación directa se produce en un subproceso independiente e independiente del subproceso de la interfaz de usuario. Como resultado, las transformaciones de salida pueden ejecutarse en paralelo a la actividad en el subproceso de la interfaz de usuario. La actividad del subproceso de la interfaz de usuario puede incluir lógica de aplicación, representación, diseño y cualquier otro elemento que consuma ciclos en el procesador.

### <a name="implementation-flexibility"></a>Flexibilidad de implementación

Las interfaces que se incluyen con la manipulación directa proporcionan compatibilidad completa para el control de entradas, el reconocimiento de interacción, las notificaciones de comentarios y las actualizaciones de la interfaz de usuario. Las interfaces también incorporan servicios del sistema como [DirectComposition](../directcomp/directcomposition-portal.md).

## <a name="basic-concepts"></a>Conceptos básicos

La implementación de la manipulación directa más básica consta de una *ventanilla*, *contenido* e *interacciones*. La *ventanilla* es una región que puede recibir y procesar la entrada de interacciones del usuario. También es la región del contenido que es visible para el usuario final. El *contenido* es el objeto real que los usuarios finales pueden ver y es lo que mueve o escala en respuesta a una interacción del usuario. Las *interacciones* del usuario principal (también conocidas como *manipulaciones*) que admite la manipulación directa son la panorámica y el zoom. Estas interacciones aplican una transformación trasladar o escalar al contenido dentro de la ventanilla, respectivamente. Se pueden configurar varias ventanillas (cada una con su propio contenido) en una sola ventana para crear una experiencia de interfaz de usuario enriquecida.

En esta ilustración se muestra una implementación de manipulación directa básica antes y después de la panorámica.

![implementación de la manipulación directa básica antes y después de la panorámica.](images/dm-art-1.png)

Durante la inicialización de la manipulación directa se crea una instancia de un objeto **DCompDirectManipulationCompositor** y se asocia a la manipulación directa. Este objeto es un contenedor alrededor de [DirectComposition](../directcomp/directcomposition-portal.md), que es el compositor del sistema. El objeto es responsable de aplicar las transformaciones de salida y de impulsar las actualizaciones visuales.

Un contacto representa un punto táctil identificado por el **pointerId** proporcionado en el mensaje de [WM/_POINTERDOWN](../inputmsg/wm-pointerdown.md) . Cuando se recibe un mensaje de **\_ POINTERDOWN de WM** , la aplicación llama a [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact). La aplicación notifica a Manipulationabout directos los contactos que deben controlarse y las ventanillas que deben reaccionar a esos contactos. La entrada del teclado y del mouse tiene valores de **pointerId** especiales para que se puedan controlar adecuadamente mediante la manipulación directa.

En nuestro caso básico anterior, cuando se llama a [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) se producen algunas cosas:

- Cuando el usuario realiza una panorámica, se envía un mensaje de [WM/_POINTERCAPTURECHANGED](../inputmsg/wm-pointercapturechanged.md) a la aplicación para notificar que el contacto lo ha consumido la manipulación directa.
- Cuando el usuario mueve los movimientos, la ventanilla desencadena eventos de actualización que usa el contenedor [DirectComposition](../directcomp/directcomposition-portal.md) para controlar las actualizaciones visuales en la pantalla. En el movimiento panorámico de un usuario en una ventanilla, parecerá que el contenido se mueve sin problemas en el contacto.
- Cuando el usuario levanta el contacto, el usuario ve que el contenido se sigue moviendo a medida que pasa a una animación de inercia, con lo que se reduce gradualmente hasta que alcanza su lugar final.

## <a name="processing-keyboard-and-mouse-input"></a>Procesar la entrada del teclado y del mouse

La manipulación directa permite que los mensajes del mouse y del teclado se reenvíen manualmente desde el subproceso de la interfaz de usuario de la aplicación a través de la API de [**ProcessInput**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager-processinput) para que se puedan controlar adecuadamente mediante la manipulación directa.

## <a name="directmanipulation-and-the-hwnd"></a>DirectManipulation y HWND

La manipulación directa está asociada a un HWND de Win32 para recibir y procesar los mensajes de entrada de puntero para esa ventana. A medida que la manipulación directa calcula valores de salida, realiza devoluciones de llamada asincrónicas a los objetos del [modelo de objetos componentes (com)](../com/component-object-model--com--portal.md) de manipulación directa que se implementan en la aplicación. Estas devoluciones de llamada informan a la aplicación sobre la transformación que se aplicó a los objetos. La manipulación directa se activa en el HWND especificado llamando a [**Activate**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager-activate).

## <a name="supporting-documentation"></a>Documentación complementaria

- [Ventanillas y contenido](directmanipulation-viewports-and-content.md)
- [Usar varias ventanillas en DirectManipulation](directmanipulation-multiple-vieports.md)
- [Procesar la entrada con DirectManipulation](directmanipulation-processing-input-with-directmanipulation.md)
- [Motor de composición](directmanipulation-composition-engine.md)
- [Referencia de manipulación directa](direct-manipulation-reference.md)

- [COMPILACIÓN 2013: WCL-022: haga que su aplicación de escritorio sea fantástica con Touch, mouse y lápiz](https://channel9.msdn.com/Events/Build/2013/4-022)
- [Procesar entrada táctil con el ejemplo de manipulación directa](https://github.com/microsoft/Windows-classic-samples/tree/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/TouchInputDirectManipulation)
