---
description: La clase singleton ScriptingStandardConsumerSetting proporciona datos de registro que son comunes a todas las instancias de la clase de consumidor estándar ActiveScriptEventConsumer.
ms.assetid: d217e058-3529-4173-b896-ebff3d7b05c6
ms.tgt_platform: multiple
title: Clase ScriptingStandardConsumerSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ScriptingStandardConsumerSetting
- ScriptingStandardConsumerSetting.Caption
- ScriptingStandardConsumerSetting.Description
- ScriptingStandardConsumerSetting.MaximumScripts
- ScriptingStandardConsumerSetting.SettingID
- ScriptingStandardConsumerSetting.Timeout
api_type:
- DllExport
api_location:
- Scrcons.exe
ms.openlocfilehash: 43eae14eea445f546f731605c94b38e770b08691
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276135"
---
# <a name="scriptingstandardconsumersetting-class"></a><span data-ttu-id="12f6d-103">Clase ScriptingStandardConsumerSetting</span><span class="sxs-lookup"><span data-stu-id="12f6d-103">ScriptingStandardConsumerSetting class</span></span>

<span data-ttu-id="12f6d-104">La clase singleton **ScriptingStandardConsumerSetting** proporciona datos de registro que son comunes a todas las instancias de la clase de consumidor estándar [**ActiveScriptEventConsumer**](activescripteventconsumer.md) .</span><span class="sxs-lookup"><span data-stu-id="12f6d-104">The singleton **ScriptingStandardConsumerSetting** class provides registration data that is common to all instances of the [**ActiveScriptEventConsumer**](activescripteventconsumer.md) standard consumer class.</span></span> <span data-ttu-id="12f6d-105">Una instancia de **ActiveScriptEventConsumer** usa las propiedades **MaximumScripts** y **timeout** .</span><span class="sxs-lookup"><span data-stu-id="12f6d-105">An **ActiveScriptEventConsumer** instance uses the **MaximumScripts** and **Timeout** properties.</span></span> <span data-ttu-id="12f6d-106">Para obtener más información, consulte [supervisión y respuesta a eventos con consumidores estándar](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="12f6d-106">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

<span data-ttu-id="12f6d-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="12f6d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="12f6d-108">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="12f6d-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="12f6d-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="12f6d-109">Syntax</span></span>

``` syntax
[Singleton, AMENDMENT]
class ScriptingStandardConsumerSetting : CIM_Setting
{
  string Caption = "Scripting Standard Consumer Setting";
  string Description = "Registration data common to all instances of the Scripting Standard Consumer";
  uint32 MaximumScripts = 300;
  string SettingID = "ScriptingStandardConsumerSetting";
  uint32 Timeout = 0;
};
```

## <a name="members"></a><span data-ttu-id="12f6d-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="12f6d-110">Members</span></span>

<span data-ttu-id="12f6d-111">La clase **ScriptingStandardConsumerSetting** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="12f6d-111">The **ScriptingStandardConsumerSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="12f6d-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="12f6d-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="12f6d-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="12f6d-113">Properties</span></span>

<span data-ttu-id="12f6d-114">La clase **ScriptingStandardConsumerSetting** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="12f6d-114">The **ScriptingStandardConsumerSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="12f6d-115">**Caption**</span><span class="sxs-lookup"><span data-stu-id="12f6d-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12f6d-116">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="12f6d-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12f6d-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="12f6d-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12f6d-118">Calificadores: [**MaxLen**](standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="12f6d-118">Qualifiers: [**MaxLen**](standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="12f6d-119">Breve descripción de un objeto de una cadena de una línea.</span><span class="sxs-lookup"><span data-stu-id="12f6d-119">A short description of an object a one line string.</span></span> <span data-ttu-id="12f6d-120">Contiene la cadena **ScriptingStandardConsumerSetting** porque se trata de una clase singleton.</span><span class="sxs-lookup"><span data-stu-id="12f6d-120">Contains the string **ScriptingStandardConsumerSetting** because this is a singleton class.</span></span>

</dd> <dt>

<span data-ttu-id="12f6d-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="12f6d-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12f6d-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="12f6d-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12f6d-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="12f6d-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12f6d-124">Una descripción de texto de un objeto.</span><span class="sxs-lookup"><span data-stu-id="12f6d-124">A text description of an object.</span></span>

</dd> <dt>

<span data-ttu-id="12f6d-125">**MaximumScripts**</span><span class="sxs-lookup"><span data-stu-id="12f6d-125">**MaximumScripts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12f6d-126">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="12f6d-126">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="12f6d-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="12f6d-127">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="12f6d-128">Número máximo de scripts que se ejecutan antes de que un consumidor inicie una nueva instancia.</span><span class="sxs-lookup"><span data-stu-id="12f6d-128">Maximum number of scripts that are run before a consumer starts a new instance.</span></span> <span data-ttu-id="12f6d-129">Para borrar las pérdidas de memoria de los scripts, cierre el consumidor con regularidad.</span><span class="sxs-lookup"><span data-stu-id="12f6d-129">To clear out memory leaks from scripts, shut down the consumer regularly.</span></span> <span data-ttu-id="12f6d-130">El valor predeterminado es 300.</span><span class="sxs-lookup"><span data-stu-id="12f6d-130">The default value is 300.</span></span>

</dd> <dt>

<span data-ttu-id="12f6d-131">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="12f6d-131">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12f6d-132">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="12f6d-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12f6d-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="12f6d-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12f6d-134">Calificadores: [**MaxLen**](standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="12f6d-134">Qualifiers: [**MaxLen**](standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="12f6d-135">Identificador del objeto de configuración.</span><span class="sxs-lookup"><span data-stu-id="12f6d-135">Identifier for the setting object.</span></span>

</dd> <dt>

<span data-ttu-id="12f6d-136">**Tiempo de espera**</span><span class="sxs-lookup"><span data-stu-id="12f6d-136">**Timeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12f6d-137">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="12f6d-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="12f6d-138">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="12f6d-138">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="12f6d-139">Calificadores: [**unidades**](standard-qualifiers.md) ("minutos")</span><span class="sxs-lookup"><span data-stu-id="12f6d-139">Qualifiers: [**units**](standard-qualifiers.md) ("Minutes")</span></span>
</dt> </dl>

<span data-ttu-id="12f6d-140">Número máximo de minutos antes de que un consumidor inicie una nueva instancia.</span><span class="sxs-lookup"><span data-stu-id="12f6d-140">Maximum number of minutes before a consumer starts a new instance.</span></span> <span data-ttu-id="12f6d-141">Si es 0 (cero), la propiedad **MaximumScripts** controla la duración del consumidor.</span><span class="sxs-lookup"><span data-stu-id="12f6d-141">If 0 (zero), the **MaximumScripts** property controls the consumer lifetime.</span></span> <span data-ttu-id="12f6d-142">El intervalo válido para el **tiempo de espera** es de 0 a 71.000 y el valor predeterminado es 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="12f6d-142">The valid range for **Timeout** is 0 through 71,000 and the default value is 0 (zero).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="12f6d-143">Observaciones</span><span class="sxs-lookup"><span data-stu-id="12f6d-143">Remarks</span></span>

<span data-ttu-id="12f6d-144">La instancia única de la clase **ScriptingStandardConsumerSetting** reside en el \\ espacio de nombres root cimv2.</span><span class="sxs-lookup"><span data-stu-id="12f6d-144">The single instance of the **ScriptingStandardConsumerSetting** class resides in the root\\cimv2 namespace.</span></span>

## <a name="requirements"></a><span data-ttu-id="12f6d-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12f6d-145">Requirements</span></span>



| <span data-ttu-id="12f6d-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="12f6d-146">Requirement</span></span> | <span data-ttu-id="12f6d-147">Value</span><span class="sxs-lookup"><span data-stu-id="12f6d-147">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="12f6d-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="12f6d-148">Minimum supported client</span></span><br/> | <span data-ttu-id="12f6d-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="12f6d-149">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="12f6d-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="12f6d-150">Minimum supported server</span></span><br/> | <span data-ttu-id="12f6d-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="12f6d-151">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="12f6d-152">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="12f6d-152">Namespace</span></span><br/>                | <span data-ttu-id="12f6d-153">\\Suscripción raíz</span><span class="sxs-lookup"><span data-stu-id="12f6d-153">Root\\subscription</span></span><br/>                                                          |
| <span data-ttu-id="12f6d-154">MOF</span><span class="sxs-lookup"><span data-stu-id="12f6d-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="12f6d-155"><dt>Scrcons. mof</dt></span><span class="sxs-lookup"><span data-stu-id="12f6d-155"><dt>Scrcons.mof</dt></span></span> </dl> |
| <span data-ttu-id="12f6d-156">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="12f6d-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12f6d-157"><dt>Scrcons.exe</dt></span><span class="sxs-lookup"><span data-stu-id="12f6d-157"><dt>Scrcons.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12f6d-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="12f6d-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12f6d-159">**Configuración de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="12f6d-159">**CIM\_Setting**</span></span>](/windows/desktop/CIMWin32Prov/cim-setting)
</dt> <dt>

[<span data-ttu-id="12f6d-160">Clases de consumidor estándar</span><span class="sxs-lookup"><span data-stu-id="12f6d-160">Standard Consumer Classes</span></span>](standard-consumer-classes.md)
</dt> <dt>

[<span data-ttu-id="12f6d-161">Ejecutar un script basado en un evento</span><span class="sxs-lookup"><span data-stu-id="12f6d-161">Running a Script Based on an Event</span></span>](running-a-script-based-on-an-event.md)
</dt> <dt>

[<span data-ttu-id="12f6d-162">Crear un consumidor lógico</span><span class="sxs-lookup"><span data-stu-id="12f6d-162">Creating a Logical Consumer</span></span>](creating-a-logical-consumer.md)
</dt> <dt>

[<span data-ttu-id="12f6d-163">Recepción de eventos en todo momento</span><span class="sxs-lookup"><span data-stu-id="12f6d-163">Receiving Events At All Times</span></span>](receiving-events-at-all-times.md)
</dt> <dt>

[<span data-ttu-id="12f6d-164">**\_\_EventConsumer**</span><span class="sxs-lookup"><span data-stu-id="12f6d-164">**\_\_EventConsumer**</span></span>](--eventconsumer.md)
</dt> </dl>

 

