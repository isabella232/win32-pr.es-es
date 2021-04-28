---
description: 'Método copy de la clase CIM_DeviceFile: el método Copy copia el archivo lógico (o directorio) especificado en la ruta de acceso del objeto a la ubicación especificada por el parámetro de entrada.'
ms.assetid: 6c1c6172-80a2-4779-903a-935f8c7091a5
ms.tgt_platform: multiple
title: Método Copy de la clase CIM_DeviceFile copia
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.Copy
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 09c6d0f9400a04cc6e5a8ed4bd49ec7075b3c190
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089812"
---
# <a name="copy-method-of-the-cim_devicefile-class"></a><span data-ttu-id="4ab1c-103">Método Copy de la clase \_ DeviceFile de CIM</span><span class="sxs-lookup"><span data-stu-id="4ab1c-103">Copy method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="4ab1c-104">El **método Copy** copia el archivo lógico (o directorio) especificado en la ruta de acceso del objeto a la ubicación especificada por el parámetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="4ab1c-104">The **Copy** method copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="4ab1c-105">No se admite una copia si requiere sobrescribir un archivo lógico existente.</span><span class="sxs-lookup"><span data-stu-id="4ab1c-105">A copy is not supported if it requires overwriting an existing logical file.</span></span> <span data-ttu-id="4ab1c-106">Este método se hereda de [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="4ab1c-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4ab1c-107">Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI.</span><span class="sxs-lookup"><span data-stu-id="4ab1c-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4ab1c-108">WMI admite actualmente solo los esquemas [de la versión CIM 2.x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4ab1c-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4ab1c-109">En este tema se Managed Object Format sintaxis de MOF .</span><span class="sxs-lookup"><span data-stu-id="4ab1c-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="4ab1c-110">Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="4ab1c-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="4ab1c-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4ab1c-111">Syntax</span></span>


