---
title: SendMessage, PostMessage y funciones relacionadas
description: En esta sección se describen las consideraciones sobre el reenvío de mensajes mediante SendMessage, PostMessage y funciones relacionadas con mensajes táctiles.
ms.assetid: 9fba2013-17a3-499c-80dc-627e89c0edaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fc42e31f3c971c704d18f04a961fb6bd40eb91d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466221"
---
# <a name="sendmessage-postmessage-and-related-functions"></a>SendMessage, PostMessage y funciones relacionadas

En esta sección se describen las consideraciones sobre el reenvío de mensajes mediante [SendMessage,](/windows/desktop/api/winuser/nf-winuser-sendmessage) [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea)y funciones relacionadas con mensajes táctiles.

Si se reenvía un mensaje táctil mediante [SendMessage,](/windows/desktop/api/winuser/nf-winuser-sendmessage) [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea)o alguna otra función relacionada, se cierra el identificador de entrada táctil. Si ha recuperado la información contenida a la que hace referencia un identificador de entrada táctil a través de una llamada a [**GetTouchInputInfo**](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo), los datos seguirán siendo válidos hasta que se libera la memoria.

Una aplicación que recibe mensajes táctiles reenviados a través de uno de estos mecanismos posee el identificador de entrada táctil que recibe en el *LPARAM* del mensaje y es responsable de cerrarlo. Si no cierra el identificador con una llamada a [**CloseTouchInputHandle**](/windows/desktop/api/winuser/nf-winuser-closetouchinputhandle), pase el mensaje a [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca)o reenvía el mensaje mediante [SendMessage,](/windows/desktop/api/winuser/nf-winuser-sendmessage) [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea)o alguna función relacionada, tendrá una pérdida de memoria.

> [!Note]  
> Los mensajes táctiles están sujetos a reglas Interfaz de usuario aislamiento de privilegios de usuario (UIPI) normales cuando se reenvía.

 

## <a name="functions-related-to-sendmessage-and-postmessage"></a>Funciones relacionadas con SendMessage y PostMessage

Las siguientes funciones que pueden afectar al estado del identificador de entrada táctil.

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

 

 