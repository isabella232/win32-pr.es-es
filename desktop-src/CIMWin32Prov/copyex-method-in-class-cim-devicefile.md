---
description: Copia el archivo de dispositivo lógico (o directorio) especificado en la ruta de acceso del objeto en la ubicación especificada por el parámetro FileName.
ms.assetid: 42cdb880-2431-4dcc-abdb-f271e2cd81a4
ms.tgt_platform: multiple
title: Método CopyEx de la clase CIM_DeviceFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.CopyEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0e9519155accadc1a41a1c91492755db90eec696
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423364"
---
# <a name="copyex-method-of-the-cim_devicefile-class"></a><span data-ttu-id="8f523-103">Método CopyEx de la \_ clase DeviceFile de CIM</span><span class="sxs-lookup"><span data-stu-id="8f523-103">CopyEx method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="8f523-104">El método **CopyEx** copia el archivo de dispositivo lógico (o directorio) especificado en la ruta de acceso del objeto en la ubicación especificada por el parámetro *filename* .</span><span class="sxs-lookup"><span data-stu-id="8f523-104">The **CopyEx** method copies the logical device file (or directory) specified in the object path to the location specified by the *FileName* parameter.</span></span> <span data-ttu-id="8f523-105">No se admite una copia si se requiere sobrescribir un archivo lógico existente.</span><span class="sxs-lookup"><span data-stu-id="8f523-105">A copy is not supported if overwriting an existing logical file is required.</span></span> <span data-ttu-id="8f523-106">Este método es una versión extendida del método de [**copia**](copy-method-in-class-cim-devicefile.md) .</span><span class="sxs-lookup"><span data-stu-id="8f523-106">This method is an extended version of the [**Copy**](copy-method-in-class-cim-devicefile.md) method.</span></span> <span data-ttu-id="8f523-107">Este método se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="8f523-107">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8f523-108">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="8f523-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8f523-109">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="8f523-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8f523-110">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="8f523-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="8f523-111">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="8f523-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="8f523-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8f523-112">Syntax</span></span>


