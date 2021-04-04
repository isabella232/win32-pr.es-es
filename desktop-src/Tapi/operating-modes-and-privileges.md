---
description: La aplicación puede solicitar uno de los dos modos de funcionamiento al abrir un dispositivo telefónico.
ms.assetid: 2bb16fbe-883e-4734-a071-f14f5e5737e3
title: Modos de funcionamiento y privilegios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ba1cc01ed0552762ac3bc97449b1ae5a923cb10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812488"
---
# <a name="operating-modes-and-privileges"></a><span data-ttu-id="1ac89-103">Modos de funcionamiento y privilegios</span><span class="sxs-lookup"><span data-stu-id="1ac89-103">Operating Modes and Privileges</span></span>

<span data-ttu-id="1ac89-104">La aplicación puede solicitar uno de los dos modos de funcionamiento al abrir un dispositivo telefónico.</span><span class="sxs-lookup"><span data-stu-id="1ac89-104">The application can request one of two operating modes when opening a phone device.</span></span> <span data-ttu-id="1ac89-105">Estos modos reflejan los privilegios que la aplicación solicita para el dispositivo:</span><span class="sxs-lookup"><span data-stu-id="1ac89-105">These modes reflect the privileges the application requests for the device:</span></span>

-   <span data-ttu-id="1ac89-106">La apertura de un teléfono para los privilegios de monitor permite a la aplicación determinar el estado del dispositivo de teléfono.</span><span class="sxs-lookup"><span data-stu-id="1ac89-106">Opening a phone for monitor privileges lets the application determine the status of the phone device.</span></span> <span data-ttu-id="1ac89-107">Los mensajes se envían a la aplicación cuando se detectan cambios de estado en el dispositivo telefónico.</span><span class="sxs-lookup"><span data-stu-id="1ac89-107">Messages are sent to the application when status changes on the phone device are detected.</span></span>
-   <span data-ttu-id="1ac89-108">Una aplicación que abre un dispositivo telefónico para privilegios de propietario puede usar operaciones que modifican el estado del dispositivo de teléfono.</span><span class="sxs-lookup"><span data-stu-id="1ac89-108">An application that opens a phone device for owner privileges can use operations that modify the state of the phone device.</span></span> <span data-ttu-id="1ac89-109">El privilegio Owner también incluye automáticamente los privilegios de supervisión completos.</span><span class="sxs-lookup"><span data-stu-id="1ac89-109">Owner privilege automatically includes full monitor privileges as well.</span></span> <span data-ttu-id="1ac89-110">En cualquier momento, un dispositivo telefónico determinado solo se puede abrir una vez para los privilegios de propietario, pero varias veces para los privilegios de supervisión.</span><span class="sxs-lookup"><span data-stu-id="1ac89-110">At any time, a given phone device can be open only once for owner privileges, but multiple times for monitor privileges.</span></span> <span data-ttu-id="1ac89-111">Todas las operaciones de **phoneSet** requieren privilegios de propietario, mientras que todas las operaciones de **phoneGet** solo requieren privilegios de monitor.</span><span class="sxs-lookup"><span data-stu-id="1ac89-111">All **phoneSet** operations require owner privileges, while all **phoneGet** operations require only monitor privileges.</span></span>

 

 



