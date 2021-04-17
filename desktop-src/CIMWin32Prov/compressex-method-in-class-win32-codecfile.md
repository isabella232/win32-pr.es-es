---
description: Comprime el archivo de códec lógico (o directorio) especificado en la ruta de acceso del objeto (este método es una versión extendida del método Compress).
ms.assetid: e1ecf0de-3b81-443e-9936-326d7d2d9210
ms.tgt_platform: multiple
title: Método CompressEx de la clase Win32_CodecFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.CompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4ab2915a4f550c799fed8a58e5573e8264b92f1e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104495947"
---
# <a name="compressex-method-of-the-win32_codecfile-class"></a><span data-ttu-id="c38da-103">Método CompressEx de la \_ clase CodecFile de Win32</span><span class="sxs-lookup"><span data-stu-id="c38da-103">CompressEx method of the Win32\_CodecFile class</span></span>

<span data-ttu-id="c38da-104">El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **CompressEx** comprime el archivo de códec lógico (o directorio) especificado en la ruta de acceso del objeto (este método es una versión extendida del método [**compress**](compress-method-in-class-win32-directory.md) ).</span><span class="sxs-lookup"><span data-stu-id="c38da-104">The **CompressEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method compresses the logical codec file (or directory) specified in the object path (this method is an extended version of the [**Compress**](compress-method-in-class-win32-directory.md) method).</span></span>

<span data-ttu-id="c38da-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="c38da-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="c38da-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="c38da-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="c38da-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c38da-107">Syntax</span></span>


