---
title: Automatización de la reproducción
description: Automatización de la reproducción
ms.assetid: 3aa05a54-58d7-4d14-93ee-459aa860b20e
keywords:
- MCIWndCreate macro
- Macro MCIWndPlay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6097d38b3d468b6de68ee7e11f98f530aff00d2b
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371996"
---
# <a name="automating-playback"></a>Automatización de la reproducción

Puede automatizar la reproducción en la aplicación mediante [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) y la macro [**MCIWndPlay,**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) junto con [**MCIWndDestroy**](/windows/desktop/api/Vfw/nf-vfw-mciwnddestroy) o la macro [**MCIWndClose.**](/windows/desktop/api/Vfw/nf-vfw-mciwndclose) Para automatizar la reproducción, especifique los estilos MCIWNDF \_ NOPLAYBAR y MCIWNDF NOTIFYMODE en el \_ parámetro **MCIWndCreate**_dwStyle._ Especifique el estilo MCIWNDF NOPLAYBAR para ocultar la barra de herramientas y el estilo NOTIFYMODE de MCIWNDF para emitir un mensaje de notificación adecuado cuando el dispositivo deje \_ \_ de reproducirse.

Puede reproducir el dispositivo o archivo especificado en **MCIWndCreate** mediante **MCIWndPlay**. La macro MCIWndPlay comienza a reproducir el contenido desde su posición de reproducción actual y continúa hasta su final.

Puede destruir o cerrar una ventana de MCIWnd mediante la macro [**MCIWndDestroy**](/windows/desktop/api/Vfw/nf-vfw-mciwnddestroy) o [**MCIWndClose.**](/windows/desktop/api/Vfw/nf-vfw-mciwndclose) La **macro MCIWndDestroy** cierra el dispositivo o archivo y destruye la ventana de MCIWnd invalidando su identificador. Si la aplicación puede reutilizar la ventana MCIWnd, use **MCIWndClose** para cerrar el dispositivo sin destruir la ventana.

La aplicación puede detectar cuándo deja de reproducirse el dispositivo y cerrar automáticamente la ventana. Para ello, especifique el estilo NOTIFYMODE de MCIWNDF para el \_ *parámetro dwStyle* [**de MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea). Esto hace que el dispositivo envíe un [**mensaje \_ NOTIFYMODE de MCIWNDM**](mciwndm-notifymode.md) cada vez que cambie de modo. La aplicación puede capturar este mensaje para determinar si el dispositivo ha dejado de reproducirse. Cuando el dispositivo deja de reproducirse, la aplicación cierra la ventana.

 

 




