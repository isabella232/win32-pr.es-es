---
description: 'Método TakeOwnerShip de la clase Win32_Directory : el método de clase WMI TakeOwnerShip obtiene la propiedad del archivo lógico especificado en la ruta de acceso del objeto.'
ms.assetid: 1112823b-0bb6-4dc0-a5c4-8d3839a47a3a
ms.tgt_platform: multiple
title: Método TakeOwnerShip de la Win32_Directory clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.TakeOwnerShip
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 178f1bf523d939883a7fc18b5bdbd7142cc4f824
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086033"
---
# <a name="takeownership-method-of-the-win32_directory-class"></a><span data-ttu-id="17cfd-103">Método TakeOwnerShip de la clase Directory de \_ Win32</span><span class="sxs-lookup"><span data-stu-id="17cfd-103">TakeOwnerShip method of the Win32\_Directory class</span></span>

<span data-ttu-id="17cfd-104">El método de clase [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **TakeOwnerShip** obtiene la propiedad del archivo lógico especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="17cfd-104">The **TakeOwnerShip** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="17cfd-105">Si el archivo lógico es realmente un directorio, **TakeOwnerShip** actúa de forma recursiva, tomando posesión de todos los archivos y subdirectorios que contiene el directorio.</span><span class="sxs-lookup"><span data-stu-id="17cfd-105">If the logical file is actually a directory, then **TakeOwnerShip** acts recursively, taking ownership of all of the files and subdirectories the directory contains.</span></span>

<span data-ttu-id="17cfd-106">En este tema se usa Managed Object Format sintaxis MOF .</span><span class="sxs-lookup"><span data-stu-id="17cfd-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="17cfd-107">Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="17cfd-107">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="17cfd-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="17cfd-108">Syntax</span></span>


```mof
uint32 TakeOwnerShip();
```



## <a name="parameters"></a><span data-ttu-id="17cfd-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="17cfd-109">Parameters</span></span>

<span data-ttu-id="17cfd-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="17cfd-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="17cfd-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="17cfd-111">Return value</span></span>

<span data-ttu-id="17cfd-112">Devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="17cfd-112">Returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="17cfd-113">**0**</span><span class="sxs-lookup"><span data-stu-id="17cfd-113">**0**</span></span>
</dt> <dd>

<span data-ttu-id="17cfd-114">La solicitud fue correcta.</span><span class="sxs-lookup"><span data-stu-id="17cfd-114">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="17cfd-115">**2**</span><span class="sxs-lookup"><span data-stu-id="17cfd-115">**2**</span></span>
</dt> <dd>

<span data-ttu-id="17cfd-116">Se denegó el acceso.</span><span class="sxs-lookup"><span data-stu-id="17cfd-116">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="17cfd-117">**8**</span><span class="sxs-lookup"><span data-stu-id="17cfd-117">**8**</span></span>
</dt> <dd>

<span data-ttu-id="17cfd-118">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="17cfd-118">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="17cfd-119">**9**</span><span class="sxs-lookup"><span data-stu-id="17cfd-119">**9**</span></span>
</dt> <dd>

<span data-ttu-id="17cfd-120">El nombre especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="17cfd-120">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="17cfd-121">**10**</span><span class="sxs-lookup"><span data-stu-id="17cfd-121">**10**</span></span>
</dt> <dd>

<span data-ttu-id="17cfd-122">El objeto especificado ya existe.</span><span class="sxs-lookup"><span data-stu-id="17cfd-122">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="17cfd-123">**11**</span><span class="sxs-lookup"><span data-stu-id="17cfd-123">**11**</span></span>
</dt> <dd>

<span data-ttu-id="17cfd-124">El sistema de archivos no es NTFS.</span><span class="sxs-lookup"><span data-stu-id="17cfd-124">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="17cfd-125">**12**</span><span class="sxs-lookup"><span data-stu-id="17cfd-125">**12**</span></span>
</dt> <dd>

<span data-ttu-id="17cfd-126">La plataforma no es Windows.</span><span class="sxs-lookup"><span data-stu-id="17cfd-126">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="17cfd-127">**13**</span><span class="sxs-lookup"><span data-stu-id="17cfd-127">**13**</span></span>
</dt> <dd>

<span data-ttu-id="17cfd-128">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="17cfd-128">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="17cfd-129">**14**</span><span class="sxs-lookup"><span data-stu-id="17cfd-129">**14**</span></span>
</dt> <dd>

<span data-ttu-id="17cfd-130">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="17cfd-130">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="17cfd-131">**15**</span><span class="sxs-lookup"><span data-stu-id="17cfd-131">**15**</span></span>
</dt> <dd>

<span data-ttu-id="17cfd-132">Ha habido una infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="17cfd-132">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="17cfd-133">**16**</span><span class="sxs-lookup"><span data-stu-id="17cfd-133">**16**</span></span>
</dt> <dd>

<span data-ttu-id="17cfd-134">El archivo de inicio especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="17cfd-134">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="17cfd-135">**17**</span><span class="sxs-lookup"><span data-stu-id="17cfd-135">**17**</span></span>
</dt> <dd>

<span data-ttu-id="17cfd-136">No se mantiene un privilegio necesario para la operación.</span><span class="sxs-lookup"><span data-stu-id="17cfd-136">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="17cfd-137">**21**</span><span class="sxs-lookup"><span data-stu-id="17cfd-137">**21**</span></span>
</dt> <dd>

<span data-ttu-id="17cfd-138">Un parámetro especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="17cfd-138">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="17cfd-139">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="17cfd-139">Examples</span></span>

<span data-ttu-id="17cfd-140">El siguiente Visual Basic script llama al [**método TakeOwnerShip**](takeownership-method-in-class-cim-directory.md) para tomar posesión de la carpeta \\ temporal C:.</span><span class="sxs-lookup"><span data-stu-id="17cfd-140">The following Visual Basic Script code calls the [**TakeOwnerShip**](takeownership-method-in-class-cim-directory.md) method to take ownership of the C:\\temp folder.</span></span>


```VB
strComputer = "." 

Set objWMIService = _
    GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 

' Obtain the definition of the class.
Set objShare = objWMIService.Get("Win32_Directory")

' Execute the method and obtain the return status.
' The OutParameters object in objOutParams
' is created by the provider.
Set objOutParams = objWMIService.ExecMethod( _
    "Win32_Directory.Name='C:\\temp'", "TakeOwnerShip")

wscript.echo objOutParams.ReturnValue
```



## <a name="requirements"></a><span data-ttu-id="17cfd-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17cfd-141">Requirements</span></span>



| <span data-ttu-id="17cfd-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="17cfd-142">Requirement</span></span> | <span data-ttu-id="17cfd-143">Valor</span><span class="sxs-lookup"><span data-stu-id="17cfd-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="17cfd-144">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="17cfd-144">Minimum supported client</span></span><br/> | <span data-ttu-id="17cfd-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="17cfd-145">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="17cfd-146">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="17cfd-146">Minimum supported server</span></span><br/> | <span data-ttu-id="17cfd-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="17cfd-147">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="17cfd-148">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="17cfd-148">Namespace</span></span><br/>                | <span data-ttu-id="17cfd-149">\\CIMV2 raíz</span><span class="sxs-lookup"><span data-stu-id="17cfd-149">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="17cfd-150">MOF</span><span class="sxs-lookup"><span data-stu-id="17cfd-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="17cfd-151"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="17cfd-151"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="17cfd-152">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="17cfd-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17cfd-153"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17cfd-153"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17cfd-154">Consulte también</span><span class="sxs-lookup"><span data-stu-id="17cfd-154">See also</span></span>

<dl> <dt>

<span data-ttu-id="17cfd-155">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="17cfd-155">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="17cfd-156">**Directorio \_ win32**</span><span class="sxs-lookup"><span data-stu-id="17cfd-156">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

