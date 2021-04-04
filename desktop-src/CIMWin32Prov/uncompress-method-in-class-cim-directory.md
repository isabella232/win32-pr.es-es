---
description: Descomprime el archivo de entrada de directorio lógico (o directorio) especificado en la ruta de acceso del objeto. Este método se hereda de \_ LOGICALFILE CIM.
ms.assetid: da3616d0-ce45-4e9a-a570-ca9e6bd0a4fa
ms.tgt_platform: multiple
title: Método UNCOMPRESS de la clase CIM_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.Uncompress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: d852305d9153fa61f33168303ccb791caad00f28
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998186"
---
# <a name="uncompress-method-of-the-cim_directory-class"></a><span data-ttu-id="7375f-104">Método UNCOMPRESS de la \_ clase de directorio CIM</span><span class="sxs-lookup"><span data-stu-id="7375f-104">Uncompress method of the CIM\_Directory class</span></span>

<span data-ttu-id="7375f-105">El método **UNCOMPRESS** descomprime el archivo de entrada de directorio lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="7375f-105">The **Uncompress** method uncompresses the logical directory entry file (or directory) specified in the object path.</span></span> <span data-ttu-id="7375f-106">Este método se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="7375f-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7375f-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="7375f-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="7375f-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="7375f-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="7375f-109">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="7375f-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="7375f-110">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="7375f-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="7375f-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7375f-111">Syntax</span></span>


```mof
uint32 Uncompress();
```



## <a name="parameters"></a><span data-ttu-id="7375f-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7375f-112">Parameters</span></span>

<span data-ttu-id="7375f-113">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="7375f-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7375f-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7375f-114">Return value</span></span>

<span data-ttu-id="7375f-115">Devuelve un valor de 0 (cero) si se realiza correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="7375f-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="7375f-116">**0**</span><span class="sxs-lookup"><span data-stu-id="7375f-116">**0**</span></span>
</dt> <dd>

<span data-ttu-id="7375f-117">Correcto.</span><span class="sxs-lookup"><span data-stu-id="7375f-117">Success.</span></span>

</dd> <dt>

<span data-ttu-id="7375f-118">**2**</span><span class="sxs-lookup"><span data-stu-id="7375f-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="7375f-119">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="7375f-119">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="7375f-120">**8**</span><span class="sxs-lookup"><span data-stu-id="7375f-120">**8**</span></span>
</dt> <dd>

<span data-ttu-id="7375f-121">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="7375f-121">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="7375f-122">**9**</span><span class="sxs-lookup"><span data-stu-id="7375f-122">**9**</span></span>
</dt> <dd>

<span data-ttu-id="7375f-123">Objeto no válido.</span><span class="sxs-lookup"><span data-stu-id="7375f-123">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="7375f-124">**10**</span><span class="sxs-lookup"><span data-stu-id="7375f-124">**10**</span></span>
</dt> <dd>

<span data-ttu-id="7375f-125">El objeto ya existe.</span><span class="sxs-lookup"><span data-stu-id="7375f-125">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="7375f-126">**11**</span><span class="sxs-lookup"><span data-stu-id="7375f-126">**11**</span></span>
</dt> <dd>

<span data-ttu-id="7375f-127">Sistema de archivos no NTFS.</span><span class="sxs-lookup"><span data-stu-id="7375f-127">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="7375f-128">**12**</span><span class="sxs-lookup"><span data-stu-id="7375f-128">**12**</span></span>
</dt> <dd>

<span data-ttu-id="7375f-129">Plataforma no Windows.</span><span class="sxs-lookup"><span data-stu-id="7375f-129">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="7375f-130">**13**</span><span class="sxs-lookup"><span data-stu-id="7375f-130">**13**</span></span>
</dt> <dd>

<span data-ttu-id="7375f-131">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="7375f-131">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="7375f-132">**14**</span><span class="sxs-lookup"><span data-stu-id="7375f-132">**14**</span></span>
</dt> <dd>

<span data-ttu-id="7375f-133">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="7375f-133">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="7375f-134">**15**</span><span class="sxs-lookup"><span data-stu-id="7375f-134">**15**</span></span>
</dt> <dd>

<span data-ttu-id="7375f-135">Infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="7375f-135">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="7375f-136">**16**</span><span class="sxs-lookup"><span data-stu-id="7375f-136">**16**</span></span>
</dt> <dd>

<span data-ttu-id="7375f-137">Archivo de inicio no válido.</span><span class="sxs-lookup"><span data-stu-id="7375f-137">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="7375f-138">**17**</span><span class="sxs-lookup"><span data-stu-id="7375f-138">**17**</span></span>
</dt> <dd>

<span data-ttu-id="7375f-139">Privilegio no mantenido.</span><span class="sxs-lookup"><span data-stu-id="7375f-139">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="7375f-140">**21**</span><span class="sxs-lookup"><span data-stu-id="7375f-140">**21**</span></span>
</dt> <dd>

<span data-ttu-id="7375f-141">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="7375f-141">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7375f-142">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7375f-142">Remarks</span></span>

<span data-ttu-id="7375f-143">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="7375f-143">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="7375f-144">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="7375f-144">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="7375f-145">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="7375f-145">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="7375f-146">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="7375f-146">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7375f-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7375f-147">Requirements</span></span>



| <span data-ttu-id="7375f-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="7375f-148">Requirement</span></span> | <span data-ttu-id="7375f-149">Value</span><span class="sxs-lookup"><span data-stu-id="7375f-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7375f-150">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7375f-150">Minimum supported client</span></span><br/> | <span data-ttu-id="7375f-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7375f-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7375f-152">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7375f-152">Minimum supported server</span></span><br/> | <span data-ttu-id="7375f-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7375f-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7375f-154">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7375f-154">Namespace</span></span><br/>                | <span data-ttu-id="7375f-155">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="7375f-155">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7375f-156">MOF</span><span class="sxs-lookup"><span data-stu-id="7375f-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7375f-157"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7375f-157"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7375f-158">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7375f-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7375f-159"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7375f-159"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7375f-160">Vea también</span><span class="sxs-lookup"><span data-stu-id="7375f-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7375f-161">**\_Directorio CIM**</span><span class="sxs-lookup"><span data-stu-id="7375f-161">**CIM\_Directory**</span></span>](uncompress-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="7375f-162">**\_Directorio CIM**</span><span class="sxs-lookup"><span data-stu-id="7375f-162">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

