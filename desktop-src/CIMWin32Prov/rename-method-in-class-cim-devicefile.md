---
description: Cambia el nombre del archivo de dispositivo (o directorio) especificado en la ruta de acceso del objeto.
ms.assetid: 48c2eab3-c76d-4e4b-927e-dbb17584cccd
ms.tgt_platform: multiple
title: Cambiar el nombre del método de la clase CIM_DeviceFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 484d66a1b98ea58b7cb5de25c8f7d15065ce905b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153372"
---
# <a name="rename-method-of-the-cim_devicefile-class"></a><span data-ttu-id="0cc06-103">Cambiar el nombre del método de la \_ clase CIM DeviceFile</span><span class="sxs-lookup"><span data-stu-id="0cc06-103">Rename method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="0cc06-104">El método **Rename** cambia el nombre del archivo de dispositivo (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="0cc06-104">The **Rename** method renames the device file (or directory) specified in the object path.</span></span> <span data-ttu-id="0cc06-105">No se admite el cambio de nombre si el destino está en otra unidad o si se requiere sobrescribir un archivo lógico existente.</span><span class="sxs-lookup"><span data-stu-id="0cc06-105">Renaming is not supported if the destination is on another drive or overwriting an existing logical file is required.</span></span> <span data-ttu-id="0cc06-106">Este método se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="0cc06-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0cc06-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="0cc06-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0cc06-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="0cc06-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0cc06-109">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="0cc06-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="0cc06-110">Para obtener más información sobre el uso de este método, vea [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="0cc06-110">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="0cc06-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0cc06-111">Syntax</span></span>


```mof
uint32 Rename(
  [in] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="0cc06-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0cc06-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0cc06-113">*Nombre de archivo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0cc06-113">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cc06-114">Nuevo nombre completo del archivo (o directorio).</span><span class="sxs-lookup"><span data-stu-id="0cc06-114">Fully qualified new name of the file (or directory).</span></span>

<span data-ttu-id="0cc06-115">Ejemplo: "c: \\ temp \\newfile.txt"</span><span class="sxs-lookup"><span data-stu-id="0cc06-115">Example: "c:\\temp\\newfile.txt"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0cc06-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0cc06-116">Return value</span></span>

<span data-ttu-id="0cc06-117">Devuelve un valor de 0 (cero) si se realiza correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="0cc06-117">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="0cc06-118">**0**</span><span class="sxs-lookup"><span data-stu-id="0cc06-118">**0**</span></span>
</dt> <dd>

<span data-ttu-id="0cc06-119">Correcto.</span><span class="sxs-lookup"><span data-stu-id="0cc06-119">Success.</span></span>

</dd> <dt>

<span data-ttu-id="0cc06-120">**2**</span><span class="sxs-lookup"><span data-stu-id="0cc06-120">**2**</span></span>
</dt> <dd>

<span data-ttu-id="0cc06-121">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="0cc06-121">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="0cc06-122">**8**</span><span class="sxs-lookup"><span data-stu-id="0cc06-122">**8**</span></span>
</dt> <dd>

<span data-ttu-id="0cc06-123">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="0cc06-123">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="0cc06-124">**9**</span><span class="sxs-lookup"><span data-stu-id="0cc06-124">**9**</span></span>
</dt> <dd>

<span data-ttu-id="0cc06-125">Objeto no válido.</span><span class="sxs-lookup"><span data-stu-id="0cc06-125">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="0cc06-126">**10**</span><span class="sxs-lookup"><span data-stu-id="0cc06-126">**10**</span></span>
</dt> <dd>

<span data-ttu-id="0cc06-127">El objeto ya existe.</span><span class="sxs-lookup"><span data-stu-id="0cc06-127">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="0cc06-128">**11**</span><span class="sxs-lookup"><span data-stu-id="0cc06-128">**11**</span></span>
</dt> <dd>

<span data-ttu-id="0cc06-129">Sistema de archivos no NTFS.</span><span class="sxs-lookup"><span data-stu-id="0cc06-129">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="0cc06-130">**12**</span><span class="sxs-lookup"><span data-stu-id="0cc06-130">**12**</span></span>
</dt> <dd>

<span data-ttu-id="0cc06-131">Plataforma no Windows.</span><span class="sxs-lookup"><span data-stu-id="0cc06-131">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="0cc06-132">**13**</span><span class="sxs-lookup"><span data-stu-id="0cc06-132">**13**</span></span>
</dt> <dd>

<span data-ttu-id="0cc06-133">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="0cc06-133">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="0cc06-134">**14**</span><span class="sxs-lookup"><span data-stu-id="0cc06-134">**14**</span></span>
</dt> <dd>

<span data-ttu-id="0cc06-135">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="0cc06-135">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="0cc06-136">**15**</span><span class="sxs-lookup"><span data-stu-id="0cc06-136">**15**</span></span>
</dt> <dd>

<span data-ttu-id="0cc06-137">Infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="0cc06-137">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="0cc06-138">**16**</span><span class="sxs-lookup"><span data-stu-id="0cc06-138">**16**</span></span>
</dt> <dd>

<span data-ttu-id="0cc06-139">Archivo de inicio no válido.</span><span class="sxs-lookup"><span data-stu-id="0cc06-139">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="0cc06-140">**17**</span><span class="sxs-lookup"><span data-stu-id="0cc06-140">**17**</span></span>
</dt> <dd>

<span data-ttu-id="0cc06-141">Privilegio no mantenido.</span><span class="sxs-lookup"><span data-stu-id="0cc06-141">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="0cc06-142">**21**</span><span class="sxs-lookup"><span data-stu-id="0cc06-142">**21**</span></span>
</dt> <dd>

<span data-ttu-id="0cc06-143">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="0cc06-143">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0cc06-144">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0cc06-144">Remarks</span></span>

<span data-ttu-id="0cc06-145">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="0cc06-145">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="0cc06-146">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="0cc06-146">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="0cc06-147">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="0cc06-147">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0cc06-148">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="0cc06-148">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0cc06-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0cc06-149">Requirements</span></span>



| <span data-ttu-id="0cc06-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="0cc06-150">Requirement</span></span> | <span data-ttu-id="0cc06-151">Value</span><span class="sxs-lookup"><span data-stu-id="0cc06-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0cc06-152">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0cc06-152">Minimum supported client</span></span><br/> | <span data-ttu-id="0cc06-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0cc06-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0cc06-154">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0cc06-154">Minimum supported server</span></span><br/> | <span data-ttu-id="0cc06-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0cc06-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0cc06-156">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0cc06-156">Namespace</span></span><br/>                | <span data-ttu-id="0cc06-157">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="0cc06-157">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0cc06-158">MOF</span><span class="sxs-lookup"><span data-stu-id="0cc06-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0cc06-159"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0cc06-159"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0cc06-160">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0cc06-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0cc06-161"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0cc06-161"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0cc06-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="0cc06-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cc06-163">\_DEVICEFILE CIM</span><span class="sxs-lookup"><span data-stu-id="0cc06-163">CIM\_DeviceFile</span></span>](rename-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="0cc06-164">**\_DEVICEFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="0cc06-164">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

