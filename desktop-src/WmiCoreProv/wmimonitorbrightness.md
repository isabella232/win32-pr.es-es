---
description: Representa los parámetros de brillo de un monitor de equipo.
ms.assetid: 01fa3efc-2a1d-4405-989f-2c180842c6b9
title: Clase WmiMonitorBrightness
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightness
- WmiMonitorBrightness.Active
- WmiMonitorBrightness.CurrentBrightness
- WmiMonitorBrightness.InstanceName
- WmiMonitorBrightness.Level
- WmiMonitorBrightness.Levels
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: b8d16c8dc20291a03fb205441c8826c85125970c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707115"
---
# <a name="wmimonitorbrightness-class"></a><span data-ttu-id="fef94-103">Clase WmiMonitorBrightness</span><span class="sxs-lookup"><span data-stu-id="fef94-103">WmiMonitorBrightness class</span></span>

<span data-ttu-id="fef94-104">La clase WMI **WmiMonitorBrightness** representa los parámetros de brillo de un monitor de equipo.</span><span class="sxs-lookup"><span data-stu-id="fef94-104">The **WmiMonitorBrightness** WMI class represents the brightness parameters of a computer monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="fef94-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fef94-105">Syntax</span></span>

``` syntax
class WmiMonitorBrightness : MSMonitorClass
{
  boolean Active;
  uint8   CurrentBrightness;
          InstanceName;
  uint8   Level[];
  uint32  Levels;
};
```

## <a name="members"></a><span data-ttu-id="fef94-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="fef94-106">Members</span></span>

<span data-ttu-id="fef94-107">La clase **WmiMonitorBrightness** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="fef94-107">The **WmiMonitorBrightness** class has these types of members:</span></span>

-   [<span data-ttu-id="fef94-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fef94-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fef94-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fef94-109">Properties</span></span>

<span data-ttu-id="fef94-110">La clase **WmiMonitorBrightness** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="fef94-110">The **WmiMonitorBrightness** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fef94-111">**Activo**</span><span class="sxs-lookup"><span data-stu-id="fef94-111">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fef94-112">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="fef94-112">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fef94-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fef94-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fef94-114">Indica si el monitor de destino está activo.</span><span class="sxs-lookup"><span data-stu-id="fef94-114">Indicates if the target monitor is active.</span></span>

</dd> <dt>

<span data-ttu-id="fef94-115">**CurrentBrightness**</span><span class="sxs-lookup"><span data-stu-id="fef94-115">**CurrentBrightness**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fef94-116">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="fef94-116">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="fef94-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fef94-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fef94-118">Brillo actual.</span><span class="sxs-lookup"><span data-stu-id="fef94-118">Current brightness.</span></span> <span data-ttu-id="fef94-119">Este valor debe ser un valor obtenido de *los niveles*.</span><span class="sxs-lookup"><span data-stu-id="fef94-119">This value must be a value taken from *Levels*.</span></span>

<span data-ttu-id="fef94-120">Ejemplo: 100</span><span class="sxs-lookup"><span data-stu-id="fef94-120">Example: 100</span></span>

</dd> <dt>

<span data-ttu-id="fef94-121">InstanceName</span><span class="sxs-lookup"><span data-stu-id="fef94-121">InstanceName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fef94-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fef94-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fef94-123">Calificadores: clave</span><span class="sxs-lookup"><span data-stu-id="fef94-123">Qualifiers: Key</span></span>
</dt> </dl>

<span data-ttu-id="fef94-124">Nombre de la instancia de monitor específica.</span><span class="sxs-lookup"><span data-stu-id="fef94-124">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="fef94-125">**Level**</span><span class="sxs-lookup"><span data-stu-id="fef94-125">**Level**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fef94-126">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="fef94-126">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="fef94-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fef94-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fef94-128">Matriz que contiene los niveles de brillo posibles.</span><span class="sxs-lookup"><span data-stu-id="fef94-128">Array containing the possible brightness levels.</span></span>

<span data-ttu-id="fef94-129">Ejemplo: \[ 0, 1, 2,..., 100 \] .</span><span class="sxs-lookup"><span data-stu-id="fef94-129">Example: \[0, 1, 2, ..., 100\].</span></span>

</dd> <dt>

<span data-ttu-id="fef94-130">**Niveles**</span><span class="sxs-lookup"><span data-stu-id="fef94-130">**Levels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fef94-131">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fef94-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fef94-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fef94-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fef94-133">El número total de niveles de brillo que admite el monitor, tal como se describe en *LEVEL*.</span><span class="sxs-lookup"><span data-stu-id="fef94-133">The total number of brightness levels the monitor supports, as described in *Level*.</span></span>

<span data-ttu-id="fef94-134">Ejemplo: 101</span><span class="sxs-lookup"><span data-stu-id="fef94-134">Example: 101</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="fef94-135">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="fef94-135">Examples</span></span>

<span data-ttu-id="fef94-136">Para obtener más información y ejemplos de código sobre el uso de esta clase en PowerShell, vea [usar PowerShell para notificar y establecer el brillo del monitor](https://blogs.technet.com/b/heyscriptingguy/archive/2013/07/25/use-powershell-to-report-and-set-monitor-brightness.aspx).</span><span class="sxs-lookup"><span data-stu-id="fef94-136">For more information and code samples on using this class in PowerShell, see [Use PowerShell to Report and Set Monitor Brightness](https://blogs.technet.com/b/heyscriptingguy/archive/2013/07/25/use-powershell-to-report-and-set-monitor-brightness.aspx).</span></span>

## <a name="requirements"></a><span data-ttu-id="fef94-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fef94-137">Requirements</span></span>



| <span data-ttu-id="fef94-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="fef94-138">Requirement</span></span> | <span data-ttu-id="fef94-139">Value</span><span class="sxs-lookup"><span data-stu-id="fef94-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fef94-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fef94-140">Minimum supported client</span></span><br/> | <span data-ttu-id="fef94-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fef94-141">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="fef94-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fef94-142">Minimum supported server</span></span><br/> | <span data-ttu-id="fef94-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fef94-143">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="fef94-144">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="fef94-144">Namespace</span></span><br/>                | <span data-ttu-id="fef94-145">\\WMI raíz</span><span class="sxs-lookup"><span data-stu-id="fef94-145">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="fef94-146">MOF</span><span class="sxs-lookup"><span data-stu-id="fef94-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fef94-147"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fef94-147"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="fef94-148">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fef94-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fef94-149"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fef94-149"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fef94-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="fef94-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fef94-151">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="fef94-151">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




