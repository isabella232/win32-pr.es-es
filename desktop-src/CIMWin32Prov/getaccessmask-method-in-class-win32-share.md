---
description: Devuelve un mapa de bits UInt32 con los derechos de acceso al recurso compartido mantenido por el usuario o grupo en cuyo nombre se devuelve la instancia.
ms.assetid: 234f44a4-ffff-431d-a973-98f2bd313c7d
ms.tgt_platform: multiple
title: Método GetAccessMask de la clase Win32_Share
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Share.GetAccessMask
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 745ce6d607adf84827c14a588640572b5d92be00
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998236"
---
# <a name="getaccessmask-method-of-the-win32_share-class"></a><span data-ttu-id="25b1f-103">Método GetAccessMask de la \_ clase de recursos compartidos de Win32</span><span class="sxs-lookup"><span data-stu-id="25b1f-103">GetAccessMask method of the Win32\_Share class</span></span>

<span data-ttu-id="25b1f-104">El método **GetAccessMask** devuelve un mapa de bits UInt32 con los derechos de acceso al recurso compartido mantenido por el usuario o grupo en cuyo nombre se devuelve la instancia.</span><span class="sxs-lookup"><span data-stu-id="25b1f-104">The **GetAccessMask** method returns a uint32 bitmap with the access rights to the share held by the user or group on whose behalf the instance is returned.</span></span>

<span data-ttu-id="25b1f-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="25b1f-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="25b1f-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="25b1f-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="25b1f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="25b1f-107">Syntax</span></span>


```mof
uint32 GetAccessMask();
```



## <a name="parameters"></a><span data-ttu-id="25b1f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="25b1f-108">Parameters</span></span>

<span data-ttu-id="25b1f-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="25b1f-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="25b1f-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="25b1f-110">Return value</span></span>

<span data-ttu-id="25b1f-111">Derechos de acceso al recurso compartido mantenido por el usuario o grupo.</span><span class="sxs-lookup"><span data-stu-id="25b1f-111">Access rights to the share held by the user or group.</span></span>

<dl> <dt>

<span data-ttu-id="25b1f-112">**directorio de la lista de archivos \_ \_**</span><span class="sxs-lookup"><span data-stu-id="25b1f-112">**FILE\_LIST\_DIRECTORY**</span></span>
</dt> <dd>

<span data-ttu-id="25b1f-113">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="25b1f-113">1 (0x1)</span></span>

<span data-ttu-id="25b1f-114">Concede el derecho a leer los datos del archivo.</span><span class="sxs-lookup"><span data-stu-id="25b1f-114">Grants the right to read data from the file.</span></span> <span data-ttu-id="25b1f-115">Para un directorio, este valor concede el derecho para mostrar el contenido del directorio.</span><span class="sxs-lookup"><span data-stu-id="25b1f-115">For a directory, this value grants the right to list the contents of the directory.</span></span>

</dd> <dt>

<span data-ttu-id="25b1f-116">**ARCHIVO \_ agregar \_ archivo**</span><span class="sxs-lookup"><span data-stu-id="25b1f-116">**FILE\_ADD\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="25b1f-117">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="25b1f-117">2 (0x2)</span></span>

<span data-ttu-id="25b1f-118">Concede el derecho para escribir datos en el archivo.</span><span class="sxs-lookup"><span data-stu-id="25b1f-118">Grants the right to write data to the file.</span></span> <span data-ttu-id="25b1f-119">Para un directorio, este valor concede el derecho a crear un archivo en el directorio.</span><span class="sxs-lookup"><span data-stu-id="25b1f-119">For a directory, this value grants the right to create a file in the directory.</span></span>

</dd> <dt>

<span data-ttu-id="25b1f-120">**\_agregar \_ subdirectorio de archivo**</span><span class="sxs-lookup"><span data-stu-id="25b1f-120">**FILE\_ADD\_SUBDIRECTORY**</span></span>
</dt> <dd>

<span data-ttu-id="25b1f-121">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="25b1f-121">4 (0x4)</span></span>

<span data-ttu-id="25b1f-122">Concede el derecho para anexar datos al archivo.</span><span class="sxs-lookup"><span data-stu-id="25b1f-122">Grants the right to append data to the file.</span></span> <span data-ttu-id="25b1f-123">Para un directorio, este valor concede el derecho a crear un subdirectorio.</span><span class="sxs-lookup"><span data-stu-id="25b1f-123">For a directory, this value grants the right to create a subdirectory.</span></span>

</dd> <dt>

<span data-ttu-id="25b1f-124">**ARCHIVO de \_ lectura \_ EA**</span><span class="sxs-lookup"><span data-stu-id="25b1f-124">**FILE\_READ\_EA**</span></span>
</dt> <dd>

<span data-ttu-id="25b1f-125">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="25b1f-125">8 (0x8)</span></span>

