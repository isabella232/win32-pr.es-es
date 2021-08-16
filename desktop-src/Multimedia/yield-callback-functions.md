---
title: Funciones de devolución de llamada yield
description: Funciones de devolución de llamada yield
ms.assetid: 8c9b43ea-fdba-41a2-ba2d-1eaa4516e14f
keywords:
- Funciones de devolución de llamada de AVICap, yield
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e87a3c986378bee05078b8cab28a0647827a1102ef1809558a47dcd5123af2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118369139"
---
# <a name="yield-callback-functions"></a>Funciones de devolución de llamada yield

Las aplicaciones pueden usar funciones de devolución de llamada yield durante la captura de streaming. (Una función de devolución de llamada yield normalmente consta de un bucle de mensajes que llama a [PeekMessage,](/windows/win32/api/winuser/nf-winuser-peekmessagea) [TranslateMessage](/windows/win32/api/winuser/nf-winuser-translatemessage)y [DispatchMessage).](/windows/win32/api/winuser/nf-winuser-dispatchmessage) La ventana de captura llama a la función de devolución de llamada yield al menos una vez para cada fotograma de vídeo capturado, pero la velocidad exacta depende de la velocidad de fotogramas y la sobrecarga del controlador de captura y el disco.

 

 