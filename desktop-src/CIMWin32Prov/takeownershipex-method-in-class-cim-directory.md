---
description: Obtiene la propiedad del archivo de entrada de directorio lógico especificado en la ruta de acceso del objeto. Este método es una versión extendida del método TakeOwnerShip y se hereda de \_ LOGICALFILE CIM.
ms.assetid: a13acaa2-2203-470a-b989-15f8276e46c6
ms.tgt_platform: multiple
title: Método TakeOwnerShipEx de la clase CIM_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.TakeOwnerShipEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: b02a6c40e99405c150a372f8eb15fe648f2df60a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152830"
---
# <a name="takeownershipex-method-of-the-cim_directory-class"></a><span data-ttu-id="4872b-104">Método TakeOwnerShipEx de la \_ clase de directorio CIM</span><span class="sxs-lookup"><span data-stu-id="4872b-104">TakeOwnerShipEx method of the CIM\_Directory class</span></span>

<span data-ttu-id="4872b-105">El método **TakeOwnerShipEx** obtiene la propiedad del archivo de entrada de directorio lógico especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="4872b-105">The **TakeOwnerShipEx** method obtains ownership of the logical directory entry file specified in the object path.</span></span> <span data-ttu-id="4872b-106">Este método es una versión extendida del método [**TakeOwnerShip**](takeownership-method-in-class-cim-directory.md) y se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="4872b-106">This method is an extended version of the [**TakeOwnerShip**](takeownership-method-in-class-cim-directory.md) method and is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span> <span data-ttu-id="4872b-107">Si el archivo lógico es un directorio, este método actúa de forma recursiva y toma la propiedad de todos los archivos y subdirectorios que contiene el directorio.</span><span class="sxs-lookup"><span data-stu-id="4872b-107">If the logical file is a directory, then this method acts recursively, taking ownership of all of the files and sub-directories that the directory contains.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4872b-108">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="4872b-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4872b-109">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4872b-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4872b-110">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="4872b-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="4872b-111">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="4872b-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="4872b-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4872b-112">Syntax</span></span>


