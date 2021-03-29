---
description: Conecta un servicio de puente transparente a una entrada de reenvío dinámica (dirección MAC aprendida).
ms.assetid: CA083F15-1E75-4EB9-BE56-95742181FDAC
title: Msvm_TransparentBridgingDynamicForwarding (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TransparentBridgingDynamicForwarding
- Msvm_TransparentBridgingDynamicForwarding.Antecedent
- Msvm_TransparentBridgingDynamicForwarding.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 01b9d9c752d4781864c07ff24fca5f866a57ae54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001400"
---
# <a name="msvm_transparentbridgingdynamicforwarding-class"></a><span data-ttu-id="0f867-103">MSVM \_ TransparentBridgingDynamicForwarding (clase)</span><span class="sxs-lookup"><span data-stu-id="0f867-103">Msvm\_TransparentBridgingDynamicForwarding class</span></span>

<span data-ttu-id="0f867-104">Conecta un servicio de puente transparente a una entrada de reenvío dinámica (dirección MAC aprendida).</span><span class="sxs-lookup"><span data-stu-id="0f867-104">Connects a transparent bridging service to a dynamic forward entry (learned MAC address).</span></span>

<span data-ttu-id="0f867-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="0f867-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f867-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0f867-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TransparentBridgingDynamicForwarding : CIM_TransparentBridgingDynamicForwarding
{
  Msvm_TransparentBridgingService REF Antecedent;
  Msvm_DynamicForwardingEntry     REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="0f867-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="0f867-107">Members</span></span>

<span data-ttu-id="0f867-108">La clase **MSVM \_ TransparentBridgingDynamicForwarding** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="0f867-108">The **Msvm\_TransparentBridgingDynamicForwarding** class has these types of members:</span></span>

-   [<span data-ttu-id="0f867-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0f867-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0f867-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0f867-110">Properties</span></span>

<span data-ttu-id="0f867-111">La clase **MSVM \_ TransparentBridgingDynamicForwarding** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="0f867-111">The **Msvm\_TransparentBridgingDynamicForwarding** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0f867-112">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="0f867-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f867-113">Tipo de datos: **[ **MSVM \_ TransparentBridgingService**](msvm-transparentbridgingservice.md)**</span><span class="sxs-lookup"><span data-stu-id="0f867-113">Data type: **[**Msvm\_TransparentBridgingService**](msvm-transparentbridgingservice.md)**</span></span>
</dt> <dt>

<span data-ttu-id="0f867-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0f867-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f867-115">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="0f867-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="0f867-116">Referencia a una instancia de la clase [**MSVM \_ TransparentBridgingService**](msvm-transparentbridgingservice.md) que representa el servicio de puente transparente.</span><span class="sxs-lookup"><span data-stu-id="0f867-116">A reference to an instance of the [**Msvm\_TransparentBridgingService**](msvm-transparentbridgingservice.md) class that represents the transparent bridging service.</span></span>

</dd> <dt>

<span data-ttu-id="0f867-117">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="0f867-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f867-118">Tipo de datos: **[ **MSVM \_ DynamicForwardingEntry**](msvm-dynamicforwardingentry.md)**</span><span class="sxs-lookup"><span data-stu-id="0f867-118">Data type: **[**Msvm\_DynamicForwardingEntry**](msvm-dynamicforwardingentry.md)**</span></span>
</dt> <dt>

<span data-ttu-id="0f867-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0f867-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f867-120">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="0f867-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="0f867-121">Referencia a una instancia de la clase [**MSVM \_ DynamicForwardingEntry**](msvm-dynamicforwardingentry.md) que representa la entrada de reenvío dinámico de la base de datos de reenvío.</span><span class="sxs-lookup"><span data-stu-id="0f867-121">A reference to an instance of the [**Msvm\_DynamicForwardingEntry**](msvm-dynamicforwardingentry.md) class that represents the dynamic forwarding entry of the forwarding database.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0f867-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0f867-122">Remarks</span></span>

<span data-ttu-id="0f867-123">El acceso a la clase **MSVM \_ TransparentBridgingDynamicForwarding** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="0f867-123">Access to the **Msvm\_TransparentBridgingDynamicForwarding** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="0f867-124">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="0f867-124">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="0f867-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f867-125">Requirements</span></span>



| <span data-ttu-id="0f867-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f867-126">Requirement</span></span> | <span data-ttu-id="0f867-127">Value</span><span class="sxs-lookup"><span data-stu-id="0f867-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f867-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0f867-128">Minimum supported client</span></span><br/> | <span data-ttu-id="0f867-129">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="0f867-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0f867-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0f867-130">Minimum supported server</span></span><br/> | <span data-ttu-id="0f867-131">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="0f867-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0f867-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0f867-132">Namespace</span></span><br/>                | <span data-ttu-id="0f867-133">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="0f867-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0f867-134">MOF</span><span class="sxs-lookup"><span data-stu-id="0f867-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0f867-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0f867-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0f867-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0f867-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f867-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0f867-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0f867-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="0f867-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f867-139">**\_TRANSPARENTBRIDGINGDYNAMICFORWARDING CIM**</span><span class="sxs-lookup"><span data-stu-id="0f867-139">**CIM\_TransparentBridgingDynamicForwarding**</span></span>](cim-transparentbridgingdynamicforwarding.md)
</dt> <dt>

[<span data-ttu-id="0f867-140">**\_TRANSPARENTBRIDGINGDYNAMICFORWARDING CIM**</span><span class="sxs-lookup"><span data-stu-id="0f867-140">**CIM\_TransparentBridgingDynamicForwarding**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-transparentbridgingdynamicforwarding)
</dt> </dl>

 

