---
description: La propiedad de contexto devuelve el contexto de esta revisión.
ms.assetid: 09c92b0b-44f3-4355-8171-03da8ba32757
title: Patch. Context (propiedad)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.Context
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 7a6495b199046a361910741545a7178050621ccd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653365"
---
# <a name="patchcontext-property"></a><span data-ttu-id="223cd-103">Patch. Context (propiedad)</span><span class="sxs-lookup"><span data-stu-id="223cd-103">Patch.Context property</span></span>

<span data-ttu-id="223cd-104">La propiedad de **contexto** devuelve el contexto de esta revisión.</span><span class="sxs-lookup"><span data-stu-id="223cd-104">The **Context** property returns the context of this patch.</span></span>

<span data-ttu-id="223cd-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="223cd-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="223cd-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="223cd-106">Syntax</span></span>


```JScript
propVal = Patch.Context
```



## <a name="property-value"></a><span data-ttu-id="223cd-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="223cd-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="223cd-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="223cd-108">Remarks</span></span>

<span data-ttu-id="223cd-109">Esta propiedad devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="223cd-109">This property returns one of the following values.</span></span>



| <span data-ttu-id="223cd-110">Context</span><span class="sxs-lookup"><span data-stu-id="223cd-110">Context</span></span>                        | <span data-ttu-id="223cd-111">Value</span><span class="sxs-lookup"><span data-stu-id="223cd-111">Value</span></span> | <span data-ttu-id="223cd-112">Significado</span><span class="sxs-lookup"><span data-stu-id="223cd-112">Meaning</span></span>                        |
|--------------------------------|-------|--------------------------------|
| <span data-ttu-id="223cd-113">MSIINSTALLCONTEXT \_ USERMANAGED</span><span class="sxs-lookup"><span data-stu-id="223cd-113">MSIINSTALLCONTEXT\_USERMANAGED</span></span> | <span data-ttu-id="223cd-114">1</span><span class="sxs-lookup"><span data-stu-id="223cd-114">1</span></span>     | <span data-ttu-id="223cd-115">Revisión en contexto administrado.</span><span class="sxs-lookup"><span data-stu-id="223cd-115">Patch under managed context.</span></span>   |
| <span data-ttu-id="223cd-116">\_usuario MSIINSTALLCONTEXT</span><span class="sxs-lookup"><span data-stu-id="223cd-116">MSIINSTALLCONTEXT\_USER</span></span>        | <span data-ttu-id="223cd-117">2</span><span class="sxs-lookup"><span data-stu-id="223cd-117">2</span></span>     | <span data-ttu-id="223cd-118">Revisión en contexto no administrado.</span><span class="sxs-lookup"><span data-stu-id="223cd-118">Patch under unmanaged context.</span></span> |
| <span data-ttu-id="223cd-119">\_máquina MSIINSTALLCONTEXT</span><span class="sxs-lookup"><span data-stu-id="223cd-119">MSIINSTALLCONTEXT\_MACHINE</span></span>     | <span data-ttu-id="223cd-120">4</span><span class="sxs-lookup"><span data-stu-id="223cd-120">4</span></span>     | <span data-ttu-id="223cd-121">Revisión en contexto de la máquina.</span><span class="sxs-lookup"><span data-stu-id="223cd-121">Patch under machine context.</span></span>   |



 

## <a name="requirements"></a><span data-ttu-id="223cd-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="223cd-122">Requirements</span></span>



| <span data-ttu-id="223cd-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="223cd-123">Requirement</span></span> | <span data-ttu-id="223cd-124">Value</span><span class="sxs-lookup"><span data-stu-id="223cd-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="223cd-125">Versión</span><span class="sxs-lookup"><span data-stu-id="223cd-125">Version</span></span><br/> | <span data-ttu-id="223cd-126">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="223cd-126">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="223cd-127">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="223cd-127">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="223cd-128">Windows Installer 3,0 o posterior en Windows Server 2003, Windows XP y Windows 2000</span><span class="sxs-lookup"><span data-stu-id="223cd-128">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="223cd-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="223cd-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="223cd-130"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="223cd-130"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="223cd-131">IID</span><span class="sxs-lookup"><span data-stu-id="223cd-131">IID</span></span><br/>     | <span data-ttu-id="223cd-132">IID \_ IPatch se define como 000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="223cd-132">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="223cd-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="223cd-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="223cd-134">**Patch (objeto)**</span><span class="sxs-lookup"><span data-stu-id="223cd-134">**Patch Object**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="223cd-135">No se admite en Windows Installer 2,0 y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="223cd-135">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




