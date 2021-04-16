---
description: Una superclase concreta para las notificaciones de alerta de CIM.
ms.assetid: ec4cf41d-decd-4f21-b805-90db4a61376d
title: CIM_AlertIndication (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AlertIndication
- CIM_AlertIndication.Description
- CIM_AlertIndication.AlertingManagedElement
- CIM_AlertIndication.AlertingElementFormat
- CIM_AlertIndication.OtherAlertingElementFormat
- CIM_AlertIndication.AlertType
- CIM_AlertIndication.OtherAlertType
- CIM_AlertIndication.PerceivedSeverity
- CIM_AlertIndication.ProbableCause
- CIM_AlertIndication.ProbableCauseDescription
- CIM_AlertIndication.Trending
- CIM_AlertIndication.RecommendedActions
- CIM_AlertIndication.EventID
- CIM_AlertIndication.EventTime
- CIM_AlertIndication.SystemCreationClassName
- CIM_AlertIndication.SystemName
- CIM_AlertIndication.ProviderName
- CIM_AlertIndication.Message
- CIM_AlertIndication.MessageArguments
- CIM_AlertIndication.MessageID
- CIM_AlertIndication.OwningEntity
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1a1916705ee696c949dba2a557f7077ade8db7ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686518"
---
# <a name="cim_alertindication-class"></a><span data-ttu-id="2403e-103">\_Clase AlertIndication de CIM</span><span class="sxs-lookup"><span data-stu-id="2403e-103">CIM\_AlertIndication class</span></span>

<span data-ttu-id="2403e-104">Una superclase concreta para las notificaciones de alerta de CIM.</span><span class="sxs-lookup"><span data-stu-id="2403e-104">A concrete superclass for CIM alert notifications.</span></span> <span data-ttu-id="2403e-105">**CIM \_ AlertIndication** es un tipo especializado de clase de **\_ indicación CIM** que contiene información sobre la gravedad, la causa, las acciones recomendadas y otros datos para un evento del mundo real.</span><span class="sxs-lookup"><span data-stu-id="2403e-105">**CIM\_AlertIndication** is a specialized type of **CIM\_Indication** class that contains information about the severity, cause, recommended actions, and other data for a real world event.</span></span> <span data-ttu-id="2403e-106">Este evento y sus datos pueden modelarse o no en la jerarquía de clases CIM.</span><span class="sxs-lookup"><span data-stu-id="2403e-106">This event and its data may or may not be modeled in the CIM class hierarchy.</span></span>

## <a name="syntax"></a><span data-ttu-id="2403e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2403e-107">Syntax</span></span>

``` syntax
[Indication, Version("2.22.0"), UMLPackagePath("CIM::Event"), AMENDMENT]
class CIM_AlertIndication : CIM_ProcessIndication
{
  string   Description;
  string   AlertingManagedElement;
  uint16   AlertingElementFormat = 0;
  string   OtherAlertingElementFormat;
  uint16   AlertType;
  string   OtherAlertType;
  uint16   PerceivedSeverity;
  uint16   ProbableCause;
  string   ProbableCauseDescription;
  uint16   Trending;
  string   RecommendedActions[];
  string   EventID;
  datetime EventTime;
  string   SystemCreationClassName;
  string   SystemName;
  string   ProviderName;
  string   Message;
  string   MessageArguments[];
  string   MessageID;
  string   OwningEntity;
};
```

## <a name="members"></a><span data-ttu-id="2403e-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="2403e-108">Members</span></span>

<span data-ttu-id="2403e-109">La clase **CIM \_ AlertIndication** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2403e-109">The **CIM\_AlertIndication** class has these types of members:</span></span>

-   [<span data-ttu-id="2403e-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2403e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2403e-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2403e-111">Properties</span></span>

<span data-ttu-id="2403e-112">La clase **CIM \_ AlertIndication** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="2403e-112">The **CIM\_AlertIndication** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2403e-113">**AlertingElementFormat**</span><span class="sxs-lookup"><span data-stu-id="2403e-113">**AlertingElementFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2403e-114">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2403e-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2403e-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2403e-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2403e-116">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**.**AlertingManagedElement**","**\_ AlertIndication CIM**.**OtherAlertingElementFormat**")</span><span class="sxs-lookup"><span data-stu-id="2403e-116">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**AlertingManagedElement**", "**CIM\_AlertIndication**.**OtherAlertingElementFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="2403e-117">Formato de la propiedad **AlertingManagedElement** .</span><span class="sxs-lookup"><span data-stu-id="2403e-117">The format of the **AlertingManagedElement** property.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2403e-118"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="2403e-118"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="2403e-119">Una aplicación cliente CIM no reconoce el formato o lo interpreta de forma significativa.</span><span class="sxs-lookup"><span data-stu-id="2403e-119">The format is unknown or not meaningfully interpretable by a CIM client application.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2403e-120"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="2403e-120"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="2403e-121">El formato se define mediante el valor de la propiedad OtherAlertingElementFormat.</span><span class="sxs-lookup"><span data-stu-id="2403e-121">The format is defined by the value of the OtherAlertingElementFormat property.</span></span>

</dd> <dt>

<span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>

<span data-ttu-id="2403e-122"><span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>**CIMObjectPath** (2)</span><span class="sxs-lookup"><span data-stu-id="2403e-122"><span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>**CIMObjectPath** (2)</span></span>


</dt> <dd>

<span data-ttu-id="2403e-123">El formato es CIMObjectPath, especificando una instancia en el esquema CIM.</span><span class="sxs-lookup"><span data-stu-id="2403e-123">The format is a CIMObjectPath, specifying an instance in the CIM Schema.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2403e-124">**AlertingManagedElement**</span><span class="sxs-lookup"><span data-stu-id="2403e-124">**AlertingManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2403e-125">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2403e-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2403e-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2403e-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2403e-127">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**.**AlertingElementFormat**")</span><span class="sxs-lookup"><span data-stu-id="2403e-127">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**AlertingElementFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="2403e-128">La información de identificación de la entidad (es decir, la instancia) para la que se genera esta indicación.</span><span class="sxs-lookup"><span data-stu-id="2403e-128">The identifying information of the entity (ie, the instance) for which this Indication is generated.</span></span> <span data-ttu-id="2403e-129">La propiedad contiene la ruta de acceso de una instancia, codificada como un parámetro de cadena, si la instancia se modela en el esquema CIM.</span><span class="sxs-lookup"><span data-stu-id="2403e-129">The property contains the path of an instance, encoded as a string parameter - if the instance is modeled in the CIM Schema.</span></span> <span data-ttu-id="2403e-130">Si no es una instancia de CIM, la propiedad contiene alguna cadena de identificación que nombra la entidad para la que se genera la alerta.</span><span class="sxs-lookup"><span data-stu-id="2403e-130">If not a CIM instance, the property contains some identifying string that names the entity for which the Alert is generated.</span></span> <span data-ttu-id="2403e-131">Se da formato a la ruta de acceso o a la cadena de identificación según la propiedad AlertingElementFormat.</span><span class="sxs-lookup"><span data-stu-id="2403e-131">The path or identifying string is formatted per the AlertingElementFormat property.</span></span>

</dd> <dt>

