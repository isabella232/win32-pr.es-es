---
title: Detalles de la implementación de EAP
description: Los puntos de acceso (APs), como el servicio de acceso remoto (RAS), interactúan con las implementaciones de EAP mediante el uso de llamadas a funciones que debe exportar el archivo DLL de EAP de terceros.
ms.assetid: 85775c03-7538-41a1-9f83-42e71025a79c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41115b16d843b0c1b087eac1c348a0491df1173a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358890"
---
# <a name="eap-implementation-details"></a><span data-ttu-id="2009d-103">Detalles de la implementación de EAP</span><span class="sxs-lookup"><span data-stu-id="2009d-103">EAP Implementation Details</span></span>

<span data-ttu-id="2009d-104">Los puntos de acceso (APs), como el servicio de acceso remoto (RAS), interactúan con las implementaciones de EAP mediante el uso de llamadas a funciones que debe exportar el archivo DLL de EAP de terceros.</span><span class="sxs-lookup"><span data-stu-id="2009d-104">Access Points (APs), such as Remote Access Service (RAS), interact with EAP implementations through the use of function calls that must be exported by the third-party EAP DLL.</span></span> <span data-ttu-id="2009d-105">En otras palabras, EAP es una API de proveedor, lo que significa que los complementos o los archivos dll implementan código para convertirse en proveedor EAP, pero no deben llamar a las propias API de EAP.</span><span class="sxs-lookup"><span data-stu-id="2009d-105">In other words, EAP is a provider API, meaning that plug-ins or DLLs implement code to become an EAP provider, but must not call the EAP APIs themselves.</span></span> <span data-ttu-id="2009d-106">Por ejemplo, un programador de una DLL de EAP crea código para una rutina de inicialización de EAP y coloca este código en la función predefinida de EAP [**RasEapInitialize**](/previous-versions/windows/desktop/legacy/aa363527(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2009d-106">For example, a programmer of an EAP DLL creates code for an EAP initialization routine and places this code in the EAP predefined function [**RasEapInitialize**](/previous-versions/windows/desktop/legacy/aa363527(v=vs.85)).</span></span> <span data-ttu-id="2009d-107">Después, en tiempo de ejecución, el administrador de conexiones de AP llama a la función **RasEapInitialize** , que contiene el código, para inicializar la implementación de EAP.</span><span class="sxs-lookup"><span data-stu-id="2009d-107">Then at run-time, the AP connection manager calls the **RasEapInitialize** function, which contains the code, to initialize the EAP implementation.</span></span>

<span data-ttu-id="2009d-108">En los temas siguientes se detalla esta interacción:</span><span class="sxs-lookup"><span data-stu-id="2009d-108">The following topics detail this interaction:</span></span>

-   [<span data-ttu-id="2009d-109">Inicialización de punto de acceso de EAP</span><span class="sxs-lookup"><span data-stu-id="2009d-109">Access Point Initialization of EAP</span></span>](ras-initialization-of-eap.md)
-   [<span data-ttu-id="2009d-110">Inicialización del Protocolo de autenticación</span><span class="sxs-lookup"><span data-stu-id="2009d-110">Authentication Protocol Initialization</span></span>](authentication-protocol-initialization.md)
-   [<span data-ttu-id="2009d-111">Interacción del Protocolo de autenticación y punto de acceso</span><span class="sxs-lookup"><span data-stu-id="2009d-111">Access Point and Authentication Protocol Interaction</span></span>](ras-and-authentication-protocol-interaction-during-authentication.md)
-   [<span data-ttu-id="2009d-112">Finalización de la sesión de autenticación</span><span class="sxs-lookup"><span data-stu-id="2009d-112">Completion of the Authentication Session</span></span>](completion-of-the-authentication-session.md)

 

 