---
description: El método ReinstallFeature del objeto Installer vuelve a instalar las características o corrige los problemas con las características instaladas.
ms.assetid: cfe2aef4-7742-49cd-b7a3-7d484e1f85e3
title: Instalador. ReinstallFeature (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ReinstallFeature
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a6bac008ee7121bbcb985b9a8ff5ba02df122266
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653889"
---
# <a name="installerreinstallfeature-method"></a><span data-ttu-id="bda6a-103">Instalador. ReinstallFeature (método)</span><span class="sxs-lookup"><span data-stu-id="bda6a-103">Installer.ReinstallFeature method</span></span>

<span data-ttu-id="bda6a-104">El método **ReinstallFeature** del objeto [**Installer**](installer-object.md) vuelve a instalar las características o corrige los problemas con las características instaladas.</span><span class="sxs-lookup"><span data-stu-id="bda6a-104">The **ReinstallFeature** method of the [**Installer**](installer-object.md) object reinstalls features or corrects problems with installed features.</span></span>

## <a name="syntax"></a><span data-ttu-id="bda6a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bda6a-105">Syntax</span></span>


```JScript
Installer.ReinstallFeature(
  Product,
  Feature,
  ReinstallMode
)
```



## <a name="parameters"></a><span data-ttu-id="bda6a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bda6a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bda6a-107">*Producto*</span><span class="sxs-lookup"><span data-stu-id="bda6a-107">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="bda6a-108">Especifica el código de producto del producto.</span><span class="sxs-lookup"><span data-stu-id="bda6a-108">Specifies the product code of the product.</span></span>

</dd> <dt>

<span data-ttu-id="bda6a-109">*Característica*</span><span class="sxs-lookup"><span data-stu-id="bda6a-109">*Feature*</span></span> 
</dt> <dd>

<span data-ttu-id="bda6a-110">Especifica la característica que se va a volver a instalar.</span><span class="sxs-lookup"><span data-stu-id="bda6a-110">Specifies the feature to be reinstalled.</span></span> <span data-ttu-id="bda6a-111">La característica primaria o la característica secundaria de la característica especificada no se reinstalan.</span><span class="sxs-lookup"><span data-stu-id="bda6a-111">The parent feature or child feature of the specified feature is not reinstalled.</span></span> <span data-ttu-id="bda6a-112">Para volver a instalar la característica primaria o secundaria, debe llamar al método **ReinstallFeature** para cada uno por separado o usar el método [**ReinstallProduct**](installer-reinstallproduct.md) .</span><span class="sxs-lookup"><span data-stu-id="bda6a-112">To reinstall the parent or child feature, you must call the **ReinstallFeature** method for each separately or use the [**ReinstallProduct**](installer-reinstallproduct.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="bda6a-113">*ReinstallMode*</span><span class="sxs-lookup"><span data-stu-id="bda6a-113">*ReinstallMode*</span></span> 
</dt> <dd>

<span data-ttu-id="bda6a-114">Especifica el tipo de reinstalación.</span><span class="sxs-lookup"><span data-stu-id="bda6a-114">Specifies the type of reinstallation.</span></span> <span data-ttu-id="bda6a-115">Este parámetro puede ser uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="bda6a-115">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="bda6a-116">Value</span><span class="sxs-lookup"><span data-stu-id="bda6a-116">Value</span></span>                                                                                                                                                                                                                                                                    | <span data-ttu-id="bda6a-117">Significado</span><span class="sxs-lookup"><span data-stu-id="bda6a-117">Meaning</span></span>                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <span id="msiReinstallModeFileMissing"></span><span id="msireinstallmodefilemissing"></span><span id="MSIREINSTALLMODEFILEMISSING"></span><dl> <span data-ttu-id="bda6a-118"><dt>**msiReinstallModeFileMissing**</dt></span><span class="sxs-lookup"><span data-stu-id="bda6a-118"><dt>**msiReinstallModeFileMissing**</dt></span></span> </dl>                     | <span data-ttu-id="bda6a-119">Vuelve a instalar solo si falta el archivo.</span><span class="sxs-lookup"><span data-stu-id="bda6a-119">Reinstalls only if the file is missing.</span></span><br/>                                |
| <span id="msiReinstallModeFileOlderVersion"></span><span id="msireinstallmodefileolderversion"></span><span id="MSIREINSTALLMODEFILEOLDERVERSION"></span><dl> <span data-ttu-id="bda6a-120"><dt>**msiReinstallModeFileOlderVersion**</dt></span><span class="sxs-lookup"><span data-stu-id="bda6a-120"><dt>**msiReinstallModeFileOlderVersion**</dt></span></span> </dl> | <span data-ttu-id="bda6a-121">Vuelve a instalar si falta el archivo o es una versión anterior.</span><span class="sxs-lookup"><span data-stu-id="bda6a-121">Reinstalls if the file is missing or is an older version.</span></span><br/>              |
| <span id="msiReinstallModeFileEqualVersion"></span><span id="msireinstallmodefileequalversion"></span><span id="MSIREINSTALLMODEFILEEQUALVERSION"></span><dl> <span data-ttu-id="bda6a-122"><dt>**msiReinstallModeFileEqualVersion**</dt></span><span class="sxs-lookup"><span data-stu-id="bda6a-122"><dt>**msiReinstallModeFileEqualVersion**</dt></span></span> </dl> | <span data-ttu-id="bda6a-123">Vuelve a instalar si falta el archivo o es una versión igual o anterior.</span><span class="sxs-lookup"><span data-stu-id="bda6a-123">Reinstalls if the file is missing or is an equal or older version.</span></span><br/>     |
| <span id="msiReinstallModeFileExact"></span><span id="msireinstallmodefileexact"></span><span id="MSIREINSTALLMODEFILEEXACT"></span><dl> <span data-ttu-id="bda6a-124"><dt>**msiReinstallModeFileExact**</dt></span><span class="sxs-lookup"><span data-stu-id="bda6a-124"><dt>**msiReinstallModeFileExact**</dt></span></span> </dl>                             | <span data-ttu-id="bda6a-125">Vuelve a instalar si falta el archivo o no es una versión exacta.</span><span class="sxs-lookup"><span data-stu-id="bda6a-125">Reinstalls if the file is missing or is not an exact version.</span></span><br/>          |
| <span id="msiReinstallModeFileVerify"></span><span id="msireinstallmodefileverify"></span><span id="MSIREINSTALLMODEFILEVERIFY"></span><dl> <span data-ttu-id="bda6a-126"><dt>**msiReinstallModeFileVerify**</dt></span><span class="sxs-lookup"><span data-stu-id="bda6a-126"><dt>**msiReinstallModeFileVerify**</dt></span></span> </dl>                         | <span data-ttu-id="bda6a-127">Comprueba los ejecutables de suma y vuelve a instalar si faltan o están dañados.</span><span class="sxs-lookup"><span data-stu-id="bda6a-127">Checks sum executables, and reinstalls if they are missing or corrupt.</span></span><br/> |
| <span id="msiReinstallModeFileReplace"></span><span id="msireinstallmodefilereplace"></span><span id="MSIREINSTALLMODEFILEREPLACE"></span><dl> <span data-ttu-id="bda6a-128"><dt>**msiReinstallModeFileReplace**</dt></span><span class="sxs-lookup"><span data-stu-id="bda6a-128"><dt>**msiReinstallModeFileReplace**</dt></span></span> </dl>                     | <span data-ttu-id="bda6a-129">Vuelve a instalar todos los archivos independientemente de la versión.</span><span class="sxs-lookup"><span data-stu-id="bda6a-129">Reinstalls all files regardless of version.</span></span><br/>                            |
| <span id="msiReinstallModeUserData"></span><span id="msireinstallmodeuserdata"></span><span id="MSIREINSTALLMODEUSERDATA"></span><dl> <span data-ttu-id="bda6a-130"><dt>**msiReinstallModeUserData**</dt></span><span class="sxs-lookup"><span data-stu-id="bda6a-130"><dt>**msiReinstallModeUserData**</dt></span></span> </dl>                                 | <span data-ttu-id="bda6a-131">Garantiza que se requieren por las entradas del registro del usuario.</span><span class="sxs-lookup"><span data-stu-id="bda6a-131">Ensures required per=user registry entries.</span></span><br/>                            |
| <span id="msiReinstallModeMachineData"></span><span id="msireinstallmodemachinedata"></span><span id="MSIREINSTALLMODEMACHINEDATA"></span><dl> <span data-ttu-id="bda6a-132"><dt>**msiReinstallModeMachineData**</dt></span><span class="sxs-lookup"><span data-stu-id="bda6a-132"><dt>**msiReinstallModeMachineData**</dt></span></span> </dl>                     | <span data-ttu-id="bda6a-133">Garantiza que se requieren por las entradas del registro del equipo.</span><span class="sxs-lookup"><span data-stu-id="bda6a-133">Ensures required per=machine registry entries.</span></span><br/>                         |
| <span id="msiReinstallModeShortcut"></span><span id="msireinstallmodeshortcut"></span><span id="MSIREINSTALLMODESHORTCUT"></span><dl> <span data-ttu-id="bda6a-134"><dt>**msiReinstallModeShortcut**</dt></span><span class="sxs-lookup"><span data-stu-id="bda6a-134"><dt>**msiReinstallModeShortcut**</dt></span></span> </dl>                                 | <span data-ttu-id="bda6a-135">Valida los accesos directos.</span><span class="sxs-lookup"><span data-stu-id="bda6a-135">Validates shortcuts.</span></span><br/>                                                   |
| <span id="msiReinstallModePackage"></span><span id="msireinstallmodepackage"></span><span id="MSIREINSTALLMODEPACKAGE"></span><dl> <span data-ttu-id="bda6a-136"><dt>**msiReinstallModePackage**</dt></span><span class="sxs-lookup"><span data-stu-id="bda6a-136"><dt>**msiReinstallModePackage**</dt></span></span> </dl>                                     | <span data-ttu-id="bda6a-137">Usa el origen de la recaché para instalar el paquete.</span><span class="sxs-lookup"><span data-stu-id="bda6a-137">Uses the recache source to install the package.</span></span><br/>                        |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bda6a-138">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bda6a-138">Return value</span></span>

<span data-ttu-id="bda6a-139">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="bda6a-139">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="bda6a-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bda6a-140">Requirements</span></span>



| <span data-ttu-id="bda6a-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="bda6a-141">Requirement</span></span> | <span data-ttu-id="bda6a-142">Value</span><span class="sxs-lookup"><span data-stu-id="bda6a-142">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bda6a-143">Versión</span><span class="sxs-lookup"><span data-stu-id="bda6a-143">Version</span></span><br/> | <span data-ttu-id="bda6a-144">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="bda6a-144">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="bda6a-145">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="bda6a-145">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="bda6a-146">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="bda6a-146">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="bda6a-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bda6a-147">DLL</span></span><br/>     | <dl> <span data-ttu-id="bda6a-148"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bda6a-148"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="bda6a-149">IID</span><span class="sxs-lookup"><span data-stu-id="bda6a-149">IID</span></span><br/>     | <span data-ttu-id="bda6a-150">IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="bda6a-150">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="bda6a-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="bda6a-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bda6a-152">**MsiReinstallFeature**</span><span class="sxs-lookup"><span data-stu-id="bda6a-152">**MsiReinstallFeature**</span></span>](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea)
</dt> <dt>

[<span data-ttu-id="bda6a-153">Funciones de instalación y configuración</span><span class="sxs-lookup"><span data-stu-id="bda6a-153">Installation and Configuration Functions</span></span>](installer-function-reference.md)
</dt> </dl>

 

 




