---
description: Describe las capacidades del MSVM ComputerSystem asociado \_ .
ms.assetid: 7e3b51ba-f85d-4b83-abc6-a094d412eca1
title: Msvm_VirtualSystemCapabilities (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemCapabilities
- Msvm_VirtualSystemCapabilities.InstanceID
- Msvm_VirtualSystemCapabilities.Caption
- Msvm_VirtualSystemCapabilities.Description
- Msvm_VirtualSystemCapabilities.ElementName
- Msvm_VirtualSystemCapabilities.ElementNameEditSupported
- Msvm_VirtualSystemCapabilities.MaxElementNameLen
- Msvm_VirtualSystemCapabilities.RequestedStatesSupported
- Msvm_VirtualSystemCapabilities.ElementNameMask
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9fbd9b747e85ec1c9a1b7754f99282a7d913994e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275222"
---
# <a name="msvm_virtualsystemcapabilities-class"></a><span data-ttu-id="4507b-103">MSVM \_ VirtualSystemCapabilities (clase)</span><span class="sxs-lookup"><span data-stu-id="4507b-103">Msvm\_VirtualSystemCapabilities class</span></span>

<span data-ttu-id="4507b-104">Describe las capacidades del [**MSVM \_ ComputerSystem**](msvm-computersystem.md)asociado.</span><span class="sxs-lookup"><span data-stu-id="4507b-104">Describes the capabilities of the associated [**Msvm\_ComputerSystem**](msvm-computersystem.md).</span></span>

<span data-ttu-id="4507b-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="4507b-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4507b-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4507b-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemCapabilities : CIM_EnabledLogicalElementCapabilities
{
  string  InstanceID;
  string  Caption = "Hyper-V Virtual System Capabilities";
  string  Description = "Defines Virtual System Capabilities";
  string  ElementName = "Hyper-V Virtual System Capabilities";
  boolean ElementNameEditSupported = True;
  unit16  MaxElementNameLen = 100;
  unit16  RequestedStatesSupported[];
  string  ElementNameMask;
};
```

## <a name="members"></a><span data-ttu-id="4507b-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="4507b-107">Members</span></span>

<span data-ttu-id="4507b-108">La clase **MSVM \_ VirtualSystemCapabilities** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="4507b-108">The **Msvm\_VirtualSystemCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="4507b-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4507b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4507b-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4507b-110">Properties</span></span>

<span data-ttu-id="4507b-111">La clase **MSVM \_ VirtualSystemCapabilities** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="4507b-111">The **Msvm\_VirtualSystemCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4507b-112">**Caption**</span><span class="sxs-lookup"><span data-stu-id="4507b-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4507b-113">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4507b-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4507b-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4507b-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4507b-115">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="4507b-115">A short description of the object.</span></span> <span data-ttu-id="4507b-116">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="4507b-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="4507b-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4507b-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4507b-118">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4507b-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4507b-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4507b-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4507b-120">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="4507b-120">A description of the object.</span></span> <span data-ttu-id="4507b-121">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="4507b-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="4507b-122">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="4507b-122">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4507b-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4507b-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4507b-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4507b-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4507b-125">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="4507b-125">A display name for the object.</span></span> <span data-ttu-id="4507b-126">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="4507b-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="4507b-127">**ElementNameEditSupported**</span><span class="sxs-lookup"><span data-stu-id="4507b-127">**ElementNameEditSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4507b-128">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="4507b-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4507b-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4507b-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4507b-130">Indica si se puede modificar la propiedad **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="4507b-130">Indicates whether the **ElementName** property can be modified.</span></span> <span data-ttu-id="4507b-131">Esta propiedad se hereda de **\_ EnabledLogicalElementCapabilities CIM**.</span><span class="sxs-lookup"><span data-stu-id="4507b-131">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="4507b-132">**ElementNameMask**</span><span class="sxs-lookup"><span data-stu-id="4507b-132">**ElementNameMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4507b-133">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4507b-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4507b-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4507b-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4507b-135">Especifica las restricciones en **ElementName**, expresadas como una expresión regular.</span><span class="sxs-lookup"><span data-stu-id="4507b-135">Specifies the restrictions on **ElementName**, expressed as a regular expression.</span></span> <span data-ttu-id="4507b-136">Esta propiedad se hereda de **\_ EnabledLogicalElementCapabilities CIM**.</span><span class="sxs-lookup"><span data-stu-id="4507b-136">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="4507b-137">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="4507b-137">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4507b-138">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4507b-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4507b-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4507b-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4507b-140">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="4507b-140">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="4507b-141">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="4507b-141">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="4507b-142">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="4507b-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="4507b-143">**MaxElementNameLen**</span><span class="sxs-lookup"><span data-stu-id="4507b-143">**MaxElementNameLen**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4507b-144">Tipo de datos: **unit16**</span><span class="sxs-lookup"><span data-stu-id="4507b-144">Data type: **unit16**</span></span>
</dt> <dt>

<span data-ttu-id="4507b-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4507b-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4507b-146">Calificadores: **MaxValue** (256)</span><span class="sxs-lookup"><span data-stu-id="4507b-146">Qualifiers: **MaxValue** (256)</span></span>
</dt> </dl>

<span data-ttu-id="4507b-147">Especifica la longitud máxima admitida de la propiedad **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="4507b-147">Specifies the maximum supported length of the **ElementName** property.</span></span> <span data-ttu-id="4507b-148">Esta propiedad se hereda de **\_ EnabledLogicalElementCapabilities CIM**.</span><span class="sxs-lookup"><span data-stu-id="4507b-148">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="4507b-149">**RequestedStatesSupported**</span><span class="sxs-lookup"><span data-stu-id="4507b-149">**RequestedStatesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4507b-150">Tipo de datos: matriz **unit16**</span><span class="sxs-lookup"><span data-stu-id="4507b-150">Data type: **unit16** array</span></span>
</dt> <dt>

<span data-ttu-id="4507b-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4507b-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4507b-152">Indica los posibles Estados que se pueden solicitar al utilizar el método **RequestStateChange** en el elemento lógico habilitado.</span><span class="sxs-lookup"><span data-stu-id="4507b-152">Indicates the possible states that can be requested when using the **RequestStateChange** method on the enabled logical element.</span></span> <span data-ttu-id="4507b-153">Esta propiedad se hereda de **\_ EnabledLogicalElementCapabilities CIM**.</span><span class="sxs-lookup"><span data-stu-id="4507b-153">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>



| <span data-ttu-id="4507b-154">Value</span><span class="sxs-lookup"><span data-stu-id="4507b-154">Value</span></span>                                                                         | <span data-ttu-id="4507b-155">Significado</span><span class="sxs-lookup"><span data-stu-id="4507b-155">Meaning</span></span>              |
|-------------------------------------------------------------------------------|----------------------|
| <dl> <span data-ttu-id="4507b-156"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="4507b-156"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="4507b-157">habilitado</span><span class="sxs-lookup"><span data-stu-id="4507b-157">Enabled</span></span><br/>   |
| <dl> <span data-ttu-id="4507b-158"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="4507b-158"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="4507b-159">Impide</span><span class="sxs-lookup"><span data-stu-id="4507b-159">Disables</span></span><br/>  |
| <dl> <span data-ttu-id="4507b-160"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="4507b-160"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="4507b-161">Apagar</span><span class="sxs-lookup"><span data-stu-id="4507b-161">Shut Down</span></span><br/> |
| <dl> <span data-ttu-id="4507b-162"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="4507b-162"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="4507b-163">Sin conexión</span><span class="sxs-lookup"><span data-stu-id="4507b-163">Offline</span></span><br/>   |
| <dl> <span data-ttu-id="4507b-164"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="4507b-164"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="4507b-165">Prueba</span><span class="sxs-lookup"><span data-stu-id="4507b-165">Test</span></span><br/>      |
| <dl> <span data-ttu-id="4507b-166"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="4507b-166"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="4507b-167">Acepta</span><span class="sxs-lookup"><span data-stu-id="4507b-167">Defer</span></span><br/>     |
| <dl> <span data-ttu-id="4507b-168"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="4507b-168"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="4507b-169">Modo de inactividad</span><span class="sxs-lookup"><span data-stu-id="4507b-169">Quiesce</span></span><br/>   |
| <dl> <span data-ttu-id="4507b-170"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="4507b-170"><dt>10</dt></span></span> </dl> | <span data-ttu-id="4507b-171">Reboot</span><span class="sxs-lookup"><span data-stu-id="4507b-171">Reboot</span></span><br/>    |
| <dl> <span data-ttu-id="4507b-172"><dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="4507b-172"><dt>11</dt></span></span> </dl> | <span data-ttu-id="4507b-173">Reset</span><span class="sxs-lookup"><span data-stu-id="4507b-173">Reset</span></span><br/>     |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4507b-174">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4507b-174">Requirements</span></span>



| <span data-ttu-id="4507b-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="4507b-175">Requirement</span></span> | <span data-ttu-id="4507b-176">Value</span><span class="sxs-lookup"><span data-stu-id="4507b-176">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4507b-177">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4507b-177">Minimum supported client</span></span><br/> | <span data-ttu-id="4507b-178">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="4507b-178">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4507b-179">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4507b-179">Minimum supported server</span></span><br/> | <span data-ttu-id="4507b-180">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="4507b-180">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4507b-181">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4507b-181">Namespace</span></span><br/>                | <span data-ttu-id="4507b-182">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="4507b-182">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4507b-183">MOF</span><span class="sxs-lookup"><span data-stu-id="4507b-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4507b-184"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4507b-184"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4507b-185">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4507b-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4507b-186"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4507b-186"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

