---
description: Recuperación automática de recursos
ms.assetid: c889dd3f-82d1-4bc3-ac2c-6f468d5b2c7f
title: Recuperación automática de recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f76721df1a3858c9ad97d2f696115fff2eb6d3d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360057"
---
# <a name="automatic-resource-reclamation"></a><span data-ttu-id="398bd-103">Recuperación automática de recursos</span><span class="sxs-lookup"><span data-stu-id="398bd-103">Automatic Resource Reclamation</span></span>

<span data-ttu-id="398bd-104">COM+ notifica al administrador dispensador cada vez que finaliza la duración de un objeto.</span><span class="sxs-lookup"><span data-stu-id="398bd-104">COM+ notifies the dispenser manager each time an object's lifetime ends.</span></span> <span data-ttu-id="398bd-105">A continuación, el administrador de dispensadores notifica a cada titular de un dispensador de recursos registrados para ver si tiene algún recurso que todavía tenga este objeto.</span><span class="sxs-lookup"><span data-stu-id="398bd-105">The dispenser manager then notifies each registered resource dispenser's Holder to see whether it has any resources still held by this object.</span></span> <span data-ttu-id="398bd-106">Si es así, se liberan esos recursos, lo que evita la posibilidad de que se produzcan pérdidas de recursos por parte de los componentes que obtienen recursos a través de un dispensador de recursos.</span><span class="sxs-lookup"><span data-stu-id="398bd-106">If so, those resources are freed, preventing the possibility of resource leaks by components that get resources through a resource dispenser.</span></span>

<span data-ttu-id="398bd-107">La característica de recuperación automática es una opción que está desactivada de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="398bd-107">The auto-reclamation feature is an option that is turned off by default.</span></span> <span data-ttu-id="398bd-108">Un dispensador de recursos puede optar por habilitar esta opción y, al hacerlo, garantiza que los métodos de objeto nunca devuelven una referencia a los recursos dispensados en un objeto.</span><span class="sxs-lookup"><span data-stu-id="398bd-108">A resource dispenser can choose to enable this option and, in doing so, guarantees that a reference to any resource dispensed to an object is never returned by the object methods.</span></span>

## <a name="related-topics"></a><span data-ttu-id="398bd-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="398bd-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="398bd-110">Conceptos del dispensador de recursos COM+</span><span class="sxs-lookup"><span data-stu-id="398bd-110">COM+ Resource Dispenser Concepts</span></span>](com--resource-dispenser-concepts.md)
</dt> </dl>

 

 



