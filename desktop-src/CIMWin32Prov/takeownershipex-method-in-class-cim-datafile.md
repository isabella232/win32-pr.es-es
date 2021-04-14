---
description: Obtiene la propiedad del archivo de datos lógico que se especifica en la ruta de acceso del objeto. Este método es una versión extendida del método TakeOwnerShip y se hereda de \_ LOGICALFILE CIM.
ms.assetid: 3bc5a060-d805-46f6-802d-9ed16b52da59
ms.tgt_platform: multiple
title: Método TakeOwnerShipEx de la clase CIM_DataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.TakeOwnerShipEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 41124567e8743227f46c9cb3b84dcb0d1f788bc3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496541"
---
# <a name="takeownershipex-method-of-the-cim_datafile-class"></a><span data-ttu-id="40790-104">Método TakeOwnerShipEx de la \_ clase de archivo de archivos CIM</span><span class="sxs-lookup"><span data-stu-id="40790-104">TakeOwnerShipEx method of the CIM\_DataFile class</span></span>

<span data-ttu-id="40790-105">El método **TakeOwnerShipEx** obtiene la propiedad del archivo de datos lógico que se especifica en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="40790-105">The **TakeOwnerShipEx** method obtains ownership of the logical data file that is specified in the object path.</span></span> <span data-ttu-id="40790-106">Este método es una versión extendida del método [**TakeOwnerShip**](takeownership-method-in-class-cim-datafile.md) y se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="40790-106">This method is an extended version of the [**TakeOwnerShip**](takeownership-method-in-class-cim-datafile.md) method and is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span> <span data-ttu-id="40790-107">Si el archivo lógico es un directorio, este método actuará de forma recursiva y tomará la propiedad de todos los archivos y subdirectorios que contenga el directorio.</span><span class="sxs-lookup"><span data-stu-id="40790-107">If the logical file is a directory, then this method will act recursively, taking ownership of all files and subdirectories that the directory contains.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="40790-108">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="40790-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="40790-109">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="40790-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="40790-110">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="40790-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="40790-111">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="40790-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="40790-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="40790-112">Syntax</span></span>


