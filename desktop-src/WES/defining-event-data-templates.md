---
title: Definición de plantillas de datos de eventos
description: Los proveedores usan plantillas de datos para definir los datos específicos del evento que incluyen con un evento y para definir los datos de filtro que una sesión de seguimiento de ETW puede pasar al proveedor cuando habilita el proveedor.
ms.assetid: 064227a2-7ce8-461a-9dc0-7519652e6628
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5480ca158916801665943bd33b886bfcd5d73015e8730c1dd108123dadc1995
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652615"
---
# <a name="defining-event-data-templates"></a>Definición de plantillas de datos de eventos

Los proveedores usan plantillas de datos para definir los datos específicos del evento que incluyen con un evento y para definir los datos de filtro que una sesión de seguimiento de ETW puede pasar al proveedor cuando habilita el proveedor. Si el evento no incluye datos específicos del evento, no definirá una plantilla. Para definir una plantilla, use el **elemento de** plantilla. Una plantilla incluye un elemento de datos para cada fragmento de datos que el proveedor incluye con el evento . Puede especificar tipos enteros, cadenas, matrices y estructuras. Debe escribir los datos del evento en el orden en que se definieron los elementos de datos en la plantilla.

También puede incluir en la plantilla, un fragmento XML que los consumidores deben usar para determinar cómo representar los datos del evento. Si no incluye el fragmento, los consumidores deben representar los datos del evento en el orden en que se definieron los elementos de datos en la plantilla.

Al definir una plantilla, debe asignarle un identificador de plantilla que use para hacer referencia a la plantilla en una definición de evento. Cada elemento de datos de la plantilla debe especificar un nombre y un tipo de datos de entrada (para obtener una lista de tipos de entrada, vea la sección Comentarios del tipo complejo [**InputType).**](eventmanifestschema-inputtype-complextype.md) Si el tipo de datos de entrada se puede representar en varios formatos, debe especificar el tipo de datos de salida que indica a los consumidores cómo representar el elemento de datos. Por ejemplo, un tipo de datos de entrada UInt32 se puede representar como un entero sin signo, un identificador de subproceso, una dirección IPv4 y un código de error win32, entre otros. Si no especifica el tipo de datos de salida, los consumidores deben usar el tipo de salida predeterminado del tipo de entrada para representar el elemento de datos.

Para especificar una matriz, incluya el atributo **count** en el elemento de datos y esta establezca en el número de elementos de la matriz. La matriz puede ser una matriz de tamaño variable o una matriz de tamaño fijo. Si la matriz es una matriz de tamaño fijo, establezca **count** en el tamaño de la matriz. Por ejemplo, si una matriz de enteros tiene un tamaño fijo de 10, establezca **count** en 10. Al escribir la matriz, debe escribir 40 bytes de datos.

Si la matriz es una matriz de tamaño variable, establezca **count** en el nombre del elemento de datos que contiene el tamaño de la matriz. Si la matriz contiene punteros, la dirección de los punteros se escribe como los datos del evento, no como los datos a los que apuntan los punteros.

Debe especificar el atributo **length** si el elemento de datos es un blob binario. También puede especificar el atributo **length para** las cadenas de longitud fija.

Especifique el **atributo de** mapa si el elemento de datos representa un valor de enumeración y desea que el consumidor imprima una cadena para el valor en lugar del propio valor.

Si incluye estructuras en la plantilla, debe escribir los miembros de la estructura individualmente en lugar de escribir la estructura a menos que pueda garantizar la alineación de límites de 8 bytes.

Debe considerar cuidadosamente la información que incluye en los eventos, especialmente cuando los eventos se escriben en los canales globales. Por lo general, no debe incluir información privada en los eventos. Esto incluye contraseñas de texto no cifrado e información personal del usuario. Además, los programas ejecutados por el usuario, las direcciones URL visitadas por el usuario y otra información relacionada con las actividades del usuario en el equipo deben considerarse privados.

