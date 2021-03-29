---
title: Automatizar la reproducción
description: Automatizar la reproducción
ms.assetid: 3aa05a54-58d7-4d14-93ee-459aa860b20e
keywords:
- MCIWndCreate (macro)
- MCIWndPlay (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6097d38b3d468b6de68ee7e11f98f530aff00d2b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779609"
---
# <a name="automating-playback"></a>Automatizar la reproducción

Puede automatizar la reproducción en la aplicación mediante [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) y la macro [**MCIWndPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) , junto con la macro [**MCIWndDestroy**](/windows/desktop/api/Vfw/nf-vfw-mciwnddestroy) o [**MCIWndClose**](/windows/desktop/api/Vfw/nf-vfw-mciwndclose) . Para automatizar la reproducción, especifique los \_ estilos MCIWNDF NOPLAYBAR y MCIWNDF \_ NOTIFYMODE en el parámetro **MCIWndCreate ** * * dwStyle. Especifique el \_ estilo MCIWNDF NOPLAYBAR para ocultar la barra de herramientas y el \_ estilo MCIWNDF NOTIFYMODE para emitir un mensaje de notificación adecuado cuando el dispositivo deje de reproducirse.

Puede reproducir el dispositivo o el archivo especificado en **MCIWndCreate** mediante **MCIWndPlay**. La macro MCIWndPlay empieza a reproducir el contenido desde su posición de reproducción actual y continúa hasta el final.

Puede destruir o cerrar una ventana de MCIWnd con la macro [**MCIWndDestroy**](/windows/desktop/api/Vfw/nf-vfw-mciwnddestroy) o [**MCIWndClose**](/windows/desktop/api/Vfw/nf-vfw-mciwndclose) . La macro **MCIWndDestroy** cierra el dispositivo o el archivo y destruye la ventana MCIWnd invalidando su identificador. Si la aplicación puede volver a usar la ventana de MCIWnd, use **MCIWndClose** para cerrar el dispositivo sin destruir la ventana.

La aplicación puede detectar Cuándo deja de reproducirse el dispositivo y cierra automáticamente la ventana. Para ello, especifique el estilo MCIWNDF \_ NOTIFYMODE para el parámetro *DwStyle* de [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea). Esto hace que el dispositivo envíe un mensaje de [**MCIWNDM \_ NOTIFYMODE**](mciwndm-notifymode.md) cada vez que cambie de modo. La aplicación puede capturar este mensaje para determinar si el dispositivo ha dejado de reproducirse. Cuando el dispositivo deja de reproducirse, la aplicación cierra la ventana.

 

 




