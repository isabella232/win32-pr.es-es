---
title: Método ResourceLocator. ClearOptions (WSManDisp. h)
description: Quita todas las opciones del objeto ResourceLocator.
ms.assetid: 1b4d7f15-c56f-4b0d-9614-8376012abca7
ms.tgt_platform: multiple
keywords:
- Método ClearOptions Administración remota de Windows
- Método ClearOptions Administración remota de Windows, objeto ResourceLocator
- Administración remota de Windows de objeto ResourceLocator, método ClearOptions
topic_type:
- apiref
api_name:
- ResourceLocator.ClearOptions
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fda4be766b65756a9bcf8de02a4417fd15a3e7f2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905066"
---
# <a name="resourcelocatorclearoptions-method"></a><span data-ttu-id="9f1d3-106">ResourceLocator. ClearOptions, método</span><span class="sxs-lookup"><span data-stu-id="9f1d3-106">ResourceLocator.ClearOptions method</span></span>

<span data-ttu-id="9f1d3-107">Quita todas [*las opciones*](windows-remote-management-glossary.md) del objeto [**ResourceLocator**](resourcelocator.md) .</span><span class="sxs-lookup"><span data-stu-id="9f1d3-107">Removes any [*options*](windows-remote-management-glossary.md) from the [**ResourceLocator**](resourcelocator.md) object.</span></span> <span data-ttu-id="9f1d3-108">Puede proporcionar un objeto [**ResourceLocator**](resourcelocator.md) en lugar de especificar un URI de recurso en operaciones de objetos de [**sesión**](session.md) como [**Session. Get**](session-get.md), [**Session. put**](session-put.md)o [**Session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="9f1d3-108">You can provide a [**ResourceLocator**](resourcelocator.md) object instead of specifying a resource URI in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9f1d3-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9f1d3-109">Syntax</span></span>


```VB
ResourceLocator.ClearOptions()
```



## <a name="parameters"></a><span data-ttu-id="9f1d3-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9f1d3-110">Parameters</span></span>

<span data-ttu-id="9f1d3-111">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="9f1d3-111">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f1d3-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9f1d3-112">Remarks</span></span>

<span data-ttu-id="9f1d3-113">**IWSManResourceLocator:: ClearOptions** es el método de C++ correspondiente.</span><span class="sxs-lookup"><span data-stu-id="9f1d3-113">**IWSManResourceLocator::ClearOptions** is the corresponding C++ method.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f1d3-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f1d3-114">Requirements</span></span>



| <span data-ttu-id="9f1d3-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f1d3-115">Requirement</span></span> | <span data-ttu-id="9f1d3-116">Value</span><span class="sxs-lookup"><span data-stu-id="9f1d3-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f1d3-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9f1d3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9f1d3-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9f1d3-118">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="9f1d3-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9f1d3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9f1d3-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9f1d3-120">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="9f1d3-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9f1d3-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f1d3-122"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f1d3-122"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="9f1d3-123">IDL</span><span class="sxs-lookup"><span data-stu-id="9f1d3-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9f1d3-124"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9f1d3-124"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="9f1d3-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9f1d3-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="9f1d3-126"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9f1d3-126"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9f1d3-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9f1d3-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f1d3-128"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f1d3-128"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9f1d3-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="9f1d3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f1d3-130">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="9f1d3-130">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

 





