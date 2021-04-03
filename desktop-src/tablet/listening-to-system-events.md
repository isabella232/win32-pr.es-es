---
description: Las aplicaciones pueden escuchar eventos del sistema mediante el objeto InkCollector y escuchando el evento SystemGesture en él.
ms.assetid: 141afdbe-b5a7-47dc-b505-46089a5eda75
title: Escuchar eventos del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1429e652140cc9624d324401edef7817dad40ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083402"
---
# <a name="listening-to-system-events"></a><span data-ttu-id="b0d9c-103">Escuchar eventos del sistema</span><span class="sxs-lookup"><span data-stu-id="b0d9c-103">Listening to System Events</span></span>

<span data-ttu-id="b0d9c-104">Las aplicaciones pueden escuchar eventos del sistema mediante el objeto [**InkCollector**](inkcollector-class.md) y escuchando el evento [**SystemGesture**](inkcollector-systemgesture.md) en él.</span><span class="sxs-lookup"><span data-stu-id="b0d9c-104">Applications can listen to system events by using the [**InkCollector**](inkcollector-class.md) object and listening for the [**SystemGesture**](inkcollector-systemgesture.md) event on it.</span></span> <span data-ttu-id="b0d9c-105">Puede establecer los eventos a los que escuchará una aplicación.</span><span class="sxs-lookup"><span data-stu-id="b0d9c-105">You can set which events an application listens to.</span></span> <span data-ttu-id="b0d9c-106">Cuando se produce una acción del lápiz de Tablet PC, el evento **SystemGesture** correspondiente se envía a la aplicación en su objeto **InkCollector** .</span><span class="sxs-lookup"><span data-stu-id="b0d9c-106">When a tablet pen action occurs, the corresponding **SystemGesture** event is sent to the application on its **InkCollector** object.</span></span> <span data-ttu-id="b0d9c-107">Una aplicación puede cancelar el mensaje del mouse que corresponde a un evento **SystemGesture** determinado cuando recibe el evento.</span><span class="sxs-lookup"><span data-stu-id="b0d9c-107">An application can cancel the mouse message that corresponds to a given **SystemGesture** event when it receives the event.</span></span> <span data-ttu-id="b0d9c-108">Para obtener más información sobre cómo cancelar los mensajes del mouse, vea evento **SystemGesture** .</span><span class="sxs-lookup"><span data-stu-id="b0d9c-108">For details about canceling mouse messages, see **SystemGesture** event.</span></span>

 

 



