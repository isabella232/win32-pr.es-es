---
description: Descomprime el archivo de datos lógico (o directorio) especificado en la ruta de acceso del objeto. Este método es una versión extendida del método UNCOMPRESS y se hereda de CIM \_ LogicalFile.
ms.assetid: 30b62930-1d4a-47c0-8b57-b460edb5dbd0
ms.tgt_platform: multiple
title: Método UncompressEx de la clase CIM_DataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.UncompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0d11585a834ecc357447394ce09b73698bf2de86
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153442"
---
# <a name="uncompressex-method-of-the-cim_datafile-class"></a><span data-ttu-id="2e2f9-104">Método UncompressEx de la \_ clase de archivo de archivos CIM</span><span class="sxs-lookup"><span data-stu-id="2e2f9-104">UncompressEx method of the CIM\_DataFile class</span></span>

<span data-ttu-id="2e2f9-105">El método **UncompressEx** descomprime el archivo de datos lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="2e2f9-105">The **UncompressEx** method uncompresses the logical data file (or directory) that is specified in the object path.</span></span> <span data-ttu-id="2e2f9-106">Este método es una versión extendida del método [**UNCOMPRESS**](uncompress-method-in-class-cim-datafile.md) y se hereda de [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="2e2f9-106">This method is an extended version of the [**Uncompress**](uncompress-method-in-class-cim-datafile.md) method and is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2e2f9-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="2e2f9-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2e2f9-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="2e2f9-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2e2f9-109">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="2e2f9-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="2e2f9-110">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="2e2f9-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="2e2f9-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2e2f9-111">Syntax</span></span>


```mof
uint32 UncompressEx(
  [out] string  StopFileName,
  [in]  string  StartFileName,
  [in]  boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="2e2f9-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2e2f9-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e2f9-113">*StopFileName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="2e2f9-113">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2e2f9-114">Nombre del archivo (o directorio) en el que se produjo un error en el método.</span><span class="sxs-lookup"><span data-stu-id="2e2f9-114">Name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="2e2f9-115">Este parámetro es **null** si el método se ejecuta correctamente.</span><span class="sxs-lookup"><span data-stu-id="2e2f9-115">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="2e2f9-116">*StartFileName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2e2f9-116">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e2f9-117">Archivo secundario (o directorio) que se va a usar como punto de partida para este método.</span><span class="sxs-lookup"><span data-stu-id="2e2f9-117">Child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="2e2f9-118">Normalmente, el parámetro *StartFileName* es el parámetro *StopFileName* que especifica el archivo (o directorio) en el que se produjo un error de la llamada al método anterior.</span><span class="sxs-lookup"><span data-stu-id="2e2f9-118">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file (or directory) at which an error occurred from the previous method call.</span></span> <span data-ttu-id="2e2f9-119">Si este parámetro es **null**, la operación se realiza en el archivo (o directorio) especificado en la llamada [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="2e2f9-119">If this parameter is **null**, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

<span data-ttu-id="2e2f9-120">Si se utiliza *StartFileName* , *Recursive* también debe establecerse en true.</span><span class="sxs-lookup"><span data-stu-id="2e2f9-120">If *StartFileName* is used, *Recursive* must be set to true as well.</span></span>

</dd> <dt>

<span data-ttu-id="2e2f9-121">*Recursivo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2e2f9-121">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e2f9-122">Si es **true**, el método también se aplica de forma recursiva a los archivos y directorios del directorio especificado por la instancia de [**archivo de \_ archivos CIM**](cim-datafile.md) .</span><span class="sxs-lookup"><span data-stu-id="2e2f9-122">If **TRUE**, the method is also applied recursively to files and directories within the directory that is specified by the [**CIM\_DataFile**](cim-datafile.md) instance.</span></span> <span data-ttu-id="2e2f9-123">En el caso de las instancias de archivo, este parámetro se omite.</span><span class="sxs-lookup"><span data-stu-id="2e2f9-123">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e2f9-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2e2f9-124">Return value</span></span>

<span data-ttu-id="2e2f9-125">Devuelve un valor de 0 (cero) si se realiza correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="2e2f9-125">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="2e2f9-126">Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="2e2f9-126">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="2e2f9-127">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="2e2f9-127">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="2e2f9-128">**0**</span><span class="sxs-lookup"><span data-stu-id="2e2f9-128">**0**</span></span>
</dt> <dd>

<span data-ttu-id="2e2f9-129">Correcto.</span><span class="sxs-lookup"><span data-stu-id="2e2f9-129">Success.</span></span>

</dd> <dt>

<span data-ttu-id="2e2f9-130">**2**</span><span class="sxs-lookup"><span data-stu-id="2e2f9-130">**2**</span></span>
</dt> <dd>

<span data-ttu-id="2e2f9-131">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="2e2f9-131">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="2e2f9-132">**8**</span><span class="sxs-lookup"><span data-stu-id="2e2f9-132">**8**</span></span>
</dt> <dd>

<span data-ttu-id="2e2f9-133">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="2e2f9-133">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="2e2f9-134">**9**</span><span class="sxs-lookup"><span data-stu-id="2e2f9-134">**9**</span></span>
</dt> <dd>

<span data-ttu-id="2e2f9-135">Objeto no válido.</span><span class="sxs-lookup"><span data-stu-id="2e2f9-135">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="2e2f9-136">**10**</span><span class="sxs-lookup"><span data-stu-id="2e2f9-136">**10**</span></span>
</dt> <dd>

<span data-ttu-id="2e2f9-137">El objeto ya existe.</span><span class="sxs-lookup"><span data-stu-id="2e2f9-137">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="2e2f9-138">**11**</span><span class="sxs-lookup"><span data-stu-id="2e2f9-138">**11**</span></span>
</dt> <dd>

<span data-ttu-id="2e2f9-139">Sistema de archivos no NTFS.</span><span class="sxs-lookup"><span data-stu-id="2e2f9-139">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="2e2f9-140">**12**</span><span class="sxs-lookup"><span data-stu-id="2e2f9-140">**12**</span></span>
</dt> <dd>

<span data-ttu-id="2e2f9-141">Plataforma no Windows.</span><span class="sxs-lookup"><span data-stu-id="2e2f9-141">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="2e2f9-142">**13**</span><span class="sxs-lookup"><span data-stu-id="2e2f9-142">**13**</span></span>
</dt> <dd>

<span data-ttu-id="2e2f9-143">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="2e2f9-143">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="2e2f9-144">**14**</span><span class="sxs-lookup"><span data-stu-id="2e2f9-144">**14**</span></span>
</dt> <dd>

<span data-ttu-id="2e2f9-145">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="2e2f9-145">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="2e2f9-146">**15**</span><span class="sxs-lookup"><span data-stu-id="2e2f9-146">**15**</span></span>
</dt> <dd>

<span data-ttu-id="2e2f9-147">Infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="2e2f9-147">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="2e2f9-148">**16**</span><span class="sxs-lookup"><span data-stu-id="2e2f9-148">**16**</span></span>
</dt> <dd>

<span data-ttu-id="2e2f9-149">Archivo de inicio no válido.</span><span class="sxs-lookup"><span data-stu-id="2e2f9-149">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="2e2f9-150">**17**</span><span class="sxs-lookup"><span data-stu-id="2e2f9-150">**17**</span></span>
</dt> <dd>

<span data-ttu-id="2e2f9-151">Privilegio no mantenido.</span><span class="sxs-lookup"><span data-stu-id="2e2f9-151">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="2e2f9-152">**21**</span><span class="sxs-lookup"><span data-stu-id="2e2f9-152">**21**</span></span>
</dt> <dd>

<span data-ttu-id="2e2f9-153">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="2e2f9-153">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2e2f9-154">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2e2f9-154">Remarks</span></span>

<span data-ttu-id="2e2f9-155">WMI implementa el método **UncompressEx** en el [**archivo de \_ archivos de CIM**](cim-datafile.md) .</span><span class="sxs-lookup"><span data-stu-id="2e2f9-155">The **UncompressEx** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="2e2f9-156">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="2e2f9-156">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2e2f9-157">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="2e2f9-157">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e2f9-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e2f9-158">Requirements</span></span>



| <span data-ttu-id="2e2f9-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e2f9-159">Requirement</span></span> | <span data-ttu-id="2e2f9-160">Value</span><span class="sxs-lookup"><span data-stu-id="2e2f9-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e2f9-161">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e2f9-161">Minimum supported client</span></span><br/> | <span data-ttu-id="2e2f9-162">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2e2f9-162">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2e2f9-163">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e2f9-163">Minimum supported server</span></span><br/> | <span data-ttu-id="2e2f9-164">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2e2f9-164">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2e2f9-165">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2e2f9-165">Namespace</span></span><br/>                | <span data-ttu-id="2e2f9-166">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="2e2f9-166">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2e2f9-167">MOF</span><span class="sxs-lookup"><span data-stu-id="2e2f9-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2e2f9-168"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2e2f9-168"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2e2f9-169">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2e2f9-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e2f9-170"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e2f9-170"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e2f9-171">Vea también</span><span class="sxs-lookup"><span data-stu-id="2e2f9-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e2f9-172">**\_Archivo de archivos CIM**</span><span class="sxs-lookup"><span data-stu-id="2e2f9-172">**CIM\_DataFile**</span></span>](uncompressex-method-in-class-cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="2e2f9-173">**\_Archivo de archivos CIM**</span><span class="sxs-lookup"><span data-stu-id="2e2f9-173">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="2e2f9-174">Tareas de WMI: archivos y carpetas</span><span class="sxs-lookup"><span data-stu-id="2e2f9-174">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="2e2f9-175">**Constantes de derechos de acceso a archivos y directorios**</span><span class="sxs-lookup"><span data-stu-id="2e2f9-175">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

