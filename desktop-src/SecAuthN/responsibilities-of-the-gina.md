---
description: Enumera y explica las responsabilidades de GINA.
ms.assetid: 5cffe4a6-6475-441e-bf81-f3cbcf1fee3f
title: Responsabilidades de GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40c3481aea9f5a92a485c42fb00b43d7062012d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082610"
---
# <a name="responsibilities-of-the-gina"></a><span data-ttu-id="3fbde-103">Responsabilidades de GINA</span><span class="sxs-lookup"><span data-stu-id="3fbde-103">Responsibilities of the GINA</span></span>

> [!Note]  
> <span data-ttu-id="3fbde-104">Los archivos dll de GINA se omiten en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3fbde-104">GINA DLLs are ignored in Windows Vista.</span></span>

 

<span data-ttu-id="3fbde-105">Un archivo dll de [*Gina*](../secgloss/g-gly.md) tiene las siguientes responsabilidades:</span><span class="sxs-lookup"><span data-stu-id="3fbde-105">A [*GINA*](../secgloss/g-gly.md) DLL has the following responsibilities:</span></span>

-   <span data-ttu-id="3fbde-106">Supervisión de SAS</span><span class="sxs-lookup"><span data-stu-id="3fbde-106">SAS monitoring</span></span>

    <span data-ttu-id="3fbde-107">GINA es responsable de reconocer una [*secuencia de atención segura*](../secgloss/s-gly.md) (SAS), la supervisión de eventos SAS y la notificación de Winlogon cuando se ha producido una SAS.</span><span class="sxs-lookup"><span data-stu-id="3fbde-107">The GINA is responsible for recognizing a [*secure attention sequence*](../secgloss/s-gly.md) (SAS), monitoring for SAS events, and notifying Winlogon when a SAS has occurred.</span></span> <span data-ttu-id="3fbde-108">Tenga en cuenta que puede haber más de una SAS definida, y el conjunto de SASs definido puede cambiar con el tiempo.</span><span class="sxs-lookup"><span data-stu-id="3fbde-108">Note that there can be more than one SAS defined, and the set of defined SASs can change over time.</span></span> <span data-ttu-id="3fbde-109">Por ejemplo, puede haber un conjunto de SASs cuando [*Winlogon*](../secgloss/w-gly.md) está en el estado de cierre de sesión y otro conjunto cuando está en el estado de la sesión iniciada.</span><span class="sxs-lookup"><span data-stu-id="3fbde-109">For example, there can be one set of SASs when [*Winlogon*](../secgloss/w-gly.md) is in the logged-off state and another set when it is in the logged-on state.</span></span>

    <span data-ttu-id="3fbde-110">Winlogon proporciona servicios para ayudar a GINA en el uso de las SA CTRL + ALT + SUPR.</span><span class="sxs-lookup"><span data-stu-id="3fbde-110">Winlogon provides services to assist the GINA in using the CTRL+ALT+DEL SAS.</span></span>

-   <span data-ttu-id="3fbde-111">Procesamiento de SAS</span><span class="sxs-lookup"><span data-stu-id="3fbde-111">SAS processing</span></span>

    <span data-ttu-id="3fbde-112">Uno de los motivos para realizar la sustitución de GINA es proporcionar mecanismos de identificación y autenticación alternativos.</span><span class="sxs-lookup"><span data-stu-id="3fbde-112">One reason for making the GINA replaceable is to provide alternative identification and authentication mechanisms.</span></span> <span data-ttu-id="3fbde-113">Para ello, GINA debe presentar todas las interfaces de usuario que resultan del reconocimiento de una SAS.</span><span class="sxs-lookup"><span data-stu-id="3fbde-113">To do this, the GINA must present all user interfaces resulting from the recognition of a SAS.</span></span> <span data-ttu-id="3fbde-114">Cuando ningún usuario ha iniciado sesión, GINA es responsable de presentar las opciones de identificación y autenticación, así como cualquier otra opción permitida que no esté autenticada.</span><span class="sxs-lookup"><span data-stu-id="3fbde-114">When no user is logged on, the GINA is responsible for presenting identification and authentication options as well as any other permissible options that are not authenticated.</span></span> <span data-ttu-id="3fbde-115">Cuando un usuario ha iniciado sesión, GINA es responsable de presentar las opciones pertinentes al usuario, así como de tomar las medidas adecuadas.</span><span class="sxs-lookup"><span data-stu-id="3fbde-115">When a user is logged on, the GINA is responsible for presenting the relevant options to the user as well as taking whatever actions are deemed appropriate.</span></span> <span data-ttu-id="3fbde-116">Por ejemplo, en un sistema que incluye una [*tarjeta inteligente*](../secgloss/s-gly.md), puede ser adecuado bloquear automáticamente la estación de trabajo si el usuario quita la tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="3fbde-116">For example, in a system that includes a [*smart card*](../secgloss/s-gly.md), it may be appropriate to automatically lock the workstation if the user removes the smart card.</span></span>

-   <span data-ttu-id="3fbde-117">Activación de Shell</span><span class="sxs-lookup"><span data-stu-id="3fbde-117">Shell activation</span></span>

    <span data-ttu-id="3fbde-118">Cuando un usuario inicia sesión, GINA es responsable de crear uno o más procesos iniciales para ese usuario.</span><span class="sxs-lookup"><span data-stu-id="3fbde-118">When a user logs on, the GINA is responsible for creating one or more initial processes for that user.</span></span> <span data-ttu-id="3fbde-119">En esta documentación, se supone que estos procesos iniciales presentan una interfaz al usuario.</span><span class="sxs-lookup"><span data-stu-id="3fbde-119">(In this documentation, it is assumed that these initial processes present an interface to the user.</span></span> <span data-ttu-id="3fbde-120">Sin embargo, los procesos pueden ser realmente cualquier proceso y no tienen por qué interactuar con el usuario). Estos procesos se conocen como el *Shell de usuario* o simplemente el *Shell*.</span><span class="sxs-lookup"><span data-stu-id="3fbde-120">However, the processes can actually be any processes and do not necessarily have to interact with the user.) These processes are referred to as the *user shell* or just the *shell*.</span></span> <span data-ttu-id="3fbde-121">Como parte de la activación del shell, GINA debe asignar el token del usuario que acaba de iniciar sesión a los procesos.</span><span class="sxs-lookup"><span data-stu-id="3fbde-121">As part of shell activation, the GINA must assign the newly logged-on user's token to the processes.</span></span> <span data-ttu-id="3fbde-122">Winlogon proporciona un servicio que ayuda a GINA a asignar el token.</span><span class="sxs-lookup"><span data-stu-id="3fbde-122">Winlogon provides a service to assist the GINA in assigning the token.</span></span>

 

 
