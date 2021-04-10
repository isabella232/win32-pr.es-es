---
description: Servicios COM+ sin componentes
ms.assetid: 5ef67411-334b-476e-b9b7-3677b24ab7df
title: Servicios COM+ sin componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1eeed5a9af96e241d137714d151cc632dd0f20e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153208"
---
# <a name="com-services-without-components"></a><span data-ttu-id="fd9bb-103">Servicios COM+ sin componentes</span><span class="sxs-lookup"><span data-stu-id="fd9bb-103">COM+ Services Without Components</span></span>

<span data-ttu-id="fd9bb-104">Con COM+ 1,5, puede usar los servicios proporcionados por COM+ sin necesidad de generar un componente que contenga los métodos que llaman a esos servicios.</span><span class="sxs-lookup"><span data-stu-id="fd9bb-104">With COM+ 1.5, you can use the services provided by COM+ without needing to build a component to contain the methods that call those services.</span></span> <span data-ttu-id="fd9bb-105">Esto beneficia a los desarrolladores que normalmente no usan componentes, sino que desean usar servicios COM+ como transacciones o el seguimiento de COM+.</span><span class="sxs-lookup"><span data-stu-id="fd9bb-105">This greatly benefits developers who do not normally use components but want to use COM+ services such as transactions or the COM+ Tracker.</span></span> <span data-ttu-id="fd9bb-106">Mediante el uso de servicios COM+ sin componentes, los desarrolladores pueden evitar la sobrecarga que supone crear un componente que se usa para tener acceso únicamente a los servicios COM+ que necesitan.</span><span class="sxs-lookup"><span data-stu-id="fd9bb-106">By using COM+ services without components, developers can avoid the overhead of creating a component that is used to access only the COM+ services they need.</span></span>

<span data-ttu-id="fd9bb-107">Por ejemplo, los entornos de scripts solían ser los mayores consumidores de los servicios COM+, pero nunca podían usar esos servicios de forma eficaz, ya que los servicios debían estar integrados en un componente de COM+.</span><span class="sxs-lookup"><span data-stu-id="fd9bb-107">For example, script environments traditionally have been the largest consumers of COM+ services but they were never able to use those services efficiently because the services needed to be bundled within a COM+ component.</span></span> <span data-ttu-id="fd9bb-108">Este requisito de agrupación aumentó los costos de rendimiento debido al aumento de la comunicación y la duplicación de los datos necesarios para que el entorno de scripting interactúe con el componente.</span><span class="sxs-lookup"><span data-stu-id="fd9bb-108">This bundling requirement increased performance costs because of the increased communication and duplication of data necessary for the scripting environment to interact with the component.</span></span> <span data-ttu-id="fd9bb-109">Al usar servicios sin componentes, se minimizan los costos.</span><span class="sxs-lookup"><span data-stu-id="fd9bb-109">By using services without components, such costs are minimized.</span></span>

<span data-ttu-id="fd9bb-110">En los temas que se describen en la tabla siguiente se proporciona información básica y de tareas sobre el uso de servicios COM+ sin componentes.</span><span class="sxs-lookup"><span data-stu-id="fd9bb-110">The topics described in the following table provide background and task information about using COM+ services without components.</span></span> <span data-ttu-id="fd9bb-111">Esta característica está pensada para los programadores de Visual C++ avanzados que preocupan del rendimiento.</span><span class="sxs-lookup"><span data-stu-id="fd9bb-111">This feature is intended for advanced Visual C++ developers who are concerned about performance.</span></span>



| <span data-ttu-id="fd9bb-112">Tema</span><span class="sxs-lookup"><span data-stu-id="fd9bb-112">Topic</span></span>                                                                                                 | <span data-ttu-id="fd9bb-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="fd9bb-113">Description</span></span>                                                                                    |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fd9bb-114">Conceptos de servicios COM+ sin componentes</span><span class="sxs-lookup"><span data-stu-id="fd9bb-114">COM+ Services Without Components Concepts</span></span>](com--services-without-components-concepts.md)<br/> | <span data-ttu-id="fd9bb-115">Proporciona información general sobre el uso de servicios COM+ sin componentes.</span><span class="sxs-lookup"><span data-stu-id="fd9bb-115">Provides an overview of using COM+ services without components.</span></span><br/>                     |
| [<span data-ttu-id="fd9bb-116">Servicios COM+ sin tareas de componentes</span><span class="sxs-lookup"><span data-stu-id="fd9bb-116">COM+ Services Without Components Tasks</span></span>](com--services-without-components-tasks.md)<br/>       | <span data-ttu-id="fd9bb-117">Proporciona instrucciones para usar COM+ con el fin de crear y usar servicios sin componentes.</span><span class="sxs-lookup"><span data-stu-id="fd9bb-117">Provides instructions for using COM+ to create and use services without components.</span></span><br/> |



 

 

 




