---
description: 'Método TakeOwnerShip de CIM_Directory clase : el método TakeOwnerShip obtiene la propiedad del archivo lógico especificado en la ruta de acceso del objeto.'
ms.assetid: 053647d0-3ba0-4cd4-a84a-a1a96ef7151c
ms.tgt_platform: multiple
title: Método TakeOwnerShip de la CIM_Directory clase
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
ms.openlocfilehash: 12c328f30e56db348b018b73b02aa4320bf99505
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086063"
---
# <a name="takeownership-method-of-the-cim_directory-class"></a><span data-ttu-id="88539-103">Método TakeOwnerShip de la clase \_ De directorio CIM</span><span class="sxs-lookup"><span data-stu-id="88539-103">TakeOwnerShip method of the CIM\_Directory class</span></span>

<span data-ttu-id="88539-104">El **método TakeOwnerShip** obtiene la propiedad del archivo lógico especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="88539-104">The **TakeOwnerShip** method obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="88539-105">Si el archivo lógico es un directorio, este método actúa de forma recursiva, tomando posesión de todos los archivos y subdirectorios que contiene el directorio.</span><span class="sxs-lookup"><span data-stu-id="88539-105">If the logical file is a directory, this method acts recursively, taking ownership of all of the files and sub-directories that the directory contains.</span></span> <span data-ttu-id="88539-106">Este método se hereda de [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="88539-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="88539-107">Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se construyen las clases WMI.</span><span class="sxs-lookup"><span data-stu-id="88539-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="88539-108">WMI admite actualmente solo los esquemas [de versión CIM 2.x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="88539-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="88539-109">En este tema se usa Managed Object Format sintaxis MOF .</span><span class="sxs-lookup"><span data-stu-id="88539-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="88539-110">Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="88539-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="88539-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="88539-111">Syntax</span></span>


```mof
uint32 TakeOwnerShip();
```



## <a name="parameters"></a><span data-ttu-id="88539-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="88539-112">Parameters</span></span>

<span data-ttu-id="88539-113">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="88539-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="88539-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="88539-114">Return value</span></span>

<span data-ttu-id="88539-115">Devuelve un valor de 0 (cero) si se ejecuta correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="88539-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="88539-116">**0**</span><span class="sxs-lookup"><span data-stu-id="88539-116">**0**</span></span>
</dt> <dd>

<span data-ttu-id="88539-117">Correcto.</span><span class="sxs-lookup"><span data-stu-id="88539-117">Success.</span></span>

</dd> <dt>

<span data-ttu-id="88539-118">**2**</span><span class="sxs-lookup"><span data-stu-id="88539-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="88539-119">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="88539-119">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="88539-120">**8**</span><span class="sxs-lookup"><span data-stu-id="88539-120">**8**</span></span>
</dt> <dd>

<span data-ttu-id="88539-121">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="88539-121">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="88539-122">**9**</span><span class="sxs-lookup"><span data-stu-id="88539-122">**9**</span></span>
</dt> <dd>

<span data-ttu-id="88539-123">Objeto no válido.</span><span class="sxs-lookup"><span data-stu-id="88539-123">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="88539-124">**10**</span><span class="sxs-lookup"><span data-stu-id="88539-124">**10**</span></span>
</dt> <dd>

<span data-ttu-id="88539-125">El objeto ya existe.</span><span class="sxs-lookup"><span data-stu-id="88539-125">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="88539-126">**11**</span><span class="sxs-lookup"><span data-stu-id="88539-126">**11**</span></span>
</dt> <dd>

<span data-ttu-id="88539-127">El sistema de archivos no es NTFS.</span><span class="sxs-lookup"><span data-stu-id="88539-127">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="88539-128">**12**</span><span class="sxs-lookup"><span data-stu-id="88539-128">**12**</span></span>
</dt> <dd>

<span data-ttu-id="88539-129">La plataforma no es Windows.</span><span class="sxs-lookup"><span data-stu-id="88539-129">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="88539-130">**13**</span><span class="sxs-lookup"><span data-stu-id="88539-130">**13**</span></span>
</dt> <dd>

<span data-ttu-id="88539-131">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="88539-131">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="88539-132">**14**</span><span class="sxs-lookup"><span data-stu-id="88539-132">**14**</span></span>
</dt> <dd>

<span data-ttu-id="88539-133">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="88539-133">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="88539-134">**15**</span><span class="sxs-lookup"><span data-stu-id="88539-134">**15**</span></span>
</dt> <dd>

<span data-ttu-id="88539-135">Infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="88539-135">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="88539-136">**16**</span><span class="sxs-lookup"><span data-stu-id="88539-136">**16**</span></span>
</dt> <dd>

<span data-ttu-id="88539-137">Archivo de inicio no válido.</span><span class="sxs-lookup"><span data-stu-id="88539-137">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="88539-138">**17**</span><span class="sxs-lookup"><span data-stu-id="88539-138">**17**</span></span>
</dt> <dd>

<span data-ttu-id="88539-139">Privilegios no mantenidos.</span><span class="sxs-lookup"><span data-stu-id="88539-139">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="88539-140">**21**</span><span class="sxs-lookup"><span data-stu-id="88539-140">**21**</span></span>
</dt> <dd>

<span data-ttu-id="88539-141">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="88539-141">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="88539-142">Comentarios</span><span class="sxs-lookup"><span data-stu-id="88539-142">Remarks</span></span>

<span data-ttu-id="88539-143">Wmi no implementa actualmente este método.</span><span class="sxs-lookup"><span data-stu-id="88539-143">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="88539-144">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="88539-144">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="88539-145">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="88539-145">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="88539-146">Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="88539-146">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="examples"></a><span data-ttu-id="88539-147">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="88539-147">Examples</span></span>

<span data-ttu-id="88539-148">El siguiente Visual Basic script llama al **método TakeOwnerShip** para tomar posesión de la carpeta \\ temporal C:.</span><span class="sxs-lookup"><span data-stu-id="88539-148">The following Visual Basic Script code calls the **TakeOwnerShip** method to take ownership of the C:\\temp folder.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="88539-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88539-149">Requirements</span></span>



| <span data-ttu-id="88539-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="88539-150">Requirement</span></span> | <span data-ttu-id="88539-151">Valor</span><span class="sxs-lookup"><span data-stu-id="88539-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="88539-152">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="88539-152">Minimum supported client</span></span><br/> | <span data-ttu-id="88539-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="88539-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="88539-154">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="88539-154">Minimum supported server</span></span><br/> | <span data-ttu-id="88539-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="88539-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="88539-156">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="88539-156">Namespace</span></span><br/>                | <span data-ttu-id="88539-157">\\CIMV2 raíz</span><span class="sxs-lookup"><span data-stu-id="88539-157">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="88539-158">MOF</span><span class="sxs-lookup"><span data-stu-id="88539-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="88539-159"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="88539-159"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="88539-160">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="88539-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88539-161"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88539-161"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88539-162">Consulte también</span><span class="sxs-lookup"><span data-stu-id="88539-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88539-163">Directorio \_ CIM</span><span class="sxs-lookup"><span data-stu-id="88539-163">CIM\_Directory</span></span>](takeownership-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="88539-164">**Directorio \_ CIM**</span><span class="sxs-lookup"><span data-stu-id="88539-164">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

