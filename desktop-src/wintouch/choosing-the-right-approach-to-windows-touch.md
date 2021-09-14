---
title: Elegir el enfoque correcto para Windows táctil
description: En esta sección se explican los distintos enfoques para Windows Touch que puede usar.
ms.assetid: 983023e4-355b-45ba-8572-d93c460d2ff8
keywords:
- Windows Toque, enfoques diferentes
- Windows Touch,choosing approaches
- Windows Táctil, mejorar las aplicaciones
- Windows Táctil, compatibilidad con zoom
- Windows Touch, compatibilidad heredada
- Windows Complemento Touch,RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86cdd35b73989541fadd5449efbb3f95d76bfa5d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127251583"
---
# <a name="choosing-the-right-approach-to-windows-touch"></a>Elegir el enfoque correcto para Windows táctil

En esta sección se explican los distintos enfoques para Windows Touch que puede usar.

Puede mejorar las aplicaciones mediante Windows touch de muchas maneras. Antes de adoptar un método, debe tener en cuenta lo que quiere hacer con la aplicación. Los siguientes escenarios son típicos de Windows Touch:

-   Quiere que la aplicación se comporte igual que en las versiones heredadas de Windows pero quiere que Windows los mensajes táctiles se comporten de forma coherente.
-   Quiere compatibilidad personalizada con la rotación de objetos, la traducción, el movimiento panorámico o el zoom en la aplicación.
-   Quiere que la aplicación tenga una interpretación específica de los gestos de Windows Touch o que interprete varias funciones táctiles en una aplicación optimizada específicamente para Windows entrada táctil.
-   Tiene una aplicación que usa el [**objeto RealTimeStylus**](/windows/desktop/api/rtscom/nn-rtscom-irealtimestylus) y desea mejorarlo con Windows touch.

## <a name="you-want-your-application-to-behave-as-it-did-in-legacy-versions-of-windows"></a>Quiere que la aplicación se comporte como en las versiones heredadas de Windows

En Windows 7, las aplicaciones generan de forma predeterminada mensajes que habilitan Windows touch. Por ejemplo, los gestos de desplazamiento horizontal desencadenan mensajes \_ \* WM SCROLL. Además de la compatibilidad con desplazamiento panorámico, el controlador WM GESTURE predeterminado de Windows 7 admite comentarios sobre \_ límites, zoom y pulsar y presionar. Los comentarios sobre límites también se habilitan a través de la compatibilidad heredada. Consulte el [Windows información general sobre gestos táctiles](windows-touch-gestures-overview.md) para obtener más información sobre cómo se asignan los gestos a los mensajes. Los desarrolladores que solo desean esta funcionalidad básica no necesitan trabajar directamente con Windows Touch API.

> [!Note]  
> Los controladores de barra de desplazamiento personalizados deben admitir la solicitud **SM \_ THUMBPOSITION** para mensajes **WM \_ VSCROLL** y deben admitir la solicitud **SB \_ LINELEFT** y la solicitud **SB \_ LINERIGHT** para los **mensajes WM \_ HSCROLL.**

 

-   En [la sección Compatibilidad heredada para el](legacy-support-for-panning-with-scrollbars.md) movimiento panorámico con barras de desplazamiento se explica cómo asegurarse de que la aplicación se comporta como esperan los usuarios en Windows 7.

## <a name="you-want-custom-object-rotation-translation-panning-or-zoom-support"></a>Quiere compatibilidad con rotación, traducción, movimiento panorámico o zoom de objetos personalizados

