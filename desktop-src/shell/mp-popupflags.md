---
description: Representa las opciones disponibles cuando se muestra un menú emergente.
title: Constantes de MP_POPUPFLAGS (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: cc1d9ff0-a03b-4bd3-b481-9b78d20eb771
api_name:
- MPPF_SETFOCUS
- MPPF_INITIALSELECT
- MPPF_NOANIMATE
- MPPF_KEYBOARD
- MPPF_REPOSITION
- MPPF_FORCEZORDER
- MPPF_FINALSELECT
- MPPF_ALIGN_LEFT
- MPPF_ALIGN_RIGHT
- MPPF_TOP
- MPPF_LEFT
- MPPF_RIGHT
- MPPF_BOTTOM
- MPPF_POS_MASK
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5d49f848df7749a732e9f0b849d44a9be56a5c3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154929"
---
# <a name="mp_popupflags-constants"></a><span data-ttu-id="ecc41-103">Constantes de POPUPFLAGS de MP \_</span><span class="sxs-lookup"><span data-stu-id="ecc41-103">MP\_POPUPFLAGS constants</span></span>

<span data-ttu-id="ecc41-104">Representa las opciones disponibles cuando se muestra un menú emergente.</span><span class="sxs-lookup"><span data-stu-id="ecc41-104">Represent options available when displaying a pop-up menu.</span></span>



| <span data-ttu-id="ecc41-105">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="ecc41-105">Constant/value</span></span>                                                                                                                                                                                                                               | <span data-ttu-id="ecc41-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="ecc41-106">Description</span></span>                                                                                                                                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPPF_SETFOCUS"></span><span id="mppf_setfocus"></span><dl> <span data-ttu-id="ecc41-107"><dt>**MPPF \_ SETFOCUS**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="ecc41-107"><dt>**MPPF\_SETFOCUS**</dt> <dt>0x00000001</dt></span></span> </dl>                | <span data-ttu-id="ecc41-108">Dé el foco al menú emergente.</span><span class="sxs-lookup"><span data-stu-id="ecc41-108">Give the pop-up menu the focus.</span></span><br/>                                                                                                                                                                                                                               |
| <span id="MPPF_INITIALSELECT"></span><span id="mppf_initialselect"></span><dl> <span data-ttu-id="ecc41-109"><dt>**MPPF \_ INITIALSELECT**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="ecc41-109"><dt>**MPPF\_INITIALSELECT**</dt> <dt>0x00000002</dt></span></span> </dl> | <span data-ttu-id="ecc41-110">Seleccione el primer elemento del menú emergente.</span><span class="sxs-lookup"><span data-stu-id="ecc41-110">Select the first item in the pop-up menu.</span></span><br/>                                                                                                                                                                                                                     |
| <span id="MPPF_NOANIMATE"></span><span id="mppf_noanimate"></span><dl> <span data-ttu-id="ecc41-111"><dt>**MPPF \_ Noanimar**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="ecc41-111"><dt>**MPPF\_NOANIMATE**</dt> <dt>0x00000004</dt></span></span> </dl>             | <span data-ttu-id="ecc41-112">No use las animaciones del sistema predeterminadas, por ejemplo, la atenuación, al mostrar el menú.</span><span class="sxs-lookup"><span data-stu-id="ecc41-112">Do not use the default system animations, for example, fade-in, when displaying the menu.</span></span><br/>                                                                                                                                                                     |
| <span id="MPPF_KEYBOARD"></span><span id="mppf_keyboard"></span><dl> <span data-ttu-id="ecc41-113"><dt>**MPPF \_ TECLADO**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="ecc41-113"><dt>**MPPF\_KEYBOARD**</dt> <dt>0x00000010</dt></span></span> </dl>                | <span data-ttu-id="ecc41-114">Active el menú mediante un método abreviado de teclado.</span><span class="sxs-lookup"><span data-stu-id="ecc41-114">Activate the menu by a keyboard shortcut.</span></span><br/>                                                                                                                                                                                                                     |
| <span id="MPPF_REPOSITION"></span><span id="mppf_reposition"></span><dl> <span data-ttu-id="ecc41-115"><dt>**MPPF \_ CAMBIAR posición**</dt> de <dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="ecc41-115"><dt>**MPPF\_REPOSITION**</dt> <dt>0x00000020</dt></span></span> </dl>          | <span data-ttu-id="ecc41-116">Mostrar la barra en una posición diferente, en función de los cambios realizados en el menú.</span><span class="sxs-lookup"><span data-stu-id="ecc41-116">Display the bar in a different position, based on changes to the menu.</span></span><br/>                                                                                                                                                                                        |
| <span id="MPPF_FORCEZORDER"></span><span id="mppf_forcezorder"></span><dl> <span data-ttu-id="ecc41-117"><dt>**MPPF \_ FORCEZORDER**</dt> <dt>0x00000040</dt></span><span class="sxs-lookup"><span data-stu-id="ecc41-117"><dt>**MPPF\_FORCEZORDER**</dt> <dt>0x00000040</dt></span></span> </dl>       | <span data-ttu-id="ecc41-118">Reservado.</span><span class="sxs-lookup"><span data-stu-id="ecc41-118">Reserved.</span></span> <span data-ttu-id="ecc41-119">No utilizar.</span><span class="sxs-lookup"><span data-stu-id="ecc41-119">Do not use.</span></span><br/>                                                                                                                                                                                                                                         |
| <span id="MPPF_FINALSELECT"></span><span id="mppf_finalselect"></span><dl> <span data-ttu-id="ecc41-120"><dt>**MPPF \_ FINALSELECT**</dt> <dt>0x00000080</dt></span><span class="sxs-lookup"><span data-stu-id="ecc41-120"><dt>**MPPF\_FINALSELECT**</dt> <dt>0x00000080</dt></span></span> </dl>       | <span data-ttu-id="ecc41-121">Seleccione el último elemento del menú.</span><span class="sxs-lookup"><span data-stu-id="ecc41-121">Select the last item in the menu.</span></span><br/>                                                                                                                                                                                                                             |
| <span id="MPPF_ALIGN_LEFT"></span><span id="mppf_align_left"></span><dl> <span data-ttu-id="ecc41-122"><dt>**MPPF \_ ALINEAr a la \_ izquierda**</dt> <dt>0x02000000</dt></span><span class="sxs-lookup"><span data-stu-id="ecc41-122"><dt>**MPPF\_ALIGN\_LEFT**</dt> <dt>0x02000000</dt></span></span> </dl>         | <span data-ttu-id="ecc41-123">**Windows Vista o posterior**: Alinee el menú emergente a la izquierda del área especificada en el parámetro *prcExclude* de [**ITrackShellMenu::P opup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup) o [**IMenuPopup::P opup**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup).</span><span class="sxs-lookup"><span data-stu-id="ecc41-123">**Windows Vista or later**: Align the pop-up menu to the left of the area specified in the *prcExclude* parameter of [**ITrackShellMenu::Popup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup) or [**IMenuPopup::Popup**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup).</span></span> <span data-ttu-id="ecc41-124">Esta es la alineación predeterminada.</span><span class="sxs-lookup"><span data-stu-id="ecc41-124">This is the default alignment.</span></span><br/> |
| <span id="MPPF_ALIGN_RIGHT"></span><span id="mppf_align_right"></span><dl> <span data-ttu-id="ecc41-125"><dt>**MPPF \_ ALINEAr a la \_ derecha**</dt> <dt>0x04000000</dt></span><span class="sxs-lookup"><span data-stu-id="ecc41-125"><dt>**MPPF\_ALIGN\_RIGHT**</dt> <dt>0x04000000</dt></span></span> </dl>      | <span data-ttu-id="ecc41-126">**Windows Vista o posterior**: Alinee el menú emergente a la derecha del área especificada en el parámetro *prcExclude* de [**ITrackShellMenu::P opup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup) o [**IMenuPopup::P opup**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup).</span><span class="sxs-lookup"><span data-stu-id="ecc41-126">**Windows Vista or later**: Align the pop-up menu to the right of the area specified in the *prcExclude* parameter of [**ITrackShellMenu::Popup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup) or [**IMenuPopup::Popup**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup).</span></span><br/>                               |
| <span id="MPPF_TOP"></span><span id="mppf_top"></span><dl> <span data-ttu-id="ecc41-127"><dt>**MPPF \_**</dt> <dt>0x20000000</dt> superior</span><span class="sxs-lookup"><span data-stu-id="ecc41-127"><dt>**MPPF\_TOP**</dt> <dt>0x20000000</dt></span></span> </dl>                               | <span data-ttu-id="ecc41-128">Coloque el menú emergente encima del punto inicial especificado en el parámetro *PPT* de [**ITrackShellMenu::P opup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup) o [**IMenuPopup::P opup**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup).</span><span class="sxs-lookup"><span data-stu-id="ecc41-128">Position the pop-up menu above the initial point specified in the *ppt* parameter of [**ITrackShellMenu::Popup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup) or [**IMenuPopup::Popup**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup).</span></span><br/>                                                                |
| <span id="MPPF_LEFT"></span><span id="mppf_left"></span><dl> <span data-ttu-id="ecc41-129"><dt>**MPPF \_**</dt> <dt>0x40000000</dt> izquierdo</span><span class="sxs-lookup"><span data-stu-id="ecc41-129"><dt>**MPPF\_LEFT**</dt> <dt>0x40000000</dt></span></span> </dl>                            | <span data-ttu-id="ecc41-130">Coloca el menú emergente a la izquierda del punto inicial.</span><span class="sxs-lookup"><span data-stu-id="ecc41-130">Position the pop-up menu to the left of the initial point.</span></span><br/>                                                                                                                                                                                                    |
| <span id="MPPF_RIGHT"></span><span id="mppf_right"></span><dl> <span data-ttu-id="ecc41-131"><dt>**MPPF \_**</dt> <dt>0x60000000</dt> derecha</span><span class="sxs-lookup"><span data-stu-id="ecc41-131"><dt>**MPPF\_RIGHT**</dt> <dt>0x60000000</dt></span></span> </dl>                         | <span data-ttu-id="ecc41-132">Coloque el menú emergente a la derecha del punto inicial.</span><span class="sxs-lookup"><span data-stu-id="ecc41-132">Position the pop-up menu to the right of the initial point.</span></span><br/>                                                                                                                                                                                                   |
| <span id="MPPF_BOTTOM"></span><span id="mppf_bottom"></span><dl> <span data-ttu-id="ecc41-133"><dt>**MPPF \_ INFERIOR**</dt> <dt>(int) 0x80000000</dt></span><span class="sxs-lookup"><span data-stu-id="ecc41-133"><dt>**MPPF\_BOTTOM**</dt> <dt>(int)0x80000000</dt></span></span> </dl>                 | <span data-ttu-id="ecc41-134">Coloque el menú emergente debajo del punto inicial.</span><span class="sxs-lookup"><span data-stu-id="ecc41-134">Position the pop-up menu below the initial point.</span></span><br/>                                                                                                                                                                                                             |
| <span id="MPPF_POS_MASK"></span><span id="mppf_pos_mask"></span><dl> <span data-ttu-id="ecc41-135"><dt>**MPPF \_ \_Máscara de pos**</dt> <dt>(int) 0xE0000000</dt></span><span class="sxs-lookup"><span data-stu-id="ecc41-135"><dt>**MPPF\_POS\_MASK**</dt> <dt>(int)0xE0000000</dt></span></span> </dl>          | <span data-ttu-id="ecc41-136">Máscara de posición del menú.</span><span class="sxs-lookup"><span data-stu-id="ecc41-136">The menu position mask.</span></span><br/>                                                                                                                                                                                                                                       |



## <a name="remarks"></a><span data-ttu-id="ecc41-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ecc41-137">Remarks</span></span>

<span data-ttu-id="ecc41-138">Estas constantes se definen en el archivo shobjidl. h a partir de Windows XP Service Pack 1 (SP1) y Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ecc41-138">These constants are defined in the Shobjidl.h file beginning in Windows XP Service Pack 1 (SP1) and Windows Server 2003</span></span>

## <a name="requirements"></a><span data-ttu-id="ecc41-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ecc41-139">Requirements</span></span>



| <span data-ttu-id="ecc41-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="ecc41-140">Requirement</span></span> | <span data-ttu-id="ecc41-141">Value</span><span class="sxs-lookup"><span data-stu-id="ecc41-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ecc41-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ecc41-142">Minimum supported client</span></span><br/> | <span data-ttu-id="ecc41-143">Solo aplicaciones de escritorio de Windows XP con SP1 \[\]</span><span class="sxs-lookup"><span data-stu-id="ecc41-143">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ecc41-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ecc41-144">Minimum supported server</span></span><br/> | <span data-ttu-id="ecc41-145">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ecc41-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ecc41-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ecc41-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="ecc41-147"><dt>Shobjidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ecc41-147"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="ecc41-148">IDL</span><span class="sxs-lookup"><span data-stu-id="ecc41-148">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ecc41-149"><dt>Shobjidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ecc41-149"><dt>Shobjidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecc41-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="ecc41-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecc41-151">**IMenuPopup::P opup**</span><span class="sxs-lookup"><span data-stu-id="ecc41-151">**IMenuPopup::Popup**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup)
</dt> <dt>

[<span data-ttu-id="ecc41-152">**ITrackShellMenu::P opup**</span><span class="sxs-lookup"><span data-stu-id="ecc41-152">**ITrackShellMenu::Popup**</span></span>](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup)
</dt> </dl>

 

 




