---
description: Representa la configuración de ACL del puerto extendido.
ms.assetid: 357dd891-6692-4ffc-b8a8-4ece40d4af28
title: Msvm_EthernetSwitchPortExtendedAclSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortExtendedAclSettingData
- Msvm_EthernetSwitchPortExtendedAclSettingData.Name
- Msvm_EthernetSwitchPortExtendedAclSettingData.Direction
- Msvm_EthernetSwitchPortExtendedAclSettingData.Action
- Msvm_EthernetSwitchPortExtendedAclSettingData.LocalIPAddress
- Msvm_EthernetSwitchPortExtendedAclSettingData.RemoteIPAddress
- Msvm_EthernetSwitchPortExtendedAclSettingData.LocalPort
- Msvm_EthernetSwitchPortExtendedAclSettingData.RemotePort
- Msvm_EthernetSwitchPortExtendedAclSettingData.Protocol
- Msvm_EthernetSwitchPortExtendedAclSettingData.Weight
- Msvm_EthernetSwitchPortExtendedAclSettingData.Stateful
- Msvm_EthernetSwitchPortExtendedAclSettingData.IdleSessionTimeout
- Msvm_EthernetSwitchPortExtendedAclSettingData.IsolationID
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 25ae81e4f00e87e41170ac5713ced0d9b523c844
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667684"
---
# <a name="msvm_ethernetswitchportextendedaclsettingdata-class"></a><span data-ttu-id="10395-103">MSVM \_ EthernetSwitchPortExtendedAclSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="10395-103">Msvm\_EthernetSwitchPortExtendedAclSettingData class</span></span>

<span data-ttu-id="10395-104">Representa la configuración de ACL del puerto extendido.</span><span class="sxs-lookup"><span data-stu-id="10395-104">Represents the extended port ACL settings.</span></span>

<span data-ttu-id="10395-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="10395-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="10395-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="10395-106">Syntax</span></span>

``` syntax
[Dynamic, UUID("CD168FF0-A16D-4514-B7B5-8BBBA791A928"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), Provider("VmmsWmiInstanceAndMethodProvider"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Extended ACL Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortExtendedAclSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string  Name = "";
  uint8   Direction = 0;
  uint8   Action = 0;
  string  LocalIPAddress = "ANY";
  string  RemoteIPAddress = "ANY";
  string  LocalPort = "ANY";
  string  RemotePort = "ANY";
  string  Protocol = "ANY";
  Uint16  Weight = 0;
  Boolean Stateful = FALSE;
  Uint16  IdleSessionTimeout = 255;
  Uint32  IsolationID = 0;
};
```

## <a name="members"></a><span data-ttu-id="10395-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="10395-107">Members</span></span>

<span data-ttu-id="10395-108">La clase **MSVM \_ EthernetSwitchPortExtendedAclSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="10395-108">The **Msvm\_EthernetSwitchPortExtendedAclSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="10395-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="10395-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="10395-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="10395-110">Properties</span></span>

<span data-ttu-id="10395-111">La clase **MSVM \_ EthernetSwitchPortExtendedAclSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="10395-111">The **Msvm\_EthernetSwitchPortExtendedAclSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="10395-112">**Acción**</span><span class="sxs-lookup"><span data-stu-id="10395-112">**Action**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10395-113">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="10395-113">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="10395-114">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="10395-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="10395-115">Calificadores: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="10395-115">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="10395-116">La acción de la ACL extendida.</span><span class="sxs-lookup"><span data-stu-id="10395-116">The action of the extended ACL.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="10395-117">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="10395-117">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>

<span data-ttu-id="10395-118">**Permitir** (1)</span><span class="sxs-lookup"><span data-stu-id="10395-118">**Allow** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Deny"></span><span id="deny"></span><span id="DENY"></span>

