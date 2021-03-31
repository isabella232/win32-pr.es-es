---
title: Elección del enfoque adecuado para Windows Touch
description: En esta sección se explican los distintos enfoques de Windows Touch que puede usar.
ms.assetid: 983023e4-355b-45ba-8572-d93c460d2ff8
keywords:
- Windows Touch, enfoques diferentes
- Windows Touch, elegir enfoques
- Windows Touch, mejorar aplicaciones
- Windows Touch, compatibilidad con zoom
- Windows Touch, compatibilidad heredada
- Windows Touch, complemento RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86cdd35b73989541fadd5449efbb3f95d76bfa5d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078128"
---
# <a name="choosing-the-right-approach-to-windows-touch"></a>Elección del enfoque adecuado para Windows Touch

En esta sección se explican los distintos enfoques de Windows Touch que puede usar.

Puede mejorar las aplicaciones mediante las características de Windows Touch de muchas maneras. Antes de adoptar un método, debe tener en cuenta lo que desea hacer con la aplicación. Los escenarios siguientes son típicos para Windows Touch:

-   Quiere que la aplicación se comporte de la misma forma que en versiones heredadas de Windows, pero quiere que los mensajes de Windows Touch se comporten de forma coherente.
-   Quiere usar la rotación de objetos personalizados, la traducción, la panorámica o la compatibilidad con el zoom en la aplicación.
-   Quiere que la aplicación tenga una interpretación específica de los gestos táctiles de Windows o para interpretar varios toques en una aplicación que está optimizada específicamente para la entrada táctil de Windows.
-   Tiene una aplicación que usa el objeto [**RealTimeStylus**](/windows/desktop/api/rtscom/nn-rtscom-irealtimestylus) y desea mejorarla con las capacidades táctiles de Windows.

## <a name="you-want-your-application-to-behave-as-it-did-in-legacy-versions-of-windows"></a>Quiere que la aplicación se comporte como ocurría en versiones heredadas de Windows

En Windows 7, las aplicaciones generan de forma predeterminada mensajes que habilitan la funcionalidad de Windows Touch. Por ejemplo, los gestos de movimiento panorámico desencadenan mensajes de desplazamiento de WM \_ \* . Además de la compatibilidad con pan, el \_ controlador de gestos de WM predeterminado en Windows 7 es compatible con los comentarios de los límites, el zoom y pulse y haga clic. Los comentarios de los límites se habilitan también a través de la compatibilidad heredada. Consulte [información general sobre los gestos táctiles de Windows](windows-touch-gestures-overview.md) para obtener más información sobre cómo se asignan los gestos a los mensajes. Los desarrolladores que solo quieren esta funcionalidad básica no necesitan trabajar directamente con la API Touch de Windows.

> [!Note]  
> Los controladores de barra de desplazamiento personalizados deben admitir la solicitud **SM \_ THUMBPOSITION** para los mensajes **\_ VSCROLL de WM** y deben admitir la solicitud **SB \_ LINELEFT** y la solicitud **SB \_ LINERIGHT** para mensajes de **WM \_ HSCROLL** .

 

-   La sección [compatibilidad heredada para la panorámica con barras de desplazamiento](legacy-support-for-panning-with-scrollbars.md) explica cómo asegurarse de que la aplicación se comporta como los usuarios esperan en Windows 7.

## <a name="you-want-custom-object-rotation-translation-panning-or-zoom-support"></a>Quiere una rotación de objetos personalizados, la traducción, la panorámica o la compatibilidad con zoom