```mof
uint32 TakeOwnerShipEx(
  [out] string  StopFileName,
  [in]  string  StartFileName,
  [in]  boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="40790-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="40790-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40790-114">*StopFileName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="40790-114">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="40790-115">Nombre del archivo (o directorio) en el que se produjo un error en el método.</span><span class="sxs-lookup"><span data-stu-id="40790-115">Name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="40790-116">Este parámetro será NULL si el método se ejecuta correctamente.</span><span class="sxs-lookup"><span data-stu-id="40790-116">This parameter will be null if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="40790-117">*StartFileName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="40790-117">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40790-118">Archivo secundario (o directorio) que se va a usar como punto de partida para este método.</span><span class="sxs-lookup"><span data-stu-id="40790-118">Child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="40790-119">Normalmente, el parámetro *StartFileName* es el parámetro *StopFileName* que especifica el archivo (o directorio) en el que se produjo un error de la llamada al método anterior.</span><span class="sxs-lookup"><span data-stu-id="40790-119">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file (or directory) at which an error occurred from the previous method call.</span></span> <span data-ttu-id="40790-120">Si este parámetro es null, la operación se realiza en el archivo (o directorio) especificado en la llamada [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="40790-120">If this parameter is null, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

<span data-ttu-id="40790-121">Si se utiliza *StartFileName* , *Recursive* también debe establecerse en true.</span><span class="sxs-lookup"><span data-stu-id="40790-121">If *StartFileName* is used, *Recursive* must be set to true as well.</span></span>

</dd> <dt>

<span data-ttu-id="40790-122">*Recursivo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="40790-122">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40790-123">Si es **true**, el método también se aplica de forma recursiva a los archivos y directorios del directorio especificado por la instancia de [**archivo de \_ archivos CIM**](cim-datafile.md) .</span><span class="sxs-lookup"><span data-stu-id="40790-123">If **TRUE**, the method is also applied recursively to files and directories within the directory that is specified by the [**CIM\_DataFile**](cim-datafile.md) instance.</span></span> <span data-ttu-id="40790-124">En el caso de las instancias de archivo, este parámetro se omite.</span><span class="sxs-lookup"><span data-stu-id="40790-124">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40790-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="40790-125">Return value</span></span>

<span data-ttu-id="40790-126">Devuelve un valor de 0 (cero) si se realiza correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="40790-126">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="40790-127">Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="40790-127">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="40790-128">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="40790-128">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="40790-129">**0**</span><span class="sxs-lookup"><span data-stu-id="40790-129">**0**</span></span>
</dt> <dd>

<span data-ttu-id="40790-130">Correcto.</span><span class="sxs-lookup"><span data-stu-id="40790-130">Success.</span></span>

</dd> <dt>

<span data-ttu-id="40790-131">**2**</span><span class="sxs-lookup"><span data-stu-id="40790-131">**2**</span></span>
</dt> <dd>

<span data-ttu-id="40790-132">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="40790-132">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="40790-133">**8**</span><span class="sxs-lookup"><span data-stu-id="40790-133">**8**</span></span>
</dt> <dd>

<span data-ttu-id="40790-134">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="40790-134">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="40790-135">**9**</span><span class="sxs-lookup"><span data-stu-id="40790-135">**9**</span></span>
</dt> <dd>

<span data-ttu-id="40790-136">Objeto no válido.</span><span class="sxs-lookup"><span data-stu-id="40790-136">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="40790-137">**10**</span><span class="sxs-lookup"><span data-stu-id="40790-137">**10**</span></span>
</dt> <dd>

<span data-ttu-id="40790-138">El objeto ya existe.</span><span class="sxs-lookup"><span data-stu-id="40790-138">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="40790-139">**11**</span><span class="sxs-lookup"><span data-stu-id="40790-139">**11**</span></span>
</dt> <dd>

<span data-ttu-id="40790-140">Sistema de archivos no NTFS.</span><span class="sxs-lookup"><span data-stu-id="40790-140">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="40790-141">**12**</span><span class="sxs-lookup"><span data-stu-id="40790-141">**12**</span></span>
</dt> <dd>

<span data-ttu-id="40790-142">Plataforma no Windows.</span><span class="sxs-lookup"><span data-stu-id="40790-142">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="40790-143">**13**</span><span class="sxs-lookup"><span data-stu-id="40790-143">**13**</span></span>
</dt> <dd>

<span data-ttu-id="40790-144">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="40790-144">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="40790-145">**14**</span><span class="sxs-lookup"><span data-stu-id="40790-145">**14**</span></span>
</dt> <dd>

<span data-ttu-id="40790-146">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="40790-146">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="40790-147">**15**</span><span class="sxs-lookup"><span data-stu-id="40790-147">**15**</span></span>
</dt> <dd>

<span data-ttu-id="40790-148">Infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="40790-148">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="40790-149">**16**</span><span class="sxs-lookup"><span data-stu-id="40790-149">**16**</span></span>
</dt> <dd>

<span data-ttu-id="40790-150">Archivo de inicio no válido.</span><span class="sxs-lookup"><span data-stu-id="40790-150">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="40790-151">**17**</span><span class="sxs-lookup"><span data-stu-id="40790-151">**17**</span></span>
</dt> <dd>

<span data-ttu-id="40790-152">Privilegio no mantenido.</span><span class="sxs-lookup"><span data-stu-id="40790-152">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="40790-153">**21**</span><span class="sxs-lookup"><span data-stu-id="40790-153">**21**</span></span>
</dt> <dd>

<span data-ttu-id="40790-154">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="40790-154">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="40790-155">Observaciones</span><span class="sxs-lookup"><span data-stu-id="40790-155">Remarks</span></span>

<span data-ttu-id="40790-156">WMI implementa el método **TakeOwnerShipEx** en el [**archivo de \_ archivos de CIM**](cim-datafile.md) .</span><span class="sxs-lookup"><span data-stu-id="40790-156">The **TakeOwnerShipEx** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="40790-157">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="40790-157">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="40790-158">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="40790-158">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="40790-159">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40790-159">Requirements</span></span>



| <span data-ttu-id="40790-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="40790-160">Requirement</span></span> | <span data-ttu-id="40790-161">Value</span><span class="sxs-lookup"><span data-stu-id="40790-161">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="40790-162">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="40790-162">Minimum supported client</span></span><br/> | <span data-ttu-id="40790-163">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="40790-163">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="40790-164">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="40790-164">Minimum supported server</span></span><br/> | <span data-ttu-id="40790-165">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="40790-165">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="40790-166">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="40790-166">Namespace</span></span><br/>                | <span data-ttu-id="40790-167">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="40790-167">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="40790-168">MOF</span><span class="sxs-lookup"><span data-stu-id="40790-168">MOF</span></span><br/>                      | <dl> <span data-ttu-id="40790-169"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="40790-169"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="40790-170">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="40790-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40790-171"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40790-171"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40790-172">Vea también</span><span class="sxs-lookup"><span data-stu-id="40790-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40790-173">\_Archivo de archivos CIM</span><span class="sxs-lookup"><span data-stu-id="40790-173">CIM\_DataFile</span></span>](takeownershipex-method-in-class-cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="40790-174">**\_Archivo de archivos CIM**</span><span class="sxs-lookup"><span data-stu-id="40790-174">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="40790-175">Tareas de WMI: archivos y carpetas</span><span class="sxs-lookup"><span data-stu-id="40790-175">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="40790-176">**Constantes de derechos de acceso a archivos y directorios**</span><span class="sxs-lookup"><span data-stu-id="40790-176">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

