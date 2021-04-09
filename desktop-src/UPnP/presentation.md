---
title: Presentación
description: La presentación es el último paso del proceso de UPnP.
ms.assetid: e8d20ae6-2dd8-4de2-b07b-6cf4e725735e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 195399316882de71c148f2369dd2978c4cfbd728
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903381"
---
# <a name="presentation"></a><span data-ttu-id="00bf9-103">Presentación</span><span class="sxs-lookup"><span data-stu-id="00bf9-103">Presentation</span></span>

<span data-ttu-id="00bf9-104">La presentación es el último paso del proceso de UPnP.</span><span class="sxs-lookup"><span data-stu-id="00bf9-104">Presentation is the final step in the UPnP process.</span></span> <span data-ttu-id="00bf9-105">Si un dispositivo tiene una dirección URL para la presentación, un punto de control puede recuperar una página de esta dirección URL y cargar la página en un explorador.</span><span class="sxs-lookup"><span data-stu-id="00bf9-105">If a device has a URL for presentation, a control point can retrieve a page from this URL and load the page into a browser.</span></span> <span data-ttu-id="00bf9-106">En función de las capacidades de la página de presentación y del dispositivo, el punto de control puede controlar el dispositivo y ver el estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="00bf9-106">Depending on the capabilities of the presentation page and the device, the control point can control the device and view the status of the device.</span></span>

<span data-ttu-id="00bf9-107">La ruta de acceso del recurso, que se pasa a [**IUPnPRegistrar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpregistrar) durante el registro, es donde se encuentran todos los archivos relevantes para la presentación del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="00bf9-107">The resource path, which is passed to [**IUPnPRegistrar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpregistrar) during registration, is where all the files relevant to the presentation of the device are located.</span></span> <span data-ttu-id="00bf9-108">Los desarrolladores de dispositivos pueden proporcionar páginas independientes para cada dispositivo incrustado.</span><span class="sxs-lookup"><span data-stu-id="00bf9-108">Device developers can provide separate pages for each embedded device.</span></span> <span data-ttu-id="00bf9-109">La dirección URL de la presentación en la plantilla Descripción del dispositivo puede ser una dirección URL absoluta o relativa.</span><span class="sxs-lookup"><span data-stu-id="00bf9-109">The presentation URL in the device description template can either be an absolute URL or a relative URL.</span></span> <span data-ttu-id="00bf9-110">En el caso de las direcciones URL relativas, que son relativas a la ruta de acceso del recurso, la plantilla de Descripción del dispositivo debe contener un nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="00bf9-110">For relative URLs, which are relative to the resource path, the device description template should contain a file name.</span></span> <span data-ttu-id="00bf9-111">**IUPnPRegistrar** lo convierte en una dirección URL con la ubicación real.</span><span class="sxs-lookup"><span data-stu-id="00bf9-111">**IUPnPRegistrar** converts this to a URL with the actual location.</span></span> <span data-ttu-id="00bf9-112">En el caso de las direcciones URL absolutas, la ubicación no se modifica.</span><span class="sxs-lookup"><span data-stu-id="00bf9-112">For absolute URLs, the location is not modified.</span></span>

<span data-ttu-id="00bf9-113">Para admitir los scripts del lado cliente dentro de una página de presentación, normalmente se anexa información adicional a la dirección URL en forma de "cadena de consulta".</span><span class="sxs-lookup"><span data-stu-id="00bf9-113">To support client side scripts within a presentation page, extra information is normally appended to the URL in the form of a "query string".</span></span> <span data-ttu-id="00bf9-114">La información adicional que se anexa es la dirección URL del documento de Descripción del dispositivo y el UDN del dispositivo o del dispositivo incrustado.</span><span class="sxs-lookup"><span data-stu-id="00bf9-114">The extra information that is appended is the URL to the device description document, and the UDN of the device or embedded device.</span></span> <span data-ttu-id="00bf9-115">La dirección URL de Descripción del dispositivo se puede usar para cargar un documento de descripción en el script y, a continuación, controlar el dispositivo a través de sus servicios.</span><span class="sxs-lookup"><span data-stu-id="00bf9-115">The device description URL can be used to load a description document in the script, and then control the device through its services.</span></span> <span data-ttu-id="00bf9-116">El UDN se usa para seleccionar un dispositivo incrustado desde el dispositivo raíz.</span><span class="sxs-lookup"><span data-stu-id="00bf9-116">The UDN is used to select an embedded device from the root device.</span></span>

<span data-ttu-id="00bf9-117">El formato de la dirección URL de presentación modificada es: la dirección URL de presentación real, un signo de interrogación ("?"), la dirección URL de la descripción del dispositivo, un signo más ("+"), el dispositivo UDN.</span><span class="sxs-lookup"><span data-stu-id="00bf9-117">The format of the modified presentation URL is: the actual presentation URL, a question mark ("?"), the device description URL, a plus sign ("+"), the device UDN.</span></span> <span data-ttu-id="00bf9-118">El signo de interrogación denota el inicio de la cadena de consulta.</span><span class="sxs-lookup"><span data-stu-id="00bf9-118">The question mark denotes the start of the query string.</span></span>

