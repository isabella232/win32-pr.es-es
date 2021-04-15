---
description: El método ConfigureFeature del objeto Installer configura el estado de instalación de una característica del producto.
ms.assetid: cc950951-3b43-4d86-9ff1-80aa2ccd11d5
title: Installer.Configmétodo ureFeature
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ConfigureFeature
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 737019f5c404beabef404751e617be975b946c04
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105654017"
---
# <a name="installerconfigurefeature-method"></a><span data-ttu-id="08902-103">Installer.Configmétodo ureFeature</span><span class="sxs-lookup"><span data-stu-id="08902-103">Installer.ConfigureFeature method</span></span>

<span data-ttu-id="08902-104">El método **ConfigureFeature** del objeto [**Installer**](installer-object.md) configura el estado de instalación de una característica del producto.</span><span class="sxs-lookup"><span data-stu-id="08902-104">The **ConfigureFeature** method of the [**Installer**](installer-object.md) object configures the installed state of a product feature.</span></span>

## <a name="syntax"></a><span data-ttu-id="08902-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="08902-105">Syntax</span></span>


```JScript
Installer.ConfigureFeature(
  Product,
  Feature,
  InstallState
)
```



## <a name="parameters"></a><span data-ttu-id="08902-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="08902-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08902-107">*Producto*</span><span class="sxs-lookup"><span data-stu-id="08902-107">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="08902-108">Especifica el código de producto del producto.</span><span class="sxs-lookup"><span data-stu-id="08902-108">Specifies the product code of the product.</span></span>

</dd> <dt>

<span data-ttu-id="08902-109">*Característica*</span><span class="sxs-lookup"><span data-stu-id="08902-109">*Feature*</span></span> 
</dt> <dd>

<span data-ttu-id="08902-110">Especifica el identificador de la característica que se va a configurar.</span><span class="sxs-lookup"><span data-stu-id="08902-110">Specifies the feature ID of the feature to be configured.</span></span>

</dd> <dt>

<span data-ttu-id="08902-111">*InstallState*</span><span class="sxs-lookup"><span data-stu-id="08902-111">*InstallState*</span></span> 
</dt> <dd>

<span data-ttu-id="08902-112">Especifica el estado de instalación de la característica.</span><span class="sxs-lookup"><span data-stu-id="08902-112">Specifies the installation state for the feature.</span></span> <span data-ttu-id="08902-113">Este parámetro debe ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="08902-113">This parameter must be one of the following values.</span></span>



| <span data-ttu-id="08902-114">Value</span><span class="sxs-lookup"><span data-stu-id="08902-114">Value</span></span>                                                                                                                                                                                                                                        | <span data-ttu-id="08902-115">Significado</span><span class="sxs-lookup"><span data-stu-id="08902-115">Meaning</span></span>                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <span id="msiInstallStateAdvertised"></span><span id="msiinstallstateadvertised"></span><span id="MSIINSTALLSTATEADVERTISED"></span><dl> <span data-ttu-id="08902-116"><dt>**msiInstallStateAdvertised**</dt></span><span class="sxs-lookup"><span data-stu-id="08902-116"><dt>**msiInstallStateAdvertised**</dt></span></span> </dl> | <span data-ttu-id="08902-117">La característica se anuncia</span><span class="sxs-lookup"><span data-stu-id="08902-117">The feature is advertised</span></span><br/>                         |
| <span id="msiInstallStateLocal"></span><span id="msiinstallstatelocal"></span><span id="MSIINSTALLSTATELOCAL"></span><dl> <span data-ttu-id="08902-118"><dt>**msiInstallStateLocal**</dt></span><span class="sxs-lookup"><span data-stu-id="08902-118"><dt>**msiInstallStateLocal**</dt></span></span> </dl>                     | <span data-ttu-id="08902-119">La característica se instala localmente.</span><span class="sxs-lookup"><span data-stu-id="08902-119">The feature is installed locally.</span></span><br/>                 |
| <span id="msiInstallStateAbsent"></span><span id="msiinstallstateabsent"></span><span id="MSIINSTALLSTATEABSENT"></span><dl> <span data-ttu-id="08902-120"><dt>**msiInstallStateAbsent**</dt></span><span class="sxs-lookup"><span data-stu-id="08902-120"><dt>**msiInstallStateAbsent**</dt></span></span> </dl>                 | <span data-ttu-id="08902-121">La característica está desinstalada.</span><span class="sxs-lookup"><span data-stu-id="08902-121">The feature is uninstalled.</span></span><br/>                       |
| <span id="msiInstallStateSource"></span><span id="msiinstallstatesource"></span><span id="MSIINSTALLSTATESOURCE"></span><dl> <span data-ttu-id="08902-122"><dt>**msiInstallStateSource**</dt></span><span class="sxs-lookup"><span data-stu-id="08902-122"><dt>**msiInstallStateSource**</dt></span></span> </dl>                 | <span data-ttu-id="08902-123">La característica se instala para ejecutarse desde el origen.</span><span class="sxs-lookup"><span data-stu-id="08902-123">The feature is installed to run from source.</span></span><br/>      |
| <span id="msiInstallStateDefault"></span><span id="msiinstallstatedefault"></span><span id="MSIINSTALLSTATEDEFAULT"></span><dl> <span data-ttu-id="08902-124"><dt>**msiInstallStateDefault**</dt></span><span class="sxs-lookup"><span data-stu-id="08902-124"><dt>**msiInstallStateDefault**</dt></span></span> </dl>             | <span data-ttu-id="08902-125">La característica se instala en su ubicación predeterminada.</span><span class="sxs-lookup"><span data-stu-id="08902-125">The feature is installed to its default location.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08902-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="08902-126">Return value</span></span>

<span data-ttu-id="08902-127">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="08902-127">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="08902-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08902-128">Requirements</span></span>



| <span data-ttu-id="08902-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="08902-129">Requirement</span></span> | <span data-ttu-id="08902-130">Value</span><span class="sxs-lookup"><span data-stu-id="08902-130">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08902-131">Versión</span><span class="sxs-lookup"><span data-stu-id="08902-131">Version</span></span><br/> | <span data-ttu-id="08902-132">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="08902-132">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="08902-133">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="08902-133">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="08902-134">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="08902-134">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="08902-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="08902-135">DLL</span></span><br/>     | <dl> <span data-ttu-id="08902-136"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08902-136"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="08902-137">IID</span><span class="sxs-lookup"><span data-stu-id="08902-137">IID</span></span><br/>     | <span data-ttu-id="08902-138">IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="08902-138">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="08902-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="08902-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08902-140">**MsiConfigureFeature**</span><span class="sxs-lookup"><span data-stu-id="08902-140">**MsiConfigureFeature**</span></span>](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea)
</dt> <dt>

[<span data-ttu-id="08902-141">Funciones de instalación y configuración</span><span class="sxs-lookup"><span data-stu-id="08902-141">Installation and Configuration Functions</span></span>](installer-function-reference.md)
</dt> </dl>

 

 




