---
title: Estructura DLGTEMPLATEEX
description: Una plantilla de cuadro de diálogo extendida comienza con un encabezado DLGTEMPLATEEX que describe el cuadro de diálogo y especifica el número de controles en el cuadro de diálogo.
ms.assetid: 9f016cc6-56e2-45d3-8773-1b405fc10d29
keywords:
- Cuadros de diálogo de la estructura DLGTEMPLATEEX
topic_type:
- apiref
api_name:
- DLGTEMPLATEEX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1c3db7127e23e3133e11fe9c1600d37695e3b1ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534738"
---
# <a name="dlgtemplateex-structure"></a><span data-ttu-id="2dd6b-104">Estructura DLGTEMPLATEEX</span><span class="sxs-lookup"><span data-stu-id="2dd6b-104">DLGTEMPLATEEX structure</span></span>

<span data-ttu-id="2dd6b-105">Una plantilla de cuadro de diálogo extendida comienza con un encabezado **DLGTEMPLATEEX** que describe el cuadro de diálogo y especifica el número de controles en el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="2dd6b-105">An extended dialog box template begins with a **DLGTEMPLATEEX** header that describes the dialog box and specifies the number of controls in the dialog box.</span></span> <span data-ttu-id="2dd6b-106">Para cada control de un cuadro de diálogo, una plantilla de cuadro de diálogo extendida tiene un bloque de datos que usa el formato [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) para describir el control.</span><span class="sxs-lookup"><span data-stu-id="2dd6b-106">For each control in a dialog box, an extended dialog box template has a block of data that uses the [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) format to describe the control.</span></span>

<span data-ttu-id="2dd6b-107">La estructura **DLGTEMPLATEEX** no está definida en ningún archivo de encabezado estándar.</span><span class="sxs-lookup"><span data-stu-id="2dd6b-107">The **DLGTEMPLATEEX** structure is not defined in any standard header file.</span></span> <span data-ttu-id="2dd6b-108">Aquí se proporciona la definición de la estructura para explicar el formato de una plantilla extendida para un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="2dd6b-108">The structure definition is provided here to explain the format of an extended template for a dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="2dd6b-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2dd6b-109">Syntax</span></span>


```C++
typedef struct {
  WORD      dlgVer;
  WORD      signature;
  DWORD     helpID;
  DWORD     exStyle;
  DWORD     style;
  WORD      cDlgItems;
  short     x;
  short     y;
  short     cx;
  short     cy;
  sz_Or_Ord menu;
  sz_Or_Ord windowClass;
  WCHAR     title[titleLen];
  WORD      pointsize;
  WORD      weight;
  BYTE      italic;
  BYTE      charset;
  WCHAR     typeface[stringLen];
} DLGTEMPLATEEX;
```



## <a name="members"></a><span data-ttu-id="2dd6b-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="2dd6b-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="2dd6b-111">**dlgVer**</span><span class="sxs-lookup"><span data-stu-id="2dd6b-111">**dlgVer**</span></span>
</dt> <dd>

<span data-ttu-id="2dd6b-112">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="2dd6b-112">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="2dd6b-113">Número de versión de la plantilla de cuadro de diálogo extendido.</span><span class="sxs-lookup"><span data-stu-id="2dd6b-113">The version number of the extended dialog box template.</span></span> <span data-ttu-id="2dd6b-114">Este miembro debe establecerse en 1.</span><span class="sxs-lookup"><span data-stu-id="2dd6b-114">This member must be set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="2dd6b-115">**firma**</span><span class="sxs-lookup"><span data-stu-id="2dd6b-115">**signature**</span></span>
</dt> <dd>

<span data-ttu-id="2dd6b-116">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="2dd6b-116">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="2dd6b-117">Indica si una plantilla es una plantilla de cuadro de diálogo extendida.</span><span class="sxs-lookup"><span data-stu-id="2dd6b-117">Indicates whether a template is an extended dialog box template.</span></span> <span data-ttu-id="2dd6b-118">Si la **firma** es 0xFFFF, se trata de una plantilla de cuadro de diálogo extendida.</span><span class="sxs-lookup"><span data-stu-id="2dd6b-118">If **signature** is 0xFFFF, this is an extended dialog box template.</span></span> <span data-ttu-id="2dd6b-119">En este caso, el miembro **dlgVer** especifica el número de versión de la plantilla.</span><span class="sxs-lookup"><span data-stu-id="2dd6b-119">In this case, the **dlgVer** member specifies the template version number.</span></span> <span data-ttu-id="2dd6b-120">Si **Signature** es cualquier valor distinto de 0xFFFF, se trata de una plantilla de cuadro de diálogo estándar que usa las estructuras [**DLGTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgtemplate) y [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) .</span><span class="sxs-lookup"><span data-stu-id="2dd6b-120">If **signature** is any value other than 0xFFFF, this is a standard dialog box template that uses the [**DLGTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgtemplate) and [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) structures.</span></span>

