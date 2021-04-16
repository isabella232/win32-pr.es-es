---
description: Obtiene la propiedad del archivo de entrada de directorio lógico especificado en la ruta de acceso del objeto. Este método es una versión extendida del método TakeOwnerShip.
ms.assetid: 73726207-e885-4957-bff8-6903c4b99278
ms.tgt_platform: multiple
title: Método TakeOwnerShipEx de la clase Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.TakeOwnerShipEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2e391e942e581d0f80d46b0f59b9b273d7bff499
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659360"
---
# <a name="takeownershipex-method-of-the-win32_directory-class"></a><span data-ttu-id="f371c-104">Método TakeOwnerShipEx de la \_ clase de directorio Win32</span><span class="sxs-lookup"><span data-stu-id="f371c-104">TakeOwnerShipEx method of the Win32\_Directory class</span></span>

<span data-ttu-id="f371c-105">El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **TakeOwnerShipEx** obtiene la propiedad del archivo de entrada de directorio lógico especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="f371c-105">The **TakeOwnerShipEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method obtains ownership of the logical directory entry file specified in the object path.</span></span> <span data-ttu-id="f371c-106">Este método es una versión extendida del método [**TakeOwnerShip**](takeownership-method-in-class-win32-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="f371c-106">This method is an extended version of the [**TakeOwnerShip**](takeownership-method-in-class-win32-directory.md) method.</span></span> <span data-ttu-id="f371c-107">Si el archivo lógico es realmente un directorio, este método actúa de forma recursiva y toma la propiedad de todos los archivos y subdirectorios que contiene el directorio.</span><span class="sxs-lookup"><span data-stu-id="f371c-107">If the logical file is actually a directory, then this method acts recursively, taking ownership of all of the files and subdirectories the directory contains.</span></span>

<span data-ttu-id="f371c-108">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="f371c-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f371c-109">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="f371c-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f371c-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f371c-110">Syntax</span></span>


```mof
uint32 TakeOwnerShipEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="f371c-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f371c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f371c-112">*StopFileName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f371c-112">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f371c-113">Nombre del archivo o directorio en el que se produjo un error en el método **TakeOwnerShipEx** .</span><span class="sxs-lookup"><span data-stu-id="f371c-113">Name of the file or directory where the **TakeOwnerShipEx** method failed.</span></span> <span data-ttu-id="f371c-114">Este parámetro es **null** si el método se ejecuta correctamente.</span><span class="sxs-lookup"><span data-stu-id="f371c-114">This parameter is **NULL** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="f371c-115">*StartFileName* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="f371c-115">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f371c-116">Asigna un nombre al archivo o directorio secundario que se va a usar como punto de partida para **TakeOwnerShipEx**.</span><span class="sxs-lookup"><span data-stu-id="f371c-116">Names the child file or directory to use as a starting point for **TakeOwnerShipEx**.</span></span> <span data-ttu-id="f371c-117">El parámetro *StartFileName* es normalmente el parámetro *StopFileName* que especifica el archivo o directorio en el que se produjo un error de la llamada al método anterior.</span><span class="sxs-lookup"><span data-stu-id="f371c-117">The *StartFileName* parameter is typically the *StopFileName* parameter that specifies the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="f371c-118">Si este parámetro es **null**, la operación se realiza en el archivo o directorio especificado en la llamada [**ExecMethod**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="f371c-118">If this parameter is **NULL**, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execmethod) call.</span></span>

<span data-ttu-id="f371c-119">Si se utiliza *StartFileName* , *Recursive* también debe establecerse en true.</span><span class="sxs-lookup"><span data-stu-id="f371c-119">If *StartFileName* is used, *Recursive* must be set to true as well.</span></span>

</dd> <dt>

<span data-ttu-id="f371c-120">*Recursivo* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="f371c-120">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f371c-121">Si es **true**, el cambio de propiedad se aplica de forma recursiva a los archivos y directorios del directorio especificado por la instancia de [**\_ LogicalFile de CIM**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="f371c-121">If **True**, the change of ownership is applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span>

> [!Note]  
> <span data-ttu-id="f371c-122">En el caso de las instancias de archivo, se omite el parámetro de entrada *recursivo* .</span><span class="sxs-lookup"><span data-stu-id="f371c-122">For file instances, the *Recursive* input parameter is ignored.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f371c-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f371c-123">Return value</span></span>

<span data-ttu-id="f371c-124">Devuelve un valor entero de 0 (cero) si se realiza correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="f371c-124">Returns an integer value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="f371c-125">**0**</span><span class="sxs-lookup"><span data-stu-id="f371c-125">**0**</span></span>
</dt> <dd>

<span data-ttu-id="f371c-126">La solicitud fue correcta.</span><span class="sxs-lookup"><span data-stu-id="f371c-126">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="f371c-127">**2**</span><span class="sxs-lookup"><span data-stu-id="f371c-127">**2**</span></span>
</dt> <dd>

<span data-ttu-id="f371c-128">Se denegó el acceso.</span><span class="sxs-lookup"><span data-stu-id="f371c-128">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="f371c-129">**8**</span><span class="sxs-lookup"><span data-stu-id="f371c-129">**8**</span></span>
</dt> <dd>

<span data-ttu-id="f371c-130">Se produjo un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="f371c-130">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="f371c-131">**9**</span><span class="sxs-lookup"><span data-stu-id="f371c-131">**9**</span></span>
</dt> <dd>

<span data-ttu-id="f371c-132">El nombre especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="f371c-132">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="f371c-133">**10**</span><span class="sxs-lookup"><span data-stu-id="f371c-133">**10**</span></span>
</dt> <dd>

<span data-ttu-id="f371c-134">El objeto especificado ya existe.</span><span class="sxs-lookup"><span data-stu-id="f371c-134">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="f371c-135">**11**</span><span class="sxs-lookup"><span data-stu-id="f371c-135">**11**</span></span>
</dt> <dd>

<span data-ttu-id="f371c-136">El sistema de archivos no es NTFS.</span><span class="sxs-lookup"><span data-stu-id="f371c-136">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="f371c-137">**12**</span><span class="sxs-lookup"><span data-stu-id="f371c-137">**12**</span></span>
</dt> <dd>

<span data-ttu-id="f371c-138">La plataforma no es Windows.</span><span class="sxs-lookup"><span data-stu-id="f371c-138">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="f371c-139">**13**</span><span class="sxs-lookup"><span data-stu-id="f371c-139">**13**</span></span>
</dt> <dd>

<span data-ttu-id="f371c-140">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="f371c-140">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="f371c-141">**14**</span><span class="sxs-lookup"><span data-stu-id="f371c-141">**14**</span></span>
</dt> <dd>

<span data-ttu-id="f371c-142">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="f371c-142">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="f371c-143">**15**</span><span class="sxs-lookup"><span data-stu-id="f371c-143">**15**</span></span>
</dt> <dd>

<span data-ttu-id="f371c-144">Se ha producido una infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="f371c-144">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="f371c-145">**16**</span><span class="sxs-lookup"><span data-stu-id="f371c-145">**16**</span></span>
</dt> <dd>

<span data-ttu-id="f371c-146">El archivo de inicio especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="f371c-146">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="f371c-147">**17**</span><span class="sxs-lookup"><span data-stu-id="f371c-147">**17**</span></span>
</dt> <dd>

<span data-ttu-id="f371c-148">No se mantiene un privilegio necesario para la operación.</span><span class="sxs-lookup"><span data-stu-id="f371c-148">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="f371c-149">**21**</span><span class="sxs-lookup"><span data-stu-id="f371c-149">**21**</span></span>
</dt> <dd>

<span data-ttu-id="f371c-150">Un parámetro especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="f371c-150">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="f371c-151">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f371c-151">Examples</span></span>

<span data-ttu-id="f371c-152">El siguiente código de script de Visual Basic llama al método [**TakeOwnerShipEx**](takeownershipex-method-in-class-cim-directory.md) para tomar posesión de la \\ carpeta C: Temp.</span><span class="sxs-lookup"><span data-stu-id="f371c-152">The following Visual Basic Script code calls the [**TakeOwnerShipEx**](takeownershipex-method-in-class-cim-directory.md) method to take ownership of the C:\\temp folder.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
' Obtain the definition of the class.
Set objShare = objWMIService.Get("Win32_Directory")
' Obtain an InParameters object specific
' to the method.
Set objInParam = objShare.Methods_("TakeOwnerShipEx").inParameters.SpawnInstance_()

' Add the input parameters.
objInParam.Properties_.Item("Recursive") =  true

' Execute the method and obtain the return status.
' The OutParameters object in objOutParams
' is created by the provider.
Set objOutParams = objWMIService.ExecMethod("Win32_Directory.Name='C:\Temp'", "TakeOwnerShipEx", objInParam)
wscript.echo objOutParams.ReturnValue
```



## <a name="requirements"></a><span data-ttu-id="f371c-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f371c-153">Requirements</span></span>



| <span data-ttu-id="f371c-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="f371c-154">Requirement</span></span> | <span data-ttu-id="f371c-155">Value</span><span class="sxs-lookup"><span data-stu-id="f371c-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f371c-156">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f371c-156">Minimum supported client</span></span><br/> | <span data-ttu-id="f371c-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f371c-157">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f371c-158">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f371c-158">Minimum supported server</span></span><br/> | <span data-ttu-id="f371c-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f371c-159">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f371c-160">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f371c-160">Namespace</span></span><br/>                | <span data-ttu-id="f371c-161">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="f371c-161">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f371c-162">MOF</span><span class="sxs-lookup"><span data-stu-id="f371c-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f371c-163"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f371c-163"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f371c-164">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f371c-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f371c-165"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f371c-165"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f371c-166">Vea también</span><span class="sxs-lookup"><span data-stu-id="f371c-166">See also</span></span>

<dl> <dt>

<span data-ttu-id="f371c-167">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f371c-167">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="f371c-168">**\_Directorio Win32**</span><span class="sxs-lookup"><span data-stu-id="f371c-168">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

