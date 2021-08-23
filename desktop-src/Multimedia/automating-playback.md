---
title: Automatización de la reproducción
description: Automatización de la reproducción
ms.assetid: 3aa05a54-58d7-4d14-93ee-459aa860b20e
keywords:
- MCIWndCreate macro
- Macro MCIWndPlay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad1c05041bade08f47505a2cf1207739777c5af825ea9f5f300b343b87efe3c7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691975"
---
# <a name="automating-playback"></a>Automatización de la reproducción

Puede automatizar la reproducción en la aplicación mediante [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) y la macro [**MCIWndPlay,**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) junto con la macro [**MCIWndDestroy**](/windows/desktop/api/Vfw/nf-vfw-mciwnddestroy) o [**MCIWndClose.**](/windows/desktop/api/Vfw/nf-vfw-mciwndclose) Para automatizar la reproducción, especifique los estilos MCIWNDF \_ NOPLAYBAR y MCIWNDF NOTIFYMODE en el \_ parámetro **MCIWndCreate**_dwStyle._ Especifique el estilo MCIWNDF NOPLAYBAR para ocultar la barra de herramientas y el estilo NOTIFYMODE de MCIWNDF para emitir un mensaje de notificación adecuado cuando el dispositivo deje \_ \_ de reproducirse.

Puede reproducir el dispositivo o archivo especificado en **MCIWndCreate** mediante **MCIWndPlay**. La macro MCIWndPlay comienza a reproducir el contenido desde su posición de reproducción actual y continúa hasta su final.

Puede destruir o cerrar una ventana de MCIWnd mediante la macro [**MCIWndDestroy**](/windows/desktop/api/Vfw/nf-vfw-mciwnddestroy) o [**MCIWndClose.**](/windows/desktop/api/Vfw/nf-vfw-mciwndclose) La **macro MCIWndDestroy** cierra el dispositivo o el archivo y destruye la ventana MCIWnd invalidando su identificador. Si la aplicación puede reutilizar la ventana MCIWnd, use **MCIWndClose** para cerrar el dispositivo sin destruir la ventana.

La aplicación puede detectar cuándo deja de reproducirse el dispositivo y cerrar automáticamente la ventana. Para ello, especifique el estilo NOTIFYMODE de MCIWNDF para el \_ *parámetro dwStyle* [**de MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea). Esto hace que el dispositivo envíe un [**mensaje \_ NOTIFYMODE de MCIWNDM**](mciwndm-notifymode.md) cada vez que cambia de modo. La aplicación puede capturar este mensaje para determinar si el dispositivo ha dejado de reproducirse. Cuando el dispositivo deja de reproducirse, la aplicación cierra la ventana.

 

 




