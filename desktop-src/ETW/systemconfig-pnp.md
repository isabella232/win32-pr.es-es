---
description: Esta clase es la clase de tipo de evento para los eventos de PnP. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 01e9a8bb-3f54-4e20-b4db-1b4bba745d4f
title: SystemConfig_PnP (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_PnP
- SystemConfig_PnP.IDLength
- SystemConfig_PnP.DescriptionLength
- SystemConfig_PnP.FriendlyNameLength
- SystemConfig_PnP.DeviceID
- SystemConfig_PnP.DeviceDescription
- SystemConfig_PnP.FriendlyName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2bd4cdbbec5c61f453a0ef6fae3fef0bd494edac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497254"
---
# <a name="systemconfig_pnp-class"></a><span data-ttu-id="fde3e-104">SystemConfig ( \_ clase PNP)</span><span class="sxs-lookup"><span data-stu-id="fde3e-104">SystemConfig\_PnP class</span></span>

<span data-ttu-id="fde3e-105">Esta clase es la clase de tipo de evento para los eventos de PnP.</span><span class="sxs-lookup"><span data-stu-id="fde3e-105">This class is the event type class for PnP events.</span></span>

<span data-ttu-id="fde3e-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="fde3e-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="fde3e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fde3e-107">Syntax</span></span>

``` syntax
[EventType(22), EventTypeName("PnP")]
class SystemConfig_PnP : SystemConfig
{
  uint32 IDLength;
  uint32 DescriptionLength;
  uint32 FriendlyNameLength;
  string DeviceID;
  string DeviceDescription;
  string FriendlyName;
};
```

## <a name="members"></a><span data-ttu-id="fde3e-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="fde3e-108">Members</span></span>

<span data-ttu-id="fde3e-109">La **clase \_ PNP SystemConfig** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="fde3e-109">The **SystemConfig\_PnP** class has these types of members:</span></span>

-   [<span data-ttu-id="fde3e-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fde3e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fde3e-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fde3e-111">Properties</span></span>

<span data-ttu-id="fde3e-112">La **clase \_ PNP SystemConfig** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="fde3e-112">The **SystemConfig\_PnP** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fde3e-113">**DescriptionLength**</span><span class="sxs-lookup"><span data-stu-id="fde3e-113">**DescriptionLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fde3e-114">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fde3e-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fde3e-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fde3e-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fde3e-116">Calificadores: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="fde3e-116">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="fde3e-117">Longitud, en caracteres, de la cadena DeviceDescription.</span><span class="sxs-lookup"><span data-stu-id="fde3e-117">Length, in characters, of the DeviceDescription string.</span></span>

</dd> <dt>

<span data-ttu-id="fde3e-118">**DeviceDescription**</span><span class="sxs-lookup"><span data-stu-id="fde3e-118">**DeviceDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fde3e-119">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fde3e-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fde3e-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fde3e-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fde3e-121">Calificadores: WmiDataId (5), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="fde3e-121">Qualifiers: WmiDataId(5), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="fde3e-122">Descripción del dispositivo PnP.</span><span class="sxs-lookup"><span data-stu-id="fde3e-122">Description of the PnP device.</span></span>

</dd> <dt>

<span data-ttu-id="fde3e-123">**ID**</span><span class="sxs-lookup"><span data-stu-id="fde3e-123">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fde3e-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fde3e-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fde3e-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fde3e-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fde3e-126">Calificadores: WmiDataId (4), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="fde3e-126">Qualifiers: WmiDataId(4), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="fde3e-127">Identifica el dispositivo PnP.</span><span class="sxs-lookup"><span data-stu-id="fde3e-127">Identifies the PnP device.</span></span>

</dd> <dt>

<span data-ttu-id="fde3e-128">**FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="fde3e-128">**FriendlyName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fde3e-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fde3e-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fde3e-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fde3e-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fde3e-131">Calificadores: WmiDataId (6), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="fde3e-131">Qualifiers: WmiDataId(6), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="fde3e-132">Nombre del dispositivo PnP que se va a usar en una interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="fde3e-132">Name of the PnP device to use in a user interface.</span></span>

</dd> <dt>

<span data-ttu-id="fde3e-133">**FriendlyNameLength**</span><span class="sxs-lookup"><span data-stu-id="fde3e-133">**FriendlyNameLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fde3e-134">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fde3e-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fde3e-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fde3e-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fde3e-136">Calificadores: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="fde3e-136">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="fde3e-137">Longitud, en caracteres, de la cadena FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="fde3e-137">Length, in characters, of the FriendlyName string.</span></span>

</dd> <dt>

<span data-ttu-id="fde3e-138">**IDLength**</span><span class="sxs-lookup"><span data-stu-id="fde3e-138">**IDLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fde3e-139">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fde3e-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fde3e-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fde3e-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fde3e-141">Calificadores: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="fde3e-141">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="fde3e-142">Longitud, en caracteres, de la cadena de DeviceID.</span><span class="sxs-lookup"><span data-stu-id="fde3e-142">Length, in characters, of the DeviceID string.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fde3e-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fde3e-143">Requirements</span></span>



| <span data-ttu-id="fde3e-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="fde3e-144">Requirement</span></span> | <span data-ttu-id="fde3e-145">Value</span><span class="sxs-lookup"><span data-stu-id="fde3e-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fde3e-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fde3e-146">Minimum supported client</span></span><br/> | <span data-ttu-id="fde3e-147">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="fde3e-147">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fde3e-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fde3e-148">Minimum supported server</span></span><br/> | <span data-ttu-id="fde3e-149">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="fde3e-149">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fde3e-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="fde3e-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fde3e-151">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="fde3e-151">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




