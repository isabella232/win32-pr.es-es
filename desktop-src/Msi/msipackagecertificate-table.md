---
description: En la tabla MsiPackageCertificate se muestran los certificados de firma digital que se usan para comprobar la identidad de los paquetes de instalación que hacen que esta Multiple-Package la instalación.
ms.assetid: d3a97325-2136-4745-8a7d-57e4d6b9d27e
title: Tabla MsiPackageCertificate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fd39ac93ff24da2fa8334a6e4865172471080b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279338"
---
# <a name="msipackagecertificate-table"></a><span data-ttu-id="6acef-103">Tabla MsiPackageCertificate</span><span class="sxs-lookup"><span data-stu-id="6acef-103">MsiPackageCertificate Table</span></span>

<span data-ttu-id="6acef-104">En la tabla MsiPackageCertificate se muestran los certificados de firma digital que se usan para comprobar la identidad de los paquetes de instalación que realizan esta [instalación de varios paquetes](multiple-package-installations.md).</span><span class="sxs-lookup"><span data-stu-id="6acef-104">The MsiPackageCertificate Table lists digital signature certificates used to verify the identity of the installation packages that make this [Multiple-Package Installation](multiple-package-installations.md).</span></span>

<span data-ttu-id="6acef-105">Use esta tabla para crear una [instalación de varios paquetes](multiple-package-installations.md) para un producto que contenga varios paquetes de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="6acef-105">Use this table to author a [multiple-package installation](multiple-package-installations.md) for a product containing multiple Windows Installer packages.</span></span> <span data-ttu-id="6acef-106">Si el primer paquete está firmado digitalmente y contiene una tabla MsiPackageCertificate que especifica certificados digitales para todos los paquetes restantes del producto, el administrador solo necesita aceptar el mensaje de [*control de cuentas de usuario*](u-gly.md) (UAC) que se muestra para el primer paquete.</span><span class="sxs-lookup"><span data-stu-id="6acef-106">If the first package is digitally signed, and contains a MsiPackageCertificate Table specifying digital certificates for all the remaining packages in the product, the administrator needs only accept the [*User Account Control*](u-gly.md) (UAC) prompt displayed for the first package.</span></span> <span data-ttu-id="6acef-107">Después de aceptar el aviso de UAC para el primer paquete, las funciones definidas por el usuario en la [tabla MsiEmbeddedChainer](msiembeddedchainer-table.md) pueden unir los paquetes restantes a la instalación de varios paquetes sin mostrar un mensaje de UAC y requerir una respuesta de administrador para cada paquete.</span><span class="sxs-lookup"><span data-stu-id="6acef-107">After accepting the UAC's prompt for the first package, the user-defined functions in the [MsiEmbeddedChainer table](msiembeddedchainer-table.md) can then join the remaining packages to the multiple-package installation without displaying a UAC prompt and requiring an administrator response for each package.</span></span>

<span data-ttu-id="6acef-108">Si una o varias de las funciones de la [tabla MsiEmbeddedChainer](msiembeddedchainer-table.md) solicitan un paquete sin firmar, se muestra otro aviso de UAC que requiere la interacción del administrador para cada paquete sin firmar.</span><span class="sxs-lookup"><span data-stu-id="6acef-108">If one or more of the functions in the [MsiEmbeddedChainer table](msiembeddedchainer-table.md) request an unsigned package, another UAC prompt requiring administrator interaction is displayed for each unsigned package.</span></span> <span data-ttu-id="6acef-109">Si el administrador acepta este aviso de UAC, la instalación de varios paquetes continúa.</span><span class="sxs-lookup"><span data-stu-id="6acef-109">If the administrator accepts this UAC prompt, the multi-package installation continues.</span></span> <span data-ttu-id="6acef-110">Una vez que un administrador ha proporcionado las credenciales para un paquete, no se mostrará ningún aviso de UAC para ese paquete durante la instalación de varios paquetes.</span><span class="sxs-lookup"><span data-stu-id="6acef-110">Once an administrator has provided credentials for a package, no UAC prompt will again be displayed for that package during this multi-package installation.</span></span> <span data-ttu-id="6acef-111">Si el administrador rechaza un aviso de UAC para un paquete, Windows Installer revierte la instalación de varios paquetes antes de que se confirme para instalar los paquetes que pertenecen al producto.</span><span class="sxs-lookup"><span data-stu-id="6acef-111">If the administrator rejects a UAC prompt for a package, the Windows installer rolls back the multi-package installation before it commits to install any packages belonging to the product.</span></span>

<span data-ttu-id="6acef-112">**[Windows Installer 4,0 o una versión anterior](not-supported-in-windows-installer-4-0.md):** No compatible.</span><span class="sxs-lookup"><span data-stu-id="6acef-112">**[Windows Installer 4.0 or earlier](not-supported-in-windows-installer-4-0.md):** Not supported.</span></span> <span data-ttu-id="6acef-113">Esta tabla está disponible a partir de Windows Installer 4,5.</span><span class="sxs-lookup"><span data-stu-id="6acef-113">This table is available beginning with Windows Installer 4.5.</span></span>

