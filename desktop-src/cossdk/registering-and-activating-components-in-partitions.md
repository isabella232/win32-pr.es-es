---
description: Registro y activación de componentes en particiones
ms.assetid: 2cca71da-c7f7-4997-b63a-74ba266e9e95
title: Registro y activación de componentes en particiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31790bc9a3df12d961a4b16271937ae22f963c38
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538800"
---
# <a name="registering-and-activating-components-in-partitions"></a><span data-ttu-id="ba0d3-103">Registro y activación de componentes en particiones</span><span class="sxs-lookup"><span data-stu-id="ba0d3-103">Registering and Activating Components in Partitions</span></span>

<span data-ttu-id="ba0d3-104">Después de crear una partición, el siguiente paso es registrar los componentes COM+ en esa partición.</span><span class="sxs-lookup"><span data-stu-id="ba0d3-104">After a partition has been created, the next step is register your COM+ components within that partition.</span></span> <span data-ttu-id="ba0d3-105">Un componente se registra en una partición cuando se crea una nueva aplicación COM+ o cuando se instala una aplicación COM+ existente en la partición.</span><span class="sxs-lookup"><span data-stu-id="ba0d3-105">A component is registered within a partition when a new COM+ application is created or when an existing COM+ application is installed into the partition.</span></span> <span data-ttu-id="ba0d3-106">Para facilitar la administración del registro cuando varias particiones contienen los mismos componentes COM+, el servicio particiones permite a un administrador copiar aplicaciones o componentes de una partición a otra.</span><span class="sxs-lookup"><span data-stu-id="ba0d3-106">To ease the administration of registration when multiple partitions contain the same COM+ components, the partitions service allows an administrator to copy applications or components from one partition into another.</span></span> <span data-ttu-id="ba0d3-107">Cuando se copia una aplicación COM+ o un componente, se copian todas las propiedades de la partición asociadas, excepto la identidad de la aplicación o cualquiera de los miembros de un rol.</span><span class="sxs-lookup"><span data-stu-id="ba0d3-107">When a COM+ application or a component is copied, all associated partition properties are copied with it, except the application's identity or any of the members of a role.</span></span>

<span data-ttu-id="ba0d3-108">Cuando el programa cliente llama a la función [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) o [**CoGetObject**](/windows/desktop/api/objbase/nf-objbase-cogetobject) para crear instancias de un objeto, com+ realiza dos pasos distintos, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="ba0d3-108">When the client program calls the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) or [**CoGetObject**](/windows/desktop/api/objbase/nf-objbase-cogetobject) function to instantiate an object, COM+ performs two distinct steps, as follows:</span></span>

1.  <span data-ttu-id="ba0d3-109">Busca la partición en la que reside el componente</span><span class="sxs-lookup"><span data-stu-id="ba0d3-109">Locates the partition in which the component resides</span></span>
2.  <span data-ttu-id="ba0d3-110">Busca el componente correcto dentro de esa partición.</span><span class="sxs-lookup"><span data-stu-id="ba0d3-110">Locates the correct component within that partition</span></span>

<span data-ttu-id="ba0d3-111">En los siguientes temas de esta sección se describen estos pasos con detalle:</span><span class="sxs-lookup"><span data-stu-id="ba0d3-111">The following topics in this section describe these steps in detail:</span></span>

-   [<span data-ttu-id="ba0d3-112">Localizar particiones durante la activación</span><span class="sxs-lookup"><span data-stu-id="ba0d3-112">Locating Partitions During Activation</span></span>](locating-partitions-during-activation.md)
-   [<span data-ttu-id="ba0d3-113">Buscar un componente para la activación</span><span class="sxs-lookup"><span data-stu-id="ba0d3-113">Locating a Component for Activation</span></span>](locating-a-component-for-activation.md)

## <a name="related-topics"></a><span data-ttu-id="ba0d3-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ba0d3-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba0d3-115">Restricciones de diseño de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="ba0d3-115">Application Design Restrictions</span></span>](application-design-restrictions.md)
</dt> <dt>

[<span data-ttu-id="ba0d3-116">Particiones y componentes en cola de COM+</span><span class="sxs-lookup"><span data-stu-id="ba0d3-116">COM+ Queued Components and Partitions</span></span>](com--queued-components-and-partitions.md)
</dt> <dt>

[<span data-ttu-id="ba0d3-117">Implementación de particiones</span><span class="sxs-lookup"><span data-stu-id="ba0d3-117">Partition Implementation</span></span>](partition-implementation.md)
</dt> <dt>

[<span data-ttu-id="ba0d3-118">¿Qué son las particiones COM+?</span><span class="sxs-lookup"><span data-stu-id="ba0d3-118">What Are COM+ Partitions?</span></span>](what-are-com--partitions-.md)
</dt> </dl>

 

 
