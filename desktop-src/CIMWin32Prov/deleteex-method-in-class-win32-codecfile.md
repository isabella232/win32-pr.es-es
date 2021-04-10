---
description: Elimine el archivo de códec de audio o vídeo lógico (o directorio) especificado en la ruta de acceso del objeto.
ms.assetid: df85c8a4-3be3-4bde-b36e-6bc8af6495a9
ms.tgt_platform: multiple
title: Método DeleteEx de la clase Win32_CodecFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.DeleteEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: df5527be497176f167ac368b872253fa3254a404
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907148"
---
# <a name="deleteex-method-of-the-win32_codecfile-class"></a><span data-ttu-id="4e716-103">Método DeleteEx de la \_ clase CodecFile de Win32</span><span class="sxs-lookup"><span data-stu-id="4e716-103">DeleteEx method of the Win32\_CodecFile class</span></span>

<span data-ttu-id="4e716-104">El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **DeleteEx** eliminará el archivo de códec de audio o vídeo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="4e716-104">The **DeleteEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method will delete the logical audio or video codec file (or directory) specified in the object path.</span></span> <span data-ttu-id="4e716-105">**DeleteEx** es una versión extendida del método [**Delete**](delete-method-in-class-win32-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="4e716-105">**DeleteEx** is an extended version of the [**Delete**](delete-method-in-class-win32-directory.md) method.</span></span>

<span data-ttu-id="4e716-106">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="4e716-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="4e716-107">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="4e716-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="4e716-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4e716-108">Syntax</span></span>


```mof
uint32 DeleteEx(
  [out] string StopFileName,
  [in]  String StartFileName
);
```



## <a name="parameters"></a><span data-ttu-id="4e716-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4e716-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e716-110">*StopFileName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4e716-110">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e716-111">Nombre del archivo o directorio en el que se produjo un error en el método **DeleteEx** .</span><span class="sxs-lookup"><span data-stu-id="4e716-111">Name of the file or directory where the **DeleteEx** method failed.</span></span> <span data-ttu-id="4e716-112">Este parámetro será **null** si el método se ejecuta correctamente.</span><span class="sxs-lookup"><span data-stu-id="4e716-112">This parameter will be **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="4e716-113">*StartFileName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4e716-113">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e716-114">Asigna un nombre al archivo o directorio secundario que se va a usar como punto de partida para **DeleteEx**.</span><span class="sxs-lookup"><span data-stu-id="4e716-114">Names the child file or directory to use as a starting point for **DeleteEx**.</span></span> <span data-ttu-id="4e716-115">El parámetro *StartFileName* es normalmente el parámetro *StopFileName* que especifica el archivo o directorio en el que se produjo un error de la llamada al método anterior.</span><span class="sxs-lookup"><span data-stu-id="4e716-115">The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="4e716-116">Si este parámetro es **null**, la operación se realiza en el archivo o directorio especificado en la llamada **ExecMethod** .</span><span class="sxs-lookup"><span data-stu-id="4e716-116">If this parameter is **NULL**, the operation is performed on the file or directory specified in the **ExecMethod** call.</span></span> <span data-ttu-id="4e716-117">Este parámetro es opcional.</span><span class="sxs-lookup"><span data-stu-id="4e716-117">This parameter is optional.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e716-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4e716-118">Return value</span></span>

<span data-ttu-id="4e716-119">Devuelve un valor entero de 0 (cero) si el archivo se ha eliminado correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="4e716-119">Returns an integer value of 0 (zero) if the file was successfully deleted, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="4e716-120">**0**</span><span class="sxs-lookup"><span data-stu-id="4e716-120">**0**</span></span>
</dt> <dd>

<span data-ttu-id="4e716-121">La solicitud fue correcta.</span><span class="sxs-lookup"><span data-stu-id="4e716-121">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="4e716-122">**2**</span><span class="sxs-lookup"><span data-stu-id="4e716-122">**2**</span></span>
</dt> <dd>

<span data-ttu-id="4e716-123">Se denegó el acceso.</span><span class="sxs-lookup"><span data-stu-id="4e716-123">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="4e716-124">**8**</span><span class="sxs-lookup"><span data-stu-id="4e716-124">**8**</span></span>
</dt> <dd>

<span data-ttu-id="4e716-125">Se produjo un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="4e716-125">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="4e716-126">**9**</span><span class="sxs-lookup"><span data-stu-id="4e716-126">**9**</span></span>
</dt> <dd>

<span data-ttu-id="4e716-127">El nombre especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="4e716-127">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="4e716-128">**10**</span><span class="sxs-lookup"><span data-stu-id="4e716-128">**10**</span></span>
</dt> <dd>

<span data-ttu-id="4e716-129">El objeto especificado ya existe.</span><span class="sxs-lookup"><span data-stu-id="4e716-129">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="4e716-130">**11**</span><span class="sxs-lookup"><span data-stu-id="4e716-130">**11**</span></span>
</dt> <dd>

<span data-ttu-id="4e716-131">El sistema de archivos no es NTFS.</span><span class="sxs-lookup"><span data-stu-id="4e716-131">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="4e716-132">**12**</span><span class="sxs-lookup"><span data-stu-id="4e716-132">**12**</span></span>
</dt> <dd>

<span data-ttu-id="4e716-133">La plataforma no es Windows.</span><span class="sxs-lookup"><span data-stu-id="4e716-133">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="4e716-134">**13**</span><span class="sxs-lookup"><span data-stu-id="4e716-134">**13**</span></span>
</dt> <dd>

<span data-ttu-id="4e716-135">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="4e716-135">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="4e716-136">**14**</span><span class="sxs-lookup"><span data-stu-id="4e716-136">**14**</span></span>
</dt> <dd>

<span data-ttu-id="4e716-137">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="4e716-137">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="4e716-138">**15**</span><span class="sxs-lookup"><span data-stu-id="4e716-138">**15**</span></span>
</dt> <dd>

<span data-ttu-id="4e716-139">Se ha producido una infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="4e716-139">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="4e716-140">**16**</span><span class="sxs-lookup"><span data-stu-id="4e716-140">**16**</span></span>
</dt> <dd>

<span data-ttu-id="4e716-141">El archivo de inicio especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="4e716-141">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="4e716-142">**17**</span><span class="sxs-lookup"><span data-stu-id="4e716-142">**17**</span></span>
</dt> <dd>

<span data-ttu-id="4e716-143">No se mantiene un privilegio necesario para la operación.</span><span class="sxs-lookup"><span data-stu-id="4e716-143">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="4e716-144">**21**</span><span class="sxs-lookup"><span data-stu-id="4e716-144">**21**</span></span>
</dt> <dd>

<span data-ttu-id="4e716-145">Un parámetro especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="4e716-145">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4e716-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e716-146">Requirements</span></span>



| <span data-ttu-id="4e716-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e716-147">Requirement</span></span> | <span data-ttu-id="4e716-148">Value</span><span class="sxs-lookup"><span data-stu-id="4e716-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e716-149">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4e716-149">Minimum supported client</span></span><br/> | <span data-ttu-id="4e716-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4e716-150">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4e716-151">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4e716-151">Minimum supported server</span></span><br/> | <span data-ttu-id="4e716-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4e716-152">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4e716-153">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4e716-153">Namespace</span></span><br/>                | <span data-ttu-id="4e716-154">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="4e716-154">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4e716-155">MOF</span><span class="sxs-lookup"><span data-stu-id="4e716-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4e716-156"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4e716-156"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4e716-157">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4e716-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e716-158"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e716-158"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e716-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="4e716-159">See also</span></span>

<dl> <dt>

<span data-ttu-id="4e716-160">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4e716-160">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="4e716-161">**Win32 \_ CodecFile**</span><span class="sxs-lookup"><span data-stu-id="4e716-161">**Win32\_CodecFile**</span></span>](win32-codecfile.md)
</dt> </dl>

 

