---
description: Filtro del mezclador de superposición 2
ms.assetid: 3d3871ac-518c-45a1-9e64-031f344f4527
title: Filtro del mezclador de superposición 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f22976a58b272cf04c098c102d32d154e361b8b9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686369"
---
# <a name="overlay-mixer-2-filter"></a>Filtro del mezclador de superposición 2

El filtro del mezclador de superposición 2 es idéntico al filtro de [mezclador de superposición](overlay-mixer-filter.md) , excepto:

-   Solo admite tipos de medios con formatos [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) .
-   Tiene un mérito mayor, lo que permite que se agregue automáticamente a un gráfico de filtros.

Se proporciona el mezclador de superposición 2 para que el administrador de gráficos de filtro lo agregue al gráfico cuando represente vídeo MPEG-2 de no DVD. La opción de usar el mezclador de superposición o el mezclador de superposición 2 se controla mediante el componente que genera el gráfico, ya sea el administrador de gráficos de filtro, el generador de gráficos de captura o el generador de gráficos de DVD. Desde la perspectiva de la aplicación, son el mismo filtro, con las mismas interfaces y funcionalidad.

La tabla siguiente contiene información específica del mezclador de superposición 2. Para el resto de datos de filtro, consulte la documentación del mezclador de superposición.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Tipos de medios de anclaje de entrada</td>
<td>Tipo de formato: Format_VIDEOINFO2</td>
</tr>
<tr class="even">
<td>Identificador CLSID</td>
<td>CLSID_OverlayMixer2</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Fundament</a></td>
<td><ul>
<li>MERIT_UNLIKELY</li>
<li>Windows Vista o posterior: MERIT_DO_NOT_USE</li>
</ul></td>
</tr>
</tbody>
</table>



 

En Windows Vista o posterior, el mérito del filtro del mezclador de superposición 2 es el mérito \_ \_ no se \_ usa, ya que los representadores de vídeo más recientes (VMR-7, VMR-9 y EVR) admiten formatos de **VIDEOINFOHEADER2** y, por tanto, no es necesario usar el mezclador de superposición.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> </dl>

 

 



