---
title: Mensaje de WM_DPICHANGED_AFTERPARENT (Winuser. h)
description: En el caso de las ventanas de nivel superior de por monitor V2, este mensaje se envía a todos los HWND del árbol de HWDN secundario de la ventana que está experimentando un cambio de PPP. | Mensaje de WM_DPICHANGED_AFTERPARENT (Winuser. h)
ms.assetid: FEA1BF07-55B6-4584-ABD3-340515831E0A
keywords:
- WM_DPICHANGED_AFTERPARENT máximo de PPP del mensaje
topic_type:
- apiref
api_name:
- WM_DPICHANGED_AFTERPARENT
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10cc76602662cefba42f62bd3ed85913ade40f15
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105689844"
---
# <a name="wm_dpichanged_afterparent-message"></a><span data-ttu-id="3a994-105">\_Mensaje AFTERPARENT de DPICHANGED de WM \_</span><span class="sxs-lookup"><span data-stu-id="3a994-105">WM\_DPICHANGED\_AFTERPARENT message</span></span>

<span data-ttu-id="3a994-106">En el caso de las ventanas de nivel superior de [por monitor V2](dpi-awareness-context.md) , este mensaje se envía a todos los HWND del árbol de HWDN secundario de la ventana que está experimentando un cambio de PPP.</span><span class="sxs-lookup"><span data-stu-id="3a994-106">For [Per Monitor v2](dpi-awareness-context.md) top-level windows, this message is sent to all HWNDs in the child HWDN tree of the window that is undergoing a DPI change.</span></span> <span data-ttu-id="3a994-107">Este mensaje se produce después de que la ventana de nivel superior reciba [**WM \_ DPICHANGED**](wm-dpichanged.md)y recorra el árbol secundario de arriba abajo.</span><span class="sxs-lookup"><span data-stu-id="3a994-107">This message occurs after the top-level window receives [**WM\_DPICHANGED**](wm-dpichanged.md), and traverses the child tree from the top down.</span></span>


```C++
#define WM_DPICHANGED_AFTERPARENT       0x02E3
```



## <a name="parameters"></a><span data-ttu-id="3a994-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3a994-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a994-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3a994-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3a994-110">Este valor no se utiliza y será cero.</span><span class="sxs-lookup"><span data-stu-id="3a994-110">This value is unused and will be zero.</span></span>

</dd> <dt>

<span data-ttu-id="3a994-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3a994-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3a994-112">Este valor no se utiliza y será cero.</span><span class="sxs-lookup"><span data-stu-id="3a994-112">This value is unused and will be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a994-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3a994-113">Return value</span></span>

<span data-ttu-id="3a994-114">El sistema no utiliza este valor y lo omite.</span><span class="sxs-lookup"><span data-stu-id="3a994-114">This value is unused and ignored by the system.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a994-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3a994-115">Remarks</span></span>

<span data-ttu-id="3a994-116">No hay ningún control predeterminado de este mensaje en [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="3a994-116">There is no default handling of this message in [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

<span data-ttu-id="3a994-117">Este mensaje solo se envía cuando la ventana de nivel superior tiene un contexto de reconocimiento de PPP de PMv2.</span><span class="sxs-lookup"><span data-stu-id="3a994-117">This message is only sent when the top-level window has a DPI awareness context of PMv2.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a994-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a994-118">Requirements</span></span>



| <span data-ttu-id="3a994-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a994-119">Requirement</span></span> | <span data-ttu-id="3a994-120">Value</span><span class="sxs-lookup"><span data-stu-id="3a994-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3a994-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3a994-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3a994-122">Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="3a994-122">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="3a994-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3a994-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3a994-124">Solo aplicaciones de escritorio de Windows Server 2016 \[\]</span><span class="sxs-lookup"><span data-stu-id="3a994-124">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="3a994-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3a994-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a994-126"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a994-126"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a994-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="3a994-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a994-128">**DPICHANGED de WM \_**</span><span class="sxs-lookup"><span data-stu-id="3a994-128">**WM\_DPICHANGED**</span></span>](wm-dpichanged.md)
</dt> <dt>

[<span data-ttu-id="3a994-129">**\_BEFOREPARENT DPICHANGED \_ WM**</span><span class="sxs-lookup"><span data-stu-id="3a994-129">**WM\_DPICHANGED\_BEFOREPARENT**</span></span>](wm-dpichanged-beforeparent.md)
</dt> </dl>

 

