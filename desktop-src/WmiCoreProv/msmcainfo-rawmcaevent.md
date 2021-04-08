---
description: Contiene un evento de arquitectura de comprobación de equipo (MCA). Esta clase solo está disponible en sistemas Windows de 64 bits.
ms.assetid: d1806b91-43a3-4329-8fe5-de1e4755740f
title: MSMCAInfo_RawMCAEvent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo_RawMCAEvent
- MSMCAInfo_RawMCAEvent.Active
- MSMCAInfo_RawMCAEvent.Count
- MSMCAInfo_RawMCAEvent.InstanceName
- MSMCAInfo_RawMCAEvent.Records
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: e15af79c67265823e0025849e4c2ef27f690265c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002653"
---
# <a name="msmcainfo_rawmcaevent-class"></a><span data-ttu-id="0d3e6-104">MSMCAInfo \_ RawMCAEvent (clase)</span><span class="sxs-lookup"><span data-stu-id="0d3e6-104">MSMCAInfo\_RawMCAEvent class</span></span>

<span data-ttu-id="0d3e6-105">La clase **MSMCAInfo \_ RawMCAEvent** contiene un evento de arquitectura de comprobación de equipo (MCA).</span><span class="sxs-lookup"><span data-stu-id="0d3e6-105">The **MSMCAInfo\_RawMCAEvent** class contains a Machine Check Architecture (MCA) event.</span></span> <span data-ttu-id="0d3e6-106">Esta clase solo está disponible en sistemas Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="0d3e6-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="0d3e6-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="0d3e6-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="0d3e6-108">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="0d3e6-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d3e6-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0d3e6-109">Syntax</span></span>

``` syntax
class MSMCAInfo_RawMCAEvent : WMIEvent
{
  boolean         Active;
  uint32          Count;
  string          InstanceName;
  MSMCAInfo_Entry Records[];
};
```

## <a name="members"></a><span data-ttu-id="0d3e6-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="0d3e6-110">Members</span></span>

<span data-ttu-id="0d3e6-111">La clase **MSMCAInfo \_ RawMCAEvent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="0d3e6-111">The **MSMCAInfo\_RawMCAEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="0d3e6-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0d3e6-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0d3e6-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0d3e6-113">Properties</span></span>

<span data-ttu-id="0d3e6-114">La clase **MSMCAInfo \_ RawMCAEvent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="0d3e6-114">The **MSMCAInfo\_RawMCAEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0d3e6-115">**Activo**</span><span class="sxs-lookup"><span data-stu-id="0d3e6-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d3e6-116">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="0d3e6-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0d3e6-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0d3e6-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d3e6-118">TRUE si esta instancia de la clase está activa; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="0d3e6-118">TRUE, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="0d3e6-119">**Recuento**</span><span class="sxs-lookup"><span data-stu-id="0d3e6-119">**Count**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d3e6-120">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0d3e6-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0d3e6-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0d3e6-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d3e6-122">Número de registros de error.</span><span class="sxs-lookup"><span data-stu-id="0d3e6-122">Number of error records.</span></span>

</dd> <dt>

<span data-ttu-id="0d3e6-123">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="0d3e6-123">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d3e6-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0d3e6-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d3e6-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0d3e6-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d3e6-126">Calificadores: [ **clave**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0d3e6-126">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0d3e6-127">Cadena que identifica de forma única esta instancia de la clase **MSMCAInfo \_ RawMCAEvent** .</span><span class="sxs-lookup"><span data-stu-id="0d3e6-127">String that uniquely identifies this instance of the **MSMCAInfo\_RawMCAEvent** class.</span></span>

</dd> <dt>

<span data-ttu-id="0d3e6-128">**Registros**</span><span class="sxs-lookup"><span data-stu-id="0d3e6-128">**Records**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d3e6-129">Tipo de datos: matriz de **\_ entrada MSMCAInfo**</span><span class="sxs-lookup"><span data-stu-id="0d3e6-129">Data type: **MSMCAInfo\_Entry** array</span></span>
</dt> <dt>

<span data-ttu-id="0d3e6-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0d3e6-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d3e6-131">Matriz de registros de error de MCA.</span><span class="sxs-lookup"><span data-stu-id="0d3e6-131">Array of MCA error records.</span></span> <span data-ttu-id="0d3e6-132">La propiedad **Count** especifica el número de registros de error de MCA en la matriz.</span><span class="sxs-lookup"><span data-stu-id="0d3e6-132">The number of MCA error records in the array is specified by the **Count** property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0d3e6-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0d3e6-133">Remarks</span></span>

<span data-ttu-id="0d3e6-134">La clase **MSMCAInfo \_ RawMCAEvent** se deriva de [**WMIEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="0d3e6-134">The **MSMCAInfo\_RawMCAEvent** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0d3e6-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d3e6-135">Requirements</span></span>



| <span data-ttu-id="0d3e6-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d3e6-136">Requirement</span></span> | <span data-ttu-id="0d3e6-137">Value</span><span class="sxs-lookup"><span data-stu-id="0d3e6-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d3e6-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0d3e6-138">Minimum supported client</span></span><br/> | <span data-ttu-id="0d3e6-139">Windows XP</span><span class="sxs-lookup"><span data-stu-id="0d3e6-139">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="0d3e6-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0d3e6-140">Minimum supported server</span></span><br/> | <span data-ttu-id="0d3e6-141">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0d3e6-141">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="0d3e6-142">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0d3e6-142">Namespace</span></span><br/>                | <span data-ttu-id="0d3e6-143">\\WMI raíz</span><span class="sxs-lookup"><span data-stu-id="0d3e6-143">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="0d3e6-144">MOF</span><span class="sxs-lookup"><span data-stu-id="0d3e6-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0d3e6-145"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0d3e6-145"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="0d3e6-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0d3e6-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d3e6-147"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d3e6-147"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d3e6-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="0d3e6-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d3e6-149">Clases MSMCA</span><span class="sxs-lookup"><span data-stu-id="0d3e6-149">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="0d3e6-150">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="0d3e6-150">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

