---
title: Mensaje de TVM_HITTEST (commctrl. h)
description: Determina la ubicación del punto especificado con respecto al área cliente de un control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro de TreeView \_ HitTest.
ms.assetid: 18ea3737-f429-4c10-9133-3b5729aa36fa
keywords:
- TVM_HITTEST controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50b91a11892a2bb904d2cd7d82b5b08cea18331b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079112"
---
# <a name="tvm_hittest-message"></a><span data-ttu-id="17dcf-105">TVM \_ HITTEST (mensaje)</span><span class="sxs-lookup"><span data-stu-id="17dcf-105">TVM\_HITTEST message</span></span>

<span data-ttu-id="17dcf-106">Determina la ubicación del punto especificado con respecto al área cliente de un control de vista de árbol.</span><span class="sxs-lookup"><span data-stu-id="17dcf-106">Determines the location of the specified point relative to the client area of a tree-view control.</span></span> <span data-ttu-id="17dcf-107">Puede enviar este mensaje explícitamente o mediante la macro de [**TreeView \_ HitTest**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_hittest) .</span><span class="sxs-lookup"><span data-stu-id="17dcf-107">You can send this message explicitly or by using the [**TreeView\_HitTest**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_hittest) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="17dcf-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="17dcf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17dcf-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="17dcf-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="17dcf-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="17dcf-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="17dcf-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="17dcf-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="17dcf-112">Puntero a una estructura [**TVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tvhittestinfo) .</span><span class="sxs-lookup"><span data-stu-id="17dcf-112">Pointer to a [**TVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tvhittestinfo) structure.</span></span> <span data-ttu-id="17dcf-113">Cuando se envía el mensaje, el miembro **PT** especifica las coordenadas del punto que se va a probar.</span><span class="sxs-lookup"><span data-stu-id="17dcf-113">When the message is sent, the **pt** member specifies the coordinates of the point to test.</span></span> <span data-ttu-id="17dcf-114">Cuando el mensaje vuelve, el miembro **hItem** es el identificador del elemento en el punto especificado o **null** si ningún elemento ocupa el punto.</span><span class="sxs-lookup"><span data-stu-id="17dcf-114">When the message returns, the **hItem** member is the handle to the item at the specified point or **NULL** if no item occupies the point.</span></span> <span data-ttu-id="17dcf-115">Además, cuando el mensaje vuelve, el miembro **Flags** es un valor de prueba de posicionamiento que indica la ubicación del punto especificado.</span><span class="sxs-lookup"><span data-stu-id="17dcf-115">Also, when the message returns, the **flags** member is a hit test value that indicates the location of the specified point.</span></span> <span data-ttu-id="17dcf-116">Para obtener una lista de los valores de las pruebas de posicionamiento, vea la descripción de la estructura **TVHITTESTINFO** .</span><span class="sxs-lookup"><span data-stu-id="17dcf-116">For a list of hit test values, see the description of the **TVHITTESTINFO** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17dcf-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="17dcf-117">Return value</span></span>

<span data-ttu-id="17dcf-118">Devuelve el identificador del elemento de vista de árbol que ocupa el punto especificado, o **null** si ningún elemento ocupa el punto.</span><span class="sxs-lookup"><span data-stu-id="17dcf-118">Returns the handle to the tree-view item that occupies the specified point, or **NULL** if no item occupies the point.</span></span>

## <a name="requirements"></a><span data-ttu-id="17dcf-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17dcf-119">Requirements</span></span>



| <span data-ttu-id="17dcf-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="17dcf-120">Requirement</span></span> | <span data-ttu-id="17dcf-121">Value</span><span class="sxs-lookup"><span data-stu-id="17dcf-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="17dcf-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="17dcf-122">Minimum supported client</span></span><br/> | <span data-ttu-id="17dcf-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="17dcf-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="17dcf-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="17dcf-124">Minimum supported server</span></span><br/> | <span data-ttu-id="17dcf-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="17dcf-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="17dcf-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="17dcf-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="17dcf-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="17dcf-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





