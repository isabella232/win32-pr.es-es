---
description: Cambia el nombre del archivo lógico (o directorio) especificado en la ruta de acceso del objeto. No se admite el cambio de nombre si el destino está en otra unidad o si se requiere sobrescribir un archivo lógico existente.
ms.assetid: 728737a7-7cb8-4237-be03-16c4dac530b2
ms.tgt_platform: multiple
title: Cambiar el nombre del método de la clase CIM_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 83429f3a5248b1d3be24832b26bf99213d442ce5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496552"
---
# <a name="rename-method-of-the-cim_directory-class"></a><span data-ttu-id="58022-104">Cambiar el nombre del método de la \_ clase de directorio CIM</span><span class="sxs-lookup"><span data-stu-id="58022-104">Rename method of the CIM\_Directory class</span></span>

<span data-ttu-id="58022-105">El método **Rename** cambia el nombre del archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="58022-105">The **Rename** method renames the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="58022-106">No se admite el cambio de nombre si el destino está en otra unidad o si se requiere sobrescribir un archivo lógico existente.</span><span class="sxs-lookup"><span data-stu-id="58022-106">Renaming is not supported if the destination is on another drive or overwriting an existing logical file is required.</span></span>

<span data-ttu-id="58022-107">Este método se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="58022-107">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="58022-108">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="58022-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="58022-109">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="58022-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="58022-110">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="58022-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="58022-111">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="58022-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="58022-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="58022-112">Syntax</span></span>


```mof
uint32 Rename(
  [in] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="58022-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="58022-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58022-114">*Nombre de archivo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="58022-114">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58022-115">Nuevo nombre completo del archivo (o directorio).</span><span class="sxs-lookup"><span data-stu-id="58022-115">Fully qualified new name of the file (or directory).</span></span>

<span data-ttu-id="58022-116">Ejemplo: "c: \\ temp \\newname.txt"</span><span class="sxs-lookup"><span data-stu-id="58022-116">Example: "c:\\temp\\newname.txt"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58022-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="58022-117">Return value</span></span>

<span data-ttu-id="58022-118">Devuelve un valor de 0 (cero) si se realiza correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="58022-118">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="58022-119">**0**</span><span class="sxs-lookup"><span data-stu-id="58022-119">**0**</span></span>
</dt> <dd>

<span data-ttu-id="58022-120">Correcto.</span><span class="sxs-lookup"><span data-stu-id="58022-120">Success.</span></span>

</dd> <dt>

<span data-ttu-id="58022-121">**2**</span><span class="sxs-lookup"><span data-stu-id="58022-121">**2**</span></span>
</dt> <dd>

<span data-ttu-id="58022-122">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="58022-122">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="58022-123">**8**</span><span class="sxs-lookup"><span data-stu-id="58022-123">**8**</span></span>
</dt> <dd>

<span data-ttu-id="58022-124">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="58022-124">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="58022-125">**9**</span><span class="sxs-lookup"><span data-stu-id="58022-125">**9**</span></span>
</dt> <dd>

<span data-ttu-id="58022-126">Objeto no válido.</span><span class="sxs-lookup"><span data-stu-id="58022-126">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="58022-127">**10**</span><span class="sxs-lookup"><span data-stu-id="58022-127">**10**</span></span>
</dt> <dd>

<span data-ttu-id="58022-128">El objeto ya existe.</span><span class="sxs-lookup"><span data-stu-id="58022-128">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="58022-129">**11**</span><span class="sxs-lookup"><span data-stu-id="58022-129">**11**</span></span>
</dt> <dd>

<span data-ttu-id="58022-130">Sistema de archivos no NTFS.</span><span class="sxs-lookup"><span data-stu-id="58022-130">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="58022-131">**12**</span><span class="sxs-lookup"><span data-stu-id="58022-131">**12**</span></span>
</dt> <dd>

<span data-ttu-id="58022-132">Plataforma no Windows.</span><span class="sxs-lookup"><span data-stu-id="58022-132">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="58022-133">**13**</span><span class="sxs-lookup"><span data-stu-id="58022-133">**13**</span></span>
</dt> <dd>

<span data-ttu-id="58022-134">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="58022-134">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="58022-135">**14**</span><span class="sxs-lookup"><span data-stu-id="58022-135">**14**</span></span>
</dt> <dd>

<span data-ttu-id="58022-136">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="58022-136">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="58022-137">**15**</span><span class="sxs-lookup"><span data-stu-id="58022-137">**15**</span></span>
</dt> <dd>

<span data-ttu-id="58022-138">Infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="58022-138">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="58022-139">**16**</span><span class="sxs-lookup"><span data-stu-id="58022-139">**16**</span></span>
</dt> <dd>

<span data-ttu-id="58022-140">Archivo de inicio no válido.</span><span class="sxs-lookup"><span data-stu-id="58022-140">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="58022-141">**17**</span><span class="sxs-lookup"><span data-stu-id="58022-141">**17**</span></span>
</dt> <dd>

<span data-ttu-id="58022-142">Privilegio no mantenido.</span><span class="sxs-lookup"><span data-stu-id="58022-142">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="58022-143">**21**</span><span class="sxs-lookup"><span data-stu-id="58022-143">**21**</span></span>
</dt> <dd>

<span data-ttu-id="58022-144">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="58022-144">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="58022-145">Observaciones</span><span class="sxs-lookup"><span data-stu-id="58022-145">Remarks</span></span>

<span data-ttu-id="58022-146">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="58022-146">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="58022-147">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="58022-147">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="58022-148">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="58022-148">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="58022-149">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="58022-149">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="58022-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58022-150">Requirements</span></span>



| <span data-ttu-id="58022-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="58022-151">Requirement</span></span> | <span data-ttu-id="58022-152">Value</span><span class="sxs-lookup"><span data-stu-id="58022-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="58022-153">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="58022-153">Minimum supported client</span></span><br/> | <span data-ttu-id="58022-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="58022-154">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="58022-155">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="58022-155">Minimum supported server</span></span><br/> | <span data-ttu-id="58022-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="58022-156">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="58022-157">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="58022-157">Namespace</span></span><br/>                | <span data-ttu-id="58022-158">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="58022-158">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="58022-159">MOF</span><span class="sxs-lookup"><span data-stu-id="58022-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="58022-160"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="58022-160"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="58022-161">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="58022-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58022-162"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58022-162"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58022-163">Vea también</span><span class="sxs-lookup"><span data-stu-id="58022-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58022-164">\_Directorio CIM</span><span class="sxs-lookup"><span data-stu-id="58022-164">CIM\_Directory</span></span>](rename-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="58022-165">**\_Directorio CIM**</span><span class="sxs-lookup"><span data-stu-id="58022-165">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

