---
description: Estas clases de WMI se declaran en CimWin32. mof.
ms.assetid: 53122499-1CC0-4B48-AEA1-B70B7BBC3A99
ms.tgt_platform: multiple
title: Proveedor WMI de CIM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a3249549e0915f51b6a9a6f2386c18ba695919a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538482"
---
# <a name="cim-wmi-provider"></a><span data-ttu-id="fde4c-103">Proveedor WMI de CIM</span><span class="sxs-lookup"><span data-stu-id="fde4c-103">CIM WMI Provider</span></span>

<span data-ttu-id="fde4c-104">Estas clases de WMI se declaran en CimWin32. mof.</span><span class="sxs-lookup"><span data-stu-id="fde4c-104">These WMI classes are declared in CimWin32.mof.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="fde4c-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="fde4c-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="fde4c-106">**Acción de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="fde4c-106">**CIM\_Action**</span></span>](cim-action.md)
</dt> <dd>

<span data-ttu-id="fde4c-107">Una clase de [**\_ acción CIM**](cim-action.md) es una operación que forma parte de un proceso para crear un elemento de software en su estado siguiente o para eliminar el elemento de software en el estado actual.</span><span class="sxs-lookup"><span data-stu-id="fde4c-107">A [**CIM\_Action**](cim-action.md) class is an operation that is part of a process to either create a software element in its next state or to eliminate the software element in the current state.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-108">**\_ACTIONSEQUENCE CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-108">**CIM\_ActionSequence**</span></span>](cim-actionsequence.md)
</dt> <dd>

<span data-ttu-id="fde4c-109">La [**Asociación \_ ActionSequence de CIM**](cim-actionsequence.md) define una serie de operaciones que transfieren el elemento de software (al que hace referencia la Asociación [**\_ SoftwareElementActions de CIM**](cim-softwareelementactions.md) ) al siguiente estado o quita el elemento de software de su estado actual.</span><span class="sxs-lookup"><span data-stu-id="fde4c-109">The [**CIM\_ActionSequence**](cim-actionsequence.md) association defines a series of operations that transition the software element (referenced by the [**CIM\_SoftwareElementActions**](cim-softwareelementactions.md) association) to its next state, or removes the software element from its current state.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-110">**\_ACTSASSPARE CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-110">**CIM\_ActsAsSpare**</span></span>](cim-actsasspare.md)
</dt> <dd>

<span data-ttu-id="fde4c-111">La [**Asociación \_ ActsAsSpare de CIM**](cim-actsasspare.md) indica qué elementos pueden ser repuestos o reemplazar otros elementos agregados.</span><span class="sxs-lookup"><span data-stu-id="fde4c-111">The [**CIM\_ActsAsSpare**](cim-actsasspare.md) association indicates which elements can be spares or replace other aggregated elements.</span></span> <span data-ttu-id="fde4c-112">Una reserva puede funcionar en modo de "espera activa" como se especifica en cada elemento.</span><span class="sxs-lookup"><span data-stu-id="fde4c-112">A spare can operate in "hot-standby" mode as specified on an element-by-element basis.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-113">**\_ADJACENTSLOTS CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-113">**CIM\_AdjacentSlots**</span></span>](cim-adjacentslots.md)
</dt> <dd>

<span data-ttu-id="fde4c-114">La [**Asociación \_ AdjacentSlots de CIM**](cim-adjacentslots.md) describe el diseño de las ranuras en una placa de hospedaje o en una tarjeta de adaptador.</span><span class="sxs-lookup"><span data-stu-id="fde4c-114">The [**CIM\_AdjacentSlots**](cim-adjacentslots.md) association describes the layout of slots on a hosting board or adapter card.</span></span> <span data-ttu-id="fde4c-115">La información, como la distancia entre las ranuras y si están "compartidas" (si se ha rellenado una, no se puede usar la otra ranura), se transmite como propiedades de asociación.</span><span class="sxs-lookup"><span data-stu-id="fde4c-115">Information, such as the distance between the slots and whether they are "shared" (if one is populated, then the other slot cannot be used), is conveyed as association properties.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-116">**\_AGGREGATEPEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-116">**CIM\_AggregatePExtent**</span></span>](cim-aggregatepextent.md)
</dt> <dd>

<span data-ttu-id="fde4c-117">La clase [**CIM \_ AggregatePExtent**](cim-aggregatepextent.md) proporciona información de resumen sobre los bloques lógicos direccionables, que están en el mismo grupo de redundancia de almacenamiento y se encuentran en el mismo medio físico.</span><span class="sxs-lookup"><span data-stu-id="fde4c-117">The [**CIM\_AggregatePExtent**](cim-aggregatepextent.md) class provides summary information about addressable logical blocks, which are in the same storage redundancy group and located on the same physical media.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-118">**\_AGGREGATEPSEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-118">**CIM\_AggregatePSExtent**</span></span>](cim-aggregatepsextent.md)
</dt> <dd>

<span data-ttu-id="fde4c-119">La clase [**CIM \_ AggregatePSExtent**](cim-aggregatepsextent.md) define el número de bloques lógicos direccionables en un único dispositivo de almacenamiento, excluidos los bloques lógicos asignados como datos de comprobación.</span><span class="sxs-lookup"><span data-stu-id="fde4c-119">The [**CIM\_AggregatePSExtent**](cim-aggregatepsextent.md) class defines the number of addressable logical blocks on a single storage device, excluding logical blocks mapped as check data.</span></span> <span data-ttu-id="fde4c-120">Si se definen conjuntos de volúmenes, los bloques lógicos se incluyen en un único conjunto de volúmenes.</span><span class="sxs-lookup"><span data-stu-id="fde4c-120">If volume sets are defined, the logical blocks are contained within a single volume set.</span></span> <span data-ttu-id="fde4c-121">Se trata de una agrupación alternativa para [**CIM \_ ProtectedSpaceExtent**](cim-protectedspaceextent.md), cuando solo se necesita información de resumen o cuando se usa la configuración automática.</span><span class="sxs-lookup"><span data-stu-id="fde4c-121">This is an alternative grouping for [**CIM\_ProtectedSpaceExtent**](cim-protectedspaceextent.md), when only summary information is needed or when automatic configuration is used.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-122">**\_AGGREGATEREDUNDANCYCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-122">**CIM\_AggregateRedundancyComponent**</span></span>](cim-aggregateredundancycomponent.md)
</dt> <dd>

<span data-ttu-id="fde4c-123">La clase [**CIM \_ AggregateRedundancyComponent**](cim-aggregateredundancycomponent.md) describe la extensión física agregada en un grupo de redundancia de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="fde4c-123">The [**CIM\_AggregateRedundancyComponent**](cim-aggregateredundancycomponent.md) class describes the aggregate physical extent in a storage redundancy group.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-124">**\_ALARMDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-124">**CIM\_AlarmDevice**</span></span>](cim-alarmdevice.md)
</dt> <dd>

<span data-ttu-id="fde4c-125">La [**clase \_ AlarmDevice de CIM**](cim-alarmdevice.md) es un dispositivo de alarma que emite indicaciones auditivas o visibles relacionadas con una situación problemática.</span><span class="sxs-lookup"><span data-stu-id="fde4c-125">The [**CIM\_AlarmDevice**](cim-alarmdevice.md) class is an alarm device that emits audible or visible indications related to a problem situation.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-126">**\_ALLOCATEDRESOURCE CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-126">**CIM\_AllocatedResource**</span></span>](cim-allocatedresource.md)
</dt> <dd>

<span data-ttu-id="fde4c-127">La clase [**CIM \_ AllocatedResource**](cim-allocatedresource.md) representa una asociación entre dispositivos lógicos y recursos del sistema e indica que el recurso está asignado al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fde4c-127">The [**CIM\_AllocatedResource**](cim-allocatedresource.md) class represents an association between logical devices and system resources and indicates that the resource is assigned to the device.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-128">**\_APPLICATIONSYSTEM CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-128">**CIM\_ApplicationSystem**</span></span>](cim-applicationsystem.md)
</dt> <dd>

<span data-ttu-id="fde4c-129">La clase [**CIM \_ ApplicationSystem**](cim-applicationsystem.md) representa una aplicación o un sistema de software que admite una determinada función empresarial que se puede administrar como una unidad independiente.</span><span class="sxs-lookup"><span data-stu-id="fde4c-129">The [**CIM\_ApplicationSystem**](cim-applicationsystem.md) class represents an application or software system that supports a particular business function that can be managed as an independent unit.</span></span> <span data-ttu-id="fde4c-130">Este tipo de sistema se puede descomponer en sus componentes funcionales mediante la clase [**CIM \_ SoftwareFeature**](cim-softwarefeature.md) .</span><span class="sxs-lookup"><span data-stu-id="fde4c-130">Such a system can be decomposed into its functional components using the [**CIM\_SoftwareFeature**](cim-softwarefeature.md) class.</span></span> <span data-ttu-id="fde4c-131">Las características de software de una aplicación o un sistema de software en particular se encuentran mediante la Asociación [**\_ ApplicationSystemSoftwareFeature de CIM**](cim-applicationsystemsoftwarefeature.md) .</span><span class="sxs-lookup"><span data-stu-id="fde4c-131">The software features for a particular application or software system are located using the [**CIM\_ApplicationSystemSoftwareFeature**](cim-applicationsystemsoftwarefeature.md) association.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-132">**\_APPLICATIONSYSTEMSOFTWAREFEATURE CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-132">**CIM\_ApplicationSystemSoftwareFeature**</span></span>](cim-applicationsystemsoftwarefeature.md)
</dt> <dd>

<span data-ttu-id="fde4c-133">La clase [**CIM \_ ApplicationSystemSoftwareFeature**](cim-applicationsystemsoftwarefeature.md) representa una asociación que identifica las características de software que componen un sistema de aplicación determinado.</span><span class="sxs-lookup"><span data-stu-id="fde4c-133">The [**CIM\_ApplicationSystemSoftwareFeature**](cim-applicationsystemsoftwarefeature.md) class represents an association that identifies the software features that make up a particular application system.</span></span> <span data-ttu-id="fde4c-134">Las características de software se pueden incluir en diferentes productos.</span><span class="sxs-lookup"><span data-stu-id="fde4c-134">The software features can be included in different products.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-135">**\_ASSOCIATEDALARM CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-135">**CIM\_AssociatedAlarm**</span></span>](cim-associatedalarm.md)
</dt> <dd>

<span data-ttu-id="fde4c-136">La [**dependencia \_ AssociatedAlarm de CIM**](cim-associatedalarm.md) asocia una alarma a un dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="fde4c-136">The [**CIM\_AssociatedAlarm**](cim-associatedalarm.md) dependency associates an alarm with a logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-137">**\_ASSOCIATEDBATTERY CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-137">**CIM\_AssociatedBattery**</span></span>](cim-associatedbattery.md)
</dt> <dd>

<span data-ttu-id="fde4c-138">La [**dependencia \_ AssociatedBattery de CIM**](cim-associatedbattery.md) asocia una batería a un dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="fde4c-138">The [**CIM\_AssociatedBattery**](cim-associatedbattery.md) dependency associates a battery with a logical device.</span></span> <span data-ttu-id="fde4c-139">Utilice esta asociación para modelar baterías individuales que componen un sistema de alimentación ininterrumpida (SAI).</span><span class="sxs-lookup"><span data-stu-id="fde4c-139">Use this association to model individual batteries that make up an uninterruptible power supply (UPS).</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-140">**\_ASSOCIATEDCOOLING CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-140">**CIM\_AssociatedCooling**</span></span>](cim-associatedcooling.md)
</dt> <dd>

<span data-ttu-id="fde4c-141">La [**Asociación \_ AssociatedCooling de CIM**](cim-associatedcooling.md) indica si los ventiladores u otros dispositivos de refrigeración son específicos de un dispositivo (en lugar de proporcionar la refrigeración del gabinete o del contenedor).</span><span class="sxs-lookup"><span data-stu-id="fde4c-141">The [**CIM\_AssociatedCooling**](cim-associatedcooling.md) association indicates when fans or other cooling devices are specific to a device (versus providing enclosure or cabinet cooling).</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-142">**\_ASSOCIATEDMEMORY CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-142">**CIM\_AssociatedMemory**</span></span>](cim-associatedmemory.md)
</dt> <dd>

<span data-ttu-id="fde4c-143">La [**clase \_ AssociateMemory de CIM**](cim-associatedmemory.md) asocia la memoria instalada o asociada, como la memoria caché con un dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="fde4c-143">The [**CIM\_AssociateMemory**](cim-associatedmemory.md) class associates installed or associated memory, such as cache memory with a logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-144">**\_ASSOCIATEDPROCESSORMEMORY CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-144">**CIM\_AssociatedProcessorMemory**</span></span>](cim-associatedprocessormemory.md)
</dt> <dd>

<span data-ttu-id="fde4c-145">La [**clase \_ AssociatedProcessorMemory de CIM**](cim-associatedprocessormemory.md) asocia el procesador y la memoria del sistema, o la memoria caché de un procesador.</span><span class="sxs-lookup"><span data-stu-id="fde4c-145">The [**CIM\_AssociatedProcessorMemory**](cim-associatedprocessormemory.md) class associates the processor and system memory, or a processor's cache.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-146">**\_ASSOCIATEDSENSOR CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-146">**CIM\_AssociatedSensor**</span></span>](cim-associatedsensor.md)
</dt> <dd>

<span data-ttu-id="fde4c-147">La [**clase \_ AssociatedSensor de CIM**](cim-associatedsensor.md) asocia un sensor instalado a un dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="fde4c-147">The [**CIM\_AssociatedSensor**](cim-associatedsensor.md) class associates an installed sensor with a logical device.</span></span> <span data-ttu-id="fde4c-148">El sensor mide las propiedades críticas de entrada y salida, y puede incluirse con el dispositivo o instalarse cerca.</span><span class="sxs-lookup"><span data-stu-id="fde4c-148">The sensor measures critical input and output properties, and can be included with the device or installed nearby.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-149">**\_ASSOCIATEDSUPPLYCURRENTSENSOR CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-149">**CIM\_AssociatedSupplyCurrentSensor**</span></span>](cim-associatedsupplycurrentsensor.md)
</dt> <dd>

<span data-ttu-id="fde4c-150">La [**clase \_ AssociatedSupplyCurrentSensor de CIM**](cim-associatedsupplycurrentsensor.md) asocia una fuente de alimentación con un sensor actual (amperaje) que supervisa la frecuencia de entrada.</span><span class="sxs-lookup"><span data-stu-id="fde4c-150">The [**CIM\_AssociatedSupplyCurrentSensor**](cim-associatedsupplycurrentsensor.md) class associates a power supply with a current (amperage) sensor that monitors its input frequency.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-151">**\_ASSOCIATEDSUPPLYVOLTAGESENSOR CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-151">**CIM\_AssociatedSupplyVoltageSensor**</span></span>](cim-associatedsupplyvoltagesensor.md)
</dt> <dd>

<span data-ttu-id="fde4c-152">Asocia una fuente de alimentación a un sensor de voltaje que supervisa su voltaje de entrada.</span><span class="sxs-lookup"><span data-stu-id="fde4c-152">Associates a power supply with a voltage sensor that monitors its input voltage.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-153">**\_BasedOn CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-153">**CIM\_BasedOn**</span></span>](cim-basedon.md)
</dt> <dd>

<span data-ttu-id="fde4c-154">La [**clase \_ basada en CIM**](cim-basedon.md) representa una asociación que describe cómo se pueden ensamblar las extensiones de almacenamiento de las extensiones de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="fde4c-154">The [**CIM\_BasedOn**](cim-basedon.md) class represents an association that describes how storage extents can be assembled from lower-level extents.</span></span> <span data-ttu-id="fde4c-155">Por ejemplo, las extensiones físicas incluyen extensiones de espacio protegido.</span><span class="sxs-lookup"><span data-stu-id="fde4c-155">For example, physical extents include protected space extents.</span></span> <span data-ttu-id="fde4c-156">Por lo tanto, los conjuntos de volúmenes se ensamblan a partir de una o más extensiones de espacio físico o protegido.</span><span class="sxs-lookup"><span data-stu-id="fde4c-156">Thus, volume sets are assembled from one or more physical or protected space extents.</span></span> <span data-ttu-id="fde4c-157">La memoria caché se puede definir de forma independiente y realizada en un elemento físico, o bien se puede basar en extensiones de almacenamiento volátiles o no volátiles.</span><span class="sxs-lookup"><span data-stu-id="fde4c-157">Cache memory can be defined independently and realized in a physical element, or it can be based on volatile or non-volatile storage extents.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-158">**\_Batería CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-158">**CIM\_Battery**</span></span>](cim-battery.md)
</dt> <dd>

<span data-ttu-id="fde4c-159">La clase de [**\_ batería CIM**](cim-battery.md) representa las capacidades y la administración del dispositivo lógico de batería.</span><span class="sxs-lookup"><span data-stu-id="fde4c-159">The [**CIM\_Battery**](cim-battery.md) class represents the capabilities and management of the battery logical device.</span></span> <span data-ttu-id="fde4c-160">Esta clase se aplica a las baterías de los sistemas portátiles y a otras baterías internas y externas.</span><span class="sxs-lookup"><span data-stu-id="fde4c-160">This class applies to batteries in laptop systems and other internal and external batteries.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-161">**\_BINARYSENSOR CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-161">**CIM\_BinarySensor**</span></span>](cim-binarysensor.md)
</dt> <dd>

<span data-ttu-id="fde4c-162">La clase [**CIM \_ BinarySensor**](cim-binarysensor.md) proporciona una salida booleana.</span><span class="sxs-lookup"><span data-stu-id="fde4c-162">The [**CIM\_BinarySensor**](cim-binarysensor.md) class provides a Boolean output.</span></span> <span data-ttu-id="fde4c-163">Las propiedades **CurrentState** y **PossibleStates** se agregaron para el sensor, por lo que la subclase **CIM \_ BinarySensor** ya no es necesaria, aunque se conserva por compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="fde4c-163">The **CurrentState** and **PossibleStates** properties were added for sensoring, thus making the **CIM\_BinarySensor** subclass no longer necessary, although, it is retained for backward compatibility.</span></span> <span data-ttu-id="fde4c-164">Se puede crear un sensor binario creando una instancia de un sensor con dos Estados posibles.</span><span class="sxs-lookup"><span data-stu-id="fde4c-164">A binary sensor can be created by instantiating a sensor with two possible states.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-165">**\_BIOSELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-165">**CIM\_BIOSElement**</span></span>](cim-bioselement.md)
</dt> <dd>

<span data-ttu-id="fde4c-166">La clase [**CIM \_ BIOSElement**](cim-bioselement.md) representa el software de bajo nivel que se carga en el almacenamiento no volátil y que se usa para iniciar y configurar un sistema de equipo.</span><span class="sxs-lookup"><span data-stu-id="fde4c-166">The [**CIM\_BIOSElement**](cim-bioselement.md) class represents the low-level software that is loaded into non-volatile storage and used to start and configure a computer system.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-167">**\_BIOSFEATURE CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-167">**CIM\_BIOSFeature**</span></span>](cim-biosfeature.md)
</dt> <dd>

<span data-ttu-id="fde4c-168">representa las capacidades del software de bajo nivel que se usa para iniciar y configurar un sistema de equipo.</span><span class="sxs-lookup"><span data-stu-id="fde4c-168">represents the capabilities of the low-level software that is used to start and configure a computer system.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-169">**\_BIOSFEATUREBIOSELEMENTS CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-169">**CIM\_BIOSFeatureBIOSElements**</span></span>](cim-biosfeaturebioselements.md)
</dt> <dd>

<span data-ttu-id="fde4c-170">La [**clase \_ BIOSFeatureBIOSElements de CIM**](cim-biosfeaturebioselements.md) asocia una característica de BIOS y sus elementos de BIOS agregados.</span><span class="sxs-lookup"><span data-stu-id="fde4c-170">The [**CIM\_BIOSFeatureBIOSElements**](cim-biosfeaturebioselements.md) class associates a BIOS feature and its aggregated BIOS elements.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-171">**\_BIOSLOADEDINNV CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-171">**CIM\_BIOSLoadedInNV**</span></span>](cim-biosloadedinnv.md)
</dt> <dd>

<span data-ttu-id="fde4c-172">La clase [**CIM \_ BIOSLoadedInNV**](cim-biosloadedinnv.md) asocia un elemento BIOS y el almacenamiento no volátil en el que se carga.</span><span class="sxs-lookup"><span data-stu-id="fde4c-172">The [**CIM\_BIOSLoadedInNV**](cim-biosloadedinnv.md) class associates a BIOS element and the non-volatile storage in which it is loaded.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-173">**\_BOOTOSFROMFS CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-173">**CIM\_BootOSFromFS**</span></span>](cim-bootosfromfs.md)
</dt> <dd>

<span data-ttu-id="fde4c-174">La [**clase \_ BootOSFromFS de CIM**](cim-bootosfromfs.md) asocia el sistema operativo y los sistemas de archivos desde los que se carga el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="fde4c-174">The [**CIM\_BootOSFromFS**](cim-bootosfromfs.md) class associates the operating system and the file systems from which the operating system is loaded.</span></span> <span data-ttu-id="fde4c-175">La asociación es de varios a varios; un sistema operativo distribuido puede depender de varios sistemas de archivos para que se carguen correctamente y por completo.</span><span class="sxs-lookup"><span data-stu-id="fde4c-175">The association is many-to-many; a distributed operating system can depend on several file systems to load correctly and completely.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-176">**\_BOOTSAP CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-176">**CIM\_BootSAP**</span></span>](cim-bootsap.md)
</dt> <dd>

<span data-ttu-id="fde4c-177">La clase [**CIM \_ BootSAP**](cim-bootsap.md) representa los puntos de acceso de un servicio de arranque.</span><span class="sxs-lookup"><span data-stu-id="fde4c-177">The [**CIM\_BootSAP**](cim-bootsap.md) class represents the access points of a boot service.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-178">**\_BOOTSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-178">**CIM\_BootService**</span></span>](cim-bootservice.md)
</dt> <dd>

<span data-ttu-id="fde4c-179">La clase [**CIM \_ BootService**](cim-bootservice.md) representa la funcionalidad proporcionada por un dispositivo o software, o por una red, para cargar un sistema operativo en un sistema de equipo unitario.</span><span class="sxs-lookup"><span data-stu-id="fde4c-179">The [**CIM\_BootService**](cim-bootservice.md) class represents the functionality provided by a device or software, or by a network, to load an operating system on a unitary computer system.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-180">**\_BOOTSERVICEACCESSBYSAP CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-180">**CIM\_BootServiceAccessBySAP**</span></span>](cim-bootserviceaccessbysap.md)
</dt> <dd>

<span data-ttu-id="fde4c-181">La [**clase \_ BootServiceAccessBySAP de CIM**](cim-bootserviceaccessbysap.md) asocia un servicio de arranque y sus puntos de acceso.</span><span class="sxs-lookup"><span data-stu-id="fde4c-181">The [**CIM\_BootServiceAccessBySAP**](cim-bootserviceaccessbysap.md) class associates a boot service and its access points.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-182">**\_CACHEMEMORY CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-182">**CIM\_CacheMemory**</span></span>](cim-cachememory.md)
</dt> <dd>

<span data-ttu-id="fde4c-183">La clase [**CIM \_ CacheMemory**](cim-cachememory.md) define las capacidades y la administración de la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="fde4c-183">The [**CIM\_CacheMemory**](cim-cachememory.md) class defines the capabilities and management of cache memory.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-184">**\_Tarjeta CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-184">**CIM\_Card**</span></span>](cim-card.md)
</dt> <dd>

<span data-ttu-id="fde4c-185">La clase de [**\_ tarjeta CIM**](cim-card.md) representa un tipo de contenedor físico que se puede conectar a otra tarjeta o panel de hospedaje, o es en sí mismo una placa de hospedaje o placa base en un chasis.</span><span class="sxs-lookup"><span data-stu-id="fde4c-185">The [**CIM\_Card**](cim-card.md) class represents a type of physical container that can be plugged into another card or hosting board, or is itself a hosting board/motherboard in a chassis.</span></span> <span data-ttu-id="fde4c-186">Esta clase incluye cualquier paquete capaz de llevar señales y proporcionar un punto de montaje para los componentes físicos, como chips u otros paquetes físicos, como otras tarjetas.</span><span class="sxs-lookup"><span data-stu-id="fde4c-186">This class includes any package that is capable of carrying signals and providing a mounting point for physical components, such as chips or other physical packages, such as other cards.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-187">**\_CARDINSLOT CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-187">**CIM\_CardInSlot**</span></span>](cim-cardinslot.md)
</dt> <dd>

