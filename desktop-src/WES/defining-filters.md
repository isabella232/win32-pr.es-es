---
title: Definición de filtros
description: Un proveedor puede definir filtros que una sesión usa para filtrar eventos en función de los datos de eventos.
ms.assetid: b43912af-0e9c-414b-b3fa-03e7e35e493c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37d9d065fe3a46fc22114cfb4aed5b5b51d9a89eafa3280e2e258199e06aad3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056023"
---
# <a name="defining-filters"></a>Definición de filtros

Un proveedor puede definir filtros que una sesión usa para filtrar eventos en función de los datos de eventos. Con las palabras clave level y , ETW determina si el evento se escribe en el registro. Sin embargo, con los filtros, el proveedor usa los criterios de datos de filtro que la sesión de control le pasa (vea la función [*EnableCallback)*](/windows/desktop/api/evntprov/nc-evntprov-penablecallback) para determinar si escribe el evento en esa sesión. Los filtros solo son aplicables cuando una sesión de seguimiento de ETW habilita al proveedor.

Normalmente, los proveedores solo escriben eventos y la sesión identifica los tipos de eventos que desea usar las palabras clave level y . Si el proveedor definió un filtro de datos para un tipo de evento, la sesión podría usarlo para filtrar los eventos de ese tipo de evento en función de los datos del evento (el proveedor define la semántica del filtro). Por ejemplo, si el proveedor genera eventos de proceso, podría definir un filtro de datos que filtrara los eventos de proceso en función de un identificador de proceso. A continuación, la sesión podría pasar un identificador de proceso como datos de filtro al proveedor y recibir solo eventos de proceso para ese identificador de proceso.

En el ejemplo siguiente se muestra cómo usar el **elemento filter** para definir un filtro. Debe especificar los atributos de nombre **y** **valor del** filtro; los demás atributos son opcionales. El **atributo tid** es necesario si el filtro requiere que la sesión pase los datos del filtro.


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