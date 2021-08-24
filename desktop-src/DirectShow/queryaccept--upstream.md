---
description: QueryAccept (upstream)
ms.assetid: 3153e3a4-2227-4fdd-b2b0-218763013d2d
title: QueryAccept (upstream)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65133e132a0e1c2e6880009eda8b56fde9bf77a8bc7d68a850a6f8963604aecd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747585"
---
# <a name="queryaccept-upstream"></a>QueryAccept (upstream)

Este mecanismo permite que un pin de entrada proponga un cambio de formato a su par ascendente. El filtro de bajada debe adjuntar un tipo de medio al ejemplo que obtendrá el filtro ascendente en la siguiente llamada a [**IMemAllocator::GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer). Para ello, sin embargo, el filtro de nivel inferior debe proporcionar un asignador personalizado para la conexión. Este asignador debe implementar un método privado que el filtro de nivel inferior puede usar para establecer el tipo de medio en el ejemplo siguiente.

Tienen lugar los pasos siguientes:

1.  El filtro de bajada comprueba si la conexión de pin usa el asignador personalizado del filtro. Si el filtro ascendente posee el asignador, el filtro de nivel inferior no puede cambiar el formato.
2.  El filtro de nivel inferior llama [**a IPin::QueryAccept en**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) el pin de salida ascendente (consulte la ilustración, paso A).
3.  Si devuelve S OK, el filtro de bajada llama al método privado en su `QueryAccept` \_ asignador para establecer el tipo de medio. Dentro de este método privado, el asignador llama [**a IMediaSample::SetMediaType en**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatype) el siguiente ejemplo disponible (B).
4.  El filtro ascendente llama a **GetBuffer** para obtener un nuevo ejemplo (C) e [**IMediaSample::GetMediaType para**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) obtener el tipo de medio (D).
5.  Cuando el filtro ascendente entrega la muestra, debe dejar el tipo de medio asociado a esa muestra. De este modo, el filtro de nivel inferior puede confirmar que el tipo de medio ha cambiado (E).

Si el filtro ascendente acepta el cambio de formato, también debe poder volver al tipo de medio original, como se muestra en el diagrama siguiente.

![queryaccept (ascendente)](images/dynformat4.png)

Los ejemplos principales de este tipo de cambio de formato implican a DirectShow representadores de vídeo.

-   El filtro [de representador de](video-renderer-filter.md) vídeo original puede cambiar entre los tipos RGB y YUV durante el streaming. Cuando se conecta el filtro, requiere un formato RGB que coincida con la configuración de presentación actual. Esto garantiza que puede volver a usar GDI si es necesario. Una vez que comienza el streaming, si DirectDraw está disponible, el representador de vídeo solicita un cambio de formato a un tipo YUV. Más adelante, podría volver a RGB si pierde la superficie de DirectDraw por cualquier motivo.
-   El filtro de representador de mezcla de vídeo (VMR) más reciente se conectará con cualquier formato que sea compatible con el hardware gráfico, incluidos los tipos YUV. Sin embargo, el hardware gráfico podría cambiar el paso de la superficie subyacente de DirectDraw para optimizar el rendimiento. El filtro VMR usa para notificar el nuevo intervalo, que se especifica en el `QueryAccept` **miembro biWidth** de la **estructura BITMAPINFOHEADER.** Los rectángulos de origen y destino de la **estructura VIDEOINFOHEADER** o **VIDEOINFOHEADER2** identifican la región donde se debe descodificar el vídeo.

**Nota de implementación**

Es poco probable que escriba un filtro que necesite solicitar cambios de formato ascendentes, ya que se trata principalmente de una característica de representadores de vídeo. Sin embargo, si escribe un filtro de transformación de vídeo o un descodificador de vídeo, el filtro debe responder correctamente a las solicitudes del representador de vídeo.

Un filtro trans-in-place que se encuentra entre el representador de vídeo y el descodificador debe pasar todas las `QueryAccept` llamadas ascendentes. Almacene la nueva información de formato cuando llegue.

Un filtro de transformación de copia (es decir, un filtro no trans-in-place) debe implementar uno de los comportamientos siguientes:

-   Pase los cambios de formato ascendentes y almacene la nueva información de formato cuando llegue. El filtro debe usar un asignador personalizado para que pueda adjuntar el formato al ejemplo ascendente.
-   Realice la conversión de formato dentro del filtro. Esto probablemente sea más fácil que pasar el cambio de formato ascendente. Sin embargo, podría ser menos eficaz que dejar que el filtro descodificador descodificase en el formato correcto.
-   Como último recurso, simplemente rechace el cambio de formato. (Para obtener más información, consulte el código fuente del método [**CTransInPlaceOutputPin::CheckMediaType**](ctransinplaceoutputpin-checkmediatype.md) en la biblioteca DirectShow de clases base). Sin embargo, rechazar un cambio de formato puede reducir el rendimiento, ya que impide que el representador de vídeo use el formato más eficaz.

El siguiente pseudocódigo muestra cómo podría implementar un filtro de copia y transformación (derivado de **CTransformFilter)** que puede cambiar entre los tipos de salida YUV y RGB. En este ejemplo se supone que el filtro realiza la propia conversión, en lugar de pasar el cambio de formato ascendente.


```C++
HRESULT CMyTransform::CheckInputType(const CMediaType *pmt)
{
    if (pmt is a YUV type that you support) {
        return S_OK;
    }
    else {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }
}

HRESULT CMyTransform::CheckTransform(
    const CMediaType *mtIn, const CMediaType *mtOut)
{
    if (mtOut is a YUV or RGB type that you support)
    {
        if ((mtIn has the same video dimensions as mtOut) &&
            (you support the mtIn-to-mtOut transform))
        {
            return S_OK;
        }
    }
    // otherwise
    return VFW_E_TYPE_NOT_ACCEPTED;
}

// GetMediaType: Return a preferred output type.
HRESULT CMyTransform::GetMediaType(int iPosition, CMediaType *pMediaType)
{
    if (iPosition < 0) {
        return E_INVALIDARG;
    }
    switch (iPosition)
    {
    case 0:
        Copy the input type (YUV) to pMediaType
        return S_OK;
    case 1:
        Construct an RGB type that matches the input type.
        return S_OK;
    default:
        return VFW_S_NO_MORE_ITEMS;
    }
}

// SetMediaType: Override from CTransformFilter. 
HRESULT CMyTransform::SetMediaType(
    PIN_DIRECTION direction, const CMediaType *pmt)
{
    // Capture this information...
    if (direction == PINDIR_OUTPUT)
    {
       m_bYuv = (pmt->subtype == MEDIASUBTYPE_UYVY);
    }
    return S_OK;
}

HRESULT CMyTransform::Transform(
    IMediaSample *pSource, IMediaSample *pDest)
{
    // Look for format changes from downstream.
    CMediaType *pMT = NULL;
    HRESULT hr = pDest->GetMediaType((AM_MEDIA_TYPE**)&pMT);
    if (hr == S_OK)
    {
        hr = m_pOutput->CheckMediaType(pMT);
        if(FAILED(hr))
        {
            DeleteMediaType(pMT);
            return E_FAIL;
        }
        // Notify our own output pin about the new type.
        m_pOutput->SetMediaType(pMT);
        DeleteMediaType(pMT);
    }
    // Process the buffers
    if (m_bYuv) {
        return ProcessFrameYUV(pSource, pDest);
    }
    else {
        return ProcessFrameRGB(pSource, pDest);
    }
}
```



 

 