<span data-ttu-id="2403e-132">**AlertType**</span><span class="sxs-lookup"><span data-stu-id="2403e-132">**AlertType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2403e-133">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2403e-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2403e-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2403e-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2403e-135">Calificadores: [**required**](/windows/desktop/WmiSdk/standard-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("recommendation. itu \| X733. Tipo de evento ")</span><span class="sxs-lookup"><span data-stu-id="2403e-135">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Event type")</span></span>
</dt> </dl>

<span data-ttu-id="2403e-136">La clasificación principal de la indicación.</span><span class="sxs-lookup"><span data-stu-id="2403e-136">The primary classification of the indication.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2403e-137"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="2403e-137"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="2403e-138">\- Distinta.</span><span class="sxs-lookup"><span data-stu-id="2403e-138">\- Other.</span></span> <span data-ttu-id="2403e-139">La propiedad OtherAlertType de la indicación transmite su clasificación.</span><span class="sxs-lookup"><span data-stu-id="2403e-139">The Indication's OtherAlertType property conveys its classification.</span></span> <span data-ttu-id="2403e-140">El uso de "Other" en una enumeración es una convención estándar de CIM.</span><span class="sxs-lookup"><span data-stu-id="2403e-140">Use of "Other" in an enumeration is a standard CIM convention.</span></span> <span data-ttu-id="2403e-141">Significa que la indicación actual no se ajusta a las categorías descritas por esta enumeración.</span><span class="sxs-lookup"><span data-stu-id="2403e-141">It means that the current Indication does not fit into the categories described by this enumeration.</span></span>

</dd> <dt>

<span id="Communications_Alert"></span><span id="communications_alert"></span><span id="COMMUNICATIONS_ALERT"></span>

<span data-ttu-id="2403e-142"><span id="Communications_Alert"></span><span id="communications_alert"></span><span id="COMMUNICATIONS_ALERT"></span>**Alerta de comunicaciones** (2)</span><span class="sxs-lookup"><span data-stu-id="2403e-142"><span id="Communications_Alert"></span><span id="communications_alert"></span><span id="COMMUNICATIONS_ALERT"></span>**Communications Alert** (2)</span></span>


</dt> <dd>

<span data-ttu-id="2403e-143">Una indicación de este tipo está asociada principalmente a los procedimientos y/o procesos necesarios para transmitir información de un punto a otro.</span><span class="sxs-lookup"><span data-stu-id="2403e-143">An Indication of this type is principally associated with the procedures and/or processes required to convey information from one point to another.</span></span>

</dd> <dt>

<span id="Quality_of_Service_Alert"></span><span id="quality_of_service_alert"></span><span id="QUALITY_OF_SERVICE_ALERT"></span>

<span data-ttu-id="2403e-144"><span id="Quality_of_Service_Alert"></span><span id="quality_of_service_alert"></span><span id="QUALITY_OF_SERVICE_ALERT"></span>**Alerta de calidad de servicio** (3)</span><span class="sxs-lookup"><span data-stu-id="2403e-144"><span id="Quality_of_Service_Alert"></span><span id="quality_of_service_alert"></span><span id="QUALITY_OF_SERVICE_ALERT"></span>**Quality of Service Alert** (3)</span></span>


</dt> <dd>

<span data-ttu-id="2403e-145">Una indicación de este tipo está asociada principalmente a una degradación o errores en el rendimiento o la función de una entidad.</span><span class="sxs-lookup"><span data-stu-id="2403e-145">An Indication of this type is principally associated with a degradation or errors in the performance or function of an entity.</span></span>

</dd> <dt>

<span id="Processing_Error"></span><span id="processing_error"></span><span id="PROCESSING_ERROR"></span>

<span data-ttu-id="2403e-146"><span id="Processing_Error"></span><span id="processing_error"></span><span id="PROCESSING_ERROR"></span>**Error de procesamiento** (4)</span><span class="sxs-lookup"><span data-stu-id="2403e-146"><span id="Processing_Error"></span><span id="processing_error"></span><span id="PROCESSING_ERROR"></span>**Processing Error** (4)</span></span>


</dt> <dd>

<span data-ttu-id="2403e-147">Una indicación de este tipo está asociada principalmente a un error de software o de procesamiento.</span><span class="sxs-lookup"><span data-stu-id="2403e-147">An Indication of this type is principally associated with a software or processing fault.</span></span>

</dd> <dt>

<span id="Device_Alert"></span><span id="device_alert"></span><span id="DEVICE_ALERT"></span>

<span data-ttu-id="2403e-148"><span id="Device_Alert"></span><span id="device_alert"></span><span id="DEVICE_ALERT"></span>**Alerta de dispositivo** (5)</span><span class="sxs-lookup"><span data-stu-id="2403e-148"><span id="Device_Alert"></span><span id="device_alert"></span><span id="DEVICE_ALERT"></span>**Device Alert** (5)</span></span>


</dt> <dd>

<span data-ttu-id="2403e-149">Una indicación de este tipo está asociada principalmente a un error de equipo o de hardware.</span><span class="sxs-lookup"><span data-stu-id="2403e-149">An Indication of this type is principally associated with an equipment or hardware fault.</span></span>

</dd> <dt>

<span id="Environmental_Alert"></span><span id="environmental_alert"></span><span id="ENVIRONMENTAL_ALERT"></span>

<span data-ttu-id="2403e-150"><span id="Environmental_Alert"></span><span id="environmental_alert"></span><span id="ENVIRONMENTAL_ALERT"></span>**Alerta de entorno** (6)</span><span class="sxs-lookup"><span data-stu-id="2403e-150"><span id="Environmental_Alert"></span><span id="environmental_alert"></span><span id="ENVIRONMENTAL_ALERT"></span>**Environmental Alert** (6)</span></span>


</dt> <dd>

<span data-ttu-id="2403e-151">Alerta de entorno.</span><span class="sxs-lookup"><span data-stu-id="2403e-151">Environmental Alert.</span></span> <span data-ttu-id="2403e-152">Una indicación de este tipo está asociada principalmente a una condición relacionada con un contenedor en el que reside el hardware, u otras consideraciones del entorno.</span><span class="sxs-lookup"><span data-stu-id="2403e-152">An Indication of this type is principally associated with a condition relating to an enclosure in which the hardware resides, or other environmental considerations.</span></span>

</dd> <dt>

<span id="Model_Change"></span><span id="model_change"></span><span id="MODEL_CHANGE"></span>

<span data-ttu-id="2403e-153"><span id="Model_Change"></span><span id="model_change"></span><span id="MODEL_CHANGE"></span>**Cambio de modelo** (7)</span><span class="sxs-lookup"><span data-stu-id="2403e-153"><span id="Model_Change"></span><span id="model_change"></span><span id="MODEL_CHANGE"></span>**Model Change** (7)</span></span>


</dt> <dd>

<span data-ttu-id="2403e-154">La indicación trata los cambios en el modelo de información.</span><span class="sxs-lookup"><span data-stu-id="2403e-154">The Indication addresses changes in the Information Model.</span></span> <span data-ttu-id="2403e-155">Por ejemplo, puede insertar una indicación del ciclo de vida para transmitir el cambio de modelo específico que se va a notificar.</span><span class="sxs-lookup"><span data-stu-id="2403e-155">For example, it may embed a Lifecycle Indication to convey the specific model change being alerted.</span></span>

</dd> <dt>

<span id="Security_Alert"></span><span id="security_alert"></span><span id="SECURITY_ALERT"></span>

<span data-ttu-id="2403e-156"><span id="Security_Alert"></span><span id="security_alert"></span><span id="SECURITY_ALERT"></span>**Alerta de seguridad** (8)</span><span class="sxs-lookup"><span data-stu-id="2403e-156"><span id="Security_Alert"></span><span id="security_alert"></span><span id="SECURITY_ALERT"></span>**Security Alert** (8)</span></span>


</dt> <dd>

<span data-ttu-id="2403e-157">.</span><span class="sxs-lookup"><span data-stu-id="2403e-157">.</span></span> <span data-ttu-id="2403e-158">Se ha asociado una indicación de este tipo.</span><span class="sxs-lookup"><span data-stu-id="2403e-158">An Indication of this type is associated.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2403e-159">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2403e-159">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2403e-160">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2403e-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2403e-161">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2403e-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2403e-162">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("RECOMMENDATION. itu \| X733. Texto adicional ")</span><span class="sxs-lookup"><span data-stu-id="2403e-162">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Additional text")</span></span>
</dt> </dl>

<span data-ttu-id="2403e-163">Breve descripción de la indicación.</span><span class="sxs-lookup"><span data-stu-id="2403e-163">A short description of the Indication.</span></span>

</dd> <dt>

<span data-ttu-id="2403e-164">**Id. de evento**</span><span class="sxs-lookup"><span data-stu-id="2403e-164">**EventID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2403e-165">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2403e-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2403e-166">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2403e-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2403e-167">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**.**ProbableCause**")</span><span class="sxs-lookup"><span data-stu-id="2403e-167">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**ProbableCause**")</span></span>
</dt> </dl>

<span data-ttu-id="2403e-168">Un valor específico de instrumentación o proveedor que describe el evento del mundo real subyacente representado por la indicación.</span><span class="sxs-lookup"><span data-stu-id="2403e-168">An instrumentation or provider specific value that describes the underlying real-world event represented by the indication.</span></span> <span data-ttu-id="2403e-169">La entidad de creación tiene en cuenta las indicaciones con el mismo valor **EventID** distinto de null para representar el mismo evento.</span><span class="sxs-lookup"><span data-stu-id="2403e-169">Indications with the same non-NULL **EventID** value are considered, by the creating entity, to represent the same event.</span></span> <span data-ttu-id="2403e-170">La comparación de dos valores **EventID** solo se define para las indicaciones de alerta con valores idénticos no NULL de las propiedades **SystemCreateClassName**, **SystemName** y **providerName** .</span><span class="sxs-lookup"><span data-stu-id="2403e-170">The comparison of two **EventID** values is only defined for alert indications with identical, non-NULL values of **SystemCreateClassName**, **SystemName** and **ProviderName** properties.</span></span>

</dd> <dt>

<span data-ttu-id="2403e-171">**EventTime**</span><span class="sxs-lookup"><span data-stu-id="2403e-171">**EventTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2403e-172">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2403e-172">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2403e-173">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2403e-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2403e-174">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**.**ProbableCause**")</span><span class="sxs-lookup"><span data-stu-id="2403e-174">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**ProbableCause**")</span></span>
</dt> </dl>

<span data-ttu-id="2403e-175">Fecha y hora que indica cuándo se detectó por primera vez el evento subyacente.</span><span class="sxs-lookup"><span data-stu-id="2403e-175">The time and date that indicates when the underlying event was first detected.</span></span> <span data-ttu-id="2403e-176">Si se especifican estos valores y la entidad que crea no es capaz de proporcionar esta información, esta propiedad debe establecerse en **null**.</span><span class="sxs-lookup"><span data-stu-id="2403e-176">If this values is specified and the creating entity is not capable of providing this information, this property must be set to **NULL**.</span></span> <span data-ttu-id="2403e-177">Este valor se basa en la noción de la fecha y hora locales del objeto **CIM \_ ManageSystemElement** que generó la indicación.</span><span class="sxs-lookup"><span data-stu-id="2403e-177">This value is based on the notion of the local date and time of the **CIM\_ManageSystemElement** object that generated the indication.</span></span>

</dd> <dt>

<span data-ttu-id="2403e-178">**Message**</span><span class="sxs-lookup"><span data-stu-id="2403e-178">**Message**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2403e-179">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2403e-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2403e-180">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2403e-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2403e-181">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**.**MessageID**","**CIM \_ AlertIndication**.**MessageArguments**")</span><span class="sxs-lookup"><span data-stu-id="2403e-181">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**MessageID**", "**CIM\_AlertIndication**.**MessageArguments**")</span></span>
</dt> </dl>

