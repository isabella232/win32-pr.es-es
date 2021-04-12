---
title: Win32_CentralPublishingChangeEvent (clase)
description: Un evento que representa un cambio en la configuración central de RDV.
ms.assetid: 95be015e-a185-4548-a7f7-a22b351a34c8
ms.tgt_platform: multiple
keywords:
- Win32_CentralPublishingChangeEvent clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_CentralPublishingChangeEvent de clase, se describe
topic_type:
- apiref
api_name:
- Win32_CentralPublishingChangeEvent
- Win32_CentralPublishingChangeEvent.SECURITY_DESCRIPTOR
- Win32_CentralPublishingChangeEvent.TIME_CREATED
- Win32_CentralPublishingChangeEvent.TargetInstance
- Win32_CentralPublishingChangeEvent.OperationType
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4695479eb33301bda51b558375a18186fa08161e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491314"
---
# <a name="win32_centralpublishingchangeevent-class"></a><span data-ttu-id="e9c9f-105">\_Clase Win32 CentralPublishingChangeEvent</span><span class="sxs-lookup"><span data-stu-id="e9c9f-105">Win32\_CentralPublishingChangeEvent class</span></span>

<span data-ttu-id="e9c9f-106">Un evento que representa un cambio en la configuración central de RDV.</span><span class="sxs-lookup"><span data-stu-id="e9c9f-106">An event that represents a change to the central RDV settings.</span></span>

<span data-ttu-id="e9c9f-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="e9c9f-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9c9f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e9c9f-108">Syntax</span></span>

``` syntax
class Win32_CentralPublishingChangeEvent : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  object TargetInstance;
  uint32 OperationType;
};
```

## <a name="members"></a><span data-ttu-id="e9c9f-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="e9c9f-109">Members</span></span>

<span data-ttu-id="e9c9f-110">La **clase \_ CentralPublishingChangeEvent de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="e9c9f-110">The **Win32\_CentralPublishingChangeEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="e9c9f-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e9c9f-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e9c9f-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e9c9f-112">Properties</span></span>

<span data-ttu-id="e9c9f-113">La **clase \_ CentralPublishingChangeEvent de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="e9c9f-113">The **Win32\_CentralPublishingChangeEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e9c9f-114">**OperationType**</span><span class="sxs-lookup"><span data-stu-id="e9c9f-114">**OperationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9c9f-115">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e9c9f-115">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e9c9f-116">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e9c9f-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9c9f-117">Tipo de operación correspondiente al evento.</span><span class="sxs-lookup"><span data-stu-id="e9c9f-117">The type of operation corresponding to the event.</span></span>

<dt>

<span id="Create"></span><span id="create"></span><span id="CREATE"></span>

<span data-ttu-id="e9c9f-118">**Crear** (0)</span><span class="sxs-lookup"><span data-stu-id="e9c9f-118">**Create** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Modify"></span><span id="modify"></span><span id="MODIFY"></span>

<span data-ttu-id="e9c9f-119">**Modificar** (1)</span><span class="sxs-lookup"><span data-stu-id="e9c9f-119">**Modify** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>

<span data-ttu-id="e9c9f-120">**Eliminar** (2)</span><span class="sxs-lookup"><span data-stu-id="e9c9f-120">**Delete** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e9c9f-121">**descriptor de seguridad \_**</span><span class="sxs-lookup"><span data-stu-id="e9c9f-121">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9c9f-122">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="e9c9f-122">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="e9c9f-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e9c9f-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9c9f-124">Descriptor utilizado por el proveedor de eventos para determinar qué usuarios pueden recibir el evento.</span><span class="sxs-lookup"><span data-stu-id="e9c9f-124">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="e9c9f-125">Esta propiedad se hereda del [**\_ \_ evento**](/windows/desktop/WmiSdk/--event).</span><span class="sxs-lookup"><span data-stu-id="e9c9f-125">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span> <span data-ttu-id="e9c9f-126">Para obtener más información sobre las constantes que se usan para establecer este descriptor de seguridad, vea [constantes de seguridad de WMI](/windows/desktop/WmiSdk/wmi-security-constants).</span><span class="sxs-lookup"><span data-stu-id="e9c9f-126">For more information about constants used to set this security descriptor, see [WMI Security Constants](/windows/desktop/WmiSdk/wmi-security-constants).</span></span>

</dd> <dt>

<span data-ttu-id="e9c9f-127">**TargetInstance**</span><span class="sxs-lookup"><span data-stu-id="e9c9f-127">**TargetInstance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9c9f-128">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="e9c9f-128">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="e9c9f-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e9c9f-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9c9f-130">Objeto modificado por la operación correspondiente al evento.</span><span class="sxs-lookup"><span data-stu-id="e9c9f-130">Object changed by the operation corresponding to the event.</span></span>

</dd> <dt>

<span data-ttu-id="e9c9f-131">**HORA de \_ creación**</span><span class="sxs-lookup"><span data-stu-id="e9c9f-131">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9c9f-132">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e9c9f-132">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e9c9f-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e9c9f-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9c9f-134">Valor único que indica la hora a la que se generó el evento.</span><span class="sxs-lookup"><span data-stu-id="e9c9f-134">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="e9c9f-135">Se trata de un valor de 64 bits que representa el número de intervalos de 100 segundos después del 1 de enero de 1601.</span><span class="sxs-lookup"><span data-stu-id="e9c9f-135">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="e9c9f-136">La información está en el formato de hora universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="e9c9f-136">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="e9c9f-137">Esta propiedad se hereda del [**\_ \_ evento**](/windows/desktop/WmiSdk/--event).</span><span class="sxs-lookup"><span data-stu-id="e9c9f-137">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span>

<span data-ttu-id="e9c9f-138">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e9c9f-138">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e9c9f-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9c9f-139">Requirements</span></span>



| <span data-ttu-id="e9c9f-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9c9f-140">Requirement</span></span> | <span data-ttu-id="e9c9f-141">Value</span><span class="sxs-lookup"><span data-stu-id="e9c9f-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9c9f-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e9c9f-142">Minimum supported client</span></span><br/> | <span data-ttu-id="e9c9f-143">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="e9c9f-143">None supported</span></span><br/>                                                                |
| <span data-ttu-id="e9c9f-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e9c9f-144">Minimum supported server</span></span><br/> | <span data-ttu-id="e9c9f-145">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e9c9f-145">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="e9c9f-146">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e9c9f-146">Namespace</span></span><br/>                | <span data-ttu-id="e9c9f-147">Raíz de \\ cimv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="e9c9f-147">Root\\cimv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="e9c9f-148">MOF</span><span class="sxs-lookup"><span data-stu-id="e9c9f-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e9c9f-149"><dt>Tscpub. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e9c9f-149"><dt>Tscpub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="e9c9f-150">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e9c9f-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9c9f-151"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9c9f-151"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 

