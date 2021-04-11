---
description: Crear instancias del códec MFTs
ms.assetid: 171f9a0f-effb-4ed7-8aff-d7b1ee6e4973
title: Crear instancias del códec MFTs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aa886f24f7dbd1acc373c7e505baddf71bc3aa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275501"
---
# <a name="instantiating-codec-mfts"></a>Crear instancias del códec MFTs

[Media Foundation transformaciones](media-foundation-transforms.md) (MFTs) son objetos com que implementan la interfaz [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) . Una MFT es un objeto para transformar los datos multimedia como parte de una canalización. Una canalización es un gráfico acíclicos dirigido, compuesto por orígenes multimedia, transformaciones multimedia y receptores multimedia. Una canalización procesa los datos multimedia de streaming de forma asincrónica.

Aunque se puede crear una instancia de MFTs y usar independientemente de la infraestructura de canalización Media Foundation, es preferible usar el marco de MediaFoundation siempre que sea posible.

Puede crear un MFT de códec mediante una llamada a la función [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) . Debe pasar el identificador de clase de MFT, el identificador de interfaz de [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)y un puntero a un puntero **IMFTransform** .

Los identificadores de clase del códec MFTs se definen como constantes en el archivo de encabezado wmcodecdsp. h.

La constante para el identificador de la interfaz [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) es IID \_ IMFTransform.

En el ejemplo de código siguiente se muestra cómo crear una instancia de un MFT de códec:


```
HRESULT CreateVideoEncoderMFT(IMFTransform** ppMFT)
{
    if (ppMFT == NULL)
        return E_POINTER;

    return CoCreateInstance(CLSID_CWMV9EncMediaObject,
                            NULL,
                            CLSCTX_INPROC_SERVER, 
                            IID_IMFTransform, 
                            (void**)ppMFT);
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con códec MFTs](workingwithcodecmfts.md)
</dt> </dl>

 

 
