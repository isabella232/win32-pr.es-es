---
description: '\_La indicación CIM es la clase base abstracta para todas las notificaciones sobre los cambios en los objetos de esquema y los datos de objetos de esquema, eventos detectados por proveedores e instrumentación. Las subclases de la \_ indicación CIM representan tipos específicos de notificaciones.'
ms.assetid: 85a70425-7b32-449c-9fc0-1cfbf34d9187
title: CIM_Indication (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Indication
- CIM_Indication.IndicationIdentifier
- CIM_Indication.CorrelatedIndications
- CIM_Indication.IndicationTime
- CIM_Indication.PerceivedSeverity
- CIM_Indication.OtherSeverity
- CIM_Indication.IndicationFilterName
- CIM_Indication.SequenceContext
- CIM_Indication.SequenceNumber
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 46b8d50f2e90d9a51c8ffa0b93de9ac16c889340
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687402"
---
# <a name="cim_indication-class"></a><span data-ttu-id="f54bf-104">\_Clase de indicación CIM</span><span class="sxs-lookup"><span data-stu-id="f54bf-104">CIM\_Indication class</span></span>

<span data-ttu-id="f54bf-105">**CIM \_ La indicación** es la clase base abstracta para todas las notificaciones sobre los cambios en los objetos de esquema y los datos de objetos de esquema, eventos detectados por proveedores e instrumentación.</span><span class="sxs-lookup"><span data-stu-id="f54bf-105">**CIM\_Indication** is the abstract base class for all notifications about changes in schema objects, and schema object data, events detected by providers and instrumentation.</span></span> <span data-ttu-id="f54bf-106">Las subclases de la **\_ indicación CIM** representan tipos específicos de notificaciones.</span><span class="sxs-lookup"><span data-stu-id="f54bf-106">Subclasses of **CIM\_Indication** represent specific types of notifications.</span></span>

## <a name="syntax"></a><span data-ttu-id="f54bf-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f54bf-107">Syntax</span></span>

``` syntax
[Indication, Version("2.24.0"), UMLPackagePath("CIM::Event"), AMENDMENT]
class CIM_Indication : __ExtrinsicEvent
{
  string   IndicationIdentifier;
  string   CorrelatedIndications[];
  datetime IndicationTime;
  uint16   PerceivedSeverity;
  string   OtherSeverity;
  string   IndicationFilterName;
  string   SequenceContext;
  sint64   SequenceNumber;
};
```

## <a name="members"></a><span data-ttu-id="f54bf-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="f54bf-108">Members</span></span>

<span data-ttu-id="f54bf-109">La clase de **\_ indicación CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f54bf-109">The **CIM\_Indication** class has these types of members:</span></span>

-   [<span data-ttu-id="f54bf-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f54bf-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f54bf-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f54bf-111">Properties</span></span>

<span data-ttu-id="f54bf-112">La clase de **\_ indicación CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f54bf-112">The **CIM\_Indication** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f54bf-113">**CorrelatedIndications**</span><span class="sxs-lookup"><span data-stu-id="f54bf-113">**CorrelatedIndications**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f54bf-114">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="f54bf-114">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f54bf-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f54bf-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f54bf-116">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("RECOMMENDATION. itu \| X733. Notificaciones correlacionadas "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ indicación de CIM**.**IndicationIdentifier**")</span><span class="sxs-lookup"><span data-stu-id="f54bf-116">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Correlated notifications"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Indication**.**IndicationIdentifier**")</span></span>
</dt> </dl>

<span data-ttu-id="f54bf-117">Una matriz que contiene los valores de **IndicationIdentifier** de las notificaciones que están relacionadas con este.</span><span class="sxs-lookup"><span data-stu-id="f54bf-117">A array that contains **IndicationIdentifier** values of notifications that are related this one.</span></span>

</dd> <dt>

<span data-ttu-id="f54bf-118">**IndicationFilterName**</span><span class="sxs-lookup"><span data-stu-id="f54bf-118">**IndicationFilterName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f54bf-119">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f54bf-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f54bf-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f54bf-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f54bf-121">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ IndicationFilter.Name")</span><span class="sxs-lookup"><span data-stu-id="f54bf-121">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_IndicationFilter.Name")</span></span>
</dt> </dl>

<span data-ttu-id="f54bf-122">Identificador del filtro de indicación que procesa la indicación.</span><span class="sxs-lookup"><span data-stu-id="f54bf-122">The identifier of the indication filter that processes the indication.</span></span> <span data-ttu-id="f54bf-123">El servicio de envío establece esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="f54bf-123">The sending service sets this property.</span></span> <span data-ttu-id="f54bf-124">Esta propiedad se correlaciona con la propiedad **Name** del objeto **CIM \_ IndicationFilter** .</span><span class="sxs-lookup"><span data-stu-id="f54bf-124">This property correlates with the **Name** property of the **CIM\_IndicationFilter** object.</span></span> <span data-ttu-id="f54bf-125">El valor de **IndicationFilterName** debe tener el formato siguiente:</span><span class="sxs-lookup"><span data-stu-id="f54bf-125">The value of **IndicationFilterName** should use the following format:</span></span>

-   <span data-ttu-id="f54bf-126">*<OrgID>*:*<LocalID>*</span><span class="sxs-lookup"><span data-stu-id="f54bf-126">*<OrgID>*:*<LocalID>*</span></span>
-   <span data-ttu-id="f54bf-127">*<OrgID>* debe incluir un nombre con copyright, marca registrada o único que sea propiedad de la entidad empresarial a la que pertenece el objeto.</span><span class="sxs-lookup"><span data-stu-id="f54bf-127">*<OrgID>* must include a copyrighted, trademarked, or unique name that is owned by the business entity that owns the object.</span></span>
-   <span data-ttu-id="f54bf-128">*<OrgID>* no debe contener dos puntos (:)</span><span class="sxs-lookup"><span data-stu-id="f54bf-128">*<OrgID>* must not contain a colon (:)</span></span>
-   <span data-ttu-id="f54bf-129">*<LocalID>* identificador único elegido por la entidad comercial que posee el objeto.</span><span class="sxs-lookup"><span data-stu-id="f54bf-129">*<LocalID>* a unique identifier chosen by the business entity that owns the object.</span></span>

</dd> <dt>

<span data-ttu-id="f54bf-130">**IndicationIdentifier**</span><span class="sxs-lookup"><span data-stu-id="f54bf-130">**IndicationIdentifier**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f54bf-131">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f54bf-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f54bf-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f54bf-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f54bf-133">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("RECOMMENDATION. itu \| X733. Identificador de notificación ")</span><span class="sxs-lookup"><span data-stu-id="f54bf-133">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Notification identifier")</span></span>
</dt> </dl>

<span data-ttu-id="f54bf-134">Identificador de la indicación.</span><span class="sxs-lookup"><span data-stu-id="f54bf-134">An identifier of the indication.</span></span> <span data-ttu-id="f54bf-135">Esta propiedad se puede utilizar como un valor de clave en la matriz de propiedades **CorrelatedIndications** .</span><span class="sxs-lookup"><span data-stu-id="f54bf-135">This property can be used as a key value in the **CorrelatedIndications** property array.</span></span> <span data-ttu-id="f54bf-136">Por lo tanto, **IndicationIdentifier** debe ser un valor único dentro del espacio de nombres de esta instancia de clase.</span><span class="sxs-lookup"><span data-stu-id="f54bf-136">Therefore, **IndicationIdentifier** should be a unique value within the namespace of this class instance.</span></span>

<span data-ttu-id="f54bf-137">Para asegurarse de que **IndicationIdentifier** sea único, debe usar el siguiente formato:</span><span class="sxs-lookup"><span data-stu-id="f54bf-137">To ensure that **IndicationIdentifier** is unique, it should use the following format:</span></span>

-   <span data-ttu-id="f54bf-138">*<OrgID>*:*<LocalID>*</span><span class="sxs-lookup"><span data-stu-id="f54bf-138">*<OrgID>*:*<LocalID>*</span></span>
-   <span data-ttu-id="f54bf-139">*<OrgID>* debe incluir un nombre con copyright, marca registrada o único que sea propiedad de la entidad empresarial a la que pertenece el objeto.</span><span class="sxs-lookup"><span data-stu-id="f54bf-139">*<OrgID>* must include a copyrighted, trademarked, or unique name that is owned by the business entity that owns the object.</span></span>
-   <span data-ttu-id="f54bf-140">*<OrgID>* no debe contener dos puntos (:)</span><span class="sxs-lookup"><span data-stu-id="f54bf-140">*<OrgID>* must not contain a colon (:)</span></span>
-   <span data-ttu-id="f54bf-141">*<LocalID>* identificador único elegido por la entidad comercial que posee el objeto.</span><span class="sxs-lookup"><span data-stu-id="f54bf-141">*<LocalID>* a unique identifier chosen by the business entity that owns the object.</span></span>
-   <span data-ttu-id="f54bf-142">En el caso de las instancias definidas por DMTF, *<OrgID>* debe establecerse en "CIM".</span><span class="sxs-lookup"><span data-stu-id="f54bf-142">For DMTF-defined instances, *<OrgID>* should be set to "CIM".</span></span>

</dd> <dt>

<span data-ttu-id="f54bf-143">**IndicationTime**</span><span class="sxs-lookup"><span data-stu-id="f54bf-143">**IndicationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f54bf-144">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f54bf-144">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f54bf-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f54bf-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f54bf-146">Fecha y hora en que se creó la indicación.</span><span class="sxs-lookup"><span data-stu-id="f54bf-146">The time and date when the indication was created.</span></span> <span data-ttu-id="f54bf-147">La propiedad se puede establecer en **null** si la entidad que creó la indicación no es capaz de determinar esta información.</span><span class="sxs-lookup"><span data-stu-id="f54bf-147">The property can be set to **NULL** if the entity that created the indication is not capable of determining this information.</span></span>

> [!Note]  
> <span data-ttu-id="f54bf-148">El valor de **IndicationTime** puede ser el mismo para las indicaciones que se generan en una sucesión rápida.</span><span class="sxs-lookup"><span data-stu-id="f54bf-148">The **IndicationTime** value can be the same for indications that are generated in rapid succession.</span></span>

 

</dd> <dt>

<span data-ttu-id="f54bf-149">**OtherSeverity**</span><span class="sxs-lookup"><span data-stu-id="f54bf-149">**OtherSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f54bf-150">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f54bf-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f54bf-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f54bf-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f54bf-152">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ AlertIndication**](cim-alertindication.md).**PerceivedSeverity**")</span><span class="sxs-lookup"><span data-stu-id="f54bf-152">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_AlertIndication**](cim-alertindication.md).**PerceivedSeverity**")</span></span>
</dt> </dl>

