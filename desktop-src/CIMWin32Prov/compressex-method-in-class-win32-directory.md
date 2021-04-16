---
description: Comprime el archivo de entrada de directorio lógico (o directorio) especificado en la ruta de acceso del objeto (este método es una versión extendida del método Compress).
ms.assetid: 6b6e559c-4ca6-49d4-b255-5e1511fdf2e2
ms.tgt_platform: multiple
title: Método CompressEx de la clase Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.CompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3ee300919efa388d27ae9d594bc2b6c27def88e6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659399"
---
# <a name="compressex-method-of-the-win32_directory-class"></a><span data-ttu-id="5ae2d-103">Método CompressEx de la \_ clase de directorio Win32</span><span class="sxs-lookup"><span data-stu-id="5ae2d-103">CompressEx method of the Win32\_Directory class</span></span>

<span data-ttu-id="5ae2d-104">El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **CompressEx** comprime el archivo de entrada de directorio lógico (o directorio) especificado en la ruta de acceso del objeto (este método es una versión extendida del método [**compress**](compress-method-in-class-win32-directory.md) ).</span><span class="sxs-lookup"><span data-stu-id="5ae2d-104">The **CompressEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method compresses the logical directory entry file (or directory) specified in the object path (this method is an extended version of the [**Compress**](compress-method-in-class-win32-directory.md) method).</span></span>

<span data-ttu-id="5ae2d-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="5ae2d-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="5ae2d-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="5ae2d-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="5ae2d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5ae2d-107">Syntax</span></span>


