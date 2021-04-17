---
description: Copia el archivo o directorio lógico del códec especificado en la ruta de acceso del objeto en la ubicación especificada por el parámetro de entrada.
ms.assetid: 77e67b01-561b-4233-899d-fa4bbf75ecf8
ms.tgt_platform: multiple
title: Método de copia de la clase Win32_CodecFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.Copy
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e3bd6621c065192eb45176444257f1c29c897201
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659587"
---
# <a name="copy-method-of-the-win32_codecfile-class"></a><span data-ttu-id="e2968-103">Método de copia de la \_ clase Win32 CodecFile</span><span class="sxs-lookup"><span data-stu-id="e2968-103">Copy method of the Win32\_CodecFile class</span></span>

<span data-ttu-id="e2968-104">El método **copiar** [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) copia el archivo de códec lógico o el directorio especificado en la ruta de acceso del objeto en la ubicación especificada por el parámetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="e2968-104">The **Copy** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method copies the logical codec file or directory specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="e2968-105">No se admite una copia si se requiere sobrescribir un archivo lógico existente.</span><span class="sxs-lookup"><span data-stu-id="e2968-105">A copy is not supported if overwriting an existing logical file is required.</span></span>

<span data-ttu-id="e2968-106">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="e2968-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="e2968-107">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="e2968-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="e2968-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e2968-108">Syntax</span></span>


```mof
uint32 Copy(
   string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="e2968-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e2968-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2968-110">*FileName*</span><span class="sxs-lookup"><span data-stu-id="e2968-110">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="e2968-111">Nombre completo de la copia del archivo (o directorio).</span><span class="sxs-lookup"><span data-stu-id="e2968-111">Fully qualified name of the copy of the file (or directory).</span></span> <span data-ttu-id="e2968-112">Ejemplo: c: \\ temp \\ newdirectory.</span><span class="sxs-lookup"><span data-stu-id="e2968-112">Example: c:\\temp\\newdirectory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2968-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e2968-113">Return value</span></span>

<span data-ttu-id="e2968-114">Devuelve un valor de 0 (cero) si el archivo se ha copiado correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="e2968-114">Returns an value of 0 (zero) if the file was successfully copied, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="e2968-115">**0**</span><span class="sxs-lookup"><span data-stu-id="e2968-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="e2968-116">La solicitud fue correcta.</span><span class="sxs-lookup"><span data-stu-id="e2968-116">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="e2968-117">**2**</span><span class="sxs-lookup"><span data-stu-id="e2968-117">**2**</span></span>
</dt> <dd>

<span data-ttu-id="e2968-118">Se denegó el acceso.</span><span class="sxs-lookup"><span data-stu-id="e2968-118">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="e2968-119">**8**</span><span class="sxs-lookup"><span data-stu-id="e2968-119">**8**</span></span>
</dt> <dd>

<span data-ttu-id="e2968-120">Se produjo un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="e2968-120">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="e2968-121">**9**</span><span class="sxs-lookup"><span data-stu-id="e2968-121">**9**</span></span>
</dt> <dd>

<span data-ttu-id="e2968-122">El nombre especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="e2968-122">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="e2968-123">**10**</span><span class="sxs-lookup"><span data-stu-id="e2968-123">**10**</span></span>
</dt> <dd>

<span data-ttu-id="e2968-124">El objeto especificado ya existe.</span><span class="sxs-lookup"><span data-stu-id="e2968-124">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="e2968-125">**11**</span><span class="sxs-lookup"><span data-stu-id="e2968-125">**11**</span></span>
</dt> <dd>

<span data-ttu-id="e2968-126">El sistema de archivos no es NTFS.</span><span class="sxs-lookup"><span data-stu-id="e2968-126">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="e2968-127">**12**</span><span class="sxs-lookup"><span data-stu-id="e2968-127">**12**</span></span>
</dt> <dd>

<span data-ttu-id="e2968-128">La plataforma no es Windows.</span><span class="sxs-lookup"><span data-stu-id="e2968-128">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="e2968-129">**13**</span><span class="sxs-lookup"><span data-stu-id="e2968-129">**13**</span></span>
</dt> <dd>

<span data-ttu-id="e2968-130">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="e2968-130">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="e2968-131">**14**</span><span class="sxs-lookup"><span data-stu-id="e2968-131">**14**</span></span>
</dt> <dd>

<span data-ttu-id="e2968-132">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="e2968-132">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="e2968-133">**15**</span><span class="sxs-lookup"><span data-stu-id="e2968-133">**15**</span></span>
</dt> <dd>

<span data-ttu-id="e2968-134">Se ha producido una infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="e2968-134">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="e2968-135">**16**</span><span class="sxs-lookup"><span data-stu-id="e2968-135">**16**</span></span>
</dt> <dd>

<span data-ttu-id="e2968-136">El archivo de inicio especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="e2968-136">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="e2968-137">**17**</span><span class="sxs-lookup"><span data-stu-id="e2968-137">**17**</span></span>
</dt> <dd>

<span data-ttu-id="e2968-138">No se mantiene un privilegio necesario para la operación.</span><span class="sxs-lookup"><span data-stu-id="e2968-138">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="e2968-139">**21**</span><span class="sxs-lookup"><span data-stu-id="e2968-139">**21**</span></span>
</dt> <dd>

<span data-ttu-id="e2968-140">Un parámetro especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="e2968-140">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e2968-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2968-141">Requirements</span></span>



| <span data-ttu-id="e2968-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2968-142">Requirement</span></span> | <span data-ttu-id="e2968-143">Value</span><span class="sxs-lookup"><span data-stu-id="e2968-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e2968-144">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e2968-144">Minimum supported client</span></span><br/> | <span data-ttu-id="e2968-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e2968-145">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e2968-146">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e2968-146">Minimum supported server</span></span><br/> | <span data-ttu-id="e2968-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e2968-147">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e2968-148">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e2968-148">Namespace</span></span><br/>                | <span data-ttu-id="e2968-149">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="e2968-149">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e2968-150">MOF</span><span class="sxs-lookup"><span data-stu-id="e2968-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e2968-151"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e2968-151"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e2968-152">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e2968-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2968-153"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2968-153"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2968-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="e2968-154">See also</span></span>

<dl> <dt>

<span data-ttu-id="e2968-155">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e2968-155">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="e2968-156">**Win32 \_ CodecFile**</span><span class="sxs-lookup"><span data-stu-id="e2968-156">**Win32\_CodecFile**</span></span>](win32-codecfile.md)
</dt> </dl>

 

