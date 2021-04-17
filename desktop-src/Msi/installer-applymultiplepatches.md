---
description: El método ApplyMultiplePatches aplica una o más revisiones a los productos que son válidos para recibir la revisión. El método establece la propiedad PATCH.
ms.assetid: 40c40e2c-60ef-4492-a4ab-0bb6b874fe80
title: Instalador. ApplyMultiplePatches (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ApplyMultiplePatches
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: d96d96157f7b1d81617be6980804fb54a6e6659f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653641"
---
# <a name="installerapplymultiplepatches-method"></a><span data-ttu-id="f467f-104">Instalador. ApplyMultiplePatches (método)</span><span class="sxs-lookup"><span data-stu-id="f467f-104">Installer.ApplyMultiplePatches method</span></span>

<span data-ttu-id="f467f-105">El método **ApplyMultiplePatches** aplica una o más revisiones a los productos que son válidos para recibir la revisión.</span><span class="sxs-lookup"><span data-stu-id="f467f-105">The **ApplyMultiplePatches** method applies one or more patches to products that are eligible to receive the patch.</span></span> <span data-ttu-id="f467f-106">El método establece la propiedad [**patch**](patch.md) .</span><span class="sxs-lookup"><span data-stu-id="f467f-106">The method sets the [**PATCH**](patch.md) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="f467f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f467f-107">Syntax</span></span>


```JScript
Installer.ApplyMultiplePatches(
  PatchPackagesList,
  Product,
  szPropertiesList
)
```



## <a name="parameters"></a><span data-ttu-id="f467f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f467f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f467f-109">*PatchPackagesList*</span><span class="sxs-lookup"><span data-stu-id="f467f-109">*PatchPackagesList*</span></span> 
</dt> <dd>

<span data-ttu-id="f467f-110">Una cadena que contiene una lista delimitada por signos de punto y coma de las rutas de acceso a los archivos de revisión.</span><span class="sxs-lookup"><span data-stu-id="f467f-110">A string that contains a semicolon-delimited list of the paths to patch files.</span></span> <span data-ttu-id="f467f-111">Por ejemplo: "c: \\ sus \\ Descargar \\ caché \\ Office \\ SP1. MSP; c: \\ \\ descargar el \\ almacenamiento en caché de \\ Office \\ QFE1. MSP; c: \\ sus \\ Descargar \\ caché \\ Office \\ QFEn. MSP ""</span><span class="sxs-lookup"><span data-stu-id="f467f-111">For example: ""c:\\sus\\download\\cache\\Office\\sp1.msp; c:\\sus\\download\\cache\\Office\\QFE1.msp;c:\\sus\\download\\cache\\Office\\QFEn.msp""</span></span>

</dd> <dt>

<span data-ttu-id="f467f-112">*Producto*</span><span class="sxs-lookup"><span data-stu-id="f467f-112">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="f467f-113">Este parámetro proporciona el [**ProductCode**](productcode.md) del producto que se va a revisar.</span><span class="sxs-lookup"><span data-stu-id="f467f-113">This parameter provides the [**ProductCode**](productcode.md) of the product being patched.</span></span> <span data-ttu-id="f467f-114">Este parámetro es opcional.</span><span class="sxs-lookup"><span data-stu-id="f467f-114">This parameter is optional.</span></span> <span data-ttu-id="f467f-115">Cuando este parámetro es null, las revisiones se aplican a todos los productos que son válidos para recibir estas revisiones.</span><span class="sxs-lookup"><span data-stu-id="f467f-115">When this parameter is null, the patches are applied to all products that are eligible to receive these patches.</span></span>

</dd> <dt>

<span data-ttu-id="f467f-116">*szPropertiesList*</span><span class="sxs-lookup"><span data-stu-id="f467f-116">*szPropertiesList*</span></span> 
</dt> <dd>

<span data-ttu-id="f467f-117">Una cadena terminada en null que especifica los valores de propiedades de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="f467f-117">A null-terminated string that specifies command-line property settings.</span></span> <span data-ttu-id="f467f-118">Este parámetro es opcional.</span><span class="sxs-lookup"><span data-stu-id="f467f-118">This parameter is optional.</span></span> <span data-ttu-id="f467f-119">Vea [acerca de las propiedades](about-properties.md) y [establecer valores de propiedades públicas en la línea de comandos](setting-public-property-values-on-the-command-line.md).</span><span class="sxs-lookup"><span data-stu-id="f467f-119">See [About Properties](about-properties.md) and [Setting Public Property Values on the Command Line](setting-public-property-values-on-the-command-line.md).</span></span> <span data-ttu-id="f467f-120">Todas las propiedades son compartidas por todos los productos de destino.</span><span class="sxs-lookup"><span data-stu-id="f467f-120">These properties are shared by all target products.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f467f-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f467f-121">Return value</span></span>

<span data-ttu-id="f467f-122">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="f467f-122">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f467f-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f467f-123">Requirements</span></span>



| <span data-ttu-id="f467f-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f467f-124">Requirement</span></span> | <span data-ttu-id="f467f-125">Value</span><span class="sxs-lookup"><span data-stu-id="f467f-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f467f-126">Versión</span><span class="sxs-lookup"><span data-stu-id="f467f-126">Version</span></span><br/> | <span data-ttu-id="f467f-127">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f467f-127">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="f467f-128">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f467f-128">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="f467f-129">Windows Installer 3,0 o posterior en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f467f-129">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span><br/> |
| <span data-ttu-id="f467f-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f467f-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="f467f-131"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f467f-131"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                    |
| <span data-ttu-id="f467f-132">IID</span><span class="sxs-lookup"><span data-stu-id="f467f-132">IID</span></span><br/>     | <span data-ttu-id="f467f-133">IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="f467f-133">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="f467f-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="f467f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f467f-135">Acerca de las propiedades</span><span class="sxs-lookup"><span data-stu-id="f467f-135">About Properties</span></span>](about-properties.md)
</dt> <dt>

[<span data-ttu-id="f467f-136">**ProductCode**</span><span class="sxs-lookup"><span data-stu-id="f467f-136">**ProductCode**</span></span>](productcode.md)
</dt> <dt>

[<span data-ttu-id="f467f-137">**DISTRIBUCIÓN**</span><span class="sxs-lookup"><span data-stu-id="f467f-137">**PATCH**</span></span>](patch.md)
</dt> <dt>

[<span data-ttu-id="f467f-138">Establecer valores de propiedades públicas en la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="f467f-138">Setting Public Property Values on the Command Line</span></span>](setting-public-property-values-on-the-command-line.md)
</dt> <dt>

[<span data-ttu-id="f467f-139">**MsiApplyMultiplePatches**</span><span class="sxs-lookup"><span data-stu-id="f467f-139">**MsiApplyMultiplePatches**</span></span>](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa)
</dt> <dt>

[<span data-ttu-id="f467f-140">No se admite en Windows Installer 2,0 y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="f467f-140">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




