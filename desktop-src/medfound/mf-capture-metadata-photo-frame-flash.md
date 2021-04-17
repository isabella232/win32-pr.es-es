---
description: Indica si se desencadenó un flash para el fotograma capturado.
ms.assetid: CF900CB4-8967-40F3-B60C-867192A641E9
title: MF_CAPTURE_METADATA_PHOTO_FRAME_FLASH atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ff5e9a47c07c8d7a2cec4e7dbf7b34669301122
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696760"
---
# <a name="mf_capture_metadata_photo_frame_flash-attribute"></a><span data-ttu-id="50a04-103">\_Atributo de \_ \_ \_ fotograma fotográfico de METAdatos de captura MF \_</span><span class="sxs-lookup"><span data-stu-id="50a04-103">MF\_CAPTURE\_METADATA\_PHOTO\_FRAME\_FLASH attribute</span></span>

<span data-ttu-id="50a04-104">Indica si se desencadenó un flash para el fotograma capturado.</span><span class="sxs-lookup"><span data-stu-id="50a04-104">Indicates if a flash was triggered for the captured frame.</span></span>

## <a name="data-type"></a><span data-ttu-id="50a04-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="50a04-105">Data type</span></span>

<span data-ttu-id="50a04-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="50a04-106">**UINT32**</span></span>



| <span data-ttu-id="50a04-107">Value</span><span class="sxs-lookup"><span data-stu-id="50a04-107">Value</span></span>                                                                               | <span data-ttu-id="50a04-108">Significado</span><span class="sxs-lookup"><span data-stu-id="50a04-108">Meaning</span></span>                                                                                                                                               |
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="50a04-109"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="50a04-109"><dt>0</dt></span></span> </dl>        | <span data-ttu-id="50a04-110">No se activó un flash en este marco.</span><span class="sxs-lookup"><span data-stu-id="50a04-110">A flash was not triggered on this frame.</span></span><br/>                                                                                                   |
| <dl> <span data-ttu-id="50a04-111"><dt>distinto de cero</dt></span><span class="sxs-lookup"><span data-stu-id="50a04-111"><dt>non-zero</dt></span></span> </dl> | <span data-ttu-id="50a04-112">Se desencadenó un flash en este marco.</span><span class="sxs-lookup"><span data-stu-id="50a04-112">A flash was triggered on this frame.</span></span><br/>                                                                                                       |
| <dl> <span data-ttu-id="50a04-113"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="50a04-113"><dt>1</dt></span></span> </dl>        | <span data-ttu-id="50a04-114">Reservado</span><span class="sxs-lookup"><span data-stu-id="50a04-114">Reserved</span></span><br/> <span data-ttu-id="50a04-115">No Compruebe explícitamente si el valor es 1.</span><span class="sxs-lookup"><span data-stu-id="50a04-115">Do not explicitly check for a value of 1.</span></span> <span data-ttu-id="50a04-116">Las aplicaciones solo deben buscar! = 0 para indicar si se desencadenó un flash.</span><span class="sxs-lookup"><span data-stu-id="50a04-116">Applications should only check for !=0 to indicate if a flash was triggered.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="50a04-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50a04-117">Requirements</span></span>



| <span data-ttu-id="50a04-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="50a04-118">Requirement</span></span> | <span data-ttu-id="50a04-119">Value</span><span class="sxs-lookup"><span data-stu-id="50a04-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="50a04-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="50a04-120">Minimum supported client</span></span><br/> | <span data-ttu-id="50a04-121">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="50a04-121">Windows 8.1 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="50a04-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="50a04-122">Minimum supported server</span></span><br/> | <span data-ttu-id="50a04-123">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="50a04-123">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="50a04-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="50a04-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="50a04-125"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="50a04-125"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50a04-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="50a04-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50a04-127">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="50a04-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




