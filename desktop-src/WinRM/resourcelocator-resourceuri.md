---
title: Propiedad ResourceLocator. ResourceURI (WSManDisp. h)
description: Obtiene o establece el URI de recurso en un objeto ResourceLocator.
ms.assetid: adb1e08a-290f-4a23-a6e4-d7567a6b7eee
ms.tgt_platform: multiple
keywords:
- Propiedad ResourceURI Administración remota de Windows
- Propiedad ResourceURI Administración remota de Windows, objeto ResourceLocator
- Administración remota de Windows objeto ResourceLocator, ResourceURI (propiedad)
topic_type:
- apiref
api_name:
- ResourceLocator.ResourceURI
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28f804835b5445c32f74094e8280a598785d1526
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491579"
---
# <a name="resourcelocatorresourceuri-property"></a><span data-ttu-id="b5266-106">Propiedad ResourceLocator. ResourceURI</span><span class="sxs-lookup"><span data-stu-id="b5266-106">ResourceLocator.ResourceURI property</span></span>

<span data-ttu-id="b5266-107">Obtiene o establece el [*URI de recurso*](windows-remote-management-glossary.md) en un objeto [**ResourceLocator**](resourcelocator.md) .</span><span class="sxs-lookup"><span data-stu-id="b5266-107">Gets or sets the [*resource URI*](windows-remote-management-glossary.md) in a [**ResourceLocator**](resourcelocator.md) object.</span></span> <span data-ttu-id="b5266-108">Puede proporcionar un objeto [**ResourceLocator**](resourcelocator.md) en lugar de especificar un URI de recurso en operaciones de objetos de [**sesión**](session.md) como [**Session. Get**](session-get.md), [**Session. put**](session-put.md)o [**Session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="b5266-108">You can provide a [**ResourceLocator**](resourcelocator.md) object instead of specifying a resource URI in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span>

<span data-ttu-id="b5266-109">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="b5266-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5266-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b5266-110">Syntax</span></span>


```VB
ResourceLocator.ResourceURI As string
```



## <a name="property-value"></a><span data-ttu-id="b5266-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="b5266-111">Property value</span></span>

<span data-ttu-id="b5266-112">Cadena que identifica el recurso.</span><span class="sxs-lookup"><span data-stu-id="b5266-112">A string that identifies the resource.</span></span> <span data-ttu-id="b5266-113">Al establecer el URI de recurso para un objeto [**ResourceLocator**](resourcelocator.md) , el URI debe contener solo la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="b5266-113">When setting the resource URI for a [**ResourceLocator**](resourcelocator.md) object, the URI must contain only the path.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5266-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b5266-114">Remarks</span></span>

<span data-ttu-id="b5266-115">El siguiente es un ejemplo de una ruta de acceso adecuada para [**ResourceURI**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanresourcelocator-get_resourceuri).</span><span class="sxs-lookup"><span data-stu-id="b5266-115">The following is an example of a proper path for [**ResourceURI**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanresourcelocator-get_resourceuri).</span></span>

``` syntax
"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service"
```

<span data-ttu-id="b5266-116">La ruta de acceso siguiente no funciona porque contiene una clave para una instancia específica.</span><span class="sxs-lookup"><span data-stu-id="b5266-116">The following path does not work because it contains a key for a specific instance.</span></span> <span data-ttu-id="b5266-117">Use el método [**ResourceLocator. AddSelector**](resourcelocator-addselector.md) para especificar una instancia determinada.</span><span class="sxs-lookup"><span data-stu-id="b5266-117">Use the [**ResourceLocator.AddSelector**](resourcelocator-addselector.md) method to specify a particular instance.</span></span>

``` syntax
"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"
```

<span data-ttu-id="b5266-118">**IWSManResourceLocator:: ResourceURI** es el método de C++ correspondiente.</span><span class="sxs-lookup"><span data-stu-id="b5266-118">**IWSManResourceLocator::ResourceURI** is the corresponding C++ method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5266-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5266-119">Requirements</span></span>



| <span data-ttu-id="b5266-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5266-120">Requirement</span></span> | <span data-ttu-id="b5266-121">Value</span><span class="sxs-lookup"><span data-stu-id="b5266-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5266-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b5266-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b5266-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b5266-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="b5266-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b5266-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b5266-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b5266-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="b5266-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b5266-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5266-127"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5266-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b5266-128">IDL</span><span class="sxs-lookup"><span data-stu-id="b5266-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b5266-129"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b5266-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="b5266-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b5266-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="b5266-131"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b5266-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b5266-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b5266-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5266-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5266-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b5266-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="b5266-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5266-135">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="b5266-135">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

 