</dd> <dt>

<span data-ttu-id="2dd6b-121">**helpID**</span><span class="sxs-lookup"><span data-stu-id="2dd6b-121">**helpID**</span></span>
</dt> <dd>

<span data-ttu-id="2dd6b-122">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="2dd6b-122">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="2dd6b-123">Identificador del contexto de ayuda para la ventana del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="2dd6b-123">The help context identifier for the dialog box window.</span></span> <span data-ttu-id="2dd6b-124">Cuando el sistema envía un mensaje de [**\_ ayuda de WM**](../shell/wm-help.md) , pasa este valor en el miembro **WContextId** de la estructura [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) .</span><span class="sxs-lookup"><span data-stu-id="2dd6b-124">When the system sends a [**WM\_HELP**](../shell/wm-help.md) message, it passes this value in the **wContextId** member of the [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) structure.</span></span>

</dd> <dt>

<span data-ttu-id="2dd6b-125">**exStyle**</span><span class="sxs-lookup"><span data-stu-id="2dd6b-125">**exStyle**</span></span>
</dt> <dd>

<span data-ttu-id="2dd6b-126">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="2dd6b-126">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="2dd6b-127">Los estilos extendidos de Windows.</span><span class="sxs-lookup"><span data-stu-id="2dd6b-127">The extended windows styles.</span></span> <span data-ttu-id="2dd6b-128">Este miembro no se usa al crear cuadros de diálogo, pero las aplicaciones que usan plantillas de cuadro de diálogo pueden usarlo para crear otros tipos de ventanas.</span><span class="sxs-lookup"><span data-stu-id="2dd6b-128">This member is not used when creating dialog boxes, but applications that use dialog box templates can use it to create other types of windows.</span></span> <span data-ttu-id="2dd6b-129">Para obtener una lista de valores, vea [**estilos extendidos de ventana**](/windows/desktop/winmsg/extended-window-styles).</span><span class="sxs-lookup"><span data-stu-id="2dd6b-129">For a list of values, see [**Extended Window Styles**](/windows/desktop/winmsg/extended-window-styles).</span></span>

</dd> <dt>

<span data-ttu-id="2dd6b-130">**style**</span><span class="sxs-lookup"><span data-stu-id="2dd6b-130">**style**</span></span>
</dt> <dd>

<span data-ttu-id="2dd6b-131">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="2dd6b-131">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="2dd6b-132">Estilo del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="2dd6b-132">The style of the dialog box.</span></span> <span data-ttu-id="2dd6b-133">Este miembro puede ser una combinación de [valores de estilo de ventana](/windows/desktop/winmsg/window-styles) y [valores de estilo de cuadro de diálogo](dialog-box-styles.md).</span><span class="sxs-lookup"><span data-stu-id="2dd6b-133">This member can be a combination of [window style values](/windows/desktop/winmsg/window-styles) and [dialog box style values](dialog-box-styles.md).</span></span>

