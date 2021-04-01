---
title: Mensaje de TVM_SETINSERTMARKCOLOR (commctrl. h)
description: Establece el color utilizado para dibujar la marca de inserción para la vista de árbol. Puede enviar este mensaje explícitamente o mediante la \_ macro SetInsertMarkColor de TreeView.
ms.assetid: c82304a8-3726-42c0-81e7-90d8f8205ead
keywords:
- TVM_SETINSERTMARKCOLOR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_SETINSERTMARKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92668b1137b089f9a09cc9a34d63d472742bce4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150451"
---
# <a name="tvm_setinsertmarkcolor-message"></a><span data-ttu-id="83185-105">\_Mensaje de SETINSERTMARKCOLOR TVM</span><span class="sxs-lookup"><span data-stu-id="83185-105">TVM\_SETINSERTMARKCOLOR message</span></span>

<span data-ttu-id="83185-106">Establece el color utilizado para dibujar la marca de inserción para la vista de árbol.</span><span class="sxs-lookup"><span data-stu-id="83185-106">Sets the color used to draw the insertion mark for the tree view.</span></span> <span data-ttu-id="83185-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ SetInsertMarkColor de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setinsertmarkcolor) .</span><span class="sxs-lookup"><span data-stu-id="83185-107">You can send this message explicitly or by using the [**TreeView\_SetInsertMarkColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setinsertmarkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="83185-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="83185-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83185-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="83185-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="83185-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="83185-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="83185-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="83185-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="83185-112">Valor de [**COLORREF**](/windows/desktop/gdi/colorref) que contiene el nuevo color de la marca de inserción.</span><span class="sxs-lookup"><span data-stu-id="83185-112">[**COLORREF**](/windows/desktop/gdi/colorref) value that contains the new insertion mark color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83185-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="83185-113">Return value</span></span>

<span data-ttu-id="83185-114">Devuelve un valor de **COLORREF** que contiene el color anterior de la marca de inserción.</span><span class="sxs-lookup"><span data-stu-id="83185-114">Returns a **COLORREF** value that contains the previous insertion mark color.</span></span>

## <a name="requirements"></a><span data-ttu-id="83185-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83185-115">Requirements</span></span>



| <span data-ttu-id="83185-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="83185-116">Requirement</span></span> | <span data-ttu-id="83185-117">Value</span><span class="sxs-lookup"><span data-stu-id="83185-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="83185-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="83185-118">Minimum supported client</span></span><br/> | <span data-ttu-id="83185-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="83185-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="83185-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="83185-120">Minimum supported server</span></span><br/> | <span data-ttu-id="83185-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="83185-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="83185-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="83185-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="83185-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="83185-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83185-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="83185-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83185-125">**TVM \_ GETINSERTMARKCOLOR**</span><span class="sxs-lookup"><span data-stu-id="83185-125">**TVM\_GETINSERTMARKCOLOR**</span></span>](tvm-getinsertmarkcolor.md)
</dt> </dl>

 