<span data-ttu-id="fde4c-188">La clase [**CIM \_ CardInSlot**](cim-cardinslot.md) asocia una tarjeta de adaptador con el contenedor en el que se inserta.</span><span class="sxs-lookup"><span data-stu-id="fde4c-188">The [**CIM\_CardInSlot**](cim-cardinslot.md) class associates an adapter card with the container into which it is inserted.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-189">**\_CARDONCARD CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-189">**CIM\_CardOnCard**</span></span>](cim-cardoncard.md)
</dt> <dd>

<span data-ttu-id="fde4c-190">La [**Asociación \_ CardOnCard de CIM**](cim-cardoncard.md) describe las relaciones de las tarjetas que se pueden conectar a las motherboards/placas base, daughtercards de un adaptador o tarjetas que admiten módulos especiales de tipo tarjeta.</span><span class="sxs-lookup"><span data-stu-id="fde4c-190">The [**CIM\_CardOnCard**](cim-cardoncard.md) association describes relationships about cards that can be plugged into motherboards/baseboards, daughtercards of an adapter, or cards that support special card-like modules.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-191">**\_CDROMDRIVE CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-191">**CIM\_CDROMDrive**</span></span>](cim-cdromdrive.md)
</dt> <dd>

<span data-ttu-id="fde4c-192">La clase [**CIM \_ CDROMDrive**](cim-cdromdrive.md) representa una unidad de CD-ROM del equipo.</span><span class="sxs-lookup"><span data-stu-id="fde4c-192">The [**CIM\_CDROMDrive**](cim-cdromdrive.md) class represents a CD-ROM drive on the computer.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-193">**\_Chasis CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-193">**CIM\_Chassis**</span></span>](cim-chassis.md)
</dt> <dd>

<span data-ttu-id="fde4c-194">La clase del [**\_ chasis CIM**](cim-chassis.md) representa los elementos físicos que contienen otros elementos y proporcionan funcionalidad definible, como un escritorio, un nodo de procesamiento, un SAI, un almacenamiento en disco o en cinta, o una combinación de estos.</span><span class="sxs-lookup"><span data-stu-id="fde4c-194">The [**CIM\_Chassis**](cim-chassis.md) class represents the physical elements that enclose other elements and provide definable functionality, such as a desktop, processing node, UPS, disk or tape storage, or a combination of these.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-195">**\_CHASSISINRACK CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-195">**CIM\_ChassisInRack**</span></span>](cim-chassisinrack.md)
</dt> <dd>

<span data-ttu-id="fde4c-196">La [**Asociación \_ ChassisInRack de CIM**](cim-chassisinrack.md) representa la relación "que contiene" entre un bastidor y un chasis que contiene.</span><span class="sxs-lookup"><span data-stu-id="fde4c-196">The [**CIM\_ChassisInRack**](cim-chassisinrack.md) association represents the "containing" relationship between a rack and a chassis that it contains.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-197">**Comprobación de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="fde4c-197">**CIM\_Check**</span></span>](cim-check.md)
</dt> <dd>

<span data-ttu-id="fde4c-198">La clase de [**\_ comprobación CIM**](cim-check.md) representa una condición o característica que se espera que sea verdadera en un entorno definido o en el ámbito de una instancia de una clase de [**\_ ComputerSystem de CIM**](cim-computersystem.md) .</span><span class="sxs-lookup"><span data-stu-id="fde4c-198">The [**CIM\_Check**](cim-check.md) class represents a condition or characteristic that is expected to be true in an environment defined or scoped by an instance of a [**CIM\_ComputerSystem**](cim-computersystem.md) class.</span></span> <span data-ttu-id="fde4c-199">Las comprobaciones asociadas a un elemento de software determinado se organizan en uno de dos grupos mediante la propiedad **Phase** de la Asociación [**\_ SoftwareElementChecks de CIM**](cim-softwareelementchecks.md) .</span><span class="sxs-lookup"><span data-stu-id="fde4c-199">The checks associated with a particular software element are organized into one of two groups using the **Phase** property of the [**CIM\_SoftwareElementChecks**](cim-softwareelementchecks.md) association.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-200">**\_Chip CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-200">**CIM\_Chip**</span></span>](cim-chip.md)
</dt> <dd>

<span data-ttu-id="fde4c-201">La clase de [**\_ chip CIM**](cim-chip.md) representa el tipo de hardware de circuito integrado, incluidos Asics, procesadores, chips de memoria, etc.</span><span class="sxs-lookup"><span data-stu-id="fde4c-201">The [**CIM\_Chip**](cim-chip.md) class represents the type of integrated circuit hardware, including ASICs, processors, memory chips, and so on.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-202">**\_CLUSTERINGSAP CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-202">**CIM\_ClusteringSAP**</span></span>](cim-clusteringsap.md)
</dt> <dd>

<span data-ttu-id="fde4c-203">La clase [**CIM \_ ClusteringSAP**](cim-clusteringsap.md) representa los puntos de acceso de un servicio de agrupación en clústeres.</span><span class="sxs-lookup"><span data-stu-id="fde4c-203">The [**CIM\_ClusteringSAP**](cim-clusteringsap.md) class represents the access points of a clustering service.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-204">**\_CLUSTERINGSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-204">**CIM\_ClusteringService**</span></span>](cim-clusteringservice.md)
</dt> <dd>

<span data-ttu-id="fde4c-205">La clase [**CIM \_ ClusteringService**](cim-clusteringservice.md) representa la funcionalidad proporcionada por un clúster.</span><span class="sxs-lookup"><span data-stu-id="fde4c-205">The [**CIM\_ClusteringService**](cim-clusteringservice.md) class represents the functionality provided by a cluster.</span></span> <span data-ttu-id="fde4c-206">Por ejemplo, la funcionalidad de conmutación por error se puede modelar como un servicio de un clúster de conmutación por error.</span><span class="sxs-lookup"><span data-stu-id="fde4c-206">For example, failover functionality can be modeled as a service of a failover cluster.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-207">**\_CLUSTERSERVICEACCESSBYSAP CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-207">**CIM\_ClusterServiceAccessBySAP**</span></span>](cim-clusterserviceaccessbysap.md)
</dt> <dd>

<span data-ttu-id="fde4c-208">La clase [**CIM \_ ClusterServiceAccessBySAP**](cim-clusterserviceaccessbysap.md) representa la relación entre un servicio de agrupación en clústeres y sus puntos de acceso.</span><span class="sxs-lookup"><span data-stu-id="fde4c-208">The [**CIM\_ClusterServiceAccessBySAP**](cim-clusterserviceaccessbysap.md) class represents the relationship between a clustering service and its access points.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-209">**\_COLLECTEDCOLLECTIONS CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-209">**CIM\_CollectedCollections**</span></span>](cim-collectedcollections.md)
</dt> <dd>

<span data-ttu-id="fde4c-210">La [**clase \_ CollectedCollections de CIM**](cim-collectedcollections.md) es una asociación de agregación que representa una colección de elementos del sistema administrados (MSE) contenidos en una colección de MSEs.</span><span class="sxs-lookup"><span data-stu-id="fde4c-210">The [**CIM\_CollectedCollections**](cim-collectedcollections.md) class is an aggregation association that represents a collection of Managed System Elements (MSE) contained in a collection of MSEs.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-211">**\_COLLECTEDMSES CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-211">**CIM\_CollectedMSEs**</span></span>](cim-collectedmses.md)
</dt> <dd>

<span data-ttu-id="fde4c-212">La clase de asociación [**CIM \_ CollectedMSEs**](cim-collectedmses.md) representa los miembros del objeto de agrupación, una clase [**CollectionOfMSEs**](cim-collectionofmses.md) .</span><span class="sxs-lookup"><span data-stu-id="fde4c-212">The [**CIM\_CollectedMSEs**](cim-collectedmses.md) association class represents the members of the grouping object, a [**CollectionOfMSEs**](cim-collectionofmses.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-213">**CollectionOfMSEs de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="fde4c-213">**CIM\_CollectionOfMSEs**</span></span>](cim-collectionofmses.md)
</dt> <dd>

<span data-ttu-id="fde4c-214">El objeto [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) permite la agrupación de objetos [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md) con el fin de asociar configuraciones y configuraciones.</span><span class="sxs-lookup"><span data-stu-id="fde4c-214">The [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object allows the grouping of [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) objects for the purpose of associating settings and configurations.</span></span> <span data-ttu-id="fde4c-215">Es abstracto requerir más definición y perfeccionamiento semántico en las subclases.</span><span class="sxs-lookup"><span data-stu-id="fde4c-215">It is abstract to require further definition and semantic refinement in subclasses.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-216">**\_COLLECTIONOFSENSORS CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-216">**CIM\_CollectionOfSensors**</span></span>](cim-collectionofsensors.md)
</dt> <dd>

<span data-ttu-id="fde4c-217">La [**Asociación \_ CollectionOfSensors de CIM**](cim-collectionofsensors.md) representa los sensores binarios que componen el sensor de múltiples Estados.</span><span class="sxs-lookup"><span data-stu-id="fde4c-217">The [**CIM\_CollectionOfSensors**](cim-collectionofsensors.md) association represents the binary sensors that make up the multistate sensor.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-218">**\_COLLECTIONSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-218">**CIM\_CollectionSetting**</span></span>](cim-collectionsetting.md)
</dt> <dd>

<span data-ttu-id="fde4c-219">La clase [**CIM \_ CollectionSetting**](cim-collectionsetting.md) representa la asociación entre un [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) y la clase de configuración definida para ellos.</span><span class="sxs-lookup"><span data-stu-id="fde4c-219">The [**CIM\_CollectionSetting**](cim-collectionsetting.md) class represents the association between a [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) and the setting class defined for them.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-220">**\_COMPATIBLEPRODUCT CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-220">**CIM\_CompatibleProduct**</span></span>](cim-compatibleproduct.md)
</dt> <dd>

<span data-ttu-id="fde4c-221">La clase [**CIM \_ CompatibleProduct**](cim-compatibleproduct.md) representa una asociación entre productos que indica si dos productos a los que se hace referencia son interoperables, por ejemplo, si se pueden instalar juntos o si puede ser el contenedor físico del otro, etc.</span><span class="sxs-lookup"><span data-stu-id="fde4c-221">The [**CIM\_CompatibleProduct**](cim-compatibleproduct.md) class represents an association between products that indicates whether two referenced products are interoperable, such as whether they can be installed together, or whether one can be the physical container for the other, and so on.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-222">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-222">**CIM\_Component**</span></span>](cim-component.md)
</dt> <dd>

<span data-ttu-id="fde4c-223">La Asociación de [**\_ componentes CIM**](cim-component.md) representa las partes de una relación entre MSEs.</span><span class="sxs-lookup"><span data-stu-id="fde4c-223">The [**CIM\_Component**](cim-component.md) association represents the parts of a relationship between MSEs.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-224">**ComputerSystem de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="fde4c-224">**CIM\_ComputerSystem**</span></span>](cim-computersystem.md)
</dt> <dd>

<span data-ttu-id="fde4c-225">Una clase de [**\_ ComputerSystem de CIM**](cim-computersystem.md) representa una colección especial de instancias de los [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md) .</span><span class="sxs-lookup"><span data-stu-id="fde4c-225">A [**CIM\_ComputerSystem**](cim-computersystem.md) class represents a special collection of [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) instances.</span></span> <span data-ttu-id="fde4c-226">Esta colección proporciona funciones de equipo y actúa como un punto de agregación para asociar uno o varios de los siguientes elementos: sistema de archivos, sistema operativo, procesador y memoria (almacenamiento volátil y no volátil).</span><span class="sxs-lookup"><span data-stu-id="fde4c-226">This collection provides computer capabilities and serves as an aggregation point to associate one or more of the following elements: file system, operating system, processor and memory (volatile and non-volatile storage).</span></span> <span data-ttu-id="fde4c-227">Esta clase se deriva del [**\_ Sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="fde4c-227">This class is derived from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-228">**\_COMPUTERSYSTEMDMA CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-228">**CIM\_ComputerSystemDMA**</span></span>](cim-computersystemdma.md)
</dt> <dd>

<span data-ttu-id="fde4c-229">La clase [**CIM \_ ComputerSystemDMA**](cim-computersystemdma.md) representa una asociación entre un equipo y sus canales de acceso directo a memoria (DMA) disponibles.</span><span class="sxs-lookup"><span data-stu-id="fde4c-229">The [**CIM\_ComputerSystemDMA**](cim-computersystemdma.md) class represents an association between a computer system and its available direct memory access (DMA) channels.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-230">**\_COMPUTERSYSTEMIRQ CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-230">**CIM\_ComputerSystemIRQ**</span></span>](cim-computersystemirq.md)
</dt> <dd>

<span data-ttu-id="fde4c-231">La clase [**CIM \_ ComputerSystemIRQ**](cim-computersystemirq.md) representa una asociación entre un equipo y sus líneas de solicitud de interrupción (IRQ) disponibles.</span><span class="sxs-lookup"><span data-stu-id="fde4c-231">The [**CIM\_ComputerSystemIRQ**](cim-computersystemirq.md) class represents an association between a computer system and its available interrupt request lines (IRQs).</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-232">**\_COMPUTERSYSTEMMAPPEDIO CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-232">**CIM\_ComputerSystemMappedIO**</span></span>](cim-computersystemmappedio.md)
</dt> <dd>

<span data-ttu-id="fde4c-233">La clase [**CIM \_ ComputerSystemMappedIO**](cim-computersystemmappedio.md) representa una asociación entre un equipo y sus puertos de e/s asignados a memoria disponibles.</span><span class="sxs-lookup"><span data-stu-id="fde4c-233">The [**CIM\_ComputerSystemMappedIO**](cim-computersystemmappedio.md) class represents an association between a computer system and its available memory-mapped I/O ports.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-234">**\_COMPUTERSYSTEMPACKAGE CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-234">**CIM\_ComputerSystemPackage**</span></span>](cim-computersystempackage.md)
</dt> <dd>

<span data-ttu-id="fde4c-235">La clase [**CIM \_ ComputerSystemPackage**](cim-computersystempackage.md) representa una asociación que define explícitamente la relación entre los sistemas de equipos unitarios y uno o varios paquetes físicos.</span><span class="sxs-lookup"><span data-stu-id="fde4c-235">The [**CIM\_ComputerSystemPackage**](cim-computersystempackage.md) class represents an association that explicitly defines the relationship between unitary computer systems and one or more physical packages.</span></span> <span data-ttu-id="fde4c-236">La asociación es similar a la forma en que los dispositivos lógicos se encontraban en los elementos físicos.</span><span class="sxs-lookup"><span data-stu-id="fde4c-236">The association is similar to the way that logical devices are realized by physical elements.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-237">**\_COMPUTERSYSTEMRESOURCE CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-237">**CIM\_ComputerSystemResource**</span></span>](cim-computersystemresource.md)
</dt> <dd>

<span data-ttu-id="fde4c-238">La clase [**CIM \_ ComputerSystemResource**](cim-computersystemresource.md) representa una asociación entre un equipo y sus recursos del sistema disponibles.</span><span class="sxs-lookup"><span data-stu-id="fde4c-238">The [**CIM\_ComputerSystemResource**](cim-computersystemresource.md) class represents an association between a computer system and its available system resources.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-239">**Configuración de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="fde4c-239">**CIM\_Configuration**</span></span>](cim-configuration.md)
</dt> <dd>

<span data-ttu-id="fde4c-240">El objeto de [**\_ configuración de CIM**](cim-configuration.md) permite agrupar los conjuntos de parámetros (definidos en objetos de [**\_ configuración de CIM**](cim-setting.md) ) y las dependencias de uno o más elementos del sistema administrados.</span><span class="sxs-lookup"><span data-stu-id="fde4c-240">The [**CIM\_Configuration**](cim-configuration.md) object allows the grouping of parameter sets (defined in [**CIM\_Setting**](cim-setting.md) objects) and dependencies for one or more managed system elements.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-241">**\_Connected de CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-241">**CIM\_ConnectedTo**</span></span>](cim-connectedto.md)
</dt> <dd>

<span data-ttu-id="fde4c-242">La clase de [**CIM \_ Connected**](cim-connectedto.md) representa una asociación que indica que dos o más conectores físicos están conectados.</span><span class="sxs-lookup"><span data-stu-id="fde4c-242">The [**CIM\_ConnectedTo**](cim-connectedto.md) class represents an association that indicates that two or more physical connectors are connected.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-243">**\_CONNECTORONPACKAGE CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-243">**CIM\_ConnectorOnPackage**</span></span>](cim-connectoronpackage.md)
</dt> <dd>

<span data-ttu-id="fde4c-244">La clase [**CIM \_ ConnectorOnPackage**](cim-connectoronpackage.md) representa una asociación que hace explícita la relación de contención entre los conectores y los paquetes.</span><span class="sxs-lookup"><span data-stu-id="fde4c-244">The [**CIM\_ConnectorOnPackage**](cim-connectoronpackage.md) class represents an association that makes explicit the containment relationship between connectors and packages.</span></span> <span data-ttu-id="fde4c-245">Los paquetes físicos contienen conectores y otros elementos físicos.</span><span class="sxs-lookup"><span data-stu-id="fde4c-245">Physical packages contain connectors as well as other physical elements.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-246">**\_Contenedor CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-246">**CIM\_Container**</span></span>](cim-container.md)
</dt> <dd>

<span data-ttu-id="fde4c-247">La clase de [**\_ contenedor CIM**](cim-container.md) representa una asociación entre un elemento contenido y un elemento físico contenedor.</span><span class="sxs-lookup"><span data-stu-id="fde4c-247">The [**CIM\_Container**](cim-container.md) class represents an association between a contained and a containing physical element.</span></span> <span data-ttu-id="fde4c-248">Un objeto contenedor debe ser un paquete físico.</span><span class="sxs-lookup"><span data-stu-id="fde4c-248">A containing object must be a physical package.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-249">**\_CONTROLLEDBY CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-249">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> <dd>

<span data-ttu-id="fde4c-250">La relación de [**\_ ControlledBy de CIM**](cim-controlledby.md) indica los dispositivos a los que se puede acceder o a los que se accede mediante el dispositivo lógico del controlador.</span><span class="sxs-lookup"><span data-stu-id="fde4c-250">The [**CIM\_ControlledBy**](cim-controlledby.md) relationship indicates which devices are commanded by, or accessed through, the controller logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-251">**\_Controlador CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-251">**CIM\_Controller**</span></span>](cim-controller.md)
</dt> <dd>

<span data-ttu-id="fde4c-252">La clase de [**\_ controlador CIM**](cim-controller.md) es una clase primaria para agrupar dispositivos varios relacionados con el control.</span><span class="sxs-lookup"><span data-stu-id="fde4c-252">The [**CIM\_Controller**](cim-controller.md) class is a parent class for grouping miscellaneous control-related devices.</span></span> <span data-ttu-id="fde4c-253">Algunos ejemplos de controladores son controladores SCSI, controladores USB y controladores serie.</span><span class="sxs-lookup"><span data-stu-id="fde4c-253">Examples of controllers are SCSI controllers, USB controllers, and serial controllers.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-254">**\_COOLINGDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-254">**CIM\_CoolingDevice**</span></span>](cim-coolingdevice.md)
</dt> <dd>

<span data-ttu-id="fde4c-255">La clase [**CIM \_ CoolingDevice**](cim-coolingdevice.md) representa las capacidades y la administración de dispositivos de enfriamiento.</span><span class="sxs-lookup"><span data-stu-id="fde4c-255">The [**CIM\_CoolingDevice**](cim-coolingdevice.md) class represents the capabilities and management of cooling devices.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-256">**\_COPYFILEACTION CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-256">**CIM\_CopyFileAction**</span></span>](cim-copyfileaction.md)
</dt> <dd>

<span data-ttu-id="fde4c-257">La clase [**CIM \_ CopyFileAction**](cim-copyfileaction.md) representa el traslado o la copia de archivos de un sistema informático a una nueva ubicación.</span><span class="sxs-lookup"><span data-stu-id="fde4c-257">The [**CIM\_CopyFileAction**](cim-copyfileaction.md) class represents moving or copying files from a computer system to a new location.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-258">**\_CREATEDIRECTORYACTION CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-258">**CIM\_CreateDirectoryAction**</span></span>](cim-createdirectoryaction.md)
</dt> <dd>

<span data-ttu-id="fde4c-259">La clase [**CIM \_ CreateDirectoryAction**](cim-createdirectoryaction.md) crea directorios vacíos para que los elementos de software se instalen de forma local.</span><span class="sxs-lookup"><span data-stu-id="fde4c-259">The [**CIM\_CreateDirectoryAction**](cim-createdirectoryaction.md) class creates empty directories for software elements to be installed locally.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-260">**\_CURRENTSENSOR CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-260">**CIM\_CurrentSensor**</span></span>](cim-currentsensor.md)
</dt> <dd>

<span data-ttu-id="fde4c-261">La [**clase \_ CurrentSensor de CIM**](cim-currentsensor.md) existe para la compatibilidad con versiones anteriores con las definiciones de esquema CIM anteriores.</span><span class="sxs-lookup"><span data-stu-id="fde4c-261">The [**CIM\_CurrentSensor**](cim-currentsensor.md) class exists for backward compatibility to earlier CIM schema definitions.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-262">**\_Archivo de archivos CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-262">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dd>

<span data-ttu-id="fde4c-263">La clase de [**\_ archivo**](cim-datafile.md) de datos CIM representa una colección con nombre de datos o código ejecutable.</span><span class="sxs-lookup"><span data-stu-id="fde4c-263">The [**CIM\_DataFile**](cim-datafile.md) class represents a named collection of data or executable code.</span></span> <span data-ttu-id="fde4c-264">Solo se devolverán las instancias de los archivos de los discos fijos locales</span><span class="sxs-lookup"><span data-stu-id="fde4c-264">Only instances of files on local fixed disks will be returned</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-265">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="fde4c-265">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dd>

<span data-ttu-id="fde4c-266">La clase de [**\_ dependencia CIM**](cim-dependency.md) representa una asociación que establece relaciones de dependencia entre objetos.</span><span class="sxs-lookup"><span data-stu-id="fde4c-266">The [**CIM\_Dependency**](cim-dependency.md) class represents an association that establishes dependency relationships between objects.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-267">**\_DEPENDENCYCONTEXT CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-267">**CIM\_DependencyContext**</span></span>](cim-dependencycontext.md)
</dt> <dd>

<span data-ttu-id="fde4c-268">La [**relación \_ DependencyContext de CIM**](cim-dependencycontext.md) asocia una clase de [**\_ dependencia CIM**](cim-dependency.md) a uno o más objetos de [**\_ configuración de CIM**](cim-configuration.md) .</span><span class="sxs-lookup"><span data-stu-id="fde4c-268">The [**CIM\_DependencyContext**](cim-dependencycontext.md) relationship associates a [**CIM\_Dependency**](cim-dependency.md) class with one or more [**CIM\_Configuration**](cim-configuration.md) objects.</span></span> <span data-ttu-id="fde4c-269">Por ejemplo, las dependencias de un equipo pueden cambiar en función de la red a la que está conectado el sistema.</span><span class="sxs-lookup"><span data-stu-id="fde4c-269">For example, a computer system's dependencies can change based on the network to which the system is attached.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-270">**\_DESKTOPMONITOR CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-270">**CIM\_DesktopMonitor**</span></span>](cim-desktopmonitor.md)
</dt> <dd>

<span data-ttu-id="fde4c-271">La clase [**CIM \_ DesktopMonitor**](cim-desktopmonitor.md) representa las capacidades y la administración del dispositivo lógico monitor de escritorio (CRT).</span><span class="sxs-lookup"><span data-stu-id="fde4c-271">The [**CIM\_DesktopMonitor**](cim-desktopmonitor.md) class represents the capabilities and management of the desktop monitor (CRT) logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-272">**\_DEVICEACCESSEDBYFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-272">**CIM\_DeviceAccessedByFile**</span></span>](cim-deviceaccessedbyfile.md)
</dt> <dd>

