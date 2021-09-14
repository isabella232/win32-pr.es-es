---
title: Patrón de control de desplazamiento
description: Describe directrices y convenciones para implementar IScrollProvider, incluida información sobre propiedades y métodos. El patrón de control Scroll se usa para admitir un control que actúa como contenedor desplazable para una colección de objetos secundarios.
ms.assetid: baf8012a-52d5-4465-b26d-aa3d7f550b54
keywords:
- Automatización de la interfaz de usuario, implementación del patrón de control Scroll
- Automatización de la interfaz de usuario,patrón de control Scroll
- Automatización de la interfaz de usuario,IScrollProvider
- IScrollProvider
- implementar patrones Automatización de la interfaz de usuario control Scroll
- Patrones de control de desplazamiento
- patrones de control, IScrollProvider
- patrones de control, implementar Automatización de la interfaz de usuario scroll
- patrones de control,Scroll
- interfaces,IScrollProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b525c77a7f89f7adc95a3d90d999f8b243cfcdb6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070486"
---
# <a name="scroll-control-pattern"></a>Patrón de control de desplazamiento

Describe directrices y convenciones para implementar [**IScrollProvider,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)incluida información sobre propiedades y métodos. El **patrón de** control Scroll se usa para admitir un control que actúa como contenedor desplazable para una colección de objetos secundarios.

El control no es necesario para usar barras de desplazamiento para admitir la funcionalidad de desplazamiento, aunque normalmente lo hace. En la imagen siguiente se muestra un control de desplazamiento que no usa barras de desplazamiento. Para obtener ejemplos de controles que implementan este patrón de control, vea [Tipos de control y Sus patrones de control admitidos.](uiauto-controlpatternmapping.md)

![captura de pantalla que muestra un control de desplazamiento sin barras de desplazamiento](images/uia-scrollpattern-without-scrollbars.jpg)

En este tema se incluyen las siguientes secciones.

-   [Directrices y convenciones de implementación](#implementation-guidelines-and-conventions)
-   [Miembros necesarios para **IScrollProvider**](#required-members-for-iscrollprovider)
-   [Temas relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Directrices y convenciones de implementación

Al implementar el patrón de control **Scroll,** tenga en cuenta las siguientes directrices y convenciones:

-   Los elementos secundarios de este control deben implementar [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider).
-   Las barras de desplazamiento de un control de contenedor no admiten el patrón de control **Scroll.** En su lugar, deben admitir el patrón de control [RangeValue.](uiauto-implementingrangevalue.md)
-   Cuando el desplazamiento se mide en porcentajes, todos los valores o cantidades relacionadas con la graduación del desplazamiento deben normalizarse a un intervalo de 0 a 100.
-   La [**propiedad IScrollProvider::HorizontallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontallyscrollable) y la propiedad [**VerticallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticallyscrollable) son independientes de **la propiedad IsEnabled.**
-   Si la propiedad [**IScrollProvider::HorizontallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontallyscrollable) es **FALSE,** la propiedad [**HorizontalViewSize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalviewsize) debe establecerse en 100 (100 %) y la propiedad [**HorizontalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalscrollpercent) debe establecerse en **UIA \_ ScrollPatternNoScroll** (-1). Del mismo modo, si la propiedad [**VerticallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticallyscrollable) es **FALSE,** la propiedad [**VerticalViewSize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalviewsize) debe establecerse en 100 (100 %) y la propiedad [**VerticalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalscrollpercent) debe establecerse en **UIA \_ ScrollPatternNoScroll** (-1). Esto permite que un cliente de Microsoft Automatización de la interfaz de usuario use estos valores de propiedad dentro del método [**SetScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-setscrollpercent) mientras se evita una condición de carrera si se activa una dirección en la que el cliente no está interesado en desplazarse.
-   La [**propiedad IScrollProvider::HorizontalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalscrollpercent) es específica de la configuración regional. El **establecimiento de HorizontalScrollPercent** en 100 debe establecer la ubicación de desplazamiento del control en el equivalente de su posición más a la derecha para idiomas como el inglés que se lee de izquierda a derecha. Como alternativa, para los idiomas como el árabe que se leen de derecha a izquierda, el establecimiento de **HorizontalScrollPercent** en 100 debe establecer la ubicación de desplazamiento en la posición más izquierda.

## <a name="required-members-for-iscrollprovider"></a>Miembros necesarios para **IScrollProvider**

Las siguientes propiedades y métodos son necesarios para implementar la [**interfaz IScrollProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)



| Miembros requeridos                                                                  | Tipo de miembro | Notas |
|-----------------------------------------------------------------------------------|-------------|-------|
| [**HorizontalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalscrollpercent) | Propiedad.    | None  |
| [**VerticalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalscrollpercent)     | Propiedad.    | None  |
| [**HorizontalViewSize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalviewsize)           | Propiedad.    | None  |
| [**VerticalViewSize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalviewsize)               | Propiedad.    | None  |
| [**HorizontallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontallyscrollable)   | Propiedad.    | None  |
| [**VerticalmenteScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticallyscrollable)       | Propiedad.    | None  |
| [**Pergamino**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-scroll)                                   | Método      | None  |
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

 

 




