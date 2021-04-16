---
description: .
ms.assetid: 753d1c5b-e824-4fc3-b731-ae9cb16c0e16
title: Funciones de mensaje (ventanas y mensajes)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29e635f61b92af4080f4283ba08b02fda387d482
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706341"
---
# <a name="message-functions-windows-and-messages"></a><span data-ttu-id="668b9-103">Funciones de mensaje (ventanas y mensajes)</span><span class="sxs-lookup"><span data-stu-id="668b9-103">Message Functions (Windows and Messages)</span></span>

-   [<span data-ttu-id="668b9-104">**BroadcastSystemMessage**</span><span class="sxs-lookup"><span data-stu-id="668b9-104">**BroadcastSystemMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-broadcastsystemmessage)
-   [<span data-ttu-id="668b9-105">**BroadcastSystemMessageEx**</span><span class="sxs-lookup"><span data-stu-id="668b9-105">**BroadcastSystemMessageEx**</span></span>](/windows/win32/api/winuser/nf-winuser-broadcastsystemmessageexa)
-   [<span data-ttu-id="668b9-106">**DispatchMessage**</span><span class="sxs-lookup"><span data-stu-id="668b9-106">**DispatchMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-dispatchmessage)
-   [<span data-ttu-id="668b9-107">**GetInputState**</span><span class="sxs-lookup"><span data-stu-id="668b9-107">**GetInputState**</span></span>](/windows/win32/api/winuser/nf-winuser-getinputstate)
-   [<span data-ttu-id="668b9-108">**GetMessage**</span><span class="sxs-lookup"><span data-stu-id="668b9-108">**GetMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-getmessage)
-   [<span data-ttu-id="668b9-109">**GetMessageExtraInfo**</span><span class="sxs-lookup"><span data-stu-id="668b9-109">**GetMessageExtraInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-getmessageextrainfo)
-   [<span data-ttu-id="668b9-110">**GetMessagePos**</span><span class="sxs-lookup"><span data-stu-id="668b9-110">**GetMessagePos**</span></span>](/windows/win32/api/winuser/nf-winuser-getmessagepos)
-   [<span data-ttu-id="668b9-111">**GetMessageTime**</span><span class="sxs-lookup"><span data-stu-id="668b9-111">**GetMessageTime**</span></span>](/windows/win32/api/winuser/nf-winuser-getmessagetime)
-   [<span data-ttu-id="668b9-112">**GetQueueStatus**</span><span class="sxs-lookup"><span data-stu-id="668b9-112">**GetQueueStatus**</span></span>](/windows/win32/api/winuser/nf-winuser-getqueuestatus)
-   [<span data-ttu-id="668b9-113">**InSendMessage**</span><span class="sxs-lookup"><span data-stu-id="668b9-113">**InSendMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-insendmessage)
-   [<span data-ttu-id="668b9-114">**InSendMessageEx**</span><span class="sxs-lookup"><span data-stu-id="668b9-114">**InSendMessageEx**</span></span>](/windows/win32/api/winuser/nf-winuser-insendmessageex)
-   [<span data-ttu-id="668b9-115">**PeekMessage**</span><span class="sxs-lookup"><span data-stu-id="668b9-115">**PeekMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-peekmessagea)
-   [<span data-ttu-id="668b9-116">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="668b9-116">**PostMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-postmessagea)
-   [<span data-ttu-id="668b9-117">**PostQuitMessage**</span><span class="sxs-lookup"><span data-stu-id="668b9-117">**PostQuitMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-postquitmessage)
-   [<span data-ttu-id="668b9-118">**PostThreadMessage**</span><span class="sxs-lookup"><span data-stu-id="668b9-118">**PostThreadMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-postthreadmessagea)
-   [<span data-ttu-id="668b9-119">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="668b9-119">**RegisterWindowMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea)
-   [<span data-ttu-id="668b9-120">**ReplyMessage**</span><span class="sxs-lookup"><span data-stu-id="668b9-120">**ReplyMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-replymessage)
-   [<span data-ttu-id="668b9-121">*SendAsyncProc*</span><span class="sxs-lookup"><span data-stu-id="668b9-121">*SendAsyncProc*</span></span>](/windows/win32/api/winuser/nc-winuser-sendasyncproc)
-   [<span data-ttu-id="668b9-122">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="668b9-122">**SendMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-sendmessage)
-   [<span data-ttu-id="668b9-123">**SendMessageCallback**</span><span class="sxs-lookup"><span data-stu-id="668b9-123">**SendMessageCallback**</span></span>](/windows/win32/api/winuser/nf-winuser-sendmessagecallbacka)
-   [<span data-ttu-id="668b9-124">**SendMessageTimeout**</span><span class="sxs-lookup"><span data-stu-id="668b9-124">**SendMessageTimeout**</span></span>](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta)
-   [<span data-ttu-id="668b9-125">**SendNotifyMessage**</span><span class="sxs-lookup"><span data-stu-id="668b9-125">**SendNotifyMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-sendnotifymessagea)
-   [<span data-ttu-id="668b9-126">**SetMessageExtraInfo**</span><span class="sxs-lookup"><span data-stu-id="668b9-126">**SetMessageExtraInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-setmessageextrainfo)
-   [<span data-ttu-id="668b9-127">**TranslateMessage**</span><span class="sxs-lookup"><span data-stu-id="668b9-127">**TranslateMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-translatemessage)
-   [<span data-ttu-id="668b9-128">**WaitMessage**</span><span class="sxs-lookup"><span data-stu-id="668b9-128">**WaitMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-waitmessage)

 

 