<span data-ttu-id="fde4c-273">La clase de asociación [**CIM \_ DeviceAccessedByFile**](cim-deviceaccessedbyfile.md) especifica el dispositivo lógico al que se tiene acceso mediante la clase [**\_ DeviceFile CIM**](cim-devicefile.md) a la que se hace referencia.</span><span class="sxs-lookup"><span data-stu-id="fde4c-273">The [**CIM\_DeviceAccessedByFile**](cim-deviceaccessedbyfile.md) association class specifies the logical device accessed by using the referenced [**CIM\_DeviceFile**](cim-devicefile.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-274">**DeviceConnection de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="fde4c-274">**CIM\_DeviceConnection**</span></span>](cim-deviceconnection.md)
</dt> <dd>

<span data-ttu-id="fde4c-275">La clase de Asociación de [**CIM \_ DeviceConnection**](cim-deviceconnection.md) representa dos o más dispositivos conectados.</span><span class="sxs-lookup"><span data-stu-id="fde4c-275">The [**CIM\_DeviceConnection**](cim-deviceconnection.md) association class represents two or more connected devices.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-276">**\_DEVICEERRORCOUNTS CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-276">**CIM\_DeviceErrorCounts**</span></span>](cim-deviceerrorcounts.md)
</dt> <dd>

<span data-ttu-id="fde4c-277">La clase [**CIM \_ DeviceErrorCounts**](cim-deviceerrorcounts.md) es una clase estadística que contiene contadores relacionados con errores para un dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="fde4c-277">The [**CIM\_DeviceErrorCounts**](cim-deviceerrorcounts.md) class is a statistical class that contains error-related counters for a logical device.</span></span> <span data-ttu-id="fde4c-278">Los tipos de errores se definen mediante CCITt (REC X. 733) e ISO (IEC 10164-4).</span><span class="sxs-lookup"><span data-stu-id="fde4c-278">The types of errors are defined by CCITT (Rec X.733) and ISO (IEC 10164-4).</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-279">**\_DEVICEFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-279">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> <dd>

<span data-ttu-id="fde4c-280">La clase [**CIM \_ DeviceFile**](cim-devicefile.md) representa un tipo de archivo lógico, que representa un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fde4c-280">The [**CIM\_DeviceFile**](cim-devicefile.md) class represents a type of logical file, which represents a device.</span></span> <span data-ttu-id="fde4c-281">Esta Convención es útil para los sistemas operativos que administran dispositivos mediante un modelo de e/s de secuencia de bytes.</span><span class="sxs-lookup"><span data-stu-id="fde4c-281">This convention is useful for operating systems that manage devices using a byte stream I/O model.</span></span> <span data-ttu-id="fde4c-282">El dispositivo lógico asociado a este archivo se especifica mediante la relación [**\_ DeviceAccessedByFile de CIM**](cim-deviceaccessedbyfile.md) .</span><span class="sxs-lookup"><span data-stu-id="fde4c-282">The logical device that is associated with this file is specified using the [**CIM\_DeviceAccessedByFile**](cim-deviceaccessedbyfile.md) relationship.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-283">**\_DEVICESAPIMPLEMENTATION CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-283">**CIM\_DeviceSAPImplementation**</span></span>](cim-devicesapimplementation.md)
</dt> <dd>

<span data-ttu-id="fde4c-284">La clase [**CIM \_ DeviceSAPImplementation**](cim-devicesapimplementation.md) representa una asociación entre un punto de acceso de servicio (SAP) y cómo se implementa.</span><span class="sxs-lookup"><span data-stu-id="fde4c-284">The [**CIM\_DeviceSAPImplementation**](cim-devicesapimplementation.md) class represents an association between a service access point (SAP) and how it is implemented.</span></span> <span data-ttu-id="fde4c-285">Cuando muchos dispositivos lógicos están asociados a un SAP, los elementos funcionan conjuntamente para proporcionar el punto de acceso.</span><span class="sxs-lookup"><span data-stu-id="fde4c-285">When many logical devices are associated with one SAP, the elements operate in conjunction to provide the access point.</span></span> <span data-ttu-id="fde4c-286">Si existen implementaciones diferentes de un SAP, cada implementación da como resultado la creación de instancias individuales del objeto SAP.</span><span class="sxs-lookup"><span data-stu-id="fde4c-286">If different implementations of a SAP exist, each implementation results in individual instantiations of the SAP object.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-287">**\_DEVICESERVICEIMPLEMENTATION CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-287">**CIM\_DeviceServiceImplementation**</span></span>](cim-deviceserviceimplementation.md)
</dt> <dd>

<span data-ttu-id="fde4c-288">La clase [**CIM \_ DeviceServiceImplementation**](cim-deviceserviceimplementation.md) representa una asociación entre un servicio y cómo se implementa.</span><span class="sxs-lookup"><span data-stu-id="fde4c-288">The [**CIM\_DeviceServiceImplementation**](cim-deviceserviceimplementation.md) class represents an association between a service and how it is implemented.</span></span> <span data-ttu-id="fde4c-289">Cuando hay varios dispositivos asociados a un servicio, los elementos funcionan conjuntamente para proporcionar el servicio.</span><span class="sxs-lookup"><span data-stu-id="fde4c-289">When multiple devices are associated with one service, the elements operate in conjunction to provide the service.</span></span> <span data-ttu-id="fde4c-290">Si existen implementaciones diferentes de un servicio, cada implementación tiene como resultado la creación de instancias individuales del objeto de servicio.</span><span class="sxs-lookup"><span data-stu-id="fde4c-290">If different implementations of a service exist, each implementation results in individual instantiations of the service object.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-291">**\_DEVICESOFTWARE CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-291">**CIM\_DeviceSoftware**</span></span>](cim-devicesoftware.md)
</dt> <dd>

<span data-ttu-id="fde4c-292">La [**relación \_ DeviceSoftware de CIM**](cim-devicesoftware.md) identifica el software que está asociado a un dispositivo, como controladores, software de la aplicación o de configuración, o firmware.</span><span class="sxs-lookup"><span data-stu-id="fde4c-292">The [**CIM\_DeviceSoftware**](cim-devicesoftware.md) relationship identifies software that is associated with a device, such as drivers, configuration or application software, or firmware.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-293">**\_Directorio CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-293">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> <dd>

<span data-ttu-id="fde4c-294">La clase de [**\_ directorio CIM**](cim-directory.md) representa un tipo de archivo que agrupa lógicamente los archivos de datos que contiene y proporciona información de la ruta de acceso para los archivos agrupados.</span><span class="sxs-lookup"><span data-stu-id="fde4c-294">The [**CIM\_Directory**](cim-directory.md) class represents a file type that logically groups the data files that it contains and provides path information for the grouped files.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-295">**\_DIRECTORYACTION CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-295">**CIM\_DirectoryAction**</span></span>](cim-directoryaction.md)
</dt> <dd>

<span data-ttu-id="fde4c-296">La clase abstracta [**\_ DirectoryAction de CIM**](cim-directoryaction.md) administra los directorios.</span><span class="sxs-lookup"><span data-stu-id="fde4c-296">The [**CIM\_DirectoryAction**](cim-directoryaction.md) abstract class manages directories.</span></span> <span data-ttu-id="fde4c-297">La clase [**CIM \_ CreateDirectoryAction**](cim-createdirectoryaction.md) controla la creación de directorios y la eliminación del directorio se controla mediante la clase [**\_ RemoveDirectoryAction de CIM**](cim-removedirectoryaction.md) .</span><span class="sxs-lookup"><span data-stu-id="fde4c-297">Directory creation is handled by the [**CIM\_CreateDirectoryAction**](cim-createdirectoryaction.md) class and directory removal is handled by the [**CIM\_RemoveDirectoryAction**](cim-removedirectoryaction.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-298">**\_DIRECTORYCONTAINSFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-298">**CIM\_DirectoryContainsFile**</span></span>](cim-directorycontainsfile.md)
</dt> <dd>

<span data-ttu-id="fde4c-299">La clase [**CIM \_ DirectoryContainsFile**](cim-directorycontainsfile.md) representa una asociación entre un directorio y los archivos contenidos en ese directorio.</span><span class="sxs-lookup"><span data-stu-id="fde4c-299">The [**CIM\_DirectoryContainsFile**](cim-directorycontainsfile.md) class represents an association between a directory and files contained within that directory.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-300">**\_DIRECTORYSPECIFICATION CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-300">**CIM\_DirectorySpecification**</span></span>](cim-directoryspecification.md)
</dt> <dd>

<span data-ttu-id="fde4c-301">La clase [**CIM \_ DirectorySpecification**](cim-directoryspecification.md) captura la estructura de directorios principal de un elemento de software.</span><span class="sxs-lookup"><span data-stu-id="fde4c-301">The [**CIM\_DirectorySpecification**](cim-directoryspecification.md) class captures the major directory structure of a software element.</span></span> <span data-ttu-id="fde4c-302">Esta clase se usa para organizar los archivos de un elemento de software en unidades administrables que se pueden reubicar en un sistema informático.</span><span class="sxs-lookup"><span data-stu-id="fde4c-302">This class is used to organize the files of a software element into manageable units that can be relocated on a computer system.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-303">**\_DIRECTORYSPECIFICATIONFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-303">**CIM\_DirectorySpecificationFile**</span></span>](cim-directoryspecificationfile.md)
</dt> <dd>

<span data-ttu-id="fde4c-304">La [**Asociación \_ DirectorySpecificationFile de CIM**](cim-directoryspecificationfile.md) representa el directorio que contiene el archivo especificado al hacer referencia a la clase [**\_ DirectorySpecification de CIM**](cim-directoryspecification.md) .</span><span class="sxs-lookup"><span data-stu-id="fde4c-304">The [**CIM\_DirectorySpecificationFile**](cim-directoryspecificationfile.md) association represents the directory that contains the file specified by referencing the [**CIM\_DirectorySpecification**](cim-directoryspecification.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-305">**\_DISCRETESENSOR CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-305">**CIM\_DiscreteSensor**</span></span>](cim-discretesensor.md)
</dt> <dd>

<span data-ttu-id="fde4c-306">La clase [**CIM \_ DiscreteSensor**](cim-discretesensor.md) tiene un conjunto de valores de cadena válidos que puede notificar.</span><span class="sxs-lookup"><span data-stu-id="fde4c-306">The [**CIM\_DiscreteSensor**](cim-discretesensor.md) class has a set of legal string values that it can report.</span></span> <span data-ttu-id="fde4c-307">Los valores se enumeran en la propiedad **PossibleValues** del sensor.</span><span class="sxs-lookup"><span data-stu-id="fde4c-307">The values are enumerated in the sensor's **PossibleValues** property.</span></span> <span data-ttu-id="fde4c-308">Un sensor discreto siempre tiene una lectura actual que corresponde a uno de los valores enumerados.</span><span class="sxs-lookup"><span data-stu-id="fde4c-308">A discrete sensor always has a current reading that corresponds to one of the enumerated values.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-309">**\_DISKDRIVE CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-309">**CIM\_DiskDrive**</span></span>](cim-diskdrive.md)
</dt> <dd>

<span data-ttu-id="fde4c-310">La clase [**CIM \_ DiskDrive**](cim-diskdrive.md) representa una unidad de disco física tal como la muestra el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="fde4c-310">The [**CIM\_DiskDrive**](cim-diskdrive.md) class represents a physical disk drive as seen by the operating system.</span></span> <span data-ttu-id="fde4c-311">Las características de la unidad de disco se corresponden con las características lógicas y de administración de la unidad, y en algunos casos, es posible que no reflejen las características físicas del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fde4c-311">The disk drive features correspond to the logical and management characteristics of the drive, and in some cases, may not reflect the physical characteristics of the device.</span></span> <span data-ttu-id="fde4c-312">Una interfaz a una unidad física es miembro de esta clase.</span><span class="sxs-lookup"><span data-stu-id="fde4c-312">An interface to a physical drive is a member of this class.</span></span> <span data-ttu-id="fde4c-313">Sin embargo, un objeto basado en otro dispositivo lógico no es miembro de esta clase.</span><span class="sxs-lookup"><span data-stu-id="fde4c-313">However, an object based on another logical device is not a member of this class.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-314">**\_DISKETTEDRIVE CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-314">**CIM\_DisketteDrive**</span></span>](cim-diskettedrive.md)
</dt> <dd>

<span data-ttu-id="fde4c-315">La clase [**CIM \_ DisketteDrive**](cim-diskettedrive.md) representa las capacidades y la administración de una unidad de disquete.</span><span class="sxs-lookup"><span data-stu-id="fde4c-315">The [**CIM\_DisketteDrive**](cim-diskettedrive.md) class represents the capabilities and management of a diskette drive.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-316">**\_DISKPARTITION CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-316">**CIM\_DiskPartition**</span></span>](cim-diskpartition.md)
</dt> <dd>

<span data-ttu-id="fde4c-317">La clase [**CIM \_ DiskPartition**](cim-diskpartition.md) representa un intervalo contiguo de bloques lógicos que el sistema operativo identifica mediante el tipo de la partición y los campos de subtipo.</span><span class="sxs-lookup"><span data-stu-id="fde4c-317">The [**CIM\_DiskPartition**](cim-diskpartition.md) class represents a contiguous range of logical blocks that is identifiable by the operating system by way of the partition's type and subtype fields.</span></span> <span data-ttu-id="fde4c-318">Las particiones de disco deben realizarse directamente mediante medios físicos (indicados por la Asociación [**\_ RealizesDiskPartition de CIM**](cim-realizesdiskpartition.md) ) o basados en volúmenes de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="fde4c-318">Disk partitions should be directly realized by physical media (indicated by the [**CIM\_RealizesDiskPartition**](cim-realizesdiskpartition.md) association) or built on storage volumes.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-319">**\_DISKSPACECHECK CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-319">**CIM\_DiskSpaceCheck**</span></span>](cim-diskspacecheck.md)
</dt> <dd>

<span data-ttu-id="fde4c-320">La [**clase \_ DiskSpaceCheck de CIM**](cim-diskspacecheck.md) comprueba la cantidad de espacio en disco disponible del sistema y lo especifica en la propiedad **AvailableDiskSpace** .</span><span class="sxs-lookup"><span data-stu-id="fde4c-320">The [**CIM\_DiskSpaceCheck**](cim-diskspacecheck.md) class checks the system's amount of available disk space and specifies it in the **AvailableDiskSpace** property.</span></span> <span data-ttu-id="fde4c-321">Los detalles se comparan con el valor de la propiedad **AvailableSpace** del objeto de sistema de [**\_ archivos CIM**](cim-filesystem.md) que está asociado al objeto [**\_ ComputerSystem de CIM**](cim-computersystem.md) , que describe el entorno del sistema.</span><span class="sxs-lookup"><span data-stu-id="fde4c-321">Details are compared with the value in the **AvailableSpace** property of the [**CIM\_FileSystem**](cim-filesystem.md) object that is associated with the [**CIM\_ComputerSystem**](cim-computersystem.md) object, which describes the system environment.</span></span> <span data-ttu-id="fde4c-322">Cuando el valor de la propiedad **AvailableSpace** es mayor o igual que el valor especificado en la propiedad **AvailableDiskSpace** , se cumple la condición.</span><span class="sxs-lookup"><span data-stu-id="fde4c-322">When the value of the **AvailableSpace** property is greater than or equal to the value specified in the **AvailableDiskSpace** property, the condition is satisfied.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-323">**Presentación de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="fde4c-323">**CIM\_Display**</span></span>](cim-display.md)
</dt> <dd>

<span data-ttu-id="fde4c-324">La clase de [**\_ presentación CIM**](cim-display.md) es una clase primaria para agrupar dispositivos de pantalla varios.</span><span class="sxs-lookup"><span data-stu-id="fde4c-324">The [**CIM\_Display**](cim-display.md) class is a parent class for grouping miscellaneous display devices.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-325">**DMA de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="fde4c-325">**CIM\_DMA**</span></span>](cim-dma.md)
</dt> <dd>

<span data-ttu-id="fde4c-326">La clase de [**\_ DMA de CIM**](cim-dma.md) representa el acceso directo a memoria (DMA) de la arquitectura del equipo.</span><span class="sxs-lookup"><span data-stu-id="fde4c-326">The [**CIM\_DMA**](cim-dma.md) class represents computer architecture direct memory access (DMA).</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-327">**CIM \_ acoplado**</span><span class="sxs-lookup"><span data-stu-id="fde4c-327">**CIM\_Docked**</span></span>](cim-docked.md)
</dt> <dd>

<span data-ttu-id="fde4c-328">La [**Asociación \_ acoplada CIM**](cim-docked.md) representa la relación entre dos chasis.</span><span class="sxs-lookup"><span data-stu-id="fde4c-328">The [**CIM\_Docked**](cim-docked.md) association represents the relationship between two chassis.</span></span> <span data-ttu-id="fde4c-329">Por ejemplo, un portátil (un tipo de chasis) se puede acoplar en una estación de acoplamiento (otro tipo de chasis).</span><span class="sxs-lookup"><span data-stu-id="fde4c-329">For example, a laptop (a type of chassis) can be docked in a docking station (another type of chassis).</span></span> <span data-ttu-id="fde4c-330">Esta relación típica se describe explícitamente.</span><span class="sxs-lookup"><span data-stu-id="fde4c-330">This typical relationship is explicitly described.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-331">**\_ELEMENTCAPACITY CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-331">**CIM\_ElementCapacity**</span></span>](cim-elementcapacity.md)
</dt> <dd>

<span data-ttu-id="fde4c-332">La [**clase \_ ElementCapacity de CIM**](cim-elementcapacity.md) asocia un objeto [**\_ PhysicalCapacity de CIM**](cim-physicalcapacity.md) con uno o más elementos físicos.</span><span class="sxs-lookup"><span data-stu-id="fde4c-332">The [**CIM\_ElementCapacity**](cim-elementcapacity.md) class associates a [**CIM\_PhysicalCapacity**](cim-physicalcapacity.md) object with one or more physical elements.</span></span> <span data-ttu-id="fde4c-333">Asocia una descripción de los requisitos de hardware mínimos y máximos (o las capacidades) a los elementos físicos que se describen.</span><span class="sxs-lookup"><span data-stu-id="fde4c-333">It associates a description of the minimum and maximum hardware requirements (or capabilities) to the physical elements being described.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-334">**\_ELEMENTCONFIGURATION CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-334">**CIM\_ElementConfiguration**</span></span>](cim-elementconfiguration.md)
</dt> <dd>

<span data-ttu-id="fde4c-335">La [**Asociación \_ ElementConfiguration de CIM**](cim-elementconfiguration.md) relaciona un objeto de [**\_ configuración de CIM**](cim-configuration.md) con uno o más elementos del sistema administrados.</span><span class="sxs-lookup"><span data-stu-id="fde4c-335">The [**CIM\_ElementConfiguration**](cim-elementconfiguration.md) association relates a [**CIM\_Configuration**](cim-configuration.md) object to one or more managed system elements.</span></span> <span data-ttu-id="fde4c-336">El objeto de **\_ configuración de CIM** representa un comportamiento determinado o un estado funcional deseado para el [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md)asociado.</span><span class="sxs-lookup"><span data-stu-id="fde4c-336">The **CIM\_Configuration** object represents a certain behavior, or a desired functional state for the associated [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-337">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-337">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dd>

<span data-ttu-id="fde4c-338">La clase [**CIM \_ ElementSetting**](cim-elementsetting.md) representa la asociación entre los elementos del sistema administrados y la clase de configuración definida para ellos.</span><span class="sxs-lookup"><span data-stu-id="fde4c-338">The [**CIM\_ElementSetting**](cim-elementsetting.md) class represents the association between managed system elements and the setting class defined for them.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-339">**\_ELEMENTSLINKED CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-339">**CIM\_ElementsLinked**</span></span>](cim-elementslinked.md)
</dt> <dd>

<span data-ttu-id="fde4c-340">La [**Asociación \_ ElementsLinked de CIM**](cim-elementslinked.md) representa los elementos físicos que están cableados juntos por un vínculo físico.</span><span class="sxs-lookup"><span data-stu-id="fde4c-340">The [**CIM\_ElementsLinked**](cim-elementslinked.md) association represents physical elements that are cabled together by a physical link.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-341">**\_ERRORCOUNTERSFORDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-341">**CIM\_ErrorCountersForDevice**</span></span>](cim-errorcountersfordevice.md)
</dt> <dd>

<span data-ttu-id="fde4c-342">La clase [**CIM \_ ErrorCountersForDevice**](cim-errorcountersfordevice.md) asocia la clase [**\_ DeviceErrorCounts de CIM**](cim-deviceerrorcounts.md) al dispositivo lógico al que se aplica.</span><span class="sxs-lookup"><span data-stu-id="fde4c-342">The [**CIM\_ErrorCountersForDevice**](cim-errorcountersfordevice.md) class associates the [**CIM\_DeviceErrorCounts**](cim-deviceerrorcounts.md) class to the logical device to which it applies.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-343">**\_EXECUTEPROGRAM CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-343">**CIM\_ExecuteProgram**</span></span>](cim-executeprogram.md)
</dt> <dd>

<span data-ttu-id="fde4c-344">La clase [**CIM \_ ExecuteProgram**](cim-executeprogram.md) representa los archivos que se pueden ejecutar en el sistema donde está instalado el elemento de software.</span><span class="sxs-lookup"><span data-stu-id="fde4c-344">The [**CIM\_ExecuteProgram**](cim-executeprogram.md) class represents files that can be executed on the system where the software element is installed.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-345">**Exportación de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="fde4c-345">**CIM\_Export**</span></span>](cim-export.md)
</dt> <dd>

<span data-ttu-id="fde4c-346">La clase de [**\_ exportación CIM**](cim-export.md) representa una asociación entre un sistema de archivos local y sus directorios, que indican que los directorios especificados están disponibles para su montaje.</span><span class="sxs-lookup"><span data-stu-id="fde4c-346">The [**CIM\_Export**](cim-export.md) class represents an association between a local file system and its directories, which indicate that the specified directories are available for mount.</span></span> <span data-ttu-id="fde4c-347">Al exportar un sistema de archivos completo, el directorio debe hacer referencia al directorio superior del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="fde4c-347">When exporting an entire file system, the directory should reference the topmost directory of the file system.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-348">**\_EXTRACAPACITYGROUP CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-348">**CIM\_ExtraCapacityGroup**</span></span>](cim-extracapacitygroup.md)
</dt> <dd>

<span data-ttu-id="fde4c-349">La clase [**CIM \_ ExtraCapacityGroup**](cim-extracapacitygroup.md) se deriva de un grupo de redundancia que indica que los elementos agregados tienen más capacidad o capacidad de la necesaria.</span><span class="sxs-lookup"><span data-stu-id="fde4c-349">The [**CIM\_ExtraCapacityGroup**](cim-extracapacitygroup.md) class is derived from a redundancy group that indicates the aggregated elements have more capacity or capability than is needed.</span></span> <span data-ttu-id="fde4c-350">Un ejemplo de este tipo de redundancia es la instalación de fuentes de alimentación N + 1 o ventiladores en un sistema.</span><span class="sxs-lookup"><span data-stu-id="fde4c-350">An example of this type of redundancy is the installation of N+1 power supplies or fans in a system.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-351">**\_Ventilador CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-351">**CIM\_Fan**</span></span>](cim-fan.md)
</dt> <dd>

<span data-ttu-id="fde4c-352">La clase del [**\_ ventilador CIM**](cim-fan.md) representa las capacidades y la administración de un dispositivo de refrigeración de ventilador.</span><span class="sxs-lookup"><span data-stu-id="fde4c-352">The [**CIM\_Fan**](cim-fan.md) class represents the capabilities and management of a fan cooling device.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-353">**\_FILEACTION CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-353">**CIM\_FileAction**</span></span>](cim-fileaction.md)
</dt> <dd>

