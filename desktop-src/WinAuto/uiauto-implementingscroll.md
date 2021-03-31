---
title: Scroll (patrón de control)
description: Describe las directrices y convenciones para implementar IScrollProvider, incluida información sobre propiedades y métodos. El patrón de control scroll se usa para admitir un control que actúa como contenedor desplazable para una colección de objetos secundarios.
ms.assetid: baf8012a-52d5-4465-b26d-aa3d7f550b54
keywords:
- Automatización de la interfaz de usuario, implementar el patrón de control scroll
- Automatización de la interfaz de usuario, patrón de control scroll
- Automatización de la interfaz de usuario, IScrollProvider
- IScrollProvider
- implementar patrones de control scroll de UI Automation
- Patrones de control scroll
- patrones de control, IScrollProvider
- patrones de control, implementar la automatización de la interfaz de usuario
- patrones de control, desplazarse
- interfaces, IScrollProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b525c77a7f89f7adc95a3d90d999f8b243cfcdb6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777707"
---
# <a name="scroll-control-pattern"></a>Scroll (patrón de control)

Describe las directrices y convenciones para implementar [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider), incluida información sobre propiedades y métodos. El patrón de control **Scroll** se usa para admitir un control que actúa como contenedor desplazable para una colección de objetos secundarios.

No es necesario que el control use barras de desplazamiento para admitir la funcionalidad de desplazamiento, aunque normalmente lo hace. En la imagen siguiente se muestra un control de desplazamiento que no utiliza barras de desplazamiento. Para obtener ejemplos de controles que implementan este patrón de control, vea [tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md).

![captura de pantalla que muestra un control de desplazamiento sin barras de desplazamiento](images/uia-scrollpattern-without-scrollbars.jpg)

En este tema se incluyen las siguientes secciones.

-   [Directrices y convenciones de implementación](#implementation-guidelines-and-conventions)
-   [Miembros requeridos para **IScrollProvider**](#required-members-for-iscrollprovider)
-   [Temas relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Directrices y convenciones de implementación

Al implementar el patrón de control **Scroll** , tenga en cuenta las siguientes directrices y convenciones:

-   Los elementos secundarios de este control deben implementar [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider).
-   Las barras de desplazamiento de un control contenedor no admiten el patrón de control **Scroll** . En su lugar, deben admitir el patrón de control [RangeValue](uiauto-implementingrangevalue.md) .
-   Cuando el desplazamiento se mide en porcentajes, todos los valores o cantidades relacionadas con la graduación del desplazamiento deben normalizarse a un intervalo de 0 a 100.
-   La propiedad [**IScrollProvider:: HorizontallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontallyscrollable) y la propiedad [**VerticallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticallyscrollable) son independientes de la propiedad **IsEnabled** .
-   Si la propiedad [**IScrollProvider:: HorizontallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontallyscrollable) es **false**, la propiedad [**HorizontalViewSize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalviewsize) debe establecerse en 100 (100%) y la propiedad [**HorizontalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalscrollpercent) debe establecerse en **UIA \_ ScrollPatternNoScroll** (-1). Del mismo modo, si la propiedad [**VerticallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticallyscrollable) es **false**, la propiedad [**VerticalViewSize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalviewsize) debe establecerse en 100 (100%). y la propiedad [**VerticalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalscrollpercent) debe establecerse en **UIA \_ ScrollPatternNoScroll** (-1). Esto permite que un cliente de automatización de la interfaz de usuario de Microsoft use estos valores de propiedad dentro del método [**SetScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-setscrollpercent) al tiempo que se evita una condición de carrera si se activa una dirección a la que el cliente no está interesado en el desplazamiento.
-   La propiedad [**IScrollProvider:: HorizontalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalscrollpercent) es específica de la configuración regional. Establecer **HorizontalScrollPercent** en 100 debe establecer la ubicación de desplazamiento del control en el equivalente de su posición más a la derecha para idiomas como el inglés que se leen de izquierda a derecha. Como alternativa, para idiomas como el árabe que se leen de derecha a izquierda, el establecimiento de **HorizontalScrollPercent** en 100 debe establecer la ubicación de desplazamiento en la posición más a la izquierda.

## <a name="required-members-for-iscrollprovider"></a>Miembros requeridos para **IScrollProvider**

Se requieren las siguientes propiedades y métodos para implementar la interfaz [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider) .



| Miembros requeridos                                                                  | Tipo de miembro | Notas |
|-----------------------------------------------------------------------------------|-------------|-------|
| [**HorizontalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalscrollpercent) | Propiedad    | None  |
| [**VerticalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalscrollpercent)     | Propiedad    | None  |
| [**HorizontalViewSize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalviewsize)           | Propiedad    | None  |
| [**VerticalViewSize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalviewsize)               | Propiedad    | None  |
| [**HorizontallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontallyscrollable)   | Propiedad    | None  |
| [**VerticallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticallyscrollable)       | Propiedad    | None  |
| [**Scroll**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-scroll)                                   | Método      | None  |
| [**SetScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-setscrollpercent)               | Método      | None  |



 

Este patrón de control no tiene eventos asociados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md)
</dt> <dt>

[Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Información general sobre el árbol de la UI Automation](uiauto-treeoverview.md)
</dt> </dl>

 

 




