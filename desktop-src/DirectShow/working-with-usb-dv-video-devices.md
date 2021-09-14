---
description: Trabajar con dispositivos de vídeo DV USB
ms.assetid: 6244f006-db9f-42b2-81cd-26eba583613e
title: Trabajar con dispositivos de vídeo DV USB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75647aa7b53bac45c155b4e0a9283418c9af58b7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061589"
---
# <a name="working-with-usb-dv-video-devices"></a>Trabajar con dispositivos de vídeo DV USB

En este tema se describe cómo escribir aplicaciones para dispositivos de vídeo de Bus serie universal (USB) que capturan vídeo DV.

El formato DV estándar tiene una velocidad de datos de aproximadamente 25 megabits por segundo (Mbps). Cuando se introdujo USB por primera vez, no tenía suficiente ancho de banda para admitir vídeo DV. Sin embargo, USB 2.0 puede admitir hasta 480 Mbps, lo que es más que suficiente para el vídeo DV. La especificación USB Video Device Class (UVC), publicada en 2003, define el formato de carga para dispositivos de vídeo DV USB. En Windows XP Service Pack 2 se introdujo un controlador de clase del modelo de controlador de Windows (WDM) para dispositivos UV Windows C.

En la mayoría de los aspectos, el controlador UVC admite el mismo modelo de programación que el controlador MSDV para IEEE 1394 dispositivos. Las aplicaciones escritas para MSDV solo deben requerir modificaciones menores para admitir dispositivos UVC.

El controlador UVC se comporta de forma diferente al controlador MSDV en las áreas siguientes:

-   [Modo de dispositivo](device-mode.md)
-   [Formato de secuencia](stream-format.md)
-   [Formato de señal](signal-format.md)
-   [Búsqueda de ubicación de cinta](tape-location-search.md)
-   [Transmitir DV de archivo a cinta.](transmit-dv-from-file-to-tape.md)

Para determinar qué controlador se usa, llame a [**IAMExtDevice::get \_ DevicePort**](/windows/desktop/api/Strmif/nf-strmif-iamextdevice-get_deviceport). El controlador MSDV devuelve la marca DEV \_ PORT 1394 y el controlador UVC devuelve la marca \_ USB DEL PUERTO \_ \_ DEV.

**Nodos de dispositivo**

En la terminología USB, los puntos de conexión son los puntos donde los datos entran o abandonan el dispositivo. Un punto de conexión tiene una dirección de flujo de datos, ya sea de entrada (de dispositivo a host) o de salida (de host a dispositivo). Puede resultar de ayuda pensar en estas direcciones como relativas al host. La entrada va al host; la salida procede del host. En el diagrama siguiente se muestran los dos puntos de conexión.

![puntos de conexión USB](images/ksnodes01.png)

En un dispositivo UVC, las funciones del dispositivo se dividen lógicamente en componentes denominados unidades y terminales. Una unidad recibe uno o varios flujos de datos como entrada y entrega exactamente una secuencia como salida. Un terminal es el punto inicial o final de un flujo de datos. Los puntos de conexión USB corresponden a terminales, pero las direcciones se invierten: un punto de conexión de entrada se representa mediante un terminal de salida y viceversa. En el diagrama siguiente se muestra la relación entre terminales y puntos de conexión.

![unidades uvc y terminales](images/ksnodes02.png)

Además, no todos los terminales corresponden a un punto de conexión USB. El término punto de conexión hace referencia específicamente a las conexiones USB y un dispositivo puede enviar o recibir datos a través de conexiones no USB. Por ejemplo, una cámara de vídeo es un terminal de entrada y una pantalla DE TECLADO es un terminal de salida.

En el filtro de proxy KS, las unidades y los terminales se representan como nodos dentro del filtro. El término nodo es más general que los términos unidad y terminal, ya que los dispositivos que no son USB también pueden tener nodos. Para obtener información sobre los nodos de un filtro, consulte el filtro para la [**interfaz IKsTopologyInfo.**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-ikstopologyinfo) Los tipos de nodo se identifican mediante GUID. Los nodos selectores son nodos que pueden cambiar entre dos o más entradas. Los nodos selectores exponen [**la interfaz ISelector.**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-iselector)

El código siguiente comprueba si un pin de salida de un filtro recibe la entrada de un nodo de un tipo determinado.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Vídeo digital en DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