<span data-ttu-id="fde4c-354">La clase [**CIM \_ FileAction**](cim-fileaction.md) permite al autor ubicar los archivos que ya existen en el equipo de un usuario y, a continuación, trasladarlos o copiarlos a una nueva ubicación.</span><span class="sxs-lookup"><span data-stu-id="fde4c-354">The [**CIM\_FileAction**](cim-fileaction.md) class allows the author to locate files that already exist on a user's computer, and then move or copy those files to a new location.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-355">**\_FILESPECIFICATION CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-355">**CIM\_FileSpecification**</span></span>](cim-filespecification.md)
</dt> <dd>

<span data-ttu-id="fde4c-356">La clase [**CIM \_ FileSpecification**](cim-filespecification.md) representa un archivo que está activado o desactivado en el sistema.</span><span class="sxs-lookup"><span data-stu-id="fde4c-356">The [**CIM\_FileSpecification**](cim-filespecification.md) class represents a file that is either on or off of the system.</span></span> <span data-ttu-id="fde4c-357">El archivo se encuentra en el directorio identificado por la [**Asociación \_ DirectorySpecificationFile de CIM**](cim-directoryspecificationfile.md) .</span><span class="sxs-lookup"><span data-stu-id="fde4c-357">The file is located in the directory identified by the [**CIM\_DirectorySpecificationFile**](cim-directoryspecificationfile.md) association.</span></span> <span data-ttu-id="fde4c-358">El método [**Invoke**](invoke-method-in-class-cim-filespecification.md) usa la información para comprobar la existencia del archivo.</span><span class="sxs-lookup"><span data-stu-id="fde4c-358">The [**Invoke**](invoke-method-in-class-cim-filespecification.md) method uses the information to check for the file's existence.</span></span> <span data-ttu-id="fde4c-359">Tenga en cuenta que las propiedades con un valor **null** no se comprueban.</span><span class="sxs-lookup"><span data-stu-id="fde4c-359">Note that properties with a **Null** value are not checked.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-360">**\_FILESTORAGE CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-360">**CIM\_FileStorage**</span></span>](cim-filestorage.md)
</dt> <dd>

<span data-ttu-id="fde4c-361">La [**Asociación \_ FileStorage de CIM**](cim-filestorage.md) vincula el sistema de archivos y los archivos lógicos que se dirigen a través del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="fde4c-361">The [**CIM\_FileStorage**](cim-filestorage.md) association links the file system and the logical files addressed through the file system.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-362">**\_Sistema de archivos CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-362">**CIM\_FileSystem**</span></span>](cim-filesystem.md)
</dt> <dd>

<span data-ttu-id="fde4c-363">La clase de sistema de archivos [**CIM \_**](cim-filesystem.md) representa un archivo o un conjunto de datos local de un equipo o montado de forma remota desde un servidor de archivos.</span><span class="sxs-lookup"><span data-stu-id="fde4c-363">The [**CIM\_FileSystem**](cim-filesystem.md) class represents a file or data set local to a computer system or remotely mounted from a file server.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-364">**\_FLATPANEL CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-364">**CIM\_FlatPanel**</span></span>](cim-flatpanel.md)
</dt> <dd>

<span data-ttu-id="fde4c-365">La clase [**CIM \_ FlatPanel**](cim-flatpanel.md) representa las capacidades y la administración del dispositivo lógico de panel plano.</span><span class="sxs-lookup"><span data-stu-id="fde4c-365">The [**CIM\_FlatPanel**](cim-flatpanel.md) class represents the capabilities and management of the flat panel logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-366">**\_FROMDIRECTORYACTION CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-366">**CIM\_FromDirectoryAction**</span></span>](cim-fromdirectoryaction.md)
</dt> <dd>

<span data-ttu-id="fde4c-367">La [**Asociación \_ FromDirectoryAction de CIM**](cim-fromdirectoryaction.md) identifica el directorio de origen para la acción de archivo.</span><span class="sxs-lookup"><span data-stu-id="fde4c-367">The [**CIM\_FromDirectoryAction**](cim-fromdirectoryaction.md) association identifies the source directory for the file action.</span></span> <span data-ttu-id="fde4c-368">Cuando se usa esta asociación, se supone que el directorio de origen fue creado por una acción anterior.</span><span class="sxs-lookup"><span data-stu-id="fde4c-368">When this association is used, the assumption is that the source directory was created by a previous action.</span></span> <span data-ttu-id="fde4c-369">Esta asociación no puede existir con una asociación [**\_ FromDirectorySpecification de CIM**](cim-fromdirectoryspecification.md) ; una acción de archivo solo puede incluir un único directorio de origen.</span><span class="sxs-lookup"><span data-stu-id="fde4c-369">This association cannot exist with a [**CIM\_FromDirectorySpecification**](cim-fromdirectoryspecification.md) association; a file action can only involve a single source directory.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-370">**\_FROMDIRECTORYSPECIFICATION CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-370">**CIM\_FromDirectorySpecification**</span></span>](cim-fromdirectoryspecification.md)
</dt> <dd>

<span data-ttu-id="fde4c-371">La [**Asociación \_ FromDirectorySpecification de CIM**](cim-fromdirectoryspecification.md) identifica el directorio de origen para la acción de archivo.</span><span class="sxs-lookup"><span data-stu-id="fde4c-371">The [**CIM\_FromDirectorySpecification**](cim-fromdirectoryspecification.md) association identifies the source directory for the file action.</span></span> <span data-ttu-id="fde4c-372">Cuando se usa esta asociación, se supone que el directorio de origen ya existe.</span><span class="sxs-lookup"><span data-stu-id="fde4c-372">When this association is used, the assumption is that the source directory already exists.</span></span> <span data-ttu-id="fde4c-373">Esta asociación no puede existir con una asociación [**\_ FromDirectoryAction de CIM**](cim-fromdirectoryaction.md) ; una acción de archivo solo puede incluir un único directorio de origen.</span><span class="sxs-lookup"><span data-stu-id="fde4c-373">This association cannot exist with a [**CIM\_FromDirectoryAction**](cim-fromdirectoryaction.md) association; a file action can only involve a single source directory.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-374">**FRU de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="fde4c-374">**CIM\_FRU**</span></span>](cim-fru.md)
</dt> <dd>

<span data-ttu-id="fde4c-375">La clase [**CIM \_ FRU**](cim-fru.md) representa una colección definida por el proveedor de productos y elementos físicos que están asociados a una unidad reemplazable en campo (FRU) para admitir, mantener o actualizar un producto en la ubicación del cliente.</span><span class="sxs-lookup"><span data-stu-id="fde4c-375">The [**CIM\_FRU**](cim-fru.md) class represents a vendor-defined collection of products and physical elements that are associated with a field replaceable unit (FRU) to support, maintain, or upgrade a product at the customer's location.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-376">**\_FRUINCLUDESPRODUCT CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-376">**CIM\_FRUIncludesProduct**</span></span>](cim-fruincludesproduct.md)
</dt> <dd>

<span data-ttu-id="fde4c-377">La clase [**CIM \_ FRUIncludesProduct**](cim-fruincludesproduct.md) indica que una unidad reemplazable en campo (FRU) puede estar formada por otros productos.</span><span class="sxs-lookup"><span data-stu-id="fde4c-377">The [**CIM\_FRUIncludesProduct**](cim-fruincludesproduct.md) class indicates that a field replaceable unit (FRU) may be composed of other products.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-378">**\_FRUPHYSICALELEMENTS CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-378">**CIM\_FRUPhysicalElements**</span></span>](cim-fruphysicalelements.md)
</dt> <dd>

<span data-ttu-id="fde4c-379">La clase [**CIM \_ FRUPhysicalElements**](cim-fruphysicalelements.md) representa los elementos físicos que componen una unidad reemplazable en campo (FRU).</span><span class="sxs-lookup"><span data-stu-id="fde4c-379">The [**CIM\_FRUPhysicalElements**](cim-fruphysicalelements.md) class represents the physical elements that make up a field replaceable unit (FRU).</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-380">**\_HEATPIPE CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-380">**CIM\_HeatPipe**</span></span>](cim-heatpipe.md)
</dt> <dd>

<span data-ttu-id="fde4c-381">La clase [**CIM \_ HeatPipe**](cim-heatpipe.md) representa las capacidades y la administración de un dispositivo de refrigeración de canalización térmica.</span><span class="sxs-lookup"><span data-stu-id="fde4c-381">The [**CIM\_HeatPipe**](cim-heatpipe.md) class represents the capabilities and management of a heat pipe cooling device.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-382">**\_HOSTEDACCESSPOINT CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-382">**CIM\_HostedAccessPoint**</span></span>](cim-hostedaccesspoint.md)
</dt> <dd>

<span data-ttu-id="fde4c-383">La clase [**CIM \_ HostedAccessPoint**](cim-hostedaccesspoint.md) representa una asociación entre un punto de acceso de servicio (SAP) y el sistema en el que se proporciona.</span><span class="sxs-lookup"><span data-stu-id="fde4c-383">The [**CIM\_HostedAccessPoint**](cim-hostedaccesspoint.md) class represents an association between a service access point (SAP) and the system on which it is provided.</span></span> <span data-ttu-id="fde4c-384">Cada sistema puede hospedar muchos SAP.</span><span class="sxs-lookup"><span data-stu-id="fde4c-384">Each system may host many SAPs.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-385">**\_HOSTEDBOOTSAP CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-385">**CIM\_HostedBootSAP**</span></span>](cim-hostedbootsap.md)
</dt> <dd>

<span data-ttu-id="fde4c-386">La clase [**CIM \_ HostedBootSAP**](cim-hostedbootsap.md) define el sistema de equipo unitario de hospedaje para una clase [**\_ BootSAP de CIM**](cim-bootsap.md) .</span><span class="sxs-lookup"><span data-stu-id="fde4c-386">The [**CIM\_HostedBootSAP**](cim-hostedbootsap.md) class defines the hosting unitary computer system for a [**CIM\_BootSAP**](cim-bootsap.md) class.</span></span> <span data-ttu-id="fde4c-387">Puesto que esta relación se subclase de [**\_ HostedAccessPoint de CIM**](cim-hostedaccesspoint.md), hereda el esquema de ámbito y de nomenclatura definido para [**\_ punto de CIM**](cim-serviceaccesspoint.md), donde un punto de acceso se pospone a su sistema de hospedaje.</span><span class="sxs-lookup"><span data-stu-id="fde4c-387">Since this relationship is subclassed from [**CIM\_HostedAccessPoint**](cim-hostedaccesspoint.md), it inherits the scoping/naming scheme defined for [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md), where an access point defers to its hosting system.</span></span> <span data-ttu-id="fde4c-388">En este caso, **\_ BootSAP CIM** debe diferir a su [**clase \_ UnitaryComputerSystem CIM**](cim-unitarycomputersystem.md) de hospedaje.</span><span class="sxs-lookup"><span data-stu-id="fde4c-388">In this case, **CIM\_BootSAP** must defer to its hosting [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-389">**\_HOSTEDBOOTSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-389">**CIM\_HostedBootService**</span></span>](cim-hostedbootservice.md)
</dt> <dd>

<span data-ttu-id="fde4c-390">La [**clase \_ HostedBootService de CIM**](cim-hostedbootservice.md) asocia un sistema de hospedaje y un servicio de arranque.</span><span class="sxs-lookup"><span data-stu-id="fde4c-390">The [**CIM\_HostedBootService**](cim-hostedbootservice.md) class associates a hosting system and a boot service.</span></span> <span data-ttu-id="fde4c-391">Puesto que esta relación se ha subclase de [**CIM \_ HostedService**](cim-hostedservice.md), hereda el esquema de ámbito y de nomenclatura definido para el servicio, donde un servicio se pospone a su sistema de hospedaje.</span><span class="sxs-lookup"><span data-stu-id="fde4c-391">Since this relationship is subclassed from [**CIM\_HostedService**](cim-hostedservice.md), it inherits the scoping/naming scheme defined for service, where a service defers to its hosting system.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-392">**\_HOSTEDFILESYSTEM CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-392">**CIM\_HostedFileSystem**</span></span>](cim-hostedfilesystem.md)
</dt> <dd>

<span data-ttu-id="fde4c-393">La [**Asociación \_ HostedFileSystem de CIM**](cim-hostedfilesystem.md) representa un vínculo entre el equipo y el sistema de archivos hospedado en el sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="fde4c-393">The [**CIM\_HostedFileSystem**](cim-hostedfilesystem.md) association represents a link between the computer system and the file system hosted on the computer system.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-394">**\_HOSTEDJOBDESTINATION CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-394">**CIM\_HostedJobDestination**</span></span>](cim-hostedjobdestination.md)
</dt> <dd>

<span data-ttu-id="fde4c-395">La clase [**CIM \_ HostedJobDestination**](cim-hostedjobdestination.md) representa una asociación entre un destino de trabajo y el sistema en el que reside.</span><span class="sxs-lookup"><span data-stu-id="fde4c-395">The [**CIM\_HostedJobDestination**](cim-hostedjobdestination.md) class represents an association between a job destination and the system on which it resides.</span></span> <span data-ttu-id="fde4c-396">Un sistema puede hospedar muchas colas de trabajos.</span><span class="sxs-lookup"><span data-stu-id="fde4c-396">A system may host many job queues.</span></span> <span data-ttu-id="fde4c-397">Los destinos del trabajo se aplazan al sistema de hospedaje.</span><span class="sxs-lookup"><span data-stu-id="fde4c-397">Job destinations defer to the hosting system.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-398">**HostedService de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="fde4c-398">**CIM\_HostedService**</span></span>](cim-hostedservice.md)
</dt> <dd>

<span data-ttu-id="fde4c-399">La clase [**CIM \_ HostedService**](cim-hostedservice.md) representa una asociación entre un servicio y el sistema en el que reside la funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="fde4c-399">The [**CIM\_HostedService**](cim-hostedservice.md) class represents an association between a service and the system on which the functionality resides.</span></span> <span data-ttu-id="fde4c-400">Un sistema puede hospedar muchos servicios, que aplazan el sistema de hospedaje.</span><span class="sxs-lookup"><span data-stu-id="fde4c-400">A system may host many services, which defer to the hosting system.</span></span> <span data-ttu-id="fde4c-401">El modelo no representa servicios hospedados en varios sistemas.</span><span class="sxs-lookup"><span data-stu-id="fde4c-401">The model does not represent services hosted across multiple systems.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-402">**\_INFRAREDCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-402">**CIM\_InfraredController**</span></span>](cim-infraredcontroller.md)
</dt> <dd>

<span data-ttu-id="fde4c-403">La clase [**CIM \_ InfraredController**](cim-infraredcontroller.md) representa las capacidades y la administración de un controlador de infrarrojos.</span><span class="sxs-lookup"><span data-stu-id="fde4c-403">The [**CIM\_InfraredController**](cim-infraredcontroller.md) class represents the capabilities and management of an infrared controller.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-404">**\_Instalado CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-404">**CIM\_InstalledOS**</span></span>](cim-installedos.md)
</dt> <dd>

<span data-ttu-id="fde4c-405">La clase de Asociación de [**CIM \_ instalados**](cim-installedos.md) representa un vínculo entre el equipo y el sistema operativo instalado.</span><span class="sxs-lookup"><span data-stu-id="fde4c-405">The [**CIM\_InstalledOS**](cim-installedos.md) association class represents a link between the computer system and the installed operating system.</span></span> <span data-ttu-id="fde4c-406">Un sistema operativo se instala cuando está en la extensión de almacenamiento de un sistema (por ejemplo, se copia en una unidad de disco o se descarga en memoria).</span><span class="sxs-lookup"><span data-stu-id="fde4c-406">An operating system is installed when it is in a computer system's storage extent (for example, copied to a disk drive or downloaded to memory).</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-407">**\_INSTALLEDSOFTWAREELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-407">**CIM\_InstalledSoftwareElement**</span></span>](cim-installedsoftwareelement.md)
</dt> <dd>

<span data-ttu-id="fde4c-408">La [**clase \_ InstalledSoftwareElement de CIM**](cim-installedsoftwareelement.md) asocia un equipo con un elemento de software instalado.</span><span class="sxs-lookup"><span data-stu-id="fde4c-408">The [**CIM\_InstalledSoftwareElement**](cim-installedsoftwareelement.md) class associates a computer system with an installed software element.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-409">**\_IRQ CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-409">**CIM\_IRQ**</span></span>](cim-irq.md)
</dt> <dd>

<span data-ttu-id="fde4c-410">La clase de [**\_ IRQ CIM**](cim-irq.md) representa una línea de solicitud de interrupción (IRQ) de arquitectura Intel.</span><span class="sxs-lookup"><span data-stu-id="fde4c-410">The [**CIM\_IRQ**](cim-irq.md) class represents an Intel architecture interrupt request line (IRQ).</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-411">**Trabajo de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="fde4c-411">**CIM\_Job**</span></span>](cim-job.md)
</dt> <dd>

<span data-ttu-id="fde4c-412">La clase de [**\_ trabajo CIM**](cim-job.md) representa una unidad de trabajo para un sistema, como un trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="fde4c-412">The [**CIM\_Job**](cim-job.md) class represents a unit of work for a system, such as a print job.</span></span> <span data-ttu-id="fde4c-413">Un trabajo es distinto de un proceso porque se puede programar un trabajo.</span><span class="sxs-lookup"><span data-stu-id="fde4c-413">A job is distinct from a process because a job can be scheduled.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-414">**\_JOBDESTINATION CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-414">**CIM\_JobDestination**</span></span>](cim-jobdestination.md)
</dt> <dd>

<span data-ttu-id="fde4c-415">La clase [**CIM \_ JobDestination**](cim-jobdestination.md) representa dónde se envía un trabajo para su procesamiento.</span><span class="sxs-lookup"><span data-stu-id="fde4c-415">The [**CIM\_JobDestination**](cim-jobdestination.md) class represents where a job is submitted for processing.</span></span> <span data-ttu-id="fde4c-416">Puede hacer referencia a una cola que contiene cero o más trabajos, como una cola de impresión que contiene los trabajos de impresión.</span><span class="sxs-lookup"><span data-stu-id="fde4c-416">It can refer to a queue that contains zero or more jobs, such as a print queue containing print jobs.</span></span> <span data-ttu-id="fde4c-417">Los destinos del trabajo se hospedan en sistemas, de forma similar a la manera en que los servicios se hospedan en los sistemas.</span><span class="sxs-lookup"><span data-stu-id="fde4c-417">Job destinations are hosted on systems, similar to the way in which services are hosted on systems.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-418">**\_JOBDESTINATIONJOBS CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-418">**CIM\_JobDestinationJobs**</span></span>](cim-jobdestinationjobs.md)
</dt> <dd>

<span data-ttu-id="fde4c-419">La [**Asociación \_ JobDestinationJobs de CIM**](cim-jobdestinationjobs.md) describe dónde se envía un trabajo para su procesamiento (es decir, a qué destino del trabajo).</span><span class="sxs-lookup"><span data-stu-id="fde4c-419">The [**CIM\_JobDestinationJobs**](cim-jobdestinationjobs.md) association describes where a job is submitted for processing (that is, to which job destination).</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-420">**\_Teclado CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-420">**CIM\_Keyboard**</span></span>](cim-keyboard.md)
</dt> <dd>

<span data-ttu-id="fde4c-421">La clase de [**\_ teclado CIM**](cim-keyboard.md) representa las capacidades y la administración del dispositivo lógico del teclado.</span><span class="sxs-lookup"><span data-stu-id="fde4c-421">The [**CIM\_Keyboard**](cim-keyboard.md) class represents the capabilities and management of the keyboard logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-422">**\_LINKHASCONNECTOR CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-422">**CIM\_LinkHasConnector**</span></span>](cim-linkhasconnector.md)
</dt> <dd>

<span data-ttu-id="fde4c-423">La [**clase \_ LinkHasConnector de CIM**](cim-linkhasconnector.md) asocia los cables y los vínculos usados como conectores físicos, que conectan los elementos físicos.</span><span class="sxs-lookup"><span data-stu-id="fde4c-423">The [**CIM\_LinkHasConnector**](cim-linkhasconnector.md) class associates cables and links used as physical connectors, which connect the physical elements.</span></span> <span data-ttu-id="fde4c-424">Esta asociación define explícitamente la relación de los conectores para [**\_ PhysicalLink CIM**](cim-physicallink.md).</span><span class="sxs-lookup"><span data-stu-id="fde4c-424">This association explicitly defines the relationship of connectors for [**CIM\_PhysicalLink**](cim-physicallink.md).</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-425">**\_LOCALFILESYSTEM CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-425">**CIM\_LocalFileSystem**</span></span>](cim-localfilesystem.md)
</dt> <dd>

<span data-ttu-id="fde4c-426">La clase [**CIM \_ LocalFileSystem**](cim-localfilesystem.md) representa el almacén de archivos controlado por un sistema informático a través de medios locales (por ejemplo, acceso directo al controlador de dispositivo).</span><span class="sxs-lookup"><span data-stu-id="fde4c-426">The [**CIM\_LocalFileSystem**](cim-localfilesystem.md) class represents the file store controlled by a computer system through local means (for example, direct device-driver access).</span></span> <span data-ttu-id="fde4c-427">El almacén de archivos se puede administrar directamente mediante el sistema del equipo, sin necesidad de que otro equipo actúe como servidor de archivos.</span><span class="sxs-lookup"><span data-stu-id="fde4c-427">The file store can be managed directly by the computer system, without the need for another computer to act as a file server.</span></span> <span data-ttu-id="fde4c-428">Sin embargo, para un sistema de archivos en clúster, el sistema de archivos es local y, por lo tanto, se pospone al clúster.</span><span class="sxs-lookup"><span data-stu-id="fde4c-428">For a clustered file system, however, the file system is local and, therefore, defers to the cluster.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-429">**Ubicación de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="fde4c-429">**CIM\_Location**</span></span>](cim-location.md)
</dt> <dd>

<span data-ttu-id="fde4c-430">La clase de [**\_ Ubicación CIM**](cim-location.md) representa la posición y la dirección de un elemento físico.</span><span class="sxs-lookup"><span data-stu-id="fde4c-430">The [**CIM\_Location**](cim-location.md) class represents the position and address of a physical element.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-431">**LogicalDevice de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="fde4c-431">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dd>

<span data-ttu-id="fde4c-432">La clase de [**\_ LogicalDevice de CIM**](cim-logicaldevice.md) representa una entidad de hardware que puede o no ser realizada en el hardware físico.</span><span class="sxs-lookup"><span data-stu-id="fde4c-432">The [**CIM\_LogicalDevice**](cim-logicaldevice.md) class represents a hardware entity that may or may not be realized in physical hardware.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-433">**LogicalDisk de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="fde4c-433">**CIM\_LogicalDisk**</span></span>](cim-logicaldisk.md)
</dt> <dd>

<span data-ttu-id="fde4c-434">La clase de [**\_ LogicalDisk de CIM**](cim-logicaldisk.md) representa un intervalo contiguo de bloques lógicos que un sistema de archivos identifica mediante el campo de **DeviceID** (clave) del disco.</span><span class="sxs-lookup"><span data-stu-id="fde4c-434">The [**CIM\_LogicalDisk**](cim-logicaldisk.md) class represents a contiguous range of logical blocks that is identifiable by a file system through the disk's **DeviceID** (key) field.</span></span> <span data-ttu-id="fde4c-435">Por ejemplo, en un entorno de Windows, el campo **DeviceID** contiene una letra de unidad; en un entorno de UNIX, contiene la ruta de acceso; y en un entorno de NetWare, contiene el nombre del volumen.</span><span class="sxs-lookup"><span data-stu-id="fde4c-435">For example, in a Windows environment, the **DeviceID** field contains a drive letter; in a UNIX environment, it contains the access path; and in a NetWare environment, it contains the volume name.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-436">**\_LOGICALDISKBASEDONPARTITION CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-436">**CIM\_LogicalDiskBasedOnPartition**</span></span>](cim-logicaldiskbasedonpartition.md)
</dt> <dd>

