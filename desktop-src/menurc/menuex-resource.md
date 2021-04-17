---
title: Recurso MENUEX
description: Define el contenido de un recurso de menú. | Recurso MENUEX
ms.assetid: a83e1e78-2af4-4257-906e-7eb6d98bcbc8
keywords:
- Menús de recursos de MENUEX y otros recursos
topic_type:
- apiref
api_name:
- MENUEX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ed379fb97d2795a166571fb48cde2c233021a33
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105717505"
---
# <a name="menuex-resource"></a><span data-ttu-id="7e06a-105">Recurso MENUEX</span><span class="sxs-lookup"><span data-stu-id="7e06a-105">MENUEX resource</span></span>

<span data-ttu-id="7e06a-106">Define el contenido de un recurso de menú.</span><span class="sxs-lookup"><span data-stu-id="7e06a-106">Defines the contents of a menu resource.</span></span> <span data-ttu-id="7e06a-107">Un recurso de menú es una colección de información que define la apariencia y la función de un menú de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7e06a-107">A menu resource is a collection of information that defines the appearance and function of an application menu.</span></span> <span data-ttu-id="7e06a-108">Un menú es una herramienta de entrada especial que permite a un usuario seleccionar comandos y abrir submenús en una lista de elementos de menú.</span><span class="sxs-lookup"><span data-stu-id="7e06a-108">A menu is a special input tool that lets a user select commands and open submenus from a list of menu items.</span></span> <span data-ttu-id="7e06a-109">También define lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="7e06a-109">It also defines the following:</span></span>

-   <span data-ttu-id="7e06a-110">Los identificadores de ayuda de los menús.</span><span class="sxs-lookup"><span data-stu-id="7e06a-110">Help identifiers on menus.</span></span>
-   <span data-ttu-id="7e06a-111">Identificadores de los menús.</span><span class="sxs-lookup"><span data-stu-id="7e06a-111">Identifiers on menus.</span></span>
-   <span data-ttu-id="7e06a-112">Uso de las marcas de tipo **MFT \_ \** _ y estado de _*MFS \_ \*\*_ .</span><span class="sxs-lookup"><span data-stu-id="7e06a-112">Use of the **MFT\_\** _ type flags and _*MFS\_\*\*_ state flags.</span></span> <span data-ttu-id="7e06a-113">Para obtener más información sobre estas marcas, consulte la estructura [_ *MENUITEMINFO* \*](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) .</span><span class="sxs-lookup"><span data-stu-id="7e06a-113">For more information on these flags, see the [_ *MENUITEMINFO*\*](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) structure.</span></span>

``` syntax
menuID MENUEX{ [{[MENUITEM itemText [,[id][, [type][, state]]]] | 
    POPUP itemText [,[id][, [type][, [state][, helpID]]]] { popupBody } } . . .]}
```

## <a name="parameters"></a><span data-ttu-id="7e06a-114">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7e06a-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e06a-115"><span id="MENUITEM"></span><span id="menuitem"></span>[**OBJETOS**](menuitem-statement.md)</span><span class="sxs-lookup"><span data-stu-id="7e06a-115"><span id="MENUITEM"></span><span id="menuitem"></span>[**MENUITEM**](menuitem-statement.md)</span></span>
</dt> <dd>

<span data-ttu-id="7e06a-116">Define un elemento de menú.</span><span class="sxs-lookup"><span data-stu-id="7e06a-116">Defines a menu item.</span></span>

<dl> <dt>

<span data-ttu-id="7e06a-117"><span id="itemText"></span><span id="itemtext"></span><span id="ITEMTEXT"></span>*itemText*</span><span class="sxs-lookup"><span data-stu-id="7e06a-117"><span id="itemText"></span><span id="itemtext"></span><span id="ITEMTEXT"></span>*itemText*</span></span>
</dt> <dd>

