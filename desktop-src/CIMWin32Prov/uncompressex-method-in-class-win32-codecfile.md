---
description: Descomprime el archivo de códec lógico (o directorio) especificado en la ruta de acceso del objeto. Este método es una versión extendida del método UNCOMPRESS.
ms.assetid: 257c69fa-c4f7-48be-8317-55db4b01601b
ms.tgt_platform: multiple
title: Método UncompressEx de la clase Win32_CodecFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.UncompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 547062a85336681b78a6081646801e78e4713e3c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539243"
---
# <a name="uncompressex-method-of-the-win32_codecfile-class"></a><span data-ttu-id="8a07a-104">Método UncompressEx de la \_ clase CodecFile de Win32</span><span class="sxs-lookup"><span data-stu-id="8a07a-104">UncompressEx method of the Win32\_CodecFile class</span></span>

<span data-ttu-id="8a07a-105">El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **UncompressEx** descomprime el archivo de códec lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="8a07a-105">The **UncompressEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method uncompresses the logical codec file (or directory) specified in the object path.</span></span> <span data-ttu-id="8a07a-106">Este método es una versión extendida del método [**UNCOMPRESS**](uncompress-method-in-class-win32-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="8a07a-106">This method is an extended version of the [**Uncompress**](uncompress-method-in-class-win32-directory.md) method.</span></span>

<span data-ttu-id="8a07a-107">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="8a07a-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="8a07a-108">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="8a07a-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="8a07a-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8a07a-109">Syntax</span></span>


```mof
uint32 UncompressEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="8a07a-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8a07a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a07a-111">*StopFileName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8a07a-111">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a07a-112">Nombre del archivo o directorio en el que se produjo un error en el método **UncompressEx** .</span><span class="sxs-lookup"><span data-stu-id="8a07a-112">Name of the file or directory where the **UncompressEx** method failed.</span></span> <span data-ttu-id="8a07a-113">Este parámetro será **null** si el método se ejecuta correctamente.</span><span class="sxs-lookup"><span data-stu-id="8a07a-113">This parameter will be **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="8a07a-114">*StartFileName* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="8a07a-114">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8a07a-115">Asigna un nombre al archivo o directorio secundario que se va a usar como punto de partida para **UncompressEx**. El parámetro *StartFileName* es normalmente el parámetro *StopFileName* que especifica el archivo o directorio en el que se produjo un error de la llamada al método anterior.</span><span class="sxs-lookup"><span data-stu-id="8a07a-115">Names the child file or directory to use as a starting point for **UncompressEx**.The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="8a07a-116">Si este parámetro es **null**, la operación se realiza en el archivo o directorio especificado en la llamada **ExecMethod** .</span><span class="sxs-lookup"><span data-stu-id="8a07a-116">If this parameter is **NULL**, the operation is performed on the file or directory specified in the **ExecMethod** call.</span></span>

</dd> <dt>

<span data-ttu-id="8a07a-117">*Recursivo* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="8a07a-117">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8a07a-118">Si **es true**, el cambio de propiedad se aplicará de forma recursiva a los archivos y directorios del directorio especificado por la instancia de [**\_ LogicalFile de CIM**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="8a07a-118">If **true**, the change of ownership will be applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span> <span data-ttu-id="8a07a-119">Nota: para las instancias de archivo, se omite el parámetro de entrada *recursivo* .</span><span class="sxs-lookup"><span data-stu-id="8a07a-119">Note: for file instances, the *Recursive* input parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a07a-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8a07a-120">Return value</span></span>

<span data-ttu-id="8a07a-121">Devuelve un valor entero de 0 (cero) si el archivo se ha descomprimido correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="8a07a-121">Returns an integer value of 0 (zero) if the file was successfully decompressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="8a07a-122">**0**</span><span class="sxs-lookup"><span data-stu-id="8a07a-122">**0**</span></span>
</dt> <dd>

<span data-ttu-id="8a07a-123">La solicitud fue correcta.</span><span class="sxs-lookup"><span data-stu-id="8a07a-123">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="8a07a-124">**2**</span><span class="sxs-lookup"><span data-stu-id="8a07a-124">**2**</span></span>
</dt> <dd>

<span data-ttu-id="8a07a-125">Se denegó el acceso.</span><span class="sxs-lookup"><span data-stu-id="8a07a-125">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="8a07a-126">**8**</span><span class="sxs-lookup"><span data-stu-id="8a07a-126">**8**</span></span>
</dt> <dd>

<span data-ttu-id="8a07a-127">Se produjo un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="8a07a-127">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="8a07a-128">**9**</span><span class="sxs-lookup"><span data-stu-id="8a07a-128">**9**</span></span>
</dt> <dd>

<span data-ttu-id="8a07a-129">El nombre especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="8a07a-129">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="8a07a-130">**10**</span><span class="sxs-lookup"><span data-stu-id="8a07a-130">**10**</span></span>
</dt> <dd>

<span data-ttu-id="8a07a-131">El objeto especificado ya existe.</span><span class="sxs-lookup"><span data-stu-id="8a07a-131">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="8a07a-132">**11**</span><span class="sxs-lookup"><span data-stu-id="8a07a-132">**11**</span></span>
</dt> <dd>

<span data-ttu-id="8a07a-133">El sistema de archivos no es NTFS.</span><span class="sxs-lookup"><span data-stu-id="8a07a-133">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="8a07a-134">**12**</span><span class="sxs-lookup"><span data-stu-id="8a07a-134">**12**</span></span>
</dt> <dd>

<span data-ttu-id="8a07a-135">La plataforma no es Windows.</span><span class="sxs-lookup"><span data-stu-id="8a07a-135">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="8a07a-136">**13**</span><span class="sxs-lookup"><span data-stu-id="8a07a-136">**13**</span></span>
</dt> <dd>

<span data-ttu-id="8a07a-137">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="8a07a-137">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="8a07a-138">**14**</span><span class="sxs-lookup"><span data-stu-id="8a07a-138">**14**</span></span>
</dt> <dd>

<span data-ttu-id="8a07a-139">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="8a07a-139">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="8a07a-140">**15**</span><span class="sxs-lookup"><span data-stu-id="8a07a-140">**15**</span></span>
</dt> <dd>

<span data-ttu-id="8a07a-141">Se ha producido una infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="8a07a-141">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="8a07a-142">**16**</span><span class="sxs-lookup"><span data-stu-id="8a07a-142">**16**</span></span>
</dt> <dd>

<span data-ttu-id="8a07a-143">El archivo de inicio especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="8a07a-143">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="8a07a-144">**17**</span><span class="sxs-lookup"><span data-stu-id="8a07a-144">**17**</span></span>
</dt> <dd>

<span data-ttu-id="8a07a-145">No se mantiene un privilegio necesario para la operación.</span><span class="sxs-lookup"><span data-stu-id="8a07a-145">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="8a07a-146">**21**</span><span class="sxs-lookup"><span data-stu-id="8a07a-146">**21**</span></span>
</dt> <dd>

<span data-ttu-id="8a07a-147">Un parámetro especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="8a07a-147">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8a07a-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a07a-148">Requirements</span></span>



| <span data-ttu-id="8a07a-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a07a-149">Requirement</span></span> | <span data-ttu-id="8a07a-150">Value</span><span class="sxs-lookup"><span data-stu-id="8a07a-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8a07a-151">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8a07a-151">Minimum supported client</span></span><br/> | <span data-ttu-id="8a07a-152">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8a07a-152">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8a07a-153">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8a07a-153">Minimum supported server</span></span><br/> | <span data-ttu-id="8a07a-154">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8a07a-154">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8a07a-155">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8a07a-155">Namespace</span></span><br/>                | <span data-ttu-id="8a07a-156">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="8a07a-156">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8a07a-157">MOF</span><span class="sxs-lookup"><span data-stu-id="8a07a-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8a07a-158"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8a07a-158"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8a07a-159">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8a07a-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a07a-160"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a07a-160"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a07a-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="8a07a-161">See also</span></span>

<dl> <dt>

<span data-ttu-id="8a07a-162">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8a07a-162">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="8a07a-163">**Win32 \_ CodecFile**</span><span class="sxs-lookup"><span data-stu-id="8a07a-163">**Win32\_CodecFile**</span></span>](win32-codecfile.md)
</dt> </dl>

 

