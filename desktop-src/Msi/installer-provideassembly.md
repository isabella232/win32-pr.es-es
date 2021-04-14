---
description: El método ProvideAssembly del objeto Installer devuelve la ruta de acceso instalada de un ensamblado.
ms.assetid: c99b1934-3834-478b-ab1d-7e7583dba779
title: Instalador::P método rovideAssembly
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProvideAssembly
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f81c9ab9b43b814307242cc828326b2b7e7d79fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653895"
---
# <a name="installerprovideassembly-method"></a><span data-ttu-id="7d273-103">Instalador::P método rovideAssembly</span><span class="sxs-lookup"><span data-stu-id="7d273-103">Installer::ProvideAssembly method</span></span>

<span data-ttu-id="7d273-104">El método **ProvideAssembly** del objeto [**Installer**](installer-object.md) devuelve la ruta de acceso instalada de un ensamblado.</span><span class="sxs-lookup"><span data-stu-id="7d273-104">The **ProvideAssembly** method of the [**Installer**](installer-object.md) object returns the installed path of an assembly.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d273-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7d273-105">Syntax</span></span>


```JScript
retVal = .ProvideAssembly(
  assembly,
  appContext,
  installMode,
  assemblyInfo
)
```



## <a name="parameters"></a><span data-ttu-id="7d273-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7d273-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d273-107">*assembl*</span><span class="sxs-lookup"><span data-stu-id="7d273-107">*assembly*</span></span> 
</dt> <dd>

<span data-ttu-id="7d273-108">Nombre seguro del ensamblado instalado que se va a consultar.</span><span class="sxs-lookup"><span data-stu-id="7d273-108">The strong name of installed assembly that is to be queried.</span></span>

</dd> <dt>

<span data-ttu-id="7d273-109">*appContext*</span><span class="sxs-lookup"><span data-stu-id="7d273-109">*appContext*</span></span> 
</dt> <dd>

<span data-ttu-id="7d273-110">Establezca en null para los ensamblados globales.</span><span class="sxs-lookup"><span data-stu-id="7d273-110">Set to null for global assemblies.</span></span> <span data-ttu-id="7d273-111">Para los ensamblados privados, establezca *appContext* en la ruta de acceso completa del archivo de configuración de la aplicación o en la ruta de acceso completa del archivo ejecutable de la aplicación en la que se ha hecho privado el ensamblado.</span><span class="sxs-lookup"><span data-stu-id="7d273-111">For private assemblies, set *appContext* to the full path of the application configuration file or to the full path of the executable file of the application to which the assembly has been made private.</span></span>

</dd> <dt>

<span data-ttu-id="7d273-112">*installMode*</span><span class="sxs-lookup"><span data-stu-id="7d273-112">*installMode*</span></span> 
</dt> <dd>

