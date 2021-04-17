---
title: Qué puede saber y cuándo puede saberlo
description: Las aplicaciones que son sensibles a los Estados inducidos por latencia deben reconocer los Estados de los problemas y tomar las medidas adecuadas.
ms.assetid: d1d0135e-2d67-47dd-82ac-4869203ce85e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e9a8a6c6def8475946ad5faa63615d17742fbcb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105656213"
---
# <a name="what-can-you-know-and-when-can-you-know-it"></a><span data-ttu-id="3619b-103">¿Qué puede saber y cuándo puede saberlo?</span><span class="sxs-lookup"><span data-stu-id="3619b-103">What Can You Know, and When Can You Know It?</span></span>

<span data-ttu-id="3619b-104">Las aplicaciones que son sensibles a los Estados inducidos por latencia deben reconocer los Estados de los problemas y tomar las medidas adecuadas.</span><span class="sxs-lookup"><span data-stu-id="3619b-104">Applications that are sensitive to latency-induced states must recognize problem states and take appropriate action.</span></span> <span data-ttu-id="3619b-105">Hay dos Estados de problema: sesgo de versión y actualización parcial.</span><span class="sxs-lookup"><span data-stu-id="3619b-105">There are two problem states: version skew and partial update.</span></span> <span data-ttu-id="3619b-106">El sesgo de versiones no se detecta examinando el servicio de directorio (Recuerde el axioma de la informática distribuida que se indica en [qué Active Directory Domain Services usar este modelo de replicación](why-active-directory-domain-services-uses-this-replication-model.md)).</span><span class="sxs-lookup"><span data-stu-id="3619b-106">Version skew is not detectable by examining the Directory Service (remember the axiom of distributed computing stated in [Why Active Directory Domain Services Use This Replication Model](why-active-directory-domain-services-uses-this-replication-model.md)).</span></span> <span data-ttu-id="3619b-107">La actualización parcial se puede detectar agregando metadatos a los objetos que componen el conjunto relacionado.</span><span class="sxs-lookup"><span data-stu-id="3619b-107">Partial update can be detected by adding metadata to the objects that compose the related set.</span></span> <span data-ttu-id="3619b-108">En secciones posteriores de este documento aparecen sugerencias para estos metadatos.</span><span class="sxs-lookup"><span data-stu-id="3619b-108">Suggestions for such metadata appear in subsequent sections of this document.</span></span> <span data-ttu-id="3619b-109">Existen estrategias de prevención que las aplicaciones pueden tomar para reducir la posibilidad de que se produzcan sesgos de versiones y actualizaciones parciales.</span><span class="sxs-lookup"><span data-stu-id="3619b-109">There are avoidance strategies applications can take to reduce the possibility of both version skew and partial update.</span></span> <span data-ttu-id="3619b-110">Estas estrategias también se tratan en secciones posteriores de este documento.</span><span class="sxs-lookup"><span data-stu-id="3619b-110">These strategies are also discussed in subsequent sections of this document.</span></span>

 

 




