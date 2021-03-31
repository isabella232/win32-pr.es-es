---
title: Mensaje de TBM_GETNUMTICS (commctrl. h)
description: Recupera el número de marcas de graduación en una barra de aumento.
ms.assetid: 3c3f7ebb-a544-474c-ba14-68eae543ee38
keywords:
- TBM_GETNUMTICS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TBM_GETNUMTICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 712e1a0190334ec279f28a68959f3e3d5d5ffd1d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996105"
---
# <a name="tbm_getnumtics-message"></a><span data-ttu-id="c83c5-104">TBM \_ GETNUMTICS</span><span class="sxs-lookup"><span data-stu-id="c83c5-104">TBM\_GETNUMTICS message</span></span>

<span data-ttu-id="c83c5-105">Recupera el número de marcas de graduación en una barra de aumento.</span><span class="sxs-lookup"><span data-stu-id="c83c5-105">Retrieves the number of tick marks in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="c83c5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c83c5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c83c5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c83c5-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c83c5-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="c83c5-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="c83c5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c83c5-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="c83c5-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="c83c5-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c83c5-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c83c5-111">Return value</span></span>

<span data-ttu-id="c83c5-112">Si no se establece ninguna [marca de graduación](trackbar-control-styles.md) , devuelve 2 para los tics inicial y final.</span><span class="sxs-lookup"><span data-stu-id="c83c5-112">If no [tick flag](trackbar-control-styles.md) is set, it returns 2 for the beginning and ending ticks.</span></span> <span data-ttu-id="c83c5-113">Si se establece [**TBS \_ noticks**](trackbar-control-styles.md) , devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="c83c5-113">If [**TBS\_NOTICKS**](trackbar-control-styles.md) is set, it returns zero.</span></span> <span data-ttu-id="c83c5-114">De lo contrario, se toma la diferencia entre el intervalo mínimo y el máximo, se divide por la frecuencia de la marca y se agrega 2.</span><span class="sxs-lookup"><span data-stu-id="c83c5-114">Otherwise, it takes the difference between the range minimum and maximum, divides by the tick frequency, and adds 2.</span></span>

## <a name="remarks"></a><span data-ttu-id="c83c5-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c83c5-115">Remarks</span></span>

<span data-ttu-id="c83c5-116">El mensaje **TBM \_ GETNUMTICS** cuenta todas las marcas de graduación, incluidas la primera y la última marca de graduación creadas por la barra de aumento.</span><span class="sxs-lookup"><span data-stu-id="c83c5-116">The **TBM\_GETNUMTICS** message counts all of the tick marks, including the first and last tick marks created by the trackbar.</span></span>

## <a name="requirements"></a><span data-ttu-id="c83c5-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c83c5-117">Requirements</span></span>



| <span data-ttu-id="c83c5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c83c5-118">Requirement</span></span> | <span data-ttu-id="c83c5-119">Value</span><span class="sxs-lookup"><span data-stu-id="c83c5-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c83c5-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c83c5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c83c5-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c83c5-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c83c5-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c83c5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c83c5-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c83c5-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c83c5-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c83c5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c83c5-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c83c5-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





