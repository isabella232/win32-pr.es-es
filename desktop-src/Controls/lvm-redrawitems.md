---
title: Mensaje de LVM_REDRAWITEMS (commctrl. h)
description: Fuerza un control de vista de lista para volver a dibujar un intervalo de elementos. Puede enviar este mensaje explícitamente o mediante la \_ macro RedrawItems de ListView.
ms.assetid: a717b17f-6e0a-4804-96f9-da93392a19ec
keywords:
- LVM_REDRAWITEMS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_REDRAWITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42568a9ab78361a28a99eee372674287a24d03cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079353"
---
# <a name="lvm_redrawitems-message"></a><span data-ttu-id="0d2c0-105">\_Mensaje REDRAWITEMS LVM</span><span class="sxs-lookup"><span data-stu-id="0d2c0-105">LVM\_REDRAWITEMS message</span></span>

<span data-ttu-id="0d2c0-106">Fuerza un control de vista de lista para volver a dibujar un intervalo de elementos.</span><span class="sxs-lookup"><span data-stu-id="0d2c0-106">Forces a list-view control to redraw a range of items.</span></span> <span data-ttu-id="0d2c0-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ RedrawItems de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_redrawitems) .</span><span class="sxs-lookup"><span data-stu-id="0d2c0-107">You can send this message explicitly or by using the [**ListView\_RedrawItems**](/windows/desktop/api/Commctrl/nf-commctrl-listview_redrawitems) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="0d2c0-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0d2c0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d2c0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0d2c0-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0d2c0-110">Índice del primer elemento que se va a volver a dibujar.</span><span class="sxs-lookup"><span data-stu-id="0d2c0-110">Index of the first item to redraw.</span></span>

</dd> <dt>

<span data-ttu-id="0d2c0-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0d2c0-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0d2c0-112">Índice del último elemento que se va a volver a dibujar.</span><span class="sxs-lookup"><span data-stu-id="0d2c0-112">Index of the last item to redraw.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d2c0-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0d2c0-113">Return value</span></span>

<span data-ttu-id="0d2c0-114">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="0d2c0-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d2c0-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0d2c0-115">Remarks</span></span>

<span data-ttu-id="0d2c0-116">Los elementos especificados no se redibujan realmente hasta que la ventana de la vista de lista recibe un mensaje de [**\_ dibujo de WM**](/windows/desktop/gdi/wm-paint) para volver a pintar.</span><span class="sxs-lookup"><span data-stu-id="0d2c0-116">The specified items are not actually redrawn until the list-view window receives a [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message to repaint.</span></span> <span data-ttu-id="0d2c0-117">Para volver a dibujar inmediatamente, llame a la función [**UpdateWindow**](/windows/desktop/api/winuser/nf-winuser-updatewindow) después de usar esta macro.</span><span class="sxs-lookup"><span data-stu-id="0d2c0-117">To repaint immediately, call the [**UpdateWindow**](/windows/desktop/api/winuser/nf-winuser-updatewindow) function after using this macro.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d2c0-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d2c0-118">Requirements</span></span>



| <span data-ttu-id="0d2c0-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d2c0-119">Requirement</span></span> | <span data-ttu-id="0d2c0-120">Value</span><span class="sxs-lookup"><span data-stu-id="0d2c0-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0d2c0-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0d2c0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0d2c0-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0d2c0-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0d2c0-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0d2c0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0d2c0-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="0d2c0-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0d2c0-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0d2c0-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d2c0-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d2c0-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