<span data-ttu-id="25b1f-126">Concede el derecho para leer atributos extendidos.</span><span class="sxs-lookup"><span data-stu-id="25b1f-126">Grants the right to read extended attributes.</span></span>

</dd> <dt>

<span data-ttu-id="25b1f-127">**escritura de archivo \_ \_ EA**</span><span class="sxs-lookup"><span data-stu-id="25b1f-127">**FILE\_WRITE\_EA**</span></span>
</dt> <dd>

<span data-ttu-id="25b1f-128">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="25b1f-128">16 (0x10)</span></span>

<span data-ttu-id="25b1f-129">Concede el derecho para escribir atributos extendidos.</span><span class="sxs-lookup"><span data-stu-id="25b1f-129">Grants the right to write extended attributes.</span></span>

</dd> <dt>

<span data-ttu-id="25b1f-130">**recorrido de archivos \_**</span><span class="sxs-lookup"><span data-stu-id="25b1f-130">**FILE\_TRAVERSE**</span></span>
</dt> <dd>

<span data-ttu-id="25b1f-131">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="25b1f-131">32 (0x20)</span></span>

<span data-ttu-id="25b1f-132">Concede el derecho para ejecutar un archivo.</span><span class="sxs-lookup"><span data-stu-id="25b1f-132">Grants the right to execute a file.</span></span> <span data-ttu-id="25b1f-133">Para un directorio, se puede atravesar el directorio.</span><span class="sxs-lookup"><span data-stu-id="25b1f-133">For a directory, the directory can be traversed.</span></span>

</dd> <dt>

<span data-ttu-id="25b1f-134">**ARCHIVO- \_ eliminar \_ secundario**</span><span class="sxs-lookup"><span data-stu-id="25b1f-134">**FILE\_DELETE\_CHILD**</span></span>
</dt> <dd>

<span data-ttu-id="25b1f-135">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="25b1f-135">64 (0x40)</span></span>

<span data-ttu-id="25b1f-136">Concede el derecho para eliminar un directorio y todos los archivos que contiene (sus elementos secundarios), incluso si los archivos son de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="25b1f-136">Grants the right to delete a directory and all of the files it contains (its children), even if the files are read-only.</span></span>

</dd> <dt>

<span data-ttu-id="25b1f-137">**\_atributos de lectura de archivo \_**</span><span class="sxs-lookup"><span data-stu-id="25b1f-137">**FILE\_READ\_ATTRIBUTES**</span></span>
</dt> <dd>

<span data-ttu-id="25b1f-138">128 (0x80)</span><span class="sxs-lookup"><span data-stu-id="25b1f-138">128 (0x80)</span></span>

<span data-ttu-id="25b1f-139">Concede el derecho a leer los atributos de archivo.</span><span class="sxs-lookup"><span data-stu-id="25b1f-139">Grants the right to read file attributes.</span></span>

</dd> <dt>

<span data-ttu-id="25b1f-140">**\_atributos de escritura de archivo \_**</span><span class="sxs-lookup"><span data-stu-id="25b1f-140">**FILE\_WRITE\_ATTRIBUTES**</span></span>
</dt> <dd>

<span data-ttu-id="25b1f-141">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="25b1f-141">256 (0x100)</span></span>

<span data-ttu-id="25b1f-142">Concede el derecho para cambiar los atributos de archivo.</span><span class="sxs-lookup"><span data-stu-id="25b1f-142">Grants the right to change file attributes.</span></span>

</dd> <dt>

<span data-ttu-id="25b1f-143">**DELETE**</span><span class="sxs-lookup"><span data-stu-id="25b1f-143">**DELETE**</span></span>
</dt> <dd>

<span data-ttu-id="25b1f-144">65536 (0x10000)</span><span class="sxs-lookup"><span data-stu-id="25b1f-144">65536 (0x10000)</span></span>

<span data-ttu-id="25b1f-145">Concede acceso de eliminación.</span><span class="sxs-lookup"><span data-stu-id="25b1f-145">Grants delete access.</span></span>

</dd> <dt>

<span data-ttu-id="25b1f-146">**CONTROL de lectura \_**</span><span class="sxs-lookup"><span data-stu-id="25b1f-146">**READ\_CONTROL**</span></span>
</dt> <dd>

<span data-ttu-id="25b1f-147">131072 (0x20000)</span><span class="sxs-lookup"><span data-stu-id="25b1f-147">131072 (0x20000)</span></span>

<span data-ttu-id="25b1f-148">Concede acceso de lectura al descriptor de seguridad y al propietario.</span><span class="sxs-lookup"><span data-stu-id="25b1f-148">Grants read access to the security descriptor and owner.</span></span>

</dd> <dt>

<span data-ttu-id="25b1f-149">**ESCRIBIR \_ DAC**</span><span class="sxs-lookup"><span data-stu-id="25b1f-149">**WRITE\_DAC**</span></span>
</dt> <dd>

