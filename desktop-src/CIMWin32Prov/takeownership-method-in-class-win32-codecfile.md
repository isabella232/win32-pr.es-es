---
description: El método de clase WMI TakeOwnerShip obtiene la propiedad del archivo lógico especificado en la ruta de acceso del objeto.
ms.assetid: c8fa0706-1f7e-4e68-aea6-694ba24c16c3
ms.tgt_platform: multiple
title: Método TakeOwnerShip de la clase Win32_CodecFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.TakeOwnerShip
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1de05f444e99be9a1ebcb5d32fa0ba754cf34254
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152831"
---
# <a name="takeownership-method-of-the-win32_codecfile-class"></a><span data-ttu-id="b3814-103">Método TakeOwnerShip de la \_ clase CodecFile de Win32</span><span class="sxs-lookup"><span data-stu-id="b3814-103">TakeOwnerShip method of the Win32\_CodecFile class</span></span>

<span data-ttu-id="b3814-104">El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **TakeOwnerShip** obtiene la propiedad del archivo lógico especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="b3814-104">The **TakeOwnerShip** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="b3814-105">Si el archivo lógico es realmente un directorio, **TakeOwnerShip** actúa de forma recursiva y toma la propiedad de todos los archivos y subdirectorios que contiene el directorio.</span><span class="sxs-lookup"><span data-stu-id="b3814-105">If the logical file is actually a directory, then **TakeOwnerShip** acts recursively, taking ownership of all of the files and subdirectories the directory contains.</span></span>

<span data-ttu-id="b3814-106">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="b3814-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="b3814-107">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="b3814-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="b3814-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b3814-108">Syntax</span></span>


```mof
uint32 TakeOwnerShip();
```



## <a name="parameters"></a><span data-ttu-id="b3814-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b3814-109">Parameters</span></span>

<span data-ttu-id="b3814-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="b3814-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b3814-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b3814-111">Return value</span></span>

<span data-ttu-id="b3814-112">Devuelve uno de los siguientes valores enteros.</span><span class="sxs-lookup"><span data-stu-id="b3814-112">Returns one of the following integer values.</span></span>

<dl> <dt>

<span data-ttu-id="b3814-113">**0**</span><span class="sxs-lookup"><span data-stu-id="b3814-113">**0**</span></span>
</dt> <dd>

<span data-ttu-id="b3814-114">La solicitud fue correcta.</span><span class="sxs-lookup"><span data-stu-id="b3814-114">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="b3814-115">**2**</span><span class="sxs-lookup"><span data-stu-id="b3814-115">**2**</span></span>
</dt> <dd>

<span data-ttu-id="b3814-116">Se denegó el acceso.</span><span class="sxs-lookup"><span data-stu-id="b3814-116">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="b3814-117">**8**</span><span class="sxs-lookup"><span data-stu-id="b3814-117">**8**</span></span>
</dt> <dd>

<span data-ttu-id="b3814-118">Se produjo un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="b3814-118">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="b3814-119">**9**</span><span class="sxs-lookup"><span data-stu-id="b3814-119">**9**</span></span>
</dt> <dd>

<span data-ttu-id="b3814-120">El nombre especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="b3814-120">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="b3814-121">**10**</span><span class="sxs-lookup"><span data-stu-id="b3814-121">**10**</span></span>
</dt> <dd>

<span data-ttu-id="b3814-122">El objeto especificado ya existe.</span><span class="sxs-lookup"><span data-stu-id="b3814-122">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="b3814-123">**11**</span><span class="sxs-lookup"><span data-stu-id="b3814-123">**11**</span></span>
</dt> <dd>

<span data-ttu-id="b3814-124">El sistema de archivos no es NTFS.</span><span class="sxs-lookup"><span data-stu-id="b3814-124">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="b3814-125">**12**</span><span class="sxs-lookup"><span data-stu-id="b3814-125">**12**</span></span>
</dt> <dd>

<span data-ttu-id="b3814-126">La plataforma no es Windows.</span><span class="sxs-lookup"><span data-stu-id="b3814-126">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="b3814-127">**13**</span><span class="sxs-lookup"><span data-stu-id="b3814-127">**13**</span></span>
</dt> <dd>

<span data-ttu-id="b3814-128">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="b3814-128">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="b3814-129">**14**</span><span class="sxs-lookup"><span data-stu-id="b3814-129">**14**</span></span>
</dt> <dd>

<span data-ttu-id="b3814-130">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="b3814-130">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="b3814-131">**15**</span><span class="sxs-lookup"><span data-stu-id="b3814-131">**15**</span></span>
</dt> <dd>

<span data-ttu-id="b3814-132">Se ha producido una infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="b3814-132">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="b3814-133">**16**</span><span class="sxs-lookup"><span data-stu-id="b3814-133">**16**</span></span>
</dt> <dd>

<span data-ttu-id="b3814-134">El archivo de inicio especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="b3814-134">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="b3814-135">**17**</span><span class="sxs-lookup"><span data-stu-id="b3814-135">**17**</span></span>
</dt> <dd>

<span data-ttu-id="b3814-136">No se mantiene un privilegio necesario para la operación.</span><span class="sxs-lookup"><span data-stu-id="b3814-136">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="b3814-137">**21**</span><span class="sxs-lookup"><span data-stu-id="b3814-137">**21**</span></span>
</dt> <dd>

<span data-ttu-id="b3814-138">Un parámetro especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="b3814-138">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b3814-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3814-139">Requirements</span></span>



| <span data-ttu-id="b3814-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3814-140">Requirement</span></span> | <span data-ttu-id="b3814-141">Value</span><span class="sxs-lookup"><span data-stu-id="b3814-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b3814-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b3814-142">Minimum supported client</span></span><br/> | <span data-ttu-id="b3814-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b3814-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b3814-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b3814-144">Minimum supported server</span></span><br/> | <span data-ttu-id="b3814-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b3814-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b3814-146">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b3814-146">Namespace</span></span><br/>                | <span data-ttu-id="b3814-147">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="b3814-147">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b3814-148">MOF</span><span class="sxs-lookup"><span data-stu-id="b3814-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b3814-149"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b3814-149"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b3814-150">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b3814-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3814-151"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3814-151"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3814-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="b3814-152">See also</span></span>

<dl> <dt>

<span data-ttu-id="b3814-153">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b3814-153">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="b3814-154">**Win32 \_ CodecFile**</span><span class="sxs-lookup"><span data-stu-id="b3814-154">**Win32\_CodecFile**</span></span>](win32-codecfile.md)
</dt> </dl>

 

