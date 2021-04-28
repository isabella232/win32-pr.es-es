---
description: 'Método DeleteEx de la Win32_PageFile : elimina el archivo de paginación lógico (o directorio) especificado en la ruta de acceso del objeto.'
ms.assetid: ea31f92a-94b9-4d4d-abd9-6c304ac5caee
ms.tgt_platform: multiple
title: Método DeleteEx de la Win32_PageFile clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.DeleteEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 34e27e80c3cfaea352ee97ad29aed0b7ca358546
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097053"
---
# <a name="deleteex-method-of-the-win32_pagefile-class"></a><span data-ttu-id="37b6e-103">Método DeleteEx de la clase PageFile de Win32 \_</span><span class="sxs-lookup"><span data-stu-id="37b6e-103">DeleteEx method of the Win32\_PageFile class</span></span>

<span data-ttu-id="37b6e-104">El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **DeleteEx** elimina el archivo de paginación lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="37b6e-104">The **DeleteEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method deletes the logical paging file (or directory) specified in the object path.</span></span> <span data-ttu-id="37b6e-105">**DeleteEx** es una versión extendida del [**método Delete.**](delete-method-in-class-win32-directory.md)</span><span class="sxs-lookup"><span data-stu-id="37b6e-105">**DeleteEx** is an extended version of the [**Delete**](delete-method-in-class-win32-directory.md) method.</span></span>

<span data-ttu-id="37b6e-106">En este tema se usa Managed Object Format sintaxis MOF .</span><span class="sxs-lookup"><span data-stu-id="37b6e-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="37b6e-107">Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="37b6e-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="37b6e-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="37b6e-108">Syntax</span></span>


```mof
uint32 DeleteEx(
  [out]          string StopFileName,
  [in, optional] string StartFileName
);
```



## <a name="parameters"></a><span data-ttu-id="37b6e-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="37b6e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37b6e-110">*StopFileName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="37b6e-110">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="37b6e-111">Nombre del archivo o directorio en el que se ha fallado **el método DeleteEx.**</span><span class="sxs-lookup"><span data-stu-id="37b6e-111">Name of the file or directory where the **DeleteEx** method failed.</span></span> <span data-ttu-id="37b6e-112">Este parámetro es **NULL** si el método se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="37b6e-112">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="37b6e-113">*StartFileName* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="37b6e-113">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="37b6e-114">Denomina el archivo o directorio secundario que se usará como punto de partida para **DeleteEx.**</span><span class="sxs-lookup"><span data-stu-id="37b6e-114">Names the child file or directory to use as a starting point for **DeleteEx**.</span></span> <span data-ttu-id="37b6e-115">El *parámetro StartFileName* suele ser el *parámetro StopFileName* que especifica el archivo o directorio en el que se produjo un error de la llamada al método anterior.</span><span class="sxs-lookup"><span data-stu-id="37b6e-115">The *StartFileName* parameter is typically the *StopFileName* parameter that specifies the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="37b6e-116">Si este parámetro es **NULL,** la operación se realiza en el archivo o directorio especificado en la llamada a ExecMethod.</span><span class="sxs-lookup"><span data-stu-id="37b6e-116">If this parameter is **NULL**, the operation is performed on the file or directory specified in the ExecMethod call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37b6e-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="37b6e-117">Return value</span></span>

<span data-ttu-id="37b6e-118">Devuelve un valor de 0 (cero) si el archivo se eliminó correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="37b6e-118">Returns a value of 0 (zero) if the file was successfully deleted, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="37b6e-119">**0**</span><span class="sxs-lookup"><span data-stu-id="37b6e-119">**0**</span></span>
</dt> <dd>

<span data-ttu-id="37b6e-120">La solicitud fue correcta.</span><span class="sxs-lookup"><span data-stu-id="37b6e-120">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="37b6e-121">**2**</span><span class="sxs-lookup"><span data-stu-id="37b6e-121">**2**</span></span>
</dt> <dd>

<span data-ttu-id="37b6e-122">Se denegó el acceso.</span><span class="sxs-lookup"><span data-stu-id="37b6e-122">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="37b6e-123">**8**</span><span class="sxs-lookup"><span data-stu-id="37b6e-123">**8**</span></span>
</dt> <dd>

