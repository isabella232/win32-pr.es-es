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
# <a name="sendmessage-postmessage-and-related-functions"></a><span data-ttu-id="6494e-103">SendMessage, PostMessage y funciones relacionadas</span><span class="sxs-lookup"><span data-stu-id="6494e-103">SendMessage, PostMessage, and Related Functions</span></span>

<span data-ttu-id="6494e-104">En esta sección se describen las consideraciones sobre el reenvío de mensajes mediante [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage), [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea)y funciones relacionadas con mensajes táctiles.</span><span class="sxs-lookup"><span data-stu-id="6494e-104">This section describes considerations about forwarding messages using [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage), [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea), and related functions with touch messages.</span></span>

<span data-ttu-id="6494e-105">Si se reenvía un mensaje táctil mediante [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage), [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea)u otra función relacionada, se cierra el controlador de entrada táctil.</span><span class="sxs-lookup"><span data-stu-id="6494e-105">If a touch message is forwarded using [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage), [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea), or some other related function, the touch input handle is closed.</span></span> <span data-ttu-id="6494e-106">Si ha recuperado la información contenida por un identificador de entrada táctil a través de una llamada a [**GetTouchInputInfo**](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo), los datos seguirán siendo válidos hasta que libere la memoria.</span><span class="sxs-lookup"><span data-stu-id="6494e-106">If you have retrieved the information contained referenced by a touch input handle through a call to [**GetTouchInputInfo**](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo), that data will remain valid until you free the memory.</span></span>

<span data-ttu-id="6494e-107">Una aplicación que recibe mensajes táctiles reenviados a través de uno de estos mecanismos posee el identificador de entrada táctil que recibe en el mensaje *lParam* y es responsable de cerrarlo.</span><span class="sxs-lookup"><span data-stu-id="6494e-107">An application that receives touch messages forwarded through one of these mechanisms owns the touch input handle it receives in the message *LPARAM* and is responsible for closing it.</span></span> <span data-ttu-id="6494e-108">Si no cierra el identificador con una llamada a [**CloseTouchInputHandle**](/windows/desktop/api/winuser/nf-winuser-closetouchinputhandle), pasa el mensaje a [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca)o reenvía el mensaje mediante [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage), [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea)o alguna función relacionada, se producirá una fuga de memoria.</span><span class="sxs-lookup"><span data-stu-id="6494e-108">If you don't close the handle with a call to [**CloseTouchInputHandle**](/windows/desktop/api/winuser/nf-winuser-closetouchinputhandle), pass the message to [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca), or forward the message using [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage), [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea), or some related function, you will have a memory leak.</span></span>

> [!Note]  
> <span data-ttu-id="6494e-109">Los mensajes táctiles están sujetos a las reglas de aislamiento de privilegios de interfaz de usuario (UIPI) normales cuando se reenvían.</span><span class="sxs-lookup"><span data-stu-id="6494e-109">Touch messages are subject to normal User Interface Privilege Isolation (UIPI) rules when they are forwarded.</span></span>

 

## <a name="functions-related-to-sendmessage-and-postmessage"></a><span data-ttu-id="6494e-110">Funciones relacionadas con SendMessage y PostMessage</span><span class="sxs-lookup"><span data-stu-id="6494e-110">Functions related to SendMessage and PostMessage</span></span>

<span data-ttu-id="6494e-111">Las siguientes funciones que pueden afectar al estado del controlador de entrada táctil.</span><span class="sxs-lookup"><span data-stu-id="6494e-111">The following functions that can affect the state of the touch input handle.</span></span>

-   [<span data-ttu-id="6494e-112">SendMessage</span><span class="sxs-lookup"><span data-stu-id="6494e-112">SendMessage</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
-   [<span data-ttu-id="6494e-113">PostMessage</span><span class="sxs-lookup"><span data-stu-id="6494e-113">PostMessage</span></span>](/windows/win32/api/winuser/nf-winuser-postmessagea)
-   <span data-ttu-id="6494e-114">SendNotifyMessage</span><span class="sxs-lookup"><span data-stu-id="6494e-114">SendNotifyMessage</span></span>
-   <span data-ttu-id="6494e-115">SendMessageCallback</span><span class="sxs-lookup"><span data-stu-id="6494e-115">SendMessageCallback</span></span>
-   <span data-ttu-id="6494e-116">SendMessageTimeout</span><span class="sxs-lookup"><span data-stu-id="6494e-116">SendMessageTimeout</span></span>
-   <span data-ttu-id="6494e-117">PostThreadMessage</span><span class="sxs-lookup"><span data-stu-id="6494e-117">PostThreadMessage</span></span>

## <a name="related-topics"></a><span data-ttu-id="6494e-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6494e-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6494e-119">Funciones</span><span class="sxs-lookup"><span data-stu-id="6494e-119">Functions</span></span>](mtfunctions.md)
</dt> <dt>

[<span data-ttu-id="6494e-120">DefWindowProc</span><span class="sxs-lookup"><span data-stu-id="6494e-120">DefWindowProc</span></span>](/windows/win32/api/winuser/nf-winuser-defwindowproca)
</dt> </dl>

 

 