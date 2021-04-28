---
description: 'Método Delete de la CIM_Directory : el método Delete elimina el archivo lógico (o directorio) especificado en la ruta de acceso del objeto. Este método se hereda de CIM \_ LogicalFile.'
ms.assetid: 74f59073-a17a-4be5-8247-fba8d023f448
ms.tgt_platform: multiple
title: Método Delete de la CIM_Directory clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6d02c9eb6b603673228671b12df98c7b6884abdd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089643"
---
# <a name="delete-method-of-the-cim_directory-class"></a><span data-ttu-id="1fc43-104">Método Delete de la clase \_ Cim Directory</span><span class="sxs-lookup"><span data-stu-id="1fc43-104">Delete method of the CIM\_Directory class</span></span>

<span data-ttu-id="1fc43-105">El **método Delete** elimina el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="1fc43-105">The **Delete** method deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="1fc43-106">Este método se hereda de [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="1fc43-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1fc43-107">Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se construyen las clases WMI.</span><span class="sxs-lookup"><span data-stu-id="1fc43-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="1fc43-108">WMI admite actualmente solo los esquemas [de versión CIM 2.x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="1fc43-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="1fc43-109">En este tema se usa Managed Object Format sintaxis MOF .</span><span class="sxs-lookup"><span data-stu-id="1fc43-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="1fc43-110">Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="1fc43-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="1fc43-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1fc43-111">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="1fc43-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1fc43-112">Parameters</span></span>

<span data-ttu-id="1fc43-113">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="1fc43-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1fc43-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1fc43-114">Return value</span></span>

<span data-ttu-id="1fc43-115">Devuelve un valor de 0 (cero) si se ejecuta correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="1fc43-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="1fc43-116">**0**</span><span class="sxs-lookup"><span data-stu-id="1fc43-116">**0**</span></span>
</dt> <dd>

<span data-ttu-id="1fc43-117">Correcto.</span><span class="sxs-lookup"><span data-stu-id="1fc43-117">Success.</span></span>

</dd> <dt>

<span data-ttu-id="1fc43-118">**2**</span><span class="sxs-lookup"><span data-stu-id="1fc43-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="1fc43-119">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="1fc43-119">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="1fc43-120">**8**</span><span class="sxs-lookup"><span data-stu-id="1fc43-120">**8**</span></span>
</dt> <dd>

<span data-ttu-id="1fc43-121">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="1fc43-121">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="1fc43-122">**9**</span><span class="sxs-lookup"><span data-stu-id="1fc43-122">**9**</span></span>
</dt> <dd>

<span data-ttu-id="1fc43-123">Objeto no válido.</span><span class="sxs-lookup"><span data-stu-id="1fc43-123">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="1fc43-124">**10**</span><span class="sxs-lookup"><span data-stu-id="1fc43-124">**10**</span></span>
</dt> <dd>

<span data-ttu-id="1fc43-125">El objeto ya existe.</span><span class="sxs-lookup"><span data-stu-id="1fc43-125">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="1fc43-126">**11**</span><span class="sxs-lookup"><span data-stu-id="1fc43-126">**11**</span></span>
</dt> <dd>

<span data-ttu-id="1fc43-127">El sistema de archivos no es NTFS.</span><span class="sxs-lookup"><span data-stu-id="1fc43-127">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="1fc43-128">**12**</span><span class="sxs-lookup"><span data-stu-id="1fc43-128">**12**</span></span>
</dt> <dd>

<span data-ttu-id="1fc43-129">Plataforma no Windows.</span><span class="sxs-lookup"><span data-stu-id="1fc43-129">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="1fc43-130">**13**</span><span class="sxs-lookup"><span data-stu-id="1fc43-130">**13**</span></span>
</dt> <dd>

<span data-ttu-id="1fc43-131">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="1fc43-131">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="1fc43-132">**14**</span><span class="sxs-lookup"><span data-stu-id="1fc43-132">**14**</span></span>
</dt> <dd>

<span data-ttu-id="1fc43-133">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="1fc43-133">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="1fc43-134">**15**</span><span class="sxs-lookup"><span data-stu-id="1fc43-134">**15**</span></span>
</dt> <dd>

<span data-ttu-id="1fc43-135">Infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="1fc43-135">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="1fc43-136">**16**</span><span class="sxs-lookup"><span data-stu-id="1fc43-136">**16**</span></span>
</dt> <dd>

<span data-ttu-id="1fc43-137">Archivo de inicio no válido.</span><span class="sxs-lookup"><span data-stu-id="1fc43-137">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="1fc43-138">**17**</span><span class="sxs-lookup"><span data-stu-id="1fc43-138">**17**</span></span>
</dt> <dd>

<span data-ttu-id="1fc43-139">Privilegios no mantenidos.</span><span class="sxs-lookup"><span data-stu-id="1fc43-139">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="1fc43-140">**21**</span><span class="sxs-lookup"><span data-stu-id="1fc43-140">**21**</span></span>
</dt> <dd>

<span data-ttu-id="1fc43-141">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="1fc43-141">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1fc43-142">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1fc43-142">Remarks</span></span>

<span data-ttu-id="1fc43-143">Wmi no implementa actualmente este método.</span><span class="sxs-lookup"><span data-stu-id="1fc43-143">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="1fc43-144">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="1fc43-144">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="1fc43-145">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="1fc43-145">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="1fc43-146">Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="1fc43-146">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fc43-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1fc43-147">Requirements</span></span>



| <span data-ttu-id="1fc43-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="1fc43-148">Requirement</span></span> | <span data-ttu-id="1fc43-149">Valor</span><span class="sxs-lookup"><span data-stu-id="1fc43-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1fc43-150">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1fc43-150">Minimum supported client</span></span><br/> | <span data-ttu-id="1fc43-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1fc43-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1fc43-152">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1fc43-152">Minimum supported server</span></span><br/> | <span data-ttu-id="1fc43-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1fc43-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1fc43-154">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1fc43-154">Namespace</span></span><br/>                | <span data-ttu-id="1fc43-155">\\CIMV2 raíz</span><span class="sxs-lookup"><span data-stu-id="1fc43-155">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1fc43-156">MOF</span><span class="sxs-lookup"><span data-stu-id="1fc43-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1fc43-157"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="1fc43-157"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1fc43-158">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1fc43-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1fc43-159"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1fc43-159"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1fc43-160">Consulte también</span><span class="sxs-lookup"><span data-stu-id="1fc43-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fc43-161">Directorio \_ CIM</span><span class="sxs-lookup"><span data-stu-id="1fc43-161">CIM\_Directory</span></span>](delete-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="1fc43-162">**Directorio \_ CIM**</span><span class="sxs-lookup"><span data-stu-id="1fc43-162">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

