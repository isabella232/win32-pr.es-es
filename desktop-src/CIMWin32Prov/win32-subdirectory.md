---
description: La \_ clase WMI de Asociación de subdirectorios de Win32 relaciona un directorio (carpeta) y uno de sus subdirectorios (subcarpetas).
ms.assetid: f0565b7b-d593-468b-96b1-3922428c61e1
ms.tgt_platform: multiple
title: Win32_SubDirectory (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SubDirectory
- Win32_SubDirectory.GroupComponent
- Win32_SubDirectory.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 046de6ad1e09874351b37d58f7277126e39e990a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153345"
---
# <a name="win32_subdirectory-class"></a><span data-ttu-id="6a70d-103">\_Clase de subdirectorio Win32</span><span class="sxs-lookup"><span data-stu-id="6a70d-103">Win32\_SubDirectory class</span></span>

<span data-ttu-id="6a70d-104">La [clase WMI](../wmisdk/retrieving-a-class.md) de Asociación de **\_ subdirectorios de Win32** relaciona un directorio (carpeta) y uno de sus subdirectorios (subcarpetas).</span><span class="sxs-lookup"><span data-stu-id="6a70d-104">The **Win32\_SubDirectory** association [WMI class](../wmisdk/retrieving-a-class.md) relates a directory (folder) and one of its subdirectories (subfolders).</span></span>

<span data-ttu-id="6a70d-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="6a70d-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="6a70d-106">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="6a70d-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a70d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6a70d-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{F25FE469-783E-11d2-90BF-0060081A46FD}"), AMENDMENT]
class Win32_SubDirectory : CIM_Component
{
  Win32_Directory REF GroupComponent;
  Win32_Directory REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="6a70d-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="6a70d-108">Members</span></span>

<span data-ttu-id="6a70d-109">La clase de **\_ subdirectorio Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="6a70d-109">The **Win32\_SubDirectory** class has these types of members:</span></span>

-   [<span data-ttu-id="6a70d-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6a70d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6a70d-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6a70d-111">Properties</span></span>

<span data-ttu-id="6a70d-112">La clase de **\_ subdirectorio Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="6a70d-112">The **Win32\_SubDirectory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6a70d-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="6a70d-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a70d-114">Tipo de datos **: \_ directorio Win32**</span><span class="sxs-lookup"><span data-stu-id="6a70d-114">Data type: **Win32\_Directory**</span></span>
</dt> <dt>

<span data-ttu-id="6a70d-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6a70d-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6a70d-116">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| directorio Win32 de WMI \_ ")</span><span class="sxs-lookup"><span data-stu-id="6a70d-116">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_Directory")</span></span>
</dt> </dl>

<span data-ttu-id="6a70d-117">Referencia a la instancia de que representa las propiedades del directorio primario (carpeta) en esta asociación.</span><span class="sxs-lookup"><span data-stu-id="6a70d-117">Reference to the instance representing the properties of the parent directory (folder) in this association.</span></span>

</dd> <dt>

<span data-ttu-id="6a70d-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="6a70d-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a70d-119">Tipo de datos **: \_ directorio Win32**</span><span class="sxs-lookup"><span data-stu-id="6a70d-119">Data type: **Win32\_Directory**</span></span>
</dt> <dt>

<span data-ttu-id="6a70d-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6a70d-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6a70d-121">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| directorio Win32 de WMI \_ ")</span><span class="sxs-lookup"><span data-stu-id="6a70d-121">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_Directory")</span></span>
</dt> </dl>

<span data-ttu-id="6a70d-122">Referencia a la instancia de que representa la parte de subdirectorio (subcarpeta) de la asociación.</span><span class="sxs-lookup"><span data-stu-id="6a70d-122">Reference to the instance representing the subdirectory (subfolder) part of the association.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6a70d-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6a70d-123">Remarks</span></span>

<span data-ttu-id="6a70d-124">La clase de **\_ subdirectorio Win32** se deriva [**del \_ componente CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="6a70d-124">The **Win32\_SubDirectory** class is derived from [**CIM\_Component**](cim-component.md).</span></span>

<span data-ttu-id="6a70d-125">Para devolver una colección de subcarpetas de una carpeta, cree una consulta de asociación que establezca *ResultRole* en *PartComponent*.</span><span class="sxs-lookup"><span data-stu-id="6a70d-125">To return a collection of subfolders for a folder, create an association query that sets the *ResultRole* to *PartComponent*.</span></span> <span data-ttu-id="6a70d-126">Esto indica que todos los elementos de la colección devuelta deben desempeñar el rol de un elemento PartComponent, o subcarpeta, del objeto Folder.</span><span class="sxs-lookup"><span data-stu-id="6a70d-126">This indicates that all the items in the returned collection must play the role of a PartComponent, or subfolder, of the folder object.</span></span> <span data-ttu-id="6a70d-127">Para devolver la carpeta principal de una carpeta, establezca *ResultRole* en *GroupComponent*.</span><span class="sxs-lookup"><span data-stu-id="6a70d-127">To return the parent folder for a folder, set the *ResultRole* to *GroupComponent*.</span></span>

<span data-ttu-id="6a70d-128">La clase de **\_ subdirectorio Win32** solo funciona en el nivel de sistema de archivos inmediatamente superior o inmediatamente inferior a la carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="6a70d-128">The **Win32\_SubDirectory** class works only on the file system level immediately above or immediately below the specified folder.</span></span>

## <a name="examples"></a><span data-ttu-id="6a70d-129">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="6a70d-129">Examples</span></span>

<span data-ttu-id="6a70d-130">En el siguiente ejemplo de VBScript se devuelve una lista de todas las subcarpetas de la carpeta C: \\ scripts.</span><span class="sxs-lookup"><span data-stu-id="6a70d-130">The following VBScript sample returns a list of all subfolders within the folder C:\\Scripts.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colSubfolders = objWMIService.ExecQuery _
 ("ASSOCIATORS OF {Win32_Directory.Name='c:\scripts'} " _
 & "WHERE AssocClass = Win32_Subdirectory " _
 & "ResultRole = PartComponent")
For Each objFolder in colSubfolders
 Wscript.Echo objFolder.Name
Next
```



## <a name="requirements"></a><span data-ttu-id="6a70d-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a70d-131">Requirements</span></span>



| <span data-ttu-id="6a70d-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a70d-132">Requirement</span></span> | <span data-ttu-id="6a70d-133">Value</span><span class="sxs-lookup"><span data-stu-id="6a70d-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6a70d-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6a70d-134">Minimum supported client</span></span><br/> | <span data-ttu-id="6a70d-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6a70d-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6a70d-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6a70d-136">Minimum supported server</span></span><br/> | <span data-ttu-id="6a70d-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6a70d-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6a70d-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6a70d-138">Namespace</span></span><br/>                | <span data-ttu-id="6a70d-139">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="6a70d-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6a70d-140">MOF</span><span class="sxs-lookup"><span data-stu-id="6a70d-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6a70d-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6a70d-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6a70d-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6a70d-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a70d-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a70d-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a70d-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="6a70d-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a70d-145">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="6a70d-145">**CIM\_Component**</span></span>](cim-component.md)
</dt> <dt>

[<span data-ttu-id="6a70d-146">Clases de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="6a70d-146">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
