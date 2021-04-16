---
title: Recurso de cuadro de diálogo
description: Define un cuadro de diálogo. | Recurso de cuadro de diálogo
ms.assetid: d166fb7d-0fe5-4e48-a545-19acc0ff80f1
keywords:
- Menús de recursos de cuadro de diálogo y otros recursos
topic_type:
- apiref
api_name:
- DIALOG
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc7a1aef314406340c42c6a4aca40b76f91ac353
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105678689"
---
# <a name="dialog-resource"></a><span data-ttu-id="7da23-105">Recurso de cuadro de diálogo</span><span class="sxs-lookup"><span data-stu-id="7da23-105">DIALOG resource</span></span>

<span data-ttu-id="7da23-106">Define un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="7da23-106">Defines a dialog box.</span></span> <span data-ttu-id="7da23-107">La instrucción define la posición y las dimensiones del cuadro de diálogo en la pantalla, así como el estilo del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="7da23-107">The statement defines the position and dimensions of the dialog box on the screen as well as the dialog box style.</span></span>

> [!Note]  
> <span data-ttu-id="7da23-108">El **cuadro de diálogo** es un identificador de recurso obsoleto.</span><span class="sxs-lookup"><span data-stu-id="7da23-108">**DIALOG** is an obsolete resource ID.</span></span> <span data-ttu-id="7da23-109">Las nuevas aplicaciones deben usar [**DIALOGEX**](dialogex-resource.md).</span><span class="sxs-lookup"><span data-stu-id="7da23-109">New applications should use [**DIALOGEX**](dialogex-resource.md).</span></span>

 

``` syntax
nameID DIALOG x, y, width, height  [optional-statements] {control-statement  . . . }
```

## <a name="parameters"></a><span data-ttu-id="7da23-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7da23-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7da23-111"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span><span class="sxs-lookup"><span data-stu-id="7da23-111"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span></span>
</dt> <dd>

<span data-ttu-id="7da23-112">Nombre único o un valor entero de 16 bits sin signo único que identifica el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="7da23-112">Unique name or a unique 16-bit unsigned integer value that identifies the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="7da23-113"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*instrucciones opcionales*</span><span class="sxs-lookup"><span data-stu-id="7da23-113"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*optional-statements*</span></span>
</dt> <dd>

<span data-ttu-id="7da23-114">Opciones del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="7da23-114">Options for the dialog box.</span></span> <span data-ttu-id="7da23-115">Puede ser cero o más de las instrucciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="7da23-115">This can be zero or more of the following statements.</span></span>



