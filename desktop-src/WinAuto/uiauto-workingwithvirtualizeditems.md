---
title: Trabajar con elementos virtualizados
description: En este tema se describe cómo usar la funcionalidad proporcionada por los patrones de control ItemContainer y VirtualizedItem para buscar y recuperar información sobre elementos virtualizados.
ms.assetid: e1898ba0-5ffa-4c61-b378-c7ef7c4a2c52
keywords:
- clients,Automatización de la interfaz de usuario virtualized items
- clients,virtualized items
- clients,control patterns
- clients,VirtualizedItem control patterns
- clients,ItemContainer control patterns
- clients,Automatización de la interfaz de usuario de control VirtualizedItem
- clients,Automatización de la interfaz de usuario de control
- clients,Automatización de la interfaz de usuario de control ItemContainer
- Automatización de la interfaz de usuario, elementos virtualizados
- Automatización de la interfaz de usuario, patrones de control
- Automatización de la interfaz de usuario, patrones de control VirtualizedItem
- Automatización de la interfaz de usuario, patrones de control ItemContainer
- Patrones de control VirtualizedItem
- Patrones de control ItemContainer
- patrones de control, VirtualizedItem
- patrones de control, ItemContainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e2c0e84f91af6bcaadef5af373b73057fb4a137480255f3ee1af4456e45eaf1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119570375"
---
# <a name="working-with-virtualized-items"></a>Trabajar con elementos virtualizados

En este tema se describe cómo usar la funcionalidad proporcionada por los patrones de control [ItemContainer](uiauto-implementingitemcontainer.md) y [VirtualizedItem](uiauto-implementingvirtualizeditem.md) para buscar y recuperar información sobre elementos virtualizados.

-   [Introducción a la virtualización](#overview-of-virtualization)
-   [Cómo un control admite la virtualización](#how-a-control-supports-virtualization)
-   [Cómo los clientes encuentran y se dan cuenta de los elementos virtualizados](#how-clients-find-and-realize-virtualized-items)
-   [Ejemplo](#example)
-   [Temas relacionados](#related-topics)

## <a name="overview-of-virtualization"></a>Introducción a la virtualización

Los controles que contienen un gran número de elementos secundarios pueden usar la virtualización para administrar eficazmente los elementos. Con la virtualización, el control mantiene toda la información en memoria solo para un subconjunto de elementos en un momento dado. Normalmente, el subconjunto incluye solo los elementos que son visibles actualmente para el usuario. La información completa sobre los elementos virtualizados restantes se mantiene en el almacenamiento y se carga en memoria, o bien se realiza cuando el control lo necesita, por ejemplo, a medida que los nuevos elementos se vuelven visibles para el usuario.

Los controles que usan la virtualización representan un desafío porque solo los elementos realizados están totalmente disponibles como elementos de microsoft Automatización de la interfaz de usuario en el Automatización de la interfaz de usuario aplicación. Los elementos virtualizados no existen en el árbol, por lo que la información sobre ellos no está disponible para los clientes. Para recuperar información sobre los elementos virtualizados, los clientes necesitan una manera de forzar a Automatización de la interfaz de usuario a pasar la solicitud para realizar los elementos al control. Una vez realizados los elementos, Automatización de la interfaz de usuario crear Automatización de la interfaz de usuario para ellos. Automatización de la interfaz de usuario incluye dos patrones de control para permitir que los clientes trabajen con elementos virtualizados: [ItemContainer](uiauto-implementingitemcontainer.md) y [VirtualizedItem](uiauto-implementingvirtualizeditem.md).

## <a name="how-a-control-supports-virtualization"></a>Cómo un control admite la virtualización

Cualquier control que pueda contener elementos virtualizados debe admitir el patrón de control [ItemContainer.](uiauto-implementingitemcontainer.md) Además, cualquier elemento que se pueda virtualizar debe admitir el patrón de control [VirtualizedItem.](uiauto-implementingvirtualizeditem.md) La funcionalidad expuesta por los patrones de control ItemContainer y VirtualizedItem es accesible para los clientes a través de las interfaces [**IUIAutomationItemContainerPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationitemcontainerpattern) e [**IUIAutomationVirtualizedItemPattern.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvirtualizeditempattern)

## <a name="how-clients-find-and-realize-virtualized-items"></a>Cómo los clientes encuentran y se dan cuenta de los elementos virtualizados

Los clientes pueden usar el método [**IUIAutomationItemContainerPattern::FindItemByProperty**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationitemcontainerpattern-finditembyproperty) para buscar elementos secundarios en el contenedor en función del valor de una propiedad determinada. El método también puede recuperar el primer elemento del contenedor o el elemento que sigue al elemento especificado. Si se encuentra un elemento secundario correspondiente, **FindItemByProperty** recupera una [**interfaz IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) para el elemento. Sin embargo, si el elemento secundario está virtualizado, la **interfaz IUIAutomationElement** es un marcador de posición. El error [**UIA \_ E \_ ELEMENTNOTAVAILABLE**](uiauto-error-codes.md) se produce cuando el cliente intenta usar la interfaz **IUIAutomationElement** para recuperar valores de propiedad o llamar a métodos que aún no están disponibles. Las propiedades o métodos disponibles a través de un marcador de posición dependen de la implementación del control. El único requisito para un marcador de posición es admitir la [**interfaz IUIAutomationVirtualizedItemPattern.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvirtualizeditempattern)

El error [**UIA \_ E \_ ELEMENTNOTAVAILABLE**](uiauto-error-codes.md) es una indicación para el cliente de que un elemento se puede virtualizar. El cliente debe responder recuperando la interfaz [**IUIAutomationVirtualizedItemPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvirtualizeditempattern) para el elemento y, a continuación, realizando la realización del elemento llamando al método [**IUIAutomationVirtualizedItemPattern::Realize.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationvirtualizeditempattern-realize) Si esto se realiza correctamente, la [**interfaz IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) es totalmente funcional con todas las propiedades adecuadas disponibles.

En función de la implementación del control, llamar a [**IUIAutomationVirtualizedItemPattern::Realize**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationvirtualizeditempattern-realize) puede hacer que el control se desplace hasta la vista. Sin embargo, un cliente no debe confiar en que el elemento se desplace a la vista o se haga visible. Para asegurarse de que el elemento está visible, el cliente puede usar el método [**IUIAutomationScrollItemPattern::ScrollIntoView.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationscrollitempattern-scrollintoview)

## <a name="example"></a>Ejemplo

Para obtener código de ejemplo que muestra cómo usar el Automatización de la interfaz de usuario compatibilidad con la virtualización, vea [Recuperación de un elemento virtualizado.](uiauto-howto-retrieve-virtualized-item.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 




