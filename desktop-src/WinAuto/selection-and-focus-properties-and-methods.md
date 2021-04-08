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
# <a name="selection-and-focus-properties-and-methods"></a><span data-ttu-id="e2800-104">Propiedades y métodos de selección y foco</span><span class="sxs-lookup"><span data-stu-id="e2800-104">Selection and Focus Properties and Methods</span></span>

<span data-ttu-id="e2800-105">Al igual que muchos elementos de las aplicaciones que se ejecutan en los sistemas operativos Microsoft Windows, los objetos accesibles *seleccionan* y reciben el *foco* de teclado.</span><span class="sxs-lookup"><span data-stu-id="e2800-105">Like many elements in applications running on Microsoft Windows operating systems, accessible objects *select* and receive keyboard *focus*.</span></span> <span data-ttu-id="e2800-106">Estos atributos permiten a los usuarios interactuar con los elementos de la aplicación, cambiar los valores y manipularlos de otro modo.</span><span class="sxs-lookup"><span data-stu-id="e2800-106">These attributes enable users to interact with application elements, change values, and otherwise manipulate them.</span></span>

<span data-ttu-id="e2800-107">Hay algunas diferencias importantes entre la selección de objetos y el foco de objetos:</span><span class="sxs-lookup"><span data-stu-id="e2800-107">There are some key differences between object selection and object focus:</span></span>

-   <span data-ttu-id="e2800-108">Un objeto enfocado es el objeto en todo el sistema operativo que recibe la entrada del teclado.</span><span class="sxs-lookup"><span data-stu-id="e2800-108">A focused object is the one object in the entire operating system that receives keyboard input.</span></span> <span data-ttu-id="e2800-109">El objeto que tiene el foco de teclado es la ventana activa o un objeto secundario de la ventana activa.</span><span class="sxs-lookup"><span data-stu-id="e2800-109">The object with the keyboard focus is either the active window or a child object of the active window.</span></span>
-   <span data-ttu-id="e2800-110">Un objeto seleccionado se marca para participar en algún tipo de operación de grupo.</span><span class="sxs-lookup"><span data-stu-id="e2800-110">A selected object is marked to participate in some type of group operation.</span></span>

<span data-ttu-id="e2800-111">Por ejemplo, un usuario puede seleccionar varios elementos en un control de vista de lista, pero el foco solo se proporciona a un objeto del sistema a la vez.</span><span class="sxs-lookup"><span data-stu-id="e2800-111">For example, a user can select several items in a list-view control, but the focus is given only to one object in the system at a time.</span></span> <span data-ttu-id="e2800-112">Tenga en cuenta que los elementos con foco provienen de una selección de elementos.</span><span class="sxs-lookup"><span data-stu-id="e2800-112">Note that focused items are from a selection of items.</span></span>

<span data-ttu-id="e2800-113">Los clientes determinan si un determinado objeto accesible o elemento secundario tiene el foco llamando a [**IAccessible:: get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus).</span><span class="sxs-lookup"><span data-stu-id="e2800-113">Clients determine whether a particular accessible object or child element has the focus by calling [**IAccessible::get\_accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus).</span></span> <span data-ttu-id="e2800-114">Los clientes determinan si un objeto está seleccionado o qué elementos secundarios dentro de un objeto accesible están seleccionados, llamando a [**IAccessible:: get \_ accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection).</span><span class="sxs-lookup"><span data-stu-id="e2800-114">Clients determine whether an object is selected, or which children within an accessible object are selected, by calling [**IAccessible::get\_accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection).</span></span> <span data-ttu-id="e2800-115">En el caso de objetos como los controles de vista de lista en los que hay más de un elemento secundario seleccionado, el objeto primario debe admitir la interfaz [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) , que permite a los clientes enumerar los elementos secundarios seleccionados.</span><span class="sxs-lookup"><span data-stu-id="e2800-115">For objects such as list-view controls in which more than one child is selected, the parent object must support the [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface, which allows clients to enumerate the selected children.</span></span>

## <a name="events-triggered-in-menus"></a><span data-ttu-id="e2800-116">Eventos desencadenados en menús</span><span class="sxs-lookup"><span data-stu-id="e2800-116">Events Triggered in Menus</span></span>

<span data-ttu-id="e2800-117">Microsoft Active Accessibility expone menús estándar creados con las API de menú de Microsoft Win32 y archivos de recursos.</span><span class="sxs-lookup"><span data-stu-id="e2800-117">Microsoft Active Accessibility exposes standard menus created with the Microsoft Win32 menu APIs and resource files.</span></span> <span data-ttu-id="e2800-118">Para ser coherente con los menús estándar, los servidores con menús personalizados desencadenan el [**\_ \_ foco del objeto de evento**](event-constants.md), no la [**\_ \_ selección de objetos de eventos**](event-constants.md), cuando un usuario resalta un elemento de menú.</span><span class="sxs-lookup"><span data-stu-id="e2800-118">To be consistent with standard menus, servers with custom menus trigger [**EVENT\_OBJECT\_FOCUS**](event-constants.md), not [**EVENT\_OBJECT\_SELECTION**](event-constants.md), when a user highlights a menu item.</span></span>

> [!Note]  
> <span data-ttu-id="e2800-119">Microsoft Active Accessibility no admite la selección del texto contenido en los controles de edición y edición enriquecida porque el texto se expone como una sola cadena en la propiedad [**Value**](value-property.md) de estos controles.</span><span class="sxs-lookup"><span data-stu-id="e2800-119">Microsoft Active Accessibility does not support the selection of the text contained in edit and rich edit controls because the text is exposed as a single string in the [**Value**](value-property.md) property for these controls.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="e2800-120">En esta sección</span><span class="sxs-lookup"><span data-stu-id="e2800-120">In this section</span></span>

-   [<span data-ttu-id="e2800-121">Seleccionar objetos secundarios</span><span class="sxs-lookup"><span data-stu-id="e2800-121">Selecting Child Objects</span></span>](selecting-child-objects.md)

 

 