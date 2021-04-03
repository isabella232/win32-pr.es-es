---
description: Identifica los posibles certificados de firmante utilizados para firmar digitalmente las revisiones.
ms.assetid: 8f76c27d-92f1-4de7-a69c-fba877e0325d
title: Tabla MsiPatchCertificate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01648e792931fd856a1231a5d876c7db843479df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082778"
---
# <a name="msipatchcertificate-table"></a><span data-ttu-id="e9ed1-103">Tabla MsiPatchCertificate</span><span class="sxs-lookup"><span data-stu-id="e9ed1-103">MsiPatchCertificate Table</span></span>

<span data-ttu-id="e9ed1-104">La tabla MsiPatchCertificate identifica los posibles certificados de firma que se usan para firmar digitalmente las revisiones.</span><span class="sxs-lookup"><span data-stu-id="e9ed1-104">The MsiPatchCertificate Table identifies the possible signer certificates used to digitally sign patches.</span></span> <span data-ttu-id="e9ed1-105">La tabla MsiPatchCertificate contiene la información necesaria para habilitar la aplicación de [revisiones del control de cuentas de usuario (UAC)](user-account-control--uac--patching.md) para una aplicación.</span><span class="sxs-lookup"><span data-stu-id="e9ed1-105">The MsiPatchCertificate Table contains the information that is needed to enable [User Account Control (UAC) Patching](user-account-control--uac--patching.md) for an application.</span></span>

<span data-ttu-id="e9ed1-106">La tabla MsiPatchCertificate tiene las columnas siguientes:</span><span class="sxs-lookup"><span data-stu-id="e9ed1-106">The MsiPatchCertificate Table has the following columns:</span></span>



| <span data-ttu-id="e9ed1-107">Columna</span><span class="sxs-lookup"><span data-stu-id="e9ed1-107">Column</span></span>               | <span data-ttu-id="e9ed1-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="e9ed1-108">Type</span></span>                         | <span data-ttu-id="e9ed1-109">Clave</span><span class="sxs-lookup"><span data-stu-id="e9ed1-109">Key</span></span> | <span data-ttu-id="e9ed1-110">Nullable</span><span class="sxs-lookup"><span data-stu-id="e9ed1-110">Nullable</span></span> |
|----------------------|------------------------------|-----|----------|
| <span data-ttu-id="e9ed1-111">PatchCertificate</span><span class="sxs-lookup"><span data-stu-id="e9ed1-111">PatchCertificate</span></span>     | [<span data-ttu-id="e9ed1-112">Identificador</span><span class="sxs-lookup"><span data-stu-id="e9ed1-112">Identifier</span></span>](identifier.md) | <span data-ttu-id="e9ed1-113">Y</span><span class="sxs-lookup"><span data-stu-id="e9ed1-113">Y</span></span>   | <span data-ttu-id="e9ed1-114">N</span><span class="sxs-lookup"><span data-stu-id="e9ed1-114">N</span></span>        |
| <span data-ttu-id="e9ed1-115">DigitalCertificate\_</span><span class="sxs-lookup"><span data-stu-id="e9ed1-115">DigitalCertificate\_</span></span> | [<span data-ttu-id="e9ed1-116">Identificador</span><span class="sxs-lookup"><span data-stu-id="e9ed1-116">Identifier</span></span>](identifier.md) | <span data-ttu-id="e9ed1-117">N</span><span class="sxs-lookup"><span data-stu-id="e9ed1-117">N</span></span>   | <span data-ttu-id="e9ed1-118">N</span><span class="sxs-lookup"><span data-stu-id="e9ed1-118">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="e9ed1-119">Columnas</span><span class="sxs-lookup"><span data-stu-id="e9ed1-119">Columns</span></span>

<dl> <dt>

<span data-ttu-id="e9ed1-120"><span id="PatchCertificate"></span><span id="patchcertificate"></span><span id="PATCHCERTIFICATE"></span>PatchCertificate</span><span class="sxs-lookup"><span data-stu-id="e9ed1-120"><span id="PatchCertificate"></span><span id="patchcertificate"></span><span id="PATCHCERTIFICATE"></span>PatchCertificate</span></span>
</dt> <dd>

<span data-ttu-id="e9ed1-121">Identificador único de esta fila en la tabla MsiPatchCertificate.</span><span class="sxs-lookup"><span data-stu-id="e9ed1-121">The unique identifier for this row in the MsiPatchCertificate Table.</span></span>

