---
title: Recurso POPUP
description: Define un elemento de menú que puede contener elementos de menú y submenús.
ms.assetid: afca21c7-605e-4354-b6ec-576b81389b69
keywords:
- Menús EMERGENTEs de recursos y otros recursos
topic_type:
- apiref
api_name:
- POPUP
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41c7a1af3bd8ed9aae8908aa7ff926a3f4799ee5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104148925"
---
# <a name="popup-resource"></a><span data-ttu-id="4a2fc-104">Recurso POPUP</span><span class="sxs-lookup"><span data-stu-id="4a2fc-104">POPUP resource</span></span>

<span data-ttu-id="4a2fc-105">Define un elemento de menú que puede contener elementos de menú y submenús.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-105">Defines a menu item that can contain menu items and submenus.</span></span>

``` syntax
POPUP text, [optionlist] {item-definitions ...}
```

## <a name="parameters"></a><span data-ttu-id="4a2fc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4a2fc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a2fc-107"><span id="text"></span><span id="TEXT"></span>*negrita*</span><span class="sxs-lookup"><span data-stu-id="4a2fc-107"><span id="text"></span><span id="TEXT"></span>*text*</span></span>
</dt> <dd>

<span data-ttu-id="4a2fc-108">Cadena que contiene el nombre del menú.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-108">String that contains the name of the menu.</span></span> <span data-ttu-id="4a2fc-109">Esta cadena se debe incluir entre comillas dobles (**"**).</span><span class="sxs-lookup"><span data-stu-id="4a2fc-109">This string must be enclosed in double quotation marks (**"**).</span></span>

</dd> <dt>

<span data-ttu-id="4a2fc-110"><span id="optionlist"></span><span id="OPTIONLIST"></span>*optionlist*</span><span class="sxs-lookup"><span data-stu-id="4a2fc-110"><span id="optionlist"></span><span id="OPTIONLIST"></span>*optionlist*</span></span>
</dt> <dd>

<span data-ttu-id="4a2fc-111">Este parámetro especifica las opciones de menú redefinidas que especifican la apariencia del elemento de menú.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-111">This parameter specifies redefined menu options that specify the appearance of the menu item.</span></span> <span data-ttu-id="4a2fc-112">Este parámetro opcional puede ser uno o varios de los siguientes.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-112">This optional parameter can be one or more of the following.</span></span>



| <span data-ttu-id="4a2fc-113">Opción</span><span class="sxs-lookup"><span data-stu-id="4a2fc-113">Option</span></span>           | <span data-ttu-id="4a2fc-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="4a2fc-114">Description</span></span>                                                                                                                                                           |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a2fc-115">**INCORPORA**</span><span class="sxs-lookup"><span data-stu-id="4a2fc-115">**CHECKED**</span></span>      | <span data-ttu-id="4a2fc-116">El elemento de menú tiene una marca de verificación junto a él.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-116">Menu item has a check mark next to it.</span></span> <span data-ttu-id="4a2fc-117">Esta opción no es válida para un menú de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-117">This option is not valid for a top-level menu.</span></span>                                                                                 |
| <span data-ttu-id="4a2fc-118">**ATENUADO**</span><span class="sxs-lookup"><span data-stu-id="4a2fc-118">**GRAYED**</span></span>       | <span data-ttu-id="4a2fc-119">El elemento de menú está inicialmente inactivo y aparece en el menú en gris o en una sombra iluminada del color del texto de menú.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-119">Menu item is initially inactive and appears on the menu in gray or a lightened shade of the menu-text color.</span></span> <span data-ttu-id="4a2fc-120">Esta opción no se puede usar con la opción **inactiva** .</span><span class="sxs-lookup"><span data-stu-id="4a2fc-120">This option cannot be used with the **INACTIVE** option.</span></span> |
| <span data-ttu-id="4a2fc-121">**Ayuda**</span><span class="sxs-lookup"><span data-stu-id="4a2fc-121">**HELP**</span></span>         | <span data-ttu-id="4a2fc-122">Identifica un elemento de ayuda.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-122">Identifies a help item.</span></span> <span data-ttu-id="4a2fc-123">El elemento de menú se coloca en la posición más a la derecha en la barra de menús.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-123">The menu item is place at the right-most position on the menu bar.</span></span>                                                                            |
| <span data-ttu-id="4a2fc-124">**INACTIVA**</span><span class="sxs-lookup"><span data-stu-id="4a2fc-124">**INACTIVE**</span></span>     | <span data-ttu-id="4a2fc-125">Se muestra el elemento de menú, pero no se puede seleccionar.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-125">Menu item is displayed but it cannot be selected.</span></span> <span data-ttu-id="4a2fc-126">Esta opción no se puede usar con la opción **atenuada** .</span><span class="sxs-lookup"><span data-stu-id="4a2fc-126">This option cannot be used with the **GRAYED** option.</span></span>                                                              |
| <span data-ttu-id="4a2fc-127">**MENUBARBREAK**</span><span class="sxs-lookup"><span data-stu-id="4a2fc-127">**MENUBARBREAK**</span></span> | <span data-ttu-id="4a2fc-128">Igual que **MENUBREAK** , excepto en el caso de los menús emergentes, separa la nueva columna de la antigua con una línea vertical.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-128">Same as **MENUBREAK** except that for pop-up menus, it separates the new column from the old column with a vertical line.</span></span>                                             |
| <span data-ttu-id="4a2fc-129">**MENUBREAK**</span><span class="sxs-lookup"><span data-stu-id="4a2fc-129">**MENUBREAK**</span></span>    | <span data-ttu-id="4a2fc-130">Coloca el elemento de menú en una nueva línea para los elementos de barra de menús estáticos.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-130">Places the menu item on a new line for static menu-bar items.</span></span> <span data-ttu-id="4a2fc-131">En los menús, coloca el elemento de menú en una nueva columna sin ninguna línea dividida entre las columnas.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-131">For menus, it places the menu item in a new column with no dividing line between the columns.</span></span>           |



 

</dd> </dl>

<span data-ttu-id="4a2fc-132">Algunos atributos también se admiten por razones de compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="4a2fc-132">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="4a2fc-133">Para obtener más información, vea [atributos comunes de recursos](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="4a2fc-133">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="examples"></a><span data-ttu-id="4a2fc-134">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="4a2fc-134">Examples</span></span>

<span data-ttu-id="4a2fc-135">En el siguiente ejemplo se muestra el uso de la instrucción **popup** :</span><span class="sxs-lookup"><span data-stu-id="4a2fc-135">The following example demonstrates the use of the **POPUP** statement:</span></span>

``` syntax
chem MENU
{
    POPUP "&Elements"
    {
         MENUITEM "&Oxygen", 200
         MENUITEM "&Carbon", 201, CHECKED
         MENUITEM "&Hydrogen", 202
         MENUITEM SEPARATOR
         MENUITEM "&Sulfur", 203
         MENUITEM "Ch&lorine", 204
    } 
    POPUP "&Compounds"
    {
         POPUP "&Sugars"
         {
            MENUITEM "&Glucose", 301
            MENUITEM "&Sucrose", 302, CHECKED
            MENUITEM "&Lactose", 303, MENUBREAK
            MENUITEM "&Fructose", 304
         }
         POPUP "&Acids"
         {
              "&Hydrochloric", 401
              "&Sulfuric", 402
         }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="4a2fc-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="4a2fc-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a2fc-137">**MENU**</span><span class="sxs-lookup"><span data-stu-id="4a2fc-137">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="4a2fc-138">**OBJETOS**</span><span class="sxs-lookup"><span data-stu-id="4a2fc-138">**MENUITEM**</span></span>](menuitem-statement.md)
</dt> </dl>

 

 