<span data-ttu-id="f54bf-153">La gravedad de la indicación del punto de vista del notificador cuando **PerceivedSeverity** se establece en "1" (otro).</span><span class="sxs-lookup"><span data-stu-id="f54bf-153">The severity of the indication from the notifier's point of view when **PerceivedSeverity** is set to "1" (Other).</span></span>

</dd> <dt>

<span data-ttu-id="f54bf-154">**PerceivedSeverity**</span><span class="sxs-lookup"><span data-stu-id="f54bf-154">**PerceivedSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f54bf-155">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f54bf-155">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f54bf-156">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f54bf-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f54bf-157">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("RECOMMENDATION. itu \| X733. Gravedad percibida ")</span><span class="sxs-lookup"><span data-stu-id="f54bf-157">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Perceived severity")</span></span>
</dt> </dl>

<span data-ttu-id="f54bf-158">La gravedad de la indicación del punto de vista del notificador.</span><span class="sxs-lookup"><span data-stu-id="f54bf-158">The severity of the indication from the notifier's point of view.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f54bf-159"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="f54bf-159"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="f54bf-160">la gravedad percibida de la indicación es desconocida o indeterminada.</span><span class="sxs-lookup"><span data-stu-id="f54bf-160">the Perceived Severity of the indication is unknown or indeterminate.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f54bf-161"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="f54bf-161"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f54bf-162">Indica que el valor de la gravedad se puede encontrar en la propiedad **OtherSeverity** .</span><span class="sxs-lookup"><span data-stu-id="f54bf-162">Indicates that the Severity's value can be found in the **OtherSeverity** property.</span></span>

