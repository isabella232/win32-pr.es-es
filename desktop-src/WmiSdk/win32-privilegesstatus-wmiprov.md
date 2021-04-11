---
description: Win32 \_ PrivilegesStatus &\# 8194; La clase WMI informa sobre los privilegios necesarios para completar una operación. Se puede devolver cuando se produce un error en una operación o cuando se ha devuelto una instancia parcialmente rellenada.
ms.assetid: 85bda855-1488-4d7a-99ed-798e9859fef7
ms.tgt_platform: multiple
title: Win32_PrivilegesStatus (clase) (WMI)
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
- Schema
api_location:
- Root\WMI
ms.openlocfilehash: 658803be4e70849531bf52e7368e4e9cbcc2f0a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279279"
---
# <a name="win32_privilegesstatus-class-wmi"></a><span data-ttu-id="1a43d-104">Win32_PrivilegesStatus (clase) (WMI)</span><span class="sxs-lookup"><span data-stu-id="1a43d-104">Win32_PrivilegesStatus class (WMI)</span></span>

<span data-ttu-id="1a43d-105">La [clase WMI](retrieving-a-class.md) **\_ PrivilegesStatus de Win32** informa sobre los privilegios necesarios para completar una operación.   </span><span class="sxs-lookup"><span data-stu-id="1a43d-105">The **Win32\_PrivilegesStatus**   [WMI class](retrieving-a-class.md) reports information about privileges required to complete an operation.</span></span> <span data-ttu-id="1a43d-106">Se puede devolver cuando se produce un error en una operación o cuando se ha devuelto una instancia parcialmente rellenada.</span><span class="sxs-lookup"><span data-stu-id="1a43d-106">It may be returned when an operation failed or when a partially populated instance has been returned.</span></span>

<span data-ttu-id="1a43d-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="1a43d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="1a43d-108">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="1a43d-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a43d-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1a43d-109">Syntax</span></span>