```mof
uint32 CompressEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="c38da-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c38da-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c38da-109">*StopFileName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c38da-109">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c38da-110">Nombre del archivo o directorio en el que se produjo un error en el método **CompressEx** .</span><span class="sxs-lookup"><span data-stu-id="c38da-110">Name of the file or directory where the **CompressEx** method failed.</span></span> <span data-ttu-id="c38da-111">Este parámetro será **null** si el método se ejecuta correctamente.</span><span class="sxs-lookup"><span data-stu-id="c38da-111">This parameter will be **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="c38da-112">*StartFileName* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="c38da-112">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c38da-113">Asigna un nombre al archivo o directorio secundario que se va a usar como punto de partida para **CompressEx** . El parámetro *StartFileName* es normalmente el parámetro *StopFileName* que especifica el archivo o directorio en el que se produjo un error de la llamada al método anterior.</span><span class="sxs-lookup"><span data-stu-id="c38da-113">Names the child file or directory to use as a starting point for **CompressEx** .The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="c38da-114">Si este parámetro es **null**, la operación se realiza en el archivo o directorio especificado en la llamada **ExecMethod** .</span><span class="sxs-lookup"><span data-stu-id="c38da-114">If this parameter is **NULL**, the operation is performed on the file or directory specified in the **ExecMethod** call.</span></span>

</dd> <dt>

<span data-ttu-id="c38da-115">*Recursivo* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="c38da-115">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c38da-116">Si **es true**, el cambio de propiedad se aplicará de forma recursiva a los archivos y directorios del directorio especificado por la instancia de [**\_ LogicalFile de CIM**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="c38da-116">If **true**, the change of ownership will be applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span> <span data-ttu-id="c38da-117">Nota: para las instancias de archivo, se omite el parámetro de entrada *recursivo* .</span><span class="sxs-lookup"><span data-stu-id="c38da-117">Note: for file instances, the *Recursive* input parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c38da-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c38da-118">Return value</span></span>

<span data-ttu-id="c38da-119">Devuelve un valor de 0 (cero) si el archivo se ha comprimido correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="c38da-119">Returns an value of 0 (zero) if the file was successfully compressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="c38da-120">**0**</span><span class="sxs-lookup"><span data-stu-id="c38da-120">**0**</span></span>
</dt> <dd>

<span data-ttu-id="c38da-121">La solicitud fue correcta.</span><span class="sxs-lookup"><span data-stu-id="c38da-121">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="c38da-122">**2**</span><span class="sxs-lookup"><span data-stu-id="c38da-122">**2**</span></span>
</dt> <dd>

<span data-ttu-id="c38da-123">Se denegó el acceso.</span><span class="sxs-lookup"><span data-stu-id="c38da-123">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="c38da-124">**8**</span><span class="sxs-lookup"><span data-stu-id="c38da-124">**8**</span></span>
</dt> <dd>

<span data-ttu-id="c38da-125">Se produjo un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="c38da-125">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="c38da-126">**9**</span><span class="sxs-lookup"><span data-stu-id="c38da-126">**9**</span></span>
</dt> <dd>

<span data-ttu-id="c38da-127">El nombre especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="c38da-127">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="c38da-128">**10**</span><span class="sxs-lookup"><span data-stu-id="c38da-128">**10**</span></span>
</dt> <dd>

<span data-ttu-id="c38da-129">El objeto especificado ya existe.</span><span class="sxs-lookup"><span data-stu-id="c38da-129">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="c38da-130">**11**</span><span class="sxs-lookup"><span data-stu-id="c38da-130">**11**</span></span>
</dt> <dd>

<span data-ttu-id="c38da-131">El sistema de archivos no es NTFS.</span><span class="sxs-lookup"><span data-stu-id="c38da-131">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="c38da-132">**12**</span><span class="sxs-lookup"><span data-stu-id="c38da-132">**12**</span></span>
</dt> <dd>

<span data-ttu-id="c38da-133">La plataforma no es Windows.</span><span class="sxs-lookup"><span data-stu-id="c38da-133">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="c38da-134">**13**</span><span class="sxs-lookup"><span data-stu-id="c38da-134">**13**</span></span>
</dt> <dd>

<span data-ttu-id="c38da-135">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="c38da-135">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="c38da-136">**14**</span><span class="sxs-lookup"><span data-stu-id="c38da-136">**14**</span></span>
</dt> <dd>

<span data-ttu-id="c38da-137">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="c38da-137">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="c38da-138">**15**</span><span class="sxs-lookup"><span data-stu-id="c38da-138">**15**</span></span>
</dt> <dd>

<span data-ttu-id="c38da-139">Se ha producido una infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="c38da-139">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="c38da-140">**16**</span><span class="sxs-lookup"><span data-stu-id="c38da-140">**16**</span></span>
</dt> <dd>

<span data-ttu-id="c38da-141">El archivo de inicio especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="c38da-141">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="c38da-142">**17**</span><span class="sxs-lookup"><span data-stu-id="c38da-142">**17**</span></span>
</dt> <dd>

<span data-ttu-id="c38da-143">No se mantiene un privilegio necesario para la operación.</span><span class="sxs-lookup"><span data-stu-id="c38da-143">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="c38da-144">**21**</span><span class="sxs-lookup"><span data-stu-id="c38da-144">**21**</span></span>
</dt> <dd>

<span data-ttu-id="c38da-145">Un parámetro especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="c38da-145">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c38da-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c38da-146">Requirements</span></span>



| <span data-ttu-id="c38da-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="c38da-147">Requirement</span></span> | <span data-ttu-id="c38da-148">Value</span><span class="sxs-lookup"><span data-stu-id="c38da-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c38da-149">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c38da-149">Minimum supported client</span></span><br/> | <span data-ttu-id="c38da-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c38da-150">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c38da-151">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c38da-151">Minimum supported server</span></span><br/> | <span data-ttu-id="c38da-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c38da-152">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c38da-153">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c38da-153">Namespace</span></span><br/>                | <span data-ttu-id="c38da-154">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="c38da-154">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c38da-155">MOF</span><span class="sxs-lookup"><span data-stu-id="c38da-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c38da-156"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c38da-156"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c38da-157">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c38da-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c38da-158"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c38da-158"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c38da-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="c38da-159">See also</span></span>

<dl> <dt>

<span data-ttu-id="c38da-160">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c38da-160">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="c38da-161">**Win32 \_ CodecFile**</span><span class="sxs-lookup"><span data-stu-id="c38da-161">**Win32\_CodecFile**</span></span>](win32-codecfile.md)
</dt> </dl>

 