```mof
uint32 TakeOwnerShipEx(
  [out] string REF StopFileName,
  [in]  string     StartFileName,
  [in]  boolean    Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="4872b-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4872b-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4872b-114">*StopFileName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4872b-114">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4872b-115">Cadena que representa el nombre del archivo (o directorio) donde se produjo un error en el método.</span><span class="sxs-lookup"><span data-stu-id="4872b-115">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="4872b-116">Este parámetro es NULL si el método se ejecuta correctamente.</span><span class="sxs-lookup"><span data-stu-id="4872b-116">This parameter is null if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="4872b-117">*StartFileName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4872b-117">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4872b-118">Cadena que representa el archivo secundario (o directorio) que se va a utilizar como punto de partida para este método.</span><span class="sxs-lookup"><span data-stu-id="4872b-118">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="4872b-119">Normalmente, este parámetro es el parámetro *StopFileName* que especifica el archivo o directorio en el que se produjo un error de la llamada al método anterior.</span><span class="sxs-lookup"><span data-stu-id="4872b-119">Typically, this parameter is the *StopFileName* parameter that specifies the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="4872b-120">Si este parámetro es null, la operación se realiza en el archivo (o directorio) especificado en la llamada [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="4872b-120">If this parameter is null, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="4872b-121">*Recursivo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4872b-121">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4872b-122">Si es **true**, el método se aplica de forma recursiva a los archivos y directorios del directorio especificado por la instancia de [**\_ directorio CIM**](cim-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="4872b-122">If **True**, the method is applied recursively to files and directories within the directory specified by the [**CIM\_Directory**](cim-directory.md) instance.</span></span> <span data-ttu-id="4872b-123">En el caso de las instancias de archivo, este parámetro se omite.</span><span class="sxs-lookup"><span data-stu-id="4872b-123">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4872b-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4872b-124">Return value</span></span>

<span data-ttu-id="4872b-125">Devuelve un valor de 0 si se ejecuta correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="4872b-125">Returns a value of 0 on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="4872b-126">0</span><span class="sxs-lookup"><span data-stu-id="4872b-126">0</span></span>

<span data-ttu-id="4872b-127">Correcto.</span><span class="sxs-lookup"><span data-stu-id="4872b-127">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="4872b-128">2</span><span class="sxs-lookup"><span data-stu-id="4872b-128">2</span></span>

<span data-ttu-id="4872b-129">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="4872b-129">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="4872b-130">8</span><span class="sxs-lookup"><span data-stu-id="4872b-130">8</span></span>

<span data-ttu-id="4872b-131">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="4872b-131">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="4872b-132">9</span><span class="sxs-lookup"><span data-stu-id="4872b-132">9</span></span>

<span data-ttu-id="4872b-133">Objeto no válido.</span><span class="sxs-lookup"><span data-stu-id="4872b-133">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="4872b-134">10</span><span class="sxs-lookup"><span data-stu-id="4872b-134">10</span></span>

<span data-ttu-id="4872b-135">El objeto ya existe.</span><span class="sxs-lookup"><span data-stu-id="4872b-135">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="4872b-136">11</span><span class="sxs-lookup"><span data-stu-id="4872b-136">11</span></span>

<span data-ttu-id="4872b-137">Sistema de archivos no NTFS.</span><span class="sxs-lookup"><span data-stu-id="4872b-137">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="4872b-138">12</span><span class="sxs-lookup"><span data-stu-id="4872b-138">12</span></span>

<span data-ttu-id="4872b-139">La plataforma no es Windows.</span><span class="sxs-lookup"><span data-stu-id="4872b-139">The platform is not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="4872b-140">13</span><span class="sxs-lookup"><span data-stu-id="4872b-140">13</span></span>

<span data-ttu-id="4872b-141">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="4872b-141">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="4872b-142">14</span><span class="sxs-lookup"><span data-stu-id="4872b-142">14</span></span>

<span data-ttu-id="4872b-143">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="4872b-143">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="4872b-144">15</span><span class="sxs-lookup"><span data-stu-id="4872b-144">15</span></span>

<span data-ttu-id="4872b-145">Infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="4872b-145">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="4872b-146">16</span><span class="sxs-lookup"><span data-stu-id="4872b-146">16</span></span>

<span data-ttu-id="4872b-147">Archivo de inicio no válido.</span><span class="sxs-lookup"><span data-stu-id="4872b-147">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="4872b-148">17</span><span class="sxs-lookup"><span data-stu-id="4872b-148">17</span></span>

<span data-ttu-id="4872b-149">Privilegio no mantenido.</span><span class="sxs-lookup"><span data-stu-id="4872b-149">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="4872b-150">21</span><span class="sxs-lookup"><span data-stu-id="4872b-150">21</span></span>

<span data-ttu-id="4872b-151">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="4872b-151">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4872b-152">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4872b-152">Remarks</span></span>

<span data-ttu-id="4872b-153">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="4872b-153">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="4872b-154">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="4872b-154">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="4872b-155">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="4872b-155">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4872b-156">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="4872b-156">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="examples"></a><span data-ttu-id="4872b-157">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="4872b-157">Examples</span></span>

<span data-ttu-id="4872b-158">El siguiente código de script de Visual Basic llama al método **TakeOwnerShipEx** para tomar posesión de la \\ carpeta C: Temp.</span><span class="sxs-lookup"><span data-stu-id="4872b-158">The following Visual Basic Script code calls the **TakeOwnerShipEx** method to take ownership of the C:\\temp folder.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject( _
    "winmgmts:\\" & strComputer & "\root\CIMV2") 
' Obtain the definition of the class.
Set objShare = objWMIService.Get("Win32_Directory")
' Obtain an InParameters object specific
' to the method.
Set objInParam = objShare.Methods_("TakeOwnerShipEx"). _
    inParameters.SpawnInstance_()

' Add the input parameters.
objInParam.Properties_.Item("Recursive") =  true

' Execute the method and obtain the return status.
' The OutParameters object in objOutParams
' is created by the provider.
Set objOutParams = objWMIService.ExecMethod( _
    "Win32_Directory.Name='C:\Temp'", "TakeOwnerShipEx", objInParam)
wscript.echo objOutParams.ReturnValue
```



## <a name="requirements"></a><span data-ttu-id="4872b-159">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4872b-159">Requirements</span></span>



| <span data-ttu-id="4872b-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="4872b-160">Requirement</span></span> | <span data-ttu-id="4872b-161">Value</span><span class="sxs-lookup"><span data-stu-id="4872b-161">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4872b-162">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4872b-162">Minimum supported client</span></span><br/> | <span data-ttu-id="4872b-163">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4872b-163">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4872b-164">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4872b-164">Minimum supported server</span></span><br/> | <span data-ttu-id="4872b-165">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4872b-165">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4872b-166">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4872b-166">Namespace</span></span><br/>                | <span data-ttu-id="4872b-167">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="4872b-167">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4872b-168">MOF</span><span class="sxs-lookup"><span data-stu-id="4872b-168">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4872b-169"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4872b-169"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4872b-170">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4872b-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4872b-171"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4872b-171"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4872b-172">Vea también</span><span class="sxs-lookup"><span data-stu-id="4872b-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4872b-173">\_Directorio CIM</span><span class="sxs-lookup"><span data-stu-id="4872b-173">CIM\_Directory</span></span>](takeownershipex-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="4872b-174">**\_Directorio CIM**</span><span class="sxs-lookup"><span data-stu-id="4872b-174">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

