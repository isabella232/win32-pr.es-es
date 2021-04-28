---
description: 'Método GetAccessMask de la clase Win32_Share: devuelve un mapa de bits uint32 con los derechos de acceso al recurso compartido que mantiene el usuario o grupo en cuyo nombre se devuelve la instancia.'
ms.assetid: 234f44a4-ffff-431d-a973-98f2bd313c7d
ms.tgt_platform: multiple
title: Método GetAccessMask de la Win32_Share clase
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
ms.openlocfilehash: fcd6396f6421060a67108e7c428c99bcd7ca9651
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097023"
---
# <a name="getaccessmask-method-of-the-win32_share-class"></a><span data-ttu-id="f5a0a-103">Método GetAccessMask de la clase Win32 \_ Share</span><span class="sxs-lookup"><span data-stu-id="f5a0a-103">GetAccessMask method of the Win32\_Share class</span></span>

<span data-ttu-id="f5a0a-104">El **método GetAccessMask** devuelve un mapa de bits uint32 con los derechos de acceso al recurso compartido que mantiene el usuario o grupo en cuyo nombre se devuelve la instancia.</span><span class="sxs-lookup"><span data-stu-id="f5a0a-104">The **GetAccessMask** method returns a uint32 bitmap with the access rights to the share held by the user or group on whose behalf the instance is returned.</span></span>

<span data-ttu-id="f5a0a-105">En este tema se Managed Object Format sintaxis de MOF .</span><span class="sxs-lookup"><span data-stu-id="f5a0a-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f5a0a-106">Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="f5a0a-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f5a0a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f5a0a-107">Syntax</span></span>


```mof
uint32 GetAccessMask();
```



## <a name="parameters"></a><span data-ttu-id="f5a0a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f5a0a-108">Parameters</span></span>

<span data-ttu-id="f5a0a-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="f5a0a-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f5a0a-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f5a0a-110">Return value</span></span>

<span data-ttu-id="f5a0a-111">Derechos de acceso al recurso compartido que mantiene el usuario o grupo.</span><span class="sxs-lookup"><span data-stu-id="f5a0a-111">Access rights to the share held by the user or group.</span></span>

<dl> <dt>

<span data-ttu-id="f5a0a-112">**DIRECTORIO DE \_ LISTA DE \_ ARCHIVOS**</span><span class="sxs-lookup"><span data-stu-id="f5a0a-112">**FILE\_LIST\_DIRECTORY**</span></span>
</dt> <dd>

<span data-ttu-id="f5a0a-113">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="f5a0a-113">1 (0x1)</span></span>

<span data-ttu-id="f5a0a-114">Concede el derecho de leer datos del archivo.</span><span class="sxs-lookup"><span data-stu-id="f5a0a-114">Grants the right to read data from the file.</span></span> <span data-ttu-id="f5a0a-115">Para un directorio, este valor concede el derecho de enumerar el contenido del directorio.</span><span class="sxs-lookup"><span data-stu-id="f5a0a-115">For a directory, this value grants the right to list the contents of the directory.</span></span>

</dd> <dt>

<span data-ttu-id="f5a0a-116">**FILE \_ ADD \_ FILE**</span><span class="sxs-lookup"><span data-stu-id="f5a0a-116">**FILE\_ADD\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="f5a0a-117">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="f5a0a-117">2 (0x2)</span></span>

<span data-ttu-id="f5a0a-118">Concede el derecho de escribir datos en el archivo.</span><span class="sxs-lookup"><span data-stu-id="f5a0a-118">Grants the right to write data to the file.</span></span> <span data-ttu-id="f5a0a-119">Para un directorio, este valor concede el derecho de crear un archivo en el directorio.</span><span class="sxs-lookup"><span data-stu-id="f5a0a-119">For a directory, this value grants the right to create a file in the directory.</span></span>

</dd> <dt>

<span data-ttu-id="f5a0a-120">**SUBDIRECTORIO \_ FILE ADD \_**</span><span class="sxs-lookup"><span data-stu-id="f5a0a-120">**FILE\_ADD\_SUBDIRECTORY**</span></span>
</dt> <dd>

<span data-ttu-id="f5a0a-121">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="f5a0a-121">4 (0x4)</span></span>

<span data-ttu-id="f5a0a-122">Concede el derecho a anexar datos al archivo.</span><span class="sxs-lookup"><span data-stu-id="f5a0a-122">Grants the right to append data to the file.</span></span> <span data-ttu-id="f5a0a-123">Para un directorio, este valor concede el derecho a crear un subdirectorio.</span><span class="sxs-lookup"><span data-stu-id="f5a0a-123">For a directory, this value grants the right to create a subdirectory.</span></span>

</dd> <dt>