| <span data-ttu-id="7da23-116">.</span><span class="sxs-lookup"><span data-stu-id="7da23-116">Statement</span></span>                                                        | <span data-ttu-id="7da23-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="7da23-117">Description</span></span>                                                                                                                                                                                  |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7da23-118">[**Título**](caption-statement.md) de "*texto*"</span><span class="sxs-lookup"><span data-stu-id="7da23-118">[**CAPTION**](caption-statement.md) "*text*"</span></span>                    | <span data-ttu-id="7da23-119">Título del cuadro de diálogo si tiene una barra de título.</span><span class="sxs-lookup"><span data-stu-id="7da23-119">Caption of the dialog box if it has a title bar.</span></span> <span data-ttu-id="7da23-120">Para obtener más información, consulte [**Caption**](caption-statement.md).</span><span class="sxs-lookup"><span data-stu-id="7da23-120">For more information, see [**CAPTION**](caption-statement.md).</span></span>                                                                             |
| <span data-ttu-id="7da23-121">[**Características**](characteristics-statement.md) *DWORD*</span><span class="sxs-lookup"><span data-stu-id="7da23-121">[**CHARACTERISTICS**](characteristics-statement.md) *dword*</span></span>     | <span data-ttu-id="7da23-122">Valor **DWORD** definido por el usuario para que lo usen las herramientas de recursos.</span><span class="sxs-lookup"><span data-stu-id="7da23-122">User-defined **DWORD** value for use by resource tools.</span></span> <span data-ttu-id="7da23-123">El sistema no utiliza este valor.</span><span class="sxs-lookup"><span data-stu-id="7da23-123">This value is not used by the system.</span></span> <span data-ttu-id="7da23-124">Para obtener más información, vea [**características**](characteristics-statement.md).</span><span class="sxs-lookup"><span data-stu-id="7da23-124">For more information, see [**CHARACTERISTICS**](characteristics-statement.md).</span></span>                |
| <span data-ttu-id="7da23-125">[](class-statement.md) *Clase de* clase</span><span class="sxs-lookup"><span data-stu-id="7da23-125">[**CLASS**](class-statement.md) *class*</span></span>                         | <span data-ttu-id="7da23-126">Entero de 16 bits sin signo o cadena, entre comillas dobles ("), que identifica la clase del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="7da23-126">A 16-bit unsigned integer or a string, enclosed in double quotation marks ("), that identifies the class of the dialog box.</span></span> <span data-ttu-id="7da23-127">Para obtener más información, vea [**clase**](class-statement.md).</span><span class="sxs-lookup"><span data-stu-id="7da23-127">For more information, see [**CLASS**](class-statement.md).</span></span>      |
| <span data-ttu-id="7da23-128">**ExStyle =** *estilos extendidos*</span><span class="sxs-lookup"><span data-stu-id="7da23-128">**EXSTYLE=** *extended-styles*</span></span>                                   | <span data-ttu-id="7da23-129">Estilo de ventana extendida del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="7da23-129">Extended window style of the dialog box.</span></span> <span data-ttu-id="7da23-130">Para obtener más información, vea [**ExStyle**](exstyle-statement.md).</span><span class="sxs-lookup"><span data-stu-id="7da23-130">For more information, see [**EXSTYLE**](exstyle-statement.md).</span></span>                                                                                     |
| <span data-ttu-id="7da23-131"> *Puntuación* de fuente, tipo de *letra*</span><span class="sxs-lookup"><span data-stu-id="7da23-131">**FONT** *pointsize*, *typeface*</span></span>                                 | <span data-ttu-id="7da23-132">Tamaño de punto y tipo de letra de la fuente.</span><span class="sxs-lookup"><span data-stu-id="7da23-132">Point size and typeface for the font.</span></span> <span data-ttu-id="7da23-133">Para obtener más información, vea [**Font**](font-statement.md).</span><span class="sxs-lookup"><span data-stu-id="7da23-133">For more information, see [**FONT**](font-statement.md).</span></span>                                                                                              |
| <span data-ttu-id="7da23-134">[](language-statement.md) *Idioma* del idioma, *subidioma*</span><span class="sxs-lookup"><span data-stu-id="7da23-134">[**LANGUAGE**](language-statement.md) *language*, *sublanguage*</span></span> | <span data-ttu-id="7da23-135">Idioma del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="7da23-135">Language of the dialog box.</span></span> <span data-ttu-id="7da23-136">Para obtener más información, vea [**Language**](language-statement.md).</span><span class="sxs-lookup"><span data-stu-id="7da23-136">For more information, see [**LANGUAGE**](language-statement.md).</span></span>                                                                                                |
| <span data-ttu-id="7da23-137"> *NombreMenú* de menú</span><span class="sxs-lookup"><span data-stu-id="7da23-137">**MENU** *menuname*</span></span>                                              | <span data-ttu-id="7da23-138">Menú que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="7da23-138">Menu to be used.</span></span> <span data-ttu-id="7da23-139">Este valor es el nombre del menú o su identificador entero.</span><span class="sxs-lookup"><span data-stu-id="7da23-139">This value is either the name of the menu or its integer identifier.</span></span>                                                                                                        |
| <span data-ttu-id="7da23-140">[](style-statement.md) *Estilos* de estilo</span><span class="sxs-lookup"><span data-stu-id="7da23-140">[**STYLE**](style-statement.md) *styles*</span></span>                        | <span data-ttu-id="7da23-141">Estilos del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="7da23-141">Styles of the dialog box.</span></span> <span data-ttu-id="7da23-142">Para obtener más información, vea [**Style**](style-statement.md).</span><span class="sxs-lookup"><span data-stu-id="7da23-142">For more information, see [**STYLE**](style-statement.md).</span></span>                                                                                                        |
| <span data-ttu-id="7da23-143">[**Versión**](version-statement.md) *DWORD*</span><span class="sxs-lookup"><span data-stu-id="7da23-143">[**VERSION**](version-statement.md) *dword*</span></span>                     | <span data-ttu-id="7da23-144">Valor **DWORD** definido por el usuario.</span><span class="sxs-lookup"><span data-stu-id="7da23-144">User-defined **DWORD** value.</span></span> <span data-ttu-id="7da23-145">Esta instrucción está pensada para su uso por parte de herramientas de recursos adicionales y el sistema no la utiliza.</span><span class="sxs-lookup"><span data-stu-id="7da23-145">This statement is intended for use by additional resource tools and is not used by the system.</span></span> <span data-ttu-id="7da23-146">Para obtener más información, vea [**versión**](version-statement.md).</span><span class="sxs-lookup"><span data-stu-id="7da23-146">For more information, see [**VERSION**](version-statement.md).</span></span> |



 

