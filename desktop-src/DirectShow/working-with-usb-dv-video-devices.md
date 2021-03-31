---
description: Trabajar con dispositivos de vídeo DV USB
ms.assetid: 6244f006-db9f-42b2-81cd-26eba583613e
title: Trabajar con dispositivos de vídeo DV USB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75647aa7b53bac45c155b4e0a9283418c9af58b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275805"
---
# <a name="working-with-usb-dv-video-devices"></a><span data-ttu-id="e1f7b-103">Trabajar con dispositivos de vídeo DV USB</span><span class="sxs-lookup"><span data-stu-id="e1f7b-103">Working with USB DV Video Devices</span></span>

<span data-ttu-id="e1f7b-104">En este tema se describe cómo escribir aplicaciones para dispositivos de vídeo de bus serie universal (USB) que capturan vídeo DV.</span><span class="sxs-lookup"><span data-stu-id="e1f7b-104">This topic describes how to write applications for Universal Serial Bus (USB) video devices that capture DV video.</span></span>

<span data-ttu-id="e1f7b-105">El formato DV estándar tiene una velocidad de datos de aproximadamente 25 megabits por segundo (Mbps).</span><span class="sxs-lookup"><span data-stu-id="e1f7b-105">Standard DV format has a data rate of about 25 megabits per second (Mbps).</span></span> <span data-ttu-id="e1f7b-106">La primera vez que se presentó USB, no tenía suficiente ancho de banda para admitir vídeo DV.</span><span class="sxs-lookup"><span data-stu-id="e1f7b-106">When USB was first introduced, it did not have enough bandwidth to support DV video.</span></span> <span data-ttu-id="e1f7b-107">Sin embargo, USB 2,0 puede admitir hasta 480 Mbps, que es más que suficiente para vídeo DV.</span><span class="sxs-lookup"><span data-stu-id="e1f7b-107">However, USB 2.0 can support up to 480 Mbps, which is more than sufficient for DV video.</span></span> <span data-ttu-id="e1f7b-108">La especificación de la clase de dispositivo de vídeo USB (UVC), publicada en 2003, define el formato de carga para dispositivos de vídeo DV de USB.</span><span class="sxs-lookup"><span data-stu-id="e1f7b-108">The USB Video Device Class (UVC) specification, released in 2003, defines the payload format for USB DV video devices.</span></span> <span data-ttu-id="e1f7b-109">En Windows XP Service Pack 2, se presentó un controlador de clase Modelo de controlador de Windows (WDM) para dispositivos UVC.</span><span class="sxs-lookup"><span data-stu-id="e1f7b-109">A Windows Driver Model (WDM) class driver for UVC devices was introduced in Windows XP Service Pack 2.</span></span>

<span data-ttu-id="e1f7b-110">En la mayoría de los aspectos, el controlador UVC admite el mismo modelo de programación que el controlador MSDV para dispositivos IEEE 1394.</span><span class="sxs-lookup"><span data-stu-id="e1f7b-110">In most respects, the UVC driver supports the same programming model as the MSDV driver for IEEE 1394 devices.</span></span> <span data-ttu-id="e1f7b-111">Las aplicaciones escritas para MSDV deben requerir solo modificaciones mínimas para admitir dispositivos UVC.</span><span class="sxs-lookup"><span data-stu-id="e1f7b-111">Applications written for MSDV should require only minor modifications to support UVC devices.</span></span>

<span data-ttu-id="e1f7b-112">El controlador UVC se comporta de forma diferente al controlador MSDV en las siguientes áreas:</span><span class="sxs-lookup"><span data-stu-id="e1f7b-112">The UVC driver behaves differently from the MSDV driver in the following areas:</span></span>

-   [<span data-ttu-id="e1f7b-113">Modo de dispositivo</span><span class="sxs-lookup"><span data-stu-id="e1f7b-113">Device Mode</span></span>](device-mode.md)
-   [<span data-ttu-id="e1f7b-114">Formato de secuencia</span><span class="sxs-lookup"><span data-stu-id="e1f7b-114">Stream Format</span></span>](stream-format.md)
-   [<span data-ttu-id="e1f7b-115">Formato de señal</span><span class="sxs-lookup"><span data-stu-id="e1f7b-115">Signal Format</span></span>](signal-format.md)
-   [<span data-ttu-id="e1f7b-116">Búsqueda de ubicación de cinta</span><span class="sxs-lookup"><span data-stu-id="e1f7b-116">Tape Location Search</span></span>](tape-location-search.md)
-   <span data-ttu-id="e1f7b-117">[Transmitir DV desde un archivo a una cinta](transmit-dv-from-file-to-tape.md).</span><span class="sxs-lookup"><span data-stu-id="e1f7b-117">[Transmit DV from File to Tape](transmit-dv-from-file-to-tape.md).</span></span>