<span data-ttu-id="2dd6b-134">Si **Style** incluye el estilo de cuadro de diálogo **\_ SHELLFONT** de **DS \_ SETFONT** o DS, el encabezado **DLGTEMPLATEEX** de la plantilla de cuadro de diálogo extendido contiene cuatro miembros adicionales ( **Pointing**, **Weight**, **Italic** y **Font) que** describen la fuente que se va a usar para el texto en el área cliente y los controles del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="2dd6b-134">If **style** includes the **DS\_SETFONT** or **DS\_SHELLFONT** dialog box style, the **DLGTEMPLATEEX** header of the extended dialog box template contains four additional members ( **pointsize**, **weight**, **italic**, and **typeface**) that describe the font to use for the text in the client area and controls of the dialog box.</span></span> <span data-ttu-id="2dd6b-135">Si es posible, el sistema crea una fuente según los valores especificados en estos miembros.</span><span class="sxs-lookup"><span data-stu-id="2dd6b-135">If possible, the system creates a font according to the values specified in these members.</span></span> <span data-ttu-id="2dd6b-136">A continuación, el sistema envía un mensaje de [**WM \_ SETFONT**](/windows/desktop/winmsg/wm-setfont) al cuadro de diálogo y a cada control para proporcionar un identificador a la fuente.</span><span class="sxs-lookup"><span data-stu-id="2dd6b-136">Then the system sends a [**WM\_SETFONT**](/windows/desktop/winmsg/wm-setfont) message to the dialog box and to each control to provide a handle to the font.</span></span>

