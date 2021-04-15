---
title: Mensaje de RB_MOVEBAND (commctrl. h)
description: Mueve una banda de un índice a otro.
ms.assetid: bb5b45de-957e-46fb-b59a-18b55b69c395
keywords:
- RB_MOVEBAND controles de mensajes de Windows
topic_type:
- apiref
api_name:
- RB_MOVEBAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 146103c4c3d70fc0514729a00eac152c4847b85c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489233"
---
# <a name="rb_moveband-message"></a><span data-ttu-id="4ecc9-104">Mensaje de MOVEBAND de RB \_</span><span class="sxs-lookup"><span data-stu-id="4ecc9-104">RB\_MOVEBAND message</span></span>

<span data-ttu-id="4ecc9-105">Mueve una banda de un índice a otro.</span><span class="sxs-lookup"><span data-stu-id="4ecc9-105">Moves a band from one index to another.</span></span>

## <a name="parameters"></a><span data-ttu-id="4ecc9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4ecc9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ecc9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4ecc9-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4ecc9-108">Índice de base cero de la banda que se va a desplace.</span><span class="sxs-lookup"><span data-stu-id="4ecc9-108">Zero-based index of the band to be moved.</span></span>

</dd> <dt>

<span data-ttu-id="4ecc9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4ecc9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4ecc9-110">Índice de base cero de la nueva posición de banda.</span><span class="sxs-lookup"><span data-stu-id="4ecc9-110">Zero-based index of the new band position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ecc9-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4ecc9-111">Return value</span></span>

<span data-ttu-id="4ecc9-112">Devuelve un valor distinto de cero si es correcto o cero de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="4ecc9-112">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ecc9-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4ecc9-113">Remarks</span></span>

<span data-ttu-id="4ecc9-114">Probablemente, este mensaje cambiará el índice de otras bandas en el control rebar.</span><span class="sxs-lookup"><span data-stu-id="4ecc9-114">This message will most likely change the index of other bands in the rebar control.</span></span> <span data-ttu-id="4ecc9-115">Si una banda se mueve del índice 6 al índice 0, se incrementará el índice en todas las bandas entre ellas.</span><span class="sxs-lookup"><span data-stu-id="4ecc9-115">If a band is moved from index 6 to index 0, all of the bands in between will have their index incremented by one.</span></span>

<span data-ttu-id="4ecc9-116">*lParam* nunca debe ser mayor que el número de bandas menos uno.</span><span class="sxs-lookup"><span data-stu-id="4ecc9-116">*lParam* must never be greater than the number of bands minus one.</span></span> <span data-ttu-id="4ecc9-117">El número de bandas puede obtenerse con el mensaje [**RB \_ GETBANDCOUNT**](rb-getbandcount.md) .</span><span class="sxs-lookup"><span data-stu-id="4ecc9-117">The number of bands can be obtained with the [**RB\_GETBANDCOUNT**](rb-getbandcount.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ecc9-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ecc9-118">Requirements</span></span>



| <span data-ttu-id="4ecc9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ecc9-119">Requirement</span></span> | <span data-ttu-id="4ecc9-120">Value</span><span class="sxs-lookup"><span data-stu-id="4ecc9-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4ecc9-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4ecc9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4ecc9-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4ecc9-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4ecc9-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4ecc9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4ecc9-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="4ecc9-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4ecc9-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4ecc9-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ecc9-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ecc9-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