Si desea compatibilidad limitada con la función táctil, pero el comportamiento predeterminado que ofrece Windows 7 no es adecuado para la aplicación, puede usar gestos para mejorar la aplicación. Mediante el uso de gestos, puede interpretar los comandos de gestos controlando el [**mensaje DE GESTO \_ DE WM.**](wm-gesture.md) Puede encontrar más información sobre los gestos en la [sección Windows Touch Gestures (Gestos táctiles).](guide-multi-touch-gestures.md) Si la aplicación solo necesita compatibilidad con rotaciones de granularidad alta, compatibilidad con zoom mejorada o movimiento panorámico con un solo dedo, los gestos son el mejor enfoque para el desarrollo Windows Touch. Además de interpretar el mensaje de gesto, puede optar por admitir los comentarios de límites. Para obtener más información sobre los comentarios sobre límites, vea la sección Comentarios de [límites](boundary-feedback.md) [de la Windows referencia de programación táctil](windows-touch-programming-reference.md). En Windows 7, el símbolo del sistema y Internet Explorer aprovechar los gestos y comentarios de los límites.

-   En [la sección Improving the Single Finger Panning Experience](improving-the-single-finger-panning-experience.md) (Mejora de la experiencia de movimiento panorámico con un solo dedo) se explica cómo personalizar la experiencia de movimiento panorámico mediante el control del mensaje WM [**\_ GESTURE.**](wm-gesture.md)

## <a name="you-want-fine-grained-gesture-interpretation-or-custom-handling-of-multiple-touch-points"></a>Quiere una interpretación de gestos detallada o un control personalizado de varios puntos táctiles.

Si desea tener un control aún más específico de los gestos que ofrece el mensaje [**GESTO \_ DE WM,**](wm-gesture.md) o si desea interpretar varios gestos en varios objetos, debe usar el procesador de manipulación. Básicamente, el procesador de manipulación es un superconjunto de gestos. El uso del procesador de manipulación requiere que implemente un receptor de eventos para las manipulaciones a las que se alimentan los datos táctiles sin procesar.

Si desea una física de objetos simple además de interpretar los gestos, debe usar un procesador de inercia junto con el procesador de manipulación. El procesador de inercia funciona con el procesador de manipulación tomando los valores de velocidad del procesador de manipulación tras la finalización de la manipulación.

Si desea interpretar varios puntos táctiles en la aplicación, debe crear un controlador de mensajes para el [**mensaje WM \_ TOUCH.**](wm-touchdown.md)

-   La [Windows entrada táctil](guide-multi-touch-input.md) explica cómo puede interpretar el mensaje WM [**\_ TOUCH.**](wm-touchdown.md)
-   En [la sección Detección y seguimiento de varios puntos](detecting-and-tracking-multiple-touch-points.md) táctiles se muestra cómo crear una aplicación sencilla que interprete varias entradas.
-   En [la sección Manipulaciones e inercia](manipulation-and-inertia.md) se explica cómo habilitar el enfoque más flexible para Windows Touch.

## <a name="you-want-to-enable-windows-touch-input-to-an-application-that-uses-the-realtimestylus"></a>Quiere habilitar la entrada Windows touch en una aplicación que usa RealTimeStylus.

Si desea habilitar la entrada para varios contactos en la plataforma de Tablet PC, debe implementar un complemento RealTimeStylus personalizado que interprete los datos Windows Touch. Microsoft presentó las interfaces [**ITablet3**](/windows/desktop/tablet/itablet3) e [**IRealTimeStylus3**](/windows/desktop/api/rtscom/nn-rtscom-irealtimestylus3) para habilitar la entrada de varios contactos en el complemento RealTimeStylus. Estas interfaces simplifican la extensión de los complementos RealTimeStylus para admitir varios puntos de contacto.

Para comprobar si está habilitada la compatibilidad con varios contactos, llame a [**IsMultiTouch**](/windows/desktop/tablet/itablet3-ismultitouch). Para comprobar el número de contactos admitidos, llame [**a GetMaximumCursors**](/windows/desktop/tablet/itablet3-getmaximumcursors). Para habilitar o deshabilitar el soporte técnico de varios contactos, [**llame a MultiTouchEnabled.**](/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus3-get_multitouchenabled)

> [!Note]  
> Si no habilita varios puntos de contacto en RealTimeStylus, recibirá mensajes de gestos como desplazamiento panorámico y zoom.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación](programming-guide.md)
</dt> </dl>

 

 