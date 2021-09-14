---
title: Experiencia de usuario intuitiva
description: Por primera vez, Windows 7 permite a los desarrolladores y a sus usuarios finales controlar sus equipos tocándose la pantalla.
ms.assetid: cf5be4d6-4284-43e3-86ba-293c4513b477
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76576883186a77c53256dad7f011b75a7e260ae2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127251756"
---
# <a name="intuitive-user-experience"></a>Experiencia de usuario intuitiva

Por primera vez, Windows 7 permite a los desarrolladores y a sus usuarios finales controlar sus equipos tocándose la pantalla. Las características táctiles y multi táctiles proporcionan una manera natural e intuitiva para que los usuarios interactúen con los equipos. La plataforma para desarrolladores incluye API de gestos de alto nivel, así como mensajes táctiles de bajo nivel y API de entrada táctil. Los elementos de la interfaz  de usuario de nivel superior, como el menú Inicio y la barra de tareas *,* tienen destinos más grandes que las versiones anteriores de Windows, lo que facilita su selección con un dedo en lugar de un mouse. Se proporcionan comentarios visuales para pulsar y pulsar dos veces. Windows Explorer y Windows Internet Explorer 8 son táctiles y se integran fácilmente con Windows 7 aplicaciones.

## <a name="multi-touch-gestures-and-manipulation-and-inertia-apis"></a>Gestos multi táctiles y API de manipulación e inercia

Windows 7 características se ha mejorado la compatibilidad táctil y de gestos, lo que permite a los desarrolladores crear rápida y fácilmente experiencias de aplicación únicas que van más allá de apuntar, hacer clic y arrastrar con el mouse. Las nuevas API multi táctiles admiten gestos enriquecidos, como desplazamiento panorámico, zoom y rotación. Todos los gestos proporcionan comentarios visuales directos e interactúan con el contenido subyacente de una manera natural e intuitiva. Por ejemplo, un gesto de zoom centra la vista en la ubicación del gesto. Las API de entrada táctil de nivel inferior también están disponibles para la definición de gestos personalizados y las experiencias avanzadas de respuesta táctil. Windows 7 proporciona una plataforma de desarrollo que proporciona a los desarrolladores las herramientas que necesitan para desarrollar aplicaciones creadoras para dispositivos de entrada multi táctil, mediante el procesamiento de la entrada del usuario desde dispositivos multi táctil y la mejora de la interfaz de usuario. El resultado son entornos más intuitivos, que permiten innovaciones en la interacción del equipo.

Windows 7 también proporciona compatibilidad con la plataforma para la manipulación de objetos y el procesamiento de inercia. Un amplio conjunto de funciones de manipulación le permiten ajustar, cambiar el tamaño o girar varios objetos simultáneamente y con una granularidad muy fina. Por ejemplo, varias fotografías digitales se pueden recortar, cambiar de tamaño y girar en una sola sesión mediante gestos táctiles.

Windows 7 incluye API de inercia que simulan la inercia cuando se mueven objetos, trabajando de la mano con las API de manipulación. Por ejemplo, en una aplicación de fotos, puede usar las API de manipulación para permitir a los usuarios rotar, cambiar el tamaño y mover las fotos. Del mismo modo, si un usuario "lanza" una foto, las API de inercia proporcionan una interacción natural y permiten que la foto se detenga o se desenlame de los bordes de la ventana de la aplicación. (Vea [Windows guía de programación táctil](../wintouch/programming-guide.md) y Windows [Touch: Recursos para desarrolladores).](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch)

## <a name="single-finger-panning"></a>Single-Finger panning

En muchas aplicaciones comunes, las características táctiles son más útiles para la navegación que para la selección de texto. Con las API táctiles extendidas, la aplicación de un desarrollador puede optar por habilitar el movimiento panorámico en lugar de arrastrar. Por ejemplo, si creó una aplicación que usa gestos multi táctiles para los usuarios que reproducen música, podría permitir que estos usuarios simplemente deslicen un dedo hacia arriba o hacia abajo para ajustar el volumen, cambiar las canciones o descargar un archivo. No se requiere desplazamiento.

Windows 7 proporciona oportunidades infinitas a los desarrolladores que están interesados en crear aplicaciones para equipos de próxima generación. Lo mejor de todo es que realiza el trabajo duro de comprobar las barras de desplazamiento e implementar la semántica de desplazamiento panorámico. Las aplicaciones también reciben un conjunto más completo de eventos y comentarios para el control personalizado de los gestos que en versiones anteriores de Windows. (Consulte [Improving the Single-Finger Panning Experience](../wintouch/improving-the-single-finger-panning-experience.md)[Mejora de la experiencia de Single-Finger desplazamiento panorámico]).

## <a name="raw-touch-input-data"></a>Datos de entrada táctil sin procesar

En Windows 7, las nuevas experiencias táctiles se habilitan mediante modelos de interacción que acceden a mensajes de entrada táctil de nivel inferior y proporcionan respuestas personalizadas a combinaciones de mensajes táctiles. La plataforma admite la recepción de datos de entrada táctil sin procesar para escenarios como aplicaciones de dibujo multi touch y gestos personalizados dentro de una aplicación. Puede usar la compatibilidad de la plataforma con la función táctil o crear sus propias experiencias originales y multi táctiles. (Vea [WM \_ TOUCH Message](../wintouch/wm-touchdown.md)).)

 

 