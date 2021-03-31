---
title: Mensaje de EM_LINESCROLL (Winuser. h)
description: Desplaza el texto en un control de edición multilínea.
ms.assetid: 5398082d-f1ef-4a3a-9e5a-83cf286adbf1
keywords:
- EM_LINESCROLL controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_LINESCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 646e225ef269ccddca2cdc29caf635d94c1671e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079567"
---
# <a name="em_linescroll-message"></a><span data-ttu-id="db1c6-104">\_Mensaje LINESCROLL em</span><span class="sxs-lookup"><span data-stu-id="db1c6-104">EM\_LINESCROLL message</span></span>

<span data-ttu-id="db1c6-105">Desplaza el texto en un control de edición multilínea.</span><span class="sxs-lookup"><span data-stu-id="db1c6-105">Scrolls the text in a multiline edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="db1c6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="db1c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db1c6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="db1c6-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="db1c6-108">**Controles de edición:** Número de caracteres que se va a desplazar horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="db1c6-108">**Edit controls:** The number of characters to scroll horizontally.</span></span>

<span data-ttu-id="db1c6-109">**Controles Rich Edit:** Este parámetro no se usa; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="db1c6-109">**Rich edit controls:** This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="db1c6-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="db1c6-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="db1c6-111">Número de líneas que se va a desplazar verticalmente.</span><span class="sxs-lookup"><span data-stu-id="db1c6-111">The number of lines to scroll vertically.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db1c6-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="db1c6-112">Return value</span></span>

<span data-ttu-id="db1c6-113">Si el mensaje se envía a un control de edición de varias líneas, el valor devuelto es **true**.</span><span class="sxs-lookup"><span data-stu-id="db1c6-113">If the message is sent to a multiline edit control, the return value is **TRUE**.</span></span>

<span data-ttu-id="db1c6-114">Si el mensaje se envía a un control de edición de una sola línea, el valor devuelto es **false**.</span><span class="sxs-lookup"><span data-stu-id="db1c6-114">If the message is sent to a single-line edit control, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="db1c6-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="db1c6-115">Remarks</span></span>

<span data-ttu-id="db1c6-116">El control no se desplaza verticalmente más allá de la última línea de texto del control de edición.</span><span class="sxs-lookup"><span data-stu-id="db1c6-116">The control does not scroll vertically past the last line of text in the edit control.</span></span> <span data-ttu-id="db1c6-117">Si la línea actual más el número de líneas especificadas por el parámetro *lParam* supera el número total de líneas en el control de edición, el valor se ajusta de modo que la última línea del control de edición se desplaza a la parte superior de la ventana Editar control.</span><span class="sxs-lookup"><span data-stu-id="db1c6-117">If the current line plus the number of lines specified by the *lParam* parameter exceeds the total number of lines in the edit control, the value is adjusted so that the last line of the edit control is scrolled to the top of the edit-control window.</span></span>

<span data-ttu-id="db1c6-118">**Controles de edición:** El **mensaje \_ LINESCROLL em** desplaza el texto vertical u horizontalmente en un control de edición multilínea.</span><span class="sxs-lookup"><span data-stu-id="db1c6-118">**Edit controls:** The **EM\_LINESCROLL** message scrolls the text vertically or horizontally in a multiline edit control.</span></span> <span data-ttu-id="db1c6-119">El **mensaje \_ LINESCROLL em** se puede usar para desplazarse horizontalmente más allá del último carácter de cualquier línea.</span><span class="sxs-lookup"><span data-stu-id="db1c6-119">The **EM\_LINESCROLL** message can be used to scroll horizontally past the last character of any line.</span></span>

<span data-ttu-id="db1c6-120">**Edición enriquecida:** Compatible con Microsoft Rich Edit 1,0 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="db1c6-120">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="db1c6-121">El **mensaje \_ LINESCROLL em** desplaza el texto verticalmente en un control de edición multilínea.</span><span class="sxs-lookup"><span data-stu-id="db1c6-121">The **EM\_LINESCROLL** message scrolls the text vertically in a multiline edit control.</span></span> <span data-ttu-id="db1c6-122">Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="db1c6-122">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="db1c6-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db1c6-123">Requirements</span></span>



| <span data-ttu-id="db1c6-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="db1c6-124">Requirement</span></span> | <span data-ttu-id="db1c6-125">Value</span><span class="sxs-lookup"><span data-stu-id="db1c6-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db1c6-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="db1c6-126">Minimum supported client</span></span><br/> | <span data-ttu-id="db1c6-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="db1c6-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="db1c6-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="db1c6-128">Minimum supported server</span></span><br/> | <span data-ttu-id="db1c6-129">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="db1c6-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="db1c6-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="db1c6-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="db1c6-131"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="db1c6-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

 





