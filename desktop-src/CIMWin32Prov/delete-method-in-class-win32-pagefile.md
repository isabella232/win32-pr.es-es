---
description: 'Método Delete de la Win32_PageFile : elimina el archivo de paginación lógico (o directorio) especificado en la ruta de acceso del objeto.'
ms.assetid: cc36d621-597e-4343-8bf6-bfca7fa29276
ms.tgt_platform: multiple
title: Método Delete de la Win32_PageFile clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8b35751633387f3db1d7dccbf13694f56717a1d3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089602"
---
# <a name="delete-method-of-the-win32_pagefile-class"></a><span data-ttu-id="e22c3-103">Método Delete de la clase PageFile de Win32 \_</span><span class="sxs-lookup"><span data-stu-id="e22c3-103">Delete method of the Win32\_PageFile class</span></span>

<span data-ttu-id="e22c3-104">El **método de** clase WMI [Delete](/windows/desktop/WmiSdk/retrieving-a-class) elimina el archivo lógico de paginación (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="e22c3-104">The **Delete** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method deletes the logical paging file (or directory) specified in the object path.</span></span>

<span data-ttu-id="e22c3-105">En este tema se Managed Object Format sintaxis de MOF .</span><span class="sxs-lookup"><span data-stu-id="e22c3-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="e22c3-106">Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="e22c3-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="e22c3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e22c3-107">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="e22c3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e22c3-108">Parameters</span></span>

<span data-ttu-id="e22c3-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="e22c3-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e22c3-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e22c3-110">Return value</span></span>

<span data-ttu-id="e22c3-111">Devuelve un valor de 0 (cero) si el archivo se eliminó correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="e22c3-111">Returns a value of 0 (zero) if the file was successfully deleted, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="e22c3-112">**0**</span><span class="sxs-lookup"><span data-stu-id="e22c3-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="e22c3-113">La solicitud fue correcta.</span><span class="sxs-lookup"><span data-stu-id="e22c3-113">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="e22c3-114">**2**</span><span class="sxs-lookup"><span data-stu-id="e22c3-114">**2**</span></span>
</dt> <dd>

<span data-ttu-id="e22c3-115">Se denegó el acceso.</span><span class="sxs-lookup"><span data-stu-id="e22c3-115">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="e22c3-116">**8**</span><span class="sxs-lookup"><span data-stu-id="e22c3-116">**8**</span></span>
</dt> <dd>

<span data-ttu-id="e22c3-117">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="e22c3-117">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="e22c3-118">**9**</span><span class="sxs-lookup"><span data-stu-id="e22c3-118">**9**</span></span>
</dt> <dd>

<span data-ttu-id="e22c3-119">El nombre especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="e22c3-119">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="e22c3-120">**10**</span><span class="sxs-lookup"><span data-stu-id="e22c3-120">**10**</span></span>
</dt> <dd>

<span data-ttu-id="e22c3-121">El objeto especificado ya existe.</span><span class="sxs-lookup"><span data-stu-id="e22c3-121">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="e22c3-122">**11**</span><span class="sxs-lookup"><span data-stu-id="e22c3-122">**11**</span></span>
</dt> <dd>

<span data-ttu-id="e22c3-123">El sistema de archivos no es NTFS.</span><span class="sxs-lookup"><span data-stu-id="e22c3-123">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="e22c3-124">**12**</span><span class="sxs-lookup"><span data-stu-id="e22c3-124">**12**</span></span>
</dt> <dd>

<span data-ttu-id="e22c3-125">La plataforma no es Windows.</span><span class="sxs-lookup"><span data-stu-id="e22c3-125">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="e22c3-126">**13**</span><span class="sxs-lookup"><span data-stu-id="e22c3-126">**13**</span></span>
</dt> <dd>

<span data-ttu-id="e22c3-127">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="e22c3-127">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="e22c3-128">**14**</span><span class="sxs-lookup"><span data-stu-id="e22c3-128">**14**</span></span>
</dt> <dd>

<span data-ttu-id="e22c3-129">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="e22c3-129">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="e22c3-130">**15**</span><span class="sxs-lookup"><span data-stu-id="e22c3-130">**15**</span></span>
</dt> <dd>

<span data-ttu-id="e22c3-131">Se ha infringido el uso compartido.</span><span class="sxs-lookup"><span data-stu-id="e22c3-131">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="e22c3-132">**16**</span><span class="sxs-lookup"><span data-stu-id="e22c3-132">**16**</span></span>
</dt> <dd>

<span data-ttu-id="e22c3-133">El archivo de inicio especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="e22c3-133">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="e22c3-134">**17**</span><span class="sxs-lookup"><span data-stu-id="e22c3-134">**17**</span></span>
</dt> <dd>

<span data-ttu-id="e22c3-135">No se mantiene un privilegio necesario para la operación.</span><span class="sxs-lookup"><span data-stu-id="e22c3-135">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="e22c3-136">**21**</span><span class="sxs-lookup"><span data-stu-id="e22c3-136">**21**</span></span>
</dt> <dd>

<span data-ttu-id="e22c3-137">Un parámetro especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="e22c3-137">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e22c3-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e22c3-138">Requirements</span></span>



| <span data-ttu-id="e22c3-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="e22c3-139">Requirement</span></span> | <span data-ttu-id="e22c3-140">Valor</span><span class="sxs-lookup"><span data-stu-id="e22c3-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e22c3-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e22c3-141">Minimum supported client</span></span><br/> | <span data-ttu-id="e22c3-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e22c3-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e22c3-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e22c3-143">Minimum supported server</span></span><br/> | <span data-ttu-id="e22c3-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e22c3-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e22c3-145">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e22c3-145">Namespace</span></span><br/>                | <span data-ttu-id="e22c3-146">\\CIMV2 raíz</span><span class="sxs-lookup"><span data-stu-id="e22c3-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e22c3-147">MOF</span><span class="sxs-lookup"><span data-stu-id="e22c3-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e22c3-148"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="e22c3-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e22c3-149">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e22c3-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e22c3-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e22c3-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e22c3-151">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e22c3-151">See also</span></span>

<dl> <dt>

<span data-ttu-id="e22c3-152">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e22c3-152">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="e22c3-153">**Win32 \_ PageFile**</span><span class="sxs-lookup"><span data-stu-id="e22c3-153">**Win32\_PageFile**</span></span>](win32-pagefile.md)
</dt> </dl>

 

