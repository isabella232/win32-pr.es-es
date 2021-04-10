---
title: Mensaje de TBM_GETCHANNELRECT (commctrl. h)
description: Recupera el tamaño y la posición del rectángulo delimitador del canal de una barra de posición.
ms.assetid: 353edae3-1a26-4e85-8a32-ba8b5a976d24
keywords:
- TBM_GETCHANNELRECT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TBM_GETCHANNELRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02982e9ce417b9fcf3e16d0e14d061e3ffd97a8a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996106"
---
# <a name="tbm_getchannelrect-message"></a><span data-ttu-id="deb5b-104">TBM \_ GETCHANNELRECT</span><span class="sxs-lookup"><span data-stu-id="deb5b-104">TBM\_GETCHANNELRECT message</span></span>

<span data-ttu-id="deb5b-105">Recupera el tamaño y la posición del rectángulo delimitador del canal de una barra de posición.</span><span class="sxs-lookup"><span data-stu-id="deb5b-105">Retrieves the size and position of the bounding rectangle for a trackbar's channel.</span></span> <span data-ttu-id="deb5b-106">(El canal es el área sobre la que se mueve el control deslizante.</span><span class="sxs-lookup"><span data-stu-id="deb5b-106">(The channel is the area over which the slider moves.</span></span> <span data-ttu-id="deb5b-107">Contiene el resaltado cuando se selecciona un intervalo).</span><span class="sxs-lookup"><span data-stu-id="deb5b-107">It contains the highlight when a range is selected.)</span></span>

## <a name="parameters"></a><span data-ttu-id="deb5b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="deb5b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="deb5b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="deb5b-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="deb5b-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="deb5b-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="deb5b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="deb5b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="deb5b-112">Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="deb5b-112">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="deb5b-113">El mensaje rellena esta estructura con el rectángulo delimitador del canal, en coordenadas de cliente de la ventana de la barra de salida.</span><span class="sxs-lookup"><span data-stu-id="deb5b-113">The message fills this structure with the channel's bounding rectangle, in client coordinates of the trackbar's window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="deb5b-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="deb5b-114">Return value</span></span>

<span data-ttu-id="deb5b-115">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="deb5b-115">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="deb5b-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="deb5b-116">Requirements</span></span>



| <span data-ttu-id="deb5b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="deb5b-117">Requirement</span></span> | <span data-ttu-id="deb5b-118">Value</span><span class="sxs-lookup"><span data-stu-id="deb5b-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="deb5b-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="deb5b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="deb5b-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="deb5b-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="deb5b-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="deb5b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="deb5b-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="deb5b-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="deb5b-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="deb5b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="deb5b-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="deb5b-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

