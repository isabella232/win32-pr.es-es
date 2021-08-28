---
title: Patrón de control DropTarget
description: Proporciona directrices y convenciones para implementar el patrón de control DropTarget mediante IDropTargetProvider, incluida información sobre propiedades y métodos.
ms.assetid: DD5EE4A0-E6C0-4657-A60F-7F59FC569E04
keywords:
- Automatización de la interfaz de usuario, implementación del patrón de control DropTarget
- Automatización de la interfaz de usuario, patrón de control DropTarget
- Automatización de la interfaz de usuario,IDropTargetProvider
- IDropTargetProvider
- implementación de Automatización de la interfaz de usuario de control DropTarget
- Patrones de control DropTarget
- patrones de control,IDropTargetProvider
- patrones de control, implementar Automatización de la interfaz de usuario DropTarget
- patrones de control,DropTarget
- interfaces,IDropTargetProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03cc425c9d41a70150eba2431c6fd317f2f8c23f878f7a0615025aec25b85b68
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098315"
---
# <a name="droptarget-control-pattern"></a>Patrón de control DropTarget

Proporciona directrices y convenciones para implementar el patrón de control **DropTarget** mediante [**IDropTargetProvider,**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-idroptargetprovider)incluida información sobre propiedades y métodos. El patrón de control **DropTarget** se usa para admitir controles que pueden ser el destino de una operación de arrastrar y colocar.

## <a name="implementation-guidelines-and-conventions"></a>Directrices y convenciones de implementación

Al implementar el patrón de control **DropTarget,** use las siguientes directrices y convenciones:

-   El **patrón DropTarget** debe ser compatible mientras hay una operación de arrastre en curso. Se puede admite incluso cuando una operación de arrastre no está en curso.
-   Se requiere la propiedad [**IDropTargetProvider::D ropTargetEffect.**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect)
-   La [**propiedad IDropTargetProvider::D ropTargetEffects**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffects) es necesaria cuando hay más de un posible efecto de colocación para el destino.
-   El elemento debe generar eventos de cambio de propiedad para las propiedades **DropTargetEffect** ([**UIA \_ DropTargetDropTargetEffectPropertyId**](uiauto-control-pattern-propids.md)) y **DropTargetEffects** ([**UIA \_ DropTargetDropTargetEffectsPropertyId)**](uiauto-control-pattern-propids.md)cuando cambian.

## <a name="required-members-for-idroptargetprovider"></a>Miembros necesarios para **IDropTargetProvider**

Las siguientes propiedades y métodos son necesarios para implementar la [**interfaz IDropTargetProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idroptargetprovider)



| Miembros requeridos                                                                              | Tipo de miembro | Notas                                                                    |
|-----------------------------------------------------------------------------------------------|-------------|--------------------------------------------------------------------------|
| [**DropTargetEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect)                       | Propiedad    | Ninguno                                                                     |
| [**DropTargetEffects**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffects)                     | Propiedad    | Obligatorio si el destino de colocación admite más de un posible efecto de colocación. |
| [**DropTarget \_ DragEnterEventId de UIA \_**](uiauto-event-ids.md) | Evento       | Ninguno                                                                     |
| [**DropTarget \_ DragLeaveEventId de UIA \_**](uiauto-event-ids.md) | Evento       | Ninguno                                                                     |
| [**DropTarget \_ DroppedEventId de UIA \_**](uiauto-event-ids.md)     | Evento       | Ninguno                                                                     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md)
</dt> <dt>

[Patrón de control de arrastre](/windows/desktop/WinAuto/uiauto-implementingdrag)
</dt> <dt>

[Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Información general sobre el árbol de la UI Automation](uiauto-treeoverview.md)
</dt> <dt>

[Automatización de la interfaz de usuario compatibilidad con arrastrar y colocar](ui-automation-support-for-drag-and-drop.md)
</dt> </dl>

 

 