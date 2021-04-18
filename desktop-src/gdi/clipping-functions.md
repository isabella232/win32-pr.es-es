---
description: Las siguientes funciones se usan con el recorte.
ms.assetid: de9e5786-63d8-47be-8522-e96d7c0f8634
title: Funciones de recorte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bf202d5ba102095c6bfddb3c3928cab1e55a230
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985043"
---
# <a name="clipping-functions"></a>Funciones de recorte

Las siguientes funciones se usan con el recorte.



| Función                                       | Descripción                                                                                                                                                                               |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ExcludeClipRect**](/windows/desktop/api/Wingdi/nf-wingdi-excludecliprect)     | Crea una nueva región de recorte que consta de la región de recorte existente menos el rectángulo especificado.                                                                                |
| [**ExtSelectClipRgn**](/windows/desktop/api/Wingdi/nf-wingdi-extselectcliprgn)   | Combina la región especificada con la región de recorte actual mediante el modo especificado.                                                                                                  |
| [**GetClipBox**](/windows/desktop/api/Wingdi/nf-wingdi-getclipbox)               | Recupera las dimensiones del rectángulo delimitador más estrecho que se puede dibujar alrededor del área visible actual en el dispositivo.                                                              |
| [**GetClipRgn**](/windows/desktop/api/Wingdi/nf-wingdi-getcliprgn)               | Recupera un identificador que identifica la región de recorte actual definida por la aplicación para el contexto de dispositivo especificado.                                                                          |
| [**GetMetaRgn**](/windows/desktop/api/Wingdi/nf-wingdi-getmetargn)               | Recupera la metaregión actual del contexto de dispositivo especificado.                                                                                                                        |
| [**GetRandomRgn**](/windows/desktop/api/Wingdi/nf-wingdi-getrandomrgn)           | Copia la región de recorte del sistema de un contexto de dispositivo especificado en una región específica.                                                                                                     |
| [**IntersectClipRect**](/windows/desktop/api/Wingdi/nf-wingdi-intersectcliprect) | Crea una nueva región de recorte a partir de la intersección de la región de recorte actual y el rectángulo especificado.                                                                           |
| [**OffsetClipRgn**](/windows/desktop/api/Wingdi/nf-wingdi-offsetcliprgn)         | Mueve la región de recorte de un contexto de dispositivo mediante los desplazamientos especificados.                                                                                                                   |
| [**PtVisible**](/windows/desktop/api/Wingdi/nf-wingdi-ptvisible)                 | Determina si el punto especificado está dentro de la región de recorte de un contexto de dispositivo.                                                                                                 |
| [**RectVisible**](/windows/desktop/api/Wingdi/nf-wingdi-rectvisible)             | Determina si alguna parte del rectángulo especificado está dentro de la región de recorte de un contexto de dispositivo.                                                                               |
| [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath)       | Selecciona la ruta de acceso actual como una región de recorte para un contexto de dispositivo, combinando la nueva región con cualquier región de recorte existente mediante el modo especificado.                               |
| [**SelectClipRgn**](/windows/desktop/api/Wingdi/nf-wingdi-selectcliprgn)         | Selecciona una región como la región de recorte actual para el contexto de dispositivo especificado.                                                                                                         |
| [**SetMetaRgn**](/windows/desktop/api/Wingdi/nf-wingdi-setmetargn)               | Forma una intersección con la región de recorte actual del contexto de dispositivo especificado con la metaregión actual y guarda la región combinada como la nueva metaregión para el contexto de dispositivo especificado. |



 

 

 



