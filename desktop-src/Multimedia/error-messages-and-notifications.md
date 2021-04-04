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
# <a name="error-messages-and-notifications"></a><span data-ttu-id="e2bc5-104">Mensajes de error y notificaciones</span><span class="sxs-lookup"><span data-stu-id="e2bc5-104">Error Messages and Notifications</span></span>

<span data-ttu-id="e2bc5-105">MCIWnd usa MCI para controlar los dispositivos que reproducen y graban datos multimedia.</span><span class="sxs-lookup"><span data-stu-id="e2bc5-105">MCIWnd uses MCI to control the devices that play and record multimedia data.</span></span> <span data-ttu-id="e2bc5-106">En general, MCIWnd muestra los errores de MCI en un cuadro de diálogo de error.</span><span class="sxs-lookup"><span data-stu-id="e2bc5-106">In general, MCIWnd displays MCI errors in an error dialog box.</span></span> <span data-ttu-id="e2bc5-107">Cuando se produce un error en un comando MCI, se genera un error de MCI.</span><span class="sxs-lookup"><span data-stu-id="e2bc5-107">An MCI error is generated whenever an MCI command fails.</span></span> <span data-ttu-id="e2bc5-108">Por ejemplo, si la aplicación intenta reanudar la reproducción en pausa mediante la macro [**MCIWndResume**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) y el dispositivo actual no admite la reanudación, se envía un error al usuario.</span><span class="sxs-lookup"><span data-stu-id="e2bc5-108">For example, if your application tries to resume paused playback by using the [**MCIWndResume**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) macro and the current device does not support resume, an error is reported to the user.</span></span>

<span data-ttu-id="e2bc5-109">MCIWnd permite dos opciones para controlar los mensajes de error:</span><span class="sxs-lookup"><span data-stu-id="e2bc5-109">MCIWnd allows you two choices for handling error messages:</span></span>

-   <span data-ttu-id="e2bc5-110">Puede evitar que los mensajes de error lleguen al usuario.</span><span class="sxs-lookup"><span data-stu-id="e2bc5-110">You can prevent error messages from reaching the user.</span></span> <span data-ttu-id="e2bc5-111">Para evitar que se muestren los mensajes de error de MCI, especifique el estilo de ventana de MCIWNDF \_ NOERRORDLG al crear una instancia de una ventana de MCIWnd mediante la función [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) o [CreateWindowEx](/windows/win32/api/winuser/nf-winuser-createwindowexa) .</span><span class="sxs-lookup"><span data-stu-id="e2bc5-111">To prevent the display of MCI error messages, specify the MCIWNDF\_NOERRORDLG window style when you create an instance of an MCIWnd window by using the [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) or [CreateWindowEx](/windows/win32/api/winuser/nf-winuser-createwindowexa) function.</span></span>
-   <span data-ttu-id="e2bc5-112">Puede redirigirlas a la aplicación para que se muestren.</span><span class="sxs-lookup"><span data-stu-id="e2bc5-112">You can redirect them to your application for display.</span></span> <span data-ttu-id="e2bc5-113">Para redirigir los mensajes de error de MCI a la aplicación, especifique el \_ estilo de ventana de MCIWNDF NOTIFYERROR al crear una instancia de una ventana de MCIWnd mediante **MCIWndCreate** o **CreateWindowEx**.</span><span class="sxs-lookup"><span data-stu-id="e2bc5-113">To redirect MCI error messages to your application, specify the MCIWNDF\_NOTIFYERROR window style when you create an instance of an MCIWnd window by using **MCIWndCreate** or **CreateWindowEx**.</span></span>

<span data-ttu-id="e2bc5-114">Cuando se habilita la notificación de errores, MCIWnd envía cada mensaje de notificación ([**MCIWNDM \_ NOTIFYERROR**](mciwndm-notifyerror.md)) al controlador de mensajes principal del elemento primario de la ventana de MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="e2bc5-114">When error notification is enabled, MCIWnd sends each notification message ([**MCIWNDM\_NOTIFYERROR**](mciwndm-notifyerror.md)) to the main message handler of the parent of the MCIWnd window.</span></span> <span data-ttu-id="e2bc5-115">La aplicación debe tener un controlador de mensajes para procesar los mensajes de notificación que recibe.</span><span class="sxs-lookup"><span data-stu-id="e2bc5-115">Your application must have a message handler to process the notification messages it receives.</span></span>

<span data-ttu-id="e2bc5-116">Puede obtener una descripción textual del mensaje de error de MCI más reciente mediante la macro [**MCIWndGetError**](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror) .</span><span class="sxs-lookup"><span data-stu-id="e2bc5-116">You can obtain a textual description of the most recent MCI error message by using the [**MCIWndGetError**](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror) macro.</span></span> <span data-ttu-id="e2bc5-117">Esta macro devuelve el texto de un búfer definido por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e2bc5-117">This macro returns the text in an application-defined buffer.</span></span> <span data-ttu-id="e2bc5-118">Si la cadena de error es más larga que el búfer, MCIWnd trunca la cadena.</span><span class="sxs-lookup"><span data-stu-id="e2bc5-118">If the error string is longer than the buffer, MCIWnd truncates the string.</span></span>

<span data-ttu-id="e2bc5-119">Puede enrutar todas las notificaciones a otra ventana mediante la macro [**MCIWndSetOwner**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetowner) .</span><span class="sxs-lookup"><span data-stu-id="e2bc5-119">You can route all notifications to another window by using the [**MCIWndSetOwner**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetowner) macro.</span></span>

 

 