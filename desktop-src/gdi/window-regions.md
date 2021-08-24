---
description: Además de la región de actualización, cada ventana tiene una región visible que define la parte de la ventana visible para el usuario.
ms.assetid: 9d8beba1-93c0-437d-a138-76880a40bc79
title: Regiones de ventana
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac3f751303d8a971d010ea7dabf7604c24db892f88d9a4029f0189d303cf5a80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119727415"
---
# <a name="window-regions"></a>Regiones de ventana

Además de la región de actualización, cada ventana tiene una *región visible* que define la parte de la ventana visible para el usuario. El sistema cambia la región visible de la ventana cada vez que cambia el tamaño de la ventana o cada vez que se mueve otra ventana, de forma que oculta o expone una parte de la ventana. Las aplicaciones no pueden cambiar la región visible directamente, pero el sistema usa automáticamente la región visible para crear la región de recorte para cualquier contexto de dispositivo para mostrar recuperado para la ventana.

La *región de recorte* determina dónde el sistema permite dibujar. Cuando la aplicación recupera un contexto de dispositivo para mostrar mediante la función [**BeginPaint,**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc)o [**GetDCEx,**](/windows/desktop/api/Winuser/nf-winuser-getdcex) el sistema establece la región de recorte del contexto del dispositivo en la intersección de la región visible y la región de actualización. Las aplicaciones pueden cambiar la región de recorte mediante funciones como [**SetWindowRgn,**](/windows/desktop/api/Winuser/nf-winuser-setwindowrgn) [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) y [**SelectClipRgn**](/windows/desktop/api/Wingdi/nf-wingdi-selectcliprgn)para limitar aún más el dibujo a una parte determinada del área de actualización.

Los estilos WS CLIPCHILDREN y \_ WS CLIPSIBLINGS especifican aún más cómo calcula el sistema la \_ región visible para una ventana. Si una ventana tiene uno o ambos estilos, la región visible excluye cualquier ventana secundaria o ventanas del mismo nivel (ventanas que tengan la misma ventana primaria). Por lo tanto, siempre se recortará el dibujo que, de lo contrario, intrusaría en estas ventanas.

 

 



