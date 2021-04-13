---
title: Propiedad ResourceLocator. FragmentDialect (WSManDisp. h)
description: Obtiene o establece el dialecto de lenguaje para un dialecto de fragmento de recurso cuando se usa ResourceLocator en operaciones de objeto de sesión como Session. get, Session. put o Session. Enumerate.
ms.assetid: 60b08084-f4b9-4049-b0cd-a7420fcffd7c
ms.tgt_platform: multiple
keywords:
- Administración remota de Windows de la propiedad FragmentDialect
- Administración remota de Windows de la propiedad FragmentDialect, objeto ResourceLocator
- Administración remota de Windows de objeto ResourceLocator, propiedad FragmentDialect
topic_type:
- apiref
api_name:
- ResourceLocator.FragmentDialect
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1fe42c2bbe15c75d5f38ea47119f9649e678931
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492676"
---
# <a name="resourcelocatorfragmentdialect-property"></a><span data-ttu-id="47e80-106">Propiedad ResourceLocator. FragmentDialect</span><span class="sxs-lookup"><span data-stu-id="47e80-106">ResourceLocator.FragmentDialect property</span></span>

<span data-ttu-id="47e80-107">Obtiene o establece el dialecto de lenguaje para un *dialecto* de [*fragmento*](windows-remote-management-glossary.md) de [*recurso*](windows-remote-management-glossary.md) cuando se usa [**ResourceLocator**](resourcelocator.md) en operaciones de objeto de [**sesión**](session.md) como [**Session. Get**](session-get.md), [**Session. put**](session-put.md)o [**Session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="47e80-107">Gets or sets the language dialect for a [*resource*](windows-remote-management-glossary.md) [*fragment*](windows-remote-management-glossary.md) *dialect* when [**ResourceLocator**](resourcelocator.md) is used in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span> <span data-ttu-id="47e80-108">Un fragmento representa una propiedad o parte de un recurso.</span><span class="sxs-lookup"><span data-stu-id="47e80-108">A fragment represents one property or part of a resource.</span></span> <span data-ttu-id="47e80-109">Puede proporcionar un objeto [**ResourceLocator**](resourcelocator.md) en lugar de especificar un URI de recurso en las operaciones del objeto de [**sesión**](session.md) .</span><span class="sxs-lookup"><span data-stu-id="47e80-109">You can provide a [**ResourceLocator**](resourcelocator.md) object instead of specifying a resource URI in [**Session**](session.md) object operations.</span></span> <span data-ttu-id="47e80-110">El dialecto indica qué lenguaje XML describe el fragmento para el servicio que implementa el [protocolo WS-Management](ws-management-protocol.md) y recibe la solicitud.</span><span class="sxs-lookup"><span data-stu-id="47e80-110">The dialect indicates what XML language describes the fragment to the service that implements the [WS-Management Protocol](ws-management-protocol.md) and receives the request.</span></span>

<span data-ttu-id="47e80-111">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="47e80-111">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="47e80-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="47e80-112">Syntax</span></span>


```VB
ResourceLocator.FragmentDialect As string
```



## <a name="property-value"></a><span data-ttu-id="47e80-113">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="47e80-113">Property value</span></span>

<span data-ttu-id="47e80-114">Cadena XML que identifica el idioma usado en la propiedad [**FragmentPath**](resourcelocator-fragmentpath.md) .</span><span class="sxs-lookup"><span data-stu-id="47e80-114">An XML string that identifies the language used in the [**FragmentPath**](resourcelocator-fragmentpath.md) property.</span></span> <span data-ttu-id="47e80-115">La cadena de dialecto tiene como valor predeterminado la especificación XPath 1,0.</span><span class="sxs-lookup"><span data-stu-id="47e80-115">The dialect string defaults to the XPath 1.0 specification.</span></span> <span data-ttu-id="47e80-116">Para más información, consulte [https://www.w3.org/TR/xpath](https://www.w3.org/TR/xpath).</span><span class="sxs-lookup"><span data-stu-id="47e80-116">For more information, see [https://www.w3.org/TR/xpath](https://www.w3.org/TR/xpath).</span></span>

## <a name="remarks"></a><span data-ttu-id="47e80-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="47e80-117">Remarks</span></span>

<span data-ttu-id="47e80-118">[**IWSManResourceLocator:: FragmentDialect**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanresourcelocator-get_fragmentdialect) es la propiedad de C++ correspondiente.</span><span class="sxs-lookup"><span data-stu-id="47e80-118">[**IWSManResourceLocator::FragmentDialect**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanresourcelocator-get_fragmentdialect) is the corresponding C++ property.</span></span>

## <a name="requirements"></a><span data-ttu-id="47e80-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47e80-119">Requirements</span></span>



| <span data-ttu-id="47e80-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="47e80-120">Requirement</span></span> | <span data-ttu-id="47e80-121">Value</span><span class="sxs-lookup"><span data-stu-id="47e80-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="47e80-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="47e80-122">Minimum supported client</span></span><br/> | <span data-ttu-id="47e80-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="47e80-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="47e80-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="47e80-124">Minimum supported server</span></span><br/> | <span data-ttu-id="47e80-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="47e80-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="47e80-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="47e80-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="47e80-127"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="47e80-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="47e80-128">IDL</span><span class="sxs-lookup"><span data-stu-id="47e80-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="47e80-129"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="47e80-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="47e80-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="47e80-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="47e80-131"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="47e80-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="47e80-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="47e80-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="47e80-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47e80-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="47e80-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="47e80-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47e80-135">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="47e80-135">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

 