<span data-ttu-id="fde4c-437">La [**clase \_ LogicalDiskBasedOnPartition de CIM**](cim-logicaldiskbasedonpartition.md) asocia un disco lógico a la partición de disco en la que reside.</span><span class="sxs-lookup"><span data-stu-id="fde4c-437">The [**CIM\_LogicalDiskBasedOnPartition**](cim-logicaldiskbasedonpartition.md) class associates a logical disk with the disk partition on which it resides.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-438">**\_LOGICALDISKBASEDONVOLUMESET CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-438">**CIM\_LogicalDiskBasedOnVolumeSet**</span></span>](cim-logicaldiskbasedonvolumeset.md)
</dt> <dd>

<span data-ttu-id="fde4c-439">La [**Asociación \_ LogicalDiskBasedOnVolumeSet de CIM**](cim-logicaldiskbasedonvolumeset.md) relaciona los discos lógicos con el volumen en el que se encuentran.</span><span class="sxs-lookup"><span data-stu-id="fde4c-439">The [**CIM\_LogicalDiskBasedOnVolumeSet**](cim-logicaldiskbasedonvolumeset.md) association relates logical disks with the volume on which they are found.</span></span> <span data-ttu-id="fde4c-440">Los discos lógicos pueden basarse en un único volumen (por ejemplo, expuesto por un administrador de volumen de software) o una partición de disco.</span><span class="sxs-lookup"><span data-stu-id="fde4c-440">Logical disks can be based on a single volume (for example, exposed by a software volume manager) or a disk partition.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-441">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-441">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dd>

<span data-ttu-id="fde4c-442">La clase [**CIM \_ LogicalElement**](cim-logicalelement.md) es la clase base para todos los componentes del sistema que representan componentes del sistema abstractos, como perfiles, procesos o capacidades del sistema, en forma de dispositivos lógicos.</span><span class="sxs-lookup"><span data-stu-id="fde4c-442">The [**CIM\_LogicalElement**](cim-logicalelement.md) class is the base class for all system components that represent abstract system components, such as profiles, processes, or system capabilities, in the form of logical devices.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-443">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-443">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> <dd>

<span data-ttu-id="fde4c-444">La clase [**CIM \_ LogicalFile**](cim-logicalfile.md) representa una colección con nombre de datos, que puede ser código ejecutable, que se encuentra en un sistema de archivos en una extensión de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="fde4c-444">The [**CIM\_LogicalFile**](cim-logicalfile.md) class represents a named collection of data, which can be executable code, that is located in a file system on a storage extent.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-445">**\_LOGICALIDENTITY CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-445">**CIM\_LogicalIdentity**</span></span>](cim-logicalidentity.md)
</dt> <dd>

<span data-ttu-id="fde4c-446">La clase [**CIM \_ LogicalIdentity**](cim-logicalidentity.md) es una asociación abstracta y genérica que indica que dos elementos lógicos representan distintos aspectos de la misma entidad subyacente.</span><span class="sxs-lookup"><span data-stu-id="fde4c-446">The [**CIM\_LogicalIdentity**](cim-logicalidentity.md) class is an abstract and generic association that indicates that two logical elements represent different aspects of the same underlying entity.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-447">**\_MAGNETOOPTICALDRIVE CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-447">**CIM\_MagnetoOpticalDrive**</span></span>](cim-magnetoopticaldrive.md)
</dt> <dd>

<span data-ttu-id="fde4c-448">La clase [**CIM \_ MagnetoOpticalDrive**](cim-magnetoopticaldrive.md) representa las capacidades y la administración de una unidad magneto-óptica, un subtipo del dispositivo de acceso a medios.</span><span class="sxs-lookup"><span data-stu-id="fde4c-448">The [**CIM\_MagnetoOpticalDrive**](cim-magnetoopticaldrive.md) class represents the capabilities and management of a magneto-optical drive, a subtype of the media access device.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-449">**ManagedSystemElement de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="fde4c-449">**CIM\_ManagedSystemElement**</span></span>](cim-managedsystemelement.md)
</dt> <dd>

<span data-ttu-id="fde4c-450">La clase del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md) es la clase base para la jerarquía de elementos del sistema.</span><span class="sxs-lookup"><span data-stu-id="fde4c-450">The [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) class is the base class for the system element hierarchy.</span></span> <span data-ttu-id="fde4c-451">Cualquier componente del sistema distinguible es un candidato para la inclusión en esta clase.</span><span class="sxs-lookup"><span data-stu-id="fde4c-451">Any distinguishable system component is a candidate for inclusion in this class.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-452">**\_MANAGEMENTCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-452">**CIM\_ManagementController**</span></span>](cim-managementcontroller.md)
</dt> <dd>

<span data-ttu-id="fde4c-453">La [**clase \_ ManagementController de CIM**](cim-managementcontroller.md) se relaciona con las capacidades y la administración de un controlador de administración.</span><span class="sxs-lookup"><span data-stu-id="fde4c-453">The [**CIM\_ManagementController**](cim-managementcontroller.md) class relates to the capabilities and management of a management controller.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-454">**\_MEDIAACCESSDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-454">**CIM\_MediaAccessDevice**</span></span>](cim-mediaaccessdevice.md)
</dt> <dd>

<span data-ttu-id="fde4c-455">La clase [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md) representa la capacidad de obtener acceso a uno o más medios y, a continuación, utilizar los medios para almacenar y recuperar datos.</span><span class="sxs-lookup"><span data-stu-id="fde4c-455">The [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md) class represents the ability to access one or more media, and then use the media to store and retrieve data.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-456">**\_MEDIAPRESENT CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-456">**CIM\_MediaPresent**</span></span>](cim-mediapresent.md)
</dt> <dd>

<span data-ttu-id="fde4c-457">La [**Asociación \_ MediaPresent de CIM**](cim-mediapresent.md) describe una relación en la que se debe tener acceso a una extensión de almacenamiento a través de un dispositivo de acceso a medios.</span><span class="sxs-lookup"><span data-stu-id="fde4c-457">The [**CIM\_MediaPresent**](cim-mediapresent.md) association describes a relationship where a storage extent must be accessed through a media access device.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-458">**Memoria de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="fde4c-458">**CIM\_Memory**</span></span>](cim-memory.md)
</dt> <dd>

<span data-ttu-id="fde4c-459">La clase de [**\_ memoria CIM**](cim-memory.md) representa las capacidades y la administración de los dispositivos lógicos relacionados con la memoria.</span><span class="sxs-lookup"><span data-stu-id="fde4c-459">The [**CIM\_Memory**](cim-memory.md) class represents the capabilities and management of memory-related logical devices.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-460">**\_MEMORYCAPACITY CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-460">**CIM\_MemoryCapacity**</span></span>](cim-memorycapacity.md)
</dt> <dd>

<span data-ttu-id="fde4c-461">La clase [**CIM \_ MemoryCapacity**](cim-memorycapacity.md) representa la memoria que se puede instalar en un elemento físico y sus configuraciones mínima y máxima.</span><span class="sxs-lookup"><span data-stu-id="fde4c-461">The [**CIM\_MemoryCapacity**](cim-memorycapacity.md) class represents memory that can be installed on a physical element and its minimum and maximum configurations.</span></span> <span data-ttu-id="fde4c-462">La información sobre la memoria que está instalada actualmente y los requisitos mínimos y máximos de un elemento se encuentra en las instancias de la clase [**\_ PhysicalMemory de CIM**](cim-physicalmemory.md) .</span><span class="sxs-lookup"><span data-stu-id="fde4c-462">Information on memory that is currently installed and an element's minimum and maximum requirements is located in instances of the [**CIM\_PhysicalMemory**](cim-physicalmemory.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-463">**\_MEMORYCHECK CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-463">**CIM\_MemoryCheck**</span></span>](cim-memorycheck.md)
</dt> <dd>

<span data-ttu-id="fde4c-464">La clase [**CIM \_ MemoryCheck**](cim-memorycheck.md) especifica una condición para la cantidad mínima de memoria que debe estar disponible en un sistema.</span><span class="sxs-lookup"><span data-stu-id="fde4c-464">The [**CIM\_MemoryCheck**](cim-memorycheck.md) class specifies a condition for the minimum amount of memory that must be available on a system.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-465">**\_MEMORYMAPPEDIO CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-465">**CIM\_MemoryMappedIO**</span></span>](cim-memorymappedio.md)
</dt> <dd>

<span data-ttu-id="fde4c-466">La clase [**CIM \_ MemoryMappedIO**](cim-memorymappedio.md) representa la arquitectura de equipo de e/s asignada a la memoria.</span><span class="sxs-lookup"><span data-stu-id="fde4c-466">The [**CIM\_MemoryMappedIO**](cim-memorymappedio.md) class represents computer architecture memory-mapped I/O.</span></span> <span data-ttu-id="fde4c-467">Esta clase trata los recursos de memoria y de e/s de puerto.</span><span class="sxs-lookup"><span data-stu-id="fde4c-467">This class addresses memory and port I/O resources.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-468">**\_MEMORYONCARD CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-468">**CIM\_MemoryOnCard**</span></span>](cim-memoryoncard.md)
</dt> <dd>

<span data-ttu-id="fde4c-469">La [**clase \_ MemoryOnCard de CIM**](cim-memoryoncard.md) asocia la memoria física que se encuentra en los paneles de hospedaje, las tarjetas de adaptador, etc.</span><span class="sxs-lookup"><span data-stu-id="fde4c-469">The [**CIM\_MemoryOnCard**](cim-memoryoncard.md) class associates physical memory located on hosting boards, adapter cards, and so on.</span></span> <span data-ttu-id="fde4c-470">Esta asociación define explícitamente la relación de memoria con las tarjetas.</span><span class="sxs-lookup"><span data-stu-id="fde4c-470">This association explicitly defines the relationship of memory to cards.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-471">**\_MEMORYWITHMEDIA CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-471">**CIM\_MemoryWithMedia**</span></span>](cim-memorywithmedia.md)
</dt> <dd>

<span data-ttu-id="fde4c-472">La [**clase \_ MemoryWithMedia de CIM**](cim-memorywithmedia.md) asocia la memoria física con un medio físico y su cartucho.</span><span class="sxs-lookup"><span data-stu-id="fde4c-472">The [**CIM\_MemoryWithMedia**](cim-memorywithmedia.md) class associates physical memory with a physical media and its cartridge.</span></span> <span data-ttu-id="fde4c-473">La memoria proporciona identificación de medios y almacena datos específicos del usuario.</span><span class="sxs-lookup"><span data-stu-id="fde4c-473">The memory provides media identification and stores user-specific data.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-474">**\_MODIFYSETTINGACTION CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-474">**CIM\_ModifySettingAction**</span></span>](cim-modifysettingaction.md)
</dt> <dd>

<span data-ttu-id="fde4c-475">La clase [**CIM \_ ModifySettingAction**](cim-modifysettingaction.md) representa la información para modificar un archivo de configuración concreto, para una entrada específica, con un valor específico.</span><span class="sxs-lookup"><span data-stu-id="fde4c-475">The [**CIM\_ModifySettingAction**](cim-modifysettingaction.md) class represents the information for modifying a specific setting file, for a specific entry, with a specific value.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-476">**\_MONITORRESOLUTION CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-476">**CIM\_MonitorResolution**</span></span>](cim-monitorresolution.md)
</dt> <dd>

<span data-ttu-id="fde4c-477">La clase [**CIM \_ MonitorResolution**](cim-monitorresolution.md) representa la relación entre las resoluciones horizontal y vertical, y la frecuencia de actualización y el modo de recorrido de un monitor de escritorio.</span><span class="sxs-lookup"><span data-stu-id="fde4c-477">The [**CIM\_MonitorResolution**](cim-monitorresolution.md) class represents the relationship between horizontal and vertical resolutions and the refresh rate and scan mode for a desktop monitor.</span></span> <span data-ttu-id="fde4c-478">Los valores se especifican en el objeto de controlador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="fde4c-478">Values are specified in the video controller object.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-479">**\_MONITORSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-479">**CIM\_MonitorSetting**</span></span>](cim-monitorsetting.md)
</dt> <dd>

<span data-ttu-id="fde4c-480">La [**clase \_ MonitorSetting de CIM**](cim-monitorsetting.md) asocia la resolución del monitor con el monitor de escritorio al que se aplica.</span><span class="sxs-lookup"><span data-stu-id="fde4c-480">The [**CIM\_MonitorSetting**](cim-monitorsetting.md) class associates the monitor resolution with the desktop monitor to which it applies.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-481">**Montaje de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="fde4c-481">**CIM\_Mount**</span></span>](cim-mount.md)
</dt> <dd>

<span data-ttu-id="fde4c-482">La clase de [**\_ montaje CIM**](cim-mount.md) representa una asociación entre un sistema de archivos y un directorio al que está asociado.</span><span class="sxs-lookup"><span data-stu-id="fde4c-482">The [**CIM\_Mount**](cim-mount.md) class represents an association between a file system and a directory to which it is attached.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-483">**\_MULTISTATESENSOR CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-483">**CIM\_MultiStateSensor**</span></span>](cim-multistatesensor.md)
</dt> <dd>

<span data-ttu-id="fde4c-484">La clase [**CIM \_ MultiStateSensor**](cim-multistatesensor.md) representa un conjunto de varios miembros de sensores binarios donde cada sensor binario informa de un resultado booleano.</span><span class="sxs-lookup"><span data-stu-id="fde4c-484">The [**CIM\_MultiStateSensor**](cim-multistatesensor.md) class represents a multi-member set of binary sensors where each binary sensor reports a Boolean result.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-485">**Adaptador de la CIM \_**</span><span class="sxs-lookup"><span data-stu-id="fde4c-485">**CIM\_NetworkAdapter**</span></span>](cim-networkadapter.md)
</dt> <dd>

<span data-ttu-id="fde4c-486">La [**clase \_ CIM**](cim-networkadapter.md) Networking es una clase abstracta que define los conceptos generales de hardware de red (por ejemplo, la dirección permanente o la velocidad de funcionamiento).</span><span class="sxs-lookup"><span data-stu-id="fde4c-486">The [**CIM\_NetworkAdapter**](cim-networkadapter.md) class is an abstract class that defines general networking hardware concepts (for example, permanent address or speed of operation).</span></span> <span data-ttu-id="fde4c-487">La información se transmite mediante la Asociación [**\_ DeviceSAPImplementation de CIM**](cim-devicesapimplementation.md) .</span><span class="sxs-lookup"><span data-stu-id="fde4c-487">The information is conveyed using the [**CIM\_DeviceSAPImplementation**](cim-devicesapimplementation.md) association.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-488">**NFS de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="fde4c-488">**CIM\_NFS**</span></span>](cim-nfs.md)
</dt> <dd>

<span data-ttu-id="fde4c-489">La clase de [**\_ NFS de CIM**](cim-nfs.md) representa un sistema de archivos remoto que se monta mediante el protocolo Network File System (NFS), desde un equipo.</span><span class="sxs-lookup"><span data-stu-id="fde4c-489">The [**CIM\_NFS**](cim-nfs.md) class represents a remote file system that is mounted, using the network file system (NFS) protocol, from a computer system.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-490">**\_NONVOLATILESTORAGE CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-490">**CIM\_NonVolatileStorage**</span></span>](cim-nonvolatilestorage.md)
</dt> <dd>

<span data-ttu-id="fde4c-491">La clase [**CIM \_ NonVolatileStorage**](cim-nonvolatilestorage.md) representa las capacidades y la administración de almacenamiento no volátil.</span><span class="sxs-lookup"><span data-stu-id="fde4c-491">The [**CIM\_NonVolatileStorage**](cim-nonvolatilestorage.md) class represents the capabilities and management of non-volatile storage.</span></span> <span data-ttu-id="fde4c-492">La memoria no volátil incluye de forma nativa el almacenamiento en Flash y ROM.</span><span class="sxs-lookup"><span data-stu-id="fde4c-492">Nonvolatile memory natively includes flash and ROM storage.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-493">**NumericSensor de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="fde4c-493">**CIM\_NumericSensor**</span></span>](cim-numericsensor.md)
</dt> <dd>

<span data-ttu-id="fde4c-494">La clase [**CIM \_ NumericSensor**](cim-numericsensor.md) representa un sensor numérico que devuelve lecturas numéricas y, opcionalmente, admite valores de umbral.</span><span class="sxs-lookup"><span data-stu-id="fde4c-494">The [**CIM\_NumericSensor**](cim-numericsensor.md) class represents a numeric sensor that returns numeric readings and optionally supports thresholds settings.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-495">**OperatingSystem de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="fde4c-495">**CIM\_OperatingSystem**</span></span>](cim-operatingsystem.md)
</dt> <dd>

<span data-ttu-id="fde4c-496">La clase [**CIM \_ OperatingSystem**](cim-operatingsystem.md) representa un sistema operativo del equipo, que se compone de software y firmware que hace que el hardware del equipo sea utilizable.</span><span class="sxs-lookup"><span data-stu-id="fde4c-496">The [**CIM\_OperatingSystem**](cim-operatingsystem.md) class represents a computer operating system, which is made up of software and firmware that make a computer system's hardware usable.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-497">**\_OPERATINGSYSTEMSOFTWAREFEATURE CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-497">**CIM\_OperatingSystemSoftwareFeature**</span></span>](cim-operatingsystemsoftwarefeature.md)
</dt> <dd>

<span data-ttu-id="fde4c-498">La clase [**CIM \_ OperatingSystemSoftwareFeature**](cim-operatingsystemsoftwarefeature.md) representa las características de software que componen el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="fde4c-498">The [**CIM\_OperatingSystemSoftwareFeature**](cim-operatingsystemsoftwarefeature.md) class represents the software features that make up the operating system.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-499">**\_OSPROCESS CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-499">**CIM\_OSProcess**</span></span>](cim-osprocess.md)
</dt> <dd>

<span data-ttu-id="fde4c-500">La [**clase \_ OSProcess de CIM**](cim-osprocess.md) asocia el sistema operativo y uno o más procesos que se ejecutan en el contexto del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="fde4c-500">The [**CIM\_OSProcess**](cim-osprocess.md) class associates the operating system and one or more processes running in the context of the operating system.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-501">**\_OSVERSIONCHECK CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-501">**CIM\_OSVersionCheck**</span></span>](cim-osversioncheck.md)
</dt> <dd>

<span data-ttu-id="fde4c-502">La clase [**CIM \_ OSVersionCheck**](cim-osversioncheck.md) especifica las versiones del sistema operativo que pueden admitir un elemento de software.</span><span class="sxs-lookup"><span data-stu-id="fde4c-502">The [**CIM\_OSVersionCheck**](cim-osversioncheck.md) class specifies the versions of the operating system that can support a software element.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-503">**\_PACKAGEALARM CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-503">**CIM\_PackageAlarm**</span></span>](cim-packagealarm.md)
</dt> <dd>

<span data-ttu-id="fde4c-504">La [**Asociación \_ PackageAlarm de CIM**](/windows/desktop/SecCrypto/extendedproperties-newenum) representa la relación en la que un dispositivo de alarma se instala como parte de un paquete.</span><span class="sxs-lookup"><span data-stu-id="fde4c-504">The [**CIM\_PackageAlarm**](/windows/desktop/SecCrypto/extendedproperties-newenum) association represents the relationship in which an alarm device is installed as part of a package.</span></span> <span data-ttu-id="fde4c-505">La instalación de indica problemas con el entorno del paquete, su estado de seguridad o su estado general.</span><span class="sxs-lookup"><span data-stu-id="fde4c-505">The installation indicates issues with the package's environment—its security state or its overall health.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-506">**\_PACKAGECOOLING CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-506">**CIM\_PackageCooling**</span></span>](cim-packagecooling.md)
</dt> <dd>

<span data-ttu-id="fde4c-507">La [**Asociación \_ PackageCooling de CIM**](cim-packagecooling.md) representa la relación en la que se instala un dispositivo de enfriamiento en un paquete, como un chasis o un bastidor, para ayudar con la refrigeración del paquete.</span><span class="sxs-lookup"><span data-stu-id="fde4c-507">The [**CIM\_PackageCooling**](cim-packagecooling.md) association represents the relationship in which a cooling device is installed in a package, such as a chassis or rack, to assist with the package's cooling.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-508">**\_PACKAGEDCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-508">**CIM\_PackagedComponent**</span></span>](cim-packagedcomponent.md)
</dt> <dd>

<span data-ttu-id="fde4c-509">La [**Asociación \_ PackagedComponent de CIM**](cim-packagedcomponent.md) representa una relación explícita en la que un componente normalmente está contenido en un paquete físico, como un chasis o una tarjeta.</span><span class="sxs-lookup"><span data-stu-id="fde4c-509">The [**CIM\_PackagedComponent**](cim-packagedcomponent.md) association represents an explicit relationship in which a component is typically contained by a physical package, such as a chassis or card.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-510">**\_PACKAGEINCHASSIS CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-510">**CIM\_PackageInChassis**</span></span>](cim-packageinchassis.md)
</dt> <dd>

<span data-ttu-id="fde4c-511">La [**Asociación \_ PackageInChassis de CIM**](cim-packageinchassis.md) representa la relación en la que un chasis puede contener otros paquetes, como otros chasis y tarjetas.</span><span class="sxs-lookup"><span data-stu-id="fde4c-511">The [**CIM\_PackageInChassis**](cim-packageinchassis.md) association represents the relationship in which a chassis can contain other packages, such as other chassis and cards.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-512">**\_PACKAGEINSLOT CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-512">**CIM\_PackageInSlot**</span></span>](cim-packageinslot.md)
</dt> <dd>

<span data-ttu-id="fde4c-513">La [**Asociación \_ PackageInSlot de CIM**](cim-packageinslot.md) representa la relación entre las tarjetas de dispositivo y el chasis en el que se montan.</span><span class="sxs-lookup"><span data-stu-id="fde4c-513">The [**CIM\_PackageInSlot**](cim-packageinslot.md) association represents the relationship between device cards and the chassis in which they are mounted.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-514">**\_PACKAGETEMPSENSOR CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-514">**CIM\_PackageTempSensor**</span></span>](cim-packagetempsensor.md)
</dt> <dd>

<span data-ttu-id="fde4c-515">La [**Asociación \_ PackageTempSensor de CIM**](cim-packagetempsensor.md) representa la relación en la que un sensor de temperatura se instala a menudo en un paquete, como un chasis o un bastidor, para supervisar el entorno del paquete.</span><span class="sxs-lookup"><span data-stu-id="fde4c-515">The [**CIM\_PackageTempSensor**](cim-packagetempsensor.md) association represents the relationship in which a temperature sensor is often installed in a package, such as a chassis or a rack, to monitor the package's environment.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-516">**\_PARALLELCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-516">**CIM\_ParallelController**</span></span>](cim-parallelcontroller.md)
</dt> <dd>

<span data-ttu-id="fde4c-517">La [**Asociación \_ ParallelController de CIM**](cim-parallelcontroller.md) se relaciona con las capacidades y la administración del dispositivo lógico de puerto paralelo.</span><span class="sxs-lookup"><span data-stu-id="fde4c-517">The [**CIM\_ParallelController**](cim-parallelcontroller.md) association relates to the capabilities and management of the parallel port logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-518">**\_PARTICIPATESINSET CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-518">**CIM\_ParticipatesInSet**</span></span>](cim-participatesinset.md)
</dt> <dd>

<span data-ttu-id="fde4c-519">La clase [**CIM \_ ParticipatesInSet**](cim-participatesinset.md) identifica los elementos físicos que se deben reemplazar juntos.</span><span class="sxs-lookup"><span data-stu-id="fde4c-519">The [**CIM\_ParticipatesInSet**](cim-participatesinset.md) class identifies physical elements that should be replaced together.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-520">**\_PCICONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-520">**CIM\_PCIController**</span></span>](cim-pcicontroller.md)
</dt> <dd>

<span data-ttu-id="fde4c-521">La clase [**CIM \_ PCIController**](cim-pcicontroller.md) representa las propiedades y la administración de un controlador PCI.</span><span class="sxs-lookup"><span data-stu-id="fde4c-521">The [**CIM\_PCIController**](cim-pcicontroller.md) class represents the properties and management of a PCI controller.</span></span> <span data-ttu-id="fde4c-522">Las propiedades de esta clase y sus subclases se definen en las diversas especificaciones de PCI publicadas por PCI SIG.</span><span class="sxs-lookup"><span data-stu-id="fde4c-522">The properties in this class and its subclasses are defined in the various PCI specifications published by the PCI SIG.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-523">**\_PCMCIACONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-523">**CIM\_PCMCIAController**</span></span>](cim-pcmciacontroller.md)
</dt> <dd>

