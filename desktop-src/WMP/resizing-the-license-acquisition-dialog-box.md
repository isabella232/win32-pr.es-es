---
title: Cambiar el tamaño del cuadro de diálogo Adquisición de licencias
description: Cambiar el tamaño del cuadro de diálogo Adquisición de licencias
ms.assetid: e091d981-1574-4ffc-bdc4-b92f74396cb7
keywords:
- Reproductor de Windows Media, cambiar el tamaño del cuadro de diálogo Adquisición de licencias
- Reproductor de Windows Media,Adquisición de licencias (cuadro de diálogo)
- Reproductor de Windows Media,DRM_LicenseAcqURL atributo
- cambiar el tamaño del cuadro de diálogo Adquisición de licencias
- Adquisición de licencias, cuadro de diálogo
- DRM_LicenseAcqURL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 440683ce65417653251bbed58d59c4d9a34dbc57
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476192"
---
# <a name="resizing-the-license-acquisition-dialog-box"></a>Cambiar el tamaño del cuadro de diálogo Adquisición de licencias

Puede anexar parámetros de cadena de consulta a la dirección URL que proporcione para el atributo **\_ LicenseAcqURL** de DRM para especificar un tamaño para el cuadro de diálogo de adquisición de licencias Reproductor de Windows Media 10 o posterior. En la tabla siguiente se enumeran los parámetros.



| Parámetro | Descripción                                        |
|-----------|----------------------------------------------------|
| *DlgX*    | Especifica el ancho del cuadro de diálogo, en píxeles.  |
| *DlgY*    | Especifica el alto del cuadro de diálogo, en píxeles. |



 

Por ejemplo, la siguiente dirección URL de adquisición de licencias haría que el cuadro de diálogo de adquisición de licencias se abra con un tamaño de 800 por 600 píxeles:


```C++
https://www.proseware.com/license/lic_acq.htm?DlgX=800&DlgY=600

```



El tamaño máximo del cuadro de diálogo nunca superará las dimensiones de pantalla actuales menos 20 píxeles. El tamaño mínimo es de 333 x 210 píxeles (el tamaño predeterminado).

Esta característica requiere Reproductor de Windows Media 10 o posterior.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Reproductor de Windows Media**](windows-media-player.md)
</dt> </dl>

 

 




