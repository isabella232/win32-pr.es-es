---
title: Cuadro de diálogo cambiar el tamaño del adquisición de licencias
description: Cuadro de diálogo cambiar el tamaño del adquisición de licencias
ms.assetid: e091d981-1574-4ffc-bdc4-b92f74396cb7
keywords:
- Windows Media Player, cambiar el tamaño de la adquisición de licencias (cuadro de diálogo)
- Windows Media Player, cuadro de diálogo adquisición de licencias
- Media Player de Windows, atributo de DRM_LicenseAcqURL
- cuadro de diálogo para cambiar el tamaño de la adquisición de licencias
- Cuadro de diálogo adquisición de licencias
- DRM_LicenseAcqURL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 440683ce65417653251bbed58d59c4d9a34dbc57
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418902"
---
# <a name="resizing-the-license-acquisition-dialog-box"></a>Cuadro de diálogo cambiar el tamaño del adquisición de licencias

Puede anexar parámetros de cadena de consulta a la dirección URL que proporcione para que el atributo **\_ LicenseAcqURL de DRM** especifique un tamaño para el cuadro de diálogo adquisición de licencias de Windows Media Player 10 o posterior. En la tabla siguiente se enumeran los parámetros.



| Parámetro | Descripción                                        |
|-----------|----------------------------------------------------|
| *DlgX*    | Especifica el ancho del cuadro de diálogo, en píxeles.  |
| *DlgY*    | Especifica el alto del cuadro de diálogo, en píxeles. |



 

Por ejemplo, la siguiente dirección URL de adquisición de licencias haría que el cuadro de diálogo adquisición de licencias se abrira con un tamaño de 800 x 600 píxeles:


```C++
https://www.proseware.com/license/lic_acq.htm?DlgX=800&DlgY=600

```



El tamaño máximo del cuadro de diálogo nunca superará las dimensiones de pantalla actuales menos 20 píxeles. El tamaño mínimo es 333 x 210 píxeles (el tamaño predeterminado).

Esta característica requiere Windows Media Player 10 o posterior.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Reproductor de Windows Media**](windows-media-player.md)
</dt> </dl>

 

 




