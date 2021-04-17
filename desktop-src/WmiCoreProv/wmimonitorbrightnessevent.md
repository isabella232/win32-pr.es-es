---
description: Representa un cambio en el brillo de un monitor.
ms.assetid: c2eb5630-a52f-4ad4-aaee-1cc8afef8c9e
title: Clase WmiMonitorBrightnessEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightnessEvent
- WmiMonitorBrightnessEvent.Active
- WmiMonitorBrightnessEvent.Brightness
- WmiMonitorBrightnessEvent.InstanceName
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 7e53f90627c959db0140b01cf3b3d385afcc6e73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706819"
---
# <a name="wmimonitorbrightnessevent-class"></a><span data-ttu-id="ea551-103">Clase WmiMonitorBrightnessEvent</span><span class="sxs-lookup"><span data-stu-id="ea551-103">WmiMonitorBrightnessEvent class</span></span>

<span data-ttu-id="ea551-104">La clase de eventos **WmiMonitorBrightnessEvent** WMI representa un cambio en el brillo de un monitor.</span><span class="sxs-lookup"><span data-stu-id="ea551-104">The **WmiMonitorBrightnessEvent** WMI event class represents a change in the brightness of a monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea551-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ea551-105">Syntax</span></span>

``` syntax
class WmiMonitorBrightnessEvent : WMIEvent
{
  boolean Active;
  uint8   Brightness;
  string  InstanceName;
};
```

## <a name="members"></a><span data-ttu-id="ea551-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="ea551-106">Members</span></span>

<span data-ttu-id="ea551-107">La clase **WmiMonitorBrightnessEvent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="ea551-107">The **WmiMonitorBrightnessEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="ea551-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ea551-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ea551-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ea551-109">Properties</span></span>

<span data-ttu-id="ea551-110">La clase **WmiMonitorBrightnessEvent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="ea551-110">The **WmiMonitorBrightnessEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ea551-111">**Activo**</span><span class="sxs-lookup"><span data-stu-id="ea551-111">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea551-112">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="ea551-112">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ea551-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ea551-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea551-114">Indica el monitor activo.</span><span class="sxs-lookup"><span data-stu-id="ea551-114">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="ea551-115">**Luminosidad**</span><span class="sxs-lookup"><span data-stu-id="ea551-115">**Brightness**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea551-116">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="ea551-116">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="ea551-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ea551-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea551-118">Brillo del monitor actual como un porcentaje.</span><span class="sxs-lookup"><span data-stu-id="ea551-118">Current monitor brightness as a percentage.</span></span>

</dd> <dt>

<span data-ttu-id="ea551-119">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="ea551-119">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea551-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ea551-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea551-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ea551-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea551-122">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="ea551-122">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="ea551-123">Nombre de la instancia de monitor específica.</span><span class="sxs-lookup"><span data-stu-id="ea551-123">Name of the specific monitor instance.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ea551-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea551-124">Requirements</span></span>



| <span data-ttu-id="ea551-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea551-125">Requirement</span></span> | <span data-ttu-id="ea551-126">Value</span><span class="sxs-lookup"><span data-stu-id="ea551-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ea551-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ea551-127">Minimum supported client</span></span><br/> | <span data-ttu-id="ea551-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ea551-128">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="ea551-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ea551-129">Minimum supported server</span></span><br/> | <span data-ttu-id="ea551-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ea551-130">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ea551-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ea551-131">Namespace</span></span><br/>                | <span data-ttu-id="ea551-132">\\WMI raíz</span><span class="sxs-lookup"><span data-stu-id="ea551-132">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="ea551-133">MOF</span><span class="sxs-lookup"><span data-stu-id="ea551-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ea551-134"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ea551-134"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="ea551-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ea551-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea551-136"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea551-136"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea551-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="ea551-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea551-138">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="ea551-138">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> <dt>

[<span data-ttu-id="ea551-139">**WmiMonitorBrightness**</span><span class="sxs-lookup"><span data-stu-id="ea551-139">**WmiMonitorBrightness**</span></span>](wmimonitorbrightness.md)
</dt> <dt>

[<span data-ttu-id="ea551-140">Recibir un evento de WMI</span><span class="sxs-lookup"><span data-stu-id="ea551-140">Receiving a WMI Event</span></span>](/windows/desktop/WmiSdk/receiving-a-wmi-event)
</dt> </dl>

 

