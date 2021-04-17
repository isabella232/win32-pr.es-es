---
description: Comprime el archivo de método abreviado lógico (o directorio) especificado en la ruta de acceso del objeto.
ms.assetid: ade588a5-4e0c-486b-b187-805fcabbf326
ms.tgt_platform: multiple
title: Método compress de la clase Win32_ShortcutFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile.Compress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 490f4d1a76844dc9ebad0449432f06833580d949
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659400"
---
# <a name="compress-method-of-the-win32_shortcutfile-class"></a><span data-ttu-id="dc6b8-103">Método compress de la \_ clase Win32 ShortcutFile</span><span class="sxs-lookup"><span data-stu-id="dc6b8-103">Compress method of the Win32\_ShortcutFile class</span></span>

<span data-ttu-id="dc6b8-104">El método **compress** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) comprime el archivo de método abreviado lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="dc6b8-104">The **Compress** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method compresses the logical shortcut file (or directory) specified in the object path.</span></span>

<span data-ttu-id="dc6b8-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="dc6b8-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="dc6b8-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="dc6b8-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="dc6b8-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dc6b8-107">Syntax</span></span>


```mof
uint32 Compress();
```



## <a name="parameters"></a><span data-ttu-id="dc6b8-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dc6b8-108">Parameters</span></span>

<span data-ttu-id="dc6b8-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="dc6b8-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dc6b8-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dc6b8-110">Return value</span></span>

<span data-ttu-id="dc6b8-111">Devuelve un valor de 0 (cero) si el archivo se ha comprimido correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="dc6b8-111">Returns a value of 0 (zero) if the file was successfully compressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="dc6b8-112">**0**</span><span class="sxs-lookup"><span data-stu-id="dc6b8-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="dc6b8-113">La solicitud fue correcta.</span><span class="sxs-lookup"><span data-stu-id="dc6b8-113">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="dc6b8-114">**2**</span><span class="sxs-lookup"><span data-stu-id="dc6b8-114">**2**</span></span>
</dt> <dd>

<span data-ttu-id="dc6b8-115">Se denegó el acceso.</span><span class="sxs-lookup"><span data-stu-id="dc6b8-115">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="dc6b8-116">**8**</span><span class="sxs-lookup"><span data-stu-id="dc6b8-116">**8**</span></span>
</dt> <dd>

<span data-ttu-id="dc6b8-117">Se produjo un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="dc6b8-117">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="dc6b8-118">**9**</span><span class="sxs-lookup"><span data-stu-id="dc6b8-118">**9**</span></span>
</dt> <dd>

<span data-ttu-id="dc6b8-119">El nombre especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="dc6b8-119">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="dc6b8-120">**10**</span><span class="sxs-lookup"><span data-stu-id="dc6b8-120">**10**</span></span>
</dt> <dd>

<span data-ttu-id="dc6b8-121">El objeto especificado ya existe.</span><span class="sxs-lookup"><span data-stu-id="dc6b8-121">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="dc6b8-122">**11**</span><span class="sxs-lookup"><span data-stu-id="dc6b8-122">**11**</span></span>
</dt> <dd>

<span data-ttu-id="dc6b8-123">El sistema de archivos no es NTFS.</span><span class="sxs-lookup"><span data-stu-id="dc6b8-123">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="dc6b8-124">**12**</span><span class="sxs-lookup"><span data-stu-id="dc6b8-124">**12**</span></span>
</dt> <dd>

<span data-ttu-id="dc6b8-125">La plataforma no es Windows.</span><span class="sxs-lookup"><span data-stu-id="dc6b8-125">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="dc6b8-126">**13**</span><span class="sxs-lookup"><span data-stu-id="dc6b8-126">**13**</span></span>
</dt> <dd>

<span data-ttu-id="dc6b8-127">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="dc6b8-127">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="dc6b8-128">**14**</span><span class="sxs-lookup"><span data-stu-id="dc6b8-128">**14**</span></span>
</dt> <dd>

<span data-ttu-id="dc6b8-129">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="dc6b8-129">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="dc6b8-130">**15**</span><span class="sxs-lookup"><span data-stu-id="dc6b8-130">**15**</span></span>
</dt> <dd>

<span data-ttu-id="dc6b8-131">Se ha producido una infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="dc6b8-131">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="dc6b8-132">**16**</span><span class="sxs-lookup"><span data-stu-id="dc6b8-132">**16**</span></span>
</dt> <dd>

<span data-ttu-id="dc6b8-133">El archivo de inicio especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="dc6b8-133">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="dc6b8-134">**17**</span><span class="sxs-lookup"><span data-stu-id="dc6b8-134">**17**</span></span>
</dt> <dd>

<span data-ttu-id="dc6b8-135">No se mantiene un privilegio necesario para la operación.</span><span class="sxs-lookup"><span data-stu-id="dc6b8-135">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="dc6b8-136">**21**</span><span class="sxs-lookup"><span data-stu-id="dc6b8-136">**21**</span></span>
</dt> <dd>

<span data-ttu-id="dc6b8-137">Un parámetro especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="dc6b8-137">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dc6b8-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc6b8-138">Requirements</span></span>



| <span data-ttu-id="dc6b8-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc6b8-139">Requirement</span></span> | <span data-ttu-id="dc6b8-140">Value</span><span class="sxs-lookup"><span data-stu-id="dc6b8-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc6b8-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dc6b8-141">Minimum supported client</span></span><br/> | <span data-ttu-id="dc6b8-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dc6b8-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dc6b8-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dc6b8-143">Minimum supported server</span></span><br/> | <span data-ttu-id="dc6b8-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dc6b8-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dc6b8-145">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="dc6b8-145">Namespace</span></span><br/>                | <span data-ttu-id="dc6b8-146">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="dc6b8-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="dc6b8-147">MOF</span><span class="sxs-lookup"><span data-stu-id="dc6b8-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dc6b8-148"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dc6b8-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="dc6b8-149">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="dc6b8-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc6b8-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc6b8-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc6b8-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="dc6b8-151">See also</span></span>

<dl> <dt>

<span data-ttu-id="dc6b8-152">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="dc6b8-152">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="dc6b8-153">**Win32 \_ ShortcutFile**</span><span class="sxs-lookup"><span data-stu-id="dc6b8-153">**Win32\_ShortcutFile**</span></span>](win32-shortcutfile.md)
</dt> </dl>

 

