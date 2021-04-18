---
title: Constantes de TS_LF_ (Textstor. h)
description: Las \_ constantes LF \_ de TS \ especifican el tipo de bloqueo del documento.
ms.assetid: f0bb6ef9-a8fc-4331-9210-6c5ba1721a73
topic_type:
- apiref
api_name:
- TS_LF_SYNC
- TS_LF_READ
- TS_LF_READWRITE
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6240511fd95e91a7f22477f631178dfab528f1e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685844"
---
# <a name="ts_lf_-constants"></a><span data-ttu-id="2e0fd-103">\_Constantes de LF de TS \_ \*</span><span class="sxs-lookup"><span data-stu-id="2e0fd-103">TS\_LF\_\* Constants</span></span>

<span data-ttu-id="2e0fd-104">Las \_ constantes LF \_ \* de TS especifican el tipo de bloqueo del documento.</span><span class="sxs-lookup"><span data-stu-id="2e0fd-104">The TS\_LF\_\* constants specify the type of document lock.</span></span>



| <span data-ttu-id="2e0fd-105">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="2e0fd-105">Constant/value</span></span>                                                                                                                                                                                                                    | <span data-ttu-id="2e0fd-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="2e0fd-106">Description</span></span>                                                                               |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| <span id="TS_LF_SYNC"></span><span id="ts_lf_sync"></span><dl> <span data-ttu-id="2e0fd-107"><dt>**TS \_ \_Sincronización de LF**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="2e0fd-107"><dt>**TS\_LF\_SYNC**</dt> <dt>( 0x1 )</dt></span></span> </dl>                | <span data-ttu-id="2e0fd-108">El documento tiene un bloqueo sincrónico si esta marca se combina con otras marcas.</span><span class="sxs-lookup"><span data-stu-id="2e0fd-108">The document has a synchronous-lock if this flag is combined with other flags.</span></span><br/> |
| <span id="TS_LF_READ"></span><span id="ts_lf_read"></span><dl> <span data-ttu-id="2e0fd-109"><dt>**TS \_ \_Lectura de LF**</dt> <dt>(0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="2e0fd-109"><dt>**TS\_LF\_READ**</dt> <dt>( 0x2 )</dt></span></span> </dl>                | <span data-ttu-id="2e0fd-110">El documento tiene un bloqueo de solo lectura y no se puede modificar.</span><span class="sxs-lookup"><span data-stu-id="2e0fd-110">The document has a read-only lock and cannot be modified.</span></span><br/>                      |
| <span id="TS_LF_READWRITE"></span><span id="ts_lf_readwrite"></span><dl> <span data-ttu-id="2e0fd-111"><dt>**TS \_ LF \_ ReadWrite**</dt> <dt>(0x6)</dt></span><span class="sxs-lookup"><span data-stu-id="2e0fd-111"><dt>**TS\_LF\_READWRITE**</dt> <dt>( 0x6 )</dt></span></span> </dl> | <span data-ttu-id="2e0fd-112">El documento tiene un bloqueo de lectura/escritura y se puede modificar.</span><span class="sxs-lookup"><span data-stu-id="2e0fd-112">The document has a read/write lock and can be modified.</span></span><br/>                        |



## <a name="requirements"></a><span data-ttu-id="2e0fd-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e0fd-113">Requirements</span></span>



| <span data-ttu-id="2e0fd-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e0fd-114">Requirement</span></span> | <span data-ttu-id="2e0fd-115">Value</span><span class="sxs-lookup"><span data-stu-id="2e0fd-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e0fd-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e0fd-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2e0fd-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="2e0fd-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="2e0fd-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e0fd-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2e0fd-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2e0fd-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2e0fd-120">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="2e0fd-120">Redistributable</span></span><br/>          | <span data-ttu-id="2e0fd-121">TSF 1,0 en Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="2e0fd-121">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="2e0fd-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2e0fd-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e0fd-123"><dt>Textstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e0fd-123"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="2e0fd-124">IDL</span><span class="sxs-lookup"><span data-stu-id="2e0fd-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2e0fd-125"><dt>Textstor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2e0fd-125"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e0fd-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="2e0fd-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e0fd-127">Bloqueos de documento</span><span class="sxs-lookup"><span data-stu-id="2e0fd-127">Document Locks</span></span>](document-locks.md)
</dt> <dt>

[<span data-ttu-id="2e0fd-128">ITextStoreACP:: RequestLock</span><span class="sxs-lookup"><span data-stu-id="2e0fd-128">ITextStoreACP::RequestLock</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestlock)
</dt> <dt>

[<span data-ttu-id="2e0fd-129">ITextStoreACPSink::OnLockGranted</span><span class="sxs-lookup"><span data-stu-id="2e0fd-129">ITextStoreACPSink::OnLockGranted</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-onlockgranted)
</dt> <dt>

[<span data-ttu-id="2e0fd-130">ITextStoreAnchor::RequestLock</span><span class="sxs-lookup"><span data-stu-id="2e0fd-130">ITextStoreAnchor::RequestLock</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestlock)
</dt> <dt>

[<span data-ttu-id="2e0fd-131">ITextStoreAnchorSink::OnLockGranted</span><span class="sxs-lookup"><span data-stu-id="2e0fd-131">ITextStoreAnchorSink::OnLockGranted</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-onlockgranted)
</dt> </dl>

 

 





