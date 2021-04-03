---
title: Mensaje EM_SETIMEOPTIONS (RichEdit. h)
description: Establece las opciones del editor de métodos de entrada (IME).
ms.assetid: 8a72ee1c-f6b8-44eb-b8df-57cd834db326
keywords:
- EM_SETIMEOPTIONS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SETIMEOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59be3148bd00abd998af200368f2ed77ad3ff911
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905363"
---
# <a name="em_setimeoptions-message"></a><span data-ttu-id="42105-104">\_Mensaje SETIMEOPTIONS em</span><span class="sxs-lookup"><span data-stu-id="42105-104">EM\_SETIMEOPTIONS message</span></span>

<span data-ttu-id="42105-105">Establece las opciones del editor de métodos de entrada (IME).</span><span class="sxs-lookup"><span data-stu-id="42105-105">Sets the Input Method Editor (IME) options.</span></span>

> [!Note]  
> <span data-ttu-id="42105-106">Este mensaje solo se admite en las versiones en idioma asiático de Microsoft Rich Edit 1,0.</span><span class="sxs-lookup"><span data-stu-id="42105-106">This message is supported only in Asian-language versions of Microsoft Rich Edit 1.0.</span></span> <span data-ttu-id="42105-107">No se admite en las versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="42105-107">It is not supported in any later versions.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="42105-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="42105-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42105-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="42105-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="42105-110">Especifica uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="42105-110">Specifies one of the following values.</span></span>



| <span data-ttu-id="42105-111">Value</span><span class="sxs-lookup"><span data-stu-id="42105-111">Value</span></span>                                                                                                                                             | <span data-ttu-id="42105-112">Significado</span><span class="sxs-lookup"><span data-stu-id="42105-112">Meaning</span></span>                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="ECOOP_SET"></span><span id="ecoop_set"></span><dl> <span data-ttu-id="42105-113"><dt>**conjunto de ECOOP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="42105-113"><dt>**ECOOP\_SET**</dt></span></span> </dl> | <span data-ttu-id="42105-114">Establece las opciones en las especificadas por *lParam*.</span><span class="sxs-lookup"><span data-stu-id="42105-114">Sets the options to those specified by *lParam*.</span></span><br/>                             |
| <span id="ECOOP_OR"></span><span id="ecoop_or"></span><dl> <span data-ttu-id="42105-115"><dt>**ECOOP \_ o**</dt></span><span class="sxs-lookup"><span data-stu-id="42105-115"><dt>**ECOOP\_OR**</dt></span></span> </dl>    | <span data-ttu-id="42105-116">Combina las opciones especificadas con las opciones actuales.</span><span class="sxs-lookup"><span data-stu-id="42105-116">Combines the specified options with the current options.</span></span><br/>                     |
| <span id="ECOOP_AND"></span><span id="ecoop_and"></span><dl> <span data-ttu-id="42105-117"><dt>**ECOOP \_ y**</dt></span><span class="sxs-lookup"><span data-stu-id="42105-117"><dt>**ECOOP\_AND**</dt></span></span> </dl> | <span data-ttu-id="42105-118">Conserva solo las opciones actuales que también especifica *lParam*.</span><span class="sxs-lookup"><span data-stu-id="42105-118">Retains only those current options that are also specified by *lParam*.</span></span><br/>      |
| <span id="ECOOP_XOR"></span><span id="ecoop_xor"></span><dl> <span data-ttu-id="42105-119"><dt>**ECOOP \_ XOR**</dt></span><span class="sxs-lookup"><span data-stu-id="42105-119"><dt>**ECOOP\_XOR**</dt></span></span> </dl> | <span data-ttu-id="42105-120">Lógicamente exclusivas o las opciones actuales con las especificadas por *lParam.*</span><span class="sxs-lookup"><span data-stu-id="42105-120">Logically exclusive OR the current options with those specified by *lParam.*</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="42105-121">*lParam*</span><span class="sxs-lookup"><span data-stu-id="42105-121">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="42105-122">Especifica uno o más de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="42105-122">Specifies one of more of the following values.</span></span>



