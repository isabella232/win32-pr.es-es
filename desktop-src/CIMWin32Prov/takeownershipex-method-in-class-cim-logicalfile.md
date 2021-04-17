---
description: Obtiene la propiedad del archivo lógico especificado en la ruta de acceso del objeto. Este método es una versión extendida del método TakeOwnerShip.
ms.assetid: c01ab071-86e4-484d-aaed-4783b6c3bebf
ms.tgt_platform: multiple
title: Método TakeOwnerShipEx de la clase CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.TakeOwnerShipEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2e7f08413440ec32037554476ced386c56827239
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659364"
---
# <a name="takeownershipex-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="8c784-104">Método TakeOwnerShipEx de la \_ clase LogicalFile de CIM</span><span class="sxs-lookup"><span data-stu-id="8c784-104">TakeOwnerShipEx method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="8c784-105">El método **TakeOwnerShipEx** obtiene la propiedad del archivo lógico especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="8c784-105">The **TakeOwnerShipEx** method obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="8c784-106">Este método es una versión extendida del método [**TakeOwnerShip**](takeownership-method-in-class-cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="8c784-106">This method is an extended version of the [**TakeOwnerShip**](takeownership-method-in-class-cim-logicalfile.md) method.</span></span> <span data-ttu-id="8c784-107">Si el archivo lógico es un directorio, este método actúa de forma recursiva y toma la propiedad de todos los archivos y subdirectorios que contiene el directorio.</span><span class="sxs-lookup"><span data-stu-id="8c784-107">If the logical file is a directory, then this method acts recursively, taking ownership of all files and sub-directories that the directory contains.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8c784-108">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="8c784-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8c784-109">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="8c784-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8c784-110">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="8c784-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="8c784-111">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="8c784-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="8c784-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8c784-112">Syntax</span></span>


