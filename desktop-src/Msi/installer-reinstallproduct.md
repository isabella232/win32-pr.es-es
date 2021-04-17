---
description: El método ReinstallProduct del objeto Installer vuelve a instalar un producto o corrige los problemas de instalación en un producto instalado.
ms.assetid: ff933cce-9f27-4215-9291-dd860d9c4d08
title: Instalador. ReinstallProduct (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ReinstallProduct
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1570f5a0dc607b4a011a5b4276a243c59a64392d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653709"
---
# <a name="installerreinstallproduct-method"></a><span data-ttu-id="56dbe-103">Instalador. ReinstallProduct (método)</span><span class="sxs-lookup"><span data-stu-id="56dbe-103">Installer.ReinstallProduct method</span></span>

<span data-ttu-id="56dbe-104">El método **ReinstallProduct** del objeto [**Installer**](installer-object.md) vuelve a instalar un producto o corrige los problemas de instalación en un producto instalado.</span><span class="sxs-lookup"><span data-stu-id="56dbe-104">The **ReinstallProduct** method of the [**Installer**](installer-object.md) object reinstalls a product or corrects installation problems in an installed product.</span></span>

## <a name="syntax"></a><span data-ttu-id="56dbe-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="56dbe-105">Syntax</span></span>


```JScript
Installer.ReinstallProduct(
  Product,
  ReinstallMode
)
```



## <a name="parameters"></a><span data-ttu-id="56dbe-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="56dbe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56dbe-107">*Producto*</span><span class="sxs-lookup"><span data-stu-id="56dbe-107">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="56dbe-108">Especifica el código de producto del producto.</span><span class="sxs-lookup"><span data-stu-id="56dbe-108">Specifies the product code of the product.</span></span>

</dd> <dt>

<span data-ttu-id="56dbe-109">*ReinstallMode*</span><span class="sxs-lookup"><span data-stu-id="56dbe-109">*ReinstallMode*</span></span> 
</dt> <dd>

<span data-ttu-id="56dbe-110">Especifica el tipo de reinstalación.</span><span class="sxs-lookup"><span data-stu-id="56dbe-110">Specifies the type of reinstallation.</span></span> <span data-ttu-id="56dbe-111">Este parámetro puede ser uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="56dbe-111">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="56dbe-112">Value</span><span class="sxs-lookup"><span data-stu-id="56dbe-112">Value</span></span>                                                                                                                                                                                                                                                                    | <span data-ttu-id="56dbe-113">Significado</span><span class="sxs-lookup"><span data-stu-id="56dbe-113">Meaning</span></span>                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <span id="msiReinstallModeFileMissing"></span><span id="msireinstallmodefilemissing"></span><span id="MSIREINSTALLMODEFILEMISSING"></span><dl> <span data-ttu-id="56dbe-114"><dt>**msiReinstallModeFileMissing**</dt></span><span class="sxs-lookup"><span data-stu-id="56dbe-114"><dt>**msiReinstallModeFileMissing**</dt></span></span> </dl>                     | <span data-ttu-id="56dbe-115">Vuelve a instalar solo si falta el archivo.</span><span class="sxs-lookup"><span data-stu-id="56dbe-115">Reinstalls only if the file is missing.</span></span><br/>                                |
| <span id="msiReinstallModeFileOlderVersion"></span><span id="msireinstallmodefileolderversion"></span><span id="MSIREINSTALLMODEFILEOLDERVERSION"></span><dl> <span data-ttu-id="56dbe-116"><dt>**msiReinstallModeFileOlderVersion**</dt></span><span class="sxs-lookup"><span data-stu-id="56dbe-116"><dt>**msiReinstallModeFileOlderVersion**</dt></span></span> </dl> | <span data-ttu-id="56dbe-117">Vuelve a instalar si falta el archivo o es una versión anterior.</span><span class="sxs-lookup"><span data-stu-id="56dbe-117">Reinstalls if the file is missing or is an older version.</span></span><br/>              |
| <span id="msiReinstallModeFileEqualVersion"></span><span id="msireinstallmodefileequalversion"></span><span id="MSIREINSTALLMODEFILEEQUALVERSION"></span><dl> <span data-ttu-id="56dbe-118"><dt>**msiReinstallModeFileEqualVersion**</dt></span><span class="sxs-lookup"><span data-stu-id="56dbe-118"><dt>**msiReinstallModeFileEqualVersion**</dt></span></span> </dl> | <span data-ttu-id="56dbe-119">Vuelve a instalar si falta el archivo o es una versión igual o anterior.</span><span class="sxs-lookup"><span data-stu-id="56dbe-119">Reinstalls if the file is missing or is an equal or older version.</span></span><br/>     |
| <span id="msiReinstallModeFileExact"></span><span id="msireinstallmodefileexact"></span><span id="MSIREINSTALLMODEFILEEXACT"></span><dl> <span data-ttu-id="56dbe-120"><dt>**msiReinstallModeFileExact**</dt></span><span class="sxs-lookup"><span data-stu-id="56dbe-120"><dt>**msiReinstallModeFileExact**</dt></span></span> </dl>                             | <span data-ttu-id="56dbe-121">Vuelve a instalar si falta el archivo o no es una versión exacta.</span><span class="sxs-lookup"><span data-stu-id="56dbe-121">Reinstalls if the file is missing or is not an exact version.</span></span><br/>          |
| <span id="msiReinstallModeFileVerify"></span><span id="msireinstallmodefileverify"></span><span id="MSIREINSTALLMODEFILEVERIFY"></span><dl> <span data-ttu-id="56dbe-122"><dt>**msiReinstallModeFileVerify**</dt></span><span class="sxs-lookup"><span data-stu-id="56dbe-122"><dt>**msiReinstallModeFileVerify**</dt></span></span> </dl>                         | <span data-ttu-id="56dbe-123">Comprueba los ejecutables de suma y vuelve a instalar si faltan o están dañados.</span><span class="sxs-lookup"><span data-stu-id="56dbe-123">Checks sum executables, and reinstalls if they are missing or corrupt.</span></span><br/> |
| <span id="msiReinstallModeFileReplace"></span><span id="msireinstallmodefilereplace"></span><span id="MSIREINSTALLMODEFILEREPLACE"></span><dl> <span data-ttu-id="56dbe-124"><dt>**msiReinstallModeFileReplace**</dt></span><span class="sxs-lookup"><span data-stu-id="56dbe-124"><dt>**msiReinstallModeFileReplace**</dt></span></span> </dl>                     | <span data-ttu-id="56dbe-125">Vuelve a instalar todos los archivos independientemente de la versión.</span><span class="sxs-lookup"><span data-stu-id="56dbe-125">Reinstalls all files regardless of version.</span></span><br/>                            |
| <span id="msiReinstallModeUserData"></span><span id="msireinstallmodeuserdata"></span><span id="MSIREINSTALLMODEUSERDATA"></span><dl> <span data-ttu-id="56dbe-126"><dt>**msiReinstallModeUserData**</dt></span><span class="sxs-lookup"><span data-stu-id="56dbe-126"><dt>**msiReinstallModeUserData**</dt></span></span> </dl>                                 | <span data-ttu-id="56dbe-127">Garantiza que se requieren por las entradas del registro del usuario.</span><span class="sxs-lookup"><span data-stu-id="56dbe-127">Ensures required per=user registry entries.</span></span><br/>                            |
| <span id="msiReinstallModeMachineData"></span><span id="msireinstallmodemachinedata"></span><span id="MSIREINSTALLMODEMACHINEDATA"></span><dl> <span data-ttu-id="56dbe-128"><dt>**msiReinstallModeMachineData**</dt></span><span class="sxs-lookup"><span data-stu-id="56dbe-128"><dt>**msiReinstallModeMachineData**</dt></span></span> </dl>                     | <span data-ttu-id="56dbe-129">Garantiza que se requieren por las entradas del registro del equipo.</span><span class="sxs-lookup"><span data-stu-id="56dbe-129">Ensures required per=machine registry entries.</span></span><br/>                         |
| <span id="msiReinstallModeShortcut"></span><span id="msireinstallmodeshortcut"></span><span id="MSIREINSTALLMODESHORTCUT"></span><dl> <span data-ttu-id="56dbe-130"><dt>**msiReinstallModeShortcut**</dt></span><span class="sxs-lookup"><span data-stu-id="56dbe-130"><dt>**msiReinstallModeShortcut**</dt></span></span> </dl>                                 | <span data-ttu-id="56dbe-131">Valida los accesos directos.</span><span class="sxs-lookup"><span data-stu-id="56dbe-131">Validates shortcuts.</span></span><br/>                                                   |
| <span id="msiReinstallModePackage"></span><span id="msireinstallmodepackage"></span><span id="MSIREINSTALLMODEPACKAGE"></span><dl> <span data-ttu-id="56dbe-132"><dt>**msiReinstallModePackage**</dt></span><span class="sxs-lookup"><span data-stu-id="56dbe-132"><dt>**msiReinstallModePackage**</dt></span></span> </dl>                                     | <span data-ttu-id="56dbe-133">Usa el origen de la recaché para instalar el paquete.</span><span class="sxs-lookup"><span data-stu-id="56dbe-133">Uses the recache source to install the package.</span></span><br/>                        |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56dbe-134">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="56dbe-134">Return value</span></span>

<span data-ttu-id="56dbe-135">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="56dbe-135">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="56dbe-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56dbe-136">Requirements</span></span>



| <span data-ttu-id="56dbe-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="56dbe-137">Requirement</span></span> | <span data-ttu-id="56dbe-138">Value</span><span class="sxs-lookup"><span data-stu-id="56dbe-138">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56dbe-139">Versión</span><span class="sxs-lookup"><span data-stu-id="56dbe-139">Version</span></span><br/> | <span data-ttu-id="56dbe-140">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="56dbe-140">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="56dbe-141">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="56dbe-141">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="56dbe-142">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="56dbe-142">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="56dbe-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="56dbe-143">DLL</span></span><br/>     | <dl> <span data-ttu-id="56dbe-144"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56dbe-144"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="56dbe-145">IID</span><span class="sxs-lookup"><span data-stu-id="56dbe-145">IID</span></span><br/>     | <span data-ttu-id="56dbe-146">IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="56dbe-146">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="56dbe-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="56dbe-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56dbe-148">**MsiReinstallProduct**</span><span class="sxs-lookup"><span data-stu-id="56dbe-148">**MsiReinstallProduct**</span></span>](/windows/desktop/api/Msi/nf-msi-msireinstallproducta)
</dt> <dt>

[<span data-ttu-id="56dbe-149">Funciones de instalación y configuración</span><span class="sxs-lookup"><span data-stu-id="56dbe-149">Installation and Configuration Functions</span></span>](installer-function-reference.md)
</dt> </dl>

 

 