Si desea una compatibilidad limitada para la funcionalidad táctil pero el comportamiento predeterminado que ofrece Windows 7 no es adecuado para su aplicación, puede usar gestos para mejorar la aplicación. Mediante el uso de gestos, puede interpretar los comandos de gestos controlando el mensaje de [**\_ gestos de WM**](wm-gesture.md) . Puede encontrar más información sobre los gestos en la sección [gestos táctiles de Windows](guide-multi-touch-gestures.md). Si su aplicación solo necesita soporte para rotaciones de alta granularidad, compatibilidad mejorada con el zoom o movimiento panorámico con un solo dedo, el mejor método para realizar el desarrollo táctil de Windows es el mejor enfoque. Además de interpretar el mensaje de gesto, puede optar por ser compatible con los comentarios de los límites. Para obtener más información sobre los comentarios de los límites, consulte la sección Comentarios de los [límites](boundary-feedback.md) de la referencia de [programación de Windows Touch](windows-touch-programming-reference.md). En Windows 7, el símbolo del sistema e Internet Explorer aprovechan los comentarios y los movimientos de los límites.

-   En la sección [mejorar la experiencia de movimiento panorámico de un solo dedo](improving-the-single-finger-panning-experience.md) se explica cómo personalizar la experiencia de movimiento panorámico mediante el control del mensaje de [**\_ gestos de WM**](wm-gesture.md) .

## <a name="you-want-fine-grained-gesture-interpretation-or-custom-handling-of-multiple-touch-points"></a>Quiere una interpretación de gestos específica o un control personalizado de varios puntos táctiles

Si desea tener un control de gestos aún más específico que el que ofrece el mensaje [**de \_ gestos de WM**](wm-gesture.md) o desea interpretar varios movimientos en varios objetos, debe usar el procesador de manipulación. Esencialmente, el procesador de manipulación es un superconjunto de gestos. El uso del procesador de manipulación requiere la implementación de un receptor de eventos para las manipulaciones en las que se alimentan datos táctiles sin procesar.

Si desea una física de objeto simple además de interpretar los gestos, debe usar un procesador de inercia junto con el procesador de manipulación. El procesador de inercia funciona con el procesador de manipulación tomando los valores de velocidad del procesador de manipulación tras la finalización de la manipulación.

Si desea interpretar varios puntos táctiles en la aplicación, debe crear un controlador de mensajes para el mensaje [**\_ Touch de WM**](wm-touchdown.md) .

-   En la sección [entrada táctil de Windows](guide-multi-touch-input.md) se explica cómo puede interpretar el mensaje de [**\_ pantalla táctil de WM**](wm-touchdown.md) .
-   En la sección [detección y seguimiento de varios puntos táctiles](detecting-and-tracking-multiple-touch-points.md) se muestra cómo crear una aplicación simple que interpreta varias entradas.
-   En la sección [manipulaciones e inercia](manipulation-and-inertia.md) se explica cómo habilitar el enfoque más flexible para Windows Touch.

## <a name="you-want-to-enable-windows-touch-input-to-an-application-that-uses-the-realtimestylus"></a>Quiere habilitar la entrada táctil de Windows en una aplicación que usa RealTimeStylus

Si desea habilitar la entrada para varios contactos en la plataforma de Tablet PC, debe implementar un complemento de RealTimeStylus personalizado que interprete los datos táctiles de Windows. Microsoft presentó las interfaces [**ITablet3**](/windows/desktop/tablet/itablet3) y [**IRealTimeStylus3**](/windows/desktop/api/rtscom/nn-rtscom-irealtimestylus3) para habilitar la entrada de varios contactos en el complemento RealTimeStylus. Estas interfaces simplifican la extensión de los complementos de RealTimeStylus para admitir varios puntos de contacto.

Para comprobar si la compatibilidad con varios contactos está habilitada, llame a [**IsMultiTouch**](/windows/desktop/tablet/itablet3-ismultitouch). Para comprobar el número de contactos admitidos, llame a [**GetMaximumCursors**](/windows/desktop/tablet/itablet3-getmaximumcursors). Para habilitar o deshabilitar la compatibilidad con varios contactos, llame a [**MultiTouchEnabled**](/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus3-get_multitouchenabled).

> [!Note]  
> Si no habilita varios puntos de contacto en RealTimeStylus, recibirá mensajes de gestos como pan y zoom.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación](programming-guide.md)
</dt> </dl>

 

 