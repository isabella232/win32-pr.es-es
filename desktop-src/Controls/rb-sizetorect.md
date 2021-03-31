---
title: Mensaje de RB_SIZETORECT (commctrl. h)
description: Intenta encontrar el mejor diseño de las bandas del rectángulo especificado.
ms.assetid: c6242b54-bd65-489b-b417-9680cc39b64a
keywords:
- RB_SIZETORECT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- RB_SIZETORECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3db5727ee8c94d2473b503c9a81b7669bb829a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151143"
---
# <a name="rb_sizetorect-message"></a><span data-ttu-id="30f81-104">Mensaje de SIZETORECT de RB \_</span><span class="sxs-lookup"><span data-stu-id="30f81-104">RB\_SIZETORECT message</span></span>

<span data-ttu-id="30f81-105">Intenta encontrar el mejor diseño de las bandas del rectángulo especificado.</span><span class="sxs-lookup"><span data-stu-id="30f81-105">Attempts to find the best layout of the bands for the given rectangle.</span></span>

## <a name="parameters"></a><span data-ttu-id="30f81-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="30f81-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30f81-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="30f81-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="30f81-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="30f81-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="30f81-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="30f81-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="30f81-110">Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que especifica el rectángulo al que se debe ajustar el tamaño del control rebar.</span><span class="sxs-lookup"><span data-stu-id="30f81-110">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that specifies the rectangle to which the rebar control should be sized.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30f81-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="30f81-111">Return value</span></span>

<span data-ttu-id="30f81-112">Devuelve un valor distinto de cero si se ha producido un cambio de diseño o cero en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="30f81-112">Returns nonzero if a layout change occurred, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="30f81-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="30f81-113">Remarks</span></span>

<span data-ttu-id="30f81-114">Las bandas rebar se organizarán y ajustarán según sea necesario para ajustarse al rectángulo.</span><span class="sxs-lookup"><span data-stu-id="30f81-114">The rebar bands will be arranged and wrapped as necessary to fit the rectangle.</span></span> <span data-ttu-id="30f81-115">Se cambiará el tamaño de las bandas que tengan el estilo RBBS VARIABLEHEIGHT de la \_ manera más uniforme posible para ajustar el rectángulo.</span><span class="sxs-lookup"><span data-stu-id="30f81-115">Bands that have the RBBS\_VARIABLEHEIGHT style will be resized as evenly as possible to fit the rectangle.</span></span> <span data-ttu-id="30f81-116">El alto de un rebar horizontal o el ancho de un rebar vertical puede cambiar en función del nuevo diseño.</span><span class="sxs-lookup"><span data-stu-id="30f81-116">The height of a horizontal rebar or the width of a vertical rebar may change, depending on the new layout.</span></span>

## <a name="requirements"></a><span data-ttu-id="30f81-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30f81-117">Requirements</span></span>



| <span data-ttu-id="30f81-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="30f81-118">Requirement</span></span> | <span data-ttu-id="30f81-119">Value</span><span class="sxs-lookup"><span data-stu-id="30f81-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="30f81-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="30f81-120">Minimum supported client</span></span><br/> | <span data-ttu-id="30f81-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="30f81-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="30f81-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="30f81-122">Minimum supported server</span></span><br/> | <span data-ttu-id="30f81-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="30f81-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="30f81-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="30f81-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="30f81-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="30f81-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

