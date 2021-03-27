---
description: Los proveedores clásicos deben usar Managed Object Format (MOF) para publicar el diseño de los datos de evento. Los consumidores pueden entonces leer el diseño publicado desde WMI en tiempo de ejecución y usarlo para leer los datos de evento.
ms.assetid: eb3d8422-2352-47cf-9825-cba9916791a9
title: Publicar el esquema de eventos para un proveedor clásico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21f51cfd30d0c9d73841ca906fb81e9d544dec88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360375"
---
# <a name="publishing-your-event-schema-for-a-classic-provider"></a><span data-ttu-id="36069-104">Publicar el esquema de eventos para un proveedor clásico</span><span class="sxs-lookup"><span data-stu-id="36069-104">Publishing Your Event Schema for a Classic Provider</span></span>

<span data-ttu-id="36069-105">Los proveedores [clásicos](about-event-tracing.md) deben usar [Managed Object Format](../wmisdk/managed-object-format--mof-.md) (MOF) para publicar el diseño de los datos de evento.</span><span class="sxs-lookup"><span data-stu-id="36069-105">[Classic](about-event-tracing.md) providers should use [Managed Object Format](../wmisdk/managed-object-format--mof-.md) (MOF) to publish the layout of their event data.</span></span> <span data-ttu-id="36069-106">Los consumidores pueden entonces leer el diseño publicado desde WMI en tiempo de ejecución y usarlo para leer los datos de evento.</span><span class="sxs-lookup"><span data-stu-id="36069-106">Consumers can then read the published layout from WMI at runtime and use it to read the event data.</span></span>

<span data-ttu-id="36069-107">Si utiliza MOF para publicar el diseño de los datos de eventos en WMI, normalmente crea los tres tipos de clases MOF siguientes en el espacio de \\ nombres WMI raíz:</span><span class="sxs-lookup"><span data-stu-id="36069-107">If you use MOF to publish the layout of your event data in WMI, you typically create the following three types of MOF classes in the root\\wmi namespace:</span></span>

