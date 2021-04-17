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
# <a name="identifying-the-provider"></a><span data-ttu-id="022a4-104">Identificación del proveedor</span><span class="sxs-lookup"><span data-stu-id="022a4-104">Identifying the Provider</span></span>

<span data-ttu-id="022a4-105">Un manifiesto puede identificar uno o más proveedores.</span><span class="sxs-lookup"><span data-stu-id="022a4-105">A manifest can identify one or more providers.</span></span> <span data-ttu-id="022a4-106">Para identificar un proveedor, use el elemento **Provider** .</span><span class="sxs-lookup"><span data-stu-id="022a4-106">To identify a provider, use the **provider** element.</span></span> <span data-ttu-id="022a4-107">Debe especificar los atributos **Name**, **GUID**, **nombrearchivorecursos**, **messageFileName** y **Symbol** .</span><span class="sxs-lookup"><span data-stu-id="022a4-107">You must specify the **name**, **guid**, **resourceFileName**, **messageFileName**, and **symbol** attributes.</span></span> <span data-ttu-id="022a4-108">Si localiza el manifiesto, también debe especificar el atributo de **mensaje** , que los consumidores usan como mostrar el nombre del proveedor.</span><span class="sxs-lookup"><span data-stu-id="022a4-108">If you localize your manifest, you should also specify the **message** attribute, which consumers use as the display the name of the provider.</span></span> <span data-ttu-id="022a4-109">Si no se especifica el atributo **Message** , los consumidores usan el valor del atributo **Name** .</span><span class="sxs-lookup"><span data-stu-id="022a4-109">If you do not specify the **message** attribute, consumers use the value of the **name** attribute.</span></span>

<span data-ttu-id="022a4-110">Puede identificar hasta 16 proveedores en el manifiesto.</span><span class="sxs-lookup"><span data-stu-id="022a4-110">You can identify up to 16 providers in the manifest.</span></span> <span data-ttu-id="022a4-111">Si desea identificar más de 16 proveedores, debe incluir la sección **messageTable** del manifiesto que los proveedores decimoséptima y on deben usar para asignar valores de recursos para las cadenas de mensaje que definen; la tabla de mensajes no debe incluir las cadenas de mensajes que se hayan definido entre el 1 y el 16.</span><span class="sxs-lookup"><span data-stu-id="022a4-111">If you want to identify more than 16 providers, you must include the **messageTable** section of the manifest that the seventeenth and on providers must use to assign resource values for the message strings that they define—the message table must not include any message strings that providers 1 through 16 defined.</span></span>

<span data-ttu-id="022a4-112">En el ejemplo siguiente se muestra cómo utilizar el elemento **Provider** para identificar un proveedor.</span><span class="sxs-lookup"><span data-stu-id="022a4-112">The following example shows how to use the **provider** element to identify a provider.</span></span>


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
