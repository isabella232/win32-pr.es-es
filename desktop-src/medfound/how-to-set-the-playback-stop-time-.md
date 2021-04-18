---
description: En este tema se describe cómo establecer una hora de detención para la reproducción cuando se usa la sesión multimedia.
ms.assetid: B8BA2154-2824-4573-AE71-853EB8AB911D
title: Cómo establecer la hora de detención de la reproducción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65269260b1e40d7907f0233fad653deb9636848b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705844"
---
# <a name="how-to-set-the-playback-stop-time"></a><span data-ttu-id="f4fc7-103">Cómo establecer la hora de detención de la reproducción</span><span class="sxs-lookup"><span data-stu-id="f4fc7-103">How to Set the Playback Stop Time</span></span>

<span data-ttu-id="f4fc7-104">En este tema se describe cómo establecer una hora de detención para la reproducción cuando se usa la [sesión multimedia](media-session.md).</span><span class="sxs-lookup"><span data-stu-id="f4fc7-104">This topic describes how to set a stop time for playback when using the [Media Session](media-session.md).</span></span>

## <a name="setting-the-stop-time-before-playback-begins"></a><span data-ttu-id="f4fc7-105">Establecer la hora de detención antes de comenzar la reproducción</span><span class="sxs-lookup"><span data-stu-id="f4fc7-105">Setting the Stop Time Before Playback Begins</span></span>

