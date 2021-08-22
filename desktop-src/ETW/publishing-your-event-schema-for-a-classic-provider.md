---
description: Los proveedores clásicos deben usar Managed Object Format (MOF) para publicar el diseño de sus datos de eventos. A continuación, los consumidores pueden leer el diseño publicado de WMI en tiempo de ejecución y usarlo para leer los datos del evento.
ms.assetid: eb3d8422-2352-47cf-9825-cba9916791a9
title: Publicación del esquema de eventos para un proveedor clásico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6607e2e9b940df5afd6e8070e9235fe40566ef2b6d2b31b3c14656756835bab2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069825"
---
# <a name="publishing-your-event-schema-for-a-classic-provider"></a>Publicación del esquema de eventos para un proveedor clásico

[Los](about-event-tracing.md) proveedores clásicos deben [usar Managed Object Format](../wmisdk/managed-object-format--mof-.md) (MOF) para publicar el diseño de sus datos de eventos. A continuación, los consumidores pueden leer el diseño publicado de WMI en tiempo de ejecución y usarlo para leer los datos del evento.

Si usa MOF para publicar el diseño de los datos de eventos en WMI, normalmente se crean los tres tipos siguientes de clases MOF en el espacio de nombres \\ wmi raíz:

-   [Una clase MOF de proveedor](#provider-mof-classes)
-   [Una o varias clases MOF de eventos](#event-mof-classes)
-   [Una o varias clases MOF de tipo de evento](#event-type-mof-classes)

## <a name="provider-mof-classes"></a>Clases MOF del proveedor

Si publica el diseño de los datos del evento, debe crear una clase MOF que identifique al proveedor. Esta clase debe derivar de la **clase MOF de EventTrace** y debe estar vacía (sin propiedades ni métodos). La clase también debe incluir el **calificador GUID** que identifica de forma única el proveedor. Este es el mismo GUID que se usa al llamar a la [**función RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) para registrar el proveedor.

## <a name="event-mof-classes"></a>Clases MOF de eventos

Una clase MOF de eventos define una clase de eventos que proporciona el proveedor. Esta clase deriva de la clase MOF del proveedor y debe estar vacía (sin propiedades ni métodos). La clase también debe incluir el **calificador Guid** que identifica de forma única la clase de eventos que definen sus clases secundarias. El proveedor usa este mismo GUID al establecer el **miembro Guid** de la estructura EVENT [**TRACE \_ \_ HEADER.**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header)

## <a name="event-type-mof-classes"></a>Clases MOF de tipo de evento

Una clase MOF de tipo de evento define los datos de evento reales. Esta clase se deriva de su clase MOF de eventos primarios. Al asignar un nombre a la clase MOF del tipo de evento, la convención es usar el nombre de clase MOF de evento al principio del nombre de clase MOF del tipo de evento. Por ejemplo, si el nombre de clase MOF del evento es HWConfig y el tipo de evento clase MOF representa información de CPU, debe llamar al tipo de evento clase MOF, \_ HWConfig CPU.

Use el **calificador EventType** en la clase MOF del tipo de evento para identificar el tipo de evento. Si varios tipos de eventos usan los mismos datos de evento, pueden usar la misma clase MOF. El proveedor usa el mismo valor de tipo de evento para identificar el evento al establecer el **miembro Class.Type** de la [**estructura EVENT TRACE \_ \_ HEADER.**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header)

La clase MOF del tipo de evento contiene propiedades. El orden de estas propiedades define el diseño de los datos del evento. En la tabla siguiente se identifican los tipos de datos y calificadores que puede usar para definir las propiedades. Para obtener más información sobre la propiedad y los calificadores de clase que puede usar, vea [Calificadores MOF](event-tracing-mof-qualifiers.md)de seguimiento de eventos .



| Tipo de datos              | Calificadores                        | Descripción                                                                                                                                                                                                                                                                                                              |
|------------------------|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **sint8**, **uint8**   | **Format**                        | Declara un entero decimal de 1 byte. Para declarar un carácter ANSI, use el **calificador Format** y establezca su valor en "c".                                                                                                                                                                                                  |
| **sint16**, **uint16** | **Format**                        | Declara un entero decimal de 2 bytes. Para indicar que el número es un número hexadecimal, use el **calificador Format.** Por ejemplo, format("x").                                                                                                                                                                               |
| **sint32,** **uint32** | **Format**                        | Declara un entero decimal de 4 bytes. Para indicar que el número es un número hexadecimal, use el calificador **Format** y establezca su valor en "x".                                                                                                                                                                                |
| **sint64**, **uint64** | **Format**                        | Declara un entero decimal de 8 bytes. Para indicar que el número es un número hexadecimal, use el calificador **Format** y establezca su valor en "x".                                                                                                                                                                                |
| **boolean**            |                                   | Declara un valor booleano. El consumidor de eventos debe interpretar el valor como BOOL (entero de 4 bytes).                                                                                                                                                                                                                        |
| **char16**             |                                   | Declara un carácter ancho. El consumidor de eventos debe interpretar matrices char16 en eventos de kernel como cadenas de caracteres anchos. (Use el tamaño de la matriz para copiar la cadena. Algunas cadenas pueden contener caracteres NULL iniciales).                                                                                                      |
| **object**             | **Extensión**                     | Declara un blob binario. El **calificador** De extensión indica el tipo de datos del blob.                                                                                                                                                                                                                              |
| **string**             | **Format**, **StringTermination** | Declara un valor de cadena. Para indicar que la cadena es una cadena de caracteres anchos, use el calificador **Format** y establezca su valor en "w". La cadena se considera una cadena ANSI si no se especifica el **calificador Format.** Para indicar cómo finaliza la cadena, use el **calificador StringTermination.** <br/> |



 

Para especificar una matriz, puede usar corchetes, \[ \] . Los corchetes pueden incluir el tamaño de la matriz. Por ejemplo:

`[WmiDataId(1), read] uint8 MyGuid[16];`

También puede usar el calificador **Max** para especificar el tamaño de una matriz. Por ejemplo:

`[WmiDataId(1), Max(16), read] uint8 MyGuid[];`

Si incluye el tamaño de la matriz entre corchetes, el compilador de MOF genera automáticamente el calificador Max.

Es importante que use el calificador **Description** para cada propiedad. La descripción debe contener un nombre para mostrar que el consumidor puede usar al mostrar los valores de propiedad.

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

Tenga en cuenta que los nombres de clase MOF del proveedor, evento y tipo de evento deben ser únicos dentro de todo el espacio de nombres. Para evitar conflictos de nomenclatura, debe usar un nombre único y descriptivo para todos los nombres de clase. Las propiedades de clase también deben ser descriptivas y únicas dentro de su jerarquía de clases: una clase secundaria que contiene el mismo nombre de propiedad que una clase primaria sobrescribe la propiedad de la clase primaria.

Después de definir las clases MOF, use el compilador MOF para generar el esquema de eventos y agregarlo al repositorio CIM. A continuación, los consumidores pueden leer el esquema desde el repositorio y leer mediante programación los datos del evento. Para obtener una descripción completa de la sintaxis de MOF y usar el compilador MOF (Mofcomp.exe) para agregar las clases MOF al repositorio CIM, [vea Managed Object Format](../wmisdk/managed-object-format--mof-.md). Para obtener información sobre el Wbemtest.exe para acceder al repositorio CIM, [vea Windows Management Instrumentation](../wmisdk/wmi-start-page.md) (WMI).

## <a name="versioning-mof-class"></a>Clase MOF de control de versiones

Si agrega o cambia una clase MOF de tipo de evento, la convención es crear versiones tanto de la clase MOF de eventos como de sus clases MOF del tipo de evento secundario. Para crear una versión de la clase MOF del evento actual, anexe Vn al nombre de clase, donde n es un \_ número incremental a partir de 0. Si esta es la primera revisión de la clase, \_ anexe V0 al nombre de clase. También debe agregar el **calificador EventVersion** a la clase . Use el mismo número de versión que usó en el nombre de clase para el valor del **calificador EventVersion.**

La nueva versión de la clase MOF del evento debe usar el mismo nombre y el mismo **calificador GUID** que la clase original. La nueva clase puede agregar opcionalmente el **calificador EventVersion.** La clase MOF de evento que no contiene el calificador **EventVersion** se considera la versión más reciente, o si todas las versiones de la clase contienen un calificador **EventVersion,** la clase con el número de versión más alto se considera la versión más reciente. El proveedor usa el **miembro Class.Version** de la [**estructura EVENT TRACE \_ \_ HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) para identificar la versión del evento incluido en el seguimiento.

En el ejemplo siguiente se muestra cómo crear versiones de una clase MOF de eventos.

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

 

 
