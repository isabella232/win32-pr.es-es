---
title: Patrón de control ItemContainer
description: Describe las directrices y convenciones para implementar IItemContainerProvider, incluida la información sobre los métodos. El patrón de control ItemContainer se usa para admitir la virtualización de elementos.
ms.assetid: 6f3dd94e-3563-4a13-9db9-5928a02bab77
keywords:
- Automatización de la interfaz de usuario, implementar el patrón de control ItemContainer
- Automatización de la interfaz de usuario,Patrón de control ItemContainer
- Automatización de la interfaz de usuario,IItemContainerProvider
- IItemContainerProvider
- implementación de Automatización de la interfaz de usuario de control ItemContainer
- Patrones de control ItemContainer
- patrones de control,IItemContainerProvider
- patrones de control, implementar Automatización de la interfaz de usuario ItemContainer
- patrones de control, ItemContainer
- interfaces,IItemContainerProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f69c0407a8f167a3a89b908c1b5555a9d32363b38b3ce5ab4d1794e726666a8c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119413464"
---
# <a name="itemcontainer-control-pattern"></a>Patrón de control ItemContainer

Describe las directrices y convenciones para implementar [**IItemContainerProvider,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iitemcontainerprovider)incluida la información sobre los métodos. El patrón de control **ItemContainer** se usa para admitir la virtualización de elementos.

Los controles que contienen un gran número de elementos secundarios pueden usar la virtualización para administrar los elementos de forma eficaz. Con la virtualización, el control mantiene toda la información en memoria solo para un subconjunto de elementos en un momento dado. Normalmente, el subconjunto incluye solo los elementos que son visibles actualmente para el usuario. La información completa sobre los elementos virtualizados restantes se mantiene en el almacenamiento y se carga en la memoria, o se realiza a medida que el control lo necesita, por ejemplo, a medida que los nuevos elementos se vuelven visibles para el usuario.

Por ejemplo, en el diagrama siguiente se muestra un cuadro de lista que contiene miles de elementos virtualizados. Dado que el control mantiene información completa solo para los elementos secundarios que están visibles actualmente, el proveedor puede exponer elementos de Microsoft Automatización de la interfaz de usuario solo para los elementos 100 a 127.

![diagrama que muestra los elementos de un cuadro de lista que están virtualizados y no virtualizados](images/virtualizeditems.jpg)

Los controles que usan la virtualización representan un desafío porque solo los elementos realizados (des virtualizados) están totalmente disponibles como elementos Automatización de la interfaz de usuario en el Automatización de la interfaz de usuario virtualizado. Los elementos virtualizados no existen en el árbol, por lo que la información sobre ellos no está disponible.

Para proporcionar información sobre los elementos virtualizados, los proveedores implementan el patrón de control **ItemContainer,** que expone la [**interfaz IItemContainerProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iitemcontainerprovider) El [**método FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) busca elementos secundarios basados en el valor de una propiedad determinada, como **Name**, **AutomationId** o **IsSelected**. Si un elemento está virtualizado, **FindItemByProperty** recupera un Automatización de la interfaz de usuario marcador de posición para el elemento. Un elemento de marcador de posición es una implementación de [**la interfaz IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) que solo admite el patrón de control [VirtualizedItem.](uiauto-implementingvirtualizeditem.md)

El [**método IVirtualizedItemProvider::Realize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) permite a un cliente solicitar que se haga realidad un elemento virtualizado, con lo que se expone un elemento Automatización de la interfaz de usuario completo para el elemento para que estén disponibles todas las propiedades y patrones necesarios.

Aunque el propósito principal del patrón de control **ItemContainer** es admitir escenarios de contenedor virtualizados, cualquier contenedor que recupere elementos secundarios por nombre, independientemente de si el contenedor usa virtualización.

En este tema se incluyen las siguientes secciones.

