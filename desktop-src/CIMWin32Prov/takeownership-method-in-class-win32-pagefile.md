---
description: 'Método TakeOwnerShip de la clase Win32_PageFile: TakeOwnerShip&\# 8194; El método de clase WMI obtiene la propiedad del archivo lógico especificado en la ruta de acceso del objeto.'
ms.assetid: c4f42d54-562c-4163-a5ec-e94f76932631
ms.tgt_platform: multiple
title: Método TakeOwnerShip de la Win32_PageFile clase
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
ms.openlocfilehash: 3aa0b2ec9f3805f1877f86bdf86d72b921d53ac9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086023"
---
# <a name="takeownership-method-of-the-win32_pagefile-class"></a><span data-ttu-id="a3f96-103">Método TakeOwnerShip de la clase PageFile de Win32 \_</span><span class="sxs-lookup"><span data-stu-id="a3f96-103">TakeOwnerShip method of the Win32\_PageFile class</span></span>

<span data-ttu-id="a3f96-104">El método de clase [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **TakeOwnerShip** obtiene la propiedad del archivo lógico especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="a3f96-104">The **TakeOwnerShip** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="a3f96-105">Si el archivo lógico es realmente un directorio, **TakeOwnerShip** actúa de forma recursiva, tomando posesión de todos los archivos y subdirectorios que contiene el directorio.</span><span class="sxs-lookup"><span data-stu-id="a3f96-105">If the logical file is actually a directory, then **TakeOwnerShip** acts recursively, taking ownership of all of the files and subdirectories the directory contains.</span></span>

<span data-ttu-id="a3f96-106">En este tema se usa Managed Object Format sintaxis de MOF.</span><span class="sxs-lookup"><span data-stu-id="a3f96-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="a3f96-107">Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="a3f96-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="a3f96-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a3f96-108">Syntax</span></span>


```mof
uint32 TakeOwnerShip();
```



## <a name="parameters"></a><span data-ttu-id="a3f96-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a3f96-109">Parameters</span></span>

<span data-ttu-id="a3f96-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="a3f96-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a3f96-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a3f96-111">Return value</span></span>

<span data-ttu-id="a3f96-112">Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="a3f96-112">Returns one of the values listed in the following list or any other value to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="a3f96-113">**0**</span><span class="sxs-lookup"><span data-stu-id="a3f96-113">**0**</span></span>
</dt> <dd>

<span data-ttu-id="a3f96-114">La solicitud fue correcta.</span><span class="sxs-lookup"><span data-stu-id="a3f96-114">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="a3f96-115">**2**</span><span class="sxs-lookup"><span data-stu-id="a3f96-115">**2**</span></span>
</dt> <dd>

<span data-ttu-id="a3f96-116">Se denegó el acceso.</span><span class="sxs-lookup"><span data-stu-id="a3f96-116">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="a3f96-117">**8**</span><span class="sxs-lookup"><span data-stu-id="a3f96-117">**8**</span></span>
</dt> <dd>

<span data-ttu-id="a3f96-118">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="a3f96-118">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="a3f96-119">**9**</span><span class="sxs-lookup"><span data-stu-id="a3f96-119">**9**</span></span>
</dt> <dd>

<span data-ttu-id="a3f96-120">El nombre especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="a3f96-120">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="a3f96-121">**10**</span><span class="sxs-lookup"><span data-stu-id="a3f96-121">**10**</span></span>
</dt> <dd>

<span data-ttu-id="a3f96-122">El objeto especificado ya existe.</span><span class="sxs-lookup"><span data-stu-id="a3f96-122">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="a3f96-123">**11**</span><span class="sxs-lookup"><span data-stu-id="a3f96-123">**11**</span></span>
</dt> <dd>

<span data-ttu-id="a3f96-124">El sistema de archivos no es NTFS.</span><span class="sxs-lookup"><span data-stu-id="a3f96-124">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="a3f96-125">**12**</span><span class="sxs-lookup"><span data-stu-id="a3f96-125">**12**</span></span>
</dt> <dd>

<span data-ttu-id="a3f96-126">La plataforma no es Windows.</span><span class="sxs-lookup"><span data-stu-id="a3f96-126">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="a3f96-127">**13**</span><span class="sxs-lookup"><span data-stu-id="a3f96-127">**13**</span></span>
</dt> <dd>

<span data-ttu-id="a3f96-128">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="a3f96-128">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="a3f96-129">**14**</span><span class="sxs-lookup"><span data-stu-id="a3f96-129">**14**</span></span>
</dt> <dd>

<span data-ttu-id="a3f96-130">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="a3f96-130">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="a3f96-131">**15**</span><span class="sxs-lookup"><span data-stu-id="a3f96-131">**15**</span></span>
</dt> <dd>

<span data-ttu-id="a3f96-132">Se ha infringido el uso compartido.</span><span class="sxs-lookup"><span data-stu-id="a3f96-132">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="a3f96-133">**16**</span><span class="sxs-lookup"><span data-stu-id="a3f96-133">**16**</span></span>
</dt> <dd>

<span data-ttu-id="a3f96-134">El archivo de inicio especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="a3f96-134">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="a3f96-135">**17**</span><span class="sxs-lookup"><span data-stu-id="a3f96-135">**17**</span></span>
</dt> <dd>

<span data-ttu-id="a3f96-136">No se mantiene un privilegio necesario para la operación.</span><span class="sxs-lookup"><span data-stu-id="a3f96-136">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="a3f96-137">**21**</span><span class="sxs-lookup"><span data-stu-id="a3f96-137">**21**</span></span>
</dt> <dd>

<span data-ttu-id="a3f96-138">Un parámetro especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="a3f96-138">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a3f96-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3f96-139">Requirements</span></span>



| <span data-ttu-id="a3f96-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3f96-140">Requirement</span></span> | <span data-ttu-id="a3f96-141">Valor</span><span class="sxs-lookup"><span data-stu-id="a3f96-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a3f96-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a3f96-142">Minimum supported client</span></span><br/> | <span data-ttu-id="a3f96-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a3f96-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a3f96-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a3f96-144">Minimum supported server</span></span><br/> | <span data-ttu-id="a3f96-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a3f96-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a3f96-146">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a3f96-146">Namespace</span></span><br/>                | <span data-ttu-id="a3f96-147">\\CIMV2 raíz</span><span class="sxs-lookup"><span data-stu-id="a3f96-147">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a3f96-148">MOF</span><span class="sxs-lookup"><span data-stu-id="a3f96-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a3f96-149"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="a3f96-149"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a3f96-150">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a3f96-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a3f96-151"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3f96-151"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3f96-152">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a3f96-152">See also</span></span>

<dl> <dt>

<span data-ttu-id="a3f96-153">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a3f96-153">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="a3f96-154">**Win32 \_ PageFile**</span><span class="sxs-lookup"><span data-stu-id="a3f96-154">**Win32\_PageFile**</span></span>](win32-pagefile.md)
</dt> </dl>

 

