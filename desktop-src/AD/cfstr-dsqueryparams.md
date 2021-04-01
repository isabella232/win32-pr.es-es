---
title: CFSTR_DSQUERYPARAMS (DSQuery. h)
description: El \_ formato del portapapeles de CFSTR DSQUERYPARAMS proporciona un identificador de memoria global (hglobal) que contiene una estructura DSQUERYPARAMS.
ms.assetid: bb8aea98-8309-42bf-993d-fa408bb4deb2
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- CFSTR_DSQUERYPARAMS
api_location:
- DSQuery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a330d228778f34118d232b2004e7294ab493ed77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996230"
---
# <a name="cfstr_dsqueryparams"></a><span data-ttu-id="8ac26-103">CFSTR \_ DSQUERYPARAMS</span><span class="sxs-lookup"><span data-stu-id="8ac26-103">CFSTR\_DSQUERYPARAMS</span></span>

<dl> <dt>

<span data-ttu-id="8ac26-104"><span id="CFSTR_DSQUERYPARAMS"></span><span id="cfstr_dsqueryparams"></span>**CFSTR \_ DSQUERYPARAMS**</span><span class="sxs-lookup"><span data-stu-id="8ac26-104"><span id="CFSTR_DSQUERYPARAMS"></span><span id="cfstr_dsqueryparams"></span>**CFSTR\_DSQUERYPARAMS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ac26-105">"DsQueryParameters"</span><span class="sxs-lookup"><span data-stu-id="8ac26-105">"DsQueryParameters"</span></span>
</dt> <dt>



<span data-ttu-id="8ac26-106">El formato del portapapeles de **CFSTR \_ DSQUERYPARAMS** es compatible con [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) proporcionado por el método [**ICommonQuery:: OpenQueryWindow**](/windows/win32/api/cmnquery/nf-cmnquery-icommonquery-openquerywindow) .</span><span class="sxs-lookup"><span data-stu-id="8ac26-106">The **CFSTR\_DSQUERYPARAMS** clipboard format is supported by the [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) provided by the [**ICommonQuery::OpenQueryWindow**](/windows/win32/api/cmnquery/nf-cmnquery-icommonquery-openquerywindow) method.</span></span> <span data-ttu-id="8ac26-107">El formato del portapapeles de **CFSTR \_ DSQUERYPARAMS** proporciona un identificador de memoria global (**HGLOBAL**) que contiene una estructura [**DSQUERYPARAMS**](/windows/desktop/api/Dsquery/ns-dsquery-dsqueryparams) .</span><span class="sxs-lookup"><span data-stu-id="8ac26-107">The **CFSTR\_DSQUERYPARAMS** clipboard format provides a global memory handle (**HGLOBAL**) that contains a [**DSQUERYPARAMS**](/windows/desktop/api/Dsquery/ns-dsquery-dsqueryparams) structure.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8ac26-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ac26-108">Requirements</span></span>



| <span data-ttu-id="8ac26-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ac26-109">Requirement</span></span> | <span data-ttu-id="8ac26-110">Value</span><span class="sxs-lookup"><span data-stu-id="8ac26-110">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8ac26-111">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8ac26-111">Minimum supported client</span></span><br/> | <span data-ttu-id="8ac26-112">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8ac26-112">Windows Vista</span></span><br/>                                                             |
| <span data-ttu-id="8ac26-113">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8ac26-113">Minimum supported server</span></span><br/> | <span data-ttu-id="8ac26-114">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8ac26-114">Windows Server 2008</span></span><br/>                                                       |
| <span data-ttu-id="8ac26-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8ac26-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ac26-116"><dt>DSQuery. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ac26-116"><dt>DSQuery.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ac26-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="8ac26-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ac26-118">**IDataObject**</span><span class="sxs-lookup"><span data-stu-id="8ac26-118">**IDataObject**</span></span>](/windows/win32/api/objidl/nn-objidl-idataobject)
</dt> <dt>

[<span data-ttu-id="8ac26-119">**ICommonQuery::OpenQueryWindow**</span><span class="sxs-lookup"><span data-stu-id="8ac26-119">**ICommonQuery::OpenQueryWindow**</span></span>](/windows/win32/api/cmnquery/nf-cmnquery-icommonquery-openquerywindow)
</dt> <dt>

[<span data-ttu-id="8ac26-120">**DSQUERYPARAMS**</span><span class="sxs-lookup"><span data-stu-id="8ac26-120">**DSQUERYPARAMS**</span></span>](/windows/desktop/api/Dsquery/ns-dsquery-dsqueryparams)
</dt> </dl>

 

