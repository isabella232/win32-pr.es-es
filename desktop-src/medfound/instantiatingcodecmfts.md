---
description: Creación de instancias de codec MFT
ms.assetid: 171f9a0f-effb-4ed7-8aff-d7b1ee6e4973
title: Creación de instancias de codec MFT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a73af4055aee1d5b7e6a3ea137ab2204c9e59194f57ae4776e6c8368429db877
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827615"
---
# <a name="instantiating-codec-mfts"></a>Creación de instancias de codec MFT

[Media Foundation transforms](media-foundation-transforms.md) (MFT) son objetos COM que implementan la [**interfaz MFTransform.**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) Un MFT es un objeto para transformar datos multimedia como parte de una canalización. Una canalización es un grafo acíclico dirigido que consta de orígenes multimedia, transformaciones de medios y receptores multimedia. Una canalización procesa el streaming de datos multimedia de forma asincrónica.

Aunque se pueden crear instancias de mfts y usarse independientemente de la infraestructura de canalización de Media Foundation, es preferible usar el marco MediaFoundation siempre que sea posible.

Puede crear un códec MFT llamando a la [**función CoCreateInstance.**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) Debe pasar el identificador de clase de MFT, el identificador de interfaz [**de IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)y un puntero a **un puntero DETRANSFORMTRANSFORM.**

Los identificadores de clase de los MTA de códec se definen como constantes en el archivo de encabezado wmcodecdsp.h.

La constante para el identificador [**de interfaz de IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) es IID \_ IMFTransform.

En el ejemplo de código siguiente se muestra cómo crear una instancia de un códec MFT:


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

[Trabajar con códecs MFT](workingwithcodecmfts.md)
</dt> </dl>

 

 
