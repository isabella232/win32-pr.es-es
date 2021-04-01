---
title: Mensaje de TTM_SETTITLE (commctrl. h)
description: Agrega un icono estándar y una cadena de título a una información sobre herramientas.
ms.assetid: e745a592-eef7-4e0d-8939-a48b52c4ab9f
keywords:
- TTM_SETTITLE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TTM_SETTITLE
- TTM_SETTITLEA
- TTM_SETTITLEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7972a9d40347995e9d641e7fc8706f9ad4c58bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905587"
---
# <a name="ttm_settitle-message"></a><span data-ttu-id="48743-104">TTM \_ SETTITLE</span><span class="sxs-lookup"><span data-stu-id="48743-104">TTM\_SETTITLE message</span></span>

<span data-ttu-id="48743-105">Agrega un icono estándar y una cadena de título a una información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="48743-105">Adds a standard icon and title string to a tooltip.</span></span>

## <a name="parameters"></a><span data-ttu-id="48743-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="48743-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48743-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="48743-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="48743-108">Establezca *wParam* en uno de los valores siguientes para especificar el icono que se va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="48743-108">Set *wParam* to one of the following values to specify the icon to be displayed.</span></span> <span data-ttu-id="48743-109">A partir de Windows XP SP2 y versiones posteriores, este parámetro también puede contener un valor de **HICON** .</span><span class="sxs-lookup"><span data-stu-id="48743-109">As of Windows XP SP2 and later, this parameter can also contain an **HICON** value.</span></span> <span data-ttu-id="48743-110">Se supone que cualquier valor mayor que TTI \_ error es **HICON**.</span><span class="sxs-lookup"><span data-stu-id="48743-110">Any value greater than TTI\_ERROR is assumed to be an **HICON**.</span></span>



| <span data-ttu-id="48743-111">Value</span><span class="sxs-lookup"><span data-stu-id="48743-111">Value</span></span>                                                                                                                                                                      | <span data-ttu-id="48743-112">Significado</span><span class="sxs-lookup"><span data-stu-id="48743-112">Meaning</span></span>                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| <span id="TTI_NONE"></span><span id="tti_none"></span><dl> <span data-ttu-id="48743-113"><dt>**TTI \_ ninguno**</dt></span><span class="sxs-lookup"><span data-stu-id="48743-113"><dt>**TTI\_NONE**</dt></span></span> </dl>                             | <span data-ttu-id="48743-114">Sin icono.</span><span class="sxs-lookup"><span data-stu-id="48743-114">No icon.</span></span><br/>         |
| <span id="TTI_INFO"></span><span id="tti_info"></span><dl> <span data-ttu-id="48743-115"><dt>**información de TTI \_**</dt></span><span class="sxs-lookup"><span data-stu-id="48743-115"><dt>**TTI\_INFO**</dt></span></span> </dl>                             | <span data-ttu-id="48743-116">Icono de información.</span><span class="sxs-lookup"><span data-stu-id="48743-116">Info icon.</span></span><br/>       |
| <span id="TTI_WARNING"></span><span id="tti_warning"></span><dl> <span data-ttu-id="48743-117"><dt>**ADVERTENCIA de TTI \_**</dt></span><span class="sxs-lookup"><span data-stu-id="48743-117"><dt>**TTI\_WARNING**</dt></span></span> </dl>                    | <span data-ttu-id="48743-118">Icono de advertencia</span><span class="sxs-lookup"><span data-stu-id="48743-118">Warning icon</span></span><br/>     |
| <span id="TTI_ERROR"></span><span id="tti_error"></span><dl> <span data-ttu-id="48743-119"><dt>**\_error TTI**</dt></span><span class="sxs-lookup"><span data-stu-id="48743-119"><dt>**TTI\_ERROR**</dt></span></span> </dl>                          | <span data-ttu-id="48743-120">Icono de error</span><span class="sxs-lookup"><span data-stu-id="48743-120">Error Icon</span></span><br/>       |
| <span id="TTI_INFO_LARGE"></span><span id="tti_info_large"></span><dl> <span data-ttu-id="48743-121"><dt>**información de TTI \_ \_ grande**</dt></span><span class="sxs-lookup"><span data-stu-id="48743-121"><dt>**TTI\_INFO\_LARGE**</dt></span></span> </dl>          | <span data-ttu-id="48743-122">Icono de error grande</span><span class="sxs-lookup"><span data-stu-id="48743-122">Large error Icon</span></span><br/> |
| <span id="TTI_WARNING_LARGE"></span><span id="tti_warning_large"></span><dl> <span data-ttu-id="48743-123"><dt>**ADVERTENCIA de TTI \_ \_ grande**</dt></span><span class="sxs-lookup"><span data-stu-id="48743-123"><dt>**TTI\_WARNING\_LARGE**</dt></span></span> </dl> | <span data-ttu-id="48743-124">Icono de error grande</span><span class="sxs-lookup"><span data-stu-id="48743-124">Large error Icon</span></span><br/> |
| <span id="TTI_ERROR_LARGE"></span><span id="tti_error_large"></span><dl> <span data-ttu-id="48743-125"><dt>**ERROR de TTI \_ \_ grande**</dt></span><span class="sxs-lookup"><span data-stu-id="48743-125"><dt>**TTI\_ERROR\_LARGE**</dt></span></span> </dl>       | <span data-ttu-id="48743-126">Icono de error grande</span><span class="sxs-lookup"><span data-stu-id="48743-126">Large error Icon</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="48743-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="48743-127">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="48743-128">Puntero a la cadena de título.</span><span class="sxs-lookup"><span data-stu-id="48743-128">Pointer to the title string.</span></span> <span data-ttu-id="48743-129">Debe asignar un valor a *lParam*.</span><span class="sxs-lookup"><span data-stu-id="48743-129">You must assign a value to *lParam*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48743-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="48743-130">Return value</span></span>

