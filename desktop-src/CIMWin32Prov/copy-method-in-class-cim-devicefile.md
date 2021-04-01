---
description: El método de copia copia el archivo lógico (o directorio) especificado en la ruta de acceso del objeto en la ubicación especificada por el parámetro de entrada.
ms.assetid: 6c1c6172-80a2-4779-903a-935f8c7091a5
ms.tgt_platform: multiple
title: Método de copia de la clase CIM_DeviceFile
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
ms.openlocfilehash: dc8bb7878f4967dbc58adf6163c92c0d2bd67713
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907280"
---
# <a name="copy-method-of-the-cim_devicefile-class"></a><span data-ttu-id="94659-103">Método de copia de la \_ clase DeviceFile de CIM</span><span class="sxs-lookup"><span data-stu-id="94659-103">Copy method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="94659-104">El método de **copia** copia el archivo lógico (o directorio) especificado en la ruta de acceso del objeto en la ubicación especificada por el parámetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="94659-104">The **Copy** method copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="94659-105">No se admite una copia si requiere sobrescribir un archivo lógico existente.</span><span class="sxs-lookup"><span data-stu-id="94659-105">A copy is not supported if it requires overwriting an existing logical file.</span></span> <span data-ttu-id="94659-106">Este método se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="94659-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="94659-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="94659-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="94659-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="94659-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="94659-109">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="94659-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="94659-110">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="94659-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="94659-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="94659-111">Syntax</span></span>


```mof
uint32 Copy(
  [in] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="94659-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="94659-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94659-113">*Nombre de archivo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="94659-113">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94659-114">Nombre completo de la copia del archivo de destino (o directorio).</span><span class="sxs-lookup"><span data-stu-id="94659-114">Fully qualified name of the destination file (or directory) copy.</span></span>

<span data-ttu-id="94659-115">Ejemplo: "c: \\ temp \\ newdirectory"</span><span class="sxs-lookup"><span data-stu-id="94659-115">Example: "c:\\temp\\newdirectory"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94659-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="94659-116">Return value</span></span>

<span data-ttu-id="94659-117">Devuelve un valor de 0 (cero) si se realiza correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="94659-117">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="94659-118">**0**</span><span class="sxs-lookup"><span data-stu-id="94659-118">**0**</span></span>
</dt> <dd>

<span data-ttu-id="94659-119">Correcto.</span><span class="sxs-lookup"><span data-stu-id="94659-119">Success.</span></span>

</dd> <dt>

<span data-ttu-id="94659-120">**2**</span><span class="sxs-lookup"><span data-stu-id="94659-120">**2**</span></span>
</dt> <dd>

<span data-ttu-id="94659-121">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="94659-121">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="94659-122">**8**</span><span class="sxs-lookup"><span data-stu-id="94659-122">**8**</span></span>
</dt> <dd>

<span data-ttu-id="94659-123">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="94659-123">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="94659-124">**9**</span><span class="sxs-lookup"><span data-stu-id="94659-124">**9**</span></span>
</dt> <dd>

<span data-ttu-id="94659-125">Objeto no válido.</span><span class="sxs-lookup"><span data-stu-id="94659-125">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="94659-126">**10**</span><span class="sxs-lookup"><span data-stu-id="94659-126">**10**</span></span>
</dt> <dd>

<span data-ttu-id="94659-127">El objeto ya existe.</span><span class="sxs-lookup"><span data-stu-id="94659-127">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="94659-128">**11**</span><span class="sxs-lookup"><span data-stu-id="94659-128">**11**</span></span>
</dt> <dd>

<span data-ttu-id="94659-129">Sistema de archivos no NTFS.</span><span class="sxs-lookup"><span data-stu-id="94659-129">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="94659-130">**12**</span><span class="sxs-lookup"><span data-stu-id="94659-130">**12**</span></span>
</dt> <dd>

<span data-ttu-id="94659-131">Plataforma no Windows.</span><span class="sxs-lookup"><span data-stu-id="94659-131">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="94659-132">**13**</span><span class="sxs-lookup"><span data-stu-id="94659-132">**13**</span></span>
</dt> <dd>

<span data-ttu-id="94659-133">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="94659-133">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="94659-134">**14**</span><span class="sxs-lookup"><span data-stu-id="94659-134">**14**</span></span>
</dt> <dd>

<span data-ttu-id="94659-135">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="94659-135">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="94659-136">**15**</span><span class="sxs-lookup"><span data-stu-id="94659-136">**15**</span></span>
</dt> <dd>

<span data-ttu-id="94659-137">Infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="94659-137">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="94659-138">**16**</span><span class="sxs-lookup"><span data-stu-id="94659-138">**16**</span></span>
</dt> <dd>

<span data-ttu-id="94659-139">Archivo de inicio no válido.</span><span class="sxs-lookup"><span data-stu-id="94659-139">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="94659-140">**17**</span><span class="sxs-lookup"><span data-stu-id="94659-140">**17**</span></span>
</dt> <dd>

<span data-ttu-id="94659-141">Privilegio no mantenido.</span><span class="sxs-lookup"><span data-stu-id="94659-141">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="94659-142">**21**</span><span class="sxs-lookup"><span data-stu-id="94659-142">**21**</span></span>
</dt> <dd>

<span data-ttu-id="94659-143">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="94659-143">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="94659-144">Observaciones</span><span class="sxs-lookup"><span data-stu-id="94659-144">Remarks</span></span>

<span data-ttu-id="94659-145">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="94659-145">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="94659-146">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="94659-146">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="94659-147">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="94659-147">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="94659-148">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="94659-148">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="94659-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94659-149">Requirements</span></span>



| <span data-ttu-id="94659-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="94659-150">Requirement</span></span> | <span data-ttu-id="94659-151">Value</span><span class="sxs-lookup"><span data-stu-id="94659-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="94659-152">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="94659-152">Minimum supported client</span></span><br/> | <span data-ttu-id="94659-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="94659-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="94659-154">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="94659-154">Minimum supported server</span></span><br/> | <span data-ttu-id="94659-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="94659-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="94659-156">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="94659-156">Namespace</span></span><br/>                | <span data-ttu-id="94659-157">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="94659-157">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="94659-158">MOF</span><span class="sxs-lookup"><span data-stu-id="94659-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="94659-159"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="94659-159"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="94659-160">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="94659-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94659-161"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94659-161"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94659-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="94659-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94659-163">\_DEVICEFILE CIM</span><span class="sxs-lookup"><span data-stu-id="94659-163">CIM\_DeviceFile</span></span>](copy-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="94659-164">**\_DEVICEFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="94659-164">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

