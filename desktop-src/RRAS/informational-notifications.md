---
title: Notificaciones informativas
description: Para los Estados de conexión conocidos como Estados en ejecución, no se requiere ninguna acción del controlador de notificación a menos que se produzca un error.
ms.assetid: 3f5ea9e0-f75a-4b02-a0dc-86cb5012c242
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d6223c808309fcac3afc563f02c160412c80c88
ms.sourcegitcommit: dc13cc13522097188392392d85f99de48a213984
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/28/2020
ms.locfileid: "104487362"
---
# <a name="informational-notifications"></a><span data-ttu-id="5f0bf-103">Notificaciones informativas</span><span class="sxs-lookup"><span data-stu-id="5f0bf-103">Informational Notifications</span></span>

<span data-ttu-id="5f0bf-104">Para los [Estados de conexión](connection-states.md) conocidos como Estados en ejecución, no se requiere ninguna acción del controlador de notificación a menos que se produzca un error.</span><span class="sxs-lookup"><span data-stu-id="5f0bf-104">For the [connection states](connection-states.md) known as running states, no action is required of the notification handler unless an error occurs.</span></span> <span data-ttu-id="5f0bf-105">Los Estados de ejecución se producen durante las partes de la operación de conexión que RAS administra automáticamente, como la conexión a los dispositivos necesarios, la autenticación del usuario y la espera de una devolución de llamada desde el servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="5f0bf-105">Running states occur during the parts of the connection operation that RAS handles automatically, such as connecting to the necessary devices, authenticating the user, and waiting for a callback from the remote server.</span></span> <span data-ttu-id="5f0bf-106">La notificación es simplemente un informe de progreso para el cliente.</span><span class="sxs-lookup"><span data-stu-id="5f0bf-106">The notification is simply a progress report to the client.</span></span>

<span data-ttu-id="5f0bf-107">El cliente puede optar por pasar estas notificaciones informativas al usuario.</span><span class="sxs-lookup"><span data-stu-id="5f0bf-107">The client can choose to pass these informational notifications on to the user.</span></span> <span data-ttu-id="5f0bf-108">En algunos Estados en ejecución, es posible que el cliente desee mostrar información adicional.</span><span class="sxs-lookup"><span data-stu-id="5f0bf-108">In some running states, the client may want to display additional information.</span></span> <span data-ttu-id="5f0bf-109">Por ejemplo, un controlador de notificación que recibe una \_ notificación ConnectDevice de RASCS puede llamar a la función [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) para obtener el nombre y el tipo del dispositivo al que se está conectando.</span><span class="sxs-lookup"><span data-stu-id="5f0bf-109">For example, a notification handler that receives a RASCS\_ConnectDevice notification can call the [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) function to get the name and type of the device being connected to.</span></span> <span data-ttu-id="5f0bf-110">Otro ejemplo es cuando el cliente recibe una notificación de RASCS \_ proyectada.</span><span class="sxs-lookup"><span data-stu-id="5f0bf-110">Another example is when the client receives a RASCS\_Projected notification.</span></span> <span data-ttu-id="5f0bf-111">Esto sucede cuando se ha completado la fase de proyección de RAS de la operación de conexión.</span><span class="sxs-lookup"><span data-stu-id="5f0bf-111">This occurs when the RAS projection phase of the connection operation has been completed.</span></span> <span data-ttu-id="5f0bf-112">El cliente puede llamar a la función [**RasGetProjectionInfo**](/previous-versions/windows/embedded/ms897107(v=msdn.10)) para obtener información adicional sobre la proyección.</span><span class="sxs-lookup"><span data-stu-id="5f0bf-112">The client can call the [**RasGetProjectionInfo**](/previous-versions/windows/embedded/ms897107(v=msdn.10)) function to get additional information about the projection.</span></span> <span data-ttu-id="5f0bf-113">El cliente puede usar esta información para notificar al usuario en qué protocolos de red puede usar esta conexión.</span><span class="sxs-lookup"><span data-stu-id="5f0bf-113">The client can use this information to notify the user as to which network protocols can be used by this connection.</span></span>

<span data-ttu-id="5f0bf-114">Debe evitar escribir código que dependa del orden o la aparición de Estados informativos determinados, ya que puede variar entre las distintas plataformas.</span><span class="sxs-lookup"><span data-stu-id="5f0bf-114">You should avoid writing code that depends on the order or occurrence of particular informational states, because this may vary between platforms.</span></span>

 

 