```mof
uint32 Copy(
  [in] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="4ab1c-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4ab1c-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ab1c-113">*FileName* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="4ab1c-113">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ab1c-114">Nombre completo de la copia del archivo (o directorio) de destino.</span><span class="sxs-lookup"><span data-stu-id="4ab1c-114">Fully qualified name of the destination file (or directory) copy.</span></span>

<span data-ttu-id="4ab1c-115">Ejemplo: "c: \\ temp \\ newdirectory"</span><span class="sxs-lookup"><span data-stu-id="4ab1c-115">Example: "c:\\temp\\newdirectory"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ab1c-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4ab1c-116">Return value</span></span>

<span data-ttu-id="4ab1c-117">Devuelve un valor de 0 (cero) si se ejecuta correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="4ab1c-117">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="4ab1c-118">**0**</span><span class="sxs-lookup"><span data-stu-id="4ab1c-118">**0**</span></span>
</dt> <dd>

<span data-ttu-id="4ab1c-119">Correcto.</span><span class="sxs-lookup"><span data-stu-id="4ab1c-119">Success.</span></span>

</dd> <dt>

<span data-ttu-id="4ab1c-120">**2**</span><span class="sxs-lookup"><span data-stu-id="4ab1c-120">**2**</span></span>
</dt> <dd>

<span data-ttu-id="4ab1c-121">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="4ab1c-121">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="4ab1c-122">**8**</span><span class="sxs-lookup"><span data-stu-id="4ab1c-122">**8**</span></span>
</dt> <dd>

<span data-ttu-id="4ab1c-123">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="4ab1c-123">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="4ab1c-124">**9**</span><span class="sxs-lookup"><span data-stu-id="4ab1c-124">**9**</span></span>
</dt> <dd>

<span data-ttu-id="4ab1c-125">Objeto no válido.</span><span class="sxs-lookup"><span data-stu-id="4ab1c-125">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="4ab1c-126">**10**</span><span class="sxs-lookup"><span data-stu-id="4ab1c-126">**10**</span></span>
</dt> <dd>

<span data-ttu-id="4ab1c-127">El objeto ya existe.</span><span class="sxs-lookup"><span data-stu-id="4ab1c-127">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="4ab1c-128">**11**</span><span class="sxs-lookup"><span data-stu-id="4ab1c-128">**11**</span></span>
</dt> <dd>

<span data-ttu-id="4ab1c-129">Sistema de archivos no NTFS.</span><span class="sxs-lookup"><span data-stu-id="4ab1c-129">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="4ab1c-130">**12**</span><span class="sxs-lookup"><span data-stu-id="4ab1c-130">**12**</span></span>
</dt> <dd>

<span data-ttu-id="4ab1c-131">Plataforma no Windows.</span><span class="sxs-lookup"><span data-stu-id="4ab1c-131">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="4ab1c-132">**13**</span><span class="sxs-lookup"><span data-stu-id="4ab1c-132">**13**</span></span>
</dt> <dd>

<span data-ttu-id="4ab1c-133">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="4ab1c-133">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="4ab1c-134">**14**</span><span class="sxs-lookup"><span data-stu-id="4ab1c-134">**14**</span></span>
</dt> <dd>

<span data-ttu-id="4ab1c-135">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="4ab1c-135">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="4ab1c-136">**15**</span><span class="sxs-lookup"><span data-stu-id="4ab1c-136">**15**</span></span>
</dt> <dd>

<span data-ttu-id="4ab1c-137">Infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="4ab1c-137">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="4ab1c-138">**16**</span><span class="sxs-lookup"><span data-stu-id="4ab1c-138">**16**</span></span>
</dt> <dd>

<span data-ttu-id="4ab1c-139">Archivo de inicio no válido.</span><span class="sxs-lookup"><span data-stu-id="4ab1c-139">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="4ab1c-140">**17**</span><span class="sxs-lookup"><span data-stu-id="4ab1c-140">**17**</span></span>
</dt> <dd>

<span data-ttu-id="4ab1c-141">Privilegios no mantenidos.</span><span class="sxs-lookup"><span data-stu-id="4ab1c-141">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="4ab1c-142">**21**</span><span class="sxs-lookup"><span data-stu-id="4ab1c-142">**21**</span></span>
</dt> <dd>

<span data-ttu-id="4ab1c-143">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="4ab1c-143">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4ab1c-144">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4ab1c-144">Remarks</span></span>

<span data-ttu-id="4ab1c-145">Wmi no implementa actualmente este método.</span><span class="sxs-lookup"><span data-stu-id="4ab1c-145">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="4ab1c-146">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="4ab1c-146">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="4ab1c-147">Esta documentación se deriva de las descripciones de clases CIM publicadas por dmtf.</span><span class="sxs-lookup"><span data-stu-id="4ab1c-147">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4ab1c-148">Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="4ab1c-148">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ab1c-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ab1c-149">Requirements</span></span>



| <span data-ttu-id="4ab1c-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ab1c-150">Requirement</span></span> | <span data-ttu-id="4ab1c-151">Valor</span><span class="sxs-lookup"><span data-stu-id="4ab1c-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4ab1c-152">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4ab1c-152">Minimum supported client</span></span><br/> | <span data-ttu-id="4ab1c-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4ab1c-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4ab1c-154">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4ab1c-154">Minimum supported server</span></span><br/> | <span data-ttu-id="4ab1c-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4ab1c-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4ab1c-156">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4ab1c-156">Namespace</span></span><br/>                | <span data-ttu-id="4ab1c-157">\\CIMV2 raíz</span><span class="sxs-lookup"><span data-stu-id="4ab1c-157">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4ab1c-158">MOF</span><span class="sxs-lookup"><span data-stu-id="4ab1c-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4ab1c-159"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="4ab1c-159"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4ab1c-160">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4ab1c-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ab1c-161"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ab1c-161"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ab1c-162">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4ab1c-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ab1c-163">CIM \_ DeviceFile</span><span class="sxs-lookup"><span data-stu-id="4ab1c-163">CIM\_DeviceFile</span></span>](copy-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="4ab1c-164">**CIM \_ DeviceFile**</span><span class="sxs-lookup"><span data-stu-id="4ab1c-164">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

