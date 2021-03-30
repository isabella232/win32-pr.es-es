---
title: Experiencia de usuario intuitiva
description: Por primera vez, Windows 7 permite a los desarrolladores y a sus usuarios finales controlar sus equipos tocando la pantalla.
ms.assetid: cf5be4d6-4284-43e3-86ba-293c4513b477
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76576883186a77c53256dad7f011b75a7e260ae2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793258"
---
# <a name="intuitive-user-experience"></a>Experiencia de usuario intuitiva

Por primera vez, Windows 7 permite a los desarrolladores y a sus usuarios finales controlar sus equipos tocando la pantalla. Las características táctiles y multitáctiles proporcionan una forma natural e intuitiva de que los usuarios puedan interactuar con los equipos. La plataforma para desarrolladores incluye API de gestos de alto nivel, así como mensajes táctiles de bajo nivel y API de entrada táctil. Los elementos de la interfaz de usuario de nivel superior, como el menú *Inicio* y la *barra de tareas*, tienen destinos más grandes que las versiones anteriores de Windows, lo que facilita su selección con un dedo en lugar de un mouse. Se proporcionan comentarios visuales para TAP y Double TAP. El explorador de Windows y Windows Internet Explorer 8 son táctiles y fáciles de integrar con las aplicaciones de Windows 7.

## <a name="multi-touch-gestures-and-manipulation-and-inertia-apis"></a>Movimientos multitáctiles y API de manipulación e inercia

Características de Windows 7: compatibilidad mejorada con funciones táctiles y gestos, lo que permite a los desarrolladores crear de forma rápida y sencilla experiencias de aplicación únicas que van más allá de apuntar al mouse sencillo, hacer clic y arrastrar. Las nuevas API multitáctiles admiten gestos enriquecidos, como pan, zoom y rotate. Todos los gestos proporcionan comentarios visuales directos e interactúan con el contenido subyacente de forma natural e intuitiva. Por ejemplo, un gesto de zoom centra la vista en la ubicación del gesto. Las API de entrada táctil de nivel inferior también están disponibles para la definición de gestos personalizados y las experiencias avanzadas de respuesta táctil. Windows 7 proporciona una plataforma de desarrollo que proporciona a los desarrolladores las herramientas necesarias para desarrollar aplicaciones creativas para dispositivos de entrada multitáctil, procesando los datos proporcionados por el usuario desde dispositivos multitáctiles y mejorando la interfaz de usuario. El resultado son entornos más intuitivos, que habilitan las innovaciones en la interacción con el equipo.

Windows 7 también proporciona compatibilidad con la plataforma para la manipulación de objetos y el procesamiento de inercia. Un amplio conjunto de funciones de manipulación le permite ampliar, cambiar de tamaño o girar varios objetos simultáneamente y en una granularidad muy precisa. Por ejemplo, se pueden recortar varias fotografías digitales, cambiar su tamaño y girarlas en una sola sesión mediante gestos táctiles.

Windows 7 incluye API de inercia que simulan la inercia cuando se mueven los objetos, trabajando en mano con las API de manipulación. Por ejemplo, en una aplicación fotográfica, puede usar las API de manipulación para permitir que los usuarios giren, cambien de tamaño y muevan fotografías. Del mismo modo, si un usuario "echa" una foto, las API de inercia proporcionan una interacción natural y permiten que la foto se pare en una parada o un rebote de los bordes de la ventana de la aplicación. (Consulte la [Guía de programación táctil de Windows](../wintouch/programming-guide.md) y [Windows Touch: recursos para desarrolladores](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch)).

## <a name="single-finger-panning"></a>Movimiento panorámico Single-Finger

En muchas aplicaciones comunes, las características táctiles son más útiles para la navegación que para la selección de texto. Con las API de toque ampliada, la aplicación de un desarrollador puede elegir habilitar el movimiento panorámico en lugar de arrastrarlo. Por ejemplo, si ha creado una aplicación que usa movimientos multitáctiles para usuarios que reproducen música, podría permitir que estos usuarios simplemente deslicen un dedo hacia arriba o hacia abajo para ajustar el volumen, cambiar canciones o descargar un archivo. No se requiere desplazamiento.

Windows 7 proporciona oportunidades infinitas para los desarrolladores interesados en la creación de aplicaciones para equipos de próxima generación. Lo mejor de todo es que realiza el trabajo difícil de comprobar las barras de desplazamiento e implementar la semántica de movimiento panorámico. Las aplicaciones también reciben un conjunto más completo de eventos y comentarios para el control personalizado de gestos que en versiones anteriores de Windows. (Consulte [mejora de la experiencia de movimiento panorámico Single-Finger](../wintouch/improving-the-single-finger-panning-experience.md)).

## <a name="raw-touch-input-data"></a>Datos de entrada táctil sin procesar

En Windows 7, las nuevas experiencias táctiles están habilitadas por los modelos de interacción que acceden a los mensajes de entrada táctil de nivel inferior y proporcionan respuestas personalizadas a las combinaciones de mensajes táctiles. La plataforma admite la recepción de datos de entrada táctil sin procesar para escenarios como aplicaciones de dibujo multitáctil y gestos personalizados dentro de una aplicación. Puede usar la compatibilidad con la plataforma para tocar o crear sus propias experiencias originales y multitáctiles. (Consulte [ \_ mensaje Touch de WM](../wintouch/wm-touchdown.md)).

 

 