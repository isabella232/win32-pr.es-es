---
title: Definición de canales
description: Los eventos se pueden escribir en canales de registro de eventos, archivos de registro de seguimiento de eventos o en ambos. Un canal es básicamente un receptor que recopila eventos.
ms.assetid: 3c2f39ee-fbc0-40ae-8279-566905250f47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89c2f932616a131e478c100996fd0b76034b3cccdebf4e3714fd5b9b38ba9678
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032485"
---
# <a name="defining-channels"></a>Definición de canales

Los eventos se pueden escribir en canales de registro de eventos, archivos de registro de seguimiento de eventos o en ambos. Un canal es básicamente un receptor que recopila eventos. Si la audiencia de destino de los eventos usa consumidores de eventos como Windows Visor de eventos, debe definir nuevos canales para recopilar los eventos o importar un canal existente definido por otro proveedor.

Para definir sus propios canales, use el **elemento channel.** Para definir un canal importado, use el **elemento importChannel.** Puede especificar hasta ocho canales en cualquier combinación de canales o canales importados que defina.

El canal debe ser de uno de cuatro tipos: Admin, Operational, Analytic y Debug. Cada tipo de canal tiene una audiencia prevista, que determina el tipo de eventos que se escriben en el canal. Para obtener una descripción de cada tipo, vea el [**tipo complejo ChannelType.**](eventmanifestschema-channeltype-complextype.md)

Para especificar el canal en el que se escribe  un evento, establezca el atributo channel de la definición de evento en el mismo valor que el atributo **chid** de la definición de canal. Los eventos solo se pueden escribir en un canal a la vez, pero también se pueden recopilar hasta siete sesiones etw al mismo tiempo.

En el ejemplo siguiente se muestra cómo importar un canal. Debe establecer los atributos **chid** **y name.** El **atributo chid** identifica de forma única el canal: cada identificador de canal de la lista de canales debe ser único. Establezca el **atributo name** en el mismo nombre que usó el proveedor al definir el canal.


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

                <channels>
                    <channel chid="c1"
                             name="Microsoft-Windows-BaseProvider/Admin"
                             symbol="CHANNEL_BASEPROVIDER_ADMIN"
                             type="Admin"/>
                </channels>

                . . .

            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="Provider.Name" value="Microsoft-Windows-SampleProvider"/>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```

Aunque Winmeta.xml define canales heredados que puede importar, no debe usarlos a menos que admita consumidores heredados que consuman eventos fuera de los canales heredados (por ejemplo, aplicación o sistema). El Winmeta.xml se incluye en el SDK de Windows.

En el ejemplo siguiente se muestra cómo definir un canal. Debe establecer los **atributos chid**, **name** y **type.** El **atributo chid** identifica de forma única el canal: cada identificador de canal de la lista de canales debe ser único. Establezca el **atributo chid** en un valor que sea único para los canales que el proveedor enumera; Se hace referencia al identificador del canal en una o varias de las definiciones de eventos. La convención para asignar un nombre al canal es usar el nombre del proveedor y el tipo de canal con el formato *providername* / *channeltype*.

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

                <channels>
                    <importChannel chid="c1"
                                   name="Microsoft-Windows-BaseProvider/Admin"
                                   symbol="CHANNEL_BASEPROVIDER_ADMIN"
                                   />

                    <channel chid="c2"
                             name="Microsoft-Windows-SampleProvider/Operational"
                             type="Operational"
                             enabled="true"
                             />
                </channels>

                . . .

            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="Provider.Name" value="Microsoft-Windows-SampleProvider"/>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```