<span data-ttu-id="10395-119">**Denegar** (2)</span><span class="sxs-lookup"><span data-stu-id="10395-119">**Deny** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="10395-120">**Dirección**</span><span class="sxs-lookup"><span data-stu-id="10395-120">**Direction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10395-121">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="10395-121">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="10395-122">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="10395-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="10395-123">Calificadores: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="10395-123">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="10395-124">Indica si la ACL extendida se aplica a la dirección de entrada o de salida.</span><span class="sxs-lookup"><span data-stu-id="10395-124">Indicates if the extended ACL applies to incoming or outgoing direction.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="10395-125">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="10395-125">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Incoming"></span><span id="incoming"></span><span id="INCOMING"></span>

<span data-ttu-id="10395-126">**Entrante** (1)</span><span class="sxs-lookup"><span data-stu-id="10395-126">**Incoming** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Outgoing"></span><span id="outgoing"></span><span id="OUTGOING"></span>

<span data-ttu-id="10395-127">**Saliente** (2)</span><span class="sxs-lookup"><span data-stu-id="10395-127">**Outgoing** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="10395-128">**IdleSessionTimeout**</span><span class="sxs-lookup"><span data-stu-id="10395-128">**IdleSessionTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10395-129">Tipo de datos: **Uint16**</span><span class="sxs-lookup"><span data-stu-id="10395-129">Data type: **Uint16**</span></span>
</dt> <dt>

<span data-ttu-id="10395-130">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="10395-130">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="10395-131">Calificadores: **WmiDataId** (11), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="10395-131">Qualifiers: **WmiDataId** (11), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="10395-132">Valor de tiempo de espera de sesión inactiva (en segundos) para ACL con estado.</span><span class="sxs-lookup"><span data-stu-id="10395-132">Idle session timeout value (in seconds) for stateful ACL.</span></span>

</dd> <dt>

<span data-ttu-id="10395-133">**IsolationID**</span><span class="sxs-lookup"><span data-stu-id="10395-133">**IsolationID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10395-134">Tipo de datos: **Uint32**</span><span class="sxs-lookup"><span data-stu-id="10395-134">Data type: **Uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10395-135">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="10395-135">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="10395-136">Calificadores: **InterfaceVersion** (1), **InterfaceRevision** (0), **WmiDataId** (12)</span><span class="sxs-lookup"><span data-stu-id="10395-136">Qualifiers: **InterfaceVersion** (1), **InterfaceRevision** (0), **WmiDataId** (12)</span></span>
</dt> </dl>

<span data-ttu-id="10395-137">IDENTIFICADOR de aislamiento para el que se debe aplicar la ACL extendida.</span><span class="sxs-lookup"><span data-stu-id="10395-137">Isolation ID for which the extended ACL should be applied.</span></span>

</dd> <dt>

<span data-ttu-id="10395-138">**LocalIPAddress**</span><span class="sxs-lookup"><span data-stu-id="10395-138">**LocalIPAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10395-139">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="10395-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10395-140">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="10395-140">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="10395-141">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (40), **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="10395-141">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (40), **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="10395-142">Dirección IP local.</span><span class="sxs-lookup"><span data-stu-id="10395-142">The local IP address.</span></span>

</dd> <dt>

<span data-ttu-id="10395-143">**LocalPort**</span><span class="sxs-lookup"><span data-stu-id="10395-143">**LocalPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10395-144">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="10395-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10395-145">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="10395-145">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="10395-146">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (21), **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="10395-146">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (21), **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="10395-147">El intervalo de puertos local.</span><span class="sxs-lookup"><span data-stu-id="10395-147">The local port range.</span></span>

</dd> <dt>

<span data-ttu-id="10395-148">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="10395-148">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10395-149">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="10395-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10395-150">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="10395-150">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="10395-151">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="10395-151">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="10395-152">Nombre descriptivo de la ACL extendida.</span><span class="sxs-lookup"><span data-stu-id="10395-152">The friendly name of the Extended ACL.</span></span>

</dd> <dt>

