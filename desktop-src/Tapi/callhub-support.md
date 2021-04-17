---
description: El seguimiento de CallHub es una nueva característica de la versión 3,0 de TAPI.
ms.assetid: 29b6e585-6da8-46a2-a612-f42d0f65f68e
title: Compatibilidad con CallHub
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9efe6891cfdad956a87745f8e4b35dd117fe775e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678119"
---
# <a name="callhub-support"></a><span data-ttu-id="5dd5c-103">Compatibilidad con CallHub</span><span class="sxs-lookup"><span data-stu-id="5dd5c-103">CallHub Support</span></span>

<span data-ttu-id="5dd5c-104">El seguimiento de CallHub es una nueva característica de la versión 3,0 de TAPI.</span><span class="sxs-lookup"><span data-stu-id="5dd5c-104">CallHub tracking is a new feature in TAPI version 3.0.</span></span> <span data-ttu-id="5dd5c-105">La funcionalidad de CallHub se agregó a los elementos de programación de TAPI 2,1 con la entrega de Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="5dd5c-105">CallHub functionality was added to the TAPI 2.1 programming elements with the delivery of Windows 2000.</span></span> <span data-ttu-id="5dd5c-106">Un *CallHub* representa una vista de terceros de una llamada, y los identificadores de llamada de TAPI representan la vista de la primera parte de una llamada.</span><span class="sxs-lookup"><span data-stu-id="5dd5c-106">A *CallHub* represents a third-party view of a call, and TAPI's call handles represent the first-party view of a call.</span></span> <span data-ttu-id="5dd5c-107">Con el seguimiento de CallHub, se solicita al proveedor de servicios que siga CallHubs y proporcione información acerca de la llamada durante la vigencia de una CallHub.</span><span class="sxs-lookup"><span data-stu-id="5dd5c-107">With CallHub tracking, the service provider is requested to follow CallHubs and give information about the call during the lifetime of a CallHub.</span></span> <span data-ttu-id="5dd5c-108">A medida que las entidades nuevas se unen y salen del CallHub, el proveedor de servicios debe informar a TAPI.</span><span class="sxs-lookup"><span data-stu-id="5dd5c-108">As new parties join and leave the CallHub, the service provider should inform TAPI.</span></span>

<span data-ttu-id="5dd5c-109">No es necesario que un proveedor de servicios implemente nuevas funciones para admitir CallHub.</span><span class="sxs-lookup"><span data-stu-id="5dd5c-109">A service provider does not need to implement any new functions in order to support CallHub.</span></span> <span data-ttu-id="5dd5c-110">Simplemente tiene que rellenar el miembro **dwCallID** de la estructura [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo) .</span><span class="sxs-lookup"><span data-stu-id="5dd5c-110">It simply needs to fill in the **dwCallID** member of the [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo) structure.</span></span> <span data-ttu-id="5dd5c-111">En TAPI 3, TAPI recopila todas las llamadas con el mismo **dwCallID** y crea un identificador de CallHub que la aplicación puede usar para realizar el seguimiento de la llamada.</span><span class="sxs-lookup"><span data-stu-id="5dd5c-111">In TAPI 3, TAPI collects all calls with the same **dwCallID** and creates a CallHub handle that the application can use to track the call.</span></span>

 

 
