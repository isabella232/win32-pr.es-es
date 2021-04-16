---
title: Constantes de TF_ES_ (msctf. h)
description: Las siguientes son constantes que usa el método ITfContext RequestEditSession.
ms.assetid: 5498329f-3302-4f66-bdec-cab7db0cdc0e
topic_type:
- apiref
api_name:
- TF_ES_ASYNCDONTCARE
- TF_ES_SYNC
- TF_ES_READ
- TF_ES_READWRITE
- TF_ES_ASYNC
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa8ed96adc1d6f6d66671e91f7a70bce856663e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686132"
---
# <a name="tf_es_-constants"></a><span data-ttu-id="d40fd-103">Constantes de TF \_ es \_ \*</span><span class="sxs-lookup"><span data-stu-id="d40fd-103">TF\_ES\_\* Constants</span></span>

<span data-ttu-id="d40fd-104">Las siguientes son constantes que usa el método [ITfContext:: RequestEditSession](/windows/desktop/api/Msctf/nf-msctf-itfcontext-requesteditsession) .</span><span class="sxs-lookup"><span data-stu-id="d40fd-104">The following are constants used by the [ITfContext::RequestEditSession](/windows/desktop/api/Msctf/nf-msctf-itfcontext-requesteditsession) method.</span></span>



