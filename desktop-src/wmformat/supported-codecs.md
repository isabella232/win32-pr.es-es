---
title: Códecs admitidos
description: Códecs admitidos
ms.assetid: d5907d38-2e26-442e-a0d1-1d7e267b9948
keywords:
- SDK de Windows Media Format, códecs admitidos
- SDK de Windows Media Format, interfaz IWMCodecInfo3
- códecs, admitidos
- IWMCodecInfo3, acerca de
- códecs, interfaz IWMCodecInfo3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5ac06ad3d58d066254fa666f96283dca9b8b6ae
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788830"
---
# <a name="supported-codecs"></a>Códecs admitidos

El SDK de Windows Media Format proporciona compatibilidad con los códecs siguientes que se incluyen al instalar el SDK.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Códec</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Windows Media Audio</td>
<td>Códec de audio para uso general en la codificación de audio complejo, como música. Las versiones más recientes de este códec son el códec Windows Media Audio 9 y el códec Windows Media Audio 9,1.<br/></td>
</tr>
<tr class="even">
<td>Windows Media Audio Professional</td>
<td>Códec de audio para audio complejo, como música. Admite la codificación multicanal y de 24 bits. Hay dos versiones de este códec:<br/>
<ul>
<li>Windows Media Audio 9 Professional</li>
<li>Windows Media Audio 9,1 Professional</li>
</ul></td>
</tr>
<tr class="odd">
<td>Windows Media Audio sin pérdida de</td>
<td>Códec de audio para la codificación sin pérdida. Hay dos versiones de este códec:<br/>
<ul>
<li>Windows Media Audio 9 sin pérdida de</li>
<li>Windows Media Audio 9,1 Lossless</li>
</ul></td>
</tr>
<tr class="even">
<td>Windows Media Audio 9 Voice</td>
<td>Códec de audio optimizado para codificar las proporciones de la voz humana a alta compresión. Este es el códec preferido para las secuencias que se componen principalmente de palabras pronunciadas. En el caso de contenido que está mezclado con música y voz, este códec puede cambiar dinámicamente el algoritmo de codificación que se usa para obtener una calidad óptima.</td>
</tr>
<tr class="odd">
<td>Windows Media Video 9</td>
<td>Códec de vídeo para uso general en la codificación de vídeo complejo, como películas.</td>
</tr>
<tr class="even">
<td>Perfil avanzado de Windows Media Video 9</td>
<td>Códec de vídeo que incorpora características avanzadas de codificación, incluida la codificación entrelazada.</td>
</tr>
<tr class="odd">
<td>Pantalla de Windows Media Video 9</td>
<td>Códec de vídeo optimizado para codificar capturas de pantalla secuenciales. Este códec se usa a menudo para aprendizaje o soporte técnico de software mediante la grabación de imágenes del monitor a medida que se usan aplicaciones para equipos.</td>
</tr>
<tr class="even">
<td>Imagen de Windows Media Video</td>
<td>Códec de vídeo para convertir imágenes de mapa de bits con información de desformación en vídeo comprimido. Hay dos versiones de este códec:<br/>
<ul>
<li>Imagen de Windows Media Video 9</li>
<li>Windows Media Video 9 imagen V2</li>
</ul></td>
</tr>
</tbody>
</table>



 

Hay disponibles versiones diferentes de los códecs de Windows Media Audio y vídeo para la codificación según la versión del SDK de Windows Media Format que instale. Cuando se usan los métodos de la interfaz [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3) para enumerar los códecs y los formatos de códec, solo se enumeran las últimas versiones compatibles.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Elección de un método de codificación**](choosing-an-encoding-method.md)
</dt> <dt>

[**Características del códec**](codec-features.md)
</dt> </dl>

 

 





