---
title: TfEditCookie (msctf. h)
description: El tipo de datos TfEditCookie identifica una sesión de edición que tiene un bloqueo.
ms.assetid: 1de17286-5d56-4302-a144-5fe6ca7d5557
keywords:
- TfEditCookie
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69281bc38b5df6c22dd5306877aecdb8025af84a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078824"
---
# <a name="tfeditcookie"></a><span data-ttu-id="07f2d-104">TfEditCookie</span><span class="sxs-lookup"><span data-stu-id="07f2d-104">TfEditCookie</span></span>

<span data-ttu-id="07f2d-105">El tipo de datos **TfEditCookie** identifica una sesión de edición que tiene un bloqueo.</span><span class="sxs-lookup"><span data-stu-id="07f2d-105">The **TfEditCookie** data type identifies an edit session that has a lock.</span></span>


```C++
typedef DWORD TfEditCookie;
```



## <a name="remarks"></a><span data-ttu-id="07f2d-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="07f2d-106">Remarks</span></span>

<span data-ttu-id="07f2d-107">El tipo de datos **TfEditCookie** es proporcionado por el administrador de TSF y lo usa un cliente (servicio de aplicación o texto) para identificar una sesión de edición con un bloqueo de solo lectura o de lectura y escritura en varios métodos.</span><span class="sxs-lookup"><span data-stu-id="07f2d-107">The **TfEditCookie** data type is supplied by the TSF manager and is used by a client (application or text service) to identify an edit session with a read-only or read/write lock in various methods.</span></span>

<span data-ttu-id="07f2d-108">Un valor **TfEditCookie** se obtiene de una de las siguientes maneras.</span><span class="sxs-lookup"><span data-stu-id="07f2d-108">A **TfEditCookie** value is obtained in one of the following ways.</span></span>

-   <span data-ttu-id="07f2d-109">El cliente llama a [ITfDocumentMgr:: CreateContext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext).</span><span class="sxs-lookup"><span data-stu-id="07f2d-109">The client calls [ITfDocumentMgr::CreateContext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext).</span></span>
-   <span data-ttu-id="07f2d-110">El administrador de TSF llama al método ITfEditSession de cliente [::D oeditsession](/windows/desktop/api/Msctf/nf-msctf-itfeditsession-doeditsession) .</span><span class="sxs-lookup"><span data-stu-id="07f2d-110">The TSF manager calls the client [ITfEditSession::DoEditSession](/windows/desktop/api/Msctf/nf-msctf-itfeditsession-doeditsession) method.</span></span>
-   <span data-ttu-id="07f2d-111">El administrador de TSF llama al método [ITfCompositionSink:: OnCompositionTerminated](/windows/desktop/api/Msctf/nf-msctf-itfcompositionsink-oncompositionterminated) del cliente.</span><span class="sxs-lookup"><span data-stu-id="07f2d-111">The TSF manager calls the client [ITfCompositionSink::OnCompositionTerminated](/windows/desktop/api/Msctf/nf-msctf-itfcompositionsink-oncompositionterminated) method.</span></span>
-   <span data-ttu-id="07f2d-112">El administrador de TSF llama al método [ITfCleanupContextSink:: OnCleanupContext](/windows/desktop/api/Msctf/nf-msctf-itfcleanupcontextsink-oncleanupcontext) del cliente.</span><span class="sxs-lookup"><span data-stu-id="07f2d-112">The TSF manager calls the client [ITfCleanupContextSink::OnCleanupContext](/windows/desktop/api/Msctf/nf-msctf-itfcleanupcontextsink-oncleanupcontext) method.</span></span>
-   <span data-ttu-id="07f2d-113">El administrador de TSF llama al método [ITfTextEditSink:: OnEndEdit](/windows/desktop/api/Msctf/nf-msctf-itftexteditsink-onendedit) del cliente.</span><span class="sxs-lookup"><span data-stu-id="07f2d-113">The TSF manager calls the client [ITfTextEditSink::OnEndEdit](/windows/desktop/api/Msctf/nf-msctf-itftexteditsink-onendedit) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="07f2d-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07f2d-114">Requirements</span></span>



| <span data-ttu-id="07f2d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="07f2d-115">Requirement</span></span> | <span data-ttu-id="07f2d-116">Value</span><span class="sxs-lookup"><span data-stu-id="07f2d-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="07f2d-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="07f2d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="07f2d-118">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]</span><span class="sxs-lookup"><span data-stu-id="07f2d-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                    |
| <span data-ttu-id="07f2d-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="07f2d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="07f2d-120">Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]</span><span class="sxs-lookup"><span data-stu-id="07f2d-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="07f2d-121">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="07f2d-121">Redistributable</span></span><br/>          | <span data-ttu-id="07f2d-122">TSF 1,0 en Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="07f2d-122">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="07f2d-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="07f2d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="07f2d-124"><dt>Msctf. h</dt></span><span class="sxs-lookup"><span data-stu-id="07f2d-124"><dt>Msctf.h</dt></span></span> </dl>   |
| <span data-ttu-id="07f2d-125">IDL</span><span class="sxs-lookup"><span data-stu-id="07f2d-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="07f2d-126"><dt>Msctf. idl</dt></span><span class="sxs-lookup"><span data-stu-id="07f2d-126"><dt>Msctf.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07f2d-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="07f2d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07f2d-128">**ITfCleanupContextSink::OnCleanupContext**</span><span class="sxs-lookup"><span data-stu-id="07f2d-128">**ITfCleanupContextSink::OnCleanupContext**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcleanupcontextsink-oncleanupcontext)
</dt> <dt>

[<span data-ttu-id="07f2d-129">**ITfCompositionSink::OnCompositionTerminated**</span><span class="sxs-lookup"><span data-stu-id="07f2d-129">**ITfCompositionSink::OnCompositionTerminated**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcompositionsink-oncompositionterminated)
</dt> <dt>

[<span data-ttu-id="07f2d-130">**ITfDocumentMgr:: CreateContext**</span><span class="sxs-lookup"><span data-stu-id="07f2d-130">**ITfDocumentMgr::CreateContext**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext)
</dt> <dt>

[<span data-ttu-id="07f2d-131">**ITfEditSession::D oEditSession**</span><span class="sxs-lookup"><span data-stu-id="07f2d-131">**ITfEditSession::DoEditSession**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfeditsession-doeditsession)
</dt> <dt>

[<span data-ttu-id="07f2d-132">**ITfTextEditSink::OnEndEdit**</span><span class="sxs-lookup"><span data-stu-id="07f2d-132">**ITfTextEditSink::OnEndEdit**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itftexteditsink-onendedit)
</dt> </dl>

 

 





