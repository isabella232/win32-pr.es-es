---
description: El método ProvideQualifiedComponent del objeto Installer devuelve la ruta de acceso completa del componente y realiza cualquier instalación necesaria. Si es necesario, este método solicita el origen e incrementa el recuento de uso de la característica.
ms.assetid: 4f9a5094-1556-4d86-8b51-c8c3ce1cbed4
title: Instalador. ProvideQualifiedComponent (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProvideQualifiedComponent
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 73c830610b49976e3625dd333c57f39e43d4be14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653711"
---
# <a name="installerprovidequalifiedcomponent-method"></a><span data-ttu-id="3eeb5-104">Instalador. ProvideQualifiedComponent (método)</span><span class="sxs-lookup"><span data-stu-id="3eeb5-104">Installer.ProvideQualifiedComponent method</span></span>

<span data-ttu-id="3eeb5-105">El método **ProvideQualifiedComponent** del objeto [**Installer**](installer-object.md) devuelve la ruta de acceso completa del componente y realiza cualquier instalación necesaria.</span><span class="sxs-lookup"><span data-stu-id="3eeb5-105">The **ProvideQualifiedComponent** method of the [**Installer**](installer-object.md) object returns the full component path and performs any necessary installation.</span></span> <span data-ttu-id="3eeb5-106">Si es necesario, este método solicita el origen e incrementa el recuento de uso de la característica.</span><span class="sxs-lookup"><span data-stu-id="3eeb5-106">If necessary, this method prompts for the source and increments the usage count for the feature.</span></span>

## <a name="syntax"></a><span data-ttu-id="3eeb5-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3eeb5-107">Syntax</span></span>


```JScript
Installer.ProvideQualifiedComponent(
  Category,
  Qualifier,
  InstallMode
)
```



## <a name="parameters"></a><span data-ttu-id="3eeb5-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3eeb5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3eeb5-109">*Categoría*</span><span class="sxs-lookup"><span data-stu-id="3eeb5-109">*Category*</span></span> 
</dt> <dd>

<span data-ttu-id="3eeb5-110">Especifica el identificador de componente para el componente solicitado.</span><span class="sxs-lookup"><span data-stu-id="3eeb5-110">Specifies the component ID for the requested component.</span></span> <span data-ttu-id="3eeb5-111">Es posible que este no sea el GUID del componente en sí, sino un servidor que proporcione la funcionalidad correcta, como en la columna ComponentId de la [tabla PublishComponent](publishcomponent-table.md).</span><span class="sxs-lookup"><span data-stu-id="3eeb5-111">This may not be the GUID for the component itself but rather a server that provides the correct functionality, as in the ComponentId column of the [PublishComponent table](publishcomponent-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="3eeb5-112">*Calificador*</span><span class="sxs-lookup"><span data-stu-id="3eeb5-112">*Qualifier*</span></span> 
</dt> <dd>

<span data-ttu-id="3eeb5-113">Especifica un calificador en una lista de componentes de publicidad (de la [tabla PublishComponent](publishcomponent-table.md)).</span><span class="sxs-lookup"><span data-stu-id="3eeb5-113">Specifies a qualifier into a list of advertising components (from [PublishComponent table](publishcomponent-table.md)).</span></span>

</dd> <dt>

<span data-ttu-id="3eeb5-114">*InstallMode*</span><span class="sxs-lookup"><span data-stu-id="3eeb5-114">*InstallMode*</span></span> 
</dt> <dd>

<span data-ttu-id="3eeb5-115">Define el modo de instalación.</span><span class="sxs-lookup"><span data-stu-id="3eeb5-115">Defines the installation mode.</span></span> <span data-ttu-id="3eeb5-116">Este parámetro puede ser uno de los valores que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="3eeb5-116">This parameter can be one of the values shown in the following table.</span></span>



| <span data-ttu-id="3eeb5-117">InstallMode</span><span class="sxs-lookup"><span data-stu-id="3eeb5-117">InstallMode</span></span>                                                                                                                                                                                                                                                                                                                                                         | <span data-ttu-id="3eeb5-118">Significado</span><span class="sxs-lookup"><span data-stu-id="3eeb5-118">Meaning</span></span>                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiInstallModeDefault"></span><span id="msiinstallmodedefault"></span><span id="MSIINSTALLMODEDEFAULT"></span><dl> <span data-ttu-id="3eeb5-119"><dt>**msiInstallModeDefault**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3eeb5-119"><dt>**msiInstallModeDefault**</dt> <dt>0</dt></span></span> </dl>                                                                                 | <span data-ttu-id="3eeb5-120">Proporciona el componente y realiza cualquier instalación necesaria.</span><span class="sxs-lookup"><span data-stu-id="3eeb5-120">Provides the component, performing any necessary installation.</span></span><br/>                                                                                                                                                           |
| <span id="msiInstallModeExisting"></span><span id="msiinstallmodeexisting"></span><span id="MSIINSTALLMODEEXISTING"></span><dl> <span data-ttu-id="3eeb5-121"><dt>**msiInstallModeExisting**</dt> <dt>: 1</dt></span><span class="sxs-lookup"><span data-stu-id="3eeb5-121"><dt>**msiInstallModeExisting**</dt> <dt>–1</dt></span></span> </dl>                                                                            | <span data-ttu-id="3eeb5-122">Proporciona el componente solo si existe la característica; de lo contrario, devuelve una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="3eeb5-122">Provides the component only if the feature exists; otherwise returns an empty string.</span></span> <span data-ttu-id="3eeb5-123">Este modo comprueba la existencia del archivo de clave del componente.</span><span class="sxs-lookup"><span data-stu-id="3eeb5-123">This mode verifies the existence of the component's key file.</span></span><br/>                                                                      |
| <span id="msiInstallModeNoDetection"></span><span id="msiinstallmodenodetection"></span><span id="MSIINSTALLMODENODETECTION"></span><dl> <span data-ttu-id="3eeb5-124"><dt>**msiInstallModeNoDetection**</dt> <dt>: 2</dt></span><span class="sxs-lookup"><span data-stu-id="3eeb5-124"><dt>**msiInstallModeNoDetection**</dt> <dt>–2</dt></span></span> </dl>                                                                | <span data-ttu-id="3eeb5-125">Proporciona el componente solo si existe la característica; de lo contrario, devuelve una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="3eeb5-125">Provides the component only if the feature exists; otherwise returns an empty string.</span></span> <span data-ttu-id="3eeb5-126">Este modo solo comprueba que el componente está registrado pero no comprueba la existencia del archivo de clave del componente.</span><span class="sxs-lookup"><span data-stu-id="3eeb5-126">This mode only checks that the component is registered but does not verify the existence of the component's key file.</span></span><br/>              |
| <span id="msiInstallModeNoSourceResolution"></span><span id="msiinstallmodenosourceresolution"></span><span id="MSIINSTALLMODENOSOURCERESOLUTION"></span><dl> <span data-ttu-id="3eeb5-127"><dt>**msiInstallModeNoSourceResolution**</dt> <dt>: 3</dt></span><span class="sxs-lookup"><span data-stu-id="3eeb5-127"><dt>**msiInstallModeNoSourceResolution**</dt> <dt>–3</dt></span></span> </dl>                                    | <span data-ttu-id="3eeb5-128">Proporciona la ruta de acceso al componente solo si la característica existe con un parámetro InstallState de *msiInstallStateLocal*.</span><span class="sxs-lookup"><span data-stu-id="3eeb5-128">Provides the component path only if the feature exists with an InstallState parameter of *msiInstallStateLocal*.</span></span> <span data-ttu-id="3eeb5-129">Comprueba el registro del componente, pero no comprueba la existencia del archivo de clave del componente.</span><span class="sxs-lookup"><span data-stu-id="3eeb5-129">This checks the component's registration but does not verify the existence of the component's key file.</span></span><br/> |
| <span id="combination_of_the_msiReinstallMode_flags"></span><span id="combination_of_the_msireinstallmode_flags"></span><span id="COMBINATION_OF_THE_MSIREINSTALLMODE_FLAGS"></span><dl> <span data-ttu-id="3eeb5-130"><dt>**combinación de las marcas msiReinstallMode**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="3eeb5-130"><dt>**combination of the msiReinstallMode flags**</dt> <dt> </dt></span></span> </dl> | <span data-ttu-id="3eeb5-131">Llama a [**ReinstallFeature**](installer-reinstallfeature.md) para volver a instalar la característica con este parámetro para el parámetro *ReinstallMode* y, a continuación, proporciona el componente.</span><span class="sxs-lookup"><span data-stu-id="3eeb5-131">Calls [**ReinstallFeature**](installer-reinstallfeature.md) to reinstall the feature using this parameter for the *ReinstallMode* parameter, and then provides the component.</span></span><br/>                                           |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3eeb5-132">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3eeb5-132">Return value</span></span>

<span data-ttu-id="3eeb5-133">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="3eeb5-133">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="3eeb5-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3eeb5-134">Requirements</span></span>



| <span data-ttu-id="3eeb5-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="3eeb5-135">Requirement</span></span> | <span data-ttu-id="3eeb5-136">Value</span><span class="sxs-lookup"><span data-stu-id="3eeb5-136">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3eeb5-137">Versión</span><span class="sxs-lookup"><span data-stu-id="3eeb5-137">Version</span></span><br/> | <span data-ttu-id="3eeb5-138">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3eeb5-138">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="3eeb5-139">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3eeb5-139">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="3eeb5-140">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="3eeb5-140">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="3eeb5-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3eeb5-141">DLL</span></span><br/>     | <dl> <span data-ttu-id="3eeb5-142"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3eeb5-142"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="3eeb5-143">IID</span><span class="sxs-lookup"><span data-stu-id="3eeb5-143">IID</span></span><br/>     | <span data-ttu-id="3eeb5-144">IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="3eeb5-144">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="3eeb5-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="3eeb5-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3eeb5-146">**MsiProvideQualifiedComponent**</span><span class="sxs-lookup"><span data-stu-id="3eeb5-146">**MsiProvideQualifiedComponent**</span></span>](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta)
</dt> </dl>

 

 




