---
description: 'Método TakeOwnerShip de la clase Win32_ShortcutFile : el&\# 8194; El método de clase WMI obtiene la propiedad del archivo lógico especificado en la ruta de acceso del objeto.'
ms.assetid: 1a8ff156-50b2-4550-abcc-7a6ae0e4630f
ms.tgt_platform: multiple
title: Método TakeOwnerShip de la Win32_ShortcutFile clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile.TakeOwnerShip
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 36364a55276842518480c3d3d37c57c3ae0a06ba
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086003"
---
# <a name="takeownership-method-of-the-win32_shortcutfile-class"></a><span data-ttu-id="d9543-103">Método TakeOwnerShip de la clase ShortcutFile de Win32 \_</span><span class="sxs-lookup"><span data-stu-id="d9543-103">TakeOwnerShip method of the Win32\_ShortcutFile class</span></span>

<span data-ttu-id="d9543-104">El método de clase [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **TakeOwnerShip** obtiene la propiedad del archivo lógico especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="d9543-104">The **TakeOwnerShip** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="d9543-105">Si el archivo lógico es realmente un directorio, **TakeOwnerShip** actúa de forma recursiva, tomando posesión de todos los archivos y subdirectorios que contiene el directorio.</span><span class="sxs-lookup"><span data-stu-id="d9543-105">If the logical file is actually a directory, then **TakeOwnerShip** acts recursively, taking ownership of all the files and subdirectories the directory contains.</span></span>

<span data-ttu-id="d9543-106">En este tema se usa Managed Object Format sintaxis MOF .</span><span class="sxs-lookup"><span data-stu-id="d9543-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="d9543-107">Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="d9543-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="d9543-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d9543-108">Syntax</span></span>


```mof
uint32 TakeOwnerShip();
```



## <a name="parameters"></a><span data-ttu-id="d9543-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d9543-109">Parameters</span></span>

<span data-ttu-id="d9543-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="d9543-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d9543-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d9543-111">Return value</span></span>

<span data-ttu-id="d9543-112">Devuelve uno de los siguientes valores enteros.</span><span class="sxs-lookup"><span data-stu-id="d9543-112">Returns one of the following integer values.</span></span>

<dl> <dt>

<span data-ttu-id="d9543-113">**0**</span><span class="sxs-lookup"><span data-stu-id="d9543-113">**0**</span></span>
</dt> <dd>

<span data-ttu-id="d9543-114">La solicitud fue correcta.</span><span class="sxs-lookup"><span data-stu-id="d9543-114">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="d9543-115">**2**</span><span class="sxs-lookup"><span data-stu-id="d9543-115">**2**</span></span>
</dt> <dd>

<span data-ttu-id="d9543-116">Se denegó el acceso.</span><span class="sxs-lookup"><span data-stu-id="d9543-116">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="d9543-117">**8**</span><span class="sxs-lookup"><span data-stu-id="d9543-117">**8**</span></span>
</dt> <dd>

<span data-ttu-id="d9543-118">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="d9543-118">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="d9543-119">**9**</span><span class="sxs-lookup"><span data-stu-id="d9543-119">**9**</span></span>
</dt> <dd>

<span data-ttu-id="d9543-120">El nombre especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="d9543-120">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="d9543-121">**10**</span><span class="sxs-lookup"><span data-stu-id="d9543-121">**10**</span></span>
</dt> <dd>

<span data-ttu-id="d9543-122">El objeto especificado ya existe.</span><span class="sxs-lookup"><span data-stu-id="d9543-122">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="d9543-123">**11**</span><span class="sxs-lookup"><span data-stu-id="d9543-123">**11**</span></span>
</dt> <dd>

<span data-ttu-id="d9543-124">El sistema de archivos no es NTFS.</span><span class="sxs-lookup"><span data-stu-id="d9543-124">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="d9543-125">**12**</span><span class="sxs-lookup"><span data-stu-id="d9543-125">**12**</span></span>
</dt> <dd>

<span data-ttu-id="d9543-126">La plataforma no es Windows.</span><span class="sxs-lookup"><span data-stu-id="d9543-126">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="d9543-127">**13**</span><span class="sxs-lookup"><span data-stu-id="d9543-127">**13**</span></span>
</dt> <dd>

<span data-ttu-id="d9543-128">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="d9543-128">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="d9543-129">**14**</span><span class="sxs-lookup"><span data-stu-id="d9543-129">**14**</span></span>
</dt> <dd>

<span data-ttu-id="d9543-130">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="d9543-130">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="d9543-131">**15**</span><span class="sxs-lookup"><span data-stu-id="d9543-131">**15**</span></span>
</dt> <dd>

<span data-ttu-id="d9543-132">Ha habido una infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="d9543-132">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="d9543-133">**16**</span><span class="sxs-lookup"><span data-stu-id="d9543-133">**16**</span></span>
</dt> <dd>

<span data-ttu-id="d9543-134">El archivo de inicio especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="d9543-134">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="d9543-135">**17**</span><span class="sxs-lookup"><span data-stu-id="d9543-135">**17**</span></span>
</dt> <dd>

<span data-ttu-id="d9543-136">No se mantiene un privilegio necesario para la operación.</span><span class="sxs-lookup"><span data-stu-id="d9543-136">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="d9543-137">**21**</span><span class="sxs-lookup"><span data-stu-id="d9543-137">**21**</span></span>
</dt> <dd>

<span data-ttu-id="d9543-138">Un parámetro especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="d9543-138">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d9543-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9543-139">Requirements</span></span>



| <span data-ttu-id="d9543-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9543-140">Requirement</span></span> | <span data-ttu-id="d9543-141">Valor</span><span class="sxs-lookup"><span data-stu-id="d9543-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d9543-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d9543-142">Minimum supported client</span></span><br/> | <span data-ttu-id="d9543-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d9543-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d9543-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d9543-144">Minimum supported server</span></span><br/> | <span data-ttu-id="d9543-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d9543-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d9543-146">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d9543-146">Namespace</span></span><br/>                | <span data-ttu-id="d9543-147">\\CIMV2 raíz</span><span class="sxs-lookup"><span data-stu-id="d9543-147">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d9543-148">MOF</span><span class="sxs-lookup"><span data-stu-id="d9543-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d9543-149"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="d9543-149"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d9543-150">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d9543-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d9543-151"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9543-151"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9543-152">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d9543-152">See also</span></span>

<dl> <dt>

<span data-ttu-id="d9543-153">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d9543-153">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d9543-154">**Win32 \_ ShortcutFile**</span><span class="sxs-lookup"><span data-stu-id="d9543-154">**Win32\_ShortcutFile**</span></span>](win32-shortcutfile.md)
</dt> </dl>

 

