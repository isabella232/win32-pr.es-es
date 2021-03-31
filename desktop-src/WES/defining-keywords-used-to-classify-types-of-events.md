---
title: Definir palabras clave utilizadas para clasificar tipos de eventos
description: Los proveedores usan palabras clave para clasificar distintos tipos de eventos.
ms.assetid: 1cbad719-bc59-4255-8a15-9e45f363d199
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d48992c5cbafec5f945fa2f133924ccf0e2e7e96
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2020
ms.locfileid: "103904447"
---
# <a name="defining-keywords-used-to-classify-types-of-events"></a>Definir palabras clave utilizadas para clasificar tipos de eventos

Los proveedores usan palabras clave para clasificar distintos tipos de eventos. Por ejemplo, puede crear una palabra clave para todos los eventos de lectura y, a continuación, aplicar la palabra clave Read a cualquier evento que realice una operación de lectura, como la lectura desde un archivo o un registro. A continuación, los consumidores pueden usar los valores de bit de palabra clave para filtrar la clasificación de los distintos eventos. Por ejemplo, el consumidor podría solicitar todos los eventos de lectura o todos los eventos de lectura de la tarea X (si también agrupa eventos por tarea). Para definir una palabra clave, use el elemento de **palabra clave** .

Una sesión de seguimiento de ETW puede usar las palabras clave (de la misma forma que usa LEVEL) para limitar los eventos que el servicio ETW escribe en el archivo de registro de seguimiento de eventos. Una sesión de seguimiento puede habilitar el proveedor mediante dos conjuntos de máscaras de fotopalabras clave: una máscara de bits "any" en la que se escribe el evento si cualquiera de los bits de palabra clave del evento coincide con cualquiera de los bits establecidos en esta máscara, y una máscara de bits "All" donde los eventos que coinciden con el caso "any", el evento se escribe solo si todos los bits de la máscara "All" existen en la máscara de la palabra clave

Por ejemplo, si el proveedor define un evento que especifica una palabra clave Read (bit 0) y una palabra clave de acceso local (bit 1), y un segundo evento que especifica una palabra clave Read (bit 0) y una palabra clave de acceso remoto (bit 2), puede establecer la máscara de bits "any" en 1 para recibir todos los eventos leídos, o bien puede establecer la máscara de bits "any" en 1 y "All" en 3 para recibir solo las lecturas locales.

Debe especificar los atributos **Name** y **Mask** de la palabra clave. La máscara solo debe establecer un bit, entre el bit 0 y el bit 47. Los bits 48 a 64 están reservados.

Los atributos **Symbol** y **Message** son opcionales.

En el ejemplo siguiente se muestra cómo definir una palabra clave.

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

                <keywords>
                    <keyword name="Read" mask="0x1" symbol="READ_KEYWORD"/>
                    <keyword name="Write" mask="0x2" symbol="WRITE_KEYWORD"/>
                    <keyword name="Local" mask="0x4" symbol="LOCAL_KEYWORD"/>
                    <keyword name="Remote" mask="0x8" symbol="REMOTE_KEYWORD"/>
                </keywords>

                . . .

            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="Provider.Name" value="Sample Provider"/>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```
