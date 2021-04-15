---
description: TakeOwnerShip&\# 8194; El método de clase WMI obtiene la propiedad del archivo lógico especificado en la ruta de acceso del objeto.
ms.assetid: c4f42d54-562c-4163-a5ec-e94f76932631
ms.tgt_platform: multiple
title: Método TakeOwnerShip de la clase Win32_PageFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.TakeOwnerShip
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3265e0acc065f63daca2ed6485269ac8c006ad8d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539375"
---
# <a name="takeownership-method-of-the-win32_pagefile-class"></a><span data-ttu-id="68c42-103">Método TakeOwnerShip de la clase de archivo de \_ paginación Win32</span><span class="sxs-lookup"><span data-stu-id="68c42-103">TakeOwnerShip method of the Win32\_PageFile class</span></span>

<span data-ttu-id="68c42-104">El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **TakeOwnerShip** obtiene la propiedad del archivo lógico especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="68c42-104">The **TakeOwnerShip** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="68c42-105">Si el archivo lógico es realmente un directorio, **TakeOwnerShip** actúa de forma recursiva y toma la propiedad de todos los archivos y subdirectorios que contiene el directorio.</span><span class="sxs-lookup"><span data-stu-id="68c42-105">If the logical file is actually a directory, then **TakeOwnerShip** acts recursively, taking ownership of all of the files and subdirectories the directory contains.</span></span>

<span data-ttu-id="68c42-106">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="68c42-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="68c42-107">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="68c42-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="68c42-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="68c42-108">Syntax</span></span>


```mof
uint32 TakeOwnerShip();
```



## <a name="parameters"></a><span data-ttu-id="68c42-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="68c42-109">Parameters</span></span>

<span data-ttu-id="68c42-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="68c42-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="68c42-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="68c42-111">Return value</span></span>

<span data-ttu-id="68c42-112">Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="68c42-112">Returns one of the values listed in the following list or any other value to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="68c42-113">**0**</span><span class="sxs-lookup"><span data-stu-id="68c42-113">**0**</span></span>
</dt> <dd>

<span data-ttu-id="68c42-114">La solicitud fue correcta.</span><span class="sxs-lookup"><span data-stu-id="68c42-114">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="68c42-115">**2**</span><span class="sxs-lookup"><span data-stu-id="68c42-115">**2**</span></span>
</dt> <dd>

<span data-ttu-id="68c42-116">Se denegó el acceso.</span><span class="sxs-lookup"><span data-stu-id="68c42-116">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="68c42-117">**8**</span><span class="sxs-lookup"><span data-stu-id="68c42-117">**8**</span></span>
</dt> <dd>

<span data-ttu-id="68c42-118">Se produjo un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="68c42-118">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="68c42-119">**9**</span><span class="sxs-lookup"><span data-stu-id="68c42-119">**9**</span></span>
</dt> <dd>

<span data-ttu-id="68c42-120">El nombre especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="68c42-120">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="68c42-121">**10**</span><span class="sxs-lookup"><span data-stu-id="68c42-121">**10**</span></span>
</dt> <dd>

<span data-ttu-id="68c42-122">El objeto especificado ya existe.</span><span class="sxs-lookup"><span data-stu-id="68c42-122">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="68c42-123">**11**</span><span class="sxs-lookup"><span data-stu-id="68c42-123">**11**</span></span>
</dt> <dd>

<span data-ttu-id="68c42-124">El sistema de archivos no es NTFS.</span><span class="sxs-lookup"><span data-stu-id="68c42-124">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="68c42-125">**12**</span><span class="sxs-lookup"><span data-stu-id="68c42-125">**12**</span></span>
</dt> <dd>

<span data-ttu-id="68c42-126">La plataforma no es Windows.</span><span class="sxs-lookup"><span data-stu-id="68c42-126">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="68c42-127">**13**</span><span class="sxs-lookup"><span data-stu-id="68c42-127">**13**</span></span>
</dt> <dd>

<span data-ttu-id="68c42-128">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="68c42-128">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="68c42-129">**14**</span><span class="sxs-lookup"><span data-stu-id="68c42-129">**14**</span></span>
</dt> <dd>

<span data-ttu-id="68c42-130">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="68c42-130">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="68c42-131">**15**</span><span class="sxs-lookup"><span data-stu-id="68c42-131">**15**</span></span>
</dt> <dd>

<span data-ttu-id="68c42-132">Se ha producido una infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="68c42-132">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="68c42-133">**16**</span><span class="sxs-lookup"><span data-stu-id="68c42-133">**16**</span></span>
</dt> <dd>

<span data-ttu-id="68c42-134">El archivo de inicio especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="68c42-134">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="68c42-135">**17**</span><span class="sxs-lookup"><span data-stu-id="68c42-135">**17**</span></span>
</dt> <dd>

<span data-ttu-id="68c42-136">No se mantiene un privilegio necesario para la operación.</span><span class="sxs-lookup"><span data-stu-id="68c42-136">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="68c42-137">**21**</span><span class="sxs-lookup"><span data-stu-id="68c42-137">**21**</span></span>
</dt> <dd>

<span data-ttu-id="68c42-138">Un parámetro especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="68c42-138">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="68c42-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68c42-139">Requirements</span></span>



| <span data-ttu-id="68c42-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="68c42-140">Requirement</span></span> | <span data-ttu-id="68c42-141">Value</span><span class="sxs-lookup"><span data-stu-id="68c42-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="68c42-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68c42-142">Minimum supported client</span></span><br/> | <span data-ttu-id="68c42-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="68c42-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="68c42-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68c42-144">Minimum supported server</span></span><br/> | <span data-ttu-id="68c42-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="68c42-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="68c42-146">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="68c42-146">Namespace</span></span><br/>                | <span data-ttu-id="68c42-147">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="68c42-147">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="68c42-148">MOF</span><span class="sxs-lookup"><span data-stu-id="68c42-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="68c42-149"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="68c42-149"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="68c42-150">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="68c42-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68c42-151"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68c42-151"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68c42-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="68c42-152">See also</span></span>

<dl> <dt>

<span data-ttu-id="68c42-153">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="68c42-153">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="68c42-154">**Archivo de \_ paginación Win32**</span><span class="sxs-lookup"><span data-stu-id="68c42-154">**Win32\_PageFile**</span></span>](win32-pagefile.md)
</dt> </dl>

 

