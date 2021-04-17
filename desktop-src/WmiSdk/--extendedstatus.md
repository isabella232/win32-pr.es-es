---
description: Se usa para notificar información detallada sobre el estado y el error.
ms.assetid: 6bdff9a8-1a7c-4860-a12e-4d3162964ee4
ms.tgt_platform: multiple
title: __ExtendedStatus (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ExtendedStatus
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: cfc364ac6523aad69e53755d96fe220d0109fab8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717208"
---
# <a name="__extendedstatus-class"></a><span data-ttu-id="f832f-103">\_\_Clase ExtendedStatus</span><span class="sxs-lookup"><span data-stu-id="f832f-103">\_\_ExtendedStatus class</span></span>

<span data-ttu-id="f832f-104">La clase del sistema **\_ \_ ExtendedStatus** se usa para informar sobre el estado detallado y la información del error.</span><span class="sxs-lookup"><span data-stu-id="f832f-104">The **\_\_ExtendedStatus** system class is used to report detailed status and error information.</span></span>

<span data-ttu-id="f832f-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="f832f-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="f832f-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="f832f-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f832f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f832f-107">Syntax</span></span>

``` syntax
class __ExtendedStatus : __NotifyStatus
{
  string Description;
  string Operation;
  string ParameterInfo;
  string ProviderName;
  uint32 StatusCode;
};
```

## <a name="members"></a><span data-ttu-id="f832f-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="f832f-108">Members</span></span>

<span data-ttu-id="f832f-109">La clase **\_ \_ ExtendedStatus** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f832f-109">The **\_\_ExtendedStatus** class has these types of members:</span></span>

-   [<span data-ttu-id="f832f-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f832f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f832f-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f832f-111">Properties</span></span>

<span data-ttu-id="f832f-112">La clase **\_ \_ ExtendedStatus** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f832f-112">The **\_\_ExtendedStatus** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f832f-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f832f-113">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f832f-114">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f832f-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f832f-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f832f-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f832f-116">Cualquier cadena definida por el usuario que describa un estado operativo o de error.</span><span class="sxs-lookup"><span data-stu-id="f832f-116">Any user-defined string that describes an error or operational status.</span></span>

</dd> <dt>

<span data-ttu-id="f832f-117">**Operación**</span><span class="sxs-lookup"><span data-stu-id="f832f-117">**Operation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f832f-118">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f832f-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f832f-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f832f-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f832f-120">Operación que tiene lugar en el momento en que se produce un error o una anomalía.</span><span class="sxs-lookup"><span data-stu-id="f832f-120">Operation that takes place at the time of a failure or anomaly.</span></span> <span data-ttu-id="f832f-121">Normalmente, Instrumental de administración de Windows (WMI) establece esta propiedad en el nombre de una API COM para un método WMI como el siguiente: [**IWbemServices:: CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum).</span><span class="sxs-lookup"><span data-stu-id="f832f-121">Typically, Windows Management Instrumentation (WMI) sets this property to the name of a COM API for WMI method such as the following: [**IWbemServices::CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum).</span></span>

</dd> <dt>

<span data-ttu-id="f832f-122">**ParameterInfo**</span><span class="sxs-lookup"><span data-stu-id="f832f-122">**ParameterInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f832f-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f832f-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f832f-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f832f-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f832f-125">Los parámetros implicados en un error o un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="f832f-125">Parameters involved in an error or status change.</span></span> <span data-ttu-id="f832f-126">Por ejemplo, si una aplicación intenta recuperar una clase que no existe, esta propiedad se establece en el nombre de clase infractora.</span><span class="sxs-lookup"><span data-stu-id="f832f-126">For example, if an application attempts to retrieve a class that does not exist, this property is set to the offending class name.</span></span>

</dd> <dt>

<span data-ttu-id="f832f-127">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="f832f-127">**ProviderName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f832f-128">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f832f-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f832f-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f832f-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f832f-130">Identifica el proveedor que produce o informa de un error o un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="f832f-130">Identifies the provider that causes or reports an error or status change.</span></span> <span data-ttu-id="f832f-131">Si un proveedor no está implicado, esta cadena se establece en "administración de Windows".</span><span class="sxs-lookup"><span data-stu-id="f832f-131">If a provider is not involved, this string is set to "Windows Management".</span></span>

</dd> <dt>

<span data-ttu-id="f832f-132">**StatusCode**</span><span class="sxs-lookup"><span data-stu-id="f832f-132">**StatusCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f832f-133">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f832f-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f832f-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f832f-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f832f-135">Contiene un código de error o de información para una operación.</span><span class="sxs-lookup"><span data-stu-id="f832f-135">Contains an error or information code for an operation.</span></span> <span data-ttu-id="f832f-136">Puede ser cualquier valor definido por el proveedor, pero el valor 0 (cero) normalmente se reserva para indicar que la operación se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="f832f-136">This can be any value defined by the provider, but the value 0 (zero) is usually reserved to indicate success.</span></span> <span data-ttu-id="f832f-137">Esta propiedad se hereda de [**\_ \_ NotifyStatus**](--notifystatus.md).</span><span class="sxs-lookup"><span data-stu-id="f832f-137">This property is inherited from [**\_\_NotifyStatus**](--notifystatus.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f832f-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f832f-138">Remarks</span></span>

<span data-ttu-id="f832f-139">La clase **\_ \_ ExtendedStatus** se deriva de la clase [**\_ \_ NotifyStatus**](--notifystatus.md) .</span><span class="sxs-lookup"><span data-stu-id="f832f-139">The **\_\_ExtendedStatus** class is derived from the [**\_\_NotifyStatus**](--notifystatus.md) class.</span></span>

<span data-ttu-id="f832f-140">Use la clase **\_ \_ ExtendedStatus** para notificar información más compleja que un código de resultado simple.</span><span class="sxs-lookup"><span data-stu-id="f832f-140">Use the **\_\_ExtendedStatus** class to report information that is more complex than a simple result code.</span></span> <span data-ttu-id="f832f-141">Los proveedores pueden derivar sus propias clases de **\_ \_ ExtendedStatus** si necesitan más propiedades para describir los errores.</span><span class="sxs-lookup"><span data-stu-id="f832f-141">Providers can derive their own classes from **\_\_ExtendedStatus** if they require more properties to describe the errors.</span></span>

<span data-ttu-id="f832f-142">La propiedad **StatusCode** , heredada de la clase primaria [**\_ \_ NotifyStatus**](--notifystatus.md) , es un entero sin signo que representa el valor de error o de estado.</span><span class="sxs-lookup"><span data-stu-id="f832f-142">The **StatusCode** property, inherited from the [**\_\_NotifyStatus**](--notifystatus.md) parent class, is an unsigned integer that represents the error or status value.</span></span> <span data-ttu-id="f832f-143">Cuando un proveedor dinámico devuelve las instancias de esta clase desde un método, las propiedades **StatusCode** y **Description** las establece el proveedor y las demás propiedades se establecen mediante WMI.</span><span class="sxs-lookup"><span data-stu-id="f832f-143">When instances of this class are returned from a method by a dynamic provider, the **StatusCode** and **Description** properties are set by the provider, and the other properties are set by WMI.</span></span>

## <a name="examples"></a><span data-ttu-id="f832f-144">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f832f-144">Examples</span></span>

<span data-ttu-id="f832f-145">El siguiente ejemplo de código, tomado de [FND: Cómo Configuration Manager controlar los errores asincrónicos](https://Gallery.TechNet.Microsoft.Com/0bc05d07-1479-43c9-8e01-0f01d0fc3daa) mediante el ejemplo de código VBScript de WMI en la galería de TechNet, describe el uso de **\_ \_ ExtendedStatus** para recuperar información de errores.</span><span class="sxs-lookup"><span data-stu-id="f832f-145">The following code sample, taken from the [FND:How to Handle Configuration Manager Asynchronous Errors by Using WMI](https://Gallery.TechNet.Microsoft.Com/0bc05d07-1479-43c9-8e01-0f01d0fc3daa) VBScript code example on TechNet Gallery, describes using **\_\_ExtendedStatus** to retrieve error information.</span></span>


```VB
Sub sink_OnCompleted(HResult, oErr, oCtx) 
    WScript.Echo "All collections returned" 
  
    if HResult <> 0 Then  
    ' Determine the type of error. 
        If oErr.Path_.Class = "__ExtendedStatus" Then 
            WScript.Echo "WMI Error: "& oErr.Description             
        ElseIf ExtendedStatus.Path_.Class = "SMS_ExtendedStatus" Then 
            WScript.Echo "Provider Error: "& oErr.Description 
            WScript.Echo "Code: " & oErr.ErrorCode 
        End If 
    End If     
    bdone = true 
End sub
```



## <a name="requirements"></a><span data-ttu-id="f832f-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f832f-146">Requirements</span></span>



| <span data-ttu-id="f832f-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="f832f-147">Requirement</span></span> | <span data-ttu-id="f832f-148">Value</span><span class="sxs-lookup"><span data-stu-id="f832f-148">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="f832f-149">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f832f-149">Minimum supported client</span></span><br/> | <span data-ttu-id="f832f-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f832f-150">Windows Vista</span></span><br/>       |
| <span data-ttu-id="f832f-151">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f832f-151">Minimum supported server</span></span><br/> | <span data-ttu-id="f832f-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f832f-152">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="f832f-153">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f832f-153">Namespace</span></span><br/>                | <span data-ttu-id="f832f-154">Todos los espacios de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="f832f-154">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="f832f-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="f832f-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f832f-156">**\_\_NotifyStatus**</span><span class="sxs-lookup"><span data-stu-id="f832f-156">**\_\_NotifyStatus**</span></span>](/windows/desktop/WmiSdk/--notifystatus)
</dt> <dt>

[<span data-ttu-id="f832f-157">Clases del sistema WMI</span><span class="sxs-lookup"><span data-stu-id="f832f-157">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

