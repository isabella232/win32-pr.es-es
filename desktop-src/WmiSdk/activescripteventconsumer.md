---
description: Ejecuta un script predefinido en un lenguaje de scripting arbitrario cuando se le entrega un evento.
ms.assetid: 2c0aa216-4255-49ff-9bbd-d6c62b5b9139
ms.tgt_platform: multiple
title: Clase ActiveScriptEventConsumer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ActiveScriptEventConsumer
- ActiveScriptEventConsumer.CreatorSID
- ActiveScriptEventConsumer.KillTimeout
- ActiveScriptEventConsumer.MachineName
- ActiveScriptEventConsumer.MaximumQueueSize
- ActiveScriptEventConsumer.Name
- ActiveScriptEventConsumer.ScriptingEngine
- ActiveScriptEventConsumer.ScriptFileName
- ActiveScriptEventConsumer.ScriptText
api_type:
- DllExport
api_location:
- Scrcons.exe
ms.openlocfilehash: 11e2886fd5d0804946433e102e24617df768dcec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716703"
---
# <a name="activescripteventconsumer-class"></a><span data-ttu-id="25041-103">Clase ActiveScriptEventConsumer</span><span class="sxs-lookup"><span data-stu-id="25041-103">ActiveScriptEventConsumer class</span></span>

