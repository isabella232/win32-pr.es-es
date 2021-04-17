---
description: Para cada producto incluido en el paquete de revisión como válido para recibir la revisión, el método ApplyPatch del objeto de instalador invoca una instalación y establece la propiedad PATCH en la ruta de acceso del paquete patch.
ms.assetid: eee93b6d-f45b-40ae-8e17-cfe6f46b66f4
title: Instalador. ApplyPatch (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ApplyPatch
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: cc1b7509ddb4c61fa84a4547dcd47f2c7637b913
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653640"
---
# <a name="installerapplypatch-method"></a><span data-ttu-id="d6422-103">Instalador. ApplyPatch (método)</span><span class="sxs-lookup"><span data-stu-id="d6422-103">Installer.ApplyPatch method</span></span>

<span data-ttu-id="d6422-104">Para cada producto incluido en el paquete de revisión como válido para recibir la revisión, el método **ApplyPatch** del objeto de [**instalador**](installer-object.md) invoca una instalación y establece la propiedad [**patch**](patch.md) en la ruta de acceso del paquete patch.</span><span class="sxs-lookup"><span data-stu-id="d6422-104">For each product listed by the patch package as eligible to receive the patch, the **ApplyPatch** method of the [**Installer**](installer-object.md) object invokes an installation and sets the [**PATCH**](patch.md) property to the path of the patch package.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6422-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d6422-105">Syntax</span></span>


```JScript
Installer.ApplyPatch(
  PatchPackage,
  InstallPackage,
  InstallType,
  CommandLine
)
```



## <a name="parameters"></a><span data-ttu-id="d6422-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d6422-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6422-107">*PatchPackage*</span><span class="sxs-lookup"><span data-stu-id="d6422-107">*PatchPackage*</span></span> 
</dt> <dd>

<span data-ttu-id="d6422-108">Especifica una ruta de acceso al paquete de revisión.</span><span class="sxs-lookup"><span data-stu-id="d6422-108">Specifies a path to the patch package.</span></span>

</dd> <dt>

<span data-ttu-id="d6422-109">*InstallPackage*</span><span class="sxs-lookup"><span data-stu-id="d6422-109">*InstallPackage*</span></span> 
</dt> <dd>

<span data-ttu-id="d6422-110">Si *InstallType* está establecido en MsiInstallTypeNetworkImage, *InstallPackage* especifica la ruta de acceso al producto que se va a revisar.</span><span class="sxs-lookup"><span data-stu-id="d6422-110">If *InstallType* is set to msiInstallTypeNetworkImage, *InstallPackage* specifies the path to the product that is to be patched.</span></span> <span data-ttu-id="d6422-111">Si *InstallType* se establece en MsiInstallTypeDefault y *InstallPackage* se establece en 0, el instalador aplica la revisión a todos los productos válidos que se enumeran en el paquete de revisión.</span><span class="sxs-lookup"><span data-stu-id="d6422-111">If *InstallType* is set to msiInstallTypeDefault and *InstallPackage* is set to 0, the installer applies the patch to every eligible product listed in the patch package.</span></span>

<span data-ttu-id="d6422-112">Si *InstallType* es msiInstallTypeSingleInstance, el instalador aplica la revisión al producto especificado por *InstallPackage*.</span><span class="sxs-lookup"><span data-stu-id="d6422-112">If *InstallType* is msiInstallTypeSingleInstance, the installer applies the patch to the product specified by *InstallPackage*.</span></span> <span data-ttu-id="d6422-113">En este caso, se omiten otros productos válidos enumerados en el paquete de revisión y el parámetro *InstallPackage* contiene la cadena terminada en null que representa el código de producto de la instancia que se va a revisar.</span><span class="sxs-lookup"><span data-stu-id="d6422-113">In this case, other eligible products listed in the patch package are ignored and the *InstallPackage* parameter contains the null-terminated string representing the product code of the instance to patch.</span></span> <span data-ttu-id="d6422-114">Este tipo de instalación requiere la versión Windows Installer incluida con Windows Server 2003 o posterior, o Windows Installer XP SP1 o posterior.</span><span class="sxs-lookup"><span data-stu-id="d6422-114">This type of installation requires the Windows Installer version shipped with the Windows Server 2003 or later or Windows Installer XP SP1 or later.</span></span>

</dd> <dt>

<span data-ttu-id="d6422-115">*InstallType*</span><span class="sxs-lookup"><span data-stu-id="d6422-115">*InstallType*</span></span> 
</dt> <dd>

<span data-ttu-id="d6422-116">Este parámetro especifica el tipo de instalación que se va a revisar.</span><span class="sxs-lookup"><span data-stu-id="d6422-116">This parameter specifies the type of installation to patch.</span></span> <span data-ttu-id="d6422-117">El parámetro *InstallType* se omite si se omite *InstallPackage* .</span><span class="sxs-lookup"><span data-stu-id="d6422-117">The *InstallType* parameter is ignored if *InstallPackage* is omitted.</span></span>



| <span data-ttu-id="d6422-118">Value</span><span class="sxs-lookup"><span data-stu-id="d6422-118">Value</span></span>                                                                                                                                                                                                                                            | <span data-ttu-id="d6422-119">Significado</span><span class="sxs-lookup"><span data-stu-id="d6422-119">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiInstallTypeNetworkImage"></span><span id="msiinstalltypenetworkimage"></span><span id="MSIINSTALLTYPENETWORKIMAGE"></span><dl> <span data-ttu-id="d6422-120"><dt>**msiInstallTypeNetworkImage**</dt></span><span class="sxs-lookup"><span data-stu-id="d6422-120"><dt>**msiInstallTypeNetworkImage**</dt></span></span> </dl> | <span data-ttu-id="d6422-121">Indica una instalación administrativa.</span><span class="sxs-lookup"><span data-stu-id="d6422-121">Indicates a administrative installation.</span></span> <span data-ttu-id="d6422-122">En este caso, *InstallPackage* se debe establecer en una ruta de acceso del paquete.</span><span class="sxs-lookup"><span data-stu-id="d6422-122">In this case, *InstallPackage* must be set to a package path.</span></span> <span data-ttu-id="d6422-123">Un valor de 1 para msiInstallTypeNetworkImage especifica una instalación administrativa.</span><span class="sxs-lookup"><span data-stu-id="d6422-123">A value of 1 for msiInstallTypeNetworkImage specifies a administrative installation.</span></span><br/>                                                                                                                                                                                                                    |
| <span id="msiInstallTypeDefault"></span><span id="msiinstalltypedefault"></span><span id="MSIINSTALLTYPEDEFAULT"></span><dl> <span data-ttu-id="d6422-124"><dt>**msiInstallTypeDefault**</dt></span><span class="sxs-lookup"><span data-stu-id="d6422-124"><dt>**msiInstallTypeDefault**</dt></span></span> </dl>                     | <span data-ttu-id="d6422-125">Busca los productos en el sistema para aplicar revisiones.</span><span class="sxs-lookup"><span data-stu-id="d6422-125">Searches system for products to patch.</span></span> <span data-ttu-id="d6422-126">En este caso, *InstallPackage* debe ser una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="d6422-126">In this case, *InstallPackage* must be an empty string.</span></span><br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="msiInstallSingleInstance"></span><span id="msiinstallsingleinstance"></span><span id="MSIINSTALLSINGLEINSTANCE"></span><dl> <span data-ttu-id="d6422-127"><dt>**msiInstallSingleInstance**</dt></span><span class="sxs-lookup"><span data-stu-id="d6422-127"><dt>**msiInstallSingleInstance**</dt></span></span> </dl>         | <span data-ttu-id="d6422-128">Aplique una revisión al producto especificado por *InstallPackage*.</span><span class="sxs-lookup"><span data-stu-id="d6422-128">Patch the product specified by *InstallPackage*.</span></span> <span data-ttu-id="d6422-129">*InstallPackage* es el código de producto de la instancia que se va a revisar.</span><span class="sxs-lookup"><span data-stu-id="d6422-129">*InstallPackage* is the product code of the instance to patch.</span></span> <span data-ttu-id="d6422-130">Este tipo de instalación requiere la versión Windows Installer incluida con Windows Server 2003 o posterior, o Windows Installer XP SP1 o posterior.</span><span class="sxs-lookup"><span data-stu-id="d6422-130">This type of installation requires the Windows Installer version shipped with Windows Server 2003 or later or Windows Installer XP SP1 or later.</span></span> <span data-ttu-id="d6422-131">Para obtener más información, vea [instalar varias instancias de productos y revisiones](installing-multiple-instances-of-products-and-patches.md).</span><span class="sxs-lookup"><span data-stu-id="d6422-131">For more information see, [Installing Multiple Instances of Products and Patches](installing-multiple-instances-of-products-and-patches.md).</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d6422-132">*CommandLine*</span><span class="sxs-lookup"><span data-stu-id="d6422-132">*CommandLine*</span></span> 
</dt> <dd>

<span data-ttu-id="d6422-133">Especifica la configuración de propiedades que se establece en la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="d6422-133">Specifies property settings being set on the command line.</span></span> <span data-ttu-id="d6422-134">vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="d6422-134">See Remarks section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6422-135">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d6422-135">Return value</span></span>

<span data-ttu-id="d6422-136">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="d6422-136">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6422-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d6422-137">Remarks</span></span>

<span data-ttu-id="d6422-138">Dado que el delimitador de lista para las transformaciones, los orígenes y las revisiones es un punto y coma, este carácter no se debe utilizar para los nombres de archivo o las rutas de acceso.</span><span class="sxs-lookup"><span data-stu-id="d6422-138">Because the list delimiter for transforms, sources, and patches is a semicolon, this character should not be used for file names or paths.</span></span>

<span data-ttu-id="d6422-139">La propiedad [**REINSTALL**](reinstall.md) es necesaria cuando se aplica una [pequeña actualización](small-updates.md) o una revisión de [actualización secundaria](minor-upgrades.md) .</span><span class="sxs-lookup"><span data-stu-id="d6422-139">The [**REINSTALL**](reinstall.md) property is required when applying a [small update](small-updates.md) or [minor upgrade](minor-upgrades.md) patch.</span></span> <span data-ttu-id="d6422-140">Sin esta propiedad, la revisión se registra en el sistema pero no se pueden actualizar los archivos.</span><span class="sxs-lookup"><span data-stu-id="d6422-140">Without this property, the patch is registered on the system but cannot update files.</span></span>

<span data-ttu-id="d6422-141">**Windows Installer 2,0:** Debe establecer la propiedad [**REINSTALL**](reinstall.md) en la línea de comandos al aplicar una [pequeña actualización](small-updates.md) o una revisión de [actualización secundaria](minor-upgrades.md) .</span><span class="sxs-lookup"><span data-stu-id="d6422-141">**Windows Installer 2.0:** You must set the [**REINSTALL**](reinstall.md) property on the command line when applying a [small update](small-updates.md) or [minor upgrade](minor-upgrades.md) patch.</span></span> <span data-ttu-id="d6422-142">En el caso de las revisiones que no usan una [acción personalizada, escriba 51](custom-action-type-51.md) para establecer automáticamente las propiedades **REINSTALL** y [**REINSTALLMODE**](reinstallmode.md) , la propiedad **REINSTALL** debe establecerse explícitamente con el parámetro *commandLine* .</span><span class="sxs-lookup"><span data-stu-id="d6422-142">For patches that do not use a [Custom Action Type 51](custom-action-type-51.md) to automatically set the **REINSTALL** and [**REINSTALLMODE**](reinstallmode.md) properties, the **REINSTALL** property must be explicitly set with the *CommandLine* parameter.</span></span> <span data-ttu-id="d6422-143">Establezca la propiedad **REINSTALL (reinstalar** ) para enumerar las características afectadas por la revisión o use una configuración predeterminada práctica de "REINSTALL = ALL".</span><span class="sxs-lookup"><span data-stu-id="d6422-143">Set the **REINSTALL** property to list the features affected by the patch, or use a practical default setting of "REINSTALL=ALL".</span></span> <span data-ttu-id="d6422-144">El valor predeterminado de la propiedad **REINSTALLMODE** es "OMUs".</span><span class="sxs-lookup"><span data-stu-id="d6422-144">The default value of the **REINSTALLMODE** property is "omus".</span></span>

<span data-ttu-id="d6422-145">**Windows Installer 3,0 y versiones posteriores:** A partir de Windows Installer versión 3,0, el instalador configura la propiedad [**REINSTALL**](reinstall.md) y no es necesario establecerla en la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="d6422-145">**Windows Installer 3.0 and later:** Beginning with Windows Installer version 3.0, the [**REINSTALL**](reinstall.md) property is configured by the installer and does not need to be set on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6422-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6422-146">Requirements</span></span>



| <span data-ttu-id="d6422-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6422-147">Requirement</span></span> | <span data-ttu-id="d6422-148">Value</span><span class="sxs-lookup"><span data-stu-id="d6422-148">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6422-149">Versión</span><span class="sxs-lookup"><span data-stu-id="d6422-149">Version</span></span><br/> | <span data-ttu-id="d6422-150">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d6422-150">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="d6422-151">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d6422-151">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="d6422-152">Windows Installer 3,0 o posterior en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d6422-152">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span><br/> |
| <span data-ttu-id="d6422-153">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d6422-153">DLL</span></span><br/>     | <dl> <span data-ttu-id="d6422-154"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6422-154"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                    |
| <span data-ttu-id="d6422-155">IID</span><span class="sxs-lookup"><span data-stu-id="d6422-155">IID</span></span><br/>     | <span data-ttu-id="d6422-156">IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="d6422-156">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="d6422-157">Vea también</span><span class="sxs-lookup"><span data-stu-id="d6422-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6422-158">**MsiApplyPatch**</span><span class="sxs-lookup"><span data-stu-id="d6422-158">**MsiApplyPatch**</span></span>](/windows/desktop/api/Msi/nf-msi-msiapplypatcha)
</dt> <dt>

[<span data-ttu-id="d6422-159">Acerca de las propiedades</span><span class="sxs-lookup"><span data-stu-id="d6422-159">About Properties</span></span>](about-properties.md)
</dt> <dt>

[<span data-ttu-id="d6422-160">No se admite en Windows Installer 2,0 y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="d6422-160">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




