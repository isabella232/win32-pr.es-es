---
title: Automatización de la interfaz de usuario compatibilidad con arrastrar y colocar
description: En este tema se describen los patrones de control que exponen información sobre la funcionalidad de arrastrar y colocar de un elemento.
ms.assetid: FFF5A296-C9FF-4B47-AAF8-A9DD581D9DBE
keywords:
- Automatización de la interfaz de usuario, compatibilidad con arrastrar y colocar
- Automatización de la interfaz de usuario,Información general sobre el patrón de arrastre
- Automatización de la interfaz de usuario, introducción al patrón DropTarget
- Automatización de la interfaz de usuario, información general sobre arrastrar y colocar
- patrones de arrastrar y colocar, acerca de
- Patrón de control de arrastre
- Patrón de control DropTarget
- patrones de control,Arrastrar
- patrones de control, DropTarget
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1eab48f4319c51a5ccbbaadae22f1ae337740df5b6d0fdf325a01ba1323f8630
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133568"
---
# <a name="ui-automation-support-for-drag-and-drop"></a>Automatización de la interfaz de usuario compatibilidad con arrastrar y colocar

Microsoft Automatización de la interfaz de usuario define dos patrones de control para admitir escenarios de arrastrar y colocar, el patrón de control [Arrastrar](/windows/desktop/WinAuto/uiauto-implementingdrag) y el patrón de control [DropTarget.](/windows/desktop/WinAuto/uiauto-implementingdroptarget) Implemente el patrón de control Drag para un elemento que se puede arrastrar y el patrón de control DropTarget para un elemento que puede recibir un elemento arrastrado; es decir, un destino de colocación. Los dos patrones de control exponen información que una tecnología de asistencia puede usar para ayudar a un usuario de accesibilidad a completar una operación de arrastrar y colocar.

