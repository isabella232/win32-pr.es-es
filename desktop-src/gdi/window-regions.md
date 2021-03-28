---
description: Además de la región de actualización, cada ventana tiene un área visible que define la parte de la ventana visible para el usuario.
ms.assetid: 9d8beba1-93c0-437d-a138-76880a40bc79
title: Regiones de ventana
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02555339412c604f79f69294febbab524fc92a70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083040"
---
# <a name="window-regions"></a>Regiones de ventana

Además de la región de actualización, cada ventana tiene un *área visible* que define la parte de la ventana visible para el usuario. El sistema cambia el área visible de la ventana cada vez que cambia el tamaño de la ventana o cuando se mueve otra ventana de forma que oculta o expone una parte de la ventana. Las aplicaciones no pueden cambiar el área visible directamente, pero el sistema utiliza automáticamente el área visible para crear la región de recorte de cualquier contexto de dispositivo de pantalla recuperado para la ventana.

La *región de recorte* determina dónde permite el dibujo el sistema. Cuando la aplicación recupera un contexto de dispositivo de pantalla mediante la función [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint), [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc)o [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) , el sistema establece la región de recorte para el contexto de dispositivo en la intersección de la región visible y la región de actualización. Las aplicaciones pueden cambiar la región de recorte mediante el uso de funciones como [**SetWindowRgn**](/windows/desktop/api/Winuser/nf-winuser-setwindowrgn), [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) y [**SelectClipRgn**](/windows/desktop/api/Wingdi/nf-wingdi-selectcliprgn), para limitar aún más el dibujo a una parte determinada del área de actualización.

Los \_ estilos WS CLIPCHILDREN y WS \_ CLIPSIBLINGS especifican el modo en que el sistema calcula el área visible para una ventana. Si una ventana tiene uno o ambos estilos, el área visible excluye cualquier ventana secundaria o ventanas del mismo nivel (ventanas que tengan la misma ventana primaria). Por lo tanto, el dibujo que de otro modo informaría en estas ventanas siempre se recortará.

 

 



