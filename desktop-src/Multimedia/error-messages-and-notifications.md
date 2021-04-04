---
title: Mensajes de error y notificaciones
description: Mensajes de error y notificaciones
ms.assetid: 7f804364-d8be-4e52-ab0e-fba05bcf76ce
keywords:
- MCIWndGetError (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37e40e78c72dc378baa37b56dbb2d5718ae2d85b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077648"
---
# <a name="error-messages-and-notifications"></a>Mensajes de error y notificaciones

MCIWnd usa MCI para controlar los dispositivos que reproducen y graban datos multimedia. En general, MCIWnd muestra los errores de MCI en un cuadro de diálogo de error. Cuando se produce un error en un comando MCI, se genera un error de MCI. Por ejemplo, si la aplicación intenta reanudar la reproducción en pausa mediante la macro [**MCIWndResume**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) y el dispositivo actual no admite la reanudación, se envía un error al usuario.

MCIWnd permite dos opciones para controlar los mensajes de error:

-   Puede evitar que los mensajes de error lleguen al usuario. Para evitar que se muestren los mensajes de error de MCI, especifique el estilo de ventana de MCIWNDF \_ NOERRORDLG al crear una instancia de una ventana de MCIWnd mediante la función [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) o [CreateWindowEx](/windows/win32/api/winuser/nf-winuser-createwindowexa) .
-   Puede redirigirlas a la aplicación para que se muestren. Para redirigir los mensajes de error de MCI a la aplicación, especifique el \_ estilo de ventana de MCIWNDF NOTIFYERROR al crear una instancia de una ventana de MCIWnd mediante **MCIWndCreate** o **CreateWindowEx**.

Cuando se habilita la notificación de errores, MCIWnd envía cada mensaje de notificación ([**MCIWNDM \_ NOTIFYERROR**](mciwndm-notifyerror.md)) al controlador de mensajes principal del elemento primario de la ventana de MCIWnd. La aplicación debe tener un controlador de mensajes para procesar los mensajes de notificación que recibe.

Puede obtener una descripción textual del mensaje de error de MCI más reciente mediante la macro [**MCIWndGetError**](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror) . Esta macro devuelve el texto de un búfer definido por la aplicación. Si la cadena de error es más larga que el búfer, MCIWnd trunca la cadena.

Puede enrutar todas las notificaciones a otra ventana mediante la macro [**MCIWndSetOwner**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetowner) .

 

 