| <span data-ttu-id="42105-123">Value</span><span class="sxs-lookup"><span data-stu-id="42105-123">Value</span></span>                                                                                                                                                                                 | <span data-ttu-id="42105-124">Significado</span><span class="sxs-lookup"><span data-stu-id="42105-124">Meaning</span></span>                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="IMF_CLOSESTATUSWINDOW"></span><span id="imf_closestatuswindow"></span><dl> <span data-ttu-id="42105-125"><dt>**CLOSESTATUSWINDOW de IMF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="42105-125"><dt>**IMF\_CLOSESTATUSWINDOW**</dt></span></span> </dl> | <span data-ttu-id="42105-126">Cierra la ventana de estado de IME cuando el control recibe el foco de entrada.</span><span class="sxs-lookup"><span data-stu-id="42105-126">Closes the IME status window when the control receives the input focus.</span></span><br/>                                                                                                               |
| <span id="IMF_FORCEACTIVE"></span><span id="imf_forceactive"></span><dl> <span data-ttu-id="42105-127"><dt>**FORCEACTIVE de IMF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="42105-127"><dt>**IMF\_FORCEACTIVE**</dt></span></span> </dl>                   | <span data-ttu-id="42105-128">Activa el IME cuando el control recibe el foco de entrada.</span><span class="sxs-lookup"><span data-stu-id="42105-128">Activates the IME when the control receives the input focus.</span></span><br/>                                                                                                                          |
| <span id="IMF_FORCEDISABLE"></span><span id="imf_forcedisable"></span><dl> <span data-ttu-id="42105-129"><dt>**FORCEDISABLE de IMF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="42105-129"><dt>**IMF\_FORCEDISABLE**</dt></span></span> </dl>                | <span data-ttu-id="42105-130">Deshabilita el IME cuando el control recibe el foco de entrada.</span><span class="sxs-lookup"><span data-stu-id="42105-130">Disables the IME when the control receives the input focus.</span></span><br/>                                                                                                                           |
| <span id="IMF_FORCEENABLE"></span><span id="imf_forceenable"></span><dl> <span data-ttu-id="42105-131"><dt>**FORCEENABLE de IMF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="42105-131"><dt>**IMF\_FORCEENABLE**</dt></span></span> </dl>                   | <span data-ttu-id="42105-132">Habilita el IME cuando el control recibe el foco de entrada.</span><span class="sxs-lookup"><span data-stu-id="42105-132">Enables the IME when the control receives the input focus.</span></span><br/>                                                                                                                            |
| <span id="IMF_FORCEINACTIVE"></span><span id="imf_forceinactive"></span><dl> <span data-ttu-id="42105-133"><dt>**FORCEINACTIVE de IMF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="42105-133"><dt>**IMF\_FORCEINACTIVE**</dt></span></span> </dl>             | <span data-ttu-id="42105-134">Desactiva el IME cuando el control recibe el foco de entrada.</span><span class="sxs-lookup"><span data-stu-id="42105-134">Inactivates the IME when the control receives the input focus.</span></span><br/>                                                                                                                        |
| <span id="IMF_FORCENONE"></span><span id="imf_forcenone"></span><dl> <span data-ttu-id="42105-135"><dt>**FORCENONE de IMF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="42105-135"><dt>**IMF\_FORCENONE**</dt></span></span> </dl>                         | <span data-ttu-id="42105-136">Deshabilita el control de IME.</span><span class="sxs-lookup"><span data-stu-id="42105-136">Disables IME handling.</span></span><br/>                                                                                                                                                                |
| <span id="IMF_FORCEREMEMBER"></span><span id="imf_forceremember"></span><dl> <span data-ttu-id="42105-137"><dt>**FORCEREMEMBER de IMF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="42105-137"><dt>**IMF\_FORCEREMEMBER**</dt></span></span> </dl>             | <span data-ttu-id="42105-138">Restaura el estado anterior del IME cuando el control recibe el foco de entrada.</span><span class="sxs-lookup"><span data-stu-id="42105-138">Restores the previous IME status when the control receives the input focus.</span></span><br/>                                                                                                           |
| <span id="IMF_MULTIPLEEDIT"></span><span id="imf_multipleedit"></span><dl> <span data-ttu-id="42105-139"><dt>**MULTIPLEEDIT de IMF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="42105-139"><dt>**IMF\_MULTIPLEEDIT**</dt></span></span> </dl>                | <span data-ttu-id="42105-140">Especifica que la cadena de composición no se cancelará o determinará por los cambios de foco.</span><span class="sxs-lookup"><span data-stu-id="42105-140">Specifies that the composition string will not be canceled or determined by focus changes.</span></span> <span data-ttu-id="42105-141">Esto permite que una aplicación tenga cadenas de composición independientes en cada control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="42105-141">This allows an application to have separate composition strings on each rich edit control.</span></span><br/> |
| <span id="IMF_VERTICAL"></span><span id="imf_vertical"></span><dl> <span data-ttu-id="42105-142"><dt>**IMF \_ vertical**</dt></span><span class="sxs-lookup"><span data-stu-id="42105-142"><dt>**IMF\_VERTICAL**</dt></span></span> </dl>                            | <span data-ttu-id="42105-143">Nota utilizada en la edición enriquecida 2,0 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="42105-143">Note used in Rich Edit 2.0 and later.</span></span> <br/>                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42105-144">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="42105-144">Return value</span></span>

<span data-ttu-id="42105-145">Si la operación se realiza correctamente, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="42105-145">If the operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="42105-146">Si se produce un error en la operación, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="42105-146">If the operation fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="42105-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42105-147">Requirements</span></span>



| <span data-ttu-id="42105-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="42105-148">Requirement</span></span> | <span data-ttu-id="42105-149">Value</span><span class="sxs-lookup"><span data-stu-id="42105-149">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="42105-150">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="42105-150">Minimum supported client</span></span><br/> | <span data-ttu-id="42105-151">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="42105-151">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="42105-152">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="42105-152">Minimum supported server</span></span><br/> | <span data-ttu-id="42105-153">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="42105-153">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="42105-154">Encabezado</span><span class="sxs-lookup"><span data-stu-id="42105-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="42105-155"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="42105-155"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42105-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="42105-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42105-157">**\_GETIMEOPTIONS em**</span><span class="sxs-lookup"><span data-stu-id="42105-157">**EM\_GETIMEOPTIONS**</span></span>](em-getimeoptions.md)
</dt> </dl>

 

 





