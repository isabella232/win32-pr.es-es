---
title: Win32_TerminalError (clase)
description: Representa un error de terminal.
ms.assetid: d3f622cd-e4ce-4c7e-999e-940b67fd116c
ms.tgt_platform: multiple
keywords:
- Win32_TerminalError clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TerminalError de clase, se describe
topic_type:
- apiref
api_name:
- Win32_TerminalError
- Win32_TerminalError.Description
- Win32_TerminalError.Operation
- Win32_TerminalError.ParameterInfo
- Win32_TerminalError.ProviderName
- Win32_TerminalError.StatusCode
- Win32_TerminalError.TerminalName
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f99724badc6c1ca7a2e4168e5c062b4dd1495ea6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150026"
---
# <a name="win32_terminalerror-class"></a><span data-ttu-id="b91cf-105">\_Clase Win32 TerminalError</span><span class="sxs-lookup"><span data-stu-id="b91cf-105">Win32\_TerminalError class</span></span>

<span data-ttu-id="b91cf-106">Representa un error de terminal.</span><span class="sxs-lookup"><span data-stu-id="b91cf-106">Represents a terminal error.</span></span>

<span data-ttu-id="b91cf-107">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="b91cf-107">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b91cf-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b91cf-108">Syntax</span></span>

``` syntax
class Win32_TerminalError : __ExtendedStatus
{
  string Description;
  string Operation;
  string ParameterInfo;
  string ProviderName;
  uint32 StatusCode;
  string TerminalName;
};
```

## <a name="members"></a><span data-ttu-id="b91cf-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="b91cf-109">Members</span></span>

<span data-ttu-id="b91cf-110">La **clase \_ TerminalError de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b91cf-110">The **Win32\_TerminalError** class has these types of members:</span></span>

