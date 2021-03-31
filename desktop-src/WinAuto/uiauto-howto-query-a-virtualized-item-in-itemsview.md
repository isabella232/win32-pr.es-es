---
title: Cómo consultar un elemento virtualizado en la vista de elementos
description: En este tema se describe cómo usar la automatización de la interfaz de usuario de Microsoft para recuperar información de la interfaz de usuario sobre elementos virtualizados en la vista de elementos de Windows 7.
ms.assetid: a0bff8a1-47b1-4750-8086-e2e65a79099e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a098635d6e1045c6ff4573de088d8455685014d3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419042"
---
# <a name="how-to-query-a-virtualized-item-in-items-view"></a>Cómo consultar un elemento virtualizado en la vista de elementos

En este tema se describe cómo usar la automatización de la interfaz de usuario de Microsoft para recuperar información de la interfaz de usuario sobre elementos virtualizados en la vista de elementos de Windows 7. En este tema se incluyen las secciones siguientes.

> [!Note]  
> Este tema solo se aplica a Windows 7. Tenga en cuenta que las características de accesibilidad descritas en este tema pueden cambiar en versiones futuras de Windows.

 

-   [Información general](#overview)
-   [Estructura de árbol de vista de elementos](#items-view-tree-structure)
-   [Virtualización](#virtualization)
-   [Obtener un recuento de todos los elementos](#obtaining-a-count-of-all-items)
-   [Obtener un índice de elemento con respecto a todos los elementos](#obtaining-an-item-index-with-respect-to-all-items)
-   [Obtener una referencia a un elemento Vitualized](#obtaining-a-reference-to-a-vitualized-item)
-   [Desplazar un elemento virtualizado en pantalla](#scrolling-a-virtualized-item-on-screen)
-   [Temas relacionados](#related-topics)

## <a name="overview"></a>Información general

La vista elementos es un componente de la interfaz de usuario que permite a los usuarios ver e interactuar con archivos y otros elementos. En Windows 7, la vista de elementos reemplaza el control de vista de lista para presentar los elementos en la vista predeterminada del explorador de Windows. La vista elementos también se usa en el cuadro de diálogo elemento común, en los resultados de búsqueda del menú Inicio y en otros elementos de la interfaz de usuario de Windows 7 que usan el control explorador del explorador. En comparación con el control de vista de lista, la vista de elementos ofrece las siguientes ventajas a los usuarios:

-   La vista de elementos puede presentar elementos de maneras más útiles, deseables y relevantes, lo que permite a los usuarios buscar y organizar los elementos de forma más sencilla, rápida y agradable.
-   La vista de elementos puede mostrar grandes conjuntos de elementos de orígenes de datos que tienen diferentes características de rendimiento, lo que permite a los usuarios examinar y buscar toda la colección de elementos en varios orígenes.

En la imagen siguiente se muestra la vista elementos del explorador de Windows.

![captura de pantalla que muestra el explorador de Windows con el componente de vista de elementos](images/itemsview.gif)

Desde la perspectiva del desarrollador, la estructura general y la funcionalidad de la vista de elementos es similar a la del control de vista de lista. La principal diferencia es que la vista de elementos admite la virtualización, mientras que el control de vista de lista no lo hace. Además, la vista de elementos usa dos nuevas interfaces de automatización de la interfaz de usuario para garantizar que el contenido virtualizado proporcionado por la vista de elementos sea accesible. Estas interfaces se describen en las siguientes secciones de este tema.

Para obtener información general sobre la virtualización en la automatización de la interfaz de usuario, consulte [trabajar con elementos virtualizados](uiauto-workingwithvirtualizeditems.md).

## <a name="items-view-tree-structure"></a>Estructura de árbol de vista de elementos

En el árbol de automatización de la interfaz de usuario, el elemento de automatización de la interfaz de usuario de nivel superior de la vista de elementos tiene el nombre "ItemsView" y el tipo de control "list". En la imagen anterior, el elemento de automatización de la interfaz de usuario de ItemsView se describe en rojo. Existen varios elementos de automatización de la interfaz de usuario bajo el nivel superior de ItemsView, pero se hace referencia a otros dos elementos de automatización de la interfaz de usuario en este documento: elementos de grupo y elementos de lista.

Los elementos de grupo son los elementos de automatización de la interfaz de usuario que contienen todos los elementos de lista de ese grupo; su tipo de control es "Group" y sus nombres varían según el nombre del grupo. En la imagen anterior, el primer elemento de grupo contiene el encabezado "A-H (1)" y el elemento de lista "carpeta", y su nombre es "A-H".

Los elementos de la lista son los elementos de automatización de la interfaz de usuario que representan los elementos hoja de la vista: su tipo de control es "ListItem" y sus nombres varían en función del nombre del elemento. En la imagen anterior, los elementos de la lista son los elementos hoja como "carpeta", "música" y "imagen". En el resto de este documento, se hace referencia a estos tres elementos de automatización de la interfaz de usuario.

## <a name="virtualization"></a>Virtualización

La vista de elementos utiliza la virtualización, lo que significa que los elementos que se encuentran fuera del área visible de la vista no se capturan del sistema y no se crea la representación de la interfaz de usuario. Estos elementos se denominan *elementos virtualizados*. Dado que no se crean, los elementos virtualizados no tienen elementos de automatización de la interfaz de usuario y, por tanto, no aparecen en el árbol de automatización de la interfaz de usuario cuando un cliente de automatización de la interfaz de usuario enumera el árbol. Además, los patrones de control de UI Automation solo funcionan en elementos visibles. Por ejemplo, el patrón de control [Selection](uiauto-implementingselection.md) devuelve solo los elementos seleccionados visibles cuando un cliente llama al método [**IUIAutomationSelectionPattern:: método getcurrentselection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionpattern-getcurrentselection) .

La vista de elementos admite la capacidad de recuperar la siguiente información acerca de los elementos virtualizados:

-   Un recuento del número total de elementos, incluidos los elementos virtualizados
-   Elementos de UI Automation para elementos virtualizados
-   Elementos de automatización de la interfaz de usuario para los elementos virtualizados seleccionados

## <a name="obtaining-a-count-of-all-items"></a>Obtener un recuento de todos los elementos

Un cliente puede utilizar el elemento ItemsView para obtener un recuento de todos los elementos, así como un recuento de los elementos seleccionados. El elemento ItemsView proporciona dos maneras de obtener estos recuentos. Lo primero es obtener la propiedad ItemStatus del elemento ItemsView y el segundo es obteniendo propiedades personalizadas del elemento ItemsView.

La propiedad ItemStatus es una cadena que especifica el recuento del número total de elementos y un recuento de los elementos seleccionados, separados por una coma. Por ejemplo: "3 elementos, 1 elemento seleccionado". Esta cadena está localizada y se puede comunicar directamente al usuario.

Las propiedades personalizadas del elemento ItemsView incluyen una propiedad para el recuento de elementos y otra para el recuento de selección. Incluyen:

-   \_Propiedad ItemCount \_ GUID (ABBF5C45-5CCC-47b7-BB4E-87CB87BBD162): recuento de todos los elementos únicos de la vista. Si se agrupa por una propiedad de varios valores (MVP) para que un único elemento pueda aparecer varias veces, cada elemento se cuenta una sola vez.

    (UIAutomationType: [**UIAutomationType \_ int**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-uiautomationtype), nombre de programación: "ItemCount")

-   \_GUID de la propiedad SelectedItemCount \_ (92A053DA-2969-4021-BF27-514CFC2E4A69): el recuento de todos los elementos únicos seleccionados en la vista. Si se agrupa por una propiedad de varios valores (MVP) para que un único elemento pueda aparecer varias veces, cada elemento se cuenta una sola vez.

    (UIAutomationType: [**UIAutomationType \_ int**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-uiautomationtype), nombre de programación: "SelectedItemCount")

Estas propiedades personalizadas se definen en Shlguid. h, que se incluye en el kit de desarrollo de software (SDK) de Windows, y estas propiedades se registran a través del método [**IUIAutomationRegistrar:: RegisterProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) . Los clientes de automatización de la interfaz de usuario usan **RegisterProperty** para recuperar los identificadores de propiedad (identificadores) de las propiedades personalizadas.

## <a name="obtaining-an-item-index-with-respect-to-all-items"></a>Obtener un índice de elemento con respecto a todos los elementos

Un cliente puede obtener el índice de un elemento obteniendo la propiedad ItemStatus de un elemento ListItem o obteniendo una propiedad personalizada de un elemento ListItem.

La propiedad ItemStatus es una cadena que contiene el índice de un elemento con respecto al número total de elementos. Por ejemplo: "elemento 1 de 3". Esta cadena está localizada y se puede comunicar directamente al usuario.

La siguiente propiedad personalizada obtiene el índice de elemento de un elemento ListItem:

-   \_Propiedad ItemIndex \_ (GUID) (92A053DA-2969-4021-BF27-514CFC2E4A69): el índice absoluto basado en 1 de un elemento. Si se agrupa por una propiedad de varios valores (MVP) para que un único elemento pueda aparecer dos veces, cada aspecto del elemento obtiene un índice independiente.

    (UIAutomationType: [**UIAutomationType \_ int**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-uiautomationtype), nombre de programación: "ItemIndex")

Esta propiedad personalizada se define en Shlguid. h, que se incluye en el Windows SDK y se registra a través del método [**IUIAutomationRegistrar:: RegisterProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) . Los clientes de automatización de la interfaz de usuario usan **RegisterProperty** para recuperar un identificador de propiedad (identificadores) para la propiedad personalizada.

## <a name="obtaining-a-reference-to-a-vitualized-item"></a>Obtener una referencia a un elemento Vitualized

Un elemento ItemsView implementa el patrón de control [ItemContainer](uiauto-implementingitemcontainer.md) (interfaz [**IItemContainerProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iitemcontainerprovider) ), que permite a un cliente obtener un elemento de automatización de la interfaz de usuario para un elemento virtualizado (un elemento que está fuera del área visible). ItemsView permite al cliente buscar un elemento ListItem buscando en el nombre y en las propiedades de selección. Si intenta buscar en cualquier otra propiedad, se producirá un error.

Un elemento virtual solo implementa el patrón de control [VirtualizedItem](uiauto-implementingvirtualizeditem.md) (interfaz [**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider) ). Dado que el elemento representado por un elemento de automatización de la interfaz de usuario virtualizado no existe todavía, se producirá un error al intentar obtener cualquier otro patrón de control o propiedad del elemento.

Los elementos ListItem y Group están virtualizados, pero solo los elementos ListItem pueden devolverse desde el patrón de control [ItemContainer](uiauto-implementingitemcontainer.md) . Dado que la llamada al método [**IUIAutomationItemContainerPattern:: FindItemByProperty**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationitemcontainerpattern-finditembyproperty) se ejecuta en el subproceso de la interfaz de usuario y está bloqueando, la vista no responderá hasta que se devuelva **FindItemByProperty** y cualquier otra llamada al método en el proveedor debe esperar hasta que finalice **FindItemByProperty** . En algunos casos, **FindItemByProperty** debe procesar todo el conjunto de datos antes de devolverse, lo que puede consumir muchos recursos. Si se especifica **null** como el elemento de inicio, **FindItemByProperty** inicia la búsqueda con el primer elemento de la vista.

ItemsView admite las siguientes propiedades para [**FindItemByProperty**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationitemcontainerpattern-finditembyproperty):

-   Nombre (UIA \_ NamePropertyId): busca el primer elemento cuyo nombre coincide con la cadena especificada. La búsqueda no hace distinción de mayúsculas y minúsculas. No se admiten caracteres comodín o coincidencias parciales. Si se especifica un nombre **null** , se devuelve el elemento siguiente después del elemento de inicio. Si se especifican nombres **null** , se permite que un cliente de automatización de la interfaz de usuario Enumere todos los elementos de la vista. sin embargo, no se recomienda enumerar todos los elementos porque hace que se produzcan todos los elementos de la vista.
-   SelectionItem \_ IsSelected (UIA \_ SelectionItemIsSelectedPropertyId): busca el primer elemento cuya \_ propiedad IsSelected SelectionItem coincida con el valor especificado. Especifique **true** para buscar el primer elemento seleccionado o **false** para buscar el primer elemento no seleccionado. Tenga cuidado al enumerar todos los elementos seleccionados porque el número de elementos seleccionados puede ser muy grande, especialmente si el usuario ha seleccionado todos los elementos.

## <a name="scrolling-a-virtualized-item-on-screen"></a>Desplazar un elemento virtualizado en pantalla

Después de obtener una referencia a un elemento de automatización de la interfaz de usuario para un elemento virtualizado (fuera de la pantalla), el cliente puede desplazar el elemento a la vista mediante el método [**IUIAutomationVirtualizeItemPattern::**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationvirtualizeditempattern-realize) acview del patrón de control [VirtualizedItem](uiauto-implementingvirtualizeditem.md) . Una vez realizado el elemento, es visible y todas las propiedades y los patrones de control asociados normalmente a un elemento ListItem están disponibles para el cliente.

Solo los elementos ListItem obtenidos por el método [**IUIAutomationItemContainerPattern:: FindItemByProperty**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationitemcontainerpattern-finditembyproperty) exponen el patrón de control [VirtualizedItem](uiauto-implementingvirtualizeditem.md) . Cuando un elemento en pantalla se desplaza fuera de la pantalla, el elemento deja de ser válido y el cliente debe llamar a **FindItemByProperty** para obtener la referencia fuera de pantalla.

También es posible desplazar elementos dentro y fuera de la vista mediante el patrón de control [Scroll](uiauto-implementingscroll.md) (o mediante las barras de desplazamiento). Los elementos y los grupos se llevan a cabo a medida que se desplazan a la vista y se virtualizan cuando se desplazan fuera de la vista.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con elementos virtualizados](uiauto-workingwithvirtualizeditems.md)
</dt> </dl>

 

 




