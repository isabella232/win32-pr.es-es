---
title: Códigos de error de WER (Werapi. h)
description: En la tabla siguiente se proporciona una lista de códigos de error personalizados usados por Informe de errores de Windows.
ms.assetid: c409b222-5e02-4b48-b39a-f2e29d199944
topic_type:
- apiref
api_name:
- WER_E_INSUFFICIENT_BUFFER
- WER_E_INVALID_STATE
- WER_E_LENGTH_EXCEEDED
- WER_E_MISSING_PARAM
- WER_E_NOT_FOUND
- WER_E_STORE_DISABLED
api_location:
- Werapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cc4c37d21a38679f1ea36151eb14d21a6c43af0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695910"
---
# <a name="wer-error-codes"></a><span data-ttu-id="2ec94-103">Códigos de error de WER</span><span class="sxs-lookup"><span data-stu-id="2ec94-103">WER Error Codes</span></span>

<span data-ttu-id="2ec94-104">En la tabla siguiente se proporciona una lista de códigos de error personalizados usados por Informe de errores de Windows.</span><span class="sxs-lookup"><span data-stu-id="2ec94-104">The following table provides a list of custom error codes used by Windows Error Reporting.</span></span>



| <span data-ttu-id="2ec94-105">Constante</span><span class="sxs-lookup"><span data-stu-id="2ec94-105">Constant</span></span>                                                                                                                                                                                            | <span data-ttu-id="2ec94-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="2ec94-106">Description</span></span>                                                |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------|
| <span id="WER_E_INSUFFICIENT_BUFFER"></span><span id="wer_e_insufficient_buffer"></span><dl> <span data-ttu-id="2ec94-107"><dt>**\_ \_ búfer insuficiente de Wer \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2ec94-107"><dt>**WER\_E\_INSUFFICIENT\_BUFFER**</dt></span></span> </dl> | <span data-ttu-id="2ec94-108">Un búfer es demasiado pequeño para contener los datos.</span><span class="sxs-lookup"><span data-stu-id="2ec94-108">A buffer is too small to contain the data.</span></span><br/>      |
| <span id="WER_E_INVALID_STATE"></span><span id="wer_e_invalid_state"></span><dl> <span data-ttu-id="2ec94-109"><dt>**\_ \_ Estado no válido de Wer E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2ec94-109"><dt>**WER\_E\_INVALID\_STATE**</dt></span></span> </dl>                   | <span data-ttu-id="2ec94-110">Se llamó a una función de forma no compatible.</span><span class="sxs-lookup"><span data-stu-id="2ec94-110">A function was called in an unsupported manner.</span></span><br/> |
| <span id="WER_E_LENGTH_EXCEEDED"></span><span id="wer_e_length_exceeded"></span><dl> <span data-ttu-id="2ec94-111"><dt>**\_ \_ longitud \_ superada de Wer E**</dt></span><span class="sxs-lookup"><span data-stu-id="2ec94-111"><dt>**WER\_E\_LENGTH\_EXCEEDED**</dt></span></span> </dl>             | <span data-ttu-id="2ec94-112">Se ha superado uno de los límites de longitud.</span><span class="sxs-lookup"><span data-stu-id="2ec94-112">One of the length limits has been exceeded.</span></span><br/>     |
| <span id="WER_E_MISSING_PARAM"></span><span id="wer_e_missing_param"></span><dl> <span data-ttu-id="2ec94-113"><dt>**falta el parámetro de WER \_ E \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2ec94-113"><dt>**WER\_E\_MISSING\_PARAM**</dt></span></span> </dl>                   | <span data-ttu-id="2ec94-114">Faltan uno o varios parámetros.</span><span class="sxs-lookup"><span data-stu-id="2ec94-114">One or more parameters are missing.</span></span><br/>             |
| <span id="WER_E_NOT_FOUND"></span><span id="wer_e_not_found"></span><dl> <span data-ttu-id="2ec94-115"><dt>**WER \_ E \_ no \_ encontrado**</dt></span><span class="sxs-lookup"><span data-stu-id="2ec94-115"><dt>**WER\_E\_NOT\_FOUND**</dt></span></span> </dl>                               | <span data-ttu-id="2ec94-116">Elemento no encontrado.</span><span class="sxs-lookup"><span data-stu-id="2ec94-116">Element not found.</span></span><br/>                              |
| <span id="WER_E_STORE_DISABLED"></span><span id="wer_e_store_disabled"></span><dl> <span data-ttu-id="2ec94-117"><dt>**almacén de WER \_ E \_ \_ deshabilitado**</dt></span><span class="sxs-lookup"><span data-stu-id="2ec94-117"><dt>**WER\_E\_STORE\_DISABLED**</dt></span></span> </dl>                | <span data-ttu-id="2ec94-118">Se ha deshabilitado el almacén.</span><span class="sxs-lookup"><span data-stu-id="2ec94-118">The store has been disabled.</span></span><br/>                    |



## <a name="requirements"></a><span data-ttu-id="2ec94-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ec94-119">Requirements</span></span>



| <span data-ttu-id="2ec94-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ec94-120">Requirement</span></span> | <span data-ttu-id="2ec94-121">Value</span><span class="sxs-lookup"><span data-stu-id="2ec94-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2ec94-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2ec94-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2ec94-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2ec94-123">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="2ec94-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2ec94-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2ec94-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="2ec94-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="2ec94-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2ec94-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ec94-127"><dt>Werapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ec94-127"><dt>Werapi.h</dt></span></span> </dl> |



 

 





