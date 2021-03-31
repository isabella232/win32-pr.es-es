---
title: Método ResourceLocator. ClearSelectors (WSManDisp. h)
description: Quita todos los selectores de un objeto ResourceLocator.
ms.assetid: 759880e6-5026-45de-b7e1-a4f5a16c32a0
ms.tgt_platform: multiple
keywords:
- Método ClearSelectors Administración remota de Windows
- Método ClearSelectors Administración remota de Windows, objeto ResourceLocator
- Administración remota de Windows de objeto ResourceLocator, método ClearSelectors
topic_type:
- apiref
api_name:
- ResourceLocator.ClearSelectors
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd5dbf1322a5e0c36a1383581e2822fbd00a00e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150935"
---
# <a name="resourcelocatorclearselectors-method"></a><span data-ttu-id="c1da8-106">ResourceLocator. ClearSelectors, método</span><span class="sxs-lookup"><span data-stu-id="c1da8-106">ResourceLocator.ClearSelectors method</span></span>

<span data-ttu-id="c1da8-107">Quita todos los [*selectores*](windows-remote-management-glossary.md) de un objeto [**ResourceLocator**](resourcelocator.md) .</span><span class="sxs-lookup"><span data-stu-id="c1da8-107">Removes all of the [*selectors*](windows-remote-management-glossary.md) from a [**ResourceLocator**](resourcelocator.md) object.</span></span> <span data-ttu-id="c1da8-108">Puede proporcionar un objeto [**ResourceLocator**](resourcelocator.md) en lugar de especificar un URI de recurso en operaciones de objetos de [**sesión**](session.md) como [**Session. Get**](session-get.md), [**Session. put**](session-put.md)o [**Session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="c1da8-108">You can provide a [**ResourceLocator**](resourcelocator.md) object instead of specifying a resource URI in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c1da8-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c1da8-109">Syntax</span></span>


```VB
ResourceLocator.ClearSelectors()
```



## <a name="parameters"></a><span data-ttu-id="c1da8-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c1da8-110">Parameters</span></span>

<span data-ttu-id="c1da8-111">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="c1da8-111">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1da8-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c1da8-112">Remarks</span></span>

<span data-ttu-id="c1da8-113">**IWSManResourceLocator:: ClearSelectors** es el método de C++ correspondiente.</span><span class="sxs-lookup"><span data-stu-id="c1da8-113">**IWSManResourceLocator::ClearSelectors** is the corresponding C++ method.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1da8-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1da8-114">Requirements</span></span>



| <span data-ttu-id="c1da8-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1da8-115">Requirement</span></span> | <span data-ttu-id="c1da8-116">Value</span><span class="sxs-lookup"><span data-stu-id="c1da8-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1da8-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c1da8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c1da8-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c1da8-118">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="c1da8-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c1da8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c1da8-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c1da8-120">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="c1da8-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c1da8-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1da8-122"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1da8-122"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c1da8-123">IDL</span><span class="sxs-lookup"><span data-stu-id="c1da8-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c1da8-124"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c1da8-124"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="c1da8-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c1da8-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="c1da8-126"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c1da8-126"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c1da8-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c1da8-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1da8-128"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1da8-128"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c1da8-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="c1da8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1da8-130">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="c1da8-130">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

 





