---
description: Las funciones siguientes se usan con recorte.
ms.assetid: de9e5786-63d8-47be-8522-e96d7c0f8634
title: Funciones de recorte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c7e3ec1c57713a87e5367ed28427caaab663e0bcd1abfe83c4040e04a7e6d75
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120115335"
---
# <a name="clipping-functions"></a>Funciones de recorte

Las funciones siguientes se usan con recorte.



| Función                                       | Descripción                                                                                                                                                                               |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ExcludeClipRect**](/windows/desktop/api/Wingdi/nf-wingdi-excludecliprect)     | Crea una nueva región de recorte que consta de la región de recorte existente menos el rectángulo especificado.                                                                                |
| [**ExtSelectClipRgn**](/windows/desktop/api/Wingdi/nf-wingdi-extselectcliprgn)   | Combina la región especificada con la región de recorte actual mediante el modo especificado.                                                                                                  |
| [**GetClipBox**](/windows/desktop/api/Wingdi/nf-wingdi-getclipbox)               | Recupera las dimensiones del rectángulo delimitador más ajustado que se puede dibujar alrededor del área visible actual en el dispositivo.                                                              |
| [**GetClipRgn**](/windows/desktop/api/Wingdi/nf-wingdi-getcliprgn)               | Recupera un identificador que identifica la región de recorte definida por la aplicación actual para el contexto de dispositivo especificado.                                                                          |
| [**GetMetaRgn**](/windows/desktop/api/Wingdi/nf-wingdi-getmetargn)               | Recupera la metaregión actual para el contexto de dispositivo especificado.                                                                                                                        |
| [**GetRandomRgn**](/windows/desktop/api/Wingdi/nf-wingdi-getrandomrgn)           | Copia la región de recorte del sistema de un contexto de dispositivo especificado en una región específica.                                                                                                     |
| [**IntersectClipRect**](/windows/desktop/api/Wingdi/nf-wingdi-intersectcliprect) | Crea una nueva región de recorte a partir de la intersección de la región de recorte actual y el rectángulo especificado.                                                                           |
| [**OffsetClipRgn**](/windows/desktop/api/Wingdi/nf-wingdi-offsetcliprgn)         | Mueve la región de recorte de un contexto de dispositivo por los desplazamientos especificados.                                                                                                                   |
| [**PtVisible**](/windows/desktop/api/Wingdi/nf-wingdi-ptvisible)                 | Determina si el punto especificado está dentro de la región de recorte de un contexto de dispositivo.                                                                                                 |
| [**RectVisible**](/windows/desktop/api/Wingdi/nf-wingdi-rectvisible)             | Determina si alguna parte del rectángulo especificado se encuentra dentro de la región de recorte de un contexto de dispositivo.                                                                               |
| [**SeleccioneClipPath.**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath)       | Selecciona la ruta de acceso actual como región de recorte para un contexto de dispositivo, combinando la nueva región con cualquier región de recorte existente mediante el modo especificado.                               |
| [**SeleccioneClipRgn.**](/windows/desktop/api/Wingdi/nf-wingdi-selectcliprgn)         | Selecciona una región como región de recorte actual para el contexto de dispositivo especificado.                                                                                                         |
| [**SetMetaRgn**](/windows/desktop/api/Wingdi/nf-wingdi-setmetargn)               | Interseca la región de recorte actual para el contexto de dispositivo especificado con la metaregión actual y guarda la región combinada como la nueva metaregión para el contexto de dispositivo especificado. |



 

 

 