<span data-ttu-id="2403e-182">Mensaje con formato para la indicación de alerta.</span><span class="sxs-lookup"><span data-stu-id="2403e-182">The formatted message for the alert indication.</span></span> <span data-ttu-id="2403e-183">Se da formato a este mensaje mediante la combinación de uno o varios de los elementos dinámicos especificados en la propiedad **MessageArguments** y con los elementos estáticos que se identifican de forma única mediante la propiedad **MessageID** .</span><span class="sxs-lookup"><span data-stu-id="2403e-183">This message is formatted by combining one or more of the dynamic elements specified in the **MessageArguments** property, and with the static elements uniquely identified by the **MessageID** property.</span></span>

</dd> <dt>

<span data-ttu-id="2403e-184">**MessageArguments**</span><span class="sxs-lookup"><span data-stu-id="2403e-184">**MessageArguments**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2403e-185">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="2403e-185">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2403e-186">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2403e-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2403e-187">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**.**Mensaje**","**CIM \_ AlertIndication**.**MessageID**")</span><span class="sxs-lookup"><span data-stu-id="2403e-187">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**Message**", "**CIM\_AlertIndication**.**MessageID**")</span></span>
</dt> </dl>

<span data-ttu-id="2403e-188">Una matriz que contiene el contenido dinámico del mensaje para la indicación de alerta.</span><span class="sxs-lookup"><span data-stu-id="2403e-188">An array that contains the dynamic content of the message for the alert indication.</span></span>

</dd> <dt>

<span data-ttu-id="2403e-189">**Identificador**</span><span class="sxs-lookup"><span data-stu-id="2403e-189">**MessageID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2403e-190">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2403e-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2403e-191">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2403e-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2403e-192">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**.**Mensaje**","**CIM \_ AlertIndication**.**MessageArguments**")</span><span class="sxs-lookup"><span data-stu-id="2403e-192">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**Message**", "**CIM\_AlertIndication**.**MessageArguments**")</span></span>
</dt> </dl>

<span data-ttu-id="2403e-193">IDENTIFICADOR único del formato de mensaje, con el ámbito de la organización especificado en **OwningEntity**.</span><span class="sxs-lookup"><span data-stu-id="2403e-193">The unique ID of the message format, withing the scope of the organization specified in **OwningEntity**.</span></span>

</dd> <dt>

<span data-ttu-id="2403e-194">**OtherAlertingElementFormat**</span><span class="sxs-lookup"><span data-stu-id="2403e-194">**OtherAlertingElementFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2403e-195">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2403e-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2403e-196">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2403e-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2403e-197">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**.**AlertingElementFormat**")</span><span class="sxs-lookup"><span data-stu-id="2403e-197">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**AlertingElementFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="2403e-198">Define el formato de la propiedad **AlertingManagedElement** cuando la propiedad **AlertingElementFormat** se establece en "1" (otro); de lo contrario, este valor debe establecerse en **null**.</span><span class="sxs-lookup"><span data-stu-id="2403e-198">Defines the format of the **AlertingManagedElement** property when the **AlertingElementFormat** property is set to "1" (other); otherwise, this value must be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="2403e-199">**OtherAlertType**</span><span class="sxs-lookup"><span data-stu-id="2403e-199">**OtherAlertType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2403e-200">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2403e-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2403e-201">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2403e-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2403e-202">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**.**AlertType**")</span><span class="sxs-lookup"><span data-stu-id="2403e-202">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**AlertType**")</span></span>
</dt> </dl>

<span data-ttu-id="2403e-203">Una cadena que describe el valor **AlertType** cuando la propiedad **AlertType** se establece en "1" (otro cambio de estado).</span><span class="sxs-lookup"><span data-stu-id="2403e-203">A string that describes the **AlertType** value when the **AlertType** property is set to "1" (Other State Change).</span></span>

</dd> <dt>

<span data-ttu-id="2403e-204">**OwningEntity**</span><span class="sxs-lookup"><span data-stu-id="2403e-204">**OwningEntity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2403e-205">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2403e-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2403e-206">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2403e-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2403e-207">IDENTIFICADOR único de la organización a la que pertenece la definición del formato de la propiedad del **mensaje** .</span><span class="sxs-lookup"><span data-stu-id="2403e-207">The unique ID of the organization that owns the definition of the format of the **Message** property.</span></span> <span data-ttu-id="2403e-208">**OwningEntity** debe incluir un nombre con copyright, marca registrada o único que sea propiedad de la entidad de negocio o del cuerpo de los estándares que haya definido el formato de mensaje.</span><span class="sxs-lookup"><span data-stu-id="2403e-208">**OwningEntity** must include a copyrighted, trademarked, or unique name that is owned by the business entity or standards body that defined the message format.</span></span>

</dd> <dt>

