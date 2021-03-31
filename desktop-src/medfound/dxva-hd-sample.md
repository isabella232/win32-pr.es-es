---
description: Muestra cómo usar Microsoft DirectX video Acceleration High Definition (DXVA-HD).
ms.assetid: dfd5cf5c-7d6e-4894-8d9b-41ef0293b3d3
title: 'DXVA: ejemplo HD'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71ae1945a98bc668aa12cc6cdf8d9e4693cbde27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907567"
---
# <a name="dxva-hd-sample"></a>DXVA: ejemplo HD

Muestra cómo usar Microsoft DirectX video Acceleration High Definition (DXVA-HD).

Este ejemplo es esencialmente un puerto del [ejemplo de \_ videoproc DXVA2](dxva2-videoproc-sample.md). Tiene las mismas funciones básicas y la mayoría de los comandos del teclado son los mismos.

El ejemplo genera mediante programación el vídeo con una secuencia principal y un subflujo. El flujo principal muestra las barras de color SMPTE. La subsecuencia se combina alfa en el flujo principal mediante la creación de claves de luminancia. El usuario puede cambiar los parámetros de procesamiento de vídeo, incluidos el valor alfa plano, los rectángulos de origen y de destino, los ajustes de color y el espacio de colores. En la imagen siguiente se muestra el vídeo que se genera.

![captura de pantalla del ejemplo DXVA-HD](images/dxva-hd-sample.png)

## <a name="apis-demonstrated"></a>API mostradas

Este ejemplo muestra las siguientes interfaces de DXVA-HD:

-   [**\_Dispositivo IDXVAHD**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device)
-   [**IDXVAHD de \_ videoprocesador**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor)

## <a name="requirements"></a>Requisitos



| Producto                                                        | Versión   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Este ejemplo está disponible en el [repositorio de github de ejemplos de Windows clásico](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/DXVA_HD).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DXVA-HD](dxva-hd.md)
</dt> <dt>

[Muestras de SDK de Media Foundation](media-foundation-sdk-samples.md)
</dt> </dl>

 

 



