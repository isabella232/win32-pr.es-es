---
description: El objeto de solicitud se crea mediante COM CoCreateInstance y expone una interfaz, ITRequest.
ms.assetid: 1e4c71ce-6846-4e64-9346-455ed82aa458
title: Objeto de solicitud
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c51e81cae01f2624ba863b304c0a5f732b221199
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677799"
---
# <a name="request-object"></a><span data-ttu-id="d7bb6-103">Objeto de solicitud</span><span class="sxs-lookup"><span data-stu-id="d7bb6-103">Request Object</span></span>

<span data-ttu-id="d7bb6-104">El objeto de solicitud se crea mediante COM **CoCreateInstance** y expone una interfaz, [**ITRequest**](/windows/desktop/api/tapi3if/nn-tapi3if-itrequest).</span><span class="sxs-lookup"><span data-stu-id="d7bb6-104">The Request Object is created using COM **CoCreateInstance** and exposes one interface, [**ITRequest**](/windows/desktop/api/tapi3if/nn-tapi3if-itrequest).</span></span> <span data-ttu-id="d7bb6-105">Esta interfaz expone el método [**MakeCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itrequest-makecall) , que permite a una aplicación TAPI 3 usar la telefonía asistida.</span><span class="sxs-lookup"><span data-stu-id="d7bb6-105">This interface exposes the [**MakeCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itrequest-makecall) method, which allows a TAPI 3 application to use Assisted Telephony.</span></span> <span data-ttu-id="d7bb6-106">La telefonía asistida proporciona aplicaciones habilitadas para telefonía con un mecanismo sencillo para realizar llamadas telefónicas sin necesidad de que el desarrollador se convierta completamente en una llamada de telefonía.</span><span class="sxs-lookup"><span data-stu-id="d7bb6-106">Assisted Telephony provides telephony-enabled applications with a simple mechanism for making phone calls without requiring the developer to become fully literate in telephony.</span></span>

<span data-ttu-id="d7bb6-107">Por ejemplo, una aplicación de hoja de cálculo puede Agregar un botón "make Call" con telefonía asistida sin implementar los controles más elaborados disponibles en una aplicación TAPI completa.</span><span class="sxs-lookup"><span data-stu-id="d7bb6-107">For example, a spreadsheet application can add a "Make Call" button using Assisted Telephony without implementing the more elaborate controls available in a full TAPI application.</span></span>

<span data-ttu-id="d7bb6-108">Consulte la [Introducción a la telefonía asistida](assisted-telephony-overview.md) para obtener información adicional.</span><span class="sxs-lookup"><span data-stu-id="d7bb6-108">See the [Assisted Telephony Overview](assisted-telephony-overview.md) for additional information.</span></span>

 

 



