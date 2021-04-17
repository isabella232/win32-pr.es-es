---
description: Comprime el archivo de entrada de directorio lógico (o directorio) especificado en la ruta de acceso del objeto. Este método se hereda de \_ LOGICALFILE CIM.
ms.assetid: 40aac2f8-4ff6-4e21-9395-5d3d40b39b00
ms.tgt_platform: multiple
title: Método compress de la clase CIM_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.Compress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: f1717e77fdedb0c6b2e218e66f61d67bcef7c1a8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659403"
---
# <a name="compress-method-of-the-cim_directory-class"></a><span data-ttu-id="99c21-104">Método compress de la \_ clase de directorio CIM</span><span class="sxs-lookup"><span data-stu-id="99c21-104">Compress method of the CIM\_Directory class</span></span>

<span data-ttu-id="99c21-105">El método **compress** comprime el archivo de entrada de directorio lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="99c21-105">The **Compress** method compresses the logical directory entry file (or directory) specified in the object path.</span></span> <span data-ttu-id="99c21-106">Este método se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="99c21-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="99c21-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="99c21-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="99c21-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="99c21-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="99c21-109">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="99c21-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="99c21-110">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="99c21-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="99c21-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="99c21-111">Syntax</span></span>


```mof
uint32 Compress();
```



## <a name="parameters"></a><span data-ttu-id="99c21-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="99c21-112">Parameters</span></span>

<span data-ttu-id="99c21-113">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="99c21-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="99c21-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="99c21-114">Return value</span></span>

<span data-ttu-id="99c21-115">Devuelve un valor de 0 (cero) si se realiza correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="99c21-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="99c21-116">**0**</span><span class="sxs-lookup"><span data-stu-id="99c21-116">**0**</span></span>
</dt> <dd>

<span data-ttu-id="99c21-117">Correcto.</span><span class="sxs-lookup"><span data-stu-id="99c21-117">Success.</span></span>

</dd> <dt>

<span data-ttu-id="99c21-118">**2**</span><span class="sxs-lookup"><span data-stu-id="99c21-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="99c21-119">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="99c21-119">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="99c21-120">**8**</span><span class="sxs-lookup"><span data-stu-id="99c21-120">**8**</span></span>
</dt> <dd>

<span data-ttu-id="99c21-121">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="99c21-121">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="99c21-122">**9**</span><span class="sxs-lookup"><span data-stu-id="99c21-122">**9**</span></span>
</dt> <dd>

<span data-ttu-id="99c21-123">Objeto no válido.</span><span class="sxs-lookup"><span data-stu-id="99c21-123">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="99c21-124">**10**</span><span class="sxs-lookup"><span data-stu-id="99c21-124">**10**</span></span>
</dt> <dd>

<span data-ttu-id="99c21-125">El objeto ya existe.</span><span class="sxs-lookup"><span data-stu-id="99c21-125">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="99c21-126">**11**</span><span class="sxs-lookup"><span data-stu-id="99c21-126">**11**</span></span>
</dt> <dd>

<span data-ttu-id="99c21-127">Sistema de archivos no NTFS.</span><span class="sxs-lookup"><span data-stu-id="99c21-127">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="99c21-128">**12**</span><span class="sxs-lookup"><span data-stu-id="99c21-128">**12**</span></span>
</dt> <dd>

<span data-ttu-id="99c21-129">Plataforma no Windows.</span><span class="sxs-lookup"><span data-stu-id="99c21-129">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="99c21-130">**13**</span><span class="sxs-lookup"><span data-stu-id="99c21-130">**13**</span></span>
</dt> <dd>

<span data-ttu-id="99c21-131">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="99c21-131">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="99c21-132">**14**</span><span class="sxs-lookup"><span data-stu-id="99c21-132">**14**</span></span>
</dt> <dd>

<span data-ttu-id="99c21-133">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="99c21-133">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="99c21-134">**15**</span><span class="sxs-lookup"><span data-stu-id="99c21-134">**15**</span></span>
</dt> <dd>

<span data-ttu-id="99c21-135">Infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="99c21-135">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="99c21-136">**16**</span><span class="sxs-lookup"><span data-stu-id="99c21-136">**16**</span></span>
</dt> <dd>

<span data-ttu-id="99c21-137">Archivo de inicio no válido.</span><span class="sxs-lookup"><span data-stu-id="99c21-137">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="99c21-138">**17**</span><span class="sxs-lookup"><span data-stu-id="99c21-138">**17**</span></span>
</dt> <dd>

<span data-ttu-id="99c21-139">Privilegio no mantenido.</span><span class="sxs-lookup"><span data-stu-id="99c21-139">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="99c21-140">**21**</span><span class="sxs-lookup"><span data-stu-id="99c21-140">**21**</span></span>
</dt> <dd>

<span data-ttu-id="99c21-141">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="99c21-141">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="99c21-142">Observaciones</span><span class="sxs-lookup"><span data-stu-id="99c21-142">Remarks</span></span>

<span data-ttu-id="99c21-143">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="99c21-143">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="99c21-144">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="99c21-144">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="99c21-145">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="99c21-145">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="99c21-146">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="99c21-146">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="99c21-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99c21-147">Requirements</span></span>



| <span data-ttu-id="99c21-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="99c21-148">Requirement</span></span> | <span data-ttu-id="99c21-149">Value</span><span class="sxs-lookup"><span data-stu-id="99c21-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="99c21-150">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="99c21-150">Minimum supported client</span></span><br/> | <span data-ttu-id="99c21-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="99c21-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="99c21-152">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="99c21-152">Minimum supported server</span></span><br/> | <span data-ttu-id="99c21-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="99c21-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="99c21-154">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="99c21-154">Namespace</span></span><br/>                | <span data-ttu-id="99c21-155">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="99c21-155">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="99c21-156">MOF</span><span class="sxs-lookup"><span data-stu-id="99c21-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="99c21-157"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="99c21-157"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="99c21-158">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="99c21-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99c21-159"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99c21-159"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99c21-160">Vea también</span><span class="sxs-lookup"><span data-stu-id="99c21-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99c21-161">\_Directorio CIM</span><span class="sxs-lookup"><span data-stu-id="99c21-161">CIM\_Directory</span></span>](compress-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="99c21-162">**\_Directorio CIM**</span><span class="sxs-lookup"><span data-stu-id="99c21-162">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

