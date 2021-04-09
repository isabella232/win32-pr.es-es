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
# <a name="defining-channels"></a><span data-ttu-id="b4a45-104">Definir canales</span><span class="sxs-lookup"><span data-stu-id="b4a45-104">Defining Channels</span></span>

<span data-ttu-id="b4a45-105">Los eventos se pueden escribir en canales de registro de eventos, archivos de registro de seguimiento de eventos o ambos.</span><span class="sxs-lookup"><span data-stu-id="b4a45-105">Events can be written to event log channels, event tracing log files, or both.</span></span> <span data-ttu-id="b4a45-106">Un canal es básicamente un receptor que recopila eventos.</span><span class="sxs-lookup"><span data-stu-id="b4a45-106">A channel is basically a sink that collects events.</span></span> <span data-ttu-id="b4a45-107">Si el público de destino de los eventos usa consumidores de eventos como el Visor de eventos de Windows, debe definir canales nuevos para recopilar los eventos o importar un canal existente definido por otro proveedor.</span><span class="sxs-lookup"><span data-stu-id="b4a45-107">If the target audience for your events uses event consumers such as the Windows Event Viewer, you must define new channels to collect your events or import an existing channel that another provider defined.</span></span>

<span data-ttu-id="b4a45-108">Para definir sus propios canales, use el elemento **Channel** .</span><span class="sxs-lookup"><span data-stu-id="b4a45-108">To define your own channels, use the **channel** element.</span></span> <span data-ttu-id="b4a45-109">Para definir un canal importado, use el elemento **importChannel** .</span><span class="sxs-lookup"><span data-stu-id="b4a45-109">To define an imported channel, use the **importChannel** element.</span></span> <span data-ttu-id="b4a45-110">Puede especificar hasta ocho canales en cualquier combinación de canales o canales importados que defina.</span><span class="sxs-lookup"><span data-stu-id="b4a45-110">You can specify up to eight channels in any combination of imported channels or channels that you define.</span></span>

<span data-ttu-id="b4a45-111">El canal debe ser de uno de cuatro tipos: admin, Operational, Analytics y Debug.</span><span class="sxs-lookup"><span data-stu-id="b4a45-111">The channel must be of one of four types: Admin, Operational, Analytic, and Debug.</span></span> <span data-ttu-id="b4a45-112">Cada tipo de canal tiene un público previsto, que determina el tipo de eventos que se escriben en el canal.</span><span class="sxs-lookup"><span data-stu-id="b4a45-112">Each channel type has an intended audience, which determines the type of events that you write to the channel.</span></span> <span data-ttu-id="b4a45-113">Para obtener una descripción de cada tipo, vea el tipo complejo de [**ChannelType**](eventmanifestschema-channeltype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="b4a45-113">For a description of each type, see the [**ChannelType**](eventmanifestschema-channeltype-complextype.md) complex type.</span></span>

<span data-ttu-id="b4a45-114">Para especificar el canal en el que se escribe un evento, establezca el atributo de **canal** de la definición de evento en el mismo valor que el atributo **chid** de la definición de canal.</span><span class="sxs-lookup"><span data-stu-id="b4a45-114">To specify the channel to which an event is written, set the event definition's **channel** attribute to the same value as the channel definition's **chid** attribute.</span></span> <span data-ttu-id="b4a45-115">Los eventos solo se pueden escribir en un canal cada vez, pero también se pueden recopilar hasta 7 otras sesiones de ETW al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="b4a45-115">Events can only be written to one channel at a time, but can also be collected by up to 7 other ETW sessions at the same time.</span></span>

<span data-ttu-id="b4a45-116">En el ejemplo siguiente se muestra cómo importar un canal.</span><span class="sxs-lookup"><span data-stu-id="b4a45-116">The following example shows how to import a channel.</span></span> <span data-ttu-id="b4a45-117">Debe establecer los atributos **chid** y **Name** .</span><span class="sxs-lookup"><span data-stu-id="b4a45-117">You must set the **chid** and **name** attributes.</span></span> <span data-ttu-id="b4a45-118">El atributo **chid** identifica de forma única el canal: cada identificador de canal de la lista de canales debe ser único.</span><span class="sxs-lookup"><span data-stu-id="b4a45-118">The **chid** attribute uniquely identifies the channel—each channel identifier in your list of channels must be unique.</span></span> <span data-ttu-id="b4a45-119">Establezca el atributo de **nombre** en el mismo nombre que el proveedor utilizado cuando definió el canal.</span><span class="sxs-lookup"><span data-stu-id="b4a45-119">Set the **name** attribute to the same name that the provider used when it defined the channel.</span></span>


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

<span data-ttu-id="b4a45-120">Aunque Winmeta.xml define canales heredados que se pueden importar, no debe usarlos a menos que sea compatible con consumidores heredados que consuman eventos de los canales heredados (por ejemplo, aplicación o sistema).</span><span class="sxs-lookup"><span data-stu-id="b4a45-120">Although Winmeta.xml defines legacy channels that you can import, you should not use them unless you are supporting legacy consumers that consume events out of the legacy channels (for example, Application or System).</span></span> <span data-ttu-id="b4a45-121">El archivo Winmeta.xml se incluye en el Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="b4a45-121">The Winmeta.xml file is included in the Windows SDK.</span></span>

<span data-ttu-id="b4a45-122">En el ejemplo siguiente se muestra cómo definir un canal.</span><span class="sxs-lookup"><span data-stu-id="b4a45-122">The following example shows how to define a channel.</span></span> <span data-ttu-id="b4a45-123">Debe establecer los atributos **chid**, **Name** y **Type** .</span><span class="sxs-lookup"><span data-stu-id="b4a45-123">You must set the **chid**, **name**, and **type** attributes.</span></span> <span data-ttu-id="b4a45-124">El atributo **chid** identifica de forma única el canal: cada identificador de canal de la lista de canales debe ser único.</span><span class="sxs-lookup"><span data-stu-id="b4a45-124">The **chid** attribute uniquely identifies the channel—each channel identifier in your list of channels must be unique.</span></span> <span data-ttu-id="b4a45-125">Establezca el atributo **chid** en un valor que sea único para los canales enumerados por el proveedor. se hace referencia al identificador de canal en una o varias de sus definiciones de eventos.</span><span class="sxs-lookup"><span data-stu-id="b4a45-125">Set the **chid** attribute to a value that is unique for the channels that your provider lists; the channel identifier is referenced in one or more of your event definitions.</span></span> <span data-ttu-id="b4a45-126">La Convención para asignar nombres al canal es usar el nombre del proveedor y el tipo de canal con el formato *providerName* / *channeltype*.</span><span class="sxs-lookup"><span data-stu-id="b4a45-126">The convention for naming the channel is to use the provider name and channel type in the form, *providername*/*channeltype*.</span></span>

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
