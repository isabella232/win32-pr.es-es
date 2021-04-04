---
description: El método DeleteEx elimina el archivo lógico (o directorio) especificado en la ruta de acceso del objeto. Este método es una versión extendida del método Delete y se hereda de CIM \_ LogicalFile.
ms.assetid: 5f924327-248c-47e2-b42e-50c83defce17
ms.tgt_platform: multiple
title: Método DeleteEx de la clase CIM_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.DeleteEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: aa6427adcc2cf87923b2b76b298cc47373231b56
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998241"
---
# <a name="deleteex-method-of-the-cim_directory-class"></a><span data-ttu-id="10f78-104">Método DeleteEx de la \_ clase de directorio CIM</span><span class="sxs-lookup"><span data-stu-id="10f78-104">DeleteEx method of the CIM\_Directory class</span></span>

<span data-ttu-id="10f78-105">El método **DeleteEx** elimina el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="10f78-105">The **DeleteEx** method deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="10f78-106">Este método es una versión extendida del método [**Delete**](delete-method-in-class-cim-directory.md) y se hereda de [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="10f78-106">This method is an extended version of the [**Delete**](delete-method-in-class-cim-directory.md) method and is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="10f78-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="10f78-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="10f78-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="10f78-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="10f78-109">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="10f78-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="10f78-110">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="10f78-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="10f78-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="10f78-111">Syntax</span></span>


```mof
uint32 DeleteEx(
  [out] string REF StopFileName,
  [in]  string     StartFileName
);
```



## <a name="parameters"></a><span data-ttu-id="10f78-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="10f78-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10f78-113">*StopFileName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="10f78-113">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="10f78-114">Cadena que representa el nombre del archivo (o directorio) donde se produjo un error en el método.</span><span class="sxs-lookup"><span data-stu-id="10f78-114">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="10f78-115">Este parámetro es NULL si el método se ejecuta correctamente.</span><span class="sxs-lookup"><span data-stu-id="10f78-115">This parameter is null if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="10f78-116">*StartFileName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="10f78-116">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10f78-117">Cadena que representa el archivo secundario (o directorio) que se va a utilizar como punto de partida para este método.</span><span class="sxs-lookup"><span data-stu-id="10f78-117">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="10f78-118">Normalmente, este parámetro es el parámetro *StopFileName* que especifica el archivo o directorio en el que se produjo un error de la llamada al método anterior.</span><span class="sxs-lookup"><span data-stu-id="10f78-118">Typically, this parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="10f78-119">Si este parámetro es null, la operación se realiza en el archivo (o directorio) especificado en la llamada [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="10f78-119">If this parameter is null, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10f78-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="10f78-120">Return value</span></span>

<span data-ttu-id="10f78-121">Devuelve un valor de 0 (cero) si se realiza correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="10f78-121">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="10f78-122">0</span><span class="sxs-lookup"><span data-stu-id="10f78-122">0</span></span>

<span data-ttu-id="10f78-123">Correcto.</span><span class="sxs-lookup"><span data-stu-id="10f78-123">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="10f78-124">2</span><span class="sxs-lookup"><span data-stu-id="10f78-124">2</span></span>

<span data-ttu-id="10f78-125">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="10f78-125">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="10f78-126">8</span><span class="sxs-lookup"><span data-stu-id="10f78-126">8</span></span>

<span data-ttu-id="10f78-127">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="10f78-127">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="10f78-128">9</span><span class="sxs-lookup"><span data-stu-id="10f78-128">9</span></span>

<span data-ttu-id="10f78-129">Objeto no válido.</span><span class="sxs-lookup"><span data-stu-id="10f78-129">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="10f78-130">10</span><span class="sxs-lookup"><span data-stu-id="10f78-130">10</span></span>

<span data-ttu-id="10f78-131">El objeto ya existe.</span><span class="sxs-lookup"><span data-stu-id="10f78-131">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="10f78-132">11</span><span class="sxs-lookup"><span data-stu-id="10f78-132">11</span></span>

<span data-ttu-id="10f78-133">Sistema de archivos no NTFS.</span><span class="sxs-lookup"><span data-stu-id="10f78-133">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="10f78-134">12</span><span class="sxs-lookup"><span data-stu-id="10f78-134">12</span></span>

<span data-ttu-id="10f78-135">Plataforma no Windows.</span><span class="sxs-lookup"><span data-stu-id="10f78-135">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="10f78-136">13</span><span class="sxs-lookup"><span data-stu-id="10f78-136">13</span></span>

<span data-ttu-id="10f78-137">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="10f78-137">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="10f78-138">14</span><span class="sxs-lookup"><span data-stu-id="10f78-138">14</span></span>

<span data-ttu-id="10f78-139">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="10f78-139">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="10f78-140">15</span><span class="sxs-lookup"><span data-stu-id="10f78-140">15</span></span>

<span data-ttu-id="10f78-141">Infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="10f78-141">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="10f78-142">16</span><span class="sxs-lookup"><span data-stu-id="10f78-142">16</span></span>

<span data-ttu-id="10f78-143">Archivo de inicio no válido.</span><span class="sxs-lookup"><span data-stu-id="10f78-143">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="10f78-144">17</span><span class="sxs-lookup"><span data-stu-id="10f78-144">17</span></span>

<span data-ttu-id="10f78-145">Privilegio no mantenido.</span><span class="sxs-lookup"><span data-stu-id="10f78-145">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="10f78-146">21</span><span class="sxs-lookup"><span data-stu-id="10f78-146">21</span></span>

<span data-ttu-id="10f78-147">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="10f78-147">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="10f78-148">Observaciones</span><span class="sxs-lookup"><span data-stu-id="10f78-148">Remarks</span></span>

<span data-ttu-id="10f78-149">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="10f78-149">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="10f78-150">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="10f78-150">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="10f78-151">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="10f78-151">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="10f78-152">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="10f78-152">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="10f78-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10f78-153">Requirements</span></span>



| <span data-ttu-id="10f78-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="10f78-154">Requirement</span></span> | <span data-ttu-id="10f78-155">Value</span><span class="sxs-lookup"><span data-stu-id="10f78-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="10f78-156">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="10f78-156">Minimum supported client</span></span><br/> | <span data-ttu-id="10f78-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="10f78-157">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="10f78-158">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="10f78-158">Minimum supported server</span></span><br/> | <span data-ttu-id="10f78-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="10f78-159">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="10f78-160">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="10f78-160">Namespace</span></span><br/>                | <span data-ttu-id="10f78-161">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="10f78-161">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="10f78-162">MOF</span><span class="sxs-lookup"><span data-stu-id="10f78-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="10f78-163"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="10f78-163"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="10f78-164">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="10f78-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10f78-165"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10f78-165"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10f78-166">Vea también</span><span class="sxs-lookup"><span data-stu-id="10f78-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10f78-167">\_Directorio CIM</span><span class="sxs-lookup"><span data-stu-id="10f78-167">CIM\_Directory</span></span>](deleteex-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="10f78-168">**\_Directorio CIM**</span><span class="sxs-lookup"><span data-stu-id="10f78-168">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

