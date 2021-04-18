---
description: El método de copia copia el archivo lógico (o directorio) especificado en la ruta de acceso del objeto en la ubicación especificada por el parámetro de entrada.
ms.assetid: 13bd7da8-a562-414b-8d23-6f58e1c55878
ms.tgt_platform: multiple
title: Método de copia de la clase CIM_DataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.Copy
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c126f1cd54470e50a700fdea1c121776d687a9dc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659588"
---
# <a name="copy-method-of-the-cim_datafile-class"></a><span data-ttu-id="8d95d-103">Método de copia de la \_ clase de archivo de archivos CIM</span><span class="sxs-lookup"><span data-stu-id="8d95d-103">Copy method of the CIM\_DataFile class</span></span>

<span data-ttu-id="8d95d-104">El método de **copia** copia el archivo lógico (o directorio) especificado en la ruta de acceso del objeto en la ubicación especificada por el parámetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="8d95d-104">The **Copy** method copies the logical file (or directory) that is specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="8d95d-105">No se admite una copia si requiere sobrescribir un archivo lógico existente.</span><span class="sxs-lookup"><span data-stu-id="8d95d-105">A copy is not supported if it requires overwriting an existing logical file.</span></span> <span data-ttu-id="8d95d-106">Este método se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="8d95d-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8d95d-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="8d95d-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8d95d-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="8d95d-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8d95d-109">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="8d95d-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="8d95d-110">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="8d95d-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="8d95d-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8d95d-111">Syntax</span></span>


