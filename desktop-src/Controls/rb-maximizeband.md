---
title: Mensaje de RB_MAXIMIZEBAND (commctrl. h)
description: Cambia el tamaño de una banda de un control rebar a su tamaño ideal o mayor.
ms.assetid: 79fff6d0-01f2-4308-b916-38dc06dad894
keywords:
- RB_MAXIMIZEBAND controles de mensajes de Windows
topic_type:
- apiref
api_name:
- RB_MAXIMIZEBAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 708a8fae7c0dd8e72eea8e5acefe43ab50054592
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905420"
---
# <a name="rb_maximizeband-message"></a><span data-ttu-id="870d3-104">Mensaje de MAXIMIZEBAND de RB \_</span><span class="sxs-lookup"><span data-stu-id="870d3-104">RB\_MAXIMIZEBAND message</span></span>

<span data-ttu-id="870d3-105">Cambia el tamaño de una banda de un control rebar a su tamaño ideal o mayor.</span><span class="sxs-lookup"><span data-stu-id="870d3-105">Resizes a band in a rebar control to either its ideal or largest size.</span></span>

## <a name="parameters"></a><span data-ttu-id="870d3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="870d3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="870d3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="870d3-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="870d3-108">Índice de base cero de la banda que se va a maximizar.</span><span class="sxs-lookup"><span data-stu-id="870d3-108">Zero-based index of the band to be maximized.</span></span>

</dd> <dt>

<span data-ttu-id="870d3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="870d3-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="870d3-110">Indica si se debe usar el ancho ideal de la banda cuando la banda está maximizada.</span><span class="sxs-lookup"><span data-stu-id="870d3-110">Indicates if the ideal width of the band should be used when the band is maximized.</span></span> <span data-ttu-id="870d3-111">Si este valor es distinto de cero, se usará el ancho ideal.</span><span class="sxs-lookup"><span data-stu-id="870d3-111">If this value is nonzero, the ideal width will be used.</span></span> <span data-ttu-id="870d3-112">Si este valor es cero, la banda se hará lo más grande posible.</span><span class="sxs-lookup"><span data-stu-id="870d3-112">If this value is zero, the band will be made as large as possible.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="870d3-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="870d3-113">Return value</span></span>

<span data-ttu-id="870d3-114">No se utiliza el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="870d3-114">The return value is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="870d3-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="870d3-115">Requirements</span></span>



| <span data-ttu-id="870d3-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="870d3-116">Requirement</span></span> | <span data-ttu-id="870d3-117">Value</span><span class="sxs-lookup"><span data-stu-id="870d3-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="870d3-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="870d3-118">Minimum supported client</span></span><br/> | <span data-ttu-id="870d3-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="870d3-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="870d3-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="870d3-120">Minimum supported server</span></span><br/> | <span data-ttu-id="870d3-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="870d3-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="870d3-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="870d3-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="870d3-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="870d3-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="870d3-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="870d3-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="870d3-125">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="870d3-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="870d3-126">**\_SETBANDINFO RB**</span><span class="sxs-lookup"><span data-stu-id="870d3-126">**RB\_SETBANDINFO**</span></span>](rb-setbandinfo.md)
</dt> </dl>

 

 





