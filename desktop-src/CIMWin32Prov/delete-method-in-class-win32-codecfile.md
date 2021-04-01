---
description: Elimina el archivo de códec de audio o vídeo lógico (o directorio) especificado en la ruta de acceso del objeto.
ms.assetid: 70233615-8924-4bd4-8a20-279a18b5c807
ms.tgt_platform: multiple
title: Método Delete de la clase Win32_CodecFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9d9395f5c5ebaf2948043fe43e84685e4c39d4d0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907505"
---
# <a name="delete-method-of-the-win32_codecfile-class"></a><span data-ttu-id="197a6-103">Método Delete de la \_ clase Win32 CodecFile</span><span class="sxs-lookup"><span data-stu-id="197a6-103">Delete method of the Win32\_CodecFile class</span></span>

<span data-ttu-id="197a6-104">El método **Delete** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) elimina el archivo de códec de audio o vídeo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="197a6-104">The **Delete** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method deletes the logical audio or video codec file (or directory) specified in the object path.</span></span>

<span data-ttu-id="197a6-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="197a6-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="197a6-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="197a6-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="197a6-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="197a6-107">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="197a6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="197a6-108">Parameters</span></span>

<span data-ttu-id="197a6-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="197a6-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="197a6-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="197a6-110">Return value</span></span>

<span data-ttu-id="197a6-111">Devuelve un valor de 0 (cero) si el archivo se eliminó correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="197a6-111">Returns a value of 0 (zero) if the file was successfully deleted, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="197a6-112">**0**</span><span class="sxs-lookup"><span data-stu-id="197a6-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="197a6-113">La solicitud fue correcta.</span><span class="sxs-lookup"><span data-stu-id="197a6-113">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="197a6-114">**2**</span><span class="sxs-lookup"><span data-stu-id="197a6-114">**2**</span></span>
</dt> <dd>

<span data-ttu-id="197a6-115">Se denegó el acceso.</span><span class="sxs-lookup"><span data-stu-id="197a6-115">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="197a6-116">**8**</span><span class="sxs-lookup"><span data-stu-id="197a6-116">**8**</span></span>
</dt> <dd>

<span data-ttu-id="197a6-117">Se produjo un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="197a6-117">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="197a6-118">**9**</span><span class="sxs-lookup"><span data-stu-id="197a6-118">**9**</span></span>
</dt> <dd>

<span data-ttu-id="197a6-119">El nombre especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="197a6-119">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="197a6-120">**10**</span><span class="sxs-lookup"><span data-stu-id="197a6-120">**10**</span></span>
</dt> <dd>

<span data-ttu-id="197a6-121">El objeto especificado ya existe.</span><span class="sxs-lookup"><span data-stu-id="197a6-121">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="197a6-122">**11**</span><span class="sxs-lookup"><span data-stu-id="197a6-122">**11**</span></span>
</dt> <dd>

<span data-ttu-id="197a6-123">El sistema de archivos no es NTFS.</span><span class="sxs-lookup"><span data-stu-id="197a6-123">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="197a6-124">**12**</span><span class="sxs-lookup"><span data-stu-id="197a6-124">**12**</span></span>
</dt> <dd>

<span data-ttu-id="197a6-125">La plataforma no es Windows NT ni Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="197a6-125">The platform is not Windows NT or Windows 2000.</span></span>

</dd> <dt>

<span data-ttu-id="197a6-126">**13**</span><span class="sxs-lookup"><span data-stu-id="197a6-126">**13**</span></span>
</dt> <dd>

<span data-ttu-id="197a6-127">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="197a6-127">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="197a6-128">**14**</span><span class="sxs-lookup"><span data-stu-id="197a6-128">**14**</span></span>
</dt> <dd>

<span data-ttu-id="197a6-129">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="197a6-129">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="197a6-130">**15**</span><span class="sxs-lookup"><span data-stu-id="197a6-130">**15**</span></span>
</dt> <dd>

<span data-ttu-id="197a6-131">Se ha producido una infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="197a6-131">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="197a6-132">**16**</span><span class="sxs-lookup"><span data-stu-id="197a6-132">**16**</span></span>
</dt> <dd>

<span data-ttu-id="197a6-133">El archivo de inicio especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="197a6-133">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="197a6-134">**17**</span><span class="sxs-lookup"><span data-stu-id="197a6-134">**17**</span></span>
</dt> <dd>

<span data-ttu-id="197a6-135">No se mantiene un privilegio necesario para la operación.</span><span class="sxs-lookup"><span data-stu-id="197a6-135">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="197a6-136">**21**</span><span class="sxs-lookup"><span data-stu-id="197a6-136">**21**</span></span>
</dt> <dd>

<span data-ttu-id="197a6-137">Un parámetro especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="197a6-137">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="197a6-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="197a6-138">Requirements</span></span>



| <span data-ttu-id="197a6-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="197a6-139">Requirement</span></span> | <span data-ttu-id="197a6-140">Value</span><span class="sxs-lookup"><span data-stu-id="197a6-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="197a6-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="197a6-141">Minimum supported client</span></span><br/> | <span data-ttu-id="197a6-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="197a6-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="197a6-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="197a6-143">Minimum supported server</span></span><br/> | <span data-ttu-id="197a6-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="197a6-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="197a6-145">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="197a6-145">Namespace</span></span><br/>                | <span data-ttu-id="197a6-146">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="197a6-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="197a6-147">MOF</span><span class="sxs-lookup"><span data-stu-id="197a6-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="197a6-148"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="197a6-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="197a6-149">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="197a6-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="197a6-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="197a6-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="197a6-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="197a6-151">See also</span></span>

<dl> <dt>

<span data-ttu-id="197a6-152">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="197a6-152">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="197a6-153">**Win32 \_ CodecFile**</span><span class="sxs-lookup"><span data-stu-id="197a6-153">**Win32\_CodecFile**</span></span>](win32-codecfile.md)
</dt> </dl>

 

