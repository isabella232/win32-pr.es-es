---
description: Representa un dispositivo lógico que permite a un usuario introducir, ver o oír datos en el sistema del equipo.
ms.assetid: 95f88a63-3a2a-4b8c-9849-564dac254933
title: CIM_UserDevice (clase, administración de Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_UserDevice
- CIM_UserDevice.IsLocked
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8776c0b5e9ddf1653747b82e94040197e4c56f27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908729"
---
# <a name="cim_userdevice-class-hyper-v-management"></a><span data-ttu-id="dbec4-103">CIM_UserDevice (clase, administración de Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="dbec4-103">CIM_UserDevice class (Hyper-V management)</span></span>

<span data-ttu-id="dbec4-104">Representa un dispositivo lógico que permite a un usuario introducir, ver o oír datos en el sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="dbec4-104">Represents a logical device that allows a user to input, view or hear data on the computer system.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbec4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dbec4-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.6.0"), UMLPackagePath("CIM::Device::UserDevices"), AMENDMENT]
class CIM_UserDevice : CIM_LogicalDevice
{
  boolean IsLocked;
};
```

## <a name="members"></a><span data-ttu-id="dbec4-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="dbec4-106">Members</span></span>

<span data-ttu-id="dbec4-107">La clase **CIM \_ UserDevice** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="dbec4-107">The **CIM\_UserDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="dbec4-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dbec4-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dbec4-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dbec4-109">Properties</span></span>

<span data-ttu-id="dbec4-110">La clase **CIM \_ UserDevice** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="dbec4-110">The **CIM\_UserDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dbec4-111">**IsLocked**</span><span class="sxs-lookup"><span data-stu-id="dbec4-111">**IsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbec4-112">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="dbec4-112">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dbec4-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dbec4-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbec4-114">**true** si el dispositivo está bloqueado, lo que impide la entrada o salida del usuario; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="dbec4-114">**true** if the device is locked, preventing user input or output; otherwise, **false**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dbec4-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dbec4-115">Requirements</span></span>



| <span data-ttu-id="dbec4-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="dbec4-116">Requirement</span></span> | <span data-ttu-id="dbec4-117">Value</span><span class="sxs-lookup"><span data-stu-id="dbec4-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbec4-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dbec4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="dbec4-119">Windows 8</span><span class="sxs-lookup"><span data-stu-id="dbec4-119">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="dbec4-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dbec4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="dbec4-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="dbec4-121">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="dbec4-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="dbec4-122">Namespace</span></span><br/>                | <span data-ttu-id="dbec4-123">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="dbec4-123">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="dbec4-124">MOF</span><span class="sxs-lookup"><span data-stu-id="dbec4-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dbec4-125"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dbec4-125"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="dbec4-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="dbec4-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dbec4-127"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dbec4-127"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="dbec4-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="dbec4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbec4-129">**LogicalDevice de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="dbec4-129">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




