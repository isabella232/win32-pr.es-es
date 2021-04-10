---
description: Descomprime el archivo de códec lógico (o directorio) especificado en la ruta de acceso del objeto.
ms.assetid: abe74267-1274-4b20-82ac-51ca94d7af33
ms.tgt_platform: multiple
title: Método UNCOMPRESS de la clase Win32_CodecFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.Uncompress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7d1ffcf99877781c7070b42dac5ffe9ef83af2d5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907081"
---
# <a name="uncompress-method-of-the-win32_codecfile-class"></a><span data-ttu-id="47726-103">Método UNCOMPRESS de la \_ clase CodecFile de Win32</span><span class="sxs-lookup"><span data-stu-id="47726-103">Uncompress method of the Win32\_CodecFile class</span></span>

<span data-ttu-id="47726-104">El método de clase **descomprimir** [WMI](/windows/desktop/WmiSdk/retrieving-a-class) descomprime el archivo de códec lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="47726-104">The **Uncompress** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method uncompresses the logical codec file (or directory) specified in the object path.</span></span>

<span data-ttu-id="47726-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="47726-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="47726-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="47726-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="47726-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="47726-107">Syntax</span></span>


```mof
uint32 Uncompress();
```



## <a name="parameters"></a><span data-ttu-id="47726-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="47726-108">Parameters</span></span>

<span data-ttu-id="47726-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="47726-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="47726-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="47726-110">Return value</span></span>

<span data-ttu-id="47726-111">Devuelve un valor entero de 0 (cero) si el archivo se ha descomprimido correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="47726-111">Returns an integer value of 0 (zero) if the file was successfully decompressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="47726-112">**0**</span><span class="sxs-lookup"><span data-stu-id="47726-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="47726-113">La solicitud fue correcta.</span><span class="sxs-lookup"><span data-stu-id="47726-113">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="47726-114">**2**</span><span class="sxs-lookup"><span data-stu-id="47726-114">**2**</span></span>
</dt> <dd>

<span data-ttu-id="47726-115">Se denegó el acceso.</span><span class="sxs-lookup"><span data-stu-id="47726-115">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="47726-116">**8**</span><span class="sxs-lookup"><span data-stu-id="47726-116">**8**</span></span>
</dt> <dd>

<span data-ttu-id="47726-117">Se produjo un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="47726-117">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="47726-118">**9**</span><span class="sxs-lookup"><span data-stu-id="47726-118">**9**</span></span>
</dt> <dd>

<span data-ttu-id="47726-119">El nombre especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="47726-119">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="47726-120">**10**</span><span class="sxs-lookup"><span data-stu-id="47726-120">**10**</span></span>
</dt> <dd>

<span data-ttu-id="47726-121">El objeto especificado ya existe.</span><span class="sxs-lookup"><span data-stu-id="47726-121">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="47726-122">**11**</span><span class="sxs-lookup"><span data-stu-id="47726-122">**11**</span></span>
</dt> <dd>

<span data-ttu-id="47726-123">El sistema de archivos no es NTFS.</span><span class="sxs-lookup"><span data-stu-id="47726-123">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="47726-124">**12**</span><span class="sxs-lookup"><span data-stu-id="47726-124">**12**</span></span>
</dt> <dd>

<span data-ttu-id="47726-125">La plataforma no es Windows.</span><span class="sxs-lookup"><span data-stu-id="47726-125">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="47726-126">**13**</span><span class="sxs-lookup"><span data-stu-id="47726-126">**13**</span></span>
</dt> <dd>

<span data-ttu-id="47726-127">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="47726-127">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="47726-128">**14**</span><span class="sxs-lookup"><span data-stu-id="47726-128">**14**</span></span>
</dt> <dd>

<span data-ttu-id="47726-129">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="47726-129">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="47726-130">**15**</span><span class="sxs-lookup"><span data-stu-id="47726-130">**15**</span></span>
</dt> <dd>

<span data-ttu-id="47726-131">Se ha producido una infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="47726-131">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="47726-132">**16**</span><span class="sxs-lookup"><span data-stu-id="47726-132">**16**</span></span>
</dt> <dd>

<span data-ttu-id="47726-133">El archivo de inicio especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="47726-133">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="47726-134">**17**</span><span class="sxs-lookup"><span data-stu-id="47726-134">**17**</span></span>
</dt> <dd>

<span data-ttu-id="47726-135">No se mantiene un privilegio necesario para la operación.</span><span class="sxs-lookup"><span data-stu-id="47726-135">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="47726-136">**21**</span><span class="sxs-lookup"><span data-stu-id="47726-136">**21**</span></span>
</dt> <dd>

<span data-ttu-id="47726-137">Un parámetro especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="47726-137">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="47726-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47726-138">Requirements</span></span>



| <span data-ttu-id="47726-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="47726-139">Requirement</span></span> | <span data-ttu-id="47726-140">Value</span><span class="sxs-lookup"><span data-stu-id="47726-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="47726-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="47726-141">Minimum supported client</span></span><br/> | <span data-ttu-id="47726-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="47726-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="47726-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="47726-143">Minimum supported server</span></span><br/> | <span data-ttu-id="47726-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="47726-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="47726-145">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="47726-145">Namespace</span></span><br/>                | <span data-ttu-id="47726-146">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="47726-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="47726-147">MOF</span><span class="sxs-lookup"><span data-stu-id="47726-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="47726-148"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="47726-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="47726-149">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="47726-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="47726-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47726-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47726-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="47726-151">See also</span></span>

<dl> <dt>

<span data-ttu-id="47726-152">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="47726-152">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="47726-153">**Win32 \_ CodecFile**</span><span class="sxs-lookup"><span data-stu-id="47726-153">**Win32\_CodecFile**</span></span>](win32-codecfile.md)
</dt> </dl>

 

