---
title: Métodos de complemento de autorización
description: Todos los puntos de entrada del complemento de autorización tienen un mecanismo de devolución de llamada para notificar si la llamada se ha realizado correctamente o no. Se llama varias veces a algunos mecanismos de devolución de llamada hasta que se notifiquen todos los resultados.
ms.assetid: 6d7c1c54-fab5-431b-b123-eee6fd4dfb92
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9253267b87a30c5cc2781440b0ecd430f244e90
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704661"
---
# <a name="authorization-plug-in-methods"></a><span data-ttu-id="c0fbc-104">Métodos de complemento de autorización</span><span class="sxs-lookup"><span data-stu-id="c0fbc-104">Authorization Plug-in Methods</span></span>

<span data-ttu-id="c0fbc-105">Todos los puntos de entrada del complemento de autorización tienen un mecanismo de devolución de llamada para notificar si la llamada se ha realizado correctamente o no.</span><span class="sxs-lookup"><span data-stu-id="c0fbc-105">All authorization plug-in entry points have a callback mechanism to report the success or failure of the call.</span></span> <span data-ttu-id="c0fbc-106">Se llama varias veces a algunos mecanismos de devolución de llamada hasta que se notifiquen todos los resultados.</span><span class="sxs-lookup"><span data-stu-id="c0fbc-106">Some callback mechanisms are called multiple times until all of the results are reported.</span></span>

<span data-ttu-id="c0fbc-107">En la tabla siguiente se proporciona información general sobre los métodos de devolución de llamada de autorización.</span><span class="sxs-lookup"><span data-stu-id="c0fbc-107">The following table provides an overview of the authorization callback methods.</span></span>



| <span data-ttu-id="c0fbc-108">Método</span><span class="sxs-lookup"><span data-stu-id="c0fbc-108">Method</span></span>                                                                           | <span data-ttu-id="c0fbc-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="c0fbc-109">Description</span></span>                                                          |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="c0fbc-110">**WSManPluginAuthzOperationComplete**</span><span class="sxs-lookup"><span data-stu-id="c0fbc-110">**WSManPluginAuthzOperationComplete**</span></span>](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzoperationcomplete)   | <span data-ttu-id="c0fbc-111">Informa de una operación de usuario correcta o errónea.</span><span class="sxs-lookup"><span data-stu-id="c0fbc-111">Reports either a successful or failed user operation.</span></span>                |
| [<span data-ttu-id="c0fbc-112">**WSManPluginAuthzQueryQuotaComplete**</span><span class="sxs-lookup"><span data-stu-id="c0fbc-112">**WSManPluginAuthzQueryQuotaComplete**</span></span>](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzqueryquotacomplete) | <span data-ttu-id="c0fbc-113">Informa de los detalles de la cuota relevantes para el usuario especificado.</span><span class="sxs-lookup"><span data-stu-id="c0fbc-113">Reports quota details that are relevant for the specified user.</span></span>      |
| [<span data-ttu-id="c0fbc-114">**WSManPluginAuthzUserComplete**</span><span class="sxs-lookup"><span data-stu-id="c0fbc-114">**WSManPluginAuthzUserComplete**</span></span>](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzusercomplete)             | <span data-ttu-id="c0fbc-115">Informa de una autorización de conexión de usuario correcta o errónea.</span><span class="sxs-lookup"><span data-stu-id="c0fbc-115">Reports either a successful or failed user connection authorization.</span></span> |



 

 

 




