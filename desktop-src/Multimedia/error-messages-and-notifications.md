---
title: Notificaciones y mensajes de error
description: Notificaciones y mensajes de error
ms.assetid: 7f804364-d8be-4e52-ab0e-fba05bcf76ce
keywords:
- Macro MCIWndGetError
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37e40e78c72dc378baa37b56dbb2d5718ae2d85b
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124372218"
---
# <a name="error-messages-and-notifications"></a>Notificaciones y mensajes de error

MCIWnd usa MCI para controlar los dispositivos que reproducen y registran datos multimedia. En general, MCIWnd muestra errores de MCI en un cuadro de diálogo de error. Se genera un error de MCI cada vez que se produce un error en un comando MCI. Por ejemplo, si la aplicación intenta reanudar la reproducción en pausa mediante la macro [**MCIWndResume**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) y el dispositivo actual no admite la reanudación, se notifica un error al usuario.

MCIWnd permite dos opciones para controlar los mensajes de error:

-   Puede evitar que los mensajes de error lleguen al usuario. Para evitar la presentación de mensajes de error de MCI, especifique el estilo de ventana MCIWNDF NOERRORDLG al crear una instancia de una ventana de MCIWnd mediante las funciones \_ [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) o [CreateWindowEx.](/windows/win32/api/winuser/nf-winuser-createwindowexa)
-   Puede redirigirlos a la aplicación para mostrarlos. Para redirigir los mensajes de error de MCI a la aplicación, especifique el estilo de ventana NOTIFYERROR de MCIWNDF al crear una instancia de una ventana \_ de MCIWnd mediante **MCIWndCreate** o **CreateWindowEx**.

Cuando se habilita la notificación de errores, MCIWnd envía cada mensaje de notificación [**(MCIWNDM \_ NOTIFYERROR**](mciwndm-notifyerror.md)) al controlador de mensajes principal del elemento primario de la ventana MCIWnd. La aplicación debe tener un controlador de mensajes para procesar los mensajes de notificación que recibe.

Puede obtener una descripción textual del mensaje de error de MCI más reciente mediante la macro [**MCIWndGetError.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror) Esta macro devuelve el texto en un búfer definido por la aplicación. Si la cadena de error es mayor que el búfer, MCIWnd trunca la cadena.

Puede enrutar todas las notificaciones a otra ventana mediante la macro [**MCIWndSetOwner.**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetowner)

 

 