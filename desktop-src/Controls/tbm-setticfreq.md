---
title: Mensaje de TBM_SETTICFREQ (commctrl. h)
description: Establece la frecuencia de intervalo para las marcas de graduación en una barra de aumento.
ms.assetid: c391260c-d6c2-4b6a-84e8-7fe5d734035b
keywords:
- TBM_SETTICFREQ controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TBM_SETTICFREQ
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b68a555a7803e663fa1708fc02214deecbb05aad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079122"
---
# <a name="tbm_setticfreq-message"></a><span data-ttu-id="1ebe5-104">TBM \_ SETTICFREQ</span><span class="sxs-lookup"><span data-stu-id="1ebe5-104">TBM\_SETTICFREQ message</span></span>

<span data-ttu-id="1ebe5-105">Establece la frecuencia de intervalo para las marcas de graduación en una barra de aumento.</span><span class="sxs-lookup"><span data-stu-id="1ebe5-105">Sets the interval frequency for tick marks in a trackbar.</span></span> <span data-ttu-id="1ebe5-106">Por ejemplo, si la frecuencia se establece en dos, se muestra una marca de graduación para cada incremento en el intervalo de la barra de aumento.</span><span class="sxs-lookup"><span data-stu-id="1ebe5-106">For example, if the frequency is set to two, a tick mark is displayed for every other increment in the trackbar's range.</span></span> <span data-ttu-id="1ebe5-107">El valor predeterminado de la frecuencia es uno; es decir, cada incremento del intervalo está asociado a una marca de graduación.</span><span class="sxs-lookup"><span data-stu-id="1ebe5-107">The default setting for the frequency is one; that is, every increment in the range is associated with a tick mark.</span></span>

## <a name="parameters"></a><span data-ttu-id="1ebe5-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1ebe5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ebe5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1ebe5-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1ebe5-110">Frecuencia de las marcas de graduación.</span><span class="sxs-lookup"><span data-stu-id="1ebe5-110">Frequency of the tick marks.</span></span>

</dd> <dt>

<span data-ttu-id="1ebe5-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1ebe5-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="1ebe5-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="1ebe5-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ebe5-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1ebe5-113">Return value</span></span>

<span data-ttu-id="1ebe5-114">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="1ebe5-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ebe5-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1ebe5-115">Remarks</span></span>

<span data-ttu-id="1ebe5-116">La barra de aumento debe tener el estilo de [**\_ marcas de graduación de TBS**](trackbar-control-styles.md) para utilizar este mensaje.</span><span class="sxs-lookup"><span data-stu-id="1ebe5-116">The trackbar must have the [**TBS\_AUTOTICKS**](trackbar-control-styles.md) style to use this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ebe5-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ebe5-117">Requirements</span></span>



| <span data-ttu-id="1ebe5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ebe5-118">Requirement</span></span> | <span data-ttu-id="1ebe5-119">Value</span><span class="sxs-lookup"><span data-stu-id="1ebe5-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1ebe5-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1ebe5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1ebe5-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1ebe5-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1ebe5-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1ebe5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1ebe5-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="1ebe5-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1ebe5-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1ebe5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ebe5-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ebe5-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





