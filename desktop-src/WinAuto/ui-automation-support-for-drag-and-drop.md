---
title: Compatibilidad de UI Automation para arrastrar y colocar
description: En este tema se describen los patrones de control que exponen información sobre la funcionalidad de arrastrar y colocar de un elemento.
ms.assetid: FFF5A296-C9FF-4B47-AAF8-A9DD581D9DBE
keywords:
- Automatización de la interfaz de usuario, compatibilidad con arrastrar y colocar
- Automatización de la interfaz de usuario, arrastrar información general del patrón
- Automatización de la interfaz de usuario, introducción al patrón DropTarget
- Automatización de la interfaz de usuario, información general de arrastrar y colocar
- patrones de arrastrar y colocar, acerca de
- Arrastrar patrón de control
- Patrón de control DropTarget
- patrones de control, arrastrar
- patrones de control, DropTarget
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4194613d15aadac4a925303ef2322d4cf53c341c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105685750"
---
# <a name="ui-automation-support-for-drag-and-drop"></a>Compatibilidad de UI Automation para arrastrar y colocar

La automatización de la interfaz de usuario de Microsoft define dos patrones de control para admitir escenarios de arrastrar y colocar, el patrón de control de [arrastre](/windows/desktop/WinAuto/uiauto-implementingdrag) y el patrón de control [DropTarget](/windows/desktop/WinAuto/uiauto-implementingdroptarget) . Se implementa el patrón de control de arrastrar para un elemento que se puede arrastrar y el patrón de control DropTarget para un elemento que puede recibir un elemento arrastrado; es decir, un destino de colocación. Los dos patrones de control exponen información que una tecnología de ayuda puede usar para ayudar a un usuario de accesibilidad a completar una operación de arrastrar y colocar.

