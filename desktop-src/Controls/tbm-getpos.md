---
title: Mensaje de TBM_GETPOS (commctrl. h)
description: Recupera la posición lógica actual del control deslizante en una barra de desplazamiento. Las posiciones lógicas son los valores enteros en el intervalo de la barra de desplazamiento mínimo al máximo.
ms.assetid: 6f082ab2-2f9a-4bc0-bfca-56f7b1a2d921
keywords:
- TBM_GETPOS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TBM_GETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 072ff9b8a107fe19afb1fee6107a2f05bad36025
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490697"
---
# <a name="tbm_getpos-message"></a><span data-ttu-id="0d8a6-105">TBM \_ GETPOS</span><span class="sxs-lookup"><span data-stu-id="0d8a6-105">TBM\_GETPOS message</span></span>

<span data-ttu-id="0d8a6-106">Recupera la posición lógica actual del control deslizante en una barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="0d8a6-106">Retrieves the current logical position of the slider in a trackbar.</span></span> <span data-ttu-id="0d8a6-107">Las posiciones lógicas son los valores enteros en el intervalo de la barra de desplazamiento mínimo al máximo.</span><span class="sxs-lookup"><span data-stu-id="0d8a6-107">The logical positions are the integer values in the trackbar's range of minimum to maximum slider positions.</span></span>

## <a name="parameters"></a><span data-ttu-id="0d8a6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0d8a6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d8a6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0d8a6-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0d8a6-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="0d8a6-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="0d8a6-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0d8a6-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="0d8a6-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="0d8a6-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d8a6-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0d8a6-113">Return value</span></span>

<span data-ttu-id="0d8a6-114">Devuelve un valor de 32 bits que especifica la posición lógica actual del control deslizante de la barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="0d8a6-114">Returns a 32-bit value that specifies the current logical position of the trackbar's slider.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d8a6-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d8a6-115">Requirements</span></span>



| <span data-ttu-id="0d8a6-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d8a6-116">Requirement</span></span> | <span data-ttu-id="0d8a6-117">Value</span><span class="sxs-lookup"><span data-stu-id="0d8a6-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0d8a6-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0d8a6-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0d8a6-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0d8a6-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0d8a6-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0d8a6-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0d8a6-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="0d8a6-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0d8a6-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0d8a6-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d8a6-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d8a6-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d8a6-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="0d8a6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d8a6-125">**TBM \_ SETPOS**</span><span class="sxs-lookup"><span data-stu-id="0d8a6-125">**TBM\_SETPOS**</span></span>](tbm-setpos.md)
</dt> </dl>

 

 





