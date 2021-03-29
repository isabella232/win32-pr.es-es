---
description: Proporciona información sobre la conectividad de red para una máquina virtual.
ms.assetid: 59503c1b-203b-46ec-8a65-f21a746f170f
title: Msvm_NetworkConnectionDiagnosticInformation (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_NetworkConnectionDiagnosticInformation
- Msvm_NetworkConnectionDiagnosticInformation.RoundTripTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 416392702e5bc06e54fe5a23b6784b87e98b7027
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002928"
---
# <a name="msvm_networkconnectiondiagnosticinformation-class"></a><span data-ttu-id="ab57e-103">MSVM \_ NetworkConnectionDiagnosticInformation (clase)</span><span class="sxs-lookup"><span data-stu-id="ab57e-103">Msvm\_NetworkConnectionDiagnosticInformation class</span></span>

<span data-ttu-id="ab57e-104">Proporciona información sobre la conectividad de red para una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ab57e-104">Provides information about the network connectivity for a virtual machine.</span></span>

<span data-ttu-id="ab57e-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="ab57e-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab57e-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ab57e-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_NetworkConnectionDiagnosticInformation
{
  uint32 RoundTripTime;
};
```

## <a name="members"></a><span data-ttu-id="ab57e-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="ab57e-107">Members</span></span>

<span data-ttu-id="ab57e-108">La clase **MSVM \_ NetworkConnectionDiagnosticInformation** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="ab57e-108">The **Msvm\_NetworkConnectionDiagnosticInformation** class has these types of members:</span></span>

-   [<span data-ttu-id="ab57e-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ab57e-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ab57e-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ab57e-110">Properties</span></span>

<span data-ttu-id="ab57e-111">La clase **MSVM \_ NetworkConnectionDiagnosticInformation** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="ab57e-111">The **Msvm\_NetworkConnectionDiagnosticInformation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ab57e-112">**RoundTripTime**</span><span class="sxs-lookup"><span data-stu-id="ab57e-112">**RoundTripTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab57e-113">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab57e-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab57e-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ab57e-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab57e-115">Tiempo de ida y vuelta para la solicitud de ping.</span><span class="sxs-lookup"><span data-stu-id="ab57e-115">The round trip time for the ping request.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ab57e-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab57e-116">Requirements</span></span>



| <span data-ttu-id="ab57e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab57e-117">Requirement</span></span> | <span data-ttu-id="ab57e-118">Value</span><span class="sxs-lookup"><span data-stu-id="ab57e-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab57e-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ab57e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ab57e-120">Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="ab57e-120">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="ab57e-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ab57e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ab57e-122">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="ab57e-122">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="ab57e-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ab57e-123">Namespace</span></span><br/>                | <span data-ttu-id="ab57e-124">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="ab57e-124">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ab57e-125">MOF</span><span class="sxs-lookup"><span data-stu-id="ab57e-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ab57e-126"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ab57e-126"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ab57e-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ab57e-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab57e-128"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ab57e-128"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

 




