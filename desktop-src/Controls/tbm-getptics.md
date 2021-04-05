---
title: Mensaje de TBM_GETPTICS (commctrl. h)
description: Recupera la dirección de una matriz que contiene las posiciones de las marcas de paso de una barra de aumento.
ms.assetid: d15a4b4d-2ced-40a4-9351-ed7ecc5a5751
keywords:
- TBM_GETPTICS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TBM_GETPTICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d5d81e67156c0118310017413b8e73714246b7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996425"
---
# <a name="tbm_getptics-message"></a><span data-ttu-id="dbaf3-104">TBM \_ GETPTICS</span><span class="sxs-lookup"><span data-stu-id="dbaf3-104">TBM\_GETPTICS message</span></span>

<span data-ttu-id="dbaf3-105">Recupera la dirección de una matriz que contiene las posiciones de las marcas de paso de una barra de aumento.</span><span class="sxs-lookup"><span data-stu-id="dbaf3-105">Retrieves the address of an array that contains the positions of the tick marks for a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="dbaf3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dbaf3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbaf3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dbaf3-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="dbaf3-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="dbaf3-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="dbaf3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dbaf3-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="dbaf3-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="dbaf3-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbaf3-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dbaf3-111">Return value</span></span>

<span data-ttu-id="dbaf3-112">Devuelve la dirección de una matriz de valores **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="dbaf3-112">Returns the address of an array of **DWORD** values.</span></span> <span data-ttu-id="dbaf3-113">Los elementos de la matriz especifican las posiciones lógicas de las marcas de graduación de la barra de aumento, sin incluir la primera y la última marca de graduación creada por la barra de aumento.</span><span class="sxs-lookup"><span data-stu-id="dbaf3-113">The elements of the array specify the logical positions of the trackbar's tick marks, not including the first and last tick marks created by the trackbar.</span></span> <span data-ttu-id="dbaf3-114">Las posiciones lógicas pueden ser cualquiera de los valores enteros del intervalo de la barra de desplazamiento mínimo y máximo de posiciones de control deslizante.</span><span class="sxs-lookup"><span data-stu-id="dbaf3-114">The logical positions can be any of the integer values in the trackbar's range of minimum to maximum slider positions.</span></span>

## <a name="remarks"></a><span data-ttu-id="dbaf3-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dbaf3-115">Remarks</span></span>

<span data-ttu-id="dbaf3-116">El número de elementos de la matriz es dos veces menor que el número de pasos devuelto por el mensaje [**\_ GETNUMTICS de TBM**](tbm-getnumtics.md) .</span><span class="sxs-lookup"><span data-stu-id="dbaf3-116">The number of elements in the array is two less than the tick count returned by the [**TBM\_GETNUMTICS**](tbm-getnumtics.md) message.</span></span> <span data-ttu-id="dbaf3-117">Tenga en cuenta que los valores de la matriz pueden incluir posiciones duplicadas y que no estén en orden secuencial.</span><span class="sxs-lookup"><span data-stu-id="dbaf3-117">Note that the values in the array may include duplicate positions and may not be in sequential order.</span></span> <span data-ttu-id="dbaf3-118">El puntero devuelto es válido hasta que se cambian las marcas de graduación de la barra de resultados.</span><span class="sxs-lookup"><span data-stu-id="dbaf3-118">The returned pointer is valid until you change the trackbar's tick marks.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbaf3-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dbaf3-119">Requirements</span></span>



| <span data-ttu-id="dbaf3-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="dbaf3-120">Requirement</span></span> | <span data-ttu-id="dbaf3-121">Value</span><span class="sxs-lookup"><span data-stu-id="dbaf3-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dbaf3-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dbaf3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="dbaf3-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="dbaf3-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dbaf3-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dbaf3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="dbaf3-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="dbaf3-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dbaf3-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dbaf3-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="dbaf3-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="dbaf3-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





