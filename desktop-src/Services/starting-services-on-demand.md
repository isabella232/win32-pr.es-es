---
description: El usuario puede iniciar un servicio con la utilidad servicios del panel de control. El usuario puede especificar argumentos para el servicio en el campo parámetros de inicio. Un programa de control de servicios puede iniciar un servicio y especificar sus argumentos con la función StartService.
ms.assetid: 72f51b38-d62c-4400-a38d-b9a0e90e9db4
title: Inicio de servicios a petición
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38c70be74e6cf54468f244ca798ae7ca48da3512
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668455"
---
# <a name="starting-services-on-demand"></a><span data-ttu-id="ec639-105">Inicio de servicios a petición</span><span class="sxs-lookup"><span data-stu-id="ec639-105">Starting Services on Demand</span></span>

<span data-ttu-id="ec639-106">El usuario puede iniciar un servicio con la utilidad servicios del panel de control.</span><span class="sxs-lookup"><span data-stu-id="ec639-106">The user can start a service with the Services control panel utility.</span></span> <span data-ttu-id="ec639-107">El usuario puede especificar argumentos para el servicio en el campo **parámetros de inicio** .</span><span class="sxs-lookup"><span data-stu-id="ec639-107">The user can specify arguments for the service in the **Start parameters** field.</span></span> <span data-ttu-id="ec639-108">Un programa de control de servicios puede iniciar un servicio y especificar sus argumentos con la función [**StartService**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) .</span><span class="sxs-lookup"><span data-stu-id="ec639-108">A service control program can start a service and specify its arguments with the [**StartService**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) function.</span></span>

<span data-ttu-id="ec639-109">Cuando se inicia el servicio, el SCM realiza los siguientes pasos:</span><span class="sxs-lookup"><span data-stu-id="ec639-109">When the service is started, the SCM performs the following steps:</span></span>

-   <span data-ttu-id="ec639-110">Recuperar la información de la cuenta almacenada en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="ec639-110">Retrieve the account information stored in the database.</span></span>
-   <span data-ttu-id="ec639-111">Inicie sesión en la cuenta de servicio.</span><span class="sxs-lookup"><span data-stu-id="ec639-111">Log on the service account.</span></span>
-   <span data-ttu-id="ec639-112">Cargue el perfil de usuario.</span><span class="sxs-lookup"><span data-stu-id="ec639-112">Load the user profile.</span></span>
-   <span data-ttu-id="ec639-113">Cree el servicio en estado suspendido.</span><span class="sxs-lookup"><span data-stu-id="ec639-113">Create the service in the suspended state.</span></span>
-   <span data-ttu-id="ec639-114">Asigne el token de inicio de sesión al proceso.</span><span class="sxs-lookup"><span data-stu-id="ec639-114">Assign the logon token to the process.</span></span>
-   <span data-ttu-id="ec639-115">Permite que el proceso se ejecute.</span><span class="sxs-lookup"><span data-stu-id="ec639-115">Allow the process to execute.</span></span>

 

 



