---
title: Mensaje de WM_COPY (Winuser. h)
description: Una aplicación envía el mensaje de copia de WM \_ a un control de edición o un cuadro combinado para copiar la selección actual en el portapapeles en \_ formato de texto CF.
ms.assetid: dcac3ad3-1e70-4b71-accd-261587224e60
keywords:
- Intercambio de datos de mensajes de WM_COPY
topic_type:
- apiref
api_name:
- WM_COPY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b298248d75b1d25d1bfef8347347fe2f1a6c7916
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/04/2021
ms.locfileid: "105707574"
---
# <a name="wm_copy-message"></a><span data-ttu-id="94f21-104">Mensaje de copia de WM \_</span><span class="sxs-lookup"><span data-stu-id="94f21-104">WM\_COPY message</span></span>

<span data-ttu-id="94f21-105">Una aplicación envía el mensaje de **\_ copia de WM** a un control de edición o un cuadro combinado para copiar la selección actual en el portapapeles en formato de [**\_ texto CF**](standard-clipboard-formats.md) .</span><span class="sxs-lookup"><span data-stu-id="94f21-105">An application sends the **WM\_COPY** message to an edit control or combo box to copy the current selection to the clipboard in [**CF\_TEXT**](standard-clipboard-formats.md) format.</span></span>


```C++
#define WM_COPY                         0x0301
```



## <a name="parameters"></a><span data-ttu-id="94f21-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="94f21-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94f21-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="94f21-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="94f21-108">Este parámetro no se utiliza y debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="94f21-108">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="94f21-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="94f21-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="94f21-110">Este parámetro no se utiliza y debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="94f21-110">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94f21-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="94f21-111">Return value</span></span>

<span data-ttu-id="94f21-112">Devuelve un valor distinto de cero si es correcto; de lo contrario, es cero.</span><span class="sxs-lookup"><span data-stu-id="94f21-112">Returns nonzero value on success, else zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="94f21-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="94f21-113">Remarks</span></span>

<span data-ttu-id="94f21-114">Cuando se envía a un cuadro combinado, el mensaje de **\_ copia de WM** se controla mediante su control de edición.</span><span class="sxs-lookup"><span data-stu-id="94f21-114">When sent to a combo box, the **WM\_COPY** message is handled by its edit control.</span></span> <span data-ttu-id="94f21-115">Este mensaje no tiene ningún efecto cuando se envía a un cuadro combinado con el estilo [**CBS \_ DROPDOWNLIST**](../controls/combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="94f21-115">This message has no effect when sent to a combo box with the [**CBS\_DROPDOWNLIST**](../controls/combo-box-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="94f21-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94f21-116">Requirements</span></span>



| <span data-ttu-id="94f21-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="94f21-117">Requirement</span></span> | <span data-ttu-id="94f21-118">Value</span><span class="sxs-lookup"><span data-stu-id="94f21-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94f21-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="94f21-119">Minimum supported client</span></span><br/> | <span data-ttu-id="94f21-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="94f21-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="94f21-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="94f21-121">Minimum supported server</span></span><br/> | <span data-ttu-id="94f21-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="94f21-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="94f21-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="94f21-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="94f21-124"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="94f21-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94f21-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="94f21-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="94f21-126">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="94f21-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="94f21-127">**\_borrado de WM**</span><span class="sxs-lookup"><span data-stu-id="94f21-127">**WM\_CLEAR**</span></span>](wm-clear.md)
</dt> <dt>

[<span data-ttu-id="94f21-128">**cortar de WM \_**</span><span class="sxs-lookup"><span data-stu-id="94f21-128">**WM\_CUT**</span></span>](wm-cut.md)
</dt> <dt>

[<span data-ttu-id="94f21-129">**pegar de WM \_**</span><span class="sxs-lookup"><span data-stu-id="94f21-129">**WM\_PASTE**</span></span>](wm-paste.md)
</dt> <dt>

[<span data-ttu-id="94f21-130">**deshacer de WM \_**</span><span class="sxs-lookup"><span data-stu-id="94f21-130">**WM\_UNDO**</span></span>](/windows/desktop/Controls/wm-undo)
</dt> <dt>

<span data-ttu-id="94f21-131">**Vista**</span><span class="sxs-lookup"><span data-stu-id="94f21-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="94f21-132">Portapapeles</span><span class="sxs-lookup"><span data-stu-id="94f21-132">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 

