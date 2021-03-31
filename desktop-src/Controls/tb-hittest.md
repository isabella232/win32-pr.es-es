---
title: Mensaje de TB_HITTEST (commctrl. h)
description: Determina dónde se encuentra un punto en un control de barra de herramientas.
ms.assetid: d08f3805-2042-470e-8f5a-8a6a681d1189
keywords:
- TB_HITTEST controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6264bc0191f091d3819081ddd67e428b64c84570
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996211"
---
# <a name="tb_hittest-message"></a><span data-ttu-id="4bbac-104">TB \_ mensaje HITTEST</span><span class="sxs-lookup"><span data-stu-id="4bbac-104">TB\_HITTEST message</span></span>

<span data-ttu-id="4bbac-105">Determina dónde se encuentra un punto en un control de barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="4bbac-105">Determines where a point lies in a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="4bbac-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4bbac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4bbac-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4bbac-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="4bbac-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="4bbac-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="4bbac-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4bbac-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4bbac-110">Puntero a una estructura de [**punto**](/previous-versions//dd162805(v=vs.85)) que contiene la coordenada x de la prueba de posicionamiento en el miembro **x** y la coordenada y de la prueba de posicionamiento en el miembro **y** .</span><span class="sxs-lookup"><span data-stu-id="4bbac-110">Pointer to a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure that contains the x-coordinate of the hit test in the **x** member and the y-coordinate of the hit test in the **y** member.</span></span> <span data-ttu-id="4bbac-111">Las coordenadas son relativas al área cliente de la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="4bbac-111">The coordinates are relative to the toolbar's client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4bbac-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4bbac-112">Return value</span></span>

<span data-ttu-id="4bbac-113">Devuelve un valor entero.</span><span class="sxs-lookup"><span data-stu-id="4bbac-113">Returns an integer value.</span></span> <span data-ttu-id="4bbac-114">Si el valor devuelto es cero o un valor positivo, es el índice de base cero del elemento no separador en el que se encuentra el punto.</span><span class="sxs-lookup"><span data-stu-id="4bbac-114">If the return value is zero or a positive value, it is the zero-based index of the nonseparator item in which the point lies.</span></span> <span data-ttu-id="4bbac-115">Si el valor devuelto es negativo, el punto no está dentro de un botón.</span><span class="sxs-lookup"><span data-stu-id="4bbac-115">If the return value is negative, the point does not lie within a button.</span></span> <span data-ttu-id="4bbac-116">El valor absoluto del valor devuelto es el índice de un elemento separador o el elemento no separador más cercano.</span><span class="sxs-lookup"><span data-stu-id="4bbac-116">The absolute value of the return value is the index of a separator item or the nearest nonseparator item.</span></span>

## <a name="requirements"></a><span data-ttu-id="4bbac-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4bbac-117">Requirements</span></span>



| <span data-ttu-id="4bbac-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="4bbac-118">Requirement</span></span> | <span data-ttu-id="4bbac-119">Value</span><span class="sxs-lookup"><span data-stu-id="4bbac-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4bbac-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4bbac-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4bbac-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4bbac-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4bbac-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4bbac-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4bbac-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="4bbac-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4bbac-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4bbac-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="4bbac-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4bbac-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