</dd> <dt>

<span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>

<span data-ttu-id="f54bf-163"><span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Información** (2)</span><span class="sxs-lookup"><span data-stu-id="f54bf-163"><span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Information** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f54bf-164">La información se debe utilizar al proporcionar una respuesta informativa.</span><span class="sxs-lookup"><span data-stu-id="f54bf-164">Information should be used when providing an informative response.</span></span>

</dd> <dt>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>

<span data-ttu-id="f54bf-165"><span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Degradado/ADVERTENCIA** (3)</span><span class="sxs-lookup"><span data-stu-id="f54bf-165"><span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Degraded/Warning** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f54bf-166">Debe usarse cuando sea adecuado para permitir que el usuario decida si es necesario realizar alguna acción.</span><span class="sxs-lookup"><span data-stu-id="f54bf-166">Should be used when its appropriate to let the user decide if action is needed.</span></span>

</dd> <dt>

<span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>

<span data-ttu-id="f54bf-167"><span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>**Secundaria** (4)</span><span class="sxs-lookup"><span data-stu-id="f54bf-167"><span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>**Minor** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f54bf-168">La acción es necesaria, pero la situación no es seria en este momento.</span><span class="sxs-lookup"><span data-stu-id="f54bf-168">Action is needed, but the situation is not serious at this time.</span></span>