<span data-ttu-id="2dd6b-137">Para obtener más información, vea [fuentes de cuadros de diálogo](about-dialog-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="2dd6b-137">For more information, see [Dialog Box Fonts](about-dialog-boxes.md).</span></span>

</dd> <dt>

<span data-ttu-id="2dd6b-138">**cDlgItems**</span><span class="sxs-lookup"><span data-stu-id="2dd6b-138">**cDlgItems**</span></span>
</dt> <dd>

<span data-ttu-id="2dd6b-139">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="2dd6b-139">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="2dd6b-140">Número de controles del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="2dd6b-140">The number of controls in the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="2dd6b-141">**x**</span><span class="sxs-lookup"><span data-stu-id="2dd6b-141">**x**</span></span>
</dt> <dd>

<span data-ttu-id="2dd6b-142">Tipo: **Short**</span><span class="sxs-lookup"><span data-stu-id="2dd6b-142">Type: **short**</span></span>

</dd> <dd>

<span data-ttu-id="2dd6b-143">La coordenada x, en unidades de cuadro de diálogo, de la esquina superior izquierda del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="2dd6b-143">The x-coordinate, in dialog box units, of the upper-left corner of the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="2dd6b-144">**y**</span><span class="sxs-lookup"><span data-stu-id="2dd6b-144">**y**</span></span>
</dt> <dd>

<span data-ttu-id="2dd6b-145">Tipo: **Short**</span><span class="sxs-lookup"><span data-stu-id="2dd6b-145">Type: **short**</span></span>

</dd> <dd>

<span data-ttu-id="2dd6b-146">La coordenada y, en unidades de cuadro de diálogo, de la esquina superior izquierda del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="2dd6b-146">The y-coordinate, in dialog box units, of the upper-left corner of the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="2dd6b-147">**serie**</span><span class="sxs-lookup"><span data-stu-id="2dd6b-147">**cx**</span></span>
</dt> <dd>

<span data-ttu-id="2dd6b-148">Tipo: **Short**</span><span class="sxs-lookup"><span data-stu-id="2dd6b-148">Type: **short**</span></span>

</dd> <dd>

<span data-ttu-id="2dd6b-149">Ancho, en unidades de cuadro de diálogo, del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="2dd6b-149">The width, in dialog box units, of the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="2dd6b-150">**CY**</span><span class="sxs-lookup"><span data-stu-id="2dd6b-150">**cy**</span></span>
</dt> <dd>

<span data-ttu-id="2dd6b-151">Tipo: **Short**</span><span class="sxs-lookup"><span data-stu-id="2dd6b-151">Type: **short**</span></span>

</dd> <dd>

<span data-ttu-id="2dd6b-152">Alto, en unidades de cuadro de diálogo, del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="2dd6b-152">The height, in dialog box units, of the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="2dd6b-153">**MENU**</span><span class="sxs-lookup"><span data-stu-id="2dd6b-153">**menu**</span></span>
</dt> <dd>

<span data-ttu-id="2dd6b-154">Tipo: **SZ \_ o \_ Ord**</span><span class="sxs-lookup"><span data-stu-id="2dd6b-154">Type: **sz\_Or\_Ord**</span></span>

</dd> <dd>

<span data-ttu-id="2dd6b-155">Matriz de longitud variable de elementos de 16 bits que identifica un recurso de menú para el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="2dd6b-155">A variable-length array of 16-bit elements that identifies a menu resource for the dialog box.</span></span> <span data-ttu-id="2dd6b-156">Si el primer elemento de esta matriz es 0x0000, el cuadro de diálogo no tiene ningún menú y la matriz no tiene ningún otro elemento.</span><span class="sxs-lookup"><span data-stu-id="2dd6b-156">If the first element of this array is 0x0000, the dialog box has no menu and the array has no other elements.</span></span> <span data-ttu-id="2dd6b-157">Si el primer elemento es 0xFFFF, la matriz tiene un elemento adicional que especifica el valor ordinal de un recurso de menú en un archivo ejecutable.</span><span class="sxs-lookup"><span data-stu-id="2dd6b-157">If the first element is 0xFFFF, the array has one additional element that specifies the ordinal value of a menu resource in an executable file.</span></span> <span data-ttu-id="2dd6b-158">Si el primer elemento tiene cualquier otro valor, el sistema trata la matriz como una cadena Unicode terminada en null que especifica el nombre de un recurso de menú en un archivo ejecutable.</span><span class="sxs-lookup"><span data-stu-id="2dd6b-158">If the first element has any other value, the system treats the array as a null-terminated Unicode string that specifies the name of a menu resource in an executable file.</span></span>

</dd> <dt>

<span data-ttu-id="2dd6b-159">**windowClass**</span><span class="sxs-lookup"><span data-stu-id="2dd6b-159">**windowClass**</span></span>
</dt> <dd>

<span data-ttu-id="2dd6b-160">Tipo: **SZ \_ o \_ Ord**</span><span class="sxs-lookup"><span data-stu-id="2dd6b-160">Type: **sz\_Or\_Ord**</span></span>

</dd> <dd>

<span data-ttu-id="2dd6b-161">Matriz de longitud variable de elementos de 16 bits que identifica la clase de ventana del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="2dd6b-161">A variable-length array of 16-bit elements that identifies the window class of the dialog box.</span></span> <span data-ttu-id="2dd6b-162">Si el primer elemento de la matriz es 0x0000, el sistema utiliza la clase de cuadro de diálogo predefinida para el cuadro de diálogo y la matriz no tiene ningún otro elemento.</span><span class="sxs-lookup"><span data-stu-id="2dd6b-162">If the first element of the array is 0x0000, the system uses the predefined dialog box class for the dialog box and the array has no other elements.</span></span> <span data-ttu-id="2dd6b-163">Si el primer elemento es 0xFFFF, la matriz tiene un elemento adicional que especifica el valor ordinal de una clase de ventana del sistema predefinida.</span><span class="sxs-lookup"><span data-stu-id="2dd6b-163">If the first element is 0xFFFF, the array has one additional element that specifies the ordinal value of a predefined system window class.</span></span> <span data-ttu-id="2dd6b-164">Si el primer elemento tiene cualquier otro valor, el sistema trata la matriz como una cadena Unicode terminada en null que especifica el nombre de una clase de ventana registrada.</span><span class="sxs-lookup"><span data-stu-id="2dd6b-164">If the first element has any other value, the system treats the array as a null-terminated Unicode string that specifies the name of a registered window class.</span></span>

</dd> <dt>

<span data-ttu-id="2dd6b-165">**title**</span><span class="sxs-lookup"><span data-stu-id="2dd6b-165">**title**</span></span>
</dt> <dd>

<span data-ttu-id="2dd6b-166">Tipo: **WCHAR \[ titleLen \]**</span><span class="sxs-lookup"><span data-stu-id="2dd6b-166">Type: **WCHAR\[titleLen\]**</span></span>

</dd> <dd>

<span data-ttu-id="2dd6b-167">Título del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="2dd6b-167">The title of the dialog box.</span></span> <span data-ttu-id="2dd6b-168">Si el primer elemento de esta matriz es 0x0000, el cuadro de diálogo no tiene ningún título y la matriz no tiene ningún otro elemento.</span><span class="sxs-lookup"><span data-stu-id="2dd6b-168">If the first element of this array is 0x0000, the dialog box has no title and the array has no other elements.</span></span>

</dd> <dt>

<span data-ttu-id="2dd6b-169">**PointSize**</span><span class="sxs-lookup"><span data-stu-id="2dd6b-169">**pointsize**</span></span>
</dt> <dd>

<span data-ttu-id="2dd6b-170">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="2dd6b-170">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="2dd6b-171">Tamaño de punto de la fuente que se va a usar para el texto del cuadro de diálogo y sus controles.</span><span class="sxs-lookup"><span data-stu-id="2dd6b-171">The point size of the font to use for the text in the dialog box and its controls.</span></span>

<span data-ttu-id="2dd6b-172">Este miembro solo está presente si el miembro de **estilo** especifica **DS \_ SETFONT** o **DS \_ SHELLFONT**.</span><span class="sxs-lookup"><span data-stu-id="2dd6b-172">This member is present only if the **style** member specifies **DS\_SETFONT** or **DS\_SHELLFONT**.</span></span>

</dd> <dt>

<span data-ttu-id="2dd6b-173">**weight**</span><span class="sxs-lookup"><span data-stu-id="2dd6b-173">**weight**</span></span>
</dt> <dd>

<span data-ttu-id="2dd6b-174">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="2dd6b-174">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="2dd6b-175">El grosor de la fuente.</span><span class="sxs-lookup"><span data-stu-id="2dd6b-175">The weight of the font.</span></span> <span data-ttu-id="2dd6b-176">Tenga en cuenta que, aunque puede ser cualquiera de los valores enumerados para el miembro **lfWeight** de la estructura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) , cualquier valor que se use se cambiará automáticamente a **FW \_ normal**.</span><span class="sxs-lookup"><span data-stu-id="2dd6b-176">Note that, although this can be any of the values listed for the **lfWeight** member of the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure, any value that is used will be automatically changed to **FW\_NORMAL**.</span></span>

