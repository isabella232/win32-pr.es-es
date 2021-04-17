---
description: El método ProvideComponent del objeto Installer devuelve la ruta de acceso completa del componente y realiza cualquier instalación necesaria.
ms.assetid: 2bf09515-6f65-4712-89c1-01c43c1ce27c
title: Instalador. ProvideComponent (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProvideComponent
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e383c532d496ed217bdb7743b8171d732d61b2d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653712"
---
# <a name="installerprovidecomponent-method"></a><span data-ttu-id="64713-103">Instalador. ProvideComponent (método)</span><span class="sxs-lookup"><span data-stu-id="64713-103">Installer.ProvideComponent method</span></span>

<span data-ttu-id="64713-104">El método **ProvideComponent** del objeto [**Installer**](installer-object.md) devuelve la ruta de acceso completa del componente y realiza cualquier instalación necesaria.</span><span class="sxs-lookup"><span data-stu-id="64713-104">The **ProvideComponent** method of the [**Installer**](installer-object.md) object returns the full component path and performs any necessary installation.</span></span> <span data-ttu-id="64713-105">Si es necesario, el método **ProvideComponent** del objeto de [**instalador**](installer-object.md) solicita el origen e incrementa el recuento de uso de la característica.</span><span class="sxs-lookup"><span data-stu-id="64713-105">If necessary, the **ProvideComponent** method of the [**Installer**](installer-object.md) object prompts for the source and increments the usage count for the feature.</span></span>

## <a name="syntax"></a><span data-ttu-id="64713-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="64713-106">Syntax</span></span>


```JScript
Installer.ProvideComponent(
  Product,
  Feature,
  Component,
  InstallMode
)
```



## <a name="parameters"></a><span data-ttu-id="64713-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="64713-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64713-108">*Producto*</span><span class="sxs-lookup"><span data-stu-id="64713-108">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="64713-109">Especifica el código de producto del producto.</span><span class="sxs-lookup"><span data-stu-id="64713-109">Specifies the product code of the product.</span></span>

</dd> <dt>

<span data-ttu-id="64713-110">*Característica*</span><span class="sxs-lookup"><span data-stu-id="64713-110">*Feature*</span></span> 
</dt> <dd>

<span data-ttu-id="64713-111">Especifica el identificador de la característica que contiene el componente.</span><span class="sxs-lookup"><span data-stu-id="64713-111">Specifies the feature ID of the feature containing the component.</span></span>

</dd> <dt>

<span data-ttu-id="64713-112">*Componente*</span><span class="sxs-lookup"><span data-stu-id="64713-112">*Component*</span></span> 
</dt> <dd>

<span data-ttu-id="64713-113">Especifica el código del componente.</span><span class="sxs-lookup"><span data-stu-id="64713-113">Specifies the component code.</span></span>

</dd> <dt>

<span data-ttu-id="64713-114">*InstallMode*</span><span class="sxs-lookup"><span data-stu-id="64713-114">*InstallMode*</span></span> 
</dt> <dd>

<span data-ttu-id="64713-115">Define el modo de instalación.</span><span class="sxs-lookup"><span data-stu-id="64713-115">Defines the installation mode.</span></span> <span data-ttu-id="64713-116">Este parámetro puede ser uno de los valores que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="64713-116">This parameter can be one of the values shown in the following table.</span></span>



| <span data-ttu-id="64713-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="64713-117">Name</span></span>                                                                                                                                                                                                                                                                                                                                                               | <span data-ttu-id="64713-118">Significado</span><span class="sxs-lookup"><span data-stu-id="64713-118">Meaning</span></span>                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiInstallModeDefault"></span><span id="msiinstallmodedefault"></span><span id="MSIINSTALLMODEDEFAULT"></span><dl> <span data-ttu-id="64713-119"><dt>**msiInstallModeDefault**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="64713-119"><dt>**msiInstallModeDefault**</dt> <dt>0</dt></span></span> </dl>                                                                                | <span data-ttu-id="64713-120">Proporciona la ruta de acceso del componente y realiza cualquier instalación, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="64713-120">Provides the component path, performing any installation, if necessary.</span></span><br/>                                                                                                                                                  |
| <span id="msiInstallModeExisting"></span><span id="msiinstallmodeexisting"></span><span id="MSIINSTALLMODEEXISTING"></span><dl> <span data-ttu-id="64713-121"><dt>**msiInstallModeExisting**</dt> <dt>: 1</dt></span><span class="sxs-lookup"><span data-stu-id="64713-121"><dt>**msiInstallModeExisting**</dt> <dt>–1</dt></span></span> </dl>                                                                           | <span data-ttu-id="64713-122">Proporciona la ruta de acceso al componente solo si existe la característica; de lo contrario, devuelve una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="64713-122">Provides the component path only if the feature exists; otherwise, returns an empty string.</span></span> <span data-ttu-id="64713-123">Este modo comprueba la existencia del archivo de clave del componente.</span><span class="sxs-lookup"><span data-stu-id="64713-123">This mode verifies the existence of the component's key file.</span></span><br/>                                                                |
| <span id="msiInstallModeNoDetection"></span><span id="msiinstallmodenodetection"></span><span id="MSIINSTALLMODENODETECTION"></span><dl> <span data-ttu-id="64713-124"><dt>**msiInstallModeNoDetection**</dt> <dt>: 2</dt></span><span class="sxs-lookup"><span data-stu-id="64713-124"><dt>**msiInstallModeNoDetection**</dt> <dt>–2</dt></span></span> </dl>                                                               | <span data-ttu-id="64713-125">Proporciona la ruta de acceso al componente solo si existe la característica.</span><span class="sxs-lookup"><span data-stu-id="64713-125">Provides the component path only if the feature exists.</span></span> <span data-ttu-id="64713-126">De lo contrario, devuelve una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="64713-126">Otherwise, returns an empty string.</span></span> <span data-ttu-id="64713-127">Este modo comprueba el registro del componente, pero no comprueba la existencia del archivo de clave del componente.</span><span class="sxs-lookup"><span data-stu-id="64713-127">This mode checks the component's registration but does not verify the existence of the component's key file.</span></span><br/>                 |
| <span id="msiInstallModeNoSourceResolution"></span><span id="msiinstallmodenosourceresolution"></span><span id="MSIINSTALLMODENOSOURCERESOLUTION"></span><dl> <span data-ttu-id="64713-128"><dt>**msiInstallModeNoSourceResolution**</dt> <dt>: 3</dt></span><span class="sxs-lookup"><span data-stu-id="64713-128"><dt>**msiInstallModeNoSourceResolution**</dt> <dt>–3</dt></span></span> </dl>                                   | <span data-ttu-id="64713-129">Proporciona la ruta de acceso al componente solo si la característica existe con un parámetro InstallState de *msiInstallStateLocal*.</span><span class="sxs-lookup"><span data-stu-id="64713-129">Provides the component path only if the feature exists with an InstallState parameter of *msiInstallStateLocal*.</span></span> <span data-ttu-id="64713-130">Comprueba el registro del componente, pero no comprueba la existencia del archivo de clave del componente.</span><span class="sxs-lookup"><span data-stu-id="64713-130">This checks the component's registration but does not verify the existence of the component's key file.</span></span><br/> |
| <span id="combination_of_the_msiReinstallMode_flags"></span><span id="combination_of_the_msireinstallmode_flags"></span><span id="COMBINATION_OF_THE_MSIREINSTALLMODE_FLAGS"></span><dl> <span data-ttu-id="64713-131"><dt>**combinación de las marcas msiReinstallMode**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="64713-131"><dt>**combination of the msiReinstallMode flags**</dt> <dt></dt></span></span> </dl> | <span data-ttu-id="64713-132">Llama a [**ReinstallFeature**](installer-reinstallfeature.md) para volver a instalar la característica con este parámetro para el parámetro *ReinstallMode* y, a continuación, proporciona el componente.</span><span class="sxs-lookup"><span data-stu-id="64713-132">Calls [**ReinstallFeature**](installer-reinstallfeature.md) to reinstall the feature using this parameter for the *ReinstallMode* parameter, and then provides the component.</span></span><br/>                                           |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64713-133">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="64713-133">Return value</span></span>

<span data-ttu-id="64713-134">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="64713-134">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="64713-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="64713-135">Remarks</span></span>

<span data-ttu-id="64713-136">El método **ProvideComponent** combina la funcionalidad de [**UseFeature**](installer-usefeature.md), [**ConfigureFeature**](installer-configurefeature.md)y [**ComponentPath**](installer-componentpath.md).</span><span class="sxs-lookup"><span data-stu-id="64713-136">The **ProvideComponent** method combines the functionality of [**UseFeature**](installer-usefeature.md), [**ConfigureFeature**](installer-configurefeature.md), and [**ComponentPath**](installer-componentpath.md).</span></span> <span data-ttu-id="64713-137">El método **ProvideComponent** simplifica la secuencia de llamada, pero también incrementa el recuento de uso y se debe usar con precaución para evitar recuentos de uso inexactos.</span><span class="sxs-lookup"><span data-stu-id="64713-137">The **ProvideComponent** method simplifies the calling sequence, but it also increments the usage count and should be used with caution to prevent inaccurate usage counts.</span></span> <span data-ttu-id="64713-138">El método **ProvideComponent** también proporciona menos flexibilidad que una serie de llamadas individuales a los métodos y propiedades previamente mencionados.</span><span class="sxs-lookup"><span data-stu-id="64713-138">The **ProvideComponent** method also provides less flexibility than a series of individual calls to the methods and properties previously mentioned.</span></span>

<span data-ttu-id="64713-139">Si la aplicación se recupera de una situación inesperada, es probable que la aplicación ya haya llamado [**UseFeature**](installer-usefeature.md) y aumentado el recuento de uso.</span><span class="sxs-lookup"><span data-stu-id="64713-139">If the application is recovering from an unexpected situation, the application has probably already called [**UseFeature**](installer-usefeature.md) and incremented the usage count.</span></span> <span data-ttu-id="64713-140">En este caso, la aplicación debe evitar incrementar el recuento de uso llamando al método [**ConfigureFeature**](installer-configurefeature.md) en lugar de al método **ProvideComponent** .</span><span class="sxs-lookup"><span data-stu-id="64713-140">In this case, the application should avoid incrementing the usage count by calling the [**ConfigureFeature**](installer-configurefeature.md) method instead of the **ProvideComponent** method.</span></span>

<span data-ttu-id="64713-141">La opción msiInstallModeExisting no se puede usar en combinación con marcas msiReinstallMode.</span><span class="sxs-lookup"><span data-stu-id="64713-141">The msiInstallModeExisting option cannot be used in combination with msiReinstallMode flags.</span></span>

## <a name="requirements"></a><span data-ttu-id="64713-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="64713-142">Requirements</span></span>



| <span data-ttu-id="64713-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="64713-143">Requirement</span></span> | <span data-ttu-id="64713-144">Value</span><span class="sxs-lookup"><span data-stu-id="64713-144">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64713-145">Versión</span><span class="sxs-lookup"><span data-stu-id="64713-145">Version</span></span><br/> | <span data-ttu-id="64713-146">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="64713-146">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="64713-147">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="64713-147">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="64713-148">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="64713-148">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="64713-149">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="64713-149">DLL</span></span><br/>     | <dl> <span data-ttu-id="64713-150"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="64713-150"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="64713-151">IID</span><span class="sxs-lookup"><span data-stu-id="64713-151">IID</span></span><br/>     | <span data-ttu-id="64713-152">IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="64713-152">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="64713-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="64713-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64713-154">**MsiProvideComponent**</span><span class="sxs-lookup"><span data-stu-id="64713-154">**MsiProvideComponent**</span></span>](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta)
</dt> </dl>

 

 