<span data-ttu-id="6acef-114">La tabla MsiPackageCertificate tiene las columnas siguientes:</span><span class="sxs-lookup"><span data-stu-id="6acef-114">The MsiPackageCertificate Table has the following columns:</span></span>



| <span data-ttu-id="6acef-115">Columna</span><span class="sxs-lookup"><span data-stu-id="6acef-115">Column</span></span>               | <span data-ttu-id="6acef-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="6acef-116">Type</span></span>                         | <span data-ttu-id="6acef-117">Clave</span><span class="sxs-lookup"><span data-stu-id="6acef-117">Key</span></span> | <span data-ttu-id="6acef-118">Nullable</span><span class="sxs-lookup"><span data-stu-id="6acef-118">Nullable</span></span> |
|----------------------|------------------------------|-----|----------|
| <span data-ttu-id="6acef-119">PackageCertificate</span><span class="sxs-lookup"><span data-stu-id="6acef-119">PackageCertificate</span></span>   | [<span data-ttu-id="6acef-120">Identificador</span><span class="sxs-lookup"><span data-stu-id="6acef-120">Identifier</span></span>](identifier.md) | <span data-ttu-id="6acef-121">Y</span><span class="sxs-lookup"><span data-stu-id="6acef-121">Y</span></span>   | <span data-ttu-id="6acef-122">N</span><span class="sxs-lookup"><span data-stu-id="6acef-122">N</span></span>        |
| <span data-ttu-id="6acef-123">DigitalCertificate\_</span><span class="sxs-lookup"><span data-stu-id="6acef-123">DigitalCertificate\_</span></span> | [<span data-ttu-id="6acef-124">Identificador</span><span class="sxs-lookup"><span data-stu-id="6acef-124">Identifier</span></span>](identifier.md) | <span data-ttu-id="6acef-125">N</span><span class="sxs-lookup"><span data-stu-id="6acef-125">N</span></span>   | <span data-ttu-id="6acef-126">N</span><span class="sxs-lookup"><span data-stu-id="6acef-126">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="6acef-127">Columnas</span><span class="sxs-lookup"><span data-stu-id="6acef-127">Columns</span></span>

<dl> <dt>

<span data-ttu-id="6acef-128"><span id="PackageCertificate"></span><span id="packagecertificate"></span><span id="PACKAGECERTIFICATE"></span>PackageCertificate</span><span class="sxs-lookup"><span data-stu-id="6acef-128"><span id="PackageCertificate"></span><span id="packagecertificate"></span><span id="PACKAGECERTIFICATE"></span>PackageCertificate</span></span>
</dt> <dd>

<span data-ttu-id="6acef-129">Identificador único de esta fila en la tabla MsiPackageCertificate.</span><span class="sxs-lookup"><span data-stu-id="6acef-129">The unique identifier for this row in the MsiPackageCertificate Table.</span></span>

</dd> <dt>

<span data-ttu-id="6acef-130"><span id="DigitalCertificate"></span><span id="digitalcertificate"></span><span id="DIGITALCERTIFICATE"></span>DigitalCertificate</span><span class="sxs-lookup"><span data-stu-id="6acef-130"><span id="DigitalCertificate"></span><span id="digitalcertificate"></span><span id="DIGITALCERTIFICATE"></span>DigitalCertificate</span></span>
</dt> <dd>

<span data-ttu-id="6acef-131">Una clave externa en la primera columna de la [tabla MsiDigitalCertificate](msidigitalcertificate-table.md).</span><span class="sxs-lookup"><span data-stu-id="6acef-131">An external key into the first column of the [MsiDigitalCertificate Table](msidigitalcertificate-table.md).</span></span> <span data-ttu-id="6acef-132">La fila indicada en la tabla MsiDigitalCertificate contiene la representación binaria del certificado del firmante.</span><span class="sxs-lookup"><span data-stu-id="6acef-132">The row indicated in the MsiDigitalCertificate Table contains the binary representation of the signer certificate.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="6acef-133">Validación</span><span class="sxs-lookup"><span data-stu-id="6acef-133">Validation</span></span>

<dl>

[<span data-ttu-id="6acef-134">ICE39</span><span class="sxs-lookup"><span data-stu-id="6acef-134">ICE39</span></span>](ice39.md)  
[<span data-ttu-id="6acef-135">ICE81</span><span class="sxs-lookup"><span data-stu-id="6acef-135">ICE81</span></span>](ice81.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="6acef-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6acef-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6acef-137">MsiEmbeddedChainer</span><span class="sxs-lookup"><span data-stu-id="6acef-137">MsiEmbeddedChainer</span></span>](msiembeddedchainer-table.md)
</dt> <dt>

[<span data-ttu-id="6acef-138">Tabla MsiDigitalCertificate</span><span class="sxs-lookup"><span data-stu-id="6acef-138">MsiDigitalCertificate Table</span></span>](msidigitalcertificate-table.md)
</dt> </dl>

 

 



