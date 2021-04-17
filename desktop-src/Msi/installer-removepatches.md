---
description: El método RemovePatches quita una o más revisiones de los productos que puedan recibir la revisión. El método RemovePatches llama a MsiRemovePatches.
ms.assetid: 09c6ad3a-9f5e-4f9a-82c8-be7e411efd60
title: Instalador. RemovePatches (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.RemovePatches
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 2130ae2958f03eb16b5145e5eb61e42f869ad775
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653708"
---
# <a name="installerremovepatches-method"></a><span data-ttu-id="b86eb-104">Instalador. RemovePatches (método)</span><span class="sxs-lookup"><span data-stu-id="b86eb-104">Installer.RemovePatches method</span></span>

<span data-ttu-id="b86eb-105">El método **RemovePatches** quita una o más revisiones de los productos que puedan recibir la revisión.</span><span class="sxs-lookup"><span data-stu-id="b86eb-105">The **RemovePatches** method removes one or more patches to products eligible to receive the patch.</span></span> <span data-ttu-id="b86eb-106">El método **RemovePatches** llama a [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa).</span><span class="sxs-lookup"><span data-stu-id="b86eb-106">The **RemovePatches** method calls [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa).</span></span>

## <a name="syntax"></a><span data-ttu-id="b86eb-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b86eb-107">Syntax</span></span>


```JScript
Installer.RemovePatches(
  PatchList,
  ProductCode,
  UninstallType,
  PropertyList
)
```



## <a name="parameters"></a><span data-ttu-id="b86eb-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b86eb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b86eb-109">*PatchList*</span><span class="sxs-lookup"><span data-stu-id="b86eb-109">*PatchList*</span></span> 
</dt> <dd>

<span data-ttu-id="b86eb-110">Una cadena que contiene una lista delimitada por punto y coma de las revisiones que se van a quitar.</span><span class="sxs-lookup"><span data-stu-id="b86eb-110">A string that contains a semicolon delimited list of patches to remove.</span></span> <span data-ttu-id="b86eb-111">Cada revisión se puede representar mediante la ruta de acceso completa al paquete de revisión o mediante el GUID de la revisión.</span><span class="sxs-lookup"><span data-stu-id="b86eb-111">Each patch can be represented by either the full path to the patch package or by patch GUID.</span></span> <span data-ttu-id="b86eb-112">Este parámetro es necesario.</span><span class="sxs-lookup"><span data-stu-id="b86eb-112">This parameter is required.</span></span>

</dd> <dt>

<span data-ttu-id="b86eb-113">*ProductCode*</span><span class="sxs-lookup"><span data-stu-id="b86eb-113">*ProductCode*</span></span> 
</dt> <dd>

<span data-ttu-id="b86eb-114">Cadena con el GUID del producto del que se van a quitar las revisiones.</span><span class="sxs-lookup"><span data-stu-id="b86eb-114">A string with the GUID of the product from which the patches are to be removed.</span></span> <span data-ttu-id="b86eb-115">Este parámetro es necesario.</span><span class="sxs-lookup"><span data-stu-id="b86eb-115">This parameter is required.</span></span>

</dd> <dt>

<span data-ttu-id="b86eb-116">*UninstallType*</span><span class="sxs-lookup"><span data-stu-id="b86eb-116">*UninstallType*</span></span> 
</dt> <dd>

<span data-ttu-id="b86eb-117">Valor entero que especifica el tipo de eliminación de la revisión.</span><span class="sxs-lookup"><span data-stu-id="b86eb-117">An integer value that specifies the type of patch removal.</span></span> <span data-ttu-id="b86eb-118">Este parámetro debe ser **msiInstallTypeSingleInstance**.</span><span class="sxs-lookup"><span data-stu-id="b86eb-118">This parameter must be **msiInstallTypeSingleInstance**.</span></span>

</dd> <dt>

<span data-ttu-id="b86eb-119">*PropertyList*</span><span class="sxs-lookup"><span data-stu-id="b86eb-119">*PropertyList*</span></span> 
</dt> <dd>

<span data-ttu-id="b86eb-120">Cadena que especifica los pares propiedad = valor que se van a incluir.</span><span class="sxs-lookup"><span data-stu-id="b86eb-120">A string that specifies the Property=Value pairs to include.</span></span> <span data-ttu-id="b86eb-121">Este parámetro es opcional.</span><span class="sxs-lookup"><span data-stu-id="b86eb-121">This parameter is optional.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b86eb-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b86eb-122">Return value</span></span>

<span data-ttu-id="b86eb-123">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="b86eb-123">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b86eb-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b86eb-124">Remarks</span></span>

<span data-ttu-id="b86eb-125">Consulte [desinstalación de revisiones](uninstalling-patches.md) para obtener un ejemplo que muestra cómo una aplicación puede quitar una revisión de todos los productos que están disponibles para el usuario.</span><span class="sxs-lookup"><span data-stu-id="b86eb-125">See [Uninstalling Patches](uninstalling-patches.md) for an example that demonstrates how an application can remove a patch from all products that are available to the user.</span></span>

## <a name="requirements"></a><span data-ttu-id="b86eb-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b86eb-126">Requirements</span></span>



| <span data-ttu-id="b86eb-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="b86eb-127">Requirement</span></span> | <span data-ttu-id="b86eb-128">Value</span><span class="sxs-lookup"><span data-stu-id="b86eb-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b86eb-129">Versión</span><span class="sxs-lookup"><span data-stu-id="b86eb-129">Version</span></span><br/> | <span data-ttu-id="b86eb-130">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b86eb-130">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="b86eb-131">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b86eb-131">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="b86eb-132">Windows Installer 3,0 o posterior en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b86eb-132">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span><br/> |
| <span data-ttu-id="b86eb-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b86eb-133">DLL</span></span><br/>     | <dl> <span data-ttu-id="b86eb-134"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b86eb-134"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                    |
| <span data-ttu-id="b86eb-135">IID</span><span class="sxs-lookup"><span data-stu-id="b86eb-135">IID</span></span><br/>     | <span data-ttu-id="b86eb-136">IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="b86eb-136">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="b86eb-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="b86eb-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b86eb-138">**ProductCode**</span><span class="sxs-lookup"><span data-stu-id="b86eb-138">**ProductCode**</span></span>](productcode.md)
</dt> <dt>

[<span data-ttu-id="b86eb-139">**MsiRemovePatches**</span><span class="sxs-lookup"><span data-stu-id="b86eb-139">**MsiRemovePatches**</span></span>](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
</dt> <dt>

[<span data-ttu-id="b86eb-140">Desinstalación de revisiones</span><span class="sxs-lookup"><span data-stu-id="b86eb-140">Uninstalling Patches</span></span>](uninstalling-patches.md)
</dt> <dt>

[<span data-ttu-id="b86eb-141">No se admite en Windows Installer 2,0 y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="b86eb-141">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




