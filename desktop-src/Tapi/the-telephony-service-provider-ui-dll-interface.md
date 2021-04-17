---
description: En telefonía de Microsoft, los proveedores de servicios de telefonía se ejecutan en un proceso independiente de las aplicaciones de telefonía.
ms.assetid: ccc40d3c-6764-469a-baac-fa625d664ea7
title: La interfaz DLL de la interfaz de usuario del proveedor de servicios de telefonía
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdab33dd9c9630aed7d7aed168982cfac2daee2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677790"
---
# <a name="the-telephony-service-provider-ui-dll-interface"></a><span data-ttu-id="94ca1-103">La interfaz DLL de la interfaz de usuario del proveedor de servicios de telefonía</span><span class="sxs-lookup"><span data-stu-id="94ca1-103">The Telephony Service Provider UI DLL Interface</span></span>

<span data-ttu-id="94ca1-104">En telefonía de Microsoft, los proveedores de servicios de telefonía se ejecutan en un proceso independiente de las aplicaciones de telefonía.</span><span class="sxs-lookup"><span data-stu-id="94ca1-104">In Microsoft Telephony, telephony service providers execute in a separate process from telephony applications.</span></span> <span data-ttu-id="94ca1-105">Los proveedores de servicios se comunican con TAPISRV a través de la interfaz del proveedor de servicios de telefonía (TSPI) y se ejecutan en su proceso. interfaz de aplicaciones a TAPI, que se cargan en el contexto de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="94ca1-105">Service providers communicate with TAPISRV through the Telephony service provider interface (TSPI) and execute in its process; applications interface to TAPI, which are loaded in the application context.</span></span>

<span data-ttu-id="94ca1-106">Los componentes de TAPI usan varios mecanismos de comunicación entre procesos para transmitir solicitudes de función y mensajes entre aplicaciones y proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="94ca1-106">The components of TAPI use various interprocess communications mechanisms to convey function requests and messages between applications and service providers.</span></span> <span data-ttu-id="94ca1-107">Las aplicaciones y los proveedores de servicios se pueden estar ejecutando no solo en procesos independientes, sino también en sistemas completamente independientes.</span><span class="sxs-lookup"><span data-stu-id="94ca1-107">The applications and the service providers may be executing not only in separate processes, but on completely separate systems.</span></span> <span data-ttu-id="94ca1-108">Por lo tanto, los proveedores de servicios no pueden mostrar cuadros de diálogo en el proceso ni siquiera en el equipo en el que se ejecutan; La interfaz de usuario debe invocarse desde dentro del contexto de la aplicación, en el equipo en el que se ejecuta la aplicación.</span><span class="sxs-lookup"><span data-stu-id="94ca1-108">Service providers therefore cannot display dialog boxes in the process or even on the computer on which they are executing; UI must be invoked from within the application context, on the computer on which the application is executing.</span></span>

<span data-ttu-id="94ca1-109">En esta sección se define el mecanismo por el que las funciones de la interfaz de usuario del proveedor de servicios se cargan y se invocan en el contexto de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="94ca1-109">This section defines the mechanism by which service provider UI functions are loaded and invoked within the application context.</span></span> <span data-ttu-id="94ca1-110">También se define un mecanismo mediante el cual los proveedores de servicios pueden abrir cuadros de diálogo espontáneamente en el contexto de la aplicación cuando no serían esperados por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="94ca1-110">A mechanism is also defined by which service providers can spontaneously open dialog boxes in the application context when they would not otherwise be expected by the application.</span></span> <span data-ttu-id="94ca1-111">Un ejemplo de este último caso sería el cuadro de diálogo **Talk/colgar** que muestra un proveedor de servicios de módem de datos cuando el módem se usa como marcador para llamadas de voz interactivas, y se debe indicar al usuario que recoja el teléfono e informará al proveedor de servicios de Cuándo debe colocar el módem.</span><span class="sxs-lookup"><span data-stu-id="94ca1-111">An example of this latter case would be the **Talk/Hangup** dialog box that is displayed by a data modem service provider when the modem is being used as a dialer for interactive voice calls, and the user must be told to pick up the phone and inform the service provider when to place the modem onhook.</span></span>

 

 



