---
title: Usar anotación de asignación de valores
description: Para ver el código de ejemplo, consulte ejemplo de anotación de asignación de valores.
ms.assetid: 29be74c7-a7c2-41f4-8b94-5771988b74ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3a3e8d003d863372e21a413fad56bc93b977ee3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420769"
---
# <a name="using-value-map-annotation"></a><span data-ttu-id="12463-103">Usar anotación de asignación de valores</span><span class="sxs-lookup"><span data-stu-id="12463-103">Using Value Map Annotation</span></span>

<span data-ttu-id="12463-104">**Para crear un mapa de valores**</span><span class="sxs-lookup"><span data-stu-id="12463-104">**To create a value map**</span></span>

1.  <span data-ttu-id="12463-105">**Cree una cadena de asignación.**</span><span class="sxs-lookup"><span data-stu-id="12463-105">**Create a mapping string.**</span></span>

    <span data-ttu-id="12463-106">Una cadena de asignación es una lista de valores numéricos de un control que corresponden a una cadena legible en Unicode.</span><span class="sxs-lookup"><span data-stu-id="12463-106">A mapping string is a list of a control's numeric values corresponding to a human-readable string in Unicode.</span></span> <span data-ttu-id="12463-107">Comienza por "A:" seguido de un número que indica el tipo de índice utilizado.</span><span class="sxs-lookup"><span data-stu-id="12463-107">It starts with "A:" followed by a number that indicates the type of index used.</span></span> <span data-ttu-id="12463-108">Solo se admiten índices de imagen; por lo tanto, el tipo de índice es siempre 0.</span><span class="sxs-lookup"><span data-stu-id="12463-108">Only image indexes are supported; therefore the index type is always 0.</span></span>

    <span data-ttu-id="12463-109">La cadena va seguida de los pares: index: result.</span><span class="sxs-lookup"><span data-stu-id="12463-109">The string is followed by :index:result pairs.</span></span> <span data-ttu-id="12463-110">El "índice" es un número que representa un índice de imagen para un List-View o vista de árbol, o el valor de un control deslizante.</span><span class="sxs-lookup"><span data-stu-id="12463-110">The "index" is a number representing an image index for a List-View or Tree-View, or the value for a slider control.</span></span>

    <span data-ttu-id="12463-111">El valor resultante es un número obtenido al asignar la propiedad role o State para una vista de lista o un control de vista de árbol.</span><span class="sxs-lookup"><span data-stu-id="12463-111">The resulting value is a number obtained when you map the Role or State property for a list view or tree view control.</span></span> <span data-ttu-id="12463-112">Estos números se expresan en formato decimal o hexadecimal con un prefijo "0x".</span><span class="sxs-lookup"><span data-stu-id="12463-112">Such numbers are expressed in decimal or hexadecimal with an "0x" prefix.</span></span>

    <span data-ttu-id="12463-113">La cadena de asignación siempre termina con un signo de dos puntos (":").</span><span class="sxs-lookup"><span data-stu-id="12463-113">The mapping string is always terminated with a final colon (":").</span></span>

    <span data-ttu-id="12463-114">A continuación se muestra un ejemplo de una asignación de anotación para las propiedades de estado y de rol de una casilla en una vista de lista o un control de vista de árbol.</span><span class="sxs-lookup"><span data-stu-id="12463-114">The following is an example of an annotation map for the State and Role properties of a check box in a list view or tree view control.</span></span> <span data-ttu-id="12463-115">Hay dos elementos en la vista que representan casillas, y cada uno tiene imágenes correspondientes al estado Checked y Unchecked.</span><span class="sxs-lookup"><span data-stu-id="12463-115">There are two items in the view that represent check boxes, and each has images corresponding to the checked and unchecked state.</span></span>

    ```C++
    LPCWSTR g_ListOrTreeStateMap = 
    L"A:0"     // Index type; always 0. !
    L":0:0x00" // Image 0 is normal !
    L":1:0x10" // Image 1 is checked - STATE_SYSTEM_CHECKED (0x10) !
    L":";

    LPCWSTR g_ListOrTreeRoleMap = 
    L"A:0"     // Index type; always 0. !
    L":0:0x2C" // Image 0 is a check box - ROLE_SYSTEM_CHECKBUTTON
    (0x2c) !
    L":1:0x2C" // image 1 is also a check box !
    L":";
    ```

    

    <span data-ttu-id="12463-116">Para los valores de rol y estado válidos, vea [funciones de objeto](object-roles.md) y [constantes de estado de objeto](object-state-constants.md).</span><span class="sxs-lookup"><span data-stu-id="12463-116">For valid Role and State values, see [Object Roles](object-roles.md) and [Object State Constants](object-state-constants.md).</span></span>

    <span data-ttu-id="12463-117">El valor de índice puede ser negativo cuando se asignan propiedades para un control deslizante.</span><span class="sxs-lookup"><span data-stu-id="12463-117">The index value may be negative when you map properties for a slider control.</span></span>

    <span data-ttu-id="12463-118">Cuando se asigna una propiedad Value o Description, el resultado es una cadena.</span><span class="sxs-lookup"><span data-stu-id="12463-118">When you map a Value or Description property, the result is a string.</span></span> <span data-ttu-id="12463-119">Las cadenas no se incluyen entre comillas y los dos puntos actúan como delimitadores.</span><span class="sxs-lookup"><span data-stu-id="12463-119">Strings are not quoted and the colons act as delimiters.</span></span>

    <span data-ttu-id="12463-120">Para obtener más información, vea [formato de asignación de anotaciones](value-map-annotation.md).</span><span class="sxs-lookup"><span data-stu-id="12463-120">For more information, see [Annotation Map Format](value-map-annotation.md).</span></span>

