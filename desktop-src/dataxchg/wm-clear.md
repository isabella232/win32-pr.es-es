---
title: Mensaje de WM_CLEAR (Winuser. h)
description: Una aplicación envía un mensaje de borrar de WM \_ a un control de edición o un cuadro combinado para eliminar (borrar) la selección actual, si la hay, del control de edición.
ms.assetid: 6730a725-01ec-4821-9ffc-1ea267d665b3
keywords:
- Intercambio de datos de mensajes de WM_CLEAR
topic_type:
- apiref
api_name:
- WM_CLEAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61a8e325704d1e8b953fe59bfaf4e8fcee62cf40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105705149"
---
# <a name="wm_clear-message"></a><span data-ttu-id="53813-104">\_Mensaje de borrado de WM</span><span class="sxs-lookup"><span data-stu-id="53813-104">WM\_CLEAR message</span></span>

<span data-ttu-id="53813-105">Una aplicación envía un mensaje de **\_ Borrar de WM** a un control de edición o un cuadro combinado para eliminar (borrar) la selección actual, si la hay, del control de edición.</span><span class="sxs-lookup"><span data-stu-id="53813-105">An application sends a **WM\_CLEAR** message to an edit control or combo box to delete (clear) the current selection, if any, from the edit control.</span></span>


```C++
#define WM_CLEAR                        0x0303
```



## <a name="parameters"></a><span data-ttu-id="53813-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="53813-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53813-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="53813-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="53813-108">Este parámetro no se utiliza y debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="53813-108">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="53813-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="53813-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="53813-110">Este parámetro no se utiliza y debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="53813-110">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53813-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="53813-111">Return value</span></span>

<span data-ttu-id="53813-112">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="53813-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="53813-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="53813-113">Remarks</span></span>

<span data-ttu-id="53813-114">La eliminación realizada por el mensaje de **\_ borrado de WM** se puede deshacer enviando el control de edición de un mensaje de [**\_ Deshacer de EM**](../controls/em-undo.md) .</span><span class="sxs-lookup"><span data-stu-id="53813-114">The deletion performed by the **WM\_CLEAR** message can be undone by sending the edit control an [**EM\_UNDO**](../controls/em-undo.md) message.</span></span>

<span data-ttu-id="53813-115">Para eliminar la selección actual y colocar el contenido eliminado en el portapapeles, utilice el mensaje de [**\_ corte de WM**](wm-cut.md) .</span><span class="sxs-lookup"><span data-stu-id="53813-115">To delete the current selection and place the deleted content on the clipboard, use the [**WM\_CUT**](wm-cut.md) message.</span></span>

<span data-ttu-id="53813-116">Cuando se envía a un cuadro combinado, el mensaje de **\_ borrado de WM** se controla mediante su control de edición.</span><span class="sxs-lookup"><span data-stu-id="53813-116">When sent to a combo box, the **WM\_CLEAR** message is handled by its edit control.</span></span> <span data-ttu-id="53813-117">Este mensaje no tiene ningún efecto cuando se envía a un cuadro combinado con el estilo [**CBS \_ DROPDOWNLIST**](../controls/combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="53813-117">This message has no effect when sent to a combo box with the [**CBS\_DROPDOWNLIST**](../controls/combo-box-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="53813-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53813-118">Requirements</span></span>



| <span data-ttu-id="53813-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="53813-119">Requirement</span></span> | <span data-ttu-id="53813-120">Value</span><span class="sxs-lookup"><span data-stu-id="53813-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53813-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="53813-121">Minimum supported client</span></span><br/> | <span data-ttu-id="53813-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="53813-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="53813-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="53813-123">Minimum supported server</span></span><br/> | <span data-ttu-id="53813-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="53813-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="53813-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="53813-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="53813-126"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="53813-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53813-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="53813-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="53813-128">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="53813-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="53813-129">**copia de WM \_**</span><span class="sxs-lookup"><span data-stu-id="53813-129">**WM\_COPY**</span></span>](wm-copy.md)
</dt> <dt>

[<span data-ttu-id="53813-130">**cortar de WM \_**</span><span class="sxs-lookup"><span data-stu-id="53813-130">**WM\_CUT**</span></span>](wm-cut.md)
</dt> <dt>

[<span data-ttu-id="53813-131">**pegar de WM \_**</span><span class="sxs-lookup"><span data-stu-id="53813-131">**WM\_PASTE**</span></span>](wm-paste.md)
</dt> <dt>

[<span data-ttu-id="53813-132">**deshacer de WM \_**</span><span class="sxs-lookup"><span data-stu-id="53813-132">**WM\_UNDO**</span></span>](/windows/desktop/Controls/wm-undo)
</dt> <dt>

<span data-ttu-id="53813-133">**Vista**</span><span class="sxs-lookup"><span data-stu-id="53813-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="53813-134">Portapapeles</span><span class="sxs-lookup"><span data-stu-id="53813-134">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 