<span data-ttu-id="2403e-209">**PerceivedSeverity**</span><span class="sxs-lookup"><span data-stu-id="2403e-209">**PerceivedSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2403e-210">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2403e-210">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2403e-211">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2403e-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2403e-212">Calificadores: [**required**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PerceivedSeverity"), [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ("recommendation. itu \| X733. Gravedad percibida ")</span><span class="sxs-lookup"><span data-stu-id="2403e-212">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PerceivedSeverity"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Perceived severity")</span></span>
</dt> </dl>

<span data-ttu-id="2403e-213">La gravedad de la indicación de alerta desde el punto de vista del elemento que provocó la alerta.</span><span class="sxs-lookup"><span data-stu-id="2403e-213">The severity of the alert indication from the point of view of the element that raised the alert.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2403e-214"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="2403e-214"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="2403e-215">Sigue el uso común.</span><span class="sxs-lookup"><span data-stu-id="2403e-215">Follows common usage.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2403e-216"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="2403e-216"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="2403e-217">Indica que el valor de la gravedad se puede encontrar en la propiedad OtherSeverity.</span><span class="sxs-lookup"><span data-stu-id="2403e-217">Indicates that the Severity's value can be found in the OtherSeverity property.</span></span>

</dd> <dt>

<span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>

<span data-ttu-id="2403e-218"><span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Información** (2)</span><span class="sxs-lookup"><span data-stu-id="2403e-218"><span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Information** (2)</span></span>


</dt> <dd>

<span data-ttu-id="2403e-219">Sigue el uso común.</span><span class="sxs-lookup"><span data-stu-id="2403e-219">Follows common usage.</span></span>

</dd> <dt>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>

<span data-ttu-id="2403e-220"><span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Degradado/ADVERTENCIA** (3)</span><span class="sxs-lookup"><span data-stu-id="2403e-220"><span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Degraded/Warning** (3)</span></span>


</dt> <dd>

<span data-ttu-id="2403e-221">Debe usarse cuando sea adecuado para permitir que el usuario decida si es necesario realizar alguna acción.</span><span class="sxs-lookup"><span data-stu-id="2403e-221">Should be used when its appropriate to let the user decide if action is needed.</span></span>

</dd> <dt>

<span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>

<span data-ttu-id="2403e-222"><span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>**Secundaria** (4)</span><span class="sxs-lookup"><span data-stu-id="2403e-222"><span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>**Minor** (4)</span></span>


</dt> <dd>

<span data-ttu-id="2403e-223">Indica que la acción es necesaria, pero la situación no es seria en este momento.</span><span class="sxs-lookup"><span data-stu-id="2403e-223">Indicates action is needed, but the situation is not serious at this time.</span></span>

</dd> <dt>

<span id="Major"></span><span id="major"></span><span id="MAJOR"></span>

<span data-ttu-id="2403e-224"><span id="Major"></span><span id="major"></span><span id="MAJOR"></span>**Principal** (5)</span><span class="sxs-lookup"><span data-stu-id="2403e-224"><span id="Major"></span><span id="major"></span><span id="MAJOR"></span>**Major** (5)</span></span>


</dt> <dd>

<span data-ttu-id="2403e-225">Indica que la acción es necesaria ahora.</span><span class="sxs-lookup"><span data-stu-id="2403e-225">Indicates action is needed now.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="2403e-226"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Crítico** (6)</span><span class="sxs-lookup"><span data-stu-id="2403e-226"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (6)</span></span>


</dt> <dd>

<span data-ttu-id="2403e-227">La acción es necesaria ahora y el ámbito es amplio (es posible que se produzca una interrupción inminente en un recurso crítico).</span><span class="sxs-lookup"><span data-stu-id="2403e-227">Action is needed NOW and the scope is broad (perhaps an imminent outage to a critical resource will result).</span></span>

</dd> <dt>

<span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>

<span data-ttu-id="2403e-228"><span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>**Irrecuperable/no recuperable** (7)</span><span class="sxs-lookup"><span data-stu-id="2403e-228"><span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>**Fatal/NonRecoverable** (7)</span></span>


</dt> <dd>

<span data-ttu-id="2403e-229">Indica que se ha producido un error, pero es demasiado tarde para tomar medidas correctivas.</span><span class="sxs-lookup"><span data-stu-id="2403e-229">Indicates an error occurred, but it's too late to take remedial action.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2403e-230">**ProbableCause**</span><span class="sxs-lookup"><span data-stu-id="2403e-230">**ProbableCause**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2403e-231">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2403e-231">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2403e-232">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2403e-232">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2403e-233">Calificadores: [**required**](/windows/desktop/WmiSdk/standard-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("recommendation. itu \| X733. Causa probable: "," recommendation. ITU \| M3100. probableCause "," ITU-IANA-Alarm-TC "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**.**ProbableCauseDescription**","**\_ AlertIndication CIM**.**EventID**","**CIM \_ AlertIndication**.**EventTime**")</span><span class="sxs-lookup"><span data-stu-id="2403e-233">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Probable cause", "Recommendation.ITU\|M3100.probableCause", "ITU-IANA-ALARM-TC"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**ProbableCauseDescription**", "**CIM\_AlertIndication**.**EventID**", "**CIM\_AlertIndication**.**EventTime**")</span></span>
</dt> </dl>

<span data-ttu-id="2403e-234">La causa probable de la situación que produjo la indicación de la alerta.</span><span class="sxs-lookup"><span data-stu-id="2403e-234">The probable cause of the situation which resulted in the alert indication.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2403e-235">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="2403e-235">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2403e-236">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="2403e-236">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Adapter_Card_Error"></span><span id="adapter_card_error"></span><span id="ADAPTER_CARD_ERROR"></span>

<span data-ttu-id="2403e-237">**Error de tarjeta/adaptador** (2)</span><span class="sxs-lookup"><span data-stu-id="2403e-237">**Adapter/Card Error** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_Subsystem_Failure"></span><span id="application_subsystem_failure"></span><span id="APPLICATION_SUBSYSTEM_FAILURE"></span>

<span data-ttu-id="2403e-238">**Error del subsistema de aplicación** (3)</span><span class="sxs-lookup"><span data-stu-id="2403e-238">**Application Subsystem Failure** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bandwidth_Reduced"></span><span id="bandwidth_reduced"></span><span id="BANDWIDTH_REDUCED"></span>

<span data-ttu-id="2403e-239">**Ancho de banda reducido** (4)</span><span class="sxs-lookup"><span data-stu-id="2403e-239">**Bandwidth Reduced** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Connection_Establishment_Error"></span><span id="connection_establishment_error"></span><span id="CONNECTION_ESTABLISHMENT_ERROR"></span>

<span data-ttu-id="2403e-240">**Error de establecimiento de conexión** (5)</span><span class="sxs-lookup"><span data-stu-id="2403e-240">**Connection Establishment Error** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Communications_Protocol_Error"></span><span id="communications_protocol_error"></span><span id="COMMUNICATIONS_PROTOCOL_ERROR"></span>

<span data-ttu-id="2403e-241">**Error de protocolo de comunicaciones** (6)</span><span class="sxs-lookup"><span data-stu-id="2403e-241">**Communications Protocol Error** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Communications_Subsystem_Failure"></span><span id="communications_subsystem_failure"></span><span id="COMMUNICATIONS_SUBSYSTEM_FAILURE"></span>

<span data-ttu-id="2403e-242">**Error del subsistema de comunicaciones** (7)</span><span class="sxs-lookup"><span data-stu-id="2403e-242">**Communications Subsystem Failure** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Configuration_Customization_Error"></span><span id="configuration_customization_error"></span><span id="CONFIGURATION_CUSTOMIZATION_ERROR"></span>

<span data-ttu-id="2403e-243">**Error de configuración/personalización** (8)</span><span class="sxs-lookup"><span data-stu-id="2403e-243">**Configuration/Customization Error** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Congestion"></span><span id="congestion"></span><span id="CONGESTION"></span>

<span data-ttu-id="2403e-244">**Congestión** (9)</span><span class="sxs-lookup"><span data-stu-id="2403e-244">**Congestion** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Corrupt_Data"></span><span id="corrupt_data"></span><span id="CORRUPT_DATA"></span>

<span data-ttu-id="2403e-245">**Datos dañados** (10)</span><span class="sxs-lookup"><span data-stu-id="2403e-245">**Corrupt Data** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="CPU_Cycles_Limit_Exceeded"></span><span id="cpu_cycles_limit_exceeded"></span><span id="CPU_CYCLES_LIMIT_EXCEEDED"></span>

<span data-ttu-id="2403e-246">Se **superó el límite de ciclos de CPU** (11)</span><span class="sxs-lookup"><span data-stu-id="2403e-246">**CPU Cycles Limit Exceeded** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Dataset_Modem_Error"></span><span id="dataset_modem_error"></span><span id="DATASET_MODEM_ERROR"></span>

<span data-ttu-id="2403e-247">**Error de conjunto** de</span><span class="sxs-lookup"><span data-stu-id="2403e-247">**Dataset/Modem Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded_Signal"></span><span id="degraded_signal"></span><span id="DEGRADED_SIGNAL"></span>

<span data-ttu-id="2403e-248">**Señal degradada** (13)</span><span class="sxs-lookup"><span data-stu-id="2403e-248">**Degraded Signal** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="DTE-DCE_Interface_Error"></span><span id="dte-dce_interface_error"></span><span id="DTE-DCE_INTERFACE_ERROR"></span>

<span data-ttu-id="2403e-249">**Error de la interfaz DTE-DCE** (14)</span><span class="sxs-lookup"><span data-stu-id="2403e-249">**DTE-DCE Interface Error** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Enclosure_Door_Open"></span><span id="enclosure_door_open"></span><span id="ENCLOSURE_DOOR_OPEN"></span>

<span data-ttu-id="2403e-250">Abertura de la **puerta del gabinete** (15)</span><span class="sxs-lookup"><span data-stu-id="2403e-250">**Enclosure Door Open** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Equipment_Malfunction"></span><span id="equipment_malfunction"></span><span id="EQUIPMENT_MALFUNCTION"></span>

<span data-ttu-id="2403e-251">**Funcionamiento incorrecto del equipo** (16)</span><span class="sxs-lookup"><span data-stu-id="2403e-251">**Equipment Malfunction** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Excessive_Vibration"></span><span id="excessive_vibration"></span><span id="EXCESSIVE_VIBRATION"></span>

<span data-ttu-id="2403e-252">**Vibración excesiva** (17)</span><span class="sxs-lookup"><span data-stu-id="2403e-252">**Excessive Vibration** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="File_Format_Error"></span><span id="file_format_error"></span><span id="FILE_FORMAT_ERROR"></span>

<span data-ttu-id="2403e-253">**Error de formato de archivo** (18)</span><span class="sxs-lookup"><span data-stu-id="2403e-253">**File Format Error** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Fire_Detected"></span><span id="fire_detected"></span><span id="FIRE_DETECTED"></span>

<span data-ttu-id="2403e-254">**Desencadenamiento detectado** (19)</span><span class="sxs-lookup"><span data-stu-id="2403e-254">**Fire Detected** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Flood_Detected"></span><span id="flood_detected"></span><span id="FLOOD_DETECTED"></span>

<span data-ttu-id="2403e-255">**Inundación detectada** (20)</span><span class="sxs-lookup"><span data-stu-id="2403e-255">**Flood Detected** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Framing_Error"></span><span id="framing_error"></span><span id="FRAMING_ERROR"></span>

<span data-ttu-id="2403e-256">**Error de tramas** (21)</span><span class="sxs-lookup"><span data-stu-id="2403e-256">**Framing Error** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HVAC_Problem"></span><span id="hvac_problem"></span><span id="HVAC_PROBLEM"></span>

<span data-ttu-id="2403e-257">**Problema de HVAC** (22)</span><span class="sxs-lookup"><span data-stu-id="2403e-257">**HVAC Problem** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="Humidity_Unacceptable"></span><span id="humidity_unacceptable"></span><span id="HUMIDITY_UNACCEPTABLE"></span>

<span data-ttu-id="2403e-258">**Humedad inaceptable** (23)</span><span class="sxs-lookup"><span data-stu-id="2403e-258">**Humidity Unacceptable** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Device_Error"></span><span id="i_o_device_error"></span><span id="I_O_DEVICE_ERROR"></span>

<span data-ttu-id="2403e-259">**Error de dispositivo de e/s** (24)</span><span class="sxs-lookup"><span data-stu-id="2403e-259">**I/O Device Error** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="Input_Device_Error"></span><span id="input_device_error"></span><span id="INPUT_DEVICE_ERROR"></span>

<span data-ttu-id="2403e-260">**Error de dispositivo de entrada** (25)</span><span class="sxs-lookup"><span data-stu-id="2403e-260">**Input Device Error** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="LAN_Error"></span><span id="lan_error"></span><span id="LAN_ERROR"></span>

<span data-ttu-id="2403e-261">**Error de LAN** (26)</span><span class="sxs-lookup"><span data-stu-id="2403e-261">**LAN Error** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Toxic_Leak_Detected"></span><span id="non-toxic_leak_detected"></span><span id="NON-TOXIC_LEAK_DETECTED"></span>

<span data-ttu-id="2403e-262">**Pérdida no tóxica detectada** (27)</span><span class="sxs-lookup"><span data-stu-id="2403e-262">**Non-Toxic Leak Detected** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Local_Node_Transmission_Error"></span><span id="local_node_transmission_error"></span><span id="LOCAL_NODE_TRANSMISSION_ERROR"></span>

<span data-ttu-id="2403e-263">**Error de transmisión del nodo local** (28)</span><span class="sxs-lookup"><span data-stu-id="2403e-263">**Local Node Transmission Error** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Frame"></span><span id="loss_of_frame"></span><span id="LOSS_OF_FRAME"></span>

<span data-ttu-id="2403e-264">**Pérdida de fotograma** (29)</span><span class="sxs-lookup"><span data-stu-id="2403e-264">**Loss of Frame** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Signal"></span><span id="loss_of_signal"></span><span id="LOSS_OF_SIGNAL"></span>

<span data-ttu-id="2403e-265">**Pérdida de señal** (30)</span><span class="sxs-lookup"><span data-stu-id="2403e-265">**Loss of Signal** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Material_Supply_Exhausted"></span><span id="material_supply_exhausted"></span><span id="MATERIAL_SUPPLY_EXHAUSTED"></span>

<span data-ttu-id="2403e-266">**Suministro de material agotado** (31)</span><span class="sxs-lookup"><span data-stu-id="2403e-266">**Material Supply Exhausted** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Multiplexer_Problem"></span><span id="multiplexer_problem"></span><span id="MULTIPLEXER_PROBLEM"></span>

<span data-ttu-id="2403e-267">**Problema del multiplexor** (32)</span><span class="sxs-lookup"><span data-stu-id="2403e-267">**Multiplexer Problem** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Out_of_Memory"></span><span id="out_of_memory"></span><span id="OUT_OF_MEMORY"></span>

<span data-ttu-id="2403e-268">**Memoria insuficiente** (33)</span><span class="sxs-lookup"><span data-stu-id="2403e-268">**Out of Memory** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="Output_Device_Error"></span><span id="output_device_error"></span><span id="OUTPUT_DEVICE_ERROR"></span>

<span data-ttu-id="2403e-269">**Error de dispositivo de salida** (34)</span><span class="sxs-lookup"><span data-stu-id="2403e-269">**Output Device Error** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="Performance_Degraded"></span><span id="performance_degraded"></span><span id="PERFORMANCE_DEGRADED"></span>

<span data-ttu-id="2403e-270">**Rendimiento degradado** (35)</span><span class="sxs-lookup"><span data-stu-id="2403e-270">**Performance Degraded** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Problem"></span><span id="power_problem"></span><span id="POWER_PROBLEM"></span>

<span data-ttu-id="2403e-271">**Problema de energía** (36)</span><span class="sxs-lookup"><span data-stu-id="2403e-271">**Power Problem** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Pressure_Unacceptable"></span><span id="pressure_unacceptable"></span><span id="PRESSURE_UNACCEPTABLE"></span>

<span data-ttu-id="2403e-272">**Presión inaceptable** (37)</span><span class="sxs-lookup"><span data-stu-id="2403e-272">**Pressure Unacceptable** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="Processor_Problem__Internal_Machine_Error_"></span><span id="processor_problem__internal_machine_error_"></span><span id="PROCESSOR_PROBLEM__INTERNAL_MACHINE_ERROR_"></span>

<span data-ttu-id="2403e-273">**Problema del procesador (error interno de la máquina)** (38)</span><span class="sxs-lookup"><span data-stu-id="2403e-273">**Processor Problem (Internal Machine Error)** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Pump_Failure"></span><span id="pump_failure"></span><span id="PUMP_FAILURE"></span>

<span data-ttu-id="2403e-274">**Error de bombeo** (39)</span><span class="sxs-lookup"><span data-stu-id="2403e-274">**Pump Failure** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Queue_Size_Exceeded"></span><span id="queue_size_exceeded"></span><span id="QUEUE_SIZE_EXCEEDED"></span>

<span data-ttu-id="2403e-275">**Tamaño de cola superado** (40)</span><span class="sxs-lookup"><span data-stu-id="2403e-275">**Queue Size Exceeded** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="Receive_Failure"></span><span id="receive_failure"></span><span id="RECEIVE_FAILURE"></span>

<span data-ttu-id="2403e-276">**Error de recepción** (41)</span><span class="sxs-lookup"><span data-stu-id="2403e-276">**Receive Failure** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Receiver_Failure"></span><span id="receiver_failure"></span><span id="RECEIVER_FAILURE"></span>

<span data-ttu-id="2403e-277">**Error del receptor** (42)</span><span class="sxs-lookup"><span data-stu-id="2403e-277">**Receiver Failure** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="Remote_Node_Transmission_Error"></span><span id="remote_node_transmission_error"></span><span id="REMOTE_NODE_TRANSMISSION_ERROR"></span>

<span data-ttu-id="2403e-278">**Error de transmisión de nodo remoto** (43)</span><span class="sxs-lookup"><span data-stu-id="2403e-278">**Remote Node Transmission Error** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="Resource_at_or_Nearing_Capacity"></span><span id="resource_at_or_nearing_capacity"></span><span id="RESOURCE_AT_OR_NEARING_CAPACITY"></span>

<span data-ttu-id="2403e-279">**Recursos a la capacidad o en proximidad** (44)</span><span class="sxs-lookup"><span data-stu-id="2403e-279">**Resource at or Nearing Capacity** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="Response_Time_Excessive"></span><span id="response_time_excessive"></span><span id="RESPONSE_TIME_EXCESSIVE"></span>

<span data-ttu-id="2403e-280">**Tiempo de respuesta excesivo** (45)</span><span class="sxs-lookup"><span data-stu-id="2403e-280">**Response Time Excessive** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="Retransmission_Rate_Excessive"></span><span id="retransmission_rate_excessive"></span><span id="RETRANSMISSION_RATE_EXCESSIVE"></span>

<span data-ttu-id="2403e-281">**Tasa de retransmisión excesiva** (46)</span><span class="sxs-lookup"><span data-stu-id="2403e-281">**Retransmission Rate Excessive** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span>

<span data-ttu-id="2403e-282">**Error de software** (47)</span><span class="sxs-lookup"><span data-stu-id="2403e-282">**Software Error** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Program_Abnormally_Terminated"></span><span id="software_program_abnormally_terminated"></span><span id="SOFTWARE_PROGRAM_ABNORMALLY_TERMINATED"></span>

<span data-ttu-id="2403e-283">**Programa de software finalizado** de manera anómala (48)</span><span class="sxs-lookup"><span data-stu-id="2403e-283">**Software Program Abnormally Terminated** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Program_Error__Incorrect_Results_"></span><span id="software_program_error__incorrect_results_"></span><span id="SOFTWARE_PROGRAM_ERROR__INCORRECT_RESULTS_"></span>

<span data-ttu-id="2403e-284">**Error del programa de software (resultados incorrectos)** (49)</span><span class="sxs-lookup"><span data-stu-id="2403e-284">**Software Program Error (Incorrect Results)** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Capacity_Problem"></span><span id="storage_capacity_problem"></span><span id="STORAGE_CAPACITY_PROBLEM"></span>

<span data-ttu-id="2403e-285">**Problema de capacidad de almacenamiento** (50)</span><span class="sxs-lookup"><span data-stu-id="2403e-285">**Storage Capacity Problem** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="Temperature_Unacceptable"></span><span id="temperature_unacceptable"></span><span id="TEMPERATURE_UNACCEPTABLE"></span>

<span data-ttu-id="2403e-286">**Temperatura inaceptable** (51)</span><span class="sxs-lookup"><span data-stu-id="2403e-286">**Temperature Unacceptable** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="Threshold_Crossed"></span><span id="threshold_crossed"></span><span id="THRESHOLD_CROSSED"></span>

<span data-ttu-id="2403e-287">**Umbral superado** (52)</span><span class="sxs-lookup"><span data-stu-id="2403e-287">**Threshold Crossed** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="Timing_Problem"></span><span id="timing_problem"></span><span id="TIMING_PROBLEM"></span>

<span data-ttu-id="2403e-288">**Problema de sincronización** (53)</span><span class="sxs-lookup"><span data-stu-id="2403e-288">**Timing Problem** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="Toxic_Leak_Detected"></span><span id="toxic_leak_detected"></span><span id="TOXIC_LEAK_DETECTED"></span>

<span data-ttu-id="2403e-289">**Pérdida tóxica detectada** (54)</span><span class="sxs-lookup"><span data-stu-id="2403e-289">**Toxic Leak Detected** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="Transmit_Failure"></span><span id="transmit_failure"></span><span id="TRANSMIT_FAILURE"></span>

<span data-ttu-id="2403e-290">**Error de transmisión** (55)</span><span class="sxs-lookup"><span data-stu-id="2403e-290">**Transmit Failure** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="Transmitter_Failure"></span><span id="transmitter_failure"></span><span id="TRANSMITTER_FAILURE"></span>

<span data-ttu-id="2403e-291">**Error de transmisor** (56)</span><span class="sxs-lookup"><span data-stu-id="2403e-291">**Transmitter Failure** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="Underlying_Resource_Unavailable"></span><span id="underlying_resource_unavailable"></span><span id="UNDERLYING_RESOURCE_UNAVAILABLE"></span>

<span data-ttu-id="2403e-292">**Recurso subyacente no disponible** (57)</span><span class="sxs-lookup"><span data-stu-id="2403e-292">**Underlying Resource Unavailable** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Version_MisMatch"></span><span id="version_mismatch"></span><span id="VERSION_MISMATCH"></span>

<span data-ttu-id="2403e-293">**Discrepancia de versiones** (58)</span><span class="sxs-lookup"><span data-stu-id="2403e-293">**Version MisMatch** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Previous_Alert_Cleared"></span><span id="previous_alert_cleared"></span><span id="PREVIOUS_ALERT_CLEARED"></span>

<span data-ttu-id="2403e-294">**Alerta anterior desactivada** (59)</span><span class="sxs-lookup"><span data-stu-id="2403e-294">**Previous Alert Cleared** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="Login_Attempts_Failed"></span><span id="login_attempts_failed"></span><span id="LOGIN_ATTEMPTS_FAILED"></span>

<span data-ttu-id="2403e-295">**Error de intentos de inicio de sesión** (60)</span><span class="sxs-lookup"><span data-stu-id="2403e-295">**Login Attempts Failed** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Virus_Detected"></span><span id="software_virus_detected"></span><span id="SOFTWARE_VIRUS_DETECTED"></span>

<span data-ttu-id="2403e-296">**Virus de software detectado** (61)</span><span class="sxs-lookup"><span data-stu-id="2403e-296">**Software Virus Detected** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="Hardware_Security_Breached"></span><span id="hardware_security_breached"></span><span id="HARDWARE_SECURITY_BREACHED"></span>

<span data-ttu-id="2403e-297">**Seguridad de hardware infringida** (62)</span><span class="sxs-lookup"><span data-stu-id="2403e-297">**Hardware Security Breached** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="Denial_of_Service_Detected"></span><span id="denial_of_service_detected"></span><span id="DENIAL_OF_SERVICE_DETECTED"></span>

<span data-ttu-id="2403e-298">**Denegación de servicio detectada** (63)</span><span class="sxs-lookup"><span data-stu-id="2403e-298">**Denial of Service Detected** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="Security_Credential_MisMatch"></span><span id="security_credential_mismatch"></span><span id="SECURITY_CREDENTIAL_MISMATCH"></span>

<span data-ttu-id="2403e-299">**No coincide la credencial de seguridad** (64)</span><span class="sxs-lookup"><span data-stu-id="2403e-299">**Security Credential MisMatch** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="Unauthorized_Access"></span><span id="unauthorized_access"></span><span id="UNAUTHORIZED_ACCESS"></span>

<span data-ttu-id="2403e-300">**Acceso no autorizado** (65)</span><span class="sxs-lookup"><span data-stu-id="2403e-300">**Unauthorized Access** (65)</span></span>


</dt> <dd></dd> <dt>

<span id="Alarm_Received"></span><span id="alarm_received"></span><span id="ALARM_RECEIVED"></span>

<span data-ttu-id="2403e-301">**Alarma recibida** (66)</span><span class="sxs-lookup"><span data-stu-id="2403e-301">**Alarm Received** (66)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Pointer"></span><span id="loss_of_pointer"></span><span id="LOSS_OF_POINTER"></span>

<span data-ttu-id="2403e-302">**Pérdida de puntero** (67)</span><span class="sxs-lookup"><span data-stu-id="2403e-302">**Loss of Pointer** (67)</span></span>


</dt> <dd></dd> <dt>

<span id="Payload_Mismatch"></span><span id="payload_mismatch"></span><span id="PAYLOAD_MISMATCH"></span>

<span data-ttu-id="2403e-303">Error de **coincidencia de carga** (68)</span><span class="sxs-lookup"><span data-stu-id="2403e-303">**Payload Mismatch** (68)</span></span>


</dt> <dd></dd> <dt>

<span id="Transmission_Error"></span><span id="transmission_error"></span><span id="TRANSMISSION_ERROR"></span>

<span data-ttu-id="2403e-304">**Error de transmisión** (69)</span><span class="sxs-lookup"><span data-stu-id="2403e-304">**Transmission Error** (69)</span></span>


</dt> <dd></dd> <dt>

<span id="Excessive_Error_Rate"></span><span id="excessive_error_rate"></span><span id="EXCESSIVE_ERROR_RATE"></span>

<span data-ttu-id="2403e-305">**Tasa de errores excesiva** (70)</span><span class="sxs-lookup"><span data-stu-id="2403e-305">**Excessive Error Rate** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="Trace_Problem"></span><span id="trace_problem"></span><span id="TRACE_PROBLEM"></span>

<span data-ttu-id="2403e-306">**Problema de seguimiento** (71)</span><span class="sxs-lookup"><span data-stu-id="2403e-306">**Trace Problem** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="Element_Unavailable"></span><span id="element_unavailable"></span><span id="ELEMENT_UNAVAILABLE"></span>

<span data-ttu-id="2403e-307">**Elemento no disponible** (72)</span><span class="sxs-lookup"><span data-stu-id="2403e-307">**Element Unavailable** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="Element_Missing"></span><span id="element_missing"></span><span id="ELEMENT_MISSING"></span>

<span data-ttu-id="2403e-308">**Falta el elemento** (73)</span><span class="sxs-lookup"><span data-stu-id="2403e-308">**Element Missing** (73)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Multi_Frame"></span><span id="loss_of_multi_frame"></span><span id="LOSS_OF_MULTI_FRAME"></span>

<span data-ttu-id="2403e-309">**Pérdida de varios fotogramas** (74)</span><span class="sxs-lookup"><span data-stu-id="2403e-309">**Loss of Multi Frame** (74)</span></span>


</dt> <dd></dd> <dt>

<span id="Broadcast_Channel_Failure"></span><span id="broadcast_channel_failure"></span><span id="BROADCAST_CHANNEL_FAILURE"></span>

<span data-ttu-id="2403e-310">**Error de canal de difusión** (75)</span><span class="sxs-lookup"><span data-stu-id="2403e-310">**Broadcast Channel Failure** (75)</span></span>


</dt> <dd></dd> <dt>

<span id="Invalid_Message_Received"></span><span id="invalid_message_received"></span><span id="INVALID_MESSAGE_RECEIVED"></span>

<span data-ttu-id="2403e-311">Se **recibió un mensaje no válido** (76)</span><span class="sxs-lookup"><span data-stu-id="2403e-311">**Invalid Message Received** (76)</span></span>


</dt> <dd></dd> <dt>

<span id="Routing_Failure"></span><span id="routing_failure"></span><span id="ROUTING_FAILURE"></span>

<span data-ttu-id="2403e-312">**Error de enrutamiento** (77)</span><span class="sxs-lookup"><span data-stu-id="2403e-312">**Routing Failure** (77)</span></span>


</dt> <dd></dd> <dt>

<span id="Backplane_Failure"></span><span id="backplane_failure"></span><span id="BACKPLANE_FAILURE"></span>

<span data-ttu-id="2403e-313">**Error de backplane** (78)</span><span class="sxs-lookup"><span data-stu-id="2403e-313">**Backplane Failure** (78)</span></span>


</dt> <dd></dd> <dt>

<span id="Identifier_Duplication"></span><span id="identifier_duplication"></span><span id="IDENTIFIER_DUPLICATION"></span>

<span data-ttu-id="2403e-314">**Duplicación de identificadores** (79)</span><span class="sxs-lookup"><span data-stu-id="2403e-314">**Identifier Duplication** (79)</span></span>


</dt> <dd></dd> <dt>

<span id="Protection_Path_Failure"></span><span id="protection_path_failure"></span><span id="PROTECTION_PATH_FAILURE"></span>

<span data-ttu-id="2403e-315">**Error de ruta de protección** (80)</span><span class="sxs-lookup"><span data-stu-id="2403e-315">**Protection Path Failure** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="Sync_Loss_or_Mismatch"></span><span id="sync_loss_or_mismatch"></span><span id="SYNC_LOSS_OR_MISMATCH"></span>

<span data-ttu-id="2403e-316">**Pérdida o desigualdad de sincronización** (81)</span><span class="sxs-lookup"><span data-stu-id="2403e-316">**Sync Loss or Mismatch** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="Terminal_Problem"></span><span id="terminal_problem"></span><span id="TERMINAL_PROBLEM"></span>

<span data-ttu-id="2403e-317">**Problema de terminal** (82)</span><span class="sxs-lookup"><span data-stu-id="2403e-317">**Terminal Problem** (82)</span></span>


</dt> <dd></dd> <dt>

<span id="Real_Time_Clock_Failure"></span><span id="real_time_clock_failure"></span><span id="REAL_TIME_CLOCK_FAILURE"></span>

<span data-ttu-id="2403e-318">**Error de reloj en tiempo real** (83)</span><span class="sxs-lookup"><span data-stu-id="2403e-318">**Real Time Clock Failure** (83)</span></span>


</dt> <dd></dd> <dt>

<span id="Antenna_Failure"></span><span id="antenna_failure"></span><span id="ANTENNA_FAILURE"></span>

<span data-ttu-id="2403e-319">**Error de antena** (84)</span><span class="sxs-lookup"><span data-stu-id="2403e-319">**Antenna Failure** (84)</span></span>


</dt> <dd></dd> <dt>

<span id="Battery_Charging_Failure"></span><span id="battery_charging_failure"></span><span id="BATTERY_CHARGING_FAILURE"></span>

<span data-ttu-id="2403e-320">**Error de carga** de la batería (85)</span><span class="sxs-lookup"><span data-stu-id="2403e-320">**Battery Charging Failure** (85)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_Failure"></span><span id="disk_failure"></span><span id="DISK_FAILURE"></span>

<span data-ttu-id="2403e-321">**Error de disco** (86)</span><span class="sxs-lookup"><span data-stu-id="2403e-321">**Disk Failure** (86)</span></span>


</dt> <dd></dd> <dt>

<span id="Frequency_Hopping_Failure"></span><span id="frequency_hopping_failure"></span><span id="FREQUENCY_HOPPING_FAILURE"></span>

<span data-ttu-id="2403e-322">**Error de salto de frecuencia** (87)</span><span class="sxs-lookup"><span data-stu-id="2403e-322">**Frequency Hopping Failure** (87)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Redundancy"></span><span id="loss_of_redundancy"></span><span id="LOSS_OF_REDUNDANCY"></span>

<span data-ttu-id="2403e-323">**Pérdida de redundancia** (88)</span><span class="sxs-lookup"><span data-stu-id="2403e-323">**Loss of Redundancy** (88)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Supply_Failure"></span><span id="power_supply_failure"></span><span id="POWER_SUPPLY_FAILURE"></span>

<span data-ttu-id="2403e-324">**Error** de la fuente de alimentación (89)</span><span class="sxs-lookup"><span data-stu-id="2403e-324">**Power Supply Failure** (89)</span></span>


</dt> <dd></dd> <dt>

<span id="Signal_Quality_Problem"></span><span id="signal_quality_problem"></span><span id="SIGNAL_QUALITY_PROBLEM"></span>

<span data-ttu-id="2403e-325">**Problema de calidad** de la señal (90)</span><span class="sxs-lookup"><span data-stu-id="2403e-325">**Signal Quality Problem** (90)</span></span>


</dt> <dd></dd> <dt>

<span id="Battery_Discharging"></span><span id="battery_discharging"></span><span id="BATTERY_DISCHARGING"></span>

<span data-ttu-id="2403e-326">**Descarga** de la batería (91)</span><span class="sxs-lookup"><span data-stu-id="2403e-326">**Battery Discharging** (91)</span></span>


</dt> <dd></dd> <dt>

<span id="Battery_Failure"></span><span id="battery_failure"></span><span id="BATTERY_FAILURE"></span>

<span data-ttu-id="2403e-327">**Error de batería** (92)</span><span class="sxs-lookup"><span data-stu-id="2403e-327">**Battery Failure** (92)</span></span>


</dt> <dd></dd> <dt>

<span id="Commercial_Power_Problem"></span><span id="commercial_power_problem"></span><span id="COMMERCIAL_POWER_PROBLEM"></span>

<span data-ttu-id="2403e-328">**Problema de alimentación comercial** (93)</span><span class="sxs-lookup"><span data-stu-id="2403e-328">**Commercial Power Problem** (93)</span></span>


</dt> <dd></dd> <dt>

<span id="Fan_Failure"></span><span id="fan_failure"></span><span id="FAN_FAILURE"></span>

<span data-ttu-id="2403e-329">**Error de ventilador** (94)</span><span class="sxs-lookup"><span data-stu-id="2403e-329">**Fan Failure** (94)</span></span>


</dt> <dd></dd> <dt>

<span id="Engine_Failure"></span><span id="engine_failure"></span><span id="ENGINE_FAILURE"></span>

<span data-ttu-id="2403e-330">**Error del motor** (95)</span><span class="sxs-lookup"><span data-stu-id="2403e-330">**Engine Failure** (95)</span></span>


</dt> <dd></dd> <dt>

<span id="Sensor_Failure"></span><span id="sensor_failure"></span><span id="SENSOR_FAILURE"></span>

<span data-ttu-id="2403e-331">**Error del sensor** (96)</span><span class="sxs-lookup"><span data-stu-id="2403e-331">**Sensor Failure** (96)</span></span>


</dt> <dd></dd> <dt>

<span id="Fuse_Failure"></span><span id="fuse_failure"></span><span id="FUSE_FAILURE"></span>

<span data-ttu-id="2403e-332">**Error de fusible** (97)</span><span class="sxs-lookup"><span data-stu-id="2403e-332">**Fuse Failure** (97)</span></span>


</dt> <dd></dd> <dt>

<span id="Generator_Failure"></span><span id="generator_failure"></span><span id="GENERATOR_FAILURE"></span>

<span data-ttu-id="2403e-333">**Error del generador** (98)</span><span class="sxs-lookup"><span data-stu-id="2403e-333">**Generator Failure** (98)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Battery"></span><span id="low_battery"></span><span id="LOW_BATTERY"></span>

<span data-ttu-id="2403e-334">**Batería baja** (99)</span><span class="sxs-lookup"><span data-stu-id="2403e-334">**Low Battery** (99)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Fuel"></span><span id="low_fuel"></span><span id="LOW_FUEL"></span>

<span data-ttu-id="2403e-335">**Combustible bajo** (100)</span><span class="sxs-lookup"><span data-stu-id="2403e-335">**Low Fuel** (100)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Water"></span><span id="low_water"></span><span id="LOW_WATER"></span>

<span data-ttu-id="2403e-336">**Bajo agua** (101)</span><span class="sxs-lookup"><span data-stu-id="2403e-336">**Low Water** (101)</span></span>


</dt> <dd></dd> <dt>

<span id="Explosive_Gas"></span><span id="explosive_gas"></span><span id="EXPLOSIVE_GAS"></span>

<span data-ttu-id="2403e-337">**Gas explosivo** (102)</span><span class="sxs-lookup"><span data-stu-id="2403e-337">**Explosive Gas** (102)</span></span>


</dt> <dd></dd> <dt>

<span id="High_Winds"></span><span id="high_winds"></span><span id="HIGH_WINDS"></span>

<span data-ttu-id="2403e-338">**Viento alto** (103)</span><span class="sxs-lookup"><span data-stu-id="2403e-338">**High Winds** (103)</span></span>


</dt> <dd></dd> <dt>

<span id="Ice_Buildup"></span><span id="ice_buildup"></span><span id="ICE_BUILDUP"></span>

<span data-ttu-id="2403e-339">**Acumulación de hielo** (104)</span><span class="sxs-lookup"><span data-stu-id="2403e-339">**Ice Buildup** (104)</span></span>


</dt> <dd></dd> <dt>

<span id="Smoke"></span><span id="smoke"></span><span id="SMOKE"></span>

<span data-ttu-id="2403e-340">**Humo** (105)</span><span class="sxs-lookup"><span data-stu-id="2403e-340">**Smoke** (105)</span></span>


</dt> <dd></dd> <dt>

<span id="Memory_Mismatch"></span><span id="memory_mismatch"></span><span id="MEMORY_MISMATCH"></span>

<span data-ttu-id="2403e-341">**No coincide la memoria** (106)</span><span class="sxs-lookup"><span data-stu-id="2403e-341">**Memory Mismatch** (106)</span></span>


</dt> <dd></dd> <dt>

<span id="Out_of_CPU_Cycles"></span><span id="out_of_cpu_cycles"></span><span id="OUT_OF_CPU_CYCLES"></span>

<span data-ttu-id="2403e-342">**Ciclos de CPU agotados** (107)</span><span class="sxs-lookup"><span data-stu-id="2403e-342">**Out of CPU Cycles** (107)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Environment_Problem"></span><span id="software_environment_problem"></span><span id="SOFTWARE_ENVIRONMENT_PROBLEM"></span>

<span data-ttu-id="2403e-343">**Problema del entorno de software** (108)</span><span class="sxs-lookup"><span data-stu-id="2403e-343">**Software Environment Problem** (108)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Download_Failure"></span><span id="software_download_failure"></span><span id="SOFTWARE_DOWNLOAD_FAILURE"></span>

<span data-ttu-id="2403e-344">**Error de descarga de software** (109)</span><span class="sxs-lookup"><span data-stu-id="2403e-344">**Software Download Failure** (109)</span></span>


</dt> <dd></dd> <dt>

<span id="Element_Reinitialized"></span><span id="element_reinitialized"></span><span id="ELEMENT_REINITIALIZED"></span>

<span data-ttu-id="2403e-345">**Elemento reinicializado** (110)</span><span class="sxs-lookup"><span data-stu-id="2403e-345">**Element Reinitialized** (110)</span></span>


</dt> <dd></dd> <dt>

<span id="Timeout"></span><span id="timeout"></span><span id="TIMEOUT"></span>

<span data-ttu-id="2403e-346">**Tiempo de espera** (111)</span><span class="sxs-lookup"><span data-stu-id="2403e-346">**Timeout** (111)</span></span>


</dt> <dd></dd> <dt>

<span id="Logging_Problems"></span><span id="logging_problems"></span><span id="LOGGING_PROBLEMS"></span>

<span data-ttu-id="2403e-347">**Problemas de registro** (112)</span><span class="sxs-lookup"><span data-stu-id="2403e-347">**Logging Problems** (112)</span></span>


</dt> <dd></dd> <dt>

<span id="Leak_Detected"></span><span id="leak_detected"></span><span id="LEAK_DETECTED"></span>

<span data-ttu-id="2403e-348">**Pérdida detectada** (113)</span><span class="sxs-lookup"><span data-stu-id="2403e-348">**Leak Detected** (113)</span></span>


</dt> <dd></dd> <dt>

<span id="Protection_Mechanism_Failure"></span><span id="protection_mechanism_failure"></span><span id="PROTECTION_MECHANISM_FAILURE"></span>

<span data-ttu-id="2403e-349">**Error del mecanismo de protección** (114)</span><span class="sxs-lookup"><span data-stu-id="2403e-349">**Protection Mechanism Failure** (114)</span></span>


</dt> <dd></dd> <dt>

<span id="Protecting_Resource_Failure"></span><span id="protecting_resource_failure"></span><span id="PROTECTING_RESOURCE_FAILURE"></span>

<span data-ttu-id="2403e-350">**Error de protección de recursos** (115)</span><span class="sxs-lookup"><span data-stu-id="2403e-350">**Protecting Resource Failure** (115)</span></span>


</dt> <dd></dd> <dt>

<span id="Database_Inconsistency"></span><span id="database_inconsistency"></span><span id="DATABASE_INCONSISTENCY"></span>

<span data-ttu-id="2403e-351">Incoherencia de la **base de datos** (116)</span><span class="sxs-lookup"><span data-stu-id="2403e-351">**Database Inconsistency** (116)</span></span>


</dt> <dd></dd> <dt>

<span id="Authentication_Failure"></span><span id="authentication_failure"></span><span id="AUTHENTICATION_FAILURE"></span>

<span data-ttu-id="2403e-352">**Error de autenticación** (117)</span><span class="sxs-lookup"><span data-stu-id="2403e-352">**Authentication Failure** (117)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_of_Confidentiality"></span><span id="breach_of_confidentiality"></span><span id="BREACH_OF_CONFIDENTIALITY"></span>

<span data-ttu-id="2403e-353">**Infracción de la confidencialidad** (118)</span><span class="sxs-lookup"><span data-stu-id="2403e-353">**Breach of Confidentiality** (118)</span></span>


</dt> <dd></dd> <dt>

<span id="Cable_Tamper"></span><span id="cable_tamper"></span><span id="CABLE_TAMPER"></span>

<span data-ttu-id="2403e-354">**Manipulación de cables** (119)</span><span class="sxs-lookup"><span data-stu-id="2403e-354">**Cable Tamper** (119)</span></span>


</dt> <dd></dd> <dt>

<span id="Delayed_Information"></span><span id="delayed_information"></span><span id="DELAYED_INFORMATION"></span>

<span data-ttu-id="2403e-355">**Información retrasada** (120)</span><span class="sxs-lookup"><span data-stu-id="2403e-355">**Delayed Information** (120)</span></span>


</dt> <dd></dd> <dt>

<span id="Duplicate_Information"></span><span id="duplicate_information"></span><span id="DUPLICATE_INFORMATION"></span>

<span data-ttu-id="2403e-356">**Información duplicada** (121)</span><span class="sxs-lookup"><span data-stu-id="2403e-356">**Duplicate Information** (121)</span></span>


</dt> <dd></dd> <dt>

<span id="Information_Missing"></span><span id="information_missing"></span><span id="INFORMATION_MISSING"></span>

<span data-ttu-id="2403e-357">**Falta información** (122)</span><span class="sxs-lookup"><span data-stu-id="2403e-357">**Information Missing** (122)</span></span>


</dt> <dd></dd> <dt>

<span id="Information_Modification"></span><span id="information_modification"></span><span id="INFORMATION_MODIFICATION"></span>

<span data-ttu-id="2403e-358">**Modificación** de la información (123)</span><span class="sxs-lookup"><span data-stu-id="2403e-358">**Information Modification** (123)</span></span>


</dt> <dd></dd> <dt>

<span id="Information_Out_of_Sequence"></span><span id="information_out_of_sequence"></span><span id="INFORMATION_OUT_OF_SEQUENCE"></span>

<span data-ttu-id="2403e-359">**Información fuera de secuencia** (124)</span><span class="sxs-lookup"><span data-stu-id="2403e-359">**Information Out of Sequence** (124)</span></span>


</dt> <dd></dd> <dt>

<span id="Key_Expired"></span><span id="key_expired"></span><span id="KEY_EXPIRED"></span>

<span data-ttu-id="2403e-360">**Clave expirada** (125)</span><span class="sxs-lookup"><span data-stu-id="2403e-360">**Key Expired** (125)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Repudiation_Failure"></span><span id="non-repudiation_failure"></span><span id="NON-REPUDIATION_FAILURE"></span>

<span data-ttu-id="2403e-361">**Error sin repudio** (126)</span><span class="sxs-lookup"><span data-stu-id="2403e-361">**Non-Repudiation Failure** (126)</span></span>


</dt> <dd></dd> <dt>

<span id="Out_of_Hours_Activity"></span><span id="out_of_hours_activity"></span><span id="OUT_OF_HOURS_ACTIVITY"></span>

<span data-ttu-id="2403e-362">**Actividad fuera de horas** (127)</span><span class="sxs-lookup"><span data-stu-id="2403e-362">**Out of Hours Activity** (127)</span></span>


</dt> <dd></dd> <dt>

<span id="Out_of_Service"></span><span id="out_of_service"></span><span id="OUT_OF_SERVICE"></span>

<span data-ttu-id="2403e-363">**Fuera de servicio** (128)</span><span class="sxs-lookup"><span data-stu-id="2403e-363">**Out of Service** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="Procedural_Error"></span><span id="procedural_error"></span><span id="PROCEDURAL_ERROR"></span>

<span data-ttu-id="2403e-364">**Error de procedimiento** (129)</span><span class="sxs-lookup"><span data-stu-id="2403e-364">**Procedural Error** (129)</span></span>


</dt> <dd></dd> <dt>

<span id="Unexpected_Information"></span><span id="unexpected_information"></span><span id="UNEXPECTED_INFORMATION"></span>

<span data-ttu-id="2403e-365">**Información inesperada** (130)</span><span class="sxs-lookup"><span data-stu-id="2403e-365">**Unexpected Information** (130)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2403e-366">**ProbableCauseDescription**</span><span class="sxs-lookup"><span data-stu-id="2403e-366">**ProbableCauseDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2403e-367">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2403e-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2403e-368">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2403e-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2403e-369">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**.**ProbableCause**")</span><span class="sxs-lookup"><span data-stu-id="2403e-369">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**ProbableCause**")</span></span>
</dt> </dl>

