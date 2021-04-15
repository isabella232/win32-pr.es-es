---
title: Mensaje de WM_CUT (Winuser. h)
description: Una aplicación envía un mensaje de corte de WM \_ a un control de edición o un cuadro combinado para eliminar (cortar) la selección actual, si existe, en el control de edición y copiar el texto eliminado en el portapapeles en \_ formato de texto CF.
ms.assetid: 6ac45589-3e34-491c-9562-e072ddc478f9
keywords:
- Intercambio de datos de mensajes de WM_CUT
topic_type:
- apiref
api_name:
- WM_CUT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a63dfe85fb637636fbabbce5fa139699fd09a65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676721"
---
# <a name="wm_cut-message"></a><span data-ttu-id="256cd-104">Mensaje de corte de WM \_</span><span class="sxs-lookup"><span data-stu-id="256cd-104">WM\_CUT message</span></span>

<span data-ttu-id="256cd-105">Una aplicación envía un mensaje de **\_ corte de WM** a un control de edición o un cuadro combinado para eliminar (cortar) la selección actual, si existe, en el control de edición y copiar el texto eliminado en el portapapeles en formato de [**\_ texto CF**](standard-clipboard-formats.md) .</span><span class="sxs-lookup"><span data-stu-id="256cd-105">An application sends a **WM\_CUT** message to an edit control or combo box to delete (cut) the current selection, if any, in the edit control and copy the deleted text to the clipboard in [**CF\_TEXT**](standard-clipboard-formats.md) format.</span></span>


```C++
#define WM_CUT                          0x0300
```



## <a name="parameters"></a><span data-ttu-id="256cd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="256cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="256cd-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="256cd-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="256cd-108">Este parámetro no se utiliza y debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="256cd-108">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="256cd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="256cd-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="256cd-110">Este parámetro no se utiliza y debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="256cd-110">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="256cd-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="256cd-111">Return value</span></span>

<span data-ttu-id="256cd-112">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="256cd-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="256cd-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="256cd-113">Remarks</span></span>

<span data-ttu-id="256cd-114">La eliminación realizada por el mensaje de **\_ corte de WM** se puede deshacer enviando el control de edición de un mensaje de [**\_ Deshacer de EM**](../controls/em-undo.md) .</span><span class="sxs-lookup"><span data-stu-id="256cd-114">The deletion performed by the **WM\_CUT** message can be undone by sending the edit control an [**EM\_UNDO**](../controls/em-undo.md) message.</span></span>

<span data-ttu-id="256cd-115">Para eliminar la selección actual sin colocar el texto eliminado en el portapapeles, utilice el mensaje de [**\_ borrado de WM**](wm-clear.md) .</span><span class="sxs-lookup"><span data-stu-id="256cd-115">To delete the current selection without placing the deleted text on the clipboard, use the [**WM\_CLEAR**](wm-clear.md) message.</span></span>

<span data-ttu-id="256cd-116">Cuando se envía a un cuadro combinado, el mensaje de **\_ corte de WM** se controla mediante su control de edición.</span><span class="sxs-lookup"><span data-stu-id="256cd-116">When sent to a combo box, the **WM\_CUT** message is handled by its edit control.</span></span> <span data-ttu-id="256cd-117">Este mensaje no tiene ningún efecto cuando se envía a un cuadro combinado con el estilo [**CBS \_ DROPDOWNLIST**](../controls/combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="256cd-117">This message has no effect when sent to a combo box with the [**CBS\_DROPDOWNLIST**](../controls/combo-box-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="256cd-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="256cd-118">Requirements</span></span>



| <span data-ttu-id="256cd-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="256cd-119">Requirement</span></span> | <span data-ttu-id="256cd-120">Value</span><span class="sxs-lookup"><span data-stu-id="256cd-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="256cd-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="256cd-121">Minimum supported client</span></span><br/> | <span data-ttu-id="256cd-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="256cd-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="256cd-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="256cd-123">Minimum supported server</span></span><br/> | <span data-ttu-id="256cd-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="256cd-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="256cd-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="256cd-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="256cd-126"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="256cd-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="256cd-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="256cd-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="256cd-128">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="256cd-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="256cd-129">**\_borrado de WM**</span><span class="sxs-lookup"><span data-stu-id="256cd-129">**WM\_CLEAR**</span></span>](wm-clear.md)
</dt> <dt>

[<span data-ttu-id="256cd-130">**copia de WM \_**</span><span class="sxs-lookup"><span data-stu-id="256cd-130">**WM\_COPY**</span></span>](wm-copy.md)
</dt> <dt>

[<span data-ttu-id="256cd-131">**pegar de WM \_**</span><span class="sxs-lookup"><span data-stu-id="256cd-131">**WM\_PASTE**</span></span>](wm-paste.md)
</dt> <dt>

[<span data-ttu-id="256cd-132">**deshacer de WM \_**</span><span class="sxs-lookup"><span data-stu-id="256cd-132">**WM\_UNDO**</span></span>](/windows/desktop/Controls/wm-undo)
</dt> <dt>

<span data-ttu-id="256cd-133">**Vista**</span><span class="sxs-lookup"><span data-stu-id="256cd-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="256cd-134">Portapapeles</span><span class="sxs-lookup"><span data-stu-id="256cd-134">Clipboard</span></span>](clipboard.md)
</dt> <dt>

<span data-ttu-id="256cd-135">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="256cd-135">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="256cd-136">**deshacer EM \_**</span><span class="sxs-lookup"><span data-stu-id="256cd-136">**EM\_UNDO**</span></span>](../controls/em-undo.md)
</dt> </dl>

 