<span data-ttu-id="e1f7b-118">Para determinar qué controlador se está usando, llame a [**IAMExtDevice:: get \_ DevicePort**](/windows/desktop/api/Strmif/nf-strmif-iamextdevice-get_deviceport).</span><span class="sxs-lookup"><span data-stu-id="e1f7b-118">To determine which driver is being used, call [**IAMExtDevice::get\_DevicePort**](/windows/desktop/api/Strmif/nf-strmif-iamextdevice-get_deviceport).</span></span> <span data-ttu-id="e1f7b-119">El controlador MSDV devuelve la marca del puerto de desarrollo \_ \_ 1394 y el controlador UVC devuelve la \_ marca USB del puerto de desarrollo \_ .</span><span class="sxs-lookup"><span data-stu-id="e1f7b-119">The MSDV driver returns the DEV\_PORT\_1394 flag, and the UVC driver returns the DEV\_PORT\_USB flag.</span></span>

<span data-ttu-id="e1f7b-120">**Nodos de dispositivo**</span><span class="sxs-lookup"><span data-stu-id="e1f7b-120">**Device Nodes**</span></span>

<span data-ttu-id="e1f7b-121">En la terminología USB, los puntos de conexión son los puntos en los que los datos entran o salen del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e1f7b-121">In USB terminology, endpoints are the points where data enters or leaves the device.</span></span> <span data-ttu-id="e1f7b-122">Un punto de conexión tiene una dirección de flujo de datos, ya sea de entrada (desde el dispositivo al host) o de salida (desde el host al dispositivo).</span><span class="sxs-lookup"><span data-stu-id="e1f7b-122">An endpoint has a direction of data flow, either input (from device to host) or output (from host to device).</span></span> <span data-ttu-id="e1f7b-123">Puede ser útil pensar en estas instrucciones como en relación con el host.</span><span class="sxs-lookup"><span data-stu-id="e1f7b-123">It may help to think of these directions as being relative to the host.</span></span> <span data-ttu-id="e1f7b-124">La entrada va al host; la salida procede del host.</span><span class="sxs-lookup"><span data-stu-id="e1f7b-124">Input goes to the host; output comes from the host.</span></span> <span data-ttu-id="e1f7b-125">En el siguiente diagrama se ilustran los dos extremos.</span><span class="sxs-lookup"><span data-stu-id="e1f7b-125">The following diagram illustrates the two endpoints.</span></span>

![extremos USB](images/ksnodes01.png)

<span data-ttu-id="e1f7b-127">En un dispositivo UVC, las funciones del dispositivo se dividen lógicamente en componentes denominados unidades y terminales.</span><span class="sxs-lookup"><span data-stu-id="e1f7b-127">In a UVC device, the functions of the device are logically divided into components called units and terminals.</span></span> <span data-ttu-id="e1f7b-128">Una unidad recibe uno o más flujos de datos como entrada y entrega exactamente un flujo como salida.</span><span class="sxs-lookup"><span data-stu-id="e1f7b-128">A unit receives one or more data streams as input and delivers exactly one stream as output.</span></span> <span data-ttu-id="e1f7b-129">Un terminal es el punto inicial o final de un flujo de datos.</span><span class="sxs-lookup"><span data-stu-id="e1f7b-129">A terminal is the starting point or ending point for a data stream.</span></span> <span data-ttu-id="e1f7b-130">Los puntos de conexión USB se corresponden con los terminales, pero las direcciones se invierten: un extremo de entrada se representa mediante un terminal de salida y viceversa.</span><span class="sxs-lookup"><span data-stu-id="e1f7b-130">USB endpoints correspond to terminals, but the directions are reversed: an input endpoint is represented by an output terminal, and vice versa.</span></span> <span data-ttu-id="e1f7b-131">En el diagrama siguiente se muestra la relación entre los terminales y los extremos.</span><span class="sxs-lookup"><span data-stu-id="e1f7b-131">The following diagram shows the relation between terminals and endpoints.</span></span>

![unidades de UVC y terminales](images/ksnodes02.png)

<span data-ttu-id="e1f7b-133">Además, no todos los terminales corresponden a un punto de conexión USB.</span><span class="sxs-lookup"><span data-stu-id="e1f7b-133">Also, not every terminal corresponds to a USB endpoint.</span></span> <span data-ttu-id="e1f7b-134">El término punto de conexión hace referencia específicamente a las conexiones USB y un dispositivo puede enviar o recibir datos a través de conexiones no USB.</span><span class="sxs-lookup"><span data-stu-id="e1f7b-134">The term endpoint refers specifically to USB connections, and a device may send or receive data through non-USB connections.</span></span> <span data-ttu-id="e1f7b-135">Por ejemplo, una cámara de vídeo es un terminal de entrada y una pantalla LCD es un terminal de salida.</span><span class="sxs-lookup"><span data-stu-id="e1f7b-135">For example, a video camera is an input terminal and an LCD screen is an output terminal.</span></span>