<span data-ttu-id="48743-131">Devuelve **true** si es correcto, **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="48743-131">Returns **TRUE** if successful, **FALSE** if not.</span></span>

## <a name="remarks"></a><span data-ttu-id="48743-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="48743-132">Remarks</span></span>

<span data-ttu-id="48743-133">El título de una información sobre herramientas aparece sobre el texto en una fuente diferente.</span><span class="sxs-lookup"><span data-stu-id="48743-133">The title of a tooltip appears above the text, in a different font.</span></span> <span data-ttu-id="48743-134">No es suficiente tener un título; la información sobre herramientas también debe tener texto o no se muestra.</span><span class="sxs-lookup"><span data-stu-id="48743-134">It is not sufficient to have a title; the tooltip must have text as well, or it is not displayed.</span></span>

<span data-ttu-id="48743-135">Cuando *wParam* contiene un **HICON**, se crea una copia del icono mediante la ventana de información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="48743-135">When *wParam* contains an **HICON**, a copy of the icon is created by the tooltip window.</span></span>

<span data-ttu-id="48743-136">Al llamar **a \_ TTM SETTITLE**, la cadena a la que apunta *lParam* no debe superar 100 **TCHARs** de longitud, incluido el **valor null** final.</span><span class="sxs-lookup"><span data-stu-id="48743-136">When calling **TTM\_SETTITLE**, the string pointed to by *lParam* must not exceed 100 **TCHARs** in length, including the terminating **NULL**.</span></span>

## <a name="examples"></a><span data-ttu-id="48743-137">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="48743-137">Examples</span></span>

<span data-ttu-id="48743-138">En el ejemplo siguiente se muestra cómo agregar un título y un icono del sistema a una información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="48743-138">The following example shows how to add a title and a system icon to a tooltip.</span></span>


```C++
// hwndTip is the handle of the tooltip window.
HICON hIcon = LoadIcon(NULL, IDI_INFORMATION);
SendMessage(hwndTip, TTM_SETTITLE, (WPARAM)hIcon, L"Title text");
DestroyIcon(hIcon);
```



## <a name="requirements"></a><span data-ttu-id="48743-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48743-139">Requirements</span></span>



| <span data-ttu-id="48743-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="48743-140">Requirement</span></span> | <span data-ttu-id="48743-141">Value</span><span class="sxs-lookup"><span data-stu-id="48743-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="48743-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="48743-142">Minimum supported client</span></span><br/> | <span data-ttu-id="48743-143">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="48743-143">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="48743-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="48743-144">Minimum supported server</span></span><br/> | <span data-ttu-id="48743-145">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="48743-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="48743-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="48743-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="48743-147"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="48743-147"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="48743-148">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="48743-148">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="48743-149">**TTM \_ SETTITLEW** (Unicode) y **TTM \_ SETTITLEA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="48743-149">**TTM\_SETTITLEW** (Unicode) and **TTM\_SETTITLEA** (ANSI)</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="48743-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="48743-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48743-151">Acerca de los controles ToolTip</span><span class="sxs-lookup"><span data-stu-id="48743-151">About Tooltip Controls</span></span>](tooltip-controls.md)
</dt> </dl>

 

 





