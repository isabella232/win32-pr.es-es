---
description: El método CopyEx copia el archivo lógico (o directorio) especificado en la ruta de acceso del objeto en la ubicación especificada por el parámetro FileName. Este método es una versión extendida del método de copia y se hereda de CIM \_ LogicalFile.
ms.assetid: e207cc80-055e-41bc-ab80-dc50131b544d
ms.tgt_platform: multiple
title: Método CopyEx de la clase CIM_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.CopyEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1d7502c46c616d9b8e1fffeebf5aefcd022dd4cc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998160"
---
# <a name="copyex-method-of-the-cim_directory-class"></a><span data-ttu-id="82715-104">Método CopyEx de la \_ clase de directorio CIM</span><span class="sxs-lookup"><span data-stu-id="82715-104">CopyEx method of the CIM\_Directory class</span></span>

<span data-ttu-id="82715-105">El método **CopyEx** copia el archivo lógico (o directorio) especificado en la ruta de acceso del objeto en la ubicación especificada por el parámetro *filename* .</span><span class="sxs-lookup"><span data-stu-id="82715-105">The **CopyEx** method copies the logical file (or directory) specified in the object path to the location specified by the *FileName* parameter.</span></span> <span data-ttu-id="82715-106">Este método es una versión extendida del método de [**copia**](copy-method-in-class-cim-directory.md) y se hereda de [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="82715-106">This method is an extended version of the [**Copy**](copy-method-in-class-cim-directory.md) method and is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="82715-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="82715-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="82715-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="82715-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="82715-109">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="82715-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="82715-110">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="82715-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="82715-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="82715-111">Syntax</span></span>


```mof
uint32 CopyEx(
  [in]  string REF FileName,
  [out] string     StopFileName,
  [in]  string     StartFileName,
  [in]  boolean    Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="82715-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="82715-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82715-113">*Nombre de archivo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="82715-113">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82715-114">Nombre completo de la copia del archivo de destino (o directorio).</span><span class="sxs-lookup"><span data-stu-id="82715-114">Fully qualified name of the copy of the destination file (or directory).</span></span>

<span data-ttu-id="82715-115">Ejemplo: "c: \\ temp \\ newdirectory"</span><span class="sxs-lookup"><span data-stu-id="82715-115">Example: "c:\\temp\\newdirectory"</span></span>

</dd> <dt>

<span data-ttu-id="82715-116">*StopFileName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="82715-116">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="82715-117">Cadena que representa el nombre del archivo (o directorio) donde se produjo un error en el método.</span><span class="sxs-lookup"><span data-stu-id="82715-117">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="82715-118">Este parámetro es **null** si el método se ejecuta correctamente.</span><span class="sxs-lookup"><span data-stu-id="82715-118">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="82715-119">*StartFileName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="82715-119">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82715-120">Cadena que representa el archivo secundario (o directorio) que se va a utilizar como punto de partida para este método.</span><span class="sxs-lookup"><span data-stu-id="82715-120">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="82715-121">Normalmente, este parámetro es el parámetro *StopFileName* que especifica el archivo o directorio en el que se produjo un error de la llamada al método anterior.</span><span class="sxs-lookup"><span data-stu-id="82715-121">Typically, this parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="82715-122">Si este parámetro es **null**, la operación se realiza en el archivo (o directorio) especificado en la llamada [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="82715-122">If this parameter is **null**, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="82715-123">*Recursivo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="82715-123">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82715-124">Si es TRUE, el método también se aplica de forma recursiva a los archivos y directorios del directorio especificado por la instancia de [**\_ directorio CIM**](cim-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="82715-124">If TRUE, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_Directory**](cim-directory.md) instance.</span></span> <span data-ttu-id="82715-125">En el caso de las instancias de archivo, este parámetro se omite.</span><span class="sxs-lookup"><span data-stu-id="82715-125">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82715-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="82715-126">Return value</span></span>

<span data-ttu-id="82715-127">Devuelve un valor de 0 (cero) si se realiza correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="82715-127">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="82715-128">0</span><span class="sxs-lookup"><span data-stu-id="82715-128">0</span></span>

<span data-ttu-id="82715-129">Correcto.</span><span class="sxs-lookup"><span data-stu-id="82715-129">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="82715-130">2</span><span class="sxs-lookup"><span data-stu-id="82715-130">2</span></span>

<span data-ttu-id="82715-131">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="82715-131">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="82715-132">8</span><span class="sxs-lookup"><span data-stu-id="82715-132">8</span></span>

<span data-ttu-id="82715-133">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="82715-133">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="82715-134">9</span><span class="sxs-lookup"><span data-stu-id="82715-134">9</span></span>

<span data-ttu-id="82715-135">Objeto no válido.</span><span class="sxs-lookup"><span data-stu-id="82715-135">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="82715-136">10</span><span class="sxs-lookup"><span data-stu-id="82715-136">10</span></span>

<span data-ttu-id="82715-137">El objeto ya existe.</span><span class="sxs-lookup"><span data-stu-id="82715-137">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="82715-138">11</span><span class="sxs-lookup"><span data-stu-id="82715-138">11</span></span>

<span data-ttu-id="82715-139">Sistema de archivos no NTFS.</span><span class="sxs-lookup"><span data-stu-id="82715-139">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="82715-140">12</span><span class="sxs-lookup"><span data-stu-id="82715-140">12</span></span>

<span data-ttu-id="82715-141">Plataforma no Windows.</span><span class="sxs-lookup"><span data-stu-id="82715-141">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="82715-142">13</span><span class="sxs-lookup"><span data-stu-id="82715-142">13</span></span>

<span data-ttu-id="82715-143">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="82715-143">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="82715-144">14</span><span class="sxs-lookup"><span data-stu-id="82715-144">14</span></span>

<span data-ttu-id="82715-145">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="82715-145">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="82715-146">15</span><span class="sxs-lookup"><span data-stu-id="82715-146">15</span></span>

<span data-ttu-id="82715-147">Infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="82715-147">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="82715-148">16</span><span class="sxs-lookup"><span data-stu-id="82715-148">16</span></span>

<span data-ttu-id="82715-149">Archivo de inicio no válido.</span><span class="sxs-lookup"><span data-stu-id="82715-149">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="82715-150">17</span><span class="sxs-lookup"><span data-stu-id="82715-150">17</span></span>

<span data-ttu-id="82715-151">Privilegio no mantenido.</span><span class="sxs-lookup"><span data-stu-id="82715-151">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="82715-152">21</span><span class="sxs-lookup"><span data-stu-id="82715-152">21</span></span>

<span data-ttu-id="82715-153">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="82715-153">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="82715-154">Observaciones</span><span class="sxs-lookup"><span data-stu-id="82715-154">Remarks</span></span>

<span data-ttu-id="82715-155">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="82715-155">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="82715-156">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="82715-156">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="82715-157">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="82715-157">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="82715-158">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="82715-158">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="82715-159">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82715-159">Requirements</span></span>



| <span data-ttu-id="82715-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="82715-160">Requirement</span></span> | <span data-ttu-id="82715-161">Value</span><span class="sxs-lookup"><span data-stu-id="82715-161">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="82715-162">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="82715-162">Minimum supported client</span></span><br/> | <span data-ttu-id="82715-163">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="82715-163">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="82715-164">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="82715-164">Minimum supported server</span></span><br/> | <span data-ttu-id="82715-165">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="82715-165">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="82715-166">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="82715-166">Namespace</span></span><br/>                | <span data-ttu-id="82715-167">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="82715-167">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="82715-168">MOF</span><span class="sxs-lookup"><span data-stu-id="82715-168">MOF</span></span><br/>                      | <dl> <span data-ttu-id="82715-169"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="82715-169"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="82715-170">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="82715-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82715-171"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82715-171"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82715-172">Vea también</span><span class="sxs-lookup"><span data-stu-id="82715-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82715-173">\_Directorio CIM</span><span class="sxs-lookup"><span data-stu-id="82715-173">CIM\_Directory</span></span>](copyex-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="82715-174">**\_Directorio CIM**</span><span class="sxs-lookup"><span data-stu-id="82715-174">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