<span data-ttu-id="2403e-370">Información adicional relacionada con la propiedad **ProbableCause** .</span><span class="sxs-lookup"><span data-stu-id="2403e-370">Additional information related to the **ProbableCause** property.</span></span>

</dd> <dt>

<span data-ttu-id="2403e-371">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="2403e-371">**ProviderName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2403e-372">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2403e-372">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2403e-373">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2403e-373">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2403e-374">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="2403e-374">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="2403e-375">Nombre del proveedor que generó la indicación.</span><span class="sxs-lookup"><span data-stu-id="2403e-375">The name of the provider that generated the indication.</span></span>

</dd> <dt>

<span data-ttu-id="2403e-376">**RecommendedActions**</span><span class="sxs-lookup"><span data-stu-id="2403e-376">**RecommendedActions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2403e-377">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="2403e-377">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2403e-378">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2403e-378">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2403e-379">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("RECOMMENDATION. itu \| X733. Acciones de reparación propuestas ")</span><span class="sxs-lookup"><span data-stu-id="2403e-379">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Proposed repair actions")</span></span>
</dt> </dl>

<span data-ttu-id="2403e-380">Descripciones de forma libre de las acciones recomendadas que se deben realizar para resolver la causa de la notificación.</span><span class="sxs-lookup"><span data-stu-id="2403e-380">Free form descriptions of the recommended actions to take to resolve the cause of the notification.</span></span>

