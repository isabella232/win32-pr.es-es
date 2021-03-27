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
# <a name="publishing-your-event-schema-for-a-classic-provider"></a>Publicar el esquema de eventos para un proveedor clásico

Los proveedores [clásicos](about-event-tracing.md) deben usar [Managed Object Format](../wmisdk/managed-object-format--mof-.md) (MOF) para publicar el diseño de los datos de evento. Los consumidores pueden entonces leer el diseño publicado desde WMI en tiempo de ejecución y usarlo para leer los datos de evento.

Si utiliza MOF para publicar el diseño de los datos de eventos en WMI, normalmente crea los tres tipos de clases MOF siguientes en el espacio de \\ nombres WMI raíz:

-   [Una clase MOF de proveedor](#provider-mof-classes)
-   [Una o más clases MOF de eventos](#event-mof-classes)
-   [Una o más clases de tipo de evento de MOF](#event-type-mof-classes)

## <a name="provider-mof-classes"></a>Clases MOF de proveedor

Si publica el diseño de los datos de eventos, debe crear una clase MOF que identifique el proveedor. Esta clase debe derivar de la clase MOF **eventtracer** y debe estar vacía (no hay propiedades ni métodos). La clase también debe incluir el calificador de **GUID** que identifica de forma única el proveedor. Este es el mismo GUID que se usa al llamar a la función [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) para registrar el proveedor.

## <a name="event-mof-classes"></a>Clases MOF de eventos

Una clase MOF de eventos define una clase de eventos que proporciona el proveedor. Esta clase se deriva de la clase MOF del proveedor y debe estar vacía (no hay propiedades ni métodos). La clase también debe incluir el calificador de **GUID** que identifica de forma única la clase de eventos que sus clases secundarias definen. El proveedor utiliza este mismo GUID al establecer el miembro **GUID** de la estructura de [**\_ \_ encabezado del seguimiento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) .

## <a name="event-type-mof-classes"></a>Clases de evento de tipo MOF

Una clase de tipo de evento MOF define los datos de evento reales. Esta clase deriva de su clase MOF de evento primario. Al asignar un nombre a la clase MOF de tipo de evento, la Convención es usar el nombre de clase MOF de evento al principio del nombre de clase MOF del tipo de evento. Por ejemplo, si el nombre de la clase MOF del evento es HWConfig y el tipo de evento clase MOF representa la información de la CPU, debe nombrar el tipo de evento MOF Class, HWConfig \_ CPU.

Use el calificador **EventType** en la clase MOF del tipo de evento para identificar el tipo de evento. Si varios tipos de eventos utilizan los mismos datos de eventos, pueden usar la misma clase MOF. El proveedor usa el mismo valor de tipo de evento para identificar el evento al establecer el miembro **Class. Type** de la estructura de [**\_ \_ encabezado del seguimiento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) .

La clase de tipo de evento MOF contiene propiedades. El orden de estas propiedades define el diseño de los datos de evento. En la tabla siguiente se identifican los tipos de datos y calificadores que puede usar para definir las propiedades. Para obtener más información sobre los calificadores de propiedad y clase que se pueden usar, consulte [calificadores MOF de seguimiento de eventos](event-tracing-mof-qualifiers.md).



| Tipo de datos              | Calificadores                        | Descripción                                                                                                                                                                                                                                                                                                              |
|------------------------|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **sint8**, **Uint8**   | **Format**                        | Declara un entero decimal de 1 byte. Para declarar un carácter ANSI, use el calificador de **formato** y establezca su valor en "c".                                                                                                                                                                                                  |
| **sint16**, **UInt16** | **Format**                        | Declara un entero decimal de 2 bytes. Para indicar que el número es un número hexadecimal, utilice el calificador de **formato** . Por ejemplo, Format ("x").                                                                                                                                                                               |
| **sint32**, **UInt32** | **Format**                        | Declara un entero decimal de 4 bytes. Para indicar que el número es un número hexadecimal, use el calificador de **formato** y establezca su valor en "x".                                                                                                                                                                                |
| **sint64**, **UInt64** | **Format**                        | Declara un entero decimal de 8 bytes. Para indicar que el número es un número hexadecimal, use el calificador de **formato** y establezca su valor en "x".                                                                                                                                                                                |
| **boolean**            |                                   | Declara un valor booleano. El consumidor de eventos debe interpretar el valor como BOOLEANO (entero de 4 bytes).                                                                                                                                                                                                                        |
| **char16**             |                                   | Declara un carácter ancho. El consumidor de eventos debe interpretar las matrices de char16 en eventos de kernel como cadenas de caracteres anchos. (Utilice el tamaño de la matriz para copiar la cadena. Algunas cadenas pueden contener caracteres NULOs iniciales).                                                                                                      |
| **object**             | **Extensión**                     | Declara un BLOB binario. El calificador de **extensión** indica el tipo de datos en el BLOB.                                                                                                                                                                                                                              |
| **string**             | **Formato**, **StringTermination** | Declara un valor de cadena. Para indicar que la cadena es una cadena de caracteres anchos, utilice el calificador de **formato** y establezca su valor en "w". La cadena se considera una cadena ANSI si no se especifica el calificador de **formato** . Para indicar cómo se termina la cadena, use el calificador **StringTermination** . <br/> |



 

Para especificar una matriz, puede usar corchetes, \[ \] . Los corchetes pueden incluir el tamaño de la matriz. Por ejemplo:

`[WmiDataId(1), read] uint8 MyGuid[16];`

También puede usar el calificador **Max** para especificar el tamaño de una matriz. Por ejemplo:

`[WmiDataId(1), Max(16), read] uint8 MyGuid[];`

Si incluye el tamaño de la matriz entre corchetes, el compilador MOF genera el calificador Max.

Es importante que use el calificador de **Descripción** para cada propiedad. La descripción debe contener un nombre para mostrar que el consumidor pueda usar al mostrar los valores de propiedad.

En el ejemplo siguiente se muestra el contenido de un archivo MOF que describe una clase MOF de proveedor, evento y tipo de evento.

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

Tenga en cuenta que los nombres de clases MOF de proveedor, evento y tipo de evento deben ser únicos en todo el espacio de nombres. Para evitar conflictos de nombres, debe usar un nombre único y descriptivo para todos los nombres de clase. Las propiedades de clase también deben ser descriptivas y únicas dentro de su jerarquía de clases; una clase secundaria que contenga el mismo nombre de propiedad que una clase primaria sobrescribe la propiedad de la clase primaria.

Después de definir las clases MOF, utilice el compilador MOF para generar el esquema de eventos y agregarlo al repositorio CIM. Los consumidores pueden entonces leer el esquema del repositorio y leer los datos de eventos mediante programación. Para obtener una descripción completa de la sintaxis MOF y usar el compilador MOF (Mofcomp.exe) para agregar las clases MOF al repositorio CIM, vea [Managed Object Format](../wmisdk/managed-object-format--mof-.md). Para obtener información sobre el uso de Wbemtest.exe para tener acceso al repositorio CIM, consulte [instrumental de administración de Windows](../wmisdk/wmi-start-page.md) (WMI).

## <a name="versioning-mof-class"></a>Control de versiones de la clase MOF

Si agrega o cambia un tipo de evento de clase MOF, la Convención es la versión de la clase MOF de eventos y sus clases MOF de tipo de evento secundario. Para la versión de la clase MOF del evento actual, anexe \_ vn al nombre de clase, donde n es un número incremental que empieza en 0. Si esta es la primera revisión de la clase, anexe \_ V0 al nombre de la clase. También debe agregar el calificador **EventVersion** a la clase. Use el mismo número de versión que usó en el nombre de clase para el valor del calificador **EventVersion** .

La nueva versión de la clase MOF de eventos debe usar el mismo nombre y calificador de **GUID** que la clase original. La nueva clase puede agregar opcionalmente el calificador **EventVersion** . La clase MOF de eventos que no contiene el calificador **EventVersion** se considera la versión más reciente, o si todas las versiones de la clase contienen un calificador **EventVersion** , la clase con el número de versión más alto se considera la versión más reciente. El proveedor utiliza el miembro **Class. version** de la estructura de [**encabezado del \_ seguimiento \_ de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) para identificar la versión del evento incluido en el seguimiento.

En el ejemplo siguiente se muestra cómo la versión de una clase MOF de eventos.

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

 

 
