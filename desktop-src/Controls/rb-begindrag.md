---
title: Mensaje de RB_BEGINDRAG (commctrl. h)
description: Coloca el control rebar en el modo de arrastrar y colocar. Este mensaje no hace que \_ se envíe una notificación de BEGINDRAG de RBN.
ms.assetid: 1e3e4928-cb84-4fd4-8056-84de1f791d1c
keywords:
- RB_BEGINDRAG controles de mensajes de Windows
topic_type:
- apiref
api_name:
- RB_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41865baa2bf6c640595296be9c157201d0cc16d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491782"
---
# <a name="rb_begindrag-message"></a><span data-ttu-id="659b7-105">Mensaje de BEGINDRAG de RB \_</span><span class="sxs-lookup"><span data-stu-id="659b7-105">RB\_BEGINDRAG message</span></span>

<span data-ttu-id="659b7-106">Coloca el control rebar en el modo de arrastrar y colocar.</span><span class="sxs-lookup"><span data-stu-id="659b7-106">Puts the rebar control in drag-and-drop mode.</span></span> <span data-ttu-id="659b7-107">Este mensaje no hace que se envíe una notificación de [ \_ BEGINDRAG de RBN](rbn-begindrag.md) .</span><span class="sxs-lookup"><span data-stu-id="659b7-107">This message does not cause a [RBN\_BEGINDRAG](rbn-begindrag.md) notification to be sent.</span></span>

## <a name="parameters"></a><span data-ttu-id="659b7-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="659b7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="659b7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="659b7-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="659b7-110">Índice de base cero de la banda a la que afectará la operación de arrastrar y colocar.</span><span class="sxs-lookup"><span data-stu-id="659b7-110">Zero-based index of the band that the drag-and-drop operation will affect.</span></span>

</dd> <dt>

<span data-ttu-id="659b7-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="659b7-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="659b7-112">Valor **DWORD** que contiene las coordenadas de inicio del mouse.</span><span class="sxs-lookup"><span data-stu-id="659b7-112">**DWORD** value that contains the starting mouse coordinates.</span></span> <span data-ttu-id="659b7-113">La coordenada horizontal está contenida en el LOWORD y la coordenada vertical está contenida en el HIWORD.</span><span class="sxs-lookup"><span data-stu-id="659b7-113">The horizontal coordinate is contained in the LOWORD and the vertical coordinate is contained in the HIWORD.</span></span> <span data-ttu-id="659b7-114">Si pasa (**DWORD**)-1, el control rebar usará la posición del mouse la última vez que el subproceso del control llamó a [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) o [**PeekMessage**](/windows/desktop/api/winuser/nf-winuser-peekmessagea).</span><span class="sxs-lookup"><span data-stu-id="659b7-114">If you pass (**DWORD**)-1, the rebar control will use the position of the mouse the last time the control's thread called [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) or [**PeekMessage**](/windows/desktop/api/winuser/nf-winuser-peekmessagea).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="659b7-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="659b7-115">Return value</span></span>

<span data-ttu-id="659b7-116">No se utiliza el valor devuelto para este mensaje.</span><span class="sxs-lookup"><span data-stu-id="659b7-116">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="659b7-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="659b7-117">Remarks</span></span>

<span data-ttu-id="659b7-118">Los **mensajes \_ RB BEGINDRAG**, [**RB \_ DRAGMOVE**](rb-dragmove.md)y [**RB \_ ENDDRAG**](rb-enddrag.md) permiten implementar una interfaz [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) para un control rebar.</span><span class="sxs-lookup"><span data-stu-id="659b7-118">The **RB\_BEGINDRAG**, [**RB\_DRAGMOVE**](rb-dragmove.md), and [**RB\_ENDDRAG**](rb-enddrag.md) messages allow you to implement an [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) interface for a rebar control.</span></span> <span data-ttu-id="659b7-119">Envía el mensaje **RB \_ BEGINDRAG** en respuesta a [**IDropTarget::D ragenter**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragenter), envía el mensaje **RB \_ DRAGMOVE** en respuesta a [**IDropTarget::D Ragover**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragover)y el mensaje **RB \_ ENDDRAG** en respuesta a [**IDropTarget::D ROP**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-drop) e [**IDropTarget::D ragleave**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragleave).</span><span class="sxs-lookup"><span data-stu-id="659b7-119">You send the **RB\_BEGINDRAG** message in response to [**IDropTarget::DragEnter**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragenter), send the **RB\_DRAGMOVE** message in response to [**IDropTarget::DragOver**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragover), and the **RB\_ENDDRAG** message in response to [**IDropTarget::Drop**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-drop) and [**IDropTarget::DragLeave**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragleave).</span></span>

## <a name="requirements"></a><span data-ttu-id="659b7-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="659b7-120">Requirements</span></span>



| <span data-ttu-id="659b7-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="659b7-121">Requirement</span></span> | <span data-ttu-id="659b7-122">Value</span><span class="sxs-lookup"><span data-stu-id="659b7-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="659b7-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="659b7-123">Minimum supported client</span></span><br/> | <span data-ttu-id="659b7-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="659b7-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="659b7-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="659b7-125">Minimum supported server</span></span><br/> | <span data-ttu-id="659b7-126">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="659b7-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="659b7-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="659b7-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="659b7-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="659b7-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

