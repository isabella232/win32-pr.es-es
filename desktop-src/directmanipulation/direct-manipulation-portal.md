---
description: Las API de manipulación directa permiten crear excelentes experiencias de desplazamiento panorámico, zoom y arrastre de usuarios. Para ello, procesa la entrada táctil en una región u objeto, genera transformaciones de salida y aplica las transformaciones a los elementos de la interfaz de usuario.
ms.assetid: 26358bc5-71e9-40f0-9243-9bddd961a0e5
title: Manipulación directa
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: f449079a1772fd6dd43b51a2e5af3920ab3e173e1dc8590567ed4555b6deaf31
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120022595"
---
# <a name="direct-manipulation"></a>Manipulación directa

Las API de manipulación directa permiten crear excelentes experiencias de desplazamiento panorámico, zoom y arrastre de usuarios. Para ello, procesa la entrada táctil en una región u objeto, genera transformaciones de salida y aplica las transformaciones a los elementos de la interfaz de usuario. Puede usar la manipulación directa para optimizar la capacidad de respuesta y reducir la latencia mediante el procesamiento de entrada fuera del subproceso, las pruebas de acceso de entrada fuera del subproceso opcionales y la predicción de entrada/salida.

Cualquier aplicación que use la manipulación directa para procesar interacciones táctiles muestra las animaciones de Windows 8 fluidos y los comportamientos de comentarios de interacción que se ajustan a las directrices para interacciones [de usuario comunes](/windows/uwp/design/input/).

## <a name="developer-audience"></a>Audiencia de los desarrolladores

Direct Manipulation API es para desarrolladores experimentados que conocen C/C++, que tienen un conocimiento sólido del modelo de objetos componentes [(COM)](../com/component-object-model--com--portal.md)y están familiarizados con los Windows de programación.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

La manipulación directa se introdujo en Windows 8. Se incluye en las versiones de 32 y 64 bits.

## <a name="why-use-directmanipulation"></a>Por qué usar DirectManipulation

### <a name="handles-interactions-in-a-straightforward-and-consistent-manner"></a>Controla las interacciones de una manera sencilla y coherente.

La manipulación directa funciona declarando previamente los comportamientos y las interacciones de una región u objeto. Por ejemplo, a menudo se configura una página web para desplazarse y hacer zoom. En tiempo de ejecución, la entrada se asocia a esta región o objeto a través de una sencilla llamada API. Desde este punto, la manipulación directa realiza todo el trabajo pesado de procesar la entrada, aplicar restricciones y personalidad, y generar las transformaciones de salida.

### <a name="build-responsive-touch-applications"></a>Creación de aplicaciones táctiles con capacidad de respuesta

Para optimizar la capacidad de respuesta y minimizar la latencia, el procesamiento de manipulación directa se produce en un subproceso independiente del subproceso de interfaz de usuario. Como resultado, las transformaciones de salida se pueden ejecutar en paralelo a la actividad en el subproceso de la interfaz de usuario. La actividad del subproceso de interfaz de usuario puede incluir lógica de aplicación, representación, diseño y cualquier otra cosa que consuma ciclos en el procesador.

### <a name="implementation-flexibility"></a>Flexibilidad de implementación

Las interfaces incluidas con manipulación directa proporcionan compatibilidad completa con el control de entradas, el reconocimiento de la interacción, las notificaciones de comentarios y las actualizaciones de la interfaz de usuario. Las interfaces también incorporan servicios del sistema como [DirectComposition.](../directcomp/directcomposition-portal.md)

## <a name="basic-concepts"></a>Conceptos básicos

La implementación de manipulación directa más básica consta de una *ventanilla*, *contenido* e *interacciones*. La *ventanilla* es una región que puede recibir y procesar la entrada de las interacciones del usuario. También es la región del contenido que es visible para el usuario final. El *contenido* es el objeto real que los usuarios finales pueden ver y es lo que se mueve o escala en respuesta a una interacción del usuario. Las interacciones del *usuario principal (también conocidas* como *manipulaciones)* compatibles con la manipulación directa son el movimiento panorámico y el zoom. Estas interacciones aplican una transformación de traducción o escala al contenido dentro de la ventanilla, respectivamente. Se pueden configurar varias ventanillas (cada una con su propio contenido) en una sola ventana para crear una experiencia de interfaz de usuario completa.

