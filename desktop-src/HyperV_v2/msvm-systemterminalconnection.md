---
description: Asocia una máquina virtual a una conexión de terminal.
ms.assetid: 31979FB8-3870-44D9-9720-AD99237C5268
title: Msvm_SystemTerminalConnection (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemTerminalConnection
- Msvm_SystemTerminalConnection.Antecedent
- Msvm_SystemTerminalConnection.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 368c25b8505ec7ddd29da3b95d95fc842602119e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686604"
---
# <a name="msvm_systemterminalconnection-class"></a><span data-ttu-id="66243-103">MSVM \_ SystemTerminalConnection (clase)</span><span class="sxs-lookup"><span data-stu-id="66243-103">Msvm\_SystemTerminalConnection class</span></span>

<span data-ttu-id="66243-104">Asocia una máquina virtual a una conexión de terminal.</span><span class="sxs-lookup"><span data-stu-id="66243-104">Associates a virtual machine with a terminal connection.</span></span>

<span data-ttu-id="66243-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="66243-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="66243-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="66243-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SystemTerminalConnection : CIM_HostedDependency
{
  Msvm_ComputerSystem     REF Antecedent;
  Msvm_TerminalConnection REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="66243-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="66243-107">Members</span></span>

<span data-ttu-id="66243-108">La clase **MSVM \_ SystemTerminalConnection** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="66243-108">The **Msvm\_SystemTerminalConnection** class has these types of members:</span></span>

-   [<span data-ttu-id="66243-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="66243-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="66243-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="66243-110">Properties</span></span>

<span data-ttu-id="66243-111">La clase **MSVM \_ SystemTerminalConnection** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="66243-111">The **Msvm\_SystemTerminalConnection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="66243-112">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="66243-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66243-113">Tipo de datos: **[ **MSVM \_ ComputerSystem**](msvm-computersystem.md)**</span><span class="sxs-lookup"><span data-stu-id="66243-113">Data type: **[**Msvm\_ComputerSystem**](msvm-computersystem.md)**</span></span>
</dt> <dt>

<span data-ttu-id="66243-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="66243-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66243-115">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="66243-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="66243-116">La máquina virtual a la que está conectada la conexión.</span><span class="sxs-lookup"><span data-stu-id="66243-116">The virtual machine to which the connection is attached.</span></span>

</dd> <dt>

<span data-ttu-id="66243-117">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="66243-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66243-118">Tipo de datos: **[ **MSVM \_ TerminalConnection**](msvm-terminalconnection.md)**</span><span class="sxs-lookup"><span data-stu-id="66243-118">Data type: **[**Msvm\_TerminalConnection**](msvm-terminalconnection.md)**</span></span>
</dt> <dt>

<span data-ttu-id="66243-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="66243-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66243-120">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="66243-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="66243-121">La conexión a la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="66243-121">The connection to the virtual machine.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="66243-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="66243-122">Remarks</span></span>

<span data-ttu-id="66243-123">El acceso a la clase **MSVM \_ SystemTerminalConnection** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="66243-123">Access to the **Msvm\_SystemTerminalConnection** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="66243-124">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="66243-124">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="66243-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66243-125">Requirements</span></span>



| <span data-ttu-id="66243-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="66243-126">Requirement</span></span> | <span data-ttu-id="66243-127">Value</span><span class="sxs-lookup"><span data-stu-id="66243-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66243-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="66243-128">Minimum supported client</span></span><br/> | <span data-ttu-id="66243-129">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="66243-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="66243-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="66243-130">Minimum supported server</span></span><br/> | <span data-ttu-id="66243-131">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="66243-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="66243-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="66243-132">Namespace</span></span><br/>                | <span data-ttu-id="66243-133">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="66243-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="66243-134">MOF</span><span class="sxs-lookup"><span data-stu-id="66243-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="66243-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="66243-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="66243-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="66243-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66243-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="66243-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="66243-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="66243-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66243-139">**\_HOSTEDDEPENDENCY CIM**</span><span class="sxs-lookup"><span data-stu-id="66243-139">**CIM\_HostedDependency**</span></span>](cim-hosteddependency.md)
</dt> <dt>

<span data-ttu-id="66243-140">[**\_HOSTEDDEPENDENCY CIM**](/previous-versions//cc136861(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="66243-140">[**CIM\_HostedDependency**](/previous-versions//cc136861(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="66243-141">Clases de vídeo</span><span class="sxs-lookup"><span data-stu-id="66243-141">Video Classes</span></span>](video-classes.md)
</dt> </dl>

 