<span data-ttu-id="fde4c-524">La clase [**CIM \_ PCMCIAController**](cim-pcmciacontroller.md) representa las capacidades y la administración de un controlador de la Asociación Internacional de tarjetas de memoria (PCMCIA) del equipo.</span><span class="sxs-lookup"><span data-stu-id="fde4c-524">The [**CIM\_PCMCIAController**](cim-pcmciacontroller.md) class represents the capabilities and management of a Personal Computer Memory Card International Association (PCMCIA) controller.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-525">**\_PCVIDEOCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-525">**CIM\_PCVideoController**</span></span>](cim-pcvideocontroller.md)
</dt> <dd>

<span data-ttu-id="fde4c-526">El [**\_ PCVideoController CIM**](cim-pcvideocontroller.md) representa las capacidades y la administración de un controlador de vídeo de equipo personal, un subtipo de controlador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="fde4c-526">The [**CIM\_PCVideoController**](cim-pcvideocontroller.md) represents the capabilities and management of a personal computer video controller, a subtype of a video controller.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-527">**\_PEXTENTREDUNDANCYCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-527">**CIM\_PExtentRedundancyComponent**</span></span>](cim-pextentredundancycomponent.md)
</dt> <dd>

<span data-ttu-id="fde4c-528">La clase [**CIM \_ PExtentRedundancyComponent**](cim-pextentredundancycomponent.md) representa las extensiones físicas que participan en un grupo de redundancia de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="fde4c-528">The [**CIM\_PExtentRedundancyComponent**](cim-pextentredundancycomponent.md) class represents the physical extents that participate in a storage redundancy group.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-529">**\_PHYSICALCAPACITY CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-529">**CIM\_PhysicalCapacity**</span></span>](cim-physicalcapacity.md)
</dt> <dd>

<span data-ttu-id="fde4c-530">La clase [**CIM \_ PhysicalCapacity**](cim-physicalcapacity.md) es una clase abstracta que representa los requisitos mínimo y máximo de un elemento físico y su capacidad para admitir distintos tipos de hardware.</span><span class="sxs-lookup"><span data-stu-id="fde4c-530">The [**CIM\_PhysicalCapacity**](cim-physicalcapacity.md) class is an abstract class that represents a physical element's minimum and maximum requirements and its ability to support different types of hardware.</span></span> <span data-ttu-id="fde4c-531">Por ejemplo, los requisitos de memoria mínima y máxima se pueden modelar como una subclase de **\_ PhysicalCapacity de CIM**.</span><span class="sxs-lookup"><span data-stu-id="fde4c-531">For example, minimum and maximum memory requirements can be modeled as a subclass of **CIM\_PhysicalCapacity**.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-532">**\_PHYSICALCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-532">**CIM\_PhysicalComponent**</span></span>](cim-physicalcomponent.md)
</dt> <dd>

<span data-ttu-id="fde4c-533">La clase [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md) representa un componente de bajo nivel o básico dentro de un paquete.</span><span class="sxs-lookup"><span data-stu-id="fde4c-533">The [**CIM\_PhysicalComponent**](cim-physicalcomponent.md) class represents a low-level or basic component within a package.</span></span> <span data-ttu-id="fde4c-534">Un elemento físico que no es un vínculo, conector o paquete es un descendiente (o miembro) de esta clase.</span><span class="sxs-lookup"><span data-stu-id="fde4c-534">A physical element that is not a link, connector, or package is a descendant (or member) of this class.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-535">**\_PHYSICALCONNECTOR CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-535">**CIM\_PhysicalConnector**</span></span>](cim-physicalconnector.md)
</dt> <dd>

<span data-ttu-id="fde4c-536">La clase [**CIM \_ PhysicalConnector**](cim-physicalconnector.md) representa cualquier elemento físico que se utiliza para conectarse a otros elementos.</span><span class="sxs-lookup"><span data-stu-id="fde4c-536">The [**CIM\_PhysicalConnector**](cim-physicalconnector.md) class represents any physical element that is used to connect to other elements.</span></span> <span data-ttu-id="fde4c-537">Cualquier objeto que pueda conectarse y transmitir señales o potencia entre dos o más elementos físicos es un descendiente (o miembro) de esta clase.</span><span class="sxs-lookup"><span data-stu-id="fde4c-537">Any object that can connect and transmit signals or power between two or more physical elements is a descendant (or member) of this class.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-538">**\_PHYSICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-538">**CIM\_PhysicalElement**</span></span>](cim-physicalelement.md)
</dt> <dd>

<span data-ttu-id="fde4c-539">Las subclases [**\_ PhysicalElement de CIM**](cim-physicalelement.md) definen cualquier componente de un sistema que tenga una identidad física distinta.</span><span class="sxs-lookup"><span data-stu-id="fde4c-539">The [**CIM\_PhysicalElement**](cim-physicalelement.md) subclasses define any component of a system that has a distinct physical identity.</span></span> <span data-ttu-id="fde4c-540">Las instancias de esta clase se pueden definir en términos de etiquetas que se pueden adjuntar físicamente al objeto.</span><span class="sxs-lookup"><span data-stu-id="fde4c-540">Instances of this class can be defined in terms of labels that can be physically attached to the object.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-541">**\_PHYSICALELEMENTLOCATION CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-541">**CIM\_PhysicalElementLocation**</span></span>](cim-physicalelementlocation.md)
</dt> <dd>

<span data-ttu-id="fde4c-542">La [**clase \_ PhysicalElementLocation de CIM**](cim-physicalelementlocation.md) asocia un elemento físico a un objeto de [**\_ Ubicación CIM**](cim-location.md) para fines de inventario o de reemplazo.</span><span class="sxs-lookup"><span data-stu-id="fde4c-542">The [**CIM\_PhysicalElementLocation**](cim-physicalelementlocation.md) class associates a physical element with a [**CIM\_Location**](cim-location.md) object for inventory or replacement purposes.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-543">**\_PHYSICALEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-543">**CIM\_PhysicalExtent**</span></span>](cim-physicalextent.md)
</dt> <dd>

<span data-ttu-id="fde4c-544">La clase [**CIM \_ PhysicalExtent**](cim-physicalextent.md) representa una implementación RAID de SCC.</span><span class="sxs-lookup"><span data-stu-id="fde4c-544">The [**CIM\_PhysicalExtent**](cim-physicalextent.md) class represents an SCC RAID implementation.</span></span> <span data-ttu-id="fde4c-545">Define las direcciones de bloque direccionables consecutivas en un único dispositivo de almacenamiento que se tratan como una única extensión de almacenamiento en la misma clase [**\_ StorageRedundancyGroup de CIM**](cim-storageredundancygroup.md) .</span><span class="sxs-lookup"><span data-stu-id="fde4c-545">It defines the consecutive addressable block addresses on a single storage device that are treated as a single storage extent in the same [**CIM\_StorageRedundancyGroup**](cim-storageredundancygroup.md) class.</span></span> <span data-ttu-id="fde4c-546">Una alternativa, cuando se utiliza la configuración automática, es crear una instancia de la [**clase \_ AggregatePExtent de CIM**](cim-aggregatepextent.md) o extenderla.</span><span class="sxs-lookup"><span data-stu-id="fde4c-546">An alternative, when automatic configuration is used, is to instantiate or extend the [**CIM\_AggregatePExtent**](cim-aggregatepextent.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-547">**\_PHYSICALFRAME CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-547">**CIM\_PhysicalFrame**</span></span>](cim-physicalframe.md)
</dt> <dd>

<span data-ttu-id="fde4c-548">La clase [**CIM \_ PhysicalFrame**](cim-physicalframe.md) es una clase primaria de bastidores, chasis y otros alojamientos de fotogramas, tal y como se definen en las clases de extensión.</span><span class="sxs-lookup"><span data-stu-id="fde4c-548">The [**CIM\_PhysicalFrame**](cim-physicalframe.md) class is a parent class of rack, chassis, and other frame enclosures as they are defined in extension classes.</span></span> <span data-ttu-id="fde4c-549">En esta clase primaria se incluyen propiedades como **VisibleAlarm** y **AudibleAlarm**, y datos relacionados con las infracciones de seguridad.</span><span class="sxs-lookup"><span data-stu-id="fde4c-549">Properties such as **VisibleAlarm** and **AudibleAlarm**, and data related to security breaches are included in this parent class.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-550">**\_PHYSICALLINK CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-550">**CIM\_PhysicalLink**</span></span>](cim-physicallink.md)
</dt> <dd>

<span data-ttu-id="fde4c-551">La clase [**CIM \_ PhysicalLink**](cim-physicallink.md) representa el cableado de los elementos físicos.</span><span class="sxs-lookup"><span data-stu-id="fde4c-551">The [**CIM\_PhysicalLink**](cim-physicallink.md) class represents the cabling of physical elements.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-552">**\_PHYSICALMEDIA CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-552">**CIM\_PhysicalMedia**</span></span>](cim-physicalmedia.md)
</dt> <dd>

<span data-ttu-id="fde4c-553">La clase [**CIM \_ PhysicalMedia**](cim-physicalmedia.md) representa los tipos de documentación y el medio de almacenamiento, como cintas, CD-ROM, etc.</span><span class="sxs-lookup"><span data-stu-id="fde4c-553">The [**CIM\_PhysicalMedia**](cim-physicalmedia.md) class represents types of documentation and storage medium, such as tapes, CD ROMs, and so on.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-554">**\_PHYSICALMEMORY CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-554">**CIM\_PhysicalMemory**</span></span>](cim-physicalmemory.md)
</dt> <dd>

<span data-ttu-id="fde4c-555">La clase [**CIM \_ PhysicalMemory**](cim-physicalmemory.md) representa dispositivos de memoria de bajo nivel, como SIMM, DIMM, chips de memoria sin procesar, etc.</span><span class="sxs-lookup"><span data-stu-id="fde4c-555">The [**CIM\_PhysicalMemory**](cim-physicalmemory.md) class represents low-level memory devices, such as SIMMS, DIMMs, raw memory chips, and so on.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-556">**\_PHYSICALPACKAGE CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-556">**CIM\_PhysicalPackage**</span></span>](cim-physicalpackage.md)
</dt> <dd>

<span data-ttu-id="fde4c-557">La clase [**CIM \_ PhysicalPackage**](cim-physicalpackage.md) representa los elementos físicos que contienen u hospedan otros componentes.</span><span class="sxs-lookup"><span data-stu-id="fde4c-557">The [**CIM\_PhysicalPackage**](cim-physicalpackage.md) class represents physical elements that contain or host other components.</span></span> <span data-ttu-id="fde4c-558">Algunos ejemplos son un alojamiento en bastidor o una tarjeta adaptadora.</span><span class="sxs-lookup"><span data-stu-id="fde4c-558">Examples are a rack enclosure or an adapter card.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-559">**\_POINTINGDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-559">**CIM\_PointingDevice**</span></span>](cim-pointingdevice.md)
</dt> <dd>

<span data-ttu-id="fde4c-560">La clase [**CIM \_ PointingDevice**](cim-pointingdevice.md) representa un dispositivo que apunta a las regiones de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="fde4c-560">The [**CIM\_PointingDevice**](cim-pointingdevice.md) class represents a device that points to regions on the display.</span></span> <span data-ttu-id="fde4c-561">Cualquier dispositivo que manipula un puntero, o apunta a regiones de una presentación visual, es un miembro de esta clase.</span><span class="sxs-lookup"><span data-stu-id="fde4c-561">Any device that manipulates a pointer, or points to regions on a visual display, is a member of this class.</span></span> <span data-ttu-id="fde4c-562">Por ejemplo, un mouse, un lápiz, un teclado táctil o una tableta.</span><span class="sxs-lookup"><span data-stu-id="fde4c-562">For example, a mouse, stylus, touch pad, or tablet.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-563">**\_POTSMODEM CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-563">**CIM\_POTSModem**</span></span>](cim-potsmodem.md)
</dt> <dd>

<span data-ttu-id="fde4c-564">La clase [**CIM \_ POTSModem**](cim-potsmodem.md) representa un dispositivo que traduce los datos binarios en modulaciones de onda para la transmisión basada en sonido mediante la conexión a la red de sistema telefónico anterior (POTS).</span><span class="sxs-lookup"><span data-stu-id="fde4c-564">The [**CIM\_POTSModem**](cim-potsmodem.md) class represents a device that translates binary data into wave modulations for sound-based transmission by connecting to the Plain Old Telephone System (POTS) network.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-565">**Sistema \_ CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-565">**CIM\_PowerSupply**</span></span>](cim-powersupply.md)
</dt> <dd>

<span data-ttu-id="fde4c-566">La clase de energía [**CIM \_**](cim-powersupply.md) representa las capacidades y la administración del dispositivo lógico de fuente de alimentación.</span><span class="sxs-lookup"><span data-stu-id="fde4c-566">The [**CIM\_PowerSupply**](cim-powersupply.md) class represents the capabilities and management of the power supply logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-567">**\_Impresora CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-567">**CIM\_Printer**</span></span>](cim-printer.md)
</dt> <dd>

<span data-ttu-id="fde4c-568">La clase de [**\_ impresora CIM**](cim-printer.md) representa las capacidades y la administración del dispositivo lógico de impresora.</span><span class="sxs-lookup"><span data-stu-id="fde4c-568">The [**CIM\_Printer**](cim-printer.md) class represents the capabilities and management of the printer logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-569">**\_Proceso CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-569">**CIM\_Process**</span></span>](cim-process.md)
</dt> <dd>

<span data-ttu-id="fde4c-570">La clase de [**\_ proceso CIM**](cim-process.md) representa una única instancia de un programa en ejecución.</span><span class="sxs-lookup"><span data-stu-id="fde4c-570">The [**CIM\_Process**](cim-process.md) class represents a single instance of a running program.</span></span> <span data-ttu-id="fde4c-571">Un usuario suele ver un proceso como una aplicación o una tarea.</span><span class="sxs-lookup"><span data-stu-id="fde4c-571">A user typically sees a process as an application or task.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-572">**\_PROCESSEXECUTABLE CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-572">**CIM\_ProcessExecutable**</span></span>](cim-processexecutable.md)
</dt> <dd>

<span data-ttu-id="fde4c-573">La clase [**CIM \_ ProcessExecutable**](cim-processexecutable.md) representa un vínculo entre un proceso y un archivo de datos e indica que el archivo participa en la ejecución del proceso.</span><span class="sxs-lookup"><span data-stu-id="fde4c-573">The [**CIM\_ProcessExecutable**](cim-processexecutable.md) class represents a link between a process and data file, and indicates that the file participates in the execution of the process.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-574">**\_Procesador CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-574">**CIM\_Processor**</span></span>](cim-processor.md)
</dt> <dd>

<span data-ttu-id="fde4c-575">La clase de [**\_ procesador de CIM**](cim-processor.md) representa las capacidades y la administración del dispositivo lógico del procesador.</span><span class="sxs-lookup"><span data-stu-id="fde4c-575">The [**CIM\_Processor**](cim-processor.md) class represents the capabilities and management of the processor logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-576">**\_PROCESSTHREAD CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-576">**CIM\_ProcessThread**</span></span>](cim-processthread.md)
</dt> <dd>

<span data-ttu-id="fde4c-577">La clase [**CIM \_ ProcessThread**](cim-processthread.md) representa un vínculo entre un proceso y los subprocesos que se ejecutan en el contexto del proceso.</span><span class="sxs-lookup"><span data-stu-id="fde4c-577">The [**CIM\_ProcessThread**](cim-processthread.md) class represents a link between a process and the threads running in the context of the process.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-578">**\_Producto CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-578">**CIM\_Product**</span></span>](cim-product.md)
</dt> <dd>

<span data-ttu-id="fde4c-579">La clase de [**\_ producto CIM**](cim-product.md) es una clase concreta que representa una colección de elementos físicos, características de software y otros productos, adquiridos como una unidad.</span><span class="sxs-lookup"><span data-stu-id="fde4c-579">The [**CIM\_Product**](cim-product.md) class is a concrete class that represents a collection of physical elements, software features and, other products, acquired as a unit.</span></span> <span data-ttu-id="fde4c-580">La adquisición implica un acuerdo entre el proveedor y el consumidor, que puede tener implicaciones en las licencias, el soporte técnico y la garantía del producto.</span><span class="sxs-lookup"><span data-stu-id="fde4c-580">Acquisition implies an agreement between the supplier and consumer, which can have implications on product licensing, support, and warranty.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-581">**\_PRODUCTFRU CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-581">**CIM\_ProductFRU**</span></span>](cim-productfru.md)
</dt> <dd>

<span data-ttu-id="fde4c-582">La clase [**CIM \_ ProductFRU**](cim-productfru.md) representa una asociación entre el producto y una unidad reemplazable en campo (FRU), que proporciona información acerca de los componentes de producto que se han reemplazado o se han sustituido.</span><span class="sxs-lookup"><span data-stu-id="fde4c-582">The [**CIM\_ProductFRU**](cim-productfru.md) class represents an association between the product and a field replaceable unit (FRU), which provides information about product components that have been, or are being replaced.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-583">**\_PRODUCTPARENTCHILD CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-583">**CIM\_ProductParentChild**</span></span>](cim-productparentchild.md)
</dt> <dd>

<span data-ttu-id="fde4c-584">La [**Asociación \_ ProductParentChild de CIM**](cim-productparentchild.md) define una jerarquía de elementos primarios y secundarios entre productos.</span><span class="sxs-lookup"><span data-stu-id="fde4c-584">The [**CIM\_ProductParentChild**](cim-productparentchild.md) association defines a parent-child hierarchy among products.</span></span> <span data-ttu-id="fde4c-585">Por ejemplo, un producto puede estar incluido en otros productos.</span><span class="sxs-lookup"><span data-stu-id="fde4c-585">For example, a product can come bundled with other products.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-586">**\_PRODUCTPHYSICALELEMENTS CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-586">**CIM\_ProductPhysicalElements**</span></span>](cim-productphysicalelements.md)
</dt> <dd>

<span data-ttu-id="fde4c-587">La clase [**CIM \_ ProductPhysicalElements**](cim-productphysicalelements.md) representa los elementos físicos que componen un producto.</span><span class="sxs-lookup"><span data-stu-id="fde4c-587">The [**CIM\_ProductPhysicalElements**](cim-productphysicalelements.md) class represents the physical elements that make up a product.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-588">**\_PRODUCTPRODUCTDEPENDENCY CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-588">**CIM\_ProductProductDependency**</span></span>](cim-productproductdependency.md)
</dt> <dd>

<span data-ttu-id="fde4c-589">La clase [**CIM \_ ProductProductDependency**](cim-productproductdependency.md) representa una asociación entre dos productos, lo que indica que se debe instalar o ausente un para que el otro funcione.</span><span class="sxs-lookup"><span data-stu-id="fde4c-589">The [**CIM\_ProductProductDependency**](cim-productproductdependency.md) class represents an association between two products, which indicates that one must be installed or absent for the other to function.</span></span> <span data-ttu-id="fde4c-590">Es conceptualmente equivalente a la Asociación [**\_ ServiceServiceDependency de CIM**](cim-serviceservicedependency.md) .</span><span class="sxs-lookup"><span data-stu-id="fde4c-590">This is conceptually equivalent to the [**CIM\_ServiceServiceDependency**](cim-serviceservicedependency.md) association.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-591">**\_PRODUCTSOFTWAREFEATURES CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-591">**CIM\_ProductSoftwareFeatures**</span></span>](cim-productsoftwarefeatures.md)
</dt> <dd>

<span data-ttu-id="fde4c-592">La [**Asociación \_ ProductSoftwareFeatures de CIM**](cim-productsoftwarefeatures.md) identifica las características de software para un producto determinado.</span><span class="sxs-lookup"><span data-stu-id="fde4c-592">The [**CIM\_ProductSoftwareFeatures**](cim-productsoftwarefeatures.md) association identifies the software features for a particular product.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-593">**\_PRODUCTSUPPORT CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-593">**CIM\_ProductSupport**</span></span>](cim-productsupport.md)
</dt> <dd>

<span data-ttu-id="fde4c-594">La clase [**CIM \_ ProductSupport**](cim-productsupport.md) representa una asociación entre el producto y el acceso de soporte que muestra cómo se obtiene la compatibilidad con el producto.</span><span class="sxs-lookup"><span data-stu-id="fde4c-594">The [**CIM\_ProductSupport**](cim-productsupport.md) class represents an association between product and support access that conveys how support is obtained for the product.</span></span> <span data-ttu-id="fde4c-595">Hay varios tipos de soporte técnico disponibles para un producto; el mismo objeto de soporte técnico puede proporcionar asistencia para varios productos.</span><span class="sxs-lookup"><span data-stu-id="fde4c-595">Various types of support are available for a product; the same support object can provide assistance for multiple products.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-596">**ProtectedSpaceExtent de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="fde4c-596">**CIM\_ProtectedSpaceExtent**</span></span>](cim-protectedspaceextent.md)
</dt> <dd>

<span data-ttu-id="fde4c-597">La clase [**CIM \_ ProtectedSpaceExtent**](cim-protectedspaceextent.md) representa direcciones de bloques lógicos direccionables, que se tratan como una única extensión de almacenamiento, pero se encuentran en una única extensión física.</span><span class="sxs-lookup"><span data-stu-id="fde4c-597">The [**CIM\_ProtectedSpaceExtent**](cim-protectedspaceextent.md) class represents addressable logical-block addresses, which are treated as a single storage extent, but are located on a single physical extent.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-598">**\_PSEXTENTBASEDONPEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-598">**CIM\_PSExtentBasedOnPExtent**</span></span>](cim-psextentbasedonpextent.md)
</dt> <dd>

<span data-ttu-id="fde4c-599">La [**clase \_ PSExtentBasedOnPExtent de CIM**](cim-psextentbasedonpextent.md) asocia las extensiones de espacio protegidas basadas en una extensión física.</span><span class="sxs-lookup"><span data-stu-id="fde4c-599">The [**CIM\_PSExtentBasedOnPExtent**](cim-psextentbasedonpextent.md) class associates protected space extents that are based on a physical extent.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-600">**\_Bastidor CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-600">**CIM\_Rack**</span></span>](cim-rack.md)
</dt> <dd>

<span data-ttu-id="fde4c-601">La clase de [**\_ bastidor CIM**](cim-rack.md) representa un bastidor (una trama física o un alojamiento) en el que se almacena el chasis.</span><span class="sxs-lookup"><span data-stu-id="fde4c-601">The [**CIM\_Rack**](cim-rack.md) class represents a rack (a physical frame or enclosure) in which chassis are stored.</span></span> <span data-ttu-id="fde4c-602">Normalmente, un bastidor representa el alojamiento; todos los componentes que funcionan están empaquetados en el chasis.</span><span class="sxs-lookup"><span data-stu-id="fde4c-602">Typically, a rack represents the enclosure; all functioning components are packaged in the chassis.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-603">**Contrataciones \_ de CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-603">**CIM\_Realizes**</span></span>](cim-realizes.md)
</dt> <dd>

<span data-ttu-id="fde4c-604">La clase [**CIM \_ Observations**](cim-realizes.md) representa la asociación que define la asignación entre un dispositivo lógico y el componente físico que implementa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fde4c-604">The [**CIM\_Realizes**](cim-realizes.md) class represents the association that defines the mapping between a logical device and the physical component that implements the device.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-605">**\_REALIZESAGGREGATEPEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-605">**CIM\_RealizesAggregatePExtent**</span></span>](cim-realizesaggregatepextent.md)
</dt> <dd>

<span data-ttu-id="fde4c-606">La [**Asociación \_ RealizesAggregatePExtent de CIM**](cim-realizesaggregatepextent.md) representa la relación en la que se realiza la clase [**\_ AggregatePExtent de CIM**](cim-aggregatepextent.md) en un medio físico.</span><span class="sxs-lookup"><span data-stu-id="fde4c-606">The [**CIM\_RealizesAggregatePExtent**](cim-realizesaggregatepextent.md) association represents the relationship in which the [**CIM\_AggregatePExtent**](cim-aggregatepextent.md) class is realized on a physical media.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-607">**\_REALIZESDISKPARTITION CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-607">**CIM\_RealizesDiskPartition**</span></span>](cim-realizesdiskpartition.md)
</dt> <dd>

