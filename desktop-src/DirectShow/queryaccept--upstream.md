---
description: QueryAccept (ascendente)
ms.assetid: 3153e3a4-2227-4fdd-b2b0-218763013d2d
title: QueryAccept (ascendente)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7707c52d36c3d065c4a7277939f724aabdb73e46
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806470"
---
# <a name="queryaccept-upstream"></a>QueryAccept (ascendente)

Este mecanismo permite a un PIN de entrada proponer un cambio de formato a su elemento del mismo nivel de nivel superior. El filtro de nivel inferior debe asociar un tipo de medio al ejemplo que el filtro ascendente obtendrá en la siguiente llamada a [**IMemAllocator:: getBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer). Para ello, sin embargo, el filtro de nivel inferior debe proporcionar un asignador personalizado para la conexión. Este asignador debe implementar un método privado que el filtro de nivel inferior pueda utilizar para establecer el tipo de medio en el ejemplo siguiente.

Tienen lugar los pasos siguientes:

1.  El filtro de nivel inferior comprueba si la conexión del PIN utiliza el asignador personalizado del filtro. Si el filtro de nivel superior posee el asignador, el filtro de nivel inferior no puede cambiar el formato.
2.  El filtro de nivel inferior llama a [**IPin:: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) en el PIN de salida ascendente (vea la ilustración, paso A).
3.  Si `QueryAccept` devuelve S \_ OK, el filtro de nivel inferior llama al método privado en su asignador para establecer el tipo de medio. Dentro de este método privado, el asignador llama a [**IMediaSample:: SetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatype) en el siguiente ejemplo disponible (B).
4.  El filtro de nivel superior llama a **getBuffer** para obtener un nuevo ejemplo (C) y [**IMediaSample:: GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) para obtener el tipo de medio (D).
5.  Cuando el filtro de nivel superior entrega el ejemplo, debe dejar el tipo de medio asociado a ese ejemplo. De este modo, el filtro de nivel inferior puede confirmar que el tipo de medio ha cambiado (E).

Si el filtro de nivel superior acepta el cambio de formato, también debe poder volver al tipo de medio original, como se muestra en el diagrama siguiente.

![queryaccept (ascendente)](images/dynformat4.png)

Los principales ejemplos de este tipo de cambio de formato implican los representadores de vídeo de DirectShow.

-   El filtro de [representador de vídeo](video-renderer-filter.md) original puede cambiar entre los tipos RGB y YUV durante el streaming. Cuando el filtro se conecta, requiere un formato RGB que coincida con la configuración de pantalla actual. Esto garantiza que puede revertirse en GDI si es necesario. Una vez que se inicia el streaming, si DirectDraw está disponible, el representador de vídeo solicita un cambio de formato a un tipo YUV. Más adelante, podría volver a RGB si pierde la superficie DirectDraw por cualquier motivo.
-   El filtro de representador de mezcla de vídeo (VMR) más reciente se conectará con cualquier formato compatible con el hardware gráfico, incluidos los tipos YUV. Sin embargo, el hardware gráfico podría cambiar el intervalo de la superficie de DirectDraw subyacente para optimizar el rendimiento. El filtro VMR utiliza `QueryAccept` para notificar el nuevo STRIDE, que se especifica en el miembro **biwidth** de la estructura **BITMAPINFOHEADER** . Los rectángulos de origen y de destino de la estructura **VIDEOINFOHEADER** o **VIDEOINFOHEADER2** identifican la región en la que se debe descodificar el vídeo.

**Nota de implementación**

Es poco probable que escriba un filtro que necesite solicitar cambios en el formato ascendente, ya que se trata principalmente de una característica de los representadores de vídeo. Sin embargo, si escribe un filtro de transformación de vídeo o un descodificador de vídeo, el filtro debe responder correctamente a las solicitudes del representador de vídeo.

Un filtro de transacciones que se encuentra entre el representador de vídeo y el descodificador debe pasar todas las `QueryAccept` llamadas de nivel superior. Almacene la nueva información de formato cuando llegue.

Un filtro de copia y transformación (es decir, un filtro que no es trans-in situ) debe implementar uno de los siguientes comportamientos:

-   Los cambios de formato de paso ascendente y almacenan la nueva información de formato cuando llega. El filtro debe utilizar un asignador personalizado para que pueda adjuntar el formato al ejemplo de nivel superior.
-   Realice la conversión de formato dentro del filtro. Esto es probablemente más fácil que pasar el cambio de formato de nivel superior. Sin embargo, puede ser menos eficaz que dejar que el filtro del descodificador se descodifique en el formato correcto.
-   Como último recurso, simplemente rechace el cambio de formato. (Para obtener más información, consulte el código fuente para el método [**CTransInPlaceOutputPin:: CheckMediaType**](ctransinplaceoutputpin-checkmediatype.md) en la biblioteca de clases base de DirectShow). Sin embargo, el rechazo de un cambio de formato puede reducir el rendimiento, ya que impide que el representador de vídeo use el formato más eficaz.

En el siguiente pseudocódigo se muestra cómo podría implementar un filtro de copia y transformación (derivado de **CTransformFilter**) que puede cambiar entre los tipos de salida YUV y RGB. En este ejemplo se da por supuesto que el filtro realiza la conversión en sí mismo, en lugar de pasar el cambio de formato de nivel superior.


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



 

 



