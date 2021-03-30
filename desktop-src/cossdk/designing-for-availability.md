---
description: La disponibilidad es la capacidad de una aplicación para tolerar errores en los recursos del servidor.
ms.assetid: 5d9a8216-a568-4443-b94f-1b2f2827a4be
title: Diseño para disponibilidad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 222583c9f53a1ccc88f2a4f984f445de02a2c976
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538812"
---
# <a name="designing-for-availability"></a><span data-ttu-id="2a8b9-103">Diseño para disponibilidad</span><span class="sxs-lookup"><span data-stu-id="2a8b9-103">Designing for Availability</span></span>

<span data-ttu-id="2a8b9-104">La disponibilidad es la capacidad de una aplicación para tolerar errores en los recursos del servidor.</span><span class="sxs-lookup"><span data-stu-id="2a8b9-104">Availability is the ability of an application to tolerate failures in server resources.</span></span> <span data-ttu-id="2a8b9-105">Esto significa que el cliente sigue atendiendo a través del error y que, idealmente, el error es transparente para el cliente.</span><span class="sxs-lookup"><span data-stu-id="2a8b9-105">This means that the client continues to be served through the failure and that, ideally, the failure is transparent to the client.</span></span> <span data-ttu-id="2a8b9-106">Obviamente, el error puede proviene de orígenes de hardware o software, por lo que debe desarrollar para ambos casos.</span><span class="sxs-lookup"><span data-stu-id="2a8b9-106">Obviously, the failure can come from either hardware or software sources, so you must develop for both cases.</span></span>

<span data-ttu-id="2a8b9-107">La disponibilidad puede verse afectada por los siguientes factores:</span><span class="sxs-lookup"><span data-stu-id="2a8b9-107">Availability can be affected by the following factors:</span></span>

-   <span data-ttu-id="2a8b9-108">Modelo de aplicación.</span><span class="sxs-lookup"><span data-stu-id="2a8b9-108">Application model.</span></span> <span data-ttu-id="2a8b9-109">Para obtener la máxima disponibilidad, asegúrese de que la lógica de la aplicación crítica se realiza mediante el servicio de [transacciones de com+](com--transactions.md) .</span><span class="sxs-lookup"><span data-stu-id="2a8b9-109">For highest availability, ensure that the critical application logic is conducted using the [COM+ transactions](com--transactions.md) service.</span></span> <span data-ttu-id="2a8b9-110">Además, el uso de un mecanismo de compensación puede ser eficaz para garantizar que los recursos permanecen en un estado correcto después de los errores.</span><span class="sxs-lookup"><span data-stu-id="2a8b9-110">In addition, using a compensation mechanism can be effective in ensuring that resources remain in a healthy state after failures.</span></span>
-   <span data-ttu-id="2a8b9-111">Modelo de cliente.</span><span class="sxs-lookup"><span data-stu-id="2a8b9-111">Client model.</span></span> <span data-ttu-id="2a8b9-112">Integre la lógica de "reintento en caso de error" en la aplicación cliente y procurar una degradación correcta en la aplicación si los recursos o servicios no están disponibles.</span><span class="sxs-lookup"><span data-stu-id="2a8b9-112">Integrate "retry on failure" logic into the client application, and strive for a graceful degradation in the application if resources or services are unavailable.</span></span> <span data-ttu-id="2a8b9-113">Comprenda lo que el cliente espera de la aplicación y cree un diseño que permita alternativas cuando se produce un error.</span><span class="sxs-lookup"><span data-stu-id="2a8b9-113">Understand what the client is expecting from the application, and create a design that allows for alternatives when a failure occurs.</span></span>
-   <span data-ttu-id="2a8b9-114">Disponibilidad de datos y estado.</span><span class="sxs-lookup"><span data-stu-id="2a8b9-114">Data/state availability.</span></span> <span data-ttu-id="2a8b9-115">Para obtener acceso coherente a los datos persistentes, utilice la organización por clústeres de Windows para proporcionar compatibilidad con la conmutación por error.</span><span class="sxs-lookup"><span data-stu-id="2a8b9-115">For consistent access to persistent data, use Windows Clustering to provide failover support.</span></span>
-   <span data-ttu-id="2a8b9-116">Disponibilidad del servicio.</span><span class="sxs-lookup"><span data-stu-id="2a8b9-116">Service availability.</span></span> <span data-ttu-id="2a8b9-117">Puede usar el equilibrio de carga de red para equilibrar la carga de las solicitudes IP entrantes a través de un clúster de servidores.</span><span class="sxs-lookup"><span data-stu-id="2a8b9-117">You can use Network Load Balancing to load balance incoming IP requests across a cluster of servers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2a8b9-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2a8b9-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a8b9-119">Diseñar para la implementación</span><span class="sxs-lookup"><span data-stu-id="2a8b9-119">Designing for Deployment</span></span>](designing-for-deployment.md)
</dt> <dt>

[<span data-ttu-id="2a8b9-120">Diseño para la escalabilidad</span><span class="sxs-lookup"><span data-stu-id="2a8b9-120">Designing for Scalability</span></span>](designing-for-scalability.md)
</dt> <dt>

[<span data-ttu-id="2a8b9-121">Diseñar para la seguridad</span><span class="sxs-lookup"><span data-stu-id="2a8b9-121">Designing for Security</span></span>](designing-for-security.md)
</dt> </dl>

 

 



