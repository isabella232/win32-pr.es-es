---
title: Trabajar con elementos virtualizados
description: En este tema se describe cómo usar la funcionalidad proporcionada por los patrones de control ItemContainer y VirtualizedItem para buscar y recuperar información acerca de los elementos virtualizados.
ms.assetid: e1898ba0-5ffa-4c61-b378-c7ef7c4a2c52
keywords:
- clientes, elementos virtualizados de automatización de la interfaz de usuario
- clientes, elementos virtualizados
- clientes, patrones de control
- clientes, patrones de control de VirtualizedItem
- clientes, patrones de control de ItemContainer
- clientes, patrones de control VirtualizedItem de UI Automation
- clientes, patrones de control de UI Automation
- clientes, patrones de control ItemContainer de UI Automation
- Automatización de la interfaz de usuario, elementos virtualizados
- Automatización de la interfaz de usuario, patrones de control
- Automatización de la interfaz de usuario, patrones de control VirtualizedItem
- Automatización de la interfaz de usuario, patrones de control ItemContainer
- Patrones de control de VirtualizedItem
- Patrones de control de ItemContainer
- patrones de control, VirtualizedItem
- patrones de control, ItemContainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb29232b06304079ad5b9dfdfb589ad510a5b51f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357454"
---
# <a name="working-with-virtualized-items"></a>Trabajar con elementos virtualizados

En este tema se describe cómo usar la funcionalidad proporcionada por los patrones de control [ItemContainer](uiauto-implementingitemcontainer.md) y [VirtualizedItem](uiauto-implementingvirtualizeditem.md) para buscar y recuperar información acerca de los elementos virtualizados.

-   [Información general sobre la virtualización](#overview-of-virtualization)
-   [Cómo un control admite la virtualización](#how-a-control-supports-virtualization)
-   [Cómo los clientes buscan y obtienen elementos virtualizados](#how-clients-find-and-realize-virtualized-items)
-   [Ejemplo](#example)
-   [Temas relacionados](#related-topics)

## <a name="overview-of-virtualization"></a>Información general sobre la virtualización

Los controles que contienen un gran número de elementos secundarios pueden utilizar la virtualización para administrar de forma eficaz los elementos. Con la virtualización, el control mantiene toda la información en memoria solo para un subconjunto de elementos en un momento dado. Normalmente, el subconjunto incluye solo los elementos que están visibles actualmente para el usuario. La información completa sobre los elementos virtualizados restantes se mantiene en el almacenamiento y se carga en la memoria, o se realiza, como lo necesita el control, por ejemplo, a medida que los nuevos elementos se vuelven visibles para el usuario.

Los controles que usan la virtualización representan un desafío porque solo los elementos realizados están totalmente disponibles como elementos de automatización de la interfaz de usuario de Microsoft en el árbol de automatización de la interfaz de usuario. Los elementos virtualizados no existen en el árbol, por lo que la información acerca de ellos no está disponible para los clientes. Para recuperar información sobre los elementos virtualizados, los clientes necesitan una manera de forzar la automatización de la interfaz de usuario para que pase la solicitud para obtener los elementos del control. Una vez que se han realizado los elementos, la automatización de la interfaz de usuario puede crear elementos de automatización de la interfaz de usuario para ellos. La automatización de la interfaz de usuario incluye dos patrones de control para que los clientes puedan trabajar con elementos virtualizados: [ItemContainer](uiauto-implementingitemcontainer.md) y [VirtualizedItem](uiauto-implementingvirtualizeditem.md).

## <a name="how-a-control-supports-virtualization"></a>Cómo un control admite la virtualización

Cualquier control que pueda contener elementos virtualizados debe admitir el patrón de control [ItemContainer](uiauto-implementingitemcontainer.md) . Además, cualquier elemento que se pueda virtualizar debe admitir el patrón de control [VirtualizedItem](uiauto-implementingvirtualizeditem.md) . La funcionalidad que exponen los patrones de control ItemContainer y VirtualizedItem es accesible para los clientes a través de las interfaces [**IUIAutomationItemContainerPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationitemcontainerpattern) y [**IUIAutomationVirtualizedItemPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvirtualizeditempattern) .

## <a name="how-clients-find-and-realize-virtualized-items"></a>Cómo los clientes buscan y obtienen elementos virtualizados

Los clientes pueden usar el método [**IUIAutomationItemContainerPattern:: FindItemByProperty**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationitemcontainerpattern-finditembyproperty) para buscar elementos secundarios en el contenedor basándose en el valor de una propiedad determinada. El método también puede recuperar el primer elemento del contenedor o el elemento que sigue al elemento especificado. Si se encuentra un elemento secundario coincidente, **FindItemByProperty** recupera una interfaz [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) para el elemento. Sin embargo, si el elemento secundario está virtualizado, la interfaz **IUIAutomationElement** es un marcador de posición. El error de [**\_ \_ ELEMENTNOTAVAILABLE UIA E**](uiauto-error-codes.md) se produce cuando el cliente intenta usar la interfaz **IUIAutomationElement** para recuperar los valores de propiedad o llamar a métodos que todavía no están disponibles. Las propiedades o los métodos que están disponibles a través de un marcador de posición dependen de la implementación del control. El único requisito para un marcador de posición es admitir la interfaz [**IUIAutomationVirtualizedItemPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvirtualizeditempattern) .

El [**error \_ \_ ELEMENTNOTAVAILABLE de UIA E**](uiauto-error-codes.md) es una indicación al cliente de que un elemento se puede virtualizar. El cliente debe responder recuperando la interfaz [**IUIAutomationVirtualizedItemPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvirtualizeditempattern) para el elemento y, a continuación, obteniendo el elemento llamando al método [**IUIAutomationVirtualizedItemPattern:: Observate**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationvirtualizeditempattern-realize) . Si esto se realiza correctamente, la interfaz [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) es totalmente funcional con todas las propiedades adecuadas disponibles.

Dependiendo de la implementación del control, la llamada a [**IUIAutomationVirtualizedItemPattern::**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationvirtualizeditempattern-realize) provisión puede hacer que el control desplace el elemento a la vista. Sin embargo, un cliente no debe basarse en el desplazamiento de elementos en la vista o en visible. Para asegurarse de que el elemento está visible, el cliente puede utilizar el método [**IUIAutomationScrollItemPattern:: ScrollIntoView**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationscrollitempattern-scrollintoview) .

## <a name="example"></a>Ejemplo

Para ver un ejemplo de código que muestra cómo usar la compatibilidad con la automatización de la interfaz de usuario para la virtualización, consulte [Cómo recuperar un elemento virtualizado](uiauto-howto-retrieve-virtualized-item.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 




