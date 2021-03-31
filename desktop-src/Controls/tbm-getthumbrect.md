---
title: Mensaje de TBM_GETTHUMBRECT (commctrl. h)
description: Recupera el tamaño y la posición del rectángulo delimitador del control deslizante en una barra de desplazamiento.
ms.assetid: f53fd7af-36f8-4490-aa95-f1fa20f34efb
keywords:
- TBM_GETTHUMBRECT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TBM_GETTHUMBRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dce1bba8af9a65f297aa0515c1103c50daa1626d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079395"
---
# <a name="tbm_getthumbrect-message"></a><span data-ttu-id="a3180-104">TBM \_ GETTHUMBRECT</span><span class="sxs-lookup"><span data-stu-id="a3180-104">TBM\_GETTHUMBRECT message</span></span>

<span data-ttu-id="a3180-105">Recupera el tamaño y la posición del rectángulo delimitador del control deslizante en una barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="a3180-105">Retrieves the size and position of the bounding rectangle for the slider in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="a3180-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a3180-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3180-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a3180-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="a3180-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="a3180-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="a3180-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a3180-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a3180-110">Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="a3180-110">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="a3180-111">El mensaje rellena esta estructura con el rectángulo delimitador del control deslizante de la barra de desplazamiento en las coordenadas de cliente de la ventana de la barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="a3180-111">The message fills this structure with the bounding rectangle of the trackbar's slider in client coordinates of the trackbar's window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3180-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a3180-112">Return value</span></span>

<span data-ttu-id="a3180-113">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="a3180-113">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3180-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3180-114">Requirements</span></span>



| <span data-ttu-id="a3180-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3180-115">Requirement</span></span> | <span data-ttu-id="a3180-116">Value</span><span class="sxs-lookup"><span data-stu-id="a3180-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a3180-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a3180-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a3180-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a3180-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a3180-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a3180-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a3180-120">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="a3180-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a3180-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a3180-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3180-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3180-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

