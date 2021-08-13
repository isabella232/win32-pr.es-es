---
title: Escribir un manifiesto de instrumentación
description: Las aplicaciones y los archivos DLL usan un manifiesto de instrumentación para identificar sus proveedores de instrumentación y los eventos que escriben los proveedores.
ms.assetid: eec9d129-acde-4302-9121-634b3fad8455
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82b3462d6adc264fba8ba155620a2bbb402d51d5d6fc24f7dbe879b9e2a91ec9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118587056"
---
# <a name="writing-an-instrumentation-manifest"></a>Escribir un manifiesto de instrumentación

Las aplicaciones y los archivos DLL usan un manifiesto de instrumentación para identificar sus proveedores de instrumentación y los eventos que escriben los proveedores. Un manifiesto es un archivo XML que contiene los elementos que identifican al proveedor. La convención es usar .man como extensión para el manifiesto. El manifiesto debe ajustarse al manifiesto de evento XSD. Para obtener más información sobre el esquema, [vea Esquema EventManifest](eventmanifestschema-schema.md).

Un proveedor de instrumentación es cualquier aplicación o DLL que llame a las funciones [**EventWriteEx**](/windows/desktop/api/evntprov/nf-evntprov-eventwriteex), [**EventWriteString**](/windows/desktop/api/evntprov/nf-evntprov-eventwritestring)o [**EventWriteTransfer**](/windows/desktop/api/evntprov/nf-evntprov-eventwritetransfer) para escribir eventos en una sesión de seguimiento de seguimiento de [eventos](/windows/desktop/ETW/event-tracing-portal) (ETW) o en un canal del registro de eventos. Una aplicación puede definir un único proveedor de instrumentación que cubre todos los eventos que escribe o puede definir un proveedor para la aplicación y un proveedor para cada uno de sus archivos DLL. El número de proveedores que define la aplicación en el manifiesto depende únicamente de cómo la aplicación quiere organizar los eventos que escribe.

La ventaja de especificar un proveedor para cada archivo DLL es que, a continuación, puede habilitar y deshabilitar los proveedores individuales y, por tanto, los eventos que generan. Esta ventaja solo se aplica si una sesión de seguimiento de ETW habilita el proveedor. Los eventos que especifican un canal de registro de eventos siempre se escriben en ese canal.

El manifiesto debe identificar el proveedor y los eventos que escribe, pero los demás metadatos, como canales, niveles y palabras clave, son opcionales. si define los metadatos opcionales depende de quién consumirá los eventos. Por ejemplo, si los administradores o el personal de soporte técnico consumen los eventos mediante una herramienta como Windows Visor de eventos que lee eventos de los canales del registro de eventos, debe definir los canales en los que se escriben los eventos. Sin embargo, si el proveedor solo lo habilitará una sesión de seguimiento de ETW, no es necesario definir canales.

Aunque los metadatos de niveles, tareas, códigos de operación y palabras clave son opcionales, debe usarlos para agrupar o agrupar los eventos de forma lógica. La agrupación de los eventos ayuda a los consumidores a consumir solo los eventos que son de interés. Por ejemplo, el consumidor podría consultar todos los eventos donde level es "critical" y keyword es "write" o consultar todos los eventos escritos por una tarea específica.

Además de los consumidores que usan palabras clave de nivel y para consumir tipos específicos de eventos, una sesión de seguimiento de ETW puede usar los metadatos de nivel y palabra clave para decir a ETW que limite los eventos que se escriben en el registro de seguimiento de eventos. Por ejemplo, la sesión podría limitar los eventos a solo los eventos en los que level es "error" o "critical" y la palabra clave es "read".

Un proveedor puede definir filtros que una sesión usa para filtrar los eventos en función de los datos de eventos. Con las palabras clave level y , ETW determina si el evento se escribe en el registro pero con filtros, el proveedor usa los criterios de datos de filtro para determinar si escribe el evento en esa sesión. Los filtros solo son aplicables cuando una sesión de seguimiento de ETW habilita al proveedor.

En las secciones siguientes se muestra cómo definir los componentes del manifiesto:

-   [Identificación del proveedor](identifying-the-provider.md)
-   [Definición de los canales en los que se escriben los eventos](defining-channels.md)
-   [Definición de los niveles de gravedad de los eventos que escribe el proveedor](defining-severity-levels.md)
-   [Definición de las tareas y operaciones que realiza el proveedor](defining-tasks-and-opcodes.md)
-   [Definición de las palabras clave que clasifican los eventos que escribe el proveedor](defining-keywords-used-to-classify-types-of-events.md)
-   [Definición de los filtros que usa el proveedor para filtrar los eventos que escribe](defining-filters.md)
-   [Definir los mapas de nombre y valor a los que hace referencia la plantilla](defining-name-value-mappings.md)
-   [Definir las plantillas que definen los datos específicos del evento](defining-event-data-templates.md)
-   [Definición de los eventos que escribe el proveedor](defining-events.md)

Aunque puede crear manualmente un manifiesto de instrumentación, considere la posibilidad de usar la herramienta ECManGen.exe que se incluye en la carpeta Bin del \\ SDK de Windows. La ECManGen.exe usa una GUI que le guía a través de la creación de un manifiesto desde cero sin tener que usar etiquetas XML. Tener conocimiento de la información de esta sección y de la sección [Esquema de EventManifest](eventmanifestschema-schema.md) le ayudará al usar la herramienta.

Si usa Visual Studio como editor XML, puede agregar el esquema [EventManifest](eventmanifestschema-schema.md) al proyecto (consulte el menú XML) para aprovechar IntelliSense, la validación de esquemas en línea y otras características para facilitar y precisa la escritura del manifiesto.

Después de escribir el manifiesto, use el compilador de mensajes para validar el manifiesto y generar los archivos de recursos y encabezados que incluya en el proveedor. Para obtener más información, [vea Compilar un manifiesto de instrumentación.](compiling-an-instrumentation-manifest.md)

En el ejemplo siguiente se muestra el esqueleto de un manifiesto de evento totalmente definido.


```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="http://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="http://www.w3.org/2001/XMLSchema"
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



 

 
