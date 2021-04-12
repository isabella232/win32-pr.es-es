---
title: Parámetro de duración del mensaje
description: Las aplicaciones suelen usar ventanas emergentes para mostrar brevemente mensajes de notificación importantes para el usuario. Una aplicación crea la ventana, la muestra para una duración definida por la aplicación y, a continuación, destruye la ventana.
ms.assetid: a3f7a8d8-78e7-4fb0-8ee2-bd9341857153
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2a99a43ace763da94944da334b0865c768cc920
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420840"
---
# <a name="message-duration-parameter"></a><span data-ttu-id="7352d-104">Parámetro de duración del mensaje</span><span class="sxs-lookup"><span data-stu-id="7352d-104">Message duration parameter</span></span>

<span data-ttu-id="7352d-105">Las aplicaciones suelen usar ventanas emergentes para mostrar brevemente mensajes de notificación importantes para el usuario.</span><span class="sxs-lookup"><span data-stu-id="7352d-105">Applications typically use pop-up windows to briefly display important notification messages to the user.</span></span> <span data-ttu-id="7352d-106">Una aplicación crea la ventana, la muestra para una duración definida por la aplicación y, a continuación, destruye la ventana.</span><span class="sxs-lookup"><span data-stu-id="7352d-106">An application creates the window, displays it for an application-defined duration, and then destroys the window.</span></span>

<span data-ttu-id="7352d-107">Dado que los usuarios con discapacidades visuales o condiciones cognitivas pueden necesitar más tiempo para leer los elementos emergentes de notificación, las aplicaciones no deben codificar la duración.</span><span class="sxs-lookup"><span data-stu-id="7352d-107">Because users with visual impairments or cognitive conditions might need more time to read notification pop-ups, applications should not hard code the duration.</span></span> <span data-ttu-id="7352d-108">En su lugar, una aplicación debe establecer la duración según el valor del parámetro del sistema **SPI \_ GETMESSAGEDURATION** .</span><span class="sxs-lookup"><span data-stu-id="7352d-108">Instead, an application should set the duration based on the value of the **SPI\_GETMESSAGEDURATION** system parameter.</span></span> <span data-ttu-id="7352d-109">Para recuperar este parámetro, use la función [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) .</span><span class="sxs-lookup"><span data-stu-id="7352d-109">To retrieve this parameter, use the [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) function.</span></span>

<span data-ttu-id="7352d-110">Las aplicaciones de tecnología de asistencia pueden establecer la duración del mensaje, en función de los datos proporcionados por el usuario, estableciendo el parámetro del sistema **SPI \_ SETMESSAGEDURATION** .</span><span class="sxs-lookup"><span data-stu-id="7352d-110">Assistive technology applications can set the message duration, based on user input, by setting the **SPI\_SETMESSAGEDURATION** system parameter.</span></span>

 

 