---
title: Recuperación y reinicio de aplicaciones
description: Escriba instaladores personalizados para reiniciar automáticamente una aplicación que se ha cerrado para completar una actualización. Guarde los datos y configure la recuperación de la aplicación antes de salir de los programas.
ms.assetid: 60b057dd-9724-4bc4-b1b0-eea7e8380ecb
keywords:
- restart
- recover
- recovery
- confiabilidad
- confiabilidad del software
- recuperación de aplicaciones
- reinicio de la aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 862236fad876307b0662a8444775c78673b92983
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903803"
---
# <a name="application-recovery-and-restart"></a><span data-ttu-id="8fe73-111">Recuperación y reinicio de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="8fe73-111">Application Recovery and Restart</span></span>

## <a name="purpose"></a><span data-ttu-id="8fe73-112">Propósito</span><span class="sxs-lookup"><span data-stu-id="8fe73-112">Purpose</span></span>

<span data-ttu-id="8fe73-113">Una aplicación puede usar la recuperación y el reinicio de la aplicación (ARR) para guardar los datos y la información de estado antes de que se cierre la aplicación debido a una excepción no controlada o cuando la aplicación deja de responder.</span><span class="sxs-lookup"><span data-stu-id="8fe73-113">An application can use Application Recovery and Restart (ARR) to save data and state information before the application exits due to an unhandled exception or when the application stops responding.</span></span> <span data-ttu-id="8fe73-114">También se reinicia la aplicación, si se solicita.</span><span class="sxs-lookup"><span data-stu-id="8fe73-114">The application is also restarted, if requested.</span></span>

<span data-ttu-id="8fe73-115">También se puede reiniciar una aplicación si un instalador actualiza un componente de la aplicación, o si el equipo tiene que reiniciarse como resultado de una actualización.</span><span class="sxs-lookup"><span data-stu-id="8fe73-115">An application can also be restarted if an installer updates a component of the application, or if the computer needs to restart as the result of an update.</span></span> <span data-ttu-id="8fe73-116">Tenga en cuenta que para admitir el reinicio automático de aplicaciones después de que un instalador actualice una aplicación, la aplicación y el instalador deben crearse de forma adecuada.</span><span class="sxs-lookup"><span data-stu-id="8fe73-116">Note that to support automatic application restart after an installer updates an application, both the application and installer need to be authored appropriately.</span></span> <span data-ttu-id="8fe73-117">Para obtener más información, consulte [registro del reinicio de la aplicación](registering-for-application-restart.md).</span><span class="sxs-lookup"><span data-stu-id="8fe73-117">For details, see [Registering for Application Restart](registering-for-application-restart.md).</span></span>

## <a name="developer-audience"></a><span data-ttu-id="8fe73-118">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="8fe73-118">Developer audience</span></span>

<span data-ttu-id="8fe73-119">ARR está diseñado para desarrolladores de C y C++.</span><span class="sxs-lookup"><span data-stu-id="8fe73-119">ARR is designed for C and C++ developers.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="8fe73-120">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="8fe73-120">Run-time requirements</span></span>

<span data-ttu-id="8fe73-121">ARR está disponible a partir del sistema operativo Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8fe73-121">ARR is available starting with the Windows Vista operating system.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="8fe73-122">En esta sección</span><span class="sxs-lookup"><span data-stu-id="8fe73-122">In this section</span></span>



| <span data-ttu-id="8fe73-123">Tema</span><span class="sxs-lookup"><span data-stu-id="8fe73-123">Topic</span></span>                                                                                                   | <span data-ttu-id="8fe73-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="8fe73-124">Description</span></span>                                                           |
|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="8fe73-125">Uso de la recuperación y reinicio de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="8fe73-125">Using Application Recovery and Restart</span></span>](using-application-recovery-and-restart.md)<br/>         | <span data-ttu-id="8fe73-126">Guía de procedimientos para el registro para recuperación y reinicio.</span><span class="sxs-lookup"><span data-stu-id="8fe73-126">Procedural guide for registering for recovery and restart.</span></span><br/> |
| [<span data-ttu-id="8fe73-127">Referencia de recuperación y reinicio de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="8fe73-127">Application Recovery and Restart Reference</span></span>](application-recovery-and-restart-reference.md)<br/> | <span data-ttu-id="8fe73-128">Información de referencia para la API de ARR.</span><span class="sxs-lookup"><span data-stu-id="8fe73-128">Reference information for the ARR API.</span></span> <br/>                    |



 

 

 





