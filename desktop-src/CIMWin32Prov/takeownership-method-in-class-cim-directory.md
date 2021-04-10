---
description: El método TakeOwnerShip obtiene la propiedad del archivo lógico especificado en la ruta de acceso del objeto.
ms.assetid: 053647d0-3ba0-4cd4-a84a-a1a96ef7151c
ms.tgt_platform: multiple
title: Método TakeOwnerShip de la clase CIM_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.TakeOwnerShip
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: dc68e974c98405f03c4bbfb45f02fdf78bf65127
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275100"
---
# <a name="takeownership-method-of-the-cim_directory-class"></a><span data-ttu-id="833d4-103">Método TakeOwnerShip de la \_ clase de directorio CIM</span><span class="sxs-lookup"><span data-stu-id="833d4-103">TakeOwnerShip method of the CIM\_Directory class</span></span>

<span data-ttu-id="833d4-104">El método **TakeOwnerShip** obtiene la propiedad del archivo lógico especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="833d4-104">The **TakeOwnerShip** method obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="833d4-105">Si el archivo lógico es un directorio, este método actúa de forma recursiva y toma la propiedad de todos los archivos y subdirectorios que contiene el directorio.</span><span class="sxs-lookup"><span data-stu-id="833d4-105">If the logical file is a directory, this method acts recursively, taking ownership of all of the files and sub-directories that the directory contains.</span></span> <span data-ttu-id="833d4-106">Este método se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="833d4-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="833d4-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="833d4-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="833d4-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="833d4-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="833d4-109">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="833d4-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="833d4-110">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="833d4-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="833d4-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="833d4-111">Syntax</span></span>


```mof
uint32 TakeOwnerShip();
```



## <a name="parameters"></a><span data-ttu-id="833d4-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="833d4-112">Parameters</span></span>

<span data-ttu-id="833d4-113">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="833d4-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="833d4-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="833d4-114">Return value</span></span>

<span data-ttu-id="833d4-115">Devuelve un valor de 0 (cero) si se realiza correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="833d4-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="833d4-116">**0**</span><span class="sxs-lookup"><span data-stu-id="833d4-116">**0**</span></span>
</dt> <dd>

<span data-ttu-id="833d4-117">Correcto.</span><span class="sxs-lookup"><span data-stu-id="833d4-117">Success.</span></span>

</dd> <dt>

<span data-ttu-id="833d4-118">**2**</span><span class="sxs-lookup"><span data-stu-id="833d4-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="833d4-119">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="833d4-119">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="833d4-120">**8**</span><span class="sxs-lookup"><span data-stu-id="833d4-120">**8**</span></span>
</dt> <dd>

<span data-ttu-id="833d4-121">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="833d4-121">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="833d4-122">**9**</span><span class="sxs-lookup"><span data-stu-id="833d4-122">**9**</span></span>
</dt> <dd>

<span data-ttu-id="833d4-123">Objeto no válido.</span><span class="sxs-lookup"><span data-stu-id="833d4-123">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="833d4-124">**10**</span><span class="sxs-lookup"><span data-stu-id="833d4-124">**10**</span></span>
</dt> <dd>

<span data-ttu-id="833d4-125">El objeto ya existe.</span><span class="sxs-lookup"><span data-stu-id="833d4-125">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="833d4-126">**11**</span><span class="sxs-lookup"><span data-stu-id="833d4-126">**11**</span></span>
</dt> <dd>

<span data-ttu-id="833d4-127">Sistema de archivos no NTFS.</span><span class="sxs-lookup"><span data-stu-id="833d4-127">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="833d4-128">**12**</span><span class="sxs-lookup"><span data-stu-id="833d4-128">**12**</span></span>
</dt> <dd>

<span data-ttu-id="833d4-129">La plataforma no es Windows.</span><span class="sxs-lookup"><span data-stu-id="833d4-129">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="833d4-130">**13**</span><span class="sxs-lookup"><span data-stu-id="833d4-130">**13**</span></span>
</dt> <dd>

<span data-ttu-id="833d4-131">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="833d4-131">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="833d4-132">**14**</span><span class="sxs-lookup"><span data-stu-id="833d4-132">**14**</span></span>
</dt> <dd>

<span data-ttu-id="833d4-133">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="833d4-133">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="833d4-134">**15**</span><span class="sxs-lookup"><span data-stu-id="833d4-134">**15**</span></span>
</dt> <dd>

<span data-ttu-id="833d4-135">Infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="833d4-135">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="833d4-136">**16**</span><span class="sxs-lookup"><span data-stu-id="833d4-136">**16**</span></span>
</dt> <dd>

<span data-ttu-id="833d4-137">Archivo de inicio no válido.</span><span class="sxs-lookup"><span data-stu-id="833d4-137">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="833d4-138">**17**</span><span class="sxs-lookup"><span data-stu-id="833d4-138">**17**</span></span>
</dt> <dd>

<span data-ttu-id="833d4-139">Privilegio no mantenido.</span><span class="sxs-lookup"><span data-stu-id="833d4-139">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="833d4-140">**21**</span><span class="sxs-lookup"><span data-stu-id="833d4-140">**21**</span></span>
</dt> <dd>

<span data-ttu-id="833d4-141">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="833d4-141">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="833d4-142">Observaciones</span><span class="sxs-lookup"><span data-stu-id="833d4-142">Remarks</span></span>

<span data-ttu-id="833d4-143">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="833d4-143">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="833d4-144">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="833d4-144">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="833d4-145">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="833d4-145">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="833d4-146">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="833d4-146">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="examples"></a><span data-ttu-id="833d4-147">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="833d4-147">Examples</span></span>

<span data-ttu-id="833d4-148">El siguiente código de script de Visual Basic llama al método **TakeOwnerShip** para tomar posesión de la \\ carpeta C: Temp.</span><span class="sxs-lookup"><span data-stu-id="833d4-148">The following Visual Basic Script code calls the **TakeOwnerShip** method to take ownership of the C:\\temp folder.</span></span>


```VB
strComputer = "." 

Set objWMIService = _
    GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 

' Obtain the definition of the class.
Set objShare = objWMIService.Get("Win32_Directory")

' Execute the method and obtain the return status.
' The OutParameters object in objOutParams
' is created by the provider.
Set objOutParams = objWMIService.ExecMethod( _
    "Win32_Directory.Name='C:\\temp'", "TakeOwnerShip")

wscript.echo objOutParams.ReturnValue
```



## <a name="requirements"></a><span data-ttu-id="833d4-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="833d4-149">Requirements</span></span>



| <span data-ttu-id="833d4-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="833d4-150">Requirement</span></span> | <span data-ttu-id="833d4-151">Value</span><span class="sxs-lookup"><span data-stu-id="833d4-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="833d4-152">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="833d4-152">Minimum supported client</span></span><br/> | <span data-ttu-id="833d4-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="833d4-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="833d4-154">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="833d4-154">Minimum supported server</span></span><br/> | <span data-ttu-id="833d4-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="833d4-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="833d4-156">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="833d4-156">Namespace</span></span><br/>                | <span data-ttu-id="833d4-157">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="833d4-157">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="833d4-158">MOF</span><span class="sxs-lookup"><span data-stu-id="833d4-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="833d4-159"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="833d4-159"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="833d4-160">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="833d4-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="833d4-161"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="833d4-161"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="833d4-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="833d4-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="833d4-163">\_Directorio CIM</span><span class="sxs-lookup"><span data-stu-id="833d4-163">CIM\_Directory</span></span>](takeownership-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="833d4-164">**\_Directorio CIM**</span><span class="sxs-lookup"><span data-stu-id="833d4-164">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