<span data-ttu-id="00bf9-119">Si la dirección URL de la presentación en la plantilla de Descripción del dispositivo era una dirección URL absoluta y ya contenía un signo de interrogación ("?"), la información adicional no se agrega a la dirección URL de la presentación.</span><span class="sxs-lookup"><span data-stu-id="00bf9-119">If the presentation URL in the device description template was an absolute URL and it already contained a question mark ("?"), then the extra information is not added to the presentation URL.</span></span>



| <span data-ttu-id="00bf9-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="00bf9-120">Description</span></span>                        | <span data-ttu-id="00bf9-121">URL</span><span class="sxs-lookup"><span data-stu-id="00bf9-121">URL</span></span>                                                                                                                                               |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00bf9-122">En la plantilla de Descripción del dispositivo</span><span class="sxs-lookup"><span data-stu-id="00bf9-122">In the device description template</span></span> | <span data-ttu-id="00bf9-123">**presentationURL** MyDevice.html **/presentationURL**</span><span class="sxs-lookup"><span data-stu-id="00bf9-123">**presentationURL** MyDevice.html **/presentationURL**</span></span>                                                                                              |
| <span data-ttu-id="00bf9-124">Generado por el host del dispositivo</span><span class="sxs-lookup"><span data-stu-id="00bf9-124">Generated by the device host</span></span>       | <span data-ttu-id="00bf9-125">**presentationURL** https://machinename/deviceID/MyDevice.html/?https://machine/upnphost/udhisapi.dll?content=uuid:487394 ...</span><span class="sxs-lookup"><span data-stu-id="00bf9-125">**presentationURL**https://machinename/deviceID/MyDevice.html/?https://machine/upnphost/udhisapi.dll?content=uuid:487394…</span></span> <span data-ttu-id="00bf9-126">+ UDN **/presentationURL**</span><span class="sxs-lookup"><span data-stu-id="00bf9-126">+ UDN **/presentationURL**</span></span> |



 

<span data-ttu-id="00bf9-127">Es posible que un script del lado cliente tenga que extraer la dirección URL de la descripción del dispositivo de la dirección URL de presentación para cargar el objeto [**IUPnPDescriptionDocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument) .</span><span class="sxs-lookup"><span data-stu-id="00bf9-127">A client-side script may have to extract the device description URL from the presentation URL to load the [**IUPnPDescriptionDocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument) object.</span></span> <span data-ttu-id="00bf9-128">Para ello, se toma la cadena de consulta y se termina en el signo más ("+").</span><span class="sxs-lookup"><span data-stu-id="00bf9-128">This is done by taking the query string, and terminating it at the plus sign ("+").</span></span>


```VB
Dim QueryString
QueryString = window.location.search
Dim DescURLString
DescURLString = Trim(Mid(QueryString,2,Instr(QueryString,"+")-2))& vbCrLf

    Dim LightDesc
    Set LightDesc = CreateObject("UPnP.DescriptionDocument.1")
    LightDesc.Load(DescURLString)
```



<span data-ttu-id="00bf9-129">En el caso de una página de presentación de un dispositivo incrustado, se requiere algún trabajo adicional.</span><span class="sxs-lookup"><span data-stu-id="00bf9-129">In the case of a presentation page for an embedded device, some additional work is required.</span></span> <span data-ttu-id="00bf9-130">Después de cargar el [**UPnPDescriptionDocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument), el script debe obtener la colección de dispositivos incrustados y, a continuación, seleccionar el dispositivo que coincida con el valor de UDN en la cadena de consulta.</span><span class="sxs-lookup"><span data-stu-id="00bf9-130">After loading the [**UPnPDescriptionDocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument), the script must obtain the collection of embedded devices, then select the device that matches the UDN in the query string.</span></span> <span data-ttu-id="00bf9-131">El siguiente script muestra cómo seleccionar el dispositivo incrustado para la página de presentación actual.</span><span class="sxs-lookup"><span data-stu-id="00bf9-131">The following script shows how to select the embedded device for the current presentation page.</span></span> <span data-ttu-id="00bf9-132">Supone que LightDesc ya está cargado.</span><span class="sxs-lookup"><span data-stu-id="00bf9-132">It assumes LightDesc is already loaded.</span></span>


```VB
Dim LightDevice
Set LightDevice = LightDesc.RootDevice

Dim EmbeddedDevices 
set EmbeddedDevices = LightDevice.Children

Dim DeviceUdnString
DeviceUdnString = Trim(Mid(QueryString,Instr(QueryString,"+")+1,Len(QueryString)))

Dim Item
set Item = EmbeddedDevices.Item(DeviceUdnString)
```



 

 




