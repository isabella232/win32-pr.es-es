---
title: Mensaje de WM_PASTE (Winuser. h)
description: Una aplicación envía un \_ mensaje de pegado de WM a un control de edición o un cuadro combinado para copiar el contenido actual del portapapeles en el control de edición situado en la posición actual del símbolo de intercalación. Los datos se insertan solo si el Portapapeles contiene datos en \_ formato de texto CF.
ms.assetid: 6830b511-986f-46ef-a977-7adedffe86ea
keywords:
- Intercambio de datos de mensajes de WM_PASTE
topic_type:
- apiref
api_name:
- WM_PASTE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86b723830ecdd0f8b7e3faa9da9adcb51161b297
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422531"
---
# <a name="wm_paste-message"></a><span data-ttu-id="32a64-105">\_Mensaje de pegado de WM</span><span class="sxs-lookup"><span data-stu-id="32a64-105">WM\_PASTE message</span></span>

<span data-ttu-id="32a64-106">Una aplicación envía un mensaje de **\_ pegado de WM** a un control de edición o un cuadro combinado para copiar el contenido actual del portapapeles en el control de edición situado en la posición actual del símbolo de intercalación.</span><span class="sxs-lookup"><span data-stu-id="32a64-106">An application sends a **WM\_PASTE** message to an edit control or combo box to copy the current content of the clipboard to the edit control at the current caret position.</span></span> <span data-ttu-id="32a64-107">Los datos se insertan solo si el Portapapeles contiene datos en formato de [**\_ texto CF**](standard-clipboard-formats.md) .</span><span class="sxs-lookup"><span data-stu-id="32a64-107">Data is inserted only if the clipboard contains data in [**CF\_TEXT**](standard-clipboard-formats.md) format.</span></span>


```C++
#define WM_PASTE                        0x0302
```



## <a name="parameters"></a><span data-ttu-id="32a64-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="32a64-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32a64-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="32a64-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="32a64-110">Este parámetro no se utiliza y debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="32a64-110">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="32a64-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="32a64-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="32a64-112">Este parámetro no se utiliza y debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="32a64-112">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32a64-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="32a64-113">Return value</span></span>

<span data-ttu-id="32a64-114">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="32a64-114">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="32a64-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="32a64-115">Remarks</span></span>

<span data-ttu-id="32a64-116">Cuando se envía a un cuadro combinado, el mensaje de **\_ pegado de WM** se controla mediante su control de edición.</span><span class="sxs-lookup"><span data-stu-id="32a64-116">When sent to a combo box, the **WM\_PASTE** message is handled by its edit control.</span></span> <span data-ttu-id="32a64-117">Este mensaje no tiene ningún efecto cuando se envía a un cuadro combinado con el estilo [**CBS \_ DROPDOWNLIST**](../controls/combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="32a64-117">This message has no effect when sent to a combo box with the [**CBS\_DROPDOWNLIST**](../controls/combo-box-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="32a64-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32a64-118">Requirements</span></span>



| <span data-ttu-id="32a64-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="32a64-119">Requirement</span></span> | <span data-ttu-id="32a64-120">Value</span><span class="sxs-lookup"><span data-stu-id="32a64-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32a64-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="32a64-121">Minimum supported client</span></span><br/> | <span data-ttu-id="32a64-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="32a64-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="32a64-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="32a64-123">Minimum supported server</span></span><br/> | <span data-ttu-id="32a64-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="32a64-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="32a64-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="32a64-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="32a64-126"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="32a64-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32a64-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="32a64-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="32a64-128">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="32a64-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="32a64-129">**\_borrado de WM**</span><span class="sxs-lookup"><span data-stu-id="32a64-129">**WM\_CLEAR**</span></span>](wm-clear.md)
</dt> <dt>

[<span data-ttu-id="32a64-130">**copia de WM \_**</span><span class="sxs-lookup"><span data-stu-id="32a64-130">**WM\_COPY**</span></span>](wm-copy.md)
</dt> <dt>

[<span data-ttu-id="32a64-131">**cortar de WM \_**</span><span class="sxs-lookup"><span data-stu-id="32a64-131">**WM\_CUT**</span></span>](wm-cut.md)
</dt> <dt>

[<span data-ttu-id="32a64-132">**deshacer de WM \_**</span><span class="sxs-lookup"><span data-stu-id="32a64-132">**WM\_UNDO**</span></span>](/windows/desktop/Controls/wm-undo)
</dt> <dt>

<span data-ttu-id="32a64-133">**Vista**</span><span class="sxs-lookup"><span data-stu-id="32a64-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="32a64-134">Portapapeles</span><span class="sxs-lookup"><span data-stu-id="32a64-134">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 

