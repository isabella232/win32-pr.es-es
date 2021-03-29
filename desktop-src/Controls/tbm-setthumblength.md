---
title: Mensaje de TBM_SETTHUMBLENGTH (commctrl. h)
description: Establece la longitud del control deslizante en una barra de desplazamiento. Este mensaje se omite si TrackBar no tiene el \_ estilo FIXEDLENGTH de TBS.
ms.assetid: 027fe341-a60a-4dbe-a48a-5ddaadef0b4a
keywords:
- TBM_SETTHUMBLENGTH controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TBM_SETTHUMBLENGTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d4ac33d2df43a267766e14ab95fb9729692bbee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535127"
---
# <a name="tbm_setthumblength-message"></a><span data-ttu-id="d9eec-105">TBM \_ SETTHUMBLENGTH</span><span class="sxs-lookup"><span data-stu-id="d9eec-105">TBM\_SETTHUMBLENGTH message</span></span>

<span data-ttu-id="d9eec-106">Establece la longitud del control deslizante en una barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="d9eec-106">Sets the length of the slider in a trackbar.</span></span> <span data-ttu-id="d9eec-107">Este mensaje se omite si TrackBar no tiene el estilo [**\_ FIXEDLENGTH de TBS**](trackbar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="d9eec-107">This message is ignored if the trackbar does not have the [**TBS\_FIXEDLENGTH**](trackbar-control-styles.md) style.</span></span>

## <a name="parameters"></a><span data-ttu-id="d9eec-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d9eec-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9eec-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d9eec-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d9eec-110">Longitud, en píxeles, del control deslizante.</span><span class="sxs-lookup"><span data-stu-id="d9eec-110">Length, in pixels, of the slider.</span></span>

</dd> <dt>

<span data-ttu-id="d9eec-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d9eec-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d9eec-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="d9eec-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9eec-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d9eec-113">Return value</span></span>

<span data-ttu-id="d9eec-114">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="d9eec-114">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9eec-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9eec-115">Requirements</span></span>



| <span data-ttu-id="d9eec-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9eec-116">Requirement</span></span> | <span data-ttu-id="d9eec-117">Value</span><span class="sxs-lookup"><span data-stu-id="d9eec-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d9eec-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d9eec-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d9eec-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d9eec-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d9eec-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d9eec-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d9eec-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d9eec-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d9eec-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d9eec-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9eec-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9eec-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9eec-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="d9eec-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9eec-125">**TBM \_ GETTHUMBLENGTH**</span><span class="sxs-lookup"><span data-stu-id="d9eec-125">**TBM\_GETTHUMBLENGTH**</span></span>](tbm-getthumblength.md)
</dt> </dl>

 

 





