---
description: El método ConfigureProduct del objeto de instalador instala o desinstala un producto.
ms.assetid: 1215a03f-6c96-4416-881f-0071c1b3c5df
title: Installer.Configmétodo ureProduct
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ConfigureProduct
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 989855508215b2cd5d04bff7903628513314b9a5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105654018"
---
# <a name="installerconfigureproduct-method"></a><span data-ttu-id="f0fd8-103">Installer.Configmétodo ureProduct</span><span class="sxs-lookup"><span data-stu-id="f0fd8-103">Installer.ConfigureProduct method</span></span>

<span data-ttu-id="f0fd8-104">El método **ConfigureProduct** del objeto de [**instalador**](installer-object.md) instala o desinstala un producto.</span><span class="sxs-lookup"><span data-stu-id="f0fd8-104">The **ConfigureProduct** method of the [**Installer**](installer-object.md) object installs or uninstalls a product.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0fd8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f0fd8-105">Syntax</span></span>


```JScript
Installer.ConfigureProduct(
  Product,
  InstallLevel,
  InstallState
)
```



## <a name="parameters"></a><span data-ttu-id="f0fd8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f0fd8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0fd8-107">*Producto*</span><span class="sxs-lookup"><span data-stu-id="f0fd8-107">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="f0fd8-108">Especifica el código de producto del producto.</span><span class="sxs-lookup"><span data-stu-id="f0fd8-108">Specifies the product code of the product.</span></span>

</dd> <dt>

<span data-ttu-id="f0fd8-109">*InstallLevel*</span><span class="sxs-lookup"><span data-stu-id="f0fd8-109">*InstallLevel*</span></span> 
</dt> <dd>

<span data-ttu-id="f0fd8-110">Especifica la configuración de instalación predeterminada del producto.</span><span class="sxs-lookup"><span data-stu-id="f0fd8-110">Specifies the default installation configuration of the product.</span></span> <span data-ttu-id="f0fd8-111">Se omite el parámetro InstallLevel y se instalan todas las características si el parámetro InstallState está establecido en cualquier otro valor que msiInstallStateDefault.</span><span class="sxs-lookup"><span data-stu-id="f0fd8-111">The InstallLevel parameter is ignored and all features are installed if the InstallState parameter is set to any other value than msiInstallStateDefault.</span></span>

<span data-ttu-id="f0fd8-112">Este parámetro debe ser 0 (instalar con los niveles de características creados), 65535 (instalar todas las características) o un valor entre 0 y 65535 para instalar un subconjunto de características disponibles.</span><span class="sxs-lookup"><span data-stu-id="f0fd8-112">This parameter must be either 0 (install using authored feature levels), 65535 (install all features), or a value between 0 and 65535 to install a subset of available features.</span></span>

</dd> <dt>

<span data-ttu-id="f0fd8-113">*InstallState*</span><span class="sxs-lookup"><span data-stu-id="f0fd8-113">*InstallState*</span></span> 
</dt> <dd>

<span data-ttu-id="f0fd8-114">Especifica el estado de instalación de la característica.</span><span class="sxs-lookup"><span data-stu-id="f0fd8-114">Specifies the installation state for the feature.</span></span> <span data-ttu-id="f0fd8-115">Este parámetro debe ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="f0fd8-115">This parameter must be one of the following values.</span></span>



