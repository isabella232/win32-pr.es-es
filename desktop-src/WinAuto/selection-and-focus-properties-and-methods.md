---
title: Métodos y propiedades de selección y foco
description: Al igual que muchos elementos de las aplicaciones que se ejecutan en Microsoft Windows sistemas operativos, los objetos accesibles seleccionan y reciben el foco del teclado. Estos atributos permiten a los usuarios interactuar con elementos de la aplicación, cambiar valores y manipularlos de otro modo.
ms.assetid: 8170fe19-f157-4d7d-8eec-d384e51f1560
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bbb5eee361707ec4876245eef5b0eb352f8dfd6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567381"
---
# <a name="selection-and-focus-properties-and-methods"></a>Métodos y propiedades de selección y foco

Al igual que muchos elementos de las aplicaciones que se ejecutan en Microsoft Windows sistemas operativos, los objetos accesibles *seleccionan* y reciben el foco de *teclado*. Estos atributos permiten a los usuarios interactuar con elementos de la aplicación, cambiar valores y manipularlos de otro modo.

Hay algunas diferencias clave entre la selección de objetos y el foco de objetos:

-   Un objeto centrado es el único objeto de todo el sistema operativo que recibe la entrada de teclado. El objeto con el foco del teclado es la ventana activa o un objeto secundario de la ventana activa.
-   Un objeto seleccionado se marca para participar en algún tipo de operación de grupo.

Por ejemplo, un usuario puede seleccionar varios elementos en un control de vista de lista, pero el foco solo se da a un objeto del sistema a la vez. Tenga en cuenta que los elementos centrados son de una selección de elementos.

Los clientes determinan si un objeto o elemento secundario accesible determinado tiene el foco mediante una llamada a [**IAccessible::get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus). Los clientes determinan si se selecciona un objeto o qué elementos secundarios dentro de un objeto accesible se seleccionan mediante una llamada a [**IAccessible::get \_ accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection). Para objetos como los controles de vista de lista en los que se selecciona más de un elemento secundario, el objeto primario debe admitir la interfaz [IEnumVARIANT,](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) que permite a los clientes enumerar los elementos secundarios seleccionados.

## <a name="events-triggered-in-menus"></a>Eventos desencadenados en menús

Microsoft Active Accessibility muestra los menús estándar creados con las API de menú y los archivos de recursos de Microsoft Win32. Para ser coherentes con los menús estándar, los servidores con menús personalizados desencadenan [**EVENT \_ OBJECT \_ FOCUS**](event-constants.md), no [**EVENT OBJECT \_ \_ SELECTION**](event-constants.md), cuando un usuario resalta un elemento de menú.

> [!Note]  
> Microsoft Active Accessibility no admite la selección del texto incluido en los controles de edición y edición enriquezca porque el texto se expone como una sola cadena en la propiedad [**Value**](value-property.md) de estos controles.

 

## <a name="in-this-section"></a>En esta sección

-   [Selección de objetos secundarios](selecting-child-objects.md)

 

 