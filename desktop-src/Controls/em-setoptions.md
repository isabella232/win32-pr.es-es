---
title: Mensaje EM_SETOPTIONS (RichEdit. h)
description: Establece las opciones de un control Rich Edit.
ms.assetid: 98ef2de9-4c34-45ba-8e8a-eaf505f97f56
keywords:
- EM_SETOPTIONS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SETOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c43dda8268b42dc264a86600826d2a6b550e35c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150199"
---
# <a name="em_setoptions-message"></a><span data-ttu-id="fe41f-104">\_Mensaje SETOPTIONS em</span><span class="sxs-lookup"><span data-stu-id="fe41f-104">EM\_SETOPTIONS message</span></span>

<span data-ttu-id="fe41f-105">Establece las opciones de un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="fe41f-105">Sets the options for a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="fe41f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fe41f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe41f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fe41f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fe41f-108">Especifica la operación, que puede ser uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="fe41f-108">Specifies the operation, which can be one of these values.</span></span>



| <span data-ttu-id="fe41f-109">Value</span><span class="sxs-lookup"><span data-stu-id="fe41f-109">Value</span></span>                                                                                                                                             | <span data-ttu-id="fe41f-110">Significado</span><span class="sxs-lookup"><span data-stu-id="fe41f-110">Meaning</span></span>                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="ECOOP_SET"></span><span id="ecoop_set"></span><dl> <span data-ttu-id="fe41f-111"><dt>**conjunto de ECOOP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fe41f-111"><dt>**ECOOP\_SET**</dt></span></span> </dl> | <span data-ttu-id="fe41f-112">Establece las opciones en las especificadas por *lParam*.</span><span class="sxs-lookup"><span data-stu-id="fe41f-112">Sets the options to those specified by *lParam*.</span></span><br/>                             |
| <span id="ECOOP_OR"></span><span id="ecoop_or"></span><dl> <span data-ttu-id="fe41f-113"><dt>**ECOOP \_ o**</dt></span><span class="sxs-lookup"><span data-stu-id="fe41f-113"><dt>**ECOOP\_OR**</dt></span></span> </dl>    | <span data-ttu-id="fe41f-114">Combina las opciones especificadas con las opciones actuales.</span><span class="sxs-lookup"><span data-stu-id="fe41f-114">Combines the specified options with the current options.</span></span><br/>                     |
| <span id="ECOOP_AND"></span><span id="ecoop_and"></span><dl> <span data-ttu-id="fe41f-115"><dt>**ECOOP \_ y**</dt></span><span class="sxs-lookup"><span data-stu-id="fe41f-115"><dt>**ECOOP\_AND**</dt></span></span> </dl> | <span data-ttu-id="fe41f-116">Conserva solo las opciones actuales que también especifica *lParam*.</span><span class="sxs-lookup"><span data-stu-id="fe41f-116">Retains only those current options that are also specified by *lParam*.</span></span><br/>      |
| <span id="ECOOP_XOR"></span><span id="ecoop_xor"></span><dl> <span data-ttu-id="fe41f-117"><dt>**ECOOP \_ XOR**</dt></span><span class="sxs-lookup"><span data-stu-id="fe41f-117"><dt>**ECOOP\_XOR**</dt></span></span> </dl> | <span data-ttu-id="fe41f-118">Lógicamente exclusivas o las opciones actuales con las especificadas por *lParam*.</span><span class="sxs-lookup"><span data-stu-id="fe41f-118">Logically exclusive OR the current options with those specified by *lParam*.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="fe41f-119">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fe41f-119">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fe41f-120">Especifica uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="fe41f-120">Specifies one or more of the following values.</span></span>