| <span data-ttu-id="f0fd8-116">Value</span><span class="sxs-lookup"><span data-stu-id="f0fd8-116">Value</span></span>                                                                                                                                                                                                                                        | <span data-ttu-id="f0fd8-117">Significado</span><span class="sxs-lookup"><span data-stu-id="f0fd8-117">Meaning</span></span>                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <span id="msiInstallStateAdvertised"></span><span id="msiinstallstateadvertised"></span><span id="MSIINSTALLSTATEADVERTISED"></span><dl> <span data-ttu-id="f0fd8-118"><dt>**msiInstallStateAdvertised**</dt></span><span class="sxs-lookup"><span data-stu-id="f0fd8-118"><dt>**msiInstallStateAdvertised**</dt></span></span> </dl> | <span data-ttu-id="f0fd8-119">La característica se anuncia</span><span class="sxs-lookup"><span data-stu-id="f0fd8-119">The feature is advertised</span></span><br/>                         |
| <span id="msiInstallStateLocal"></span><span id="msiinstallstatelocal"></span><span id="MSIINSTALLSTATELOCAL"></span><dl> <span data-ttu-id="f0fd8-120"><dt>**msiInstallStateLocal**</dt></span><span class="sxs-lookup"><span data-stu-id="f0fd8-120"><dt>**msiInstallStateLocal**</dt></span></span> </dl>                     | <span data-ttu-id="f0fd8-121">La característica se instala localmente.</span><span class="sxs-lookup"><span data-stu-id="f0fd8-121">The feature is installed locally.</span></span><br/>                 |
| <span id="msiInstallStateAbsent"></span><span id="msiinstallstateabsent"></span><span id="MSIINSTALLSTATEABSENT"></span><dl> <span data-ttu-id="f0fd8-122"><dt>**msiInstallStateAbsent**</dt></span><span class="sxs-lookup"><span data-stu-id="f0fd8-122"><dt>**msiInstallStateAbsent**</dt></span></span> </dl>                 | <span data-ttu-id="f0fd8-123">La característica está desinstalada.</span><span class="sxs-lookup"><span data-stu-id="f0fd8-123">The feature is uninstalled.</span></span><br/>                       |
| <span id="msiInstallStateSource"></span><span id="msiinstallstatesource"></span><span id="MSIINSTALLSTATESOURCE"></span><dl> <span data-ttu-id="f0fd8-124"><dt>**msiInstallStateSource**</dt></span><span class="sxs-lookup"><span data-stu-id="f0fd8-124"><dt>**msiInstallStateSource**</dt></span></span> </dl>                 | <span data-ttu-id="f0fd8-125">La característica se instala para ejecutarse desde el origen.</span><span class="sxs-lookup"><span data-stu-id="f0fd8-125">The feature is installed to run from source.</span></span><br/>      |
| <span id="msiInstallStateDefault"></span><span id="msiinstallstatedefault"></span><span id="MSIINSTALLSTATEDEFAULT"></span><dl> <span data-ttu-id="f0fd8-126"><dt>**msiInstallStateDefault**</dt></span><span class="sxs-lookup"><span data-stu-id="f0fd8-126"><dt>**msiInstallStateDefault**</dt></span></span> </dl>             | <span data-ttu-id="f0fd8-127">La característica se instala en su ubicación predeterminada.</span><span class="sxs-lookup"><span data-stu-id="f0fd8-127">The feature is installed to its default location.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0fd8-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f0fd8-128">Return value</span></span>

<span data-ttu-id="f0fd8-129">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="f0fd8-129">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0fd8-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f0fd8-130">Remarks</span></span>

<span data-ttu-id="f0fd8-131">El método **ConfigureProduct** muestra la interfaz de usuario mediante la configuración actual.</span><span class="sxs-lookup"><span data-stu-id="f0fd8-131">The **ConfigureProduct** method displays the user interface using current settings.</span></span> <span data-ttu-id="f0fd8-132">La configuración de la interfaz de usuario se puede cambiar modificando la [**propiedad elemento uilevel (objeto Installer)**](installer-uilevel.md) antes de llamar al método **ConfigureProduct** .</span><span class="sxs-lookup"><span data-stu-id="f0fd8-132">User interface settings can be changed by modifying the [**UILevel property (Installer object)**](installer-uilevel.md) before calling the **ConfigureProduct** method.</span></span>

<span data-ttu-id="f0fd8-133">Si el parámetro *InstallState* se establece en cualquier otro valor que no sea msiInstallStateDefault, el parámetro *InstallLevel* se omite y se instalan todas las características del producto.</span><span class="sxs-lookup"><span data-stu-id="f0fd8-133">If the *InstallState* parameter is set to any other value than msiInstallStateDefault, the *InstallLevel* parameter is ignored and all features of the product are installed.</span></span> <span data-ttu-id="f0fd8-134">Use el método [**ConfigureFeature**](installer-configurefeature.md) para controlar la instalación de características individuales cuando el parámetro *InstallState* no se establece en msiInstallStateDefault.</span><span class="sxs-lookup"><span data-stu-id="f0fd8-134">Use the [**ConfigureFeature**](installer-configurefeature.md) method to control the installation of individual features when the *InstallState* parameter is not set to msiInstallStateDefault.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0fd8-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0fd8-135">Requirements</span></span>



| <span data-ttu-id="f0fd8-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0fd8-136">Requirement</span></span> | <span data-ttu-id="f0fd8-137">Value</span><span class="sxs-lookup"><span data-stu-id="f0fd8-137">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0fd8-138">Versión</span><span class="sxs-lookup"><span data-stu-id="f0fd8-138">Version</span></span><br/> | <span data-ttu-id="f0fd8-139">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f0fd8-139">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="f0fd8-140">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f0fd8-140">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="f0fd8-141">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="f0fd8-141">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="f0fd8-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f0fd8-142">DLL</span></span><br/>     | <dl> <span data-ttu-id="f0fd8-143"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f0fd8-143"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="f0fd8-144">IID</span><span class="sxs-lookup"><span data-stu-id="f0fd8-144">IID</span></span><br/>     | <span data-ttu-id="f0fd8-145">IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="f0fd8-145">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="f0fd8-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="f0fd8-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0fd8-147">**MsiConfigureProduct**</span><span class="sxs-lookup"><span data-stu-id="f0fd8-147">**MsiConfigureProduct**</span></span>](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta)
</dt> <dt>

[<span data-ttu-id="f0fd8-148">Funciones de instalación y configuración</span><span class="sxs-lookup"><span data-stu-id="f0fd8-148">Installation and Configuration Functions</span></span>](installer-function-reference.md)
</dt> </dl>

 

 




