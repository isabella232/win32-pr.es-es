---
title: Datos de la secuencia de registro
description: Datos de la secuencia de registro
ms.assetid: c902a755-afdd-4dea-bc3e-036555fdff10
keywords:
- Listas de reproducción de metarchivos de Windows Media, datos de flujo de registro
- listas de reproducción, datos de flujo de registro
- listas de reproducción de metarchivos, datos de secuencias de registro
- Listas de reproducción de metarchivos de Windows Media, registro de datos de flujo
- listas de reproducción, registro de datos de secuencias
- listas de reproducción de metarchivos, registro de datos de secuencias
- datos de la secuencia de registro
- registro de datos de flujo
- Windows Media Player, registro de datos de flujo
- Media Player de Windows, registro de datos de flujo
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f234851cabf071ed2308fb5c96df2b53b60b9d45
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104148859"
---
# <a name="logging-stream-data"></a><span data-ttu-id="3b617-113">Datos de la secuencia de registro</span><span class="sxs-lookup"><span data-stu-id="3b617-113">Logging Stream Data</span></span>

<span data-ttu-id="3b617-114">La información registrada puede adquirirse y usarse para determinar el comportamiento del visor, por ejemplo, la frecuencia con la que se ve un flujo o si un usuario específico vio un flujo y el tiempo de calidad.</span><span class="sxs-lookup"><span data-stu-id="3b617-114">Logged information can be acquired and used to determine viewer behavior, for example, how often a stream is viewed, or if a specific user viewed a stream and for how long at what quality.</span></span>

<span data-ttu-id="3b617-115">La información de registro se envía automáticamente al servidor desde el que se originó la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="3b617-115">Logging information is automatically sent to the server from which the playlist originated.</span></span> <span data-ttu-id="3b617-116">También puede enviar información de registro a servidores adicionales, incluidos los servidores web que usa exclusivamente para el registro.</span><span class="sxs-lookup"><span data-stu-id="3b617-116">You can also send logging information to additional servers, including web servers you use exclusively for logging.</span></span> <span data-ttu-id="3b617-117">Para ello, use el elemento **LOGURL** y especifique una dirección URL válida para el atributo **href** .</span><span class="sxs-lookup"><span data-stu-id="3b617-117">To do this, use the **LOGURL** element, specifying a valid URL for the **HREF** attribute.</span></span> <span data-ttu-id="3b617-118">Puede incluir elementos **LOGURL** como elementos secundarios del elemento **ASX** y como elementos secundarios de los elementos de **entrada** individuales.</span><span class="sxs-lookup"><span data-stu-id="3b617-118">You can include **LOGURL** elements as children of the **ASX** element and as children of individual **ENTRY** elements.</span></span> <span data-ttu-id="3b617-119">Cuando se abre la lista de reproducción por primera vez, la información de registro se envía al servidor de origen y a cada dirección URL especificada en **LOGURL** elementos secundarios del elemento **ASX** .</span><span class="sxs-lookup"><span data-stu-id="3b617-119">When the playlist is first opened, logging information is sent to the origin server and to each URL specified in **LOGURL** children of the **ASX** element.</span></span> <span data-ttu-id="3b617-120">A continuación, a medida que se alcanza cada entrada, la información de registro específica de esa entrada se envía a cada dirección URL especificada en **LOGURL** elementos secundarios del elemento de **entrada** .</span><span class="sxs-lookup"><span data-stu-id="3b617-120">Then, as each entry is reached, logging information specific to that entry is sent to each URL specified in **LOGURL** children of the **ENTRY** element.</span></span>

<span data-ttu-id="3b617-121">El SDK de Windows Media Format admite el elemento **LOGURL** a través de la interfaz **IWMSReaderNetworkConfig** y los métodos siguientes:</span><span class="sxs-lookup"><span data-stu-id="3b617-121">The Windows Media Format SDK supports the **LOGURL** element through the **IWMSReaderNetworkConfig** interface and the following methods:</span></span>


```XML
HRESULT AddLoggingUrl(LPCWSTR pwszUrl);
HRESULT GetLoggingUrl(DWORD dwIndex, LPCWSTR pwszUrl, DWORD *pcchUrl);
HRESULT GetLoggingUrlCount(DWORD *pdwUrlCount);
HRESULT ResetLoggingUrlList();

```



<span data-ttu-id="3b617-122">Además de la información que se registra automáticamente, una lista de reproducción de metarchivo puede registrar información personalizada mediante el uso del elemento **param** .</span><span class="sxs-lookup"><span data-stu-id="3b617-122">In addition to the information that is automatically logged, a metafile playlist can log custom information through the use of the **PARAM** element.</span></span> <span data-ttu-id="3b617-123">Para usar el elemento **param** de esta manera, establezca el atributo **Name** en "log:" seguido de un nombre de campo de registro y un espacio de nombres XML opcional separado del nombre del campo por otro signo de dos puntos (":").</span><span class="sxs-lookup"><span data-stu-id="3b617-123">To use the **PARAM** element in this way, set the **NAME** attribute to "log:" followed by a log field name and an optional XML namespace separated from the field name by another colon (":").</span></span> <span data-ttu-id="3b617-124">Todo lo que va después del segundo signo de dos puntos se trata como un espacio de nombres, por lo que el nombre del campo no debe contener un signo de dos puntos.</span><span class="sxs-lookup"><span data-stu-id="3b617-124">Everything after the second colon is treated as a namespace, so the field name should not contain a colon.</span></span>

<span data-ttu-id="3b617-125">El campo de registro especificado en el atributo **Name** se establece en el valor del atributo **Value** .</span><span class="sxs-lookup"><span data-stu-id="3b617-125">The log field specified in the **NAME** attribute is set to the value of the **VALUE** attribute.</span></span> <span data-ttu-id="3b617-126">Si el registro todavía no contiene un campo con el nombre especificado, se agregará.</span><span class="sxs-lookup"><span data-stu-id="3b617-126">If the log does not already contain a field with the specified name, it will be added.</span></span>

<span data-ttu-id="3b617-127">**Código de ejemplo**</span><span class="sxs-lookup"><span data-stu-id="3b617-127">**Example Code**</span></span>


```XML

    <ASX version="3.0">
      <LOGURL href="https://www.proseware.com/log.asp?SomeArg=SomeVal" />
      <ENTRY>
        <REF href="mms://ucast.proseware.com/Media1.wma" />
        <LOGURL href="https://www.proseware.com/cgi-bin/logging.pl?SomeArg=SomeVal" />
        <LOGURL href="https://www.proseware.com/WMLogging.dll?SomeArg=SomeVal" />
        <PARAM name="log:cs-media-role" value="Advertisement"/>
        <PARAM name="log:cs-media-name:namespace" value="Music"/>
        <REF href=rtsp://ucast.proseware.com/Media1.wma"/>
      </ENTRY>
      <ENTRY>
        <REF href="mms://ucast.proseware.com/Media2.wma"/>
      </ENTRY>
    </ASX>
    

```



## <a name="related-topics"></a><span data-ttu-id="3b617-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3b617-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b617-129">**Listas de reproducción de metarchivos**</span><span class="sxs-lookup"><span data-stu-id="3b617-129">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="3b617-130">**Referencia de elementos de metarchivo de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="3b617-130">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> </dl>

 

 