```mof
uint32 CopyEx(
  [in]  string     FileName,
  [out] string REF StopFileName,
  [in]  string     StartFileName,
  [in]  boolean    Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="8f523-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8f523-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f523-114">*Nombre de archivo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8f523-114">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f523-115">Nombre completo del archivo de destino (o directorio).</span><span class="sxs-lookup"><span data-stu-id="8f523-115">Fully qualified name of the destination file (or directory).</span></span>

<span data-ttu-id="8f523-116">Ejemplo: "c: \\ temp \\ newdirectory"</span><span class="sxs-lookup"><span data-stu-id="8f523-116">Example: "c:\\temp\\newdirectory"</span></span>

</dd> <dt>

<span data-ttu-id="8f523-117">*StopFileName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8f523-117">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8f523-118">Cadena que representa el nombre del archivo (o directorio) donde se produjo un error en el método.</span><span class="sxs-lookup"><span data-stu-id="8f523-118">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="8f523-119">Este parámetro es **null** si el método se ejecuta correctamente.</span><span class="sxs-lookup"><span data-stu-id="8f523-119">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="8f523-120">*StartFileName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8f523-120">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f523-121">Cadena que representa el archivo secundario (o directorio) que se va a utilizar como punto de partida para este método.</span><span class="sxs-lookup"><span data-stu-id="8f523-121">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="8f523-122">Normalmente, el parámetro *StartFileName* es el parámetro *StopFileName* que especifica el archivo o directorio en el que se produjo un error de la llamada al método anterior.</span><span class="sxs-lookup"><span data-stu-id="8f523-122">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="8f523-123">Si este parámetro es **null**, la operación se realiza en el archivo (o directorio) especificado en la llamada [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="8f523-123">If this parameter is **null**, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="8f523-124">*Recursivo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8f523-124">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f523-125">Si es TRUE, el método también se aplica de forma recursiva a los archivos y directorios del directorio especificado por la instancia de [**\_ DeviceFile de CIM**](cim-devicefile.md) .</span><span class="sxs-lookup"><span data-stu-id="8f523-125">If TRUE, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_DeviceFile**](cim-devicefile.md) instance.</span></span> <span data-ttu-id="8f523-126">En el caso de las instancias de archivo, este parámetro se omite.</span><span class="sxs-lookup"><span data-stu-id="8f523-126">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f523-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8f523-127">Return value</span></span>

<span data-ttu-id="8f523-128">Devuelve un valor de 0 (cero) si se realiza correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="8f523-128">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="8f523-129">0</span><span class="sxs-lookup"><span data-stu-id="8f523-129">0</span></span>

<span data-ttu-id="8f523-130">Correcto.</span><span class="sxs-lookup"><span data-stu-id="8f523-130">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8f523-131">2</span><span class="sxs-lookup"><span data-stu-id="8f523-131">2</span></span>

<span data-ttu-id="8f523-132">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="8f523-132">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8f523-133">8</span><span class="sxs-lookup"><span data-stu-id="8f523-133">8</span></span>

<span data-ttu-id="8f523-134">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="8f523-134">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8f523-135">9</span><span class="sxs-lookup"><span data-stu-id="8f523-135">9</span></span>

<span data-ttu-id="8f523-136">Objeto no válido.</span><span class="sxs-lookup"><span data-stu-id="8f523-136">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8f523-137">10</span><span class="sxs-lookup"><span data-stu-id="8f523-137">10</span></span>

<span data-ttu-id="8f523-138">El objeto ya existe.</span><span class="sxs-lookup"><span data-stu-id="8f523-138">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8f523-139">11</span><span class="sxs-lookup"><span data-stu-id="8f523-139">11</span></span>

<span data-ttu-id="8f523-140">Sistema de archivos no NTFS.</span><span class="sxs-lookup"><span data-stu-id="8f523-140">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8f523-141">12</span><span class="sxs-lookup"><span data-stu-id="8f523-141">12</span></span>

<span data-ttu-id="8f523-142">Plataforma no Windows.</span><span class="sxs-lookup"><span data-stu-id="8f523-142">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8f523-143">13</span><span class="sxs-lookup"><span data-stu-id="8f523-143">13</span></span>

<span data-ttu-id="8f523-144">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="8f523-144">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8f523-145">14</span><span class="sxs-lookup"><span data-stu-id="8f523-145">14</span></span>

<span data-ttu-id="8f523-146">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="8f523-146">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8f523-147">15</span><span class="sxs-lookup"><span data-stu-id="8f523-147">15</span></span>

<span data-ttu-id="8f523-148">Infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="8f523-148">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8f523-149">16</span><span class="sxs-lookup"><span data-stu-id="8f523-149">16</span></span>

<span data-ttu-id="8f523-150">Archivo de inicio no válido.</span><span class="sxs-lookup"><span data-stu-id="8f523-150">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8f523-151">17</span><span class="sxs-lookup"><span data-stu-id="8f523-151">17</span></span>

<span data-ttu-id="8f523-152">Privilegio no mantenido.</span><span class="sxs-lookup"><span data-stu-id="8f523-152">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8f523-153">21</span><span class="sxs-lookup"><span data-stu-id="8f523-153">21</span></span>

<span data-ttu-id="8f523-154">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="8f523-154">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8f523-155">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8f523-155">Remarks</span></span>

<span data-ttu-id="8f523-156">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="8f523-156">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="8f523-157">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="8f523-157">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="8f523-158">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="8f523-158">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8f523-159">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="8f523-159">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f523-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f523-160">Requirements</span></span>



| <span data-ttu-id="8f523-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f523-161">Requirement</span></span> | <span data-ttu-id="8f523-162">Value</span><span class="sxs-lookup"><span data-stu-id="8f523-162">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f523-163">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8f523-163">Minimum supported client</span></span><br/> | <span data-ttu-id="8f523-164">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8f523-164">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8f523-165">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8f523-165">Minimum supported server</span></span><br/> | <span data-ttu-id="8f523-166">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8f523-166">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8f523-167">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8f523-167">Namespace</span></span><br/>                | <span data-ttu-id="8f523-168">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="8f523-168">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8f523-169">MOF</span><span class="sxs-lookup"><span data-stu-id="8f523-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8f523-170"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8f523-170"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8f523-171">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8f523-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f523-172"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f523-172"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f523-173">Vea también</span><span class="sxs-lookup"><span data-stu-id="8f523-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f523-174">\_DEVICEFILE CIM</span><span class="sxs-lookup"><span data-stu-id="8f523-174">CIM\_DeviceFile</span></span>](copyex-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="8f523-175">**\_DEVICEFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="8f523-175">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

