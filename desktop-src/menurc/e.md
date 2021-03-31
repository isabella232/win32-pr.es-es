---
title: E (menús y otros recursos)
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 14e12ba3-8451-4a93-a555-e1c9e6040a67
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 029f8d26d341a114ab7bfeae269a391f8df90423
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104149828"
---
# <a name="e-menus-and-other-resources"></a><span data-ttu-id="7574b-103">E (menús y otros recursos)</span><span class="sxs-lookup"><span data-stu-id="7574b-103">E (Menus and Other Resources)</span></span>

<span data-ttu-id="7574b-104">[A](a.md) [B](b.md) [C](c.md) D E [F](f.md) G H [I](i.md) J K L M [N](n.md) [o](o.md) p Q [R](r.md) s [T](t.md) [U](u.md) [V](v.md) [W](w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="7574b-104">[A](a.md) [B](b.md) [C](c.md) D E [F](f.md) G H [I](i.md) J K L M [N](n.md) [O](o.md) P Q [R](r.md) S [T](t.md) [U](u.md) [V](v.md) [W](w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="7574b-105"><span id="tools.e_1_gly"></span><span id="TOOLS.E_1_GLY"></span>**No se permiten menús vacíos**</span><span class="sxs-lookup"><span data-stu-id="7574b-105"><span id="tools.e_1_gly"></span><span id="TOOLS.E_1_GLY"></span>**Empty menus not allowed**</span></span>
</dt> <dd>

<span data-ttu-id="7574b-106">Aparece una palabra clave **End** antes de que se defina algún elemento de menú en la instrucción de [**menú**](menu-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="7574b-106">An **END** keyword appears before any menu items are defined in the [**MENU**](menu-resource.md) statement.</span></span> <span data-ttu-id="7574b-107">El compilador de recursos de Microsoft Windows 32 (RC) no permite menús vacíos.</span><span class="sxs-lookup"><span data-stu-id="7574b-107">Empty menus are not permitted by Microsoft Windows 32 Resource Compiler (RC).</span></span> <span data-ttu-id="7574b-108">Asegúrese de que no tiene Comillas de apertura dentro de la instrucción de **menú** .</span><span class="sxs-lookup"><span data-stu-id="7574b-108">Make sure that you do not have any opening quotation marks within the **MENU** statement.</span></span>

</dd> <dt>

<span data-ttu-id="7574b-109"><span id="tools.e_2_gly"></span><span id="TOOLS.E_2_GLY"></span>**Se esperaba END en el cuadro de diálogo**</span><span class="sxs-lookup"><span data-stu-id="7574b-109"><span id="tools.e_2_gly"></span><span id="TOOLS.E_2_GLY"></span>**END expected in Dialog**</span></span>
</dt> <dd>

<span data-ttu-id="7574b-110">La palabra clave **End** debe aparecer al final de una instrucción [**Dialog**](dialog-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="7574b-110">The **END** keyword must appear at the end of a [**DIALOG**](dialog-resource.md) statement.</span></span> <span data-ttu-id="7574b-111">Asegúrese de que no quedan comillas de apertura de la instrucción anterior.</span><span class="sxs-lookup"><span data-stu-id="7574b-111">Make sure that there are no opening quotation marks left from the preceding statement.</span></span>

</dd> <dt>

<span data-ttu-id="7574b-112"><span id="tools.e_3_gly"></span><span id="TOOLS.E_3_GLY"></span>**Se esperaba END en el menú**</span><span class="sxs-lookup"><span data-stu-id="7574b-112"><span id="tools.e_3_gly"></span><span id="TOOLS.E_3_GLY"></span>**END expected in menu**</span></span>
</dt> <dd>

<span data-ttu-id="7574b-113">La palabra clave **End** debe aparecer al final de una instrucción [**Menu**](menu-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="7574b-113">The **END** keyword must appear at the end of a [**MENU**](menu-resource.md) statement.</span></span> <span data-ttu-id="7574b-114">Asegúrese de que no hay instrucciones **Begin** y **End** no coincidentes.</span><span class="sxs-lookup"><span data-stu-id="7574b-114">Make sure that there are no mismatched **BEGIN** and **END** statements.</span></span>

</dd> <dt>

<span data-ttu-id="7574b-115"><span id="tools.e_4_gly"></span><span id="TOOLS.E_4_GLY"></span>**Creatingresource de error: nombre**</span><span class="sxs-lookup"><span data-stu-id="7574b-115"><span id="tools.e_4_gly"></span><span id="TOOLS.E_4_GLY"></span>**Error Creatingresource-name**</span></span>
</dt> <dd>

<span data-ttu-id="7574b-116">El compilador de recursos de Microsoft Windows 32 (RC) no pudo crear el recurso binario especificado (. RES).</span><span class="sxs-lookup"><span data-stu-id="7574b-116">Microsoft Windows 32 Resource Compiler (RC) could not create the specified binary resource (.RES) file.</span></span> <span data-ttu-id="7574b-117">Asegúrese de que no se está creando en una unidad de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="7574b-117">Make sure that it is not being created on a read-only drive.</span></span> <span data-ttu-id="7574b-118">Use la opción **/v** para averiguar si se está creando el archivo.</span><span class="sxs-lookup"><span data-stu-id="7574b-118">Use the **/v** option to find out whether the file is being created.</span></span>

</dd> <dt>

<span data-ttu-id="7574b-119"><span id="tools.e_5_gly"></span><span id="TOOLS.E_5_GLY"></span>**Coma esperada en la tabla de aceleradores**</span><span class="sxs-lookup"><span data-stu-id="7574b-119"><span id="tools.e_5_gly"></span><span id="TOOLS.E_5_GLY"></span>**Expected Comma in Accelerator Table**</span></span>
</dt> <dd>

<span data-ttu-id="7574b-120">El compilador de recursos 32 de Microsoft Windows (RC) requiere una coma entre los parámetros *Event* y *idvalue* de la instrucción [**Accelerators**](accelerators-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="7574b-120">Microsoft Windows 32 Resource Compiler (RC) requires a comma between the *event* and *idvalue* parameters in the [**ACCELERATORS**](accelerators-resource.md) statement.</span></span>

</dd> <dt>

<span data-ttu-id="7574b-121"><span id="tools.e_6_gly"></span><span id="TOOLS.E_6_GLY"></span>**Se esperaba un nombre de clase de control**</span><span class="sxs-lookup"><span data-stu-id="7574b-121"><span id="tools.e_6_gly"></span><span id="TOOLS.E_6_GLY"></span>**Expected control class name**</span></span>
</dt> <dd>

<span data-ttu-id="7574b-122">El parámetro de *clase* de una instrucción de [**control**](control-control.md) en la instrucción [**Dialog**](dialog-resource.md) debe ser uno de los siguientes tipos de control: **Button**, [**ComboBox**](combobox-control.md), **Edit**, [**ListBox**](listbox-control.md), [**ScrollBar**](scrollbar-control.md), **static** o definido por el usuario.</span><span class="sxs-lookup"><span data-stu-id="7574b-122">The *class* parameter of a [**CONTROL**](control-control.md) statement in the [**DIALOG**](dialog-resource.md) statement must be one of the following control types: **BUTTON**, [**COMBOBOX**](combobox-control.md), **EDIT**, [**LISTBOX**](listbox-control.md), [**SCROLLBAR**](scrollbar-control.md), **STATIC**, or user-defined.</span></span> <span data-ttu-id="7574b-123">Asegúrese de que la clase está escrita correctamente.</span><span class="sxs-lookup"><span data-stu-id="7574b-123">Make sure that the class is spelled correctly.</span></span>

</dd> <dt>

<span data-ttu-id="7574b-124"><span id="tools.e_7_gly"></span><span id="TOOLS.E_7_GLY"></span>**Se esperaba un nombre de fuente**</span><span class="sxs-lookup"><span data-stu-id="7574b-124"><span id="tools.e_7_gly"></span><span id="TOOLS.E_7_GLY"></span>**Expected font face name**</span></span>
</dt> <dd>

<span data-ttu-id="7574b-125">El parámetro de tipo de *letra* de la instrucción **Font** de la instrucción [**Dialog**](dialog-resource.md) debe ser una cadena de caracteres entre comillas dobles (").</span><span class="sxs-lookup"><span data-stu-id="7574b-125">The *typeface* parameter of the **FONT** statement in the [**DIALOG**](dialog-resource.md) statement must be a character string enclosed in double quotation marks (").</span></span> <span data-ttu-id="7574b-126">Este parámetro especifica el nombre de una fuente.</span><span class="sxs-lookup"><span data-stu-id="7574b-126">This parameter specifies the name of a font.</span></span>

</dd> <dt>

<span data-ttu-id="7574b-127"><span id="tools.e_8_gly"></span><span id="TOOLS.E_8_GLY"></span>**Se esperaba un valor de identificador para MenuItem**</span><span class="sxs-lookup"><span data-stu-id="7574b-127"><span id="tools.e_8_gly"></span><span id="TOOLS.E_8_GLY"></span>**Expected ID value for Menuitem**</span></span>
</dt> <dd>

<span data-ttu-id="7574b-128">La instrucción [**Menu**](menu-resource.md) debe contener una instrucción [**MenuItem**](menuitem-statement.md) , que tiene un entero o una constante simbólica en el parámetro *menuid* .</span><span class="sxs-lookup"><span data-stu-id="7574b-128">The [**MENU**](menu-resource.md) statement must contain a [**MENUITEM**](menuitem-statement.md) statement, which has either an integer or a symbolic constant in the *MenuID* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="7574b-129"><span id="tools.e_9_gly"></span><span id="TOOLS.E_9_GLY"></span>**Se esperaba una cadena de menú**</span><span class="sxs-lookup"><span data-stu-id="7574b-129"><span id="tools.e_9_gly"></span><span id="TOOLS.E_9_GLY"></span>**Expected Menu String**</span></span>
</dt> <dd>

<span data-ttu-id="7574b-130">Cada instrucción [**MenuItem**](menuitem-statement.md) y [**popup**](popup-resource.md) debe contener un parámetro de *texto* .</span><span class="sxs-lookup"><span data-stu-id="7574b-130">Each [**MENUITEM**](menuitem-statement.md) and [**POPUP**](popup-resource.md) statement must contain a *text* parameter.</span></span> <span data-ttu-id="7574b-131">Este parámetro es una cadena entre comillas dobles (") que especifica el nombre del elemento de menú o menú emergente.</span><span class="sxs-lookup"><span data-stu-id="7574b-131">This parameter is a string enclosed in double quotation marks (") that specifies the name of the menu item or pop-up menu.</span></span> <span data-ttu-id="7574b-132">Una instrucción **MenuItem separator** no requiere ninguna cadena entrecomillada.</span><span class="sxs-lookup"><span data-stu-id="7574b-132">A **MENUITEM SEPARATOR** statement requires no quoted string.</span></span>

</dd> <dt>

<span data-ttu-id="7574b-133"><span id="tools.e_10_gly"></span><span id="TOOLS.E_10_GLY"></span>**Valor de comando numérico esperado**</span><span class="sxs-lookup"><span data-stu-id="7574b-133"><span id="tools.e_10_gly"></span><span id="TOOLS.E_10_GLY"></span>**Expected numeric command value**</span></span>
</dt> <dd>

<span data-ttu-id="7574b-134">El compilador de recursos de Microsoft Windows (RC) esperaba un parámetro *idvalue* numérico en la instrucción [**Accelerators**](accelerators-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="7574b-134">Microsoft Windows Resource Compiler (RC) was expecting a numeric *idvalue* parameter in the [**ACCELERATORS**](accelerators-resource.md) statement.</span></span> <span data-ttu-id="7574b-135">Asegúrese de que ha usado una instrucción [**\# define**](-define.md) para especificar el valor y que la constante usada está escrita correctamente.</span><span class="sxs-lookup"><span data-stu-id="7574b-135">Make sure that you have used a [**\#define**](-define.md) statement to specify the value and that the constant used is spelled correctly.</span></span>

</dd> <dt>

<span data-ttu-id="7574b-136"><span id="tools.e_11_gly"></span><span id="TOOLS.E_11_GLY"></span>**Se esperaba una constante numérica en la tabla de cadenas**</span><span class="sxs-lookup"><span data-stu-id="7574b-136"><span id="tools.e_11_gly"></span><span id="TOOLS.E_11_GLY"></span>**Expected numeric constant in string table**</span></span>
</dt> <dd>

<span data-ttu-id="7574b-137">Una constante numérica, definida en una instrucción [**\# define**](-define.md) , debe seguir inmediatamente a la palabra clave **Begin** en una instrucción [**stringtable**](stringtable-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="7574b-137">A numeric constant, defined in a [**\#define**](-define.md) statement, must immediately follow the **BEGIN** keyword in a [**STRINGTABLE**](stringtable-resource.md) statement.</span></span>

</dd> <dt>

<span data-ttu-id="7574b-138"><span id="tools.e_12_gly"></span><span id="TOOLS.E_12_GLY"></span>**Se esperaba un tamaño de punto numérico**</span><span class="sxs-lookup"><span data-stu-id="7574b-138"><span id="tools.e_12_gly"></span><span id="TOOLS.E_12_GLY"></span>**Expected numeric point size**</span></span>
</dt> <dd>

<span data-ttu-id="7574b-139">El parámetro de *puntuación* de la instrucción [**Font**](font-statement.md) en la instrucción [**Dialog**](dialog-resource.md) debe ser un valor entero de tamaño de punto.</span><span class="sxs-lookup"><span data-stu-id="7574b-139">The *pointsize* parameter of the [**FONT**](font-statement.md) statement in the [**DIALOG**](dialog-resource.md) statement must be an integer point-size value.</span></span>

</dd> <dt>

<span data-ttu-id="7574b-140"><span id="tools.e_13_gly"></span><span id="TOOLS.E_13_GLY"></span>**Se esperaba una constante de cuadro de diálogo numérica**</span><span class="sxs-lookup"><span data-stu-id="7574b-140"><span id="tools.e_13_gly"></span><span id="TOOLS.E_13_GLY"></span>**Expected Numerical Dialog constant**</span></span>
</dt> <dd>

<span data-ttu-id="7574b-141">Una instrucción [**Dialog**](dialog-resource.md) requiere valores enteros para los parámetros *x*, *y*, *ancho* y *alto* .</span><span class="sxs-lookup"><span data-stu-id="7574b-141">A [**DIALOG**](dialog-resource.md) statement requires integer values for the *x*, *y*, *width*, and *height* parameters.</span></span> <span data-ttu-id="7574b-142">Asegúrese de que estos valores, que se incluyen después de la palabra clave **Dialog** , no sean negativos.</span><span class="sxs-lookup"><span data-stu-id="7574b-142">Make sure that these values, which are included after the **DIALOG** keyword, are not negative.</span></span>

</dd> <dt>

<span data-ttu-id="7574b-143"><span id="tools.e_14_gly"></span><span id="TOOLS.E_14_GLY"></span>**Se esperaba una cadena en STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="7574b-143"><span id="tools.e_14_gly"></span><span id="TOOLS.E_14_GLY"></span>**Expected String in STRINGTABLE**</span></span>
</dt> <dd>

<span data-ttu-id="7574b-144">Se espera una cadena después de cada parámetro *stringid* numérico en una instrucción [**stringtable**](stringtable-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="7574b-144">A string is expected after each numeric *stringid* parameter in a [**STRINGTABLE**](stringtable-resource.md) statement.</span></span>

</dd> <dt>

<span data-ttu-id="7574b-145"><span id="tools.e_15_gly"></span><span id="TOOLS.E_15_GLY"></span>**Comando de acelerador de constante o cadena esperado**</span><span class="sxs-lookup"><span data-stu-id="7574b-145"><span id="tools.e_15_gly"></span><span id="TOOLS.E_15_GLY"></span>**Expected String or Constant Accelerator command**</span></span>
</dt> <dd>

<span data-ttu-id="7574b-146">El compilador de recursos de Microsoft Windows (RC) no pudo determinar qué clave se estaba configurando para el acelerador.</span><span class="sxs-lookup"><span data-stu-id="7574b-146">Microsoft Windows Resource Compiler (RC) was not able to determine which key was being set up for the accelerator.</span></span> <span data-ttu-id="7574b-147">Es posible que el parámetro de *evento* de la instrucción [**Accelerators**](accelerators-resource.md) no sea válido.</span><span class="sxs-lookup"><span data-stu-id="7574b-147">The *event* parameter in the [**ACCELERATORS**](accelerators-resource.md) statement might be invalid.</span></span>

</dd> <dt>

<span data-ttu-id="7574b-148"><span id="tools.e_16_gly"></span><span id="TOOLS.E_16_GLY"></span>**Se esperaba la palabra clave VALUE, BLOCK o END.**</span><span class="sxs-lookup"><span data-stu-id="7574b-148"><span id="tools.e_16_gly"></span><span id="TOOLS.E_16_GLY"></span>**Expected VALUE, BLOCK, or END keyword.**</span></span>
</dt> <dd>

<span data-ttu-id="7574b-149">La estructura [**versionInfo**](versioninfo-resource.md) requiere una palabra clave **Value**, **Block** o **End** .</span><span class="sxs-lookup"><span data-stu-id="7574b-149">The [**VERSIONINFO**](versioninfo-resource.md) structure requires a **VALUE**, **BLOCK**, or **END** keyword.</span></span>

</dd> <dt>

<span data-ttu-id="7574b-150"><span id="tools.e_17_gly"></span><span id="TOOLS.E_17_GLY"></span>**Se espera un número para el identificador**</span><span class="sxs-lookup"><span data-stu-id="7574b-150"><span id="tools.e_17_gly"></span><span id="TOOLS.E_17_GLY"></span>**Expecting number for ID**</span></span>
</dt> <dd>

<span data-ttu-id="7574b-151">Se espera un número para el parámetro *ID* de una instrucción de [**control**](control-control.md) en la instrucción [**Dialog**](dialog-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="7574b-151">A number is expected for the *id* parameter of a [**CONTROL**](control-control.md) statement in the [**DIALOG**](dialog-resource.md) statement.</span></span> <span data-ttu-id="7574b-152">Asegúrese de que tiene un número o una instrucción de [**\# definición**](-define.md) para el identificador de control.</span><span class="sxs-lookup"><span data-stu-id="7574b-152">Make sure that you have a number or a [**\#define**](-define.md) statement for the control identifier.</span></span>

</dd> <dt>

<span data-ttu-id="7574b-153"><span id="tools.e_18_gly"></span><span id="TOOLS.E_18_GLY"></span>**Se espera una cadena entre comillas para la clave**</span><span class="sxs-lookup"><span data-stu-id="7574b-153"><span id="tools.e_18_gly"></span><span id="TOOLS.E_18_GLY"></span>**Expecting quoted string for key**</span></span>
</dt> <dd>

<span data-ttu-id="7574b-154">La cadena de clave que sigue a la palabra clave **Block** o **Value** se debe incluir entre comillas dobles.</span><span class="sxs-lookup"><span data-stu-id="7574b-154">The key string following the **BLOCK** or **VALUE** keyword should be enclosed in double quotation marks.</span></span>

</dd> <dt>

<span data-ttu-id="7574b-155"><span id="tools.e_19_gly"></span><span id="TOOLS.E_19_GLY"></span>**Se espera una cadena entrecomillada en una clase de cuadro de diálogo**</span><span class="sxs-lookup"><span data-stu-id="7574b-155"><span id="tools.e_19_gly"></span><span id="TOOLS.E_19_GLY"></span>**Expecting quoted string in dialog class**</span></span>
</dt> <dd>

<span data-ttu-id="7574b-156">El parámetro *Class* de la instrucción [**Class**](class-statement.md) en la instrucción [**Dialog**](dialog-resource.md) debe ser un entero o una cadena entre comillas dobles (").</span><span class="sxs-lookup"><span data-stu-id="7574b-156">The *class* parameter of the [**CLASS**](class-statement.md) statement in the [**DIALOG**](dialog-resource.md) statement must be an integer or a string enclosed in double quotation marks (").</span></span>

</dd> <dt>

<span data-ttu-id="7574b-157"><span id="tools.e_20_gly"></span><span id="TOOLS.E_20_GLY"></span>**Se espera una cadena entrecomillada en el título del cuadro de diálogo**</span><span class="sxs-lookup"><span data-stu-id="7574b-157"><span id="tools.e_20_gly"></span><span id="TOOLS.E_20_GLY"></span>**Expecting quoted string in dialog title**</span></span>
</dt> <dd>

<span data-ttu-id="7574b-158">El parámetro *captiontext* de la instrucción [**Caption**](caption-statement.md) de la instrucción [**Dialog**](dialog-resource.md) debe ser una cadena de caracteres, entre comillas dobles (").</span><span class="sxs-lookup"><span data-stu-id="7574b-158">The *captiontext* parameter of the [**CAPTION**](caption-statement.md) statement in the [**DIALOG**](dialog-resource.md) statement must be a character string, enclosed in double quotation marks (").</span></span>

</dd> </dl>

 

 




