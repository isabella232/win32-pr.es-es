---
description: Muestra cómo escribir un descodificador para Microsoft Media Foundation.
ms.assetid: 941e5400-e679-41f4-9830-3548dc6037aa
title: Ejemplo de descodificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dd7586534876cfa7f530e675b0342a92bf46b8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000863"
---
# <a name="decoder-sample"></a>Ejemplo de descodificador

Muestra cómo escribir un descodificador para Microsoft Media Foundation.

En este ejemplo se implementa un descodificador de vídeo de MPEG-1 ficticio que muestra el código de tiempo para cada fotograma de vídeo. Realmente no descodifica MPEG-1 fragmentada. En la imagen siguiente se muestra la salida de vídeo del descodificador.

![captura de pantalla de un fotograma de vídeo desde el descodificador](images/decodersample.png)

> [!Note]  
> Antes de la Windows SDK para Windows 7, este ejemplo se incluyó como parte del [ejemplo MPEG1Source](mpeg1source-sample.md).

 

## <a name="apis-demonstrated"></a>API mostradas

Este ejemplo muestra las siguientes interfaces de Media Foundation:

-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="requirements"></a>Requisitos



| Producto                                                        | Versión   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Este ejemplo está disponible en el [repositorio de github de ejemplos de Windows clásico](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/Decoder).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Muestras de SDK de Media Foundation](media-foundation-sdk-samples.md)
</dt> <dt>

[Media Foundation transformaciones](media-foundation-transforms.md)
</dt> <dt>

[Escribir una MFT personalizada](writing-a-custom-mft.md)
</dt> </dl>

 

 



