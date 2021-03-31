---
description: Las interfaces de programación de aplicaciones de telefonía de Microsoft admiten el desarrollo de aplicaciones de comunicaciones para Microsoft Windows. En la tabla siguiente se enumeran las interfaces de telefonía.
ms.assetid: e7348296-ee2d-4e0a-b274-3563dccea841
title: Interfaces de programación de aplicaciones de telefonía
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a19fd6a520c8a53440967eeef753b7ed8c90ba5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912765"
---
# <a name="telephony-application-programming-interfaces"></a><span data-ttu-id="03fc7-104">Interfaces de programación de aplicaciones de telefonía</span><span class="sxs-lookup"><span data-stu-id="03fc7-104">Telephony Application Programming Interfaces</span></span>

<span data-ttu-id="03fc7-105">Las interfaces de programación de aplicaciones de telefonía de Microsoft admiten el desarrollo de aplicaciones de comunicaciones para Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="03fc7-105">The Microsoft telephony application programming interfaces support the development of communications applications for Microsoft Windows.</span></span> <span data-ttu-id="03fc7-106">En la tabla siguiente se enumeran las interfaces de telefonía.</span><span class="sxs-lookup"><span data-stu-id="03fc7-106">The telephony interfaces are listed in the following table.</span></span>



| <span data-ttu-id="03fc7-107">Interfaz</span><span class="sxs-lookup"><span data-stu-id="03fc7-107">Interface</span></span>                                                  | <span data-ttu-id="03fc7-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="03fc7-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                             |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="03fc7-109">TAPI 2. x</span><span class="sxs-lookup"><span data-stu-id="03fc7-109">TAPI 2.x</span></span>](./tapi-2-2-start-page.md)               | <span data-ttu-id="03fc7-110">Una API basada en lenguaje de programación C que le permite implementar aplicaciones de comunicaciones que van desde el control básico de módem hasta centros de llamadas con varios agentes y conmutadores.</span><span class="sxs-lookup"><span data-stu-id="03fc7-110">A C-programming language based API that enables you to implement communications applications ranging from basic modem control to call centers with multiple agents and switches.</span></span>                                                                                                                                                                        |
| [<span data-ttu-id="03fc7-111">TAPI 3. x</span><span class="sxs-lookup"><span data-stu-id="03fc7-111">TAPI 3.x</span></span>](tapi-3-1-start-page.md)                        | <span data-ttu-id="03fc7-112">Una API basada en COM que combina la telefonía clásica y la IP.</span><span class="sxs-lookup"><span data-stu-id="03fc7-112">A COM-based API that merges classic and IP telephony.</span></span>                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="03fc7-113">TSPI</span><span class="sxs-lookup"><span data-stu-id="03fc7-113">TSPI</span></span>](./telephony-service-providers-start-page.md) | <span data-ttu-id="03fc7-114">Un proveedor de servicios de telefonía (TSP) es una biblioteca de vínculos dinámicos (DLL) que admite el control de los dispositivos de comunicaciones a través de un conjunto de funciones de servicio exportadas.</span><span class="sxs-lookup"><span data-stu-id="03fc7-114">A telephony service provider (TSP) is a dynamic-link library (DLL) that supports communications device control through a set of exported service functions.</span></span> <span data-ttu-id="03fc7-115">Una aplicación TAPI usa comandos estandarizados, TAPI pasa información al proveedor de servicios de telefonía y el TSP controla los comandos específicos que se deben intercambiar con el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="03fc7-115">A TAPI application uses standardized commands, TAPI passes information to the telephony service provider, and the TSP handles the specific commands that must be exchanged with the device.</span></span> |
| [<span data-ttu-id="03fc7-116">MSPI</span><span class="sxs-lookup"><span data-stu-id="03fc7-116">MSPI</span></span>](media-service-providers-start-page.md)             | <span data-ttu-id="03fc7-117">Un proveedor de servicios multimedia (MSP) permite que una aplicación tenga un control considerable sobre los medios de un mecanismo de transporte determinado.</span><span class="sxs-lookup"><span data-stu-id="03fc7-117">A media service provider (MSP) allows an application considerable control over the media for a particular transport mechanism.</span></span> <span data-ttu-id="03fc7-118">Un MSP siempre se empareja con un proveedor de servicios de telefonía (TSP).</span><span class="sxs-lookup"><span data-stu-id="03fc7-118">An MSP is always paired with a telephony service provider (TSP).</span></span>                                                                                                                                                         |



 

 

 