<span data-ttu-id="f4fc7-106">Antes de poner en cola una topología para la reproducción, puede especificar la hora de detención mediante el atributo [MF \_ TOPONODE \_ MEDIASTOP](mf-toponode-mediastop-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="f4fc7-106">Before you queue a topology for playback, you can specify the stop time by using the [MF\_TOPONODE\_MEDIASTOP](mf-toponode-mediastop-attribute.md) attribute.</span></span> <span data-ttu-id="f4fc7-107">Para cada nodo de salida en la topología, establezca el valor de MF \_ TOPONODE \_ MEDIASTOP en la hora de detención en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="f4fc7-107">For each output node in the topology, set the value of the MF\_TOPONODE\_MEDIASTOP to the stop time in 100-nanosecond units.</span></span>

<span data-ttu-id="f4fc7-108">Tenga en cuenta que establecer este atributo después de que se inicie la reproducción no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="f4fc7-108">Note that setting this attribute after playback starts has no effect.</span></span> <span data-ttu-id="f4fc7-109">Por lo tanto, establezca el atributo antes de llamar a [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span><span class="sxs-lookup"><span data-stu-id="f4fc7-109">Therefore, set the attribute before calling [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span></span>

<span data-ttu-id="f4fc7-110">El código siguiente muestra cómo establecer la hora de detención en una topología existente.</span><span class="sxs-lookup"><span data-stu-id="f4fc7-110">The following code shows how to set the stop time on an existing topology.</span></span>


```C++
template <class Q>
HRESULT GetCollectionObject(IMFCollection *pCollection, DWORD dwIndex, Q **ppObject)
{
    *ppObject = NULL;   // zero output

    IUnknown *pUnk = NULL;
    HRESULT hr = pCollection->GetElement(dwIndex, &pUnk);
    if (SUCCEEDED(hr))
    {
        hr = pUnk->QueryInterface(IID_PPV_ARGS(ppObject));
        pUnk->Release();
    }
    return hr;
}

HRESULT SetMediaStop(IMFTopology *pTopology, const LONGLONG& stop)
{
    IMFCollection *pCol = NULL;
    DWORD cNodes;

    HRESULT hr = pTopology->GetSourceNodeCollection(&pCol);
    if (SUCCEEDED(hr))
    {
        hr = pCol->GetElementCount(&cNodes);
    }
    if (SUCCEEDED(hr))
    {
        for (DWORD i = 0; i < cNodes; i++)
        {
            IMFTopologyNode *pNode;
            hr = GetCollectionObject(pCol, i, &pNode);
            if (SUCCEEDED(hr))
            {
                pNode->SetUINT64(MF_TOPONODE_MEDIASTOP, stop);
            }
            pNode->Release();
        }
    }
    SafeRelease(&pCol);
    return hr;
}
```



## <a name="setting-the-stop-time-after-playback-has-started"></a><span data-ttu-id="f4fc7-111">Establecer la hora de detención después de que se haya iniciado la reproducción</span><span class="sxs-lookup"><span data-stu-id="f4fc7-111">Setting the Stop Time After Playback Has Started</span></span>

<span data-ttu-id="f4fc7-112">Hay una manera de establecer la hora de detención después de que la [sesión multimedia](media-session.md) inicie la reproducción, mediante la interfaz [**IMFTopologyNodeAttributeEditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor) .</span><span class="sxs-lookup"><span data-stu-id="f4fc7-112">There is a way to set the stop time after the [Media Session](media-session.md) starts playback, by using the [**IMFTopologyNodeAttributeEditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor) interface.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f4fc7-113">Esta interfaz tiene una limitación seria, porque la hora de detención se especifica como un valor de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="f4fc7-113">This interface has a serious limitation, because the stop time is specified as a 32-bit value.</span></span> <span data-ttu-id="f4fc7-114">Esto significa que el tiempo de detención máximo que se puede establecer mediante esta interfaz es 0xFFFFFFFF o solo durante 7 minutos.</span><span class="sxs-lookup"><span data-stu-id="f4fc7-114">That means the maximum stop time that you can set using this interface is 0xFFFFFFFF, or just over 7 minutes.</span></span> <span data-ttu-id="f4fc7-115">Esta limitación se debe a una definición de estructura incorrecta.</span><span class="sxs-lookup"><span data-stu-id="f4fc7-115">This limitation is due to an incorrect structure definition.</span></span>

 

<span data-ttu-id="f4fc7-116">Para establecer la hora de detención mediante la interfaz [**IMFTopologyNodeAttributeEditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor) , realice los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="f4fc7-116">To set the stop time using the [**IMFTopologyNodeAttributeEditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor) interface, perform the following steps.</span></span>

1.  <span data-ttu-id="f4fc7-117">Llame a [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) para obtener la interfaz [**IMFTopologyNodeAttributeEditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor) de la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="f4fc7-117">Call [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) to get the [**IMFTopologyNodeAttributeEditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor) interface from the Media Session.</span></span>
2.  <span data-ttu-id="f4fc7-118">Llame a [**IMFTopology:: GetTopologyID**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-gettopologyid) para obtener el identificador de la topología de reproducción.</span><span class="sxs-lookup"><span data-stu-id="f4fc7-118">Call [**IMFTopology::GetTopologyID**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-gettopologyid) to get the ID of the playback topology.</span></span>
3.  <span data-ttu-id="f4fc7-119">Para cada nodo de salida en la topología, llame a [**IMFTopologyNodeAttributeEditor:: UpdateNodeAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynodeattributeeditor-updatenodeattributes).</span><span class="sxs-lookup"><span data-stu-id="f4fc7-119">For each output node in the topology, call [**IMFTopologyNodeAttributeEditor::UpdateNodeAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynodeattributeeditor-updatenodeattributes).</span></span> <span data-ttu-id="f4fc7-120">Este método toma el identificador de la topología y un puntero a una estructura de [**\_ \_ actualización del atributo MFTOPONODE**](/windows/desktop/api/mfidl/ns-mfidl-mftoponode_attribute_update) .</span><span class="sxs-lookup"><span data-stu-id="f4fc7-120">This method takes the topology ID and a pointer to a [**MFTOPONODE\_ATTRIBUTE\_UPDATE**](/windows/desktop/api/mfidl/ns-mfidl-mftoponode_attribute_update) structure.</span></span> <span data-ttu-id="f4fc7-121">Inicialice la estructura como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="f4fc7-121">Initialize the structure as follows.</span></span>

    | <span data-ttu-id="f4fc7-122">Miembro</span><span class="sxs-lookup"><span data-stu-id="f4fc7-122">Member</span></span>               | <span data-ttu-id="f4fc7-123">Valor</span><span class="sxs-lookup"><span data-stu-id="f4fc7-123">Value</span></span>                                                                                                               |
    |----------------------|---------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="f4fc7-124">**NodeId**</span><span class="sxs-lookup"><span data-stu-id="f4fc7-124">**NodeId**</span></span>           | <span data-ttu-id="f4fc7-125">Identificador del nodo.</span><span class="sxs-lookup"><span data-stu-id="f4fc7-125">The node ID.</span></span> <span data-ttu-id="f4fc7-126">Para obtener el identificador de nodo, llame a [**IMFTopologyNode:: GetTopoNodeID**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-gettoponodeid).</span><span class="sxs-lookup"><span data-stu-id="f4fc7-126">To get the node ID, call call [**IMFTopologyNode::GetTopoNodeID**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-gettoponodeid).</span></span> |
    | <span data-ttu-id="f4fc7-127">**guidAttributeKey**</span><span class="sxs-lookup"><span data-stu-id="f4fc7-127">**guidAttributeKey**</span></span> | <span data-ttu-id="f4fc7-128">**MF \_ TOPONODE \_ MEDIASTOP**</span><span class="sxs-lookup"><span data-stu-id="f4fc7-128">**MF\_TOPONODE\_MEDIASTOP**</span></span>                                                                                         |
    | <span data-ttu-id="f4fc7-129">**attrType**</span><span class="sxs-lookup"><span data-stu-id="f4fc7-129">**attrType**</span></span>         | <span data-ttu-id="f4fc7-130">**MF \_ Attribute \_ UINT64**</span><span class="sxs-lookup"><span data-stu-id="f4fc7-130">**MF\_ATTRIBUTE\_UINT64**</span></span>                                                                                           |
    | <span data-ttu-id="f4fc7-131">**u64**</span><span class="sxs-lookup"><span data-stu-id="f4fc7-131">**u64**</span></span>              | <span data-ttu-id="f4fc7-132">La hora de detención, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="f4fc7-132">The stop time, in 100-nanosecond units.</span></span>                                                                             |

    

     

<span data-ttu-id="f4fc7-133">Tenga cuidado de establecer el valor de **attrType** correctamente.</span><span class="sxs-lookup"><span data-stu-id="f4fc7-133">Be careful to set the value of **attrType** correctly.</span></span> <span data-ttu-id="f4fc7-134">Aunque **U64** es un tipo de 32 bits, el método requiere que **attrType** se establezca en **el \_ atributo \_ de MF**.</span><span class="sxs-lookup"><span data-stu-id="f4fc7-134">Although **u64** is a 32-bit type, the method requires that **attrType** be set to **MF\_ATTRIBUTE\_UINT64**.</span></span>

<span data-ttu-id="f4fc7-135">En el código siguiente se muestran estos pasos.</span><span class="sxs-lookup"><span data-stu-id="f4fc7-135">The following code shows these steps.</span></span>


```C++
HRESULT SetMediaStopDynamic(IMFMediaSession *pSession, IMFTopology *pTopology, const LONGLONG& stop)
{
    if (stop > MAXUINT32)
    {
        return E_INVALIDARG;
    }

    IMFTopologyNodeAttributeEditor *pAttr = NULL;
    IMFCollection *pCol = NULL;
    IMFTopologyNode *pNode = NULL;

    HRESULT hr = MFGetService(pSession, MF_TOPONODE_ATTRIBUTE_EDITOR_SERVICE, IID_PPV_ARGS(&pAttr));
    if (FAILED(hr))
    {
        goto done;
    }

    TOPOID id;
    hr = pTopology->GetTopologyID(&id);
    if (FAILED(hr))
    {
        goto done;
    }

    DWORD cNodes;
    hr = pTopology->GetSourceNodeCollection(&pCol);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pCol->GetElementCount(&cNodes);
    if (FAILED(hr))
    {
        goto done;
    }

    for (DWORD i = 0; i < cNodes; i++)
    {
        IMFTopologyNode *pNode;
        hr = GetCollectionObject(pCol, i, &pNode);
        if (FAILED(hr))
        {
            goto done;
        }

        TOPOID nodeID;
        hr = pNode->GetTopoNodeID(&nodeID);
        if (FAILED(hr))
        {
            goto done;
        }

        MFTOPONODE_ATTRIBUTE_UPDATE update;
        update.NodeId = nodeID;
        update.guidAttributeKey = MF_TOPONODE_MEDIASTOP;
        update.attrType = MF_ATTRIBUTE_UINT64;
        update.u64 = (UINT32)stop;

        hr = pAttr->UpdateNodeAttributes(id, 1, &update);
        if (FAILED(hr))
        {
            goto done;
        }
        SafeRelease(&pNode);
    }

done:
    SafeRelease(&pNode);
    SafeRelease(&pCol);
    SafeRelease(&pAttr);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="f4fc7-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f4fc7-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4fc7-137">Reproducción de audio y vídeo</span><span class="sxs-lookup"><span data-stu-id="f4fc7-137">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> </dl>

 

 