-   [Directrices y convenciones de implementación](#implementation-guidelines-and-conventions)
-   [Miembros necesarios para IItemContainerProvider](#required-members-for-iitemcontainerprovider)
-   [Temas relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Directrices y convenciones de implementación

Al implementar el patrón de control **ItemContainer,** tenga en cuenta las siguientes directrices y convenciones:

-   Cualquier control que pueda contener elementos virtualizados debe admitir el patrón de control **ItemContainer.** Cualquier contenedor que admita la recuperación de elementos basados en un valor de propiedad puede admitir este patrón, independientemente de si el contenedor usa virtualización.
-   Cuando se virtualiza un contenedor, se pueden ver afectados otros patrones de controles como [Selección,](uiauto-implementingselection.md) [Tabla](uiauto-implementingtable.md) [y](uiauto-implementinggrid.md) Cuadrícula. Por ejemplo, el método [**ISelectionProvider::GetSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-getselection) solo puede admitir elementos que se encuentran en la ventanilla o solo los elementos seleccionados que no están virtualizados actualmente.
-   El [patrón de](uiauto-implementingscroll.md) control Scroll no debe estar afectado por la virtualización.
-   No hay información de índice o recuento de elementos disponible para los elementos virtualizados. Un control virtualizado puede usar la **propiedad DescribedBy** o **ItemStatus** para proporcionar esta información, si es necesario.
-   Los desarrolladores de controles deben documentar y publicar detalles Automatización de la interfaz de usuario propiedades y patrones de control afectados por el uso de la virtualización. Aunque los patrones de control ItemContainer y [VirtualizedItem](uiauto-implementingvirtualizeditem.md) ofrecen compatibilidad básica, es posible que no admitan algunos comportamientos de virtualización.

Las siguientes directrices y requisitos se aplican [**al método IItemContainerProvider::FindItemByProperty.**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty)

-   Aunque no es necesario, Microsoft recomienda encarecidamente que [**FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) admita las propiedades **Name**, **AutomationId** e **IsSelected.**
-   [**FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) puede ser lento si necesita recorrer varios objetos para encontrar uno que coincida.
-   [**Se puede llamar a FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) repetidamente para buscar elementos en secuencia. Los elementos pueden estar en cualquier orden siempre y cuando cada elemento se devuelva una sola vez.
-   [**FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) se puede implementar para buscar solo los elementos que aparecen en el control o la vista de contenido del Automatización de la interfaz de usuario árbol. Los elementos que solo aparecen en la vista sin formato se pueden omitir para evitar la recuperación de varios elementos que representan solo una parte de un "elemento" para el usuario.
-   Cuando los criterios de búsqueda coinciden con un elemento virtualizado, el proveedor puede devolver un elemento de marcador de posición que admita el patrón de control [VirtualizedItem.](uiauto-implementingvirtualizeditem.md) Las instrucciones siguientes se aplican a los elementos de marcador de posición:
    -   La recuperación de un elemento de marcador de posición para un elemento virtualizado no debe producir cambios en la interfaz de usuario.
    -   El elemento de marcador de posición debe ser un elemento del mismo nivel que otros elementos secundarios (se requiere un evento de cambio de estructura).
    -   Cuando sea posible, el proveedor puede crear un elemento de automatización completo en lugar de un marcador de posición.
-   Cuando los criterios de búsqueda coinciden con un elemento no virtualizado, el proveedor debe devolver el elemento real, no un marcador de posición.
-   Cuando no se encuentra ningún elemento, [**IItemContainerProvider::FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) debe establecer el *parámetro pFound* en **NULL** y devolver **S \_ OK**.
-   Cuando el *parámetro propertyId* es 0, el proveedor debe devolver el siguiente elemento después de *pStartAfter*.
-   Si el *parámetro pStartAfter* es **NULL** y *propertyId* es 0, el proveedor debe devolver el primer elemento del contenedor.
-   Cuando el *parámetro propertyId* es 0, se omite el parámetro value.

Las siguientes directrices y requisitos se aplican a los elementos de marcador de posición para los elementos virtualizados del Automatización de la interfaz de usuario virtualizado.

-   Aunque se recomienda que los proveedores admitan más propiedades y patrones de control para un elemento de marcador de posición, solo se requiere el patrón de control [VirtualizedItem.](uiauto-implementingvirtualizeditem.md)
-   El proveedor puede invalidar un elemento de marcador de posición anterior cuando se vuelve a llamar a [**IItemContainerProvider::FindItemByProperty.**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) (Si un cliente necesita obtener el elemento de marcador de posición, debe hacerlo inmediatamente; de lo contrario, el elemento se puede invalidar si se vuelve a llamar a **FindItemByProperty** o si la ventanilla cambia por cualquier motivo).
-   Las acciones de la interfaz de usuario, como el desplazamiento o el cambio de tamaño, pueden hacer que la ventanilla del contenedor cambie y que un nuevo conjunto de elementos secundarios se vuelva visible. En este caso, es posible que los elementos de marcador de posición recuperados previamente no estén disponibles en el Automatización de la interfaz de usuario anterior.
-   El proveedor no debe virtualizar los elementos de la interfaz de usuario que están disponibles en pantalla en la ventanilla del objeto contenedor.

## <a name="required-members-for-iitemcontainerprovider"></a>Miembros necesarios para IItemContainerProvider

El método siguiente es necesario para implementar la [**interfaz IItemContainerProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iitemcontainerprovider)



| Miembros requeridos                                                               | Tipo de miembro | Notas |
|--------------------------------------------------------------------------------|-------------|-------|
| [**FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) | Método      | None  |



 

El patrón de control **ItemContainer** no tiene propiedades ni eventos asociados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md)
</dt> <dt>

[Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Información general sobre el árbol de la UI Automation](uiauto-treeoverview.md)
</dt> <dt>

[Patrón de control VirtualizedItem](uiauto-implementingvirtualizeditem.md)
</dt> </dl>

 

 




