---
description: Implementación para una comunicación más rápida
ms.assetid: 9099f9df-b620-4623-826e-c541202ebc4a
title: Implementación para una comunicación más rápida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2594a7dbd34813013257350e2deb9d93db6bae5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677244"
---
# <a name="deploying-for-faster-communication"></a><span data-ttu-id="a2095-103">Implementación para una comunicación más rápida</span><span class="sxs-lookup"><span data-stu-id="a2095-103">Deploying for Faster Communication</span></span>

<span data-ttu-id="a2095-104">El rendimiento es una consideración importante a la hora de implementar una aplicación COM+ y la ubicación del componente es la clave para obtener el mejor rendimiento de una aplicación bien diseñada.</span><span class="sxs-lookup"><span data-stu-id="a2095-104">Performance is a key consideration when deploying a COM+ application, and component location is the key to getting the best performance from a well-designed application.</span></span>

<span data-ttu-id="a2095-105">Una vez que se mantuvo con arquitecturas de aplicaciones escalables, el rendimiento se podía solucionar simplemente moviendo los componentes principales de la aplicación a un hardware más rápido.</span><span class="sxs-lookup"><span data-stu-id="a2095-105">It was once widely held that with scalable application architectures, performance could be addressed by simply moving primary components of the application to faster hardware.</span></span> <span data-ttu-id="a2095-106">Esto ha demostrado que no es cierto.</span><span class="sxs-lookup"><span data-stu-id="a2095-106">This has proven not to be true.</span></span> <span data-ttu-id="a2095-107">Los problemas de rendimiento no se producen desde el rendimiento de los componentes individuales, sino desde los vínculos que conectan los componentes.</span><span class="sxs-lookup"><span data-stu-id="a2095-107">Performance problems arise not from individual component performance but from the links connecting components.</span></span>

<span data-ttu-id="a2095-108">El factor principal para el éxito es la ubicación.</span><span class="sxs-lookup"><span data-stu-id="a2095-108">The primary factor for success is location.</span></span> <span data-ttu-id="a2095-109">La ubicación física o la proximidad, la hora, la capacidad y el propósito son distintos aspectos de la ubicación que se aplican a la implementación de una aplicación COM+, lo que afecta al rendimiento.</span><span class="sxs-lookup"><span data-stu-id="a2095-109">Proximity or physical location, time, capacity, and purpose are distinct aspects of location that apply to the deployment of a COM+ application, all of which affect performance.</span></span>

<span data-ttu-id="a2095-110">El mejor rendimiento se produce cuando se diseñan e implementan los componentes y los recursos de la aplicación para que coincidan con las demandas aplicadas por la carga de trabajo de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a2095-110">The best performance comes when the application components and resources are designed and deployed to match the demands placed upon them by the application workload.</span></span>

<span data-ttu-id="a2095-111">En general, debe implementar los componentes para minimizar la comunicación entre los componentes y el proceso entre los distintos procesos.</span><span class="sxs-lookup"><span data-stu-id="a2095-111">In general, you should deploy components to minimize cross-process, and especially cross-computer, communication between components.</span></span> <span data-ttu-id="a2095-112">Si el diseño de la aplicación es eficaz, las clases de un componente se agrupan por uso y función para maximizar las comunicaciones dentro de los componentes.</span><span class="sxs-lookup"><span data-stu-id="a2095-112">If your application design is efficient, classes within a component are grouped by use and function to maximize communications within components.</span></span> <span data-ttu-id="a2095-113">En la implementación de componentes, debe asegurarse de que los componentes están ubicados lógicamente para hacer uso de las relaciones entre los componentes y reducir la cantidad de mensajería entre los componentes.</span><span class="sxs-lookup"><span data-stu-id="a2095-113">In deploying components, you need to ensure that the components are logically located to make use of the relationships between the components and to reduce the amount of messaging between components.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a2095-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a2095-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2095-115">Diseñar para la implementación</span><span class="sxs-lookup"><span data-stu-id="a2095-115">Designing for Deployment</span></span>](designing-for-deployment.md)
</dt> </dl>

 

 



