---
title: Definir canales
description: Los eventos se pueden escribir en canales de registro de eventos, archivos de registro de seguimiento de eventos o ambos. Un canal es básicamente un receptor que recopila eventos.
ms.assetid: 3c2f39ee-fbc0-40ae-8279-566905250f47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab3c73697aa11e7b63ace0ece33be23ca7a1b883
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2020
ms.locfileid: "104149134"
---
# <a name="defining-channels"></a>Definir canales

Los eventos se pueden escribir en canales de registro de eventos, archivos de registro de seguimiento de eventos o ambos. Un canal es básicamente un receptor que recopila eventos. Si el público de destino de los eventos usa consumidores de eventos como el Visor de eventos de Windows, debe definir canales nuevos para recopilar los eventos o importar un canal existente definido por otro proveedor.

Para definir sus propios canales, use el elemento **Channel** . Para definir un canal importado, use el elemento **importChannel** . Puede especificar hasta ocho canales en cualquier combinación de canales o canales importados que defina.

El canal debe ser de uno de cuatro tipos: admin, Operational, Analytics y Debug. Cada tipo de canal tiene un público previsto, que determina el tipo de eventos que se escriben en el canal. Para obtener una descripción de cada tipo, vea el tipo complejo de [**ChannelType**](eventmanifestschema-channeltype-complextype.md) .

Para especificar el canal en el que se escribe un evento, establezca el atributo de **canal** de la definición de evento en el mismo valor que el atributo **chid** de la definición de canal. Los eventos solo se pueden escribir en un canal cada vez, pero también se pueden recopilar hasta 7 otras sesiones de ETW al mismo tiempo.

En el ejemplo siguiente se muestra cómo importar un canal. Debe establecer los atributos **chid** y **Name** . El atributo **chid** identifica de forma única el canal: cada identificador de canal de la lista de canales debe ser único. Establezca el atributo de **nombre** en el mismo nombre que el proveedor utilizado cuando definió el canal.


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

Aunque Winmeta.xml define canales heredados que se pueden importar, no debe usarlos a menos que sea compatible con consumidores heredados que consuman eventos de los canales heredados (por ejemplo, aplicación o sistema). El archivo Winmeta.xml se incluye en el Windows SDK.

En el ejemplo siguiente se muestra cómo definir un canal. Debe establecer los atributos **chid**, **Name** y **Type** . El atributo **chid** identifica de forma única el canal: cada identificador de canal de la lista de canales debe ser único. Establezca el atributo **chid** en un valor que sea único para los canales enumerados por el proveedor. se hace referencia al identificador de canal en una o varias de sus definiciones de eventos. La Convención para asignar nombres al canal es usar el nombre del proveedor y el tipo de canal con el formato *providerName* / *channeltype*.

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
