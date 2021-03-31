---
title: Estructura POPUPMENUITEM
description: Contiene información sobre los elementos de menú en un recurso de menú que abre un menú o un submenú. La definición de la estructura que se proporciona aquí solo es para explicación; no se encuentra en ningún archivo de encabezado estándar.
ms.assetid: cb8faeb2-bca9-4ff5-8f80-d273c3fca504
keywords:
- Menús de la estructura POPUPMENUITEM y otros recursos
topic_type:
- apiref
api_name:
- POPUPMENUITEM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: faa755c2ec7a2b9eeb2f123d7fd3e169b2df1be1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996066"
---
# <a name="popupmenuitem-structure"></a><span data-ttu-id="6aed1-105">Estructura POPUPMENUITEM</span><span class="sxs-lookup"><span data-stu-id="6aed1-105">POPUPMENUITEM structure</span></span>

<span data-ttu-id="6aed1-106">Contiene información sobre los elementos de menú en un recurso de menú que abre un menú o un submenú.</span><span class="sxs-lookup"><span data-stu-id="6aed1-106">Contains information about the menu items in a menu resource that open a menu or a submenu.</span></span> <span data-ttu-id="6aed1-107">La definición de la estructura que se proporciona aquí solo es para explicación; no se encuentra en ningún archivo de encabezado estándar.</span><span class="sxs-lookup"><span data-stu-id="6aed1-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="6aed1-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6aed1-108">Syntax</span></span>


```C++
typedef struct {
  DWORD   type;
  DWORD   state;
  DWORD   id;
  WORD    resInfo;
  szOrOrd menuText;
} POPUPMENUITEM;
```



## <a name="members"></a><span data-ttu-id="6aed1-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="6aed1-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="6aed1-110">**type**</span><span class="sxs-lookup"><span data-stu-id="6aed1-110">**type**</span></span>
</dt> <dd>

<span data-ttu-id="6aed1-111">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="6aed1-111">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="6aed1-112">Describe el elemento de menú.</span><span class="sxs-lookup"><span data-stu-id="6aed1-112">Describes the menu item.</span></span> <span data-ttu-id="6aed1-113">Algunos de los valores que este miembro puede tener incluyen los que se muestran en la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="6aed1-113">Some of the values this member can have include those shown in the list below.</span></span>

<span data-ttu-id="6aed1-114">Además de los valores mostrados, este miembro también puede ser una combinación de los valores de tipo enumerados con el miembro **fType** de la estructura [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) .</span><span class="sxs-lookup"><span data-stu-id="6aed1-114">In addition to the values shown, this member can also be a combination of the type values listed with the **fType** member of the [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) structure.</span></span> <span data-ttu-id="6aed1-115">Los valores de tipo son los que comienzan por MFT \_ .</span><span class="sxs-lookup"><span data-stu-id="6aed1-115">The type values are those that begin with MFT\_.</span></span> <span data-ttu-id="6aed1-116">Para usar estos valores predefinidos \_ \* de tipo MFT, incluya la siguiente instrucción en el archivo. RC:</span><span class="sxs-lookup"><span data-stu-id="6aed1-116">To use these predefined MFT\_\* type values, include the following statement in your .rc file:</span></span>

`#include "winuser.h"`