<span data-ttu-id="25b1f-150">262144 (0x40000)</span><span class="sxs-lookup"><span data-stu-id="25b1f-150">262144 (0x40000)</span></span>

<span data-ttu-id="25b1f-151">Concede acceso de escritura a la lista de control de acceso discrecional (DACL).</span><span class="sxs-lookup"><span data-stu-id="25b1f-151">Grants write access to the discretionary access control list (DACL).</span></span>

</dd> <dt>

<span data-ttu-id="25b1f-152">**propietario de escritura \_**</span><span class="sxs-lookup"><span data-stu-id="25b1f-152">**WRITE\_OWNER**</span></span>
</dt> <dd>

<span data-ttu-id="25b1f-153">524288 (0x80000)</span><span class="sxs-lookup"><span data-stu-id="25b1f-153">524288 (0x80000)</span></span>

<span data-ttu-id="25b1f-154">Asigna el propietario de la escritura.</span><span class="sxs-lookup"><span data-stu-id="25b1f-154">Assigns the write owner.</span></span>

</dd> <dt>

<span data-ttu-id="25b1f-155">**SYNCHRONIZE**</span><span class="sxs-lookup"><span data-stu-id="25b1f-155">**SYNCHRONIZE**</span></span>
</dt> <dd>

<span data-ttu-id="25b1f-156">1048576 (0x100000)</span><span class="sxs-lookup"><span data-stu-id="25b1f-156">1048576 (0x100000)</span></span>

<span data-ttu-id="25b1f-157">Sincroniza el acceso y permite que un proceso espere a que un objeto entre en el estado señalado.</span><span class="sxs-lookup"><span data-stu-id="25b1f-157">Synchronizes access and allows a process to wait for an object to enter the signaled state.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="25b1f-158">Observaciones</span><span class="sxs-lookup"><span data-stu-id="25b1f-158">Remarks</span></span>

<span data-ttu-id="25b1f-159">El método **GetAccessMask** es un método de objeto y se usa en una aparición de esta clase.</span><span class="sxs-lookup"><span data-stu-id="25b1f-159">**GetAccessMask** method is an object method and is used on an occurrence of this class.</span></span>

## <a name="examples"></a><span data-ttu-id="25b1f-160">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="25b1f-160">Examples</span></span>

<span data-ttu-id="25b1f-161">En el ejemplo de código de VBScript siguiente se crea una carpeta de recurso compartido y, a continuación, se obtiene el valor de la máscara de acceso en el descriptor de seguridad que protege la carpeta de recursos compartidos.</span><span class="sxs-lookup"><span data-stu-id="25b1f-161">The following VBScript code example creates a share folder and then gets the value of the access mask in the security descriptor that secures the share folder.</span></span>


```VB
Const FILE_SHARE = 0
Const MAXIMUM_CONNECTIONS = 4000 
strComputer = "."

Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set objNewShare = objWMIService.Get("Win32_Share")
Return = objNewShare.Create ("C:\Temp", "TestShare", FILE_SHARE, MAXIMUM_CONNECTIONS, "test share")

If Return <> 0 Then
          WScript.Echo Return
          WScript.Quit
End If

Set objShare = objWMIService.Get("Win32_Share.Name='TestShare'")
Return = objShare.GetAccessMask
WScript.Echo Return
```



## <a name="requirements"></a><span data-ttu-id="25b1f-162">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25b1f-162">Requirements</span></span>



| <span data-ttu-id="25b1f-163">Requisito</span><span class="sxs-lookup"><span data-stu-id="25b1f-163">Requirement</span></span> | <span data-ttu-id="25b1f-164">Value</span><span class="sxs-lookup"><span data-stu-id="25b1f-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="25b1f-165">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25b1f-165">Minimum supported client</span></span><br/> | <span data-ttu-id="25b1f-166">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="25b1f-166">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="25b1f-167">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25b1f-167">Minimum supported server</span></span><br/> | <span data-ttu-id="25b1f-168">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="25b1f-168">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="25b1f-169">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="25b1f-169">Namespace</span></span><br/>                | <span data-ttu-id="25b1f-170">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="25b1f-170">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="25b1f-171">MOF</span><span class="sxs-lookup"><span data-stu-id="25b1f-171">MOF</span></span><br/>                      | <dl> <span data-ttu-id="25b1f-172"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="25b1f-172"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="25b1f-173">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="25b1f-173">DLL</span></span><br/>                      | <dl> <span data-ttu-id="25b1f-174"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25b1f-174"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25b1f-175">Vea también</span><span class="sxs-lookup"><span data-stu-id="25b1f-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25b1f-176">**\_Recurso compartido de Win32**</span><span class="sxs-lookup"><span data-stu-id="25b1f-176">**Win32\_Share**</span></span>](win32-share.md)
</dt> </dl>

 

