---
description: Los mensajes de dispositivo son mensajes del sistema que notifican a las aplicaciones y otras características de los eventos de cambio de dispositivo.
ms.assetid: 4d1ace87-2d02-4ba4-9bcc-da86cf3481db
title: Mensajes del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e22fe5b9f8b3f9fcc2a075767aa684bd92962f32
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659665"
---
# <a name="device-messages"></a><span data-ttu-id="74868-103">Mensajes del dispositivo</span><span class="sxs-lookup"><span data-stu-id="74868-103">Device Messages</span></span>

<span data-ttu-id="74868-104">Los mensajes de dispositivo son mensajes del sistema que notifican a las aplicaciones y otras características de los eventos de cambio de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="74868-104">Device messages are system messages that notify applications and other features of device change events.</span></span> <span data-ttu-id="74868-105">Estos eventos se producen siempre que el sistema detecta un cambio en el hardware del sistema, por ejemplo, cuando el usuario acopla y desacopla un equipo portátil, o inserta o quita un dispositivo como una tarjeta PCMCIA.</span><span class="sxs-lookup"><span data-stu-id="74868-105">These events occur whenever the system detects a change to the system hardware, such as when the user docks and undocks a laptop computer, or inserts or removes a device such as a PCMCIA card.</span></span> <span data-ttu-id="74868-106">Los eventos de dispositivo pueden producirse mientras el sistema se está ejecutando o cuando el sistema reanuda la operación después de suspenderse temporalmente.</span><span class="sxs-lookup"><span data-stu-id="74868-106">Device events can occur while the system is running or when the system resumes operation after temporarily being suspended.</span></span>

<span data-ttu-id="74868-107">Para asegurarse de que las aplicaciones no pierdan datos cuando los dispositivos dejen de estar disponibles, el sistema supervisa la configuración de hardware y envía mensajes de dispositivo a las aplicaciones para notificar los cambios y dar la oportunidad de prepararse para los cambios antes de que se produzcan.</span><span class="sxs-lookup"><span data-stu-id="74868-107">To help ensure that applications do not lose data when devices become unavailable, the system monitors the hardware configuration and sends device messages to the applications to notify them of the changes and to give them the opportunity to prepare for the changes before they occur.</span></span>

<span data-ttu-id="74868-108">Para cada evento de dispositivo, el sistema difunde un mensaje de [**\_ DEVICECHANGE de WM**](wm-devicechange.md) a todas las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="74868-108">For each device event, the system broadcasts a [**WM\_DEVICECHANGE**](wm-devicechange.md) message to all applications.</span></span> <span data-ttu-id="74868-109">En este mensaje, el parámetro *wParam* identifica el [tipo de evento de dispositivo](device-event-types.md) y el parámetro *lParam* es un puntero a datos específicos del evento.</span><span class="sxs-lookup"><span data-stu-id="74868-109">In this message, the *wParam* parameter identifies the [device event type](device-event-types.md) and the *lParam* parameter is a pointer to event-specific data.</span></span>

 

 



