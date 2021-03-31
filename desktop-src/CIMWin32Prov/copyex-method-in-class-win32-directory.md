---
description: Copia el archivo de entrada de directorio lógico o el directorio especificado en la ruta de acceso del objeto en la ubicación especificada por el parámetro FileName. Este método es una versión extendida del método de copia.
ms.assetid: c15bd1ae-a60d-4875-a76e-99486820c42c
ms.tgt_platform: multiple
title: Método CopyEx de la clase Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.CopyEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 55f2fdb0aa4e8306e8ec0aa4f5f265c0a8ee6689
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907544"
---
# <a name="copyex-method-of-the-win32_directory-class"></a><span data-ttu-id="36c33-104">Método CopyEx de la \_ clase de directorio Win32</span><span class="sxs-lookup"><span data-stu-id="36c33-104">CopyEx method of the Win32\_Directory class</span></span>

<span data-ttu-id="36c33-105">El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **CopyEx** copia el archivo de entrada de directorio lógico o el directorio especificado en la ruta de acceso del objeto en la ubicación especificada por el parámetro *filename* .</span><span class="sxs-lookup"><span data-stu-id="36c33-105">The **CopyEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method copies the logical directory entry file or directory specified in the object path to the location specified by the *FileName* parameter.</span></span> <span data-ttu-id="36c33-106">Este método es una versión extendida del método de [**copia**](copy-method-in-class-win32-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="36c33-106">This method is an extended version of the [**Copy**](copy-method-in-class-win32-directory.md) method.</span></span> <span data-ttu-id="36c33-107">No se admite una copia si se requiere sobrescribir un archivo lógico existente.</span><span class="sxs-lookup"><span data-stu-id="36c33-107">A copy is not supported if overwriting an existing logical file is required.</span></span>

<span data-ttu-id="36c33-108">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="36c33-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="36c33-109">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="36c33-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="36c33-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="36c33-110">Syntax</span></span>


```mof
uint32 CopyEx(
  [in]           string  FileName,
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="36c33-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="36c33-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36c33-112">*Nombre de archivo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="36c33-112">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36c33-113">Nombre completo de la copia del archivo (o directorio).</span><span class="sxs-lookup"><span data-stu-id="36c33-113">Fully qualified name of the copy of the file (or directory).</span></span> <span data-ttu-id="36c33-114">Ejemplo: c: \\ temp \\ newdirectory.</span><span class="sxs-lookup"><span data-stu-id="36c33-114">Example: c:\\temp\\newdirectory.</span></span>

</dd> <dt>

<span data-ttu-id="36c33-115">*StopFileName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="36c33-115">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="36c33-116">Nombre del archivo o directorio en el que se produjo un error en el método **CopyEx** .</span><span class="sxs-lookup"><span data-stu-id="36c33-116">Name of the file or directory where the **CopyEx** method failed.</span></span> <span data-ttu-id="36c33-117">Este parámetro será **null** si el método se ejecuta correctamente.</span><span class="sxs-lookup"><span data-stu-id="36c33-117">This parameter will be **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="36c33-118">*StartFileName* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="36c33-118">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="36c33-119">Asigna un nombre al archivo o directorio secundario que se va a usar como punto de partida para **CopyEx**.</span><span class="sxs-lookup"><span data-stu-id="36c33-119">Names the child file or directory to use as a starting point for **CopyEx**.</span></span> <span data-ttu-id="36c33-120">El parámetro *StartFileName* es normalmente el parámetro *StopFileName* que especifica el archivo o directorio en el que se produjo un error de la llamada al método anterior.</span><span class="sxs-lookup"><span data-stu-id="36c33-120">The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="36c33-121">Si este parámetro es **null**, la operación se realiza en el archivo o directorio especificado en la llamada **ExecMethod** .</span><span class="sxs-lookup"><span data-stu-id="36c33-121">If this parameter is **NULL**, the operation is performed on the file or directory specified in the **ExecMethod** call.</span></span>

<span data-ttu-id="36c33-122">Si se utiliza *StartFileName* , *Recursive* también debe establecerse en true.</span><span class="sxs-lookup"><span data-stu-id="36c33-122">If *StartFileName* is used, *Recursive* must be set to true as well.</span></span>

</dd> <dt>

<span data-ttu-id="36c33-123">*Recursivo* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="36c33-123">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="36c33-124">Si **es true**, los archivos y directorios se copiarán de forma recursiva en el directorio especificado por la instancia de [**\_ LogicalFile de CIM**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="36c33-124">If **true**, files and directories will be copied recursively within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span>

> [!Note]  
> <span data-ttu-id="36c33-125">En el caso de las instancias de archivo, se omite el parámetro de entrada *recursivo* .</span><span class="sxs-lookup"><span data-stu-id="36c33-125">For file instances, the *Recursive* input parameter is ignored.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36c33-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="36c33-126">Return value</span></span>

<span data-ttu-id="36c33-127">Devuelve un valor de 0 (cero) si el archivo se ha copiado correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="36c33-127">Returns a value of 0 (zero) if the file was successfully copied, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="36c33-128">**0**</span><span class="sxs-lookup"><span data-stu-id="36c33-128">**0**</span></span>
</dt> <dd>

<span data-ttu-id="36c33-129">La solicitud fue correcta.</span><span class="sxs-lookup"><span data-stu-id="36c33-129">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="36c33-130">**2**</span><span class="sxs-lookup"><span data-stu-id="36c33-130">**2**</span></span>
</dt> <dd>

<span data-ttu-id="36c33-131">Se denegó el acceso.</span><span class="sxs-lookup"><span data-stu-id="36c33-131">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="36c33-132">**8**</span><span class="sxs-lookup"><span data-stu-id="36c33-132">**8**</span></span>
</dt> <dd>

<span data-ttu-id="36c33-133">Se produjo un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="36c33-133">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="36c33-134">**9**</span><span class="sxs-lookup"><span data-stu-id="36c33-134">**9**</span></span>
</dt> <dd>

<span data-ttu-id="36c33-135">El nombre especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="36c33-135">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="36c33-136">**10**</span><span class="sxs-lookup"><span data-stu-id="36c33-136">**10**</span></span>
</dt> <dd>

<span data-ttu-id="36c33-137">El objeto especificado ya existe.</span><span class="sxs-lookup"><span data-stu-id="36c33-137">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="36c33-138">**11**</span><span class="sxs-lookup"><span data-stu-id="36c33-138">**11**</span></span>
</dt> <dd>

<span data-ttu-id="36c33-139">El sistema de archivos no es NTFS.</span><span class="sxs-lookup"><span data-stu-id="36c33-139">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="36c33-140">**12**</span><span class="sxs-lookup"><span data-stu-id="36c33-140">**12**</span></span>
</dt> <dd>

<span data-ttu-id="36c33-141">La plataforma no es Windows.</span><span class="sxs-lookup"><span data-stu-id="36c33-141">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="36c33-142">**13**</span><span class="sxs-lookup"><span data-stu-id="36c33-142">**13**</span></span>
</dt> <dd>

<span data-ttu-id="36c33-143">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="36c33-143">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="36c33-144">**14**</span><span class="sxs-lookup"><span data-stu-id="36c33-144">**14**</span></span>
</dt> <dd>

<span data-ttu-id="36c33-145">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="36c33-145">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="36c33-146">**15**</span><span class="sxs-lookup"><span data-stu-id="36c33-146">**15**</span></span>
</dt> <dd>

<span data-ttu-id="36c33-147">Se ha producido una infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="36c33-147">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="36c33-148">**16**</span><span class="sxs-lookup"><span data-stu-id="36c33-148">**16**</span></span>
</dt> <dd>

<span data-ttu-id="36c33-149">El archivo de inicio especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="36c33-149">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="36c33-150">**17**</span><span class="sxs-lookup"><span data-stu-id="36c33-150">**17**</span></span>
</dt> <dd>

<span data-ttu-id="36c33-151">No se mantiene un privilegio necesario para la operación.</span><span class="sxs-lookup"><span data-stu-id="36c33-151">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="36c33-152">**21**</span><span class="sxs-lookup"><span data-stu-id="36c33-152">**21**</span></span>
</dt> <dd>

<span data-ttu-id="36c33-153">Un parámetro especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="36c33-153">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="36c33-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36c33-154">Requirements</span></span>



| <span data-ttu-id="36c33-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="36c33-155">Requirement</span></span> | <span data-ttu-id="36c33-156">Value</span><span class="sxs-lookup"><span data-stu-id="36c33-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="36c33-157">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="36c33-157">Minimum supported client</span></span><br/> | <span data-ttu-id="36c33-158">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="36c33-158">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="36c33-159">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="36c33-159">Minimum supported server</span></span><br/> | <span data-ttu-id="36c33-160">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="36c33-160">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="36c33-161">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="36c33-161">Namespace</span></span><br/>                | <span data-ttu-id="36c33-162">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="36c33-162">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="36c33-163">MOF</span><span class="sxs-lookup"><span data-stu-id="36c33-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="36c33-164"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="36c33-164"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="36c33-165">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="36c33-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36c33-166"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36c33-166"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36c33-167">Vea también</span><span class="sxs-lookup"><span data-stu-id="36c33-167">See also</span></span>

<dl> <dt>

<span data-ttu-id="36c33-168">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="36c33-168">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="36c33-169">**\_Directorio Win32**</span><span class="sxs-lookup"><span data-stu-id="36c33-169">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

