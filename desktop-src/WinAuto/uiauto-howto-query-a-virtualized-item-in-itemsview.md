---
title: Consulta de un elemento virtualizado en la vista Elementos
description: En este tema se describe cómo usar Microsoft Automatización de la interfaz de usuario recuperar información de la interfaz de usuario sobre los elementos virtualizados en la Windows 7 elementos.
ms.assetid: a0bff8a1-47b1-4750-8086-e2e65a79099e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9196d62e7aa93b21aed15b76b8ced6a9520b27fb5bcee74a0e0d4ddc510c86f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119759255"
---
# <a name="how-to-query-a-virtualized-item-in-items-view"></a>Consulta de un elemento virtualizado en la vista Elementos

En este tema se describe cómo usar Microsoft Automatización de la interfaz de usuario recuperar información de la interfaz de usuario sobre los elementos virtualizados en la Windows 7 elementos. En este tema se incluyen las secciones siguientes.

> [!Note]  
> Este tema solo se aplica Windows 7. Tenga en cuenta que las características de accesibilidad descritas en este tema pueden cambiar en versiones futuras de Windows.

 

-   [Información general](#overview)
-   [Estructura del árbol de vista Elementos](#items-view-tree-structure)
-   [Virtualización](#virtualization)
-   [Obtener un recuento de todos los elementos](#obtaining-a-count-of-all-items)
-   [Obtener un índice de elementos con respecto a todos los elementos](#obtaining-an-item-index-with-respect-to-all-items)
-   [Obtener una referencia a un elemento Vitualized](#obtaining-a-reference-to-a-vitualized-item)
-   [Desplazamiento de un elemento virtualizado en pantalla](#scrolling-a-virtualized-item-on-screen)
-   [Temas relacionados](#related-topics)

## <a name="overview"></a>Información general

Vista elementos es un componente de interfaz de usuario que permite a los usuarios ver archivos y otros elementos e interactuar con ellos. En Windows 7, vista Elementos reemplaza el control de vista de lista para presentar elementos en la vista predeterminada de Windows Explorer. La vista Elementos también se usa en el cuadro de diálogo Elemento común, menú Inicio resultados de búsqueda y otros Windows de interfaz de usuario de Windows 7 que usan el control Explorador del Explorador. En comparación con el control list-view, la vista Elementos ofrece las siguientes ventajas a los usuarios:

-   La vista Elementos puede presentar elementos de maneras más útiles, deseables y pertinentes, lo que permite a los usuarios buscar y organizar elementos de forma más sencilla, rápida y sencilla.
-   La vista Elementos puede mostrar grandes conjuntos de elementos de orígenes de datos que tienen características de rendimiento diferentes, lo que permite a los usuarios examinar y buscar toda su colección de elementos en varios orígenes.

En la imagen siguiente se muestra la vista Elementos en Windows Explorer.

![captura de pantalla que muestra el explorador de Windows con el componente de vista de elementos](images/itemsview.gif)

Desde la perspectiva de un desarrollador, la estructura general y la funcionalidad de la vista elementos es similar a la del control list-view. La principal diferencia es que la vista Elementos admite la virtualización, mientras que el control list-view no. Además, la vista Elementos usa dos nuevas interfaces Automatización de la interfaz de usuario para asegurarse de que el contenido virtualizado proporcionado por la vista Elementos es accesible. Estas interfaces se describen en las secciones siguientes de este tema.

Para obtener información general sobre la virtualización Automatización de la interfaz de usuario, vea [Trabajar con elementos virtualizados.](uiauto-workingwithvirtualizeditems.md)

## <a name="items-view-tree-structure"></a>Estructura del árbol de vista Elementos

En el Automatización de la interfaz de usuario, el elemento de nivel superior Automatización de la interfaz de usuario de la vista elementos tiene el nombre "ItemsView" y el tipo de control "list". En la imagen anterior, el elemento Automatización de la interfaz de usuario ItemsView se describe en rojo. Existen varios Automatización de la interfaz de usuario de datos por debajo del nivel superior de ItemsView, pero solo se hace referencia a otros dos elementos Automatización de la interfaz de usuario en este documento: elementos de grupo y elementos de lista.

Los elementos de grupo son los Automatización de la interfaz de usuario que contienen todos los elementos de lista de ese grupo; su tipo de control es "Group" y sus nombres varían en función del nombre del grupo. En la imagen anterior, el primer elemento de grupo contiene el encabezado "A-H (1)" y el elemento de lista "Carpeta", y su nombre es "A-H".

Los elementos de lista son Automatización de la interfaz de usuario que representan los elementos hoja en la vista; su tipo de control es "ListItem" y sus nombres varían en función del nombre del elemento. En la imagen anterior, los elementos de lista son los elementos hoja, como "Carpeta", "Música" e "Imagen". Estos tres Automatización de la interfaz de usuario se conocen mediante los términos Elemento ItemsView, Elemento Group y Elemento ListItem en el resto de este documento.

## <a name="virtualization"></a>La virtualización

La vista Elementos usa virtualización, lo que significa que los elementos fuera del área visible de la vista no se capturan del sistema y no se crea la representación de la interfaz de usuario de ellos. Estos elementos se *denominan elementos virtualizados.* Dado que no se crean, los elementos virtualizados no tienen elementos Automatización de la interfaz de usuario y, por tanto, no aparecen en el árbol de Automatización de la interfaz de usuario cuando un cliente de Automatización de la interfaz de usuario enumera el árbol. Además, Automatización de la interfaz de usuario de control solo funcionan en elementos visibles. Por ejemplo, el patrón de control [Selection](uiauto-implementingselection.md) devuelve solo los elementos seleccionados visibles cuando un cliente llama al método [**IUIAutomationSelectionPattern::GetCurrentSelection.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionpattern-getcurrentselection)

La vista Elementos admite la capacidad de recuperar la siguiente información sobre los elementos virtualizados:

-   Recuento del número total de elementos, incluidos los elementos virtualizados
-   Automatización de la interfaz de usuario para elementos virtualizados
-   Automatización de la interfaz de usuario para los elementos virtualizados seleccionados

## <a name="obtaining-a-count-of-all-items"></a>Obtener un recuento de todos los elementos

Un cliente puede usar el elemento ItemsView para obtener un recuento de todos los elementos, así como un recuento de los elementos seleccionados. El elemento ItemsView proporciona dos maneras de obtener estos recuentos. La primera es obtener la propiedad ItemStatus del elemento ItemsView y la segunda es obtener propiedades personalizadas del elemento ItemsView.

La propiedad ItemStatus es una cadena que especifica un recuento del número total de elementos y un recuento de los elementos seleccionados, separados por una coma. Por ejemplo: "3 elementos, 1 elemento seleccionado". Esta cadena está localizada y se puede comunicar directamente al usuario.

Las propiedades personalizadas del elemento ItemsView incluyen una propiedad para el recuento de elementos y otra para el recuento de selección. Entre ellas, las siguientes:

-   GUID de la propiedad ItemCount \_ \_ (ABBF5C45-5CCC-47b7-BB4E-87CB87BBD162): el recuento de todos los elementos únicos de la vista. Si se agrupa por una propiedad de varios valores (MVP) para que un único elemento pueda aparecer varias veces, cada elemento se cuenta solo una vez.

    (UIAutomationType: [**UIAutomationType \_ Int**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-uiautomationtype), Nombre de programación: "ItemCount")

-   GUID de propiedad SelectedItemCount \_ \_ (92A053DA-2969-4021-BF27-514CFC2E4A69): el recuento de todos los elementos únicos seleccionados en la vista. Si se agrupa por una propiedad de varios valores (MVP) para que un único elemento pueda aparecer varias veces, cada elemento se cuenta solo una vez.

    (UIAutomationType: [**UIAutomationType \_ Int**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-uiautomationtype), Nombre de programación: "SelectedItemCount")

Estas propiedades personalizadas se definen en Shlguid.h, que se incluye en el Kit de desarrollo de software (SDK) de Windows y estas propiedades se registran mediante el método [**IUIAutomationRegistrar::RegisterProperty.**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) Automatización de la interfaz de usuario usan **RegisterProperty para** recuperar los identificadores de propiedad (PROPERTYID) de las propiedades personalizadas.

## <a name="obtaining-an-item-index-with-respect-to-all-items"></a>Obtener un índice de elementos con respecto a todos los elementos

Un cliente puede obtener el índice de un elemento obteniendo la propiedad ItemStatus de un elemento ListItem o obteniendo una propiedad personalizada de un elemento ListItem.

La propiedad ItemStatus es una cadena que contiene el índice de un elemento con respecto al número total de elementos. Por ejemplo: "elemento 1 de 3". Esta cadena está localizada y se puede comunicar directamente al usuario.

La siguiente propiedad personalizada obtiene el índice de elemento de un elemento ListItem:

-   GUID de propiedad ItemIndex \_ \_ (92A053DA-2969-4021-BF27-514CFC2E4A69): índice absoluto basado en 1 de un elemento. Si se agrupa por una propiedad de varios valores (MVP) para que un único elemento pueda aparecer dos veces, cada apariencia del elemento obtiene un índice independiente.

    (UIAutomationType: [**UIAutomationType \_ Int**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-uiautomationtype), Nombre de programación: "ItemIndex")

Esta propiedad personalizada se define en Shlguid.h, que se incluye en el SDK de Windows y se registra mediante el método [**IUIAutomationRegistrar::RegisterProperty.**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) Automatización de la interfaz de usuario clientes usan **RegisterProperty para** recuperar un identificador de propiedad (PROPERTYIDs) para la propiedad personalizada.

## <a name="obtaining-a-reference-to-a-vitualized-item"></a>Obtener una referencia a un elemento Vitualized

Un elemento ItemsView implementa el patrón de control [ItemContainer](uiauto-implementingitemcontainer.md) (interfaz [**IItemContainerProvider),**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iitemcontainerprovider) que permite a un cliente obtener un elemento Automatización de la interfaz de usuario para un elemento virtualizado (un elemento que está fuera del área visible). ItemsView permite al cliente encontrar un elemento ListItem mediante la búsqueda en las propiedades Name y Selection, ya que se producirá un error al intentar buscar en cualquier otra propiedad.

Un elemento virtual implementa solo el patrón de control [VirtualizedItem](uiauto-implementingvirtualizeditem.md) [**(interfaz IVirtualizedItemProvider).**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider) Dado que el elemento representado por un elemento Automatización de la interfaz de usuario virtualizado aún no existe, se producirá un error al intentar obtener cualquier otro patrón de control o propiedad del elemento.

Los elementos ListItem y Group están virtualizados, pero solo se pueden devolver elementos ListItem desde el patrón de control [ItemContainer.](uiauto-implementingitemcontainer.md) Dado que la llamada al método [**IUIAutomationItemContainerPattern::FindItemByProperty**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationitemcontainerpattern-finditembyproperty) se ejecuta en el subproceso de interfaz de usuario y está bloqueando, la vista no responderá hasta que se devuelva **FindItemByProperty** y cualquier otra llamada al método en el proveedor debe esperar hasta que **finalice FindItemByProperty.** En algunos casos, **FindItemByProperty** debe procesar todo el conjunto de datos antes de devolverlo, lo que puede hacer un uso intensivo de los recursos. Si se **especifica NULL** como elemento inicial, **FindItemByProperty** comienza la búsqueda con el primer elemento de la vista.

ItemsView admite las siguientes propiedades [**para FindItemByProperty**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationitemcontainerpattern-finditembyproperty):

-   Name (UIA NamePropertyId): busca el primer elemento \_ cuyo nombre coincide totalmente con la cadena especificada. La búsqueda no hace distinción de mayúsculas y minúsculas. No se admiten caracteres comodín ni coincidencia parcial. Si se **especifica** un nombre NULL, se devuelve el siguiente elemento después del elemento inicial. La **especificación de** nombres NULL permite a Automatización de la interfaz de usuario cliente enumerar todos los elementos de la vista; sin embargo, no se recomienda enumerar todos los elementos porque hace que todos los elementos de la vista se puedan realizar.
-   SelectionItem \_ IsSelected (UIA \_ SelectionItemIsSelectedPropertyId): busca el primer elemento cuya propiedad SelectionItem IsSelected coincida con \_ el valor especificado. Especifique **TRUE** para buscar el primer elemento seleccionado o **FALSE** para buscar el primer elemento no seleccionado. Tenga cuidado al enumerar todos los elementos seleccionados porque el número de elementos seleccionados puede ser muy grande, especialmente si el usuario ha seleccionado todos los elementos.

## <a name="scrolling-a-virtualized-item-on-screen"></a>Desplazamiento de un elemento virtualizado en pantalla

Después de obtener una referencia a un elemento Automatización de la interfaz de usuario para un elemento virtualizado (fuera de la pantalla), el cliente puede desplazar el elemento a la vista mediante el método [**IUIAutomationVirtualizeItemPattern::Realize**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationvirtualizeditempattern-realize) del patrón de control [VirtualizedItem.](uiauto-implementingvirtualizeditem.md) Una vez realizado el elemento, está visible y todas las propiedades y los patrones de control normalmente asociados a un elemento ListItem están disponibles para el cliente.

Solo los elementos ListItem obtenidos por el método [**IUIAutomationItemContainerPattern::FindItemByProperty**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationitemcontainerpattern-finditembyproperty) exponen el patrón de control [VirtualizedItem.](uiauto-implementingvirtualizeditem.md) Cuando un elemento en pantalla se desplaza fuera de la pantalla, el elemento deja de ser válido y el cliente debe llamar a **FindItemByProperty** para obtener la referencia fuera de pantalla.

También es posible mover elementos dentro y fuera de la vista mediante el patrón de control [Scroll](uiauto-implementingscroll.md) (o mediante las barras de desplazamiento). Los elementos y grupos se realizan a medida que se desplazan a la vista y se virtualizan a medida que se desplazan fuera de la vista.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con elementos virtualizados](uiauto-workingwithvirtualizeditems.md)
</dt> </dl>

 

 




