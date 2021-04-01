---
title: Mensaje de TVM_GETINSERTMARKCOLOR (commctrl. h)
description: Recupera el color usado para dibujar la marca de inserción para la vista de árbol. Puede enviar este mensaje explícitamente o mediante la \_ macro GetInsertMarkColor de TreeView.
ms.assetid: d1fba4bb-1bdb-44e0-8083-b564cdafc055
keywords:
- TVM_GETINSERTMARKCOLOR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_GETINSERTMARKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61416a428fed88ece8f50ca640dd9a05ec131614
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997019"
---
# <a name="tvm_getinsertmarkcolor-message"></a><span data-ttu-id="41049-105">\_Mensaje de GETINSERTMARKCOLOR TVM</span><span class="sxs-lookup"><span data-stu-id="41049-105">TVM\_GETINSERTMARKCOLOR message</span></span>

<span data-ttu-id="41049-106">Recupera el color usado para dibujar la marca de inserción para la vista de árbol.</span><span class="sxs-lookup"><span data-stu-id="41049-106">Retrieves the color used to draw the insertion mark for the tree view.</span></span> <span data-ttu-id="41049-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetInsertMarkColor de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getinsertmarkcolor) .</span><span class="sxs-lookup"><span data-stu-id="41049-107">You can send this message explicitly or by using the [**TreeView\_GetInsertMarkColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getinsertmarkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="41049-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="41049-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41049-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="41049-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="41049-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="41049-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="41049-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="41049-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="41049-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="41049-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41049-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="41049-113">Return value</span></span>

<span data-ttu-id="41049-114">Devuelve un valor de [**COLORREF**](/windows/desktop/gdi/colorref) que contiene el color de la marca de inserción actual.</span><span class="sxs-lookup"><span data-stu-id="41049-114">Returns a [**COLORREF**](/windows/desktop/gdi/colorref) value that contains the current insertion mark color.</span></span>

## <a name="requirements"></a><span data-ttu-id="41049-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41049-115">Requirements</span></span>



| <span data-ttu-id="41049-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="41049-116">Requirement</span></span> | <span data-ttu-id="41049-117">Value</span><span class="sxs-lookup"><span data-stu-id="41049-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="41049-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="41049-118">Minimum supported client</span></span><br/> | <span data-ttu-id="41049-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="41049-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="41049-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="41049-120">Minimum supported server</span></span><br/> | <span data-ttu-id="41049-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="41049-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="41049-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="41049-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="41049-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="41049-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41049-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="41049-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41049-125">**TVM \_ SETINSERTMARKCOLOR**</span><span class="sxs-lookup"><span data-stu-id="41049-125">**TVM\_SETINSERTMARKCOLOR**</span></span>](tvm-setinsertmarkcolor.md)
</dt> </dl>

 

