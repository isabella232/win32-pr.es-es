---
title: Definir palabras clave utilizadas para clasificar tipos de eventos
description: Los proveedores usan palabras clave para clasificar distintos tipos de eventos.
ms.assetid: 1cbad719-bc59-4255-8a15-9e45f363d199
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d48992c5cbafec5f945fa2f133924ccf0e2e7e96
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2020
ms.locfileid: "103904447"
---
# <a name="defining-keywords-used-to-classify-types-of-events"></a><span data-ttu-id="ae2f1-103">Definir palabras clave utilizadas para clasificar tipos de eventos</span><span class="sxs-lookup"><span data-stu-id="ae2f1-103">Defining Keywords Used to Classify Types of Events</span></span>

<span data-ttu-id="ae2f1-104">Los proveedores usan palabras clave para clasificar distintos tipos de eventos.</span><span class="sxs-lookup"><span data-stu-id="ae2f1-104">Providers use keywords to classify different types of events.</span></span> <span data-ttu-id="ae2f1-105">Por ejemplo, puede crear una palabra clave para todos los eventos de lectura y, a continuación, aplicar la palabra clave Read a cualquier evento que realice una operación de lectura, como la lectura desde un archivo o un registro.</span><span class="sxs-lookup"><span data-stu-id="ae2f1-105">For example, you can create a keyword for all read events and then apply the read keyword to any event that performs a read operation such as reading from a file or registry.</span></span> <span data-ttu-id="ae2f1-106">A continuación, los consumidores pueden usar los valores de bit de palabra clave para filtrar la clasificación de los distintos eventos.</span><span class="sxs-lookup"><span data-stu-id="ae2f1-106">Consumers could then use the keyword bit values to filter for different classification of events.</span></span> <span data-ttu-id="ae2f1-107">Por ejemplo, el consumidor podría solicitar todos los eventos de lectura o todos los eventos de lectura de la tarea X (si también agrupa eventos por tarea).</span><span class="sxs-lookup"><span data-stu-id="ae2f1-107">For example, the consumer could request all read events or all read events from task X (if you also group events by task).</span></span> <span data-ttu-id="ae2f1-108">Para definir una palabra clave, use el elemento de **palabra clave** .</span><span class="sxs-lookup"><span data-stu-id="ae2f1-108">To define a keyword, use the **keyword** element.</span></span>

<span data-ttu-id="ae2f1-109">Una sesión de seguimiento de ETW puede usar las palabras clave (de la misma forma que usa LEVEL) para limitar los eventos que el servicio ETW escribe en el archivo de registro de seguimiento de eventos.</span><span class="sxs-lookup"><span data-stu-id="ae2f1-109">An ETW tracing session can use the keywords (in the same way that it uses level) to limit the events that the ETW service writes to its event tracing log file.</span></span> <span data-ttu-id="ae2f1-110">Una sesión de seguimiento puede habilitar el proveedor mediante dos conjuntos de máscaras de fotopalabras clave: una máscara de bits "any" en la que se escribe el evento si cualquiera de los bits de palabra clave del evento coincide con cualquiera de los bits establecidos en esta máscara, y una máscara de bits "All" donde los eventos que coinciden con el caso "any", el evento se escribe solo si todos los bits de la máscara "All" existen en la máscara de la palabra clave</span><span class="sxs-lookup"><span data-stu-id="ae2f1-110">A tracing session can enable the provider using two sets of keyword bitmasks: an "Any" bitmask where the event is written if any of the event's keyword bits match any of the bits set in this mask, and an "All" bitmask where for those events that matched the "Any" case, the event is written only if all of the bits in the "All" mask exist in the event's keyword bitmask.</span></span>

<span data-ttu-id="ae2f1-111">Por ejemplo, si el proveedor define un evento que especifica una palabra clave Read (bit 0) y una palabra clave de acceso local (bit 1), y un segundo evento que especifica una palabra clave Read (bit 0) y una palabra clave de acceso remoto (bit 2), puede establecer la máscara de bits "any" en 1 para recibir todos los eventos leídos, o bien puede establecer la máscara de bits "any" en 1 y "All" en 3 para recibir solo las lecturas locales.</span><span class="sxs-lookup"><span data-stu-id="ae2f1-111">For example, if the provider defines an event that specifies a read keyword (bit 0) and a local access keyword (bit 1), and a second event that specifies a read keyword (bit 0) and a remote access keyword (bit 2), you could set the "Any" bitmask to 1 to receive all read events, or you could set the "Any" bitmask to 1 and "All" bitmask to 3 to receive only local reads.</span></span>

<span data-ttu-id="ae2f1-112">Debe especificar los atributos **Name** y **Mask** de la palabra clave.</span><span class="sxs-lookup"><span data-stu-id="ae2f1-112">You must specify the keyword's **name** and **mask** attributes.</span></span> <span data-ttu-id="ae2f1-113">La máscara solo debe establecer un bit, entre el bit 0 y el bit 47.</span><span class="sxs-lookup"><span data-stu-id="ae2f1-113">The mask must set only one bit, between bit 0 and bit 47.</span></span> <span data-ttu-id="ae2f1-114">Los bits 48 a 64 están reservados.</span><span class="sxs-lookup"><span data-stu-id="ae2f1-114">Bits 48 through 64 are reserved.</span></span>

<span data-ttu-id="ae2f1-115">Los atributos **Symbol** y **Message** son opcionales.</span><span class="sxs-lookup"><span data-stu-id="ae2f1-115">The **symbol** and **message** attributes are optional.</span></span>

<span data-ttu-id="ae2f1-116">En el ejemplo siguiente se muestra cómo definir una palabra clave.</span><span class="sxs-lookup"><span data-stu-id="ae2f1-116">The following example shows how to define a keyword.</span></span>

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

                <keywords>
                    <keyword name="Read" mask="0x1" symbol="READ_KEYWORD"/>
                    <keyword name="Write" mask="0x2" symbol="WRITE_KEYWORD"/>
                    <keyword name="Local" mask="0x4" symbol="LOCAL_KEYWORD"/>
                    <keyword name="Remote" mask="0x8" symbol="REMOTE_KEYWORD"/>
                </keywords>

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
