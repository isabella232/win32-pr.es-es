---
description: ICE73 comprueba que el paquete no reutiliza códigos de paquete, códigos de actualización ni códigos de producto de los ejemplos del SDK de Windows Installer. Los paquetes nunca deben reutilizar el paquete, la actualización o los códigos de producto de otro producto.
ms.assetid: a04429c2-ff9e-4ec8-8d07-faf1479f4920
title: ICE73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11ac0e192f7c2ab7fb6f6236e45e0e4da70157e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666683"
---
# <a name="ice73"></a><span data-ttu-id="7fde2-104">ICE73</span><span class="sxs-lookup"><span data-stu-id="7fde2-104">ICE73</span></span>

<span data-ttu-id="7fde2-105">ICE73 comprueba que el paquete no reutiliza códigos de paquete, códigos de actualización ni códigos de producto de los ejemplos del SDK de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="7fde2-105">ICE73 verifies that your package does not reuse package codes, upgrade codes, or product codes of the Windows Installer SDK samples.</span></span> <span data-ttu-id="7fde2-106">Los paquetes nunca deben reutilizar el paquete, la actualización o los códigos de producto de otro producto.</span><span class="sxs-lookup"><span data-stu-id="7fde2-106">Packages should never reuse the package, upgrade, or product codes of another product.</span></span>

## <a name="result"></a><span data-ttu-id="7fde2-107">Resultado</span><span class="sxs-lookup"><span data-stu-id="7fde2-107">Result</span></span>

<span data-ttu-id="7fde2-108">ICE73 genera una advertencia si el paquete de su producto vuelve a usar un paquete o un código de producto de un ejemplo de SDK de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="7fde2-108">ICE73 outputs a warning if your product's package reuses a package or product code of a Windows Installer SDK sample.</span></span>

## <a name="example"></a><span data-ttu-id="7fde2-109">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7fde2-109">Example</span></span>

<span data-ttu-id="7fde2-110">ICE73 notifica los siguientes errores para el ejemplo mostrado:</span><span class="sxs-lookup"><span data-stu-id="7fde2-110">ICE73 reports the following errors for the example shown:</span></span>

``` syntax
This package reuses the '{80F7E030-A751-11D2-A7D4-006097C99860}' ProductCode of the orca.msi 1.0 Windows Installer SDK package.
This package reuses the '{000C1101-0000-0000-C000-000000000047}' Package Code of the msispy.msi 1.0 Windows Installer SDK package.
This package reuses the '{8FC7****-88A0-4b41-82B8-8905D4AA904C}' Upgrade Code of a 1.1 Windows Installer SDK package.
```

> [!Note]  
> <span data-ttu-id="7fde2-111">Los asteriscos ( \* \* \* \* ) del GUID representan el intervalo de GUID reservado para los paquetes del SDK de Windows Installer posteriores.</span><span class="sxs-lookup"><span data-stu-id="7fde2-111">The asterisks (\*\*\*\*) in the GUID represent the range of GUIDs reserved for subsequent Windows Installer SDK packages.</span></span>

 

<span data-ttu-id="7fde2-112">Para corregir los errores, genere un nuevo GUID único para los códigos de producto y paquete del paquete.</span><span class="sxs-lookup"><span data-stu-id="7fde2-112">To fix the errors, generate a new unique GUID for your package's product and package codes.</span></span> <span data-ttu-id="7fde2-113">También necesitará un nuevo GUID único para el código de actualización del paquete.</span><span class="sxs-lookup"><span data-stu-id="7fde2-113">You will also need a new unique GUID for your package's upgrade code.</span></span>

<span data-ttu-id="7fde2-114">[Secuencia de información de Resumen](summary-information-stream.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="7fde2-114">[Summary Information Stream](summary-information-stream.md) (partial)</span></span>



| <span data-ttu-id="7fde2-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7fde2-115">Property</span></span>       | <span data-ttu-id="7fde2-116">Value</span><span class="sxs-lookup"><span data-stu-id="7fde2-116">Value</span></span>                                  |
|----------------|----------------------------------------|
| <span data-ttu-id="7fde2-117">PID \_ REVNUMBER</span><span class="sxs-lookup"><span data-stu-id="7fde2-117">PID\_REVNUMBER</span></span> | <span data-ttu-id="7fde2-118">{000C1101-0000-0000-C000-000000000047}</span><span class="sxs-lookup"><span data-stu-id="7fde2-118">{000C1101-0000-0000-C000-000000000047}</span></span> |



 

<span data-ttu-id="7fde2-119">[Tabla de propiedades](property-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="7fde2-119">[Property Table](property-table.md) (partial)</span></span>



| <span data-ttu-id="7fde2-120">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7fde2-120">Property</span></span>                           | <span data-ttu-id="7fde2-121">Value</span><span class="sxs-lookup"><span data-stu-id="7fde2-121">Value</span></span>                                  |
|------------------------------------|----------------------------------------|
| [<span data-ttu-id="7fde2-122">**ProductCode**</span><span class="sxs-lookup"><span data-stu-id="7fde2-122">**ProductCode**</span></span>](productcode.md) | <span data-ttu-id="7fde2-123">{80F7E030-A751-11D2-A7D4-006097C99860}</span><span class="sxs-lookup"><span data-stu-id="7fde2-123">{80F7E030-A751-11D2-A7D4-006097C99860}</span></span> |
| [<span data-ttu-id="7fde2-124">**UpgradeCode**</span><span class="sxs-lookup"><span data-stu-id="7fde2-124">**UpgradeCode**</span></span>](upgradecode.md) | <span data-ttu-id="7fde2-125">{8FC70000-88A0-4b41-82B8-8905D4AA904C}</span><span class="sxs-lookup"><span data-stu-id="7fde2-125">{8FC70000-88A0-4b41-82B8-8905D4AA904C}</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="7fde2-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7fde2-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7fde2-127">Códigos de paquete</span><span class="sxs-lookup"><span data-stu-id="7fde2-127">Package Codes</span></span>](package-codes.md)
</dt> <dt>

[<span data-ttu-id="7fde2-128">Códigos de producto</span><span class="sxs-lookup"><span data-stu-id="7fde2-128">Product Codes</span></span>](product-codes.md)
</dt> <dt>

[<span data-ttu-id="7fde2-129">**Propiedad de Resumen de número de revisión**</span><span class="sxs-lookup"><span data-stu-id="7fde2-129">**Revision Number Summary Property**</span></span>](revision-number-summary.md)
</dt> <dt>

[<span data-ttu-id="7fde2-130">**Propiedad UpgradeCode**</span><span class="sxs-lookup"><span data-stu-id="7fde2-130">**UpgradeCode Property**</span></span>](upgradecode.md)
</dt> <dt>

[<span data-ttu-id="7fde2-131">**Propiedad ProductCode**</span><span class="sxs-lookup"><span data-stu-id="7fde2-131">**ProductCode Property**</span></span>](productcode.md)
</dt> <dt>

[<span data-ttu-id="7fde2-132">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="7fde2-132">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



