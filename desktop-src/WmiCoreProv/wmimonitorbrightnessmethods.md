---
description: Contiene métodos que administran el brillo del monitor.
ms.assetid: e7e4139e-b985-4163-9c95-03008a2cc8cb
title: Clase WmiMonitorBrightnessMethods
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightnessMethods
- WmiMonitorBrightnessMethods.Active
- WmiMonitorBrightnessMethods.InstanceName
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 36fe823703d5d5e4f1f6008d02c600828fe2b53f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678112"
---
# <a name="wmimonitorbrightnessmethods-class"></a><span data-ttu-id="2d07f-103">Clase WmiMonitorBrightnessMethods</span><span class="sxs-lookup"><span data-stu-id="2d07f-103">WmiMonitorBrightnessMethods class</span></span>

<span data-ttu-id="2d07f-104">La clase WMI **WmiMonitorBrightnessMethods** contiene métodos que administran el brillo del monitor.</span><span class="sxs-lookup"><span data-stu-id="2d07f-104">The **WmiMonitorBrightnessMethods** WMI class contains methods that manage monitor brightness.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d07f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2d07f-105">Syntax</span></span>

``` syntax
class WmiMonitorBrightnessMethods
{
  boolean Active;
  string  InstanceName;
};
```

## <a name="members"></a><span data-ttu-id="2d07f-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="2d07f-106">Members</span></span>

<span data-ttu-id="2d07f-107">La clase **WmiMonitorBrightnessMethods** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2d07f-107">The **WmiMonitorBrightnessMethods** class has these types of members:</span></span>

-   [<span data-ttu-id="2d07f-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="2d07f-108">Methods</span></span>](#wmimonitorbrightnessmethods-class)
-   [<span data-ttu-id="2d07f-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2d07f-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2d07f-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="2d07f-110">Methods</span></span>

<span data-ttu-id="2d07f-111">La clase **WmiMonitorBrightnessMethods** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="2d07f-111">The **WmiMonitorBrightnessMethods** class has these methods.</span></span>



| <span data-ttu-id="2d07f-112">Método</span><span class="sxs-lookup"><span data-stu-id="2d07f-112">Method</span></span>                                                                                                         | <span data-ttu-id="2d07f-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="2d07f-113">Description</span></span>                                                    |
|:---------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------|
| [<span data-ttu-id="2d07f-114">**WmiRevertToPolicyBrightness**</span><span class="sxs-lookup"><span data-stu-id="2d07f-114">**WmiRevertToPolicyBrightness**</span></span>](wmireverttopolicybrightness-method-in-class-wmimonitorbrightnessmethods.md) | <span data-ttu-id="2d07f-115">Vuelve a establecer el brillo en la configuración de directiva.</span><span class="sxs-lookup"><span data-stu-id="2d07f-115">Sets the brightness back to the policy setting.</span></span><br/>     |
| [<span data-ttu-id="2d07f-116">**WmiSetALSBrightness**</span><span class="sxs-lookup"><span data-stu-id="2d07f-116">**WmiSetALSBrightness**</span></span>](wmisetalsbrightness-method-in-class-wmimonitorbrightnessmethods.md)                 | <span data-ttu-id="2d07f-117">Establece el valor de brillo del sensor de luz ambiente.</span><span class="sxs-lookup"><span data-stu-id="2d07f-117">Sets the ambient light sensor brightness value.</span></span><br/>     |
| [<span data-ttu-id="2d07f-118">**WmiSetALSBrightnessState**</span><span class="sxs-lookup"><span data-stu-id="2d07f-118">**WmiSetALSBrightnessState**</span></span>](wmisetalsbrightnessstate-method-in-class-wmimonitorbrightnessmethods.md)       | <span data-ttu-id="2d07f-119">Controla el estado de brillo del sensor de luz ambiente.</span><span class="sxs-lookup"><span data-stu-id="2d07f-119">Controls the ambient light sensor brightness state.</span></span><br/> |
| [<span data-ttu-id="2d07f-120">**WmiSetBrightness**</span><span class="sxs-lookup"><span data-stu-id="2d07f-120">**WmiSetBrightness**</span></span>](wmisetbrightness-method-in-class-wmimonitorbrightnessmethods.md)                       | <span data-ttu-id="2d07f-121">Establece el brillo del monitor.</span><span class="sxs-lookup"><span data-stu-id="2d07f-121">Sets the monitor brightness.</span></span><br/>                        |



 

### <a name="properties"></a><span data-ttu-id="2d07f-122">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2d07f-122">Properties</span></span>

<span data-ttu-id="2d07f-123">La clase **WmiMonitorBrightnessMethods** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="2d07f-123">The **WmiMonitorBrightnessMethods** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2d07f-124">**Activo**</span><span class="sxs-lookup"><span data-stu-id="2d07f-124">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d07f-125">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2d07f-125">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2d07f-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2d07f-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d07f-127">Indica el monitor activo.</span><span class="sxs-lookup"><span data-stu-id="2d07f-127">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="2d07f-128">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="2d07f-128">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d07f-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2d07f-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d07f-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2d07f-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d07f-131">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="2d07f-131">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="2d07f-132">Nombre de la instancia de monitor específica.</span><span class="sxs-lookup"><span data-stu-id="2d07f-132">Name of the specific monitor instance.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2d07f-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d07f-133">Requirements</span></span>



| <span data-ttu-id="2d07f-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d07f-134">Requirement</span></span> | <span data-ttu-id="2d07f-135">Value</span><span class="sxs-lookup"><span data-stu-id="2d07f-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2d07f-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2d07f-136">Minimum supported client</span></span><br/> | <span data-ttu-id="2d07f-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2d07f-137">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="2d07f-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2d07f-138">Minimum supported server</span></span><br/> | <span data-ttu-id="2d07f-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2d07f-139">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="2d07f-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2d07f-140">Namespace</span></span><br/>                | <span data-ttu-id="2d07f-141">\\WMI raíz</span><span class="sxs-lookup"><span data-stu-id="2d07f-141">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="2d07f-142">MOF</span><span class="sxs-lookup"><span data-stu-id="2d07f-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2d07f-143"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2d07f-143"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="2d07f-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2d07f-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d07f-145"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d07f-145"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d07f-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="2d07f-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d07f-147">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="2d07f-147">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