-   [Arrastrar estilos](#dragging-styles)
    -   [Estilo de origen/destino](#sourcetarget-style)
    -   [Estilo de solo origen](#source-only-style)
-   [Arrastrar varios elementos](#dragging-multiple-items)
-   [Interfaces de cliente para arrastrar y colocar](#client-interfaces-for-drag-and-drop)

## <a name="dragging-styles"></a>Arrastrar estilos

Al implementar el patrón de control de [arrastrar](/windows/desktop/WinAuto/uiauto-implementingdrag) para un elemento arrastrable, debe decidir si implementar el estilo de arrastre de *origen o destino* , o el estilo *de arrastre solo de origen* .

### <a name="sourcetarget-style"></a>Estilo de origen/destino

En el estilo de origen/destino de arrastrar y colocar, el elemento arrastrado (el "origen") y el elemento de destino de colocación (el "destino") son distintos, y cada uno de ellos genera un conjunto distinto de eventos. A continuación se muestra el ciclo de vida de una operación de arrastre que usa el estilo de origen/destino: <dl> Cuando el usuario inicia una operación de arrastre:

-   El origen genera el evento DragStart ([**UIA \_ Drag \_ DragStartEventId**](uiauto-event-ids.md)).
-   El origen establece la propiedad [**IDragProvider:: IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) en **true**.
-   Los destinos actualizan sus propiedades [**DropTargetEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) .

  
Cuando la operación de arrastrar entra en una región de destino:

-   El destino genera el evento DragEnter ([**UIA \_ DropTarget \_ DragEnterEventId**](uiauto-event-ids.md)).

  
Cuando la operación de arrastrar sale de una región de destino:

-   El destino genera el evento DragLeave ([**UIA \_ DropTarget \_ DragLeaveEventId**](uiauto-event-ids.md)).

  
Cuando el usuario suelta el elemento arrastrado a través de un objeto que no es de destino:

-   El origen genera el evento DragCancel ([**UIA \_ Drag \_ DragCancelEventId**](uiauto-event-ids.md)).
-   El origen establece la propiedad [**IDragProvider:: IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) en **false**.

  
Cuando el usuario suelta el elemento arrastrado a través de un destino:

-   El origen genera el evento DragComplete ([**UIA \_ Drag \_ DragCompleteEventId**](uiauto-event-ids.md)).
-   El origen establece la propiedad [**IDragProvider:: IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) en **false**.
-   El destino establece la propiedad [**IDropTargetProvider::D roptargeteffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) para indicar el efecto que se ha producido.
-   El destino provoca el evento quitado ([**UIA \_ DropTarget \_ DroppedEventId**](uiauto-event-ids.md)).

  
</dl>

Los eventos de los objetos de origen y de destino están estrechamente relacionados, pero distintos. Los datos sobre lo que se está arrastrando provienen del origen, mientras que los datos sobre "lo que podría suceder" y "Qué sucedió" provienen del destino.

Cuando una operación de arrastre está en curso, el elemento arrastrado se puede arrastrar hacia dentro y fuera de las regiones de destino cualquier número de veces antes de que se complete la operación.

Cualquier destino de colocación que necesite actualizar su propiedad [**IDropTargetProvider::D roptargeteffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) sobre la marcha debe generar un evento de cambio de propiedad adicional en esa propiedad.

### <a name="source-only-style"></a>Estilo de solo origen

El estilo de arrastre solo de origen permite a un proveedor evitar la implementación de destinos de colocación. No implementar destinos de colocación ayuda a reducir el costo de implementación, pero no proporciona a las aplicaciones cliente de accesibilidad ninguna información sobre el objeto que recibió la eliminación. A continuación se muestra el ciclo de vida de una operación de arrastre que usa el estilo de solo origen: <dl> Cuando el usuario inicia una operación de arrastre:

-   El origen genera el evento DragStart ([**UIA \_ Drag \_ DragStartEventId**](uiauto-event-ids.md)).
-   El origen establece la propiedad [**IDragProvider:: IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) en **true**.

  
Cuando la operación de arrastrar entra en una región de destino:

-   El origen establece la propiedad [**IDragProvider::D ropeffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) en el valor adecuado.

  
Cuando la operación de arrastrar sale de una región de destino:

-   El origen establece la propiedad [**IDragProvider::D ropeffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) en el valor adecuado.

  
Cuando el usuario suelta el elemento arrastrado a través de un objeto que no es de destino:

-   El origen genera el evento DragCancel ([**UIA \_ Drag \_ DragCancelEventId**](uiauto-event-ids.md)).
-   El origen establece la propiedad [**IDragProvider:: IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) en **false**.

  
Cuando el usuario suelta el elemento arrastrado a través de un destino:

-   El origen genera el evento DragComplete ([**UIA \_ Drag \_ DragCompleteEventId**](uiauto-event-ids.md)).
-   El origen establece la propiedad [**IDragProvider::D ropeffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) para indicar el efecto que tuvo lugar cuando se quitó el elemento.

  
</dl>

## <a name="dragging-multiple-items"></a>Arrastrar varios elementos

Si un proveedor implementa operaciones de arrastrar y colocar en las que el usuario puede arrastrar varios objetos al mismo tiempo, el proveedor utiliza los estilos de origen/destino o solo de origen, tal y como se describe en la sección anterior, pero con una pequeña diferencia. Cuando el usuario inicia la operación de arrastre, el proveedor crea un elemento de origen maestro que representa el conjunto completo de elementos que se arrastran. El elemento de origen maestro genera todos los eventos en nombre del conjunto de elementos arrastrados; los elementos no generan eventos propios.<dl> Cuando el usuario inicia una operación de arrastre:

-   El proveedor crea el elemento de origen principal.
-   El elemento de origen maestro genera el evento DragStart ([**UIA \_ Drag \_ DragStartEventId**](uiauto-event-ids.md)).
-   El elemento de origen Maestro establece la propiedad [**IDragProvider:: IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) en **true**.
-   El elemento de origen principal actualiza la lista de elementos capturados para incluir todos los elementos que se arrastran para que el método [**GetGrabbedItems**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-getgrabbeditems) pueda recuperar la lista.

  
</dl>

En ese momento, el elemento de origen maestro realiza el mismo rol que el elemento de origen, tal y como se describe en la sección anterior.

## <a name="client-interfaces-for-drag-and-drop"></a>Interfaces de cliente para arrastrar y colocar

Las aplicaciones cliente de automatización de la interfaz de usuario usan las interfaces [**IUIAutomationDragPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) y [**IUIAutomationDropTargetPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern) para tener acceso a la información de arrastrar y colocar desde los elementos de la interfaz de usuario.

 

 