<span data-ttu-id="7d273-113">Define el modo de instalación.</span><span class="sxs-lookup"><span data-stu-id="7d273-113">Defines the installation mode.</span></span> <span data-ttu-id="7d273-114">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="7d273-114">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="7d273-115">Valor</span><span class="sxs-lookup"><span data-stu-id="7d273-115">Value</span></span>                                                                                                                                                                                                                                                                                                                                                                              | <span data-ttu-id="7d273-116">Significado</span><span class="sxs-lookup"><span data-stu-id="7d273-116">Meaning</span></span>                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiInstallModeDefault"></span><span id="msiinstallmodedefault"></span><span id="MSIINSTALLMODEDEFAULT"></span><dl> <span data-ttu-id="7d273-117"><dt>**msiInstallModeDefault**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7d273-117"><dt>**msiInstallModeDefault**</dt> <dt>0</dt></span></span> </dl>                                                                                                | <span data-ttu-id="7d273-118">Proporcione el componente y realice cualquier instalación necesaria para proporcionar el componente.</span><span class="sxs-lookup"><span data-stu-id="7d273-118">Provide the component and perform any installation necessary to provide the component.</span></span> <br/>                                                                                        |
| <span id="msiInstallModeExisting"></span><span id="msiinstallmodeexisting"></span><span id="MSIINSTALLMODEEXISTING"></span><dl> <span data-ttu-id="7d273-119"><dt>**msiInstallModeExisting**</dt> <dt>-1</dt></span><span class="sxs-lookup"><span data-stu-id="7d273-119"><dt>**msiInstallModeExisting**</dt> <dt>-1</dt></span></span> </dl>                                                                                           | <span data-ttu-id="7d273-120">Proporcione el componente solo si existe la característica.</span><span class="sxs-lookup"><span data-stu-id="7d273-120">Provide the component only if the feature exists.</span></span> <span data-ttu-id="7d273-121">Esta opción comprueba que el ensamblado existe.</span><span class="sxs-lookup"><span data-stu-id="7d273-121">This option will verify that the assembly exists.</span></span><br/>                                                                            |
| <span id="msiInstallModeNoDetection"></span><span id="msiinstallmodenodetection"></span><span id="MSIINSTALLMODENODETECTION"></span><dl> <span data-ttu-id="7d273-122"><dt>**msiInstallModeNoDetection**</dt> <dt>-2</dt></span><span class="sxs-lookup"><span data-stu-id="7d273-122"><dt>**msiInstallModeNoDetection**</dt> <dt>-2</dt></span></span> </dl>                                                                               | <span data-ttu-id="7d273-123">Proporcione el componente solo si existe la característica.</span><span class="sxs-lookup"><span data-stu-id="7d273-123">Provide the component only if the feature exists.</span></span> <span data-ttu-id="7d273-124">Esta opción no comprueba si el ensamblado existe.</span><span class="sxs-lookup"><span data-stu-id="7d273-124">This option does not verify that the assembly exists.</span></span><br/>                                                                        |
| <span id="msiInstallModeNoSourceResolution"></span><span id="msiinstallmodenosourceresolution"></span><span id="MSIINSTALLMODENOSOURCERESOLUTION"></span><dl> <span data-ttu-id="7d273-125"><dt>**msiInstallModeNoSourceResolution**</dt> <dt>-3</dt></span><span class="sxs-lookup"><span data-stu-id="7d273-125"><dt>**msiInstallModeNoSourceResolution**</dt> <dt>-3</dt></span></span> </dl>                                                   | <span data-ttu-id="7d273-126">Proporciona el ensamblado solo si el ensamblado está instalado local.</span><span class="sxs-lookup"><span data-stu-id="7d273-126">Provides the assembly only if the assembly is installed local.</span></span><br/>                                                                                                                 |
| <span id="Combination_of_the_flags_used_by_ReinstallFeature"></span><span id="combination_of_the_flags_used_by_reinstallfeature"></span><span id="COMBINATION_OF_THE_FLAGS_USED_BY_REINSTALLFEATURE"></span><dl> <span data-ttu-id="7d273-127"><dt>**Combinación de las marcas usadas por [ **ReinstallFeature**](installer-reinstallfeature.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="7d273-127"><dt>**Combination of the flags used by [**ReinstallFeature**](installer-reinstallfeature.md)**</dt></span></span> </dl> | <span data-ttu-id="7d273-128">Llama al método [**ReinstallFeature**](installer-reinstallfeature.md) para volver a instalar la característica mediante este parámetro para *ReinstallMode* y, a continuación, devuelve la ruta de acceso del ensamblado.</span><span class="sxs-lookup"><span data-stu-id="7d273-128">Calls the [**ReinstallFeature**](installer-reinstallfeature.md) method to reinstall the feature using this parameter for *ReinstallMode*, and then returns the assembly path.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="7d273-129">*assemblyInfo*</span><span class="sxs-lookup"><span data-stu-id="7d273-129">*assemblyInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="7d273-130">Información de ensamblado y tipo de ensamblado.</span><span class="sxs-lookup"><span data-stu-id="7d273-130">Assembly information and assembly type.</span></span> <span data-ttu-id="7d273-131">Establezca en uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="7d273-131">Set to one of the following values.</span></span>



| <span data-ttu-id="7d273-132">Value</span><span class="sxs-lookup"><span data-stu-id="7d273-132">Value</span></span>                                                                                                                                                                                                                                                                                       | <span data-ttu-id="7d273-133">Significado</span><span class="sxs-lookup"><span data-stu-id="7d273-133">Meaning</span></span>                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| <span id="msiProvideAssemblyNet"></span><span id="msiprovideassemblynet"></span><span id="MSIPROVIDEASSEMBLYNET"></span><dl> <span data-ttu-id="7d273-134"><dt>**msiProvideAssemblyNet**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7d273-134"><dt>**msiProvideAssemblyNet**</dt> <dt>0</dt></span></span> </dl>         | <span data-ttu-id="7d273-135">Un ensamblado .NET.</span><span class="sxs-lookup"><span data-stu-id="7d273-135">A .NET assembly.</span></span><br/>               |
| <span id="msiProvideAssemblyWin32"></span><span id="msiprovideassemblywin32"></span><span id="MSIPROVIDEASSEMBLYWIN32"></span><dl> <span data-ttu-id="7d273-136"><dt>**msiProvideAssemblyWin32**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="7d273-136"><dt>**msiProvideAssemblyWin32**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="7d273-137">Ensamblado en paralelo de Win32.</span><span class="sxs-lookup"><span data-stu-id="7d273-137">A Win32 side-by-side assembly.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d273-138">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7d273-138">Return value</span></span>

<span data-ttu-id="7d273-139">Ruta de acceso al ensamblado instalado.</span><span class="sxs-lookup"><span data-stu-id="7d273-139">The path to the installed assembly.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d273-140">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7d273-140">Remarks</span></span>

<span data-ttu-id="7d273-141">El método **ProvideAssembly** utiliza la función [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya) .</span><span class="sxs-lookup"><span data-stu-id="7d273-141">The **ProvideAssembly** method uses the [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya) function.</span></span>

## <a name="examples"></a><span data-ttu-id="7d273-142">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="7d273-142">Examples</span></span>

<span data-ttu-id="7d273-143">En el siguiente script de ejemplo se muestra el uso del método ProvideAssembly.</span><span class="sxs-lookup"><span data-stu-id="7d273-143">The following sample script demonstrates the use of the ProvideAssembly method.</span></span>


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

'
' ProvideAssembly - .NET global
'   
MsgBox Installer.ProvideAssembly("System.Security,Version=""1.0.5000.0"",PublicKeyToken=""b03f5f7f11d50a3a"",Culture=""neutral"",FileVersion=""1.1.4322.573""", vbNullString, 0, 0)

'
' ProvideAssembly - .NET private
'   
MsgBox Installer.ProvideAssembly("Sample,Version=""1.0.0.0"",Culture=""neutral""", "C:\Program Files\Microsoft\Sample\Sample.exe", 0, 0)

'
' ProvideAssembly - win32 global
'
MsgBox Installer.ProvideAssembly("Microsoft.MSXML2,publicKeyToken=""6bd6b9abf345378f"",version=""4.1.0.0"",type=""win32"",processorArchitecture=""x86""", vbNullString , -2, 1)
```



## <a name="requirements"></a><span data-ttu-id="7d273-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7d273-144">Requirements</span></span>



| <span data-ttu-id="7d273-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d273-145">Requirement</span></span> | <span data-ttu-id="7d273-146">Value</span><span class="sxs-lookup"><span data-stu-id="7d273-146">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d273-147">Versión</span><span class="sxs-lookup"><span data-stu-id="7d273-147">Version</span></span><br/> | <span data-ttu-id="7d273-148">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7d273-148">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="7d273-149">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7d273-149">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="7d273-150">Windows Installer 4,5 en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="7d273-150">Windows Installer 4.5 on Windows Server 2003 and Windows XP</span></span><br/> |
| <span data-ttu-id="7d273-151">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7d273-151">DLL</span></span><br/>     | <dl> <span data-ttu-id="7d273-152"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d273-152"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                           |
| <span data-ttu-id="7d273-153">IID</span><span class="sxs-lookup"><span data-stu-id="7d273-153">IID</span></span><br/>     | <span data-ttu-id="7d273-154">IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="7d273-154">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



## <a name="see-also"></a><span data-ttu-id="7d273-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="7d273-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d273-156">**Instalador**</span><span class="sxs-lookup"><span data-stu-id="7d273-156">**Installer**</span></span>](installer-object.md)
</dt> <dt>

[<span data-ttu-id="7d273-157">No se admite en Windows Installer 3,1 y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="7d273-157">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




