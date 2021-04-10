---
description: Registro de cliente
ms.assetid: f91b48ae-3989-4c1d-929c-8ab28d7c8177
title: Registro de clientes (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb3cb03c8026e91acd567358e7004211b7fdde4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275144"
---
# <a name="client-logging-microsoft-media-foundation"></a><span data-ttu-id="2fd3b-103">Registro de clientes (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="2fd3b-103">Client Logging (Microsoft Media Foundation)</span></span>

<span data-ttu-id="2fd3b-104">El origen de red es compatible con el registro de cliente, que proporciona una manera para que el servidor multimedia realice un seguimiento de la actividad de los clientes que se conectan a él.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-104">The network source supports client logging, which provides a way for the media server to track the activity of the clients that connect to it.</span></span> <span data-ttu-id="2fd3b-105">Los registros de cliente permiten que un servidor registre las estadísticas de conexión, representación y transmisión por secuencias.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-105">Client logs enable a server to record connection, rendering, and streaming statistics.</span></span> <span data-ttu-id="2fd3b-106">Los proveedores de contenido pueden utilizar estos registros en varios escenarios, como, para realizar un seguimiento del uso del servidor multimedia y generar la facturación, o para proporcionar contenido de calidad adecuada en función de la velocidad de la red del cliente.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-106">These logs can be used by content providers in various scenarios, such as, to trace media server usage and generate billing, or to deliver suitable-quality content depending on the speed of the client's network.</span></span>

<span data-ttu-id="2fd3b-107">Un archivo de registro contiene varias entradas de eventos de cliente.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-107">A log file contains several client event entries.</span></span> <span data-ttu-id="2fd3b-108">Cada entrada de registro contiene varios campos delimitados por espacios.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-108">Each log entry contains a number of space-delimited fields.</span></span> <span data-ttu-id="2fd3b-109">Hay dos tipos de registros de cliente: *representación* (reproducción) y *transmisión por secuencias* (recepción).</span><span class="sxs-lookup"><span data-stu-id="2fd3b-109">There are two types of client logs: *rendering* (playing) and *streaming* (receiving).</span></span> <span data-ttu-id="2fd3b-110">Dado que el contenido se puede reproducir y transmitir simultáneamente, el cliente puede enviar una combinación de ambos tipos de datos de registro.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-110">Because content can be played and streamed simultaneously, the client can send a combination of both types of log data.</span></span> <span data-ttu-id="2fd3b-111">En algunos casos, pueden existir dos entradas de registro para la misma sesión.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-111">In certain cases, two log entries can exist for the same session.</span></span> <span data-ttu-id="2fd3b-112">Por ejemplo, cuando la memoria caché rápida está habilitada, el cliente puede terminar de recibir el contenido transmitido antes de que termine de presentarlo.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-112">For example, when Fast Cache is enabled, the client can finish receiving the streamed content before it finishes rendering it.</span></span> <span data-ttu-id="2fd3b-113">En ese caso, los datos del registro de streaming se enviarían antes que los datos de registro de representación.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-113">In that case, the streaming log data would be sent before the rendering log data.</span></span>

<span data-ttu-id="2fd3b-114">El cliente envía los datos de registro de representación al servidor cuando el cliente cambia de cualquier estado de reproducción (reproducción, avance rápido o rebobinado) a un estado de no reproducción (detención, pausa, finalización del flujo y comienzo de la secuencia).</span><span class="sxs-lookup"><span data-stu-id="2fd3b-114">The client sends rendering log data to the server when the client changes from any playing state (play, fast-forward, or rewind) to a non-playing state (stop, pause, end of stream, and beginning of stream).</span></span> <span data-ttu-id="2fd3b-115">Cuando se envían datos para un registro de representación, se establece una conexión directamente con el servidor multimedia o un servidor proxy configurado.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-115">When data for a rendering log is submitted, a connection is made directly to the media server or a configured proxy server.</span></span>

<span data-ttu-id="2fd3b-116">Si el contenido se almacena en un archivo de caché local temporal en el equipo que ejecuta el cliente de, el cliente puede leer un archivo de su caché local y enviar los datos de registro de representación para indicar que ha reproducido el contenido.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-116">If the content is stored in a temporary local cache file on the computer that is running the client, the client can read a file from its local cache and submit the rendering log data to indicate that it has played the content.</span></span> <span data-ttu-id="2fd3b-117">En este caso, el cliente Lee un archivo de la memoria caché local, la entrada del registro de representación no contiene ninguna estadística de red y el protocolo se establece en caché.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-117">In this case, the client reads a file from its local cache, the rendering log entry does not contain any network statistics, and the protocol is set to Cache.</span></span>

<span data-ttu-id="2fd3b-118">El cliente envía datos de registro de streaming al servidor para indicar cómo el cliente recibió el contenido, pero no cómo se representó.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-118">The client sends streaming log data to the server to indicate how the client received the content, but not how it was rendered.</span></span> <span data-ttu-id="2fd3b-119">El cliente puede enviar el registro de streaming durante el tiempo antes de que el cliente termine de representar el contenido.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-119">The client can send the streaming log long before the client finishes rendering the content.</span></span>

<span data-ttu-id="2fd3b-120">En este tema no se proporciona información sobre todos los campos de registro.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-120">This topic does not provide information about all the log fields.</span></span> <span data-ttu-id="2fd3b-121">Para obtener una referencia completa, vea [estructura de datos del registro de Windows Media](/openspecs/windows_protocols/ms-wmlog/42c620eb-0d77-4350-b070-bcd1e182fe84).</span><span class="sxs-lookup"><span data-stu-id="2fd3b-121">For a complete reference, see [Windows Media Log Data Structure](/openspecs/windows_protocols/ms-wmlog/42c620eb-0d77-4350-b070-bcd1e182fe84).</span></span>

## <a name="configuring-log-fields"></a><span data-ttu-id="2fd3b-122">Configuración de campos de registro</span><span class="sxs-lookup"><span data-stu-id="2fd3b-122">Configuring Log Fields</span></span>

<span data-ttu-id="2fd3b-123">Media Foundation permite al cliente configurar el origen de red mediante propiedades.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-123">Media Foundation enables the client to configure the network source by using properties.</span></span> <span data-ttu-id="2fd3b-124">La aplicación debe establecer las propiedades adecuadas en un almacén de propiedades y pasarlo a uno de los métodos de resolución de origen.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-124">The application must set the appropriate properties in a property store and pass it to one of the source resolver methods.</span></span> <span data-ttu-id="2fd3b-125">La resolución de origen crea el origen de red tal y como se solicitó y abre una conexión con el servidor.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-125">The source resolver creates the network source as requested and opens a connection with the server.</span></span> <span data-ttu-id="2fd3b-126">Si la conexión se realiza correctamente, el cliente envía información sobre sí misma.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-126">If the connection is successful, the client sends information about itself.</span></span>

<span data-ttu-id="2fd3b-127">En la tabla siguiente se describen los campos de registro y las propiedades correspondientes que una aplicación puede establecer a través de la resolución de origen.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-127">The following table describes the log fields and the corresponding properties that an application can set through the source resolver.</span></span> <span data-ttu-id="2fd3b-128">Esta información no cambia durante la sesión.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-128">This information does not change during the session.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2fd3b-129">Campo de registro</span><span class="sxs-lookup"><span data-stu-id="2fd3b-129">Logging field</span></span></th>
<th><span data-ttu-id="2fd3b-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="2fd3b-130">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2fd3b-131">c-playerid</span><span class="sxs-lookup"><span data-stu-id="2fd3b-131">c-playerid</span></span></td>
<td><span data-ttu-id="2fd3b-132">Identificación única del reproductor.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-132">Unique identification of the player.</span></span> <span data-ttu-id="2fd3b-133">Esta información se envía al principio de la conexión.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-133">This information is sent at the beginning of the connection.</span></span> <span data-ttu-id="2fd3b-134">Normalmente, se trata de un GUID del cliente de.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-134">Typically, this is a GUID of the client.</span></span> <span data-ttu-id="2fd3b-135">El cliente puede enviar esta información al servidor en la <a href="mfnetsource-playerid-property.md"><strong>MFNETSOURCE_PLAYERID</strong></a> propiedad.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-135">The client can send this information to the server in the <a href="mfnetsource-playerid-property.md"><strong>MFNETSOURCE_PLAYERID</strong></a> property.</span></span><br/> <span data-ttu-id="2fd3b-136">El cliente envía esta información al servidor al principio de la conexión.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-136">The client sends this information to the server at the beginning of the connection.</span></span><br/> <span data-ttu-id="2fd3b-137">Valor de ejemplo: &quot; {c579d042-CECC-11D1-BB31-00a0c9603954}&quot;</span><span class="sxs-lookup"><span data-stu-id="2fd3b-137">Sample value: &quot;{c579d042-cecc-11d1-bb31-00a0c9603954}&quot;</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2fd3b-138">c-playerversion</span><span class="sxs-lookup"><span data-stu-id="2fd3b-138">c-playerversion</span></span></td>
<td><span data-ttu-id="2fd3b-139">Número de versión del reproductor que se envía al principio de la conexión.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-139">The version number of the player that is sent at the beginning of the connection.</span></span> <span data-ttu-id="2fd3b-140">El cliente puede enviar esta información al servidor en la <a href="mfnetsource-playerversion-property.md"><strong>MFNETSOURCE_PLAYERVERSION</strong></a> propiedad.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-140">The client can send this information to the server in the <a href="mfnetsource-playerversion-property.md"><strong>MFNETSOURCE_PLAYERVERSION</strong></a> property.</span></span><br/> <span data-ttu-id="2fd3b-141">El cliente envía esta información al servidor al principio de la conexión.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-141">The client sends this information to the server at the beginning of the connection.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2fd3b-142">CS (User-Agent)</span><span class="sxs-lookup"><span data-stu-id="2fd3b-142">cs(User-Agent)</span></span></td>
<td><span data-ttu-id="2fd3b-143">Tipo de explorador que se usa si el reproductor estaba incrustado en un explorador.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-143">Browser type used if the player was embedded in a browser.</span></span> <span data-ttu-id="2fd3b-144">El cliente puede establecer este valor en la propiedad <a href="mfnetsource-browseruseragent-property.md"><strong>MFNETSOURCE_BROWSERUSERAGENT</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="2fd3b-144">This value can be set by the client in the <a href="mfnetsource-browseruseragent-property.md"><strong>MFNETSOURCE_BROWSERUSERAGENT</strong></a> property.</span></span><br/> <span data-ttu-id="2fd3b-145">Si no se incrustó el reproductor, este campo hace referencia al agente de usuario del cliente que generó el registro.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-145">If the player was not embedded, this field refers to the user agent of the client that generated the log.</span></span> <span data-ttu-id="2fd3b-146">En este caso, el cliente debe establecer la propiedad <a href="mfnetsource-playeruseragent-property.md"><strong>MFNETSOURCE_PLAYERUSERAGENT</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="2fd3b-146">In this case, the client must set the <a href="mfnetsource-playeruseragent-property.md"><strong>MFNETSOURCE_PLAYERUSERAGENT</strong></a> property.</span></span><br/> <span data-ttu-id="2fd3b-147">El cliente envía esta información al servidor al principio de la conexión.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-147">The client sends this information to the server at the beginning of the connection.</span></span><br/> <span data-ttu-id="2fd3b-148">Valor de ejemplo: &quot; Mozilla/4.0 _ (compatible; _MSIE_4.01; _Windows_98)&quot;</span><span class="sxs-lookup"><span data-stu-id="2fd3b-148">Sample value: &quot;Mozilla/4.0_(compatible;_MSIE_4.01;_Windows_98)&quot;</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2fd3b-149">CS (referer)</span><span class="sxs-lookup"><span data-stu-id="2fd3b-149">cs(Referer)</span></span></td>
<td><span data-ttu-id="2fd3b-150">Dirección URL de la página web en la que se incrustó el reproductor (si se incrustó).</span><span class="sxs-lookup"><span data-stu-id="2fd3b-150">URL of the webpage in which the player was embedded (if it was embedded).</span></span> <span data-ttu-id="2fd3b-151">El cliente puede enviar esta información al servidor en la <a href="mfnetsource-browserwebpage-property.md"><strong>MFNETSOURCE_BROWSERWEBPAGE</strong></a> propiedad.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-151">The client can send this information to the server in the <a href="mfnetsource-browserwebpage-property.md"><strong>MFNETSOURCE_BROWSERWEBPAGE</strong></a> property.</span></span><br/> <span data-ttu-id="2fd3b-152">El cliente envía esta información al servidor al final de la conexión.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-152">The client sends this information to the server at the end of the connection.</span></span><br/> <span data-ttu-id="2fd3b-153">Valor de ejemplo: &quot; https://www.example.microsoft.com&quot ;</span><span class="sxs-lookup"><span data-stu-id="2fd3b-153">Sample value: &quot;https://www.example.microsoft.com&quot;</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2fd3b-154">c-hostexe</span><span class="sxs-lookup"><span data-stu-id="2fd3b-154">c-hostexe</span></span></td>
<td><span data-ttu-id="2fd3b-155">Para las entradas de registro del reproductor, el programa host (. exe) que se ejecutó.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-155">For player log entries, the host program (.exe) that was run.</span></span> <span data-ttu-id="2fd3b-156">Por ejemplo, una página web en un explorador, un applet de Microsoft Visual Basic o un reproductor independiente.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-156">For example, a webpage in a browser, a Microsoft Visual Basic applet, or a stand-alone player.</span></span> <span data-ttu-id="2fd3b-157">El cliente puede enviar esta información al servidor en la <a href="mfnetsource-hostexe-property.md"><strong>MFNETSOURCE_HOSTEXE</strong></a> propiedad.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-157">The client can send this information to the server in the <a href="mfnetsource-hostexe-property.md"><strong>MFNETSOURCE_HOSTEXE</strong></a> property.</span></span><br/> <span data-ttu-id="2fd3b-158">El cliente envía esta información al servidor al final de la conexión.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-158">The client sends this information to the server at the end of the connection.</span></span><br/> <span data-ttu-id="2fd3b-159">Valores de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="2fd3b-159">Sample values:</span></span><br/>
<ul>
<li><span data-ttu-id="2fd3b-160">&quot;iexplore.exe&quot;</span><span class="sxs-lookup"><span data-stu-id="2fd3b-160">&quot;iexplore.exe&quot;</span></span></li>
<li><span data-ttu-id="2fd3b-161">&quot;myplayer.exe&quot;</span><span class="sxs-lookup"><span data-stu-id="2fd3b-161">&quot;myplayer.exe&quot;</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2fd3b-162">c-hostexever</span><span class="sxs-lookup"><span data-stu-id="2fd3b-162">c-hostexever</span></span></td>
<td><span data-ttu-id="2fd3b-163">Número de versión del programa host (. exe).</span><span class="sxs-lookup"><span data-stu-id="2fd3b-163">Host program (.exe) version number.</span></span> <span data-ttu-id="2fd3b-164">El cliente puede enviar esta información al servidor en la <a href="mfnetsource-hostversion-property.md"><strong>MFNETSOURCE_HOSTVERSION</strong></a> propiedad.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-164">The client can send this information to the server in the <a href="mfnetsource-hostversion-property.md"><strong>MFNETSOURCE_HOSTVERSION</strong></a> property.</span></span><br/> <span data-ttu-id="2fd3b-165">El cliente envía esta información al servidor al final de la conexión.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-165">The client sends this information to the server at the end of the connection.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="2fd3b-166">En el ejemplo de código siguiente se muestra cómo una aplicación cliente configura el origen de red.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-166">The following code example shows how a client application configures the network source.</span></span> <span data-ttu-id="2fd3b-167">En este ejemplo se establece el campo de registro "c-hostexe".</span><span class="sxs-lookup"><span data-stu-id="2fd3b-167">This example sets the "c-hostexe" log field.</span></span>


```C++
// Creates a media source from a URL.
//
// This example demonstrates how to set the MFNETSOURCE_HOSTEXE
// configuration property on the network source.

HRESULT CreateMediaSourceWithLogParams(
    PCWSTR pszURL, 
    IMFMediaSource **ppSource
    )
{
    IPropertyStore *pConfig = NULL;

    // Configure the property store.
    HRESULT hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&pConfig));

    if (SUCCEEDED(hr))
    {
        PROPERTYKEY key;
        key.fmtid =  MFNETSOURCE_HOSTEXE;
        key.pid = 0;

        PROPVARIANT var;
        var.vt = VT_LPWSTR;
        var.pwszVal = L"MyPlayer.exe";

        hr = pConfig->SetValue(key, var);
    }

    // Create the source media source.
    if (SUCCEEDED(hr))
    {
        hr = CreateMediaSource(pszURL, pConfig, ppSource);
    }

    SafeRelease(&pConfig);
    return hr;
}
```



## <a name="retrieving-network-statistics"></a><span data-ttu-id="2fd3b-168">Recuperando estadísticas de red</span><span class="sxs-lookup"><span data-stu-id="2fd3b-168">Retrieving Network Statistics</span></span>

<span data-ttu-id="2fd3b-169">Cuando la aplicación llama a uno de los métodos de resolución de origen, crea el origen de red, establece las propiedades especificadas en el almacén de propiedades y abre una sesión con el servidor multimedia.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-169">When the application calls one of the source resolver methods, it creates the network source, sets the properties specified in the property store, and opens a session with the media server.</span></span> <span data-ttu-id="2fd3b-170">Además de la información configurable descrita en la sección anterior, los datos adicionales se transfieren entre el servidor y el cliente al principio de la sesión, durante el streaming y cuando se cierra la sesión.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-170">In addition to the configurable information described in the previous section, additional data is transferred between the server and the client at the beginning of the session, during streaming, and when the session is closed.</span></span>

<span data-ttu-id="2fd3b-171">La aplicación puede recuperar estadísticas de red mediante el identificador del servicio **MFNETSOURCE \_ Statistics \_ Service** .</span><span class="sxs-lookup"><span data-stu-id="2fd3b-171">The application can retrieve network statistics by using the **MFNETSOURCE\_STATISTICS\_SERVICE** service identifier.</span></span> <span data-ttu-id="2fd3b-172">Para usar este servicio, la aplicación puede llamar a la función [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) para obtener el almacén de propiedades que contiene las estadísticas de red en la propiedad [**MFNETSOURCE \_ Statistics**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids) .</span><span class="sxs-lookup"><span data-stu-id="2fd3b-172">To use this service, the application can call the [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) function to get the property store that contains network statistics in the [**MFNETSOURCE\_STATISTICS**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids) property.</span></span> <span data-ttu-id="2fd3b-173">Los valores específicos se pueden recuperar proporcionando el identificador correspondiente definido en la enumeración de **\_ \_ identificadores de estadísticas de MFNETSOURCE** .</span><span class="sxs-lookup"><span data-stu-id="2fd3b-173">Specific values can be retrieved by providing the corresponding identifier defined in the **MFNETSOURCE\_STATISTICS\_IDS** enumeration.</span></span>

<span data-ttu-id="2fd3b-174">En el ejemplo de código siguiente se muestra cómo utilizar el servicio para obtener el número de paquetes recibidos por el cliente.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-174">The following code example shows how to use the service to get the number of packets received by the client.</span></span>


```C++
HRESULT GetPacketsReceived(IMFMediaSession *pSession, DWORD *pcPackets)
{
    IPropertyStore *pProp = NULL;
    PROPVARIANT var;

    // Get the property store from the media session.
    HRESULT hr = MFGetService(
        pSession, 
        MFNETSOURCE_STATISTICS_SERVICE, 
        IID_PPV_ARGS(&pProp)
        );

    // Get the number of packets received by the client.

    if (SUCCEEDED(hr))
    {
        PROPERTYKEY key;
        key.fmtid = MFNETSOURCE_STATISTICS;
        key.pid = MFNETSOURCE_RECVPACKETS_ID;

        hr = pProp->GetValue(key, &var);
    }

    if (SUCCEEDED(hr))
    {
        *pcPackets = var.lVal;
    }

    PropVariantClear(&var);
    SafeRelease(&pProp);
    return hr;
}
```



<span data-ttu-id="2fd3b-175">En la lista siguiente se describen algunos de los identificadores de estadísticas de red definidos en los [**\_ \_ identificadores de estadísticas de MFNETSOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids).</span><span class="sxs-lookup"><span data-stu-id="2fd3b-175">The following list describes some of the network statistics identifiers defined in [**MFNETSOURCE\_STATISTICS\_IDS**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids).</span></span>



| <span data-ttu-id="2fd3b-176">Identificador de estadísticas de red</span><span class="sxs-lookup"><span data-stu-id="2fd3b-176">Network statistics identifier</span></span>              | <span data-ttu-id="2fd3b-177">Descripción</span><span class="sxs-lookup"><span data-stu-id="2fd3b-177">Description</span></span>                                                                                                                                                                                                                |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fd3b-178">**MFNETSOURCE \_ \_ ID AVGBANDWIDTHBPS**</span><span class="sxs-lookup"><span data-stu-id="2fd3b-178">**MFNETSOURCE\_AVGBANDWIDTHBPS\_ID**</span></span>       | <span data-ttu-id="2fd3b-179">Promedio de ancho de banda (en bits por segundo) en el que el cliente se conectó al servidor.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-179">Average bandwidth (in bits per second) at which the client was connected to the server.</span></span> <span data-ttu-id="2fd3b-180">El valor se calcula a lo largo de toda la duración de la conexión.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-180">The value is calculated across the entire duration of the connection.</span></span>                                                              |
| <span data-ttu-id="2fd3b-181">**MFNETSOURCE \_ \_ ID BUFFERINGCOUNT**</span><span class="sxs-lookup"><span data-stu-id="2fd3b-181">**MFNETSOURCE\_BUFFERINGCOUNT\_ID**</span></span>        | <span data-ttu-id="2fd3b-182">Número de veces que el cliente ha almacenado en búfer mientras se reproduce la secuencia.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-182">Number of times the client buffered while playing the stream.</span></span>                                                                                                                                                              |
| <span data-ttu-id="2fd3b-183">**MFNETSOURCE \_ \_ ID BYTESRECEIVED**</span><span class="sxs-lookup"><span data-stu-id="2fd3b-183">**MFNETSOURCE\_BYTESRECEIVED\_ID**</span></span>         | <span data-ttu-id="2fd3b-184">Número de bytes recibidos por el cliente desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-184">Number of bytes received by the client from the server.</span></span> <span data-ttu-id="2fd3b-185">El valor no incluye ninguna sobrecarga agregada por la pila de red.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-185">The value does not include any overhead that is added by the network stack.</span></span> <span data-ttu-id="2fd3b-186">El mismo contenido transmitido mediante distintos protocolos puede dar lugar a valores diferentes.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-186">The same content streamed by using different protocols can result in different values.</span></span> |
| <span data-ttu-id="2fd3b-187">**MFNETSOURCE \_ \_ ID LINKBANDWIDTH**</span><span class="sxs-lookup"><span data-stu-id="2fd3b-187">**MFNETSOURCE\_LINKBANDWIDTH\_ID**</span></span>         | <span data-ttu-id="2fd3b-188">Ancho de banda máximo disponible del cliente en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-188">Maximum available bandwidth of the client in bits per second.</span></span>                                                                                                                                                              |
| <span data-ttu-id="2fd3b-189">**MFNETSOURCE \_ \_ ID LOSTPACKETS**</span><span class="sxs-lookup"><span data-stu-id="2fd3b-189">**MFNETSOURCE\_LOSTPACKETS\_ID**</span></span>           | <span data-ttu-id="2fd3b-190">Número de paquetes enviados por el servidor, que se han perdido durante la transmisión y nunca lo reproduce el cliente.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-190">Number of packets sent by the server but lost during transmission, and never played by the client.</span></span> <span data-ttu-id="2fd3b-191">El valor no incluye los paquetes TCP o UDP.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-191">The value does not include TCP or UDP packets.</span></span>                                                                          |
| <span data-ttu-id="2fd3b-192">**MFNETSOURCE \_ \_ ID RECVPACKETS**</span><span class="sxs-lookup"><span data-stu-id="2fd3b-192">**MFNETSOURCE\_RECVPACKETS\_ID**</span></span>           | <span data-ttu-id="2fd3b-193">Número de paquetes recibidos del servidor. el valor no incluye los paquetes TCP o UDP.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-193">Number of packets received from the server The value does not include TCP or UDP packets.</span></span>                                                                                                                                  |
| <span data-ttu-id="2fd3b-194">**MFNETSOURCE \_ \_ ID RECOVEREDBYECCPACKETS**</span><span class="sxs-lookup"><span data-stu-id="2fd3b-194">**MFNETSOURCE\_RECOVEREDBYECCPACKETS\_ID**</span></span> | <span data-ttu-id="2fd3b-195">Paquetes perdidos en la red que se reparó y se recuperaron en el nivel de cliente.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-195">Packets lost in the network that were repaired and recovered at the client layer.</span></span> <span data-ttu-id="2fd3b-196">Este valor no incluye los paquetes TCP o UDP.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-196">This value does not include TCP or UDP packets.</span></span>                                                                                          |
| <span data-ttu-id="2fd3b-197">**MFNETSOURCE \_ \_ ID RESENDSREQUESTED**</span><span class="sxs-lookup"><span data-stu-id="2fd3b-197">**MFNETSOURCE\_RESENDSREQUESTED\_ID**</span></span>      | <span data-ttu-id="2fd3b-198">El número de solicitudes realizadas por el cliente para recibir nuevos paquetes.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-198">The number of requests made by the client to receive new packets.</span></span> <span data-ttu-id="2fd3b-199">Este valor no incluye los paquetes TCP o UDP.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-199">This value does not include TCP or UDP packets.</span></span>                                                                                                          |
| <span data-ttu-id="2fd3b-200">**MFNETSOURCE \_ \_ ID RECOVEREDPACKETS**</span><span class="sxs-lookup"><span data-stu-id="2fd3b-200">**MFNETSOURCE\_RECOVEREDPACKETS\_ID**</span></span>      | <span data-ttu-id="2fd3b-201">Número de paquetes recuperados porque se reenviaron a través de UDP.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-201">Number of packets recovered because they were resent through UDP.</span></span> <span data-ttu-id="2fd3b-202">Este valor no incluye los paquetes TCP o UDP.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-202">This value does not include TCP or UDP packets.</span></span> <span data-ttu-id="2fd3b-203">Este campo contiene un cero a menos que el cliente use el reenvío de UDP.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-203">This field contains a zero unless the client is using UDP resend.</span></span>                                        |
| <span data-ttu-id="2fd3b-204">**MFNETSOURCE \_ \_ ID BUFFERPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="2fd3b-204">**MFNETSOURCE\_BUFFERPROGRESS\_ID**</span></span>        | <span data-ttu-id="2fd3b-205">Porcentaje del búfer de emisión rellenado durante el almacenamiento en búfer.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-205">The percentage of the playout buffer filled during buffering.</span></span>                                                                                                                                                              |
| <span data-ttu-id="2fd3b-206">**\_identificador de protocolo MFNETSOURCE \_**</span><span class="sxs-lookup"><span data-stu-id="2fd3b-206">**MFNETSOURCE\_PROTOCOL\_ID**</span></span>              | <span data-ttu-id="2fd3b-207">Protocolo utilizado para tener acceso a la secuencia.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-207">Protocol used to access the stream.</span></span> <span data-ttu-id="2fd3b-208">Esto puede diferir del protocolo solicitado por el cliente.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-208">This may differ from the protocol requested by the client.</span></span>                                                                                                                             |
| <span data-ttu-id="2fd3b-209">**\_identificador de transporte de MFNETSOURCE \_**</span><span class="sxs-lookup"><span data-stu-id="2fd3b-209">**MFNETSOURCE\_TRANSPORT\_ID**</span></span>             | <span data-ttu-id="2fd3b-210">Protocolo de transporte que se usa para proporcionar la secuencia.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-210">Transport protocol used to deliver the stream.</span></span> <span data-ttu-id="2fd3b-211">Debe ser UDP o TCP.</span><span class="sxs-lookup"><span data-stu-id="2fd3b-211">This must be either UDP or TCP.</span></span>                                                                                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="2fd3b-212">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2fd3b-212">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2fd3b-213">Características de origen de red</span><span class="sxs-lookup"><span data-stu-id="2fd3b-213">Network Source Features</span></span>](network-source-features.md)
</dt> <dt>

[<span data-ttu-id="2fd3b-214">Funciones de red en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2fd3b-214">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

