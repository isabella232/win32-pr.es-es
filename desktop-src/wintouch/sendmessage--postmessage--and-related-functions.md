---
title: SendMessage, PostMessage y funciones relacionadas
description: En esta sección se describen las consideraciones sobre el reenvío de mensajes mediante SendMessage, PostMessage y funciones relacionadas con mensajes táctiles.
ms.assetid: 9fba2013-17a3-499c-80dc-627e89c0edaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fc42e31f3c971c704d18f04a961fb6bd40eb91d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421035"
---
# <a name="sendmessage-postmessage-and-related-functions"></a>SendMessage, PostMessage y funciones relacionadas

En esta sección se describen las consideraciones sobre el reenvío de mensajes mediante [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage), [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea)y funciones relacionadas con mensajes táctiles.

Si se reenvía un mensaje táctil mediante [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage), [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea)u otra función relacionada, se cierra el controlador de entrada táctil. Si ha recuperado la información contenida por un identificador de entrada táctil a través de una llamada a [**GetTouchInputInfo**](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo), los datos seguirán siendo válidos hasta que libere la memoria.

Una aplicación que recibe mensajes táctiles reenviados a través de uno de estos mecanismos posee el identificador de entrada táctil que recibe en el mensaje *lParam* y es responsable de cerrarlo. Si no cierra el identificador con una llamada a [**CloseTouchInputHandle**](/windows/desktop/api/winuser/nf-winuser-closetouchinputhandle), pasa el mensaje a [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca)o reenvía el mensaje mediante [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage), [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea)o alguna función relacionada, se producirá una fuga de memoria.

> [!Note]  
> Los mensajes táctiles están sujetos a las reglas de aislamiento de privilegios de interfaz de usuario (UIPI) normales cuando se reenvían.

 

## <a name="functions-related-to-sendmessage-and-postmessage"></a>Funciones relacionadas con SendMessage y PostMessage

Las siguientes funciones que pueden afectar al estado del controlador de entrada táctil.

-   [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage)
-   [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea)
-   SendNotifyMessage
-   SendMessageCallback
-   SendMessageTimeout
-   PostThreadMessage

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Funciones](mtfunctions.md)
</dt> <dt>

[DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca)
</dt> </dl>

 

 