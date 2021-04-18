---
description: Representa el registro de un servicio en la plataforma de Microsoft Hyper-V.
ms.assetid: 706557C2-49D6-453F-9DC0-2C655888EEBE
title: Msvm_VirtualizationComponentRegistration (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualizationComponentRegistration
- Msvm_VirtualizationComponentRegistration.Component
- Msvm_VirtualizationComponentRegistration.ResourceType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7e9704dcade0474a10ca60383280941ec2e3591b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686599"
---
# <a name="msvm_virtualizationcomponentregistration-class"></a><span data-ttu-id="45fed-103">MSVM \_ VirtualizationComponentRegistration (clase)</span><span class="sxs-lookup"><span data-stu-id="45fed-103">Msvm\_VirtualizationComponentRegistration class</span></span>

<span data-ttu-id="45fed-104">Representa el registro de un servicio en la plataforma de Microsoft Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="45fed-104">Represents the registration of a service in the Microsoft Hyper-V platform.</span></span>

<span data-ttu-id="45fed-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="45fed-105">The following syntax is simplified Managed Object Format (MOF) code.</span></span>

## <a name="syntax"></a><span data-ttu-id="45fed-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="45fed-106">Syntax</span></span>

``` syntax
class Msvm_VirtualizationComponentRegistration
{
  Msvm_VirtualizationComponent REF Component;
  Msvm_ResourceTypeDefinition  REF ResourceType;
};
```

## <a name="members"></a><span data-ttu-id="45fed-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="45fed-107">Members</span></span>

<span data-ttu-id="45fed-108">La clase **MSVM \_ VirtualizationComponentRegistration** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="45fed-108">The **Msvm\_VirtualizationComponentRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="45fed-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="45fed-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="45fed-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="45fed-110">Properties</span></span>

<span data-ttu-id="45fed-111">La clase **MSVM \_ VirtualizationComponentRegistration** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="45fed-111">The **Msvm\_VirtualizationComponentRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="45fed-112">**Componente**</span><span class="sxs-lookup"><span data-stu-id="45fed-112">**Component**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45fed-113">Tipo de datos: **[ **MSVM \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)**</span><span class="sxs-lookup"><span data-stu-id="45fed-113">Data type: **[**Msvm\_VirtualizationComponent**](msvm-virtualizationcomponent.md)**</span></span>
</dt> <dt>

<span data-ttu-id="45fed-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="45fed-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45fed-115">Referencia a una instancia de que describe el objeto COM que implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="45fed-115">A reference to an instance that describes the COM object that implements this class.</span></span>

</dd> <dt>

<span data-ttu-id="45fed-116">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="45fed-116">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45fed-117">Tipo de datos: **[ **MSVM \_ ResourceTypeDefinition**](msvm-resourcetypedefinition.md)**</span><span class="sxs-lookup"><span data-stu-id="45fed-117">Data type: **[**Msvm\_ResourceTypeDefinition**](msvm-resourcetypedefinition.md)**</span></span>
</dt> <dt>

<span data-ttu-id="45fed-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="45fed-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45fed-119">Referencia a una instancia de que describe un tipo de recurso admitido por el servicio.</span><span class="sxs-lookup"><span data-stu-id="45fed-119">A reference to an instance that describes a resource type supported by the service.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="45fed-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="45fed-120">Remarks</span></span>

<span data-ttu-id="45fed-121">El acceso a la clase **MSVM \_ VirtualizationComponentRegistration** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="45fed-121">Access to the **Msvm\_VirtualizationComponentRegistration** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="45fed-122">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="45fed-122">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="45fed-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45fed-123">Requirements</span></span>



| <span data-ttu-id="45fed-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="45fed-124">Requirement</span></span> | <span data-ttu-id="45fed-125">Value</span><span class="sxs-lookup"><span data-stu-id="45fed-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45fed-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="45fed-126">Minimum supported client</span></span><br/> | <span data-ttu-id="45fed-127">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="45fed-127">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="45fed-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="45fed-128">Minimum supported server</span></span><br/> | <span data-ttu-id="45fed-129">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="45fed-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="45fed-130">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="45fed-130">End of client support</span></span><br/>    | <span data-ttu-id="45fed-131">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="45fed-131">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="45fed-132">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="45fed-132">End of server support</span></span><br/>    | <span data-ttu-id="45fed-133">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="45fed-133">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="45fed-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="45fed-134">Namespace</span></span><br/>                | <span data-ttu-id="45fed-135">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="45fed-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="45fed-136">MOF</span><span class="sxs-lookup"><span data-stu-id="45fed-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="45fed-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="45fed-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="45fed-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="45fed-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45fed-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="45fed-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