<span data-ttu-id="f5a0a-124">**FILE \_ READ \_ EA**</span><span class="sxs-lookup"><span data-stu-id="f5a0a-124">**FILE\_READ\_EA**</span></span>
</dt> <dd>

<span data-ttu-id="f5a0a-125">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="f5a0a-125">8 (0x8)</span></span>

<span data-ttu-id="f5a0a-126">Concede el derecho a leer atributos extendidos.</span><span class="sxs-lookup"><span data-stu-id="f5a0a-126">Grants the right to read extended attributes.</span></span>

</dd> <dt>

<span data-ttu-id="f5a0a-127">**EA DE \_ ESCRITURA \_ DE ARCHIVOS**</span><span class="sxs-lookup"><span data-stu-id="f5a0a-127">**FILE\_WRITE\_EA**</span></span>
</dt> <dd>

<span data-ttu-id="f5a0a-128">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="f5a0a-128">16 (0x10)</span></span>

<span data-ttu-id="f5a0a-129">Concede el derecho a escribir atributos extendidos.</span><span class="sxs-lookup"><span data-stu-id="f5a0a-129">Grants the right to write extended attributes.</span></span>

</dd> <dt>

<span data-ttu-id="f5a0a-130">**RECORRIDO DE \_ ARCHIVOS**</span><span class="sxs-lookup"><span data-stu-id="f5a0a-130">**FILE\_TRAVERSE**</span></span>
</dt> <dd>

<span data-ttu-id="f5a0a-131">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="f5a0a-131">32 (0x20)</span></span>

<span data-ttu-id="f5a0a-132">Concede el derecho a ejecutar un archivo.</span><span class="sxs-lookup"><span data-stu-id="f5a0a-132">Grants the right to execute a file.</span></span> <span data-ttu-id="f5a0a-133">Para un directorio, se puede recorrer el directorio.</span><span class="sxs-lookup"><span data-stu-id="f5a0a-133">For a directory, the directory can be traversed.</span></span>

</dd> <dt>

<span data-ttu-id="f5a0a-134">**FILE \_ DELETE \_ CHILD**</span><span class="sxs-lookup"><span data-stu-id="f5a0a-134">**FILE\_DELETE\_CHILD**</span></span>
</dt> <dd>

<span data-ttu-id="f5a0a-135">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="f5a0a-135">64 (0x40)</span></span>

<span data-ttu-id="f5a0a-136">Concede el derecho a eliminar un directorio y todos los archivos que contiene (sus elementos secundarios), incluso si los archivos son de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="f5a0a-136">Grants the right to delete a directory and all of the files it contains (its children), even if the files are read-only.</span></span>

</dd> <dt>

<span data-ttu-id="f5a0a-137">**ATRIBUTOS DE \_ LECTURA \_ DE ARCHIVOS**</span><span class="sxs-lookup"><span data-stu-id="f5a0a-137">**FILE\_READ\_ATTRIBUTES**</span></span>
</dt> <dd>

<span data-ttu-id="f5a0a-138">128 (0x80)</span><span class="sxs-lookup"><span data-stu-id="f5a0a-138">128 (0x80)</span></span>

<span data-ttu-id="f5a0a-139">Concede el derecho a leer atributos de archivo.</span><span class="sxs-lookup"><span data-stu-id="f5a0a-139">Grants the right to read file attributes.</span></span>

</dd> <dt>

<span data-ttu-id="f5a0a-140">**ATRIBUTOS DE \_ ESCRITURA \_ DE ARCHIVOS**</span><span class="sxs-lookup"><span data-stu-id="f5a0a-140">**FILE\_WRITE\_ATTRIBUTES**</span></span>
</dt> <dd>

<span data-ttu-id="f5a0a-141">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="f5a0a-141">256 (0x100)</span></span>

<span data-ttu-id="f5a0a-142">Concede el derecho a cambiar los atributos de archivo.</span><span class="sxs-lookup"><span data-stu-id="f5a0a-142">Grants the right to change file attributes.</span></span>

</dd> <dt>

<span data-ttu-id="f5a0a-143">**DELETE**</span><span class="sxs-lookup"><span data-stu-id="f5a0a-143">**DELETE**</span></span>
</dt> <dd>

<span data-ttu-id="f5a0a-144">65536 (0x10000)</span><span class="sxs-lookup"><span data-stu-id="f5a0a-144">65536 (0x10000)</span></span>

<span data-ttu-id="f5a0a-145">Concede acceso de eliminación.</span><span class="sxs-lookup"><span data-stu-id="f5a0a-145">Grants delete access.</span></span>

</dd> <dt>

<span data-ttu-id="f5a0a-146">**CONTROL DE \_ LECTURA**</span><span class="sxs-lookup"><span data-stu-id="f5a0a-146">**READ\_CONTROL**</span></span>
</dt> <dd>

