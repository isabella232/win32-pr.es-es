---
title: Constantes de TF_SD_ (msctf. h)
description: Las constantes de TF \_ SD \_ \ describen el estado del documento.
ms.assetid: 953d39cd-8af1-4c86-8fb8-8b8ec917c631
topic_type:
- apiref
api_name:
- TF_SD_READONLY
- TF_SD_LOADING
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12ed0d68c8a8afd9299b908eb81a04a31fbd3d85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149960"
---
# <a name="tf_sd_-constants"></a><span data-ttu-id="0286a-103">Constantes de TF \_ SD \_ \*</span><span class="sxs-lookup"><span data-stu-id="0286a-103">TF\_SD\_\* Constants</span></span>

<span data-ttu-id="0286a-104">Las constantes de TF \_ SD \_ \* describen el estado del documento.</span><span class="sxs-lookup"><span data-stu-id="0286a-104">The TF\_SD\_\* constants describe the document status.</span></span>



| <span data-ttu-id="0286a-105">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="0286a-105">Constant/value</span></span>                                                                                                                                                                                                                              | <span data-ttu-id="0286a-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="0286a-106">Description</span></span>                                                  |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------|
| <span id="TF_SD_READONLY"></span><span id="tf_sd_readonly"></span><dl> <span data-ttu-id="0286a-107"><dt>**TF \_ SD \_ ReadOnly**</dt> <dt>(TS \_ SD \_ ReadOnly)</dt></span><span class="sxs-lookup"><span data-stu-id="0286a-107"><dt>**TF\_SD\_READONLY**</dt> <dt>( TS\_SD\_READONLY )</dt></span></span> </dl> | <span data-ttu-id="0286a-108">El documento es de solo lectura y no se puede modificar.</span><span class="sxs-lookup"><span data-stu-id="0286a-108">The document is read-only and cannot be modified.</span></span><br/> |
| <span id="TF_SD_LOADING"></span><span id="tf_sd_loading"></span><dl> <span data-ttu-id="0286a-109"><dt>**TF \_ \_carga de SD**</dt> <dt>( \_ \_ carga SD de TS)</dt></span><span class="sxs-lookup"><span data-stu-id="0286a-109"><dt>**TF\_SD\_LOADING**</dt> <dt>( TS\_SD\_LOADING )</dt></span></span> </dl>     | <span data-ttu-id="0286a-110">El documento se está cargando y puede estar incompleto.</span><span class="sxs-lookup"><span data-stu-id="0286a-110">The document is loading and can be incomplete.</span></span><br/>    |



## <a name="remarks"></a><span data-ttu-id="0286a-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0286a-111">Remarks</span></span>

<span data-ttu-id="0286a-112">El miembro **dwDynamicFlags** de la estructura de [ \_ Estado de TF](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85)) utiliza estas constantes.</span><span class="sxs-lookup"><span data-stu-id="0286a-112">The **dwDynamicFlags** member of the [TF\_STATUS](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85)) structure uses these constants.</span></span>

## <a name="requirements"></a><span data-ttu-id="0286a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0286a-113">Requirements</span></span>



| <span data-ttu-id="0286a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0286a-114">Requirement</span></span> | <span data-ttu-id="0286a-115">Value</span><span class="sxs-lookup"><span data-stu-id="0286a-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0286a-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0286a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0286a-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0286a-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="0286a-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0286a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0286a-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0286a-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="0286a-120">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="0286a-120">Redistributable</span></span><br/>          | <span data-ttu-id="0286a-121">TSF 1,0 en Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0286a-121">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="0286a-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0286a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="0286a-123"><dt>Msctf. h</dt></span><span class="sxs-lookup"><span data-stu-id="0286a-123"><dt>Msctf.h</dt></span></span> </dl>   |
| <span data-ttu-id="0286a-124">IDL</span><span class="sxs-lookup"><span data-stu-id="0286a-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0286a-125"><dt>Msctf. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0286a-125"><dt>Msctf.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0286a-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="0286a-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="0286a-127">[Estado de TF \_](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0286a-127">[TF\_STATUS](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="0286a-128">Constantes de TS \_ SD \_ \*</span><span class="sxs-lookup"><span data-stu-id="0286a-128">TS\_SD\_\* Constants</span></span>](ts-sd--constants.md)
</dt> <dt>

[<span data-ttu-id="0286a-129">ITfContextOwner:: GetStatus</span><span class="sxs-lookup"><span data-stu-id="0286a-129">ITfContextOwner::GetStatus</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontextowner-getstatus)
</dt> <dt>

[<span data-ttu-id="0286a-130">ITfContextOwnerServices:: OnStatusChange</span><span class="sxs-lookup"><span data-stu-id="0286a-130">ITfContextOwnerServices::OnStatusChange</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontextownerservices-onstatuschange)
</dt> <dt>

[<span data-ttu-id="0286a-131">ITextStoreACP:: GetStatus</span><span class="sxs-lookup"><span data-stu-id="0286a-131">ITextStoreACP::GetStatus</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getstatus)
</dt> <dt>

[<span data-ttu-id="0286a-132">ITfStatusSunk:: OnStatusChange</span><span class="sxs-lookup"><span data-stu-id="0286a-132">ITfStatusSunk::OnStatusChange</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfstatussink-onstatuschange)
</dt> </dl>

 

