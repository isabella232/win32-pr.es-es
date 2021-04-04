---
description: Win32 \_ PrivilegesStatus&\# 8194; La clase WMI informa sobre los privilegios necesarios para completar una operación. Se puede devolver cuando se produce un error en una operación o cuando se ha devuelto una instancia parcialmente rellenada.
ms.assetid: 295ec2bd-7996-4031-8503-d4e869d8368d
ms.tgt_platform: multiple
title: Win32_PrivilegesStatus (clase) (proveedores WMI de CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrivilegesStatus
- Win32_PrivilegesStatus.Description
- Win32_PrivilegesStatus.Operation
- Win32_PrivilegesStatus.ParameterInfo
- Win32_PrivilegesStatus.ProviderName
- Win32_PrivilegesStatus.StatusCode
- Win32_PrivilegesStatus.PrivilegesNotHeld
- Win32_PrivilegesStatus.PrivilegesRequired
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ab399ce08374a954b3bbc015cfee7b4d20167b70
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907250"
---
# <a name="win32_privilegesstatus-class-cimwin32-wmi-providers"></a><span data-ttu-id="c2b59-104">Win32_PrivilegesStatus (clase) (proveedores WMI de CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="c2b59-104">Win32_PrivilegesStatus class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="c2b59-105">La  [clase WMI](../wmisdk/retrieving-a-class.md) **\_ PrivilegesStatus de Win32** informa sobre los privilegios necesarios para completar una operación.</span><span class="sxs-lookup"><span data-stu-id="c2b59-105">The **Win32\_PrivilegesStatus** [WMI class](../wmisdk/retrieving-a-class.md) reports information about privileges required to complete an operation.</span></span> <span data-ttu-id="c2b59-106">Se puede devolver cuando se produce un error en una operación o cuando se ha devuelto una instancia parcialmente rellenada.</span><span class="sxs-lookup"><span data-stu-id="c2b59-106">It may be returned when an operation failed or when a partially populated instance has been returned.</span></span>

<span data-ttu-id="c2b59-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="c2b59-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="c2b59-108">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="c2b59-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2b59-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c2b59-109">Syntax</span></span>

``` syntax
[UUID("{BE46D060-7A7C-11d2-BC85-00104B2CF71C}"), AMENDMENT]
class Win32_PrivilegesStatus : __ExtendedStatus
{
  string Description;
  string Operation;
  string ParameterInfo;
  string ProviderName;
  uint32 StatusCode;
  string PrivilegesNotHeld[];
  string PrivilegesRequired[];
};
```

## <a name="members"></a><span data-ttu-id="c2b59-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="c2b59-110">Members</span></span>

<span data-ttu-id="c2b59-111">La **clase \_ PrivilegesStatus de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c2b59-111">The **Win32\_PrivilegesStatus** class has these types of members:</span></span>

-   [<span data-ttu-id="c2b59-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c2b59-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c2b59-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c2b59-113">Properties</span></span>

<span data-ttu-id="c2b59-114">La **clase \_ PrivilegesStatus de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="c2b59-114">The **Win32\_PrivilegesStatus** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c2b59-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c2b59-115">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2b59-116">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c2b59-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2b59-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c2b59-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2b59-118">Cualquier cadena definida por el usuario que describa un estado operativo o de error.</span><span class="sxs-lookup"><span data-stu-id="c2b59-118">Any user-defined string that describes an error or operational status.</span></span>

<span data-ttu-id="c2b59-119">Esta propiedad se hereda de [**\_ \_ ExtendedStatus**](../wmisdk/--extendedstatus.md).</span><span class="sxs-lookup"><span data-stu-id="c2b59-119">This property is inherited from [**\_\_ExtendedStatus**](../wmisdk/--extendedstatus.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2b59-120">**Operación**</span><span class="sxs-lookup"><span data-stu-id="c2b59-120">**Operation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2b59-121">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c2b59-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2b59-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c2b59-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2b59-123">Operación que tiene lugar en el momento en que se produce un error o una anomalía.</span><span class="sxs-lookup"><span data-stu-id="c2b59-123">Operation that takes place at the time of a failure or anomaly.</span></span> <span data-ttu-id="c2b59-124">Normalmente, Instrumental de administración de Windows (WMI) establece esta propiedad en el nombre de una API COM para un método WMI como el siguiente: [**IWbemServices:: CreateInstanceEnum**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenum).</span><span class="sxs-lookup"><span data-stu-id="c2b59-124">Typically, Windows Management Instrumentation (WMI) sets this property to the name of a COM API for WMI method such as the following: [**IWbemServices::CreateInstanceEnum**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenum).</span></span>

<span data-ttu-id="c2b59-125">Esta propiedad se hereda de [**\_ \_ ExtendedStatus**](../wmisdk/--extendedstatus.md).</span><span class="sxs-lookup"><span data-stu-id="c2b59-125">This property is inherited from [**\_\_ExtendedStatus**](../wmisdk/--extendedstatus.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2b59-126">**ParameterInfo**</span><span class="sxs-lookup"><span data-stu-id="c2b59-126">**ParameterInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2b59-127">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c2b59-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2b59-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c2b59-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2b59-129">Los parámetros implicados en un error o un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="c2b59-129">Parameters involved in an error or status change.</span></span> <span data-ttu-id="c2b59-130">Por ejemplo, si una aplicación intenta recuperar una clase que no existe, esta propiedad se establece en el nombre de clase infractora.</span><span class="sxs-lookup"><span data-stu-id="c2b59-130">For example, if an application attempts to retrieve a class that does not exist, this property is set to the offending class name.</span></span>

<span data-ttu-id="c2b59-131">Esta propiedad se hereda de [**\_ \_ ExtendedStatus**](../wmisdk/--extendedstatus.md).</span><span class="sxs-lookup"><span data-stu-id="c2b59-131">This property is inherited from [**\_\_ExtendedStatus**](../wmisdk/--extendedstatus.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2b59-132">**PrivilegesNotHeld**</span><span class="sxs-lookup"><span data-stu-id="c2b59-132">**PrivilegesNotHeld**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2b59-133">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="c2b59-133">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c2b59-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c2b59-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2b59-135">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| AccessControl \| Windows NT privileges")</span><span class="sxs-lookup"><span data-stu-id="c2b59-135">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|AccessControl\|Windows NT Privileges")</span></span>
</dt> </dl>

<span data-ttu-id="c2b59-136">Falta la lista de privilegios de acceso necesarios para completar una operación.</span><span class="sxs-lookup"><span data-stu-id="c2b59-136">Listing required access privileges missing to complete an operation.</span></span> <span data-ttu-id="c2b59-137">Los tipos de privilegios de acceso se pueden encontrar en privilegios de Windows.</span><span class="sxs-lookup"><span data-stu-id="c2b59-137">The types of access privileges can be found under the Windows Privileges.</span></span>

<span data-ttu-id="c2b59-138">Ejemplo: "SE ha \_ cerrado \_ el nombre"</span><span class="sxs-lookup"><span data-stu-id="c2b59-138">Example: "SE\_SHUTDOWN\_NAME"</span></span>

</dd> <dt>

<span data-ttu-id="c2b59-139">**PrivilegesRequired**</span><span class="sxs-lookup"><span data-stu-id="c2b59-139">**PrivilegesRequired**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2b59-140">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="c2b59-140">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c2b59-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c2b59-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2b59-142">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| AccessControl \| Windows NT privileges")</span><span class="sxs-lookup"><span data-stu-id="c2b59-142">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|AccessControl\|Windows NT Privileges")</span></span>
</dt> </dl>

<span data-ttu-id="c2b59-143">Lista de todos los privilegios necesarios para realizar una operación.</span><span class="sxs-lookup"><span data-stu-id="c2b59-143">Listing of all of the privileges required to perform an operation.</span></span> <span data-ttu-id="c2b59-144">Esto incluye los valores de la propiedad **PrivilegesNotHeld** .</span><span class="sxs-lookup"><span data-stu-id="c2b59-144">This includes values from the **PrivilegesNotHeld** property.</span></span>

<span data-ttu-id="c2b59-145">Ejemplo: "SE ha \_ cerrado \_ el nombre"</span><span class="sxs-lookup"><span data-stu-id="c2b59-145">Example: "SE\_SHUTDOWN\_NAME"</span></span>

</dd> <dt>

<span data-ttu-id="c2b59-146">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="c2b59-146">**ProviderName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2b59-147">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c2b59-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2b59-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c2b59-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2b59-149">Identifica el proveedor que produce o informa de un error o un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="c2b59-149">Identifies the provider that causes or reports an error or status change.</span></span> <span data-ttu-id="c2b59-150">Si un proveedor no está implicado, esta cadena se establece en "administración de Windows".</span><span class="sxs-lookup"><span data-stu-id="c2b59-150">If a provider is not involved, this string is set to "Windows Management".</span></span>

<span data-ttu-id="c2b59-151">Esta propiedad se hereda de [**\_ \_ ExtendedStatus**](../wmisdk/--extendedstatus.md).</span><span class="sxs-lookup"><span data-stu-id="c2b59-151">This property is inherited from [**\_\_ExtendedStatus**](../wmisdk/--extendedstatus.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2b59-152">**StatusCode**</span><span class="sxs-lookup"><span data-stu-id="c2b59-152">**StatusCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2b59-153">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c2b59-153">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c2b59-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c2b59-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2b59-155">Contiene un código de error o de información para una operación.</span><span class="sxs-lookup"><span data-stu-id="c2b59-155">Contains an error or information code for an operation.</span></span> <span data-ttu-id="c2b59-156">Puede ser cualquier valor definido por el proveedor, pero el valor 0 (cero) normalmente se reserva para indicar que la operación se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="c2b59-156">This can be any value defined by the provider, but the value 0 (zero) is usually reserved to indicate success.</span></span>

<span data-ttu-id="c2b59-157">Esta propiedad se hereda de [**\_ \_ NotifyStatus**](../wmisdk/--notifystatus.md).</span><span class="sxs-lookup"><span data-stu-id="c2b59-157">This property is inherited from [**\_\_NotifyStatus**](../wmisdk/--notifystatus.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c2b59-158">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c2b59-158">Remarks</span></span>

<span data-ttu-id="c2b59-159">La **clase \_ PrivilegesStatus de Win32** se deriva de [**\_ \_ ExtendedStatus**](../wmisdk/--extendedstatus.md).</span><span class="sxs-lookup"><span data-stu-id="c2b59-159">The **Win32\_PrivilegesStatus** class is derived from [**\_\_ExtendedStatus**](../wmisdk/--extendedstatus.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c2b59-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2b59-160">Requirements</span></span>



| <span data-ttu-id="c2b59-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2b59-161">Requirement</span></span> | <span data-ttu-id="c2b59-162">Value</span><span class="sxs-lookup"><span data-stu-id="c2b59-162">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c2b59-163">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c2b59-163">Minimum supported client</span></span><br/> | <span data-ttu-id="c2b59-164">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c2b59-164">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c2b59-165">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c2b59-165">Minimum supported server</span></span><br/> | <span data-ttu-id="c2b59-166">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c2b59-166">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c2b59-167">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c2b59-167">Namespace</span></span><br/>                | <span data-ttu-id="c2b59-168">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="c2b59-168">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c2b59-169">MOF</span><span class="sxs-lookup"><span data-stu-id="c2b59-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c2b59-170"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c2b59-170"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c2b59-171">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c2b59-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2b59-172"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2b59-172"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2b59-173">Vea también</span><span class="sxs-lookup"><span data-stu-id="c2b59-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2b59-174">**\_\_ExtendedStatus**</span><span class="sxs-lookup"><span data-stu-id="c2b59-174">**\_\_ExtendedStatus**</span></span>](../wmisdk/--extendedstatus.md)
</dt> </dl>

 

 
