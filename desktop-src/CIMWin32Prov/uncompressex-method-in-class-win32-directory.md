---
description: Descomprime el archivo de entrada de directorio lógico (o directorio) especificado en la ruta de acceso del objeto. Este método es una versión extendida del método UNCOMPRESS.
ms.assetid: cd18d8b7-ab63-475c-a3a6-79611c9e032d
ms.tgt_platform: multiple
title: Método UncompressEx de la clase Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.UncompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a0fd02d0757745199249d64fa08d73f8b5ec65a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153438"
---
# <a name="uncompressex-method-of-the-win32_directory-class"></a><span data-ttu-id="1cea5-104">Método UncompressEx de la \_ clase de directorio Win32</span><span class="sxs-lookup"><span data-stu-id="1cea5-104">UncompressEx method of the Win32\_Directory class</span></span>

<span data-ttu-id="1cea5-105">El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **UncompressEx** descomprime el archivo de entrada de directorio lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="1cea5-105">The **UncompressEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method uncompresses the logical directory entry file (or directory) specified in the object path.</span></span> <span data-ttu-id="1cea5-106">Este método es una versión extendida del método [**UNCOMPRESS**](uncompress-method-in-class-win32-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="1cea5-106">This method is an extended version of the [**Uncompress**](uncompress-method-in-class-win32-directory.md) method.</span></span>

<span data-ttu-id="1cea5-107">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="1cea5-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="1cea5-108">Para obtener más información sobre el uso de este método, vea [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="1cea5-108">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="1cea5-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1cea5-109">Syntax</span></span>


```mof
uint32 UncompressEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="1cea5-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1cea5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cea5-111">*StopFileName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1cea5-111">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1cea5-112">Nombre del archivo o directorio en el que se produjo un error en el método **UncompressEx** .</span><span class="sxs-lookup"><span data-stu-id="1cea5-112">Name of the file/directory where the **UncompressEx** method failed.</span></span> <span data-ttu-id="1cea5-113">Este parámetro será **null** si el método se ejecuta correctamente.</span><span class="sxs-lookup"><span data-stu-id="1cea5-113">This parameter will be **NULL** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="1cea5-114">*StartFileName* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="1cea5-114">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1cea5-115">Designa el archivo o directorio secundario que se va a usar como punto de partida para **UncompressEx**.</span><span class="sxs-lookup"><span data-stu-id="1cea5-115">Names the child file/directory to use as a starting point for **UncompressEx**.</span></span> <span data-ttu-id="1cea5-116">El parámetro *StartFileName* es normalmente el parámetro *StopFileName* que especifica el archivo o directorio en el que se produjo un error de la llamada al método anterior.</span><span class="sxs-lookup"><span data-stu-id="1cea5-116">The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="1cea5-117">Si este parámetro es **null**, la operación se realiza en el archivo o directorio especificado en la llamada ExecMethod.</span><span class="sxs-lookup"><span data-stu-id="1cea5-117">If this parameter is **NULL**, the operation is performed on the file or directory specified in the ExecMethod call.</span></span>

<span data-ttu-id="1cea5-118">Si se utiliza *StartFileName* , *Recursive* también debe establecerse en true.</span><span class="sxs-lookup"><span data-stu-id="1cea5-118">If *StartFileName* is used, *Recursive* must be set to true as well.</span></span>

</dd> <dt>

<span data-ttu-id="1cea5-119">*Recursivo* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="1cea5-119">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1cea5-120">Si **es true**, el cambio de propiedad se aplicará de forma recursiva a los archivos y directorios del directorio especificado por la instancia de [**\_ LogicalFile de CIM**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="1cea5-120">If **true**, the change of ownership will be applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span> <span data-ttu-id="1cea5-121">Nota: para las instancias de archivo, se omite el parámetro de entrada *recursivo* .</span><span class="sxs-lookup"><span data-stu-id="1cea5-121">Note: for file instances, the *Recursive* input parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cea5-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1cea5-122">Return value</span></span>

<span data-ttu-id="1cea5-123">Devuelve un valor de 0 (cero) si el archivo se ha descomprimido correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="1cea5-123">Returns an value of 0 (zero) if the file was successfully decompressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="1cea5-124">**0**</span><span class="sxs-lookup"><span data-stu-id="1cea5-124">**0**</span></span>
</dt> <dd>

<span data-ttu-id="1cea5-125">La solicitud fue correcta.</span><span class="sxs-lookup"><span data-stu-id="1cea5-125">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="1cea5-126">**2**</span><span class="sxs-lookup"><span data-stu-id="1cea5-126">**2**</span></span>
</dt> <dd>

<span data-ttu-id="1cea5-127">Se denegó el acceso.</span><span class="sxs-lookup"><span data-stu-id="1cea5-127">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="1cea5-128">**8**</span><span class="sxs-lookup"><span data-stu-id="1cea5-128">**8**</span></span>
</dt> <dd>

<span data-ttu-id="1cea5-129">Se produjo un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="1cea5-129">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="1cea5-130">**9**</span><span class="sxs-lookup"><span data-stu-id="1cea5-130">**9**</span></span>
</dt> <dd>

<span data-ttu-id="1cea5-131">El nombre especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="1cea5-131">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="1cea5-132">**10**</span><span class="sxs-lookup"><span data-stu-id="1cea5-132">**10**</span></span>
</dt> <dd>

<span data-ttu-id="1cea5-133">El objeto especificado ya existe.</span><span class="sxs-lookup"><span data-stu-id="1cea5-133">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="1cea5-134">**11**</span><span class="sxs-lookup"><span data-stu-id="1cea5-134">**11**</span></span>
</dt> <dd>

<span data-ttu-id="1cea5-135">El sistema de archivos no es NTFS.</span><span class="sxs-lookup"><span data-stu-id="1cea5-135">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="1cea5-136">**12**</span><span class="sxs-lookup"><span data-stu-id="1cea5-136">**12**</span></span>
</dt> <dd>

<span data-ttu-id="1cea5-137">La plataforma no es Windows.</span><span class="sxs-lookup"><span data-stu-id="1cea5-137">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="1cea5-138">**13**</span><span class="sxs-lookup"><span data-stu-id="1cea5-138">**13**</span></span>
</dt> <dd>

<span data-ttu-id="1cea5-139">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="1cea5-139">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="1cea5-140">**14**</span><span class="sxs-lookup"><span data-stu-id="1cea5-140">**14**</span></span>
</dt> <dd>

<span data-ttu-id="1cea5-141">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="1cea5-141">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="1cea5-142">**15**</span><span class="sxs-lookup"><span data-stu-id="1cea5-142">**15**</span></span>
</dt> <dd>

<span data-ttu-id="1cea5-143">Se ha producido una infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="1cea5-143">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="1cea5-144">**16**</span><span class="sxs-lookup"><span data-stu-id="1cea5-144">**16**</span></span>
</dt> <dd>

<span data-ttu-id="1cea5-145">El archivo de inicio especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="1cea5-145">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="1cea5-146">**17**</span><span class="sxs-lookup"><span data-stu-id="1cea5-146">**17**</span></span>
</dt> <dd>

<span data-ttu-id="1cea5-147">No se mantiene un privilegio necesario para la operación.</span><span class="sxs-lookup"><span data-stu-id="1cea5-147">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="1cea5-148">**21**</span><span class="sxs-lookup"><span data-stu-id="1cea5-148">**21**</span></span>
</dt> <dd>

<span data-ttu-id="1cea5-149">Un parámetro especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="1cea5-149">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1cea5-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1cea5-150">Requirements</span></span>



| <span data-ttu-id="1cea5-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="1cea5-151">Requirement</span></span> | <span data-ttu-id="1cea5-152">Value</span><span class="sxs-lookup"><span data-stu-id="1cea5-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1cea5-153">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1cea5-153">Minimum supported client</span></span><br/> | <span data-ttu-id="1cea5-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1cea5-154">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1cea5-155">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1cea5-155">Minimum supported server</span></span><br/> | <span data-ttu-id="1cea5-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1cea5-156">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1cea5-157">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1cea5-157">Namespace</span></span><br/>                | <span data-ttu-id="1cea5-158">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="1cea5-158">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1cea5-159">MOF</span><span class="sxs-lookup"><span data-stu-id="1cea5-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1cea5-160"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1cea5-160"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1cea5-161">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1cea5-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1cea5-162"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1cea5-162"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1cea5-163">Vea también</span><span class="sxs-lookup"><span data-stu-id="1cea5-163">See also</span></span>

<dl> <dt>

<span data-ttu-id="1cea5-164">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1cea5-164">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="1cea5-165">**\_Directorio Win32**</span><span class="sxs-lookup"><span data-stu-id="1cea5-165">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

