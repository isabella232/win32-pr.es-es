---
title: Patrón de control RangeValue
description: Describe las directrices y convenciones para implementar IRangeValueProvider, incluida información sobre propiedades y métodos. El patrón de control RangeValue se usa para admitir controles que se pueden establecer en un valor dentro de un intervalo.
ms.assetid: e5c1104c-4b20-4fdd-bd12-dfc27cb73ac5
keywords:
- Automatización de la interfaz de usuario, implementar el patrón de control RangeValue
- Automatización de la interfaz de usuario, patrón de control RangeValue
- Automatización de la interfaz de usuario, IRangeValueProvider
- IRangeValueProvider
- implementación de patrones de control RangeValue de UI Automation
- Patrones de control de RangeValue
- patrones de control, IRangeValueProvider
- patrones de control, implementar la automatización de la interfaz de usuario RangeValue
- patrones de control, RangeValue
- interfaces, IRangeValueProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf426069ad88ad272fd78c521a220ba7ccf72275
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704699"
---
# <a name="rangevalue-control-pattern"></a>Patrón de control RangeValue

Describe las directrices y convenciones para implementar [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider), incluida información sobre propiedades y métodos. El patrón de control **RangeValue** se usa para admitir controles que se pueden establecer en un valor dentro de un intervalo.

Para obtener ejemplos de controles que implementan este patrón de control, vea [tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md).

En este tema se incluyen las siguientes secciones.

-   [Directrices y convenciones de implementación](#implementation-guidelines-and-conventions)
-   [Miembros requeridos para **IRangeValueProvider**](#required-members-for-irangevalueprovider)
-   [Temas relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Directrices y convenciones de implementación

Al implementar el patrón de control **RangeValue** , tenga en cuenta las siguientes directrices y convenciones:

-   Los controles permiten la recalibración de sus propiedades compatibles según las preferencias de usuario o la configuración regional. Un ejemplo de esto es un control de termómetro que puede establecerse para mostrar la temperatura en grados Fahrenheit o Celsius.
-   Los controles que tienen valores de intervalo ambiguos, como las barras de progreso o los controles deslizantes, deben tener dichos valores normalizados.

## <a name="required-members-for-irangevalueprovider"></a>Miembros requeridos para **IRangeValueProvider**

Se requieren las siguientes propiedades y métodos para implementar la interfaz [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) .



| Miembros requeridos                                              | Tipo de miembro | Notas |
|---------------------------------------------------------------|-------------|-------|
| [**IsReadOnly**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_isreadonly)   | Propiedad    | None  |
| [**Valor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_value)             | Propiedad    | None  |
| [**LargeChange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_largechange) | Propiedad    | None  |
| [**SmallChange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_smallchange) | Propiedad    | None  |
| [**Máxima**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_maximum)         | Propiedad    | None  |
| [**Mínima**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_minimum)         | Propiedad    | None  |
| [**SetValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-setvalue)       | Método      | None  |



 

Este patrón de control no tiene eventos asociados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md)
</dt> <dt>

[Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Información general sobre el árbol de la UI Automation](uiauto-treeoverview.md)
</dt> </dl>

 

 




