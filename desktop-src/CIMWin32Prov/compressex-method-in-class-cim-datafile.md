---
description: 'Método CompressEx de la clase CIM_DataFile : usa la compresión NTFS para comprimir el archivo lógico (o directorio) especificado en la ruta de acceso del objeto. Este método se hereda de CIM \_ LogicalFile.'
ms.assetid: 553b6a90-d16c-4abb-9015-66fe8e1606f6
ms.tgt_platform: multiple
title: Método CompressEx de la CIM_DataFile clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.CompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ccc155c04c6c25f38050bd37827eb0c2e2e0e73e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089793"
---
# <a name="compressex-method-of-the-cim_datafile-class"></a><span data-ttu-id="589dc-104">Método CompressEx de la clase \_ DataFile de CIM</span><span class="sxs-lookup"><span data-stu-id="589dc-104">CompressEx method of the CIM\_DataFile class</span></span>

<span data-ttu-id="589dc-105">El **método CompressEx** usa la compresión NTFS para comprimir el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="589dc-105">The **CompressEx** method uses NTFS compression to compress the logical file (or directory) that is specified in the object path.</span></span> <span data-ttu-id="589dc-106">Este método se hereda de [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="589dc-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span> <span data-ttu-id="589dc-107">Este método es una versión extendida del método [**Compress**](compress-method-in-class-cim-datafile.md) y se hereda de [CIM \_ LogicalFile](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="589dc-107">This method is an extended version of the [**Compress**](compress-method-in-class-cim-datafile.md) method and is inherited from [CIM\_LogicalFile](/windows/desktop/WmiSdk/calling-a-method).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="589dc-108">Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se construyen las clases WMI.</span><span class="sxs-lookup"><span data-stu-id="589dc-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="589dc-109">WMI admite actualmente solo los esquemas [de versión CIM 2.x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="589dc-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="589dc-110">En este tema se usa Managed Object Format sintaxis MOF .</span><span class="sxs-lookup"><span data-stu-id="589dc-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="589dc-111">Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="589dc-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="589dc-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="589dc-112">Syntax</span></span>


```mof
uint32 CompressEx(
  [out] string  StopFileName,
  [in]  string  StartFileName,
  [in]  boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="589dc-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="589dc-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="589dc-114">*StopFileName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="589dc-114">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="589dc-115">Cadena que representa el nombre del archivo (o directorio) en el que se ha fallado el método.</span><span class="sxs-lookup"><span data-stu-id="589dc-115">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="589dc-116">Este parámetro es NULL si el método se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="589dc-116">This parameter is null if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="589dc-117">*StartFileName* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="589dc-117">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="589dc-118">Cadena que representa el archivo secundario (o directorio) que se va a usar como punto de partida para este método.</span><span class="sxs-lookup"><span data-stu-id="589dc-118">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="589dc-119">Normalmente, el *parámetro StartFileName* es el *parámetro StopFileName* que especifica el archivo o directorio en el que se produjo un error de la llamada al método anterior.</span><span class="sxs-lookup"><span data-stu-id="589dc-119">Typically, the *StartFileName* parameter is the *StopFileName* parameter that specifies the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="589dc-120">Si este parámetro es NULL, la operación se realiza en el archivo o directorio especificado en la **llamada a ExecMethod.**</span><span class="sxs-lookup"><span data-stu-id="589dc-120">If this parameter is null, the operation is performed on the file or directory specified in the **ExecMethod** call.</span></span>

<span data-ttu-id="589dc-121">Si *se usa StartFileName,* *Recursive* también debe establecerse en true.</span><span class="sxs-lookup"><span data-stu-id="589dc-121">If *StartFileName* is used, *Recursive* must be set to true as well.</span></span>

</dd> <dt>

<span data-ttu-id="589dc-122">*Recursivo* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="589dc-122">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="589dc-123">Si **es TRUE,** el método también se aplica de forma recursiva a los archivos y directorios dentro del directorio especificado por la instancia [**de \_ DataFile de CIM.**](cim-datafile.md)</span><span class="sxs-lookup"><span data-stu-id="589dc-123">If **TRUE**, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_DataFile**](cim-datafile.md) instance.</span></span> <span data-ttu-id="589dc-124">En el caso de las instancias de archivo, este parámetro se omite.</span><span class="sxs-lookup"><span data-stu-id="589dc-124">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="589dc-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="589dc-125">Return value</span></span>

<span data-ttu-id="589dc-126">Devuelve un valor de 0 (cero) si se ejecuta correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="589dc-126">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="589dc-127">Para obtener códigos de error adicionales, [**vea Constantes de error WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="589dc-127">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="589dc-128">Para obtener valores **HRESULT** generales, vea [Códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="589dc-128">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="589dc-129">**0**</span><span class="sxs-lookup"><span data-stu-id="589dc-129">**0**</span></span>
</dt> <dd>

<span data-ttu-id="589dc-130">Correcto.</span><span class="sxs-lookup"><span data-stu-id="589dc-130">Success.</span></span>

</dd> <dt>

<span data-ttu-id="589dc-131">**2**</span><span class="sxs-lookup"><span data-stu-id="589dc-131">**2**</span></span>
</dt> <dd>

<span data-ttu-id="589dc-132">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="589dc-132">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="589dc-133">**8**</span><span class="sxs-lookup"><span data-stu-id="589dc-133">**8**</span></span>
</dt> <dd>

<span data-ttu-id="589dc-134">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="589dc-134">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="589dc-135">**9**</span><span class="sxs-lookup"><span data-stu-id="589dc-135">**9**</span></span>
</dt> <dd>

<span data-ttu-id="589dc-136">Objeto no válido.</span><span class="sxs-lookup"><span data-stu-id="589dc-136">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="589dc-137">**10**</span><span class="sxs-lookup"><span data-stu-id="589dc-137">**10**</span></span>
</dt> <dd>

<span data-ttu-id="589dc-138">El objeto ya existe.</span><span class="sxs-lookup"><span data-stu-id="589dc-138">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="589dc-139">**11**</span><span class="sxs-lookup"><span data-stu-id="589dc-139">**11**</span></span>
</dt> <dd>

<span data-ttu-id="589dc-140">El sistema de archivos no es NTFS.</span><span class="sxs-lookup"><span data-stu-id="589dc-140">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="589dc-141">**12**</span><span class="sxs-lookup"><span data-stu-id="589dc-141">**12**</span></span>
</dt> <dd>

<span data-ttu-id="589dc-142">Plataforma no Windows.</span><span class="sxs-lookup"><span data-stu-id="589dc-142">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="589dc-143">**13**</span><span class="sxs-lookup"><span data-stu-id="589dc-143">**13**</span></span>
</dt> <dd>

<span data-ttu-id="589dc-144">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="589dc-144">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="589dc-145">**14**</span><span class="sxs-lookup"><span data-stu-id="589dc-145">**14**</span></span>
</dt> <dd>

<span data-ttu-id="589dc-146">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="589dc-146">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="589dc-147">**15**</span><span class="sxs-lookup"><span data-stu-id="589dc-147">**15**</span></span>
</dt> <dd>

<span data-ttu-id="589dc-148">Infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="589dc-148">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="589dc-149">**16**</span><span class="sxs-lookup"><span data-stu-id="589dc-149">**16**</span></span>
</dt> <dd>

<span data-ttu-id="589dc-150">Archivo de inicio no válido.</span><span class="sxs-lookup"><span data-stu-id="589dc-150">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="589dc-151">**17**</span><span class="sxs-lookup"><span data-stu-id="589dc-151">**17**</span></span>
</dt> <dd>

<span data-ttu-id="589dc-152">Privilegios no mantenidos.</span><span class="sxs-lookup"><span data-stu-id="589dc-152">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="589dc-153">**21**</span><span class="sxs-lookup"><span data-stu-id="589dc-153">**21**</span></span>
</dt> <dd>

<span data-ttu-id="589dc-154">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="589dc-154">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="589dc-155">Comentarios</span><span class="sxs-lookup"><span data-stu-id="589dc-155">Remarks</span></span>

<span data-ttu-id="589dc-156">WMI implementa el método **CompressEx** [**en CIM \_ DataFile.**](cim-datafile.md)</span><span class="sxs-lookup"><span data-stu-id="589dc-156">The **CompressEx** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="589dc-157">Esta documentación se deriva de las descripciones de clases CIM publicadas por dmtf.</span><span class="sxs-lookup"><span data-stu-id="589dc-157">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="589dc-158">Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="589dc-158">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="589dc-159">Requisitos</span><span class="sxs-lookup"><span data-stu-id="589dc-159">Requirements</span></span>



| <span data-ttu-id="589dc-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="589dc-160">Requirement</span></span> | <span data-ttu-id="589dc-161">Valor</span><span class="sxs-lookup"><span data-stu-id="589dc-161">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="589dc-162">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="589dc-162">Minimum supported client</span></span><br/> | <span data-ttu-id="589dc-163">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="589dc-163">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="589dc-164">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="589dc-164">Minimum supported server</span></span><br/> | <span data-ttu-id="589dc-165">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="589dc-165">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="589dc-166">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="589dc-166">Namespace</span></span><br/>                | <span data-ttu-id="589dc-167">\\CIMV2 raíz</span><span class="sxs-lookup"><span data-stu-id="589dc-167">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="589dc-168">MOF</span><span class="sxs-lookup"><span data-stu-id="589dc-168">MOF</span></span><br/>                      | <dl> <span data-ttu-id="589dc-169"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="589dc-169"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="589dc-170">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="589dc-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="589dc-171"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="589dc-171"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="589dc-172">Consulte también</span><span class="sxs-lookup"><span data-stu-id="589dc-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="589dc-173">CIM \_ DataFile</span><span class="sxs-lookup"><span data-stu-id="589dc-173">CIM\_DataFile</span></span>](compressex-method-in-class-cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="589dc-174">**CIM \_ DataFile**</span><span class="sxs-lookup"><span data-stu-id="589dc-174">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="589dc-175">Tareas wmi: archivos y carpetas</span><span class="sxs-lookup"><span data-stu-id="589dc-175">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="589dc-176">**Constantes de derechos de acceso a archivos y directorios**</span><span class="sxs-lookup"><span data-stu-id="589dc-176">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

