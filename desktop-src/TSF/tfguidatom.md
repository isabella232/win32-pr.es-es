---
title: TfGuidAtom (msctf. h)
description: El tipo de datos TfGuidAtom identifica un GUID en TSF. Un TfGuidAtom se obtiene llamando a ITfCategoryMgr RegisterGUID.
ms.assetid: 91696612-1829-4052-81d1-eddc23278d35
keywords:
- TfGuidAtom
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c05d3c9a3bc7d725bf2df38069d7bc6112dad08b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149867"
---
# <a name="tfguidatom"></a><span data-ttu-id="ea03d-105">TfGuidAtom</span><span class="sxs-lookup"><span data-stu-id="ea03d-105">TfGuidAtom</span></span>

<span data-ttu-id="ea03d-106">El tipo de datos **TfGuidAtom** identifica un **GUID** en TSF.</span><span class="sxs-lookup"><span data-stu-id="ea03d-106">The **TfGuidAtom** data type identifies a **GUID** within TSF.</span></span> <span data-ttu-id="ea03d-107">Un **TfGuidAtom** se obtiene llamando a [**ITfCategoryMgr:: RegisterGUID**](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid).</span><span class="sxs-lookup"><span data-stu-id="ea03d-107">A **TfGuidAtom** is obtained by calling [**ITfCategoryMgr::RegisterGUID**](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid).</span></span>


```C++
typedef DWORD TfGuidAtom;
```



## <a name="remarks"></a><span data-ttu-id="ea03d-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ea03d-108">Remarks</span></span>

<span data-ttu-id="ea03d-109">Un valor **TfGuidAtom** solo es válido dentro del proceso desde el que se llama a **ITfCategoryMgr:: RegisterGUID** .</span><span class="sxs-lookup"><span data-stu-id="ea03d-109">A **TfGuidAtom** value is only valid within the process that **ITfCategoryMgr::RegisterGUID** is called from.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea03d-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea03d-110">Requirements</span></span>



| <span data-ttu-id="ea03d-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea03d-111">Requirement</span></span> | <span data-ttu-id="ea03d-112">Value</span><span class="sxs-lookup"><span data-stu-id="ea03d-112">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ea03d-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ea03d-113">Minimum supported client</span></span><br/> | <span data-ttu-id="ea03d-114">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ea03d-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="ea03d-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ea03d-115">Minimum supported server</span></span><br/> | <span data-ttu-id="ea03d-116">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ea03d-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ea03d-117">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="ea03d-117">Redistributable</span></span><br/>          | <span data-ttu-id="ea03d-118">TSF 1,0 en Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ea03d-118">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="ea03d-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ea03d-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea03d-120"><dt>Msctf. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea03d-120"><dt>Msctf.h</dt></span></span> </dl>   |
| <span data-ttu-id="ea03d-121">IDL</span><span class="sxs-lookup"><span data-stu-id="ea03d-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ea03d-122"><dt>Msctf. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ea03d-122"><dt>Msctf.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea03d-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="ea03d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea03d-124">**ITfCategoryMgr:: GetGUID**</span><span class="sxs-lookup"><span data-stu-id="ea03d-124">**ITfCategoryMgr::GetGUID**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid)
</dt> <dt>

[<span data-ttu-id="ea03d-125">**ITfCategoryMgr::IsEqualTfGuidAtom**</span><span class="sxs-lookup"><span data-stu-id="ea03d-125">**ITfCategoryMgr::IsEqualTfGuidAtom**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-isequaltfguidatom)
</dt> <dt>

[<span data-ttu-id="ea03d-126">**ITfCategoryMgr::RegisterGUID**</span><span class="sxs-lookup"><span data-stu-id="ea03d-126">**ITfCategoryMgr::RegisterGUID**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid)
</dt> </dl>

 

 





