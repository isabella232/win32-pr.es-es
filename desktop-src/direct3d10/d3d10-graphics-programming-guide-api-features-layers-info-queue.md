---
description: Personalizar la salida de depuración con ID3D10InfoQueue (Direct3D 10)
ms.assetid: 082c7783-c53a-4b73-b8f2-3f60e2c2689a
title: Personalizar la salida de depuración con ID3D10InfoQueue (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 843ac7dd34b19cfe1fc7835a2026ae2dd28b9dcd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080230"
---
# <a name="customize-debug-output-with-id3d10infoqueue-direct3d-10"></a><span data-ttu-id="2efc7-103">Personalizar la salida de depuración con ID3D10InfoQueue (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="2efc7-103">Customize Debug Output with ID3D10InfoQueue (Direct3D 10)</span></span>

<span data-ttu-id="2efc7-104">La cola de información se administra mediante una interfaz (vea la [**interfaz ID3D10InfoQueue**](/windows/desktop/api/D3D10SDKLayers/nn-d3d10sdklayers-id3d10infoqueue)) que almacena, recupera y filtra los mensajes de depuración.</span><span class="sxs-lookup"><span data-stu-id="2efc7-104">The information queue is managed by an interface (see [**ID3D10InfoQueue Interface**](/windows/desktop/api/D3D10SDKLayers/nn-d3d10sdklayers-id3d10infoqueue)) that stores, retrieves, and filters debug messages.</span></span> <span data-ttu-id="2efc7-105">La cola consta de: una cola de mensajes, una pila de filtros de almacenamiento opcional y una pila de filtros de recuperación opcional.</span><span class="sxs-lookup"><span data-stu-id="2efc7-105">The queue consists of: a message queue, an optional storage filter stack, and a optional retrieval filter stack.</span></span> <span data-ttu-id="2efc7-106">La pila de filtros de almacenamiento se puede usar para filtrar los mensajes que desea almacenar; la pila de filtros de recuperación se puede usar para filtrar los mensajes que desea almacenar.</span><span class="sxs-lookup"><span data-stu-id="2efc7-106">The storage-filter stack can be used to filter the messages you want stored; the retrieval-filter stack can be used to filter the messages you want stored.</span></span> <span data-ttu-id="2efc7-107">Una vez que haya filtrado un mensaje, el mensaje se imprimirá en la ventana de depuración y se almacenará en la pila adecuada.</span><span class="sxs-lookup"><span data-stu-id="2efc7-107">Once you have filtered a message, the message will be printed out to the debug window and stored in the appropriate stack.</span></span>

<span data-ttu-id="2efc7-108">En general:</span><span class="sxs-lookup"><span data-stu-id="2efc7-108">In general:</span></span>

-   <span data-ttu-id="2efc7-109">Llamar a [**ID3D10InfoQueue:: AddApplicationMessage**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-addapplicationmessage) para generar mensajes definidos por el usuario</span><span class="sxs-lookup"><span data-stu-id="2efc7-109">Call [**ID3D10InfoQueue::AddApplicationMessage**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-addapplicationmessage) to generate user-defined messages</span></span>
-   <span data-ttu-id="2efc7-110">La llamada a [**ID3D10InfoQueue:: GetMessage**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-getmessage) se usa para obtener mensajes (que pasan un filtro de recuperación opcional).</span><span class="sxs-lookup"><span data-stu-id="2efc7-110">Call [**ID3D10InfoQueue::GetMessage**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-getmessage) is used to get messages (that pass an optional retrieval filter).</span></span>

## <a name="registry-controls"></a><span data-ttu-id="2efc7-111">Controles del registro</span><span class="sxs-lookup"><span data-stu-id="2efc7-111">Registry Controls</span></span>

<span data-ttu-id="2efc7-112">Use las claves del registro para ajustar la configuración del filtro, ajustar los puntos de interrupción y silenciar los resultados de la depuración.</span><span class="sxs-lookup"><span data-stu-id="2efc7-112">Use registry keys to adjust filter settings, adjust break points, and to mute the debug output.</span></span> <span data-ttu-id="2efc7-113">El nivel de depuración comprobará estas rutas de acceso para las claves del registro; se usará la primera ruta de acceso encontrada.</span><span class="sxs-lookup"><span data-stu-id="2efc7-113">The debug layer will check these paths for registry keys; the first path found will be used.</span></span>

1.  <span data-ttu-id="2efc7-114">HKCU \\ software \\ Microsoft \\ Direct3D \\<subclave definida por el usuario></span><span class="sxs-lookup"><span data-stu-id="2efc7-114">HKCU\\Software\\Microsoft\\Direct3D\\<user-defined subkey></span></span>
2.  <span data-ttu-id="2efc7-115">HKLM \\ software \\ Microsoft \\ Direct3D \\<subclave definida por el usuario></span><span class="sxs-lookup"><span data-stu-id="2efc7-115">HKLM\\Software\\Microsoft\\Direct3D\\<user-defined subkey></span></span>
3.  <span data-ttu-id="2efc7-116">HKCU \\ software \\ Microsoft \\ Direct3D</span><span class="sxs-lookup"><span data-stu-id="2efc7-116">HKCU\\Software\\Microsoft\\Direct3D</span></span>

<span data-ttu-id="2efc7-117">Donde:</span><span class="sxs-lookup"><span data-stu-id="2efc7-117">Where:</span></span>

-   <span data-ttu-id="2efc7-118">El usuario actual de la versión HKEY es el de la \_ \_ \_ máquina local \_ .</span><span class="sxs-lookup"><span data-stu-id="2efc7-118">HKCU stand for HKEY\_CURRENT\_USER, and HKLM stand for HKEY\_LOCAL\_MACHINE.</span></span>
-   <span data-ttu-id="2efc7-119"><subclave definida por el usuario> es un nombre arbitrario para almacenar la configuración de depuración de una aplicación</span><span class="sxs-lookup"><span data-stu-id="2efc7-119"><user-defined subkey> is an arbitrary name to store debug settings for an application</span></span>

### <a name="filtering-debug-messages-using-registry-keys"></a><span data-ttu-id="2efc7-120">Filtrado de mensajes de depuración con claves del registro</span><span class="sxs-lookup"><span data-stu-id="2efc7-120">Filtering Debug Messages using Registry Keys</span></span>

<span data-ttu-id="2efc7-121">Si el registro contiene una clave InfoQueueStorageFilterOverride (y es distinto de cero), se pueden filtrar los mensajes (y la salida de depuración) agregando los siguientes controles del registro.</span><span class="sxs-lookup"><span data-stu-id="2efc7-121">If the registry contains an InfoQueueStorageFilterOverride key (and is non-zero), then messages (and debug output) can be filtered by adding the following registry controls.</span></span>

-   <span data-ttu-id="2efc7-122">DWORD silenciar \_ categoría \_ \* : salida de depuración si esta clave es distinta de cero.</span><span class="sxs-lookup"><span data-stu-id="2efc7-122">DWORD Mute\_CATEGORY\_\* - Debug output if this key is non-zero.</span></span>
-   <span data-ttu-id="2efc7-123">\_Gravedad de silencio \_ \* de DWORD: la salida de depuración está deshabilitada si esta clave es distinta de cero.</span><span class="sxs-lookup"><span data-stu-id="2efc7-123">DWORD Mute\_SEVERITY\_\* - Debug output is disabled if this key is non-zero.</span></span>
-   <span data-ttu-id="2efc7-124">Identificador de \_ silencio \_ \* de DWORD: el nombre o número del mensaje se puede usar para \* (al igual que para el ID. de interrupción \_ \_ \* descrito anteriormente).</span><span class="sxs-lookup"><span data-stu-id="2efc7-124">DWORD Mute\_ID\_\* - Message name or number can be used for \* (just like for BreakOn\_ID\_\* described earlier).</span></span> <span data-ttu-id="2efc7-125">La salida de depuración está deshabilitada si esta clave es distinta de cero.</span><span class="sxs-lookup"><span data-stu-id="2efc7-125">Debug output is disabled if this key is non-zero.</span></span>
-   <span data-ttu-id="2efc7-126">DWORD Unmute \_ Severity \_ info: la salida de depuración está habilitada si esta clave es distinta de cero.</span><span class="sxs-lookup"><span data-stu-id="2efc7-126">DWORD Unmute\_SEVERITY\_INFO - Debug output is ENABLED if this key is non-zero.</span></span> <span data-ttu-id="2efc7-127">De forma predeterminada, cuando InfoQueueStorageFilterOverride está habilitado, los mensajes de depuración con información de gravedad están silenciados; por lo tanto, esta clave permite volver a activar la información.</span><span class="sxs-lookup"><span data-stu-id="2efc7-127">By default when InfoQueueStorageFilterOverride is enabled, debug messages with severity INFO are muted - therefore for this key allows INFO to be turned back on.</span></span>

<span data-ttu-id="2efc7-128">Estos controles cambian si se registra o muestra un mensaje; no afectan a si una API supera o no.</span><span class="sxs-lookup"><span data-stu-id="2efc7-128">These controls change whether a message is recorded or displayed; they do not affect whether an API passes or fails.</span></span>

### <a name="setting-break-conditions-using-registry-keys"></a><span data-ttu-id="2efc7-129">Establecer condiciones de interrupción mediante claves del registro</span><span class="sxs-lookup"><span data-stu-id="2efc7-129">Setting Break Conditions using Registry Keys</span></span>

<span data-ttu-id="2efc7-130">Las aplicaciones pueden verse obligadas a interrumpir en un mensaje con las siguientes claves del registro.</span><span class="sxs-lookup"><span data-stu-id="2efc7-130">Applications can be forced to break on a message using the following registry keys.</span></span>

<span data-ttu-id="2efc7-131">**EnableBreakOnMessage** : esta clave permite la interrupción de mensajes (y hace que se omita la configuración de SetBreakOnCategory ()/SetBreakOnSeverity ()/SetBreakOnID ().</span><span class="sxs-lookup"><span data-stu-id="2efc7-131">**EnableBreakOnMessage** - This key enables breaking on messages (and causes i's SetBreakOnCategory()/SetBreakOnSeverity()/SetBreakOnID() settings to be ignored).</span></span> <span data-ttu-id="2efc7-132">Los mensajes reales en los que se debe interrumpir se definen mediante uno o varios valores de breakon \_ \* definidos a continuación.</span><span class="sxs-lookup"><span data-stu-id="2efc7-132">The actual messages to break on are defined using one or more BreakOn\_\* values defined below.</span></span>

-   <span data-ttu-id="2efc7-133">\**\_ Breakon \_Categoría \** _-break en cualquier mensaje que pase a través de los filtros de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="2efc7-133">\**BreakOn\_CATEGORY\_\** _ - Break on any message passing through the storage filters.</span></span> <span data-ttu-id="2efc7-134">\_ es uno de los mensajes de la \_ categoría de mensajes D3D10 \_ .</span><span class="sxs-lookup"><span data-stu-id="2efc7-134">\_ is one of the D3D10\_MESSAGE\_CATEGORY messages.</span></span>
-   <span data-ttu-id="2efc7-135">\**\_ Breakon \_Gravedad \** _-break en cualquier mensaje que pase a través de los filtros de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="2efc7-135">\**BreakOn\_SEVERITY\_\** _ - Break on any message passing through the storage filters.</span></span> <span data-ttu-id="2efc7-136">\_ es uno de los mensajes de gravedad del mensaje de D3D10 \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="2efc7-136">\_ is one of the D3D10\_MESSAGE\_SEVERITY\_ messages.</span></span>
-   <span data-ttu-id="2efc7-137">\**\_ Breakon \_Identificador \** _-break en cualquier mensaje que pase a través de los filtros de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="2efc7-137">\**BreakOn\_ID\_\** _ - Break on any message passing through the storage filters.</span></span> <span data-ttu-id="2efc7-138">\_ es uno de los \_ mensajes de \_ ID. de mensaje D3D10 \_ o puede ser el valor numérico de la enumeración error.</span><span class="sxs-lookup"><span data-stu-id="2efc7-138">\_ is one of the D3D10\_MESSAGE\_ID\_ messages or can be the numerical value of the error enumeration.</span></span> <span data-ttu-id="2efc7-139">Por ejemplo, supongamos que el mensaje con el identificador "D3D10 \_ Message \_ ID \_ hipotético" tenía el valor 123 en la \_ \_ enumeración D3D10 Message ID.</span><span class="sxs-lookup"><span data-stu-id="2efc7-139">For example, Suppose the message with ID "D3D10\_MESSAGE\_ID\_HYPOTHETICAL" had the value 123 in the D3D10\_MESSAGE\_ID enumeration.</span></span> <span data-ttu-id="2efc7-140">En este caso, la creación del valor de \_ ID. de interrupción \_ hipotética = 1 o el \_ ID. de interrupción \_ 123 = 1 realizaría la misma interrupción cuando se encuentra un mensaje con el ID. de mensaje de identificador D3D10 \_ \_ \_ hipotética.</span><span class="sxs-lookup"><span data-stu-id="2efc7-140">In this case, creating the value BreakOn\_ID\_HYPOTHETICAL=1 or BreakOn\_ID\_123=1 would both accomplish the same thing - break when a message having ID D3D10\_MESSAGE\_ID\_HYPOTHETICAL is encountered.</span></span>

### <a name="muting-debug-output-using-registry-keys"></a><span data-ttu-id="2efc7-141">Silenciar la salida de depuración con claves del registro</span><span class="sxs-lookup"><span data-stu-id="2efc7-141">Muting Debug Output using Registry Keys</span></span>

<span data-ttu-id="2efc7-142">La salida de depuración se puede silenciar mediante una clave MuteDebugOutput.</span><span class="sxs-lookup"><span data-stu-id="2efc7-142">Debug output can be muted using a MuteDebugOutput key.</span></span> <span data-ttu-id="2efc7-143">La presencia de este valor en el registro fuerza la invalidación del método [**ID3D10InfoQueue:: SetMuteDebugOutput**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-setmutedebugoutput) de InfoQueue.</span><span class="sxs-lookup"><span data-stu-id="2efc7-143">The presence of this value in the registry forces override of the InfoQueue's [**ID3D10InfoQueue::SetMuteDebugOutput**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-setmutedebugoutput) method.</span></span> <span data-ttu-id="2efc7-144">MuteDebugOutput detiene los mensajes que pasan el filtro de almacenamiento para que no se envíen a la salida de depuración.</span><span class="sxs-lookup"><span data-stu-id="2efc7-144">MuteDebugOutput stops messages that pass the storage filter from being sent to debug output.</span></span>

## <a name="disabling-debug-layer-messages"></a><span data-ttu-id="2efc7-145">Deshabilitar mensajes de la capa de depuración</span><span class="sxs-lookup"><span data-stu-id="2efc7-145">Disabling Debug Layer Messages</span></span>

<span data-ttu-id="2efc7-146">Los mensajes de la capa de depuración se pueden deshabilitar individualmente o como un grupo en tiempo de ejecución mediante la especificación de filtros mediante [**ID3D10InfoQueue:: AddStorageFilterEntries**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-addstoragefilterentries).</span><span class="sxs-lookup"><span data-stu-id="2efc7-146">Debug layer messages can be disabled individualy or as a group at runtime by specifying filters using [**ID3D10InfoQueue::AddStorageFilterEntries**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-addstoragefilterentries).</span></span> <span data-ttu-id="2efc7-147">El argumento *pFilter* de **ID3D10InfoQueue:: AddStorageFilterEntries** toma una estructura de filtro de [**cola de D3D10 \_ \_ \_ info**](/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_info_queue_filter) que contiene una lista de permitidos y una lista de denegación.</span><span class="sxs-lookup"><span data-stu-id="2efc7-147">The *pFilter* argument to **ID3D10InfoQueue::AddStorageFilterEntries** takes a [**D3D10\_INFO\_QUEUE\_FILTER**](/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_info_queue_filter) structure that contains an allow list and a deny list.</span></span> <span data-ttu-id="2efc7-148">Las listas de permitidos y denegadas se describen en [**D3D10 \_ info \_ Queue \_ Filter \_ DESC**](/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_info_queue_filter_desc) Structures que permiten que los filtros se especifiquen mediante categoría, Severity y el ID. de mensaje individual.</span><span class="sxs-lookup"><span data-stu-id="2efc7-148">The allow and deny lists are described by [**D3D10\_INFO\_QUEUE\_FILTER\_DESC**](/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_info_queue_filter_desc) structures that allow filtering to be specified by catergory, severity and individual message ID.</span></span>

<span data-ttu-id="2efc7-149">El código siguiente es un ejemplo de la configuración de la [**interfaz ID3D10InfoQueue**](/windows/desktop/api/D3D10SDKLayers/nn-d3d10sdklayers-id3d10infoqueue) para denegar el \_ mensaje D3D10 Message \_ ID \_ Device \_ Draw \_ \_ búfer \_ demasiado \_ pequeño.</span><span class="sxs-lookup"><span data-stu-id="2efc7-149">The following code is an example of setting up the [**ID3D10InfoQueue Interface**](/windows/desktop/api/D3D10SDKLayers/nn-d3d10sdklayers-id3d10infoqueue) to deny the D3D10\_MESSAGE\_ID\_DEVICE\_DRAW\_INDEX\_BUFFER\_TOO\_SMALL message.</span></span>


```
  //retrieve the ID3D10InfoQueue from a Direct3D device created with the D3D10_CREATE_DEVICE_DEBUG flag
  ID3D10InfoQueue * pInfoQueue;
    g_pd3dDevice->QueryInterface( __uuidof(ID3D10InfoQueue),  (void **)&pInfoQueue );
    
  //set up the list of messages to filter
    D3D10_MESSAGE_ID messageIDs [] = { D3D10_MESSAGE_ID_DEVICE_DRAW_INDEX_BUFFER_TOO_SMALL };
    
  //set the DenyList to use the list of messages
    D3D10_INFO_QUEUE_FILTER filter = { 0 };
    filter.DenyList.NumIDs = 1;
    filter.DenyList.pIDList = messageIDs;
    
  //apply the filter to the info queue
    pInfoQueue->AddStorageFilterEntries( &filter );  
```



## <a name="related-topics"></a><span data-ttu-id="2efc7-150">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2efc7-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2efc7-151">Niveles de API</span><span class="sxs-lookup"><span data-stu-id="2efc7-151">API Layers</span></span>](d3d10-graphics-programming-guide-api-features-layers.md)
</dt> <dt>

[<span data-ttu-id="2efc7-152">Características de la API (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="2efc7-152">API Features (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 



