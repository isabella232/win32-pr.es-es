---
title: Cuándo responder al mensaje de WM_GETOBJECT
description: Si una aplicación admite Microsoft Active Accessibility o la automatización de la interfaz de usuario para un elemento de la interfaz de usuario, la aplicación no debe responder al mensaje de la GETOBJECT de WM \_ antes de que el objeto que representa el elemento de la interfaz de usuario esté completamente inicializado o después de que la aplicación haya empezado a cerrarse.
ms.assetid: cc99f7ef-1eb6-40c4-9ec0-8fb18cb4a3e5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18cfa8d6604a13e84ffa89bf1fcf93d5d13e66e4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488138"
---
# <a name="when-to-respond-to-the-wm_getobject-message"></a><span data-ttu-id="fdd4c-103">Cuándo responder al mensaje de la \_ GETOBJECT de WM</span><span class="sxs-lookup"><span data-stu-id="fdd4c-103">When to Respond to the WM\_GETOBJECT Message</span></span>

<span data-ttu-id="fdd4c-104">Si una aplicación admite Microsoft Active Accessibility o la automatización de la interfaz de usuario para un elemento de la interfaz de usuario, la aplicación no debe responder al mensaje de la [**\_ GETOBJECT de WM**](wm-getobject.md) antes de que el objeto que representa el elemento de la interfaz de usuario esté completamente inicializado o después de que la aplicación haya empezado a cerrarse.</span><span class="sxs-lookup"><span data-stu-id="fdd4c-104">If an application supports Microsoft Active Accessibility or UI Automation for a UI element, the application must not respond to the [**WM\_GETOBJECT**](wm-getobject.md) message before the object that represents the UI element is fully initialized, or after the application has begun to close.</span></span> <span data-ttu-id="fdd4c-105">Cuando una aplicación crea una ventana nueva, el sistema genera el [**objeto de evento \_ \_ Create**](event-constants.md) WinEvent para notificar a los clientes antes de enviar el mensaje de [**\_ creación de WM**](/windows/desktop/winmsg/wm-create) al procedimiento de ventana de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="fdd4c-105">When an application creates a new window, the system raises the [**EVENT\_OBJECT\_CREATE**](event-constants.md) WinEvent to notify clients before sending the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message to the application's window procedure.</span></span> <span data-ttu-id="fdd4c-106">Dado que muchas aplicaciones usan **WM \_ Create** para iniciar el proceso de inicialización, cualquier implementación de accesibilidad de un elemento de la interfaz de usuario no responde al mensaje de la [**\_ GETOBJECT de WM**](wm-getobject.md) hasta que la aplicación haya finalizado el procesamiento del mensaje de **\_ creación de WM** .</span><span class="sxs-lookup"><span data-stu-id="fdd4c-106">Because many applications use **WM\_CREATE** to start the initialization process, any accessibility implementation of a UI element does not respond to the [**WM\_GETOBJECT**](wm-getobject.md) message until after the application has finished processing the **WM\_CREATE** message.</span></span>

 

 