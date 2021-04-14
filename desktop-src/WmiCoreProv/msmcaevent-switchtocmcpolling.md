---
description: Representa el control de comprobación de la máquina (CMC) corregido que se va a cambiar del controlador de interrupción al sondeo. Esta clase solo está disponible en sistemas Windows de 64 bits.
ms.assetid: c5e99e13-0f65-40bc-8863-b2ca7ea221df
title: MSMCAEvent_SwitchToCMCPolling (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_SwitchToCMCPolling
- MSMCAEvent_SwitchToCMCPolling.Active
- MSMCAEvent_SwitchToCMCPolling.InstanceName
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: f7d0d543dc36054550d4ddf6cc1a77ce80cf1647
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360288"
---
# <a name="msmcaevent_switchtocmcpolling-class"></a><span data-ttu-id="568d5-104">MSMCAEvent \_ SwitchToCMCPolling (clase)</span><span class="sxs-lookup"><span data-stu-id="568d5-104">MSMCAEvent\_SwitchToCMCPolling class</span></span>

<span data-ttu-id="568d5-105">La clase **MSMCAEvent \_ SwitchToCMCPolling** representa el control correcto de la comprobación de la máquina (CMC) que se va a cambiar del controlador de interrupción al sondeo.</span><span class="sxs-lookup"><span data-stu-id="568d5-105">The **MSMCAEvent\_SwitchToCMCPolling** class represents the corrected machine check (CMC) handling to be switched from the interrupt driver to polling.</span></span> <span data-ttu-id="568d5-106">En algunos casos, el kernel sondea la capa de abstracción del sistema (SAL) en busca de cualquier error de plataforma CMC o corregido (CPE) que se produjera en el intervalo de sondeo anterior.</span><span class="sxs-lookup"><span data-stu-id="568d5-106">In some cases, the kernel polls the system abstraction layer (SAL) for any CMC or corrected platform error (CPE) that occurred within the previous polling interval.</span></span> <span data-ttu-id="568d5-107">Esta clase solo está disponible en sistemas Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="568d5-107">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="568d5-108">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="568d5-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="568d5-109">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="568d5-109">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="568d5-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="568d5-110">Syntax</span></span>

``` syntax
class MSMCAEvent_SwitchToCMCPolling : WMIEvent
{
  boolean Active;
  string  InstanceName;
};
```

## <a name="members"></a><span data-ttu-id="568d5-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="568d5-111">Members</span></span>

<span data-ttu-id="568d5-112">La clase **MSMCAEvent \_ SwitchToCMCPolling** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="568d5-112">The **MSMCAEvent\_SwitchToCMCPolling** class has these types of members:</span></span>

-   [<span data-ttu-id="568d5-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="568d5-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="568d5-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="568d5-114">Properties</span></span>

<span data-ttu-id="568d5-115">La clase **MSMCAEvent \_ SwitchToCMCPolling** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="568d5-115">The **MSMCAEvent\_SwitchToCMCPolling** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="568d5-116">**Activo**</span><span class="sxs-lookup"><span data-stu-id="568d5-116">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="568d5-117">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="568d5-117">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="568d5-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="568d5-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="568d5-119">**True** si esta instancia de la clase está activa; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="568d5-119">**TRUE**, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="568d5-120">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="568d5-120">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="568d5-121">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="568d5-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="568d5-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="568d5-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="568d5-123">Calificadores: [ **clave**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="568d5-123">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="568d5-124">Identificador único de esta instancia de la clase.</span><span class="sxs-lookup"><span data-stu-id="568d5-124">Unique identifier of this instance of the class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="568d5-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="568d5-125">Remarks</span></span>

<span data-ttu-id="568d5-126">La clase **MSMCAEvent \_ SwitchToCMCPolling** se deriva de [**WMIEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="568d5-126">The **MSMCAEvent\_SwitchToCMCPolling** class is derived from [**WMIEvent**](wmievent.md).</span></span>

<span data-ttu-id="568d5-127">La capa de abstracción del sistema (SAL) es código grabado en el ROM que el sistema operativo llama para realizar operaciones dependientes de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="568d5-127">The system abstraction layer (SAL) is code burned onto ROM that the operating system calls to perform platform-dependent operations.</span></span> <span data-ttu-id="568d5-128">Es similar al BIOS en una plataforma x86.</span><span class="sxs-lookup"><span data-stu-id="568d5-128">It is similar to the BIOS on an x86 platform.</span></span> <span data-ttu-id="568d5-129">En los casos en los que la plataforma no admite interrupciones para sondeos CMC o CPE, el sistema operativo sondea cada minuto y comprueba si se ha producido un error anteriormente.</span><span class="sxs-lookup"><span data-stu-id="568d5-129">In cases where the platform does not support interrupts for CMC or CPE polling, the operating system polls every minute, checking if an error occurred previously.</span></span> <span data-ttu-id="568d5-130">Si la plataforma admite interrupciones y el sistema operativo recibe una cantidad definida por el usuario de sondeos CMC o CPE en un minuto, se deshabilitará la interrupción y el sondeo.</span><span class="sxs-lookup"><span data-stu-id="568d5-130">If the platform does support interrupts and the operating system receives a user defined amount of CMC or CPE polls within one minute, then it disables the interrupt and poll.</span></span> <span data-ttu-id="568d5-131">Si el usuario no define el número de sondeos en un minuto, el sistema establece un valor predeterminado de 10 sondeos por minuto.</span><span class="sxs-lookup"><span data-stu-id="568d5-131">If the user does not define the number of polls within one minute, the system sets a default to 10 polls per minute.</span></span>

## <a name="requirements"></a><span data-ttu-id="568d5-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="568d5-132">Requirements</span></span>



| <span data-ttu-id="568d5-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="568d5-133">Requirement</span></span> | <span data-ttu-id="568d5-134">Value</span><span class="sxs-lookup"><span data-stu-id="568d5-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="568d5-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="568d5-135">Minimum supported client</span></span><br/> | <span data-ttu-id="568d5-136">Windows XP</span><span class="sxs-lookup"><span data-stu-id="568d5-136">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="568d5-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="568d5-137">Minimum supported server</span></span><br/> | <span data-ttu-id="568d5-138">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="568d5-138">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="568d5-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="568d5-139">Namespace</span></span><br/>                | <span data-ttu-id="568d5-140">\\WMI raíz</span><span class="sxs-lookup"><span data-stu-id="568d5-140">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="568d5-141">MOF</span><span class="sxs-lookup"><span data-stu-id="568d5-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="568d5-142"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="568d5-142"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="568d5-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="568d5-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="568d5-144"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="568d5-144"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="568d5-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="568d5-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="568d5-146">Clases MSMCA</span><span class="sxs-lookup"><span data-stu-id="568d5-146">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="568d5-147">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="568d5-147">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

