---
title: MENUITEM (instrucción)
description: Define un elemento de menú.
ms.assetid: b154211a-5267-4dcf-9e70-ac36671d10d3
keywords:
- Menús de instrucciones MENUITEM y otros recursos
topic_type:
- apiref
api_name:
- MENUITEM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da2051b326b2f2f37c9e24e03bcb5e5116cf290a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105665763"
---
# <a name="menuitem-statement"></a><span data-ttu-id="81357-104">MENUITEM (instrucción)</span><span class="sxs-lookup"><span data-stu-id="81357-104">MENUITEM statement</span></span>

<span data-ttu-id="81357-105">Define un elemento de menú.</span><span class="sxs-lookup"><span data-stu-id="81357-105">Defines a menu item.</span></span>

``` syntax
MENUITEM text, result, [optionlist]  
MENUITEM SEPARATOR
```

<dl> <dt>

<span data-ttu-id="81357-106"><span id="text"></span><span id="TEXT"></span>*negrita*</span><span class="sxs-lookup"><span data-stu-id="81357-106"><span id="text"></span><span id="TEXT"></span>*text*</span></span>
</dt> <dd>

<span data-ttu-id="81357-107">Nombre del elemento de menú.</span><span class="sxs-lookup"><span data-stu-id="81357-107">The name of the menu item.</span></span>

<span data-ttu-id="81357-108">La cadena puede contener los caracteres de escape **\\ t** y **\\ a**.</span><span class="sxs-lookup"><span data-stu-id="81357-108">The string can contain the escape characters **\\t** and **\\a**.</span></span> <span data-ttu-id="81357-109">El carácter **\\ t** inserta una tabulación en la cadena y se usa para alinear el texto en las columnas.</span><span class="sxs-lookup"><span data-stu-id="81357-109">The **\\t** character inserts a tab in the string and is used to align text in columns.</span></span> <span data-ttu-id="81357-110">Los caracteres de tabulación solo se deben usar en menús, no en barras de menús.</span><span class="sxs-lookup"><span data-stu-id="81357-110">Tab characters should be used only in menus, not in menu bars.</span></span> <span data-ttu-id="81357-111">(Para obtener información sobre los menús, vea [**elemento popup**](popup-resource.md)). El carácter **\\ a** alinea todo el texto que sigue a su derecha en la barra de menús o en el menú emergente.</span><span class="sxs-lookup"><span data-stu-id="81357-111">(For information on menus, see [**POPUP Resource**](popup-resource.md).) The **\\a** character aligns all text that follows it flush right to the menu bar or pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="81357-112"><span id="result"></span><span id="RESULT"></span>*da*</span><span class="sxs-lookup"><span data-stu-id="81357-112"><span id="result"></span><span id="RESULT"></span>*result*</span></span>
</dt> <dd>

<span data-ttu-id="81357-113">Número que especifica el resultado generado cuando el usuario selecciona el elemento de menú.</span><span class="sxs-lookup"><span data-stu-id="81357-113">A number that specifies the result generated when the user selects the menu item.</span></span> <span data-ttu-id="81357-114">Este parámetro toma un valor entero.</span><span class="sxs-lookup"><span data-stu-id="81357-114">This parameter takes an integer value.</span></span> <span data-ttu-id="81357-115">Los resultados de los elementos de menú siempre son enteros; Cuando el usuario hace clic en el nombre del elemento de menú, el resultado se envía a la ventana que posee el menú.</span><span class="sxs-lookup"><span data-stu-id="81357-115">Menu-item results are always integers; when the user clicks the menu-item name, the result is sent to the window that owns the menu.</span></span>

</dd> <dt>

<span data-ttu-id="81357-116"><span id="optionlist"></span><span id="OPTIONLIST"></span>*optionlist*</span><span class="sxs-lookup"><span data-stu-id="81357-116"><span id="optionlist"></span><span id="OPTIONLIST"></span>*optionlist*</span></span>
</dt> <dd>

<span data-ttu-id="81357-117">Apariencia del elemento de menú.</span><span class="sxs-lookup"><span data-stu-id="81357-117">The appearance of the menu item.</span></span> <span data-ttu-id="81357-118">Este parámetro opcional toma una o varias de las siguientes opciones de menú redefinidas, separadas por comas o espacios.</span><span class="sxs-lookup"><span data-stu-id="81357-118">This optional parameter takes one or more of the following redefined menu options, separated by commas or spaces.</span></span>