-   [<span data-ttu-id="b91cf-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b91cf-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b91cf-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b91cf-112">Properties</span></span>

<span data-ttu-id="b91cf-113">La **clase \_ TerminalError de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b91cf-113">The **Win32\_TerminalError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b91cf-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b91cf-114">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b91cf-115">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b91cf-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b91cf-116">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b91cf-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b91cf-117">Cualquier cadena definida por el usuario que describa un estado operativo o de error.</span><span class="sxs-lookup"><span data-stu-id="b91cf-117">Any user-defined string that describes an error or operational status.</span></span>

<span data-ttu-id="b91cf-118">Esta propiedad se hereda de [**\_ \_ ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus).</span><span class="sxs-lookup"><span data-stu-id="b91cf-118">This property is inherited from [**\_\_ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus).</span></span>

</dd> <dt>

<span data-ttu-id="b91cf-119">**Operación**</span><span class="sxs-lookup"><span data-stu-id="b91cf-119">**Operation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b91cf-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b91cf-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b91cf-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b91cf-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b91cf-122">Operación que tiene lugar en el momento en que se produce un error o una anomalía.</span><span class="sxs-lookup"><span data-stu-id="b91cf-122">Operation that takes place at the time of a failure or anomaly.</span></span> <span data-ttu-id="b91cf-123">Normalmente, WMI establece esta propiedad en el nombre de una API COM para un método WMI como el siguiente: [**IWbemServices:: CreateInstanceEnum**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenum).</span><span class="sxs-lookup"><span data-stu-id="b91cf-123">Typically, WMI sets this property to the name of a COM API for WMI method such as the following: [**IWbemServices::CreateInstanceEnum**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenum).</span></span>

<span data-ttu-id="b91cf-124">Esta propiedad se hereda de [**\_ \_ ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus).</span><span class="sxs-lookup"><span data-stu-id="b91cf-124">This property is inherited from [**\_\_ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus).</span></span>

</dd> <dt>

<span data-ttu-id="b91cf-125">**ParameterInfo**</span><span class="sxs-lookup"><span data-stu-id="b91cf-125">**ParameterInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b91cf-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b91cf-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b91cf-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b91cf-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b91cf-128">Los parámetros implicados en un error o un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="b91cf-128">Parameters involved in an error or status change.</span></span> <span data-ttu-id="b91cf-129">Por ejemplo, si una aplicación intenta recuperar una clase que no existe, esta propiedad se establece en el nombre de clase infractora.</span><span class="sxs-lookup"><span data-stu-id="b91cf-129">For example, if an application attempts to retrieve a class that does not exist, this property is set to the offending class name.</span></span>

<span data-ttu-id="b91cf-130">Esta propiedad se hereda de [**\_ \_ ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus).</span><span class="sxs-lookup"><span data-stu-id="b91cf-130">This property is inherited from [**\_\_ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus).</span></span>

</dd> <dt>

<span data-ttu-id="b91cf-131">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="b91cf-131">**ProviderName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b91cf-132">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b91cf-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b91cf-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b91cf-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b91cf-134">Identifica el proveedor que produce o informa de un error o un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="b91cf-134">Identifies the provider that causes or reports an error or status change.</span></span> <span data-ttu-id="b91cf-135">Si un proveedor no está implicado, esta cadena se establece en "administración de Windows".</span><span class="sxs-lookup"><span data-stu-id="b91cf-135">If a provider is not involved, this string is set to "Windows Management".</span></span>

<span data-ttu-id="b91cf-136">Esta propiedad se hereda de [**\_ \_ ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus).</span><span class="sxs-lookup"><span data-stu-id="b91cf-136">This property is inherited from [**\_\_ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus).</span></span>

</dd> <dt>

<span data-ttu-id="b91cf-137">**StatusCode**</span><span class="sxs-lookup"><span data-stu-id="b91cf-137">**StatusCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b91cf-138">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b91cf-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b91cf-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b91cf-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b91cf-140">Contiene un código de error o de información para una operación.</span><span class="sxs-lookup"><span data-stu-id="b91cf-140">Contains an error or information code for an operation.</span></span> <span data-ttu-id="b91cf-141">Puede ser cualquier valor definido por el proveedor, pero el valor 0 (cero) normalmente se reserva para indicar que la operación se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="b91cf-141">This can be any value defined by the provider, but the value 0 (zero) is usually reserved to indicate success.</span></span> <span data-ttu-id="b91cf-142">Esta propiedad se hereda de [**\_ \_ NotifyStatus**](/windows/desktop/WmiSdk/--notifystatus).</span><span class="sxs-lookup"><span data-stu-id="b91cf-142">This property is inherited from [**\_\_NotifyStatus**](/windows/desktop/WmiSdk/--notifystatus).</span></span>

</dd> <dt>

<span data-ttu-id="b91cf-143">**TerminalName**</span><span class="sxs-lookup"><span data-stu-id="b91cf-143">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b91cf-144">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b91cf-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b91cf-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b91cf-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b91cf-146">Nombre del terminal sin el que se produjo el error.</span><span class="sxs-lookup"><span data-stu-id="b91cf-146">The name of the terminal sin which the error occurred.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b91cf-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b91cf-147">Requirements</span></span>



| <span data-ttu-id="b91cf-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="b91cf-148">Requirement</span></span> | <span data-ttu-id="b91cf-149">Value</span><span class="sxs-lookup"><span data-stu-id="b91cf-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b91cf-150">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b91cf-150">Minimum supported client</span></span><br/> | <span data-ttu-id="b91cf-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b91cf-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b91cf-152">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b91cf-152">Minimum supported server</span></span><br/> | <span data-ttu-id="b91cf-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b91cf-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b91cf-154">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b91cf-154">Namespace</span></span><br/>                | <span data-ttu-id="b91cf-155">Raíz de \\ cimv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="b91cf-155">Root\\cimv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="b91cf-156">MOF</span><span class="sxs-lookup"><span data-stu-id="b91cf-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b91cf-157"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b91cf-157"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="b91cf-158">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b91cf-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b91cf-159"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b91cf-159"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b91cf-160">Vea también</span><span class="sxs-lookup"><span data-stu-id="b91cf-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b91cf-161">**\_\_ExtendedStatus**</span><span class="sxs-lookup"><span data-stu-id="b91cf-161">**\_\_ExtendedStatus**</span></span>](/windows/desktop/WmiSdk/--extendedstatus)
</dt> </dl>

 

