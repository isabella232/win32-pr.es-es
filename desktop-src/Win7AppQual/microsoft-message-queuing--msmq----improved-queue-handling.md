---
description: 'Microsoft Message Queuing (MSMQ): control mejorado de colas'
ms.assetid: 49bdfdfa-c77e-4a57-8079-bf4ff6b5010b
title: 'Microsoft Message Queuing (MSMQ): control mejorado de colas'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f7b7b00cfce68a183d7925f7cfab5ff7ab54b9b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088163"
---
# <a name="microsoft-message-queuing-msmq---improved-queue-handling"></a><span data-ttu-id="66c3c-103">Microsoft Message Queuing (MSMQ): control mejorado de colas</span><span class="sxs-lookup"><span data-stu-id="66c3c-103">Microsoft Message Queuing (MSMQ) - Improved Queue Handling</span></span>

## <a name="platforms"></a><span data-ttu-id="66c3c-104">Plataformas</span><span class="sxs-lookup"><span data-stu-id="66c3c-104">Platforms</span></span>

<span data-ttu-id="66c3c-105">**Clientes:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="66c3c-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="66c3c-106">**Servidores:** Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="66c3c-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="66c3c-107">Impacto en las características</span><span class="sxs-lookup"><span data-stu-id="66c3c-107">Feature Impact</span></span>

 <span data-ttu-id="66c3c-108">**Gravedad:** baja</span><span class="sxs-lookup"><span data-stu-id="66c3c-108">**Severity** - Low</span></span>  
<span data-ttu-id="66c3c-109">**Frecuencia:** baja</span><span class="sxs-lookup"><span data-stu-id="66c3c-109">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="66c3c-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="66c3c-110">Description</span></span>

<span data-ttu-id="66c3c-111">El servicio MSMQ no pone un límite máximo en el número de colas que se pueden crear en un sistema.</span><span class="sxs-lookup"><span data-stu-id="66c3c-111">MSMQ Service does not put a hard limit on the number of queues that can be created on a system.</span></span> <span data-ttu-id="66c3c-112">Sin embargo, el rendimiento del sistema se afecta cuando se crea un gran número de colas.</span><span class="sxs-lookup"><span data-stu-id="66c3c-112">However, the performance of the system is impacted when a large number of queues is created.</span></span> <span data-ttu-id="66c3c-113">En concreto, cuando hay más de unos miles de colas, el tiempo de inicio del servicio MSMQ aumenta exponencialmente, lo que provoca un impacto visible.</span><span class="sxs-lookup"><span data-stu-id="66c3c-113">Specifically, when there are more than a few thousand queues, the start-up time of the MSMQ Service increases exponentially resulting in a visible impact.</span></span>

<span data-ttu-id="66c3c-114">Microsoft ha optimizado el inicio del servicio MSMQ en Windows 7 para reducir la sobrecarga de búsqueda para cargar las colas en la memoria.</span><span class="sxs-lookup"><span data-stu-id="66c3c-114">Microsoft has optimized the MSMQ Service start-up in Windows 7 to reduce the lookup overhead for loading the queues into memory.</span></span> <span data-ttu-id="66c3c-115">Esta optimización ha llevado a una mejora considerable del tiempo de inicio del servicio MSMQ incluso cuando se crean varios miles de colas en el sistema.</span><span class="sxs-lookup"><span data-stu-id="66c3c-115">This optimization has led to a dramatic improvement of the start-up time of the MSMQ Service even when several thousand queues are created in the system.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="66c3c-116">Demostración del impacto</span><span class="sxs-lookup"><span data-stu-id="66c3c-116">Manifestation of Impact</span></span>

<span data-ttu-id="66c3c-117">Esta mejora del rendimiento no afecta a la funcionalidad de ninguna aplicación existente.</span><span class="sxs-lookup"><span data-stu-id="66c3c-117">This performance improvement does not impact the functionality of any existing application.</span></span>

## <a name="leveraging-the-changed-feature"></a><span data-ttu-id="66c3c-118">Aprovechamiento de la característica modificada</span><span class="sxs-lookup"><span data-stu-id="66c3c-118">Leveraging the Changed Feature</span></span>

<span data-ttu-id="66c3c-119">Los desarrolladores de aplicaciones que usan MSMQ en Windows 7 ahora pueden diseñar sus soluciones sin limitar el número de colas.</span><span class="sxs-lookup"><span data-stu-id="66c3c-119">Application developers using MSMQ on Windows 7 can now architect their solutions without limiting the number of queues.</span></span> <span data-ttu-id="66c3c-120">Tenga en cuenta que el número de colas sigue afectando al rendimiento general del servidor MSMQ, pero el impacto en el rendimiento se encuentra ahora en una escala lineal en lugar de exponencial.</span><span class="sxs-lookup"><span data-stu-id="66c3c-120">Note that the number of queues still affects overall performance of the MSMQ Server, but the performance impact is now on a linear rather than exponential scale.</span></span>

## <a name="compatibility-performance-reliability-and-usability-tests"></a><span data-ttu-id="66c3c-121">Pruebas de compatibilidad, rendimiento, confiabilidad y facilidad de uso</span><span class="sxs-lookup"><span data-stu-id="66c3c-121">Compatibility, Performance, Reliability, and Usability Tests</span></span>

<span data-ttu-id="66c3c-122">Si usa un gran número de colas, simule el entorno de producción en un nivel de prueba, supervise el rendimiento y analice el tiempo de inicio del servicio y el rendimiento del mensaje con un gran número de colas y mensajes presentes en el sistema de prueba.</span><span class="sxs-lookup"><span data-stu-id="66c3c-122">If you use a large number of queues, simulate the production environment on a test bed, monitor performance, and analyze the service start-up time and the message throughput with a large number of queues and messages present in the test system.</span></span>

 

 



