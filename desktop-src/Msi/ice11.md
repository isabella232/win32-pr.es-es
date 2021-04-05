---
description: ICE11 se usa con instalaciones simultáneas. No se recomiendan instalaciones simultáneas para la instalación de aplicaciones destinadas a publicarse en el público. Para obtener información acerca de las instalaciones simultáneas, consulte instalaciones simultáneas.
ms.assetid: fbcc94fa-be94-4ad1-a3f0-ea7d50ee0a15
title: ICE11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d3f85a4dc4d736acfbd4385324aa35565f399bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002255"
---
# <a name="ice11"></a><span data-ttu-id="3f613-105">ICE11</span><span class="sxs-lookup"><span data-stu-id="3f613-105">ICE11</span></span>

<span data-ttu-id="3f613-106">ICE11 se usa con instalaciones simultáneas.</span><span class="sxs-lookup"><span data-stu-id="3f613-106">The ICE11 is used with concurrent installations.</span></span> <span data-ttu-id="3f613-107">No se recomiendan instalaciones simultáneas para la instalación de aplicaciones destinadas a publicarse en el público.</span><span class="sxs-lookup"><span data-stu-id="3f613-107">Concurrent installations are not recommended for the installation of applications intended for release to the public.</span></span> <span data-ttu-id="3f613-108">Para obtener información acerca de las instalaciones simultáneas, consulte [instalaciones](concurrent-installations.md)simultáneas.</span><span class="sxs-lookup"><span data-stu-id="3f613-108">For information about concurrent installations please see [Concurrent Installations](concurrent-installations.md).</span></span>

## <a name="result"></a><span data-ttu-id="3f613-109">Resultado</span><span class="sxs-lookup"><span data-stu-id="3f613-109">Result</span></span>

<span data-ttu-id="3f613-110">ICE11 valida la columna de origen de la [tabla CustomAction](customaction-table.md) de acciones personalizadas de instalación simultánea.</span><span class="sxs-lookup"><span data-stu-id="3f613-110">ICE11 validates the Source column of the [CustomAction table](customaction-table.md) of concurrent installation custom actions.</span></span> <span data-ttu-id="3f613-111">La columna de origen debe contener un [GUID](guid.md) válido (código de producto MSI).</span><span class="sxs-lookup"><span data-stu-id="3f613-111">The Source column must contain a valid [GUID](guid.md) (MSI product code).</span></span>

<span data-ttu-id="3f613-112">ICE11 publica un error si la columna de origen de la tabla CustomAction no se creó correctamente para las acciones personalizadas de instalación simultánea.</span><span class="sxs-lookup"><span data-stu-id="3f613-112">ICE11 posts an error if the Source column of the CustomAction table is authored incorrectly for concurrent installation custom actions.</span></span>

## <a name="example"></a><span data-ttu-id="3f613-113">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3f613-113">Example</span></span>

<span data-ttu-id="3f613-114">ICE envía los siguientes mensajes de error para el ejemplo que se muestra.</span><span class="sxs-lookup"><span data-stu-id="3f613-114">ICE posts the following error messages for the example shown.</span></span>

``` syntax
CustomAction: CA4 is a nested install of an advertised MSI.  The 'Source' must contain a valid MSI product code.  Current: ProductCode.
CustomAction: CA1 is a nested install of an advertised MSI.  It duplicates the ProductCode of the base MSI package.  Current: {BFB69273-F0AE-45C4-9853-0AF946714768}.
CustomAction: CA2 is a nested install of an advertised MSI.  The GUID must be all upper-case.  Current: {BFB69273-F0AE-55c5-9853-0AF946714768}.
```

