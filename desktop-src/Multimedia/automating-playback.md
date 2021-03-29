---
title: Automatizar la reproducción
description: Automatizar la reproducción
ms.assetid: 3aa05a54-58d7-4d14-93ee-459aa860b20e
keywords:
- MCIWndCreate (macro)
- MCIWndPlay (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6097d38b3d468b6de68ee7e11f98f530aff00d2b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779609"
---
# <a name="automating-playback"></a><span data-ttu-id="228b3-105">Automatizar la reproducción</span><span class="sxs-lookup"><span data-stu-id="228b3-105">Automating Playback</span></span>

<span data-ttu-id="228b3-106">Puede automatizar la reproducción en la aplicación mediante [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) y la macro [**MCIWndPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) , junto con la macro [**MCIWndDestroy**](/windows/desktop/api/Vfw/nf-vfw-mciwnddestroy) o [**MCIWndClose**](/windows/desktop/api/Vfw/nf-vfw-mciwndclose) .</span><span class="sxs-lookup"><span data-stu-id="228b3-106">You can automate playback in your application by using [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) and the [**MCIWndPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) macro, along with either the [**MCIWndDestroy**](/windows/desktop/api/Vfw/nf-vfw-mciwnddestroy) or the [**MCIWndClose**](/windows/desktop/api/Vfw/nf-vfw-mciwndclose) macro.</span></span> <span data-ttu-id="228b3-107">Para automatizar la reproducción, especifique los \_ estilos MCIWNDF NOPLAYBAR y MCIWNDF \_ NOTIFYMODE en el parámetro \*\*MCIWndCreate \*\* \* \* dwStyle.</span><span class="sxs-lookup"><span data-stu-id="228b3-107">To automate playback, specify the MCIWNDF\_NOPLAYBAR and MCIWNDF\_NOTIFYMODE styles in the \**MCIWndCreate\*\*\*dwStyle* parameter.</span></span> <span data-ttu-id="228b3-108">Especifique el \_ estilo MCIWNDF NOPLAYBAR para ocultar la barra de herramientas y el \_ estilo MCIWNDF NOTIFYMODE para emitir un mensaje de notificación adecuado cuando el dispositivo deje de reproducirse.</span><span class="sxs-lookup"><span data-stu-id="228b3-108">Specify the MCIWNDF\_NOPLAYBAR style to hide the toolbar, and the MCIWNDF\_NOTIFYMODE style to issue an appropriate notification message when the device stops playing.</span></span>

<span data-ttu-id="228b3-109">Puede reproducir el dispositivo o el archivo especificado en **MCIWndCreate** mediante **MCIWndPlay**.</span><span class="sxs-lookup"><span data-stu-id="228b3-109">You can play the device or file specified in **MCIWndCreate** by using **MCIWndPlay**.</span></span> <span data-ttu-id="228b3-110">La macro MCIWndPlay empieza a reproducir el contenido desde su posición de reproducción actual y continúa hasta el final.</span><span class="sxs-lookup"><span data-stu-id="228b3-110">The MCIWndPlay macro starts playing the content from its current playback position and continues to its end.</span></span>

<span data-ttu-id="228b3-111">Puede destruir o cerrar una ventana de MCIWnd con la macro [**MCIWndDestroy**](/windows/desktop/api/Vfw/nf-vfw-mciwnddestroy) o [**MCIWndClose**](/windows/desktop/api/Vfw/nf-vfw-mciwndclose) .</span><span class="sxs-lookup"><span data-stu-id="228b3-111">You can destroy or close an MCIWnd window by using the [**MCIWndDestroy**](/windows/desktop/api/Vfw/nf-vfw-mciwnddestroy) or [**MCIWndClose**](/windows/desktop/api/Vfw/nf-vfw-mciwndclose) macro.</span></span> <span data-ttu-id="228b3-112">La macro **MCIWndDestroy** cierra el dispositivo o el archivo y destruye la ventana MCIWnd invalidando su identificador.</span><span class="sxs-lookup"><span data-stu-id="228b3-112">The **MCIWndDestroy** macro closes the device or file and destroys the MCIWnd window by invalidating its handle.</span></span> <span data-ttu-id="228b3-113">Si la aplicación puede volver a usar la ventana de MCIWnd, use **MCIWndClose** para cerrar el dispositivo sin destruir la ventana.</span><span class="sxs-lookup"><span data-stu-id="228b3-113">If your application can reuse the MCIWnd window, use **MCIWndClose** to close the device without destroying the window.</span></span>

<span data-ttu-id="228b3-114">La aplicación puede detectar Cuándo deja de reproducirse el dispositivo y cierra automáticamente la ventana.</span><span class="sxs-lookup"><span data-stu-id="228b3-114">Your application can detect when the device stops playing and automatically close the window.</span></span> <span data-ttu-id="228b3-115">Para ello, especifique el estilo MCIWNDF \_ NOTIFYMODE para el parámetro *DwStyle* de [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea).</span><span class="sxs-lookup"><span data-stu-id="228b3-115">To do this, specify the MCIWNDF\_NOTIFYMODE style for the *dwStyle* parameter of [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea).</span></span> <span data-ttu-id="228b3-116">Esto hace que el dispositivo envíe un mensaje de [**MCIWNDM \_ NOTIFYMODE**](mciwndm-notifymode.md) cada vez que cambie de modo.</span><span class="sxs-lookup"><span data-stu-id="228b3-116">This causes the device to send a [**MCIWNDM\_NOTIFYMODE**](mciwndm-notifymode.md) message whenever it changes modes.</span></span> <span data-ttu-id="228b3-117">La aplicación puede capturar este mensaje para determinar si el dispositivo ha dejado de reproducirse.</span><span class="sxs-lookup"><span data-stu-id="228b3-117">Your application can trap this message to determine whether the device has stopped playing.</span></span> <span data-ttu-id="228b3-118">Cuando el dispositivo deja de reproducirse, la aplicación cierra la ventana.</span><span class="sxs-lookup"><span data-stu-id="228b3-118">When the device stops playing, the application closes the window.</span></span>

 

 