| <span data-ttu-id="6aed1-117">Value</span><span class="sxs-lookup"><span data-stu-id="6aed1-117">Value</span></span>                                                                                                                                                                                                    | <span data-ttu-id="6aed1-118">Significado</span><span class="sxs-lookup"><span data-stu-id="6aed1-118">Meaning</span></span>                                                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="MF_END"></span><span id="mf_end"></span><dl> <span data-ttu-id="6aed1-119"><dt>**MF \_ FINALIZAR**</dt> <dt>0x80</dt></span><span class="sxs-lookup"><span data-stu-id="6aed1-119"><dt>**MF\_END**</dt> <dt>0x80</dt></span></span> </dl>       | <span data-ttu-id="6aed1-120">El elemento de menú es el último en el menú; el sistema utiliza internamente la marca.</span><span class="sxs-lookup"><span data-stu-id="6aed1-120">The menu item is the last on the menu; the flag is used internally by the system.</span></span> <br/>   |
| <span id="MF_POPUP"></span><span id="mf_popup"></span><dl> <span data-ttu-id="6aed1-121"><dt>**MF \_ EMERGENTE**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="6aed1-121"><dt>**MF\_POPUP**</dt> <dt>0x01</dt></span></span> </dl> | <span data-ttu-id="6aed1-122">El elemento de menú abre un menú o un submenú; el sistema utiliza internamente la marca.</span><span class="sxs-lookup"><span data-stu-id="6aed1-122">The menu item opens a menu or a submenu; the flag is used internally by the system.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="6aed1-123">**state**</span><span class="sxs-lookup"><span data-stu-id="6aed1-123">**state**</span></span>
</dt> <dd>

<span data-ttu-id="6aed1-124">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="6aed1-124">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="6aed1-125">Describe el elemento de menú.</span><span class="sxs-lookup"><span data-stu-id="6aed1-125">Describes the menu item.</span></span> <span data-ttu-id="6aed1-126">Este miembro puede ser una combinación de los valores de estado enumerados con el miembro **dwState** de la estructura [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) .</span><span class="sxs-lookup"><span data-stu-id="6aed1-126">This member can be a combination of the state values listed with the **dwState** member of the [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) structure.</span></span> <span data-ttu-id="6aed1-127">Los valores de estado son los que comienzan por MFS \_ .</span><span class="sxs-lookup"><span data-stu-id="6aed1-127">The state values are those that begin with MFS\_.</span></span> <span data-ttu-id="6aed1-128">Para usar estos \_ \* valores de estado de MFS predefinidos, incluya la siguiente instrucción en el archivo. RC:</span><span class="sxs-lookup"><span data-stu-id="6aed1-128">To use these predefined MFS\_\* state values, include the following statement in your .rc file:</span></span>

`#include "winuser.h"`

</dd> <dt>

<span data-ttu-id="6aed1-129">**id**</span><span class="sxs-lookup"><span data-stu-id="6aed1-129">**id**</span></span>
</dt> <dd>

