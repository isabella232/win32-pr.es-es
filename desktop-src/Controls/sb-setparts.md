---
title: Mensaje de SB_SETPARTS (commctrl. h)
description: Establece el número de partes de una ventana de estado y la coordenada del borde derecho de cada parte.
ms.assetid: e29e8b09-c018-4ea4-8b47-6f3713113427
keywords:
- SB_SETPARTS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- SB_SETPARTS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 062058fa3778cd0394cadd9d76b363a0353ffb2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534822"
---
# <a name="sb_setparts-message"></a><span data-ttu-id="51ee2-104">\_Mensaje SETPARTS de SB</span><span class="sxs-lookup"><span data-stu-id="51ee2-104">SB\_SETPARTS message</span></span>

<span data-ttu-id="51ee2-105">Establece el número de partes de una ventana de estado y la coordenada del borde derecho de cada parte.</span><span class="sxs-lookup"><span data-stu-id="51ee2-105">Sets the number of parts in a status window and the coordinate of the right edge of each part.</span></span>

## <a name="parameters"></a><span data-ttu-id="51ee2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="51ee2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51ee2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="51ee2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="51ee2-108">Número de elementos que se van a establecer (no puede ser mayor que 256).</span><span class="sxs-lookup"><span data-stu-id="51ee2-108">Number of parts to set (cannot be greater than 256).</span></span>

</dd> <dt>

<span data-ttu-id="51ee2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="51ee2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="51ee2-110">Puntero a una matriz de enteros.</span><span class="sxs-lookup"><span data-stu-id="51ee2-110">Pointer to an integer array.</span></span> <span data-ttu-id="51ee2-111">El número de elementos se especifica en *wParam*.</span><span class="sxs-lookup"><span data-stu-id="51ee2-111">The number of elements is specified in *wParam*.</span></span> <span data-ttu-id="51ee2-112">Cada elemento especifica la posición, en coordenadas de cliente, del borde derecho de la parte correspondiente.</span><span class="sxs-lookup"><span data-stu-id="51ee2-112">Each element specifies the position, in client coordinates, of the right edge of the corresponding part.</span></span> <span data-ttu-id="51ee2-113">Si un elemento es-1, el borde derecho de la parte correspondiente se extiende hasta el borde de la ventana.</span><span class="sxs-lookup"><span data-stu-id="51ee2-113">If an element is -1, the right edge of the corresponding part extends to the border of the window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51ee2-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="51ee2-114">Return value</span></span>

<span data-ttu-id="51ee2-115">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="51ee2-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="51ee2-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51ee2-116">Requirements</span></span>



| <span data-ttu-id="51ee2-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="51ee2-117">Requirement</span></span> | <span data-ttu-id="51ee2-118">Value</span><span class="sxs-lookup"><span data-stu-id="51ee2-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="51ee2-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="51ee2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="51ee2-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="51ee2-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="51ee2-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="51ee2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="51ee2-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="51ee2-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="51ee2-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="51ee2-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="51ee2-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="51ee2-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





