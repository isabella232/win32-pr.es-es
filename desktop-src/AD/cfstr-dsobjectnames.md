---
title: CFSTR_DSOBJECTNAMES (DSClient. h)
description: El \_ formato del portapapeles de CFSTR DSOBJECTNAMES proporciona un identificador de memoria global (hglobal) que contiene la estructura DSOBJECTNAMES.
ms.assetid: b28428fa-1504-4dcc-9b2b-32ca1ae30ec5
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- CFSTR_DSOBJECTNAMES
api_location:
- DSClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 816f99f1b50f97ac362706cc46e4dbe4edf5f486
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150142"
---
# <a name="cfstr_dsobjectnames"></a><span data-ttu-id="25188-103">CFSTR \_ DSOBJECTNAMES</span><span class="sxs-lookup"><span data-stu-id="25188-103">CFSTR\_DSOBJECTNAMES</span></span>

<dl> <dt>

<span data-ttu-id="25188-104"><span id="CFSTR_DSOBJECTNAMES"></span><span id="cfstr_dsobjectnames"></span>**CFSTR \_ DSOBJECTNAMES**</span><span class="sxs-lookup"><span data-stu-id="25188-104"><span id="CFSTR_DSOBJECTNAMES"></span><span id="cfstr_dsobjectnames"></span>**CFSTR\_DSOBJECTNAMES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25188-105">"DsObjectNames"</span><span class="sxs-lookup"><span data-stu-id="25188-105">"DsObjectNames"</span></span>
</dt> <dt>



<span data-ttu-id="25188-106">El formato del portapapeles de **CFSTR \_ DSOBJECTNAMES** es compatible con [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) proporcionado por el método [**ICommonQuery:: OpenQueryWindow**](/windows/win32/api/cmnquery/nf-cmnquery-icommonquery-openquerywindow) .</span><span class="sxs-lookup"><span data-stu-id="25188-106">The **CFSTR\_DSOBJECTNAMES** clipboard format is supported by the [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) provided by the [**ICommonQuery::OpenQueryWindow**](/windows/win32/api/cmnquery/nf-cmnquery-icommonquery-openquerywindow) method.</span></span> <span data-ttu-id="25188-107">El formato del portapapeles de **CFSTR \_ DSOBJECTNAMES** proporciona un identificador de memoria global (**HGLOBAL**) que contiene la estructura [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) .</span><span class="sxs-lookup"><span data-stu-id="25188-107">The **CFSTR\_DSOBJECTNAMES** clipboard format provides a global memory handle (**HGLOBAL**) that contains [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) structure.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="25188-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25188-108">Requirements</span></span>



| <span data-ttu-id="25188-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="25188-109">Requirement</span></span> | <span data-ttu-id="25188-110">Value</span><span class="sxs-lookup"><span data-stu-id="25188-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="25188-111">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25188-111">Minimum supported client</span></span><br/> | <span data-ttu-id="25188-112">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="25188-112">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="25188-113">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25188-113">Minimum supported server</span></span><br/> | <span data-ttu-id="25188-114">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="25188-114">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="25188-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="25188-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="25188-116"><dt>DSClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="25188-116"><dt>DSClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25188-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="25188-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25188-118">**IDataObject**</span><span class="sxs-lookup"><span data-stu-id="25188-118">**IDataObject**</span></span>](/windows/win32/api/objidl/nn-objidl-idataobject)
</dt> <dt>

[<span data-ttu-id="25188-119">**ICommonQuery::OpenQueryWindow**</span><span class="sxs-lookup"><span data-stu-id="25188-119">**ICommonQuery::OpenQueryWindow**</span></span>](/windows/win32/api/cmnquery/nf-cmnquery-icommonquery-openquerywindow)
</dt> <dt>

[<span data-ttu-id="25188-120">**DSOBJECTNAMES**</span><span class="sxs-lookup"><span data-stu-id="25188-120">**DSOBJECTNAMES**</span></span>](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames)
</dt> </dl>

 

