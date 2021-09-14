---
title: Definir palabras clave usadas para clasificar tipos de eventos
description: Los proveedores usan palabras clave para clasificar distintos tipos de eventos.
ms.assetid: 1cbad719-bc59-4255-8a15-9e45f363d199
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d48992c5cbafec5f945fa2f133924ccf0e2e7e96
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126885545"
---
# <a name="defining-keywords-used-to-classify-types-of-events"></a>Definir palabras clave usadas para clasificar tipos de eventos

Los proveedores usan palabras clave para clasificar distintos tipos de eventos. Por ejemplo, puede crear una palabra clave para todos los eventos de lectura y, a continuación, aplicar la palabra clave read a cualquier evento que realice una operación de lectura, como leer desde un archivo o registro. A continuación, los consumidores podrían usar los valores de bits de la palabra clave para filtrar por diferentes clasificaciones de eventos. Por ejemplo, el consumidor podría solicitar todos los eventos de lectura o todos los eventos de lectura de la tarea X (si también agrupa eventos por tarea). Para definir una palabra clave, use el elemento **keyword** .

Una sesión de seguimiento de ETW puede usar las palabras clave (de la misma manera que usa level) para limitar los eventos que el servicio ETW escribe en su archivo de registro de seguimiento de eventos. Una sesión de seguimiento puede habilitar el proveedor mediante dos conjuntos de máscaras de bits de palabras clave: una máscara de bits "Any" en la que se escribe el evento si alguno de los bits de palabra clave del evento coincide con cualquiera de los bits establecidos en esta máscara y una máscara de bits "All" donde para los eventos que coinciden con el caso "Any", el evento se escribe solo si todos los bits de la máscara "All" existen en la máscara de palabras clave del evento.

Por ejemplo, si el proveedor define un evento que especifica una palabra clave read (bit 0) y una palabra clave de acceso local (bit 1) y un segundo evento que especifica una palabra clave read (bit 0) y una palabra clave de acceso remoto (bit 2), podría establecer la máscara de bits "Any" en 1 para recibir todos los eventos de lectura, o bien podría establecer la máscara de bits "Any" en 1 y "All" en 3 para recibir solo lecturas locales.

Debe especificar los atributos  name y mask de la **palabra** clave. La máscara solo debe establecer un bit, entre el bit 0 y el bit 47. Los bits del 48 al 64 están reservados.

Los **atributos de** símbolo **y** mensaje son opcionales.

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