</dd> </dl>

<span data-ttu-id="7da23-147">Algunos atributos también se admiten por razones de compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="7da23-147">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="7da23-148">Para obtener más información, vea [atributos comunes de recursos](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="7da23-148">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7da23-149">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7da23-149">Remarks</span></span>

<span data-ttu-id="7da23-150">La función [**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits) devuelve las unidades base de cuadro de diálogo en píxeles.</span><span class="sxs-lookup"><span data-stu-id="7da23-150">The [**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits) function returns the dialog base units in pixels.</span></span> <span data-ttu-id="7da23-151">El significado exacto de las coordenadas depende del estilo definido por la instrucción de la opción de [**estilo**](style-statement.md) .</span><span class="sxs-lookup"><span data-stu-id="7da23-151">The exact meaning of the coordinates depends on the style defined by the [**STYLE**](style-statement.md) option statement.</span></span> <span data-ttu-id="7da23-152">En el caso de los cuadros de diálogo de estilo secundario, las coordenadas son relativas al origen de la ventana primaria, a menos que el cuadro de diálogo tenga el estilo **DS \_ ABSALIGN**; en ese caso, las coordenadas son relativas al origen de la pantalla de presentación.</span><span class="sxs-lookup"><span data-stu-id="7da23-152">For child-style dialog boxes, the coordinates are relative to the origin of the parent window, unless the dialog box has the style **DS\_ABSALIGN**; in that case, the coordinates are relative to the origin of the display screen.</span></span>

<span data-ttu-id="7da23-153">No use el estilo **\_ secundario WS** con un cuadro de diálogo modal.</span><span class="sxs-lookup"><span data-stu-id="7da23-153">Do not use the **WS\_CHILD** style with a modal dialog box.</span></span> <span data-ttu-id="7da23-154">La función [**DialogBox**](/windows/win32/api/winuser/nf-winuser-dialogboxa) siempre deshabilita el elemento primario/propietario del cuadro de diálogo que se acaba de crear.</span><span class="sxs-lookup"><span data-stu-id="7da23-154">The [**DialogBox**](/windows/win32/api/winuser/nf-winuser-dialogboxa) function always disables the parent/owner of the newly created dialog box.</span></span> <span data-ttu-id="7da23-155">Cuando una ventana primaria está deshabilitada, sus ventanas secundarias se deshabilitan implícitamente.</span><span class="sxs-lookup"><span data-stu-id="7da23-155">When a parent window is disabled, its child windows are implicitly disabled.</span></span> <span data-ttu-id="7da23-156">Dado que la ventana primaria del cuadro de diálogo de estilo secundario está deshabilitada, el cuadro de diálogo de estilo secundario también es.</span><span class="sxs-lookup"><span data-stu-id="7da23-156">Since the parent window of the child-style dialog box is disabled, the child-style dialog box is too.</span></span>

<span data-ttu-id="7da23-157">Si un cuadro de diálogo tiene el estilo **\_ ABSALIGN de DS** , las coordenadas del cuadro de diálogo de la esquina superior izquierda son relativas al origen de la pantalla en lugar de a la esquina superior izquierda de la ventana primaria.</span><span class="sxs-lookup"><span data-stu-id="7da23-157">If a dialog box has the **DS\_ABSALIGN** style, the dialog coordinates for its upper-left corner are relative to the screen origin instead of to the upper-left corner of the parent window.</span></span> <span data-ttu-id="7da23-158">Normalmente se utiliza este estilo cuando se desea que el cuadro de diálogo se inicie en una parte específica de la pantalla, independientemente de dónde pueda estar la ventana primaria en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="7da23-158">You would typically use this style when you wanted the dialog box to start in a specific part of the display no matter where the parent window may be on the screen.</span></span>

<span data-ttu-id="7da23-159">También se puede usar el cuadro de **diálogo** nombre como parámetro de nombre de clase para la función [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) con el fin de crear una ventana con atributos de cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="7da23-159">The name **DIALOG** can also be used as the class-name parameter to the [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) function to create a window with dialog-box attributes.</span></span>

## <a name="examples"></a><span data-ttu-id="7da23-160">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="7da23-160">Examples</span></span>

<span data-ttu-id="7da23-161">A continuación se muestra el uso de la instrucción **Dialog** :</span><span class="sxs-lookup"><span data-stu-id="7da23-161">The following demonstrates the usage of the **DIALOG** statement:</span></span>

``` syntax
#include <windows.h>

ErrorDialog DIALOG  10, 10, 300, 110
STYLE WS_POPUP | WS_BORDER
CAPTION "Error!" 
{
    CTEXT "Select One:", 1, 10, 10, 280, 12
    PUSHBUTTON "&Retry", 2, 75, 30, 60, 12
    PUSHBUTTON "&Abort", 3, 75, 50, 60, 12
    PUSHBUTTON "&Ignore", 4, 75, 80, 60, 12
}
```

## <a name="see-also"></a><span data-ttu-id="7da23-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="7da23-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7da23-163">Usar cuadros de diálogo</span><span class="sxs-lookup"><span data-stu-id="7da23-163">Using Dialog Boxes</span></span>](../dlgbox/using-dialog-boxes.md)
</dt> <dt>

[<span data-ttu-id="7da23-164">**ACELERADORES**</span><span class="sxs-lookup"><span data-stu-id="7da23-164">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="7da23-165">**SUS**</span><span class="sxs-lookup"><span data-stu-id="7da23-165">**CHARACTERISTICS**</span></span>](characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="7da23-166">**CONTROL**</span><span class="sxs-lookup"><span data-stu-id="7da23-166">**CONTROL**</span></span>](control-control.md)
</dt> <dt>

[<span data-ttu-id="7da23-167">**CreateDialog**</span><span class="sxs-lookup"><span data-stu-id="7da23-167">**CreateDialog**</span></span>](/windows/win32/api/winuser/nf-winuser-createdialoga)
</dt> <dt>

[<span data-ttu-id="7da23-168">**CreateWindow**</span><span class="sxs-lookup"><span data-stu-id="7da23-168">**CreateWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[<span data-ttu-id="7da23-169">**DialogBox**</span><span class="sxs-lookup"><span data-stu-id="7da23-169">**DialogBox**</span></span>](/windows/win32/api/winuser/nf-winuser-dialogboxa)
</dt> <dt>

[<span data-ttu-id="7da23-170">**GetDialogBaseUnits**</span><span class="sxs-lookup"><span data-stu-id="7da23-170">**GetDialogBaseUnits**</span></span>](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[<span data-ttu-id="7da23-171">**MÓDULO**</span><span class="sxs-lookup"><span data-stu-id="7da23-171">**LANGUAGE**</span></span>](language-statement.md)
</dt> <dt>

[<span data-ttu-id="7da23-172">**MENU**</span><span class="sxs-lookup"><span data-stu-id="7da23-172">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="7da23-173">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="7da23-173">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="7da23-174">**STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="7da23-174">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> <dt>

[<span data-ttu-id="7da23-175">**Versión**</span><span class="sxs-lookup"><span data-stu-id="7da23-175">**VERSION**</span></span>](version-statement.md)
</dt> </dl>

 

 
