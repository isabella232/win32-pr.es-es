---
description: La \_ clase WMI DMAChannel de Win32 representa un canal de acceso directo a memoria (DMA) en un equipo que ejecuta Windows.
ms.assetid: cc517aac-7bd4-4937-8b07-2597076fca2c
ms.tgt_platform: multiple
title: Win32_DMAChannel (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DMAChannel
- Win32_DMAChannel.AddressSize
- Win32_DMAChannel.Availability
- Win32_DMAChannel.BurstMode
- Win32_DMAChannel.ByteMode
- Win32_DMAChannel.Caption
- Win32_DMAChannel.ChannelTiming
- Win32_DMAChannel.CreationClassName
- Win32_DMAChannel.CSCreationClassName
- Win32_DMAChannel.CSName
- Win32_DMAChannel.Description
- Win32_DMAChannel.DMAChannel
- Win32_DMAChannel.InstallDate
- Win32_DMAChannel.MaxTransferSize
- Win32_DMAChannel.Name
- Win32_DMAChannel.Port
- Win32_DMAChannel.Status
- Win32_DMAChannel.TransferWidths
- Win32_DMAChannel.TypeCTiming
- Win32_DMAChannel.WordMode
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0c2b36ff17931133d0dc4529e34f31ac24e00653
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907419"
---
# <a name="win32_dmachannel-class"></a><span data-ttu-id="53685-103">\_Clase Win32 DMAChannel</span><span class="sxs-lookup"><span data-stu-id="53685-103">Win32\_DMAChannel class</span></span>

<span data-ttu-id="53685-104">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ DMAChannel de Win32** representa un canal de acceso directo a memoria (DMA) en un equipo que ejecuta Windows.</span><span class="sxs-lookup"><span data-stu-id="53685-104">The **Win32\_DMAChannel** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a direct memory access (DMA) channel on a computer system running Windows.</span></span> <span data-ttu-id="53685-105">DMA es un método para mover datos desde un dispositivo a la memoria (o viceversa) sin la ayuda del microprocesador.</span><span class="sxs-lookup"><span data-stu-id="53685-105">DMA is a method of moving data from a device to memory (or vice versa) without the help of the microprocessor.</span></span> <span data-ttu-id="53685-106">La placa del sistema usa un controlador DMA para controlar un número fijo de canales, cada uno de los cuales puede usarse en un solo dispositivo cada vez.</span><span class="sxs-lookup"><span data-stu-id="53685-106">The system board uses a DMA controller to handle a fixed number of channels, each of which can be used by one (and only one) device at a time.</span></span>

<span data-ttu-id="53685-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="53685-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="53685-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="53685-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="53685-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="53685-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D1-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DMAChannel : CIM_DMA
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
  uint32   Port;
  string   Status;
  uint16   TransferWidths[];
  uint16   TypeCTiming;
  uint16   WordMode;
};
```

## <a name="members"></a><span data-ttu-id="53685-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="53685-110">Members</span></span>

<span data-ttu-id="53685-111">La **clase \_ DMAChannel de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="53685-111">The **Win32\_DMAChannel** class has these types of members:</span></span>

-   [<span data-ttu-id="53685-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="53685-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="53685-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="53685-113">Properties</span></span>

<span data-ttu-id="53685-114">La **clase \_ DMAChannel de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="53685-114">The **Win32\_DMAChannel** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="53685-115">**AddressSize**</span><span class="sxs-lookup"><span data-stu-id="53685-115">**AddressSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53685-116">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="53685-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="53685-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="53685-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53685-118">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Recurso del sistema DMTF información \| de DMA 001,3 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="53685-118">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.3"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="53685-119">Tamaño de dirección de canal DMA en bits.</span><span class="sxs-lookup"><span data-stu-id="53685-119">DMA channel address size in bits.</span></span> <span data-ttu-id="53685-120">Los valores permitidos son 8, 16, 32 o 64 bits.</span><span class="sxs-lookup"><span data-stu-id="53685-120">Permissible values are 8, 16, 32, or 64 bits.</span></span> <span data-ttu-id="53685-121">Si es desconocido, escriba 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="53685-121">If unknown, enter 0 (zero).</span></span>

<span data-ttu-id="53685-122">Esta propiedad se hereda del [**\_ DMA de CIM**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="53685-122">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

<dt>



 <span data-ttu-id="53685-123"> (0)</span><span class="sxs-lookup"><span data-stu-id="53685-123">(0)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="53685-124">(8)</span><span class="sxs-lookup"><span data-stu-id="53685-124">(8)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="53685-125">(16)</span><span class="sxs-lookup"><span data-stu-id="53685-125">(16)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="53685-126">(32)</span><span class="sxs-lookup"><span data-stu-id="53685-126">(32)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="53685-127">(64)</span><span class="sxs-lookup"><span data-stu-id="53685-127">(64)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="53685-128">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="53685-128">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53685-129">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="53685-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="53685-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="53685-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53685-131">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| DMA \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="53685-131">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|DMA\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="53685-132">Disponibilidad del DMA.</span><span class="sxs-lookup"><span data-stu-id="53685-132">Availability of the DMA.</span></span> <span data-ttu-id="53685-133">Esta propiedad se hereda del [**\_ DMA de CIM**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="53685-133">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="53685-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="53685-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="53685-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="53685-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>

<span data-ttu-id="53685-136"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Disponible** (3)</span><span class="sxs-lookup"><span data-stu-id="53685-136"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Available** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>

<span data-ttu-id="53685-137"><span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>**En uso/no disponible** (4)</span><span class="sxs-lookup"><span data-stu-id="53685-137"><span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>**In Use/Not Available** (4)</span></span>


</dt> <dd>

<span data-ttu-id="53685-138">En uso o no disponible</span><span class="sxs-lookup"><span data-stu-id="53685-138">In Use or Not Available</span></span>

</dd> <dt>

<span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>

<span data-ttu-id="53685-139"><span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>**En uso y disponible/compartible** (5)</span><span class="sxs-lookup"><span data-stu-id="53685-139"><span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>**In Use and Available/Shareable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="53685-140">En uso y disponible o compartible</span><span class="sxs-lookup"><span data-stu-id="53685-140">In Use and Available or Sharable</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="53685-141">**BurstMode**</span><span class="sxs-lookup"><span data-stu-id="53685-141">**BurstMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53685-142">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="53685-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="53685-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="53685-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53685-144">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| DMA \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="53685-144">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|DMA\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="53685-145">Indica si el canal DMA admite el modo de ráfaga.</span><span class="sxs-lookup"><span data-stu-id="53685-145">Indicates whether or not the DMA channel supports burst mode.</span></span>

<span data-ttu-id="53685-146">Esta propiedad se hereda del [**\_ DMA de CIM**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="53685-146">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

</dd> <dt>

<span data-ttu-id="53685-147">**ByteMode**</span><span class="sxs-lookup"><span data-stu-id="53685-147">**ByteMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53685-148">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="53685-148">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="53685-149">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="53685-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53685-150">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Recurso del sistema DMTF información de DMA \| 001,7 ")</span><span class="sxs-lookup"><span data-stu-id="53685-150">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="53685-151">Modo de ejecución de DMA.</span><span class="sxs-lookup"><span data-stu-id="53685-151">DMA execution mode.</span></span>

<span data-ttu-id="53685-152">Esta propiedad se hereda del [**\_ DMA de CIM**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="53685-152">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="53685-153"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="53685-153"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="53685-154"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="53685-154"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_execute_in__count_by_byte__mode"></span><span id="not_execute_in__count_by_byte__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>

<span data-ttu-id="53685-155"><span id="Not_execute_in__count_by_byte__mode"></span><span id="not_execute_in__count_by_byte__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>**No se ejecuta en modo "recuento por byte"** (3)</span><span class="sxs-lookup"><span data-stu-id="53685-155"><span id="Not_execute_in__count_by_byte__mode"></span><span id="not_execute_in__count_by_byte__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>**Not execute in 'count by byte' mode** (3)</span></span>


</dt> <dd>

<span data-ttu-id="53685-156">No se ejecuta en modo "recuento por byte"</span><span class="sxs-lookup"><span data-stu-id="53685-156">Does not execute in "count by byte" mode</span></span>

</dd> <dt>

<span id="Execute_in__count_by_byte__mode"></span><span id="execute_in__count_by_byte__mode"></span><span id="EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>

<span data-ttu-id="53685-157"><span id="Execute_in__count_by_byte__mode"></span><span id="execute_in__count_by_byte__mode"></span><span id="EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>**Ejecutar en modo "recuento por byte"** (4)</span><span class="sxs-lookup"><span data-stu-id="53685-157"><span id="Execute_in__count_by_byte__mode"></span><span id="execute_in__count_by_byte__mode"></span><span id="EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>**Execute in 'count by byte' mode** (4)</span></span>


</dt> <dd>

<span data-ttu-id="53685-158">Ejecutar en modo "recuento por byte"</span><span class="sxs-lookup"><span data-stu-id="53685-158">Execute in "count by byte" mode</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="53685-159">**Caption**</span><span class="sxs-lookup"><span data-stu-id="53685-159">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53685-160">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="53685-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="53685-161">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="53685-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53685-162">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="53685-162">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="53685-163">Breve descripción del objeto de una cadena de una línea.</span><span class="sxs-lookup"><span data-stu-id="53685-163">Short description of the object a one-line string.</span></span>

<span data-ttu-id="53685-164">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="53685-164">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="53685-165">**ChannelTiming**</span><span class="sxs-lookup"><span data-stu-id="53685-165">**ChannelTiming**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53685-166">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="53685-166">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="53685-167">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="53685-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53685-168">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Recurso del sistema DMTF información de DMA \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="53685-168">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="53685-169">Temporización del canal DMA.</span><span class="sxs-lookup"><span data-stu-id="53685-169">DMA channel timing.</span></span>

<span data-ttu-id="53685-170">Esta propiedad se hereda del [**\_ DMA de CIM**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="53685-170">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="53685-171">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="53685-171">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="53685-172">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="53685-172">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA_Compatible"></span><span id="isa_compatible"></span><span id="ISA_COMPATIBLE"></span>

<span data-ttu-id="53685-173">**Compatible con ISA** (3)</span><span class="sxs-lookup"><span data-stu-id="53685-173">**ISA Compatible** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Type_A"></span><span id="type_a"></span><span id="TYPE_A"></span>

<span data-ttu-id="53685-174">**Escriba A** (4)</span><span class="sxs-lookup"><span data-stu-id="53685-174">**Type A** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Type_B"></span><span id="type_b"></span><span id="TYPE_B"></span>

<span data-ttu-id="53685-175">**Tipo B** (5)</span><span class="sxs-lookup"><span data-stu-id="53685-175">**Type B** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Type_F"></span><span id="type_f"></span><span id="TYPE_F"></span>

<span data-ttu-id="53685-176">**Escriba F** (6)</span><span class="sxs-lookup"><span data-stu-id="53685-176">**Type F** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="53685-177">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="53685-177">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53685-178">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="53685-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="53685-179">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="53685-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53685-180">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="53685-180">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="53685-181">Nombre de la primera clase concreta que debe aparecer en la cadena de herencia utilizada en la creación de una instancia.</span><span class="sxs-lookup"><span data-stu-id="53685-181">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="53685-182">Cuando se usa con las otras propiedades de clave de la clase, la propiedad permite que todas las instancias de esta clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="53685-182">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="53685-183">Esta propiedad se hereda del [**\_ DMA de CIM**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="53685-183">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

</dd> <dt>

<span data-ttu-id="53685-184">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="53685-184">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53685-185">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="53685-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="53685-186">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="53685-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53685-187">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="53685-187">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="53685-188">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="53685-188">Name of the scoping computer system creation class.</span></span>

<span data-ttu-id="53685-189">Esta propiedad se hereda del [**\_ DMA de CIM**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="53685-189">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

</dd> <dt>

<span data-ttu-id="53685-190">**CSName**</span><span class="sxs-lookup"><span data-stu-id="53685-190">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53685-191">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="53685-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="53685-192">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="53685-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53685-193">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Nombre**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="53685-193">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="53685-194">Nombre del sistema de ámbito del equipo.</span><span class="sxs-lookup"><span data-stu-id="53685-194">Name of the scoping computer system.</span></span>

<span data-ttu-id="53685-195">Esta propiedad se hereda del [**\_ DMA de CIM**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="53685-195">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

</dd> <dt>

<span data-ttu-id="53685-196">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="53685-196">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53685-197">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="53685-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="53685-198">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="53685-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53685-199">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="53685-199">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="53685-200">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="53685-200">Description of the object.</span></span>

<span data-ttu-id="53685-201">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="53685-201">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="53685-202">**DMAChannel**</span><span class="sxs-lookup"><span data-stu-id="53685-202">**DMAChannel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53685-203">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="53685-203">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="53685-204">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="53685-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53685-205">Calificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| DMA \| 001,1 ")</span><span class="sxs-lookup"><span data-stu-id="53685-205">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|DMA\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="53685-206">Número de canal DMA, parte del valor de clave del objeto.</span><span class="sxs-lookup"><span data-stu-id="53685-206">DMA channel number, part of the object's key value.</span></span>

<span data-ttu-id="53685-207">Esta propiedad se hereda del [**\_ DMA de CIM**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="53685-207">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

</dd> <dt>

<span data-ttu-id="53685-208">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="53685-208">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53685-209">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="53685-209">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="53685-210">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="53685-210">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53685-211">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="53685-211">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="53685-212">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="53685-212">Date and time the object was installed.</span></span> <span data-ttu-id="53685-213">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="53685-213">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="53685-214">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="53685-214">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="53685-215">**MaxTransferSize**</span><span class="sxs-lookup"><span data-stu-id="53685-215">**MaxTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53685-216">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="53685-216">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="53685-217">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="53685-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53685-218">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Recurso del sistema DMTF información DMA \| 001,4 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="53685-218">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="53685-219">Número máximo de bytes que puede transferir este canal DMA.</span><span class="sxs-lookup"><span data-stu-id="53685-219">Maximum number of bytes that can be transferred by this DMA channel.</span></span> <span data-ttu-id="53685-220">Si es desconocido, escriba 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="53685-220">If unknown, enter 0 (zero).</span></span>

<span data-ttu-id="53685-221">Esta propiedad se hereda del [**\_ DMA de CIM**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="53685-221">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

</dd> <dt>

<span data-ttu-id="53685-222">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="53685-222">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53685-223">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="53685-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="53685-224">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="53685-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53685-225">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="53685-225">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="53685-226">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="53685-226">Label by which the object is known.</span></span> <span data-ttu-id="53685-227">Cuando se subclasen, la propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="53685-227">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="53685-228">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="53685-228">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="53685-229">**Puerto**</span><span class="sxs-lookup"><span data-stu-id="53685-229">**Port**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53685-230">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="53685-230">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="53685-231">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="53685-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53685-232">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| System Structure \| [**cm \_ partial \_ Resource \_ descriptor**](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_cm_partial_resource_descriptor) \| DMA \| Port")</span><span class="sxs-lookup"><span data-stu-id="53685-232">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|System Structures\|[**CM\_PARTIAL\_RESOURCE\_DESCRIPTOR**](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_cm_partial_resource_descriptor)\|Dma\|Port")</span></span>
</dt> </dl>

<span data-ttu-id="53685-233">Puerto DMA que usa el adaptador de bus host.</span><span class="sxs-lookup"><span data-stu-id="53685-233">DMA port used by the host bus adapter.</span></span> <span data-ttu-id="53685-234">Esto es significativo para buses de tipo MCA.</span><span class="sxs-lookup"><span data-stu-id="53685-234">This is meaningful for MCA-type buses.</span></span>

<span data-ttu-id="53685-235">Ejemplo: 12</span><span class="sxs-lookup"><span data-stu-id="53685-235">Example: 12</span></span>

</dd> <dt>

<span data-ttu-id="53685-236">**Estado**</span><span class="sxs-lookup"><span data-stu-id="53685-236">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53685-237">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="53685-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="53685-238">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="53685-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53685-239">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="53685-239">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="53685-240">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="53685-240">Current status of the object.</span></span> <span data-ttu-id="53685-241">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="53685-241">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="53685-242">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="53685-242">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="53685-243">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="53685-243">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="53685-244">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="53685-244">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="53685-245">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="53685-245">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="53685-246">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="53685-246">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="53685-247">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="53685-247">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="53685-248">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="53685-248">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="53685-249">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="53685-249">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="53685-250">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="53685-250">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="53685-251">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="53685-251">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="53685-252">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="53685-252">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="53685-253">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="53685-253">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="53685-254">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="53685-254">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="53685-255">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="53685-255">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="53685-256">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="53685-256">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="53685-257">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="53685-257">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="53685-258">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="53685-258">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="53685-259">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="53685-259">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="53685-260">**TransferWidths**</span><span class="sxs-lookup"><span data-stu-id="53685-260">**TransferWidths**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53685-261">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="53685-261">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="53685-262">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="53685-262">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53685-263">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Recurso del sistema DMTF información \| de DMA 001,2 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="53685-263">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="53685-264">Matriz de todos los anchos de transferencia (en bits) admitidos por este canal DMA.</span><span class="sxs-lookup"><span data-stu-id="53685-264">Array of all the transfer widths (in bits) supported by this DMA channel.</span></span> <span data-ttu-id="53685-265">Si es desconocido, escriba 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="53685-265">If unknown, enter 0 (zero).</span></span>

<span data-ttu-id="53685-266">Esta propiedad se hereda del [**\_ DMA de CIM**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="53685-266">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

<dt>



 <span data-ttu-id="53685-267"> (0)</span><span class="sxs-lookup"><span data-stu-id="53685-267">(0)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="53685-268">(8)</span><span class="sxs-lookup"><span data-stu-id="53685-268">(8)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="53685-269">(16)</span><span class="sxs-lookup"><span data-stu-id="53685-269">(16)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="53685-270">(32)</span><span class="sxs-lookup"><span data-stu-id="53685-270">(32)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="53685-271">(64)</span><span class="sxs-lookup"><span data-stu-id="53685-271">(64)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="53685-272">(128)</span><span class="sxs-lookup"><span data-stu-id="53685-272">(128)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="53685-273">**TypeCTiming**</span><span class="sxs-lookup"><span data-stu-id="53685-273">**TypeCTiming**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53685-274">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="53685-274">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="53685-275">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="53685-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53685-276">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Recurso del sistema DMTF información de DMA \| 001,10 ")</span><span class="sxs-lookup"><span data-stu-id="53685-276">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.10")</span></span>
</dt> </dl>

<span data-ttu-id="53685-277">Compatibilidad con el tiempo de tipo C (ráfaga).</span><span class="sxs-lookup"><span data-stu-id="53685-277">Support for C type (burst) timing.</span></span>

<span data-ttu-id="53685-278">Esta propiedad se hereda del [**\_ DMA de CIM**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="53685-278">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="53685-279">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="53685-279">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="53685-280">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="53685-280">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA_Compatible"></span><span id="isa_compatible"></span><span id="ISA_COMPATIBLE"></span>

<span data-ttu-id="53685-281">**Compatible con ISA** (3)</span><span class="sxs-lookup"><span data-stu-id="53685-281">**ISA Compatible** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="53685-282">**No compatible** (4)</span><span class="sxs-lookup"><span data-stu-id="53685-282">**Not Supported** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span>

<span data-ttu-id="53685-283">**Compatible** (5)</span><span class="sxs-lookup"><span data-stu-id="53685-283">**Supported** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="53685-284">**WordMode**</span><span class="sxs-lookup"><span data-stu-id="53685-284">**WordMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53685-285">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="53685-285">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="53685-286">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="53685-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53685-287">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Recurso del sistema DMTF información de DMA \| 001,8 ")</span><span class="sxs-lookup"><span data-stu-id="53685-287">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.8")</span></span>
</dt> </dl>

<span data-ttu-id="53685-288">Modo de ejecución de DMA.</span><span class="sxs-lookup"><span data-stu-id="53685-288">DMA execution mode.</span></span>

<span data-ttu-id="53685-289">Esta propiedad se hereda del [**\_ DMA de CIM**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="53685-289">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="53685-290"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="53685-290"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="53685-291"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="53685-291"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_execute_in__count_by_word__mode"></span><span id="not_execute_in__count_by_word__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_WORD__MODE"></span>

<span data-ttu-id="53685-292"><span id="Not_execute_in__count_by_word__mode"></span><span id="not_execute_in__count_by_word__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_WORD__MODE"></span>**No se ejecuta en modo "recuento por palabra"** (3)</span><span class="sxs-lookup"><span data-stu-id="53685-292"><span id="Not_execute_in__count_by_word__mode"></span><span id="not_execute_in__count_by_word__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_WORD__MODE"></span>**Not execute in 'count by word' mode** (3)</span></span>


</dt> <dd>

<span data-ttu-id="53685-293">No se ejecuta en modo "recuento por palabra"</span><span class="sxs-lookup"><span data-stu-id="53685-293">Does not execute in "count by word" mode</span></span>

</dd> <dt>

<span id="Execute_in__count_by_word__mode"></span><span id="execute_in__count_by_word__mode"></span><span id="EXECUTE_IN__COUNT_BY_WORD__MODE"></span>

<span data-ttu-id="53685-294"><span id="Execute_in__count_by_word__mode"></span><span id="execute_in__count_by_word__mode"></span><span id="EXECUTE_IN__COUNT_BY_WORD__MODE"></span>**Ejecutar en modo "recuento por palabra"** (4)</span><span class="sxs-lookup"><span data-stu-id="53685-294"><span id="Execute_in__count_by_word__mode"></span><span id="execute_in__count_by_word__mode"></span><span id="EXECUTE_IN__COUNT_BY_WORD__MODE"></span>**Execute in 'count by word' mode** (4)</span></span>


</dt> <dd>

<span data-ttu-id="53685-295">Ejecutar en modo "recuento por palabra"</span><span class="sxs-lookup"><span data-stu-id="53685-295">Execute in "count by word" mode</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="53685-296">Observaciones</span><span class="sxs-lookup"><span data-stu-id="53685-296">Remarks</span></span>

<span data-ttu-id="53685-297">La **clase \_ DMAChannel de Win32** se deriva [**del \_ DMA CIM**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="53685-297">The **Win32\_DMAChannel** class is derived from [**CIM\_DMA**](cim-dma.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="53685-298">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53685-298">Requirements</span></span>



| <span data-ttu-id="53685-299">Requisito</span><span class="sxs-lookup"><span data-stu-id="53685-299">Requirement</span></span> | <span data-ttu-id="53685-300">Value</span><span class="sxs-lookup"><span data-stu-id="53685-300">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="53685-301">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="53685-301">Minimum supported client</span></span><br/> | <span data-ttu-id="53685-302">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="53685-302">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="53685-303">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="53685-303">Minimum supported server</span></span><br/> | <span data-ttu-id="53685-304">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="53685-304">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="53685-305">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="53685-305">Namespace</span></span><br/>                | <span data-ttu-id="53685-306">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="53685-306">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="53685-307">MOF</span><span class="sxs-lookup"><span data-stu-id="53685-307">MOF</span></span><br/>                      | <dl> <span data-ttu-id="53685-308"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="53685-308"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="53685-309">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="53685-309">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53685-310"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53685-310"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53685-311">Vea también</span><span class="sxs-lookup"><span data-stu-id="53685-311">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53685-312">**DMA de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="53685-312">**CIM\_DMA**</span></span>](cim-dma.md)
</dt> <dt>

[<span data-ttu-id="53685-313">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="53685-313">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

