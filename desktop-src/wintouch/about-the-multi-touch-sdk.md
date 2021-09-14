---
title: Acerca de Windows Touch
description: En este tema se proporciona una breve introducción a Windows Touch.
ms.assetid: 19100652-3778-4f25-8d54-70e70363239b
keywords:
- Windows Touch,software development kit
- Windows Touch,SDK
- Windows Touch,about
- Windows Características táctiles y nuevas
- Windows Touch, novedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81e9a3ebab9a5c85127a1548c07c2ea0fa2cae54
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127251606"
---
# <a name="about-windows-touch"></a>Acerca de Windows Touch

En este tema se proporciona una breve introducción a Windows Touch.

Los nuevos elementos de hardware y API del sistema operativo Windows 7 proporcionan a las aplicaciones la capacidad de recibir entradas de varios contactos. Esto ofrece a estas aplicaciones la capacidad de detectar y responder a varios puntos táctiles simultáneos en la superficie visible de la aplicación. La funcionalidad de esta característica Windows 7 se proporciona mediante un nuevo mensaje que informa y realiza un seguimiento de las funciones táctiles. El nuevo mensaje, [**WM \_ TOUCH,**](wm-touchdown.md)informa de la acción (arriba, abajo, mover), posición y un identificador de puntos táctiles. Windows Los mensajes táctiles se generan Windows y se entregan a las ventanas que se registran para Windows entrada táctil.

Además del nuevo mensaje de entrada táctil, se han agregado mensajes de gesto a la lista existente de mensajes de ventana. La compatibilidad de mensajería con gestos se habilita mediante un único mensaje de ventana nuevo [**(WM \_ GESTURE)**](wm-gesture.md)que se envía o se publica en las ventanas de aplicación adecuadas cuando la entrada del usuario se reconoce como un gesto. Las funciones de API dedicadas encapsulan los detalles para la creación y el consumo de este mensaje. Esto se hace porque la información asociada al mensaje puede cambiar en el futuro sin dividir las aplicaciones que ya consumen este mensaje.

Además de los mensajes de gesto, se han agregado interfaces especializadas al SDK de Windows. Estas interfaces permiten la compatibilidad avanzada con la entrada táctil para que los desarrolladores de aplicaciones puedan crear fácilmente interfaces de usuario naturales. La [**interfaz IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) interpreta los mensajes [**WM \_ TOUCH**](wm-touchdown.md) para generar eventos que contienen información de traducción, rotación y escala sobre una colección de puntos táctiles. La [**interfaz IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) se puede usar junto con la interfaz **IManipulationProcessor** para habilitar la animación y asegurarse de que los objetos permanecen en la pantalla del usuario cuando se mueven.

Los elementos de API para Windows Touch tienen algunas similitudes con el SDK de Microsoft PixelSense (anteriormente conocido como Microsoft Surface SDK), pero las aplicaciones destinadas a Microsoft PixelSense no se ejecutan en equipos Windows Touch. Además, las aplicaciones que tienen Windows Touch no se ejecutan en Microsoft PixelSense.

Parte de la funcionalidad de Windows Touch está integrada en el núcleo de Windows 7. Esta funcionalidad está disponible para los usuarios sin necesidad de que los desarrolladores habiliten explícitamente la compatibilidad. Sin embargo, para aprovechar al máximo Windows Touch, los desarrolladores deben usar Windows Touch API. Para empezar a aprender cómo funciona Windows Touch, consulte la Guía de programación o comience por Elegir el enfoque correcto [para Windows Touch](choosing-the-right-approach-to-windows-touch.md). [](programming-guide.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información general sobre la arquitectura](architectural-overview.md)
</dt> <dt>

[Elegir el enfoque correcto para Windows táctil](choosing-the-right-approach-to-windows-touch.md)
</dt> <dt>

[Windows Tocar](windows-touch-portal.md)
</dt> </dl>

 

 




