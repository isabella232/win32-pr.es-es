---
title: Descripción de los problemas de escalado de pantalla
description: Windows Vista y versiones posteriores del sistema operativo permiten a los usuarios cambiar la configuración de puntos por pulgada (ppp) para que la mayoría de los elementos de la interfaz de usuario de la pantalla parezcan más grandes.
ms.assetid: 27dc49e7-2466-4ea3-a6d9-5ea86d6b4c60
keywords:
- clients,Automatización de la interfaz de usuario de pantalla
- clients,screen scaling
- clients,scaling
- Automatización de la interfaz de usuario, escalado de pantalla
- Automatización de la interfaz de usuario, escalado
- escalado de pantalla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05d790ee7747f258847cd23aea8bbbe8c25813fe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359243"
---
# <a name="understanding-screen-scaling-issues"></a>Descripción de los problemas de escalado de pantalla

Windows Vista y versiones posteriores del sistema operativo permiten a los usuarios cambiar la configuración de puntos por pulgada (ppp) para que la mayoría de los elementos de la interfaz de usuario de la pantalla parezcan más grandes. En versiones anteriores de Windows, las aplicaciones tenían que implementar el escalado. En Windows Vista y versiones posteriores, el Administrador de ventanas de escritorio (DWM) realiza el escalado predeterminado para todas las aplicaciones que no controlan su propio escalado. Las Automatización de la interfaz de usuario cliente de Microsoft deben tener en cuenta esta característica.

Este tema contiene las siguientes secciones:

-   [Escalado en Windows Vista y versiones posteriores](#scaling-in-windows-vista-and-later)
-   [Escalado en los clientes de automatización de la interfaz de usuario](#scaling-in-ui-automation-clients)

## <a name="scaling-in-windows-vista-and-later"></a>Escalado en Windows Vista y versiones posteriores

El valor de ppp predeterminado es 96, lo que significa que 96 píxeles ocupan un ancho o alto de una pulgada notal. La medida exacta de una "pulgada" depende del tamaño y de la resolución física del monitor. Por ejemplo, en un monitor de 12 pulgadas de ancho, con una resolución horizontal de 1280 píxeles, una línea horizontal de 96 píxeles se amplía aproximadamente 9/10 de una pulgada.

Cambiar la configuración de ppp no es lo mismo que cambiar la resolución de pantalla. Con el escalado de ppp, el número de píxeles físicos en la pantalla sigue siendo el mismo. Sin embargo, el escalado se aplica al tamaño y la ubicación de los elementos de la interfaz de usuario. DwM puede realizar este escalado automáticamente para el escritorio y para las aplicaciones que no piden explícitamente que no se esscalen.

De hecho, cuando el usuario establece el factor de escala en 120 ppp, una pulgada vertical u horizontal en la pantalla se hace más grande en un 25 %. Todas las dimensiones se escalan en consecuencia. El desplazamiento de una ventana de aplicación desde el borde superior e izquierdo de la pantalla aumenta un 25 %. Si el escalado de aplicaciones está habilitado y la aplicación no tiene en cuenta ppp, el tamaño de la ventana aumenta en la misma proporción, junto con los desplazamientos y tamaños de todos los elementos de la interfaz de usuario que contiene.

> [!Note]  
> De forma predeterminada, dwm no realiza el escalado para aplicaciones que no tienen en cuenta ppp cuando el usuario establece el valor de ppp en 120, pero realiza el escalado cuando el valor de ppp está establecido en un valor personalizado de 144 o superior. Sin embargo, el usuario puede invalidar el comportamiento predeterminado.

 

El escalado de pantalla crea nuevos desafíos para las aplicaciones a las que les preocupa de cualquier manera las coordenadas de pantalla. La pantalla contiene ahora dos sistemas de coordenadas: físico y lógico. Las coordenadas físicas de un punto son el desplazamiento real en píxeles de la parte superior izquierda del punto de origen. Las coordenadas lógicas son los desplazamientos de la manera que serían si se escalaran los propios píxeles.

Supongamos que diseña un cuadro de diálogo con un botón en las coordenadas (100, 48). Cuando este cuadro de diálogo se muestra con el valor predeterminado de 96 ppp, el botón se encuentra en coordenadas físicas de (100, 48). A 120 ppp, se encuentra en coordenadas físicas de (125, 60). Pero las coordenadas lógicas son las mismas en cualquier configuración de ppp: (100, 48).

Las coordenadas lógicas son importantes, ya que hacen que el comportamiento del sistema operativo y las aplicaciones sea coherente, independientemente de la configuración de ppp. Por ejemplo, normalmente, la [**función GetCursorPos**](/windows/desktop/api/winuser/nf-winuser-getcursorpos) devuelve las coordenadas lógicas. Si mueve el cursor sobre un elemento de un cuadro de diálogo, se devuelven las mismas coordenadas, independientemente de la configuración de ppp. Si dibuja un control en (100, 100), se dibuja en esas coordenadas lógicas y ocupará la misma posición relativa en cualquier configuración de ppp.

## <a name="scaling-in-ui-automation-clients"></a>Escalado en los clientes de automatización de la interfaz de usuario

La API Automatización de la interfaz de usuario no usa coordenadas lógicas. Los métodos y propiedades siguientes devuelven coordenadas físicas o toman coordenadas físicas como parámetros.

-   [**IUIAutomation::ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)
-   [**IUIAutomation::ElementFromPointBuildCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompointbuildcache)
-   [**IUIAutomationElement::GetClickablePoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getclickablepoint)
-   [**IUIAutomationElement::CurrentBoundingRectangle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentboundingrectangle)
-   [**IUIAutomationElement::CachedBoundingRectangle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedboundingrectangle)
-   [**IRawElementProviderFragment::BoundingRectangle**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-get_boundingrectangle)

De forma predeterminada, Automatización de la interfaz de usuario aplicaciones que se ejecutan en un entorno que no está establecido en 96 ppp no obtendrán los resultados correctos de estos métodos y propiedades. Por ejemplo, dado que la posición del cursor está en coordenadas lógicas, el cliente no puede pasar estas coordenadas a [**IUIAutomation::ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint) para obtener el elemento que está bajo el cursor. Además, la aplicación no podrá colocar correctamente ventanas fuera de su área de cliente.

La solución tiene dos partes.

En primer lugar, haga que la aplicación cliente tenga en cuenta los valores de ppp. Para ello, llame a la [**función SetProcessDPIAware en**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) el inicio. Esta función hace que todo el proceso tenga en cuenta los valores de ppp, lo que significa que todas las ventanas que pertenecen al proceso no se escalan.

En segundo lugar, para obtener coordenadas de cursor, llame a [**la función GetPhysicalCursorPos.**](/windows/desktop/api/winuser/nf-winuser-getphysicalcursorpos)

 

 