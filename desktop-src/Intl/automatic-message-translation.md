---
description: Las aplicaciones que usan las funciones de la API de juegos de caracteres y Unicode suelen usar la misma clase de ventana. El sistema operativo traduce de forma transparente los mensajes entre ventanas de clases diferentes.
ms.assetid: 68e9839b-39f8-411a-8ae4-4a627c667cae
title: Traducción automática de mensajes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20b02a5c5a4951189333608aa448f09ba9c6866d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809524"
---
# <a name="automatic-message-translation"></a><span data-ttu-id="825a7-104">Traducción automática de mensajes</span><span class="sxs-lookup"><span data-stu-id="825a7-104">Automatic Message Translation</span></span>

<span data-ttu-id="825a7-105">Las aplicaciones que usan las funciones de la API de juegos de caracteres y Unicode suelen usar la misma clase de ventana.</span><span class="sxs-lookup"><span data-stu-id="825a7-105">Applications using the Unicode and character set API functions generally use the same window class.</span></span> <span data-ttu-id="825a7-106">El sistema operativo traduce de forma transparente los mensajes entre ventanas de clases diferentes.</span><span class="sxs-lookup"><span data-stu-id="825a7-106">The operating system transparently translates messages between windows of different classes.</span></span>

<span data-ttu-id="825a7-107">Una función de ventana se implementa para recibir mensajes en formato de página de códigos Unicode o Windows.</span><span class="sxs-lookup"><span data-stu-id="825a7-107">A window function is implemented to receive messages in Unicode or Windows code page format.</span></span> <span data-ttu-id="825a7-108">La función de ventana puede enviar mensajes o llamar a funciones de cualquier tipo.</span><span class="sxs-lookup"><span data-stu-id="825a7-108">The window function can send messages or call functions of either type.</span></span>

<span data-ttu-id="825a7-109">Los mensajes siguientes tienen argumentos de texto y están sujetos a la conversión de texto automática.</span><span class="sxs-lookup"><span data-stu-id="825a7-109">The following messages have text arguments and are subject to automatic text translation.</span></span> <span data-ttu-id="825a7-110">Para obtener información sobre la traducción automática, consulte [subclases y traducción automática de mensajes](subclassing-and-automatic-message-translation.md).</span><span class="sxs-lookup"><span data-stu-id="825a7-110">For information about automatic translation, see [Subclassing and Automatic Message Translation](subclassing-and-automatic-message-translation.md).</span></span>

<dl>

