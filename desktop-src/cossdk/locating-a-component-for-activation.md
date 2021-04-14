---
description: Buscar un componente para la activación
ms.assetid: 2ba9484a-c646-4a35-8b32-268fe7a9520f
title: Buscar un componente para la activación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80bd90068c34469d61af36e6de8c409cb02e078c
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2021
ms.locfileid: "104552398"
---
# <a name="locating-a-component-for-activation"></a><span data-ttu-id="c4190-103">Buscar un componente para la activación</span><span class="sxs-lookup"><span data-stu-id="c4190-103">Locating a Component for Activation</span></span>

<span data-ttu-id="c4190-104">Cuando COM+ encuentra la partición correcta, a través del conjunto de particiones predeterminado de la identidad del usuario, un moniker de la partición o el identificador de la partición en el contexto del objeto, COM + debe localizar el componente correcto dentro de esa partición.</span><span class="sxs-lookup"><span data-stu-id="c4190-104">When COM+ has located the correct partition—through the user identity's default partition set, a partition moniker, or the partition ID in the object's context—COM+ must then locate the correct component within that partition.</span></span> <span data-ttu-id="c4190-105">En la ilustración siguiente se muestra cómo se encuentra y se activa un componente cuando ese componente reside en una partición.</span><span class="sxs-lookup"><span data-stu-id="c4190-105">The following illustration shows how a component is found and activated when that component resides in a partition.</span></span>

> [!Note]  
> <span data-ttu-id="c4190-106">Antes de cualquier activación de componentes, COM+ realiza una validación para comprobar que la identidad de usuario que intenta activar el componente tiene derechos de acceso al conjunto de particiones en el que reside el componente.</span><span class="sxs-lookup"><span data-stu-id="c4190-106">Prior to any component activation, COM+ performs a validation to verify that the user identity attempting to activate the component has rights to access the partition set in which the component resides.</span></span>

 

![Diagrama que muestra un árbol de solución de problemas para buscar un componente para la activación.](images/26c26a37-ec95-4f9f-aa59-4d84a7bb0fa3.png)

<span data-ttu-id="c4190-108">En la ilustración anterior se muestra lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="c4190-108">The preceding illustration shows the following:</span></span>

-   <span data-ttu-id="c4190-109">Si el componente que se está llamando reside en una partición y está en la misma aplicación que el componente que realiza la llamada, el componente se activa si el componente al que se llama está marcado como público o privado.</span><span class="sxs-lookup"><span data-stu-id="c4190-109">If the component being called resides in a partition and is in the same application as the calling component, the component is activated whether the component being called is marked as public or private.</span></span>
-   <span data-ttu-id="c4190-110">Si el componente al que se llama reside en una partición, pero no existe en la misma aplicación que el componente que realiza la llamada, COM+ comprueba para ver si el componente está marcado como público.</span><span class="sxs-lookup"><span data-stu-id="c4190-110">If the component being called resides in a partition but does not exist in the same application as the calling component, COM+ checks to see whether the component is marked as public.</span></span> <span data-ttu-id="c4190-111">Si no se encuentra ninguna versión pública, COM+ busca en la partición global para encontrar una versión pública del componente.</span><span class="sxs-lookup"><span data-stu-id="c4190-111">If no public version is found, COM+ searches the Global Partition to find a public version of the component.</span></span> <span data-ttu-id="c4190-112">Si no se encuentra ninguna versión pública del componente en la partición global o si la identidad del usuario no tiene derechos en la partición, se produce un error en la activación.</span><span class="sxs-lookup"><span data-stu-id="c4190-112">If no public version of the component is found in the Global Partition or if the user identity has no rights to the partition, the activation fails.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c4190-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c4190-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4190-114">Localizar particiones durante la activación</span><span class="sxs-lookup"><span data-stu-id="c4190-114">Locating Partitions During Activation</span></span>](locating-partitions-during-activation.md)
</dt> </dl>

 

 



