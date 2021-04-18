---
description: Cambia el nombre del archivo de paginación especificado en la ruta de acceso del objeto.
ms.assetid: 6a98e05f-337e-4224-a847-f01913031b20
ms.tgt_platform: multiple
title: Cambiar el nombre del método de la clase Win32_PageFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7c9ba8162cd115a567e9e9010420c558061fed08
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659324"
---
# <a name="rename-method-of-the-win32_pagefile-class"></a><span data-ttu-id="44274-103">Cambiar el nombre del método de la clase de archivo de \_ paginación Win32</span><span class="sxs-lookup"><span data-stu-id="44274-103">Rename method of the Win32\_PageFile class</span></span>

<span data-ttu-id="44274-104">El método **Rename** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) cambia el nombre del archivo de paginación especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="44274-104">The **Rename** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method renames the paging file specified in the object path.</span></span> <span data-ttu-id="44274-105">No se admite el cambio de nombre si el destino está en otra unidad o si se requiere sobrescribir un archivo lógico existente.</span><span class="sxs-lookup"><span data-stu-id="44274-105">A rename is not supported if the destination is on another drive or if overwriting an existing logical file is required.</span></span>

<span data-ttu-id="44274-106">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="44274-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="44274-107">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="44274-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="44274-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="44274-108">Syntax</span></span>


```mof
uint32 Rename(
  [in] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="44274-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="44274-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44274-110">*Nombre de archivo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="44274-110">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44274-111">Nuevo nombre completo del archivo (o directorio).</span><span class="sxs-lookup"><span data-stu-id="44274-111">Fully qualified new name of the file (or directory).</span></span>

<span data-ttu-id="44274-112">Ejemplo: c: \\ temp \\newfile.txt</span><span class="sxs-lookup"><span data-stu-id="44274-112">Example: c:\\temp\\newfile.txt</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44274-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="44274-113">Return value</span></span>

<span data-ttu-id="44274-114">Devuelve un valor de 0 (cero) si se cambió el nombre del archivo correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="44274-114">Returns a value of 0 (zero) if the file was successfully renamed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="44274-115">**0**</span><span class="sxs-lookup"><span data-stu-id="44274-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="44274-116">La solicitud fue correcta.</span><span class="sxs-lookup"><span data-stu-id="44274-116">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="44274-117">**2**</span><span class="sxs-lookup"><span data-stu-id="44274-117">**2**</span></span>
</dt> <dd>

<span data-ttu-id="44274-118">Se denegó el acceso.</span><span class="sxs-lookup"><span data-stu-id="44274-118">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="44274-119">**8**</span><span class="sxs-lookup"><span data-stu-id="44274-119">**8**</span></span>
</dt> <dd>

<span data-ttu-id="44274-120">Se produjo un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="44274-120">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="44274-121">**9**</span><span class="sxs-lookup"><span data-stu-id="44274-121">**9**</span></span>
</dt> <dd>

<span data-ttu-id="44274-122">El nombre especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="44274-122">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="44274-123">**10**</span><span class="sxs-lookup"><span data-stu-id="44274-123">**10**</span></span>
</dt> <dd>

<span data-ttu-id="44274-124">El objeto especificado ya existe.</span><span class="sxs-lookup"><span data-stu-id="44274-124">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="44274-125">**11**</span><span class="sxs-lookup"><span data-stu-id="44274-125">**11**</span></span>
</dt> <dd>

<span data-ttu-id="44274-126">El sistema de archivos no es NTFS.</span><span class="sxs-lookup"><span data-stu-id="44274-126">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="44274-127">**12**</span><span class="sxs-lookup"><span data-stu-id="44274-127">**12**</span></span>
</dt> <dd>

<span data-ttu-id="44274-128">La plataforma no es Windows.</span><span class="sxs-lookup"><span data-stu-id="44274-128">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="44274-129">**13**</span><span class="sxs-lookup"><span data-stu-id="44274-129">**13**</span></span>
</dt> <dd>

<span data-ttu-id="44274-130">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="44274-130">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="44274-131">**14**</span><span class="sxs-lookup"><span data-stu-id="44274-131">**14**</span></span>
</dt> <dd>

<span data-ttu-id="44274-132">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="44274-132">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="44274-133">**15**</span><span class="sxs-lookup"><span data-stu-id="44274-133">**15**</span></span>
</dt> <dd>

<span data-ttu-id="44274-134">Se ha producido una infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="44274-134">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="44274-135">**16**</span><span class="sxs-lookup"><span data-stu-id="44274-135">**16**</span></span>
</dt> <dd>

<span data-ttu-id="44274-136">El archivo de inicio especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="44274-136">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="44274-137">**17**</span><span class="sxs-lookup"><span data-stu-id="44274-137">**17**</span></span>
</dt> <dd>

<span data-ttu-id="44274-138">No se mantiene un privilegio necesario para la operación.</span><span class="sxs-lookup"><span data-stu-id="44274-138">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="44274-139">**21**</span><span class="sxs-lookup"><span data-stu-id="44274-139">**21**</span></span>
</dt> <dd>

<span data-ttu-id="44274-140">Un parámetro especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="44274-140">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="44274-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44274-141">Requirements</span></span>



| <span data-ttu-id="44274-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="44274-142">Requirement</span></span> | <span data-ttu-id="44274-143">Value</span><span class="sxs-lookup"><span data-stu-id="44274-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="44274-144">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="44274-144">Minimum supported client</span></span><br/> | <span data-ttu-id="44274-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="44274-145">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="44274-146">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="44274-146">Minimum supported server</span></span><br/> | <span data-ttu-id="44274-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="44274-147">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="44274-148">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="44274-148">Namespace</span></span><br/>                | <span data-ttu-id="44274-149">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="44274-149">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="44274-150">MOF</span><span class="sxs-lookup"><span data-stu-id="44274-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="44274-151"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="44274-151"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="44274-152">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="44274-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44274-153"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44274-153"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44274-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="44274-154">See also</span></span>

<dl> <dt>

<span data-ttu-id="44274-155">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="44274-155">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="44274-156">**Archivo de \_ paginación Win32**</span><span class="sxs-lookup"><span data-stu-id="44274-156">**Win32\_PageFile**</span></span>](win32-pagefile.md)
</dt> </dl>

 

