---
title: Identificación del proveedor
description: Un manifiesto puede identificar uno o más proveedores. Para identificar un proveedor, use el elemento Provider.
ms.assetid: 3bd40405-2b7a-4709-aef7-8615de8c5b6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45941a540f8804beccc408435fc202593ddad601
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2020
ms.locfileid: "104533058"
---
# <a name="identifying-the-provider"></a>Identificación del proveedor

Un manifiesto puede identificar uno o más proveedores. Para identificar un proveedor, use el elemento **Provider** . Debe especificar los atributos **Name**, **GUID**, **nombrearchivorecursos**, **messageFileName** y **Symbol** . Si localiza el manifiesto, también debe especificar el atributo de **mensaje** , que los consumidores usan como mostrar el nombre del proveedor. Si no se especifica el atributo **Message** , los consumidores usan el valor del atributo **Name** .

Puede identificar hasta 16 proveedores en el manifiesto. Si desea identificar más de 16 proveedores, debe incluir la sección **messageTable** del manifiesto que los proveedores decimoséptima y on deben usar para asignar valores de recursos para las cadenas de mensaje que definen; la tabla de mensajes no debe incluir las cadenas de mensajes que se hayan definido entre el 1 y el 16.

En el ejemplo siguiente se muestra cómo utilizar el elemento **Provider** para identificar un proveedor.


```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="https://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="https://www.w3.org/2001/XMLSchema"    
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
