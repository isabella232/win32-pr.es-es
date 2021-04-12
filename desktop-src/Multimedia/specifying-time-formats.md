---
title: Especificar formatos de hora
description: Especificar formatos de hora
ms.assetid: 11d28d63-ed3e-4137-b9d8-1681bf0e33ff
keywords:
- MCIWndGetTimeFormat (macro)
- MCIWndSetTimeFormat (macro)
- MCIWndUseTime (macro)
- MCIWndUseFrames (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e390e811bde4d797572c19f372923906f6b738b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357118"
---
# <a name="specifying-time-formats"></a>Especificar formatos de hora

Normalmente, los tipos de datos multimedia pueden usar el tiempo para identificar posiciones significativas dentro de su contenido. Los formatos de hora comunes son milisegundos, pistas y fotogramas; también existen otros formatos de hora menos comunes, como SMPTE (sociedad de la imagen de movimiento y ingenieros de televisión) 24. La hora es el sistema de formato y de referencia para los datos de audio de forma de onda, MIDI y CD. El vídeo admite el tiempo aunque se grabe como una secuencia de fotogramas (secuencia) que normalmente se reproduce a una velocidad específica. Hay varias macros disponibles para designar el formato de hora.

Puede recuperar el formato de hora actual para un archivo o dispositivo mediante la macro [**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat) . Puede cambiar el formato de hora actual a cualquier otro formato de hora compatible con un dispositivo mediante la macro [**MCIWndSetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimeformat) . O bien, puede establecer el formato de hora en milisegundos o en marcos mediante el uso de las macros [**MCIWndUseTime**](/windows/desktop/api/Vfw/nf-vfw-mciwndusetime) o [**MCIWndUseFrames**](/windows/desktop/api/Vfw/nf-vfw-mciwnduseframes) .

> [!Note]  
> Los formatos no continuos, como las pistas y SMPTE, pueden hacer que la barra de herramientas se comporte de forma errática. Para estos formatos de hora, puede que desee desactivar la barra de herramientas especificando el estilo de ventana de MCIWNDF \_ NOPLAYBAR al crear una ventana de MCIWnd.

 

 

 




