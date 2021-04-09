---
title: Métodos del complemento de operaciones
description: Métodos del complemento de operaciones
ms.assetid: 81fe751f-51fd-4da6-b44a-0af9007eea9a
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff64a53c4c63b9e552efe90ac057b8a31d603b64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993804"
---
# <a name="operations-plug-in-methods"></a><span data-ttu-id="31746-103">Métodos del complemento de operaciones</span><span class="sxs-lookup"><span data-stu-id="31746-103">Operations Plug-in Methods</span></span>

<span data-ttu-id="31746-104">Todos los puntos de entrada del complemento de operaciones tienen un mecanismo de devolución de llamada para notificar si la llamada se ha realizado correctamente o no.</span><span class="sxs-lookup"><span data-stu-id="31746-104">All operations plug-in entry points have a callback mechanism to report the success or failure of the call.</span></span> <span data-ttu-id="31746-105">Algunos mecanismos de devolución de llamada se llaman varias veces, hasta que se notifiquen todos los resultados.</span><span class="sxs-lookup"><span data-stu-id="31746-105">Some callback mechanisms are called multiple times, until all of the results are reported.</span></span>

<span data-ttu-id="31746-106">En la tabla siguiente se proporciona información general sobre los métodos de devolución de llamada de operaciones.</span><span class="sxs-lookup"><span data-stu-id="31746-106">The following table provides an overview of the operations callback methods.</span></span>



| <span data-ttu-id="31746-107">Método</span><span class="sxs-lookup"><span data-stu-id="31746-107">Method</span></span>                                                                         | <span data-ttu-id="31746-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="31746-108">Description</span></span>                                                                                                                                          |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="31746-109">**WSManPluginFreeRequestDetails**</span><span class="sxs-lookup"><span data-stu-id="31746-109">**WSManPluginFreeRequestDetails**</span></span>](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginfreerequestdetails)         | <span data-ttu-id="31746-110">Libera la memoria asignada para la estructura de [**\_ \_ solicitud del complemento WSMAN**](/windows/desktop/api/Wsman/ns-wsman-wsman_plugin_request) .</span><span class="sxs-lookup"><span data-stu-id="31746-110">Releases memory that is allocated for the [**WSMAN\_PLUGIN\_REQUEST**](/windows/desktop/api/Wsman/ns-wsman-wsman_plugin_request) structure.</span></span>                                          |
| [<span data-ttu-id="31746-111">**WSManPluginGetOperationParameters**</span><span class="sxs-lookup"><span data-stu-id="31746-111">**WSManPluginGetOperationParameters**</span></span>](/windows/desktop/api/Wsman/nf-wsman-wsmanplugingetoperationparameters) | <span data-ttu-id="31746-112">Obtiene información operativa, como tiempos de espera y restricciones de datos asociados a una operación.</span><span class="sxs-lookup"><span data-stu-id="31746-112">Gets operational information, such as time-outs and data restrictions that are associated with an operation.</span></span>                                         |
| [<span data-ttu-id="31746-113">**WSManPluginOperationComplete**</span><span class="sxs-lookup"><span data-stu-id="31746-113">**WSManPluginOperationComplete**</span></span>](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginoperationcomplete)           | <span data-ttu-id="31746-114">Registra la finalización de una operación.</span><span class="sxs-lookup"><span data-stu-id="31746-114">Records the completion of an operation.</span></span>                                                                                                              |
| [<span data-ttu-id="31746-115">**WSManPluginReceiveResult**</span><span class="sxs-lookup"><span data-stu-id="31746-115">**WSManPluginReceiveResult**</span></span>](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginreceiveresult)                   | <span data-ttu-id="31746-116">Informa de los resultados a Administración remota de Windows (WinRM) complementos.</span><span class="sxs-lookup"><span data-stu-id="31746-116">Reports results to Windows Remote Management (WinRM) plug-ins.</span></span>                                                                                       |
| [<span data-ttu-id="31746-117">**WSManPluginReportContext**</span><span class="sxs-lookup"><span data-stu-id="31746-117">**WSManPluginReportContext**</span></span>](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginreportcontext)                   | <span data-ttu-id="31746-118">Devuelve el Shell y el contexto del comando a la infraestructura de WinRM para que se puedan realizar más operaciones con el shell o el comando.</span><span class="sxs-lookup"><span data-stu-id="31746-118">Reports the shell and command context back to the WinRM infrastructure so that further operations can be performed against the shell and/or command.</span></span> |



 

 

 




