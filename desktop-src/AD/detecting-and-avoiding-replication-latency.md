---
title: Detección y prevención de la latencia de replicación
description: La latencia de replicación es un hecho de vida en un sistema distribuido de acoplamiento flexible.
ms.assetid: ea65759b-2bfa-4859-8d2a-5949bbb9adef
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 271b4d84689068824a6e46095a5ed93462f49e2f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773255"
---
# <a name="detecting-and-avoiding-replication-latency"></a><span data-ttu-id="57638-103">Detección y prevención de la latencia de replicación</span><span class="sxs-lookup"><span data-stu-id="57638-103">Detecting and Avoiding Replication Latency</span></span>

<span data-ttu-id="57638-104">La latencia de replicación es un hecho de vida en un sistema distribuido de acoplamiento flexible.</span><span class="sxs-lookup"><span data-stu-id="57638-104">Replication latency is a fact of life in a loosely coupled distributed system.</span></span> <span data-ttu-id="57638-105">Las aplicaciones deben adaptarse a este.</span><span class="sxs-lookup"><span data-stu-id="57638-105">Applications must accommodate this.</span></span> <span data-ttu-id="57638-106">La mejor manera de adaptarse a la latencia de replicación es diseñar aplicaciones para minimizar los efectos.</span><span class="sxs-lookup"><span data-stu-id="57638-106">The best way to accommodate replication latency is to design applications to minimize the effects.</span></span> <span data-ttu-id="57638-107">La aplicación ideal habilitada para el directorio:</span><span class="sxs-lookup"><span data-stu-id="57638-107">The ideal directory-enabled application:</span></span>

-   <span data-ttu-id="57638-108">No distingue el sesgo de la versión.</span><span class="sxs-lookup"><span data-stu-id="57638-108">Is insensitive to version skew.</span></span>
-   <span data-ttu-id="57638-109">No depende de las relaciones entre varios objetos.</span><span class="sxs-lookup"><span data-stu-id="57638-109">Does not depend on relationships among multiple objects.</span></span>
-   <span data-ttu-id="57638-110">No tiene ningún requisito de coherencia entre objetos.</span><span class="sxs-lookup"><span data-stu-id="57638-110">Has no intra- or inter-object consistency requirements.</span></span>

<span data-ttu-id="57638-111">No es necesario que las aplicaciones y los servicios que se ajustan a este perfil afecten a la latencia de replicación.</span><span class="sxs-lookup"><span data-stu-id="57638-111">Applications and services that fit this profile need not be concerned with replication latency.</span></span> <span data-ttu-id="57638-112">Otras aplicaciones deben diseñarse teniendo en cuenta la latencia de replicación.</span><span class="sxs-lookup"><span data-stu-id="57638-112">Other applications must be designed with replication latency in mind.</span></span> <span data-ttu-id="57638-113">La clave para el éxito en el diseño de una aplicación de este tipo es el conocimiento del proceso de replicación.</span><span class="sxs-lookup"><span data-stu-id="57638-113">The key to success in designing such an application is awareness of the replication process.</span></span> <span data-ttu-id="57638-114">Pasos que se llevan a cabo en el tiempo de diseño para reducir las dependencias entre objetos y minimizar las ventanas de actualización parciales pagará grandes dividendos en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="57638-114">Steps taken at design time to reduce inter-object dependencies and minimize partial update windows will pay large dividends at run time.</span></span> <span data-ttu-id="57638-115">Los enfoques para tratar con la latencia de replicación se dividen en dos clases: evitar estrategias que reducen el impacto de la latencia y las estrategias de detección que permiten a una aplicación detectar Estados inducidos por latencia.</span><span class="sxs-lookup"><span data-stu-id="57638-115">Approaches to dealing with replication latency are divided into two classes—avoidance strategies that reduce the impact of latency and detection strategies that allow an application to detect latency-induced states.</span></span>

 

 




