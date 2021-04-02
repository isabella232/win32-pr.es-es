---
title: Mensaje de SB_GETBORDERS (commctrl. h)
description: Recupera los anchos actuales de los bordes horizontal y vertical de una ventana de estado.
ms.assetid: 120c1e0d-6f42-424e-94e0-a080d216d39d
keywords:
- SB_GETBORDERS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- SB_GETBORDERS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 854df2cd367a852a2e6a0e638b470187efabe58c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150753"
---
# <a name="sb_getborders-message"></a><span data-ttu-id="d976e-104">\_Mensaje GETBORDERS de SB</span><span class="sxs-lookup"><span data-stu-id="d976e-104">SB\_GETBORDERS message</span></span>

<span data-ttu-id="d976e-105">Recupera los anchos actuales de los bordes horizontal y vertical de una ventana de estado.</span><span class="sxs-lookup"><span data-stu-id="d976e-105">Retrieves the current widths of the horizontal and vertical borders of a status window.</span></span>

## <a name="parameters"></a><span data-ttu-id="d976e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d976e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d976e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d976e-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d976e-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="d976e-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d976e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d976e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d976e-110">Puntero a una matriz de enteros que tiene tres elementos.</span><span class="sxs-lookup"><span data-stu-id="d976e-110">Pointer to an integer array that has three elements.</span></span> <span data-ttu-id="d976e-111">El primer elemento recibe el ancho del borde horizontal, el segundo recibe el ancho del borde vertical y el tercero recibe el ancho del borde entre los rectángulos.</span><span class="sxs-lookup"><span data-stu-id="d976e-111">The first element receives the width of the horizontal border, the second receives the width of the vertical border, and the third receives the width of the border between rectangles.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d976e-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d976e-112">Return value</span></span>

<span data-ttu-id="d976e-113">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="d976e-113">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d976e-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d976e-114">Remarks</span></span>

<span data-ttu-id="d976e-115">Los bordes determinan el espaciado entre el borde exterior de la ventana y los rectángulos dentro de la ventana que contienen texto.</span><span class="sxs-lookup"><span data-stu-id="d976e-115">The borders determine the spacing between the outside edge of the window and the rectangles within the window that contain text.</span></span> <span data-ttu-id="d976e-116">Los bordes también determinan el espaciado entre los rectángulos.</span><span class="sxs-lookup"><span data-stu-id="d976e-116">The borders also determine the spacing between rectangles.</span></span>

## <a name="requirements"></a><span data-ttu-id="d976e-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d976e-117">Requirements</span></span>



| <span data-ttu-id="d976e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d976e-118">Requirement</span></span> | <span data-ttu-id="d976e-119">Value</span><span class="sxs-lookup"><span data-stu-id="d976e-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d976e-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d976e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d976e-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d976e-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d976e-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d976e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d976e-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d976e-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d976e-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d976e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d976e-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d976e-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





