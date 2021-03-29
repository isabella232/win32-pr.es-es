---
description: Obtiene la propiedad del archivo de dispositivo lógico especificado en la ruta de acceso del objeto. Este método es una versión extendida del método TakeOwnerShip y se hereda de \_ LOGICALFILE CIM.
ms.assetid: 084f755a-e837-4d21-8bd2-0f63f80302fc
ms.tgt_platform: multiple
title: Método TakeOwnerShipEx de la clase CIM_DeviceFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.TakeOwnerShipEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3c36239d7d0ea6b0bf3bfa67bfb2f59617ab209a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103906981"
---
# <a name="takeownershipex-method-of-the-cim_devicefile-class"></a><span data-ttu-id="4df4d-104">Método TakeOwnerShipEx de la \_ clase DeviceFile de CIM</span><span class="sxs-lookup"><span data-stu-id="4df4d-104">TakeOwnerShipEx method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="4df4d-105">El método **TakeOwnerShipEx** obtiene la propiedad del archivo de dispositivo lógico especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="4df4d-105">The **TakeOwnerShipEx** method obtains ownership of the logical device file specified in the object path.</span></span> <span data-ttu-id="4df4d-106">Este método es una versión extendida del método [**TakeOwnerShip**](takeownership-method-in-class-cim-devicefile.md) y se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="4df4d-106">This method is an extended version of the [**TakeOwnerShip**](takeownership-method-in-class-cim-devicefile.md) method and is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span> <span data-ttu-id="4df4d-107">Si el archivo lógico es un directorio, este método actúa de forma recursiva y toma la propiedad de todos los archivos y subdirectorios que contiene el directorio.</span><span class="sxs-lookup"><span data-stu-id="4df4d-107">If the logical file is a directory, then this method acts recursively, taking ownership of all of the files and sub-directories that the directory contains.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4df4d-108">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="4df4d-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4df4d-109">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4df4d-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4df4d-110">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="4df4d-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="4df4d-111">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="4df4d-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="4df4d-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4df4d-112">Syntax</span></span>


