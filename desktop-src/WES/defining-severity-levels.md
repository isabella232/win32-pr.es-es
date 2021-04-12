---
title: Definir los niveles de gravedad
description: Los niveles se usan para agrupar eventos y suelen indicar la gravedad o el nivel de detalle de un evento.
ms.assetid: dfa4e0a9-4d89-4f50-aef9-1dae0dc11726
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c8e2e979e75057a77cca267e540b3ec5469562f
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2020
ms.locfileid: "104420484"
---
# <a name="defining-severity-levels"></a><span data-ttu-id="105d9-103">Definir los niveles de gravedad</span><span class="sxs-lookup"><span data-stu-id="105d9-103">Defining Severity Levels</span></span>

<span data-ttu-id="105d9-104">Los niveles se usan para agrupar eventos y suelen indicar la gravedad o el nivel de detalle de un evento.</span><span class="sxs-lookup"><span data-stu-id="105d9-104">Levels are used to group events and typically indicate the severity or verbosity of an event.</span></span> <span data-ttu-id="105d9-105">Para definir un nivel, use el elemento **LEVEL** .</span><span class="sxs-lookup"><span data-stu-id="105d9-105">To define a level, use the **level** element.</span></span> <span data-ttu-id="105d9-106">El archivo Winmeta.xml define los siguientes niveles de gravedad usados con frecuencia:</span><span class="sxs-lookup"><span data-stu-id="105d9-106">The Winmeta.xml file defines the following commonly used severity levels:</span></span>

-   <span data-ttu-id="105d9-107">win:Critical</span><span class="sxs-lookup"><span data-stu-id="105d9-107">win:Critical</span></span>
-   <span data-ttu-id="105d9-108">win:Error</span><span class="sxs-lookup"><span data-stu-id="105d9-108">win:Error</span></span>
-   <span data-ttu-id="105d9-109">win:Warning</span><span class="sxs-lookup"><span data-stu-id="105d9-109">win:Warning</span></span>
-   <span data-ttu-id="105d9-110">win:Informational</span><span class="sxs-lookup"><span data-stu-id="105d9-110">win:Informational</span></span>
-   <span data-ttu-id="105d9-111">win:Verbose</span><span class="sxs-lookup"><span data-stu-id="105d9-111">win:Verbose</span></span>

<span data-ttu-id="105d9-112">Los consumidores usan niveles para consultar los eventos que contienen un valor de nivel específico.</span><span class="sxs-lookup"><span data-stu-id="105d9-112">Consumers use levels to query for events that contain a specific level value.</span></span> <span data-ttu-id="105d9-113">Una sesión de seguimiento de ETW también puede usar niveles para limitar los eventos que se escriben en el archivo de registro de seguimiento de eventos; los eventos con un valor de nivel igual o menor que el valor de nivel especificado se escriben en el archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="105d9-113">An ETW tracing session can also use levels to limit the events that are written to the event tracing log file; events with a level value equal to or less than the specified level value are written to the log file.</span></span> <span data-ttu-id="105d9-114">Por ejemplo, si la sesión especificó el valor de nivel de Win: Warning, el archivo de registro contendría los eventos de advertencia, error y crítico.</span><span class="sxs-lookup"><span data-stu-id="105d9-114">For example, if the session specified the level value for win:Warning, the log file would contain warning, error, and critical events.</span></span>

<span data-ttu-id="105d9-115">En el ejemplo siguiente se muestra cómo definir un nivel.</span><span class="sxs-lookup"><span data-stu-id="105d9-115">The following example shows how to define a level.</span></span> <span data-ttu-id="105d9-116">Debe especificar los atributos de **nombre** y **valor** del nivel.</span><span class="sxs-lookup"><span data-stu-id="105d9-116">You must specify the level's **name** and **value** attributes.</span></span> <span data-ttu-id="105d9-117">El valor del atributo **Value** debe estar en el intervalo comprendido entre 16 y 255.</span><span class="sxs-lookup"><span data-stu-id="105d9-117">The value of the **value** attribute must be in the range from 16 through 255.</span></span> <span data-ttu-id="105d9-118">Los atributos **Symbol** y **Message** son opcionales.</span><span class="sxs-lookup"><span data-stu-id="105d9-118">The **symbol** and **message** attributes are optional.</span></span>


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