```mof
uint32 CompressEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="5ae2d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5ae2d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ae2d-109">*StopFileName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="5ae2d-109">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5ae2d-110">Nombre del archivo o directorio en el que se produjo un error en el método **CompressEx** .</span><span class="sxs-lookup"><span data-stu-id="5ae2d-110">Name of the file or directory where the **CompressEx** method failed.</span></span> <span data-ttu-id="5ae2d-111">Este parámetro será **null** si el método se ejecuta correctamente.</span><span class="sxs-lookup"><span data-stu-id="5ae2d-111">This parameter will be **NULL** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="5ae2d-112">*StartFileName* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="5ae2d-112">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5ae2d-113">Asigna un nombre al archivo o directorio secundario que se va a usar como punto de partida para **CompressEx**.</span><span class="sxs-lookup"><span data-stu-id="5ae2d-113">Names the child file or directory to use as a starting point for **CompressEx**.</span></span> <span data-ttu-id="5ae2d-114">El parámetro *StartFileName* es normalmente el parámetro *StopFileName* que especifica el archivo o directorio en el que se produjo un error de la llamada al método anterior.</span><span class="sxs-lookup"><span data-stu-id="5ae2d-114">The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="5ae2d-115">Si este parámetro es **null**, la operación se realiza en el archivo o directorio especificado en la llamada **ExecMethod** .</span><span class="sxs-lookup"><span data-stu-id="5ae2d-115">If this parameter is **NULL**, the operation is performed on the file or directory specified in the **ExecMethod** call.</span></span>

<span data-ttu-id="5ae2d-116">Si se utiliza *StartFileName* , *Recursive* también debe establecerse en true.</span><span class="sxs-lookup"><span data-stu-id="5ae2d-116">If *StartFileName* is used, *Recursive* must be set to true as well.</span></span>

</dd> <dt>

<span data-ttu-id="5ae2d-117">*Recursivo* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="5ae2d-117">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5ae2d-118">Si **es true**, el cambio de propiedad se aplicará de forma recursiva a los archivos y directorios del directorio especificado por la instancia de [**\_ LogicalFile de CIM**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="5ae2d-118">If **true**, the change of ownership will be applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span>

> [!Note]  
> <span data-ttu-id="5ae2d-119">En el caso de las instancias de archivo, se omite el parámetro de entrada *recursivo* .</span><span class="sxs-lookup"><span data-stu-id="5ae2d-119">For file instances, the *Recursive* input parameter is ignored.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ae2d-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5ae2d-120">Return value</span></span>

<span data-ttu-id="5ae2d-121">Devuelve un valor de 0 (cero) si el archivo se ha comprimido correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="5ae2d-121">Returns a value of 0 (zero) if the file was successfully compressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="5ae2d-122">**0**</span><span class="sxs-lookup"><span data-stu-id="5ae2d-122">**0**</span></span>
</dt> <dd>

<span data-ttu-id="5ae2d-123">La solicitud fue correcta.</span><span class="sxs-lookup"><span data-stu-id="5ae2d-123">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="5ae2d-124">**2**</span><span class="sxs-lookup"><span data-stu-id="5ae2d-124">**2**</span></span>
</dt> <dd>

<span data-ttu-id="5ae2d-125">Se denegó el acceso.</span><span class="sxs-lookup"><span data-stu-id="5ae2d-125">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="5ae2d-126">**8**</span><span class="sxs-lookup"><span data-stu-id="5ae2d-126">**8**</span></span>
</dt> <dd>

<span data-ttu-id="5ae2d-127">Se produjo un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="5ae2d-127">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="5ae2d-128">**9**</span><span class="sxs-lookup"><span data-stu-id="5ae2d-128">**9**</span></span>
</dt> <dd>

<span data-ttu-id="5ae2d-129">El nombre especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="5ae2d-129">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="5ae2d-130">**10**</span><span class="sxs-lookup"><span data-stu-id="5ae2d-130">**10**</span></span>
</dt> <dd>

<span data-ttu-id="5ae2d-131">El objeto especificado ya existe.</span><span class="sxs-lookup"><span data-stu-id="5ae2d-131">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="5ae2d-132">**11**</span><span class="sxs-lookup"><span data-stu-id="5ae2d-132">**11**</span></span>
</dt> <dd>

<span data-ttu-id="5ae2d-133">El sistema de archivos no es NTFS.</span><span class="sxs-lookup"><span data-stu-id="5ae2d-133">The file system is not an NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="5ae2d-134">**12**</span><span class="sxs-lookup"><span data-stu-id="5ae2d-134">**12**</span></span>
</dt> <dd>

<span data-ttu-id="5ae2d-135">La plataforma no es Windows.</span><span class="sxs-lookup"><span data-stu-id="5ae2d-135">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="5ae2d-136">**13**</span><span class="sxs-lookup"><span data-stu-id="5ae2d-136">**13**</span></span>
</dt> <dd>

<span data-ttu-id="5ae2d-137">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="5ae2d-137">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="5ae2d-138">**14**</span><span class="sxs-lookup"><span data-stu-id="5ae2d-138">**14**</span></span>
</dt> <dd>

<span data-ttu-id="5ae2d-139">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="5ae2d-139">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="5ae2d-140">**15**</span><span class="sxs-lookup"><span data-stu-id="5ae2d-140">**15**</span></span>
</dt> <dd>

<span data-ttu-id="5ae2d-141">Se ha producido una infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="5ae2d-141">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="5ae2d-142">**16**</span><span class="sxs-lookup"><span data-stu-id="5ae2d-142">**16**</span></span>
</dt> <dd>

<span data-ttu-id="5ae2d-143">El archivo de inicio especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="5ae2d-143">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="5ae2d-144">**17**</span><span class="sxs-lookup"><span data-stu-id="5ae2d-144">**17**</span></span>
</dt> <dd>

<span data-ttu-id="5ae2d-145">No se mantiene un privilegio necesario para la operación.</span><span class="sxs-lookup"><span data-stu-id="5ae2d-145">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="5ae2d-146">**21**</span><span class="sxs-lookup"><span data-stu-id="5ae2d-146">**21**</span></span>
</dt> <dd>

<span data-ttu-id="5ae2d-147">Un parámetro especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="5ae2d-147">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5ae2d-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ae2d-148">Requirements</span></span>



| <span data-ttu-id="5ae2d-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ae2d-149">Requirement</span></span> | <span data-ttu-id="5ae2d-150">Value</span><span class="sxs-lookup"><span data-stu-id="5ae2d-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ae2d-151">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5ae2d-151">Minimum supported client</span></span><br/> | <span data-ttu-id="5ae2d-152">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5ae2d-152">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5ae2d-153">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5ae2d-153">Minimum supported server</span></span><br/> | <span data-ttu-id="5ae2d-154">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5ae2d-154">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5ae2d-155">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5ae2d-155">Namespace</span></span><br/>                | <span data-ttu-id="5ae2d-156">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="5ae2d-156">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5ae2d-157">MOF</span><span class="sxs-lookup"><span data-stu-id="5ae2d-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5ae2d-158"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5ae2d-158"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5ae2d-159">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5ae2d-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ae2d-160"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ae2d-160"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ae2d-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="5ae2d-161">See also</span></span>

<dl> <dt>

<span data-ttu-id="5ae2d-162">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5ae2d-162">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="5ae2d-163">**\_Directorio Win32**</span><span class="sxs-lookup"><span data-stu-id="5ae2d-163">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

