---
title: Definición de filtros
description: Un proveedor puede definir los filtros que una sesión utiliza para filtrar los eventos basándose en los datos de evento.
ms.assetid: b43912af-0e9c-414b-b3fa-03e7e35e493c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61dd2a21b9c4e01ebc4a32a160b24022c79197b0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149557"
---
# <a name="defining-filters"></a><span data-ttu-id="ea17b-103">Definición de filtros</span><span class="sxs-lookup"><span data-stu-id="ea17b-103">Defining Filters</span></span>

<span data-ttu-id="ea17b-104">Un proveedor puede definir los filtros que una sesión utiliza para filtrar los eventos basándose en los datos de evento.</span><span class="sxs-lookup"><span data-stu-id="ea17b-104">A provider can define filters that a session uses to filter events based on event data.</span></span> <span data-ttu-id="ea17b-105">Con el nivel y las palabras clave, ETW determina si el evento se escribe en el registro.</span><span class="sxs-lookup"><span data-stu-id="ea17b-105">With level and keywords, ETW determines whether the event is written to the log.</span></span> <span data-ttu-id="ea17b-106">Sin embargo, con los filtros, el proveedor utiliza los criterios de datos de filtro que la sesión de control le pasa (vea la función [*EnableCallback*](/windows/desktop/api/evntprov/nc-evntprov-penablecallback) ) para determinar si escribe el evento en esa sesión.</span><span class="sxs-lookup"><span data-stu-id="ea17b-106">However, with filters, the provider uses the filter data criteria that the controlling session passes to it (see the [*EnableCallback*](/windows/desktop/api/evntprov/nc-evntprov-penablecallback) function) to determine whether it writes the event to that session.</span></span> <span data-ttu-id="ea17b-107">Los filtros solo se aplican cuando una sesión de seguimiento de ETW habilita el proveedor.</span><span class="sxs-lookup"><span data-stu-id="ea17b-107">The filters are applicable only when an ETW tracing session enables your provider.</span></span>

<span data-ttu-id="ea17b-108">Normalmente, los proveedores simplemente escriben eventos y la sesión identifica los tipos de eventos que desea usar el nivel y las palabras clave.</span><span class="sxs-lookup"><span data-stu-id="ea17b-108">Typically, providers just write events, and the session identifies the types of events that it wants using level and keywords.</span></span> <span data-ttu-id="ea17b-109">Si el proveedor definía un filtro de datos para un tipo de evento, la sesión podría utilizarlo para filtrar los eventos de ese tipo de evento en función de los datos de evento (la semántica del filtro se define mediante el proveedor).</span><span class="sxs-lookup"><span data-stu-id="ea17b-109">If the provider defined a data filter for an event type, the session could use it to filter out events for that event type based on the event data (the semantics of the filter is defined by the provider).</span></span> <span data-ttu-id="ea17b-110">Por ejemplo, si el proveedor genera eventos de proceso, podría definir un filtro de datos que filtrara los eventos de proceso en función de un identificador de proceso.</span><span class="sxs-lookup"><span data-stu-id="ea17b-110">For example, if your provider generates process events, you could define a data filter that filtered process events based on a process identifier.</span></span> <span data-ttu-id="ea17b-111">A continuación, la sesión podría pasar un identificador de proceso como datos de filtro al proveedor y recibir solo los eventos de proceso para ese identificador de proceso.</span><span class="sxs-lookup"><span data-stu-id="ea17b-111">The session could then pass a process identifier as filter data to the provider and receive only process events for that process identifier.</span></span>

<span data-ttu-id="ea17b-112">En el ejemplo siguiente se muestra cómo utilizar el elemento **Filter** para definir un filtro.</span><span class="sxs-lookup"><span data-stu-id="ea17b-112">The following example shows how to use the **filter** element to define a filter.</span></span> <span data-ttu-id="ea17b-113">Debe especificar los atributos de **nombre** y **valor** del filtro; los demás atributos son opcionales.</span><span class="sxs-lookup"><span data-stu-id="ea17b-113">You must specify the filter's **name** and **value** attributes; the other attributes are optional.</span></span> <span data-ttu-id="ea17b-114">El atributo **TID** es obligatorio si el filtro requiere que la sesión pase los datos de filtro.</span><span class="sxs-lookup"><span data-stu-id="ea17b-114">The **tid** attribute is required if the filter requires that the session pass filter data.</span></span>


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

                <filters>
                    <filter name="Pid"
                            value="1"
                            tid="t1"
                            symbol="FILTER_PID"/>
                </filters>

                <templates>
                    <template tid="t1">
                        <data name="Pid" inType="win:UInt32"/>
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
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```