</dd> <dt>

<span id="Major"></span><span id="major"></span><span id="MAJOR"></span>

<span data-ttu-id="f54bf-169"><span id="Major"></span><span id="major"></span><span id="MAJOR"></span>**Principal** (5)</span><span class="sxs-lookup"><span data-stu-id="f54bf-169"><span id="Major"></span><span id="major"></span><span id="MAJOR"></span>**Major** (5)</span></span>


</dt> <dd>

<span data-ttu-id="f54bf-170">La acción es necesaria ahora.</span><span class="sxs-lookup"><span data-stu-id="f54bf-170">Action is needed NOW.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="f54bf-171"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Crítico** (6)</span><span class="sxs-lookup"><span data-stu-id="f54bf-171"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (6)</span></span>


</dt> <dd>

<span data-ttu-id="f54bf-172">La acción es necesaria ahora y el ámbito es amplio (es posible que se produzca una interrupción inminente en un recurso crítico).</span><span class="sxs-lookup"><span data-stu-id="f54bf-172">Action is needed NOW and the scope is broad (perhaps an imminent outage to a critical resource will result).</span></span>

</dd> <dt>

<span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>

<span data-ttu-id="f54bf-173"><span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>**Irrecuperable/no recuperable** (7)</span><span class="sxs-lookup"><span data-stu-id="f54bf-173"><span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>**Fatal/NonRecoverable** (7)</span></span>


</dt> <dd>

<span data-ttu-id="f54bf-174">se produjo un error, pero es demasiado tarde para tomar medidas correctivas.</span><span class="sxs-lookup"><span data-stu-id="f54bf-174">an error occurred, but it's too late to take remedial action.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="f54bf-175"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="f54bf-175"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f54bf-176">**SequenceContext**</span><span class="sxs-lookup"><span data-stu-id="f54bf-176">**SequenceContext**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f54bf-177">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f54bf-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f54bf-178">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f54bf-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f54bf-179">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ indicación CIM**.**SequenceNumber**")</span><span class="sxs-lookup"><span data-stu-id="f54bf-179">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Indication**.**SequenceNumber**")</span></span>
</dt> </dl>

