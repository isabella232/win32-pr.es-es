---
description: Obtenga información sobre el registro de cliente para Microsoft Media Foundation. El registro proporciona una manera de que el servidor multimedia realice un seguimiento de la actividad de los clientes que se conectan a él.
ms.assetid: f91b48ae-3989-4c1d-929c-8ab28d7c8177
title: Registro de cliente (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d994531ff16466054ca0645a35082a4845e4aa4
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409938"
---
# <a name="client-logging-microsoft-media-foundation"></a><span data-ttu-id="9b03d-104">Registro de cliente (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="9b03d-104">Client Logging (Microsoft Media Foundation)</span></span>

<span data-ttu-id="9b03d-105">El origen de red admite el registro de cliente, que proporciona una manera de que el servidor multimedia realice un seguimiento de la actividad de los clientes que se conectan a él.</span><span class="sxs-lookup"><span data-stu-id="9b03d-105">The network source supports client logging, which provides a way for the media server to track the activity of the clients that connect to it.</span></span> <span data-ttu-id="9b03d-106">Los registros de cliente permiten a un servidor registrar estadísticas de conexión, representación y streaming.</span><span class="sxs-lookup"><span data-stu-id="9b03d-106">Client logs enable a server to record connection, rendering, and streaming statistics.</span></span> <span data-ttu-id="9b03d-107">Los proveedores de contenido pueden usar estos registros en varios escenarios, como para realizar un seguimiento del uso del servidor multimedia y generar facturación, o para entregar contenido de calidad adecuada según la velocidad de la red del cliente.</span><span class="sxs-lookup"><span data-stu-id="9b03d-107">These logs can be used by content providers in various scenarios, such as, to trace media server usage and generate billing, or to deliver suitable-quality content depending on the speed of the client's network.</span></span>

<span data-ttu-id="9b03d-108">Un archivo de registro contiene varias entradas de eventos de cliente.</span><span class="sxs-lookup"><span data-stu-id="9b03d-108">A log file contains several client event entries.</span></span> <span data-ttu-id="9b03d-109">Cada entrada de registro contiene una serie de campos delimitados por espacios.</span><span class="sxs-lookup"><span data-stu-id="9b03d-109">Each log entry contains a number of space-delimited fields.</span></span> <span data-ttu-id="9b03d-110">Hay dos tipos de registros de cliente: *representación* (reproducción) y *streaming* (recepción).</span><span class="sxs-lookup"><span data-stu-id="9b03d-110">There are two types of client logs: *rendering* (playing) and *streaming* (receiving).</span></span> <span data-ttu-id="9b03d-111">Dado que el contenido se puede reproducir y transmitir simultáneamente, el cliente puede enviar una combinación de ambos tipos de datos de registro.</span><span class="sxs-lookup"><span data-stu-id="9b03d-111">Because content can be played and streamed simultaneously, the client can send a combination of both types of log data.</span></span> <span data-ttu-id="9b03d-112">En algunos casos, pueden existir dos entradas de registro para la misma sesión.</span><span class="sxs-lookup"><span data-stu-id="9b03d-112">In certain cases, two log entries can exist for the same session.</span></span> <span data-ttu-id="9b03d-113">Por ejemplo, cuando Fast Cache está habilitado, el cliente puede terminar de recibir el contenido transmitido antes de terminar de representarlo.</span><span class="sxs-lookup"><span data-stu-id="9b03d-113">For example, when Fast Cache is enabled, the client can finish receiving the streamed content before it finishes rendering it.</span></span> <span data-ttu-id="9b03d-114">En ese caso, los datos de registro de streaming se enviarían antes que los datos de registro de representación.</span><span class="sxs-lookup"><span data-stu-id="9b03d-114">In that case, the streaming log data would be sent before the rendering log data.</span></span>

<span data-ttu-id="9b03d-115">El cliente envía datos de registro de representación al servidor cuando el cliente cambia de cualquier estado de reproducción (reproducción, avance rápido o rebobinado) a un estado de no reproducción (detenerse, pausar, finalizar la secuencia e iniciar la secuencia).</span><span class="sxs-lookup"><span data-stu-id="9b03d-115">The client sends rendering log data to the server when the client changes from any playing state (play, fast-forward, or rewind) to a non-playing state (stop, pause, end of stream, and beginning of stream).</span></span> <span data-ttu-id="9b03d-116">Cuando se envían datos para un registro de representación, se realiza una conexión directamente al servidor multimedia o a un servidor proxy configurado.</span><span class="sxs-lookup"><span data-stu-id="9b03d-116">When data for a rendering log is submitted, a connection is made directly to the media server or a configured proxy server.</span></span>

<span data-ttu-id="9b03d-117">Si el contenido se almacena en un archivo de caché local temporal en el equipo que ejecuta el cliente, el cliente puede leer un archivo de su caché local y enviar los datos de registro de representación para indicar que ha reproducdo el contenido.</span><span class="sxs-lookup"><span data-stu-id="9b03d-117">If the content is stored in a temporary local cache file on the computer that is running the client, the client can read a file from its local cache and submit the rendering log data to indicate that it has played the content.</span></span> <span data-ttu-id="9b03d-118">En este caso, el cliente lee un archivo de su caché local, la entrada del registro de representación no contiene estadísticas de red y el protocolo se establece en Caché.</span><span class="sxs-lookup"><span data-stu-id="9b03d-118">In this case, the client reads a file from its local cache, the rendering log entry does not contain any network statistics, and the protocol is set to Cache.</span></span>

<span data-ttu-id="9b03d-119">El cliente envía datos de registro de streaming al servidor para indicar cómo el cliente recibió el contenido, pero no cómo se representó.</span><span class="sxs-lookup"><span data-stu-id="9b03d-119">The client sends streaming log data to the server to indicate how the client received the content, but not how it was rendered.</span></span> <span data-ttu-id="9b03d-120">El cliente puede enviar el registro de streaming mucho antes de que el cliente termine de representar el contenido.</span><span class="sxs-lookup"><span data-stu-id="9b03d-120">The client can send the streaming log long before the client finishes rendering the content.</span></span>

<span data-ttu-id="9b03d-121">En este tema no se proporciona información sobre todos los campos de registro.</span><span class="sxs-lookup"><span data-stu-id="9b03d-121">This topic does not provide information about all the log fields.</span></span> <span data-ttu-id="9b03d-122">Para obtener una referencia completa, vea [Estructura de datos de registro de Windows Media](/openspecs/windows_protocols/ms-wmlog/42c620eb-0d77-4350-b070-bcd1e182fe84).</span><span class="sxs-lookup"><span data-stu-id="9b03d-122">For a complete reference, see [Windows Media Log Data Structure](/openspecs/windows_protocols/ms-wmlog/42c620eb-0d77-4350-b070-bcd1e182fe84).</span></span>

## <a name="configuring-log-fields"></a><span data-ttu-id="9b03d-123">Configuración de campos de registro</span><span class="sxs-lookup"><span data-stu-id="9b03d-123">Configuring Log Fields</span></span>

<span data-ttu-id="9b03d-124">Media Foundation permite al cliente configurar el origen de red mediante propiedades.</span><span class="sxs-lookup"><span data-stu-id="9b03d-124">Media Foundation enables the client to configure the network source by using properties.</span></span> <span data-ttu-id="9b03d-125">La aplicación debe establecer las propiedades adecuadas en un almacén de propiedades y pasarla a uno de los métodos de resolución de origen.</span><span class="sxs-lookup"><span data-stu-id="9b03d-125">The application must set the appropriate properties in a property store and pass it to one of the source resolver methods.</span></span> <span data-ttu-id="9b03d-126">El solucionador de origen crea el origen de red como se solicitó y abre una conexión con el servidor.</span><span class="sxs-lookup"><span data-stu-id="9b03d-126">The source resolver creates the network source as requested and opens a connection with the server.</span></span> <span data-ttu-id="9b03d-127">Si la conexión es correcta, el cliente envía información sobre sí mismo.</span><span class="sxs-lookup"><span data-stu-id="9b03d-127">If the connection is successful, the client sends information about itself.</span></span>

<span data-ttu-id="9b03d-128">En la tabla siguiente se describen los campos de registro y las propiedades correspondientes que una aplicación puede establecer a través del solucionador de origen.</span><span class="sxs-lookup"><span data-stu-id="9b03d-128">The following table describes the log fields and the corresponding properties that an application can set through the source resolver.</span></span> <span data-ttu-id="9b03d-129">Esta información no cambia durante la sesión.</span><span class="sxs-lookup"><span data-stu-id="9b03d-129">This information does not change during the session.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9b03d-130">Campo De registro</span><span class="sxs-lookup"><span data-stu-id="9b03d-130">Logging field</span></span></th>
<th><span data-ttu-id="9b03d-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="9b03d-131">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9b03d-132">c-playerid</span><span class="sxs-lookup"><span data-stu-id="9b03d-132">c-playerid</span></span></td>
<td><span data-ttu-id="9b03d-133">Identificación única del jugador.</span><span class="sxs-lookup"><span data-stu-id="9b03d-133">Unique identification of the player.</span></span> <span data-ttu-id="9b03d-134">Esta información se envía al principio de la conexión.</span><span class="sxs-lookup"><span data-stu-id="9b03d-134">This information is sent at the beginning of the connection.</span></span> <span data-ttu-id="9b03d-135">Normalmente, se trata de un GUID del cliente.</span><span class="sxs-lookup"><span data-stu-id="9b03d-135">Typically, this is a GUID of the client.</span></span> <span data-ttu-id="9b03d-136">El cliente puede enviar esta información al servidor en la <a href="mfnetsource-playerid-property.md"><strong>MFNETSOURCE_PLAYERID</strong></a> propiedad .</span><span class="sxs-lookup"><span data-stu-id="9b03d-136">The client can send this information to the server in the <a href="mfnetsource-playerid-property.md"><strong>MFNETSOURCE_PLAYERID</strong></a> property.</span></span><br/> <span data-ttu-id="9b03d-137">El cliente envía esta información al servidor al principio de la conexión.</span><span class="sxs-lookup"><span data-stu-id="9b03d-137">The client sends this information to the server at the beginning of the connection.</span></span><br/> <span data-ttu-id="9b03d-138">Valor de ejemplo: &quot; {c579d042-cecc-11d1-bb31-00a0c9603954}&quot;</span><span class="sxs-lookup"><span data-stu-id="9b03d-138">Sample value: &quot;{c579d042-cecc-11d1-bb31-00a0c9603954}&quot;</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b03d-139">c-playerversion</span><span class="sxs-lookup"><span data-stu-id="9b03d-139">c-playerversion</span></span></td>
<td><span data-ttu-id="9b03d-140">Número de versión del reproductor que se envía al principio de la conexión.</span><span class="sxs-lookup"><span data-stu-id="9b03d-140">The version number of the player that is sent at the beginning of the connection.</span></span> <span data-ttu-id="9b03d-141">El cliente puede enviar esta información al servidor en la <a href="mfnetsource-playerversion-property.md"><strong>MFNETSOURCE_PLAYERVERSION</strong></a> propiedad .</span><span class="sxs-lookup"><span data-stu-id="9b03d-141">The client can send this information to the server in the <a href="mfnetsource-playerversion-property.md"><strong>MFNETSOURCE_PLAYERVERSION</strong></a> property.</span></span><br/> <span data-ttu-id="9b03d-142">El cliente envía esta información al servidor al principio de la conexión.</span><span class="sxs-lookup"><span data-stu-id="9b03d-142">The client sends this information to the server at the beginning of the connection.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b03d-143">cs(User-Agent)</span><span class="sxs-lookup"><span data-stu-id="9b03d-143">cs(User-Agent)</span></span></td>
<td><span data-ttu-id="9b03d-144">Tipo de explorador usado si el reproductor se insertó en un explorador.</span><span class="sxs-lookup"><span data-stu-id="9b03d-144">Browser type used if the player was embedded in a browser.</span></span> <span data-ttu-id="9b03d-145">El cliente puede establecer este valor en la <a href="mfnetsource-browseruseragent-property.md"><strong>MFNETSOURCE_BROWSERUSERAGENT</strong></a> propiedad .</span><span class="sxs-lookup"><span data-stu-id="9b03d-145">This value can be set by the client in the <a href="mfnetsource-browseruseragent-property.md"><strong>MFNETSOURCE_BROWSERUSERAGENT</strong></a> property.</span></span><br/> <span data-ttu-id="9b03d-146">Si el reproductor no está incrustado, este campo hace referencia al agente de usuario del cliente que generó el registro.</span><span class="sxs-lookup"><span data-stu-id="9b03d-146">If the player was not embedded, this field refers to the user agent of the client that generated the log.</span></span> <span data-ttu-id="9b03d-147">En este caso, el cliente debe establecer la <a href="mfnetsource-playeruseragent-property.md"><strong>MFNETSOURCE_PLAYERUSERAGENT</strong></a> propiedad .</span><span class="sxs-lookup"><span data-stu-id="9b03d-147">In this case, the client must set the <a href="mfnetsource-playeruseragent-property.md"><strong>MFNETSOURCE_PLAYERUSERAGENT</strong></a> property.</span></span><br/> <span data-ttu-id="9b03d-148">El cliente envía esta información al servidor al principio de la conexión.</span><span class="sxs-lookup"><span data-stu-id="9b03d-148">The client sends this information to the server at the beginning of the connection.</span></span><br/> <span data-ttu-id="9b03d-149">Valor de ejemplo: &quot; Mozilla/4.0_(compatible;_MSIE_4.01;_Windows_98)&quot;</span><span class="sxs-lookup"><span data-stu-id="9b03d-149">Sample value: &quot;Mozilla/4.0_(compatible;_MSIE_4.01;_Windows_98)&quot;</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b03d-150">cs(Referer)</span><span class="sxs-lookup"><span data-stu-id="9b03d-150">cs(Referer)</span></span></td>
<td><span data-ttu-id="9b03d-151">Dirección URL de la página web en la que se insertó el reproductor (si se insertó).</span><span class="sxs-lookup"><span data-stu-id="9b03d-151">URL of the webpage in which the player was embedded (if it was embedded).</span></span> <span data-ttu-id="9b03d-152">El cliente puede enviar esta información al servidor en la <a href="mfnetsource-browserwebpage-property.md"><strong>MFNETSOURCE_BROWSERWEBPAGE</strong></a> propiedad .</span><span class="sxs-lookup"><span data-stu-id="9b03d-152">The client can send this information to the server in the <a href="mfnetsource-browserwebpage-property.md"><strong>MFNETSOURCE_BROWSERWEBPAGE</strong></a> property.</span></span><br/> <span data-ttu-id="9b03d-153">El cliente envía esta información al servidor al final de la conexión.</span><span class="sxs-lookup"><span data-stu-id="9b03d-153">The client sends this information to the server at the end of the connection.</span></span><br/> <span data-ttu-id="9b03d-154">Valor de ejemplo: &quot; https://www.example.microsoft.com&quot ;</span><span class="sxs-lookup"><span data-stu-id="9b03d-154">Sample value: &quot;https://www.example.microsoft.com&quot;</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b03d-155">c-hostexe</span><span class="sxs-lookup"><span data-stu-id="9b03d-155">c-hostexe</span></span></td>
<td><span data-ttu-id="9b03d-156">Para las entradas de registro del reproductor, el programa host (.exe) que se ha ejecutado.</span><span class="sxs-lookup"><span data-stu-id="9b03d-156">For player log entries, the host program (.exe) that was run.</span></span> <span data-ttu-id="9b03d-157">Por ejemplo, una página web en un explorador, un applet Visual Basic microsoft o un reproductor independiente.</span><span class="sxs-lookup"><span data-stu-id="9b03d-157">For example, a webpage in a browser, a Microsoft Visual Basic applet, or a stand-alone player.</span></span> <span data-ttu-id="9b03d-158">El cliente puede enviar esta información al servidor en la <a href="mfnetsource-hostexe-property.md"><strong>MFNETSOURCE_HOSTEXE</strong></a> propiedad .</span><span class="sxs-lookup"><span data-stu-id="9b03d-158">The client can send this information to the server in the <a href="mfnetsource-hostexe-property.md"><strong>MFNETSOURCE_HOSTEXE</strong></a> property.</span></span><br/> <span data-ttu-id="9b03d-159">El cliente envía esta información al servidor al final de la conexión.</span><span class="sxs-lookup"><span data-stu-id="9b03d-159">The client sends this information to the server at the end of the connection.</span></span><br/> <span data-ttu-id="9b03d-160">Valores de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="9b03d-160">Sample values:</span></span><br/>
<ul>
<li><span data-ttu-id="9b03d-161">&quot;iexplore.exe&quot;</span><span class="sxs-lookup"><span data-stu-id="9b03d-161">&quot;iexplore.exe&quot;</span></span></li>
<li><span data-ttu-id="9b03d-162">&quot;myplayer.exe&quot;</span><span class="sxs-lookup"><span data-stu-id="9b03d-162">&quot;myplayer.exe&quot;</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b03d-163">c-hostexever</span><span class="sxs-lookup"><span data-stu-id="9b03d-163">c-hostexever</span></span></td>
<td><span data-ttu-id="9b03d-164">Número de versión del programa host (.exe).</span><span class="sxs-lookup"><span data-stu-id="9b03d-164">Host program (.exe) version number.</span></span> <span data-ttu-id="9b03d-165">El cliente puede enviar esta información al servidor en la <a href="mfnetsource-hostversion-property.md"><strong>MFNETSOURCE_HOSTVERSION</strong></a> propiedad .</span><span class="sxs-lookup"><span data-stu-id="9b03d-165">The client can send this information to the server in the <a href="mfnetsource-hostversion-property.md"><strong>MFNETSOURCE_HOSTVERSION</strong></a> property.</span></span><br/> <span data-ttu-id="9b03d-166">El cliente envía esta información al servidor al final de la conexión.</span><span class="sxs-lookup"><span data-stu-id="9b03d-166">The client sends this information to the server at the end of the connection.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="9b03d-167">En el ejemplo de código siguiente se muestra cómo una aplicación cliente configura el origen de red.</span><span class="sxs-lookup"><span data-stu-id="9b03d-167">The following code example shows how a client application configures the network source.</span></span> <span data-ttu-id="9b03d-168">En este ejemplo se establece el campo de registro "c-hostexe".</span><span class="sxs-lookup"><span data-stu-id="9b03d-168">This example sets the "c-hostexe" log field.</span></span>


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



## <a name="retrieving-network-statistics"></a><span data-ttu-id="9b03d-169">Recuperación de estadísticas de red</span><span class="sxs-lookup"><span data-stu-id="9b03d-169">Retrieving Network Statistics</span></span>

<span data-ttu-id="9b03d-170">Cuando la aplicación llama a uno de los métodos de resolución de origen, crea el origen de red, establece las propiedades especificadas en el almacén de propiedades y abre una sesión con el servidor multimedia.</span><span class="sxs-lookup"><span data-stu-id="9b03d-170">When the application calls one of the source resolver methods, it creates the network source, sets the properties specified in the property store, and opens a session with the media server.</span></span> <span data-ttu-id="9b03d-171">Además de la información configurable descrita en la sección anterior, se transfieren datos adicionales entre el servidor y el cliente al principio de la sesión, durante el streaming y cuando se cierra la sesión.</span><span class="sxs-lookup"><span data-stu-id="9b03d-171">In addition to the configurable information described in the previous section, additional data is transferred between the server and the client at the beginning of the session, during streaming, and when the session is closed.</span></span>

<span data-ttu-id="9b03d-172">La aplicación puede recuperar estadísticas de red mediante el identificador de servicio **MFNETSOURCE \_ STATISTICS \_ SERVICE.**</span><span class="sxs-lookup"><span data-stu-id="9b03d-172">The application can retrieve network statistics by using the **MFNETSOURCE\_STATISTICS\_SERVICE** service identifier.</span></span> <span data-ttu-id="9b03d-173">Para usar este servicio, la aplicación puede llamar a la función [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) para obtener el almacén de propiedades que contiene estadísticas de red en la [**propiedad MFNETSOURCE \_ STATISTICS.**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids)</span><span class="sxs-lookup"><span data-stu-id="9b03d-173">To use this service, the application can call the [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) function to get the property store that contains network statistics in the [**MFNETSOURCE\_STATISTICS**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids) property.</span></span> <span data-ttu-id="9b03d-174">Se pueden recuperar valores específicos proporcionando el identificador correspondiente definido en la enumeración **MFNETSOURCE \_ STATISTICS \_ IDS.**</span><span class="sxs-lookup"><span data-stu-id="9b03d-174">Specific values can be retrieved by providing the corresponding identifier defined in the **MFNETSOURCE\_STATISTICS\_IDS** enumeration.</span></span>

<span data-ttu-id="9b03d-175">En el ejemplo de código siguiente se muestra cómo usar el servicio para obtener el número de paquetes recibidos por el cliente.</span><span class="sxs-lookup"><span data-stu-id="9b03d-175">The following code example shows how to use the service to get the number of packets received by the client.</span></span>


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



<span data-ttu-id="9b03d-176">En la lista siguiente se describen algunos de los identificadores de estadísticas de red definidos en [**MFNETSOURCE \_ STATISTICS \_ IDS**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids).</span><span class="sxs-lookup"><span data-stu-id="9b03d-176">The following list describes some of the network statistics identifiers defined in [**MFNETSOURCE\_STATISTICS\_IDS**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids).</span></span>



| <span data-ttu-id="9b03d-177">Identificador de estadísticas de red</span><span class="sxs-lookup"><span data-stu-id="9b03d-177">Network statistics identifier</span></span>              | <span data-ttu-id="9b03d-178">Descripción</span><span class="sxs-lookup"><span data-stu-id="9b03d-178">Description</span></span>                                                                                                                                                                                                                |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b03d-179">**ID. \_ DE AVGBANDWIDTHBPS DE \_ MFNETSOURCE**</span><span class="sxs-lookup"><span data-stu-id="9b03d-179">**MFNETSOURCE\_AVGBANDWIDTHBPS\_ID**</span></span>       | <span data-ttu-id="9b03d-180">Ancho de banda medio (en bits por segundo) en el que el cliente estaba conectado al servidor.</span><span class="sxs-lookup"><span data-stu-id="9b03d-180">Average bandwidth (in bits per second) at which the client was connected to the server.</span></span> <span data-ttu-id="9b03d-181">El valor se calcula a lo largo de toda la duración de la conexión.</span><span class="sxs-lookup"><span data-stu-id="9b03d-181">The value is calculated across the entire duration of the connection.</span></span>                                                              |
| <span data-ttu-id="9b03d-182">**ID. \_ DE MFNETSOURCE \_ BUFFERINGCOUNT**</span><span class="sxs-lookup"><span data-stu-id="9b03d-182">**MFNETSOURCE\_BUFFERINGCOUNT\_ID**</span></span>        | <span data-ttu-id="9b03d-183">Número de veces que el cliente ha almacenado en búfer durante la reproducción de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="9b03d-183">Number of times the client buffered while playing the stream.</span></span>                                                                                                                                                              |
| <span data-ttu-id="9b03d-184">**MFNETSOURCE \_ BYTESRECEIVED \_ ID**</span><span class="sxs-lookup"><span data-stu-id="9b03d-184">**MFNETSOURCE\_BYTESRECEIVED\_ID**</span></span>         | <span data-ttu-id="9b03d-185">Número de bytes recibidos por el cliente del servidor.</span><span class="sxs-lookup"><span data-stu-id="9b03d-185">Number of bytes received by the client from the server.</span></span> <span data-ttu-id="9b03d-186">El valor no incluye ninguna sobrecarga agregada por la pila de red.</span><span class="sxs-lookup"><span data-stu-id="9b03d-186">The value does not include any overhead that is added by the network stack.</span></span> <span data-ttu-id="9b03d-187">El mismo contenido transmitido mediante protocolos diferentes puede dar lugar a valores diferentes.</span><span class="sxs-lookup"><span data-stu-id="9b03d-187">The same content streamed by using different protocols can result in different values.</span></span> |
| <span data-ttu-id="9b03d-188">**ID. DE \_ MFNETSOURCE LINKBANDWIDTH \_**</span><span class="sxs-lookup"><span data-stu-id="9b03d-188">**MFNETSOURCE\_LINKBANDWIDTH\_ID**</span></span>         | <span data-ttu-id="9b03d-189">Ancho de banda máximo disponible del cliente en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="9b03d-189">Maximum available bandwidth of the client in bits per second.</span></span>                                                                                                                                                              |
| <span data-ttu-id="9b03d-190">**ID. \_ DE LOSTPACKETS DE MFNETSOURCE \_**</span><span class="sxs-lookup"><span data-stu-id="9b03d-190">**MFNETSOURCE\_LOSTPACKETS\_ID**</span></span>           | <span data-ttu-id="9b03d-191">Número de paquetes enviados por el servidor pero perdidos durante la transmisión y nunca reproducida por el cliente.</span><span class="sxs-lookup"><span data-stu-id="9b03d-191">Number of packets sent by the server but lost during transmission, and never played by the client.</span></span> <span data-ttu-id="9b03d-192">El valor no incluye paquetes TCP o UDP.</span><span class="sxs-lookup"><span data-stu-id="9b03d-192">The value does not include TCP or UDP packets.</span></span>                                                                          |
| <span data-ttu-id="9b03d-193">**ID. \_ DE RECVPACKETS DE MFNETSOURCE \_**</span><span class="sxs-lookup"><span data-stu-id="9b03d-193">**MFNETSOURCE\_RECVPACKETS\_ID**</span></span>           | <span data-ttu-id="9b03d-194">Número de paquetes recibidos del servidor El valor no incluye paquetes TCP o UDP.</span><span class="sxs-lookup"><span data-stu-id="9b03d-194">Number of packets received from the server The value does not include TCP or UDP packets.</span></span>                                                                                                                                  |
| <span data-ttu-id="9b03d-195">**ID. \_ DE MFNETSOURCE RECOVEREDBYECCPACKETS \_**</span><span class="sxs-lookup"><span data-stu-id="9b03d-195">**MFNETSOURCE\_RECOVEREDBYECCPACKETS\_ID**</span></span> | <span data-ttu-id="9b03d-196">Paquetes perdidos en la red que se repararon y recuperaron en la capa de cliente.</span><span class="sxs-lookup"><span data-stu-id="9b03d-196">Packets lost in the network that were repaired and recovered at the client layer.</span></span> <span data-ttu-id="9b03d-197">Este valor no incluye paquetes TCP o UDP.</span><span class="sxs-lookup"><span data-stu-id="9b03d-197">This value does not include TCP or UDP packets.</span></span>                                                                                          |
| <span data-ttu-id="9b03d-198">**MFNETSOURCE \_ RESENDSREQUESTED \_ ID**</span><span class="sxs-lookup"><span data-stu-id="9b03d-198">**MFNETSOURCE\_RESENDSREQUESTED\_ID**</span></span>      | <span data-ttu-id="9b03d-199">Número de solicitudes realizadas por el cliente para recibir nuevos paquetes.</span><span class="sxs-lookup"><span data-stu-id="9b03d-199">The number of requests made by the client to receive new packets.</span></span> <span data-ttu-id="9b03d-200">Este valor no incluye paquetes TCP o UDP.</span><span class="sxs-lookup"><span data-stu-id="9b03d-200">This value does not include TCP or UDP packets.</span></span>                                                                                                          |
| <span data-ttu-id="9b03d-201">**ID. \_ DE MFNETSOURCE RECOVEREDPACKETS \_**</span><span class="sxs-lookup"><span data-stu-id="9b03d-201">**MFNETSOURCE\_RECOVEREDPACKETS\_ID**</span></span>      | <span data-ttu-id="9b03d-202">Número de paquetes recuperados porque se han reenviado a través de UDP.</span><span class="sxs-lookup"><span data-stu-id="9b03d-202">Number of packets recovered because they were resent through UDP.</span></span> <span data-ttu-id="9b03d-203">Este valor no incluye paquetes TCP o UDP.</span><span class="sxs-lookup"><span data-stu-id="9b03d-203">This value does not include TCP or UDP packets.</span></span> <span data-ttu-id="9b03d-204">Este campo contiene un cero a menos que el cliente use el reenenlaz de UDP.</span><span class="sxs-lookup"><span data-stu-id="9b03d-204">This field contains a zero unless the client is using UDP resend.</span></span>                                        |
| <span data-ttu-id="9b03d-205">**ID. \_ DE BUFFERPROGRESS DE \_ MFNETSOURCE**</span><span class="sxs-lookup"><span data-stu-id="9b03d-205">**MFNETSOURCE\_BUFFERPROGRESS\_ID**</span></span>        | <span data-ttu-id="9b03d-206">Porcentaje del búfer de reproducción rellenado durante el almacenamiento en búfer.</span><span class="sxs-lookup"><span data-stu-id="9b03d-206">The percentage of the playout buffer filled during buffering.</span></span>                                                                                                                                                              |
| <span data-ttu-id="9b03d-207">**ID. DE \_ PROTOCOLO \_ MFNETSOURCE**</span><span class="sxs-lookup"><span data-stu-id="9b03d-207">**MFNETSOURCE\_PROTOCOL\_ID**</span></span>              | <span data-ttu-id="9b03d-208">Protocolo utilizado para acceder a la secuencia.</span><span class="sxs-lookup"><span data-stu-id="9b03d-208">Protocol used to access the stream.</span></span> <span data-ttu-id="9b03d-209">Esto puede diferir del protocolo solicitado por el cliente.</span><span class="sxs-lookup"><span data-stu-id="9b03d-209">This may differ from the protocol requested by the client.</span></span>                                                                                                                             |
| <span data-ttu-id="9b03d-210">**ID. DE \_ TRANSPORTE DE MFNETSOURCE \_**</span><span class="sxs-lookup"><span data-stu-id="9b03d-210">**MFNETSOURCE\_TRANSPORT\_ID**</span></span>             | <span data-ttu-id="9b03d-211">Protocolo de transporte utilizado para entregar la secuencia.</span><span class="sxs-lookup"><span data-stu-id="9b03d-211">Transport protocol used to deliver the stream.</span></span> <span data-ttu-id="9b03d-212">Debe ser UDP o TCP.</span><span class="sxs-lookup"><span data-stu-id="9b03d-212">This must be either UDP or TCP.</span></span>                                                                                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="9b03d-213">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9b03d-213">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b03d-214">Características de origen de red</span><span class="sxs-lookup"><span data-stu-id="9b03d-214">Network Source Features</span></span>](network-source-features.md)
</dt> <dt>

[<span data-ttu-id="9b03d-215">Redes en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9b03d-215">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