-   [<span data-ttu-id="36069-108">Una clase MOF de proveedor</span><span class="sxs-lookup"><span data-stu-id="36069-108">A provider MOF class</span></span>](#provider-mof-classes)
-   [<span data-ttu-id="36069-109">Una o más clases MOF de eventos</span><span class="sxs-lookup"><span data-stu-id="36069-109">One or more event MOF classes</span></span>](#event-mof-classes)
-   [<span data-ttu-id="36069-110">Una o más clases de tipo de evento de MOF</span><span class="sxs-lookup"><span data-stu-id="36069-110">One or more event type MOF classes</span></span>](#event-type-mof-classes)

## <a name="provider-mof-classes"></a><span data-ttu-id="36069-111">Clases MOF de proveedor</span><span class="sxs-lookup"><span data-stu-id="36069-111">Provider MOF classes</span></span>

<span data-ttu-id="36069-112">Si publica el diseño de los datos de eventos, debe crear una clase MOF que identifique el proveedor.</span><span class="sxs-lookup"><span data-stu-id="36069-112">If you publish the layout of your event data, you must create a MOF class that identifies your provider.</span></span> <span data-ttu-id="36069-113">Esta clase debe derivar de la clase MOF **eventtracer** y debe estar vacía (no hay propiedades ni métodos).</span><span class="sxs-lookup"><span data-stu-id="36069-113">This class must derive from the **EventTrace** MOF class and must be empty (no properties or methods).</span></span> <span data-ttu-id="36069-114">La clase también debe incluir el calificador de **GUID** que identifica de forma única el proveedor.</span><span class="sxs-lookup"><span data-stu-id="36069-114">The class must also include the **Guid** qualifier which uniquely identifies the provider.</span></span> <span data-ttu-id="36069-115">Este es el mismo GUID que se usa al llamar a la función [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) para registrar el proveedor.</span><span class="sxs-lookup"><span data-stu-id="36069-115">This is the same GUID you use when you calling the [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) function to register your provider.</span></span>

## <a name="event-mof-classes"></a><span data-ttu-id="36069-116">Clases MOF de eventos</span><span class="sxs-lookup"><span data-stu-id="36069-116">Event MOF classes</span></span>

<span data-ttu-id="36069-117">Una clase MOF de eventos define una clase de eventos que proporciona el proveedor.</span><span class="sxs-lookup"><span data-stu-id="36069-117">An event MOF class defines a class of events that the provider provides.</span></span> <span data-ttu-id="36069-118">Esta clase se deriva de la clase MOF del proveedor y debe estar vacía (no hay propiedades ni métodos).</span><span class="sxs-lookup"><span data-stu-id="36069-118">This class derives from the provider MOF class and must be empty (no properties or methods).</span></span> <span data-ttu-id="36069-119">La clase también debe incluir el calificador de **GUID** que identifica de forma única la clase de eventos que sus clases secundarias definen.</span><span class="sxs-lookup"><span data-stu-id="36069-119">The class must also include the **Guid** qualifier which uniquely identifies the class of events that its child classes define.</span></span> <span data-ttu-id="36069-120">El proveedor utiliza este mismo GUID al establecer el miembro **GUID** de la estructura de [**\_ \_ encabezado del seguimiento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) .</span><span class="sxs-lookup"><span data-stu-id="36069-120">The provider uses this same GUID when setting the **Guid** member of the [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) structure.</span></span>

## <a name="event-type-mof-classes"></a><span data-ttu-id="36069-121">Clases de evento de tipo MOF</span><span class="sxs-lookup"><span data-stu-id="36069-121">Event type MOF classes</span></span>

<span data-ttu-id="36069-122">Una clase de tipo de evento MOF define los datos de evento reales.</span><span class="sxs-lookup"><span data-stu-id="36069-122">An event type MOF class defines the actual event data.</span></span> <span data-ttu-id="36069-123">Esta clase deriva de su clase MOF de evento primario.</span><span class="sxs-lookup"><span data-stu-id="36069-123">This class derives from its parent event MOF class.</span></span> <span data-ttu-id="36069-124">Al asignar un nombre a la clase MOF de tipo de evento, la Convención es usar el nombre de clase MOF de evento al principio del nombre de clase MOF del tipo de evento.</span><span class="sxs-lookup"><span data-stu-id="36069-124">When naming the event type MOF class, the convention is to use the event MOF class name at the beginning of the event type MOF class name.</span></span> <span data-ttu-id="36069-125">Por ejemplo, si el nombre de la clase MOF del evento es HWConfig y el tipo de evento clase MOF representa la información de la CPU, debe nombrar el tipo de evento MOF Class, HWConfig \_ CPU.</span><span class="sxs-lookup"><span data-stu-id="36069-125">For example, if the event MOF class name is HWConfig and the event type MOF class represents CPU information, you should name the event type MOF class, HWConfig\_CPU.</span></span>

<span data-ttu-id="36069-126">Use el calificador **EventType** en la clase MOF del tipo de evento para identificar el tipo de evento.</span><span class="sxs-lookup"><span data-stu-id="36069-126">Use the **EventType** qualifier on the event type MOF class to identify the event type.</span></span> <span data-ttu-id="36069-127">Si varios tipos de eventos utilizan los mismos datos de eventos, pueden usar la misma clase MOF.</span><span class="sxs-lookup"><span data-stu-id="36069-127">If multiple event types use the same event data, they can use the same MOF class.</span></span> <span data-ttu-id="36069-128">El proveedor usa el mismo valor de tipo de evento para identificar el evento al establecer el miembro **Class. Type** de la estructura de [**\_ \_ encabezado del seguimiento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) .</span><span class="sxs-lookup"><span data-stu-id="36069-128">The provider uses the same event type value to identify the event when setting the **Class.Type** member of the [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) structure.</span></span>

<span data-ttu-id="36069-129">La clase de tipo de evento MOF contiene propiedades.</span><span class="sxs-lookup"><span data-stu-id="36069-129">The event type MOF class contains properties.</span></span> <span data-ttu-id="36069-130">El orden de estas propiedades define el diseño de los datos de evento.</span><span class="sxs-lookup"><span data-stu-id="36069-130">The order of these properties define the layout of the event data.</span></span> <span data-ttu-id="36069-131">En la tabla siguiente se identifican los tipos de datos y calificadores que puede usar para definir las propiedades.</span><span class="sxs-lookup"><span data-stu-id="36069-131">The following table identifies the data types and qualifiers you can use to define the properties.</span></span> <span data-ttu-id="36069-132">Para obtener más información sobre los calificadores de propiedad y clase que se pueden usar, consulte [calificadores MOF de seguimiento de eventos](event-tracing-mof-qualifiers.md).</span><span class="sxs-lookup"><span data-stu-id="36069-132">For more information on the property and class qualifiers that you can use, see [Event Tracing MOF Qualifiers](event-tracing-mof-qualifiers.md).</span></span>



| <span data-ttu-id="36069-133">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="36069-133">Data type</span></span>              | <span data-ttu-id="36069-134">Calificadores</span><span class="sxs-lookup"><span data-stu-id="36069-134">Qualifiers</span></span>                        | <span data-ttu-id="36069-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="36069-135">Description</span></span>                                                                                                                                                                                                                                                                                                              |
|------------------------|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36069-136">**sint8**, **Uint8**</span><span class="sxs-lookup"><span data-stu-id="36069-136">**sint8**, **uint8**</span></span>   | <span data-ttu-id="36069-137">**Format**</span><span class="sxs-lookup"><span data-stu-id="36069-137">**Format**</span></span>                        | <span data-ttu-id="36069-138">Declara un entero decimal de 1 byte.</span><span class="sxs-lookup"><span data-stu-id="36069-138">Declares a 1-byte decimal integer.</span></span> <span data-ttu-id="36069-139">Para declarar un carácter ANSI, use el calificador de **formato** y establezca su valor en "c".</span><span class="sxs-lookup"><span data-stu-id="36069-139">To declare an ANSI character, use the **Format** qualifier and set its value to "c".</span></span>                                                                                                                                                                                                  |
| <span data-ttu-id="36069-140">**sint16**, **UInt16**</span><span class="sxs-lookup"><span data-stu-id="36069-140">**sint16**, **uint16**</span></span> | <span data-ttu-id="36069-141">**Format**</span><span class="sxs-lookup"><span data-stu-id="36069-141">**Format**</span></span>                        | <span data-ttu-id="36069-142">Declara un entero decimal de 2 bytes.</span><span class="sxs-lookup"><span data-stu-id="36069-142">Declares a 2-byte decimal integer.</span></span> <span data-ttu-id="36069-143">Para indicar que el número es un número hexadecimal, utilice el calificador de **formato** .</span><span class="sxs-lookup"><span data-stu-id="36069-143">To indicate the number is a hexadecimal number, use the **Format** qualifier.</span></span> <span data-ttu-id="36069-144">Por ejemplo, Format ("x").</span><span class="sxs-lookup"><span data-stu-id="36069-144">For example, format("x").</span></span>                                                                                                                                                                               |
| <span data-ttu-id="36069-145">**sint32**, **UInt32**</span><span class="sxs-lookup"><span data-stu-id="36069-145">**sint32**, **uint32**</span></span> | <span data-ttu-id="36069-146">**Format**</span><span class="sxs-lookup"><span data-stu-id="36069-146">**Format**</span></span>                        | <span data-ttu-id="36069-147">Declara un entero decimal de 4 bytes.</span><span class="sxs-lookup"><span data-stu-id="36069-147">Declares a 4-byte decimal integer.</span></span> <span data-ttu-id="36069-148">Para indicar que el número es un número hexadecimal, use el calificador de **formato** y establezca su valor en "x".</span><span class="sxs-lookup"><span data-stu-id="36069-148">To indicate the number is a hexadecimal number, use the **Format** qualifier and set its value to "x".</span></span>                                                                                                                                                                                |
| <span data-ttu-id="36069-149">**sint64**, **UInt64**</span><span class="sxs-lookup"><span data-stu-id="36069-149">**sint64**, **uint64**</span></span> | <span data-ttu-id="36069-150">**Format**</span><span class="sxs-lookup"><span data-stu-id="36069-150">**Format**</span></span>                        | <span data-ttu-id="36069-151">Declara un entero decimal de 8 bytes.</span><span class="sxs-lookup"><span data-stu-id="36069-151">Declares a 8-byte decimal integer.</span></span> <span data-ttu-id="36069-152">Para indicar que el número es un número hexadecimal, use el calificador de **formato** y establezca su valor en "x".</span><span class="sxs-lookup"><span data-stu-id="36069-152">To indicate the number is a hexadecimal number, use the **Format** qualifier and set its value to "x".</span></span>                                                                                                                                                                                |
| <span data-ttu-id="36069-153">**boolean**</span><span class="sxs-lookup"><span data-stu-id="36069-153">**boolean**</span></span>            |                                   | <span data-ttu-id="36069-154">Declara un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="36069-154">Declares a Boolean value.</span></span> <span data-ttu-id="36069-155">El consumidor de eventos debe interpretar el valor como BOOLEANO (entero de 4 bytes).</span><span class="sxs-lookup"><span data-stu-id="36069-155">The event consumer should interpret the value as BOOL (4-byte integer).</span></span>                                                                                                                                                                                                                        |
| <span data-ttu-id="36069-156">**char16**</span><span class="sxs-lookup"><span data-stu-id="36069-156">**char16**</span></span>             |                                   | <span data-ttu-id="36069-157">Declara un carácter ancho.</span><span class="sxs-lookup"><span data-stu-id="36069-157">Declares a wide character.</span></span> <span data-ttu-id="36069-158">El consumidor de eventos debe interpretar las matrices de char16 en eventos de kernel como cadenas de caracteres anchos.</span><span class="sxs-lookup"><span data-stu-id="36069-158">The event consumer should interpret char16 arrays in kernel events as wide character strings.</span></span> <span data-ttu-id="36069-159">(Utilice el tamaño de la matriz para copiar la cadena.</span><span class="sxs-lookup"><span data-stu-id="36069-159">(Use the array size to copy the string.</span></span> <span data-ttu-id="36069-160">Algunas cadenas pueden contener caracteres NULOs iniciales).</span><span class="sxs-lookup"><span data-stu-id="36069-160">Some strings may contain leading NULL characters.)</span></span>                                                                                                      |
| <span data-ttu-id="36069-161">**object**</span><span class="sxs-lookup"><span data-stu-id="36069-161">**object**</span></span>             | <span data-ttu-id="36069-162">**Extensión**</span><span class="sxs-lookup"><span data-stu-id="36069-162">**Extension**</span></span>                     | <span data-ttu-id="36069-163">Declara un BLOB binario.</span><span class="sxs-lookup"><span data-stu-id="36069-163">Declares a binary blob.</span></span> <span data-ttu-id="36069-164">El calificador de **extensión** indica el tipo de datos en el BLOB.</span><span class="sxs-lookup"><span data-stu-id="36069-164">The **Extension** qualifier indicates the type of data in the blob.</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="36069-165">**string**</span><span class="sxs-lookup"><span data-stu-id="36069-165">**string**</span></span>             | <span data-ttu-id="36069-166">**Formato**, **StringTermination**</span><span class="sxs-lookup"><span data-stu-id="36069-166">**Format**, **StringTermination**</span></span> | <span data-ttu-id="36069-167">Declara un valor de cadena.</span><span class="sxs-lookup"><span data-stu-id="36069-167">Declares a string value.</span></span> <span data-ttu-id="36069-168">Para indicar que la cadena es una cadena de caracteres anchos, utilice el calificador de **formato** y establezca su valor en "w".</span><span class="sxs-lookup"><span data-stu-id="36069-168">To indicate the string is a wide-character string use the **Format** qualifier and set its value to "w".</span></span> <span data-ttu-id="36069-169">La cadena se considera una cadena ANSI si no se especifica el calificador de **formato** .</span><span class="sxs-lookup"><span data-stu-id="36069-169">The string is considered an ANSI string if you do not specify the **Format** qualifier.</span></span> <span data-ttu-id="36069-170">Para indicar cómo se termina la cadena, use el calificador **StringTermination** .</span><span class="sxs-lookup"><span data-stu-id="36069-170">To indicate how the string is terminated, use the **StringTermination** qualifier.</span></span> <br/> |



 

<span data-ttu-id="36069-171">Para especificar una matriz, puede usar corchetes, \[ \] .</span><span class="sxs-lookup"><span data-stu-id="36069-171">To specify an array, you can use square brackets, \[\].</span></span> <span data-ttu-id="36069-172">Los corchetes pueden incluir el tamaño de la matriz.</span><span class="sxs-lookup"><span data-stu-id="36069-172">The square brackets can include the size of the array.</span></span> <span data-ttu-id="36069-173">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="36069-173">For example:</span></span>

`[WmiDataId(1), read] uint8 MyGuid[16];`

<span data-ttu-id="36069-174">También puede usar el calificador **Max** para especificar el tamaño de una matriz.</span><span class="sxs-lookup"><span data-stu-id="36069-174">You can also use the **Max** qualifier to specify the size of an array.</span></span> <span data-ttu-id="36069-175">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="36069-175">For example:</span></span>

`[WmiDataId(1), Max(16), read] uint8 MyGuid[];`

<span data-ttu-id="36069-176">Si incluye el tamaño de la matriz entre corchetes, el compilador MOF genera el calificador Max.</span><span class="sxs-lookup"><span data-stu-id="36069-176">If you include the size of the array in the square brackets, the MOF compiler generates the Max qualifier for you.</span></span>

<span data-ttu-id="36069-177">Es importante que use el calificador de **Descripción** para cada propiedad.</span><span class="sxs-lookup"><span data-stu-id="36069-177">It is important that you use the **Description** qualifier for each property.</span></span> <span data-ttu-id="36069-178">La descripción debe contener un nombre para mostrar que el consumidor pueda usar al mostrar los valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="36069-178">The description should contain a display name that the consumer can use when displaying the property values.</span></span>

<span data-ttu-id="36069-179">En el ejemplo siguiente se muestra el contenido de un archivo MOF que describe una clase MOF de proveedor, evento y tipo de evento.</span><span class="sxs-lookup"><span data-stu-id="36069-179">The following example shows the contents of a MOF file that describes a provider, event, and event type MOF class.</span></span>

``` syntax
#pragma namespace("\\\\.\\root\\wmi")

[dynamic: ToInstance, Description("Defines my event provider"),
 Guid("{7C214FB1-9CAC-4b8d-BAED-7BF48BF63BB3}")]
class MyProvider : EventTrace
{
};

[dynamic: ToInstance, Description("Defines a category of events that my provider logs."): Amended,
 Guid("{B49D5931-AD85-4070-B1B1-3F81F1532875}")]
class MyCategory : MyProvider
{
};

[dynamic: ToInstance, Description("Defines an event within the category of events that my provider logs."): Amended,
 EventType(1)]
class MyCategory_MyEvent : MyCategory
{
    [WmiDataId(1), Description("Cost factor"): Amended, read] sint32 Cost;
    [WmiDataId(2), Description("Index values"): Amended, read] uint32 Indices[3];
    [WmiDataId(3), Description("Signature"): Amended, read, StringTermination("NullTerminated"), Format("w")] string Signature;
    [WmiDataId(4), Description("Is complete copy"): Amended, read] boolean IsComplete;
    [WmiDataId(5), Description("Class identifier"): Amended, read, Extension("Guid")] object ID;
};
```

<span data-ttu-id="36069-180">Tenga en cuenta que los nombres de clases MOF de proveedor, evento y tipo de evento deben ser únicos en todo el espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="36069-180">Note that the provider, event, and event type MOF class names must be unique within the entire namespace.</span></span> <span data-ttu-id="36069-181">Para evitar conflictos de nombres, debe usar un nombre único y descriptivo para todos los nombres de clase.</span><span class="sxs-lookup"><span data-stu-id="36069-181">To avoid naming conflicts, you should use unique and descriptive name for all class names.</span></span> <span data-ttu-id="36069-182">Las propiedades de clase también deben ser descriptivas y únicas dentro de su jerarquía de clases; una clase secundaria que contenga el mismo nombre de propiedad que una clase primaria sobrescribe la propiedad de la clase primaria.</span><span class="sxs-lookup"><span data-stu-id="36069-182">Class properties should also be descriptive and unique within its class hierarchy—a child class that contains the same property name as a parent class overwrites the property of the parent class.</span></span>

<span data-ttu-id="36069-183">Después de definir las clases MOF, utilice el compilador MOF para generar el esquema de eventos y agregarlo al repositorio CIM.</span><span class="sxs-lookup"><span data-stu-id="36069-183">After defining your MOF classes, use the MOF compiler to generate your event schema and add it to the CIM repository.</span></span> <span data-ttu-id="36069-184">Los consumidores pueden entonces leer el esquema del repositorio y leer los datos de eventos mediante programación.</span><span class="sxs-lookup"><span data-stu-id="36069-184">Consumers can then read the schema from the repository and programmatically read the event data.</span></span> <span data-ttu-id="36069-185">Para obtener una descripción completa de la sintaxis MOF y usar el compilador MOF (Mofcomp.exe) para agregar las clases MOF al repositorio CIM, vea [Managed Object Format](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="36069-185">For a complete description of the MOF syntax and using the MOF compiler (Mofcomp.exe) to add your MOF classes to the CIM repository, see [Managed Object Format](../wmisdk/managed-object-format--mof-.md).</span></span> <span data-ttu-id="36069-186">Para obtener información sobre el uso de Wbemtest.exe para tener acceso al repositorio CIM, consulte [instrumental de administración de Windows](../wmisdk/wmi-start-page.md) (WMI).</span><span class="sxs-lookup"><span data-stu-id="36069-186">For information on using Wbemtest.exe to access the CIM repository, see [Windows Management Instrumentation](../wmisdk/wmi-start-page.md) (WMI).</span></span>

## <a name="versioning-mof-class"></a><span data-ttu-id="36069-187">Control de versiones de la clase MOF</span><span class="sxs-lookup"><span data-stu-id="36069-187">Versioning MOF class</span></span>

<span data-ttu-id="36069-188">Si agrega o cambia un tipo de evento de clase MOF, la Convención es la versión de la clase MOF de eventos y sus clases MOF de tipo de evento secundario.</span><span class="sxs-lookup"><span data-stu-id="36069-188">If you add or change an event type MOF class, the convention is to version both the event MOF class and its child event type MOF classes.</span></span> <span data-ttu-id="36069-189">Para la versión de la clase MOF del evento actual, anexe \_ vn al nombre de clase, donde n es un número incremental que empieza en 0.</span><span class="sxs-lookup"><span data-stu-id="36069-189">To version the current event MOF class, append \_Vn to the class name, where n is an incremental number starting at 0.</span></span> <span data-ttu-id="36069-190">Si esta es la primera revisión de la clase, anexe \_ V0 al nombre de la clase.</span><span class="sxs-lookup"><span data-stu-id="36069-190">If this is the first revision to the class, append \_V0 to the class name.</span></span> <span data-ttu-id="36069-191">También debe agregar el calificador **EventVersion** a la clase.</span><span class="sxs-lookup"><span data-stu-id="36069-191">You must also add the **EventVersion** qualifier to the class.</span></span> <span data-ttu-id="36069-192">Use el mismo número de versión que usó en el nombre de clase para el valor del calificador **EventVersion** .</span><span class="sxs-lookup"><span data-stu-id="36069-192">Use the same version number you used in the class name for the value of the **EventVersion** qualifier.</span></span>

<span data-ttu-id="36069-193">La nueva versión de la clase MOF de eventos debe usar el mismo nombre y calificador de **GUID** que la clase original.</span><span class="sxs-lookup"><span data-stu-id="36069-193">The new version of the event MOF class must use the same name and **Guid** qualifier as the original class.</span></span> <span data-ttu-id="36069-194">La nueva clase puede agregar opcionalmente el calificador **EventVersion** .</span><span class="sxs-lookup"><span data-stu-id="36069-194">The new class may optionally add the **EventVersion** qualifier.</span></span> <span data-ttu-id="36069-195">La clase MOF de eventos que no contiene el calificador **EventVersion** se considera la versión más reciente, o si todas las versiones de la clase contienen un calificador **EventVersion** , la clase con el número de versión más alto se considera la versión más reciente.</span><span class="sxs-lookup"><span data-stu-id="36069-195">The event MOF class that does not contain the **EventVersion** qualifier is considered the latest version, or if all the versions of the class contain an **EventVersion** qualifier, then the class with the highest version number is considered the latest version.</span></span> <span data-ttu-id="36069-196">El proveedor utiliza el miembro **Class. version** de la estructura de [**encabezado del \_ seguimiento \_ de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) para identificar la versión del evento incluido en el seguimiento.</span><span class="sxs-lookup"><span data-stu-id="36069-196">The provider uses the **Class.Version** member of the [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) structure to identify the version of the event included in the trace.</span></span>

<span data-ttu-id="36069-197">En el ejemplo siguiente se muestra cómo la versión de una clase MOF de eventos.</span><span class="sxs-lookup"><span data-stu-id="36069-197">The following example shows how to version an event MOF class.</span></span>

``` syntax
#pragma namespace("\\\\.\\root\\wmi")
#pragma classflags("forceupdate")

[dynamic: ToInstance, Description("Defines my event provider"),
 Guid("{7C214FB1-9CAC-4b8d-BAED-7BF48BF63BB3}")]
class MyProvider : EventTrace
{
};

[dynamic: ToInstance, Description("Defines a category of events that my provider logs."),
 Guid("{B49D5931-AD85-4070-B1B1-3F81F1532875}"),
 EventVersion(1)]
class MyCategory : MyProvider
{
};

[dynamic: ToInstance, Description("Defines an event within the category of events that my provider logs."): Amended,
 EventType(1),
 EventName("MyEvent")]
class MyCategory_MyEvent : MyCategory
{
    [WmiDataId(1), Description("Cost factor"): Amended, read] sint32 Cost;
    [WmiDataId(2), Description("Index values"): Amended, read] uint32 Indices[3];
    [WmiDataId(3), Description("Signature"): Amended, read, StringTermination("NullTerminated"), Format("w")] string Signature;
    [WmiDataId(4), Description("Is complete copy"): Amended, read] boolean IsComplete;
    [WmiDataId(5), Description("Identifier"): Amended, read, Extension("Guid")] object ID;
    [WmiDataId(6), Description("Buffer Size"): Amended, read] uint32 Size;
};

[dynamic: ToInstance, Description("Defines a category of events that my provider logs."): Amended,
 Guid("{B49D5931-AD85-4070-B1B1-3F81F1532875}"),
 EventVersion(0)]
class MyCategory_V0 : MyProvider
{
};

[dynamic: ToInstance, Description("Defines an event within the category of events that my provider logs."): Amended,
 EventType(1)]
class MyCategory_V0_MyEvent : MyCategory_V0
{
    [WmiDataId(1), Description("Cost factor"): Amended, read] sint32 Cost;
    [WmiDataId(2), Description("Index values"): Amended, read] uint32 Indices[3];
    [WmiDataId(3), Description("Signature"): Amended, read, StringTermination("NullTerminated"), Format("w")] string Signature;
    [WmiDataId(4), Description("Is complete copy"): Amended, read] boolean IsComplete;
    [WmiDataId(5), Description("Identifier"): Amended, read, Extension("Guid")] object ID;
};
```

 

 