``` syntax
[UUID("{BE46D060-7A7C-11d2-BC85-00104B2CF71C}")]
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

## <a name="members"></a><span data-ttu-id="1a43d-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="1a43d-110">Members</span></span>

<span data-ttu-id="1a43d-111">La **clase \_ PrivilegesStatus de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="1a43d-111">The **Win32\_PrivilegesStatus** class has these types of members:</span></span>

-   [<span data-ttu-id="1a43d-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1a43d-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1a43d-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1a43d-113">Properties</span></span>

<span data-ttu-id="1a43d-114">La **clase \_ PrivilegesStatus de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="1a43d-114">The **Win32\_PrivilegesStatus** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1a43d-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1a43d-115">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a43d-116">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1a43d-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a43d-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1a43d-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a43d-118">Cualquier cadena definida por el usuario que describa un estado operativo o de error.</span><span class="sxs-lookup"><span data-stu-id="1a43d-118">Any user-defined string that describes an error or operational status.</span></span>

<span data-ttu-id="1a43d-119">Esta propiedad se hereda de [**\_ \_ ExtendedStatus**](--extendedstatus.md).</span><span class="sxs-lookup"><span data-stu-id="1a43d-119">This property is inherited from [**\_\_ExtendedStatus**](--extendedstatus.md).</span></span>

</dd> <dt>

<span data-ttu-id="1a43d-120">**Operación**</span><span class="sxs-lookup"><span data-stu-id="1a43d-120">**Operation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a43d-121">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1a43d-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a43d-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1a43d-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a43d-123">Operación que tiene lugar en el momento en que se produce un error o una anomalía.</span><span class="sxs-lookup"><span data-stu-id="1a43d-123">Operation that takes place at the time of a failure or anomaly.</span></span> <span data-ttu-id="1a43d-124">Normalmente, Instrumental de administración de Windows (WMI) establece esta propiedad en el nombre de una API COM para un método WMI como el siguiente: [**IWbemServices:: CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum).</span><span class="sxs-lookup"><span data-stu-id="1a43d-124">Typically, Windows Management Instrumentation (WMI) sets this property to the name of a COM API for WMI method such as the following: [**IWbemServices::CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum).</span></span>

<span data-ttu-id="1a43d-125">Esta propiedad se hereda de [**\_ \_ ExtendedStatus**](--extendedstatus.md).</span><span class="sxs-lookup"><span data-stu-id="1a43d-125">This property is inherited from [**\_\_ExtendedStatus**](--extendedstatus.md).</span></span>

</dd> <dt>

<span data-ttu-id="1a43d-126">**ParameterInfo**</span><span class="sxs-lookup"><span data-stu-id="1a43d-126">**ParameterInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a43d-127">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1a43d-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a43d-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1a43d-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a43d-129">Los parámetros implicados en un error o un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="1a43d-129">Parameters involved in an error or status change.</span></span> <span data-ttu-id="1a43d-130">Por ejemplo, si una aplicación intenta recuperar una clase que no existe, esta propiedad se establece en el nombre de clase infractora.</span><span class="sxs-lookup"><span data-stu-id="1a43d-130">For example, if an application attempts to retrieve a class that does not exist, this property is set to the offending class name.</span></span>

<span data-ttu-id="1a43d-131">Esta propiedad se hereda de [**\_ \_ ExtendedStatus**](--extendedstatus.md).</span><span class="sxs-lookup"><span data-stu-id="1a43d-131">This property is inherited from [**\_\_ExtendedStatus**](--extendedstatus.md).</span></span>

</dd> <dt>

<span data-ttu-id="1a43d-132">**PrivilegesNotHeld**</span><span class="sxs-lookup"><span data-stu-id="1a43d-132">**PrivilegesNotHeld**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a43d-133">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="1a43d-133">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1a43d-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1a43d-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a43d-135">Falta la lista de privilegios de acceso necesarios para completar una operación.</span><span class="sxs-lookup"><span data-stu-id="1a43d-135">Listing required access privileges missing to complete an operation.</span></span> <span data-ttu-id="1a43d-136">Los tipos de privilegios de acceso se pueden encontrar en privilegios de Windows.</span><span class="sxs-lookup"><span data-stu-id="1a43d-136">The types of access privileges can be found under the Windows Privileges.</span></span>

<span data-ttu-id="1a43d-137">Ejemplo: "SE ha \_ cerrado \_ el nombre"</span><span class="sxs-lookup"><span data-stu-id="1a43d-137">Example: "SE\_SHUTDOWN\_NAME"</span></span>

</dd> <dt>

<span data-ttu-id="1a43d-138">**PrivilegesRequired**</span><span class="sxs-lookup"><span data-stu-id="1a43d-138">**PrivilegesRequired**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a43d-139">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="1a43d-139">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1a43d-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1a43d-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a43d-141">Lista de todos los privilegios necesarios para realizar una operación.</span><span class="sxs-lookup"><span data-stu-id="1a43d-141">Listing of all of the privileges required to perform an operation.</span></span> <span data-ttu-id="1a43d-142">Esto incluye los valores de la propiedad **PrivilegesNotHeld** .</span><span class="sxs-lookup"><span data-stu-id="1a43d-142">This includes values from the **PrivilegesNotHeld** property.</span></span>

<span data-ttu-id="1a43d-143">Ejemplo: "SE ha \_ cerrado \_ el nombre"</span><span class="sxs-lookup"><span data-stu-id="1a43d-143">Example: "SE\_SHUTDOWN\_NAME"</span></span>

</dd> <dt>

<span data-ttu-id="1a43d-144">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="1a43d-144">**ProviderName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a43d-145">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1a43d-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a43d-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1a43d-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a43d-147">Identifica el proveedor que produce o informa de un error o un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="1a43d-147">Identifies the provider that causes or reports an error or status change.</span></span> <span data-ttu-id="1a43d-148">Si un proveedor no está implicado, esta cadena se establece en "administración de Windows".</span><span class="sxs-lookup"><span data-stu-id="1a43d-148">If a provider is not involved, this string is set to "Windows Management".</span></span>

<span data-ttu-id="1a43d-149">Esta propiedad se hereda de [**\_ \_ ExtendedStatus**](--extendedstatus.md).</span><span class="sxs-lookup"><span data-stu-id="1a43d-149">This property is inherited from [**\_\_ExtendedStatus**](--extendedstatus.md).</span></span>

</dd> <dt>

<span data-ttu-id="1a43d-150">**StatusCode**</span><span class="sxs-lookup"><span data-stu-id="1a43d-150">**StatusCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a43d-151">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1a43d-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1a43d-152">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1a43d-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a43d-153">Contiene un código de error o de información para una operación.</span><span class="sxs-lookup"><span data-stu-id="1a43d-153">Contains an error or information code for an operation.</span></span> <span data-ttu-id="1a43d-154">Puede ser cualquier valor definido por el proveedor, pero el valor 0 (cero) normalmente se reserva para indicar que la operación se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="1a43d-154">This can be any value defined by the provider, but the value 0 (zero) is usually reserved to indicate success.</span></span> <span data-ttu-id="1a43d-155">Esta propiedad se hereda de [**\_ \_ NotifyStatus**](--notifystatus.md).</span><span class="sxs-lookup"><span data-stu-id="1a43d-155">This property is inherited from [**\_\_NotifyStatus**](--notifystatus.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1a43d-156">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1a43d-156">Remarks</span></span>

<span data-ttu-id="1a43d-157">La **clase \_ PrivilegesStatus de Win32** se deriva de [**\_ \_ ExtendedStatus**](--extendedstatus.md).</span><span class="sxs-lookup"><span data-stu-id="1a43d-157">The **Win32\_PrivilegesStatus** class is derived from [**\_\_ExtendedStatus**](--extendedstatus.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1a43d-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a43d-158">Requirements</span></span>



| <span data-ttu-id="1a43d-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a43d-159">Requirement</span></span> | <span data-ttu-id="1a43d-160">Value</span><span class="sxs-lookup"><span data-stu-id="1a43d-160">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1a43d-161">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1a43d-161">Minimum supported client</span></span><br/> | <span data-ttu-id="1a43d-162">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1a43d-162">Windows Vista</span></span><br/>                                                           |
| <span data-ttu-id="1a43d-163">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1a43d-163">Minimum supported server</span></span><br/> | <span data-ttu-id="1a43d-164">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1a43d-164">Windows Server 2008</span></span><br/>                                                     |
| <span data-ttu-id="1a43d-165">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1a43d-165">Namespace</span></span><br/>                | <span data-ttu-id="1a43d-166">\\WMI raíz</span><span class="sxs-lookup"><span data-stu-id="1a43d-166">Root\\WMI</span></span><br/>                                                               |
| <span data-ttu-id="1a43d-167">MOF</span><span class="sxs-lookup"><span data-stu-id="1a43d-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1a43d-168"><dt>WMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1a43d-168"><dt>Wmi.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a43d-169">Vea también</span><span class="sxs-lookup"><span data-stu-id="1a43d-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a43d-170">**\_\_ExtendedStatus**</span><span class="sxs-lookup"><span data-stu-id="1a43d-170">**\_\_ExtendedStatus**</span></span>](--extendedstatus.md)
</dt> </dl>

 

 