<span data-ttu-id="f54bf-180">El contexto de secuencia del identificador de secuencia para la indicación.</span><span class="sxs-lookup"><span data-stu-id="f54bf-180">The sequence context of the sequence identifier for the indication.</span></span> <span data-ttu-id="f54bf-181">Si un servicio no admite identificadores de secuencia para las indicaciones, esta propiedad debe establecerse en **null**.</span><span class="sxs-lookup"><span data-stu-id="f54bf-181">If a service does not support sequence identifiers for indications, this property should be set to **NULL**.</span></span> <span data-ttu-id="f54bf-182">Si se vuelve a entregar la indicación, esta propiedad sigue siendo la misma.</span><span class="sxs-lookup"><span data-stu-id="f54bf-182">If the indication is redelivered, this property remains the same.</span></span>

> [!Note]  
> <span data-ttu-id="f54bf-183">El identificador de secuencia de la indicación permite a un agente de escucha identificar las indicaciones duplicadas cuando el servicio intenta volver a ofrecer indicaciones, reordenar las indicaciones que llegan desordenadas y detectar las indicaciones perdidas.</span><span class="sxs-lookup"><span data-stu-id="f54bf-183">The sequence identifier for the indication enables a listener to identify duplicate indications when the service attempts to redeliver indications, reorder indications that arrive out of order, and detect lost indications.</span></span>

 

<span data-ttu-id="f54bf-184">Para asegurarse de que **SequenceContext** sea único, debe usar el siguiente formato:</span><span class="sxs-lookup"><span data-stu-id="f54bf-184">To ensure that **SequenceContext** is unique, it should use the following format:</span></span>

-   <span data-ttu-id="f54bf-185">*indicación-nombre* \# de servicio *CIM-Service-Start-ID* \# *agente de escucha-destino-creación-hora*</span><span class="sxs-lookup"><span data-stu-id="f54bf-185">*indication-service-name*\#*cim-service-start-id* \#*listener-destination-creation-time*</span></span>
-   <span data-ttu-id="f54bf-186">*indica-Service-Name* es el valor de la propiedad **Name** de la instancia de **\_ IndicationService de CIM** que entrega la indicación.</span><span class="sxs-lookup"><span data-stu-id="f54bf-186">*indication-service-name* is the value of the **Name** property of the **CIM\_IndicationService** instance that delivers the indication.</span></span>
-   <span data-ttu-id="f54bf-187">*CIM-Service-Start-ID* es un identificador que identifica de forma única la operación de inicio de un servicio.</span><span class="sxs-lookup"><span data-stu-id="f54bf-187">*cim-service-start-id* is an identifier that uniquely identifies the start operation of a service.</span></span> <span data-ttu-id="f54bf-188">Por ejemplo, podría ser una marca de tiempo de la hora de inicio o un contador que aumente para cada inicio o reinicio del servicio.</span><span class="sxs-lookup"><span data-stu-id="f54bf-188">For example, this could be a timestamp of the start time, or a counter that increases for each start or restart of the service.</span></span>
-   <span data-ttu-id="f54bf-189">*Listener-Destination-Creation-time* es una marca de tiempo de la hora de creación de la instancia de **\_ ListenerDestination de CIM** que representa el destino del agente de escucha. nSince este formato es solo una recomendación, los clientes CIM tratarán el valor como un identificador opaco para el contexto de secuencia y no se basarán en este formato.</span><span class="sxs-lookup"><span data-stu-id="f54bf-189">*listener-destination-creation-time* is a timestamp of the creation time of the **CIM\_ListenerDestination** instance representing the listener destination.nSince this format is only a recommendation, CIM clients shall treat the value as an opaque identifier for the sequence context and shall not rely on this format.</span></span>

</dd> <dt>

