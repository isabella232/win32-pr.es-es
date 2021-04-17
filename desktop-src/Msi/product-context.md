---
description: La propiedad de contexto devuelve el contexto de este producto.
ms.assetid: aa772a95-eb4e-45af-9788-9833d62139e8
title: Propiedad product. Context
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.Context
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8334ca57d552681afeb77d0b213eca8b92bc1234
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653787"
---
# <a name="productcontext-property"></a><span data-ttu-id="6213c-103">Propiedad product. Context</span><span class="sxs-lookup"><span data-stu-id="6213c-103">Product.Context property</span></span>

<span data-ttu-id="6213c-104">La propiedad de **contexto** devuelve el contexto de este producto.</span><span class="sxs-lookup"><span data-stu-id="6213c-104">The **Context** property returns the context of this product.</span></span>

<span data-ttu-id="6213c-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="6213c-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6213c-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6213c-106">Syntax</span></span>


```JScript
propVal = Product.Context
```



## <a name="property-value"></a><span data-ttu-id="6213c-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="6213c-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="6213c-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6213c-108">Remarks</span></span>

<span data-ttu-id="6213c-109">Esta propiedad puede devolver uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="6213c-109">This property can return one of the following values.</span></span>



| <span data-ttu-id="6213c-110">Context</span><span class="sxs-lookup"><span data-stu-id="6213c-110">Context</span></span>                        | <span data-ttu-id="6213c-111">Value</span><span class="sxs-lookup"><span data-stu-id="6213c-111">Value</span></span> | <span data-ttu-id="6213c-112">Significado</span><span class="sxs-lookup"><span data-stu-id="6213c-112">Meaning</span></span>                           |
|--------------------------------|-------|-----------------------------------|
| <span data-ttu-id="6213c-113">MSIINSTALLCONTEXT \_ USERMANAGED</span><span class="sxs-lookup"><span data-stu-id="6213c-113">MSIINSTALLCONTEXT\_USERMANAGED</span></span> | <span data-ttu-id="6213c-114">1</span><span class="sxs-lookup"><span data-stu-id="6213c-114">1</span></span>     | <span data-ttu-id="6213c-115">Productos en contexto administrado.</span><span class="sxs-lookup"><span data-stu-id="6213c-115">Products under managed context.</span></span>   |
| <span data-ttu-id="6213c-116">\_usuario MSIINSTALLCONTEXT</span><span class="sxs-lookup"><span data-stu-id="6213c-116">MSIINSTALLCONTEXT\_USER</span></span>        | <span data-ttu-id="6213c-117">2</span><span class="sxs-lookup"><span data-stu-id="6213c-117">2</span></span>     | <span data-ttu-id="6213c-118">Productos en contexto no administrado.</span><span class="sxs-lookup"><span data-stu-id="6213c-118">Products under unmanaged context.</span></span> |
| <span data-ttu-id="6213c-119">\_máquina MSIINSTALLCONTEXT</span><span class="sxs-lookup"><span data-stu-id="6213c-119">MSIINSTALLCONTEXT\_MACHINE</span></span>     | <span data-ttu-id="6213c-120">4</span><span class="sxs-lookup"><span data-stu-id="6213c-120">4</span></span>     | <span data-ttu-id="6213c-121">Productos en contexto del equipo.</span><span class="sxs-lookup"><span data-stu-id="6213c-121">Products under machine context.</span></span>   |



 

## <a name="requirements"></a><span data-ttu-id="6213c-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6213c-122">Requirements</span></span>



| <span data-ttu-id="6213c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="6213c-123">Requirement</span></span> | <span data-ttu-id="6213c-124">Value</span><span class="sxs-lookup"><span data-stu-id="6213c-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6213c-125">Versión</span><span class="sxs-lookup"><span data-stu-id="6213c-125">Version</span></span><br/> | <span data-ttu-id="6213c-126">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6213c-126">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="6213c-127">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6213c-127">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="6213c-128">Windows Installer 3,0 o posterior en Windows Server 2003, Windows XP y Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6213c-128">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="6213c-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6213c-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="6213c-130"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6213c-130"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="6213c-131">IID</span><span class="sxs-lookup"><span data-stu-id="6213c-131">IID</span></span><br/>     | <span data-ttu-id="6213c-132">IID \_ IProduct se define como 000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="6213c-132">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="6213c-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="6213c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6213c-134">**Manuales**</span><span class="sxs-lookup"><span data-stu-id="6213c-134">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="6213c-135">No se admite en Windows Installer 2,0 y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="6213c-135">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




