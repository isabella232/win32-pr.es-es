---
title: Estructura DLGITEMTEMPLATEEX
description: Bloque de texto utilizado por una plantilla de cuadro de diálogo extendido para describir el cuadro de diálogo extendido. Para obtener una descripción del formato de una plantilla de cuadro de diálogo extendido, vea DLGTEMPLATEEX.
ms.assetid: c60fd8db-ee4b-433b-a2fb-68b9a677bac8
keywords:
- Cuadros de diálogo de la estructura DLGITEMTEMPLATEEX
topic_type:
- apiref
api_name:
- DLGITEMTEMPLATEEX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7261fa832e5acfb4ef7d9723bc93b862947ef380
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422591"
---
# <a name="dlgitemtemplateex-structure"></a><span data-ttu-id="f767c-105">Estructura DLGITEMTEMPLATEEX</span><span class="sxs-lookup"><span data-stu-id="f767c-105">DLGITEMTEMPLATEEX structure</span></span>

<span data-ttu-id="f767c-106">Bloque de texto utilizado por una plantilla de cuadro de diálogo extendido para describir el cuadro de diálogo extendido.</span><span class="sxs-lookup"><span data-stu-id="f767c-106">A block of text used by an extended dialog box template to describe the extended dialog box.</span></span> <span data-ttu-id="f767c-107">Para obtener una descripción del formato de una plantilla de cuadro de diálogo extendido, vea [**DLGTEMPLATEEX**](dlgtemplateex.md).</span><span class="sxs-lookup"><span data-stu-id="f767c-107">For a description of the format of an extended dialog box template, see [**DLGTEMPLATEEX**](dlgtemplateex.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f767c-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f767c-108">Syntax</span></span>


```C++
typedef struct {
  DWORD     helpID;
  DWORD     exStyle;
  DWORD     style;
  short     x;
  short     y;
  short     cx;
  short     cy;
  DWORD     id;
  sz_Or_Ord windowClass;
  sz_Or_Ord title;
  WORD      extraCount;
} DLGITEMTEMPLATEEX;
```



## <a name="members"></a><span data-ttu-id="f767c-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="f767c-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="f767c-110">**helpID**</span><span class="sxs-lookup"><span data-stu-id="f767c-110">**helpID**</span></span>
</dt> <dd>

<span data-ttu-id="f767c-111">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="f767c-111">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="f767c-112">Identificador del contexto de ayuda para el control.</span><span class="sxs-lookup"><span data-stu-id="f767c-112">The help context identifier for the control.</span></span> <span data-ttu-id="f767c-113">Cuando el sistema envía un mensaje de [**\_ ayuda de WM**](../shell/wm-help.md) , pasa el valor **helpID** en el miembro **dwContextId** de la estructura [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) .</span><span class="sxs-lookup"><span data-stu-id="f767c-113">When the system sends a [**WM\_HELP**](../shell/wm-help.md) message, it passes the **helpID** value in the **dwContextId** member of the [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) structure.</span></span>

</dd> <dt>

<span data-ttu-id="f767c-114">**exStyle**</span><span class="sxs-lookup"><span data-stu-id="f767c-114">**exStyle**</span></span>
</dt> <dd>

<span data-ttu-id="f767c-115">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="f767c-115">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="f767c-116">Los estilos extendidos de una ventana.</span><span class="sxs-lookup"><span data-stu-id="f767c-116">The extended styles for a window.</span></span> <span data-ttu-id="f767c-117">Este miembro no se utiliza para crear controles en cuadros de diálogo, pero las aplicaciones que usan plantillas de cuadro de diálogo pueden usarlo para crear otros tipos de ventanas.</span><span class="sxs-lookup"><span data-stu-id="f767c-117">This member is not used to create controls in dialog boxes, but applications that use dialog box templates can use it to create other types of windows.</span></span> <span data-ttu-id="f767c-118">Para obtener una lista de valores, vea [**estilos extendidos de ventana**](/windows/desktop/winmsg/extended-window-styles).</span><span class="sxs-lookup"><span data-stu-id="f767c-118">For a list of values, see [**Extended Window Styles**](/windows/desktop/winmsg/extended-window-styles).</span></span>

</dd> <dt>

<span data-ttu-id="f767c-119">**style**</span><span class="sxs-lookup"><span data-stu-id="f767c-119">**style**</span></span>
</dt> <dd>

<span data-ttu-id="f767c-120">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="f767c-120">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="f767c-121">El estilo del control.</span><span class="sxs-lookup"><span data-stu-id="f767c-121">The style of the control.</span></span> <span data-ttu-id="f767c-122">Este miembro puede ser una combinación de [valores de estilo de ventana](/windows/desktop/winmsg/window-styles) ( **como WS \_ Border**) y uno o varios de los valores de estilo de [control](/windows/desktop/Controls/common-control-styles) (por ejemplo, el **\_ PUSHBUTTON de BS** y **es \_ left**).</span><span class="sxs-lookup"><span data-stu-id="f767c-122">This member can be a combination of [window style values](/windows/desktop/winmsg/window-styles) (such as **WS\_BORDER**) and one or more of the [control style values](/windows/desktop/Controls/common-control-styles) (such as **BS\_PUSHBUTTON** and **ES\_LEFT**).</span></span>

</dd> <dt>

<span data-ttu-id="f767c-123">**x**</span><span class="sxs-lookup"><span data-stu-id="f767c-123">**x**</span></span>
</dt> <dd>

<span data-ttu-id="f767c-124">Tipo: **Short**</span><span class="sxs-lookup"><span data-stu-id="f767c-124">Type: **short**</span></span>

</dd> <dd>

<span data-ttu-id="f767c-125">La coordenada x, en unidades de cuadro de diálogo, de la esquina superior izquierda del control.</span><span class="sxs-lookup"><span data-stu-id="f767c-125">The x-coordinate, in dialog box units, of the upper-left corner of the control.</span></span> <span data-ttu-id="f767c-126">Esta coordenada siempre es relativa a la esquina superior izquierda del área cliente del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="f767c-126">This coordinate is always relative to the upper-left corner of the dialog box's client area.</span></span>

</dd> <dt>

<span data-ttu-id="f767c-127">**y**</span><span class="sxs-lookup"><span data-stu-id="f767c-127">**y**</span></span>
</dt> <dd>

<span data-ttu-id="f767c-128">Tipo: **Short**</span><span class="sxs-lookup"><span data-stu-id="f767c-128">Type: **short**</span></span>

</dd> <dd>

<span data-ttu-id="f767c-129">La coordenada y, en unidades de cuadro de diálogo, de la esquina superior izquierda del control.</span><span class="sxs-lookup"><span data-stu-id="f767c-129">The y-coordinate, in dialog box units, of the upper-left corner of the control.</span></span> <span data-ttu-id="f767c-130">Esta coordenada siempre es relativa a la esquina superior izquierda del área cliente del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="f767c-130">This coordinate is always relative to the upper-left corner of the dialog box's client area.</span></span>

</dd> <dt>

<span data-ttu-id="f767c-131">**serie**</span><span class="sxs-lookup"><span data-stu-id="f767c-131">**cx**</span></span>
</dt> <dd>

<span data-ttu-id="f767c-132">Tipo: **Short**</span><span class="sxs-lookup"><span data-stu-id="f767c-132">Type: **short**</span></span>

</dd> <dd>

<span data-ttu-id="f767c-133">Ancho, en unidades de cuadro de diálogo, del control.</span><span class="sxs-lookup"><span data-stu-id="f767c-133">The width, in dialog box units, of the control.</span></span>

</dd> <dt>

<span data-ttu-id="f767c-134">**CY**</span><span class="sxs-lookup"><span data-stu-id="f767c-134">**cy**</span></span>
</dt> <dd>

<span data-ttu-id="f767c-135">Tipo: **Short**</span><span class="sxs-lookup"><span data-stu-id="f767c-135">Type: **short**</span></span>

</dd> <dd>

<span data-ttu-id="f767c-136">Alto, en unidades de cuadro de diálogo, del control.</span><span class="sxs-lookup"><span data-stu-id="f767c-136">The height, in dialog box units, of the control.</span></span>

</dd> <dt>

<span data-ttu-id="f767c-137">**id**</span><span class="sxs-lookup"><span data-stu-id="f767c-137">**id**</span></span>
</dt> <dd>

<span data-ttu-id="f767c-138">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="f767c-138">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="f767c-139">Identificador del control.</span><span class="sxs-lookup"><span data-stu-id="f767c-139">The control identifier.</span></span>

</dd> <dt>

<span data-ttu-id="f767c-140">**windowClass**</span><span class="sxs-lookup"><span data-stu-id="f767c-140">**windowClass**</span></span>
</dt> <dd>

<span data-ttu-id="f767c-141">Tipo: **SZ \_ o \_ Ord**</span><span class="sxs-lookup"><span data-stu-id="f767c-141">Type: **sz\_Or\_Ord**</span></span>

</dd> <dd>

<span data-ttu-id="f767c-142">Matriz de longitud variable de elementos de 16 bits que especifica la clase de ventana del control.</span><span class="sxs-lookup"><span data-stu-id="f767c-142">A variable-length array of 16-bit elements that specifies the window class of the control.</span></span> <span data-ttu-id="f767c-143">Si el primer elemento de esta matriz tiene cualquier valor distinto de 0xFFFF, el sistema trata la matriz como una cadena Unicode terminada en null que especifica el nombre de una clase de ventana registrada.</span><span class="sxs-lookup"><span data-stu-id="f767c-143">If the first element of this array is any value other than 0xFFFF, the system treats the array as a null-terminated Unicode string that specifies the name of a registered window class.</span></span>

<span data-ttu-id="f767c-144">Si el primer elemento es 0xFFFF, la matriz tiene un elemento adicional que especifica el valor ordinal de una clase del sistema predefinida.</span><span class="sxs-lookup"><span data-stu-id="f767c-144">If the first element is 0xFFFF, the array has one additional element that specifies the ordinal value of a predefined system class.</span></span> <span data-ttu-id="f767c-145">El ordinal puede ser uno de los siguientes valores Atom.</span><span class="sxs-lookup"><span data-stu-id="f767c-145">The ordinal can be one of the following atom values.</span></span>



| <span data-ttu-id="f767c-146">Value</span><span class="sxs-lookup"><span data-stu-id="f767c-146">Value</span></span>                                                                             | <span data-ttu-id="f767c-147">Significado</span><span class="sxs-lookup"><span data-stu-id="f767c-147">Meaning</span></span>               |
|-----------------------------------------------------------------------------------|-----------------------|
| <dl> <span data-ttu-id="f767c-148"><dt>0x0080</dt></span><span class="sxs-lookup"><span data-stu-id="f767c-148"><dt>0x0080</dt></span></span> </dl> | <span data-ttu-id="f767c-149">Botón</span><span class="sxs-lookup"><span data-stu-id="f767c-149">Button</span></span><br/>     |
| <dl> <span data-ttu-id="f767c-150"><dt>0x0081</dt></span><span class="sxs-lookup"><span data-stu-id="f767c-150"><dt>0x0081</dt></span></span> </dl> | <span data-ttu-id="f767c-151">Editar</span><span class="sxs-lookup"><span data-stu-id="f767c-151">Edit</span></span><br/>       |
| <dl> <span data-ttu-id="f767c-152"><dt>0x0082</dt></span><span class="sxs-lookup"><span data-stu-id="f767c-152"><dt>0x0082</dt></span></span> </dl> | <span data-ttu-id="f767c-153">estática</span><span class="sxs-lookup"><span data-stu-id="f767c-153">Static</span></span><br/>     |
| <dl> <span data-ttu-id="f767c-154"><dt>0x0083</dt></span><span class="sxs-lookup"><span data-stu-id="f767c-154"><dt>0x0083</dt></span></span> </dl> | <span data-ttu-id="f767c-155">Cuadro de lista</span><span class="sxs-lookup"><span data-stu-id="f767c-155">List box</span></span><br/>   |
| <dl> <span data-ttu-id="f767c-156"><dt>0x0084</dt></span><span class="sxs-lookup"><span data-stu-id="f767c-156"><dt>0x0084</dt></span></span> </dl> | <span data-ttu-id="f767c-157">Barra de desplazamiento</span><span class="sxs-lookup"><span data-stu-id="f767c-157">Scroll bar</span></span><br/> |
| <dl> <span data-ttu-id="f767c-158"><dt>0x0085</dt></span><span class="sxs-lookup"><span data-stu-id="f767c-158"><dt>0x0085</dt></span></span> </dl> | <span data-ttu-id="f767c-159">Cuadro combinado</span><span class="sxs-lookup"><span data-stu-id="f767c-159">Combo box</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="f767c-160">**title**</span><span class="sxs-lookup"><span data-stu-id="f767c-160">**title**</span></span>
</dt> <dd>

<span data-ttu-id="f767c-161">Tipo: **SZ \_ o \_ Ord**</span><span class="sxs-lookup"><span data-stu-id="f767c-161">Type: **sz\_Or\_Ord**</span></span>

</dd> <dd>

<span data-ttu-id="f767c-162">Matriz de longitud variable de elementos de 16 bits que contiene el texto inicial o el identificador de recursos del control.</span><span class="sxs-lookup"><span data-stu-id="f767c-162">A variable-length array of 16-bit elements that contains the initial text or resource identifier of the control.</span></span> <span data-ttu-id="f767c-163">Si el primer elemento de esta matriz es 0xFFFF, la matriz tiene un elemento adicional que especifica el valor ordinal de un recurso, como un icono, en un archivo ejecutable.</span><span class="sxs-lookup"><span data-stu-id="f767c-163">If the first element of this array is 0xFFFF, the array has one additional element that specifies the ordinal value of a resource, such as an icon, in an executable file.</span></span> <span data-ttu-id="f767c-164">Puede usar un identificador de recursos para los controles, como los controles de iconos estáticos, que cargan y muestran un icono u otro recurso en lugar de texto.</span><span class="sxs-lookup"><span data-stu-id="f767c-164">You can use a resource identifier for controls, such as static icon controls, that load and display an icon or other resource rather than text.</span></span> <span data-ttu-id="f767c-165">Si el primer elemento es cualquier valor distinto de 0xFFFF, el sistema trata la matriz como una cadena Unicode terminada en null que especifica el texto inicial.</span><span class="sxs-lookup"><span data-stu-id="f767c-165">If the first element is any value other than 0xFFFF, the system treats the array as a null-terminated Unicode string that specifies the initial text.</span></span>

</dd> <dt>

<span data-ttu-id="f767c-166">**extracount**</span><span class="sxs-lookup"><span data-stu-id="f767c-166">**extraCount**</span></span>
</dt> <dd>

<span data-ttu-id="f767c-167">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="f767c-167">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="f767c-168">El número de bytes de datos de creación que siguen a este miembro.</span><span class="sxs-lookup"><span data-stu-id="f767c-168">The number of bytes of creation data that follow this member.</span></span> <span data-ttu-id="f767c-169">Si este valor es mayor que cero, los datos de creación comienzan en el siguiente límite de **palabras** .</span><span class="sxs-lookup"><span data-stu-id="f767c-169">If this value is greater than zero, the creation data begins at the next **WORD** boundary.</span></span> <span data-ttu-id="f767c-170">Estos datos de creación pueden tener cualquier tamaño y formato.</span><span class="sxs-lookup"><span data-stu-id="f767c-170">This creation data can be of any size and format.</span></span> <span data-ttu-id="f767c-171">El procedimiento de ventana del control debe ser capaz de interpretar los datos.</span><span class="sxs-lookup"><span data-stu-id="f767c-171">The control's window procedure must be able to interpret the data.</span></span> <span data-ttu-id="f767c-172">Cuando el sistema crea el control, pasa un puntero a estos datos en el parámetro *lParam* del mensaje de [**\_ creación de WM**](/windows/desktop/winmsg/wm-create) que envía al control.</span><span class="sxs-lookup"><span data-stu-id="f767c-172">When the system creates the control, it passes a pointer to this data in the *lParam* parameter of the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message that it sends to the control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f767c-173">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f767c-173">Remarks</span></span>

<span data-ttu-id="f767c-174">Una plantilla extendida para un cuadro de diálogo se compone de un encabezado [**DLGTEMPLATEEX**](dlgtemplateex.md) seguido de una estructura **DLGITEMTEMPLATEEX** para cada control del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="f767c-174">An extended template for a dialog box consists of a [**DLGTEMPLATEEX**](dlgtemplateex.md) header followed by a **DLGITEMTEMPLATEEX** structure for each control in the dialog box.</span></span>

<span data-ttu-id="f767c-175">Cada estructura **DLGITEMTEMPLATEEX** debe estar alineada en un límite **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="f767c-175">Each **DLGITEMTEMPLATEEX** structure must be aligned on a **DWORD** boundary.</span></span> <span data-ttu-id="f767c-176">Las matrices de **título** y **windowClass** de longitud variable deben alinearse en los límites de **palabras** .</span><span class="sxs-lookup"><span data-stu-id="f767c-176">The variable-length **windowClass** and **title** arrays must be aligned on **WORD** boundaries.</span></span> <span data-ttu-id="f767c-177">La matriz de datos de creación, si la hay, debe estar alineada en un límite de **palabras** .</span><span class="sxs-lookup"><span data-stu-id="f767c-177">The creation data array, if any, must be aligned on a **WORD** boundary.</span></span>

<span data-ttu-id="f767c-178">Si especifica cadenas de caracteres en las matrices **windowClass** y **title** , debe utilizar cadenas Unicode.</span><span class="sxs-lookup"><span data-stu-id="f767c-178">If you specify character strings in the **windowClass** and **title** arrays, you must use Unicode strings.</span></span> <span data-ttu-id="f767c-179">Utilice la función [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) para generar cadenas Unicode a partir de cadenas ANSI.</span><span class="sxs-lookup"><span data-stu-id="f767c-179">Use the [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) function to generate Unicode strings from ANSI strings.</span></span>

<span data-ttu-id="f767c-180">Los miembros **x**, **y**, **CX** y **CY** especifican valores en las unidades del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="f767c-180">The **x**, **y**, **cx**, and **cy** members specify values in dialog box units.</span></span> <span data-ttu-id="f767c-181">Puede convertir estos valores en unidades de pantalla (píxeles) mediante la función [**MapDialogRect**](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect) .</span><span class="sxs-lookup"><span data-stu-id="f767c-181">You can convert these values to screen units (pixels) by using the [**MapDialogRect**](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f767c-182">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f767c-182">Requirements</span></span>



| <span data-ttu-id="f767c-183">Requisito</span><span class="sxs-lookup"><span data-stu-id="f767c-183">Requirement</span></span> | <span data-ttu-id="f767c-184">Value</span><span class="sxs-lookup"><span data-stu-id="f767c-184">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="f767c-185">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f767c-185">Minimum supported client</span></span><br/> | <span data-ttu-id="f767c-186">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f767c-186">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f767c-187">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f767c-187">Minimum supported server</span></span><br/> | <span data-ttu-id="f767c-188">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f767c-188">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="f767c-189">Vea también</span><span class="sxs-lookup"><span data-stu-id="f767c-189">See also</span></span>

<dl> <dt>

<span data-ttu-id="f767c-190">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="f767c-190">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f767c-191">**CreateDialogIndirect**</span><span class="sxs-lookup"><span data-stu-id="f767c-191">**CreateDialogIndirect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createdialogindirecta)
</dt> <dt>

[<span data-ttu-id="f767c-192">**CreateDialogIndirectParam**</span><span class="sxs-lookup"><span data-stu-id="f767c-192">**CreateDialogIndirectParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama)
</dt> <dt>

[<span data-ttu-id="f767c-193">**CreateWindowEx**</span><span class="sxs-lookup"><span data-stu-id="f767c-193">**CreateWindowEx**</span></span>](/windows/desktop/api/winuser/nf-winuser-createwindowexa)
</dt> <dt>

[<span data-ttu-id="f767c-194">**DialogBoxIndirect**</span><span class="sxs-lookup"><span data-stu-id="f767c-194">**DialogBoxIndirect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta)
</dt> <dt>

[<span data-ttu-id="f767c-195">**DialogBoxIndirectParam**</span><span class="sxs-lookup"><span data-stu-id="f767c-195">**DialogBoxIndirectParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)
</dt> <dt>

[<span data-ttu-id="f767c-196">**DLGTEMPLATEEX**</span><span class="sxs-lookup"><span data-stu-id="f767c-196">**DLGTEMPLATEEX**</span></span>](dlgtemplateex.md)
</dt> <dt>

[<span data-ttu-id="f767c-197">**MapDialogRect**</span><span class="sxs-lookup"><span data-stu-id="f767c-197">**MapDialogRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect)
</dt> <dt>

[<span data-ttu-id="f767c-198">**creación de WM \_**</span><span class="sxs-lookup"><span data-stu-id="f767c-198">**WM\_CREATE**</span></span>](/windows/desktop/winmsg/wm-create)
</dt> <dt>

<span data-ttu-id="f767c-199">**Vista**</span><span class="sxs-lookup"><span data-stu-id="f767c-199">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f767c-200">Cuadros de diálogo</span><span class="sxs-lookup"><span data-stu-id="f767c-200">Dialog Boxes</span></span>](dialog-boxes.md)
</dt> <dt>

<span data-ttu-id="f767c-201">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="f767c-201">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="f767c-202">**MultiByteToWideChar**</span><span class="sxs-lookup"><span data-stu-id="f767c-202">**MultiByteToWideChar**</span></span>](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar)
</dt> <dt>

[<span data-ttu-id="f767c-203">**ayuda de WM \_**</span><span class="sxs-lookup"><span data-stu-id="f767c-203">**WM\_HELP**</span></span>](../shell/wm-help.md)
</dt> </dl>

 

