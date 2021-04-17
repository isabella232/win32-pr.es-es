---
description: ICE74 comprueba que la propiedad FASTOEM no se ha creado en la tabla de propiedades.
ms.assetid: 2af132f0-0ffa-405f-9d05-7cb5d5f826b8
title: ICE74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fe2762710e061f2c88f55893294a40fbac8700f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652479"
---
# <a name="ice74"></a><span data-ttu-id="4c80d-103">ICE74</span><span class="sxs-lookup"><span data-stu-id="4c80d-103">ICE74</span></span>

<span data-ttu-id="4c80d-104">ICE74 comprueba que la propiedad [**FASTOEM**](fastoem.md) no se ha creado en la tabla de [propiedades](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="4c80d-104">ICE74 verifies that the [**FASTOEM**](fastoem.md) property has not been authored into the [Property table](property-table.md).</span></span>

<span data-ttu-id="4c80d-105">La propiedad [**FASTOEM**](fastoem.md) permite a los OEM reducir el tiempo necesario para instalar Windows Installer aplicaciones por primera vez.</span><span class="sxs-lookup"><span data-stu-id="4c80d-105">The [**FASTOEM**](fastoem.md) property enables OEMs to reduce the time required to install Windows Installer applications for the first time.</span></span> <span data-ttu-id="4c80d-106">No se puede usar después de la primera instalación.</span><span class="sxs-lookup"><span data-stu-id="4c80d-106">It cannot be used after the first install.</span></span> <span data-ttu-id="4c80d-107">La propiedad **FASTOEM** no se debe crear en la tabla de propiedades porque interfiere con las instalaciones posteriores para el mantenimiento, la eliminación o la reparación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4c80d-107">The **FASTOEM** property must not be authored in the Property table because this interferes with subsequent installations for the maintenance, removal, or repair of the application.</span></span>

<span data-ttu-id="4c80d-108">ICE74 también comprueba que la propiedad [**UpgradeCode**](upgradecode.md) se crea en la tabla de [propiedades](property-table.md)y que su valor no es un GUID nulo, {00000000-0000-0000-0000-000000000000} .</span><span class="sxs-lookup"><span data-stu-id="4c80d-108">ICE74 also verifies that the [**UpgradeCode**](upgradecode.md) property is authored into the [Property table](property-table.md), and that its value is not a null GUID, {00000000-0000-0000-0000-000000000000}.</span></span>

## <a name="result"></a><span data-ttu-id="4c80d-109">Resultado</span><span class="sxs-lookup"><span data-stu-id="4c80d-109">Result</span></span>

<span data-ttu-id="4c80d-110">ICE74 puede exponer los errores siguientes.</span><span class="sxs-lookup"><span data-stu-id="4c80d-110">ICE74 can post the following errors.</span></span>



| <span data-ttu-id="4c80d-111">Error ICE74</span><span class="sxs-lookup"><span data-stu-id="4c80d-111">ICE74 error</span></span>                                                                       | <span data-ttu-id="4c80d-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="4c80d-112">Description</span></span>                                                                                             |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c80d-113">La propiedad [**FASTOEM**](fastoem.md) no se puede crear en la tabla de propiedades.</span><span class="sxs-lookup"><span data-stu-id="4c80d-113">The [**FASTOEM**](fastoem.md) property cannot be authored in the Property table.</span></span> | <span data-ttu-id="4c80d-114">La propiedad [**FASTOEM**](fastoem.md) se ha establecido en la tabla de propiedades.</span><span class="sxs-lookup"><span data-stu-id="4c80d-114">The [**FASTOEM**](fastoem.md) property has been set in the Property table.</span></span>                             |
| <span data-ttu-id="4c80d-115">' \[ 2 \] ' no es un [**UpgradeCode**](upgradecode.md)válido.</span><span class="sxs-lookup"><span data-stu-id="4c80d-115">'\[2\]' is not a valid [**UpgradeCode**](upgradecode.md).</span></span>                        | <span data-ttu-id="4c80d-116">Se ha especificado un GUID null para la propiedad [**UpgradeCode**](upgradecode.md) en la tabla de propiedades.</span><span class="sxs-lookup"><span data-stu-id="4c80d-116">A null GUID has been entered for the [**UpgradeCode**](upgradecode.md) property in the Property table.</span></span> |



 

<span data-ttu-id="4c80d-117">ICE74 puede enviar la siguiente advertencia.</span><span class="sxs-lookup"><span data-stu-id="4c80d-117">ICE74 can post the following warning.</span></span>



| <span data-ttu-id="4c80d-118">ADVERTENCIA de ICE74</span><span class="sxs-lookup"><span data-stu-id="4c80d-118">ICE74 warning</span></span>                                                                                                                                                                                             | <span data-ttu-id="4c80d-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="4c80d-119">Description</span></span>                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c80d-120">La propiedad [**UpgradeCode**](upgradecode.md) no se crea en la tabla de propiedades.</span><span class="sxs-lookup"><span data-stu-id="4c80d-120">The [**UpgradeCode**](upgradecode.md) property is not authored in the Property table.</span></span> <span data-ttu-id="4c80d-121">Se recomienda encarecidamente que los autores de los paquetes de instalación especifiquen **UpgradeCode** para su aplicación.</span><span class="sxs-lookup"><span data-stu-id="4c80d-121">It is strongly recommended that authors of installation packages specify an **UpgradeCode** for their application.</span></span> | <span data-ttu-id="4c80d-122">La propiedad [**UpgradeCode**](upgradecode.md) no se crea en la tabla de propiedades.</span><span class="sxs-lookup"><span data-stu-id="4c80d-122">The [**UpgradeCode**](upgradecode.md) property is not authored in the Property table.</span></span> |



 

## <a name="example"></a><span data-ttu-id="4c80d-123">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4c80d-123">Example</span></span>

<span data-ttu-id="4c80d-124">ICE74 notifica el siguiente error si se establece la propiedad [**FASTOEM**](fastoem.md) : FASTOEM</span><span class="sxs-lookup"><span data-stu-id="4c80d-124">ICE74 reports the following error if the [**FASTOEM**](fastoem.md) property is set: The FASTOEM</span></span>

``` syntax
 property cannot be authored in the Property table.
```

<span data-ttu-id="4c80d-125">[Tabla de propiedades](property-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="4c80d-125">[Property Table](property-table.md) (partial)</span></span>



| <span data-ttu-id="4c80d-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4c80d-126">Property</span></span>                   | <span data-ttu-id="4c80d-127">Value</span><span class="sxs-lookup"><span data-stu-id="4c80d-127">Value</span></span> |
|----------------------------|-------|
| [<span data-ttu-id="4c80d-128">**FASTOEM**</span><span class="sxs-lookup"><span data-stu-id="4c80d-128">**FASTOEM**</span></span>](fastoem.md) | <span data-ttu-id="4c80d-129">1</span><span class="sxs-lookup"><span data-stu-id="4c80d-129">1</span></span>     |



 

<span data-ttu-id="4c80d-130">Para corregir este error, quite la propiedad [**FASTOEM**](fastoem.md) de la tabla de propiedades.</span><span class="sxs-lookup"><span data-stu-id="4c80d-130">To fix this error remove the [**FASTOEM**](fastoem.md) property from the Property Table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4c80d-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4c80d-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c80d-132">**propiedad FASTOEM**</span><span class="sxs-lookup"><span data-stu-id="4c80d-132">**FASTOEM property**</span></span>](fastoem.md)
</dt> <dt>

[<span data-ttu-id="4c80d-133">Tabla de propiedades</span><span class="sxs-lookup"><span data-stu-id="4c80d-133">Property table</span></span>](property-table.md)
</dt> <dt>

[<span data-ttu-id="4c80d-134">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="4c80d-134">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



