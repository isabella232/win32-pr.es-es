---
description: El método DeleteEx elimina el archivo lógico (o directorio) especificado en la ruta de acceso del objeto. Este método es una versión extendida del método Delete y se hereda de CIM \_ LogicalFile.
ms.assetid: 565d604f-01e0-4cd4-b182-9750c58bae5f
ms.tgt_platform: multiple
title: Método DeleteEx de la clase CIM_DataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.DeleteEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9af120c76e4ab8c53c945bd13aa62a2295385ac2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153006"
---
# <a name="deleteex-method-of-the-cim_datafile-class"></a><span data-ttu-id="765c9-104">Método DeleteEx de la \_ clase de archivo de archivos CIM</span><span class="sxs-lookup"><span data-stu-id="765c9-104">DeleteEx method of the CIM\_DataFile class</span></span>

<span data-ttu-id="765c9-105">El método **DeleteEx** elimina el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="765c9-105">The **DeleteEx** method deletes the logical file (or directory) that is specified in the object path.</span></span> <span data-ttu-id="765c9-106">Este método es una versión extendida del método [**Delete**](delete-method-in-class-cim-datafile.md) y se hereda de [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="765c9-106">This method is an extended version of the [**Delete**](delete-method-in-class-cim-datafile.md) method and is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="765c9-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="765c9-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="765c9-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="765c9-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="765c9-109">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="765c9-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="765c9-110">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="765c9-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="765c9-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="765c9-111">Syntax</span></span>


```mof
uint32 DeleteEx(
  [out] string REF StopFileName,
  [in]  string     StartFileName
);
```



## <a name="parameters"></a><span data-ttu-id="765c9-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="765c9-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="765c9-113">*StopFileName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="765c9-113">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="765c9-114">Cadena que representa el nombre del archivo (o directorio) donde se produjo un error en el método.</span><span class="sxs-lookup"><span data-stu-id="765c9-114">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="765c9-115">Este parámetro es NULL si el método se ejecuta correctamente.</span><span class="sxs-lookup"><span data-stu-id="765c9-115">This parameter is null if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="765c9-116">*StartFileName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="765c9-116">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="765c9-117">Cadena que representa el archivo secundario (o directorio) que se va a utilizar como punto de partida para este método.</span><span class="sxs-lookup"><span data-stu-id="765c9-117">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="765c9-118">Normalmente, el parámetro *StartFileName* es el parámetro *StopFileName* que especifica el archivo o directorio en el que se produjo un error de la llamada al método anterior.</span><span class="sxs-lookup"><span data-stu-id="765c9-118">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="765c9-119">Si este parámetro es null, la operación se realiza en el archivo (o directorio) especificado en la llamada [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="765c9-119">If this parameter is null, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="765c9-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="765c9-120">Return value</span></span>

<span data-ttu-id="765c9-121">Devuelve un valor de 0 (cero) si se realiza correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="765c9-121">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="765c9-122">Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="765c9-122">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="765c9-123">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="765c9-123">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="765c9-124">0</span><span class="sxs-lookup"><span data-stu-id="765c9-124">0</span></span>

<span data-ttu-id="765c9-125">Correcto.</span><span class="sxs-lookup"><span data-stu-id="765c9-125">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="765c9-126">2</span><span class="sxs-lookup"><span data-stu-id="765c9-126">2</span></span>

<span data-ttu-id="765c9-127">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="765c9-127">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="765c9-128">8</span><span class="sxs-lookup"><span data-stu-id="765c9-128">8</span></span>

<span data-ttu-id="765c9-129">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="765c9-129">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="765c9-130">9</span><span class="sxs-lookup"><span data-stu-id="765c9-130">9</span></span>

<span data-ttu-id="765c9-131">Objeto no válido.</span><span class="sxs-lookup"><span data-stu-id="765c9-131">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="765c9-132">10</span><span class="sxs-lookup"><span data-stu-id="765c9-132">10</span></span>

<span data-ttu-id="765c9-133">El objeto ya existe.</span><span class="sxs-lookup"><span data-stu-id="765c9-133">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="765c9-134">11</span><span class="sxs-lookup"><span data-stu-id="765c9-134">11</span></span>

<span data-ttu-id="765c9-135">Sistema de archivos no NTFS.</span><span class="sxs-lookup"><span data-stu-id="765c9-135">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="765c9-136">12</span><span class="sxs-lookup"><span data-stu-id="765c9-136">12</span></span>

<span data-ttu-id="765c9-137">Plataforma no Windows.</span><span class="sxs-lookup"><span data-stu-id="765c9-137">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="765c9-138">13</span><span class="sxs-lookup"><span data-stu-id="765c9-138">13</span></span>

<span data-ttu-id="765c9-139">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="765c9-139">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="765c9-140">14</span><span class="sxs-lookup"><span data-stu-id="765c9-140">14</span></span>

<span data-ttu-id="765c9-141">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="765c9-141">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="765c9-142">15</span><span class="sxs-lookup"><span data-stu-id="765c9-142">15</span></span>

<span data-ttu-id="765c9-143">Infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="765c9-143">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="765c9-144">16</span><span class="sxs-lookup"><span data-stu-id="765c9-144">16</span></span>

<span data-ttu-id="765c9-145">Archivo de inicio no válido.</span><span class="sxs-lookup"><span data-stu-id="765c9-145">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="765c9-146">17</span><span class="sxs-lookup"><span data-stu-id="765c9-146">17</span></span>

<span data-ttu-id="765c9-147">Privilegio no mantenido.</span><span class="sxs-lookup"><span data-stu-id="765c9-147">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="765c9-148">21</span><span class="sxs-lookup"><span data-stu-id="765c9-148">21</span></span>

<span data-ttu-id="765c9-149">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="765c9-149">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="765c9-150">Observaciones</span><span class="sxs-lookup"><span data-stu-id="765c9-150">Remarks</span></span>

<span data-ttu-id="765c9-151">WMI implementa el método **DeleteEx** en el [**archivo de \_ archivos de CIM**](cim-datafile.md) .</span><span class="sxs-lookup"><span data-stu-id="765c9-151">The **DeleteEx** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="765c9-152">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="765c9-152">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="765c9-153">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="765c9-153">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="765c9-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="765c9-154">Requirements</span></span>



| <span data-ttu-id="765c9-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="765c9-155">Requirement</span></span> | <span data-ttu-id="765c9-156">Value</span><span class="sxs-lookup"><span data-stu-id="765c9-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="765c9-157">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="765c9-157">Minimum supported client</span></span><br/> | <span data-ttu-id="765c9-158">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="765c9-158">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="765c9-159">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="765c9-159">Minimum supported server</span></span><br/> | <span data-ttu-id="765c9-160">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="765c9-160">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="765c9-161">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="765c9-161">Namespace</span></span><br/>                | <span data-ttu-id="765c9-162">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="765c9-162">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="765c9-163">MOF</span><span class="sxs-lookup"><span data-stu-id="765c9-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="765c9-164"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="765c9-164"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="765c9-165">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="765c9-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="765c9-166"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="765c9-166"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="765c9-167">Consulte también</span><span class="sxs-lookup"><span data-stu-id="765c9-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="765c9-168">\_Archivo de archivos CIM</span><span class="sxs-lookup"><span data-stu-id="765c9-168">CIM\_DataFile</span></span>](deleteex-method-in-class-cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="765c9-169">**\_Archivo de archivos CIM**</span><span class="sxs-lookup"><span data-stu-id="765c9-169">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="765c9-170">Tareas de WMI: archivos y carpetas</span><span class="sxs-lookup"><span data-stu-id="765c9-170">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="765c9-171">**Constantes de derechos de acceso a archivos y directorios**</span><span class="sxs-lookup"><span data-stu-id="765c9-171">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