2.  <span data-ttu-id="12463-121">**Cree el administrador de anotaciones y obtenga un puntero a su** interfaz [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices)**.**</span><span class="sxs-lookup"><span data-stu-id="12463-121">**Create the annotation manager and obtain a pointer to its**[**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices)**interface.**</span></span>

    <span data-ttu-id="12463-122">El siguiente es un ejemplo de cómo crear el administrador de anotaciones.</span><span class="sxs-lookup"><span data-stu-id="12463-122">The following is an example of how to create the annotation manager.</span></span>

    ```C++
    IAccPropServices * pAccPropSvc = NULL;
    HRESULT hr = CoCreateInstance(CLSID_AccPropServices, NULL,
    CLSCTX_SERVER, IID_IAccPropServices, (void**) & pAccPropSvc));
    
    ```

    

3.  <span data-ttu-id="12463-123">**Adjunte la cadena de asignación al control.**</span><span class="sxs-lookup"><span data-stu-id="12463-123">**Attach the mapping string to the control.**</span></span>

    <span data-ttu-id="12463-124">Llame a [**IAccPropServices:: SetHwndPropStr**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr), pasando el **hWnd** del control y un puntero a la cadena de asignación.</span><span class="sxs-lookup"><span data-stu-id="12463-124">Call [**IAccPropServices::SetHwndPropStr**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr), passing the **HWND** of the control and a pointer to the mapping string.</span></span>

    <span data-ttu-id="12463-125">El parámetro *IdProp* será uno de los siguientes.</span><span class="sxs-lookup"><span data-stu-id="12463-125">The *IdProp* parameter will be one of the following.</span></span>

    

    | <span data-ttu-id="12463-126">Parámetro</span><span class="sxs-lookup"><span data-stu-id="12463-126">Parameter</span></span>                   | <span data-ttu-id="12463-127">Se usa para</span><span class="sxs-lookup"><span data-stu-id="12463-127">Used for</span></span>                                                |
    |-----------------------------|---------------------------------------------------------|
    | <span data-ttu-id="12463-128">MSAAPROPID \_ ROLEMAP</span><span class="sxs-lookup"><span data-stu-id="12463-128">MSAAPROPID\_ROLEMAP</span></span>         | <span data-ttu-id="12463-129">Para establecer un mapa de roles para los controles de vista de lista o de vista de árbol.</span><span class="sxs-lookup"><span data-stu-id="12463-129">To set a role map for list view or tree view controls.</span></span>  |
    | <span data-ttu-id="12463-130">MSAAPROPID \_ STATEMAP</span><span class="sxs-lookup"><span data-stu-id="12463-130">MSAAPROPID\_STATEMAP</span></span>        | <span data-ttu-id="12463-131">Para establecer un mapa de estado para los controles de vista de lista o de vista de árbol.</span><span class="sxs-lookup"><span data-stu-id="12463-131">To set a state map for list view or tree view controls.</span></span> |
    | <span data-ttu-id="12463-132">DESCRIPTIONMAP de la \_ ACC \_</span><span class="sxs-lookup"><span data-stu-id="12463-132">PROPID\_ACC\_DESCRIPTIONMAP</span></span> | <span data-ttu-id="12463-133">Para establecer un mapa de descripción para las vistas de lista o de árbol.</span><span class="sxs-lookup"><span data-stu-id="12463-133">To set a description map for list view or tree views.</span></span>   |
    | <span data-ttu-id="12463-134">MSAAPROPID \_ VALUEMAP</span><span class="sxs-lookup"><span data-stu-id="12463-134">MSAAPROPID\_VALUEMAP</span></span>        | <span data-ttu-id="12463-135">Para establecer un mapa de valores en los controles deslizantes.</span><span class="sxs-lookup"><span data-stu-id="12463-135">To set a value map on slider controls.</span></span>                  |

    

     

4.  <span data-ttu-id="12463-136">**Limpieza.**</span><span class="sxs-lookup"><span data-stu-id="12463-136">**Clean up.**</span></span>

    <span data-ttu-id="12463-137">Antes de destruir los controles anotados de asignación de valores (por ejemplo, al controlar [WM \_ Destroy](../winmsg/wm-destroy.md)), debe borrar las propiedades registradas anteriormente y liberar el administrador de anotaciones.</span><span class="sxs-lookup"><span data-stu-id="12463-137">Before you destroy any value map annotated controls (for example, when handling [WM\_DESTROY](../winmsg/wm-destroy.md)), you must clear previously registered properties and release the annotation manager.</span></span>

    <span data-ttu-id="12463-138">Para ello, llame a [**IAccPropServices:: ClearHwndProps**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-clearhwndprops) según corresponda y suelte el puntero a [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices).</span><span class="sxs-lookup"><span data-stu-id="12463-138">To do this, call [**IAccPropServices::ClearHwndProps**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-clearhwndprops) as appropriate and release your pointer to [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices).</span></span>

<span data-ttu-id="12463-139">Para ver el código de ejemplo, consulte [ejemplo de anotación de asignación de valores](value-map-annotation-sample.md).</span><span class="sxs-lookup"><span data-stu-id="12463-139">For sample code, see [Value Map Annotation Sample](value-map-annotation-sample.md).</span></span>

 

 