En esta ilustración se muestra una implementación básica de manipulación directa antes y después del movimiento panorámico.

![implementación básica de manipulación directa antes y después del movimiento panorámico.](images/dm-art-1.png)

Durante la inicialización de manipulación directa, se crea una instancia de un objeto **DCompDirectManipulationCompositor** y se asocia a la manipulación directa. Este objeto es un contenedor alrededor de [DirectComposition](../directcomp/directcomposition-portal.md), que es el compositor del sistema. El objeto es responsable de aplicar las transformaciones de salida y de impulsar las actualizaciones visuales.

Un contacto representa un punto táctil identificado por el **pointerId** proporcionado en el [mensaje WM/_POINTERDOWN.](../inputmsg/wm-pointerdown.md) Cuando se **recibe \_ un mensaje POINTERDOWN de WM,** la aplicación llama a [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact). La aplicación notifica a manipulación directa los contactos que se deben controlar y las ventanillas que deben reaccionar a esos contactos. La entrada de teclado y mouse tiene valores **de pointerId** especiales, por lo que la manipulación directa puede controlarlos correctamente.

En nuestro caso básico anterior, cuando se llama a [**SetContact,**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) suceden algunas cosas:

- Cuando el usuario realiza una panorámica, se envía un mensaje [wm/_POINTERCAPTURECHANGED](../inputmsg/wm-pointercapturechanged.md) a la aplicación para notificar que el contacto se ha consumido mediante manipulación directa.
- Cuando el usuario mueve los movimientos, la ventanilla activa eventos de actualización que usa el contenedor [DirectComposition](../directcomp/directcomposition-portal.md) para dirigir las actualizaciones visuales a la pantalla. Para un usuario que se desplaza en un desplazamiento panorámico en una ventanilla, el contenido parecerá moverse sin problemas bajo el contacto.
- Cuando el usuario eleva el contacto, el usuario ve que el contenido continúa moverse a medida que pasa a una animación de inercia, disminuyendo gradualmente hasta llegar a su lugar de reposo final.

## <a name="processing-keyboard-and-mouse-input"></a>Procesamiento de la entrada de teclado y mouse

La manipulación directa permite que los mensajes del teclado y del mouse se reenván manualmente desde el subproceso de interfaz de usuario de la aplicación a través de la API [**ProcessInput**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager-processinput) para que se puedan controlar correctamente mediante manipulación directa.

## <a name="directmanipulation-and-the-hwnd"></a>DirectManipulation y HWND

La manipulación directa está asociada a un HWND de Win32 para recibir y procesar mensajes de entrada de puntero para esa ventana. A medida que Manipulación directa calcula los valores de salida, realiza devoluciones de llamada asincrónicas a los objetos del Modelo de objetos componentes de manipulación directa [(COM)](../com/component-object-model--com--portal.md) que se implementan en la aplicación. Estas devoluciones de llamada informan a la aplicación sobre la transformación que se aplicó a los objetos . La manipulación directa se activa en el HWND especificado mediante una llamada a [**Activate**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager-activate).

## <a name="supporting-documentation"></a>Documentación de soporte técnico

- [Ventanillas y contenido](directmanipulation-viewports-and-content.md)
- [Uso de varias ventanillas en DirectManipulation](directmanipulation-multiple-vieports.md)
- [Procesamiento de entradas con DirectManipulation](directmanipulation-processing-input-with-directmanipulation.md)
- [Motor de composición](directmanipulation-composition-engine.md)
- [Referencia de manipulación directa](direct-manipulation-reference.md)

- [BUILD 2013: WCL-022: Make your desktop app great with touch, mouse, and pen](https://channel9.msdn.com/Events/Build/2013/4-022)
- [Procesar la entrada táctil con el ejemplo de manipulación directa](https://github.com/microsoft/Windows-classic-samples/tree/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/TouchInputDirectManipulation)