<span data-ttu-id="2dd6b-177">Este miembro solo está presente si el miembro de **estilo** especifica **DS \_ SETFONT** o **DS \_ SHELLFONT**.</span><span class="sxs-lookup"><span data-stu-id="2dd6b-177">This member is present only if the **style** member specifies **DS\_SETFONT** or **DS\_SHELLFONT**.</span></span>

</dd> <dt>

<span data-ttu-id="2dd6b-178">**cursiva**</span><span class="sxs-lookup"><span data-stu-id="2dd6b-178">**italic**</span></span>
</dt> <dd>

<span data-ttu-id="2dd6b-179">Tipo: **byte**</span><span class="sxs-lookup"><span data-stu-id="2dd6b-179">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="2dd6b-180">Indica si la fuente está en cursiva.</span><span class="sxs-lookup"><span data-stu-id="2dd6b-180">Indicates whether the font is italic.</span></span> <span data-ttu-id="2dd6b-181">Si este valor es **true**, la fuente está en cursiva.</span><span class="sxs-lookup"><span data-stu-id="2dd6b-181">If this value is **TRUE**, the font is italic.</span></span>

<span data-ttu-id="2dd6b-182">Este miembro solo está presente si el miembro de **estilo** especifica **DS \_ SETFONT** o **DS \_ SHELLFONT**.</span><span class="sxs-lookup"><span data-stu-id="2dd6b-182">This member is present only if the **style** member specifies **DS\_SETFONT** or **DS\_SHELLFONT**.</span></span>

</dd> <dt>

<span data-ttu-id="2dd6b-183">**charset**</span><span class="sxs-lookup"><span data-stu-id="2dd6b-183">**charset**</span></span>
</dt> <dd>

<span data-ttu-id="2dd6b-184">Tipo: **byte**</span><span class="sxs-lookup"><span data-stu-id="2dd6b-184">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="2dd6b-185">Juego de caracteres que se va a utilizar.</span><span class="sxs-lookup"><span data-stu-id="2dd6b-185">The character set to be used.</span></span> <span data-ttu-id="2dd6b-186">Para obtener más información, vea el miembro **lfcharset** de [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta).</span><span class="sxs-lookup"><span data-stu-id="2dd6b-186">For more information, see the **lfcharset** member of [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta).</span></span>

<span data-ttu-id="2dd6b-187">Este miembro solo está presente si el miembro de **estilo** especifica **DS \_ SETFONT** o **DS \_ SHELLFONT**.</span><span class="sxs-lookup"><span data-stu-id="2dd6b-187">This member is present only if the **style** member specifies **DS\_SETFONT** or **DS\_SHELLFONT**.</span></span>

</dd> <dt>