</dd> <dt>

<span data-ttu-id="2403e-381">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2403e-381">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2403e-382">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2403e-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2403e-383">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2403e-383">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2403e-384">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="2403e-384">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="2403e-385">Valor de **CreationClassName** del sistema de ámbito para el proveedor que generó la indicación.</span><span class="sxs-lookup"><span data-stu-id="2403e-385">The **CreationClassName** value of the scoping system for the provider that generated the indication.</span></span>

</dd> <dt>

<span data-ttu-id="2403e-386">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="2403e-386">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2403e-387">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2403e-387">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2403e-388">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2403e-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2403e-389">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="2403e-389">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="2403e-390">Nombre del sistema de ámbito del proveedor que generó la indicación.</span><span class="sxs-lookup"><span data-stu-id="2403e-390">The scoping system name for the provider that generated the indication.</span></span>

</dd> <dt>

<span data-ttu-id="2403e-391">**Tendencias**</span><span class="sxs-lookup"><span data-stu-id="2403e-391">**Trending**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2403e-392">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2403e-392">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2403e-393">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2403e-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2403e-394">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("RECOMMENDATION. itu \| X733. TrendIndication")</span><span class="sxs-lookup"><span data-stu-id="2403e-394">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.TrendIndication")</span></span>
</dt> </dl>

