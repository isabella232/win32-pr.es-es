---
description: 'Método DeleteEx de la CIM_Directory : el método DeleteEx elimina el archivo lógico (o directorio) especificado en la ruta de acceso del objeto. Este método es una versión extendida del método Delete y se hereda de CIM \_ LogicalFile.'
ms.assetid: 5f924327-248c-47e2-b42e-50c83defce17
ms.tgt_platform: multiple
title: Método DeleteEx de la CIM_Directory clase
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
ms.openlocfilehash: 4a3704507405ebb2d310ed7341cd1db174e00588
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097103"
---
# <a name="deleteex-method-of-the-cim_directory-class"></a><span data-ttu-id="c68ea-104">Método DeleteEx de la clase \_ De directorio CIM</span><span class="sxs-lookup"><span data-stu-id="c68ea-104">DeleteEx method of the CIM\_Directory class</span></span>

<span data-ttu-id="c68ea-105">El **método DeleteEx** elimina el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="c68ea-105">The **DeleteEx** method deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="c68ea-106">Este método es una versión extendida del [**método Delete**](delete-method-in-class-cim-directory.md) y se hereda de [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="c68ea-106">This method is an extended version of the [**Delete**](delete-method-in-class-cim-directory.md) method and is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c68ea-107">Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se construyen las clases WMI.</span><span class="sxs-lookup"><span data-stu-id="c68ea-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c68ea-108">WMI admite actualmente solo los esquemas [de versión CIM 2.x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c68ea-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c68ea-109">En este tema se usa Managed Object Format sintaxis MOF .</span><span class="sxs-lookup"><span data-stu-id="c68ea-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="c68ea-110">Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="c68ea-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="c68ea-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c68ea-111">Syntax</span></span>


```mof
uint32 DeleteEx(
  [out] string REF StopFileName,
  [in]  string     StartFileName
);
```



## <a name="parameters"></a><span data-ttu-id="c68ea-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c68ea-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c68ea-113">*StopFileName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c68ea-113">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c68ea-114">Cadena que representa el nombre del archivo (o directorio) en el que se ha fallado el método.</span><span class="sxs-lookup"><span data-stu-id="c68ea-114">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="c68ea-115">Este parámetro es NULL si el método se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="c68ea-115">This parameter is null if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="c68ea-116">*StartFileName* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="c68ea-116">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c68ea-117">Cadena que representa el archivo secundario (o directorio) que se va a usar como punto de partida para este método.</span><span class="sxs-lookup"><span data-stu-id="c68ea-117">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="c68ea-118">Normalmente, este parámetro es el *parámetro StopFileName* que especifica el archivo o directorio en el que se produjo un error de la llamada al método anterior.</span><span class="sxs-lookup"><span data-stu-id="c68ea-118">Typically, this parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="c68ea-119">Si este parámetro es NULL, la operación se realiza en el archivo (o directorio) especificado en la [**llamada a ExecMethod.**](/windows/desktop/WmiSdk/swbemservices-execmethod)</span><span class="sxs-lookup"><span data-stu-id="c68ea-119">If this parameter is null, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c68ea-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c68ea-120">Return value</span></span>

<span data-ttu-id="c68ea-121">Devuelve un valor de 0 (cero) si se ejecuta correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="c68ea-121">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="c68ea-122">0</span><span class="sxs-lookup"><span data-stu-id="c68ea-122">0</span></span>

<span data-ttu-id="c68ea-123">Correcto.</span><span class="sxs-lookup"><span data-stu-id="c68ea-123">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="c68ea-124">2</span><span class="sxs-lookup"><span data-stu-id="c68ea-124">2</span></span>

<span data-ttu-id="c68ea-125">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="c68ea-125">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="c68ea-126">8</span><span class="sxs-lookup"><span data-stu-id="c68ea-126">8</span></span>

<span data-ttu-id="c68ea-127">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="c68ea-127">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="c68ea-128">9</span><span class="sxs-lookup"><span data-stu-id="c68ea-128">9</span></span>

<span data-ttu-id="c68ea-129">Objeto no válido.</span><span class="sxs-lookup"><span data-stu-id="c68ea-129">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="c68ea-130">10</span><span class="sxs-lookup"><span data-stu-id="c68ea-130">10</span></span>

<span data-ttu-id="c68ea-131">El objeto ya existe.</span><span class="sxs-lookup"><span data-stu-id="c68ea-131">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="c68ea-132">11</span><span class="sxs-lookup"><span data-stu-id="c68ea-132">11</span></span>

<span data-ttu-id="c68ea-133">Sistema de archivos no NTFS.</span><span class="sxs-lookup"><span data-stu-id="c68ea-133">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="c68ea-134">12</span><span class="sxs-lookup"><span data-stu-id="c68ea-134">12</span></span>

<span data-ttu-id="c68ea-135">Plataforma no Windows.</span><span class="sxs-lookup"><span data-stu-id="c68ea-135">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="c68ea-136">13</span><span class="sxs-lookup"><span data-stu-id="c68ea-136">13</span></span>

<span data-ttu-id="c68ea-137">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="c68ea-137">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="c68ea-138">14</span><span class="sxs-lookup"><span data-stu-id="c68ea-138">14</span></span>

<span data-ttu-id="c68ea-139">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="c68ea-139">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="c68ea-140">15</span><span class="sxs-lookup"><span data-stu-id="c68ea-140">15</span></span>

<span data-ttu-id="c68ea-141">Infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="c68ea-141">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="c68ea-142">16</span><span class="sxs-lookup"><span data-stu-id="c68ea-142">16</span></span>

<span data-ttu-id="c68ea-143">Archivo de inicio no válido.</span><span class="sxs-lookup"><span data-stu-id="c68ea-143">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="c68ea-144">17</span><span class="sxs-lookup"><span data-stu-id="c68ea-144">17</span></span>

<span data-ttu-id="c68ea-145">Privilegio no mantenido.</span><span class="sxs-lookup"><span data-stu-id="c68ea-145">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="c68ea-146">21</span><span class="sxs-lookup"><span data-stu-id="c68ea-146">21</span></span>

<span data-ttu-id="c68ea-147">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="c68ea-147">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c68ea-148">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c68ea-148">Remarks</span></span>

<span data-ttu-id="c68ea-149">Wmi no implementa actualmente este método.</span><span class="sxs-lookup"><span data-stu-id="c68ea-149">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="c68ea-150">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="c68ea-150">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="c68ea-151">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="c68ea-151">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c68ea-152">Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="c68ea-152">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c68ea-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c68ea-153">Requirements</span></span>



| <span data-ttu-id="c68ea-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="c68ea-154">Requirement</span></span> | <span data-ttu-id="c68ea-155">Valor</span><span class="sxs-lookup"><span data-stu-id="c68ea-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c68ea-156">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c68ea-156">Minimum supported client</span></span><br/> | <span data-ttu-id="c68ea-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c68ea-157">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c68ea-158">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c68ea-158">Minimum supported server</span></span><br/> | <span data-ttu-id="c68ea-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c68ea-159">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c68ea-160">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c68ea-160">Namespace</span></span><br/>                | <span data-ttu-id="c68ea-161">\\CIMV2 raíz</span><span class="sxs-lookup"><span data-stu-id="c68ea-161">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c68ea-162">MOF</span><span class="sxs-lookup"><span data-stu-id="c68ea-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c68ea-163"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="c68ea-163"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c68ea-164">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c68ea-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c68ea-165"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c68ea-165"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c68ea-166">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c68ea-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c68ea-167">Directorio \_ CIM</span><span class="sxs-lookup"><span data-stu-id="c68ea-167">CIM\_Directory</span></span>](deleteex-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="c68ea-168">**Directorio \_ CIM**</span><span class="sxs-lookup"><span data-stu-id="c68ea-168">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

