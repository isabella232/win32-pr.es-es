---
description: Uso de WPUCloseEvent para destruir un objeto de evento (aplicación o proveedor de servicios) cuando ya no se necesita el objeto de evento.
ms.assetid: ad6f7018-3647-4ab8-9a77-d833d18cd4b6
title: Destruir objetos de evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 359f0a17f623d0dd9ebceaf76b963ce72306000b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360307"
---
# <a name="destroying-event-objects"></a><span data-ttu-id="9a511-103">Destruir objetos de evento</span><span class="sxs-lookup"><span data-stu-id="9a511-103">Destroying Event Objects</span></span>

<span data-ttu-id="9a511-104">La entidad que crea un objeto de evento (aplicación o proveedor de servicios) es responsable de destruirlo cuando ya no es necesario.</span><span class="sxs-lookup"><span data-stu-id="9a511-104">The entity that creates an event object (application or service provider) is responsible for destroying it when it is no longer required.</span></span> <span data-ttu-id="9a511-105">Los proveedores de servicios lo hacen a través de **WPUCloseEvent**.</span><span class="sxs-lookup"><span data-stu-id="9a511-105">Service providers do this through **WPUCloseEvent**.</span></span>

 

 