<span data-ttu-id="2dd6b-188">**tipográfico**</span><span class="sxs-lookup"><span data-stu-id="2dd6b-188">**typeface**</span></span>
</dt> <dd>

<span data-ttu-id="2dd6b-189">Tipo: **WCHAR \[ stringLen \]**</span><span class="sxs-lookup"><span data-stu-id="2dd6b-189">Type: **WCHAR\[stringLen\]**</span></span>

</dd> <dd>

<span data-ttu-id="2dd6b-190">Nombre del tipo de letra de la fuente.</span><span class="sxs-lookup"><span data-stu-id="2dd6b-190">The name of the typeface for the font.</span></span>

<span data-ttu-id="2dd6b-191">Este miembro solo está presente si el miembro de **estilo** especifica **DS \_ SETFONT** o **DS \_ SHELLFONT**.</span><span class="sxs-lookup"><span data-stu-id="2dd6b-191">This member is present only if the **style** member specifies **DS\_SETFONT** or **DS\_SHELLFONT**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2dd6b-192">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2dd6b-192">Remarks</span></span>

<span data-ttu-id="2dd6b-193">Puede usar una plantilla de cuadro de diálogo extendida en lugar de una plantilla de cuadro de diálogo estándar en las funciones [**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama), [**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama), [**CreateDialogIndirect**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirecta)y [**DialogBoxIndirect**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta) .</span><span class="sxs-lookup"><span data-stu-id="2dd6b-193">You can use an extended dialog box template instead of a standard dialog box template in the [**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama), [**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama), [**CreateDialogIndirect**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirecta), and [**DialogBoxIndirect**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta) functions.</span></span>

<span data-ttu-id="2dd6b-194">Seguir el encabezado de **DLGTEMPLATEEX** en una plantilla de cuadro de diálogo extendida es una o varias estructuras [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) que describen los controles del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="2dd6b-194">Following the **DLGTEMPLATEEX** header in an extended dialog box template is one or more [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) structures that describe the controls of the dialog box.</span></span> <span data-ttu-id="2dd6b-195">El miembro **cDlgItems** de la estructura **DLGITEMTEMPLATEEX** especifica el número de estructuras **DLGITEMTEMPLATEEX** que siguen en la plantilla.</span><span class="sxs-lookup"><span data-stu-id="2dd6b-195">The **cDlgItems** member of the **DLGITEMTEMPLATEEX** structure specifies the number of **DLGITEMTEMPLATEEX** structures that follow in the template.</span></span>

<span data-ttu-id="2dd6b-196">Cada estructura [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) de la plantilla debe estar alineada en un límite **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="2dd6b-196">Each [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) structure in the template must be aligned on a **DWORD** boundary.</span></span> <span data-ttu-id="2dd6b-197">Si el miembro de **estilo** especifica el estilo de **DS \_ SETFONT** o **DS \_ SHELLFONT** , la primera estructura de **DLGITEMTEMPLATEEX** comienza en el primer límite **DWORD** después de la cadena de tipo de **letra** .</span><span class="sxs-lookup"><span data-stu-id="2dd6b-197">If the **style** member specifies the **DS\_SETFONT** or **DS\_SHELLFONT** style, the first **DLGITEMTEMPLATEEX** structure begins on the first **DWORD** boundary after the **typeface** string.</span></span> <span data-ttu-id="2dd6b-198">Si no se especifican estos estilos, la primera estructura comienza en el primer límite **DWORD** después de la cadena de **título** .</span><span class="sxs-lookup"><span data-stu-id="2dd6b-198">If these styles are not specified, the first structure begins on the first **DWORD** boundary after the **title** string.</span></span>

<span data-ttu-id="2dd6b-199">Las matrices de **menú**, **windowClass**, **título** y tipo de **letra** se deben alinear en los límites de **palabras** .</span><span class="sxs-lookup"><span data-stu-id="2dd6b-199">The **menu**, **windowClass**, **title**, and **typeface** arrays must be aligned on **WORD** boundaries.</span></span>

