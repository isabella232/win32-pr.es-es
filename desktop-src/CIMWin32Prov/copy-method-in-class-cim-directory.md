---
description: 'Método copy de la clase CIM_Directory: el método Copy copia el archivo lógico (o directorio) especificado en la ruta de acceso del objeto a la ubicación especificada por el parámetro de entrada.'
ms.assetid: 71481cc8-9052-4c62-9c26-6887ea646ee1
ms.tgt_platform: multiple
title: Método Copy de la CIM_Directory clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.Copy
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6aff8ce62cf0358f494d5b3d83872b831e07ec4b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089743"
---
# <a name="copy-method-of-the-cim_directory-class"></a><span data-ttu-id="2a967-103">Método copy de la clase \_ Cim Directory</span><span class="sxs-lookup"><span data-stu-id="2a967-103">Copy method of the CIM\_Directory class</span></span>

<span data-ttu-id="2a967-104">El **método Copy** copia el archivo lógico (o directorio) especificado en la ruta de acceso del objeto a la ubicación especificada por el parámetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="2a967-104">The **Copy** method copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="2a967-105">No se admite una copia si se requiere sobrescribir un archivo lógico existente.</span><span class="sxs-lookup"><span data-stu-id="2a967-105">A copy is not supported if overwriting an existing logical file is required.</span></span> <span data-ttu-id="2a967-106">Este método se hereda de [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="2a967-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2a967-107">Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se construyen las clases WMI.</span><span class="sxs-lookup"><span data-stu-id="2a967-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2a967-108">WMI admite actualmente solo los esquemas [de versión CIM 2.x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="2a967-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2a967-109">En este tema se usa Managed Object Format sintaxis MOF .</span><span class="sxs-lookup"><span data-stu-id="2a967-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="2a967-110">Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="2a967-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="2a967-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2a967-111">Syntax</span></span>


```mof
uint32 Copy(
  [in] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="2a967-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2a967-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a967-113">*FileName* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="2a967-113">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a967-114">Nombre completo de la copia del archivo de destino (o directorio).</span><span class="sxs-lookup"><span data-stu-id="2a967-114">Fully qualified name of the copy of the destination file (or directory).</span></span>

<span data-ttu-id="2a967-115">Ejemplo: "c: \\ temp \\ newdirectory"</span><span class="sxs-lookup"><span data-stu-id="2a967-115">Example: "c:\\temp\\newdirectory"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a967-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2a967-116">Return value</span></span>

<span data-ttu-id="2a967-117">Devuelve un valor de 0 si se ejecuta correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="2a967-117">Returns a value of 0 on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="2a967-118">**0**</span><span class="sxs-lookup"><span data-stu-id="2a967-118">**0**</span></span>
</dt> <dd>

<span data-ttu-id="2a967-119">Correcto.</span><span class="sxs-lookup"><span data-stu-id="2a967-119">Success.</span></span>

</dd> <dt>

<span data-ttu-id="2a967-120">**2**</span><span class="sxs-lookup"><span data-stu-id="2a967-120">**2**</span></span>
</dt> <dd>

<span data-ttu-id="2a967-121">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="2a967-121">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="2a967-122">**8**</span><span class="sxs-lookup"><span data-stu-id="2a967-122">**8**</span></span>
</dt> <dd>

<span data-ttu-id="2a967-123">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="2a967-123">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="2a967-124">**9**</span><span class="sxs-lookup"><span data-stu-id="2a967-124">**9**</span></span>
</dt> <dd>

<span data-ttu-id="2a967-125">Objeto no válido.</span><span class="sxs-lookup"><span data-stu-id="2a967-125">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="2a967-126">**10**</span><span class="sxs-lookup"><span data-stu-id="2a967-126">**10**</span></span>
</dt> <dd>

<span data-ttu-id="2a967-127">El objeto ya existe.</span><span class="sxs-lookup"><span data-stu-id="2a967-127">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="2a967-128">**11**</span><span class="sxs-lookup"><span data-stu-id="2a967-128">**11**</span></span>
</dt> <dd>

<span data-ttu-id="2a967-129">El sistema de archivos no es NTFS.</span><span class="sxs-lookup"><span data-stu-id="2a967-129">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="2a967-130">**12**</span><span class="sxs-lookup"><span data-stu-id="2a967-130">**12**</span></span>
</dt> <dd>

<span data-ttu-id="2a967-131">Plataforma no Windows.</span><span class="sxs-lookup"><span data-stu-id="2a967-131">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="2a967-132">**13**</span><span class="sxs-lookup"><span data-stu-id="2a967-132">**13**</span></span>
</dt> <dd>

<span data-ttu-id="2a967-133">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="2a967-133">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="2a967-134">**14**</span><span class="sxs-lookup"><span data-stu-id="2a967-134">**14**</span></span>
</dt> <dd>

<span data-ttu-id="2a967-135">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="2a967-135">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="2a967-136">**15**</span><span class="sxs-lookup"><span data-stu-id="2a967-136">**15**</span></span>
</dt> <dd>

<span data-ttu-id="2a967-137">Infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="2a967-137">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="2a967-138">**16**</span><span class="sxs-lookup"><span data-stu-id="2a967-138">**16**</span></span>
</dt> <dd>

<span data-ttu-id="2a967-139">Archivo de inicio no válido.</span><span class="sxs-lookup"><span data-stu-id="2a967-139">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="2a967-140">**17**</span><span class="sxs-lookup"><span data-stu-id="2a967-140">**17**</span></span>
</dt> <dd>

<span data-ttu-id="2a967-141">Privilegio no mantenido.</span><span class="sxs-lookup"><span data-stu-id="2a967-141">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="2a967-142">**21**</span><span class="sxs-lookup"><span data-stu-id="2a967-142">**21**</span></span>
</dt> <dd>

<span data-ttu-id="2a967-143">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="2a967-143">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2a967-144">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2a967-144">Remarks</span></span>

<span data-ttu-id="2a967-145">Wmi no implementa actualmente este método.</span><span class="sxs-lookup"><span data-stu-id="2a967-145">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="2a967-146">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="2a967-146">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="2a967-147">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="2a967-147">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2a967-148">Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="2a967-148">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a967-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a967-149">Requirements</span></span>



| <span data-ttu-id="2a967-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a967-150">Requirement</span></span> | <span data-ttu-id="2a967-151">Valor</span><span class="sxs-lookup"><span data-stu-id="2a967-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2a967-152">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2a967-152">Minimum supported client</span></span><br/> | <span data-ttu-id="2a967-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2a967-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2a967-154">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2a967-154">Minimum supported server</span></span><br/> | <span data-ttu-id="2a967-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2a967-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2a967-156">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2a967-156">Namespace</span></span><br/>                | <span data-ttu-id="2a967-157">\\CIMV2 raíz</span><span class="sxs-lookup"><span data-stu-id="2a967-157">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2a967-158">MOF</span><span class="sxs-lookup"><span data-stu-id="2a967-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2a967-159"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="2a967-159"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2a967-160">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2a967-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2a967-161"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2a967-161"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a967-162">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2a967-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a967-163">Directorio \_ CIM</span><span class="sxs-lookup"><span data-stu-id="2a967-163">CIM\_Directory</span></span>](copy-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="2a967-164">**Directorio \_ CIM**</span><span class="sxs-lookup"><span data-stu-id="2a967-164">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

