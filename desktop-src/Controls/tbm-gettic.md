---
title: Mensaje de TBM_GETTIC (commctrl. h)
description: Recupera la posición lógica de una marca de graduación en una barra de aumento. La posición lógica puede ser cualquiera de los valores enteros en el intervalo de la barra de desplazamiento mínimo y máximo de posiciones de control deslizante.
ms.assetid: 9d70c860-de97-4579-bb10-e9e9db7f1784
keywords:
- TBM_GETTIC controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TBM_GETTIC
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d534d5100e20cc544c31fca2fc9e49cda3bd976
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490690"
---
# <a name="tbm_gettic-message"></a><span data-ttu-id="dea36-105">TBM \_ GETTIC</span><span class="sxs-lookup"><span data-stu-id="dea36-105">TBM\_GETTIC message</span></span>

<span data-ttu-id="dea36-106">Recupera la posición lógica de una marca de graduación en una barra de aumento.</span><span class="sxs-lookup"><span data-stu-id="dea36-106">Retrieves the logical position of a tick mark in a trackbar.</span></span> <span data-ttu-id="dea36-107">La posición lógica puede ser cualquiera de los valores enteros en el intervalo de la barra de desplazamiento mínimo y máximo de posiciones de control deslizante.</span><span class="sxs-lookup"><span data-stu-id="dea36-107">The logical position can be any of the integer values in the trackbar's range of minimum to maximum slider positions.</span></span>

## <a name="parameters"></a><span data-ttu-id="dea36-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dea36-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dea36-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dea36-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dea36-110">Índice de base cero que identifica una marca de graduación.</span><span class="sxs-lookup"><span data-stu-id="dea36-110">Zero-based index identifying a tick mark.</span></span> <span data-ttu-id="dea36-111">Los índices válidos están en el intervalo de cero a dos menos que el número de pasos que devuelve el mensaje [**\_ GETNUMTICS de TBM**](tbm-getnumtics.md) .</span><span class="sxs-lookup"><span data-stu-id="dea36-111">Valid indexes are in the range from zero to two less than the tick count returned by the [**TBM\_GETNUMTICS**](tbm-getnumtics.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="dea36-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dea36-112">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="dea36-113">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="dea36-113">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dea36-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dea36-114">Return value</span></span>

<span data-ttu-id="dea36-115">Devuelve la posición lógica de la marca de graduación especificada, o-1 si *wParam* no especifica un índice válido.</span><span class="sxs-lookup"><span data-stu-id="dea36-115">Returns the logical position of the specified tick mark, or -1 if *wParam* does not specify a valid index.</span></span>

## <a name="requirements"></a><span data-ttu-id="dea36-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dea36-116">Requirements</span></span>



| <span data-ttu-id="dea36-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="dea36-117">Requirement</span></span> | <span data-ttu-id="dea36-118">Value</span><span class="sxs-lookup"><span data-stu-id="dea36-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dea36-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dea36-119">Minimum supported client</span></span><br/> | <span data-ttu-id="dea36-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="dea36-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dea36-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dea36-121">Minimum supported server</span></span><br/> | <span data-ttu-id="dea36-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="dea36-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dea36-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dea36-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="dea36-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="dea36-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