<span data-ttu-id="2dd6b-200">Si especifica cadenas de caracteres en las matrices de **menús**, **windowClass**, **title** y tipo de **letra** , debe utilizar cadenas Unicode.</span><span class="sxs-lookup"><span data-stu-id="2dd6b-200">If you specify character strings in the **menu**, **windowClass**, **title**, and **typeface** arrays, you must use Unicode strings.</span></span> <span data-ttu-id="2dd6b-201">Utilice la función [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) para generar estas cadenas Unicode a partir de cadenas ANSI.</span><span class="sxs-lookup"><span data-stu-id="2dd6b-201">Use the [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) function to generate these Unicode strings from ANSI strings.</span></span>

<span data-ttu-id="2dd6b-202">Los miembros **x**, **y**, **CX** y **CY** especifican valores en las unidades del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="2dd6b-202">The **x**, **y**, **cx**, and **cy** members specify values in dialog box units.</span></span> <span data-ttu-id="2dd6b-203">Puede convertir estos valores en unidades de pantalla (píxeles) mediante la función [**MapDialogRect**](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect) .</span><span class="sxs-lookup"><span data-stu-id="2dd6b-203">You can convert these values to screen units (pixels) by using the [**MapDialogRect**](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="2dd6b-204">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2dd6b-204">Requirements</span></span>



| <span data-ttu-id="2dd6b-205">Requisito</span><span class="sxs-lookup"><span data-stu-id="2dd6b-205">Requirement</span></span> | <span data-ttu-id="2dd6b-206">Value</span><span class="sxs-lookup"><span data-stu-id="2dd6b-206">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="2dd6b-207">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2dd6b-207">Minimum supported client</span></span><br/> | <span data-ttu-id="2dd6b-208">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="2dd6b-208">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="2dd6b-209">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2dd6b-209">Minimum supported server</span></span><br/> | <span data-ttu-id="2dd6b-210">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2dd6b-210">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="2dd6b-211">Vea también</span><span class="sxs-lookup"><span data-stu-id="2dd6b-211">See also</span></span>

<dl> <dt>

<span data-ttu-id="2dd6b-212">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="2dd6b-212">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2dd6b-213">**CreateDialogIndirect**</span><span class="sxs-lookup"><span data-stu-id="2dd6b-213">**CreateDialogIndirect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createdialogindirecta)
</dt> <dt>

[<span data-ttu-id="2dd6b-214">**CreateDialogIndirectParam**</span><span class="sxs-lookup"><span data-stu-id="2dd6b-214">**CreateDialogIndirectParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama)
</dt> <dt>

[<span data-ttu-id="2dd6b-215">**DialogBoxIndirect**</span><span class="sxs-lookup"><span data-stu-id="2dd6b-215">**DialogBoxIndirect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta)
</dt> <dt>

[<span data-ttu-id="2dd6b-216">**DialogBoxIndirectParam**</span><span class="sxs-lookup"><span data-stu-id="2dd6b-216">**DialogBoxIndirectParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)
</dt> <dt>

[<span data-ttu-id="2dd6b-217">**DLGITEMTEMPLATEEX**</span><span class="sxs-lookup"><span data-stu-id="2dd6b-217">**DLGITEMTEMPLATEEX**</span></span>](dlgitemtemplateex.md)
</dt> <dt>

[<span data-ttu-id="2dd6b-218">**MapDialogRect**</span><span class="sxs-lookup"><span data-stu-id="2dd6b-218">**MapDialogRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect)
</dt> <dt>

[<span data-ttu-id="2dd6b-219">**WM \_**</span><span class="sxs-lookup"><span data-stu-id="2dd6b-219">**WM\_SETFONT**</span></span>](/windows/desktop/winmsg/wm-setfont)
</dt> <dt>

<span data-ttu-id="2dd6b-220">**Vista**</span><span class="sxs-lookup"><span data-stu-id="2dd6b-220">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2dd6b-221">Cuadros de diálogo</span><span class="sxs-lookup"><span data-stu-id="2dd6b-221">Dialog Boxes</span></span>](dialog-boxes.md)
</dt> <dt>

<span data-ttu-id="2dd6b-222">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="2dd6b-222">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="2dd6b-223">**NDPTECGDI**</span><span class="sxs-lookup"><span data-stu-id="2dd6b-223">**LOGFONT**</span></span>](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> <dt>

[<span data-ttu-id="2dd6b-224">**MultiByteToWideChar**</span><span class="sxs-lookup"><span data-stu-id="2dd6b-224">**MultiByteToWideChar**</span></span>](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar)
</dt> </dl>

 