<span data-ttu-id="f5a0a-147">131072 (0x20000)</span><span class="sxs-lookup"><span data-stu-id="f5a0a-147">131072 (0x20000)</span></span>

<span data-ttu-id="f5a0a-148">Concede acceso de lectura al descriptor de seguridad y al propietario.</span><span class="sxs-lookup"><span data-stu-id="f5a0a-148">Grants read access to the security descriptor and owner.</span></span>

</dd> <dt>

<span data-ttu-id="f5a0a-149">**ESCRIBIR \_ DAC**</span><span class="sxs-lookup"><span data-stu-id="f5a0a-149">**WRITE\_DAC**</span></span>
</dt> <dd>

<span data-ttu-id="f5a0a-150">262144 (0x40000)</span><span class="sxs-lookup"><span data-stu-id="f5a0a-150">262144 (0x40000)</span></span>

<span data-ttu-id="f5a0a-151">Concede acceso de escritura a la lista de control de acceso discrecional (DACL).</span><span class="sxs-lookup"><span data-stu-id="f5a0a-151">Grants write access to the discretionary access control list (DACL).</span></span>

</dd> <dt>

<span data-ttu-id="f5a0a-152">**PROPIETARIO \_ DE ESCRITURA**</span><span class="sxs-lookup"><span data-stu-id="f5a0a-152">**WRITE\_OWNER**</span></span>
</dt> <dd>

<span data-ttu-id="f5a0a-153">524288 (0x80000)</span><span class="sxs-lookup"><span data-stu-id="f5a0a-153">524288 (0x80000)</span></span>

<span data-ttu-id="f5a0a-154">Asigna el propietario de escritura.</span><span class="sxs-lookup"><span data-stu-id="f5a0a-154">Assigns the write owner.</span></span>

</dd> <dt>

<span data-ttu-id="f5a0a-155">**SYNCHRONIZE**</span><span class="sxs-lookup"><span data-stu-id="f5a0a-155">**SYNCHRONIZE**</span></span>
</dt> <dd>

<span data-ttu-id="f5a0a-156">1048576 (0x100000)</span><span class="sxs-lookup"><span data-stu-id="f5a0a-156">1048576 (0x100000)</span></span>

<span data-ttu-id="f5a0a-157">Sincroniza el acceso y permite que un proceso espere a que un objeto entre en el estado señalado.</span><span class="sxs-lookup"><span data-stu-id="f5a0a-157">Synchronizes access and allows a process to wait for an object to enter the signaled state.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f5a0a-158">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f5a0a-158">Remarks</span></span>

<span data-ttu-id="f5a0a-159">**El método GetAccessMask** es un método de objeto y se usa en una aparición de esta clase.</span><span class="sxs-lookup"><span data-stu-id="f5a0a-159">**GetAccessMask** method is an object method and is used on an occurrence of this class.</span></span>

## <a name="examples"></a><span data-ttu-id="f5a0a-160">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f5a0a-160">Examples</span></span>

<span data-ttu-id="f5a0a-161">En el siguiente ejemplo de código de VBScript se crea una carpeta de recurso compartido y, a continuación, se obtiene el valor de la máscara de acceso en el descriptor de seguridad que protege la carpeta del recurso compartido.</span><span class="sxs-lookup"><span data-stu-id="f5a0a-161">The following VBScript code example creates a share folder and then gets the value of the access mask in the security descriptor that secures the share folder.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="f5a0a-162">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5a0a-162">Requirements</span></span>



| <span data-ttu-id="f5a0a-163">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5a0a-163">Requirement</span></span> | <span data-ttu-id="f5a0a-164">Valor</span><span class="sxs-lookup"><span data-stu-id="f5a0a-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5a0a-165">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f5a0a-165">Minimum supported client</span></span><br/> | <span data-ttu-id="f5a0a-166">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f5a0a-166">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f5a0a-167">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f5a0a-167">Minimum supported server</span></span><br/> | <span data-ttu-id="f5a0a-168">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f5a0a-168">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f5a0a-169">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f5a0a-169">Namespace</span></span><br/>                | <span data-ttu-id="f5a0a-170">\\CIMV2 raíz</span><span class="sxs-lookup"><span data-stu-id="f5a0a-170">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f5a0a-171">MOF</span><span class="sxs-lookup"><span data-stu-id="f5a0a-171">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f5a0a-172"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="f5a0a-172"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f5a0a-173">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f5a0a-173">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5a0a-174"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5a0a-174"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5a0a-175">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f5a0a-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5a0a-176">**Recurso compartido de \_ Win32**</span><span class="sxs-lookup"><span data-stu-id="f5a0a-176">**Win32\_Share**</span></span>](win32-share.md)
</dt> </dl>

 

