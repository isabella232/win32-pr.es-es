---
description: Se requiere un cierre adecuado de las sesiones de comunicaciones y de una aplicación completa para evitar que los recursos permanezcan relacionados en las llamadas o aplicaciones que ya no las necesiten.
ms.assetid: 40694b7f-474b-41aa-be3f-48e4ca517a6f
title: Apagado de TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 661273a3d72559d965fa1ea6066f1090f8e6b6e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688410"
---
# <a name="tapi-shutdown"></a><span data-ttu-id="d3741-103">Apagado de TAPI</span><span class="sxs-lookup"><span data-stu-id="d3741-103">TAPI Shutdown</span></span>

<span data-ttu-id="d3741-104">Se requiere un cierre adecuado de las sesiones de comunicaciones y de una aplicación completa para evitar que los recursos permanezcan relacionados en las llamadas o aplicaciones que ya no las necesiten.</span><span class="sxs-lookup"><span data-stu-id="d3741-104">Proper shutdown of communications sessions and of an entire application is required to prevent resources from remaining tied up in calls or applications that no longer need them.</span></span>

<span data-ttu-id="d3741-105">TAPI proporciona una serie de funciones y métodos para ayudar en el proceso.</span><span class="sxs-lookup"><span data-stu-id="d3741-105">TAPI provides a series of functions and methods to assist in the process.</span></span> <span data-ttu-id="d3741-106">Obviamente, la aplicación también debe asumir la responsabilidad de liberar correctamente la memoria asignada, ya sea en forma de estructuras de datos o de referencias COM.</span><span class="sxs-lookup"><span data-stu-id="d3741-106">Obviously, the application must also take responsibility for properly releasing allocated memory, whether in the form of data structures or COM references.</span></span>



| <span data-ttu-id="d3741-107">Funciones de TAPI 2. x</span><span class="sxs-lookup"><span data-stu-id="d3741-107">TAPI 2.x functions</span></span>                                                            | <span data-ttu-id="d3741-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="d3741-108">Description</span></span>                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="d3741-109">**lineRegisterRequestRecipient**</span><span class="sxs-lookup"><span data-stu-id="d3741-109">**lineRegisterRequestRecipient**</span></span>](/windows/win32/api/tapi/nf-tapi-lineregisterrequestrecipient) | <span data-ttu-id="d3741-110">Anula el registro de la aplicación como un controlador para llamadas de telefonía asistidas.</span><span class="sxs-lookup"><span data-stu-id="d3741-110">Unregisters the application as a handler for assisted telephony calls.</span></span> |
| [<span data-ttu-id="d3741-111">**lineClose**</span><span class="sxs-lookup"><span data-stu-id="d3741-111">**lineClose**</span></span>](/windows/win32/api/tapi/nf-tapi-lineclose)                                       | <span data-ttu-id="d3741-112">Desconecta la aplicación como administrador de llamadas en la línea determinada.</span><span class="sxs-lookup"><span data-stu-id="d3741-112">Disconnects the application as a manager for calls on the given line.</span></span>  |
| [<span data-ttu-id="d3741-113">**lineShutdown**</span><span class="sxs-lookup"><span data-stu-id="d3741-113">**lineShutdown**</span></span>](/windows/win32/api/tapi/nf-tapi-lineshutdown)                                 | <span data-ttu-id="d3741-114">Cierra el uso de la aplicación de la abstracción de línea.</span><span class="sxs-lookup"><span data-stu-id="d3741-114">Shuts down the application's usage of the line abstraction.</span></span>            |



 



| <span data-ttu-id="d3741-115">Interfaces o métodos TAPI 3. x</span><span class="sxs-lookup"><span data-stu-id="d3741-115">TAPI 3.x interfaces or methods</span></span>                                            | <span data-ttu-id="d3741-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="d3741-116">Description</span></span>                                                                |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="d3741-117">**ITTAPI::UnregisterNotifications**</span><span class="sxs-lookup"><span data-stu-id="d3741-117">**ITTAPI::UnregisterNotifications**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-unregisternotifications) | <span data-ttu-id="d3741-118">Quita cualquier registro de notificación de eventos realizado por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d3741-118">Removes any event notification registrations performed by the application.</span></span> |
| [<span data-ttu-id="d3741-119">**ITTAPI:: Shutdown**</span><span class="sxs-lookup"><span data-stu-id="d3741-119">**ITTAPI::Shutdown**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-shutdown)                               | <span data-ttu-id="d3741-120">Desconecta la aplicación como administrador de llamadas.</span><span class="sxs-lookup"><span data-stu-id="d3741-120">Disconnects the application as a call manager.</span></span>                             |



 

 

 
