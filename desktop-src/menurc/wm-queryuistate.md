---
title: Mensaje de WM_QUERYUISTATE (Winuser. h)
description: Una aplicación envía el mensaje de QUERYUISTATE de WM \_ para recuperar el estado de la interfaz de usuario de una ventana.
ms.assetid: 3a9e3477-b5d7-4c55-b6d4-8a479451fee8
keywords:
- WM_QUERYUISTATE menús de mensajes y otros recursos
topic_type:
- apiref
api_name:
- WM_QUERYUISTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1574fe0dab2a0885c8012bf19eed50facfd6cce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105696058"
---
# <a name="wm_queryuistate-message"></a><span data-ttu-id="32f3a-104">Mensaje de QUERYUISTATE de WM \_</span><span class="sxs-lookup"><span data-stu-id="32f3a-104">WM\_QUERYUISTATE message</span></span>

<span data-ttu-id="32f3a-105">Una aplicación envía el mensaje de **\_ QUERYUISTATE de WM** para recuperar el estado de la interfaz de usuario de una ventana.</span><span class="sxs-lookup"><span data-stu-id="32f3a-105">An application sends the **WM\_QUERYUISTATE** message to retrieve the UI state for a window.</span></span>


```C++
#define WM_QUERYUISTATE                 0x0129
```



## <a name="parameters"></a><span data-ttu-id="32f3a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="32f3a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32f3a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="32f3a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="32f3a-108">Este parámetro no se utiliza y debe ser 0.</span><span class="sxs-lookup"><span data-stu-id="32f3a-108">This parameter is not used and must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="32f3a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="32f3a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="32f3a-110">Este parámetro no se utiliza y debe ser 0.</span><span class="sxs-lookup"><span data-stu-id="32f3a-110">This parameter is not used and must be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32f3a-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="32f3a-111">Return value</span></span>

<span data-ttu-id="32f3a-112">El valor devuelto es **null** si están visibles los indicadores de foco y los aceleradores de teclado.</span><span class="sxs-lookup"><span data-stu-id="32f3a-112">The return value is **NULL** if the focus indicators and the keyboard accelerators are visible.</span></span> <span data-ttu-id="32f3a-113">De lo contrario, el valor devuelto puede ser uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="32f3a-113">Otherwise, the return value can be one or more of the following values.</span></span>



| <span data-ttu-id="32f3a-114">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="32f3a-114">Return code/value</span></span>                                                                                                                                       | <span data-ttu-id="32f3a-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="32f3a-115">Description</span></span>                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="32f3a-116"><dt>**UISF \_**</dt> <dt>0x4</dt> activo</span><span class="sxs-lookup"><span data-stu-id="32f3a-116"><dt>**UISF\_ACTIVE**</dt> <dt>0x4</dt></span></span> </dl>    | <span data-ttu-id="32f3a-117">Un control debe dibujarse en el estilo utilizado para los controles activos.</span><span class="sxs-lookup"><span data-stu-id="32f3a-117">A control should be drawn in the style used for active controls.</span></span><br/> |
| <dl> <span data-ttu-id="32f3a-118"><dt>**UISF \_ HIDEACCEL**</dt> <dt>0X2</dt></span><span class="sxs-lookup"><span data-stu-id="32f3a-118"><dt>**UISF\_HIDEACCEL**</dt> <dt>0x2</dt></span></span> </dl> | <span data-ttu-id="32f3a-119">Los aceleradores de teclado están ocultos.</span><span class="sxs-lookup"><span data-stu-id="32f3a-119">Keyboard accelerators are hidden.</span></span><br/>                                |
| <dl> <span data-ttu-id="32f3a-120"><dt>**UISF \_ HIDEFOCUS**</dt> <dt>0x1</dt></span><span class="sxs-lookup"><span data-stu-id="32f3a-120"><dt>**UISF\_HIDEFOCUS**</dt> <dt>0x1</dt></span></span> </dl> | <span data-ttu-id="32f3a-121">Los indicadores de foco están ocultos.</span><span class="sxs-lookup"><span data-stu-id="32f3a-121">Focus indicators are hidden.</span></span><br/>                                     |



 

## <a name="requirements"></a><span data-ttu-id="32f3a-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32f3a-122">Requirements</span></span>



| <span data-ttu-id="32f3a-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="32f3a-123">Requirement</span></span> | <span data-ttu-id="32f3a-124">Value</span><span class="sxs-lookup"><span data-stu-id="32f3a-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32f3a-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="32f3a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="32f3a-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="32f3a-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="32f3a-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="32f3a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="32f3a-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="32f3a-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="32f3a-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="32f3a-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="32f3a-130"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="32f3a-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32f3a-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="32f3a-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="32f3a-132">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="32f3a-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="32f3a-133">**CHANGEUISTATE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="32f3a-133">**WM\_CHANGEUISTATE**</span></span>](wm-changeuistate.md)
</dt> <dt>

[<span data-ttu-id="32f3a-134">**UPDATEUISTATE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="32f3a-134">**WM\_UPDATEUISTATE**</span></span>](wm-updateuistate.md)
</dt> <dt>

<span data-ttu-id="32f3a-135">**Vista**</span><span class="sxs-lookup"><span data-stu-id="32f3a-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="32f3a-136">Aceleradores de teclado</span><span class="sxs-lookup"><span data-stu-id="32f3a-136">Keyboard Accelerators</span></span>](keyboard-accelerators.md)
</dt> </dl>

 

 