<span data-ttu-id="37b6e-124">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="37b6e-124">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="37b6e-125">**9**</span><span class="sxs-lookup"><span data-stu-id="37b6e-125">**9**</span></span>
</dt> <dd>

<span data-ttu-id="37b6e-126">El nombre especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="37b6e-126">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="37b6e-127">**10**</span><span class="sxs-lookup"><span data-stu-id="37b6e-127">**10**</span></span>
</dt> <dd>

<span data-ttu-id="37b6e-128">El objeto especificado ya existe.</span><span class="sxs-lookup"><span data-stu-id="37b6e-128">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="37b6e-129">**11**</span><span class="sxs-lookup"><span data-stu-id="37b6e-129">**11**</span></span>
</dt> <dd>

<span data-ttu-id="37b6e-130">El sistema de archivos no es NTFS.</span><span class="sxs-lookup"><span data-stu-id="37b6e-130">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="37b6e-131">**12**</span><span class="sxs-lookup"><span data-stu-id="37b6e-131">**12**</span></span>
</dt> <dd>

<span data-ttu-id="37b6e-132">La plataforma no es Windows.</span><span class="sxs-lookup"><span data-stu-id="37b6e-132">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="37b6e-133">**13**</span><span class="sxs-lookup"><span data-stu-id="37b6e-133">**13**</span></span>
</dt> <dd>

<span data-ttu-id="37b6e-134">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="37b6e-134">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="37b6e-135">**14**</span><span class="sxs-lookup"><span data-stu-id="37b6e-135">**14**</span></span>
</dt> <dd>

<span data-ttu-id="37b6e-136">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="37b6e-136">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="37b6e-137">**15**</span><span class="sxs-lookup"><span data-stu-id="37b6e-137">**15**</span></span>
</dt> <dd>

<span data-ttu-id="37b6e-138">Se ha infringido el uso compartido.</span><span class="sxs-lookup"><span data-stu-id="37b6e-138">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="37b6e-139">**16**</span><span class="sxs-lookup"><span data-stu-id="37b6e-139">**16**</span></span>
</dt> <dd>

<span data-ttu-id="37b6e-140">El archivo de inicio especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="37b6e-140">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="37b6e-141">**17**</span><span class="sxs-lookup"><span data-stu-id="37b6e-141">**17**</span></span>
</dt> <dd>

<span data-ttu-id="37b6e-142">No se mantiene un privilegio necesario para la operación.</span><span class="sxs-lookup"><span data-stu-id="37b6e-142">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="37b6e-143">**21**</span><span class="sxs-lookup"><span data-stu-id="37b6e-143">**21**</span></span>
</dt> <dd>

<span data-ttu-id="37b6e-144">Un parámetro especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="37b6e-144">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="37b6e-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37b6e-145">Requirements</span></span>



| <span data-ttu-id="37b6e-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="37b6e-146">Requirement</span></span> | <span data-ttu-id="37b6e-147">Valor</span><span class="sxs-lookup"><span data-stu-id="37b6e-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="37b6e-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="37b6e-148">Minimum supported client</span></span><br/> | <span data-ttu-id="37b6e-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="37b6e-149">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="37b6e-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="37b6e-150">Minimum supported server</span></span><br/> | <span data-ttu-id="37b6e-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="37b6e-151">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="37b6e-152">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="37b6e-152">Namespace</span></span><br/>                | <span data-ttu-id="37b6e-153">\\CIMV2 raíz</span><span class="sxs-lookup"><span data-stu-id="37b6e-153">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="37b6e-154">MOF</span><span class="sxs-lookup"><span data-stu-id="37b6e-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="37b6e-155"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="37b6e-155"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="37b6e-156">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="37b6e-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37b6e-157"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37b6e-157"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37b6e-158">Consulte también</span><span class="sxs-lookup"><span data-stu-id="37b6e-158">See also</span></span>

<dl> <dt>

<span data-ttu-id="37b6e-159">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="37b6e-159">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="37b6e-160">**Win32 \_ PageFile**</span><span class="sxs-lookup"><span data-stu-id="37b6e-160">**Win32\_PageFile**</span></span>](win32-pagefile.md)
</dt> </dl>

 

