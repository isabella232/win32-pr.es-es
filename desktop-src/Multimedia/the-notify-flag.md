---
title: Marca de notificación
description: Marca de notificación
ms.assetid: ed5dbb0b-ce4d-4bda-8daa-c62cfda717d1
keywords:
- MCI_NOTIFY marca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9093e539becb4ba2f09b48d628a57d8243bd837c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420673"
---
# <a name="the-notify-flag"></a><span data-ttu-id="ea906-104">Marca de notificación</span><span class="sxs-lookup"><span data-stu-id="ea906-104">The Notify Flag</span></span>

<span data-ttu-id="ea906-105">La marca "notificar" (notificación de MCI \_ ) indica al dispositivo que envíe un mensaje [**mm MCINOTIFY**](mm-mcinotify.md) cuando el dispositivo completa una acción.</span><span class="sxs-lookup"><span data-stu-id="ea906-105">The "notify" (MCI\_NOTIFY) flag directs the device to post an [**MM MCINOTIFY**](mm-mcinotify.md) message when the device completes an action.</span></span> <span data-ttu-id="ea906-106">La aplicación debe tener un procedimiento de ventana para procesar el \_ mensaje de MCINOTIFY mm para que la notificación surta efecto.</span><span class="sxs-lookup"><span data-stu-id="ea906-106">Your application must have a window procedure to process the MM\_MCINOTIFY message for notification to have any effect.</span></span> <span data-ttu-id="ea906-107">Un \_ mensaje de MCINOTIFY mm indica que el procesamiento de un comando se ha completado, pero no indica si el comando se completó correctamente, produjo un error o se sustituyó o anuló.</span><span class="sxs-lookup"><span data-stu-id="ea906-107">An MM\_MCINOTIFY message indicates that the processing of a command has completed, but it does not indicate whether the command was completed successfully, failed, or was superseded or aborted.</span></span>

<span data-ttu-id="ea906-108">La aplicación especifica el identificador de la ventana de destino para el mensaje cuando emite un comando.</span><span class="sxs-lookup"><span data-stu-id="ea906-108">The application specifies the handle to the destination window for the message when it issues a command.</span></span> <span data-ttu-id="ea906-109">En la interfaz de cadena de comandos, este identificador es el último parámetro de la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ea906-109">In the command-string interface, this handle is the last parameter of the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function.</span></span> <span data-ttu-id="ea906-110">En la interfaz de mensaje de comando, el identificador se especifica en la palabra de orden inferior del miembro **dwCallBack** de la estructura enviada con el mensaje de comando.</span><span class="sxs-lookup"><span data-stu-id="ea906-110">In the command-message interface, the handle is specified in the low-order word of the **dwCallBack** member of the structure sent with the command message.</span></span> <span data-ttu-id="ea906-111">(Cada estructura asociada con un mensaje de comando contiene este miembro).</span><span class="sxs-lookup"><span data-stu-id="ea906-111">(Every structure associated with a command message contains this member.)</span></span>

 

 