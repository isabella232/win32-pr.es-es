---
description: Muestra cómo usar alta definición de aceleración de vídeo de Microsoft DirectX (DXVA-HD).
ms.assetid: dfd5cf5c-7d6e-4894-8d9b-41ef0293b3d3
title: Ejemplo de DXVA-HD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71ae1945a98bc668aa12cc6cdf8d9e4693cbde27
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127248540"
---
# <a name="dxva-hd-sample"></a>Ejemplo de DXVA-HD

Muestra cómo usar alta definición de aceleración de vídeo de Microsoft DirectX (DXVA-HD).

Este ejemplo es básicamente un puerto del ejemplo [ \_ dxva2 videoproc](dxva2-videoproc-sample.md). Tiene las mismas funciones básicas y la mayoría de los comandos de teclado son iguales.

El ejemplo genera vídeo mediante programación con una secuencia principal y una subsección. La secuencia principal muestra las barras de color de SMPTE. La subtratación se combina alfa en la secuencia principal mediante la clave luma. El usuario puede cambiar los parámetros de procesamiento de vídeo, incluidos el valor alfa plana, los rectángulos de origen y destino, los ajustes de color y el espacio de color. En la imagen siguiente se muestra el vídeo que se genera.

![captura de pantalla del ejemplo dxva-hd](images/dxva-hd-sample.png)

## <a name="apis-demonstrated"></a>API demostradas

En este ejemplo se muestran las siguientes interfaces DXVA-HD:

-   [**Dispositivo \_ IDXVAHD**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device)
-   [**IDXVAHD \_ VideoProcessor**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor)

## <a name="requirements"></a>Requisitos



| Producto                                                        | Versión   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Este ejemplo está disponible en el repositorio [de GitHub Windows ejemplos clásicos.](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/DXVA_HD)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DXVA-HD](dxva-hd.md)
</dt> <dt>

[Muestras de SDK de Media Foundation](media-foundation-sdk-samples.md)
</dt> </dl>

 

 