<span data-ttu-id="2403e-395">Proporciona información sobre tendencias: tendencia hacia arriba, hacia abajo o sin cambios.</span><span class="sxs-lookup"><span data-stu-id="2403e-395">Provides information on trending - trending up, down or no change.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2403e-396">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="2403e-396">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="2403e-397">**No aplicable** (1)</span><span class="sxs-lookup"><span data-stu-id="2403e-397">**Not Applicable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Trending_Up"></span><span id="trending_up"></span><span id="TRENDING_UP"></span>

<span data-ttu-id="2403e-398">**Tendencia hacia arriba** (2)</span><span class="sxs-lookup"><span data-stu-id="2403e-398">**Trending Up** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Trending_Down"></span><span id="trending_down"></span><span id="TRENDING_DOWN"></span>

<span data-ttu-id="2403e-399">**Tendencia hacia abajo** (3)</span><span class="sxs-lookup"><span data-stu-id="2403e-399">**Trending Down** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span>

<span data-ttu-id="2403e-400">**Sin cambios** (4)</span><span class="sxs-lookup"><span data-stu-id="2403e-400">**No Change** (4)</span></span>


<span data-ttu-id="2403e-401"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="2403e-401"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="2403e-402">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2403e-402">Requirements</span></span>



| <span data-ttu-id="2403e-403">Requisito</span><span class="sxs-lookup"><span data-stu-id="2403e-403">Requirement</span></span> | <span data-ttu-id="2403e-404">Value</span><span class="sxs-lookup"><span data-stu-id="2403e-404">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2403e-405">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2403e-405">Minimum supported client</span></span><br/> | <span data-ttu-id="2403e-406">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2403e-406">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="2403e-407">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2403e-407">Minimum supported server</span></span><br/> | <span data-ttu-id="2403e-408">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="2403e-408">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="2403e-409">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2403e-409">Namespace</span></span><br/>                | <span data-ttu-id="2403e-410">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="2403e-410">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2403e-411">MOF</span><span class="sxs-lookup"><span data-stu-id="2403e-411">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2403e-412"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2403e-412"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2403e-413">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2403e-413">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2403e-414"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2403e-414"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2403e-415">Vea también</span><span class="sxs-lookup"><span data-stu-id="2403e-415">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2403e-416">**\_PROCESSINDICATION CIM**</span><span class="sxs-lookup"><span data-stu-id="2403e-416">**CIM\_ProcessIndication**</span></span>](cim-processindication.md)
</dt> </dl>

 