```mof
uint32 Copy(
  [in] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="8d95d-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8d95d-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d95d-113">*Nombre de archivo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8d95d-113">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d95d-114">Nombre completo del archivo de destino (o directorio).</span><span class="sxs-lookup"><span data-stu-id="8d95d-114">Fully qualified name of the destination file (or directory).</span></span>

<span data-ttu-id="8d95d-115">Ejemplo: "c: \\ temp \\ newdirectory"</span><span class="sxs-lookup"><span data-stu-id="8d95d-115">Example: "c:\\temp\\newdirectory"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d95d-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8d95d-116">Return value</span></span>

<span data-ttu-id="8d95d-117">Devuelve un valor de 0 si se ejecuta correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="8d95d-117">Returns a value of 0 on success, and any other number to indicate an error.</span></span> <span data-ttu-id="8d95d-118">Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="8d95d-118">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="8d95d-119">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="8d95d-119">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="8d95d-120">**0**</span><span class="sxs-lookup"><span data-stu-id="8d95d-120">**0**</span></span>
</dt> <dd>

<span data-ttu-id="8d95d-121">Correcto.</span><span class="sxs-lookup"><span data-stu-id="8d95d-121">Success.</span></span>

</dd> <dt>

<span data-ttu-id="8d95d-122">**2**</span><span class="sxs-lookup"><span data-stu-id="8d95d-122">**2**</span></span>
</dt> <dd>

<span data-ttu-id="8d95d-123">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="8d95d-123">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="8d95d-124">**8**</span><span class="sxs-lookup"><span data-stu-id="8d95d-124">**8**</span></span>
</dt> <dd>

<span data-ttu-id="8d95d-125">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="8d95d-125">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="8d95d-126">**9**</span><span class="sxs-lookup"><span data-stu-id="8d95d-126">**9**</span></span>
</dt> <dd>

<span data-ttu-id="8d95d-127">Objeto no válido.</span><span class="sxs-lookup"><span data-stu-id="8d95d-127">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="8d95d-128">**10**</span><span class="sxs-lookup"><span data-stu-id="8d95d-128">**10**</span></span>
</dt> <dd>

<span data-ttu-id="8d95d-129">El objeto ya existe.</span><span class="sxs-lookup"><span data-stu-id="8d95d-129">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="8d95d-130">**11**</span><span class="sxs-lookup"><span data-stu-id="8d95d-130">**11**</span></span>
</dt> <dd>

<span data-ttu-id="8d95d-131">Sistema de archivos no NTFS.</span><span class="sxs-lookup"><span data-stu-id="8d95d-131">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="8d95d-132">**12**</span><span class="sxs-lookup"><span data-stu-id="8d95d-132">**12**</span></span>
</dt> <dd>

<span data-ttu-id="8d95d-133">Plataforma no Windows.</span><span class="sxs-lookup"><span data-stu-id="8d95d-133">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="8d95d-134">**13**</span><span class="sxs-lookup"><span data-stu-id="8d95d-134">**13**</span></span>
</dt> <dd>

<span data-ttu-id="8d95d-135">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="8d95d-135">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="8d95d-136">**14**</span><span class="sxs-lookup"><span data-stu-id="8d95d-136">**14**</span></span>
</dt> <dd>

<span data-ttu-id="8d95d-137">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="8d95d-137">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="8d95d-138">**15**</span><span class="sxs-lookup"><span data-stu-id="8d95d-138">**15**</span></span>
</dt> <dd>

<span data-ttu-id="8d95d-139">Infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="8d95d-139">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="8d95d-140">**16**</span><span class="sxs-lookup"><span data-stu-id="8d95d-140">**16**</span></span>
</dt> <dd>

<span data-ttu-id="8d95d-141">Archivo de inicio no válido.</span><span class="sxs-lookup"><span data-stu-id="8d95d-141">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="8d95d-142">**17**</span><span class="sxs-lookup"><span data-stu-id="8d95d-142">**17**</span></span>
</dt> <dd>

<span data-ttu-id="8d95d-143">Privilegio no mantenido.</span><span class="sxs-lookup"><span data-stu-id="8d95d-143">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="8d95d-144">**21**</span><span class="sxs-lookup"><span data-stu-id="8d95d-144">**21**</span></span>
</dt> <dd>

<span data-ttu-id="8d95d-145">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="8d95d-145">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8d95d-146">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8d95d-146">Remarks</span></span>

<span data-ttu-id="8d95d-147">WMI implementa el método de **copia** en el [**archivo de \_ archivos de CIM**](cim-datafile.md) .</span><span class="sxs-lookup"><span data-stu-id="8d95d-147">The **Copy** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="8d95d-148">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="8d95d-148">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8d95d-149">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="8d95d-149">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d95d-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d95d-150">Requirements</span></span>



| <span data-ttu-id="8d95d-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d95d-151">Requirement</span></span> | <span data-ttu-id="8d95d-152">Value</span><span class="sxs-lookup"><span data-stu-id="8d95d-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d95d-153">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8d95d-153">Minimum supported client</span></span><br/> | <span data-ttu-id="8d95d-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8d95d-154">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8d95d-155">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8d95d-155">Minimum supported server</span></span><br/> | <span data-ttu-id="8d95d-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8d95d-156">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8d95d-157">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8d95d-157">Namespace</span></span><br/>                | <span data-ttu-id="8d95d-158">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="8d95d-158">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8d95d-159">MOF</span><span class="sxs-lookup"><span data-stu-id="8d95d-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8d95d-160"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8d95d-160"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8d95d-161">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8d95d-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d95d-162"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d95d-162"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d95d-163">Vea también</span><span class="sxs-lookup"><span data-stu-id="8d95d-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d95d-164">\_Archivo de archivos CIM</span><span class="sxs-lookup"><span data-stu-id="8d95d-164">CIM\_DataFile</span></span>](copy-method-in-class-cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="8d95d-165">**\_Archivo de archivos CIM**</span><span class="sxs-lookup"><span data-stu-id="8d95d-165">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="8d95d-166">Tareas de WMI: archivos y carpetas</span><span class="sxs-lookup"><span data-stu-id="8d95d-166">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="8d95d-167">**Constantes de derechos de acceso a archivos y directorios**</span><span class="sxs-lookup"><span data-stu-id="8d95d-167">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

