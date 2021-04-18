---
description: Representa un grupo de controladores que controlan la operación y la función de los dispositivos que inician los protocolos.
ms.assetid: fb6b65d4-3a1a-47b1-afc7-9b10e8eeaa32
title: CIM_ProtocolController (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProtocolController
- CIM_ProtocolController.MaxUnitsControlled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 27372bc57ad36f37689d75b3963ec0c4b1106956
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666234"
---
# <a name="cim_protocolcontroller-class"></a><span data-ttu-id="93a66-103">\_Clase ProtocolController de CIM</span><span class="sxs-lookup"><span data-stu-id="93a66-103">CIM\_ProtocolController class</span></span>

<span data-ttu-id="93a66-104">Representa un grupo de controladores que controlan la operación y la función de los dispositivos que inician los protocolos.</span><span class="sxs-lookup"><span data-stu-id="93a66-104">Represents a group of controllers that control the operation and function of devices that initiate protocols.</span></span>

## <a name="syntax"></a><span data-ttu-id="93a66-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="93a66-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.8.0"), UMLPackagePath("CIM::Device::ProtocolController"), AMENDMENT]
class CIM_ProtocolController : CIM_LogicalDevice
{
  uint32 MaxUnitsControlled;
};
```

## <a name="members"></a><span data-ttu-id="93a66-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="93a66-106">Members</span></span>

<span data-ttu-id="93a66-107">La clase **CIM \_ ProtocolController** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="93a66-107">The **CIM\_ProtocolController** class has these types of members:</span></span>

-   [<span data-ttu-id="93a66-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="93a66-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="93a66-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="93a66-109">Properties</span></span>

<span data-ttu-id="93a66-110">La clase **CIM \_ ProtocolController** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="93a66-110">The **CIM\_ProtocolController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="93a66-111">**MaxUnitsControlled**</span><span class="sxs-lookup"><span data-stu-id="93a66-111">**MaxUnitsControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93a66-112">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93a66-112">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93a66-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93a66-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93a66-114">Número máximo de unidades que se pueden controlar o a las que se tiene acceso a través del controlador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="93a66-114">The maximum number of units that can be controlled by or accessed through the protocol controller.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="93a66-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93a66-115">Requirements</span></span>



| <span data-ttu-id="93a66-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="93a66-116">Requirement</span></span> | <span data-ttu-id="93a66-117">Value</span><span class="sxs-lookup"><span data-stu-id="93a66-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93a66-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="93a66-118">Minimum supported client</span></span><br/> | <span data-ttu-id="93a66-119">Windows 8</span><span class="sxs-lookup"><span data-stu-id="93a66-119">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="93a66-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="93a66-120">Minimum supported server</span></span><br/> | <span data-ttu-id="93a66-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="93a66-121">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="93a66-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="93a66-122">Namespace</span></span><br/>                | <span data-ttu-id="93a66-123">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="93a66-123">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="93a66-124">MOF</span><span class="sxs-lookup"><span data-stu-id="93a66-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="93a66-125"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="93a66-125"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="93a66-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="93a66-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93a66-127"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="93a66-127"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="93a66-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="93a66-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93a66-129">**LogicalDevice de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="93a66-129">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