<span data-ttu-id="6aed1-130">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="6aed1-130">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="6aed1-131">Expresión numérica que identifica el elemento de menú que se pasa en el mensaje del [**\_ comando de WM**](wm-command.md) .</span><span class="sxs-lookup"><span data-stu-id="6aed1-131">A numeric expression that identifies the menu item that is passed in the [**WM\_COMMAND**](wm-command.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="6aed1-132">**resInfo**</span><span class="sxs-lookup"><span data-stu-id="6aed1-132">**resInfo**</span></span>
</dt> <dd>

<span data-ttu-id="6aed1-133">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="6aed1-133">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="6aed1-134">Un conjunto de marcadores de bits que especifican el tipo de elemento de menú.</span><span class="sxs-lookup"><span data-stu-id="6aed1-134">A set of bit flags that specify the type of menu item.</span></span> <span data-ttu-id="6aed1-135">Este miembro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="6aed1-135">This member can be one of the following values.</span></span>



| <span data-ttu-id="6aed1-136">Value</span><span class="sxs-lookup"><span data-stu-id="6aed1-136">Value</span></span>                                                                                                                                                                                                       | <span data-ttu-id="6aed1-137">Significado</span><span class="sxs-lookup"><span data-stu-id="6aed1-137">Meaning</span></span>                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="MFR_END"></span><span id="mfr_end"></span><dl> <span data-ttu-id="6aed1-138"><dt>**MFR \_ FINALIZAR**</dt> <dt>0x80</dt></span><span class="sxs-lookup"><span data-stu-id="6aed1-138"><dt>**MFR\_END**</dt> <dt>0x80</dt></span></span> </dl>       | <span data-ttu-id="6aed1-139">El elemento de menú es el último de este recurso de menú o submenú; Este marcador lo utiliza internamente el sistema.</span><span class="sxs-lookup"><span data-stu-id="6aed1-139">The menu item is the last in this submenu or menu resource; this flag is used internally by the system.</span></span><br/> |
| <span id="MFR_POPUP"></span><span id="mfr_popup"></span><dl> <span data-ttu-id="6aed1-140"><dt>**MFR \_ EMERGENTE**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="6aed1-140"><dt>**MFR\_POPUP**</dt> <dt>0x01</dt></span></span> </dl> | <span data-ttu-id="6aed1-141">El elemento de menú abre un menú o un submenú; el sistema utiliza internamente la marca.</span><span class="sxs-lookup"><span data-stu-id="6aed1-141">The menu item opens a menu or a submenu; the flag is used internally by the system.</span></span><br/>                     |



 

</dd> <dt>

<span data-ttu-id="6aed1-142">**menuText**</span><span class="sxs-lookup"><span data-stu-id="6aed1-142">**menuText**</span></span>
</dt> <dd>

<span data-ttu-id="6aed1-143">Tipo: **szOrOrd**</span><span class="sxs-lookup"><span data-stu-id="6aed1-143">Type: **szOrOrd**</span></span>

</dd> <dd>

<span data-ttu-id="6aed1-144">Una cadena Unicode terminada en null que contiene el texto de este elemento de menú.</span><span class="sxs-lookup"><span data-stu-id="6aed1-144">A null-terminated Unicode string that contains the text for this menu item.</span></span> <span data-ttu-id="6aed1-145">No hay ningún límite fijo en el tamaño de esta cadena.</span><span class="sxs-lookup"><span data-stu-id="6aed1-145">There is no fixed limit on the size of this string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6aed1-146">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6aed1-146">Remarks</span></span>

<span data-ttu-id="6aed1-147">Hay una estructura **POPUPMENUITEM** para cada elemento de menú que abre un menú o un submenú.</span><span class="sxs-lookup"><span data-stu-id="6aed1-147">There is one **POPUPMENUITEM** structure for each menu item that opens a menu or a submenu.</span></span> <span data-ttu-id="6aed1-148">Identifique este tipo de elemento de menú estableciendo el miembro de **tipo** en el **\_ elemento emergente MF** y estableciendo el bit **\_ emergente MFR** en el miembro **resInfo** en 0x0001.</span><span class="sxs-lookup"><span data-stu-id="6aed1-148">Identify this type of menu item by setting the **type** member to **MF\_POPUP** and by setting the **MFR\_POPUP** bit in the **resInfo** member to 0x0001.</span></span> <span data-ttu-id="6aed1-149">En este caso, los datos finales escritos en el recurso de [**\_ menú RT**](/windows/desktop/menurc/resource-types) para el menú o el submenú son la estructura [**MENUHELPID**](menuhelpid.md) .</span><span class="sxs-lookup"><span data-stu-id="6aed1-149">In this case, the final data written to the [**RT\_MENU**](/windows/desktop/menurc/resource-types) resource for the menu or submenu is the [**MENUHELPID**](menuhelpid.md) structure.</span></span> <span data-ttu-id="6aed1-150">**MENUHELPID** contiene una expresión numérica que identifica el menú durante el procesamiento de la [**\_ ayuda de WM**](../shell/wm-help.md) .</span><span class="sxs-lookup"><span data-stu-id="6aed1-150">**MENUHELPID** contains a numeric expression that identifies the menu during [**WM\_HELP**](../shell/wm-help.md) processing.</span></span>

<span data-ttu-id="6aed1-151">Además, cada estructura de **POPUPMENUITEM** que tenga el bit de **\_ menú emergente MFR** establecido en el miembro **ResInfo** irá seguida de una estructura [**MENUHELPID**](menuhelpid.md) más un número adicional de estructuras **POPUPMENUITEM** , una para cada elemento de menú de ese submenú.</span><span class="sxs-lookup"><span data-stu-id="6aed1-151">Additionally, every **POPUPMENUITEM** structure that has the **MFR\_POPUP** bit set in the **resInfo** member will be followed by a [**MENUHELPID**](menuhelpid.md) structure plus an additional number of **POPUPMENUITEM** structures, one for each menu item in that submenu.</span></span> <span data-ttu-id="6aed1-152">La última estructura **POPUPMENUITEM** del submenú tendrá el bit de **\_ final MFR** establecido en el miembro **resInfo** .</span><span class="sxs-lookup"><span data-stu-id="6aed1-152">The last **POPUPMENUITEM** structure in the submenu will have the **MFR\_END** bit set in the **resInfo** member.</span></span> <span data-ttu-id="6aed1-153">Para buscar el final del recurso, busque un **\_ extremo MFR** coincidente para cada **\_ elemento popup MFR** más un **\_ extremo MFR** adicional que coincida con el conjunto más externo de elementos de menú.</span><span class="sxs-lookup"><span data-stu-id="6aed1-153">To find the end of the resource, look for a matching **MFR\_END** for every **MFR\_POPUP** plus one additional **MFR\_END** that matches the outermost set of menu items.</span></span>

<span data-ttu-id="6aed1-154">Indique el último elemento de menú estableciendo el miembro de **tipo** en **MF \_ End**.</span><span class="sxs-lookup"><span data-stu-id="6aed1-154">Indicate the last menu item by setting the **type** member to **MF\_END**.</span></span> <span data-ttu-id="6aed1-155">Dado que puede anidar submenús, puede haber varios niveles de **MF \_ End**.</span><span class="sxs-lookup"><span data-stu-id="6aed1-155">Because you can nest submenus, there can be multiple levels of **MF\_END**.</span></span> <span data-ttu-id="6aed1-156">En estos casos, los elementos de menú son secuenciales.</span><span class="sxs-lookup"><span data-stu-id="6aed1-156">In these instances, the menu items are sequential.</span></span>

## <a name="requirements"></a><span data-ttu-id="6aed1-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6aed1-157">Requirements</span></span>



| <span data-ttu-id="6aed1-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="6aed1-158">Requirement</span></span> | <span data-ttu-id="6aed1-159">Value</span><span class="sxs-lookup"><span data-stu-id="6aed1-159">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="6aed1-160">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6aed1-160">Minimum supported client</span></span><br/> | <span data-ttu-id="6aed1-161">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="6aed1-161">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6aed1-162">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6aed1-162">Minimum supported server</span></span><br/> | <span data-ttu-id="6aed1-163">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6aed1-163">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="6aed1-164">Vea también</span><span class="sxs-lookup"><span data-stu-id="6aed1-164">See also</span></span>

<dl> <dt>

<span data-ttu-id="6aed1-165">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="6aed1-165">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6aed1-166">**MENUHEADER**</span><span class="sxs-lookup"><span data-stu-id="6aed1-166">**MENUHEADER**</span></span>](menuheader.md)
</dt> <dt>

[<span data-ttu-id="6aed1-167">**MENUHELPID**</span><span class="sxs-lookup"><span data-stu-id="6aed1-167">**MENUHELPID**</span></span>](menuhelpid.md)
</dt> <dt>

[<span data-ttu-id="6aed1-168">**MENUITEMINFO**</span><span class="sxs-lookup"><span data-stu-id="6aed1-168">**MENUITEMINFO**</span></span>](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)
</dt> <dt>

[<span data-ttu-id="6aed1-169">**NORMALMENUITEM**</span><span class="sxs-lookup"><span data-stu-id="6aed1-169">**NORMALMENUITEM**</span></span>](normalmenuitem.md)
</dt> <dt>

<span data-ttu-id="6aed1-170">**Vista**</span><span class="sxs-lookup"><span data-stu-id="6aed1-170">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6aed1-171">Recursos</span><span class="sxs-lookup"><span data-stu-id="6aed1-171">Resources</span></span>](resources.md)
</dt> </dl>

 

