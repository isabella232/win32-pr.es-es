---
description: Descomprime el archivo de datos lógico (o directorio) especificado en la ruta de acceso del objeto. Este método se hereda de \_ LOGICALFILE CIM.
ms.assetid: 0966ba13-8bbc-4283-919a-7675444409be
ms.tgt_platform: multiple
title: Método UNCOMPRESS de la clase CIM_DataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.Uncompress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 24495c94cca0eb6b99bc209cad8f25fac8f66896
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104495989"
---
# <a name="uncompress-method-of-the-cim_datafile-class"></a><span data-ttu-id="56779-104">Método UNCOMPRESS de la \_ clase de archivo de archivos CIM</span><span class="sxs-lookup"><span data-stu-id="56779-104">Uncompress method of the CIM\_DataFile class</span></span>

<span data-ttu-id="56779-105">El método **UNCOMPRESS** descomprime el archivo de datos lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="56779-105">The **Uncompress** method uncompresses the logical data file (or directory) that is specified in the object path.</span></span> <span data-ttu-id="56779-106">Este método se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="56779-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="56779-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="56779-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="56779-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="56779-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="56779-109">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="56779-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="56779-110">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="56779-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="56779-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="56779-111">Syntax</span></span>


```mof
uint32 Uncompress();
```



## <a name="parameters"></a><span data-ttu-id="56779-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="56779-112">Parameters</span></span>

<span data-ttu-id="56779-113">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="56779-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="56779-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="56779-114">Return value</span></span>

<span data-ttu-id="56779-115">Devuelve un valor de 0 (cero) si se realiza correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="56779-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="56779-116">Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="56779-116">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="56779-117">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="56779-117">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="56779-118">**0**</span><span class="sxs-lookup"><span data-stu-id="56779-118">**0**</span></span>
</dt> <dd>

<span data-ttu-id="56779-119">Correcto.</span><span class="sxs-lookup"><span data-stu-id="56779-119">Success.</span></span>

</dd> <dt>

<span data-ttu-id="56779-120">**2**</span><span class="sxs-lookup"><span data-stu-id="56779-120">**2**</span></span>
</dt> <dd>

<span data-ttu-id="56779-121">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="56779-121">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="56779-122">**8**</span><span class="sxs-lookup"><span data-stu-id="56779-122">**8**</span></span>
</dt> <dd>

<span data-ttu-id="56779-123">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="56779-123">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="56779-124">**9**</span><span class="sxs-lookup"><span data-stu-id="56779-124">**9**</span></span>
</dt> <dd>

<span data-ttu-id="56779-125">Objeto no válido.</span><span class="sxs-lookup"><span data-stu-id="56779-125">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="56779-126">**10**</span><span class="sxs-lookup"><span data-stu-id="56779-126">**10**</span></span>
</dt> <dd>

<span data-ttu-id="56779-127">El objeto ya existe.</span><span class="sxs-lookup"><span data-stu-id="56779-127">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="56779-128">**11**</span><span class="sxs-lookup"><span data-stu-id="56779-128">**11**</span></span>
</dt> <dd>

<span data-ttu-id="56779-129">Sistema de archivos no NTFS.</span><span class="sxs-lookup"><span data-stu-id="56779-129">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="56779-130">**12**</span><span class="sxs-lookup"><span data-stu-id="56779-130">**12**</span></span>
</dt> <dd>

<span data-ttu-id="56779-131">Plataforma no Windows.</span><span class="sxs-lookup"><span data-stu-id="56779-131">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="56779-132">**13**</span><span class="sxs-lookup"><span data-stu-id="56779-132">**13**</span></span>
</dt> <dd>

<span data-ttu-id="56779-133">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="56779-133">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="56779-134">**14**</span><span class="sxs-lookup"><span data-stu-id="56779-134">**14**</span></span>
</dt> <dd>

<span data-ttu-id="56779-135">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="56779-135">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="56779-136">**15**</span><span class="sxs-lookup"><span data-stu-id="56779-136">**15**</span></span>
</dt> <dd>

<span data-ttu-id="56779-137">Infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="56779-137">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="56779-138">**16**</span><span class="sxs-lookup"><span data-stu-id="56779-138">**16**</span></span>
</dt> <dd>

<span data-ttu-id="56779-139">Archivo de inicio no válido.</span><span class="sxs-lookup"><span data-stu-id="56779-139">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="56779-140">**17**</span><span class="sxs-lookup"><span data-stu-id="56779-140">**17**</span></span>
</dt> <dd>

<span data-ttu-id="56779-141">Privilegio no mantenido.</span><span class="sxs-lookup"><span data-stu-id="56779-141">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="56779-142">**21**</span><span class="sxs-lookup"><span data-stu-id="56779-142">**21**</span></span>
</dt> <dd>

<span data-ttu-id="56779-143">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="56779-143">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="56779-144">Observaciones</span><span class="sxs-lookup"><span data-stu-id="56779-144">Remarks</span></span>

<span data-ttu-id="56779-145">WMI implementa el método **UNCOMPRESS** en el [**archivo de \_ archivos de CIM**](cim-datafile.md) .</span><span class="sxs-lookup"><span data-stu-id="56779-145">The **Uncompress** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="56779-146">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="56779-146">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="56779-147">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="56779-147">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="56779-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56779-148">Requirements</span></span>



| <span data-ttu-id="56779-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="56779-149">Requirement</span></span> | <span data-ttu-id="56779-150">Value</span><span class="sxs-lookup"><span data-stu-id="56779-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="56779-151">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="56779-151">Minimum supported client</span></span><br/> | <span data-ttu-id="56779-152">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="56779-152">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="56779-153">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="56779-153">Minimum supported server</span></span><br/> | <span data-ttu-id="56779-154">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="56779-154">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="56779-155">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="56779-155">Namespace</span></span><br/>                | <span data-ttu-id="56779-156">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="56779-156">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="56779-157">MOF</span><span class="sxs-lookup"><span data-stu-id="56779-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="56779-158"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="56779-158"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="56779-159">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="56779-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56779-160"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56779-160"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56779-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="56779-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56779-162">**\_Archivo de archivos CIM**</span><span class="sxs-lookup"><span data-stu-id="56779-162">**CIM\_DataFile**</span></span>](uncompress-method-in-class-cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="56779-163">**\_Archivo de archivos CIM**</span><span class="sxs-lookup"><span data-stu-id="56779-163">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="56779-164">Tareas de WMI: archivos y carpetas</span><span class="sxs-lookup"><span data-stu-id="56779-164">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="56779-165">**Constantes de derechos de acceso a archivos y directorios**</span><span class="sxs-lookup"><span data-stu-id="56779-165">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

