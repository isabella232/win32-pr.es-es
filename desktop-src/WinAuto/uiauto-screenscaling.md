---
title: Descripción de los problemas de escalado de pantalla
description: Windows Vista y las versiones posteriores del sistema operativo permiten a los usuarios cambiar la configuración de puntos por pulgada (PPP) para que la mayoría de los elementos de la interfaz de usuario de la pantalla parezcan más grandes.
ms.assetid: 27dc49e7-2466-4ea3-a6d9-5ea86d6b4c60
keywords:
- clientes, escalado de pantalla de UI Automation
- clientes, ajuste de escala de pantalla
- clientes, escalado
- Automatización de la interfaz de usuario, escalado de pantalla
- Automatización de la interfaz de usuario, escalado
- ajuste de escala de pantalla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05d790ee7747f258847cd23aea8bbbe8c25813fe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421222"
---
# <a name="understanding-screen-scaling-issues"></a>Descripción de los problemas de escalado de pantalla

Windows Vista y las versiones posteriores del sistema operativo permiten a los usuarios cambiar la configuración de puntos por pulgada (PPP) para que la mayoría de los elementos de la interfaz de usuario de la pantalla parezcan más grandes. En versiones anteriores de Windows, el escalado debía ser implementado por aplicaciones. En Windows Vista y versiones posteriores, el Administrador de ventanas de escritorio (DWM) realiza el escalado predeterminado para todas las aplicaciones que no controlan su propia escala. Las aplicaciones cliente de automatización de la interfaz de usuario de Microsoft deben tener en cuenta esta característica.

Este tema contiene las siguientes secciones:

-   [Escalado en Windows Vista y versiones posteriores](#scaling-in-windows-vista-and-later)
-   [Escalado en los clientes de automatización de la interfaz de usuario](#scaling-in-ui-automation-clients)

## <a name="scaling-in-windows-vista-and-later"></a>Escalado en Windows Vista y versiones posteriores

La configuración de PPP predeterminada es 96, lo que significa que 96 píxeles ocupan el ancho o el alto de una pulgada teórica. La medida exacta de una "pulgada" depende del tamaño y de la resolución física del monitor. Por ejemplo, en un monitor de 12 pulgadas de ancho, con una resolución horizontal de 1280 píxeles, una línea horizontal de 96 píxeles se amplía aproximadamente 9/10 de una pulgada.

Cambiar la configuración de PPP no es lo mismo que cambiar la resolución de pantalla. Con el ajuste de escala de PPP, el número de píxeles físicos de la pantalla sigue siendo el mismo. Sin embargo, el escalado se aplica al tamaño y la ubicación de los elementos de la interfaz de usuario. Este ajuste de escala se puede realizar automáticamente mediante el DWM para el escritorio y para las aplicaciones que no solicitan explícitamente el escalado.

En efecto, cuando el usuario establece el factor de escala en 120 ppp, una pulgada vertical u horizontal en la pantalla aumenta en un 25 por ciento. Todas las dimensiones se escalan en consecuencia. El desplazamiento de una ventana de aplicación desde el borde superior y el borde izquierdo de la pantalla aumenta en un 25 por ciento. Si el ajuste de escala de aplicación está habilitado y la aplicación no es compatible con los PPP, el tamaño de la ventana aumenta en la misma proporción, junto con los desplazamientos y los tamaños de todos los elementos de la interfaz de usuario que contiene.

> [!Note]  
> De forma predeterminada, el DWM no realiza el escalado para las aplicaciones que no reconocen el valor de PPP cuando el usuario establece el valor de PPP en 120, pero realiza el escalado cuando el valor de PPP está establecido en un valor personalizado de 144 o superior. Sin embargo, el usuario puede invalidar el comportamiento predeterminado.

 

El escalado de pantalla crea nuevos desafíos para las aplicaciones a las que les preocupa de cualquier manera las coordenadas de pantalla. La pantalla contiene ahora dos sistemas de coordenadas: físico y lógico. Las coordenadas físicas de un punto son el desplazamiento real en píxeles desde la parte superior izquierda del punto de origen. Las coordenadas lógicas son los desplazamientos de la manera que serían si se escalaran los propios píxeles.

Supongamos que diseña un cuadro de diálogo con un botón en las coordenadas (100, 48). Cuando se muestra este cuadro de diálogo con el valor predeterminado de 96 PPP, el botón se encuentra en las coordenadas físicas de (100, 48). En 120 ppp, se encuentra en las coordenadas físicas de (125, 60). Sin embargo, las coordenadas lógicas son las mismas en cualquier configuración de PPP: (100, 48).

Las coordenadas lógicas son importantes porque hacen que el comportamiento del sistema operativo y las aplicaciones sean coherentes, independientemente del valor de PPP. Por ejemplo, normalmente, la función [**GetCursorPos**](/windows/desktop/api/winuser/nf-winuser-getcursorpos) devuelve las coordenadas lógicas. Si mueve el cursor sobre un elemento en un cuadro de diálogo, se devuelven las mismas coordenadas, independientemente del valor de PPP. Si dibuja un control en (100, 100), se dibuja en esas coordenadas lógicas y ocupará la misma posición relativa en cualquier valor de PPP.

## <a name="scaling-in-ui-automation-clients"></a>Escalado en los clientes de automatización de la interfaz de usuario

La API de automatización de la interfaz de usuario no usa coordenadas lógicas. Los siguientes métodos y propiedades devuelven coordenadas físicas o toman coordenadas físicas como parámetros.

-   [**IUIAutomation::ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)
-   [**IUIAutomation::ElementFromPointBuildCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompointbuildcache)
-   [**IUIAutomationElement::GetClickablePoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getclickablepoint)
-   [**IUIAutomationElement::CurrentBoundingRectangle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentboundingrectangle)
-   [**IUIAutomationElement::CachedBoundingRectangle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedboundingrectangle)
-   [**IRawElementProviderFragment::BoundingRectangle**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-get_boundingrectangle)

De forma predeterminada, las aplicaciones de automatización de la interfaz de usuario que se ejecutan en un entorno que no se establece en 96 PPP no obtendrán los resultados correctos de estos métodos y propiedades. Por ejemplo, dado que la posición del cursor se encuentra en coordenadas lógicas, el cliente no puede pasar estas coordenadas a [**IUIAutomation:: ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint) para obtener el elemento que se encuentra debajo del cursor. Además, la aplicación no podrá colocar correctamente ventanas fuera de su área de cliente.

La solución tiene dos partes.

En primer lugar, haga que la aplicación cliente sea compatible con PPP. Para ello, llame a la función [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) en el inicio. Esta función hace que todo el proceso sea compatible con PPP, lo que significa que todas las ventanas que pertenecen al proceso no se escalan.

En segundo lugar, para obtener coordenadas de cursor, llame a la función [**GetPhysicalCursorPos**](/windows/desktop/api/winuser/nf-winuser-getphysicalcursorpos) .

 

 