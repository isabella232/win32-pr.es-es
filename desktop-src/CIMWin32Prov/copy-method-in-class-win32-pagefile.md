---
description: Copia el archivo de paginación lógico o el directorio especificado en la ruta de acceso del objeto en la ubicación especificada por el parámetro de entrada.
ms.assetid: e1ff3e91-dc30-4849-b80a-8838b527ad63
ms.tgt_platform: multiple
title: Método de copia de la clase Win32_PageFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.Copy
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: bde9e0b5cf9b8ab88b5efa1c6aae58a9b8a54cfb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104274985"
---
# <a name="copy-method-of-the-win32_pagefile-class"></a><span data-ttu-id="75aa7-103">Método de copia de la clase de archivo de \_ paginación Win32</span><span class="sxs-lookup"><span data-stu-id="75aa7-103">Copy method of the Win32\_PageFile class</span></span>

<span data-ttu-id="75aa7-104">El método **copiar** [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) copia el archivo de paginación lógico o el directorio especificado en la ruta de acceso del objeto en la ubicación especificada por el parámetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="75aa7-104">The **Copy** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method copies the logical paging file or directory specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="75aa7-105">No se admite una copia si se requiere sobrescribir un archivo lógico existente.</span><span class="sxs-lookup"><span data-stu-id="75aa7-105">A copy is not supported if overwriting an existing logical file is required.</span></span>

<span data-ttu-id="75aa7-106">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="75aa7-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="75aa7-107">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="75aa7-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="75aa7-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="75aa7-108">Syntax</span></span>


```mof
uint32 Copy(
  [in] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="75aa7-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="75aa7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75aa7-110">*Nombre de archivo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="75aa7-110">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75aa7-111">Nombre completo de la copia del archivo (o directorio).</span><span class="sxs-lookup"><span data-stu-id="75aa7-111">Fully qualified name of the copy of the file (or directory).</span></span>

<span data-ttu-id="75aa7-112">Ejemplo: c: \\ temp \\ newdirectory</span><span class="sxs-lookup"><span data-stu-id="75aa7-112">Example: c:\\temp\\newdirectory</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75aa7-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="75aa7-113">Return value</span></span>

<span data-ttu-id="75aa7-114">Devuelve un valor de 0 (cero) si el archivo se ha copiado correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="75aa7-114">Returns a value of 0 (zero) if the file was successfully copied, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="75aa7-115">**0**</span><span class="sxs-lookup"><span data-stu-id="75aa7-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="75aa7-116">La solicitud fue correcta.</span><span class="sxs-lookup"><span data-stu-id="75aa7-116">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="75aa7-117">**2**</span><span class="sxs-lookup"><span data-stu-id="75aa7-117">**2**</span></span>
</dt> <dd>

<span data-ttu-id="75aa7-118">Se denegó el acceso.</span><span class="sxs-lookup"><span data-stu-id="75aa7-118">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="75aa7-119">**8**</span><span class="sxs-lookup"><span data-stu-id="75aa7-119">**8**</span></span>
</dt> <dd>

<span data-ttu-id="75aa7-120">Se produjo un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="75aa7-120">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="75aa7-121">**9**</span><span class="sxs-lookup"><span data-stu-id="75aa7-121">**9**</span></span>
</dt> <dd>

<span data-ttu-id="75aa7-122">El nombre especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="75aa7-122">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="75aa7-123">**10**</span><span class="sxs-lookup"><span data-stu-id="75aa7-123">**10**</span></span>
</dt> <dd>

<span data-ttu-id="75aa7-124">El objeto especificado ya existe.</span><span class="sxs-lookup"><span data-stu-id="75aa7-124">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="75aa7-125">**11**</span><span class="sxs-lookup"><span data-stu-id="75aa7-125">**11**</span></span>
</dt> <dd>

<span data-ttu-id="75aa7-126">El sistema de archivos no es NTFS.</span><span class="sxs-lookup"><span data-stu-id="75aa7-126">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="75aa7-127">**12**</span><span class="sxs-lookup"><span data-stu-id="75aa7-127">**12**</span></span>
</dt> <dd>

<span data-ttu-id="75aa7-128">La plataforma no es Windows.</span><span class="sxs-lookup"><span data-stu-id="75aa7-128">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="75aa7-129">**13**</span><span class="sxs-lookup"><span data-stu-id="75aa7-129">**13**</span></span>
</dt> <dd>

<span data-ttu-id="75aa7-130">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="75aa7-130">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="75aa7-131">**14**</span><span class="sxs-lookup"><span data-stu-id="75aa7-131">**14**</span></span>
</dt> <dd>

<span data-ttu-id="75aa7-132">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="75aa7-132">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="75aa7-133">**15**</span><span class="sxs-lookup"><span data-stu-id="75aa7-133">**15**</span></span>
</dt> <dd>

<span data-ttu-id="75aa7-134">Se ha producido una infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="75aa7-134">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="75aa7-135">**16**</span><span class="sxs-lookup"><span data-stu-id="75aa7-135">**16**</span></span>
</dt> <dd>

<span data-ttu-id="75aa7-136">El archivo de inicio especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="75aa7-136">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="75aa7-137">**17**</span><span class="sxs-lookup"><span data-stu-id="75aa7-137">**17**</span></span>
</dt> <dd>

<span data-ttu-id="75aa7-138">No se mantiene un privilegio necesario para la operación.</span><span class="sxs-lookup"><span data-stu-id="75aa7-138">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="75aa7-139">**21**</span><span class="sxs-lookup"><span data-stu-id="75aa7-139">**21**</span></span>
</dt> <dd>

<span data-ttu-id="75aa7-140">Un parámetro especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="75aa7-140">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="75aa7-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75aa7-141">Requirements</span></span>



| <span data-ttu-id="75aa7-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="75aa7-142">Requirement</span></span> | <span data-ttu-id="75aa7-143">Value</span><span class="sxs-lookup"><span data-stu-id="75aa7-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="75aa7-144">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="75aa7-144">Minimum supported client</span></span><br/> | <span data-ttu-id="75aa7-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="75aa7-145">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="75aa7-146">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="75aa7-146">Minimum supported server</span></span><br/> | <span data-ttu-id="75aa7-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="75aa7-147">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="75aa7-148">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="75aa7-148">Namespace</span></span><br/>                | <span data-ttu-id="75aa7-149">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="75aa7-149">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="75aa7-150">MOF</span><span class="sxs-lookup"><span data-stu-id="75aa7-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="75aa7-151"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="75aa7-151"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="75aa7-152">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="75aa7-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75aa7-153"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75aa7-153"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75aa7-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="75aa7-154">See also</span></span>

<dl> <dt>

<span data-ttu-id="75aa7-155">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="75aa7-155">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="75aa7-156">**Archivo de \_ paginación Win32**</span><span class="sxs-lookup"><span data-stu-id="75aa7-156">**Win32\_PageFile**</span></span>](win32-pagefile.md)
</dt> </dl>

 