<span data-ttu-id="25041-104">La clase **ActiveScriptEventConsumer** ejecuta un script predefinido en un lenguaje de scripting arbitrario cuando se le entrega un evento.</span><span class="sxs-lookup"><span data-stu-id="25041-104">The **ActiveScriptEventConsumer** class runs a predefined script in an arbitrary scripting language when an event is delivered to it.</span></span> <span data-ttu-id="25041-105">Esta clase es uno de los consumidores de eventos estándar que proporciona WMI.</span><span class="sxs-lookup"><span data-stu-id="25041-105">This class is one of the standard event consumers that WMI provides.</span></span> <span data-ttu-id="25041-106">Para obtener más información, consulte [supervisión y respuesta a eventos con consumidores estándar](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="25041-106">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>


```cmd
Mofcomp -n:root\<namespace> scrcons.mof
```



<span data-ttu-id="25041-107">Puede configurar el rendimiento de todas las instancias de **ActiveScriptEventConsumer** en un sistema mediante el establecimiento de los valores de la propiedad [**timeout**](scriptingstandardconsumersetting.md) o **MaximumScripts** en la instancia única de **ScriptingStandardConsumerSetting**.</span><span class="sxs-lookup"><span data-stu-id="25041-107">You can configure the performance of all instances of **ActiveScriptEventConsumer** on a system by setting the values of either the [**Timeout**](scriptingstandardconsumersetting.md) or **MaximumScripts** property in the single instance of **ScriptingStandardConsumerSetting**.</span></span>

## <a name="syntax"></a><span data-ttu-id="25041-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="25041-108">Syntax</span></span>

``` syntax
[AMENDMENT]
class ActiveScriptEventConsumer : __EventConsumer
{
  uint8  CreatorSID[] = {1,1,0,0,0,0,0,5,18,0,0,0};
  uint32 KillTimeout = 0;
  string MachineName;
  uint32 MaximumQueueSize;
  string Name;
  string ScriptingEngine;
  string ScriptFileName;
  string ScriptText;
};
```

## <a name="members"></a><span data-ttu-id="25041-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="25041-109">Members</span></span>

<span data-ttu-id="25041-110">La clase **ActiveScriptEventConsumer** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="25041-110">The **ActiveScriptEventConsumer** class has these types of members:</span></span>

-   [<span data-ttu-id="25041-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="25041-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="25041-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="25041-112">Properties</span></span>

<span data-ttu-id="25041-113">La clase **ActiveScriptEventConsumer** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="25041-113">The **ActiveScriptEventConsumer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="25041-114">**CreatorSID**</span><span class="sxs-lookup"><span data-stu-id="25041-114">**CreatorSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25041-115">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="25041-115">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="25041-116">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="25041-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25041-117">Matriz que representa el identificador de seguridad (SID), que identifica de forma única al creador del consumidor de eventos de script activo.</span><span class="sxs-lookup"><span data-stu-id="25041-117">Array that represents the security identifier (SID), which uniquely identifies the creator of the Active Script Event consumer.</span></span> <span data-ttu-id="25041-118">Esta propiedad se hereda de [**\_ \_ EventConsumer**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="25041-118">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="25041-119">**KillTimeout**</span><span class="sxs-lookup"><span data-stu-id="25041-119">**KillTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25041-120">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="25041-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="25041-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="25041-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25041-122">Número, en segundos, que se permite ejecutar el script.</span><span class="sxs-lookup"><span data-stu-id="25041-122">Number, in seconds, that the script is allowed to run.</span></span> <span data-ttu-id="25041-123">Si es 0 (cero), que es el valor predeterminado, el script no se termina.</span><span class="sxs-lookup"><span data-stu-id="25041-123">If 0 (zero), which is the default, the script is not terminated.</span></span>

</dd> <dt>

<span data-ttu-id="25041-124">**MachineName**</span><span class="sxs-lookup"><span data-stu-id="25041-124">**MachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25041-125">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="25041-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="25041-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="25041-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25041-127">Nombre del equipo al que WMI envía eventos.</span><span class="sxs-lookup"><span data-stu-id="25041-127">Name of the computer to which WMI sends events.</span></span> <span data-ttu-id="25041-128">Por Convención de los consumidores estándar de Microsoft, el consumidor de script no se puede ejecutar de forma remota.</span><span class="sxs-lookup"><span data-stu-id="25041-128">By convention of Microsoft standard consumers, the script consumer cannot be run remotely.</span></span> <span data-ttu-id="25041-129">Los consumidores de terceros también pueden usar esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="25041-129">Third-party consumers can also use this property.</span></span> <span data-ttu-id="25041-130">Esta propiedad se hereda de [**\_ \_ EventConsumer**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="25041-130">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="25041-131">**MaximumQueueSize**</span><span class="sxs-lookup"><span data-stu-id="25041-131">**MaximumQueueSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25041-132">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="25041-132">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="25041-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="25041-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25041-134">Cola máxima, en bytes, para el consumidor de eventos de script activo.</span><span class="sxs-lookup"><span data-stu-id="25041-134">Maximum queue, in bytes, for the Active Script Event consumer.</span></span> <span data-ttu-id="25041-135">Esta propiedad se hereda de [**\_ \_ EventConsumer**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="25041-135">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="25041-136">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="25041-136">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25041-137">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="25041-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="25041-138">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="25041-138">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="25041-139">Calificadores: [ **clave**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="25041-139">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="25041-140">Identificador único para el consumidor de eventos.</span><span class="sxs-lookup"><span data-stu-id="25041-140">Unique identifier for the event consumer.</span></span> <span data-ttu-id="25041-141">Si cambia el nombre del consumidor, el resultado son dos consumidores iguales que tienen nombres diferentes.</span><span class="sxs-lookup"><span data-stu-id="25041-141">If you rename the consumer, the result is two equal consumers that have different names.</span></span>

</dd> <dt>

<span data-ttu-id="25041-142">**ScriptFileName**</span><span class="sxs-lookup"><span data-stu-id="25041-142">**ScriptFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25041-143">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="25041-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="25041-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="25041-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25041-145">Nombre del archivo desde el que se lee el texto del script, diseñado como una alternativa a especificar el texto del script en la propiedad **ScriptText** .</span><span class="sxs-lookup"><span data-stu-id="25041-145">Name of the file from which the script text is read, intended as an alternative to specifying the text of the script in the **ScriptText** property.</span></span> <span data-ttu-id="25041-146">Esta propiedad debe ser **null** si la propiedad **ScriptText** no es **null**.</span><span class="sxs-lookup"><span data-stu-id="25041-146">This property must be **NULL** if the **ScriptText** property is not **NULL**.</span></span>

> [!Note]  
> <span data-ttu-id="25041-147">Cuando se especifica **ScriptFileName**, es importante proteger el archivo ejecutable que se está iniciando.</span><span class="sxs-lookup"><span data-stu-id="25041-147">When you specify the **ScriptFileName**, it is important to secure the executable that you are launching.</span></span> <span data-ttu-id="25041-148">Si el archivo ejecutable no está en una ubicación segura o está protegido con una lista de control de acceso (ACL) segura, cualquiera puede reemplazar el ejecutable por otro diferente.</span><span class="sxs-lookup"><span data-stu-id="25041-148">If the executable is not in a secure location or secured with a strong access control list (ACL), anyone can replace the executable with a different one.</span></span> <span data-ttu-id="25041-149">Para obtener más información acerca de las ACL, vea [crear un descriptor de seguridad (SD) para un nuevo objeto en C++](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span><span class="sxs-lookup"><span data-stu-id="25041-149">For more information about ACLs, see [Creating a Security Descriptor (SD) for a New Object in C++](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span></span>

 

</dd> <dt>

<span data-ttu-id="25041-150">**ScriptingEngine**</span><span class="sxs-lookup"><span data-stu-id="25041-150">**ScriptingEngine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25041-151">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="25041-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="25041-152">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="25041-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25041-153">Nombre del motor de scripting que se va a usar, por ejemplo, "VBScript".</span><span class="sxs-lookup"><span data-stu-id="25041-153">Name of the scripting engine to use, for example, "VBScript".</span></span> <span data-ttu-id="25041-154">Esta propiedad no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="25041-154">This property cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="25041-155">**ScriptText**</span><span class="sxs-lookup"><span data-stu-id="25041-155">**ScriptText**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25041-156">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="25041-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="25041-157">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="25041-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25041-158">Texto del script que se expresa en un lenguaje conocido por el motor de scripting.</span><span class="sxs-lookup"><span data-stu-id="25041-158">Text of the script that is expressed in a language known to the scripting engine.</span></span> <span data-ttu-id="25041-159">Esta propiedad debe ser **null** si la propiedad **ScriptFileName** no es **null**.</span><span class="sxs-lookup"><span data-stu-id="25041-159">This property must be **NULL** if the **ScriptFileName** property is not **NULL**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="25041-160">Observaciones</span><span class="sxs-lookup"><span data-stu-id="25041-160">Remarks</span></span>

<span data-ttu-id="25041-161">Esta clase se deriva de la clase abstracta [**\_ \_ EventConsumer**](--eventconsumer.md) .</span><span class="sxs-lookup"><span data-stu-id="25041-161">This class is derived from the [**\_\_EventConsumer**](--eventconsumer.md) abstract class.</span></span> <span data-ttu-id="25041-162">Se encuentra en el espacio de \\ nombres de la suscripción raíz.</span><span class="sxs-lookup"><span data-stu-id="25041-162">It is located in the root\\subscription namespace.</span></span>

<span data-ttu-id="25041-163">Cuando se especifica el texto de un script en la instancia de consumidor de eventos, el script tiene acceso a la instancia de evento en la variable de entorno de script **TargetEvent**.</span><span class="sxs-lookup"><span data-stu-id="25041-163">When the text of a script is specified in the event consumer instance, the script has access to the event instance in the script environment variable **TargetEvent**.</span></span>

<span data-ttu-id="25041-164">Los scripts se ejecutan en el contexto de seguridad de LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="25041-164">The scripts run in the LocalSystem security context.</span></span> <span data-ttu-id="25041-165">Como medida de seguridad, solo un administrador del sistema local o un administrador de dominio puede configurar el consumidor de scripting.</span><span class="sxs-lookup"><span data-stu-id="25041-165">As a security measure, only a local system administrator or a domain administrator can configure the scripting consumer.</span></span> <span data-ttu-id="25041-166">Los derechos de acceso no se comprueban hasta el tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="25041-166">Access rights are not checked until run time.</span></span> <span data-ttu-id="25041-167">Una vez configurado el consumidor, cualquier usuario puede desencadenar el evento que provoca el script.</span><span class="sxs-lookup"><span data-stu-id="25041-167">After the consumer is configured, any user can trigger the event that causes the script to .</span></span>

<span data-ttu-id="25041-168">Un error al cargar el motor de scripting o analizar y validar el script se considera un error.</span><span class="sxs-lookup"><span data-stu-id="25041-168">Failure to load the scripting engine or parse and validate the script is considered a failure.</span></span> <span data-ttu-id="25041-169">Los códigos de retorno de error del script y el final del script mediante un tiempo de espera también se consideran errores.</span><span class="sxs-lookup"><span data-stu-id="25041-169">Error return codes from the script and terminating the script by using a time-out are also considered failures.</span></span>

<span data-ttu-id="25041-170">El valor de **ScriptText** o **ScriptFileName** debe ser not **null**.</span><span class="sxs-lookup"><span data-stu-id="25041-170">Either **ScriptText** or **ScriptFileName** must be not **NULL**.</span></span> <span data-ttu-id="25041-171">Si ambas propiedades son **null** o not **null**, se genera un error.</span><span class="sxs-lookup"><span data-stu-id="25041-171">If both properties are **NULL** or not **NULL**, an error is generated.</span></span>

<span data-ttu-id="25041-172">Cuando WMI se ejecuta como un servicio, los scripts ejecutados por **ActiveScriptEventConsumer** no generan resultados de pantalla.</span><span class="sxs-lookup"><span data-stu-id="25041-172">When WMI is run as a service, scripts run by **ActiveScriptEventConsumer** do not generate screen output.</span></span> <span data-ttu-id="25041-173">Los scripts que usan **MsgBox** se ejecutan, pero no muestran información en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="25041-173">Scripts that use **MsgBox** do run, but they do not display information on the screen.</span></span> <span data-ttu-id="25041-174">No se admite la ejecución del servicio WMI como un archivo ejecutable, pero WMI permite que los scripts que utilizan la función **MsgBox** muestren la salida o acepten datos proporcionados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="25041-174">Running the WMI service as an executable file is not supported, but WMI allows scripts that use the **MsgBox** function to display output or accept user input.</span></span> <span data-ttu-id="25041-175">No se puede usar ninguno de los métodos proporcionados por el objeto [Wscript](/previous-versions//at5ydy31(v=vs.85)) porque **ActiveScriptEventConsumer** no utiliza Windows Script Host (WSH).</span><span class="sxs-lookup"><span data-stu-id="25041-175">None of the methods provided by the [WScript](/previous-versions//at5ydy31(v=vs.85)) object can be used because **ActiveScriptEventConsumer** does not use Windows Script Host (WSH).</span></span>

## <a name="examples"></a><span data-ttu-id="25041-176">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="25041-176">Examples</span></span>

<span data-ttu-id="25041-177">El ejemplo de [creación de registro de eventos de WMI permanente para supervisar archivos](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) de PowerShell en la galería de TechNet usa **ActiveScriptEventConsumer** como parte de un script complejo para configurar un registro de eventos de WMI permanente.</span><span class="sxs-lookup"><span data-stu-id="25041-177">The [Create Permanent WMI Event registration to monitor files](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) PowerShell example on TechNet Gallery uses **ActiveScriptEventConsumer** as part of a complex script to set up a permanent WMI event registration.</span></span>

## <a name="requirements"></a><span data-ttu-id="25041-178">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25041-178">Requirements</span></span>



| <span data-ttu-id="25041-179">Requisito</span><span class="sxs-lookup"><span data-stu-id="25041-179">Requirement</span></span> | <span data-ttu-id="25041-180">Value</span><span class="sxs-lookup"><span data-stu-id="25041-180">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="25041-181">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25041-181">Minimum supported client</span></span><br/> | <span data-ttu-id="25041-182">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="25041-182">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="25041-183">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25041-183">Minimum supported server</span></span><br/> | <span data-ttu-id="25041-184">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="25041-184">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="25041-185">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="25041-185">Namespace</span></span><br/>                | <span data-ttu-id="25041-186">\\Suscripción raíz</span><span class="sxs-lookup"><span data-stu-id="25041-186">Root\\subscription</span></span><br/>                                                          |
| <span data-ttu-id="25041-187">MOF</span><span class="sxs-lookup"><span data-stu-id="25041-187">MOF</span></span><br/>                      | <dl> <span data-ttu-id="25041-188"><dt>Scrcons. mof</dt></span><span class="sxs-lookup"><span data-stu-id="25041-188"><dt>Scrcons.mof</dt></span></span> </dl> |
| <span data-ttu-id="25041-189">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="25041-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="25041-190"><dt>Scrcons.exe</dt></span><span class="sxs-lookup"><span data-stu-id="25041-190"><dt>Scrcons.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25041-191">Vea también</span><span class="sxs-lookup"><span data-stu-id="25041-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25041-192">Clases de consumidor estándar</span><span class="sxs-lookup"><span data-stu-id="25041-192">Standard Consumer Classes</span></span>](standard-consumer-classes.md)
</dt> <dt>

[<span data-ttu-id="25041-193">Ejecutar un script basado en un evento</span><span class="sxs-lookup"><span data-stu-id="25041-193">Running a Script Based on an Event</span></span>](running-a-script-based-on-an-event.md)
</dt> <dt>

[<span data-ttu-id="25041-194">Recepción de eventos en todo momento</span><span class="sxs-lookup"><span data-stu-id="25041-194">Receiving Events At All Times</span></span>](receiving-events-at-all-times.md)
</dt> <dt>

[<span data-ttu-id="25041-195">Crear un consumidor lógico</span><span class="sxs-lookup"><span data-stu-id="25041-195">Creating a Logical Consumer</span></span>](creating-a-logical-consumer.md)
</dt> <dt>

[<span data-ttu-id="25041-196">**\_\_EventConsumer**</span><span class="sxs-lookup"><span data-stu-id="25041-196">**\_\_EventConsumer**</span></span>](--eventconsumer.md)
</dt> <dt>

[<span data-ttu-id="25041-197">**ScriptingStandardConsumerSetting**</span><span class="sxs-lookup"><span data-stu-id="25041-197">**ScriptingStandardConsumerSetting**</span></span>](scriptingstandardconsumersetting.md)
</dt> </dl>

 