<span data-ttu-id="e1f7b-136">En el filtro de proxy de KS, las unidades y los terminales se representan como nodos dentro del filtro.</span><span class="sxs-lookup"><span data-stu-id="e1f7b-136">In the KS Proxy filter, units and terminals are represented as nodes inside the filter.</span></span> <span data-ttu-id="e1f7b-137">El término nodo es más general que los términos unidad y terminal, ya que los dispositivos que no son USB también pueden tener nodos.</span><span class="sxs-lookup"><span data-stu-id="e1f7b-137">The term node is more general than the terms unit and terminal because non-USB devices can also have nodes.</span></span> <span data-ttu-id="e1f7b-138">Para obtener información sobre los nodos de un filtro, consulte el filtro de la interfaz [**IKsTopologyInfo**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-ikstopologyinfo) .</span><span class="sxs-lookup"><span data-stu-id="e1f7b-138">To get information about the nodes in a filter, query the filter for the [**IKsTopologyInfo**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-ikstopologyinfo) interface.</span></span> <span data-ttu-id="e1f7b-139">Los tipos de nodo se identifican mediante GUID.</span><span class="sxs-lookup"><span data-stu-id="e1f7b-139">Node types are identified by GUIDs.</span></span> <span data-ttu-id="e1f7b-140">Los nodos de selector son nodos que pueden alternar entre dos o más entradas.</span><span class="sxs-lookup"><span data-stu-id="e1f7b-140">Selector nodes are nodes that can switch between two or more inputs.</span></span> <span data-ttu-id="e1f7b-141">Los nodos de selector exponen la interfaz [**ISelector**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-iselector) .</span><span class="sxs-lookup"><span data-stu-id="e1f7b-141">Selector nodes expose the [**ISelector**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-iselector) interface.</span></span>

<span data-ttu-id="e1f7b-142">El código siguiente comprueba si un PIN de salida de un filtro recibe la entrada de un nodo de un tipo determinado.</span><span class="sxs-lookup"><span data-stu-id="e1f7b-142">The following code tests whether an output pin on a filter receives input from a node of a given type.</span></span>


