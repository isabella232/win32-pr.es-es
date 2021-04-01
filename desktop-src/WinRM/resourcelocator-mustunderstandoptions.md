---
title: Propiedad ResourceLocator. MustUnderstandOptions (WSManDisp. h)
description: Obtiene o establece el valor de MustUnderstandOptions para el objeto ResourceLocator.
ms.assetid: d366696c-9128-4cbd-98d0-6c2d16c75d59
ms.tgt_platform: multiple
keywords:
- Administración remota de Windows de la propiedad MustUnderstandOptions
- Administración remota de Windows de la propiedad MustUnderstandOptions, objeto ResourceLocator
- Administración remota de Windows de objeto ResourceLocator, propiedad MustUnderstandOptions
topic_type:
- apiref
api_name:
- ResourceLocator.MustUnderstandOptions
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2945efd1a224c333f45956a29df779efc98e944f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996975"
---
# <a name="resourcelocatormustunderstandoptions-property"></a><span data-ttu-id="fd14b-106">Propiedad ResourceLocator. MustUnderstandOptions</span><span class="sxs-lookup"><span data-stu-id="fd14b-106">ResourceLocator.MustUnderstandOptions property</span></span>

<span data-ttu-id="fd14b-107">Obtiene o establece el valor de **MustUnderstandOptions** para el objeto [**ResourceLocator**](resourcelocator.md) .</span><span class="sxs-lookup"><span data-stu-id="fd14b-107">Gets or sets the **MustUnderstandOptions** value for the [**ResourceLocator**](resourcelocator.md) object.</span></span> <span data-ttu-id="fd14b-108">Puede proporcionar un objeto [**ResourceLocator**](resourcelocator.md) en lugar de especificar un URI de recurso en operaciones de objetos de [**sesión**](session.md) como [**Session. Get**](session-get.md), [**Session. put**](session-put.md)o [**Session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="fd14b-108">You can provide a [**ResourceLocator**](resourcelocator.md) object instead of specifying a resource URI in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span>

<span data-ttu-id="fd14b-109">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="fd14b-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd14b-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fd14b-110">Syntax</span></span>


```VB
ResourceLocator.MustUnderstandOptions As boolean
```



## <a name="property-value"></a><span data-ttu-id="fd14b-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="fd14b-111">Property value</span></span>

<span data-ttu-id="fd14b-112">Indica que, cuando es **true**, el servicio que implementa el [protocolo WS-Management](ws-management-protocol.md) debe devolver un error si no es capaz de procesar la opción.</span><span class="sxs-lookup"><span data-stu-id="fd14b-112">Indicates, when **True**, that the service which implements the [WS-Management Protocol](ws-management-protocol.md) must return an error if it is not capable of processing the option.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd14b-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fd14b-113">Remarks</span></span>

<span data-ttu-id="fd14b-114">**IWSManResourceLocator:: MustUnderstandOptions** es la propiedad de C++ correspondiente.</span><span class="sxs-lookup"><span data-stu-id="fd14b-114">**IWSManResourceLocator::MustUnderstandOptions** is the corresponding C++ property.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd14b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd14b-115">Requirements</span></span>



| <span data-ttu-id="fd14b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd14b-116">Requirement</span></span> | <span data-ttu-id="fd14b-117">Value</span><span class="sxs-lookup"><span data-stu-id="fd14b-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd14b-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fd14b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fd14b-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fd14b-119">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="fd14b-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fd14b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fd14b-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fd14b-121">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="fd14b-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fd14b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd14b-123"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd14b-123"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="fd14b-124">IDL</span><span class="sxs-lookup"><span data-stu-id="fd14b-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fd14b-125"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fd14b-125"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="fd14b-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fd14b-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="fd14b-127"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="fd14b-127"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="fd14b-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fd14b-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd14b-129"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd14b-129"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fd14b-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="fd14b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd14b-131">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="fd14b-131">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

 





