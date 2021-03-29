---
description: Representa la configuración de seguridad en tiempo de ejecución de un ComputerSystem de CIM \_ .
ms.assetid: fa4448dc-9353-475f-ac9b-5c50f36360d8
title: Msvm_SecurityElement (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityElement
- Msvm_SecurityElement.SystemCreationClassName
- Msvm_SecurityElement.SystemName
- Msvm_SecurityElement.CreationClassName
- Msvm_SecurityElement.Shielded
- Msvm_SecurityElement.EncryptStateAndVmMigrationTrafficEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0f0de0fe1a515db0e7b1d8d49b96b61500703480
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003223"
---
# <a name="msvm_securityelement-class"></a><span data-ttu-id="f6470-103">MSVM ( \_ clase de SecurityElement)</span><span class="sxs-lookup"><span data-stu-id="f6470-103">Msvm\_SecurityElement class</span></span>

<span data-ttu-id="f6470-104">Representa la configuración de seguridad en tiempo de ejecución de un [**\_ ComputerSystem de CIM**](cim-computersystem.md).</span><span class="sxs-lookup"><span data-stu-id="f6470-104">Represents the runtime security settings of a [**CIM\_ComputerSystem**](cim-computersystem.md).</span></span>

<span data-ttu-id="f6470-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="f6470-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6470-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f6470-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SecurityElement : CIM_EnabledLogicalElement
{
  string  SystemCreationClassName;
  string  SystemName;
  string  CreationClassName;
  boolean Shielded;
  boolean EncryptStateAndVmMigrationTrafficEnabled;
};
```

## <a name="members"></a><span data-ttu-id="f6470-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="f6470-107">Members</span></span>

<span data-ttu-id="f6470-108">La **clase \_ SecurityElement MSVM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f6470-108">The **Msvm\_SecurityElement** class has these types of members:</span></span>

-   [<span data-ttu-id="f6470-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f6470-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f6470-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f6470-110">Properties</span></span>

<span data-ttu-id="f6470-111">La **clase \_ SecurityElement MSVM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f6470-111">The **Msvm\_SecurityElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f6470-112">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f6470-112">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6470-113">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f6470-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6470-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6470-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6470-115">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f6470-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f6470-116">El nombre de la clase o la subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="f6470-116">The name of the class or the subclass used in the creation of an instance.</span></span> <span data-ttu-id="f6470-117">Cuando se usa con las otras propiedades de clave de esta clase, **CreationClassName** permite que todas las instancias de esta clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="f6470-117">When used with the other key properties of this class, **CreationClassName** allows all instances of this class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="f6470-118">**EncryptStateAndVmMigrationTrafficEnabled**</span><span class="sxs-lookup"><span data-stu-id="f6470-118">**EncryptStateAndVmMigrationTrafficEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6470-119">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="f6470-119">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f6470-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6470-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6470-121">Indica si la máquina virtual tiene actualmente su estado y el tráfico de migración cifrado.</span><span class="sxs-lookup"><span data-stu-id="f6470-121">Indicates whether the VM is currently having its state and migration traffic encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="f6470-122">**Blindada**</span><span class="sxs-lookup"><span data-stu-id="f6470-122">**Shielded**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6470-123">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="f6470-123">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f6470-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6470-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6470-125">Indica si la máquina virtual está blindada actualmente.</span><span class="sxs-lookup"><span data-stu-id="f6470-125">Indicates whether the VM is currently shielded.</span></span>

</dd> <dt>

<span data-ttu-id="f6470-126">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f6470-126">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6470-127">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f6470-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6470-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6470-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6470-129">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**")</span><span class="sxs-lookup"><span data-stu-id="f6470-129">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="f6470-130">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="f6470-130">The creation class name of the scoping system.</span></span>

</dd> <dt>

<span data-ttu-id="f6470-131">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="f6470-131">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6470-132">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f6470-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6470-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6470-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6470-134">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Nombre**")</span><span class="sxs-lookup"><span data-stu-id="f6470-134">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="f6470-135">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="f6470-135">The name of the scoping system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f6470-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6470-136">Requirements</span></span>



| <span data-ttu-id="f6470-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6470-137">Requirement</span></span> | <span data-ttu-id="f6470-138">Value</span><span class="sxs-lookup"><span data-stu-id="f6470-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6470-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f6470-139">Minimum supported client</span></span><br/> | <span data-ttu-id="f6470-140">Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="f6470-140">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f6470-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f6470-141">Minimum supported server</span></span><br/> | <span data-ttu-id="f6470-142">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f6470-142">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="f6470-143">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f6470-143">Namespace</span></span><br/>                | <span data-ttu-id="f6470-144">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="f6470-144">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f6470-145">MOF</span><span class="sxs-lookup"><span data-stu-id="f6470-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f6470-146"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f6470-146"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f6470-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f6470-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6470-148"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f6470-148"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f6470-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="f6470-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6470-150">**\_ENABLEDLOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="f6470-150">**CIM\_EnabledLogicalElement**</span></span>](cim-enabledlogicalelement.md)
</dt> </dl>

 