```mof
uint32 TakeOwnerShipEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="8c784-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8c784-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c784-114">*StopFileName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8c784-114">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8c784-115">Cadena que representa el nombre del archivo (o directorio) donde se produjo un error en el método.</span><span class="sxs-lookup"><span data-stu-id="8c784-115">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="8c784-116">Este parámetro es **null** si el método se ejecuta correctamente.</span><span class="sxs-lookup"><span data-stu-id="8c784-116">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="8c784-117">*StartFileName* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="8c784-117">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8c784-118">Cadena que nombra el archivo secundario (o directorio) que se va a utilizar como punto de partida para el método.</span><span class="sxs-lookup"><span data-stu-id="8c784-118">String that names the child file (or directory) to use as a starting point for the method.</span></span> <span data-ttu-id="8c784-119">Normalmente, este parámetro es el parámetro *StopFileName* que especifica el archivo o directorio en el que se produjo un error de la llamada al método anterior.</span><span class="sxs-lookup"><span data-stu-id="8c784-119">Typically, this parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="8c784-120">Si este parámetro es **null**, la operación se realiza en el archivo (o directorio) especificado en la llamada [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="8c784-120">If this parameter is **null**, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="8c784-121">*Recursivo* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="8c784-121">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8c784-122">Si es **true**, el método también se aplica de forma recursiva a los archivos y directorios del directorio especificado por la instancia de [**\_ LogicalFile de CIM**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="8c784-122">If **TRUE**, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span> <span data-ttu-id="8c784-123">En el caso de las instancias de archivo, este parámetro se omite.</span><span class="sxs-lookup"><span data-stu-id="8c784-123">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c784-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8c784-124">Return value</span></span>

<span data-ttu-id="8c784-125">Devuelve un valor de 0 (cero) si se realiza correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="8c784-125">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="8c784-126">**Success**</span><span class="sxs-lookup"><span data-stu-id="8c784-126">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="8c784-127">0</span><span class="sxs-lookup"><span data-stu-id="8c784-127">0</span></span>

<span data-ttu-id="8c784-128">Correcto.</span><span class="sxs-lookup"><span data-stu-id="8c784-128">Success.</span></span>

</dd> <dt>

<span data-ttu-id="8c784-129">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="8c784-129">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="8c784-130">2</span><span class="sxs-lookup"><span data-stu-id="8c784-130">2</span></span>

<span data-ttu-id="8c784-131">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="8c784-131">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="8c784-132">**Error no especificado**</span><span class="sxs-lookup"><span data-stu-id="8c784-132">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="8c784-133">8</span><span class="sxs-lookup"><span data-stu-id="8c784-133">8</span></span>

<span data-ttu-id="8c784-134">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="8c784-134">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="8c784-135">**Objeto no válido**</span><span class="sxs-lookup"><span data-stu-id="8c784-135">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="8c784-136">9</span><span class="sxs-lookup"><span data-stu-id="8c784-136">9</span></span>

<span data-ttu-id="8c784-137">Objeto no válido.</span><span class="sxs-lookup"><span data-stu-id="8c784-137">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="8c784-138">**El objeto ya existe**</span><span class="sxs-lookup"><span data-stu-id="8c784-138">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="8c784-139">10</span><span class="sxs-lookup"><span data-stu-id="8c784-139">10</span></span>

<span data-ttu-id="8c784-140">El objeto ya existe.</span><span class="sxs-lookup"><span data-stu-id="8c784-140">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="8c784-141">**Sistema de archivos no NTFS**</span><span class="sxs-lookup"><span data-stu-id="8c784-141">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="8c784-142">11</span><span class="sxs-lookup"><span data-stu-id="8c784-142">11</span></span>

<span data-ttu-id="8c784-143">Sistema de archivos no NTFS.</span><span class="sxs-lookup"><span data-stu-id="8c784-143">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="8c784-144">**Plataforma no NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="8c784-144">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="8c784-145">12</span><span class="sxs-lookup"><span data-stu-id="8c784-145">12</span></span>

<span data-ttu-id="8c784-146">Plataforma no Windows.</span><span class="sxs-lookup"><span data-stu-id="8c784-146">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="8c784-147">**La unidad no es la misma**</span><span class="sxs-lookup"><span data-stu-id="8c784-147">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="8c784-148">13</span><span class="sxs-lookup"><span data-stu-id="8c784-148">13</span></span>

<span data-ttu-id="8c784-149">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="8c784-149">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="8c784-150">**El directorio no está vacío**</span><span class="sxs-lookup"><span data-stu-id="8c784-150">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="8c784-151">14</span><span class="sxs-lookup"><span data-stu-id="8c784-151">14</span></span>

<span data-ttu-id="8c784-152">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="8c784-152">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="8c784-153">**Infracción de uso compartido**</span><span class="sxs-lookup"><span data-stu-id="8c784-153">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="8c784-154">15</span><span class="sxs-lookup"><span data-stu-id="8c784-154">15</span></span>

<span data-ttu-id="8c784-155">Infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="8c784-155">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="8c784-156">**Archivo de inicio no válido**</span><span class="sxs-lookup"><span data-stu-id="8c784-156">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="8c784-157">16</span><span class="sxs-lookup"><span data-stu-id="8c784-157">16</span></span>

<span data-ttu-id="8c784-158">Archivo de inicio no válido.</span><span class="sxs-lookup"><span data-stu-id="8c784-158">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="8c784-159">**Privilegio no mantenido**</span><span class="sxs-lookup"><span data-stu-id="8c784-159">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="8c784-160">17</span><span class="sxs-lookup"><span data-stu-id="8c784-160">17</span></span>

<span data-ttu-id="8c784-161">Privilegio no mantenido.</span><span class="sxs-lookup"><span data-stu-id="8c784-161">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="8c784-162">**parámetro no válido**</span><span class="sxs-lookup"><span data-stu-id="8c784-162">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="8c784-163">21</span><span class="sxs-lookup"><span data-stu-id="8c784-163">21</span></span>

<span data-ttu-id="8c784-164">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="8c784-164">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8c784-165">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8c784-165">Remarks</span></span>

<span data-ttu-id="8c784-166">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="8c784-166">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="8c784-167">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="8c784-167">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="8c784-168">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="8c784-168">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8c784-169">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="8c784-169">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c784-170">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c784-170">Requirements</span></span>



| <span data-ttu-id="8c784-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c784-171">Requirement</span></span> | <span data-ttu-id="8c784-172">Value</span><span class="sxs-lookup"><span data-stu-id="8c784-172">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c784-173">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c784-173">Minimum supported client</span></span><br/> | <span data-ttu-id="8c784-174">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8c784-174">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8c784-175">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c784-175">Minimum supported server</span></span><br/> | <span data-ttu-id="8c784-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8c784-176">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8c784-177">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8c784-177">Namespace</span></span><br/>                | <span data-ttu-id="8c784-178">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="8c784-178">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8c784-179">MOF</span><span class="sxs-lookup"><span data-stu-id="8c784-179">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8c784-180"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8c784-180"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8c784-181">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8c784-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c784-182"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c784-182"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c784-183">Vea también</span><span class="sxs-lookup"><span data-stu-id="8c784-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c784-184">\_LOGICALFILE CIM</span><span class="sxs-lookup"><span data-stu-id="8c784-184">CIM\_LogicalFile</span></span>](takeownershipex-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="8c784-185">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="8c784-185">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

