---
title: Definir niveles de gravedad
description: Los niveles se usan para agrupar eventos y normalmente indican la gravedad o el nivel de detalle de un evento.
ms.assetid: dfa4e0a9-4d89-4f50-aef9-1dae0dc11726
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c8e2e979e75057a77cca267e540b3ec5469562f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126885537"
---
# <a name="defining-severity-levels"></a>Definir niveles de gravedad

Los niveles se usan para agrupar eventos y normalmente indican la gravedad o el nivel de detalle de un evento. Para definir un nivel, use el **elemento level.** El Winmeta.xml archivo define los siguientes niveles de gravedad usados habitualmente:

-   win:Critical
-   win:Error
-   win:Warning
-   win:Informational
-   win:Verbose

Los consumidores usan niveles para consultar eventos que contienen un valor de nivel específico. Una sesión de seguimiento de ETW también puede usar niveles para limitar los eventos que se escriben en el archivo de registro de seguimiento de eventos; Los eventos con un valor de nivel igual o menor que el valor de nivel especificado se escriben en el archivo de registro. Por ejemplo, si la sesión especifica el valor de nivel para win:Warning, el archivo de registro contendrá eventos críticos, de error y de advertencia.

En el ejemplo siguiente se muestra cómo definir un nivel. Debe especificar los atributos de nombre **y** **valor del** nivel. El valor del atributo **value** debe estar en el intervalo de 16 a 255. Los **atributos de** símbolo **y** mensaje son opcionales.


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

                <levels>
                    <level name="NotValid"
                           value="16"
                           symbol="LEVEL_SAMPLEPROVIDER_NOTVALID"
                           message="$(string.Level.NotValid)"/>
                    <level name="Valid"
                           value="17"
                           symbol="LEVEL_SAMPLEPROVIDER_VALID"
                           message="$(string.Level.Valid)"/>
                </levels>

                . . .

            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="Provider.Name" value="Sample Provider"/>
                <string id="Level.Valid" value="Valid"/>
                <string id="Level.NotValid" value="Not Valid"/>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```
