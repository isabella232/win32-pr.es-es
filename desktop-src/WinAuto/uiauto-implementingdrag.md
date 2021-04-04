---
title: Arrastrar patrón de control
description: Proporciona directrices y convenciones para implementar el patrón de control de arrastre mediante IDragProvider, incluida información sobre propiedades y métodos. El patrón de control arrastrar se usa para admitir controles arrastrables o controles con elementos arrastrables.
ms.assetid: 9853E9CB-D04B-4F67-8E9E-7F1F99BACEA7
keywords:
- Automatización de la interfaz de usuario, implementar el patrón de control arrastrar
- Automatización de la interfaz de usuario, arrastrar patrón de control
- Automatización de la interfaz de usuario, IDragProvider
- IDragProvider
- implementar patrones de control de arrastre de automatización de la interfaz de usuario
- Arrastrar patrones de control
- patrones de control, IDragProvider
- patrones de control, implementar la automatización de la interfaz de usuario
- patrones de control, arrastrar
- interfaces, IDragProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 548f0212eca37e1890596143f27e9af70e1fb19a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077973"
---
# <a name="drag-control-pattern"></a>Arrastrar patrón de control

Proporciona directrices y convenciones para implementar el patrón de control de **arrastre** mediante [**IDragProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-idragprovider), incluida información sobre propiedades y métodos. El patrón de control **arrastrar** se usa para admitir controles arrastrables o controles con elementos arrastrables.

## <a name="implementation-guidelines-and-conventions"></a>Directrices y convenciones de implementación

Al implementar el patrón de control de **arrastre** , use estas directrices y convenciones:

-   La interfaz [**IDragProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idragprovider) admite dos estilos de arrastre diferentes: el estilo de origen y destino, y el estilo de solo origen. Debe elegir el estilo que mejor se adapte a los escenarios de arrastrar y colocar:
    -   **Estilo de origen/destino:** Cada posible destino de colocación se representa mediante un elemento que implementa la interfaz [**IDropTargetProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idroptargetprovider) . Durante una operación de arrastre, los eventos de automatización de la interfaz de usuario de Microsoft se originan a partir del elemento que se está arrastrando y de los elementos de destino.
    -   **Estilo de solo origen:** Los destinos de colocación no se representan mediante elementos de automatización de la interfaz de usuario. Durante una operación de arrastre, los eventos solo se originan desde el elemento que se está arrastrando.
-   [**IDragProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idragprovider) es una interfaz de solo lectura diseñada para la supervisión de operaciones de arrastre. No se puede utilizar para controlar una operación de arrastre. Puede automatizar las operaciones de arrastre enviando la entrada del mouse a un control.
-   La propiedad [**IDragProvider:: IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) es obligatoria.
-   Las propiedades [**IDragProvider::D ropeffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) y [**IDragProvider::D ropeffects**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffects) son necesarias para una implementación de estilo de solo origen y están prohibidas para una implementación de estilo de origen/destino. En una implementación de estilo de origen/destino, se pueden consultar los elementos de destino de colocación para sus efectos de colocación.
-   La propiedad [**IDragProvider:: GrabbedItems**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-getgrabbeditems) representa el arrastre de varios elementos. Cuando el usuario inicia la operación de arrastre, debe crear un nuevo elemento de automatización de la interfaz de usuario para actuar como el elemento de origen del evento. Este nuevo elemento activa todos los eventos que el elemento de origen habría desencadenado en el modo de origen/destino o de solo origen, mientras que ninguno de los elementos que se arrastran realmente activa cualquier evento. Una vez completada la operación de arrastre, destruya el elemento de origen del evento.
-   El elemento debe desencadenar eventos de cambio de propiedad para las propiedades **DropEffect** ([**UIA \_ DragDropEffectPropertyId**](uiauto-control-pattern-propids.md)) y **DropEffects** ([**UIA \_ DragDropEffectsPropertyId**](uiauto-control-pattern-propids.md)) cuando cambian. Se permiten eventos de cambio de propiedad para las demás propiedades, pero se pueden inferir a partir de los eventos **DragStart** ([**UIA \_ Drag \_ DragStartEventId**](uiauto-event-ids.md)), **DragCancel** ([**UIA \_ Drag \_ DragCancelEventId**](uiauto-event-ids.md)) y **DragComplete** ([**UIA \_ Drag \_ DragCompleteEventId**](uiauto-event-ids.md)) necesarios.
-   

## <a name="required-members-for-idragprovider"></a>Miembros requeridos para **IDragProvider**

Se requieren las siguientes propiedades y métodos para implementar la interfaz [**IDragProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-idragprovider) .



| Miembros requeridos                                                                        | Tipo de miembro | Notas                                                                         |
|-----------------------------------------------------------------------------------------|-------------|-------------------------------------------------------------------------------|
| [**IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed)                                     | Propiedad    | None                                                                          |
| [**DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect)                                   | Propiedad    | Se requiere para una implementación del estilo de solo origen.                      |
| [**DropEffects**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffects)                                 | Propiedad    | Obligatorio si hay más de un posible efecto de colocar para el elemento capturado. |
| [**GetGrabbedItems**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-getgrabbeditems)                         | Método      | Se requiere para una operación de arrastre de varios elementos.                                  |
| [**UIA \_ arrastrar \_ DragStartEventId**](uiauto-event-ids.md)       | Evento       | None                                                                          |
| [**UIA \_ arrastrar \_ DragCancelEventId**](uiauto-event-ids.md)     | Evento       | None                                                                          |
| [**UIA \_ arrastrar \_ DragCompleteEventId**](uiauto-event-ids.md) | Evento       | None                                                                          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md)
</dt> <dt>

[Patrón de control DropTarget](/windows/desktop/WinAuto/uiauto-implementingdroptarget)
</dt> <dt>

[Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Información general sobre el árbol de la UI Automation](uiauto-treeoverview.md)
</dt> <dt>

[Compatibilidad de UI Automation para arrastrar y colocar](ui-automation-support-for-drag-and-drop.md)
</dt> </dl>

 

 