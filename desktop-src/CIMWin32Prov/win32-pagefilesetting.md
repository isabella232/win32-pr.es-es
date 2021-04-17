---
description: Win32 \_ PageFileSetting&\# 8194; La clase WMI representa la configuración de un archivo de paginación.
ms.assetid: 22190ede-1db6-4d69-ae74-63d10977cc78
ms.tgt_platform: multiple
title: Win32_PageFileSetting (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFileSetting
- Win32_PageFileSetting.Caption
- Win32_PageFileSetting.Description
- Win32_PageFileSetting.SettingID
- Win32_PageFileSetting.InitialSize
- Win32_PageFileSetting.MaximumSize
- Win32_PageFileSetting.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b3ec2fa36e31cf9075f218f31d3063e3a298b8ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659696"
---
# <a name="win32_pagefilesetting-class"></a><span data-ttu-id="c3cff-103">\_Clase Win32 PageFileSetting</span><span class="sxs-lookup"><span data-stu-id="c3cff-103">Win32\_PageFileSetting class</span></span>

<span data-ttu-id="c3cff-104">La  [clase WMI](../wmisdk/retrieving-a-class.md) **\_ PageFileSetting de Win32** representa la configuración de un archivo de paginación.</span><span class="sxs-lookup"><span data-stu-id="c3cff-104">The **Win32\_PageFileSetting** [WMI class](../wmisdk/retrieving-a-class.md) represents the settings of a page file.</span></span> <span data-ttu-id="c3cff-105">La información contenida en los objetos de los que se ha creado una instancia de esta clase especifica los parámetros del archivo de paginación que se usan cuando se crea el archivo al iniciar el sistema.</span><span class="sxs-lookup"><span data-stu-id="c3cff-105">Information contained within objects instantiated from this class specify the page file parameters used when the file is created at system startup.</span></span> <span data-ttu-id="c3cff-106">Las propiedades de esta clase se pueden modificar y diferir hasta el inicio.</span><span class="sxs-lookup"><span data-stu-id="c3cff-106">The properties in this class can be modified and deferred until startup.</span></span> <span data-ttu-id="c3cff-107">Esta configuración es diferente del estado de tiempo de ejecución de un archivo de paginación expresado a través de la clase asociada [**Win32 \_ PageFileUsage**](win32-pagefileusage.md).</span><span class="sxs-lookup"><span data-stu-id="c3cff-107">These settings are different from the run-time state of a page file expressed through the associated class [**Win32\_PageFileUsage**](win32-pagefileusage.md).</span></span>

<span data-ttu-id="c3cff-108">Para crear una instancia de esta clase, habilite el privilegio **SeCreatePagefilePrivilege** .</span><span class="sxs-lookup"><span data-stu-id="c3cff-108">To create an instance of this class, enable the **SeCreatePagefilePrivilege** privilege.</span></span> <span data-ttu-id="c3cff-109">Para obtener más información, vea [**constantes de privilegios**](../wmisdk/privilege-constants.md) y [ejecutar operaciones con privilegios](../wmisdk/executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="c3cff-109">For more information, see [**Privilege Constants**](../wmisdk/privilege-constants.md) and [Executing Privileged Operations](../wmisdk/executing-privileged-operations.md).</span></span>

<span data-ttu-id="c3cff-110">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="c3cff-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="c3cff-111">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="c3cff-111">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3cff-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c3cff-112">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeCreatePagefilePrivilege"), UUID("{514A9270-C856-11D2-B364-00105A1f77A1}"), SupportsCreate, CreateBy("PutInstance"), SupportsDelete, DeleteBy("DeleteInstance"), SupportsUpdate, AMENDMENT]
class Win32_PageFileSetting : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  uint32 InitialSize;
  uint32 MaximumSize;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="c3cff-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="c3cff-113">Members</span></span>

<span data-ttu-id="c3cff-114">La **clase \_ PageFileSetting de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c3cff-114">The **Win32\_PageFileSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="c3cff-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c3cff-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c3cff-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c3cff-116">Properties</span></span>

<span data-ttu-id="c3cff-117">La **clase \_ PageFileSetting de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="c3cff-117">The **Win32\_PageFileSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c3cff-118">**Caption**</span><span class="sxs-lookup"><span data-stu-id="c3cff-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3cff-119">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c3cff-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3cff-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c3cff-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3cff-121">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="c3cff-121">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="c3cff-122">Breve descripción textual del objeto actual.</span><span class="sxs-lookup"><span data-stu-id="c3cff-122">Short textual description of the current object.</span></span>

<span data-ttu-id="c3cff-123">Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="c3cff-123">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="c3cff-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c3cff-124">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3cff-125">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c3cff-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3cff-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c3cff-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3cff-127">Descripción textual del objeto actual.</span><span class="sxs-lookup"><span data-stu-id="c3cff-127">Textual description of the current object.</span></span>

<span data-ttu-id="c3cff-128">Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="c3cff-128">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="c3cff-129">**InitialSize**</span><span class="sxs-lookup"><span data-stu-id="c3cff-129">**InitialSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3cff-130">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c3cff-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c3cff-131">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c3cff-131">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c3cff-132">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ Session Manager \\ \\ Administración \| de memoria PagingFiles"), [**unidades**](../wmisdk/standard-qualifiers.md) ("megabytes")</span><span class="sxs-lookup"><span data-stu-id="c3cff-132">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\Session Manager\\\\Memory Management\|PagingFiles"), [**Units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="c3cff-133">Tamaño inicial del archivo de paginación.</span><span class="sxs-lookup"><span data-stu-id="c3cff-133">Initial size of the page file.</span></span>

<span data-ttu-id="c3cff-134">Ejemplo: 139</span><span class="sxs-lookup"><span data-stu-id="c3cff-134">Example: 139</span></span>

</dd> <dt>

<span data-ttu-id="c3cff-135">**Tamañomáximo**</span><span class="sxs-lookup"><span data-stu-id="c3cff-135">**MaximumSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3cff-136">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c3cff-136">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c3cff-137">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c3cff-137">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c3cff-138">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ Session Manager \\ \\ Administración \| de memoria PagingFiles"), [**unidades**](../wmisdk/standard-qualifiers.md) ("megabytes")</span><span class="sxs-lookup"><span data-stu-id="c3cff-138">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\Session Manager\\\\Memory Management\|PagingFiles"), [**Units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="c3cff-139">Tamaño máximo del archivo de paginación.</span><span class="sxs-lookup"><span data-stu-id="c3cff-139">Maximum size of the page file.</span></span>

<span data-ttu-id="c3cff-140">Ejemplo: 178</span><span class="sxs-lookup"><span data-stu-id="c3cff-140">Example: 178</span></span>

</dd> <dt>

<span data-ttu-id="c3cff-141">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="c3cff-141">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3cff-142">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c3cff-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3cff-143">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c3cff-143">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c3cff-144">Calificadores: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="c3cff-144">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="c3cff-145">Ruta de acceso y nombre de archivo del archivo de paginación.</span><span class="sxs-lookup"><span data-stu-id="c3cff-145">Path and file name of the page file.</span></span>

<span data-ttu-id="c3cff-146">Ejemplo: "C: \\PAGEFILE.SYS"</span><span class="sxs-lookup"><span data-stu-id="c3cff-146">Example: "C:\\PAGEFILE.SYS"</span></span>

</dd> <dt>

<span data-ttu-id="c3cff-147">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="c3cff-147">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3cff-148">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c3cff-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3cff-149">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c3cff-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3cff-150">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="c3cff-150">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="c3cff-151">Identificador por el que se conoce el objeto actual.</span><span class="sxs-lookup"><span data-stu-id="c3cff-151">Identifier by which the current object is known.</span></span>

<span data-ttu-id="c3cff-152">Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="c3cff-152">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c3cff-153">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c3cff-153">Remarks</span></span>

<span data-ttu-id="c3cff-154">La **clase \_ PageFileSetting de Win32** se deriva de la [**\_ configuración de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="c3cff-154">The **Win32\_PageFileSetting** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c3cff-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3cff-155">Requirements</span></span>



| <span data-ttu-id="c3cff-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3cff-156">Requirement</span></span> | <span data-ttu-id="c3cff-157">Value</span><span class="sxs-lookup"><span data-stu-id="c3cff-157">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c3cff-158">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c3cff-158">Minimum supported client</span></span><br/> | <span data-ttu-id="c3cff-159">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c3cff-159">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c3cff-160">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c3cff-160">Minimum supported server</span></span><br/> | <span data-ttu-id="c3cff-161">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c3cff-161">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c3cff-162">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c3cff-162">Namespace</span></span><br/>                | <span data-ttu-id="c3cff-163">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="c3cff-163">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c3cff-164">MOF</span><span class="sxs-lookup"><span data-stu-id="c3cff-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c3cff-165"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c3cff-165"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c3cff-166">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c3cff-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c3cff-167"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3cff-167"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3cff-168">Vea también</span><span class="sxs-lookup"><span data-stu-id="c3cff-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3cff-169">**Configuración de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="c3cff-169">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="c3cff-170">Clases de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="c3cff-170">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
