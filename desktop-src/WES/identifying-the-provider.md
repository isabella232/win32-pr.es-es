---
title: Identificación del proveedor
description: Un manifiesto puede identificar uno o varios proveedores. Para identificar un proveedor, use el elemento provider.
ms.assetid: 3bd40405-2b7a-4709-aef7-8615de8c5b6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbce9b07aa8a2322311397ae9a48b3d72d60b784e5c55b028afc9772b53f63d9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119470934"
---
# <a name="identifying-the-provider"></a>Identificación del proveedor

Un manifiesto puede identificar uno o varios proveedores. Para identificar un proveedor, use el **elemento provider.** Debe especificar los atributos **name**, **guid**, **resourceFileName**, **messageFileName** y **symbol.** Si localiza el manifiesto, también debe especificar el atributo **de** mensaje, que los consumidores usan como para mostrar el nombre del proveedor. Si no especifica el atributo **de mensaje,** los consumidores usan el valor del **atributo name.**

Puede identificar hasta 16 proveedores en el manifiesto. Si desea identificar más de 16 proveedores, debe incluir la sección **messageTable** del manifiesto que los proveedores de 1 a 16 deben usar para asignar valores de recursos para las cadenas de mensaje que definen. La tabla de mensajes no debe incluir ninguna cadena de mensaje definida por los proveedores del 1 al 16.

En el ejemplo siguiente se muestra cómo usar el **elemento provider** para identificar un proveedor.


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