-   [Arrastrar estilos](#dragging-styles)
    -   [Estilo de origen/destino](#sourcetarget-style)
    -   [Estilo de solo origen](#source-only-style)
-   [Arrastrar varios elementos](#dragging-multiple-items)
-   [Interfaces de cliente para arrastrar y colocar](#client-interfaces-for-drag-and-drop)

## <a name="dragging-styles"></a>Arrastrar estilos

Al implementar el patrón [de](/windows/desktop/WinAuto/uiauto-implementingdrag) control Arrastrar para un elemento arrastrable, debe decidir si se debe implementar el estilo de arrastre de origen/destino o el estilo de arrastre solo *de* origen. 

### <a name="sourcetarget-style"></a>Estilo de origen/destino

En el estilo de origen o destino de arrastrar y colocar, el elemento arrastrado (el "origen") y el elemento drop-target (el "destino") son distintos y cada uno genera un conjunto distinto de eventos. Este es el ciclo de vida de una operación de arrastre que usa el estilo de origen o destino: <dl> Cuando el usuario inicia una operación de arrastre:

-   El origen genera el evento DragStart [**\_ \_ (DragStartEventId) de UIA DragStart.**](uiauto-event-ids.md)
-   El origen establece la [**propiedad IDragProvider::IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) en **TRUE.**
-   Los destinos actualizan [**sus propiedades DropTargetEffect.**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect)

  
Cuando la operación de arrastre entra en una región de destino:

-   El destino genera el evento DragEnter [**(UIA \_ DropTarget \_ DragEnterEventId).**](uiauto-event-ids.md)

  
Cuando la operación de arrastre sale de una región de destino:

-   El destino genera el evento DragLeave [**(UIA \_ DropTarget \_ DragLeaveEventId).**](uiauto-event-ids.md)

  
Cuando el usuario libera el elemento arrastrado sobre un elemento que no es de destino:

-   El origen genera el evento DragCancel [**(DragCancelEventId) de UIA \_ \_ DragCancelEventId.**](uiauto-event-ids.md)
-   El origen establece la [**propiedad IDragProvider::IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) en **FALSE.**

  
Cuando el usuario libera el elemento arrastrado sobre un destino:

-   El origen genera el evento DragComplete [**\_ \_ (DragCompleteEventId) de UIA DragComplete.**](uiauto-event-ids.md)
-   El origen establece la [**propiedad IDragProvider::IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) en **FALSE.**
-   El destino establece la [**propiedad IDropTargetProvider::D ropTargetEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) para indicar el efecto que se produjo.
-   El destino genera el evento Dropped [**\_ (DropTarget \_ DroppedEventId) de UIA.**](uiauto-event-ids.md)

  
</dl>

Los eventos de los objetos de origen y de destino están estrechamente relacionados, pero distintos. Los datos sobre lo que se arrastra proceden del origen, mientras que los datos sobre "lo que podría suceder" y "lo que ha ocurrido" proceden del destino.

Cuando una operación de arrastre está en curso, el elemento arrastrado se puede arrastrar dentro y fuera de las regiones de destino varias veces antes de que se complete la operación.

Cualquier destino de colocación que necesite actualizar su [**propiedad IDropTargetProvider::D ropTargetEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) sobre la marcha debe generar un evento de cambio de propiedad adicional en esa propiedad.

### <a name="source-only-style"></a>Estilo de solo origen

El estilo de arrastre solo de origen permite a un proveedor evitar la implementación de destinos de colocación. No implementar destinos de colocación ayuda a reducir el costo de implementación, pero no proporciona a las aplicaciones cliente de accesibilidad ninguna información sobre el objeto que recibió la colocación. Este es el ciclo de vida de una operación de arrastre que usa el estilo de solo origen: <dl> Cuando el usuario inicia una operación de arrastre:

-   El origen genera el evento DragStart [**\_ \_ (DragStartEventId) de UIA DragStart.**](uiauto-event-ids.md)
-   El origen establece la [**propiedad IDragProvider::IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) en **TRUE.**

  
Cuando la operación de arrastre entra en una región de destino:

-   El origen establece la [**propiedad IDragProvider::D ropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) en el valor adecuado.

  
Cuando la operación de arrastre sale de una región de destino:

-   El origen establece la [**propiedad IDragProvider::D ropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) en el valor adecuado.

  
Cuando el usuario libera el elemento arrastrado sobre un elemento que no es de destino:

-   El origen genera el evento DragCancel [**(DragCancelEventId) de UIA \_ \_ DragCancelEventId.**](uiauto-event-ids.md)
-   El origen establece la [**propiedad IDragProvider::IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) en **FALSE.**

  
Cuando el usuario libera el elemento arrastrado sobre un destino:

-   El origen genera el evento DragComplete [**\_ \_ (DragCompleteEventId) de UIA DragComplete.**](uiauto-event-ids.md)
-   El origen establece la [**propiedad IDragProvider::D ropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) para indicar el efecto que tuvo lugar cuando se quitó el elemento.

  
</dl>

## <a name="dragging-multiple-items"></a>Arrastrar varios elementos

Si un proveedor implementa operaciones de arrastrar y colocar en las que el usuario puede arrastrar varios objetos al mismo tiempo, el proveedor usa los estilos de origen/destino o solo origen, como se describe en la sección anterior, pero con una pequeña diferencia. Cuando el usuario comienza la operación de arrastre, el proveedor crea un elemento de origen maestro que representa el conjunto completo de elementos que se arrastran. El elemento de origen maestro genera todos los eventos en nombre del conjunto de elementos arrastrados; los elementos no genera ningún evento propio.<dl> Cuando el usuario inicia una operación de arrastre:

-   El proveedor crea el elemento de origen maestro.
-   El elemento de origen maestro genera el evento DragStart ([**UIA \_ \_ DragStartEventId**](uiauto-event-ids.md)).
-   El elemento de origen maestro establece [**la propiedad IDragProvider::IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) en **TRUE.**
-   El elemento de origen maestro actualiza la lista de elementos tomados para incluir todos los elementos que se arrastran para que el [**método GetGrabbedItems**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-getgrabbeditems) pueda recuperar la lista.

  
</dl>

Para ese punto, el elemento de origen maestro realiza el mismo rol que el del elemento de origen como se describe en la sección anterior.

## <a name="client-interfaces-for-drag-and-drop"></a>Interfaces de cliente para arrastrar y colocar

Automatización de la interfaz de usuario aplicaciones cliente usan las interfaces [**IUIAutomationDragPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) e [**IUIAutomationDropTargetPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern) para acceder a la información de arrastrar y colocar desde elementos de la interfaz de usuario.

 

 