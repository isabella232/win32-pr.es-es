---
description: Descomprime el archivo de entrada de directorio lógico (o directorio) especificado en la ruta de acceso del objeto.
ms.assetid: dd39aae3-7c88-48fc-93ed-5225d2f1491c
ms.tgt_platform: multiple
title: Método UNCOMPRESS de la clase Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.Uncompress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7c46a6bb90d43c1b793350bb96822a1aaed8dd9a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153443"
---
# <a name="uncompress-method-of-the-win32_directory-class"></a><span data-ttu-id="54053-103">Método UNCOMPRESS de la \_ clase de directorio Win32</span><span class="sxs-lookup"><span data-stu-id="54053-103">Uncompress method of the Win32\_Directory class</span></span>

<span data-ttu-id="54053-104">El método de clase **descomprimir** [WMI](/windows/desktop/WmiSdk/retrieving-a-class) descomprime el archivo de entrada de directorio lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="54053-104">The **Uncompress** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method uncompresses the logical directory entry file (or directory) specified in the object path.</span></span>

<span data-ttu-id="54053-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="54053-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="54053-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="54053-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="54053-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="54053-107">Syntax</span></span>


```mof
uint32 Uncompress();
```



## <a name="parameters"></a><span data-ttu-id="54053-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="54053-108">Parameters</span></span>

<span data-ttu-id="54053-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="54053-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="54053-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="54053-110">Return value</span></span>

<span data-ttu-id="54053-111">Devuelve un valor entero de 0 (cero) si el archivo se ha descomprimido correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="54053-111">Returns an integer value of 0 (zero) if the file was successfully decompressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="54053-112">**0**</span><span class="sxs-lookup"><span data-stu-id="54053-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="54053-113">La solicitud fue correcta.</span><span class="sxs-lookup"><span data-stu-id="54053-113">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="54053-114">**2**</span><span class="sxs-lookup"><span data-stu-id="54053-114">**2**</span></span>
</dt> <dd>

<span data-ttu-id="54053-115">Se denegó el acceso.</span><span class="sxs-lookup"><span data-stu-id="54053-115">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="54053-116">**8**</span><span class="sxs-lookup"><span data-stu-id="54053-116">**8**</span></span>
</dt> <dd>

<span data-ttu-id="54053-117">Se produjo un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="54053-117">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="54053-118">**9**</span><span class="sxs-lookup"><span data-stu-id="54053-118">**9**</span></span>
</dt> <dd>

<span data-ttu-id="54053-119">El nombre especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="54053-119">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="54053-120">**10**</span><span class="sxs-lookup"><span data-stu-id="54053-120">**10**</span></span>
</dt> <dd>

<span data-ttu-id="54053-121">El objeto especificado ya existe.</span><span class="sxs-lookup"><span data-stu-id="54053-121">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="54053-122">**11**</span><span class="sxs-lookup"><span data-stu-id="54053-122">**11**</span></span>
</dt> <dd>

<span data-ttu-id="54053-123">El sistema de archivos no es NTFS.</span><span class="sxs-lookup"><span data-stu-id="54053-123">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="54053-124">**12**</span><span class="sxs-lookup"><span data-stu-id="54053-124">**12**</span></span>
</dt> <dd>

<span data-ttu-id="54053-125">La plataforma no es Windows.</span><span class="sxs-lookup"><span data-stu-id="54053-125">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="54053-126">**13**</span><span class="sxs-lookup"><span data-stu-id="54053-126">**13**</span></span>
</dt> <dd>

<span data-ttu-id="54053-127">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="54053-127">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="54053-128">**14**</span><span class="sxs-lookup"><span data-stu-id="54053-128">**14**</span></span>
</dt> <dd>

<span data-ttu-id="54053-129">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="54053-129">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="54053-130">**15**</span><span class="sxs-lookup"><span data-stu-id="54053-130">**15**</span></span>
</dt> <dd>

<span data-ttu-id="54053-131">Se ha producido una infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="54053-131">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="54053-132">**16**</span><span class="sxs-lookup"><span data-stu-id="54053-132">**16**</span></span>
</dt> <dd>

<span data-ttu-id="54053-133">El archivo de inicio especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="54053-133">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="54053-134">**17**</span><span class="sxs-lookup"><span data-stu-id="54053-134">**17**</span></span>
</dt> <dd>

<span data-ttu-id="54053-135">No se mantiene un privilegio necesario para la operación.</span><span class="sxs-lookup"><span data-stu-id="54053-135">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="54053-136">**21**</span><span class="sxs-lookup"><span data-stu-id="54053-136">**21**</span></span>
</dt> <dd>

<span data-ttu-id="54053-137">Un parámetro especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="54053-137">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="54053-138">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="54053-138">Examples</span></span>

<span data-ttu-id="54053-139">En el siguiente ejemplo de VBScript se descomprime la carpeta c: \\ scripts.</span><span class="sxs-lookup"><span data-stu-id="54053-139">The following VBScript sample uncompresses the folder c:\\Scripts.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colFolders = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_Directory WHERE Name = 'c:\\Scripts'")
For Each objFolder in colFolders
 errResults = objFolder.Uncompress
 Wscript.Echo errResults
Next
```



## <a name="requirements"></a><span data-ttu-id="54053-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54053-140">Requirements</span></span>



| <span data-ttu-id="54053-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="54053-141">Requirement</span></span> | <span data-ttu-id="54053-142">Value</span><span class="sxs-lookup"><span data-stu-id="54053-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="54053-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="54053-143">Minimum supported client</span></span><br/> | <span data-ttu-id="54053-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="54053-144">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="54053-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="54053-145">Minimum supported server</span></span><br/> | <span data-ttu-id="54053-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="54053-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="54053-147">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="54053-147">Namespace</span></span><br/>                | <span data-ttu-id="54053-148">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="54053-148">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="54053-149">MOF</span><span class="sxs-lookup"><span data-stu-id="54053-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="54053-150"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="54053-150"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="54053-151">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="54053-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54053-152"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54053-152"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54053-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="54053-153">See also</span></span>

<dl> <dt>

<span data-ttu-id="54053-154">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="54053-154">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="54053-155">**\_Directorio Win32**</span><span class="sxs-lookup"><span data-stu-id="54053-155">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> <dt>

[<span data-ttu-id="54053-156">**Comprimir**</span><span class="sxs-lookup"><span data-stu-id="54053-156">**Compress**</span></span>](compress-method-in-class-win32-directory.md)
</dt> </dl>

 

