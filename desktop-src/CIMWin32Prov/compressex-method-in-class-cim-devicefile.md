---
description: El método CompressEx comprime el archivo lógico (o directorio) especificado en la ruta de acceso del objeto. Este método es una versión extendida del método compress. Este método se hereda de \_ LOGICALFILE CIM.
ms.assetid: a5f7b35b-5d52-4129-bf7e-6db5e0ff6852
ms.tgt_platform: multiple
title: Método CompressEx de la clase CIM_DeviceFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.CompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8e607497a8bb49d0a5926e5b50eb3310c671d9f4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907023"
---
# <a name="compressex-method-of-the-cim_devicefile-class"></a><span data-ttu-id="5aeb7-105">Método CompressEx de la \_ clase DeviceFile de CIM</span><span class="sxs-lookup"><span data-stu-id="5aeb7-105">CompressEx method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="5aeb7-106">El método **CompressEx** comprime el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="5aeb7-106">The **CompressEx** method compresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="5aeb7-107">Este método es una versión extendida del método [**compress**](compress-method-in-class-cim-devicefile.md) .</span><span class="sxs-lookup"><span data-stu-id="5aeb7-107">This method is an extended version of the [**Compress**](compress-method-in-class-cim-devicefile.md) method.</span></span> <span data-ttu-id="5aeb7-108">Este método se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5aeb7-108">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5aeb7-109">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="5aeb7-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="5aeb7-110">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="5aeb7-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="5aeb7-111">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="5aeb7-111">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="5aeb7-112">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="5aeb7-112">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="5aeb7-113">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5aeb7-113">Syntax</span></span>