<span data-ttu-id="7e06a-118">Cadena que contiene el texto del elemento de menú.</span><span class="sxs-lookup"><span data-stu-id="7e06a-118">String containing the text for the menu item.</span></span> <span data-ttu-id="7e06a-119">Para obtener más información, vea [**MenuItem**](menuitem-statement.md).</span><span class="sxs-lookup"><span data-stu-id="7e06a-119">For more information, see [**MENUITEM**](menuitem-statement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7e06a-120"><span id="id"></span><span id="ID"></span>*sesión*</span><span class="sxs-lookup"><span data-stu-id="7e06a-120"><span id="id"></span><span id="ID"></span>*id*</span></span>
</dt> <dd>

<span data-ttu-id="7e06a-121">Expresión numérica que indica el identificador del elemento de menú.</span><span class="sxs-lookup"><span data-stu-id="7e06a-121">Numeric expression indicating the identifier of the menu item.</span></span>

</dd> <dt>

<span data-ttu-id="7e06a-122"><span id="type"></span><span id="TYPE"></span>*automáticamente*</span><span class="sxs-lookup"><span data-stu-id="7e06a-122"><span id="type"></span><span id="TYPE"></span>*type*</span></span>
</dt> <dd>

<span data-ttu-id="7e06a-123">Expresión numérica que indica el tipo de elemento de menú para usar los valores de tipo de MFT predefinidos \_ \* , incluya la siguiente instrucción en el archivo. RC:`#include "winuser.h"`</span><span class="sxs-lookup"><span data-stu-id="7e06a-123">Numeric expression indicating the type of the menu item To use the predefined MFT\_\* type values, include the following statement in your .rc file: `#include "winuser.h"`</span></span>

</dd> <dt>

<span data-ttu-id="7e06a-124"><span id="state"></span><span id="STATE"></span>*State*</span><span class="sxs-lookup"><span data-stu-id="7e06a-124"><span id="state"></span><span id="STATE"></span>*state*</span></span>
</dt> <dd>

<span data-ttu-id="7e06a-125">Expresión numérica que indica el estado del elemento de menú para usar los valores de estado de la MFS predefinidos \_ \* , incluya la siguiente instrucción en su. Archivo RC:`#include "winuser.h"`</span><span class="sxs-lookup"><span data-stu-id="7e06a-125">Numeric expression indicating the state of the menu item To use the predefined MFS\_\* state values, include the following statement in your .RC file: `#include "winuser.h"`</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="7e06a-126"><span id="POPUP"></span><span id="popup"></span>[**EMERGENTE**](popup-resource.md)</span><span class="sxs-lookup"><span data-stu-id="7e06a-126"><span id="POPUP"></span><span id="popup"></span>[**POPUP**](popup-resource.md)</span></span>
</dt> <dd>

<span data-ttu-id="7e06a-127">Define un elemento de menú que tiene un submenú asociado a él.</span><span class="sxs-lookup"><span data-stu-id="7e06a-127">Defines a menu item that has a submenu associated with it.</span></span>

<dl> <dt>

<span data-ttu-id="7e06a-128"><span id="itemText"></span><span id="itemtext"></span><span id="ITEMTEXT"></span>*itemText*</span><span class="sxs-lookup"><span data-stu-id="7e06a-128"><span id="itemText"></span><span id="itemtext"></span><span id="ITEMTEXT"></span>*itemText*</span></span>
</dt> <dd>

<span data-ttu-id="7e06a-129">Cadena que contiene el texto del elemento de menú.</span><span class="sxs-lookup"><span data-stu-id="7e06a-129">String containing the text for the menu item.</span></span>

</dd> <dt>

<span data-ttu-id="7e06a-130"><span id="id"></span><span id="ID"></span>*sesión*</span><span class="sxs-lookup"><span data-stu-id="7e06a-130"><span id="id"></span><span id="ID"></span>*id*</span></span>
</dt> <dd>

<span data-ttu-id="7e06a-131">Expresión numérica que indica el identificador del elemento de menú.</span><span class="sxs-lookup"><span data-stu-id="7e06a-131">Numeric expression indicating the identifier of the menu item.</span></span>

</dd> <dt>

<span data-ttu-id="7e06a-132"><span id="type"></span><span id="TYPE"></span>*automáticamente*</span><span class="sxs-lookup"><span data-stu-id="7e06a-132"><span id="type"></span><span id="TYPE"></span>*type*</span></span>
</dt> <dd>

<span data-ttu-id="7e06a-133">Expresión numérica que indica el tipo de elemento de menú para usar los valores de tipo de MFT predefinidos \_ \* , incluya la siguiente instrucción en su. Archivo RC:`#include "winuser.h"`</span><span class="sxs-lookup"><span data-stu-id="7e06a-133">Numeric expression indicating the type of the menu item To use the predefined MFT\_\* type values, include the following statement in your .RC file: `#include "winuser.h"`</span></span>

</dd> <dt>

<span data-ttu-id="7e06a-134"><span id="state"></span><span id="STATE"></span>*State*</span><span class="sxs-lookup"><span data-stu-id="7e06a-134"><span id="state"></span><span id="STATE"></span>*state*</span></span>
</dt> <dd>

<span data-ttu-id="7e06a-135">Expresión numérica que indica el estado del elemento de menú para usar los valores de estado de la MFS predefinidos \_ \* , incluya la siguiente instrucción en el archivo. RC:`#include "winuser.h"`</span><span class="sxs-lookup"><span data-stu-id="7e06a-135">Numeric expression indicating the state of the menu item To use the predefined MFS\_\* state values, include the following statement in your .rc file: `#include "winuser.h"`</span></span>

</dd> <dt>

<span data-ttu-id="7e06a-136"><span id="helpID"></span><span id="helpid"></span><span id="HELPID"></span>*helpID*</span><span class="sxs-lookup"><span data-stu-id="7e06a-136"><span id="helpID"></span><span id="helpid"></span><span id="HELPID"></span>*helpID*</span></span>
</dt> <dd>

<span data-ttu-id="7e06a-137">Expresión numérica que indica el identificador usado para identificar el menú durante el procesamiento de la [**\_ ayuda de WM**](../shell/wm-help.md) .</span><span class="sxs-lookup"><span data-stu-id="7e06a-137">Numeric expression indicating the identifier used to identify the menu during [**WM\_HELP**](../shell/wm-help.md) processing.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="7e06a-138"><span id="popupBody"></span><span id="popupbody"></span><span id="POPUPBODY"></span>*popupBody*</span><span class="sxs-lookup"><span data-stu-id="7e06a-138"><span id="popupBody"></span><span id="popupbody"></span><span id="POPUPBODY"></span>*popupBody*</span></span>
</dt> <dd>

<span data-ttu-id="7e06a-139">Contiene cualquier combinación de las instrucciones [**MenuItem**](menuitem-statement.md) y [**popup**](popup-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="7e06a-139">Contains any combination of the [**MENUITEM**](menuitem-statement.md) and [**POPUP**](popup-resource.md) statements.</span></span>

</dd> </dl>

<span data-ttu-id="7e06a-140">Algunos atributos también se admiten por razones de compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="7e06a-140">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="7e06a-141">Para obtener más información, vea [atributos comunes de recursos](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="7e06a-141">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7e06a-142">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7e06a-142">Remarks</span></span>

<span data-ttu-id="7e06a-143">Las operaciones aritméticas y booleanas válidas que se pueden incluir en cualquiera de las expresiones numéricas de las instrucciones de **MENUEX** son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="7e06a-143">The valid arithmetic and Boolean operations that can be contained in any of the numeric expressions in the statements of **MENUEX** are as follows:</span></span>

-   <span data-ttu-id="7e06a-144">Agregar (' + ')</span><span class="sxs-lookup"><span data-stu-id="7e06a-144">Add ('+')</span></span>
-   <span data-ttu-id="7e06a-145">Resta ('-')</span><span class="sxs-lookup"><span data-stu-id="7e06a-145">Subtract ('-')</span></span>
-   <span data-ttu-id="7e06a-146">Unario menos ('-')</span><span class="sxs-lookup"><span data-stu-id="7e06a-146">Unary minus ('-')</span></span>
-   <span data-ttu-id="7e06a-147">Unario no (' ~ ')</span><span class="sxs-lookup"><span data-stu-id="7e06a-147">Unary NOT ('~')</span></span>
-   <span data-ttu-id="7e06a-148">Y (' & ')</span><span class="sxs-lookup"><span data-stu-id="7e06a-148">AND ('&')</span></span>
-   <span data-ttu-id="7e06a-149">O (' \| ')</span><span class="sxs-lookup"><span data-stu-id="7e06a-149">OR ('\|')</span></span>

## <a name="see-also"></a><span data-ttu-id="7e06a-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="7e06a-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e06a-151">Uso de los menús</span><span class="sxs-lookup"><span data-stu-id="7e06a-151">Using Menus</span></span>](./using-menus.md)
</dt> <dt>

[<span data-ttu-id="7e06a-152">**ACELERADORES**</span><span class="sxs-lookup"><span data-stu-id="7e06a-152">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="7e06a-153">**SUS**</span><span class="sxs-lookup"><span data-stu-id="7e06a-153">**CHARACTERISTICS**</span></span>](characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="7e06a-154">**DIÁLOGO**</span><span class="sxs-lookup"><span data-stu-id="7e06a-154">**DIALOG**</span></span>](dialog-resource.md)
</dt> <dt>

[<span data-ttu-id="7e06a-155">**MÓDULO**</span><span class="sxs-lookup"><span data-stu-id="7e06a-155">**LANGUAGE**</span></span>](language-statement.md)
</dt> <dt>

[<span data-ttu-id="7e06a-156">**MENU**</span><span class="sxs-lookup"><span data-stu-id="7e06a-156">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="7e06a-157">**OBJETOS**</span><span class="sxs-lookup"><span data-stu-id="7e06a-157">**MENUITEM**</span></span>](menuitem-statement.md)
</dt> <dt>

[<span data-ttu-id="7e06a-158">**EMERGENTE**</span><span class="sxs-lookup"><span data-stu-id="7e06a-158">**POPUP**</span></span>](popup-resource.md)
</dt> <dt>

[<span data-ttu-id="7e06a-159">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="7e06a-159">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="7e06a-160">**STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="7e06a-160">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> <dt>

[<span data-ttu-id="7e06a-161">**Versión**</span><span class="sxs-lookup"><span data-stu-id="7e06a-161">**VERSION**</span></span>](version-statement.md)
</dt> </dl>

 

 
