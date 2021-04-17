---
title: Escritura de un manifiesto de instrumentación
description: Las aplicaciones y los archivos dll utilizan un manifiesto de instrumentación para identificar sus proveedores de instrumentación y los eventos que escriben los proveedores.
ms.assetid: eec9d129-acde-4302-9121-634b3fad8455
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cdad802526ad177eb5daa8846535c434fff32eb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420751"
---
# <a name="writing-an-instrumentation-manifest"></a>Escritura de un manifiesto de instrumentación

Las aplicaciones y los archivos dll utilizan un manifiesto de instrumentación para identificar sus proveedores de instrumentación y los eventos que escriben los proveedores. Un manifiesto es un archivo XML que contiene los elementos que identifican el proveedor. La Convención es usar. man como extensión del manifiesto. El manifiesto debe cumplir el manifiesto del evento XSD. Para más información sobre el esquema, consulte [esquema de EventManifest](eventmanifestschema-schema.md).

Un proveedor de instrumentación es cualquier aplicación o DLL que llama a las funciones [**EventWriteEx**](/windows/desktop/api/evntprov/nf-evntprov-eventwriteex), [**EventWriteString**](/windows/desktop/api/evntprov/nf-evntprov-eventwritestring)o [**EventWriteTransfer**](/windows/desktop/api/evntprov/nf-evntprov-eventwritetransfer) para escribir eventos en una sesión de seguimiento de [seguimiento de eventos](/windows/desktop/ETW/event-tracing-portal) (ETW) o en un canal de registro de eventos. Una aplicación puede definir un proveedor de instrumentación único que abarque todos los eventos que escribe o puede definir un proveedor para la aplicación y un proveedor para cada uno de sus dll. El número de proveedores que define la aplicación en el manifiesto depende únicamente del modo en que la aplicación desea organizar los eventos que escribe.

La ventaja de especificar un proveedor para cada DLL es que, a continuación, puede habilitar y deshabilitar los proveedores individuales y, por tanto, los eventos que generan. Esta ventaja solo se aplica si el proveedor está habilitado por una sesión de seguimiento de ETW. Cualquier evento que especifique un canal de registro de eventos siempre se escribe en ese canal.

El manifiesto debe identificar el proveedor y los eventos que escribe, pero los demás metadatos, como los canales, los niveles y las palabras clave, son opcionales. la definición de los metadatos opcionales depende de quién vaya a consumir los eventos. Por ejemplo, si los administradores o el personal de soporte técnico consumen los eventos con una herramienta como Windows Visor de eventos que lee los eventos de los canales del registro de eventos, debe definir los canales en los que se escriben los eventos. Sin embargo, si el proveedor solo se va a habilitar mediante una sesión de seguimiento de ETW, no es necesario definir canales.

Aunque los metadatos de los niveles, las tareas, los códigos de operación y las palabras clave son opcionales, deben usarse para agrupar o depositar lógicamente los eventos. La agrupación de eventos ayuda a los consumidores a consumir solo los eventos que le interesan. Por ejemplo, el consumidor podría consultar todos los eventos en los que el nivel sea "crítico" y la palabra clave sea "escribir", o bien consultar todos los eventos escritos por una tarea específica.

Además de los consumidores que usan el nivel y las palabras clave para consumir tipos de eventos específicos, una sesión de seguimiento de ETW puede usar los metadatos de nivel y de palabra clave para indicar a ETW que limite los eventos que se escriben en el registro de seguimiento de eventos. Por ejemplo, la sesión podría limitar los eventos a solo los eventos en los que el nivel sea "error" o "crítico" y la palabra clave sea "lectura".

Un proveedor puede definir los filtros que una sesión utiliza para filtrar los eventos en función de los datos de evento. Con el nivel y las palabras clave, ETW determina si el evento se escribe en el registro, pero con filtros, el proveedor utiliza los criterios de datos de filtro para determinar si escribe el evento en esa sesión. Los filtros solo se aplican cuando una sesión de seguimiento de ETW habilita el proveedor.

En las secciones siguientes se muestra cómo definir los componentes del manifiesto:

-   [Identificación del proveedor](identifying-the-provider.md)
-   [Definir los canales en los que se escriben los eventos](defining-channels.md)
-   [Definir los niveles de gravedad de los eventos que escribe el proveedor](defining-severity-levels.md)
-   [Definir las tareas y las operaciones que realiza el proveedor](defining-tasks-and-opcodes.md)
-   [Definir las palabras clave que clasifican los eventos que escribe el proveedor](defining-keywords-used-to-classify-types-of-events.md)
-   [Definir los filtros que utiliza el proveedor para filtrar los eventos que escribe](defining-filters.md)
-   [Definir las asignaciones de nombre y valor a las que hacen referencia los datos de la plantilla](defining-name-value-mappings.md)
-   [Definir las plantillas que definen los datos específicos del evento](defining-event-data-templates.md)
-   [Definir los eventos que escribe el proveedor](defining-events.md)

Aunque puede crear un manifiesto de instrumentación manualmente, debería considerar la posibilidad de usar la herramienta de ECManGen.exe que se incluye en la \\ carpeta bin de la Windows SDK. La herramienta ECManGen.exe usa una GUI que le guía a través de la creación de un manifiesto desde cero sin tener que usar etiquetas XML. Conocer la información de esta sección y en la sección del [esquema EventManifest](eventmanifestschema-schema.md) le ayudará a usar la herramienta.

Si usa Visual Studio como editor XML, puede Agregar el esquema [EventManifest](eventmanifestschema-schema.md) al proyecto (vea el menú XML) para aprovechar las ventajas de IntelliSense, la validación de esquemas en línea y otras características para que la escritura del manifiesto sea fácil y precisa.

Después de escribir el manifiesto, use el compilador de mensajes para validar el manifiesto y generar los archivos de recursos y de encabezado que se incluyen en el proveedor. Para obtener más información, vea [compilar un manifiesto de instrumentación](compiling-an-instrumentation-manifest.md).

En el ejemplo siguiente se muestra el esqueleto de un manifiesto de evento totalmente definido.


```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="https://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="https://www.w3.org/2001/XMLSchema"    
    >

    <instrumentation>
        <events>
            <provider ...>
                <channels>
                    <importChannel .../>
                    <channel .../>
                </channels>
                <levels>
                    <level .../>
                </levels>
                <tasks>
                    <task .../>
                </tasks>
                <opcodes>
                    <opcode .../>
                </opcodes>
                <keywords>
                    <keyword .../>
                </keywords>
                <filters>
                    <filter .../>
                </filters>
                <maps>
                    <valueMap ...>
                        <map .../>
                    </valueMap>
                    <bitMap ...>
                        <map .../>
                    </bitMap>
                </maps>
                <templates>
                    <template ...>
                        <data .../>
                        <UserData>
                            <!-- valid XML fragment -->
                        </UserData>
                    </template>
                </templates>
                <events>
                    <event .../>
                </events>
            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources ...>
            <stringTable>
                <string .../>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```



 

 