---
description: Muestra cómo escribir un descodificador para Microsoft Media Foundation.
ms.assetid: 941e5400-e679-41f4-9830-3548dc6037aa
title: Ejemplo de descodificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 290f8b2db32b12d535feaeef65f37b77e1a29115cd8844a8d8aad29fb7ce699a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119449395"
---
# <a name="decoder-sample"></a>Ejemplo de descodificador

Muestra cómo escribir un descodificador para Microsoft Media Foundation.

En este ejemplo se implementa un descodificador de vídeo MPEG-1 ficticio que muestra el código de hora de cada fotograma de vídeo. En realidad, no descodifica la secuencia de bits MPEG-1. En la imagen siguiente se muestra la salida de vídeo del descodificador.

![captura de pantalla de un fotograma de vídeo desde el descodificador](images/decodersample.png)

> [!Note]  
> Antes del SDK Windows para Windows 7, este ejemplo se incluía como parte del [ejemplo MPEG1Source](mpeg1source-sample.md).

 

## <a name="apis-demonstrated"></a>API demostradas

En este ejemplo se muestran las Media Foundation siguientes:

-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="requirements"></a>Requisitos



| Producto                                                        | Versión   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Este ejemplo está disponible en el repositorio [de github Windows ejemplos clásicos](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/Decoder).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Muestras de SDK de Media Foundation](media-foundation-sdk-samples.md)
</dt> <dt>

[Media Foundation transformaciones](media-foundation-transforms.md)
</dt> <dt>

[Escritura de un MFT personalizado](writing-a-custom-mft.md)
</dt> </dl>

 

 



