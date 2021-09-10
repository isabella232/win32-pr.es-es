---
title: Especificar formatos de hora
description: Especificar formatos de hora
ms.assetid: 11d28d63-ed3e-4137-b9d8-1681bf0e33ff
keywords:
- Macro MCIWndGetTimeFormat
- Macro MCIWndSetTimeFormat
- Macro MCIWndUseTime
- Macro MCIWndUseFrames
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e390e811bde4d797572c19f372923906f6b738b
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124372170"
---
# <a name="specifying-time-formats"></a>Especificar formatos de hora

Normalmente, los tipos de datos multimedia pueden usar tiempo para identificar posiciones significativas dentro de su contenido. Los formatos de hora comunes son milisegundos, pistas y fotogramas. También existen otros formatos de hora menos comunes, como SMPTE (Society of Motion Picture and Tv Engineers) 24. La hora es el formato y el sistema de referencia para los datos de audio de forma de onda, MIDI y CD. El vídeo admite el tiempo aunque se grabe como una secuencia de fotogramas (secuencia) que normalmente se reproduce a una velocidad específica. Hay varias macros disponibles para designar el formato de hora.

Puede recuperar el formato de hora actual de un archivo o dispositivo mediante la macro [**MCIWndGetTimeFormat.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat) Puede cambiar el formato de hora actual a cualquier otro formato de hora admitido por un dispositivo mediante la macro [**MCIWndSetTimeFormat.**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimeformat) También puede establecer el formato de hora en milisegundos o fotogramas mediante las macros [**MCIWndUseTime**](/windows/desktop/api/Vfw/nf-vfw-mciwndusetime) o [**MCIWndUseFrames.**](/windows/desktop/api/Vfw/nf-vfw-mciwnduseframes)

> [!Note]  
> Los formatos no comunes, como pistas y SMPTE, pueden hacer que la barra de herramientas se comporte de forma errática. Para estos formatos de tiempo, es posible que quiera desactivar la barra de herramientas especificando el estilo de ventana MCIWNDF NOPLAYBAR al crear una \_ ventana de MCIWnd.

 

 

 