<span data-ttu-id="3f613-115">[Tabla de propiedades](property-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="3f613-115">[Property Table](property-table.md) (partial)</span></span>



| <span data-ttu-id="3f613-116">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3f613-116">Property</span></span>        | <span data-ttu-id="3f613-117">Value</span><span class="sxs-lookup"><span data-stu-id="3f613-117">Value</span></span>                                  |
|-----------------|----------------------------------------|
| <span data-ttu-id="3f613-118">**ProductCode**</span><span class="sxs-lookup"><span data-stu-id="3f613-118">**ProductCode**</span></span> | <span data-ttu-id="3f613-119">{BFB69273-F0AE-45C4-9853-0AF946714768}</span><span class="sxs-lookup"><span data-stu-id="3f613-119">{BFB69273-F0AE-45C4-9853-0AF946714768}</span></span> |



 

<span data-ttu-id="3f613-120">[Tabla CustomAction](customaction-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="3f613-120">[CustomAction Table](customaction-table.md) (partial)</span></span>



| <span data-ttu-id="3f613-121">CustomAction</span><span class="sxs-lookup"><span data-stu-id="3f613-121">CustomAction</span></span> | <span data-ttu-id="3f613-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="3f613-122">Type</span></span> | <span data-ttu-id="3f613-123">Source</span><span class="sxs-lookup"><span data-stu-id="3f613-123">Source</span></span>                                 |
|--------------|------|----------------------------------------|
| <span data-ttu-id="3f613-124">CA1</span><span class="sxs-lookup"><span data-stu-id="3f613-124">CA1</span></span>          | <span data-ttu-id="3f613-125">39</span><span class="sxs-lookup"><span data-stu-id="3f613-125">39</span></span>   | <span data-ttu-id="3f613-126">{BFB69273-F0AE-45C4-9853-0AF946714768}</span><span class="sxs-lookup"><span data-stu-id="3f613-126">{BFB69273-F0AE-45C4-9853-0AF946714768}</span></span> |
| <span data-ttu-id="3f613-127">CA2</span><span class="sxs-lookup"><span data-stu-id="3f613-127">CA2</span></span>          | <span data-ttu-id="3f613-128">39</span><span class="sxs-lookup"><span data-stu-id="3f613-128">39</span></span>   | <span data-ttu-id="3f613-129">{BFB69273-F0AE-55c5-9853-0AF946714768}</span><span class="sxs-lookup"><span data-stu-id="3f613-129">{BFB69273-F0AE-55c5-9853-0AF946714768}</span></span> |
| <span data-ttu-id="3f613-130">CA3</span><span class="sxs-lookup"><span data-stu-id="3f613-130">CA3</span></span>          | <span data-ttu-id="3f613-131">39</span><span class="sxs-lookup"><span data-stu-id="3f613-131">39</span></span>   | <span data-ttu-id="3f613-132">{BFB69273-F0AE-66C6-9853-0AF946714768}</span><span class="sxs-lookup"><span data-stu-id="3f613-132">{BFB69273-F0AE-66C6-9853-0AF946714768}</span></span> |
| <span data-ttu-id="3f613-133">CA4</span><span class="sxs-lookup"><span data-stu-id="3f613-133">CA4</span></span>          | <span data-ttu-id="3f613-134">39</span><span class="sxs-lookup"><span data-stu-id="3f613-134">39</span></span>   | <span data-ttu-id="3f613-135">ProductCode</span><span class="sxs-lookup"><span data-stu-id="3f613-135">ProductCode</span></span>                            |



 

<span data-ttu-id="3f613-136">Para corregir los errores, en el caso de CA1, no puede realizar una instalación simultánea del "paquete base".</span><span class="sxs-lookup"><span data-stu-id="3f613-136">To fix the errors, for CA1, you cannot do a concurrent installation of the "base package".</span></span> <span data-ttu-id="3f613-137">Esto daría lugar a una instalación recursiva.</span><span class="sxs-lookup"><span data-stu-id="3f613-137">This would result in a recursive installation.</span></span> <span data-ttu-id="3f613-138">Esta entrada se debe quitar o la columna de origen debe cambiarse por un GUID para una MSI anunciada que difiere del GUID del paquete base.</span><span class="sxs-lookup"><span data-stu-id="3f613-138">This entry should be removed or the Source column should be changed to a GUID for an advertised MSI that differs from the base package's GUID.</span></span> <span data-ttu-id="3f613-139">En el caso de CA2, haga que todos los caracteres del GUID estén en mayúsculas.</span><span class="sxs-lookup"><span data-stu-id="3f613-139">For CA2, make all characters of the GUID uppercase.</span></span> <span data-ttu-id="3f613-140">Por último, cambie la columna de origen de CA4's para que haga referencia a un GUID válido de una MSI anunciada.</span><span class="sxs-lookup"><span data-stu-id="3f613-140">Lastly, change CA4's Source column to reference a valid GUID of an advertised MSI.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3f613-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3f613-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f613-142">Instalaciones simultáneas</span><span class="sxs-lookup"><span data-stu-id="3f613-142">Concurrent Installations</span></span>](concurrent-installations.md)
</dt> <dt>

[<span data-ttu-id="3f613-143">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="3f613-143">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