<span data-ttu-id="f54bf-190">**SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="f54bf-190">**SequenceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f54bf-191">Tipo de datos: **sint64**</span><span class="sxs-lookup"><span data-stu-id="f54bf-191">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="f54bf-192">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f54bf-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f54bf-193">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ indicación CIM**.**SequenceContext**")</span><span class="sxs-lookup"><span data-stu-id="f54bf-193">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Indication**.**SequenceContext**")</span></span>
</dt> </dl>

<span data-ttu-id="f54bf-194">El número de secuencia del identificador de secuencia para la indicación.</span><span class="sxs-lookup"><span data-stu-id="f54bf-194">The sequence number of the sequence identifier for the indication.</span></span>

> [!Note]  
> <span data-ttu-id="f54bf-195">El identificador de secuencia de la indicación permite a un agente de escucha identificar las indicaciones duplicadas cuando el servicio intenta volver a ofrecer indicaciones, reordenar las indicaciones que llegan desordenadas y detectar las indicaciones perdidas.</span><span class="sxs-lookup"><span data-stu-id="f54bf-195">The sequence identifier for the indication enables a listener to identify duplicate indications when the service attempts to redeliver indications, reorder indications that arrive out of order, and detect lost indications.</span></span>

 

<span data-ttu-id="f54bf-196">El número de secuencia tiene las siguientes características:</span><span class="sxs-lookup"><span data-stu-id="f54bf-196">The sequence number has the following characteristics:</span></span>

-   <span data-ttu-id="f54bf-197">El número de secuencia se restablece en "0" cada vez que cambia el valor de **SequenceContext** .</span><span class="sxs-lookup"><span data-stu-id="f54bf-197">The sequence number is reset to "0" whenever the **SequenceContext** value changes.</span></span>
-   <span data-ttu-id="f54bf-198">Siempre que el destino del agente de escucha recibe una nueva indicación, el número de secuencia aumenta en "1".</span><span class="sxs-lookup"><span data-stu-id="f54bf-198">Whenever the listener destination receives a new indication, the sequence number is increased by "1".</span></span>
-   <span data-ttu-id="f54bf-199">El número de secuencia se ajusta a "0" cuando se supera el intervalo de valores.</span><span class="sxs-lookup"><span data-stu-id="f54bf-199">The sequence number wraps to "0" when the value range is exceeded.</span></span>
-   <span data-ttu-id="f54bf-200">Si se vuelve a entregar la indicación, **SequenceNumber** sigue siendo el mismo.</span><span class="sxs-lookup"><span data-stu-id="f54bf-200">If the indication is redelivered, the **SequenceNumber** remains the same.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f54bf-201">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f54bf-201">Requirements</span></span>



| <span data-ttu-id="f54bf-202">Requisito</span><span class="sxs-lookup"><span data-stu-id="f54bf-202">Requirement</span></span> | <span data-ttu-id="f54bf-203">Value</span><span class="sxs-lookup"><span data-stu-id="f54bf-203">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f54bf-204">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f54bf-204">Minimum supported client</span></span><br/> | <span data-ttu-id="f54bf-205">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="f54bf-205">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="f54bf-206">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f54bf-206">Minimum supported server</span></span><br/> | <span data-ttu-id="f54bf-207">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="f54bf-207">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="f54bf-208">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f54bf-208">Namespace</span></span><br/>                | <span data-ttu-id="f54bf-209">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="f54bf-209">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f54bf-210">MOF</span><span class="sxs-lookup"><span data-stu-id="f54bf-210">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f54bf-211"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f54bf-211"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f54bf-212">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f54bf-212">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f54bf-213"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f54bf-213"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f54bf-214">Vea también</span><span class="sxs-lookup"><span data-stu-id="f54bf-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f54bf-215">**\_\_ExtrinsicEvent**</span><span class="sxs-lookup"><span data-stu-id="f54bf-215">**\_\_ExtrinsicEvent**</span></span>](/windows/desktop/WmiSdk/--extrinsicevent)
</dt> </dl>

 