<span data-ttu-id="10395-153">**Protocolo**</span><span class="sxs-lookup"><span data-stu-id="10395-153">**Protocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10395-154">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="10395-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10395-155">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="10395-155">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="10395-156">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (15), **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="10395-156">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (15), **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="10395-157">Cadena de protocolo.</span><span class="sxs-lookup"><span data-stu-id="10395-157">The protocol string.</span></span>

</dd> <dt>

<span data-ttu-id="10395-158">**RemoteIPAddress**</span><span class="sxs-lookup"><span data-stu-id="10395-158">**RemoteIPAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10395-159">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="10395-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10395-160">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="10395-160">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="10395-161">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (40), **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="10395-161">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (40), **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="10395-162">Dirección IP remota.</span><span class="sxs-lookup"><span data-stu-id="10395-162">The remote IP address.</span></span>

</dd> <dt>

<span data-ttu-id="10395-163">**RemotePort**</span><span class="sxs-lookup"><span data-stu-id="10395-163">**RemotePort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10395-164">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="10395-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10395-165">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="10395-165">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="10395-166">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (21), **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="10395-166">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (21), **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="10395-167">El intervalo de puertos remotos.</span><span class="sxs-lookup"><span data-stu-id="10395-167">The remote port range.</span></span>

</dd> <dt>

<span data-ttu-id="10395-168">**Con estado**</span><span class="sxs-lookup"><span data-stu-id="10395-168">**Stateful**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10395-169">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="10395-169">Data type: **Boolean**</span></span>
</dt> <dt>

<span data-ttu-id="10395-170">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="10395-170">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="10395-171">Calificadores: **WmiDataId** (10), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="10395-171">Qualifiers: **WmiDataId** (10), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="10395-172">Indica si la ACL extendida es con estado o sin estado.</span><span class="sxs-lookup"><span data-stu-id="10395-172">Indicates if the extended ACL is stateful or stateless.</span></span>

</dd> <dt>

<span data-ttu-id="10395-173">**Peso**</span><span class="sxs-lookup"><span data-stu-id="10395-173">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10395-174">Tipo de datos: **Uint16**</span><span class="sxs-lookup"><span data-stu-id="10395-174">Data type: **Uint16**</span></span>
</dt> <dt>

<span data-ttu-id="10395-175">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="10395-175">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="10395-176">Calificadores: **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="10395-176">Qualifiers: **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="10395-177">Peso aplicado a la ACL extendida.</span><span class="sxs-lookup"><span data-stu-id="10395-177">The weight applied to the extended ACL.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="10395-178">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10395-178">Requirements</span></span>



| <span data-ttu-id="10395-179">Requisito</span><span class="sxs-lookup"><span data-stu-id="10395-179">Requirement</span></span> | <span data-ttu-id="10395-180">Value</span><span class="sxs-lookup"><span data-stu-id="10395-180">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10395-181">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="10395-181">Minimum supported client</span></span><br/> | <span data-ttu-id="10395-182">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="10395-182">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="10395-183">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="10395-183">Minimum supported server</span></span><br/> | <span data-ttu-id="10395-184">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="10395-184">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="10395-185">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="10395-185">Namespace</span></span><br/>                | <span data-ttu-id="10395-186">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="10395-186">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="10395-187">MOF</span><span class="sxs-lookup"><span data-stu-id="10395-187">MOF</span></span><br/>                      | <dl> <span data-ttu-id="10395-188"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="10395-188"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="10395-189">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="10395-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10395-190"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="10395-190"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="10395-191">Vea también</span><span class="sxs-lookup"><span data-stu-id="10395-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10395-192">**MSVM \_ EthernetSwitchPortFeatureSettingData**</span><span class="sxs-lookup"><span data-stu-id="10395-192">**Msvm\_EthernetSwitchPortFeatureSettingData**</span></span>](msvm-ethernetswitchportfeaturesettingdata.md)
</dt> </dl>

 

