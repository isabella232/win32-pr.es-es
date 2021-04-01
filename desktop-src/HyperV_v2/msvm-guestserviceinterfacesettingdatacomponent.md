---
description: Clase de asociación entre un componente de interfaz de servicio invitado y el recurso de servicio invitado.
ms.assetid: 4c16c3ab-4137-40ab-be2e-f385d8e36a41
title: Msvm_GuestServiceInterfaceSettingDataComponent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestServiceInterfaceSettingDataComponent
- Msvm_GuestServiceInterfaceSettingDataComponent.GroupComponent
- Msvm_GuestServiceInterfaceSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 988975fea1fd519a5e3917faeb73d345334d74b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275570"
---
# <a name="msvm_guestserviceinterfacesettingdatacomponent-class"></a><span data-ttu-id="3aa74-103">MSVM \_ GuestServiceInterfaceSettingDataComponent (clase)</span><span class="sxs-lookup"><span data-stu-id="3aa74-103">Msvm\_GuestServiceInterfaceSettingDataComponent class</span></span>

<span data-ttu-id="3aa74-104">Clase de asociación entre un componente de interfaz de servicio invitado y el recurso de servicio invitado.</span><span class="sxs-lookup"><span data-stu-id="3aa74-104">Association class between a guest service interface component and the guest service resource.</span></span>

<span data-ttu-id="3aa74-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="3aa74-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3aa74-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3aa74-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestServiceInterfaceSettingDataComponent : CIM_Component
{
  Msvm_GuestServiceInterfaceComponentSettingData REF GroupComponent;
  CIM_SettingData                                REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="3aa74-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="3aa74-107">Members</span></span>

<span data-ttu-id="3aa74-108">La clase **MSVM \_ GuestServiceInterfaceSettingDataComponent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="3aa74-108">The **Msvm\_GuestServiceInterfaceSettingDataComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="3aa74-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3aa74-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3aa74-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3aa74-110">Properties</span></span>

<span data-ttu-id="3aa74-111">La clase **MSVM \_ GuestServiceInterfaceSettingDataComponent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="3aa74-111">The **Msvm\_GuestServiceInterfaceSettingDataComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3aa74-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="3aa74-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3aa74-113">Tipo de datos: **MSVM \_ GuestServiceInterfaceComponentSettingData**</span><span class="sxs-lookup"><span data-stu-id="3aa74-113">Data type: **Msvm\_GuestServiceInterfaceComponentSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="3aa74-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3aa74-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3aa74-115">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="3aa74-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="3aa74-116">Un [**MSVM \_ GuestServiceInterfaceComponentSettingData**](msvm-guestserviceinterfacecomponentsettingdata.md) que hace referencia al componente de la interfaz de servicio invitado.</span><span class="sxs-lookup"><span data-stu-id="3aa74-116">A [**Msvm\_GuestServiceInterfaceComponentSettingData**](msvm-guestserviceinterfacecomponentsettingdata.md) referencing the guest service interface component.</span></span>

</dd> <dt>

<span data-ttu-id="3aa74-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="3aa74-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3aa74-118">Tipo de datos **: \_ SettingData de CIM**</span><span class="sxs-lookup"><span data-stu-id="3aa74-118">Data type: **CIM\_SettingData**</span></span>
</dt> <dt>

<span data-ttu-id="3aa74-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3aa74-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3aa74-120">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="3aa74-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="3aa74-121">Un [**\_ SettingData de CIM**](cim-settingdata.md) que hace referencia al recurso de servicio invitado.</span><span class="sxs-lookup"><span data-stu-id="3aa74-121">A [**CIM\_SettingData**](cim-settingdata.md) that references the guest service resource.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3aa74-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3aa74-122">Requirements</span></span>



| <span data-ttu-id="3aa74-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="3aa74-123">Requirement</span></span> | <span data-ttu-id="3aa74-124">Value</span><span class="sxs-lookup"><span data-stu-id="3aa74-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3aa74-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3aa74-125">Minimum supported client</span></span><br/> | <span data-ttu-id="3aa74-126">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="3aa74-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="3aa74-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3aa74-127">Minimum supported server</span></span><br/> | <span data-ttu-id="3aa74-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="3aa74-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="3aa74-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3aa74-129">Namespace</span></span><br/>                | <span data-ttu-id="3aa74-130">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="3aa74-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="3aa74-131">MOF</span><span class="sxs-lookup"><span data-stu-id="3aa74-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3aa74-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3aa74-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3aa74-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3aa74-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3aa74-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3aa74-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3aa74-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="3aa74-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3aa74-136">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="3aa74-136">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

