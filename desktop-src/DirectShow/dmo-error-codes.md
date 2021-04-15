---
description: La tabla siguiente contiene códigos de error específicos de Microsoft DirectX media Objects (DMOs). Estos códigos de error se definen en el archivo de encabezado Mediaerr. h.
ms.assetid: 1ded5656-084d-4315-a414-aebf4a1820dc
title: Códigos de error de DMO (Mediaerr. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d76c8cd5e7001751cd2cf9eb7da4d88b2dc100bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653943"
---
# <a name="dmo-error-codes"></a><span data-ttu-id="7fbdf-104">Códigos de error de DMO</span><span class="sxs-lookup"><span data-stu-id="7fbdf-104">DMO Error Codes</span></span>

<span data-ttu-id="7fbdf-105">La tabla siguiente contiene códigos de error específicos de Microsoft DirectX media Objects (DMOs).</span><span class="sxs-lookup"><span data-stu-id="7fbdf-105">The following table contains error codes that are specific to Microsoft DirectX Media Objects (DMOs).</span></span> <span data-ttu-id="7fbdf-106">Estos códigos de error se definen en el archivo de encabezado Mediaerr. h.</span><span class="sxs-lookup"><span data-stu-id="7fbdf-106">These error codes are defined in the header file Mediaerr.h.</span></span>



| <span data-ttu-id="7fbdf-107">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="7fbdf-107">Constant/value</span></span>                                                                                                                                                                                                                                                  | <span data-ttu-id="7fbdf-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="7fbdf-108">Description</span></span>                                                                                                                                                         |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DMO_E_INVALIDSTREAMINDEX"></span><span id="dmo_e_invalidstreamindex"></span><dl> <span data-ttu-id="7fbdf-109"><dt>**DMO \_ E \_ INVALIDSTREAMINDEX**</dt> <dt>0x80040201</dt></span><span class="sxs-lookup"><span data-stu-id="7fbdf-109"><dt>**DMO\_E\_INVALIDSTREAMINDEX**</dt> <dt>0x80040201</dt></span></span> </dl> | <span data-ttu-id="7fbdf-110">Índice de secuencia no válido.</span><span class="sxs-lookup"><span data-stu-id="7fbdf-110">Invalid stream index.</span></span><br/>                                                                                                                                    |
| <span id="DMO_E_INVALIDTYPE"></span><span id="dmo_e_invalidtype"></span><dl> <span data-ttu-id="7fbdf-111"><dt>**DMO \_ E \_ INVALIDTYPE**</dt> <dt>0x80040202</dt></span><span class="sxs-lookup"><span data-stu-id="7fbdf-111"><dt>**DMO\_E\_INVALIDTYPE**</dt> <dt>0x80040202</dt></span></span> </dl>                      | <span data-ttu-id="7fbdf-112">Tipo de medio no válido.</span><span class="sxs-lookup"><span data-stu-id="7fbdf-112">Invalid media type.</span></span><br/>                                                                                                                                      |
| <span id="DMO_E_TYPE_NOT_SET"></span><span id="dmo_e_type_not_set"></span><dl> <span data-ttu-id="7fbdf-113"><dt>**DMO \_ E \_ tipo \_ no \_ establecido**</dt> <dt>0x80040203</dt></span><span class="sxs-lookup"><span data-stu-id="7fbdf-113"><dt>**DMO\_E\_TYPE\_NOT\_SET**</dt> <dt>0x80040203</dt></span></span> </dl>                 | <span data-ttu-id="7fbdf-114">No se estableció el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="7fbdf-114">Media type was not set.</span></span> <span data-ttu-id="7fbdf-115">Una o más secuencias requieren un tipo de medio para poder realizar esta operación.</span><span class="sxs-lookup"><span data-stu-id="7fbdf-115">One or more streams require a media type before this operation can be performed.</span></span><br/>                                                 |
| <span id="DMO_E_NOTACCEPTING"></span><span id="dmo_e_notaccepting"></span><dl> <span data-ttu-id="7fbdf-116"><dt>**DMO \_ E \_ NOTACCEPTING**</dt> <dt>0x80040204</dt></span><span class="sxs-lookup"><span data-stu-id="7fbdf-116"><dt>**DMO\_E\_NOTACCEPTING**</dt> <dt>0x80040204</dt></span></span> </dl>                   | <span data-ttu-id="7fbdf-117">No se pueden aceptar datos en esta secuencia.</span><span class="sxs-lookup"><span data-stu-id="7fbdf-117">Data cannot be accepted on this stream.</span></span> <span data-ttu-id="7fbdf-118">Es posible que tenga que procesar más datos de salida; vea [**IMediaObject::P rocessinput**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processinput).</span><span class="sxs-lookup"><span data-stu-id="7fbdf-118">You might need to process more output data; see [**IMediaObject::ProcessInput**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processinput).</span></span><br/> |
| <span id="DMO_E_TYPE_NOT_ACCEPTED"></span><span id="dmo_e_type_not_accepted"></span><dl> <span data-ttu-id="7fbdf-119"><dt>**DMO \_ E \_ tipo \_ no \_ aceptado**</dt> <dt>0x80040205</dt></span><span class="sxs-lookup"><span data-stu-id="7fbdf-119"><dt>**DMO\_E\_TYPE\_NOT\_ACCEPTED**</dt> <dt>0x80040205</dt></span></span> </dl>  | <span data-ttu-id="7fbdf-120">No se aceptó el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="7fbdf-120">Media type was not accepted.</span></span><br/>                                                                                                                             |
| <span id="DMO_E_NO_MORE_ITEMS"></span><span id="dmo_e_no_more_items"></span><dl> <span data-ttu-id="7fbdf-121"><dt>**DMO \_ E \_ no hay \_ más \_ elementos**</dt> <dt>0x80040206</dt></span><span class="sxs-lookup"><span data-stu-id="7fbdf-121"><dt>**DMO\_E\_NO\_MORE\_ITEMS**</dt> <dt>0x80040206</dt></span></span> </dl>              | <span data-ttu-id="7fbdf-122">El índice de tipo de medio está fuera del intervalo.</span><span class="sxs-lookup"><span data-stu-id="7fbdf-122">Media-type index is out of range.</span></span><br/>                                                                                                                        |



## <a name="requirements"></a><span data-ttu-id="7fbdf-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7fbdf-123">Requirements</span></span>



| <span data-ttu-id="7fbdf-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="7fbdf-124">Requirement</span></span> | <span data-ttu-id="7fbdf-125">Value</span><span class="sxs-lookup"><span data-stu-id="7fbdf-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7fbdf-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7fbdf-126">Header</span></span><br/> | <dl> <span data-ttu-id="7fbdf-127"><dt>Mediaerr. h</dt></span><span class="sxs-lookup"><span data-stu-id="7fbdf-127"><dt>Mediaerr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fbdf-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="7fbdf-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fbdf-129">Constantes de DMO</span><span class="sxs-lookup"><span data-stu-id="7fbdf-129">DMO Constants</span></span>](dmo-constants.md)
</dt> </dl>

 

 