<span data-ttu-id="fde4c-608">La clase [**CIM \_ RealizesDiskPartition**](cim-realizesdiskpartition.md) representa una partición de disco en un medio físico que modela la creación de particiones en una unidad SCSI o IDE sin procesar.</span><span class="sxs-lookup"><span data-stu-id="fde4c-608">The [**CIM\_RealizesDiskPartition**](cim-realizesdiskpartition.md) class represents a disk partition on a physical media that models the creation of partitions on a raw SCSI or IDE drive.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-609">**\_REALIZESPEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-609">**CIM\_RealizesPExtent**</span></span>](cim-realizespextent.md)
</dt> <dd>

<span data-ttu-id="fde4c-610">La [**Asociación \_ RealizesPExtent de CIM**](cim-realizespextent.md) representa la relación en la que se realizan las extensiones físicas en un medio físico.</span><span class="sxs-lookup"><span data-stu-id="fde4c-610">The [**CIM\_RealizesPExtent**](cim-realizespextent.md) association represents the relationship in which physical extents are realized on a physical media.</span></span> <span data-ttu-id="fde4c-611">Además, se especifica la dirección inicial de la extensión física en el medio físico.</span><span class="sxs-lookup"><span data-stu-id="fde4c-611">In addition, the starting address of the physical extent on the physical media is specified.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-612">**\_REBOOTACTION CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-612">**CIM\_RebootAction**</span></span>](cim-rebootaction.md)
</dt> <dd>

<span data-ttu-id="fde4c-613">La [**clase \_ RebootAction de CIM**](cim-rebootaction.md) provoca un reinicio del sistema en el que está instalado el elemento de software.</span><span class="sxs-lookup"><span data-stu-id="fde4c-613">The [**CIM\_RebootAction**](cim-rebootaction.md) class causes a system reboot where the software element is installed.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-614">**\_REDUNDANCYCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-614">**CIM\_RedundancyComponent**</span></span>](cim-redundancycomponent.md)
</dt> <dd>

<span data-ttu-id="fde4c-615">La clase [**CIM \_ RedundancyComponent**](cim-redundancycomponent.md) asocia un grupo de redundancia compuesto por elementos del sistema administrados e indica que, juntos, los elementos proporcionan redundancia.</span><span class="sxs-lookup"><span data-stu-id="fde4c-615">The [**CIM\_RedundancyComponent**](cim-redundancycomponent.md) class associates a redundancy group composed of managed system elements and indicates that, together, the elements provide redundancy.</span></span> <span data-ttu-id="fde4c-616">Todos los elementos agregados en un grupo de redundancia deben ser instancias de la misma clase de objeto.</span><span class="sxs-lookup"><span data-stu-id="fde4c-616">All elements aggregated in a redundancy group should be instantiations of the same object class.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-617">**\_REDUNDANCYGROUP CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-617">**CIM\_RedundancyGroup**</span></span>](cim-redundancygroup.md)
</dt> <dd>

<span data-ttu-id="fde4c-618">La clase [**CIM \_ RedundancyGroup**](cim-redundancygroup.md) representa una colección de elementos del sistema administrados, que indica que los componentes agregados, juntos, proporcionan redundancia.</span><span class="sxs-lookup"><span data-stu-id="fde4c-618">The [**CIM\_RedundancyGroup**](cim-redundancygroup.md) class represents a collection of managed system elements, which indicates that the aggregated components, together, provide redundancy.</span></span> <span data-ttu-id="fde4c-619">Todos los elementos agregados en un grupo de redundancia deben ser instancias de la misma clase de objeto.</span><span class="sxs-lookup"><span data-stu-id="fde4c-619">All elements aggregated in a redundancy group should be instantiations of the same object class.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-620">**\_Refrigeración CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-620">**CIM\_Refrigeration**</span></span>](cim-refrigeration.md)
</dt> <dd>

<span data-ttu-id="fde4c-621">La clase de [**\_ refrigeración CIM**](cim-refrigeration.md) representa las capacidades y la administración de un dispositivo de enfriamiento de refrigeración.</span><span class="sxs-lookup"><span data-stu-id="fde4c-621">The [**CIM\_Refrigeration**](cim-refrigeration.md) class represents the capabilities and management of a refrigeration cooling device.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-622">**\_RELATEDSTATISTICS CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-622">**CIM\_RelatedStatistics**</span></span>](cim-relatedstatistics.md)
</dt> <dd>

<span data-ttu-id="fde4c-623">La [**Asociación \_ RelatedStatistics de CIM**](cim-relatedstatistics.md) representa jerarquías y dependencias de las clases de [**\_ StatisticalInformation CIM**](cim-statisticalinformation.md) relacionadas.</span><span class="sxs-lookup"><span data-stu-id="fde4c-623">The [**CIM\_RelatedStatistics**](cim-relatedstatistics.md) association represents hierarchies and dependencies of related [**CIM\_StatisticalInformation**](cim-statisticalinformation.md) classes.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-624">**\_REMOTEFILESYSTEM CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-624">**CIM\_RemoteFileSystem**</span></span>](cim-remotefilesystem.md)
</dt> <dd>

<span data-ttu-id="fde4c-625">La clase [**CIM \_ RemoteFileSystem**](cim-remotefilesystem.md) representa un sistema de archivos remoto al que se tiene acceso por medio de un servicio relacionado con la red.</span><span class="sxs-lookup"><span data-stu-id="fde4c-625">The [**CIM\_RemoteFileSystem**](cim-remotefilesystem.md) class represents a remote file system that is accessed by way of a network-related service.</span></span> <span data-ttu-id="fde4c-626">En este caso, el almacén de archivos está hospedado en un equipo, que actúa como servidor de archivos.</span><span class="sxs-lookup"><span data-stu-id="fde4c-626">In this case, the file store is hosted by a computer, which acts as a file server.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-627">**\_REMOVEDIRECTORYACTION CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-627">**CIM\_RemoveDirectoryAction**</span></span>](cim-removedirectoryaction.md)
</dt> <dd>

<span data-ttu-id="fde4c-628">La [**clase \_ RemoveDirectoryAction de CIM**](cim-removedirectoryaction.md) quita los directorios de los elementos de software.</span><span class="sxs-lookup"><span data-stu-id="fde4c-628">The [**CIM\_RemoveDirectoryAction**](cim-removedirectoryaction.md) class removes directories for software elements.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-629">**\_REMOVEFILEACTION CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-629">**CIM\_RemoveFileAction**</span></span>](cim-removefileaction.md)
</dt> <dd>

<span data-ttu-id="fde4c-630">La [**clase \_ RemoveFileAction de CIM**](cim-removefileaction.md) desinstala los archivos.</span><span class="sxs-lookup"><span data-stu-id="fde4c-630">The [**CIM\_RemoveFileAction**](cim-removefileaction.md) class uninstalls files.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-631">**\_REPLACEMENTSET CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-631">**CIM\_ReplacementSet**</span></span>](cim-replacementset.md)
</dt> <dd>

<span data-ttu-id="fde4c-632">La clase [**CIM \_ ReplacementSet**](cim-replacementset.md) agrega elementos físicos que se deben reemplazar juntos.</span><span class="sxs-lookup"><span data-stu-id="fde4c-632">The [**CIM\_ReplacementSet**](cim-replacementset.md) class aggregates physical elements that must be replaced together.</span></span> <span data-ttu-id="fde4c-633">Por ejemplo, al reemplazar una tarjeta de memoria, los chips de memoria de componente también se pueden quitar y reemplazar.</span><span class="sxs-lookup"><span data-stu-id="fde4c-633">For example, when replacing a memory card, the component memory chips can also be removed and replaced.</span></span> <span data-ttu-id="fde4c-634">O bien, esta asociación se puede usar para reemplazar o actualizar un conjunto de chips de memoria.</span><span class="sxs-lookup"><span data-stu-id="fde4c-634">Or, this association can be used to replace or upgrade a set of memory chips.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-635">**\_RESIDESONEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-635">**CIM\_ResidesOnExtent**</span></span>](cim-residesonextent.md)
</dt> <dd>

<span data-ttu-id="fde4c-636">La clase [**CIM \_ ResidesOnExtent**](cim-residesonextent.md) representa una asociación entre un sistema de archivos y la extensión de almacenamiento donde se encuentra.</span><span class="sxs-lookup"><span data-stu-id="fde4c-636">The [**CIM\_ResidesOnExtent**](cim-residesonextent.md) class represents an association between a file system and the storage extent where it is located.</span></span> <span data-ttu-id="fde4c-637">Normalmente, un sistema de archivos reside en un disco lógico.</span><span class="sxs-lookup"><span data-stu-id="fde4c-637">Typically, a file system resides on a logical disk.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-638">**Ejecución de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="fde4c-638">**CIM\_RunningOS**</span></span>](cim-runningos.md)
</dt> <dd>

<span data-ttu-id="fde4c-639">La clase [**CIM \_ Runnings**](cim-runningos.md) representa el sistema operativo que se está ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="fde4c-639">The [**CIM\_RunningOS**](cim-runningos.md) class represents the currently executing operating system.</span></span> <span data-ttu-id="fde4c-640">Como máximo, un sistema operativo puede ejecutarse en cualquier momento en un sistema informático; es posible que no se haya iniciado el equipo o que el sistema operativo sea desconocido.</span><span class="sxs-lookup"><span data-stu-id="fde4c-640">At most, one operating system can execute at any time on a computer system; the computer system may not be currently booted, or its operating system may be unknown.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-641">**\_SAPSAPDEPENDENCY CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-641">**CIM\_SAPSAPDependency**</span></span>](cim-sapsapdependency.md)
</dt> <dd>

<span data-ttu-id="fde4c-642">La [**clase \_ SAPSAPDependency de CIM**](cim-sapsapdependency.md) es una asociación entre dos puntos de acceso de servicio (SAP), que indica que el segundo SAP es necesario para que el primer SAP se conecte con su servicio.</span><span class="sxs-lookup"><span data-stu-id="fde4c-642">The [**CIM\_SAPSAPDependency**](cim-sapsapdependency.md) class is an association between two service access points (SAPs), which indicates that the second SAP is required for the first SAP to connect with its service.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-643">**\_Escáner CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-643">**CIM\_Scanner**</span></span>](cim-scanner.md)
</dt> <dd>

<span data-ttu-id="fde4c-644">El [**\_ analizador de CIM**](cim-scanner.md) representa las capacidades y la administración del dispositivo lógico del escáner.</span><span class="sxs-lookup"><span data-stu-id="fde4c-644">The [**CIM\_Scanner**](cim-scanner.md) represents the capabilities and management of the scanner logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-645">**\_SCSICONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-645">**CIM\_SCSIController**</span></span>](cim-scsicontroller.md)
</dt> <dd>

<span data-ttu-id="fde4c-646">La clase [**CIM \_ SCSIController**](cim-scsicontroller.md) representa las capacidades y la administración del dispositivo lógico SCSI Controller.</span><span class="sxs-lookup"><span data-stu-id="fde4c-646">The [**CIM\_SCSIController**](cim-scsicontroller.md) class represents the capabilities and management of the SCSI controller logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-647">**\_SCSIINTERFACE CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-647">**CIM\_SCSIInterface**</span></span>](cim-scsiinterface.md)
</dt> <dd>

<span data-ttu-id="fde4c-648">representa una relación de [**\_ ControlledBy de CIM**](cim-controlledby.md) que indica a qué dispositivos se tiene acceso a través de una controladora SCSI y las características de acceso.</span><span class="sxs-lookup"><span data-stu-id="fde4c-648">represents a [**CIM\_ControlledBy**](cim-controlledby.md) relationship that indicates which devices are accessed through a SCSI controller and the access characteristics.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-649">**\_Sensor CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-649">**CIM\_Sensor**</span></span>](cim-sensor.md)
</dt> <dd>

<span data-ttu-id="fde4c-650">La clase de [**\_ sensor CIM**](cim-sensor.md) representa un dispositivo de hardware capaz de medir las características de una propiedad física (por ejemplo, las características de temperatura o voltaje de un sistema de equipo unitario).</span><span class="sxs-lookup"><span data-stu-id="fde4c-650">The [**CIM\_Sensor**](cim-sensor.md) class represents a hardware device that is capable of measuring the characteristics of a physical property (for example, the temperature or voltage characteristics of a unitary computer system).</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-651">**\_SERIALCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-651">**CIM\_SerialController**</span></span>](cim-serialcontroller.md)
</dt> <dd>

<span data-ttu-id="fde4c-652">La clase [**CIM \_ SerialController**](cim-serialcontroller.md) representa las capacidades y la administración del dispositivo lógico de puerto serie.</span><span class="sxs-lookup"><span data-stu-id="fde4c-652">The [**CIM\_SerialController**](cim-serialcontroller.md) class represents the capabilities and management of the serial port logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-653">**\_SERIALINTERFACE CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-653">**CIM\_SerialInterface**</span></span>](cim-serialinterface.md)
</dt> <dd>

<span data-ttu-id="fde4c-654">La clase [**CIM \_ SerialInterface**](cim-serialinterface.md) representa una relación [**\_ ControlledBy de CIM**](cim-controlledby.md) que indica a qué dispositivos se tiene acceso a través del controlador serie y las características del acceso.</span><span class="sxs-lookup"><span data-stu-id="fde4c-654">The [**CIM\_SerialInterface**](cim-serialinterface.md) class represents a [**CIM\_ControlledBy**](cim-controlledby.md) relationship that indicates which devices are accessed through the serial controller and the characteristics of the access.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-655">**\_Servicio CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-655">**CIM\_Service**</span></span>](cim-service.md)
</dt> <dd>

<span data-ttu-id="fde4c-656">La clase de [**\_ servicio CIM**](cim-service.md) representa un elemento lógico que contiene información para representar y administrar la funcionalidad proporcionada por una característica de dispositivo o software.</span><span class="sxs-lookup"><span data-stu-id="fde4c-656">The [**CIM\_Service**](cim-service.md) class represents a logical element that contains information to represent and manage the functionality provided by a device or software feature.</span></span> <span data-ttu-id="fde4c-657">Un servicio es un objeto de uso general para configurar y administrar la implementación de la funcionalidad. no es la propia funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="fde4c-657">A service is a general-purpose object to configure and manage the implementation of functionality; it is not the functionality itself.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-658">**\_SERVICEACCESSBYSAP CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-658">**CIM\_ServiceAccessBySAP**</span></span>](cim-serviceaccessbysap.md)
</dt> <dd>

<span data-ttu-id="fde4c-659">La clase de asociación [**CIM \_ ServiceAccessBySAP**](cim-serviceaccessbysap.md) representa los puntos de acceso de un servicio.</span><span class="sxs-lookup"><span data-stu-id="fde4c-659">The [**CIM\_ServiceAccessBySAP**](cim-serviceaccessbysap.md) association class represents the access points for a service.</span></span> <span data-ttu-id="fde4c-660">Por ejemplo, se puede tener acceso a una impresora a través de los puntos de acceso de servicio (SAP, Macintosh o Windows), que pueden hospedarse en sistemas diferentes.</span><span class="sxs-lookup"><span data-stu-id="fde4c-660">For example, a printer can be accessed by NetWare, Macintosh, or Windows service access points (SAPs), which are potentially hosted on different systems.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-661">**\_Punto CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-661">**CIM\_ServiceAccessPoint**</span></span>](cim-serviceaccesspoint.md)
</dt> <dd>

<span data-ttu-id="fde4c-662">La clase [**CIM \_ punto**](cim-serviceaccesspoint.md) representa la capacidad de usar o invocar un servicio.</span><span class="sxs-lookup"><span data-stu-id="fde4c-662">The [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) class represents the ability to use or invoke a service.</span></span> <span data-ttu-id="fde4c-663">Los puntos de acceso representan servicios que están disponibles para su uso por parte de otras entidades.</span><span class="sxs-lookup"><span data-stu-id="fde4c-663">Access points represent services that are available for use by other entities.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-664">**\_SERVICESAPDEPENDENCY CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-664">**CIM\_ServiceSAPDependency**</span></span>](cim-servicesapdependency.md)
</dt> <dd>

<span data-ttu-id="fde4c-665">La clase [**CIM \_ ServiceSAPDependency**](cim-servicesapdependency.md) representa una asociación entre un servicio y un punto de acceso de servicio (SAP), que indica que el servicio utiliza el SAP al que se hace referencia para proporcionar su funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="fde4c-665">The [**CIM\_ServiceSAPDependency**](cim-servicesapdependency.md) class represents an association between a service and a service access point (SAP), which indicates that the referenced SAP is used by the service to provide its functionality.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-666">**\_SERVICESERVICEDEPENDENCY CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-666">**CIM\_ServiceServiceDependency**</span></span>](cim-serviceservicedependency.md)
</dt> <dd>

<span data-ttu-id="fde4c-667">La clase [**CIM \_ ServiceServiceDependency**](cim-serviceservicedependency.md) representa una asociación entre dos servicios.</span><span class="sxs-lookup"><span data-stu-id="fde4c-667">The [**CIM\_ServiceServiceDependency**](cim-serviceservicedependency.md) class represents an association between two services.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-668">**Configuración de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="fde4c-668">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dd>

<span data-ttu-id="fde4c-669">La clase de [**\_ configuración CIM**](cim-setting.md) representa parámetros operativos y relacionados con la configuración de uno o más elementos del sistema administrados.</span><span class="sxs-lookup"><span data-stu-id="fde4c-669">The [**CIM\_Setting**](cim-setting.md) class represents configuration-related and operational parameters for one or more managed system elements.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-670">**\_SETTINGCHECK CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-670">**CIM\_SettingCheck**</span></span>](cim-settingcheck.md)
</dt> <dd>

<span data-ttu-id="fde4c-671">La clase [**CIM \_ SettingCheck**](cim-settingcheck.md) especifica la información necesaria para comprobar un archivo de configuración determinado para una entrada específica que contiene un valor igual al valor especificado.</span><span class="sxs-lookup"><span data-stu-id="fde4c-671">The [**CIM\_SettingCheck**](cim-settingcheck.md) class specifies information needed to check a particular setting file for a specific entry that contains a value equal to the value specified.</span></span> <span data-ttu-id="fde4c-672">Se supone que todas las comparaciones no distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="fde4c-672">All comparisons are assumed to be case insensitive.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-673">**\_SETTINGCONTEXT CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-673">**CIM\_SettingContext**</span></span>](cim-settingcontext.md)
</dt> <dd>

<span data-ttu-id="fde4c-674">La [**clase \_ SettingContext de CIM**](cim-settingcontext.md) asocia objetos de configuración con objetos de configuración.</span><span class="sxs-lookup"><span data-stu-id="fde4c-674">The [**CIM\_SettingContext**](cim-settingcontext.md) class associates configuration objects with setting objects.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-675">**\_Ranura CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-675">**CIM\_Slot**</span></span>](cim-slot.md)
</dt> <dd>

<span data-ttu-id="fde4c-676">La clase de [**\_ ranura CIM**](cim-slot.md) representa los conectores en los que se insertan los paquetes.</span><span class="sxs-lookup"><span data-stu-id="fde4c-676">The [**CIM\_Slot**](cim-slot.md) class represents connectors into which packages are inserted.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-677">**\_SLOTINSLOT CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-677">**CIM\_SlotInSlot**</span></span>](cim-slotinslot.md)
</dt> <dd>

<span data-ttu-id="fde4c-678">La [**relación \_ SlotInSlot de CIM**](cim-slotinslot.md) representa la capacidad de un adaptador especial de extender la estructura de ranura existente para habilitar la conexión de tarjetas que, de lo contrario, no es compatible con un marco o un panel de hospedaje.</span><span class="sxs-lookup"><span data-stu-id="fde4c-678">The [**CIM\_SlotInSlot**](cim-slotinslot.md) relationship represents the ability of a special adapter to extend the existing slot structure to enable otherwise incompatible cards to be plugged into a frame or hosting board.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-679">**\_SOFTWAREELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-679">**CIM\_SoftwareElement**</span></span>](cim-softwareelement.md)
</dt> <dd>

<span data-ttu-id="fde4c-680">La [**clase \_ SoftwareElement de CIM**](cim-softwareelement.md) descompone un [**objeto \_ SoftwareFeature de CIM**](cim-softwarefeature.md) en un conjunto de elementos que se pueden administrar o implementar individualmente para una plataforma determinada.</span><span class="sxs-lookup"><span data-stu-id="fde4c-680">The [**CIM\_SoftwareElement**](cim-softwareelement.md) class decomposes a [**CIM\_SoftwareFeature**](cim-softwarefeature.md) object into a set of individually manageable or deployable parts for a particular platform.</span></span> <span data-ttu-id="fde4c-681">La plataforma de un elemento de software está identificada de forma exclusiva por su sistema operativo y la arquitectura de hardware subyacente.</span><span class="sxs-lookup"><span data-stu-id="fde4c-681">A software element's platform is uniquely identified by its underlying hardware architecture and operating system.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-682">**\_SOFTWAREELEMENTACTIONS CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-682">**CIM\_SoftwareElementActions**</span></span>](cim-softwareelementactions.md)
</dt> <dd>

<span data-ttu-id="fde4c-683">La [**Asociación \_ SoftwareElementActions de CIM**](cim-softwareelementactions.md) identifica las acciones de un elemento de software.</span><span class="sxs-lookup"><span data-stu-id="fde4c-683">The [**CIM\_SoftwareElementActions**](cim-softwareelementactions.md) association identifies the actions for a software element.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-684">**\_SOFTWAREELEMENTCHECKS CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-684">**CIM\_SoftwareElementChecks**</span></span>](cim-softwareelementchecks.md)
</dt> <dd>

<span data-ttu-id="fde4c-685">La clase de asociación [**CIM \_ SoftwareElementChecks**](cim-softwareelementchecks.md) relaciona un elemento de software con información de condición o ubicación que una característica puede necesitar.</span><span class="sxs-lookup"><span data-stu-id="fde4c-685">The [**CIM\_SoftwareElementChecks**](cim-softwareelementchecks.md) association class relates a software element with condition or location information that a feature may require.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-686">**\_SOFTWAREELEMENTVERSIONCHECK CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-686">**CIM\_SoftwareElementVersionCheck**</span></span>](cim-softwareelementversioncheck.md)
</dt> <dd>

<span data-ttu-id="fde4c-687">La clase [**CIM \_ SoftwareElementVersionCheck**](cim-softwareelementversioncheck.md) representa un tipo de elemento de software que debe existir en el entorno.</span><span class="sxs-lookup"><span data-stu-id="fde4c-687">The [**CIM\_SoftwareElementVersionCheck**](cim-softwareelementversioncheck.md) class represents a type of software element that must exist in the environment.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-688">**\_SOFTWAREFEATURE CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-688">**CIM\_SoftwareFeature**</span></span>](cim-softwarefeature.md)
</dt> <dd>

<span data-ttu-id="fde4c-689">La clase [**CIM \_ SoftwareFeature**](cim-softwarefeature.md) representa una función o funcionalidad determinada de un sistema de aplicaciones o productos.</span><span class="sxs-lookup"><span data-stu-id="fde4c-689">The [**CIM\_SoftwareFeature**](cim-softwarefeature.md) class represents a particular function or capability of a product or application system.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-690">**\_SOFTWAREFEATURESAPIMPLEMENTATION CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-690">**CIM\_SoftwareFeatureSAPImplementation**</span></span>](cim-softwarefeaturesapimplementation.md)
</dt> <dd>

<span data-ttu-id="fde4c-691">La clase [**CIM \_ SoftwareFeatureSAPImplementation**](cim-softwarefeaturesapimplementation.md) representa una asociación entre un punto de acceso al servicio (SAP) y cómo se implementa en el software.</span><span class="sxs-lookup"><span data-stu-id="fde4c-691">The [**CIM\_SoftwareFeatureSAPImplementation**](cim-softwarefeaturesapimplementation.md) class represents an association between a service access point (SAP) and how it is implemented in software.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-692">**\_SOFTWAREFEATURESERVICEIMPLEMENTATION CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-692">**CIM\_SoftwareFeatureServiceImplementation**</span></span>](cim-softwarefeatureserviceimplementation.md)
</dt> <dd>

