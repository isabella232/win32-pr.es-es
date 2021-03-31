---
title: Propiedad ResourceLocator. FragmentPath (WSManDisp. h)
description: Obtiene o establece la ruta de acceso de un fragmento de recursos o propiedad cuando se usa ResourceLocator en operaciones de objeto de sesión como Session. get, Session. put o Session. Enumerate.
ms.assetid: 4d059b57-fca5-4a75-9396-6505920498c3
ms.tgt_platform: multiple
keywords:
- Administración remota de Windows de la propiedad FragmentPath
- Administración remota de Windows de la propiedad FragmentPath, objeto ResourceLocator
- Administración remota de Windows de objeto ResourceLocator, propiedad FragmentPath
topic_type:
- apiref
api_name:
- ResourceLocator.FragmentPath
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e15fba102f9a7c8a2581271c575857b49bc5df1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079411"
---
# <a name="resourcelocatorfragmentpath-property"></a><span data-ttu-id="c7a10-106">Propiedad ResourceLocator. FragmentPath</span><span class="sxs-lookup"><span data-stu-id="c7a10-106">ResourceLocator.FragmentPath property</span></span>

<span data-ttu-id="c7a10-107">Obtiene o establece la ruta de acceso de un [*fragmento*](windows-remote-management-glossary.md) de [*recursos*](windows-remote-management-glossary.md) o propiedad cuando se usa [**ResourceLocator**](resourcelocator.md) en operaciones de objeto de [**sesión**](session.md) como [**Session. Get**](session-get.md), [**Session. put**](session-put.md)o [**Session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="c7a10-107">Gets or sets the path for a [*resource*](windows-remote-management-glossary.md) [*fragment*](windows-remote-management-glossary.md) or property when [**ResourceLocator**](resourcelocator.md) is used in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span>

<span data-ttu-id="c7a10-108">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="c7a10-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7a10-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c7a10-109">Syntax</span></span>


```VB
ResourceLocator.FragmentPath
```



## <a name="property-value"></a><span data-ttu-id="c7a10-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="c7a10-110">Property value</span></span>

<span data-ttu-id="c7a10-111">Cadena que identifica el fragmento o la propiedad del recurso.</span><span class="sxs-lookup"><span data-stu-id="c7a10-111">String that identifies the fragment or property of the resource.</span></span> <span data-ttu-id="c7a10-112">Por ejemplo, si el recurso es una unidad de disco y la propiedad solicitada es fabricante, la cadena puede contener `Diskdrive/Manufacturer` .</span><span class="sxs-lookup"><span data-stu-id="c7a10-112">For example, if the resource is a disk drive and the requested property is Manufacturer, the string may contain `Diskdrive/Manufacturer`.</span></span> <span data-ttu-id="c7a10-113">El texto del fragmento distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="c7a10-113">The fragment text is case-sensitive.</span></span> <span data-ttu-id="c7a10-114">En este caso, no se puede usar `diskdrive/manufacturer` .</span><span class="sxs-lookup"><span data-stu-id="c7a10-114">In this case, you cannot use `diskdrive/manufacturer`.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7a10-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c7a10-115">Remarks</span></span>

<span data-ttu-id="c7a10-116">**IWSManResourceLocator:: FragmentPath** es la propiedad de C++ correspondiente.</span><span class="sxs-lookup"><span data-stu-id="c7a10-116">**IWSManResourceLocator::FragmentPath** is the corresponding C++ property.</span></span>

<span data-ttu-id="c7a10-117">Puede especificar un elemento de una propiedad de matriz proporcionando el índice de la matriz como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="c7a10-117">You can specify one element of an array property by supplying the array index as shown in the following example.</span></span> <span data-ttu-id="c7a10-118">Tenga en cuenta que la indización de matriz empieza por 1 en lugar de 0.</span><span class="sxs-lookup"><span data-stu-id="c7a10-118">Be aware that array indexing starts with 1 rather than 0.</span></span>


```VB
Const Uri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_NetworkAdapterConfiguration"
Const FragmentPath = "DNSServerSearchOrder[1]"
```



<span data-ttu-id="c7a10-119">Para obtener toda la matriz, especifique el nombre de la propiedad de matriz como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="c7a10-119">To get the whole array, specify the array property name as shown in the following example.</span></span>


```VB
Const Uri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_NetworkAdapterConfiguration"
Const FragmentPath = "DNSServerSearchOrder"
```



## <a name="requirements"></a><span data-ttu-id="c7a10-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7a10-120">Requirements</span></span>



| <span data-ttu-id="c7a10-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7a10-121">Requirement</span></span> | <span data-ttu-id="c7a10-122">Value</span><span class="sxs-lookup"><span data-stu-id="c7a10-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7a10-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c7a10-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c7a10-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c7a10-124">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="c7a10-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c7a10-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c7a10-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c7a10-126">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="c7a10-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c7a10-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7a10-128"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7a10-128"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c7a10-129">IDL</span><span class="sxs-lookup"><span data-stu-id="c7a10-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c7a10-130"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c7a10-130"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="c7a10-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c7a10-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="c7a10-132"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c7a10-132"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c7a10-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c7a10-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7a10-134"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7a10-134"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c7a10-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="c7a10-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7a10-136">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="c7a10-136">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

 





