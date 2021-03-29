---
title: Estructura NORMALMENUITEM
description: Contiene información sobre cada elemento de un recurso de menú que no abre un menú o un submenú. La definición de la estructura que se proporciona aquí solo es para explicación; no se encuentra en ningún archivo de encabezado estándar.
ms.assetid: c1b84264-2d7f-4bc3-8e74-7b921a0bfe30
keywords:
- Menús de la estructura NORMALMENUITEM y otros recursos
topic_type:
- apiref
api_name:
- NORMALMENUITEM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c90efe624346e30483c42f6f8ff51cd6d3550922
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359701"
---
# <a name="normalmenuitem-structure"></a><span data-ttu-id="fa809-105">Estructura NORMALMENUITEM</span><span class="sxs-lookup"><span data-stu-id="fa809-105">NORMALMENUITEM structure</span></span>

<span data-ttu-id="fa809-106">Contiene información sobre cada elemento de un recurso de menú que no abre un menú o un submenú.</span><span class="sxs-lookup"><span data-stu-id="fa809-106">Contains information about each item in a menu resource that does not open a menu or a submenu.</span></span> <span data-ttu-id="fa809-107">La definición de la estructura que se proporciona aquí solo es para explicación; no se encuentra en ningún archivo de encabezado estándar.</span><span class="sxs-lookup"><span data-stu-id="fa809-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa809-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fa809-108">Syntax</span></span>


```C++
typedef struct {
  WORD    resInfo;
  szOrOrd menuText;
} NORMALMENUITEM;
```



## <a name="members"></a><span data-ttu-id="fa809-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="fa809-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="fa809-110">**resInfo**</span><span class="sxs-lookup"><span data-stu-id="fa809-110">**resInfo**</span></span>
</dt> <dd>

<span data-ttu-id="fa809-111">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="fa809-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="fa809-112">El tipo de elemento de menú.</span><span class="sxs-lookup"><span data-stu-id="fa809-112">The type of menu item.</span></span> <span data-ttu-id="fa809-113">Este miembro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="fa809-113">This member can be one of the following values.</span></span>



| <span data-ttu-id="fa809-114">Value</span><span class="sxs-lookup"><span data-stu-id="fa809-114">Value</span></span>                                                                                                                                                                                                       | <span data-ttu-id="fa809-115">Significado</span><span class="sxs-lookup"><span data-stu-id="fa809-115">Meaning</span></span>                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="MFR_END"></span><span id="mfr_end"></span><dl> <span data-ttu-id="fa809-116"><dt>**MFR \_ FINALIZAR**</dt> <dt>0x80</dt></span><span class="sxs-lookup"><span data-stu-id="fa809-116"><dt>**MFR\_END**</dt> <dt>0x80</dt></span></span> </dl>       | <span data-ttu-id="fa809-117">El elemento de menú es el último de este recurso de menú o submenú; Este marcador lo utiliza internamente el sistema.</span><span class="sxs-lookup"><span data-stu-id="fa809-117">The menu item is the last in this submenu or menu resource; this flag is used internally by the system.</span></span><br/> |
| <span id="MFR_POPUP"></span><span id="mfr_popup"></span><dl> <span data-ttu-id="fa809-118"><dt>**MFR \_ EMERGENTE**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="fa809-118"><dt>**MFR\_POPUP**</dt> <dt>0x01</dt></span></span> </dl> | <span data-ttu-id="fa809-119">El elemento de menú abre un menú o un submenú; el sistema utiliza internamente la marca.</span><span class="sxs-lookup"><span data-stu-id="fa809-119">The menu item opens a menu or a submenu; the flag is used internally by the system.</span></span> <br/>                    |



 

</dd> <dt>

<span data-ttu-id="fa809-120">**menuText**</span><span class="sxs-lookup"><span data-stu-id="fa809-120">**menuText**</span></span>
</dt> <dd>

<span data-ttu-id="fa809-121">Tipo: **szOrOrd**</span><span class="sxs-lookup"><span data-stu-id="fa809-121">Type: **szOrOrd**</span></span>

</dd> <dd>

<span data-ttu-id="fa809-122">Una cadena Unicode terminada en null que contiene el texto de este elemento de menú.</span><span class="sxs-lookup"><span data-stu-id="fa809-122">A null-terminated Unicode string that contains the text for this menu item.</span></span> <span data-ttu-id="fa809-123">No hay ningún límite fijo en el tamaño de esta cadena.</span><span class="sxs-lookup"><span data-stu-id="fa809-123">There is no fixed limit on the size of this string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fa809-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fa809-124">Remarks</span></span>

<span data-ttu-id="fa809-125">Hay una estructura **NORMALMENUITEM** para cada elemento de menú que no abre un menú o un submenú.</span><span class="sxs-lookup"><span data-stu-id="fa809-125">There is one **NORMALMENUITEM** structure for each menu item that does not open a menu or a submenu.</span></span> <span data-ttu-id="fa809-126">Indicar el último elemento de menú de un menú estableciendo el miembro **resInfo** en **MFR \_ End**.</span><span class="sxs-lookup"><span data-stu-id="fa809-126">Indicate the last menu item on a menu by setting the **resInfo** member to **MFR\_END**.</span></span>

<span data-ttu-id="fa809-127">Un separador de menús es un tipo especial de elemento de menú que está inactivo, pero aparece como una barra divisoria entre dos elementos de menú activos.</span><span class="sxs-lookup"><span data-stu-id="fa809-127">A menu separator is a special type of menu item that is inactive but appears as a dividing bar between two active menu items.</span></span> <span data-ttu-id="fa809-128">Indicar un separador de menús manteniendo el miembro de **menuText** vacío.</span><span class="sxs-lookup"><span data-stu-id="fa809-128">Indicate a menu separator by leaving the **menuText** member empty.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa809-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa809-129">Requirements</span></span>



| <span data-ttu-id="fa809-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa809-130">Requirement</span></span> | <span data-ttu-id="fa809-131">Value</span><span class="sxs-lookup"><span data-stu-id="fa809-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="fa809-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fa809-132">Minimum supported client</span></span><br/> | <span data-ttu-id="fa809-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="fa809-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="fa809-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fa809-134">Minimum supported server</span></span><br/> | <span data-ttu-id="fa809-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fa809-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="fa809-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="fa809-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="fa809-137">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="fa809-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="fa809-138">**MENUHEADER**</span><span class="sxs-lookup"><span data-stu-id="fa809-138">**MENUHEADER**</span></span>](menuheader.md)
</dt> <dt>

[<span data-ttu-id="fa809-139">**MENUITEMINFO**</span><span class="sxs-lookup"><span data-stu-id="fa809-139">**MENUITEMINFO**</span></span>](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)
</dt> <dt>

[<span data-ttu-id="fa809-140">**POPUPMENUITEM**</span><span class="sxs-lookup"><span data-stu-id="fa809-140">**POPUPMENUITEM**</span></span>](popupmenuitem.md)
</dt> <dt>

<span data-ttu-id="fa809-141">**Vista**</span><span class="sxs-lookup"><span data-stu-id="fa809-141">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="fa809-142">Recursos</span><span class="sxs-lookup"><span data-stu-id="fa809-142">Resources</span></span>](resources.md)
</dt> </dl>

 

 





