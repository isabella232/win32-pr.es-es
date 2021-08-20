---
title: Patrón de control RangeValue
description: Describe directrices y convenciones para implementar IRangeValueProvider, incluida información sobre propiedades y métodos. El patrón de control RangeValue se usa para admitir controles que se pueden establecer en un valor dentro de un intervalo.
ms.assetid: e5c1104c-4b20-4fdd-bd12-dfc27cb73ac5
keywords:
- Automatización de la interfaz de usuario, implementación del patrón de control RangeValue
- Automatización de la interfaz de usuario,patrón de control RangeValue
- Automatización de la interfaz de usuario,IRangeValueProvider
- IRangeValueProvider
- implementación de Automatización de la interfaz de usuario de control RangeValue
- Patrones de control RangeValue
- patrones de control,IRangeValueProvider
- patrones de control, implementar Automatización de la interfaz de usuario RangeValue
- patrones de control,RangeValue
- interfaces,IRangeValueProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae87ca25fd1ada2f57ce77412fb589875792541fd2b5d31d6eb0aa86192dee36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118114866"
---
# <a name="rangevalue-control-pattern"></a>Patrón de control RangeValue

Describe directrices y convenciones para implementar [**IRangeValueProvider,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider)incluida información sobre propiedades y métodos. El patrón de control **RangeValue** se usa para admitir controles que se pueden establecer en un valor dentro de un intervalo.

Para obtener ejemplos de controles que implementan este patrón de control, vea [Tipos de control y sus patrones de control admitidos.](uiauto-controlpatternmapping.md)

En este tema se incluyen las siguientes secciones.

-   [Directrices y convenciones de implementación](#implementation-guidelines-and-conventions)
-   [Miembros necesarios para **IRangeValueProvider**](#required-members-for-irangevalueprovider)
-   [Temas relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Directrices y convenciones de implementación

Al implementar el patrón de control **RangeValue,** tenga en cuenta las siguientes directrices y convenciones:

-   Los controles permiten la recalibración de sus propiedades compatibles según las preferencias de usuario o la configuración regional. Un ejemplo de esto es un control de termómetro que puede establecerse para mostrar la temperatura en grados Fahrenheit o Celsius.
-   Los controles que tienen valores de intervalo ambiguos, como las barras de progreso o los controles deslizantes, deben tener dichos valores normalizados.

## <a name="required-members-for-irangevalueprovider"></a>Miembros necesarios para **IRangeValueProvider**

Las siguientes propiedades y métodos son necesarios para implementar la [**interfaz IRangeValueProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider)



| Miembros requeridos                                              | Tipo de miembro | Notas |
|---------------------------------------------------------------|-------------|-------|
| [**IsReadOnly**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_isreadonly)   | Propiedad    | Ninguno  |
| [**Valor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_value)             | Propiedad    | Ninguno  |
| [**LargeChange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_largechange) | Propiedad    | Ninguno  |
| [**SmallChange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_smallchange) | Propiedad    | Ninguno  |
| [**Máximo**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_maximum)         | Propiedad    | Ninguno  |
| [**Mínima**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_minimum)         | Propiedad    | Ninguno  |
| [**SetValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-setvalue)       | Método      | Ninguno  |



 

Este patrón de control no tiene eventos asociados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md)
</dt> <dt>

[Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Información general sobre el árbol de la UI Automation](uiauto-treeoverview.md)
</dt> </dl>

 

 