</dd> <dt>

<span data-ttu-id="e9ed1-122"><span id="DigitalCertificate"></span><span id="digitalcertificate"></span><span id="DIGITALCERTIFICATE"></span>DigitalCertificate</span><span class="sxs-lookup"><span data-stu-id="e9ed1-122"><span id="DigitalCertificate"></span><span id="digitalcertificate"></span><span id="DIGITALCERTIFICATE"></span>DigitalCertificate</span></span>
</dt> <dd>

<span data-ttu-id="e9ed1-123">Una clave externa en la primera columna de la [tabla MsiDigitalCertificate](msidigitalcertificate-table.md).</span><span class="sxs-lookup"><span data-stu-id="e9ed1-123">An external key into the first column of the [MsiDigitalCertificate Table](msidigitalcertificate-table.md).</span></span> <span data-ttu-id="e9ed1-124">La fila indicada en la tabla MsiDigitalCertificate contiene la representación binaria del certificado del firmante.</span><span class="sxs-lookup"><span data-stu-id="e9ed1-124">The row indicated in the MsiDigitalCertificate Table contains the binary representation of the signer certificate.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e9ed1-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e9ed1-125">Remarks</span></span>

<span data-ttu-id="e9ed1-126">Las revisiones siempre se evalúan con respecto a la tabla MsiPatchCertificate que está actualizada en el momento en que se aplica la revisión.</span><span class="sxs-lookup"><span data-stu-id="e9ed1-126">Patches are always evaluated against the MsiPatchCertificate Table that is current at the time the patch is applied.</span></span> <span data-ttu-id="e9ed1-127">Una revisión puede modificar la tabla MsiPatchCertificate agregando o quitando entradas.</span><span class="sxs-lookup"><span data-stu-id="e9ed1-127">A patch can modify the MsiPatchCertificate Table by adding or removing entries.</span></span> <span data-ttu-id="e9ed1-128">Esto permite que una revisión modifique la evaluación de revisiones futuras que se aplican posteriormente en la secuencia de aplicación de revisiones.</span><span class="sxs-lookup"><span data-stu-id="e9ed1-128">This enables a patch to modify the evaluation of future patches that are applied later in the patching sequence.</span></span> <span data-ttu-id="e9ed1-129">Puede haber varios certificados en la tabla y la revisión debe coincidir con al menos un certificado que se va a aplicar.</span><span class="sxs-lookup"><span data-stu-id="e9ed1-129">Multiple certificates can exist in the table, and the patch must match at least one certificate to be applied.</span></span>

## <a name="validation"></a><span data-ttu-id="e9ed1-130">Validación</span><span class="sxs-lookup"><span data-stu-id="e9ed1-130">Validation</span></span>

<dl>

[<span data-ttu-id="e9ed1-131">ICE03</span><span class="sxs-lookup"><span data-stu-id="e9ed1-131">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="e9ed1-132">ICE06</span><span class="sxs-lookup"><span data-stu-id="e9ed1-132">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="e9ed1-133">ICE32</span><span class="sxs-lookup"><span data-stu-id="e9ed1-133">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="e9ed1-134">ICE81</span><span class="sxs-lookup"><span data-stu-id="e9ed1-134">ICE81</span></span>](ice81.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="e9ed1-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e9ed1-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9ed1-136">DisableLUAPatching</span><span class="sxs-lookup"><span data-stu-id="e9ed1-136">DisableLUAPatching</span></span>](disableluapatching.md)
</dt> <dt>

[<span data-ttu-id="e9ed1-137">Revisión de control de cuentas de usuario (UAC)</span><span class="sxs-lookup"><span data-stu-id="e9ed1-137">User Account Control (UAC) Patching</span></span>](user-account-control--uac--patching.md)
</dt> <dt>

[<span data-ttu-id="e9ed1-138">**MSIDISABLELUAPATCHING**</span><span class="sxs-lookup"><span data-stu-id="e9ed1-138">**MSIDISABLELUAPATCHING**</span></span>](msidisableluapatching.md)
</dt> <dt>

[<span data-ttu-id="e9ed1-139">Firmas digitales y Windows Installer</span><span class="sxs-lookup"><span data-stu-id="e9ed1-139">Digital Signatures and Windows Installer</span></span>](digital-signatures-and-windows-installer.md)
</dt> <dt>

[<span data-ttu-id="e9ed1-140">No se admite en Windows Installer 2,0 y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="e9ed1-140">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