```C++
// Structure to hold topology information.
struct TopologyConnections
{
    KSTOPOLOGY_CONNECTION *connections; // Array of connections
    DWORD count;  // Number of elements in the array
};

/////////////////////////////////////////////////////////////////////
// Name: GetTopologyConnections
// Desc: Gets the topology information from a filter.
//
// pTopo:       Pointer to the filter's IKsTopologyInfo interface.
// connectInfo: Pointer to a TopologyConnections structure. The 
//              function fills in this structure.
//
// Note: If the function succeeds, call CoTaskMemFree to free the
//       pConnectInfo->connections array.
/////////////////////////////////////////////////////////////////////

HRESULT GetTopologyConnections(
    IKsTopologyInfo *pTopo, 
    TopologyConnections *pConnectInfo
    )
{
    DWORD count;
    HRESULT hr = pTopo->get_NumConnections(&count);
    if (FAILED(hr))
    {
        return hr;
    }

    pConnectInfo->count = count;
    pConnectInfo->connections = NULL;
    if (count > 0)
    {
        // Allocate an array for the connection information.
        SIZE_T cb = sizeof(KSTOPOLOGY_CONNECTION) * count;
        KSTOPOLOGY_CONNECTION *pConnections = 
            (KSTOPOLOGY_CONNECTION*) CoTaskMemAlloc(cb);
        if (pConnections == NULL)
        {
            return E_OUTOFMEMORY;
        }
        // Fill the array.
        for (DWORD ix = 0; ix < count; ix++)
        {
            hr = pTopo->get_ConnectionInfo(ix, &pConnections[ix]);
            if (FAILED(hr))
            {
                break;
            }
        }
        if (SUCCEEDED(hr))
        {
            pConnectInfo->connections = pConnections;
        }
        else
        {
           CoTaskMemFree(pConnections);
        }
    }
    return hr;
}

/////////////////////////////////////////////////////////////////////
// Name: IsNodeDownstreamFromNode
// Desc: Searches upstream from a node for a specified node type.
//
// pTopo:        Pointer to the filter's IKsTopologyInfo interface.
// connectInfo:  Contains toplogy information. To fill in this
//               structure, call GetTopologyConnections.
// nodeID:       ID of the starting node in the search.
// nodeType:     Type of node to find.
// pIsConnected: Receives true if connected, or false otherwise.
//
// Note: If the source node matches the type, this function returns 
//       true without searching upstream.
/////////////////////////////////////////////////////////////////////

HRESULT IsNodeDownstreamFromNode(
    IKsTopologyInfo *pTopo,
    const TopologyConnections& connectInfo, 
    DWORD nodeID,
    const GUID& nodeType,
    bool *pIsConnected
    )
{
    *pIsConnected = false;
    // Base case for recursion: check the source node.
    GUID type;
    HRESULT hr = pTopo->get_NodeType(nodeID, &type);
    if (FAILED(hr))
    {
        return hr;
    }
    if (type == nodeType)
    {
        *pIsConnected = true;
        return S_OK;
    }

    // If the source node is a selector, get the input node.
    CComPtr<ISelector> pSelector;
    hr = pTopo->CreateNodeInstance(nodeID, __uuidof(ISelector), 
        (void**)&pSelector);
    if (SUCCEEDED(hr))
    {
        DWORD sourceNodeID;
        hr = pSelector->get_SourceNodeId(&sourceNodeID);
        if (SUCCEEDED(hr))
        {
            // Recursive call with the selector's input node.
            return IsNodeDownstreamFromNode(pTopo, connectInfo, 
                       sourceNodeID, nodeType, pIsConnected);
        }
    }
    else if (hr == E_NOINTERFACE)
    {
        hr = S_OK;  // This node is not a selector. Not a failure.
    }
    else
    {
        return hr;
    }

    // Test all of the upstream connections on this pin. 
    for (DWORD ix = 0; ix < connectInfo.count; ix++)
    {
        if ((connectInfo.connections[ix].ToNode == nodeID) &&
            (connectInfo.connections[ix].FromNode != KSFILTER_NODE))
        {
            // FromNode is connected to the source node.
            DWORD fromNode = connectInfo.connections[ix].FromNode;

            // Recursive call with the upstream node.
            bool bIsConnected;
            hr = IsNodeDownstreamFromNode(pTopo, connectInfo, 
                fromNode, nodeType, &bIsConnected);
            if (FAILED(hr))
            {
                break;
            }
            if (bIsConnected)
            {
                *pIsConnected = true;
                break;
            }
        }
    }
    return hr;
}


/////////////////////////////////////////////////////////////////////
// Name: GetNodeUpstreamFromPin
// Desc: Finds the node connected to an output pin.
//
// connectInfo: Contains toplogy information. To fill in this
//              structure, call GetTopologyConnections.
// nPinIndex:   Index of the output pin.
// pNodeID:     Receives the ID of the connected node.
/////////////////////////////////////////////////////////////////////

HRESULT GetNodeUpstreamFromPin(
    const TopologyConnections& connectInfo, 
    UINT nPinIndex, 
    DWORD *pNodeID
    )
{
    bool bFound = false;
    for (DWORD ix = 0; ix < connectInfo.count; ix++)
    {
        if ((connectInfo.connections[ix].ToNode == KSFILTER_NODE) &&
            (connectInfo.connections[ix].ToNodePin == nPinIndex))
        {
            *pNodeID = connectInfo.connections[ix].FromNode;
            bFound = true;
            break;
        }
    }
    if (bFound)
    {
        return S_OK;
    }
    else
    {
        return E_FAIL;
    }
}


/////////////////////////////////////////////////////////////////////
// Name: IsPinDownstreamFromNode
// Desc: Tests whether an output pin gets data from a node of
//       a specified type.
// 
// pFilter:      Pointer to the filter's IBaseFilter interface.
// UINT:         Index of the output pin to test.
// nodeType:     Type of node to find.
// pIsConnected: Receives true if connected; false otherwise.
/////////////////////////////////////////////////////////////////////

HRESULT IsPinDownstreamFromNode(
    IBaseFilter *pFilter, 
    UINT nPinIndex, 
    const GUID& nodeType,
    bool *pIsConnected
    )
{
    CComQIPtr<IKsTopologyInfo> pTopo(pFilter);
    if (pTopo == NULL)
    {
        return E_NOINTERFACE;
    }

    // Get the topology connection information.
    TopologyConnections connectionInfo;
    HRESULT hr = GetTopologyConnections(pTopo, &connectionInfo);
    if (FAILED(hr))
    {
        return hr;
    }

    // Find the node upstream from this pin.
    DWORD nodeID;
    hr = GetNodeUpstreamFromPin(connectionInfo, nPinIndex, &nodeID);
    if (SUCCEEDED(hr))
    {
        bool isConnected;
        hr = IsNodeDownstreamFromNode(pTopo, connectionInfo, 
            nodeID, nodeType, &isConnected);
        if (SUCCEEDED(hr))
        {
            *pIsConnected = isConnected;
        }
    }
    CoTaskMemFree(connectionInfo.connections);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="e1f7b-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e1f7b-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1f7b-144">Vídeo digital en DirectShow</span><span class="sxs-lookup"><span data-stu-id="e1f7b-144">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



