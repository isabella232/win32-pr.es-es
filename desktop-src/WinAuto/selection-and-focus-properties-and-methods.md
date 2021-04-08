---
title: Propiedades y métodos de selección y foco
description: Al igual que muchos elementos de las aplicaciones que se ejecutan en los sistemas operativos Microsoft Windows, los objetos accesibles seleccionan y reciben el foco de teclado. Estos atributos permiten a los usuarios interactuar con los elementos de la aplicación, cambiar los valores y manipularlos de otro modo.
ms.assetid: 8170fe19-f157-4d7d-8eec-d384e51f1560
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bbb5eee361707ec4876245eef5b0eb352f8dfd6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792472"
---
# <a name="selection-and-focus-properties-and-methods"></a>Propiedades y métodos de selección y foco

Al igual que muchos elementos de las aplicaciones que se ejecutan en los sistemas operativos Microsoft Windows, los objetos accesibles *seleccionan* y reciben el *foco* de teclado. Estos atributos permiten a los usuarios interactuar con los elementos de la aplicación, cambiar los valores y manipularlos de otro modo.

Hay algunas diferencias importantes entre la selección de objetos y el foco de objetos:

-   Un objeto enfocado es el objeto en todo el sistema operativo que recibe la entrada del teclado. El objeto que tiene el foco de teclado es la ventana activa o un objeto secundario de la ventana activa.
-   Un objeto seleccionado se marca para participar en algún tipo de operación de grupo.

Por ejemplo, un usuario puede seleccionar varios elementos en un control de vista de lista, pero el foco solo se proporciona a un objeto del sistema a la vez. Tenga en cuenta que los elementos con foco provienen de una selección de elementos.

Los clientes determinan si un determinado objeto accesible o elemento secundario tiene el foco llamando a [**IAccessible:: get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus). Los clientes determinan si un objeto está seleccionado o qué elementos secundarios dentro de un objeto accesible están seleccionados, llamando a [**IAccessible:: get \_ accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection). En el caso de objetos como los controles de vista de lista en los que hay más de un elemento secundario seleccionado, el objeto primario debe admitir la interfaz [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) , que permite a los clientes enumerar los elementos secundarios seleccionados.

## <a name="events-triggered-in-menus"></a>Eventos desencadenados en menús

Microsoft Active Accessibility expone menús estándar creados con las API de menú de Microsoft Win32 y archivos de recursos. Para ser coherente con los menús estándar, los servidores con menús personalizados desencadenan el [**\_ \_ foco del objeto de evento**](event-constants.md), no la [**\_ \_ selección de objetos de eventos**](event-constants.md), cuando un usuario resalta un elemento de menú.

> [!Note]  
> Microsoft Active Accessibility no admite la selección del texto contenido en los controles de edición y edición enriquecida porque el texto se expone como una sola cadena en la propiedad [**Value**](value-property.md) de estos controles.

 

## <a name="in-this-section"></a>En esta sección

-   [Seleccionar objetos secundarios](selecting-child-objects.md)

 

 