[<span data-ttu-id="825a7-111">CB \_ ADDSTRING</span><span class="sxs-lookup"><span data-stu-id="825a7-111">CB\_ADDSTRING</span></span>](../controls/cb-addstring.md)  
[<span data-ttu-id="825a7-112">\_directorio CB</span><span class="sxs-lookup"><span data-stu-id="825a7-112">CB\_DIR</span></span>](../controls/cb-dir.md)  
[<span data-ttu-id="825a7-113">CB \_ FINDSTRING</span><span class="sxs-lookup"><span data-stu-id="825a7-113">CB\_FINDSTRING</span></span>](../controls/cb-findstring.md)  
[<span data-ttu-id="825a7-114">CB \_ GETLBTEXT</span><span class="sxs-lookup"><span data-stu-id="825a7-114">CB\_GETLBTEXT</span></span>](../controls/cb-getlbtext.md)  
[<span data-ttu-id="825a7-115">CB \_ INSERTSTRING</span><span class="sxs-lookup"><span data-stu-id="825a7-115">CB\_INSERTSTRING</span></span>](../controls/cb-insertstring.md)  
[<span data-ttu-id="825a7-116">CB \_ SELECTSTRING</span><span class="sxs-lookup"><span data-stu-id="825a7-116">CB\_SELECTSTRING</span></span>](../controls/cb-selectstring.md)  
[<span data-ttu-id="825a7-117">\_GETLINE em</span><span class="sxs-lookup"><span data-stu-id="825a7-117">EM\_GETLINE</span></span>](../controls/em-getline.md)  
[<span data-ttu-id="825a7-118">\_REPLACESEL em</span><span class="sxs-lookup"><span data-stu-id="825a7-118">EM\_REPLACESEL</span></span>](../controls/em-replacesel.md)  
[<span data-ttu-id="825a7-119">\_SETPASSWORDCHAR em</span><span class="sxs-lookup"><span data-stu-id="825a7-119">EM\_SETPASSWORDCHAR</span></span>](../controls/em-setpasswordchar.md)  
[<span data-ttu-id="825a7-120">LB \_ ADDFILE</span><span class="sxs-lookup"><span data-stu-id="825a7-120">LB\_ADDFILE</span></span>](../controls/lb-addfile.md)  
[<span data-ttu-id="825a7-121">LB \_ ADDSTRING</span><span class="sxs-lookup"><span data-stu-id="825a7-121">LB\_ADDSTRING</span></span>](../controls/lb-addstring.md)  
[<span data-ttu-id="825a7-122">DIR de LB \_</span><span class="sxs-lookup"><span data-stu-id="825a7-122">LB\_DIR</span></span>](../controls/lb-dir.md)  
[<span data-ttu-id="825a7-123">LB \_ FINDSTRING</span><span class="sxs-lookup"><span data-stu-id="825a7-123">LB\_FINDSTRING</span></span>](../controls/lb-findstring.md)  
[<span data-ttu-id="825a7-124">\_apgettext GETTEXT</span><span class="sxs-lookup"><span data-stu-id="825a7-124">LB\_GETTEXT</span></span>](../controls/lb-gettext.md)  
[<span data-ttu-id="825a7-125">LB \_ INSERTSTRING</span><span class="sxs-lookup"><span data-stu-id="825a7-125">LB\_INSERTSTRING</span></span>](../controls/lb-insertstring.md)  
[<span data-ttu-id="825a7-126">LB \_ SELECTSTRING</span><span class="sxs-lookup"><span data-stu-id="825a7-126">LB\_SELECTSTRING</span></span>](../controls/lb-selectstring.md)  
[<span data-ttu-id="825a7-127">ASKCBFORMATNAME de WM \_</span><span class="sxs-lookup"><span data-stu-id="825a7-127">WM\_ASKCBFORMATNAME</span></span>](../dataxchg/wm-askcbformatname.md)  
[<span data-ttu-id="825a7-128">carácter de WM \_</span><span class="sxs-lookup"><span data-stu-id="825a7-128">WM\_CHAR</span></span>](../inputdev/wm-char.md)  
[<span data-ttu-id="825a7-129">CHARTOITEM de WM \_</span><span class="sxs-lookup"><span data-stu-id="825a7-129">WM\_CHARTOITEM</span></span>](../controls/wm-chartoitem.md)  
[<span data-ttu-id="825a7-130">creación de WM \_</span><span class="sxs-lookup"><span data-stu-id="825a7-130">WM\_CREATE</span></span>](../winmsg/wm-create.md)  
[<span data-ttu-id="825a7-131">DEADCHAR de WM \_</span><span class="sxs-lookup"><span data-stu-id="825a7-131">WM\_DEADCHAR</span></span>](../inputdev/wm-deadchar.md)  
[<span data-ttu-id="825a7-132">DEVMODECHANGE de WM \_</span><span class="sxs-lookup"><span data-stu-id="825a7-132">WM\_DEVMODECHANGE</span></span>](../gdi/wm-devmodechange.md)  
[<span data-ttu-id="825a7-133">GETTEXT de WM \_</span><span class="sxs-lookup"><span data-stu-id="825a7-133">WM\_GETTEXT</span></span>](../winmsg/wm-gettext.md)  
[<span data-ttu-id="825a7-134">MDICREATE de WM \_</span><span class="sxs-lookup"><span data-stu-id="825a7-134">WM\_MDICREATE</span></span>](../winmsg/wm-mdicreate.md)  
[<span data-ttu-id="825a7-135">MENUCHAR de WM \_</span><span class="sxs-lookup"><span data-stu-id="825a7-135">WM\_MENUCHAR</span></span>](../menurc/wm-menuchar.md)  
[<span data-ttu-id="825a7-136">NCCREATE de WM \_</span><span class="sxs-lookup"><span data-stu-id="825a7-136">WM\_NCCREATE</span></span>](../winmsg/wm-nccreate.md)  
[<span data-ttu-id="825a7-137">SETTEXT de WM \_</span><span class="sxs-lookup"><span data-stu-id="825a7-137">WM\_SETTEXT</span></span>](../winmsg/wm-settext.md)  
[<span data-ttu-id="825a7-138">SYSCHAR de WM \_</span><span class="sxs-lookup"><span data-stu-id="825a7-138">WM\_SYSCHAR</span></span>](../menurc/wm-syschar.md)  
[<span data-ttu-id="825a7-139">SYSDEADCHAR de WM \_</span><span class="sxs-lookup"><span data-stu-id="825a7-139">WM\_SYSDEADCHAR</span></span>](../inputdev/wm-sysdeadchar.md)  
[<span data-ttu-id="825a7-140">WININICHANGE de WM \_</span><span class="sxs-lookup"><span data-stu-id="825a7-140">WM\_WININICHANGE</span></span>](../winmsg/wm-wininichange.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="825a7-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="825a7-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="825a7-142">Unicode en la API de Windows</span><span class="sxs-lookup"><span data-stu-id="825a7-142">Unicode in the Windows API</span></span>](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