```mof
uint32 TakeOwnerShipEx(
  [out] string REF StopFileName,
  [in]  string     StartFileName,
  [in]  boolean    Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="4df4d-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4df4d-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4df4d-114">*StopFileName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4df4d-114">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4df4d-115">Cadena que representa el nombre del archivo (o directorio) donde se produjo un error en el método.</span><span class="sxs-lookup"><span data-stu-id="4df4d-115">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="4df4d-116">Este parámetro es **null** si el método se ejecuta correctamente.</span><span class="sxs-lookup"><span data-stu-id="4df4d-116">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="4df4d-117">*StartFileName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4df4d-117">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4df4d-118">Cadena que representa el archivo secundario (o directorio) que se va a utilizar como punto de partida para este método.</span><span class="sxs-lookup"><span data-stu-id="4df4d-118">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="4df4d-119">Normalmente, el parámetro *StartFileName* es el parámetro *StopFileName* que especifica el archivo o directorio en el que se produjo un error de la llamada al método anterior.</span><span class="sxs-lookup"><span data-stu-id="4df4d-119">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="4df4d-120">Si este parámetro es **null**, la operación se realiza en el archivo o directorio especificado en la llamada **ExecMethod** .</span><span class="sxs-lookup"><span data-stu-id="4df4d-120">If this parameter is **null**, the operation is performed on the file or directory specified in the **ExecMethod** call.</span></span>

</dd> <dt>

<span data-ttu-id="4df4d-121">*Recursivo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4df4d-121">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4df4d-122">Si es **true**, el método también se aplica de forma recursiva a los archivos y directorios del directorio especificado por la instancia de [**\_ DeviceFile de CIM**](cim-devicefile.md) .</span><span class="sxs-lookup"><span data-stu-id="4df4d-122">If **TRUE**, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_DeviceFile**](cim-devicefile.md) instance.</span></span> <span data-ttu-id="4df4d-123">En el caso de las instancias de archivo, este parámetro se omite.</span><span class="sxs-lookup"><span data-stu-id="4df4d-123">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4df4d-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4df4d-124">Return value</span></span>

<span data-ttu-id="4df4d-125">Devuelve un valor de 0 (cero) si se realiza correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="4df4d-125">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="4df4d-126">0</span><span class="sxs-lookup"><span data-stu-id="4df4d-126">0</span></span>

<span data-ttu-id="4df4d-127">Correcto.</span><span class="sxs-lookup"><span data-stu-id="4df4d-127">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="4df4d-128">2</span><span class="sxs-lookup"><span data-stu-id="4df4d-128">2</span></span>

<span data-ttu-id="4df4d-129">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="4df4d-129">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="4df4d-130">8</span><span class="sxs-lookup"><span data-stu-id="4df4d-130">8</span></span>

<span data-ttu-id="4df4d-131">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="4df4d-131">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="4df4d-132">9</span><span class="sxs-lookup"><span data-stu-id="4df4d-132">9</span></span>

<span data-ttu-id="4df4d-133">Objeto no válido.</span><span class="sxs-lookup"><span data-stu-id="4df4d-133">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="4df4d-134">10</span><span class="sxs-lookup"><span data-stu-id="4df4d-134">10</span></span>

<span data-ttu-id="4df4d-135">El objeto ya existe.</span><span class="sxs-lookup"><span data-stu-id="4df4d-135">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="4df4d-136">11</span><span class="sxs-lookup"><span data-stu-id="4df4d-136">11</span></span>

<span data-ttu-id="4df4d-137">Sistema de archivos no NTFS.</span><span class="sxs-lookup"><span data-stu-id="4df4d-137">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="4df4d-138">12</span><span class="sxs-lookup"><span data-stu-id="4df4d-138">12</span></span>

<span data-ttu-id="4df4d-139">Plataforma no Windows.</span><span class="sxs-lookup"><span data-stu-id="4df4d-139">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="4df4d-140">13</span><span class="sxs-lookup"><span data-stu-id="4df4d-140">13</span></span>

<span data-ttu-id="4df4d-141">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="4df4d-141">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="4df4d-142">14</span><span class="sxs-lookup"><span data-stu-id="4df4d-142">14</span></span>

<span data-ttu-id="4df4d-143">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="4df4d-143">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="4df4d-144">15</span><span class="sxs-lookup"><span data-stu-id="4df4d-144">15</span></span>

<span data-ttu-id="4df4d-145">Infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="4df4d-145">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="4df4d-146">16</span><span class="sxs-lookup"><span data-stu-id="4df4d-146">16</span></span>

<span data-ttu-id="4df4d-147">Archivo de inicio no válido.</span><span class="sxs-lookup"><span data-stu-id="4df4d-147">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="4df4d-148">17</span><span class="sxs-lookup"><span data-stu-id="4df4d-148">17</span></span>

<span data-ttu-id="4df4d-149">Privilegio no mantenido.</span><span class="sxs-lookup"><span data-stu-id="4df4d-149">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="4df4d-150">21</span><span class="sxs-lookup"><span data-stu-id="4df4d-150">21</span></span>

<span data-ttu-id="4df4d-151">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="4df4d-151">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4df4d-152">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4df4d-152">Remarks</span></span>

<span data-ttu-id="4df4d-153">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="4df4d-153">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="4df4d-154">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="4df4d-154">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="4df4d-155">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="4df4d-155">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4df4d-156">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="4df4d-156">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4df4d-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4df4d-157">Requirements</span></span>



| <span data-ttu-id="4df4d-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="4df4d-158">Requirement</span></span> | <span data-ttu-id="4df4d-159">Value</span><span class="sxs-lookup"><span data-stu-id="4df4d-159">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4df4d-160">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4df4d-160">Minimum supported client</span></span><br/> | <span data-ttu-id="4df4d-161">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4df4d-161">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4df4d-162">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4df4d-162">Minimum supported server</span></span><br/> | <span data-ttu-id="4df4d-163">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4df4d-163">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4df4d-164">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4df4d-164">Namespace</span></span><br/>                | <span data-ttu-id="4df4d-165">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="4df4d-165">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4df4d-166">MOF</span><span class="sxs-lookup"><span data-stu-id="4df4d-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4df4d-167"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4df4d-167"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4df4d-168">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4df4d-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4df4d-169"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4df4d-169"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4df4d-170">Vea también</span><span class="sxs-lookup"><span data-stu-id="4df4d-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4df4d-171">\_DEVICEFILE CIM</span><span class="sxs-lookup"><span data-stu-id="4df4d-171">CIM\_DeviceFile</span></span>](takeownershipex-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="4df4d-172">**\_DEVICEFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="4df4d-172">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