Si debe registrar direcciones URL y nombres de usuario en los eventos, no los escriba en los canales de Windows (sistema y aplicación) porque todos los usuarios autenticados pueden leer estos canales. En su lugar, escríbalos en sus propios canales operativos o analíticos. Establezca los permisos de acceso en estos canales para permitir que solo los administradores lean los eventos. Es posible que tenga que proporcionar una divulgación adecuada para notificar a los usuarios el hecho de que la información privada está disponible para los administradores.

En el ejemplo siguiente se muestra cómo definir una plantilla. Debe especificar el atributo **tid** de la plantilla al que hace referencia en la definición de evento o la definición de filtro.


```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="http://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="http://www.w3.org/2001/XMLSchema"
    >

    <instrumentation>
        <events>
            <provider name="Microsoft-Windows-SampleProvider"
                guid="{1db28f2e-8f80-4027-8c5a-a11f7f10f62d}"
                symbol="PROVIDER_GUID"
                resourceFileName="<path to the exe or dll that contains the metadata resources>"
                messageFileName="<path to the exe or dll that contains the string resources>"
                message="$(string.Provider.Name)">

                . . .

                <maps>
                    <valueMap name="TransferType">
                        <map value="1" message="$(string.TransferType.Download)"/>
                        <map value="2" message="$(string.TransferType.Upload)"/>
                        <map value="3" message="$(string.TransferType.UploadReply)"/>
                    </valueMap>
                    <bitMap name="DaysOfTheWeek">
                        <map value="0x1" message="$(string.DaysOfTheWeek.Sunday)"/>
                        <map value="0x2" message="$(string.DaysOfTheWeek.Monday)"/>
                        <map value="0x4" message="$(string.DaysOfTheWeek.Tuesday)"/>
                        <map value="0x8" message="$(string.DaysOfTheWeek.Wednesday)"/>
                        <map value="0x10" message="$(string.DaysOfTheWeek.Thursday)"/>
                        <map value="0x20" message="$(string.DaysOfTheWeek.Friday)"/>
                        <map value="0x40" message="$(string.DaysOfTheWeek.Saturday)"/>
                    </bitMap>
                </maps>

                <templates>
                    <template tid="t2">
                        <data name="TransferName" inType="win:UnicodeString"/>
                        <data name="Day" inType="win:UInt32" map="DaysOfTheWeek"/>
                        <data name="Transfer" inType="win:UInt32" map="TransferType"/>
                    </template>

                    <template tid="t3">
                        <data name="TransferName" inType="win:UnicodeString"/>
                        <data name="ErrorCode" inType="win:Int32" outType="win:HResult"/>
                        <data name="FilesCount" inType="win:UInt16" />
                        <data name="Files" inType="win:UnicodeString" count="FilesCount"/>
                        <data name="BufferSize" inType="win:UInt32" />
                        <data name="Buffer" inType="win:Binary" length="BufferSize"/>
                        <data name="Certificate" inType="win:Binary" length="11" />
                        <data name="IsLocal" inType="win:Boolean" />
                        <data name="Path" inType="win:UnicodeString" />
                        <data name="ValuesCount" inType="win:UInt16" />
                        <struct name="Values" count="ValuesCount" >
                            <data name="Value" inType="win:UInt16" />
                            <data name="Name" inType="win:UnicodeString" />
                        </struct>
                    </template>
                </templates>

                . . .

            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="Provider.Name" value="Sample Provider"/>
                <string id="TransferType.Download" value="Download"/>
                <string id="TransferType.Upload" value="Upload"/>
                <string id="TransferType.UploadReply" value="Upload-reply"/>
                <string id="DaysOfTheWeek.Sunday" value="Sunday"/>
                <string id="DaysOfTheWeek.Monday" value="Monday"/>
                <string id="DaysOfTheWeek.Tuesday" value="Tuesday"/>
                <string id="DaysOfTheWeek.Wednesday" value="Wednesday"/>
                <string id="DaysOfTheWeek.Thursday" value="Thursday"/>
                <string id="DaysOfTheWeek.Friday" value="Friday"/>
                <string id="DaysOfTheWeek.Saturday" value="Saturday"/>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```
