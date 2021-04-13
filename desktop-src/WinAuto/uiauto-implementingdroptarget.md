---
title: Patrón de control DropTarget
description: Proporciona directrices y convenciones para implementar el patrón de control DropTarget mediante IDropTargetProvider, incluida información sobre propiedades y métodos.
ms.assetid: DD5EE4A0-E6C0-4657-A60F-7F59FC569E04
keywords:
- Automatización de la interfaz de usuario, implementar el patrón de control DropTarget
- Automatización de la interfaz de usuario, patrón de control DropTarget
- Automatización de la interfaz de usuario, IDropTargetProvider
- IDropTargetProvider
- implementación de patrones de control DropTarget de UI Automation
- Patrones de control de DropTarget
- patrones de control, IDropTargetProvider
- patrones de control, implementar la automatización de la interfaz de usuario DropTarget
- patrones de control, DropTarget
- interfaces, IDropTargetProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd03d219ce8b26a0ac01806ebab09892a027fbd1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359152"
---
# <a name="droptarget-control-pattern"></a>Patrón de control DropTarget

Proporciona directrices y convenciones para implementar el patrón de control **DropTarget** mediante [**IDropTargetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-idroptargetprovider), incluida información sobre propiedades y métodos. El patrón de control **DropTarget** se usa para admitir controles que pueden ser el destino de una operación de arrastrar y colocar.

## <a name="implementation-guidelines-and-conventions"></a>Directrices y convenciones de implementación

Al implementar el patrón de control **DropTarget** , use las siguientes directrices y convenciones:

-   Se debe admitir el patrón **DropTarget** mientras se está realizando una operación de arrastre. Se puede admitir incluso cuando una operación de arrastre no está en curso.
-   La propiedad [**IDropTargetProvider::D roptargeteffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) es obligatoria.
-   La propiedad [**IDropTargetProvider::D roptargeteffects**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffects) es necesaria cuando hay más de un efecto de colocación posible para el destino.
-   El elemento debe provocar eventos de cambio de propiedad para las propiedades **DropTargetEffect** ([**UIA \_ DropTargetDropTargetEffectPropertyId**](uiauto-control-pattern-propids.md)) y **DropTargetEffects** ([**UIA \_ DropTargetDropTargetEffectsPropertyId**](uiauto-control-pattern-propids.md)) cuando cambien.

## <a name="required-members-for-idroptargetprovider"></a>Miembros requeridos para **IDropTargetProvider**

Se requieren las siguientes propiedades y métodos para implementar la interfaz [**IDropTargetProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idroptargetprovider) .



| Miembros requeridos                                                                              | Tipo de miembro | Notas                                                                    |
|-----------------------------------------------------------------------------------------------|-------------|--------------------------------------------------------------------------|
| [**DropTargetEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect)                       | Propiedad    | None                                                                     |
| [**DropTargetEffects**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffects)                     | Propiedad    | Obligatorio si el destino de colocación admite más de un posible efecto de colocación. |
| [**UIA \_ DropTarget \_ DragEnterEventId**](uiauto-event-ids.md) | Evento       | None                                                                     |
| [**UIA \_ DropTarget \_ DragLeaveEventId**](uiauto-event-ids.md) | Evento       | None                                                                     |
| [**UIA \_ DropTarget \_ DroppedEventId**](uiauto-event-ids.md)     | Evento       | None                                                                     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md)
</dt> <dt>

[Arrastrar patrón de control](/windows/desktop/WinAuto/uiauto-implementingdrag)
</dt> <dt>

[Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Información general sobre el árbol de la UI Automation](uiauto-treeoverview.md)
</dt> <dt>

[Compatibilidad de UI Automation para arrastrar y colocar](ui-automation-support-for-drag-and-drop.md)
</dt> </dl>

 

 