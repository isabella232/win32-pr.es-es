---
description: 'Método Compress de la clase CIM_DataFile : usa la compresión NTFS para comprimir el archivo lógico (o directorio) especificado en la ruta de acceso del objeto. Este método se hereda de CIM \_ LogicalFile.'
ms.assetid: fce57569-8290-420e-a938-10ab08ac67c3
ms.tgt_platform: multiple
title: Método Compress de la CIM_DataFile clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.Compress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3cc63ed3cafd676a0d865953c52a14e6247d4b70
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089783"
---
# <a name="compress-method-of-the-cim_datafile-class"></a><span data-ttu-id="8c6c1-104">Método Compress de la clase \_ DataFile de CIM</span><span class="sxs-lookup"><span data-stu-id="8c6c1-104">Compress method of the CIM\_DataFile class</span></span>

<span data-ttu-id="8c6c1-105">El **método Compress** usa la compresión NTFS para comprimir el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="8c6c1-105">The **Compress** method uses NTFS compression to compress the logical file (or directory) that is specified in the object path.</span></span> <span data-ttu-id="8c6c1-106">Este método se hereda de [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="8c6c1-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8c6c1-107">Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se construyen las clases WMI.</span><span class="sxs-lookup"><span data-stu-id="8c6c1-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8c6c1-108">WMI admite actualmente solo los esquemas [de versión CIM 2.x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="8c6c1-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8c6c1-109">En este tema se usa Managed Object Format sintaxis MOF .</span><span class="sxs-lookup"><span data-stu-id="8c6c1-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="8c6c1-110">Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="8c6c1-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="8c6c1-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8c6c1-111">Syntax</span></span>


```mof
uint32 Compress();
```



## <a name="parameters"></a><span data-ttu-id="8c6c1-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8c6c1-112">Parameters</span></span>

<span data-ttu-id="8c6c1-113">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="8c6c1-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8c6c1-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8c6c1-114">Return value</span></span>

<span data-ttu-id="8c6c1-115">Devuelve un valor de 0 (cero) si se ejecuta correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="8c6c1-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="8c6c1-116">Para obtener códigos de error adicionales, [**vea Constantes de error WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="8c6c1-116">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="8c6c1-117">Para obtener valores **HRESULT** generales, vea [Códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="8c6c1-117">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="8c6c1-118">**0**</span><span class="sxs-lookup"><span data-stu-id="8c6c1-118">**0**</span></span>
</dt> <dd>

<span data-ttu-id="8c6c1-119">Correcto.</span><span class="sxs-lookup"><span data-stu-id="8c6c1-119">Success.</span></span>

</dd> <dt>

<span data-ttu-id="8c6c1-120">**2**</span><span class="sxs-lookup"><span data-stu-id="8c6c1-120">**2**</span></span>
</dt> <dd>

<span data-ttu-id="8c6c1-121">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="8c6c1-121">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="8c6c1-122">**8**</span><span class="sxs-lookup"><span data-stu-id="8c6c1-122">**8**</span></span>
</dt> <dd>

<span data-ttu-id="8c6c1-123">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="8c6c1-123">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="8c6c1-124">**9**</span><span class="sxs-lookup"><span data-stu-id="8c6c1-124">**9**</span></span>
</dt> <dd>

<span data-ttu-id="8c6c1-125">Objeto no válido.</span><span class="sxs-lookup"><span data-stu-id="8c6c1-125">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="8c6c1-126">**10**</span><span class="sxs-lookup"><span data-stu-id="8c6c1-126">**10**</span></span>
</dt> <dd>

<span data-ttu-id="8c6c1-127">El objeto ya existe.</span><span class="sxs-lookup"><span data-stu-id="8c6c1-127">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="8c6c1-128">**11**</span><span class="sxs-lookup"><span data-stu-id="8c6c1-128">**11**</span></span>
</dt> <dd>

<span data-ttu-id="8c6c1-129">El sistema de archivos no es NTFS.</span><span class="sxs-lookup"><span data-stu-id="8c6c1-129">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="8c6c1-130">**12**</span><span class="sxs-lookup"><span data-stu-id="8c6c1-130">**12**</span></span>
</dt> <dd>

<span data-ttu-id="8c6c1-131">Plataforma no Windows.</span><span class="sxs-lookup"><span data-stu-id="8c6c1-131">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="8c6c1-132">**13**</span><span class="sxs-lookup"><span data-stu-id="8c6c1-132">**13**</span></span>
</dt> <dd>

<span data-ttu-id="8c6c1-133">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="8c6c1-133">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="8c6c1-134">**14**</span><span class="sxs-lookup"><span data-stu-id="8c6c1-134">**14**</span></span>
</dt> <dd>

<span data-ttu-id="8c6c1-135">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="8c6c1-135">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="8c6c1-136">**15**</span><span class="sxs-lookup"><span data-stu-id="8c6c1-136">**15**</span></span>
</dt> <dd>

<span data-ttu-id="8c6c1-137">Infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="8c6c1-137">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="8c6c1-138">**16**</span><span class="sxs-lookup"><span data-stu-id="8c6c1-138">**16**</span></span>
</dt> <dd>

<span data-ttu-id="8c6c1-139">Archivo de inicio no válido.</span><span class="sxs-lookup"><span data-stu-id="8c6c1-139">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="8c6c1-140">**17**</span><span class="sxs-lookup"><span data-stu-id="8c6c1-140">**17**</span></span>
</dt> <dd>

<span data-ttu-id="8c6c1-141">Privilegios no mantenidos.</span><span class="sxs-lookup"><span data-stu-id="8c6c1-141">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="8c6c1-142">**21**</span><span class="sxs-lookup"><span data-stu-id="8c6c1-142">**21**</span></span>
</dt> <dd>

<span data-ttu-id="8c6c1-143">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="8c6c1-143">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8c6c1-144">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8c6c1-144">Remarks</span></span>

<span data-ttu-id="8c6c1-145">WMI implementa el método **Compress** en [**CIM \_ DataFile.**](cim-datafile.md)</span><span class="sxs-lookup"><span data-stu-id="8c6c1-145">The **Compress** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="8c6c1-146">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="8c6c1-146">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8c6c1-147">Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="8c6c1-147">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c6c1-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c6c1-148">Requirements</span></span>



| <span data-ttu-id="8c6c1-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c6c1-149">Requirement</span></span> | <span data-ttu-id="8c6c1-150">Valor</span><span class="sxs-lookup"><span data-stu-id="8c6c1-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c6c1-151">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c6c1-151">Minimum supported client</span></span><br/> | <span data-ttu-id="8c6c1-152">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8c6c1-152">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8c6c1-153">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c6c1-153">Minimum supported server</span></span><br/> | <span data-ttu-id="8c6c1-154">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8c6c1-154">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8c6c1-155">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8c6c1-155">Namespace</span></span><br/>                | <span data-ttu-id="8c6c1-156">\\CIMV2 raíz</span><span class="sxs-lookup"><span data-stu-id="8c6c1-156">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8c6c1-157">MOF</span><span class="sxs-lookup"><span data-stu-id="8c6c1-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8c6c1-158"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="8c6c1-158"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8c6c1-159">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8c6c1-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c6c1-160"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c6c1-160"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c6c1-161">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8c6c1-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c6c1-162">**Archivo de datos CIM \_**</span><span class="sxs-lookup"><span data-stu-id="8c6c1-162">**CIM\_DataFile**</span></span>](compress-method-in-class-cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="8c6c1-163">**Archivo de datos CIM \_**</span><span class="sxs-lookup"><span data-stu-id="8c6c1-163">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="8c6c1-164">Tareas wmi: archivos y carpetas</span><span class="sxs-lookup"><span data-stu-id="8c6c1-164">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="8c6c1-165">**Constantes de derechos de acceso a archivos y directorios**</span><span class="sxs-lookup"><span data-stu-id="8c6c1-165">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

