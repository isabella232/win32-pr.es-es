---
title: Funciones de devolución de llamada yield
description: Funciones de devolución de llamada yield
ms.assetid: 8c9b43ea-fdba-41a2-ba2d-1eaa4516e14f
keywords:
- Funciones de devolución de llamada AVICap, yield
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3666ea24a1d37402ffc13c09ca8ab95fcd19e1f7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790540"
---
# <a name="yield-callback-functions"></a>Funciones de devolución de llamada yield

Las aplicaciones pueden usar funciones de devolución de llamada yield durante la captura de streaming. (Una función de devolución de llamada yield consta normalmente de un bucle de mensajes que llama a [PeekMessage](/windows/win32/api/winuser/nf-winuser-peekmessagea), [TranslateMessage](/windows/win32/api/winuser/nf-winuser-translatemessage)y [DispatchMessage](/windows/win32/api/winuser/nf-winuser-dispatchmessage)). La ventana captura llama a la función de devolución de llamada yield al menos una vez para cada fotograma de vídeo capturado, pero la velocidad exacta depende de la velocidad de fotogramas y la sobrecarga del disco y del controlador de captura.

 

 