| <span data-ttu-id="d40fd-105">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="d40fd-105">Constant/value</span></span>                                                                                                                                                                                                                              | <span data-ttu-id="d40fd-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="d40fd-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                             |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_ES_ASYNCDONTCARE"></span><span id="tf_es_asyncdontcare"></span><dl> <span data-ttu-id="d40fd-107"><dt>**TF \_ ES \_ ASYNCDONTCARE**</dt> <dt>(0)</dt></span><span class="sxs-lookup"><span data-stu-id="d40fd-107"><dt>**TF\_ES\_ASYNCDONTCARE**</dt> <dt>( 0 )</dt></span></span> </dl> | <span data-ttu-id="d40fd-108">La sesión de edición puede realizarse de forma sincrónica o asincrónica, a discreción del administrador.</span><span class="sxs-lookup"><span data-stu-id="d40fd-108">The edit session can occur synchronously or asynchronously, at the discretion of the manager.</span></span> <span data-ttu-id="d40fd-109">El administrador intentará programar una sesión de edición sincrónica para mejorar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="d40fd-109">The manager will attempt to schedule a synchronous edit session for improved performance.</span></span> <span data-ttu-id="d40fd-110">Este valor no se puede combinar con los \_ valores de sincronización de TF es \_ Async o TF \_ es \_ .</span><span class="sxs-lookup"><span data-stu-id="d40fd-110">This value cannot be combined with the TF\_ES\_ASYNC or TF\_ES\_SYNC values.</span></span><br/>                                                                         |
| <span id="TF_ES_SYNC"></span><span id="tf_es_sync"></span><dl> <span data-ttu-id="d40fd-111"><dt>**TF \_ \_Sincronización es**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="d40fd-111"><dt>**TF\_ES\_SYNC**</dt> <dt>( 0x1 )</dt></span></span> </dl>                          | <span data-ttu-id="d40fd-112">La sesión de edición debe ser sincrónica o se producirá un error en la solicitud (con TF \_ E \_ Synchronous).</span><span class="sxs-lookup"><span data-stu-id="d40fd-112">The edit session must be synchronous or the request will fail (with TF\_E\_SYNCHRONOUS).</span></span> <span data-ttu-id="d40fd-113">Esta marca solo se debe usar en situaciones documentadas (por ejemplo, el control de pulsaciones de teclas), donde se puede esperar que se realice correctamente.</span><span class="sxs-lookup"><span data-stu-id="d40fd-113">This flag should only be used in documented situations (such as keystroke handling) where it can be expected to succeed.</span></span> <span data-ttu-id="d40fd-114">De lo contrario, es probable que se produzca un error en la llamada.</span><span class="sxs-lookup"><span data-stu-id="d40fd-114">Otherwise the call will likely fail.</span></span> <span data-ttu-id="d40fd-115">Este valor no se puede combinar con los \_ valores de TF es \_ ASYNCDONTCARE o TF \_ es \_ Async.</span><span class="sxs-lookup"><span data-stu-id="d40fd-115">This value cannot be combined with the TF\_ES\_ASYNCDONTCARE or TF\_ES\_ASYNC values.</span></span><br/> |
| <span id="TF_ES_READ"></span><span id="tf_es_read"></span><dl> <span data-ttu-id="d40fd-116"><dt>**TF \_ ES \_ leída**</dt> <dt>(0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="d40fd-116"><dt>**TF\_ES\_READ**</dt> <dt>( 0x2 )</dt></span></span> </dl>                          | <span data-ttu-id="d40fd-117">Solicita acceso de solo lectura al contexto.</span><span class="sxs-lookup"><span data-stu-id="d40fd-117">Requests read-only access to the context.</span></span><br/>                                                                                                                                                                                                                                                                                                    |
| <span id="TF_ES_READWRITE"></span><span id="tf_es_readwrite"></span><dl> <span data-ttu-id="d40fd-118"><dt>**TF \_ ES \_ ReadWrite**</dt> <dt>(0x6)</dt></span><span class="sxs-lookup"><span data-stu-id="d40fd-118"><dt>**TF\_ES\_READWRITE**</dt> <dt>( 0x6 )</dt></span></span> </dl>           | <span data-ttu-id="d40fd-119">Solicita acceso de lectura/escritura al contexto.</span><span class="sxs-lookup"><span data-stu-id="d40fd-119">Requests read/write access to the context.</span></span><br/>                                                                                                                                                                                                                                                                                                   |
| <span id="TF_ES_ASYNC"></span><span id="tf_es_async"></span><dl> <span data-ttu-id="d40fd-120"><dt>**TF \_ S \_ Async**</dt> <dt>(0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="d40fd-120"><dt>**TF\_ES\_ASYNC**</dt> <dt>( 0x8 )</dt></span></span> </dl>                       | <span data-ttu-id="d40fd-121">La sesión de edición debe ser asincrónica o se producirá un error en la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d40fd-121">The edit session must be asynchronous or the request will fail.</span></span> <span data-ttu-id="d40fd-122">Este valor no se puede combinar con los \_ valores de sincronización TF es \_ ASYNCDONTCARE o TF \_ es \_ .</span><span class="sxs-lookup"><span data-stu-id="d40fd-122">This value cannot be combined with the TF\_ES\_ASYNCDONTCARE or TF\_ES\_SYNC values.</span></span><br/>                                                                                                                                                                                         |



## <a name="requirements"></a><span data-ttu-id="d40fd-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d40fd-123">Requirements</span></span>



| <span data-ttu-id="d40fd-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="d40fd-124">Requirement</span></span> | <span data-ttu-id="d40fd-125">Value</span><span class="sxs-lookup"><span data-stu-id="d40fd-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d40fd-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d40fd-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d40fd-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d40fd-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="d40fd-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d40fd-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d40fd-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d40fd-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d40fd-130">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="d40fd-130">Redistributable</span></span><br/>          | <span data-ttu-id="d40fd-131">TSF 1,0 en Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d40fd-131">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="d40fd-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d40fd-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="d40fd-133"><dt>Msctf. h</dt></span><span class="sxs-lookup"><span data-stu-id="d40fd-133"><dt>Msctf.h</dt></span></span> </dl>   |
| <span data-ttu-id="d40fd-134">IDL</span><span class="sxs-lookup"><span data-stu-id="d40fd-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d40fd-135"><dt>Msctf. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d40fd-135"><dt>Msctf.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d40fd-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="d40fd-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d40fd-137">ITfContext::RequestEditSession</span><span class="sxs-lookup"><span data-stu-id="d40fd-137">ITfContext::RequestEditSession</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontext-requesteditsession)
</dt> </dl>

 

 