<span data-ttu-id="fde4c-693">La clase [**CIM \_ SoftwareFeatureServiceImplementation**](cim-softwarefeatureserviceimplementation.md) representa una asociación entre un servicio y cómo se implementa en el software.</span><span class="sxs-lookup"><span data-stu-id="fde4c-693">The [**CIM\_SoftwareFeatureServiceImplementation**](cim-softwarefeatureserviceimplementation.md) class represents an association between a service and how it is implemented in software.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-694">**\_SOFTWAREFEATURESOFTWAREELEMENTS CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-694">**CIM\_SoftwareFeatureSoftwareElements**</span></span>](cim-softwarefeaturesoftwareelements.md)
</dt> <dd>

<span data-ttu-id="fde4c-695">La [**Asociación \_ SoftwareFeatureSoftwareElements de CIM**](cim-softwarefeaturesoftwareelements.md) identifica los elementos de software que componen una característica de software específica.</span><span class="sxs-lookup"><span data-stu-id="fde4c-695">The [**CIM\_SoftwareFeatureSoftwareElements**](cim-softwarefeaturesoftwareelements.md) association identifies the software elements that make up a specific software feature.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-696">**\_SPAREGROUP CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-696">**CIM\_SpareGroup**</span></span>](cim-sparegroup.md)
</dt> <dd>

<span data-ttu-id="fde4c-697">La clase [**CIM \_ SpareGroup**](cim-sparegroup.md) se deriva de la clase [**\_ RedundancyGroup de CIM**](cim-redundancygroup.md) e indica que uno o varios de los elementos agregados se pueden retener.</span><span class="sxs-lookup"><span data-stu-id="fde4c-697">The [**CIM\_SpareGroup**](cim-sparegroup.md) class is derived from the [**CIM\_RedundancyGroup**](cim-redundancygroup.md) class and indicates that one or more of the aggregated elements can be spared.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-698">**\_STATISTICALINFORMATION CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-698">**CIM\_StatisticalInformation**</span></span>](cim-statisticalinformation.md)
</dt> <dd>

<span data-ttu-id="fde4c-699">La clase [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md) es una clase raíz para la colección arbitraria de datos estadísticos o métricas aplicables a uno o varios elementos del sistema administrados.</span><span class="sxs-lookup"><span data-stu-id="fde4c-699">The [**CIM\_StatisticalInformation**](cim-statisticalinformation.md) class is a root class for the arbitrary collection of statistical data or metrics applicable to one or more managed system elements.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-700">**Estadísticas de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="fde4c-700">**CIM\_Statistics**</span></span>](cim-statistics.md)
</dt> <dd>

<span data-ttu-id="fde4c-701">La clase de [**\_ estadísticas CIM**](cim-statistics.md) representa una asociación que relaciona los elementos del sistema administrados con los grupos estadísticos que se aplican a ellos.</span><span class="sxs-lookup"><span data-stu-id="fde4c-701">The [**CIM\_Statistics**](cim-statistics.md) class represents an association that relates managed system elements to the statistical groups that apply to them.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-702">**\_STORAGEDEFECT CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-702">**CIM\_StorageDefect**</span></span>](cim-storagedefect.md)
</dt> <dd>

<span data-ttu-id="fde4c-703">La agregación [**\_ StorageDefect de CIM**](cim-storagedefect.md) recopila los errores de almacenamiento para una extensión de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="fde4c-703">The [**CIM\_StorageDefect**](cim-storagedefect.md) aggregation collects the storage errors for a storage extent.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-704">**\_STORAGEERROR CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-704">**CIM\_StorageError**</span></span>](cim-storageerror.md)
</dt> <dd>

<span data-ttu-id="fde4c-705">La clase [**CIM \_ StorageError**](cim-storageerror.md) representa bloques de medios o espacio de memoria que se asignan sin usar debido a errores.</span><span class="sxs-lookup"><span data-stu-id="fde4c-705">The [**CIM\_StorageError**](cim-storageerror.md) class represents blocks of media or memory space that are mapped out-of-use due to errors.</span></span> <span data-ttu-id="fde4c-706">La clave de la clase es la propiedad **StartingAddress** de los bytes con error.</span><span class="sxs-lookup"><span data-stu-id="fde4c-706">The key of the class is the **StartingAddress** property of the bytes in error.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-707">**\_STORAGEEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-707">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> <dd>

<span data-ttu-id="fde4c-708">La clase [**CIM \_ StorageExtent**](cim-storageextent.md) representa las capacidades y la administración de los distintos medios que existen para almacenar datos y permitir la recuperación de datos.</span><span class="sxs-lookup"><span data-stu-id="fde4c-708">The [**CIM\_StorageExtent**](cim-storageextent.md) class represents the capabilities and management of the various media that exist to store data and allow data retrieval.</span></span> <span data-ttu-id="fde4c-709">Esta clase primaria puede representar los distintos componentes de RAID (hardware o software) o una extensión lógica sin procesar sobre medios físicos.</span><span class="sxs-lookup"><span data-stu-id="fde4c-709">This parent class can represent the various components of RAID (hardware or software) or a raw logical extent on top of physical media.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-710">**\_STORAGEREDUNDANCYGROUP CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-710">**CIM\_StorageRedundancyGroup**</span></span>](cim-storageredundancygroup.md)
</dt> <dd>

<span data-ttu-id="fde4c-711">La clase [**CIM \_ StorageRedundancyGroup**](cim-storageredundancygroup.md) representa información de redundancia relacionada con el almacenamiento masivo.</span><span class="sxs-lookup"><span data-stu-id="fde4c-711">The [**CIM\_StorageRedundancyGroup**](cim-storageredundancygroup.md) class represents mass storage-related redundancy information.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-712">**\_SUPPORTACCESS CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-712">**CIM\_SupportAccess**</span></span>](cim-supportaccess.md)
</dt> <dd>

<span data-ttu-id="fde4c-713">La clase [**CIM \_ SupportAccess**](cim-supportaccess.md) define cómo obtener ayuda para un producto.</span><span class="sxs-lookup"><span data-stu-id="fde4c-713">The [**CIM\_SupportAccess**](cim-supportaccess.md) class defines how to obtain assistance for a product.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-714">**\_SWAPSPACECHECK CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-714">**CIM\_SwapSpaceCheck**</span></span>](cim-swapspacecheck.md)
</dt> <dd>

<span data-ttu-id="fde4c-715">La clase [**CIM \_ SwapSpaceCheck**](cim-swapspacecheck.md) especifica la cantidad de espacio de intercambio que debe estar disponible en el sistema.</span><span class="sxs-lookup"><span data-stu-id="fde4c-715">The [**CIM\_SwapSpaceCheck**](cim-swapspacecheck.md) class specifies the amount of swap space that must be available on the system.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-716">**\_Sistema CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-716">**CIM\_System**</span></span>](cim-system.md)
</dt> <dd>

<span data-ttu-id="fde4c-717">La [**clase \_ del sistema CIM**](cim-system.md) agrega un conjunto enumerable de elementos del sistema administrados.</span><span class="sxs-lookup"><span data-stu-id="fde4c-717">The [**CIM\_System**](cim-system.md) class aggregates an enumerable set of managed system elements.</span></span> <span data-ttu-id="fde4c-718">La agregación funciona como un todo funcional.</span><span class="sxs-lookup"><span data-stu-id="fde4c-718">The aggregation operates as a functional whole.</span></span> <span data-ttu-id="fde4c-719">Dentro de cualquier subclase del sistema, existe una lista bien definida de las clases de elementos del sistema administradas cuyas instancias deben agregarse.</span><span class="sxs-lookup"><span data-stu-id="fde4c-719">Within any particular subclass of the system, there is a well-defined list of managed system element classes whose instances must be aggregated.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-720">**\_SYSTEMCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-720">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> <dd>

<span data-ttu-id="fde4c-721">una clase de asociación Modelo de información común (CIM) que establece relaciones entre un sistema y los elementos del sistema administrados en los que se compone.</span><span class="sxs-lookup"><span data-stu-id="fde4c-721">a Common Information Model (CIM) association class that establishes relationships between a system and the managed system elements of which it is composed.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-722">**\_SYSTEMDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-722">**CIM\_SystemDevice**</span></span>](cim-systemdevice.md)
</dt> <dd>

<span data-ttu-id="fde4c-723">La [**Asociación \_ SystemDevice de CIM**](cim-systemdevice.md) representa una relación explícita en la que un sistema puede agregar dispositivos lógicos.</span><span class="sxs-lookup"><span data-stu-id="fde4c-723">The [**CIM\_SystemDevice**](cim-systemdevice.md) association represents an explicit relationship in which logical devices can be aggregated by a system.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-724">**\_SYSTEMRESOURCE CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-724">**CIM\_SystemResource**</span></span>](cim-systemresource.md)
</dt> <dd>

<span data-ttu-id="fde4c-725">La clase [**CIM \_ SystemResource**](cim-systemresource.md) representa una entidad administrada por BIOS o un sistema operativo que está disponible para su uso por software y dispositivos lógicos.</span><span class="sxs-lookup"><span data-stu-id="fde4c-725">The [**CIM\_SystemResource**](cim-systemresource.md) class represents an entity managed by BIOS, or an operating system that is available for use by software and logical devices.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-726">**\_Tacómetro CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-726">**CIM\_Tachometer**</span></span>](cim-tachometer.md)
</dt> <dd>

<span data-ttu-id="fde4c-727">La clase de [**\_ tacómetro CIM**](cim-tachometer.md) existe para la compatibilidad con versiones anteriores con definiciones de esquema CIM anteriores.</span><span class="sxs-lookup"><span data-stu-id="fde4c-727">The [**CIM\_Tachometer**](cim-tachometer.md) class exists for backward compatibility with earlier CIM schema definitions.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-728">**CIM \_ TapeDrive**</span><span class="sxs-lookup"><span data-stu-id="fde4c-728">**CIM\_TapeDrive**</span></span>](cim-tapedrive.md)
</dt> <dd>

<span data-ttu-id="fde4c-729">La clase [**CIM \_ TapeDrive**](cim-tapedrive.md) representa una unidad de cinta en el sistema.</span><span class="sxs-lookup"><span data-stu-id="fde4c-729">The [**CIM\_TapeDrive**](cim-tapedrive.md) class represents a tape drive on the system.</span></span> <span data-ttu-id="fde4c-730">Las unidades de cinta se distinguen principalmente en que solo se puede tener acceso a ellas de forma secuencial.</span><span class="sxs-lookup"><span data-stu-id="fde4c-730">Tape drives are primarily distinguished in that they can only be accessed sequentially.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-731">**\_TEMPERATURESENSOR CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-731">**CIM\_TemperatureSensor**</span></span>](cim-temperaturesensor.md)
</dt> <dd>

<span data-ttu-id="fde4c-732">La [**clase \_ TemperatureSensor de CIM**](cim-temperaturesensor.md) existe por compatibilidad con versiones anteriores de definiciones de esquema CIM.</span><span class="sxs-lookup"><span data-stu-id="fde4c-732">The [**CIM\_TemperatureSensor**](cim-temperaturesensor.md) class exists for backward compatibility with earlier CIM schema definitions.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-733">**Subproceso CIM \_**</span><span class="sxs-lookup"><span data-stu-id="fde4c-733">**CIM\_Thread**</span></span>](cim-thread.md)
</dt> <dd>

<span data-ttu-id="fde4c-734">La clase de [**\_ subproceso CIM**](cim-thread.md) representa la capacidad de ejecutar unidades de un proceso o una tarea, en paralelo.</span><span class="sxs-lookup"><span data-stu-id="fde4c-734">The [**CIM\_Thread**](cim-thread.md) class represents the ability to execute units of a process or task, in parallel.</span></span> <span data-ttu-id="fde4c-735">Un proceso puede tener muchos subprocesos, cada uno de los cuales es débil para el proceso.</span><span class="sxs-lookup"><span data-stu-id="fde4c-735">A process can have many threads, each of which is weak to the process.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-736">**\_TODIRECTORYACTION CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-736">**CIM\_ToDirectoryAction**</span></span>](cim-todirectoryaction.md)
</dt> <dd>

<span data-ttu-id="fde4c-737">La [**Asociación \_ ToDirectoryAction de CIM**](cim-todirectoryaction.md) identifica el directorio de destino de la acción de archivo.</span><span class="sxs-lookup"><span data-stu-id="fde4c-737">The [**CIM\_ToDirectoryAction**](cim-todirectoryaction.md) association identifies the target directory for the file action.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-738">**\_TODIRECTORYSPECIFICATION CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-738">**CIM\_ToDirectorySpecification**</span></span>](cim-todirectoryspecification.md)
</dt> <dd>

<span data-ttu-id="fde4c-739">La [**Asociación \_ ToDirectorySpecification de CIM**](cim-todirectoryspecification.md) identifica el directorio de destino de la acción de archivo.</span><span class="sxs-lookup"><span data-stu-id="fde4c-739">The [**CIM\_ToDirectorySpecification**](cim-todirectoryspecification.md) association identifies the target directory for the file action.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-740">**\_UNINTERRUPTIBLEPOWERSUPPLY CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-740">**CIM\_UninterruptiblePowerSupply**</span></span>](cim-uninterruptiblepowersupply.md)
</dt> <dd>

<span data-ttu-id="fde4c-741">La clase [**CIM \_ UninterruptiblePowerSupply**](cim-uninterruptiblepowersupply.md) representa las capacidades y la administración de un sistema de alimentación ininterrumpida (SAI).</span><span class="sxs-lookup"><span data-stu-id="fde4c-741">The [**CIM\_UninterruptiblePowerSupply**](cim-uninterruptiblepowersupply.md) class represents the capabilities and management of an uninterruptible power supply (UPS).</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-742">**\_UNITARYCOMPUTERSYSTEM CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-742">**CIM\_UnitaryComputerSystem**</span></span>](cim-unitarycomputersystem.md)
</dt> <dd>

<span data-ttu-id="fde4c-743">La clase [**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md) representa un equipo de escritorio, móvil, de red, servidor u otro tipo de sistema de un solo nodo.</span><span class="sxs-lookup"><span data-stu-id="fde4c-743">The [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md) class represents a desktop, mobile, network computer, server, or other type of single-node computer system.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-744">**\_USBCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-744">**CIM\_USBController**</span></span>](cim-usbcontroller.md)
</dt> <dd>

<span data-ttu-id="fde4c-745">La clase [**CIM \_ USBController**](cim-usbcontroller.md) representa las capacidades y la administración de una controladora USB.</span><span class="sxs-lookup"><span data-stu-id="fde4c-745">The [**CIM\_USBController**](cim-usbcontroller.md) class represents the capabilities and management of a USB controller.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-746">**\_USBCONTROLLERHASHUB CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-746">**CIM\_USBControllerHasHub**</span></span>](cim-usbcontrollerhashub.md)
</dt> <dd>

<span data-ttu-id="fde4c-747">La clase [**CIM \_ USBControllerHasHub**](cim-usbcontrollerhashub.md) define los concentradores que son inferiores al controlador USB.</span><span class="sxs-lookup"><span data-stu-id="fde4c-747">The [**CIM\_USBControllerHasHub**](cim-usbcontrollerhashub.md) class defines the hubs that are downstream of the USB controller.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-748">**\_USBDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-748">**CIM\_USBDevice**</span></span>](cim-usbdevice.md)
</dt> <dd>

<span data-ttu-id="fde4c-749">La clase [**CIM \_ USBDevice**](cim-usbdevice.md) representa las características de administración de un dispositivo USB.</span><span class="sxs-lookup"><span data-stu-id="fde4c-749">The [**CIM\_USBDevice**](cim-usbdevice.md) class represents the management characteristics of a USB device.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-750">**USBHub de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="fde4c-750">**CIM\_USBHub**</span></span>](cim-usbhub.md)
</dt> <dd>

<span data-ttu-id="fde4c-751">La clase de [**\_ USBHub de CIM**](cim-usbhub.md) representa las capacidades y la administración de un concentrador USB.</span><span class="sxs-lookup"><span data-stu-id="fde4c-751">The [**CIM\_USBHub**](cim-usbhub.md) class represents the capabilities and management of a USB hub.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-752">**\_USERDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-752">**CIM\_UserDevice**</span></span>](cim-userdevice.md)
</dt> <dd>

<span data-ttu-id="fde4c-753">La clase [**CIM \_ UserDevice**](cim-userdevice.md) es una clase primaria de la que otras clases, como [**el \_ teclado CIM**](cim-keyboard.md) o [**\_ DesktopMonitor CIM**](cim-desktopmonitor.md), descienden.</span><span class="sxs-lookup"><span data-stu-id="fde4c-753">The [**CIM\_UserDevice**](cim-userdevice.md) class is a parent class from which other classes, such as [**CIM\_Keyboard**](cim-keyboard.md) or [**CIM\_DesktopMonitor**](cim-desktopmonitor.md), descend.</span></span> <span data-ttu-id="fde4c-754">Los dispositivos de usuario son dispositivos lógicos que permiten al usuario del equipo escribir, ver o oír datos.</span><span class="sxs-lookup"><span data-stu-id="fde4c-754">User devices are logical devices that allow a computer system's user to input, view, or hear data.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-755">**\_VERSIONCOMPATIBILITYCHECK CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-755">**CIM\_VersionCompatibilityCheck**</span></span>](cim-versioncompatibilitycheck.md)
</dt> <dd>

<span data-ttu-id="fde4c-756">La clase [**CIM \_ VersionCompatibilityCheck**](cim-versioncompatibilitycheck.md) especifica si se permite crear el siguiente estado de un elemento de software.</span><span class="sxs-lookup"><span data-stu-id="fde4c-756">The [**CIM\_VersionCompatibilityCheck**](cim-versioncompatibilitycheck.md) class specifies whether it is permissible to create the next state of a software element.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-757">**\_VIDEOBIOSELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-757">**CIM\_VideoBIOSElement**</span></span>](cim-videobioselement.md)
</dt> <dd>

<span data-ttu-id="fde4c-758">La clase [**CIM \_ VideoBIOSElement**](cim-videobioselement.md) representa el software de bajo nivel que se carga en el almacenamiento no volátil y se usa para configurar y tener acceso al controlador de vídeo de un equipo y mostrarlo.</span><span class="sxs-lookup"><span data-stu-id="fde4c-758">The [**CIM\_VideoBIOSElement**](cim-videobioselement.md) class represents the low-level software that is loaded into non-volatile storage and used to configure and access a computer system's video controller and display.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-759">**\_VIDEOBIOSFEATURE CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-759">**CIM\_VideoBIOSFeature**</span></span>](cim-videobiosfeature.md)
</dt> <dd>

<span data-ttu-id="fde4c-760">La clase [**CIM \_ VideoBIOSFeature**](cim-videobiosfeature.md) representa las capacidades del software de bajo nivel que se usa para configurar y tener acceso al controlador de vídeo de un equipo y mostrarlo.</span><span class="sxs-lookup"><span data-stu-id="fde4c-760">The [**CIM\_VideoBIOSFeature**](cim-videobiosfeature.md) class represents the capabilities of the low-level software used to configure and access a computer system's video controller and display.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-761">**\_VIDEOBIOSFEATUREVIDEOBIOSELEMENTS CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-761">**CIM\_VideoBIOSFeatureVideoBIOSElements**</span></span>](cim-videobiosfeaturevideobioselements.md)
</dt> <dd>

<span data-ttu-id="fde4c-762">La [**clase \_ VideoBIOSFeatureVideoBIOSElements de CIM**](cim-videobiosfeaturevideobioselements.md) asocia una característica de BIOS de vídeo y sus elementos de BIOS de vídeo agregados.</span><span class="sxs-lookup"><span data-stu-id="fde4c-762">The [**CIM\_VideoBIOSFeatureVideoBIOSElements**](cim-videobiosfeaturevideobioselements.md) class associates a video BIOS feature and its aggregated video BIOS elements.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-763">**\_Videocontroladora CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-763">**CIM\_VideoController**</span></span>](cim-videocontroller.md)
</dt> <dd>

<span data-ttu-id="fde4c-764">La clase de [**\_ videocontroladora CIM**](cim-videocontroller.md) representa las capacidades y la administración del controlador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="fde4c-764">The [**CIM\_VideoController**](cim-videocontroller.md) class represents the capabilities and management of the video controller.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-765">**\_VIDEOCONTROLLERRESOLUTION CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-765">**CIM\_VideoControllerResolution**</span></span>](cim-videocontrollerresolution.md)
</dt> <dd>

<span data-ttu-id="fde4c-766">La clase [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md) representa los distintos modos de vídeo que puede admitir un controlador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="fde4c-766">The [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md) class represents the various video modes that a video controller can support.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-767">**Videoconfiguración de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="fde4c-767">**CIM\_VideoSetting**</span></span>](cim-videosetting.md)
</dt> <dd>

<span data-ttu-id="fde4c-768">La clase de [**\_ videoconfiguración de CIM**](cim-videosetting.md) asocia el objeto de configuración [**\_ VideoControllerResolution de CIM**](cim-videocontrollerresolution.md) con el controlador al que se aplica.</span><span class="sxs-lookup"><span data-stu-id="fde4c-768">The [**CIM\_VideoSetting**](cim-videosetting.md) class associates the [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md) setting object with the controller to which it applies.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-769">**\_VOLATILESTORAGE CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-769">**CIM\_VolatileStorage**</span></span>](cim-volatilestorage.md)
</dt> <dd>

<span data-ttu-id="fde4c-770">La clase [**CIM \_ VolatileStorage**](cim-volatilestorage.md) representa las capacidades y la administración del almacenamiento volátil.</span><span class="sxs-lookup"><span data-stu-id="fde4c-770">The [**CIM\_VolatileStorage**](cim-volatilestorage.md) class represents the capabilities and management of volatile storage.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-771">**\_VOLTAGESENSOR CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-771">**CIM\_VoltageSensor**</span></span>](cim-voltagesensor.md)
</dt> <dd>

<span data-ttu-id="fde4c-772">La [**clase \_ VoltageSensor de CIM**](cim-voltagesensor.md) existe para la compatibilidad con versiones anteriores con las definiciones de esquema CIM anteriores.</span><span class="sxs-lookup"><span data-stu-id="fde4c-772">The [**CIM\_VoltageSensor**](cim-voltagesensor.md) class exists for backward compatibility to earlier CIM schema definitions.</span></span> <span data-ttu-id="fde4c-773">Con las adiciones al [**\_ sensor CIM**](cim-sensor.md) y las clases de [**CIM \_ NumericSensor**](cim-numericsensor.md) en la versión 2,2, ya no es necesario.</span><span class="sxs-lookup"><span data-stu-id="fde4c-773">With additions to the [**CIM\_Sensor**](cim-sensor.md) and [**CIM\_NumericSensor**](cim-numericsensor.md) classes in version 2.2, it is no longer necessary.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-774">**\_VOLUMESET CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-774">**CIM\_VolumeSet**</span></span>](cim-volumeset.md)
</dt> <dd>

<span data-ttu-id="fde4c-775">La clase [**CIM \_ VolumeSet**](cim-volumeset.md) representa un intervalo contiguo de bloques lógicos que se presentan al entorno operativo para leer y escribir datos de usuario.</span><span class="sxs-lookup"><span data-stu-id="fde4c-775">The [**CIM\_VolumeSet**](cim-volumeset.md) class represents a contiguous range of logical blocks presented to the operating environment for reading and writing user data.</span></span>

</dd> <dt>

[<span data-ttu-id="fde4c-776">**\_WORMDRIVE CIM**</span><span class="sxs-lookup"><span data-stu-id="fde4c-776">**CIM\_WORMDrive**</span></span>](cim-wormdrive.md)
</dt> <dd>

<span data-ttu-id="fde4c-777">La clase [**CIM \_ WORMDrive**](cim-wormdrive.md) representa las capacidades y la administración de una unidad Worm, un subtipo del dispositivo de acceso a medios.</span><span class="sxs-lookup"><span data-stu-id="fde4c-777">The [**CIM\_WORMDrive**](cim-wormdrive.md) class represents the capabilities and management of a WORM drive, a subtype of the media access device.</span></span>

</dd> </dl>

 

 
