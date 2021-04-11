---
description: Representa la configuración utilizada para probar la conectividad de red de una máquina virtual.
ms.assetid: d719d9c9-7ca9-40a0-ada8-185b8cd44c22
title: Msvm_NetworkConnectionDiagnosticSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_NetworkConnectionDiagnosticSettingData
- Msvm_NetworkConnectionDiagnosticSettingData.IsSender
- Msvm_NetworkConnectionDiagnosticSettingData.SenderIP
- Msvm_NetworkConnectionDiagnosticSettingData.ReceiverIP
- Msvm_NetworkConnectionDiagnosticSettingData.ReceiverMac
- Msvm_NetworkConnectionDiagnosticSettingData.IsolationId
- Msvm_NetworkConnectionDiagnosticSettingData.SequenceNumber
- Msvm_NetworkConnectionDiagnosticSettingData.PayloadSize
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ec0df1957df6c925cf12ce363c89a0bdad52d3e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083360"
---
# <a name="msvm_networkconnectiondiagnosticsettingdata-class"></a><span data-ttu-id="82e04-103">MSVM \_ NetworkConnectionDiagnosticSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="82e04-103">Msvm\_NetworkConnectionDiagnosticSettingData class</span></span>

<span data-ttu-id="82e04-104">Representa la configuración utilizada para probar la conectividad de red de una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="82e04-104">Represents the settings used to test the network connectivity of a virtual machine.</span></span> <span data-ttu-id="82e04-105">Lo usa el método [**DiagnoseNetworkConnection**](msvm-virtualsystemmanagementservice-diagnosenetworkconnection.md) de la [**clase \_ VirtualSystemManagementService de MSVM**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="82e04-105">Used by the [**DiagnoseNetworkConnection**](msvm-virtualsystemmanagementservice-diagnosenetworkconnection.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<span data-ttu-id="82e04-106">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="82e04-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="82e04-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="82e04-107">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_NetworkConnectionDiagnosticSettingData : CIM_SettingData
{
  boolean IsSender;
  string  SenderIP;
  string  ReceiverIP;
  string  ReceiverMac;
  uint32  IsolationId;
  uint32  SequenceNumber;
  uint32  PayloadSize;
};
```

## <a name="members"></a><span data-ttu-id="82e04-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="82e04-108">Members</span></span>

<span data-ttu-id="82e04-109">La clase **MSVM \_ NetworkConnectionDiagnosticSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="82e04-109">The **Msvm\_NetworkConnectionDiagnosticSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="82e04-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="82e04-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="82e04-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="82e04-111">Properties</span></span>

<span data-ttu-id="82e04-112">La clase **MSVM \_ NetworkConnectionDiagnosticSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="82e04-112">The **Msvm\_NetworkConnectionDiagnosticSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="82e04-113">**IsolationId**</span><span class="sxs-lookup"><span data-stu-id="82e04-113">**IsolationId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82e04-114">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="82e04-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="82e04-115">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="82e04-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="82e04-116">IDENTIFICADOR de aislamiento.</span><span class="sxs-lookup"><span data-stu-id="82e04-116">The Isolation ID.</span></span>

</dd> <dt>

<span data-ttu-id="82e04-117">**IsSender**</span><span class="sxs-lookup"><span data-stu-id="82e04-117">**IsSender**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82e04-118">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="82e04-118">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="82e04-119">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="82e04-119">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="82e04-120">Indica si este método se invoca en el remitente o en el receptor.</span><span class="sxs-lookup"><span data-stu-id="82e04-120">Indicates whether this method is being invoked at the sender or the receiver.</span></span>

</dd> <dt>

<span data-ttu-id="82e04-121">**PayloadSize**</span><span class="sxs-lookup"><span data-stu-id="82e04-121">**PayloadSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82e04-122">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="82e04-122">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="82e04-123">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="82e04-123">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="82e04-124">Tamaño de carga.</span><span class="sxs-lookup"><span data-stu-id="82e04-124">The payload size.</span></span>

</dd> <dt>

<span data-ttu-id="82e04-125">**ReceiverIP**</span><span class="sxs-lookup"><span data-stu-id="82e04-125">**ReceiverIP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82e04-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="82e04-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82e04-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="82e04-127">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="82e04-128">Dirección IP del receptor.</span><span class="sxs-lookup"><span data-stu-id="82e04-128">The receiver IP address.</span></span>

</dd> <dt>

<span data-ttu-id="82e04-129">**ReceiverMac**</span><span class="sxs-lookup"><span data-stu-id="82e04-129">**ReceiverMac**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82e04-130">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="82e04-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82e04-131">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="82e04-131">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="82e04-132">Dirección MAC del receptor.</span><span class="sxs-lookup"><span data-stu-id="82e04-132">The receiver MAC address.</span></span>

</dd> <dt>

<span data-ttu-id="82e04-133">**SenderIP**</span><span class="sxs-lookup"><span data-stu-id="82e04-133">**SenderIP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82e04-134">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="82e04-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82e04-135">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="82e04-135">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="82e04-136">Dirección IP del remitente.</span><span class="sxs-lookup"><span data-stu-id="82e04-136">The sender IP address.</span></span>

</dd> <dt>

<span data-ttu-id="82e04-137">**SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="82e04-137">**SequenceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82e04-138">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="82e04-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="82e04-139">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="82e04-139">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="82e04-140">El número de secuencia global.</span><span class="sxs-lookup"><span data-stu-id="82e04-140">The sequence number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="82e04-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82e04-141">Requirements</span></span>



| <span data-ttu-id="82e04-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="82e04-142">Requirement</span></span> | <span data-ttu-id="82e04-143">Value</span><span class="sxs-lookup"><span data-stu-id="82e04-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82e04-144">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="82e04-144">Minimum supported client</span></span><br/> | <span data-ttu-id="82e04-145">Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="82e04-145">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="82e04-146">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="82e04-146">Minimum supported server</span></span><br/> | <span data-ttu-id="82e04-147">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="82e04-147">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="82e04-148">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="82e04-148">Namespace</span></span><br/>                | <span data-ttu-id="82e04-149">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="82e04-149">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="82e04-150">MOF</span><span class="sxs-lookup"><span data-stu-id="82e04-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="82e04-151"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="82e04-151"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="82e04-152">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="82e04-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82e04-153"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="82e04-153"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="82e04-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="82e04-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82e04-155">**SettingData de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="82e04-155">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 




