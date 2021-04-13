---
title: Mensaje de TBM_CLEARTICS (commctrl. h)
description: Quita las marcas de graduación actuales de una barra de aumento. Este mensaje no quita la primera y última marca de graduación, creadas automáticamente por la barra de aumento.
ms.assetid: 2830497c-2cf0-4068-810c-c05d4e0abb8b
keywords:
- TBM_CLEARTICS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TBM_CLEARTICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a1ecb4f9f931c976b2542a1f263fc069f1eca10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489814"
---
# <a name="tbm_cleartics-message"></a><span data-ttu-id="9f6b8-105">TBM \_ CLEARTICS</span><span class="sxs-lookup"><span data-stu-id="9f6b8-105">TBM\_CLEARTICS message</span></span>

<span data-ttu-id="9f6b8-106">Quita las marcas de graduación actuales de una barra de aumento.</span><span class="sxs-lookup"><span data-stu-id="9f6b8-106">Removes the current tick marks from a trackbar.</span></span> <span data-ttu-id="9f6b8-107">Este mensaje no quita la primera y última marca de graduación, creadas automáticamente por la barra de aumento.</span><span class="sxs-lookup"><span data-stu-id="9f6b8-107">This message does not remove the first and last tick marks, which are created automatically by the trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="9f6b8-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9f6b8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f6b8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9f6b8-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9f6b8-110">Volver a dibujar el marcador.</span><span class="sxs-lookup"><span data-stu-id="9f6b8-110">Redraw flag.</span></span> <span data-ttu-id="9f6b8-111">Si este parámetro es **true**, la barra de aumento se vuelve a dibujar una vez que se han desactivado las marcas de graduación.</span><span class="sxs-lookup"><span data-stu-id="9f6b8-111">If this parameter is **TRUE**, the trackbar is redrawn after the tick marks are cleared.</span></span> <span data-ttu-id="9f6b8-112">Si este parámetro es **false**, el mensaje borra las marcas de graduación pero no vuelve a dibujar la barra de aumento.</span><span class="sxs-lookup"><span data-stu-id="9f6b8-112">If this parameter is **FALSE**, the message clears the tick marks but does not redraw the trackbar.</span></span>

</dd> <dt>

<span data-ttu-id="9f6b8-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9f6b8-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="9f6b8-114">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="9f6b8-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f6b8-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9f6b8-115">Return value</span></span>

<span data-ttu-id="9f6b8-116">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="9f6b8-116">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f6b8-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f6b8-117">Requirements</span></span>



| <span data-ttu-id="9f6b8-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f6b8-118">Requirement</span></span> | <span data-ttu-id="9f6b8-119">Value</span><span class="sxs-lookup"><span data-stu-id="9f6b8-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9f6b8-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9f6b8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9f6b8-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9f6b8-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9f6b8-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9f6b8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9f6b8-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="9f6b8-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9f6b8-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9f6b8-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f6b8-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f6b8-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