| <span data-ttu-id="fe41f-121">Value</span><span class="sxs-lookup"><span data-stu-id="fe41f-121">Value</span></span>                                                                                                                                                                                 | <span data-ttu-id="fe41f-122">Significado</span><span class="sxs-lookup"><span data-stu-id="fe41f-122">Meaning</span></span>                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="ECO_AUTOWORDSELECTION"></span><span id="eco_autowordselection"></span><dl> <span data-ttu-id="fe41f-123"><dt>**AUTOWORDSELECTION de ECO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fe41f-123"><dt>**ECO\_AUTOWORDSELECTION**</dt></span></span> </dl> | <span data-ttu-id="fe41f-124">Selección automática de palabra al hacer doble clic.</span><span class="sxs-lookup"><span data-stu-id="fe41f-124">Automatic selection of word on double-click.</span></span><br/>                                                                           |
| <span id="ECO_AUTOVSCROLL"></span><span id="eco_autovscroll"></span><dl> <span data-ttu-id="fe41f-125"><dt>**AUTOVSCROLL de ECO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fe41f-125"><dt>**ECO\_AUTOVSCROLL**</dt></span></span> </dl>                   | <span data-ttu-id="fe41f-126">Igual que el estilo [**\_ AUTOVSCROLL**](rich-edit-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="fe41f-126">Same as [**ES\_AUTOVSCROLL**](rich-edit-control-styles.md) style.</span></span><br/>                                      |
| <span id="ECO_AUTOHSCROLL"></span><span id="eco_autohscroll"></span><dl> <span data-ttu-id="fe41f-127"><dt>**AUTOHSCROLL de ECO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fe41f-127"><dt>**ECO\_AUTOHSCROLL**</dt></span></span> </dl>                   | <span data-ttu-id="fe41f-128">Igual que el estilo [**\_ AUTOHSCROLL**](rich-edit-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="fe41f-128">Same as [**ES\_AUTOHSCROLL**](rich-edit-control-styles.md) style.</span></span><br/>                                      |
| <span id="ECO_NOHIDESEL"></span><span id="eco_nohidesel"></span><dl> <span data-ttu-id="fe41f-129"><dt>**NOHIDESEL de ECO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fe41f-129"><dt>**ECO\_NOHIDESEL**</dt></span></span> </dl>                         | <span data-ttu-id="fe41f-130">Igual que el estilo [**\_ NOHIDESEL**](rich-edit-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="fe41f-130">Same as [**ES\_NOHIDESEL**](rich-edit-control-styles.md) style.</span></span><br/>                                          |
| <span id="ECO_READONLY"></span><span id="eco_readonly"></span><dl> <span data-ttu-id="fe41f-131"><dt>**\_solo lectura de eco**</dt></span><span class="sxs-lookup"><span data-stu-id="fe41f-131"><dt>**ECO\_READONLY**</dt></span></span> </dl>                            | <span data-ttu-id="fe41f-132">Igual que el estilo de [**\_ solo lectura**](rich-edit-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="fe41f-132">Same as [**ES\_READONLY**](rich-edit-control-styles.md) style.</span></span><br/>                                            |
| <span id="ECO_WANTRETURN"></span><span id="eco_wantreturn"></span><dl> <span data-ttu-id="fe41f-133"><dt>**WANTRETURN de ECO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fe41f-133"><dt>**ECO\_WANTRETURN**</dt></span></span> </dl>                      | <span data-ttu-id="fe41f-134">Igual que el estilo [**\_ WANTRETURN**](rich-edit-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="fe41f-134">Same as [**ES\_WANTRETURN**](rich-edit-control-styles.md) style.</span></span><br/>                                        |
| <span id="ECO_SELECTIONBAR"></span><span id="eco_selectionbar"></span><dl> <span data-ttu-id="fe41f-135"><dt>**SELECTIONBAR de ECO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fe41f-135"><dt>**ECO\_SELECTIONBAR**</dt></span></span> </dl>                | <span data-ttu-id="fe41f-136">Igual que el estilo [**\_ SELECTIONBAR**](rich-edit-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="fe41f-136">Same as [**ES\_SELECTIONBAR**](rich-edit-control-styles.md) style.</span></span><br/>                                    |
| <span id="ECO_VERTICAL"></span><span id="eco_vertical"></span><dl> <span data-ttu-id="fe41f-137"><dt>**\_vertical ecológica**</dt></span><span class="sxs-lookup"><span data-stu-id="fe41f-137"><dt>**ECO\_VERTICAL**</dt></span></span> </dl>                            | <span data-ttu-id="fe41f-138">Igual que el estilo [**\_ vertical**](rich-edit-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="fe41f-138">Same as [**ES\_VERTICAL**](rich-edit-control-styles.md) style.</span></span> <span data-ttu-id="fe41f-139">Disponible solo en versiones de idioma asiático.</span><span class="sxs-lookup"><span data-stu-id="fe41f-139">Available in Asian-language versions only.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe41f-140">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fe41f-140">Return value</span></span>

<span data-ttu-id="fe41f-141">Este mensaje devuelve las opciones actuales del control de edición.</span><span class="sxs-lookup"><span data-stu-id="fe41f-141">This message returns the current options of the edit control.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe41f-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe41f-142">Requirements</span></span>



| <span data-ttu-id="fe41f-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe41f-143">Requirement</span></span> | <span data-ttu-id="fe41f-144">Value</span><span class="sxs-lookup"><span data-stu-id="fe41f-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fe41f-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fe41f-145">Minimum supported client</span></span><br/> | <span data-ttu-id="fe41f-146">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="fe41f-146">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fe41f-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fe41f-147">Minimum supported server</span></span><br/> | <span data-ttu-id="fe41f-148">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="fe41f-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fe41f-149">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fe41f-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe41f-150"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe41f-150"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe41f-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="fe41f-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe41f-152">**Estilos de control Rich Edit**</span><span class="sxs-lookup"><span data-stu-id="fe41f-152">**Rich Edit Control Styles**</span></span>](rich-edit-control-styles.md)
</dt> </dl>

 

 





