---
description: Un proveedor de servicios de telefonía (TSP) es una biblioteca de vínculos dinámicos (DLL) que admite el control de los dispositivos de comunicaciones a través de un conjunto de funciones de servicio exportadas.
ms.assetid: 276c27ac-b6ee-42a7-8327-33dfd87e69bd
title: Proveedores de servicios de telefonía
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40c3c8887723cc74a1bf0d77bcdcfd06c8468a4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912762"
---
# <a name="telephony-service-providers"></a><span data-ttu-id="40e0c-103">Proveedores de servicios de telefonía</span><span class="sxs-lookup"><span data-stu-id="40e0c-103">Telephony Service Providers</span></span>

## <a name="purpose"></a><span data-ttu-id="40e0c-104">Propósito</span><span class="sxs-lookup"><span data-stu-id="40e0c-104">Purpose</span></span>

<span data-ttu-id="40e0c-105">Un proveedor de servicios de telefonía (TSP) es una biblioteca de vínculos dinámicos (DLL) que admite el control de los dispositivos de comunicaciones a través de un conjunto de funciones de servicio exportadas.</span><span class="sxs-lookup"><span data-stu-id="40e0c-105">A telephony service provider (TSP) is a dynamic-link library (DLL) that supports communications device control through a set of exported service functions.</span></span> <span data-ttu-id="40e0c-106">Una aplicación TAPI usa comandos estandarizados, TAPI pasa información al proveedor de servicios de telefonía y el TSP controla los comandos específicos que se deben intercambiar con el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="40e0c-106">A TAPI application uses standardized commands, TAPI passes information to the telephony service provider, and the TSP handles the specific commands that must be exchanged with the device.</span></span>

<span data-ttu-id="40e0c-107">Un TSP debe ajustarse a la interfaz del proveedor de servicios de telefonía (TSPI) para que funcione como un proveedor de servicios en el entorno de telefonía de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="40e0c-107">A TSP must conform to the Telephony Service Provider Interface (TSPI) to function as a service provider within the Microsoft Telephony environment.</span></span> <span data-ttu-id="40e0c-108">TSPI define las funciones externas expuestas por un proveedor de servicios de telefonía proporcionado con el equipo de comunicaciones.</span><span class="sxs-lookup"><span data-stu-id="40e0c-108">TSPI defines the external functions exposed by a telephony service provider supplied with communications equipment.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="40e0c-109">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="40e0c-109">Developer audience</span></span>

<span data-ttu-id="40e0c-110">Puede escribir aplicaciones habilitadas para TAPI en muchos lenguajes, como Java, Visual Basic y C/C++.</span><span class="sxs-lookup"><span data-stu-id="40e0c-110">You can write TAPI-enabled applications in many languages, including Java, Visual Basic, and C/C++.</span></span> <span data-ttu-id="40e0c-111">La experiencia de desarrollo anterior con las telecomunicaciones u otras aplicaciones de telefonía es útil, pero no es necesario.</span><span class="sxs-lookup"><span data-stu-id="40e0c-111">Previous development experience with telecommunications or other telephony applications is helpful but not necessary.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="40e0c-112">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="40e0c-112">Run-time requirements</span></span>

<span data-ttu-id="40e0c-113">TSPI habilita el desarrollo de profesionales para todas las versiones de Windows.</span><span class="sxs-lookup"><span data-stu-id="40e0c-113">TSPI enables development of TSPs for all versions of Windows.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="40e0c-114">En esta sección</span><span class="sxs-lookup"><span data-stu-id="40e0c-114">In this section</span></span>



| <span data-ttu-id="40e0c-115">Tema</span><span class="sxs-lookup"><span data-stu-id="40e0c-115">Topic</span></span>                                                                | <span data-ttu-id="40e0c-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="40e0c-116">Description</span></span>                                                              |
|----------------------------------------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="40e0c-117">Información general</span><span class="sxs-lookup"><span data-stu-id="40e0c-117">Overview</span></span>](about-the-telephony-service-provider-tsp-.md)<br/> | <span data-ttu-id="40e0c-118">Información general sobre la arquitectura y los componentes de TSPI.</span><span class="sxs-lookup"><span data-stu-id="40e0c-118">General information about TSPI's architecture and components.</span></span><br/> |
| [<span data-ttu-id="40e0c-119">Referencia</span><span class="sxs-lookup"><span data-stu-id="40e0c-119">Reference</span></span>](tspi-reference.md)<br/>                           | <span data-ttu-id="40e0c-120">Documentación de las interfaces TSPI.</span><span class="sxs-lookup"><span data-stu-id="40e0c-120">Documentation for the TSPI interfaces.</span></span><br/>                        |



 

## <a name="related-topics"></a><span data-ttu-id="40e0c-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="40e0c-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40e0c-122">Introducción a la telefonía de Microsoft</span><span class="sxs-lookup"><span data-stu-id="40e0c-122">Microsoft Telephony Overview</span></span>](./microsoft-telephony-overview.md)
</dt> <dt>

[<span data-ttu-id="40e0c-123">Proveedores de servicios multimedia</span><span class="sxs-lookup"><span data-stu-id="40e0c-123">Media Service Providers</span></span>](./media-service-providers-start-page.md)
</dt> <dt>

[<span data-ttu-id="40e0c-124">TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="40e0c-124">TAPI 2.2</span></span>](./tapi-2-2-start-page.md)
</dt> <dt>

[<span data-ttu-id="40e0c-125">TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="40e0c-125">TAPI 3.1</span></span>](./tapi-3-1-start-page.md)
</dt> </dl>

 