```mof
uint32 CompressEx(
  [out] string REF StopFileName,
  [in]  string     StartFileName,
  [in]  boolean    Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="5aeb7-114">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5aeb7-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5aeb7-115">*StopFileName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="5aeb7-115">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5aeb7-116">Cadena que representa el nombre del archivo (o directorio) donde se produjo un error en el método.</span><span class="sxs-lookup"><span data-stu-id="5aeb7-116">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="5aeb7-117">Este parámetro es **null** si el método se ejecuta correctamente.</span><span class="sxs-lookup"><span data-stu-id="5aeb7-117">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="5aeb7-118">*StartFileName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5aeb7-118">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5aeb7-119">Cadena que representa el archivo secundario (o directorio) que se va a utilizar como punto de partida para este método.</span><span class="sxs-lookup"><span data-stu-id="5aeb7-119">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="5aeb7-120">Normalmente, el parámetro *StartFileName* es el parámetro *StopFileName* que especifica el archivo (o directorio) en el que se produjo un error de la llamada al método anterior.</span><span class="sxs-lookup"><span data-stu-id="5aeb7-120">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file (or directory) at which an error occurred from the previous method call.</span></span> <span data-ttu-id="5aeb7-121">Si este parámetro es **null**, la operación se realiza en el archivo (o directorio) especificado en la llamada [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="5aeb7-121">If this parameter is **null**, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="5aeb7-122">*Recursivo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5aeb7-122">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5aeb7-123">Si es **true**, el método también se aplica de forma recursiva a los archivos y directorios del directorio especificado por la instancia de [**\_ DeviceFile de CIM**](cim-devicefile.md) .</span><span class="sxs-lookup"><span data-stu-id="5aeb7-123">If **TRUE**, the method is also applied recursively to files and directories within the directory that is specified by the [**CIM\_DeviceFile**](cim-devicefile.md) instance.</span></span> <span data-ttu-id="5aeb7-124">En el caso de las instancias de archivo, este parámetro se omite.</span><span class="sxs-lookup"><span data-stu-id="5aeb7-124">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5aeb7-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5aeb7-125">Return value</span></span>

<span data-ttu-id="5aeb7-126">Devuelve un valor de 0 (cero) si se realiza correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="5aeb7-126">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="5aeb7-127">0</span><span class="sxs-lookup"><span data-stu-id="5aeb7-127">0</span></span>

<span data-ttu-id="5aeb7-128">Correcto.</span><span class="sxs-lookup"><span data-stu-id="5aeb7-128">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="5aeb7-129">2</span><span class="sxs-lookup"><span data-stu-id="5aeb7-129">2</span></span>

<span data-ttu-id="5aeb7-130">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="5aeb7-130">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="5aeb7-131">8</span><span class="sxs-lookup"><span data-stu-id="5aeb7-131">8</span></span>

<span data-ttu-id="5aeb7-132">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="5aeb7-132">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="5aeb7-133">9</span><span class="sxs-lookup"><span data-stu-id="5aeb7-133">9</span></span>

<span data-ttu-id="5aeb7-134">Objeto no válido.</span><span class="sxs-lookup"><span data-stu-id="5aeb7-134">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="5aeb7-135">10</span><span class="sxs-lookup"><span data-stu-id="5aeb7-135">10</span></span>

<span data-ttu-id="5aeb7-136">El objeto ya existe.</span><span class="sxs-lookup"><span data-stu-id="5aeb7-136">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="5aeb7-137">11</span><span class="sxs-lookup"><span data-stu-id="5aeb7-137">11</span></span>

<span data-ttu-id="5aeb7-138">Sistema de archivos no NTFS.</span><span class="sxs-lookup"><span data-stu-id="5aeb7-138">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="5aeb7-139">12</span><span class="sxs-lookup"><span data-stu-id="5aeb7-139">12</span></span>

<span data-ttu-id="5aeb7-140">Plataforma no Windows.</span><span class="sxs-lookup"><span data-stu-id="5aeb7-140">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="5aeb7-141">13</span><span class="sxs-lookup"><span data-stu-id="5aeb7-141">13</span></span>

<span data-ttu-id="5aeb7-142">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="5aeb7-142">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="5aeb7-143">14</span><span class="sxs-lookup"><span data-stu-id="5aeb7-143">14</span></span>

<span data-ttu-id="5aeb7-144">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="5aeb7-144">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="5aeb7-145">15</span><span class="sxs-lookup"><span data-stu-id="5aeb7-145">15</span></span>

<span data-ttu-id="5aeb7-146">Infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="5aeb7-146">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="5aeb7-147">16</span><span class="sxs-lookup"><span data-stu-id="5aeb7-147">16</span></span>

<span data-ttu-id="5aeb7-148">Archivo de inicio no válido.</span><span class="sxs-lookup"><span data-stu-id="5aeb7-148">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="5aeb7-149">17</span><span class="sxs-lookup"><span data-stu-id="5aeb7-149">17</span></span>

<span data-ttu-id="5aeb7-150">Privilegio no mantenido.</span><span class="sxs-lookup"><span data-stu-id="5aeb7-150">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="5aeb7-151">21</span><span class="sxs-lookup"><span data-stu-id="5aeb7-151">21</span></span>

<span data-ttu-id="5aeb7-152">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="5aeb7-152">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5aeb7-153">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5aeb7-153">Remarks</span></span>

<span data-ttu-id="5aeb7-154">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="5aeb7-154">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="5aeb7-155">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="5aeb7-155">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="5aeb7-156">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="5aeb7-156">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="5aeb7-157">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="5aeb7-157">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5aeb7-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5aeb7-158">Requirements</span></span>



| <span data-ttu-id="5aeb7-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="5aeb7-159">Requirement</span></span> | <span data-ttu-id="5aeb7-160">Value</span><span class="sxs-lookup"><span data-stu-id="5aeb7-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5aeb7-161">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5aeb7-161">Minimum supported client</span></span><br/> | <span data-ttu-id="5aeb7-162">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5aeb7-162">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5aeb7-163">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5aeb7-163">Minimum supported server</span></span><br/> | <span data-ttu-id="5aeb7-164">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5aeb7-164">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5aeb7-165">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5aeb7-165">Namespace</span></span><br/>                | <span data-ttu-id="5aeb7-166">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="5aeb7-166">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5aeb7-167">MOF</span><span class="sxs-lookup"><span data-stu-id="5aeb7-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5aeb7-168"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5aeb7-168"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5aeb7-169">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5aeb7-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5aeb7-170"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5aeb7-170"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5aeb7-171">Vea también</span><span class="sxs-lookup"><span data-stu-id="5aeb7-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5aeb7-172">\_DEVICEFILE CIM</span><span class="sxs-lookup"><span data-stu-id="5aeb7-172">CIM\_DeviceFile</span></span>](compressex-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="5aeb7-173">**\_DEVICEFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="5aeb7-173">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

