---
description: El método CopyEx copia el archivo lógico (o directorio) especificado en la ruta de acceso del objeto en la ubicación especificada por el parámetro FileName.
ms.assetid: e52c1a0f-e34c-4a61-9e54-ed172976cb61
ms.tgt_platform: multiple
title: Método CopyEx de la clase CIM_DataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.CopyEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a83f1556aeeafbb5cc95eddbd84806bdaef0be14
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659583"
---
# <a name="copyex-method-of-the-cim_datafile-class"></a><span data-ttu-id="a58f1-103">Método CopyEx de la \_ clase de archivo de archivos CIM</span><span class="sxs-lookup"><span data-stu-id="a58f1-103">CopyEx method of the CIM\_DataFile class</span></span>

<span data-ttu-id="a58f1-104">El método **CopyEx** copia el archivo lógico (o directorio) especificado en la ruta de acceso del objeto en la ubicación especificada por el parámetro *filename* .</span><span class="sxs-lookup"><span data-stu-id="a58f1-104">The **CopyEx** method copies the logical file (or directory) that is specified in the object path to the location specified by the *FileName* parameter.</span></span> <span data-ttu-id="a58f1-105">No se admite una copia si requiere sobrescribir un archivo lógico existente.</span><span class="sxs-lookup"><span data-stu-id="a58f1-105">A copy is not supported if it requires overwriting an existing logical file.</span></span> <span data-ttu-id="a58f1-106">Este método es una versión extendida del método de [**copia**](copy-method-in-class-cim-datafile.md) y se hereda de [CIM \_ LogicalFile](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="a58f1-106">This method is an extended version of the [**Copy**](copy-method-in-class-cim-datafile.md) method and is inherited from [CIM\_LogicalFile](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a58f1-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="a58f1-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a58f1-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a58f1-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a58f1-109">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="a58f1-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="a58f1-110">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="a58f1-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="a58f1-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a58f1-111">Syntax</span></span>


```mof
uint32 CopyEx(
  [in]  string     FileName,
  [out] string REF StopFileName,
  [in]  string     StartFileName,
  [in]  boolean    Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="a58f1-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a58f1-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a58f1-113">*Nombre de archivo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a58f1-113">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a58f1-114">Nombre completo del archivo de destino (o directorio).</span><span class="sxs-lookup"><span data-stu-id="a58f1-114">Fully qualified name of the destination file (or directory).</span></span>

<span data-ttu-id="a58f1-115">Ejemplo: "c: \\ temp \\ newdirectory"</span><span class="sxs-lookup"><span data-stu-id="a58f1-115">Example: "c:\\temp\\newdirectory"</span></span>

</dd> <dt>

<span data-ttu-id="a58f1-116">*StopFileName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a58f1-116">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a58f1-117">Cadena que representa el nombre del archivo (o directorio) donde se produjo un error en el método.</span><span class="sxs-lookup"><span data-stu-id="a58f1-117">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="a58f1-118">Este parámetro será **null** si el método se ejecuta correctamente.</span><span class="sxs-lookup"><span data-stu-id="a58f1-118">This parameter will be **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="a58f1-119">*StartFileName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a58f1-119">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a58f1-120">Cadena que representa el archivo secundario (o directorio) que se va a utilizar como punto de partida para este método.</span><span class="sxs-lookup"><span data-stu-id="a58f1-120">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="a58f1-121">Normalmente, el parámetro *StartFileName* es el parámetro *StopFileName* que especifica el archivo (o directorio) en el que se produjo un error de la llamada al método anterior.</span><span class="sxs-lookup"><span data-stu-id="a58f1-121">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file (or directory) at which an error occurred from the previous method call.</span></span> <span data-ttu-id="a58f1-122">Si este parámetro es **null**, la operación se realiza en el archivo (o directorio) especificado en la llamada [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="a58f1-122">If this parameter is **null**, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

<span data-ttu-id="a58f1-123">Si se utiliza *StartFileName* , *Recursive* también debe establecerse en true.</span><span class="sxs-lookup"><span data-stu-id="a58f1-123">If *StartFileName* is used, *Recursive* must be set to true as well.</span></span>

</dd> <dt>

<span data-ttu-id="a58f1-124">*Recursivo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a58f1-124">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a58f1-125">Si es TRUE, el método también se aplica de forma recursiva a los archivos y directorios dentro del directorio especificado por la instancia de [**\_ archivo de archivos CIM**](cim-datafile.md) .</span><span class="sxs-lookup"><span data-stu-id="a58f1-125">If TRUE, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_DataFile**](cim-datafile.md) instance.</span></span> <span data-ttu-id="a58f1-126">En el caso de las instancias de archivo, este parámetro se omite.</span><span class="sxs-lookup"><span data-stu-id="a58f1-126">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a58f1-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a58f1-127">Return value</span></span>

<span data-ttu-id="a58f1-128">Devuelve un valor de 0 (cero) si se realiza correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="a58f1-128">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="a58f1-129">Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="a58f1-129">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="a58f1-130">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="a58f1-130">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="a58f1-131">0</span><span class="sxs-lookup"><span data-stu-id="a58f1-131">0</span></span>

<span data-ttu-id="a58f1-132">Correcto.</span><span class="sxs-lookup"><span data-stu-id="a58f1-132">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="a58f1-133">2</span><span class="sxs-lookup"><span data-stu-id="a58f1-133">2</span></span>

<span data-ttu-id="a58f1-134">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="a58f1-134">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="a58f1-135">8</span><span class="sxs-lookup"><span data-stu-id="a58f1-135">8</span></span>

<span data-ttu-id="a58f1-136">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="a58f1-136">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="a58f1-137">9</span><span class="sxs-lookup"><span data-stu-id="a58f1-137">9</span></span>

<span data-ttu-id="a58f1-138">Objeto no válido.</span><span class="sxs-lookup"><span data-stu-id="a58f1-138">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="a58f1-139">10</span><span class="sxs-lookup"><span data-stu-id="a58f1-139">10</span></span>

<span data-ttu-id="a58f1-140">El objeto ya existe.</span><span class="sxs-lookup"><span data-stu-id="a58f1-140">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="a58f1-141">11</span><span class="sxs-lookup"><span data-stu-id="a58f1-141">11</span></span>

<span data-ttu-id="a58f1-142">Sistema de archivos no NTFS.</span><span class="sxs-lookup"><span data-stu-id="a58f1-142">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="a58f1-143">12</span><span class="sxs-lookup"><span data-stu-id="a58f1-143">12</span></span>

<span data-ttu-id="a58f1-144">Plataforma no Windows.</span><span class="sxs-lookup"><span data-stu-id="a58f1-144">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="a58f1-145">13</span><span class="sxs-lookup"><span data-stu-id="a58f1-145">13</span></span>

<span data-ttu-id="a58f1-146">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="a58f1-146">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="a58f1-147">14</span><span class="sxs-lookup"><span data-stu-id="a58f1-147">14</span></span>

<span data-ttu-id="a58f1-148">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="a58f1-148">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="a58f1-149">15</span><span class="sxs-lookup"><span data-stu-id="a58f1-149">15</span></span>

<span data-ttu-id="a58f1-150">Infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="a58f1-150">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="a58f1-151">16</span><span class="sxs-lookup"><span data-stu-id="a58f1-151">16</span></span>

<span data-ttu-id="a58f1-152">Archivo de inicio no válido.</span><span class="sxs-lookup"><span data-stu-id="a58f1-152">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="a58f1-153">17</span><span class="sxs-lookup"><span data-stu-id="a58f1-153">17</span></span>

<span data-ttu-id="a58f1-154">Privilegio no mantenido.</span><span class="sxs-lookup"><span data-stu-id="a58f1-154">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="a58f1-155">21</span><span class="sxs-lookup"><span data-stu-id="a58f1-155">21</span></span>

<span data-ttu-id="a58f1-156">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="a58f1-156">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a58f1-157">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a58f1-157">Remarks</span></span>

<span data-ttu-id="a58f1-158">WMI implementa el método **CopyEx** en el [**archivo de \_ archivos de CIM**](cim-datafile.md) .</span><span class="sxs-lookup"><span data-stu-id="a58f1-158">The **CopyEx** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="a58f1-159">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="a58f1-159">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a58f1-160">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="a58f1-160">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a58f1-161">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a58f1-161">Requirements</span></span>



| <span data-ttu-id="a58f1-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="a58f1-162">Requirement</span></span> | <span data-ttu-id="a58f1-163">Value</span><span class="sxs-lookup"><span data-stu-id="a58f1-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a58f1-164">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a58f1-164">Minimum supported client</span></span><br/> | <span data-ttu-id="a58f1-165">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a58f1-165">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a58f1-166">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a58f1-166">Minimum supported server</span></span><br/> | <span data-ttu-id="a58f1-167">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a58f1-167">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a58f1-168">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a58f1-168">Namespace</span></span><br/>                | <span data-ttu-id="a58f1-169">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="a58f1-169">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a58f1-170">MOF</span><span class="sxs-lookup"><span data-stu-id="a58f1-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a58f1-171"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a58f1-171"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a58f1-172">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a58f1-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a58f1-173"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a58f1-173"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a58f1-174">Vea también</span><span class="sxs-lookup"><span data-stu-id="a58f1-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a58f1-175">**\_Archivo de archivos CIM**</span><span class="sxs-lookup"><span data-stu-id="a58f1-175">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="a58f1-176">Tareas de WMI: archivos y carpetas</span><span class="sxs-lookup"><span data-stu-id="a58f1-176">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="a58f1-177">**Constantes de derechos de acceso a archivos y directorios**</span><span class="sxs-lookup"><span data-stu-id="a58f1-177">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

