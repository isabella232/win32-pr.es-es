---
title: Mensaje de EM_REPLACESEL (Winuser. h)
description: Reemplaza el texto seleccionado en un control de edición o un control Rich Edit con el texto especificado.
ms.assetid: 525e6f5a-f52f-4bab-bc76-caa484729897
keywords:
- EM_REPLACESEL controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_REPLACESEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d9745b870a310626a6cbbbddbef118a63c64479
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151149"
---
# <a name="em_replacesel-message"></a><span data-ttu-id="f6649-104">\_Mensaje REPLACESEL em</span><span class="sxs-lookup"><span data-stu-id="f6649-104">EM\_REPLACESEL message</span></span>

<span data-ttu-id="f6649-105">Reemplaza el texto seleccionado en un control de edición o un control Rich Edit con el texto especificado.</span><span class="sxs-lookup"><span data-stu-id="f6649-105">Replaces the selected text in an edit control or a rich edit control with the specified text.</span></span>

## <a name="parameters"></a><span data-ttu-id="f6649-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f6649-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6649-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f6649-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f6649-108">Especifica si se puede deshacer la operación de reemplazo.</span><span class="sxs-lookup"><span data-stu-id="f6649-108">Specifies whether the replacement operation can be undone.</span></span> <span data-ttu-id="f6649-109">Si es **true**, se puede deshacer la operación.</span><span class="sxs-lookup"><span data-stu-id="f6649-109">If this is **TRUE**, the operation can be undone.</span></span> <span data-ttu-id="f6649-110">Si es **false** , la operación no se puede deshacer.</span><span class="sxs-lookup"><span data-stu-id="f6649-110">If this is **FALSE** , the operation cannot be undone.</span></span>

</dd> <dt>

<span data-ttu-id="f6649-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f6649-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f6649-112">Puntero a una cadena terminada en null que contiene el texto de reemplazo.</span><span class="sxs-lookup"><span data-stu-id="f6649-112">A pointer to a null-terminated string containing the replacement text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6649-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f6649-113">Return value</span></span>

<span data-ttu-id="f6649-114">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="f6649-114">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6649-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f6649-115">Remarks</span></span>

<span data-ttu-id="f6649-116">Use el **mensaje \_ REPLACESEL em** para reemplazar solo una parte del texto en un control de edición.</span><span class="sxs-lookup"><span data-stu-id="f6649-116">Use the **EM\_REPLACESEL** message to replace only a portion of the text in an edit control.</span></span> <span data-ttu-id="f6649-117">Para reemplazar todo el texto, use el mensaje de [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) .</span><span class="sxs-lookup"><span data-stu-id="f6649-117">To replace all of the text, use the [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext) message.</span></span>

<span data-ttu-id="f6649-118">Si no hay ninguna selección, el texto de sustitución se inserta en el símbolo de intercalación.</span><span class="sxs-lookup"><span data-stu-id="f6649-118">If there is no selection, the replacement text is inserted at the caret.</span></span>

<span data-ttu-id="f6649-119">**Edición enriquecida:** Compatible con Microsoft Rich Edit 1,0 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="f6649-119">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="f6649-120">Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="f6649-120">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

<span data-ttu-id="f6649-121">En un control Rich Edit, el texto de reemplazo toma el formato del carácter en el símbolo de intercalación o, si hay una selección, del primer carácter de la selección.</span><span class="sxs-lookup"><span data-stu-id="f6649-121">In a rich edit control, the replacement text takes the formatting of the character at the caret or, if there is a selection, of the first character in the selection.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6649-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6649-122">Requirements</span></span>



| <span data-ttu-id="f6649-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6649-123">Requirement</span></span> | <span data-ttu-id="f6649-124">Value</span><span class="sxs-lookup"><span data-stu-id="f6649-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6649-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f6649-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f6649-126">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f6649-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f6649-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f6649-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f6649-128">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f6649-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f6649-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f6649-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6649-130"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f6649-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6649-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="f6649-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6649-132">**SETTEXT de WM \_**</span><span class="sxs-lookup"><span data-stu-id="f6649-132">**WM\_SETTEXT**</span></span>](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

