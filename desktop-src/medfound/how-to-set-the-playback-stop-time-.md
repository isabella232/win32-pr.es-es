---
description: En este tema se describe cómo establecer un tiempo de detenerse para la reproducción cuando se usa la sesión multimedia.
ms.assetid: B8BA2154-2824-4573-AE71-853EB8AB911D
title: Cómo establecer el tiempo de detenerse de reproducción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08c14145f798795dfeb8116195afad2f020eb4219b9c2529f96b8fa904f2e1d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119466005"
---
# <a name="how-to-set-the-playback-stop-time"></a>Cómo establecer el tiempo de detenerse de reproducción

En este tema se describe cómo establecer un tiempo de detenerse para la reproducción cuando se usa la [sesión multimedia](media-session.md).

## <a name="setting-the-stop-time-before-playback-begins"></a>Establecimiento del tiempo de detenerse antes de que comience la reproducción

Antes de poner en cola una topología para la reproducción, puede especificar la hora de detección mediante el atributo [MF \_ TOPONODE \_ MEDIASTOP.](mf-toponode-mediastop-attribute.md) Para cada nodo de salida de la topología, establezca el valor de MF TOPONODE MEDIASTOP en el tiempo de detección en \_ \_ unidades de 100 nanosegundos.

Tenga en cuenta que establecer este atributo después de que se inicie la reproducción no tiene ningún efecto. Por lo tanto, establezca el atributo antes de llamar [**a IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).

El código siguiente muestra cómo establecer la hora de detección en una topología existente.


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



## <a name="setting-the-stop-time-after-playback-has-started"></a>Establecimiento del tiempo de detenerse después de que se haya iniciado la reproducción

Hay una manera de establecer la hora de detenerse después de que [la](media-session.md) sesión multimedia inicie la reproducción mediante la interfaz [**DETOPOLOGYNodeAttributeEditor.**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor)

> [!IMPORTANT]
> Esta interfaz tiene una limitación grave, porque el tiempo de detenerse se especifica como un valor de 32 bits. Esto significa que el tiempo máximo de detenerse que se puede establecer mediante esta interfaz es 0xFFFFFFFF o poco más de 7 minutos. Esta limitación se debe a una definición de estructura incorrecta.

 

Para establecer la hora de detenerse mediante la [**interfaz DEFTOPOLOGYNodeAttributeEditor,**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor) realice los pasos siguientes.

1.  Llame [**a MFGetService para**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) obtener la interfaz [**MFTopologyNodeAttributeEditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor) de la sesión multimedia.
2.  Llame [**a IMFTopology::GetTopologyID para**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-gettopologyid) obtener el identificador de la topología de reproducción.
3.  Para cada nodo de salida de la topología, llame [**a IMFTopologyNodeAttributeEditor::UpdateNodeAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynodeattributeeditor-updatenodeattributes). Este método toma el identificador de topología y un puntero a una [**estructura MFTOPONODE \_ ATTRIBUTE \_ UPDATE.**](/windows/desktop/api/mfidl/ns-mfidl-mftoponode_attribute_update) Inicialice la estructura como se muestra a continuación.

    | Miembro               | Valor                                                                                                               |
    |----------------------|---------------------------------------------------------------------------------------------------------------------|
    | **NodeId**           | Identificador del nodo. Para obtener el identificador de nodo, llame a [**LA LLAMADA ATOPOLOGYNode::GetTopoNodeID.**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-gettoponodeid) |
    | **guidAttributeKey** | **MF \_ TOPONODE \_ MEDIASTOP**                                                                                         |
    | **attrType**         | **ATRIBUTO \_ MF \_ UINT64**                                                                                           |
    | **u64**              | Tiempo de detenerse, en unidades de 100 nanosegundos.                                                                             |

    

     

Tenga cuidado de establecer correctamente **el valor de attrType.** Aunque **u64 es** un tipo de 32 bits, el método requiere que **attrType** se establezca en **MF ATTRIBUTE \_ \_ UINT64**.

En el código siguiente se muestran estos pasos.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Reproducción de audio y vídeo](audio-video-playback.md)
</dt> </dl>

 

 