| <span data-ttu-id="81357-119">Opción</span><span class="sxs-lookup"><span data-stu-id="81357-119">Option</span></span>           | <span data-ttu-id="81357-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="81357-120">Description</span></span>                                                                                                                                                           |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81357-121">**INCORPORA**</span><span class="sxs-lookup"><span data-stu-id="81357-121">**CHECKED**</span></span>      | <span data-ttu-id="81357-122">El elemento de menú tiene una marca de verificación junto a él.</span><span class="sxs-lookup"><span data-stu-id="81357-122">Menu item has a check mark next to it.</span></span>                                                                                                                                |
| <span data-ttu-id="81357-123">**ATENUADO**</span><span class="sxs-lookup"><span data-stu-id="81357-123">**GRAYED**</span></span>       | <span data-ttu-id="81357-124">El elemento de menú está inicialmente inactivo y aparece en el menú en gris o en una sombra iluminada del color del texto de menú.</span><span class="sxs-lookup"><span data-stu-id="81357-124">Menu item is initially inactive and appears on the menu in gray or a lightened shade of the menu-text color.</span></span> <span data-ttu-id="81357-125">Esta opción no se puede usar con la opción **inactiva** .</span><span class="sxs-lookup"><span data-stu-id="81357-125">This option cannot be used with the **INACTIVE** option.</span></span> |
| <span data-ttu-id="81357-126">**Ayuda**</span><span class="sxs-lookup"><span data-stu-id="81357-126">**HELP**</span></span>         | <span data-ttu-id="81357-127">Identifica un elemento de ayuda.</span><span class="sxs-lookup"><span data-stu-id="81357-127">Identifies a help item.</span></span> <span data-ttu-id="81357-128">Esta opción no tiene ningún efecto en la apariencia del elemento de menú.</span><span class="sxs-lookup"><span data-stu-id="81357-128">This option has no effect on the appearance of the menu item.</span></span>                                                                                 |
| <span data-ttu-id="81357-129">**INACTIVA**</span><span class="sxs-lookup"><span data-stu-id="81357-129">**INACTIVE**</span></span>     | <span data-ttu-id="81357-130">Se muestra el elemento de menú, pero no se puede seleccionar.</span><span class="sxs-lookup"><span data-stu-id="81357-130">Menu item is displayed but it cannot be selected.</span></span> <span data-ttu-id="81357-131">Esta opción no se puede usar con la opción **atenuada** .</span><span class="sxs-lookup"><span data-stu-id="81357-131">This option cannot be used with the **GRAYED** option.</span></span>                                                              |
| <span data-ttu-id="81357-132">**MENUBARBREAK**</span><span class="sxs-lookup"><span data-stu-id="81357-132">**MENUBARBREAK**</span></span> | <span data-ttu-id="81357-133">Igual que **MENUBREAK** , excepto en el caso de los menús emergentes, separa la nueva columna de la antigua con una línea vertical.</span><span class="sxs-lookup"><span data-stu-id="81357-133">Same as **MENUBREAK** except that for pop-up menus, it separates the new column from the old column with a vertical line.</span></span>                                             |
| <span data-ttu-id="81357-134">**MENUBREAK**</span><span class="sxs-lookup"><span data-stu-id="81357-134">**MENUBREAK**</span></span>    | <span data-ttu-id="81357-135">Coloca el elemento de menú en una nueva línea para los elementos de barra de menús estáticos.</span><span class="sxs-lookup"><span data-stu-id="81357-135">Places the menu item on a new line for static menu-bar items.</span></span> <span data-ttu-id="81357-136">En los menús, coloca el elemento de menú en una nueva columna sin ninguna línea dividida entre las columnas.</span><span class="sxs-lookup"><span data-stu-id="81357-136">For menus, it places the menu item in a new column with no dividing line between the columns.</span></span>           |



 

</dd> <dt>

<span data-ttu-id="81357-137"><span id="MENUITEM_SEPARATOR"></span><span id="menuitem_separator"></span>**SEPARADOR MENUITEM**</span><span class="sxs-lookup"><span data-stu-id="81357-137"><span id="MENUITEM_SEPARATOR"></span><span id="menuitem_separator"></span>**MENUITEM SEPARATOR**</span></span>
</dt> <dd>

<span data-ttu-id="81357-138">La forma del **SEparador MenuItem** de la instrucción **MenuItem** crea un elemento de menú inactivo que sirve como barra divisoria entre dos elementos de menú activos en un menú.</span><span class="sxs-lookup"><span data-stu-id="81357-138">The **MENUITEM SEPARATOR** form of the **MENUITEM** statement creates an inactive menu item that serves as a dividing bar between two active menu items on a menu.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="81357-139">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="81357-139">Examples</span></span>

<span data-ttu-id="81357-140">En el ejemplo siguiente se muestra el uso de las instrucciones de **SEparador** **MenuItem** y MenuItem:</span><span class="sxs-lookup"><span data-stu-id="81357-140">The following example demonstrates the use of the **MENUITEM** and **MENUITEM SEPARATOR** statements:</span></span>

``` syntax
MENUITEM "&Roman", 206, CHECKED, GRAYED
MENUITEM SEPARATOR
MENUITEM "&Blackletter", 301
```

## <a name="see-also"></a><span data-ttu-id="81357-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="81357-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81357-142">**MENU**</span><span class="sxs-lookup"><span data-stu-id="81357-142">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="81357-143">**EMERGENTE**</span><span class="sxs-lookup"><span data-stu-id="81357-143">**POPUP**</span></span>](popup-resource.md)
</dt> </dl>

 

 




