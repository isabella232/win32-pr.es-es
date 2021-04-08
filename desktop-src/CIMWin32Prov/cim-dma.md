---
description: La clase de DMA de CIM \_ representa el acceso directo a memoria (DMA) de la arquitectura del equipo.
ms.assetid: 101fa9f3-a403-487d-8482-b1e8e9f957d6
ms.tgt_platform: multiple
title: CIM_DMA (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DMA
- CIM_DMA.AddressSize
- CIM_DMA.Availability
- CIM_DMA.BurstMode
- CIM_DMA.ByteMode
- CIM_DMA.Caption
- CIM_DMA.ChannelTiming
- CIM_DMA.CreationClassName
- CIM_DMA.CSCreationClassName
- CIM_DMA.CSName
- CIM_DMA.Description
- CIM_DMA.DMAChannel
- CIM_DMA.InstallDate
- CIM_DMA.MaxTransferSize
- CIM_DMA.Name
- CIM_DMA.Status
- CIM_DMA.TransferWidths
- CIM_DMA.TypeCTiming
- CIM_DMA.WordMode
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 71fe9c0ad29afa7be20df6fbf05c5d1183d23d13
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000628"
---
# <a name="cim_dma-class"></a><span data-ttu-id="fd68d-103">\_Clase DMA de CIM</span><span class="sxs-lookup"><span data-stu-id="fd68d-103">CIM\_DMA class</span></span>

<span data-ttu-id="fd68d-104">La clase de **\_ DMA de CIM** representa el acceso directo a memoria (DMA) de la arquitectura del equipo.</span><span class="sxs-lookup"><span data-stu-id="fd68d-104">The **CIM\_DMA** class represents computer architecture direct memory access (DMA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fd68d-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="fd68d-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="fd68d-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="fd68d-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="fd68d-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="fd68d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="fd68d-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="fd68d-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd68d-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fd68d-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C523-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_DMA : CIM_SystemResource
{
  uint16   AddressSize;
  uint16   Availability;
  boolean  BurstMode;
  uint16   ByteMode;
  string   Caption;
  uint16   ChannelTiming;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  uint32   DMAChannel;
  datetime InstallDate;
  uint32   MaxTransferSize;
  string   Name;
  string   Status;
  uint16   TransferWidths[];
  uint16   TypeCTiming;
  uint16   WordMode;
};
```

## <a name="members"></a><span data-ttu-id="fd68d-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="fd68d-110">Members</span></span>

<span data-ttu-id="fd68d-111">La clase de **\_ DMA de CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="fd68d-111">The **CIM\_DMA** class has these types of members:</span></span>

-   [<span data-ttu-id="fd68d-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fd68d-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fd68d-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fd68d-113">Properties</span></span>

<span data-ttu-id="fd68d-114">La clase de **\_ DMA de CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="fd68d-114">The **CIM\_DMA** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fd68d-115">**AddressSize**</span><span class="sxs-lookup"><span data-stu-id="fd68d-115">**AddressSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd68d-116">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fd68d-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fd68d-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fd68d-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd68d-118">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Recurso del sistema DMTF información \| de DMA 001,3 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="fd68d-118">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.3"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="fd68d-119">Tamaño de la dirección del canal DMA, en bits.</span><span class="sxs-lookup"><span data-stu-id="fd68d-119">DMA channel address size, in bits.</span></span> <span data-ttu-id="fd68d-120">Los valores permitidos son 8, 16, 32 y 64.</span><span class="sxs-lookup"><span data-stu-id="fd68d-120">Permissible values are 8, 16, 32, and 64.</span></span> <span data-ttu-id="fd68d-121">Si es desconocido, escriba 0.</span><span class="sxs-lookup"><span data-stu-id="fd68d-121">If unknown, enter 0.</span></span>

<dt>



 <span data-ttu-id="fd68d-122"> (0)</span><span class="sxs-lookup"><span data-stu-id="fd68d-122">(0)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="fd68d-123">(8)</span><span class="sxs-lookup"><span data-stu-id="fd68d-123">(8)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="fd68d-124">(16)</span><span class="sxs-lookup"><span data-stu-id="fd68d-124">(16)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="fd68d-125">(32)</span><span class="sxs-lookup"><span data-stu-id="fd68d-125">(32)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="fd68d-126">(64)</span><span class="sxs-lookup"><span data-stu-id="fd68d-126">(64)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="fd68d-127">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="fd68d-127">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd68d-128">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fd68d-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fd68d-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fd68d-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd68d-130">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| DMA \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="fd68d-130">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|DMA\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="fd68d-131">Disponibilidad del DMA.</span><span class="sxs-lookup"><span data-stu-id="fd68d-131">Availability of the DMA.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="fd68d-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="fd68d-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fd68d-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="fd68d-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="fd68d-134">Desconocido.</span><span class="sxs-lookup"><span data-stu-id="fd68d-134">Unknown.</span></span>

</dd> <dt>

<span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>

<span data-ttu-id="fd68d-135"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Disponible** (3)</span><span class="sxs-lookup"><span data-stu-id="fd68d-135"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Available** (3)</span></span>


</dt> <dd>

<span data-ttu-id="fd68d-136">Disponible.</span><span class="sxs-lookup"><span data-stu-id="fd68d-136">Available.</span></span>

</dd> <dt>

<span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>

<span data-ttu-id="fd68d-137"><span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>**En uso/no disponible** (4)</span><span class="sxs-lookup"><span data-stu-id="fd68d-137"><span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>**In Use/Not Available** (4)</span></span>


</dt> <dd>

<span data-ttu-id="fd68d-138">En uso (no disponible).</span><span class="sxs-lookup"><span data-stu-id="fd68d-138">In use (not available).</span></span>

</dd> <dt>

<span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>

<span data-ttu-id="fd68d-139"><span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>**En uso y disponible/compartible** (5)</span><span class="sxs-lookup"><span data-stu-id="fd68d-139"><span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>**In Use and Available/Shareable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="fd68d-140">En uso, pero disponible (se puede compartir).</span><span class="sxs-lookup"><span data-stu-id="fd68d-140">In use, but available (sharable).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="fd68d-141">**BurstMode**</span><span class="sxs-lookup"><span data-stu-id="fd68d-141">**BurstMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd68d-142">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="fd68d-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fd68d-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fd68d-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd68d-144">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| DMA \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="fd68d-144">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|DMA\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="fd68d-145">Si **es true**, el canal DMA admite el modo de ráfaga.</span><span class="sxs-lookup"><span data-stu-id="fd68d-145">If **TRUE**, the DMA channel supports burst mode.</span></span>

</dd> <dt>

<span data-ttu-id="fd68d-146">**ByteMode**</span><span class="sxs-lookup"><span data-stu-id="fd68d-146">**ByteMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd68d-147">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fd68d-147">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fd68d-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fd68d-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd68d-149">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Recurso del sistema DMTF información de DMA \| 001,7 ")</span><span class="sxs-lookup"><span data-stu-id="fd68d-149">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="fd68d-150">Indica si DMA puede ejecutarse en el modo de recuento por byte.</span><span class="sxs-lookup"><span data-stu-id="fd68d-150">Indicates whether DMA can execute in count-by-byte mode.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="fd68d-151"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="fd68d-151"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="fd68d-152">Otros.</span><span class="sxs-lookup"><span data-stu-id="fd68d-152">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fd68d-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="fd68d-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="fd68d-154">Desconocido.</span><span class="sxs-lookup"><span data-stu-id="fd68d-154">Unknown.</span></span>

</dd> <dt>

<span id="Not_execute_in__count_by_byte__mode"></span><span id="not_execute_in__count_by_byte__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>

<span data-ttu-id="fd68d-155"><span id="Not_execute_in__count_by_byte__mode"></span><span id="not_execute_in__count_by_byte__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>**No se ejecuta en modo "recuento por byte"** (3)</span><span class="sxs-lookup"><span data-stu-id="fd68d-155"><span id="Not_execute_in__count_by_byte__mode"></span><span id="not_execute_in__count_by_byte__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>**Not execute in 'count by byte' mode** (3)</span></span>


</dt> <dd>

<span data-ttu-id="fd68d-156">No se puede ejecutar en el modo de recuento por byte.</span><span class="sxs-lookup"><span data-stu-id="fd68d-156">Cannot execute in count-by-byte mode.</span></span>

</dd> <dt>

<span id="Execute_in__count_by_byte__mode"></span><span id="execute_in__count_by_byte__mode"></span><span id="EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>

<span data-ttu-id="fd68d-157"><span id="Execute_in__count_by_byte__mode"></span><span id="execute_in__count_by_byte__mode"></span><span id="EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>**Ejecutar en modo "recuento por byte"** (4)</span><span class="sxs-lookup"><span data-stu-id="fd68d-157"><span id="Execute_in__count_by_byte__mode"></span><span id="execute_in__count_by_byte__mode"></span><span id="EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>**Execute in 'count by byte' mode** (4)</span></span>


</dt> <dd>

<span data-ttu-id="fd68d-158">Puede ejecutarse en el modo de recuento por byte.</span><span class="sxs-lookup"><span data-stu-id="fd68d-158">Able to execute in count-by-byte mode.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="fd68d-159">**Caption**</span><span class="sxs-lookup"><span data-stu-id="fd68d-159">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd68d-160">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fd68d-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd68d-161">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fd68d-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd68d-162">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="fd68d-162">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="fd68d-163">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="fd68d-163">Short textual description of the object.</span></span>

<span data-ttu-id="fd68d-164">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="fd68d-164">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd68d-165">**ChannelTiming**</span><span class="sxs-lookup"><span data-stu-id="fd68d-165">**ChannelTiming**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd68d-166">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fd68d-166">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fd68d-167">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fd68d-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd68d-168">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Recurso del sistema DMTF información de DMA \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="fd68d-168">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="fd68d-169">Temporización del canal DMA.</span><span class="sxs-lookup"><span data-stu-id="fd68d-169">DMA channel timing.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="fd68d-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="fd68d-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="fd68d-171">Otros.</span><span class="sxs-lookup"><span data-stu-id="fd68d-171">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fd68d-172"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="fd68d-172"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="fd68d-173">Desconocido.</span><span class="sxs-lookup"><span data-stu-id="fd68d-173">Unknown.</span></span>

</dd> <dt>

<span id="ISA_Compatible"></span><span id="isa_compatible"></span><span id="ISA_COMPATIBLE"></span>

<span data-ttu-id="fd68d-174"><span id="ISA_Compatible"></span><span id="isa_compatible"></span><span id="ISA_COMPATIBLE"></span>**Compatible con ISA** (3)</span><span class="sxs-lookup"><span data-stu-id="fd68d-174"><span id="ISA_Compatible"></span><span id="isa_compatible"></span><span id="ISA_COMPATIBLE"></span>**ISA Compatible** (3)</span></span>


</dt> <dd>

<span data-ttu-id="fd68d-175">Compatible con ISA.</span><span class="sxs-lookup"><span data-stu-id="fd68d-175">ISA-compatible.</span></span>

</dd> <dt>

<span id="Type_A"></span><span id="type_a"></span><span id="TYPE_A"></span>

<span data-ttu-id="fd68d-176"><span id="Type_A"></span><span id="type_a"></span><span id="TYPE_A"></span>**Escriba A** (4)</span><span class="sxs-lookup"><span data-stu-id="fd68d-176"><span id="Type_A"></span><span id="type_a"></span><span id="TYPE_A"></span>**Type A** (4)</span></span>


</dt> <dd>

<span data-ttu-id="fd68d-177">Escriba.</span><span class="sxs-lookup"><span data-stu-id="fd68d-177">Type A.</span></span>

</dd> <dt>

<span id="Type_B"></span><span id="type_b"></span><span id="TYPE_B"></span>

<span data-ttu-id="fd68d-178"><span id="Type_B"></span><span id="type_b"></span><span id="TYPE_B"></span>**Tipo B** (5)</span><span class="sxs-lookup"><span data-stu-id="fd68d-178"><span id="Type_B"></span><span id="type_b"></span><span id="TYPE_B"></span>**Type B** (5)</span></span>


</dt> <dd>

<span data-ttu-id="fd68d-179">Escriba B.</span><span class="sxs-lookup"><span data-stu-id="fd68d-179">Type B.</span></span>

</dd> <dt>

<span id="Type_F"></span><span id="type_f"></span><span id="TYPE_F"></span>

<span data-ttu-id="fd68d-180"><span id="Type_F"></span><span id="type_f"></span><span id="TYPE_F"></span>**Escriba F** (6)</span><span class="sxs-lookup"><span data-stu-id="fd68d-180"><span id="Type_F"></span><span id="type_f"></span><span id="TYPE_F"></span>**Type F** (6)</span></span>


</dt> <dd>

<span data-ttu-id="fd68d-181">Escriba F.</span><span class="sxs-lookup"><span data-stu-id="fd68d-181">Type F.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="fd68d-182">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="fd68d-182">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd68d-183">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fd68d-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd68d-184">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fd68d-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd68d-185">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="fd68d-185">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="fd68d-186">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="fd68d-186">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="fd68d-187">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="fd68d-187">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="fd68d-188">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="fd68d-188">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd68d-189">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fd68d-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd68d-190">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fd68d-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd68d-191">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="fd68d-191">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="fd68d-192">Ámbito del nombre de la clase de creación del sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="fd68d-192">Scoping computer system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="fd68d-193">**CSName**</span><span class="sxs-lookup"><span data-stu-id="fd68d-193">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd68d-194">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fd68d-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd68d-195">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fd68d-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd68d-196">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Nombre**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="fd68d-196">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="fd68d-197">Ámbito del nombre del sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="fd68d-197">Scoping computer system's name.</span></span>

</dd> <dt>

<span data-ttu-id="fd68d-198">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fd68d-198">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd68d-199">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fd68d-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd68d-200">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fd68d-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd68d-201">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="fd68d-201">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="fd68d-202">Descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="fd68d-202">Textual description of the object.</span></span>

<span data-ttu-id="fd68d-203">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="fd68d-203">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd68d-204">**DMAChannel**</span><span class="sxs-lookup"><span data-stu-id="fd68d-204">**DMAChannel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd68d-205">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fd68d-205">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd68d-206">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fd68d-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd68d-207">Calificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| DMA \| 001,1 ")</span><span class="sxs-lookup"><span data-stu-id="fd68d-207">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|DMA\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="fd68d-208">Número de canal DMA.</span><span class="sxs-lookup"><span data-stu-id="fd68d-208">DMA channel number.</span></span> <span data-ttu-id="fd68d-209">Este número forma parte del valor de clave del objeto.</span><span class="sxs-lookup"><span data-stu-id="fd68d-209">This number is part of the object's key value.</span></span>

</dd> <dt>

<span data-ttu-id="fd68d-210">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="fd68d-210">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd68d-211">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="fd68d-211">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="fd68d-212">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fd68d-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd68d-213">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="fd68d-213">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="fd68d-214">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="fd68d-214">Date and time the object was installed.</span></span> <span data-ttu-id="fd68d-215">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="fd68d-215">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="fd68d-216">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="fd68d-216">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd68d-217">**MaxTransferSize**</span><span class="sxs-lookup"><span data-stu-id="fd68d-217">**MaxTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd68d-218">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fd68d-218">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd68d-219">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fd68d-219">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd68d-220">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Recurso del sistema DMTF información DMA \| 001,4 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="fd68d-220">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="fd68d-221">Número máximo de bytes que puede transferir este canal DMA.</span><span class="sxs-lookup"><span data-stu-id="fd68d-221">Maximum number of bytes that can be transferred by this DMA channel.</span></span> <span data-ttu-id="fd68d-222">Si es desconocido, escriba 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="fd68d-222">If unknown, enter 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="fd68d-223">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="fd68d-223">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd68d-224">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fd68d-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd68d-225">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fd68d-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd68d-226">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="fd68d-226">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="fd68d-227">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="fd68d-227">Label by which the object is known.</span></span> <span data-ttu-id="fd68d-228">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="fd68d-228">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="fd68d-229">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="fd68d-229">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd68d-230">**Estado**</span><span class="sxs-lookup"><span data-stu-id="fd68d-230">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd68d-231">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fd68d-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd68d-232">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fd68d-232">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd68d-233">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="fd68d-233">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="fd68d-234">Indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="fd68d-234">Indicates the current status of the object.</span></span>

<span data-ttu-id="fd68d-235">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="fd68d-235">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="fd68d-236">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="fd68d-236">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="fd68d-237">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="fd68d-237">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="fd68d-238">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="fd68d-238">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="fd68d-239">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="fd68d-239">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fd68d-240">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="fd68d-240">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="fd68d-241">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="fd68d-241">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="fd68d-242">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="fd68d-242">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="fd68d-243">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="fd68d-243">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="fd68d-244">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="fd68d-244">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="fd68d-245">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="fd68d-245">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="fd68d-246">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="fd68d-246">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="fd68d-247">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="fd68d-247">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="fd68d-248">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="fd68d-248">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="fd68d-249">**TransferWidths**</span><span class="sxs-lookup"><span data-stu-id="fd68d-249">**TransferWidths**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd68d-250">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fd68d-250">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="fd68d-251">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fd68d-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd68d-252">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Recurso del sistema DMTF información \| de DMA 001,2 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="fd68d-252">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="fd68d-253">Matriz que indica todos los anchos de transferencia, en bits, admitidos por este canal DMA.</span><span class="sxs-lookup"><span data-stu-id="fd68d-253">Array that indicates all of the transfer widths, in bits, supported by this DMA channel.</span></span> <span data-ttu-id="fd68d-254">Los valores permitidos son los bits 8, 16, 32, 64 y 128.</span><span class="sxs-lookup"><span data-stu-id="fd68d-254">Permissible values are 8, 16, 32, 64, and 128 bits.</span></span> <span data-ttu-id="fd68d-255">Si es desconocido, escriba 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="fd68d-255">If unknown, enter 0 (zero).</span></span>

<dt>



 <span data-ttu-id="fd68d-256"> (0)</span><span class="sxs-lookup"><span data-stu-id="fd68d-256">(0)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="fd68d-257">(8)</span><span class="sxs-lookup"><span data-stu-id="fd68d-257">(8)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="fd68d-258">(16)</span><span class="sxs-lookup"><span data-stu-id="fd68d-258">(16)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="fd68d-259">(32)</span><span class="sxs-lookup"><span data-stu-id="fd68d-259">(32)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="fd68d-260">(64)</span><span class="sxs-lookup"><span data-stu-id="fd68d-260">(64)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="fd68d-261">(128)</span><span class="sxs-lookup"><span data-stu-id="fd68d-261">(128)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="fd68d-262">**TypeCTiming**</span><span class="sxs-lookup"><span data-stu-id="fd68d-262">**TypeCTiming**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd68d-263">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fd68d-263">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fd68d-264">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fd68d-264">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd68d-265">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Recurso del sistema DMTF información de DMA \| 001,10 ")</span><span class="sxs-lookup"><span data-stu-id="fd68d-265">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.10")</span></span>
</dt> </dl>

<span data-ttu-id="fd68d-266">Indica si se admite el control de tiempo de tipo C (ráfaga).</span><span class="sxs-lookup"><span data-stu-id="fd68d-266">Indicates whether Type C (burst) timing is supported.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="fd68d-267"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="fd68d-267"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="fd68d-268">Otros.</span><span class="sxs-lookup"><span data-stu-id="fd68d-268">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fd68d-269"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="fd68d-269"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="fd68d-270">Desconocido.</span><span class="sxs-lookup"><span data-stu-id="fd68d-270">Unknown.</span></span>

</dd> <dt>

<span id="ISA_Compatible"></span><span id="isa_compatible"></span><span id="ISA_COMPATIBLE"></span>

<span data-ttu-id="fd68d-271"><span id="ISA_Compatible"></span><span id="isa_compatible"></span><span id="ISA_COMPATIBLE"></span>**Compatible con ISA** (3)</span><span class="sxs-lookup"><span data-stu-id="fd68d-271"><span id="ISA_Compatible"></span><span id="isa_compatible"></span><span id="ISA_COMPATIBLE"></span>**ISA Compatible** (3)</span></span>


</dt> <dd>

<span data-ttu-id="fd68d-272">Compatible con ISA.</span><span class="sxs-lookup"><span data-stu-id="fd68d-272">ISA-compatible.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="fd68d-273"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (4)</span><span class="sxs-lookup"><span data-stu-id="fd68d-273"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (4)</span></span>


</dt> <dd>

<span data-ttu-id="fd68d-274">No se admite.</span><span class="sxs-lookup"><span data-stu-id="fd68d-274">Not supported.</span></span>

</dd> <dt>

<span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span>

<span data-ttu-id="fd68d-275"><span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span>**Compatible** (5)</span><span class="sxs-lookup"><span data-stu-id="fd68d-275"><span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span>**Supported** (5)</span></span>


</dt> <dd>

<span data-ttu-id="fd68d-276">Compatible.</span><span class="sxs-lookup"><span data-stu-id="fd68d-276">Supported.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="fd68d-277">**WordMode**</span><span class="sxs-lookup"><span data-stu-id="fd68d-277">**WordMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd68d-278">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fd68d-278">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fd68d-279">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fd68d-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd68d-280">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Recurso del sistema DMTF información de DMA \| 001,8 ")</span><span class="sxs-lookup"><span data-stu-id="fd68d-280">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.8")</span></span>
</dt> </dl>

<span data-ttu-id="fd68d-281">Indica si DMA puede ejecutarse en modo de recuento por palabra.</span><span class="sxs-lookup"><span data-stu-id="fd68d-281">Indicates whether DMA can execute in count-by-word mode.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="fd68d-282"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="fd68d-282"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="fd68d-283">Otros.</span><span class="sxs-lookup"><span data-stu-id="fd68d-283">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fd68d-284"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="fd68d-284"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="fd68d-285">Desconocido.</span><span class="sxs-lookup"><span data-stu-id="fd68d-285">Unknown.</span></span>

</dd> <dt>

<span id="Not_execute_in__count_by_word__mode"></span><span id="not_execute_in__count_by_word__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_WORD__MODE"></span>

<span data-ttu-id="fd68d-286"><span id="Not_execute_in__count_by_word__mode"></span><span id="not_execute_in__count_by_word__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_WORD__MODE"></span>**No se ejecuta en modo "recuento por palabra"** (3)</span><span class="sxs-lookup"><span data-stu-id="fd68d-286"><span id="Not_execute_in__count_by_word__mode"></span><span id="not_execute_in__count_by_word__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_WORD__MODE"></span>**Not execute in 'count by word' mode** (3)</span></span>


</dt> <dd>

<span data-ttu-id="fd68d-287">No se puede ejecutar en modo de número por palabra.</span><span class="sxs-lookup"><span data-stu-id="fd68d-287">Cannot execute in count-by-word mode.</span></span>

</dd> <dt>

<span id="Execute_in__count_by_word__mode"></span><span id="execute_in__count_by_word__mode"></span><span id="EXECUTE_IN__COUNT_BY_WORD__MODE"></span>

<span data-ttu-id="fd68d-288"><span id="Execute_in__count_by_word__mode"></span><span id="execute_in__count_by_word__mode"></span><span id="EXECUTE_IN__COUNT_BY_WORD__MODE"></span>**Ejecutar en modo "recuento por palabra"** (4)</span><span class="sxs-lookup"><span data-stu-id="fd68d-288"><span id="Execute_in__count_by_word__mode"></span><span id="execute_in__count_by_word__mode"></span><span id="EXECUTE_IN__COUNT_BY_WORD__MODE"></span>**Execute in 'count by word' mode** (4)</span></span>


</dt> <dd>

<span data-ttu-id="fd68d-289">Se puede ejecutar en modo de número por palabra.</span><span class="sxs-lookup"><span data-stu-id="fd68d-289">Able to execute in count-by-word mode.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fd68d-290">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fd68d-290">Remarks</span></span>

<span data-ttu-id="fd68d-291">La clase de **\_ DMA de CIM** se deriva de [**\_ SystemResource de CIM**](cim-systemresource.md).</span><span class="sxs-lookup"><span data-stu-id="fd68d-291">The **CIM\_DMA** class is derived from [**CIM\_SystemResource**](cim-systemresource.md).</span></span>

<span data-ttu-id="fd68d-292">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="fd68d-292">WMI does not implement this class.</span></span> <span data-ttu-id="fd68d-293">Para las clases derivadas de la **\_ DMA de CIM**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="fd68d-293">For classes derived from **CIM\_DMA**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="fd68d-294">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="fd68d-294">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="fd68d-295">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="fd68d-295">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd68d-296">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd68d-296">Requirements</span></span>



| <span data-ttu-id="fd68d-297">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd68d-297">Requirement</span></span> | <span data-ttu-id="fd68d-298">Value</span><span class="sxs-lookup"><span data-stu-id="fd68d-298">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd68d-299">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fd68d-299">Minimum supported client</span></span><br/> | <span data-ttu-id="fd68d-300">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fd68d-300">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fd68d-301">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fd68d-301">Minimum supported server</span></span><br/> | <span data-ttu-id="fd68d-302">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fd68d-302">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fd68d-303">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="fd68d-303">Namespace</span></span><br/>                | <span data-ttu-id="fd68d-304">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="fd68d-304">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fd68d-305">MOF</span><span class="sxs-lookup"><span data-stu-id="fd68d-305">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fd68d-306"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fd68d-306"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fd68d-307">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fd68d-307">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd68d-308"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd68d-308"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd68d-309">Vea también</span><span class="sxs-lookup"><span data-stu-id="fd68d-309">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd68d-310">**\_SYSTEMRESOURCE CIM**</span><span class="sxs-lookup"><span data-stu-id="fd68d-310">**CIM\_SystemResource**</span></span>](cim-systemresource.md)
</dt> </dl>

 

