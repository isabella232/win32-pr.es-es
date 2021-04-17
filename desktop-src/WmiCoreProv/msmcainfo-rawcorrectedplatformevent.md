---
description: Contiene un evento de plataforma corregido (CPE). Esta clase solo está disponible en sistemas Windows de 64 bits.
ms.assetid: b24a390e-293d-4dd4-b747-33c298a5d45f
title: MSMCAInfo_RawCorrectedPlatformEvent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo_RawCorrectedPlatformEvent
- MSMCAInfo_RawCorrectedPlatformEvent.Active
- MSMCAInfo_RawCorrectedPlatformEvent.Count
- MSMCAInfo_RawCorrectedPlatformEvent.Records
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 906587ca9ee153eb93542c3e749e8164e6a5ee7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716705"
---
# <a name="msmcainfo_rawcorrectedplatformevent-class"></a><span data-ttu-id="83452-104">MSMCAInfo \_ RawCorrectedPlatformEvent (clase)</span><span class="sxs-lookup"><span data-stu-id="83452-104">MSMCAInfo\_RawCorrectedPlatformEvent class</span></span>

<span data-ttu-id="83452-105">La clase **MSMCAInfo \_ RawCorrectedPlatformEvent** contiene un evento de plataforma corregido (CPE).</span><span class="sxs-lookup"><span data-stu-id="83452-105">The **MSMCAInfo\_RawCorrectedPlatformEvent** class contains a Corrected Platform Event (CPE).</span></span> <span data-ttu-id="83452-106">Esta clase solo está disponible en sistemas Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="83452-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="83452-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="83452-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="83452-108">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="83452-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="83452-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="83452-109">Syntax</span></span>

``` syntax
class MSMCAInfo_RawCorrectedPlatformEvent : WMIEvent
{
  boolean         Active;
  uint32          Count;
  MSMCAInfo_Entry Records[];
};
```

## <a name="members"></a><span data-ttu-id="83452-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="83452-110">Members</span></span>

<span data-ttu-id="83452-111">La clase **MSMCAInfo \_ RawCorrectedPlatformEvent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="83452-111">The **MSMCAInfo\_RawCorrectedPlatformEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="83452-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="83452-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="83452-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="83452-113">Properties</span></span>

<span data-ttu-id="83452-114">La clase **MSMCAInfo \_ RawCorrectedPlatformEvent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="83452-114">The **MSMCAInfo\_RawCorrectedPlatformEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="83452-115">**Activo**</span><span class="sxs-lookup"><span data-stu-id="83452-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83452-116">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="83452-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="83452-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="83452-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83452-118">TRUE si esta instancia de la clase está activa; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="83452-118">TRUE, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="83452-119">**Recuento**</span><span class="sxs-lookup"><span data-stu-id="83452-119">**Count**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83452-120">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="83452-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83452-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="83452-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83452-122">Número de registros de error.</span><span class="sxs-lookup"><span data-stu-id="83452-122">Number of error records.</span></span>

</dd> <dt>

<span data-ttu-id="83452-123">**Registros**</span><span class="sxs-lookup"><span data-stu-id="83452-123">**Records**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83452-124">Tipo de datos: matriz de **\_ entrada MSMCAInfo**</span><span class="sxs-lookup"><span data-stu-id="83452-124">Data type: **MSMCAInfo\_Entry** array</span></span>
</dt> <dt>

<span data-ttu-id="83452-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="83452-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83452-126">Matriz de registros de error de MCA.</span><span class="sxs-lookup"><span data-stu-id="83452-126">Array of MCA error records.</span></span> <span data-ttu-id="83452-127">La propiedad **Count** especifica el número de registros de error de MCA en la matriz.</span><span class="sxs-lookup"><span data-stu-id="83452-127">The number of MCA error records in the array is specified by the **Count** property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="83452-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="83452-128">Remarks</span></span>

<span data-ttu-id="83452-129">La clase **MSMCAInfo \_ RawCorrectedPlatformEvent** se deriva de [**WMIEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="83452-129">The **MSMCAInfo\_RawCorrectedPlatformEvent** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="83452-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83452-130">Requirements</span></span>



| <span data-ttu-id="83452-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="83452-131">Requirement</span></span> | <span data-ttu-id="83452-132">Value</span><span class="sxs-lookup"><span data-stu-id="83452-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="83452-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="83452-133">Minimum supported client</span></span><br/> | <span data-ttu-id="83452-134">Windows XP</span><span class="sxs-lookup"><span data-stu-id="83452-134">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="83452-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="83452-135">Minimum supported server</span></span><br/> | <span data-ttu-id="83452-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="83452-136">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="83452-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="83452-137">Namespace</span></span><br/>                | <span data-ttu-id="83452-138">\\WMI raíz</span><span class="sxs-lookup"><span data-stu-id="83452-138">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="83452-139">MOF</span><span class="sxs-lookup"><span data-stu-id="83452-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="83452-140"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="83452-140"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="83452-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="83452-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83452-142"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83452-142"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83452-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="83452-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83452-144">Clases MSMCA</span><span class="sxs-lookup"><span data-stu-id="83452-144">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="83452-145">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="83452-145">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

 




