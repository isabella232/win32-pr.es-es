---
description: El método CompressEx comprime el archivo lógico (o directorio) especificado en la ruta de acceso del objeto. Este método es una versión extendida del método compress y se hereda de CIM \_ LogicalFile.
ms.assetid: 82a28a3b-b2e4-4834-b4a5-02ffe94f3fc7
ms.tgt_platform: multiple
title: Método CompressEx de la clase CIM_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.CompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8bebd729d87e012c3fce6dd2eb87b1c61ffa423a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538476"
---
# <a name="compressex-method-of-the-cim_directory-class"></a><span data-ttu-id="99ef4-104">Método CompressEx de la \_ clase de directorio CIM</span><span class="sxs-lookup"><span data-stu-id="99ef4-104">CompressEx method of the CIM\_Directory class</span></span>

<span data-ttu-id="99ef4-105">El método **CompressEx** comprime el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="99ef4-105">The **CompressEx** method compresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="99ef4-106">Este método es una versión extendida del método [**compress**](compress-method-in-class-cim-directory.md) y se hereda de [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="99ef4-106">This method is an extended version of the [**Compress**](compress-method-in-class-cim-directory.md) method and is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="99ef4-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="99ef4-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="99ef4-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="99ef4-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="99ef4-109">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="99ef4-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="99ef4-110">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="99ef4-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="99ef4-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="99ef4-111">Syntax</span></span>


```mof
uint32 CompressEx(
  [out] string REF StopFileName,
  [in]  string     StartFileName,
  [in]  boolean    Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="99ef4-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="99ef4-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99ef4-113">*StopFileName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="99ef4-113">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="99ef4-114">Cadena que representa el nombre del archivo (o directorio) donde se produjo un error en el método.</span><span class="sxs-lookup"><span data-stu-id="99ef4-114">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="99ef4-115">Este parámetro es NULL si el método se ejecuta correctamente.</span><span class="sxs-lookup"><span data-stu-id="99ef4-115">This parameter is null if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="99ef4-116">*StartFileName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="99ef4-116">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99ef4-117">Cadena que representa el archivo secundario (o directorio) que se va a utilizar como punto de partida para este método.</span><span class="sxs-lookup"><span data-stu-id="99ef4-117">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="99ef4-118">Normalmente, este parámetro es el parámetro *StopFileName* que especifica el archivo o directorio en el que se produjo un error de la llamada al método anterior.</span><span class="sxs-lookup"><span data-stu-id="99ef4-118">Typically, this parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="99ef4-119">Si este parámetro es null, la operación se realiza en el archivo (o directorio) especificado en la llamada [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="99ef4-119">If this parameter is null, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="99ef4-120">*Recursivo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="99ef4-120">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99ef4-121">Si es **true**, el método también se aplica de forma recursiva a los archivos y directorios del directorio especificado por la instancia de [**\_ directorio CIM**](cim-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="99ef4-121">If **TRUE**, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_Directory**](cim-directory.md) instance.</span></span> <span data-ttu-id="99ef4-122">En el caso de las instancias de archivo, este parámetro se omite.</span><span class="sxs-lookup"><span data-stu-id="99ef4-122">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99ef4-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="99ef4-123">Return value</span></span>

<span data-ttu-id="99ef4-124">Devuelve un valor de 0 (cero) si se realiza correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="99ef4-124">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="99ef4-125">0</span><span class="sxs-lookup"><span data-stu-id="99ef4-125">0</span></span>

<span data-ttu-id="99ef4-126">Correcto.</span><span class="sxs-lookup"><span data-stu-id="99ef4-126">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="99ef4-127">2</span><span class="sxs-lookup"><span data-stu-id="99ef4-127">2</span></span>

<span data-ttu-id="99ef4-128">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="99ef4-128">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="99ef4-129">8</span><span class="sxs-lookup"><span data-stu-id="99ef4-129">8</span></span>

<span data-ttu-id="99ef4-130">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="99ef4-130">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="99ef4-131">9</span><span class="sxs-lookup"><span data-stu-id="99ef4-131">9</span></span>

<span data-ttu-id="99ef4-132">Objeto no válido.</span><span class="sxs-lookup"><span data-stu-id="99ef4-132">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="99ef4-133">10</span><span class="sxs-lookup"><span data-stu-id="99ef4-133">10</span></span>

<span data-ttu-id="99ef4-134">El objeto ya existe.</span><span class="sxs-lookup"><span data-stu-id="99ef4-134">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="99ef4-135">11</span><span class="sxs-lookup"><span data-stu-id="99ef4-135">11</span></span>

<span data-ttu-id="99ef4-136">Sistema de archivos no NTFS.</span><span class="sxs-lookup"><span data-stu-id="99ef4-136">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="99ef4-137">12</span><span class="sxs-lookup"><span data-stu-id="99ef4-137">12</span></span>

<span data-ttu-id="99ef4-138">Plataforma no Windows.</span><span class="sxs-lookup"><span data-stu-id="99ef4-138">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="99ef4-139">13</span><span class="sxs-lookup"><span data-stu-id="99ef4-139">13</span></span>

<span data-ttu-id="99ef4-140">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="99ef4-140">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="99ef4-141">14</span><span class="sxs-lookup"><span data-stu-id="99ef4-141">14</span></span>

<span data-ttu-id="99ef4-142">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="99ef4-142">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="99ef4-143">15</span><span class="sxs-lookup"><span data-stu-id="99ef4-143">15</span></span>

<span data-ttu-id="99ef4-144">Infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="99ef4-144">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="99ef4-145">16</span><span class="sxs-lookup"><span data-stu-id="99ef4-145">16</span></span>

<span data-ttu-id="99ef4-146">Archivo de inicio no válido.</span><span class="sxs-lookup"><span data-stu-id="99ef4-146">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="99ef4-147">17</span><span class="sxs-lookup"><span data-stu-id="99ef4-147">17</span></span>

<span data-ttu-id="99ef4-148">Privilegio no mantenido.</span><span class="sxs-lookup"><span data-stu-id="99ef4-148">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="99ef4-149">21</span><span class="sxs-lookup"><span data-stu-id="99ef4-149">21</span></span>

<span data-ttu-id="99ef4-150">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="99ef4-150">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="99ef4-151">Observaciones</span><span class="sxs-lookup"><span data-stu-id="99ef4-151">Remarks</span></span>

<span data-ttu-id="99ef4-152">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="99ef4-152">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="99ef4-153">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="99ef4-153">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="99ef4-154">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="99ef4-154">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="99ef4-155">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="99ef4-155">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="99ef4-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99ef4-156">Requirements</span></span>



| <span data-ttu-id="99ef4-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="99ef4-157">Requirement</span></span> | <span data-ttu-id="99ef4-158">Value</span><span class="sxs-lookup"><span data-stu-id="99ef4-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="99ef4-159">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="99ef4-159">Minimum supported client</span></span><br/> | <span data-ttu-id="99ef4-160">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="99ef4-160">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="99ef4-161">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="99ef4-161">Minimum supported server</span></span><br/> | <span data-ttu-id="99ef4-162">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="99ef4-162">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="99ef4-163">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="99ef4-163">Namespace</span></span><br/>                | <span data-ttu-id="99ef4-164">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="99ef4-164">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="99ef4-165">MOF</span><span class="sxs-lookup"><span data-stu-id="99ef4-165">MOF</span></span><br/>                      | <dl> <span data-ttu-id="99ef4-166"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="99ef4-166"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="99ef4-167">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="99ef4-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99ef4-168"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99ef4-168"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99ef4-169">Vea también</span><span class="sxs-lookup"><span data-stu-id="99ef4-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99ef4-170">\_Directorio CIM</span><span class="sxs-lookup"><span data-stu-id="99ef4-170">CIM\_Directory</span></span>](compressex-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="99ef4-171">**\_Directorio CIM**</span><span class="sxs-lookup"><span data-stu-id="99ef4-171">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

