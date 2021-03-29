---
title: Acerca de Windows Touch
description: En este tema se ofrece una breve introducción a Windows Touch.
ms.assetid: 19100652-3778-4f25-8d54-70e70363239b
keywords:
- Windows Touch, kit de desarrollo de software
- Windows Touch, SDK
- Windows Touch, acerca de
- Windows Touch, nuevas características
- Windows Touch, novedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81e9a3ebab9a5c85127a1548c07c2ea0fa2cae54
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993948"
---
# <a name="about-windows-touch"></a>Acerca de Windows Touch

En este tema se ofrece una breve introducción a Windows Touch.

Los nuevos elementos de hardware y API del sistema operativo Windows 7 proporcionan a las aplicaciones la capacidad de recibir entradas de varios contactos. Esto proporciona a estas aplicaciones la capacidad de detectar y responder a varios puntos táctiles simultáneos en la superficie visible de la aplicación. La funcionalidad de esta característica en Windows 7 se proporciona mediante un nuevo mensaje que informa y realiza un seguimiento de los toques. El nuevo mensaje, [**\_ tecnología táctil de WM**](wm-touchdown.md), informa de la acción (arriba, abajo, movimiento), posición y un identificador para los puntos táctiles. Windows genera mensajes de Windows Touch y se entregan a Windows que se registran para la entrada táctil de Windows.

Además del nuevo mensaje de entrada táctil, los mensajes de gestos se han agregado a la lista de mensajes de ventana existente. La compatibilidad de mensajería con gestos se habilita con un único mensaje de ventana nuevo ([**\_ gesto de WM**](wm-gesture.md)) que se envía o se envía a las ventanas de aplicación adecuadas cuando la entrada del usuario se reconoce como un gesto. Las funciones de API dedicadas encapsulan los detalles para la creación y el consumo de este mensaje. Esto se hace porque la información asociada al mensaje puede cambiar en el futuro sin interrumpir las aplicaciones que ya consumen este mensaje.

Además de los mensajes de gestos, se han agregado interfaces especializadas a la Windows SDK. Estas interfaces permiten la compatibilidad avanzada con la entrada táctil para que los desarrolladores de aplicaciones puedan crear fácilmente interfaces de usuario naturales. La interfaz [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) interpreta los [**mensajes \_ táctiles de WM**](wm-touchdown.md) para generar eventos que contengan información de traslación, rotación y escalado sobre una colección de puntos de toque. La interfaz [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) se puede usar junto con la interfaz **IManipulationProcessor** para habilitar la animación y asegurarse de que los objetos permanecen en la pantalla del usuario cuando se mueven.

Los elementos de la API de Windows Touch tienen algunas similitudes con el SDK de Microsoft PixelSense (anteriormente conocido como Microsoft Surface SDK), pero las aplicaciones destinadas a Microsoft PixelSense no se ejecutan en equipos con Windows Touch. Además, las aplicaciones que tienen como destino Windows Touch no se ejecutan en Microsoft PixelSense.

Parte de la funcionalidad de Windows Touch está integrada en el núcleo de Windows 7. Esta funcionalidad está disponible para los usuarios sin necesidad de que los desarrolladores habiliten explícitamente la compatibilidad. Sin embargo, para sacar el máximo partido de la interacción táctil de Windows, los desarrolladores deben usar la API Touch de Windows. Para empezar a aprender cómo funciona Windows Touch, consulte la [Guía de programación](programming-guide.md) o comience por [elegir el enfoque adecuado para Windows Touch](choosing-the-right-approach-to-windows-touch.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información general sobre la arquitectura](architectural-overview.md)
</dt> <dt>

[Elección del enfoque adecuado para Windows Touch](choosing-the-right-approach-to-windows-touch.md)
</dt> <dt>

[Windows Touch](windows-touch-portal.md)
</dt> </dl>

 

 




